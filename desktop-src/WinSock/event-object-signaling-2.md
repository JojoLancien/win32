---
Description: WSPEventSelect behaves exactly like WSPAsyncSelect except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Event Object Signaling
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Event Object Signaling

[**WSPEventSelect**](/windows/desktop/api/Ws2spi/) behaves exactly like [**WSPAsyncSelect**](/windows/desktop/api/Ws2spi/) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.

Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider. This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled. A call to [**WSPEnumNetworkEvents**](/windows/desktop/api/Ws2spi/) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared. The client may also designate a particular event object to be cleared atomically along with the network event memory.

 

 



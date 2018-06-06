---
Description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
Robots: noindex, nofollow
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.prod: windows-server-dev
ms.technology: windows-management-instrumentation
ms.tgt_platform: multiple
title: E
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# E

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**
</dt> <dd>

A WMI class that *event consumers* can subscribe to by an *event query*. The class reports a specific type of occurrence. For example, the [**Win32\_ProcessStopTrace**](https://msdn.microsoft.com/library/aa394376) class reports that a specific process has stopped.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**
</dt> <dd>

A recipient of notifications that report an occurrence of an event. An event consumer is either [*temporary*](gloss-t.md#wmi-gloss-temporary-consumer) or [*permanent*](gloss-p.md#wmi-gloss-permanent-consumer).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**
</dt> <dd>

A provider that determines which permanent event consumer handles a given event. An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md#wmi-gloss-logical-consumer) classes that the event consumer provider supports. An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md#wmi-gloss-physical-consumer) to *logical consumers*. An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**
</dt> <dd>

An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification. A consumer uses an event filter to register to receive notification of a specific type of event.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**
</dt> <dd>

A WMI provider that monitors a source of events and notifies WMI when events occur. An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**
</dt> <dd>

A [*WMI Query Language*](gloss-w.md#wmi-gloss-wmi-query-language) statement that event consumers use to register to receive notification of specific events. An event provider uses an event query to register to generate notifications of specific events.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**
</dt> <dd>

The third layer of the [*CIM schema*](gloss-c.md#wmi-gloss-cim-schema), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server. Also see [*common model*](gloss-c.md#wmi-gloss-common-model) and core model.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**
</dt> <dd>

An event notification from a provider. Most providers create an instance of an event class defined in the provider MOF files. An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md). For example, the [Event Log Provider](https://msdn.microsoft.com/library/aa390413) defines the event class [**Win32\_NTLogEvent**](https://msdn.microsoft.com/library/aa394226). Also see [*intrinsic event*](gloss-i.md#wmi-gloss-intrinsic-event).

</dd> </dl>

 

 



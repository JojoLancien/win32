---
Description: Builds a customized, left-handed perspective projection matrix.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- D3DXMatrixPerspectiveOffCenterLH
api_type: 
- LibDef
api_location: 
- d3dx9.lib
- d3dx9.dll
---

# D3DXMatrixPerspectiveOffCenterLH function

Builds a customized, left-handed perspective projection matrix.

## Syntax


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## Parameters

<dl> <dt>

*pOut* \[in, out\]
</dt> <dd>

Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***

Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.

</dd> <dt>

*l* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Minimum x-value of the view volume.

</dd> <dt>

*r* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Maximum x-value of the view volume.

</dd> <dt>

*b* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Minimum y-value of the view volume.

</dd> <dt>

*t* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Maximum y-value of the view volume.

</dd> <dt>

*zn* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Minimum z-value of the view volume.

</dd> <dt>

*zf* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Maximum z-value of the view volume.

</dd> </dl>

## Return value

Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***

Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.

## Remarks

All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space. The parameters describe the dimensions of the view volume.

The return value for this function is the same value returned in the *pOut* parameter. In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.

This function uses the following formula to compute the returned matrix.


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Math Functions](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 





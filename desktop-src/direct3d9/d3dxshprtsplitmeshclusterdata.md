---
description: D3DXSHPRTSPLITMESHCLUSTERDATA 結構
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: 'D3DXSHPRTSPLITMESHCLUSTERDATA 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: c4405b383e0403326c3cb84f43c97f4c7da826872b62cb21c94b3edb9ef0e475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298287"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a>D3DXSHPRTSPLITMESHCLUSTERDATA 結構

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**uVertStart**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

重新對應頂點陣列的初始頂點。

</dd> <dt>

**uVertLength**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此 supercluster 中的頂點數目。

</dd> <dt>

**uFaceStart**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

臉部陣列的初始索引。

</dd> <dt>

**uFaceLength**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此 supercluster 中的臉部數目。

</dd> <dt>

**uClusterStart**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

群集陣列的初始索引。

</dd> <dt>

**uClusterLength**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

這個 supercluster 陣列中的群集數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 

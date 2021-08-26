---
description: D3DXSHPRTSPLITMESHVERTDATA 結構
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: 'D3DXSHPRTSPLITMESHVERTDATA 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: cc32ee70cd1685351f8cca8860d9d45ab4ea597affed2fbe7cf078d44a8ed437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027058"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a>D3DXSHPRTSPLITMESHVERTDATA 結構

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**uVertRemap**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始網格中對應的頂點。

</dd> <dt>

**uSubCluster**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

相對於 supercluster 的叢集索引。

</dd> <dt>

**ucVertStatus**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

如果頂點具有有效的資料，則為1，如果是「完整」，則為0。

</dd> </dl>

## <a name="remarks"></a>備註

配置於 [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

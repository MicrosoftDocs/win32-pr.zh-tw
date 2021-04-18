---
description: 網格資料結構。
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: 'D3DXMESHDATA 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322647"
---
# <a name="d3dxmeshdata-structure"></a>D3DXMESHDATA 結構

網格資料結構。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

類型： **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

定義網格資料類型。 請參閱 [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)。

</dd> <dt>

**pMesh**
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

網格的指標。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> <dt>

**pPatchMesh**
</dt> <dd>

類型： **LPD3DXPATCHMESH**

</dd> <dd>

修補程式網格的指標。 請參閱 [**ID3DXPatchMesh**](id3dxpatchmesh.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 

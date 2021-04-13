---
description: 封裝轉換框架階層中的網格物件。
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: 'D3DXMESHCONTAINER 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322648"
---
# <a name="d3dxmeshcontainer-structure"></a>D3DXMESHCONTAINER 結構

封裝轉換框架階層中的網格物件。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **LPSTR**

</dd> <dd>

網格名稱。

</dd> <dt>

**MeshData**
</dt> <dd>

類型： **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

網格中的資料類型。 請參閱 [**D3DXMESHDATA**](d3dxmeshdata.md)。

</dd> <dt>

**pMaterials**
</dt> <dd>

類型： **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

網格材質的陣列。 請參閱 [**D3DXMATERIAL**](d3dxmaterial.md)。

</dd> <dt>

**pEffects**
</dt> <dd>

類型： **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

一組預設效果參數的指標。 請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。

</dd> <dt>

**NumMaterials**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

網格中的材質數目。

</dd> <dt>

**pAdjacency**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

包含相鄰資訊之網格的每個三角形的陣列指標。

</dd> <dt>

**pSkinInfo**
</dt> <dd>

類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

外觀資訊介面的指標。 請參閱 [**ID3DXSkinInfo**](id3dxskininfo.md)。

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

類型： * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

下一個網格容器的指標。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式可以從此結構衍生，以新增其他資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

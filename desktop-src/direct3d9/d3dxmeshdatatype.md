---
description: 定義存在於 D3DXMESHDATA 中的網格資料類型。
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: 'D3DXMESHDATATYPE 列舉 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985884"
---
# <a name="d3dxmeshdatatype-enumeration"></a>D3DXMESHDATATYPE 列舉

定義存在於 [**D3DXMESHDATA**](d3dxmeshdata.md)中的網格資料類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE \_ 網格**
</dt> <dd>

資料類型是網格。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> <dt>

<span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ PATCHMESH**
</dt> <dd>

資料類型是修補程式網格。 請參閱 [**ID3DXPatchMesh**](id3dxpatchmesh.md)。

</dd> <dt>

<span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXMESHDATA**](d3dxmeshdata.md)
</dt> </dl>

 

 





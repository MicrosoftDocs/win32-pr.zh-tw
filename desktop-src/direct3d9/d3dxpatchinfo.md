---
description: 結構，其中包含 patch 網狀架構的屬性。
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: 'D3DXPATCHINFO 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322635"
---
# <a name="d3dxpatchinfo-structure"></a>D3DXPATCHINFO 結構

結構，其中包含 patch 網狀架構的屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**PatchType**
</dt> <dd>

類型： **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

修補類型。 如需修補程式類型的詳細資訊，請參閱 [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)。

</dd> <dt>

**角度**
</dt> <dd>

類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

用來建立修補程式的曲線程度。 如需所支援之度數的詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。

</dd> <dt>

**Basis**
</dt> <dd>

類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

用來建立修補程式的曲線類型。 如需支援之基礎類型的詳細資訊，請參閱 [**D3DBASISTYPE**](./d3dbasistype.md)。

</dd> </dl>

## <a name="remarks"></a>備註

網格是一組臉部，每個臉部都由一個簡單的多邊形描述。 您可以將數個網格連接在一起來建立物件。 修補程式網格是由修補程式所構成。 Patch 是從曲線構成的四側幾何。 使用的曲線類型和曲線的順序可能會不同，因此 patch 介面幾乎可以容納任何介面圖形。

支援下列類型的 patch 組合：



| 修補類型 | 基礎       | 角度 |
|------------|-------------|--------|
| 矩形  | 貝茲      | 2，3，5  |
| 矩形  | B-曲線    | 2，3，5  |
| 矩形  | Catmull-Rom | 3      |
| Triangle   | 貝茲      | 2，3，5  |
| N-修補程式    | N/A         | 3      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)
</dt> <dt>

[**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 

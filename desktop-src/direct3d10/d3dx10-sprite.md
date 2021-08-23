---
description: 定義 sprite 的位置、材質和色彩資訊。
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: 'D3DX10_SPRITE 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ec8b220d55d3ac55d2a8b68fa3b95398a395611da150235d03314114055214e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753508"
---
# <a name="d3dx10_sprite-structure"></a>D3DX10 \_ SPRITE 結構

定義 sprite 的位置、材質和色彩資訊。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>成員

<dl> <dt>

**matWorld**
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Sprite 的模型世界轉換。 這會定義世界空間中 sprite 的位置和方向。

</dd> <dt>

**TexCoord**
</dt> <dd>

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

從材質左上角算起的位移，表示 sprite 影像在材質中的開始位置。 **TexCoord** 是以材質座標表示。

</dd> <dt>

**TexSize**
</dt> <dd>

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

向量，包含材質座標中 sprite 的寬度和高度。

</dd> <dt>

**ColorModulate**
</dt> <dd>

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

將在轉譯之前乘以圖元色彩的色彩。

</dd> <dt>

**pTexture**
</dt> <dd>

類型： **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

著色器資源檢視的指標，代表 sprite 的材質。 請參閱 [**ID3D10ShaderResourceView 介面**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)。

</dd> <dt>

**TextureIndex**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質的索引。 如果 pTexture 不代表材質陣列，則這應該是0。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

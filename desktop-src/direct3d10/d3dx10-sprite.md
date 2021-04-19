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
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989219"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="a1428-103">D3DX10 \_ SPRITE 結構</span><span class="sxs-lookup"><span data-stu-id="a1428-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="a1428-104">定義 sprite 的位置、材質和色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="a1428-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1428-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1428-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a1428-106">成員</span><span class="sxs-lookup"><span data-stu-id="a1428-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1428-107">**matWorld**</span><span class="sxs-lookup"><span data-stu-id="a1428-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="a1428-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1428-109">Sprite 的模型世界轉換。</span><span class="sxs-lookup"><span data-stu-id="a1428-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="a1428-110">這會定義世界空間中 sprite 的位置和方向。</span><span class="sxs-lookup"><span data-stu-id="a1428-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="a1428-111">**TexCoord**</span><span class="sxs-lookup"><span data-stu-id="a1428-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-112">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="a1428-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1428-113">從材質左上角算起的位移，表示 sprite 影像在材質中的開始位置。</span><span class="sxs-lookup"><span data-stu-id="a1428-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="a1428-114">**TexCoord** 是以材質座標表示。</span><span class="sxs-lookup"><span data-stu-id="a1428-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a1428-115">**TexSize**</span><span class="sxs-lookup"><span data-stu-id="a1428-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-116">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="a1428-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1428-117">向量，包含材質座標中 sprite 的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="a1428-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a1428-118">**ColorModulate**</span><span class="sxs-lookup"><span data-stu-id="a1428-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-119">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a1428-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1428-120">將在轉譯之前乘以圖元色彩的色彩。</span><span class="sxs-lookup"><span data-stu-id="a1428-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="a1428-121">**pTexture**</span><span class="sxs-lookup"><span data-stu-id="a1428-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-122">類型： **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="a1428-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="a1428-123">著色器資源檢視的指標，代表 sprite 的材質。</span><span class="sxs-lookup"><span data-stu-id="a1428-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="a1428-124">請參閱 [**ID3D10ShaderResourceView 介面**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)。</span><span class="sxs-lookup"><span data-stu-id="a1428-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="a1428-125">**TextureIndex**</span><span class="sxs-lookup"><span data-stu-id="a1428-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a1428-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1428-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1428-127">材質的索引。</span><span class="sxs-lookup"><span data-stu-id="a1428-127">The index of the texture.</span></span> <span data-ttu-id="a1428-128">如果 pTexture 不代表材質陣列，則這應該是0。</span><span class="sxs-lookup"><span data-stu-id="a1428-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1428-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1428-129">Requirements</span></span>



| <span data-ttu-id="a1428-130">需求</span><span class="sxs-lookup"><span data-stu-id="a1428-130">Requirement</span></span> | <span data-ttu-id="a1428-131">值</span><span class="sxs-lookup"><span data-stu-id="a1428-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1428-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a1428-132">Header</span></span><br/> | <dl> <span data-ttu-id="a1428-133"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1428-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1428-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1428-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1428-135">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="a1428-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

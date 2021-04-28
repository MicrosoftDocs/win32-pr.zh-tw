---
description: D3DXFillVolumeTextureTX 函式-使用編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: 'D3DXFillVolumeTextureTX 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30aac53aa6451885bbd4ae2cac63050b01157974
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107626"
---
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="0fcee-103">D3DXFillVolumeTextureTX 函式</span><span class="sxs-lookup"><span data-stu-id="0fcee-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="0fcee-104">使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。</span><span class="sxs-lookup"><span data-stu-id="0fcee-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcee-105">語法</span><span class="sxs-lookup"><span data-stu-id="0fcee-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="0fcee-106">參數</span><span class="sxs-lookup"><span data-stu-id="0fcee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcee-107">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0fcee-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fcee-108">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="0fcee-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="0fcee-109">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)物件的指標，代表要填滿的材質。</span><span class="sxs-lookup"><span data-stu-id="0fcee-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="0fcee-110">*pTextureShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0fcee-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fcee-111">類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="0fcee-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="0fcee-112">[**ID3DXTextureShader**](id3dxtextureshader.md)紋理著色器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0fcee-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fcee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fcee-113">Return value</span></span>

<span data-ttu-id="0fcee-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0fcee-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0fcee-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0fcee-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0fcee-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0fcee-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fcee-117">備註</span><span class="sxs-lookup"><span data-stu-id="0fcee-117">Remarks</span></span>

<span data-ttu-id="0fcee-118">紋理目標必須是 HLSL 函式，且此函式會包含下列語義：</span><span class="sxs-lookup"><span data-stu-id="0fcee-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="0fcee-119">一個輸入參數必須使用位置語義。</span><span class="sxs-lookup"><span data-stu-id="0fcee-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="0fcee-120">一個輸入參數必須使用 PSIZE 語義。</span><span class="sxs-lookup"><span data-stu-id="0fcee-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="0fcee-121">函數必須傳回使用色彩語義的參數。</span><span class="sxs-lookup"><span data-stu-id="0fcee-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="0fcee-122">輸入參數可以依任何順序排列。</span><span class="sxs-lookup"><span data-stu-id="0fcee-122">The input parameters can be in any order.</span></span> <span data-ttu-id="0fcee-123">如需範例，請參閱 [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="0fcee-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcee-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fcee-124">Requirements</span></span>



| <span data-ttu-id="0fcee-125">需求</span><span class="sxs-lookup"><span data-stu-id="0fcee-125">Requirement</span></span> | <span data-ttu-id="0fcee-126">值</span><span class="sxs-lookup"><span data-stu-id="0fcee-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0fcee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0fcee-128"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fcee-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0fcee-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="0fcee-129">Library</span></span><br/> | <dl> <span data-ttu-id="0fcee-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fcee-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0fcee-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fcee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcee-132">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="0fcee-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="0fcee-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="0fcee-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="0fcee-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="0fcee-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 

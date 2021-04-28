---
description: D3DXFillTextureTX 函式-使用編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: 'D3DXFillTextureTX 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107636"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="0f1fe-103">D3DXFillTextureTX 函式</span><span class="sxs-lookup"><span data-stu-id="0f1fe-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="0f1fe-104">使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1fe-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f1fe-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="0f1fe-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f1fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f1fe-107">*pTexture* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0f1fe-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f1fe-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0f1fe-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0f1fe-109">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)物件的指標，代表要填滿的材質。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="0f1fe-110">*pTextureShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f1fe-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f1fe-111">類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="0f1fe-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="0f1fe-112">[**ID3DXTextureShader**](id3dxtextureshader.md)紋理著色器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f1fe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f1fe-113">Return value</span></span>

<span data-ttu-id="0f1fe-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f1fe-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f1fe-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f1fe-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1fe-117">備註</span><span class="sxs-lookup"><span data-stu-id="0f1fe-117">Remarks</span></span>

<span data-ttu-id="0f1fe-118">紋理目標必須是 HLSL 函式，且此函式會包含下列語義：</span><span class="sxs-lookup"><span data-stu-id="0f1fe-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="0f1fe-119">一個輸入參數必須使用位置語義。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="0f1fe-120">一個輸入參數必須使用 PSIZE 語義。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="0f1fe-121">函數必須傳回使用色彩語義的參數。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="0f1fe-122">以下是這類 HLSL 函數的範例：</span><span class="sxs-lookup"><span data-stu-id="0f1fe-122">The following is an example of such an HLSL function:</span></span>


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



<span data-ttu-id="0f1fe-123">請注意，輸入參數可以依任何順序排列，但必須表示這兩個輸入語義。</span><span class="sxs-lookup"><span data-stu-id="0f1fe-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f1fe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f1fe-124">Requirements</span></span>



| <span data-ttu-id="0f1fe-125">需求</span><span class="sxs-lookup"><span data-stu-id="0f1fe-125">Requirement</span></span> | <span data-ttu-id="0f1fe-126">值</span><span class="sxs-lookup"><span data-stu-id="0f1fe-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1fe-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0f1fe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0f1fe-128"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f1fe-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0f1fe-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f1fe-129">Library</span></span><br/> | <dl> <span data-ttu-id="0f1fe-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f1fe-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0f1fe-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f1fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1fe-132">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="0f1fe-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="0f1fe-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="0f1fe-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="0f1fe-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="0f1fe-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 

---
description: 使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: 'D3DXFillCubeTextureTX 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37a831ef95d50f9b0389be0f1c9937e46748f6d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696643"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="ee215-103">D3DXFillCubeTextureTX 函式</span><span class="sxs-lookup"><span data-stu-id="ee215-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="ee215-104">使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。</span><span class="sxs-lookup"><span data-stu-id="ee215-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee215-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee215-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="ee215-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee215-107">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee215-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee215-108">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="ee215-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="ee215-109">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)物件的指標，代表要填滿的材質。</span><span class="sxs-lookup"><span data-stu-id="ee215-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="ee215-110">*pTextureShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee215-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee215-111">類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="ee215-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="ee215-112">[**ID3DXTextureShader**](id3dxtextureshader.md)紋理著色器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ee215-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee215-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee215-113">Return value</span></span>

<span data-ttu-id="ee215-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee215-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee215-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ee215-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee215-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="ee215-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee215-117">備註</span><span class="sxs-lookup"><span data-stu-id="ee215-117">Remarks</span></span>

<span data-ttu-id="ee215-118">紋理目標必須是 HLSL 函式，且此函式會包含下列語義：</span><span class="sxs-lookup"><span data-stu-id="ee215-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="ee215-119">一個輸入參數必須使用位置語義。</span><span class="sxs-lookup"><span data-stu-id="ee215-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="ee215-120">一個輸入參數必須使用 PSIZE 語義。</span><span class="sxs-lookup"><span data-stu-id="ee215-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="ee215-121">函數必須傳回使用色彩語義的參數。</span><span class="sxs-lookup"><span data-stu-id="ee215-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="ee215-122">輸入參數可以依任何順序排列。</span><span class="sxs-lookup"><span data-stu-id="ee215-122">The input parameters can be in any order.</span></span> <span data-ttu-id="ee215-123">如需範例，請參閱 [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="ee215-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ee215-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee215-124">Requirements</span></span>



| <span data-ttu-id="ee215-125">需求</span><span class="sxs-lookup"><span data-stu-id="ee215-125">Requirement</span></span> | <span data-ttu-id="ee215-126">值</span><span class="sxs-lookup"><span data-stu-id="ee215-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee215-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ee215-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ee215-128"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee215-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ee215-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee215-129">Library</span></span><br/> | <dl> <span data-ttu-id="ee215-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee215-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ee215-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee215-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee215-132">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="ee215-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="ee215-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="ee215-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 

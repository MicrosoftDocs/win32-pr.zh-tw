---
description: 從記憶體載入介面。
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: 'D3DXLoadSurfaceFromMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035332"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="0580d-103">D3DXLoadSurfaceFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="0580d-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="0580d-104">從記憶體載入介面。</span><span class="sxs-lookup"><span data-stu-id="0580d-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0580d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0580d-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="0580d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0580d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0580d-107">*pDestSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-108">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="0580d-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="0580d-109">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0580d-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="0580d-110">指定接收影像的目的地介面。</span><span class="sxs-lookup"><span data-stu-id="0580d-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="0580d-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="0580d-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0580d-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-114">*pDestRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-115">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="0580d-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="0580d-116">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0580d-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="0580d-117">指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="0580d-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="0580d-118">將此參數設定為 **Null** ，以指定整個表面。</span><span class="sxs-lookup"><span data-stu-id="0580d-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-119">*pSrcMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-120">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0580d-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0580d-121">記憶體中來源影像左上角的指標。</span><span class="sxs-lookup"><span data-stu-id="0580d-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-122">*SrcFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-123">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0580d-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0580d-124">[D3DFORMAT](d3dformat.md)列舉型別的成員，也就是來源影像的像素格式。</span><span class="sxs-lookup"><span data-stu-id="0580d-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-125">*SrcPitch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0580d-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0580d-127">來源影像的音調（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0580d-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="0580d-128">若為 DXT 格式，這個數位應該表示一列資料格的寬度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0580d-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-129">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-130">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="0580d-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="0580d-131">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的來源調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0580d-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-132">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-133">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="0580d-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="0580d-134">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0580d-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="0580d-135">指定記憶體中來源影像的維度。</span><span class="sxs-lookup"><span data-stu-id="0580d-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="0580d-136">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0580d-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-137">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-138">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0580d-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0580d-139">用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。</span><span class="sxs-lookup"><span data-stu-id="0580d-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="0580d-140">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="0580d-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="0580d-141">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0580d-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0580d-142">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="0580d-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="0580d-143">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="0580d-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="0580d-144">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="0580d-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="0580d-145">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="0580d-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="0580d-146">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="0580d-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0580d-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="0580d-147">Return value</span></span>

<span data-ttu-id="0580d-148">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0580d-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0580d-149">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0580d-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0580d-150">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="0580d-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0580d-151">備註</span><span class="sxs-lookup"><span data-stu-id="0580d-151">Remarks</span></span>

<span data-ttu-id="0580d-152">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="0580d-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="0580d-153">寫入至非層級零的介面並不會更新中途的矩形。</span><span class="sxs-lookup"><span data-stu-id="0580d-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="0580d-154">如果呼叫 **D3DXLoadSurfaceFromMemory** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。</span><span class="sxs-lookup"><span data-stu-id="0580d-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0580d-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="0580d-155">Requirements</span></span>



| <span data-ttu-id="0580d-156">需求</span><span class="sxs-lookup"><span data-stu-id="0580d-156">Requirement</span></span> | <span data-ttu-id="0580d-157">值</span><span class="sxs-lookup"><span data-stu-id="0580d-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0580d-158">標頭</span><span class="sxs-lookup"><span data-stu-id="0580d-158">Header</span></span><br/>  | <dl> <span data-ttu-id="0580d-159"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="0580d-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0580d-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="0580d-160">Library</span></span><br/> | <dl> <span data-ttu-id="0580d-161"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0580d-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0580d-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0580d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0580d-163">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="0580d-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

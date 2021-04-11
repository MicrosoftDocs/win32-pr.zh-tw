---
description: 從資源載入介面。
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: 'D3DXLoadSurfaceFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946048"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="4c72e-103">D3DXLoadSurfaceFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="4c72e-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="4c72e-104">從資源載入介面。</span><span class="sxs-lookup"><span data-stu-id="4c72e-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c72e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c72e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4c72e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c72e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c72e-107">*pDestSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-108">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="4c72e-109">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4c72e-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="4c72e-110">指定接收影像的目的地介面。</span><span class="sxs-lookup"><span data-stu-id="4c72e-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4c72e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4c72e-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4c72e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-114">*pDestRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-115">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4c72e-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4c72e-116">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4c72e-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4c72e-117">指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="4c72e-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="4c72e-118">將此參數設定為 **Null** ，以指定整個表面。</span><span class="sxs-lookup"><span data-stu-id="4c72e-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-119">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-120">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c72e-121">資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4c72e-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-122">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-123">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c72e-124">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4c72e-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="4c72e-125">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="4c72e-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4c72e-126">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="4c72e-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4c72e-127">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4c72e-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-128">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-129">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4c72e-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4c72e-130">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4c72e-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4c72e-131">指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="4c72e-131">Specifies the source rectangle.</span></span> <span data-ttu-id="4c72e-132">將此參數設定為 **Null** ，以指定整個映射。</span><span class="sxs-lookup"><span data-stu-id="4c72e-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-133">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c72e-135">用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。</span><span class="sxs-lookup"><span data-stu-id="4c72e-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4c72e-136">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="4c72e-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-137">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-138">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4c72e-139">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="4c72e-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4c72e-140">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="4c72e-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4c72e-141">Alpha 是很重要的，而且通常會針對不透明的色彩索引鍵設定為 FF，因此，若為不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="4c72e-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4c72e-142">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4c72e-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c72e-143">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c72e-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4c72e-144">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4c72e-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c72e-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c72e-145">Return value</span></span>

<span data-ttu-id="4c72e-146">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c72e-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c72e-147">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4c72e-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c72e-148">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="4c72e-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c72e-149">備註</span><span class="sxs-lookup"><span data-stu-id="4c72e-149">Remarks</span></span>

<span data-ttu-id="4c72e-150">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="4c72e-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4c72e-151">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadSurfaceFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="4c72e-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="4c72e-152">否則，函式呼叫會解析為 D3DXLoadSurfaceFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="4c72e-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="4c72e-153">要載入的資源必須是 RT \_ 點陣圖或 rt RCDATA 類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4c72e-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="4c72e-154">資源類型 RT \_ RCDATA 可用來載入點陣圖以外的格式 (例如 tga、.jpg 和 dds) 。</span><span class="sxs-lookup"><span data-stu-id="4c72e-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="4c72e-155">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="4c72e-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="4c72e-156">寫入至非層級零的介面並不會更新中途的矩形。</span><span class="sxs-lookup"><span data-stu-id="4c72e-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="4c72e-157">如果呼叫 [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。</span><span class="sxs-lookup"><span data-stu-id="4c72e-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c72e-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c72e-158">Requirements</span></span>



| <span data-ttu-id="4c72e-159">需求</span><span class="sxs-lookup"><span data-stu-id="4c72e-159">Requirement</span></span> | <span data-ttu-id="4c72e-160">值</span><span class="sxs-lookup"><span data-stu-id="4c72e-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c72e-161">標頭</span><span class="sxs-lookup"><span data-stu-id="4c72e-161">Header</span></span><br/>  | <dl> <span data-ttu-id="4c72e-162"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c72e-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4c72e-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c72e-163">Library</span></span><br/> | <dl> <span data-ttu-id="4c72e-164"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c72e-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4c72e-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c72e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c72e-166">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="4c72e-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

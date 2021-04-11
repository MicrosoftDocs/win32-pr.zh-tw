---
description: 從檔案載入介面。
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: 'D3DXLoadSurfaceFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696835"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="fff3a-103">D3DXLoadSurfaceFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="fff3a-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="fff3a-104">從檔案載入介面。</span><span class="sxs-lookup"><span data-stu-id="fff3a-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="fff3a-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fff3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="fff3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff3a-107">*pDestSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-108">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="fff3a-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="fff3a-109">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fff3a-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="fff3a-110">指定接收影像的目的地介面。</span><span class="sxs-lookup"><span data-stu-id="fff3a-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fff3a-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fff3a-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fff3a-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-114">*pDestRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-115">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="fff3a-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="fff3a-116">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fff3a-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="fff3a-117">指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="fff3a-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="fff3a-118">將此參數設定為 **Null** ，以指定整個表面。</span><span class="sxs-lookup"><span data-stu-id="fff3a-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-119">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-120">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fff3a-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fff3a-121">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="fff3a-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="fff3a-122">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="fff3a-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fff3a-123">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="fff3a-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fff3a-124">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="fff3a-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-125">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-126">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="fff3a-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="fff3a-127">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fff3a-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="fff3a-128">指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="fff3a-128">Specifies the source rectangle.</span></span> <span data-ttu-id="fff3a-129">將此參數設定為 **Null** ，以指定整個映射。</span><span class="sxs-lookup"><span data-stu-id="fff3a-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-130">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fff3a-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fff3a-132">用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。</span><span class="sxs-lookup"><span data-stu-id="fff3a-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="fff3a-133">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="fff3a-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-134">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-135">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fff3a-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="fff3a-136">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="fff3a-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="fff3a-137">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="fff3a-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="fff3a-138">Alpha 是很重要的，而且通常會針對不透明的色彩索引鍵設定為 FF，因此，若為不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="fff3a-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="fff3a-139">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="fff3a-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fff3a-140">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fff3a-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="fff3a-141">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fff3a-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff3a-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="fff3a-142">Return value</span></span>

<span data-ttu-id="fff3a-143">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fff3a-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fff3a-144">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fff3a-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fff3a-145">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="fff3a-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="fff3a-146">備註</span><span class="sxs-lookup"><span data-stu-id="fff3a-146">Remarks</span></span>

<span data-ttu-id="fff3a-147">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="fff3a-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fff3a-148">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadSurfaceFromFileW。</span><span class="sxs-lookup"><span data-stu-id="fff3a-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="fff3a-149">否則，函式呼叫會解析為 D3DXLoadSurfaceFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="fff3a-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="fff3a-150">此函式會處理壓縮紋理格式的轉換，並支援下列檔案格式： .bmp、.jpg、.dib、hdr、.jpg、. pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="fff3a-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="fff3a-151">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="fff3a-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="fff3a-152">寫入至非層級零的介面並不會更新中途的矩形。</span><span class="sxs-lookup"><span data-stu-id="fff3a-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="fff3a-153">如果呼叫 **D3DXLoadSurfaceFromFile** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。</span><span class="sxs-lookup"><span data-stu-id="fff3a-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff3a-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="fff3a-154">Requirements</span></span>



| <span data-ttu-id="fff3a-155">需求</span><span class="sxs-lookup"><span data-stu-id="fff3a-155">Requirement</span></span> | <span data-ttu-id="fff3a-156">值</span><span class="sxs-lookup"><span data-stu-id="fff3a-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fff3a-157">標頭</span><span class="sxs-lookup"><span data-stu-id="fff3a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="fff3a-158"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="fff3a-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fff3a-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="fff3a-159">Library</span></span><br/> | <dl> <span data-ttu-id="fff3a-160"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fff3a-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fff3a-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fff3a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff3a-162">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="fff3a-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

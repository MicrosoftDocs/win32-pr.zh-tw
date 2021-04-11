---
description: 從記憶體中的檔案載入介面。
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: 'D3DXLoadSurfaceFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696832"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="4b950-103">D3DXLoadSurfaceFromFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="4b950-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="4b950-104">從記憶體中的檔案載入介面。</span><span class="sxs-lookup"><span data-stu-id="4b950-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b950-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b950-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4b950-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b950-107">*pDestSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-108">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="4b950-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="4b950-109">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4b950-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="4b950-110">指定接收影像的目的地介面。</span><span class="sxs-lookup"><span data-stu-id="4b950-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4b950-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4b950-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4b950-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-114">*pDestRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-115">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4b950-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4b950-116">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4b950-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4b950-117">指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="4b950-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="4b950-118">將此參數設定為 **Null** ，以指定整個表面。</span><span class="sxs-lookup"><span data-stu-id="4b950-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-119">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-120">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b950-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b950-121">要載入介面之記憶體中的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="4b950-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-122">*>srcdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b950-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b950-124">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b950-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-125">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-126">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4b950-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4b950-127">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4b950-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4b950-128">指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="4b950-128">Specifies the source rectangle.</span></span> <span data-ttu-id="4b950-129">將此參數設定為 **Null** ，以指定整個映射。</span><span class="sxs-lookup"><span data-stu-id="4b950-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-130">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b950-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b950-132">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="4b950-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4b950-133">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="4b950-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-134">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b950-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-135">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4b950-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4b950-136">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="4b950-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4b950-137">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="4b950-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4b950-138">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="4b950-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="4b950-139">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="4b950-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4b950-140">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4b950-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b950-141">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b950-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4b950-142">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入來源影像檔案中的資料描述或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4b950-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b950-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b950-143">Return value</span></span>

<span data-ttu-id="4b950-144">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b950-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b950-145">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4b950-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4b950-146">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="4b950-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b950-147">備註</span><span class="sxs-lookup"><span data-stu-id="4b950-147">Remarks</span></span>

<span data-ttu-id="4b950-148">此函式會處理壓縮紋理格式的轉換，並支援下列檔案格式： .bmp、.jpg、.dib、hdr、.jpg、. pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="4b950-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="4b950-149">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="4b950-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="4b950-150">寫入至非層級零的介面並不會更新中途的矩形。</span><span class="sxs-lookup"><span data-stu-id="4b950-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="4b950-151">如果呼叫 **D3DXLoadSurfaceFromFileInMemory** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。</span><span class="sxs-lookup"><span data-stu-id="4b950-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b950-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b950-152">Requirements</span></span>



| <span data-ttu-id="4b950-153">需求</span><span class="sxs-lookup"><span data-stu-id="4b950-153">Requirement</span></span> | <span data-ttu-id="4b950-154">值</span><span class="sxs-lookup"><span data-stu-id="4b950-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b950-155">標頭</span><span class="sxs-lookup"><span data-stu-id="4b950-155">Header</span></span><br/>  | <dl> <span data-ttu-id="4b950-156"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b950-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4b950-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b950-157">Library</span></span><br/> | <dl> <span data-ttu-id="4b950-158"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b950-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4b950-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b950-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b950-160">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="4b950-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

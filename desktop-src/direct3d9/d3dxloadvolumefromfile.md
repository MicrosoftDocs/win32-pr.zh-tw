---
description: 從檔案載入磁片區。
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: 'D3DXLoadVolumeFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981988"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="4e133-103">D3DXLoadVolumeFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="4e133-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="4e133-104">從檔案載入磁片區。</span><span class="sxs-lookup"><span data-stu-id="4e133-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e133-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e133-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e133-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e133-107">*pDestVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-108">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="4e133-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="4e133-109">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4e133-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="4e133-110">指定目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="4e133-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4e133-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4e133-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e133-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-114">*pDestBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-115">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e133-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="4e133-116">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4e133-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="4e133-117">指定目的地方塊。</span><span class="sxs-lookup"><span data-stu-id="4e133-117">Specifies the destination box.</span></span> <span data-ttu-id="4e133-118">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="4e133-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-119">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-120">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e133-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e133-121">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4e133-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="4e133-122">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="4e133-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4e133-123">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="4e133-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4e133-124">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4e133-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-125">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-126">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e133-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="4e133-127">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4e133-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="4e133-128">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="4e133-128">Specifies the source box.</span></span> <span data-ttu-id="4e133-129">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="4e133-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-130">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e133-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e133-132">一或多個 [D3DX \_ 篩選](d3dx-filter.md)的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="4e133-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="4e133-133">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="4e133-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-134">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-135">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4e133-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4e133-136">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="4e133-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4e133-137">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="4e133-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4e133-138">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="4e133-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="4e133-139">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="4e133-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4e133-140">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e133-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e133-141">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e133-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4e133-142">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e133-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e133-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e133-143">Return value</span></span>

<span data-ttu-id="4e133-144">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e133-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e133-145">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4e133-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e133-146">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="4e133-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e133-147">備註</span><span class="sxs-lookup"><span data-stu-id="4e133-147">Remarks</span></span>

<span data-ttu-id="4e133-148">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="4e133-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4e133-149">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadVolumeFromFileW。</span><span class="sxs-lookup"><span data-stu-id="4e133-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="4e133-150">否則，函式呼叫會解析為 D3DXLoadVolumeFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="4e133-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="4e133-151">此函式會處理壓縮紋理格式的轉換，並支援下列檔案格式： .bmp、.jpg、.dib、hdr、.jpg、. pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="4e133-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="4e133-152">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="4e133-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="4e133-153">寫入至非層級零的音量材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="4e133-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="4e133-154">如果呼叫 **D3DXLoadVolumeFromFile** ，但材質尚未中途變更 (在) 的一般使用案例下，應用程式必須明確地呼叫磁片區材質上的 [**IDirect3DVolumeTexture9：： AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) 。</span><span class="sxs-lookup"><span data-stu-id="4e133-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e133-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e133-155">Requirements</span></span>



| <span data-ttu-id="4e133-156">需求</span><span class="sxs-lookup"><span data-stu-id="4e133-156">Requirement</span></span> | <span data-ttu-id="4e133-157">值</span><span class="sxs-lookup"><span data-stu-id="4e133-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e133-158">標頭</span><span class="sxs-lookup"><span data-stu-id="4e133-158">Header</span></span><br/>  | <dl> <span data-ttu-id="4e133-159"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e133-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4e133-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e133-160">Library</span></span><br/> | <dl> <span data-ttu-id="4e133-161"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e133-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4e133-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e133-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e133-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="4e133-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="4e133-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="4e133-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="4e133-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="4e133-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="4e133-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="4e133-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="4e133-167">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="4e133-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

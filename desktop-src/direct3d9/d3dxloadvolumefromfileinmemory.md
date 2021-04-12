---
description: 從記憶體中的檔案載入磁片區。
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: 'D3DXLoadVolumeFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946082"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a><span data-ttu-id="660f7-103">D3DXLoadVolumeFromFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="660f7-103">D3DXLoadVolumeFromFileInMemory function</span></span>

<span data-ttu-id="660f7-104">從記憶體中的檔案載入磁片區。</span><span class="sxs-lookup"><span data-stu-id="660f7-104">Loads a volume from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="660f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="660f7-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="660f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="660f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660f7-107">*pDestVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-108">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="660f7-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="660f7-109">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="660f7-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="660f7-110">指定目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="660f7-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="660f7-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="660f7-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="660f7-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-114">*pDestBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-115">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="660f7-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="660f7-116">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="660f7-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="660f7-117">指定目的地方塊。</span><span class="sxs-lookup"><span data-stu-id="660f7-117">Specifies the destination box.</span></span> <span data-ttu-id="660f7-118">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="660f7-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-119">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-120">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="660f7-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="660f7-121">要載入磁片區之記憶體中的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="660f7-121">Pointer to the file in memory from which to load the volume.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-122">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-122">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="660f7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="660f7-124">記憶體中檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="660f7-124">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-125">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-126">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="660f7-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="660f7-127">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="660f7-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="660f7-128">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="660f7-128">Specifies the source box.</span></span> <span data-ttu-id="660f7-129">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="660f7-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-130">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="660f7-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="660f7-132">一或多個 [D3DX \_ 篩選](d3dx-filter.md)的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="660f7-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="660f7-133">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="660f7-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-134">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-135">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="660f7-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="660f7-136">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="660f7-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="660f7-137">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="660f7-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="660f7-138">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="660f7-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="660f7-139">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="660f7-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="660f7-140">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="660f7-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660f7-141">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="660f7-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="660f7-142">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="660f7-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660f7-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="660f7-143">Return value</span></span>

<span data-ttu-id="660f7-144">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="660f7-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="660f7-145">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="660f7-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="660f7-146">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="660f7-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="660f7-147">備註</span><span class="sxs-lookup"><span data-stu-id="660f7-147">Remarks</span></span>

<span data-ttu-id="660f7-148">此函式會處理壓縮紋理格式的轉換，並支援下列檔案格式： .bmp、.jpg、.dib、hdr、.jpg、. pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="660f7-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="660f7-149">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="660f7-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="660f7-150">寫入至非層級零的音量材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="660f7-150">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="660f7-151">如果呼叫 **D3DXLoadVolumeFromFileInMemory** ，但材質尚未中途變更 (在) 的一般使用案例下，應用程式必須明確地呼叫磁片區材質上的 [**IDirect3DVolumeTexture9：： AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) 。</span><span class="sxs-lookup"><span data-stu-id="660f7-151">If **D3DXLoadVolumeFromFileInMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="660f7-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="660f7-152">Requirements</span></span>



| <span data-ttu-id="660f7-153">需求</span><span class="sxs-lookup"><span data-stu-id="660f7-153">Requirement</span></span> | <span data-ttu-id="660f7-154">值</span><span class="sxs-lookup"><span data-stu-id="660f7-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="660f7-155">標頭</span><span class="sxs-lookup"><span data-stu-id="660f7-155">Header</span></span><br/>  | <dl> <span data-ttu-id="660f7-156"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="660f7-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="660f7-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="660f7-157">Library</span></span><br/> | <dl> <span data-ttu-id="660f7-158"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="660f7-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="660f7-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="660f7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660f7-160">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="660f7-160">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="660f7-161">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="660f7-161">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="660f7-162">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="660f7-162">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="660f7-163">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="660f7-163">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="660f7-164">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="660f7-164">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

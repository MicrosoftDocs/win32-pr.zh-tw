---
description: 從資源載入磁片區。
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: 'D3DXLoadVolumeFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989182"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="df93d-103">D3DXLoadVolumeFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="df93d-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="df93d-104">從資源載入磁片區。</span><span class="sxs-lookup"><span data-stu-id="df93d-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="df93d-105">語法</span><span class="sxs-lookup"><span data-stu-id="df93d-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="df93d-106">參數</span><span class="sxs-lookup"><span data-stu-id="df93d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df93d-107">*pDestVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-108">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="df93d-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="df93d-109">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="df93d-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="df93d-110">指定目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="df93d-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="df93d-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="df93d-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="df93d-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-114">*pDestBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-115">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="df93d-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="df93d-116">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="df93d-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="df93d-117">指定目的地方塊。</span><span class="sxs-lookup"><span data-stu-id="df93d-117">Specifies the destination box.</span></span> <span data-ttu-id="df93d-118">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="df93d-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-119">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-120">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df93d-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df93d-121">資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="df93d-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-122">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-123">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df93d-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df93d-124">字串的指標，指定來源影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="df93d-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="df93d-125">如果 \_ 已定義 unicode 或 unicode，則此參數類型為 LPCWSTR，否則為 LPCSTR 類型。</span><span class="sxs-lookup"><span data-stu-id="df93d-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-126">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-127">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="df93d-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="df93d-128">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="df93d-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="df93d-129">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="df93d-129">Specifies the source box.</span></span> <span data-ttu-id="df93d-130">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="df93d-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-131">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df93d-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df93d-133">一或多個 [D3DX \_ 篩選](d3dx-filter.md)的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="df93d-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="df93d-134">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="df93d-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-135">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-136">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="df93d-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="df93d-137">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="df93d-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="df93d-138">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="df93d-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="df93d-139">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="df93d-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="df93d-140">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="df93d-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="df93d-141">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df93d-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df93d-142">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="df93d-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="df93d-143">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="df93d-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df93d-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="df93d-144">Return value</span></span>

<span data-ttu-id="df93d-145">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df93d-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df93d-146">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="df93d-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df93d-147">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="df93d-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="df93d-148">備註</span><span class="sxs-lookup"><span data-stu-id="df93d-148">Remarks</span></span>

<span data-ttu-id="df93d-149">要載入的資源必須是點陣圖資源 (RT \_ 點陣圖) 。</span><span class="sxs-lookup"><span data-stu-id="df93d-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="df93d-150">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="df93d-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="df93d-151">寫入至非層級零的音量材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="df93d-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="df93d-152">如果呼叫 [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) ，但材質尚未中途變更 (在) 的一般使用案例下，應用程式必須明確地呼叫磁片區材質上的 [**IDirect3DVolumeTexture9：： AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) 。</span><span class="sxs-lookup"><span data-stu-id="df93d-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="df93d-153">此函數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="df93d-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="df93d-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="df93d-154">Requirements</span></span>



| <span data-ttu-id="df93d-155">需求</span><span class="sxs-lookup"><span data-stu-id="df93d-155">Requirement</span></span> | <span data-ttu-id="df93d-156">值</span><span class="sxs-lookup"><span data-stu-id="df93d-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df93d-157">標頭</span><span class="sxs-lookup"><span data-stu-id="df93d-157">Header</span></span><br/>  | <dl> <span data-ttu-id="df93d-158"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="df93d-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="df93d-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="df93d-159">Library</span></span><br/> | <dl> <span data-ttu-id="df93d-160"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df93d-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="df93d-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df93d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df93d-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="df93d-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="df93d-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="df93d-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="df93d-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="df93d-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="df93d-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="df93d-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="df93d-166">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="df93d-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

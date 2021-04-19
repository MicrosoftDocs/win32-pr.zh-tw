---
description: 從記憶體載入磁片區。
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: 'D3DXLoadVolumeFromMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986721"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="12252-103">D3DXLoadVolumeFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="12252-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="12252-104">從記憶體載入磁片區。</span><span class="sxs-lookup"><span data-stu-id="12252-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="12252-105">語法</span><span class="sxs-lookup"><span data-stu-id="12252-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="12252-106">參數</span><span class="sxs-lookup"><span data-stu-id="12252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12252-107">*pDestVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-108">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="12252-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="12252-109">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="12252-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="12252-110">指定接收映射的目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="12252-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="12252-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="12252-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="12252-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="12252-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12252-114">*pDestBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-115">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="12252-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="12252-116">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="12252-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="12252-117">指定目的地方塊。</span><span class="sxs-lookup"><span data-stu-id="12252-117">Specifies the destination box.</span></span> <span data-ttu-id="12252-118">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="12252-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="12252-119">*pSrcMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-120">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12252-121">記憶體中來源磁片區左上角的指標。</span><span class="sxs-lookup"><span data-stu-id="12252-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="12252-122">*SrcFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-123">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="12252-124">[D3DFORMAT](d3dformat.md)列舉型別的成員，也就是來源磁片區的像素格式。</span><span class="sxs-lookup"><span data-stu-id="12252-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="12252-125">*SrcRowPitch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12252-127">來源影像的音調（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="12252-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="12252-128">針對 DXT 格式 (壓縮的材質格式) ，這個數位應該代表一個資料列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="12252-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="12252-129">*SrcSlicePitch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-130">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12252-131">來源影像的音調（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="12252-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="12252-132">若為 DXT 格式 (壓縮的材質格式) ，這個數位應該代表一個資料格磁區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="12252-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="12252-133">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-134">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="12252-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="12252-135">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的來源調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="12252-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12252-136">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-137">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="12252-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="12252-138">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="12252-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="12252-139">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="12252-139">Specifies the source box.</span></span> <span data-ttu-id="12252-140">**Null** 對此參數而言不是有效的值。</span><span class="sxs-lookup"><span data-stu-id="12252-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="12252-141">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-142">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12252-143">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="12252-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="12252-144">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="12252-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="12252-145">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12252-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12252-146">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="12252-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="12252-147">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="12252-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="12252-148">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="12252-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="12252-149">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="12252-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="12252-150">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="12252-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12252-151">傳回值</span><span class="sxs-lookup"><span data-stu-id="12252-151">Return value</span></span>

<span data-ttu-id="12252-152">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12252-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12252-153">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="12252-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="12252-154">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="12252-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="12252-155">備註</span><span class="sxs-lookup"><span data-stu-id="12252-155">Remarks</span></span>

<span data-ttu-id="12252-156">寫入至非層級零的音量材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="12252-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="12252-157">如果呼叫 **D3DXLoadVolumeFromMemory** ，但材質尚未中途變更 (在) 的一般使用案例下，應用程式必須明確地呼叫磁片區材質上的 [**IDirect3DVolumeTexture9：： AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) 。</span><span class="sxs-lookup"><span data-stu-id="12252-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="12252-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="12252-158">Requirements</span></span>



| <span data-ttu-id="12252-159">需求</span><span class="sxs-lookup"><span data-stu-id="12252-159">Requirement</span></span> | <span data-ttu-id="12252-160">值</span><span class="sxs-lookup"><span data-stu-id="12252-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12252-161">標頭</span><span class="sxs-lookup"><span data-stu-id="12252-161">Header</span></span><br/>  | <dl> <span data-ttu-id="12252-162"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="12252-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="12252-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="12252-163">Library</span></span><br/> | <dl> <span data-ttu-id="12252-164"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="12252-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="12252-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12252-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12252-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="12252-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="12252-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="12252-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="12252-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="12252-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="12252-169">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="12252-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

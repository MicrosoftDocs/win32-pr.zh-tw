---
description: 從另一個磁片區載入磁片區。
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: 'D3DXLoadVolumeFromVolume 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946192"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="fc71f-103">D3DXLoadVolumeFromVolume 函式</span><span class="sxs-lookup"><span data-stu-id="fc71f-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="fc71f-104">從另一個磁片區載入磁片區。</span><span class="sxs-lookup"><span data-stu-id="fc71f-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc71f-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc71f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="fc71f-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc71f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc71f-107">*pDestVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-108">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="fc71f-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="fc71f-109">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fc71f-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="fc71f-110">指定接收映射的目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="fc71f-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-111">*pDestPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-112">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fc71f-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fc71f-113">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fc71f-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-114">*pDestBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-115">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc71f-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="fc71f-116">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fc71f-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="fc71f-117">指定目的地方塊。</span><span class="sxs-lookup"><span data-stu-id="fc71f-117">Specifies the destination box.</span></span> <span data-ttu-id="fc71f-118">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="fc71f-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-119">*pSrcVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-120">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="fc71f-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="fc71f-121">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fc71f-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="fc71f-122">指定來源磁片區。</span><span class="sxs-lookup"><span data-stu-id="fc71f-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-123">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-124">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fc71f-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fc71f-125">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的來源調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fc71f-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-126">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-127">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc71f-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="fc71f-128">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fc71f-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="fc71f-129">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="fc71f-129">Specifies the source box.</span></span> <span data-ttu-id="fc71f-130">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="fc71f-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-131">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc71f-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc71f-133">一或多個 [D3DX \_ 篩選](d3dx-filter.md)的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="fc71f-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="fc71f-134">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="fc71f-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="fc71f-135">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc71f-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc71f-136">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fc71f-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="fc71f-137">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="fc71f-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="fc71f-138">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="fc71f-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="fc71f-139">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="fc71f-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="fc71f-140">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="fc71f-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc71f-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc71f-141">Return value</span></span>

<span data-ttu-id="fc71f-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc71f-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc71f-143">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fc71f-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc71f-144">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="fc71f-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc71f-145">備註</span><span class="sxs-lookup"><span data-stu-id="fc71f-145">Remarks</span></span>

<span data-ttu-id="fc71f-146">寫入至非層級零的音量材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="fc71f-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="fc71f-147">如果呼叫 **D3DXLoadVolumeFromVolume** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確地呼叫 [**IDirect3DVolumeTexture9：： AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) 。</span><span class="sxs-lookup"><span data-stu-id="fc71f-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc71f-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc71f-148">Requirements</span></span>



| <span data-ttu-id="fc71f-149">需求</span><span class="sxs-lookup"><span data-stu-id="fc71f-149">Requirement</span></span> | <span data-ttu-id="fc71f-150">值</span><span class="sxs-lookup"><span data-stu-id="fc71f-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc71f-151">標頭</span><span class="sxs-lookup"><span data-stu-id="fc71f-151">Header</span></span><br/>  | <dl> <span data-ttu-id="fc71f-152"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc71f-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fc71f-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc71f-153">Library</span></span><br/> | <dl> <span data-ttu-id="fc71f-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc71f-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fc71f-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc71f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc71f-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="fc71f-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="fc71f-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="fc71f-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="fc71f-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="fc71f-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="fc71f-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="fc71f-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="fc71f-160">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="fc71f-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

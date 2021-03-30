---
title: 'D3DX11_IMAGE_INFO 結構 (D3DX11tex .h) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 |D3DX11_IMAGE_INFO 結構 (D3DX11tex .h) '
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO 結構 Direct3D 11
- LPD3DX11_IMAGE_INFO 結構指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974710"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="dad15-107">D3DX11 \_ 影像 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="dad15-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="dad15-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="dad15-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="dad15-109">選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。</span><span class="sxs-lookup"><span data-stu-id="dad15-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="dad15-110">\_任何這些參數的 D3DX11 預設值都會導致 D3DX 自動使用來源檔案的值。</span><span class="sxs-lookup"><span data-stu-id="dad15-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad15-111">語法</span><span class="sxs-lookup"><span data-stu-id="dad15-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="dad15-112">成員</span><span class="sxs-lookup"><span data-stu-id="dad15-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="dad15-113">**寬度**</span><span class="sxs-lookup"><span data-stu-id="dad15-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-115">材質的目標寬度。</span><span class="sxs-lookup"><span data-stu-id="dad15-115">The target width of the texture.</span></span> <span data-ttu-id="dad15-116">如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。</span><span class="sxs-lookup"><span data-stu-id="dad15-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-117">**高度**</span><span class="sxs-lookup"><span data-stu-id="dad15-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-119">材質的目標高度。</span><span class="sxs-lookup"><span data-stu-id="dad15-119">The target height of the texture.</span></span> <span data-ttu-id="dad15-120">如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。</span><span class="sxs-lookup"><span data-stu-id="dad15-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-121">**深度**</span><span class="sxs-lookup"><span data-stu-id="dad15-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-122">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-123">材質的深度。</span><span class="sxs-lookup"><span data-stu-id="dad15-123">The depth of the texture.</span></span> <span data-ttu-id="dad15-124">這僅適用于磁片區紋理。</span><span class="sxs-lookup"><span data-stu-id="dad15-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-125">[陣列大小]</span><span class="sxs-lookup"><span data-stu-id="dad15-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-126">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-127">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="dad15-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-128">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="dad15-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-129">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-130">材質中 mipmap 層級的最大數目。</span><span class="sxs-lookup"><span data-stu-id="dad15-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="dad15-131">請參閱 [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)中的備註。</span><span class="sxs-lookup"><span data-stu-id="dad15-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="dad15-132">使用0或 D3DX11 \_ 預設值，將會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="dad15-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-133">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="dad15-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-134">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dad15-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-135">使用 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 標旗標指定的其他資源屬性。</span><span class="sxs-lookup"><span data-stu-id="dad15-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-136">**格式**</span><span class="sxs-lookup"><span data-stu-id="dad15-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-137">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="dad15-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-138">一個 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉，用來指定材質載入後的材質格式。</span><span class="sxs-lookup"><span data-stu-id="dad15-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-139">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="dad15-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-140">類型： **[ **D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="dad15-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-141">識別資源類型的 [**D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) 值。</span><span class="sxs-lookup"><span data-stu-id="dad15-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="dad15-142">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="dad15-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="dad15-143">類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="dad15-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dad15-144">用來識別影像格式的 [**D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md) 值。</span><span class="sxs-lookup"><span data-stu-id="dad15-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dad15-145">備註</span><span class="sxs-lookup"><span data-stu-id="dad15-145">Remarks</span></span>

<span data-ttu-id="dad15-146">此結構是由方法所使用，例如： [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md)、 [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)或 [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)。</span><span class="sxs-lookup"><span data-stu-id="dad15-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dad15-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="dad15-147">Requirements</span></span>



| <span data-ttu-id="dad15-148">需求</span><span class="sxs-lookup"><span data-stu-id="dad15-148">Requirement</span></span> | <span data-ttu-id="dad15-149">值</span><span class="sxs-lookup"><span data-stu-id="dad15-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dad15-150">標頭</span><span class="sxs-lookup"><span data-stu-id="dad15-150">Header</span></span><br/> | <dl> <span data-ttu-id="dad15-151"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="dad15-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad15-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dad15-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad15-153">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="dad15-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 


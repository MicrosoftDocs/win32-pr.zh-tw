---
description: 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 \_任何這些參數的 D3DX10 預設值都會導致 D3DX 自動使用來源檔案的值。
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: 'D3DX10_IMAGE_LOAD_INFO 結構 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976738"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="bba32-104">D3DX10 \_ 映射 \_ 載入 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="bba32-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="bba32-105">選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。</span><span class="sxs-lookup"><span data-stu-id="bba32-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="bba32-106">\_任何這些參數的 D3DX10 預設值都會導致 D3DX 自動使用來源檔案的值。</span><span class="sxs-lookup"><span data-stu-id="bba32-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba32-107">語法</span><span class="sxs-lookup"><span data-stu-id="bba32-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="bba32-108">成員</span><span class="sxs-lookup"><span data-stu-id="bba32-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bba32-109">**寬度**</span><span class="sxs-lookup"><span data-stu-id="bba32-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-111">材質的目標寬度。</span><span class="sxs-lookup"><span data-stu-id="bba32-111">The target width of the texture.</span></span> <span data-ttu-id="bba32-112">如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。</span><span class="sxs-lookup"><span data-stu-id="bba32-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="bba32-113">**高度**</span><span class="sxs-lookup"><span data-stu-id="bba32-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-115">材質的目標高度。</span><span class="sxs-lookup"><span data-stu-id="bba32-115">The target height of the texture.</span></span> <span data-ttu-id="bba32-116">如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。</span><span class="sxs-lookup"><span data-stu-id="bba32-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="bba32-117">**深度**</span><span class="sxs-lookup"><span data-stu-id="bba32-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-119">材質的深度。</span><span class="sxs-lookup"><span data-stu-id="bba32-119">The depth of the texture.</span></span> <span data-ttu-id="bba32-120">這僅適用于磁片區紋理。</span><span class="sxs-lookup"><span data-stu-id="bba32-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="bba32-121">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="bba32-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-123">材質的最高解析度 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="bba32-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="bba32-124">如果大於0，則在載入紋理之後，FirstMipLevel 會對應至 mipmap 層級0。</span><span class="sxs-lookup"><span data-stu-id="bba32-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="bba32-125">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="bba32-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-127">材質將擁有的最大 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="bba32-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="bba32-128">使用0或 D3DX10 \_ 預設值，將會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="bba32-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="bba32-129">**使用量**</span><span class="sxs-lookup"><span data-stu-id="bba32-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-130">類型： **[ **D3D10 \_ 使用** 方式](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="bba32-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-131">材質資源的使用方式。</span><span class="sxs-lookup"><span data-stu-id="bba32-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="bba32-132">請參閱 [**D3D10 \_ 使用量**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)。</span><span class="sxs-lookup"><span data-stu-id="bba32-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="bba32-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-134">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-135">將允許紋理系結的管線階段。</span><span class="sxs-lookup"><span data-stu-id="bba32-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="bba32-136">請參閱 [**D3D10 \_ BIND \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)標。</span><span class="sxs-lookup"><span data-stu-id="bba32-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-137">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="bba32-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-138">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-139">Cpu 對材質資源將擁有的存取權限。</span><span class="sxs-lookup"><span data-stu-id="bba32-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="bba32-140">請參閱 [**D3D10 \_ CPU \_ 存取 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)標。</span><span class="sxs-lookup"><span data-stu-id="bba32-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-141">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="bba32-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-142">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-143">其他資源屬性 (參閱 [**D3D10 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) 標) 。</span><span class="sxs-lookup"><span data-stu-id="bba32-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-144">**格式**</span><span class="sxs-lookup"><span data-stu-id="bba32-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-145">類型： **[ **DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="bba32-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-146">材質載入後將採用的格式。</span><span class="sxs-lookup"><span data-stu-id="bba32-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="bba32-147">請參閱 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。</span><span class="sxs-lookup"><span data-stu-id="bba32-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="bba32-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-149">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-150">只有在重新取樣) 時，才使用指定的篩選 (篩選材質。</span><span class="sxs-lookup"><span data-stu-id="bba32-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="bba32-151">請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="bba32-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="bba32-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-153">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba32-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba32-154">只有在產生 mipmap) 時，才使用指定的篩選 (來篩選材質 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="bba32-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="bba32-155">有效的值為 D3DX10 \_ filter \_ NONE、D3DX10 \_ FILTER \_ POINT、D3DX10 \_ filter \_ 線性或 D3DX10 \_ filter \_ 三角形。</span><span class="sxs-lookup"><span data-stu-id="bba32-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="bba32-156">請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="bba32-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba32-157">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="bba32-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="bba32-158">類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba32-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="bba32-159">原始影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bba32-159">Information about the original image.</span></span> <span data-ttu-id="bba32-160">請參閱 [**D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)。</span><span class="sxs-lookup"><span data-stu-id="bba32-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="bba32-161">可以使用 [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)、 [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)或 [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)取得。</span><span class="sxs-lookup"><span data-stu-id="bba32-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bba32-162">備註</span><span class="sxs-lookup"><span data-stu-id="bba32-162">Remarks</span></span>

<span data-ttu-id="bba32-163">在初始化結構時，您可以將任何成員設定為 D3DX10 \_ 預設值，而 D3DX 會在載入紋理時，使用來源材質的預設值將它初始化。</span><span class="sxs-lookup"><span data-stu-id="bba32-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="bba32-164">下列 Api 可以使用此結構：</span><span class="sxs-lookup"><span data-stu-id="bba32-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="bba32-165">建立資源，例如 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)。</span><span class="sxs-lookup"><span data-stu-id="bba32-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="bba32-166">建立資料處理器，例如 [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) 或 [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md)。</span><span class="sxs-lookup"><span data-stu-id="bba32-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bba32-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="bba32-167">Requirements</span></span>



| <span data-ttu-id="bba32-168">需求</span><span class="sxs-lookup"><span data-stu-id="bba32-168">Requirement</span></span> | <span data-ttu-id="bba32-169">值</span><span class="sxs-lookup"><span data-stu-id="bba32-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba32-170">標頭</span><span class="sxs-lookup"><span data-stu-id="bba32-170">Header</span></span><br/> | <dl> <span data-ttu-id="bba32-171"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="bba32-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba32-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bba32-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba32-173">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="bba32-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

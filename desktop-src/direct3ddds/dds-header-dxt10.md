---
title: 'DDS_HEADER_DXT10 結構 (Dd. h) '
description: 用來處理資源陣列的 DDS 標頭延伸、未對應到舊版 Microsoft DirectDraw 像素格式結構的 DXGI 像素格式，以及其他中繼資料。
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 結構 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981246"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="b4e78-104">DDS \_ 標頭 \_ DXT10 結構</span><span class="sxs-lookup"><span data-stu-id="b4e78-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="b4e78-105">用來處理資源陣列的 DDS 標頭延伸、未對應到舊版 Microsoft DirectDraw 像素格式結構的 DXGI 像素格式，以及其他中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b4e78-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e78-106">語法</span><span class="sxs-lookup"><span data-stu-id="b4e78-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="b4e78-107">成員</span><span class="sxs-lookup"><span data-stu-id="b4e78-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4e78-108">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="b4e78-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="b4e78-109">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b4e78-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="b4e78-110">Surface 像素格式 (查看 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="b4e78-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="b4e78-111">**resourceDimension**</span><span class="sxs-lookup"><span data-stu-id="b4e78-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="b4e78-112">類型： **[ **D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="b4e78-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="b4e78-113">識別資源的類型。</span><span class="sxs-lookup"><span data-stu-id="b4e78-113">Identifies the type of resource.</span></span> <span data-ttu-id="b4e78-114">此成員的下列值是 [**D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) 或 [**D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) 列舉中值的子集：</span><span class="sxs-lookup"><span data-stu-id="b4e78-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="b4e78-115">類型</span><span class="sxs-lookup"><span data-stu-id="b4e78-115">Type</span></span>                                                              | <span data-ttu-id="b4e78-116">描述</span><span class="sxs-lookup"><span data-stu-id="b4e78-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="b4e78-117">值</span><span class="sxs-lookup"><span data-stu-id="b4e78-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="b4e78-118">DDS \_ 維度 \_ TEXTURE1D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE1D) </span><span class="sxs-lookup"><span data-stu-id="b4e78-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="b4e78-119">資源是一 [維紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)。</span><span class="sxs-lookup"><span data-stu-id="b4e78-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="b4e78-120">[**DDS \_ 標頭**](dds-header.md)的 **dwWidth** 成員會指定紋理的大小。</span><span class="sxs-lookup"><span data-stu-id="b4e78-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="b4e78-121">一般來說，您會將 **dds \_ 標頭** 的 **dwHeight** 成員設為 1; 您也必須 \_ 在 **dds \_ 標頭** 的 **dwFlags** 成員中設定 DDSD HEIGHT 旗標。</span><span class="sxs-lookup"><span data-stu-id="b4e78-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="b4e78-122">2</span><span class="sxs-lookup"><span data-stu-id="b4e78-122">2</span></span>     |
| <span data-ttu-id="b4e78-123">DDS \_ 維度 \_ TEXTURE2D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE2D) </span><span class="sxs-lookup"><span data-stu-id="b4e78-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="b4e78-124">資源是 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)，具有由 [**DDS \_ 標頭**](dds-header.md)的 **dwWidth** 和 **dwHeight** 成員所指定的區域。</span><span class="sxs-lookup"><span data-stu-id="b4e78-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="b4e78-125">您也可以使用此類型來識別 cube 對應材質。</span><span class="sxs-lookup"><span data-stu-id="b4e78-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="b4e78-126">如需如何識別 cube 對應材質的詳細資訊，請參閱 **miscFlag** 和 **arraySize** 成員。</span><span class="sxs-lookup"><span data-stu-id="b4e78-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="b4e78-127">3</span><span class="sxs-lookup"><span data-stu-id="b4e78-127">3</span></span>     |
| <span data-ttu-id="b4e78-128">DDS \_ 維度 \_ TEXTURE3D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE3D) </span><span class="sxs-lookup"><span data-stu-id="b4e78-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="b4e78-129">資源是包含 **dwWidth**、 **dwHeight** 和 **dwDepth** 之 [**DDS \_ 標頭**](dds-header.md)成員所指定之磁片區的 [3d 紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)。</span><span class="sxs-lookup"><span data-stu-id="b4e78-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="b4e78-130">您也必須 \_ 在 **DDS \_ 標頭** 的 **dwFlags** 成員中設定 DDSD DEPTH 旗標。</span><span class="sxs-lookup"><span data-stu-id="b4e78-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="b4e78-131">4</span><span class="sxs-lookup"><span data-stu-id="b4e78-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="b4e78-132">**miscFlag**</span><span class="sxs-lookup"><span data-stu-id="b4e78-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="b4e78-133">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4e78-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4e78-134">識別其他較不常用的資源選項。</span><span class="sxs-lookup"><span data-stu-id="b4e78-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="b4e78-135">此成員的下列值是 [**D3D10 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) 標或 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) 標列舉中值的子集：</span><span class="sxs-lookup"><span data-stu-id="b4e78-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="b4e78-136">類型</span><span class="sxs-lookup"><span data-stu-id="b4e78-136">Type</span></span>                             | <span data-ttu-id="b4e78-137">描述</span><span class="sxs-lookup"><span data-stu-id="b4e78-137">Description</span></span>                                                                                                  | <span data-ttu-id="b4e78-138">值</span><span class="sxs-lookup"><span data-stu-id="b4e78-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="b4e78-139">DDS \_ 資源的 \_ 其他 \_ TEXTURECUBE</span><span class="sxs-lookup"><span data-stu-id="b4e78-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="b4e78-140">表示 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) 是 cube 地圖材質。</span><span class="sxs-lookup"><span data-stu-id="b4e78-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="b4e78-141">0x4</span><span class="sxs-lookup"><span data-stu-id="b4e78-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="b4e78-142">**arraySize**</span><span class="sxs-lookup"><span data-stu-id="b4e78-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="b4e78-143">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4e78-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4e78-144">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="b4e78-144">The number of elements in the array.</span></span>

<span data-ttu-id="b4e78-145">針對也是 cube 對應材質的 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) ，此數位代表 cube 的數目。</span><span class="sxs-lookup"><span data-stu-id="b4e78-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="b4e78-146">這個數位與 [**D3D10 \_ TEXCUBE \_ Array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)或 [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)) 的 **NumCubes** 成員中的數位相同。</span><span class="sxs-lookup"><span data-stu-id="b4e78-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="b4e78-147">在此情況下，DDS 檔案包含 **arraySize** \* 6 2d 材質。</span><span class="sxs-lookup"><span data-stu-id="b4e78-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="b4e78-148">如需此案例的詳細資訊，請參閱 **miscFlag** 描述。</span><span class="sxs-lookup"><span data-stu-id="b4e78-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="b4e78-149">若為 [3d 紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)，您必須將此數位設定為1。</span><span class="sxs-lookup"><span data-stu-id="b4e78-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="b4e78-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="b4e78-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="b4e78-151">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4e78-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4e78-152">包含先前保留)  (的額外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b4e78-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="b4e78-153">較低的3位表示相關聯資源的 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="b4e78-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="b4e78-154">前29個位是保留的，通常是0。</span><span class="sxs-lookup"><span data-stu-id="b4e78-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="b4e78-155">類型</span><span class="sxs-lookup"><span data-stu-id="b4e78-155">Type</span></span>                            | <span data-ttu-id="b4e78-156">描述</span><span class="sxs-lookup"><span data-stu-id="b4e78-156">Description</span></span>                                                                                                                              | <span data-ttu-id="b4e78-157">值</span><span class="sxs-lookup"><span data-stu-id="b4e78-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="b4e78-158">DDS \_ ALPHA \_ 模式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="b4e78-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="b4e78-159">Alpha 通道內容不明。</span><span class="sxs-lookup"><span data-stu-id="b4e78-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="b4e78-160">這是舊版檔案的值，通常會假設為「直接」 Alpha。</span><span class="sxs-lookup"><span data-stu-id="b4e78-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="b4e78-161">0x0</span><span class="sxs-lookup"><span data-stu-id="b4e78-161">0x0</span></span>   |
| <span data-ttu-id="b4e78-162">DDS \_ ALPHA \_ 模式 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="b4e78-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="b4e78-163">任何 Alpha 通道內容都會假設為使用直接 Alpha。</span><span class="sxs-lookup"><span data-stu-id="b4e78-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="b4e78-164">0x1</span><span class="sxs-lookup"><span data-stu-id="b4e78-164">0x1</span></span>   |
| <span data-ttu-id="b4e78-165">已預乘的 DDS \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="b4e78-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="b4e78-166">任何 Alpha 通道內容都使用預乘 Alpha。</span><span class="sxs-lookup"><span data-stu-id="b4e78-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="b4e78-167">唯一指出此資訊的舊版檔案格式為 ' DX2 ' 和 ' DX4 '。</span><span class="sxs-lookup"><span data-stu-id="b4e78-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="b4e78-168">0x2</span><span class="sxs-lookup"><span data-stu-id="b4e78-168">0x2</span></span>   |
| <span data-ttu-id="b4e78-169">DDS \_ ALPHA \_ 模式不 \_ 透明</span><span class="sxs-lookup"><span data-stu-id="b4e78-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="b4e78-170">所有 Alpha 通道內容都設為完全不透明。</span><span class="sxs-lookup"><span data-stu-id="b4e78-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="b4e78-171">0x3</span><span class="sxs-lookup"><span data-stu-id="b4e78-171">0x3</span></span>   |
| <span data-ttu-id="b4e78-172">DDS \_ ALPHA \_ 模式 \_ 自訂</span><span class="sxs-lookup"><span data-stu-id="b4e78-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="b4e78-173">任何 Alpha 通道內容都是用來作為第四個通道，而不是用來表示 (直接或預乘) 的透明度。</span><span class="sxs-lookup"><span data-stu-id="b4e78-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="b4e78-174">0x4</span><span class="sxs-lookup"><span data-stu-id="b4e78-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="b4e78-175">舊版 D3DX 10 和 [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) 公用程式程式庫將無法載入任何一個。 **MiscFlags2** 不等於零的 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="b4e78-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4e78-176">備註</span><span class="sxs-lookup"><span data-stu-id="b4e78-176">Remarks</span></span>

<span data-ttu-id="b4e78-177">將此結構與 [**dds \_ 標頭**](dds-header.md) 搭配使用，以將資源陣列儲存在 dds 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b4e78-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="b4e78-178">如需詳細資訊，請參閱 [材質陣列](dx-graphics-dds-pguide.md)。</span><span class="sxs-lookup"><span data-stu-id="b4e78-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="b4e78-179">如果 [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)結構的 **dwFourCC** 成員設定為 ' DX10 '，就會出現此標頭。</span><span class="sxs-lookup"><span data-stu-id="b4e78-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e78-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4e78-180">Requirements</span></span>



| <span data-ttu-id="b4e78-181">需求</span><span class="sxs-lookup"><span data-stu-id="b4e78-181">Requirement</span></span> | <span data-ttu-id="b4e78-182">值</span><span class="sxs-lookup"><span data-stu-id="b4e78-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4e78-183">標頭</span><span class="sxs-lookup"><span data-stu-id="b4e78-183">Header</span></span><br/> | <dl> <span data-ttu-id="b4e78-184"><dt>Dd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4e78-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4e78-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4e78-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e78-186">DDS 的參考</span><span class="sxs-lookup"><span data-stu-id="b4e78-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 


---
title: 'D3DX11_IMAGE_LOAD_INFO 結構 (D3DX11tex .h) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 |D3DX11_IMAGE_LOAD_INFO 結構 (D3DX11tex .h) '
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO 結構 Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO 結構指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974709"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="6d7db-107">D3DX11 \_ 映射 \_ 載入 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="6d7db-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="6d7db-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6d7db-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="6d7db-109">選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。</span><span class="sxs-lookup"><span data-stu-id="6d7db-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="6d7db-110">\_任何這些參數的 D3DX11 預設值都會導致 D3DX 自動使用來源檔案的值。</span><span class="sxs-lookup"><span data-stu-id="6d7db-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7db-111">語法</span><span class="sxs-lookup"><span data-stu-id="6d7db-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="6d7db-112">成員</span><span class="sxs-lookup"><span data-stu-id="6d7db-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d7db-113">**寬度**</span><span class="sxs-lookup"><span data-stu-id="6d7db-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-115">材質的目標寬度。</span><span class="sxs-lookup"><span data-stu-id="6d7db-115">The target width of the texture.</span></span> <span data-ttu-id="6d7db-116">如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。</span><span class="sxs-lookup"><span data-stu-id="6d7db-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-117">**高度**</span><span class="sxs-lookup"><span data-stu-id="6d7db-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-119">材質的目標高度。</span><span class="sxs-lookup"><span data-stu-id="6d7db-119">The target height of the texture.</span></span> <span data-ttu-id="6d7db-120">如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。</span><span class="sxs-lookup"><span data-stu-id="6d7db-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-121">**深度**</span><span class="sxs-lookup"><span data-stu-id="6d7db-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-122">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-123">材質的深度。</span><span class="sxs-lookup"><span data-stu-id="6d7db-123">The depth of the texture.</span></span> <span data-ttu-id="6d7db-124">這僅適用于磁片區紋理。</span><span class="sxs-lookup"><span data-stu-id="6d7db-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-125">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="6d7db-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-126">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-127">材質的最高解析度 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="6d7db-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="6d7db-128">如果大於0，則在載入紋理之後，FirstMipLevel 會對應至 mipmap 層級0。</span><span class="sxs-lookup"><span data-stu-id="6d7db-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-129">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="6d7db-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-130">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-131">材質中 mipmap 層級的最大數目。</span><span class="sxs-lookup"><span data-stu-id="6d7db-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="6d7db-132">請參閱 [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)中的備註。</span><span class="sxs-lookup"><span data-stu-id="6d7db-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="6d7db-133">使用0或 D3DX11 \_ 預設值，將會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="6d7db-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-134">**使用量**</span><span class="sxs-lookup"><span data-stu-id="6d7db-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-135">類型： **[ **D3D11 \_ 使用** 方式](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-136">材質資源的使用方式。</span><span class="sxs-lookup"><span data-stu-id="6d7db-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="6d7db-137">請參閱 [**D3D11 \_ 使用量**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)。</span><span class="sxs-lookup"><span data-stu-id="6d7db-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="6d7db-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-139">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-140">將允許紋理系結的管線階段。</span><span class="sxs-lookup"><span data-stu-id="6d7db-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="6d7db-141">請參閱 [**D3D11 \_ BIND \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標。</span><span class="sxs-lookup"><span data-stu-id="6d7db-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-142">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="6d7db-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-143">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-144">Cpu 對材質資源將擁有的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6d7db-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="6d7db-145">請參閱 [**D3D11 \_ CPU \_ 存取 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)標。</span><span class="sxs-lookup"><span data-stu-id="6d7db-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-146">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="6d7db-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-147">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-148">其他資源屬性 (參閱 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 標) 。</span><span class="sxs-lookup"><span data-stu-id="6d7db-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-149">**格式**</span><span class="sxs-lookup"><span data-stu-id="6d7db-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-150">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-151">一個 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉，指出材質載入後的材質格式。</span><span class="sxs-lookup"><span data-stu-id="6d7db-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-152">**Filter**</span><span class="sxs-lookup"><span data-stu-id="6d7db-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-153">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-154">只有在重新取樣) 時，才使用指定的篩選 (篩選材質。</span><span class="sxs-lookup"><span data-stu-id="6d7db-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="6d7db-155">請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="6d7db-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="6d7db-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-157">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d7db-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-158">只有在產生 mipmap) 時，才使用指定的篩選 (來篩選材質 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="6d7db-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="6d7db-159">有效的值為 D3DX11 \_ filter \_ NONE、D3DX11 \_ FILTER \_ POINT、D3DX11 \_ filter \_ 線性或 D3DX11 \_ filter \_ 三角形。</span><span class="sxs-lookup"><span data-stu-id="6d7db-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="6d7db-160">請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="6d7db-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d7db-161">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="6d7db-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6d7db-162">類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d7db-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="6d7db-163">原始影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d7db-163">Information about the original image.</span></span> <span data-ttu-id="6d7db-164">請參閱 [**D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)。</span><span class="sxs-lookup"><span data-stu-id="6d7db-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="6d7db-165">可以使用 [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md)、 [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)或 [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)取得。</span><span class="sxs-lookup"><span data-stu-id="6d7db-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d7db-166">備註</span><span class="sxs-lookup"><span data-stu-id="6d7db-166">Remarks</span></span>

<span data-ttu-id="6d7db-167">在初始化結構時，您可以將任何成員設定為 D3DX11 \_ 預設值，而 D3DX 會在載入紋理時，使用來源材質的預設值將它初始化。</span><span class="sxs-lookup"><span data-stu-id="6d7db-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="6d7db-168">下列 Api 可以使用此結構：</span><span class="sxs-lookup"><span data-stu-id="6d7db-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="6d7db-169">建立資源，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md)。</span><span class="sxs-lookup"><span data-stu-id="6d7db-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="6d7db-170">建立資料處理器，例如 [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) 或 [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md)。</span><span class="sxs-lookup"><span data-stu-id="6d7db-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="6d7db-171">預設值是：</span><span class="sxs-lookup"><span data-stu-id="6d7db-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="6d7db-172">以下是在載入材質時，使用此結構來提供像素格式的簡短範例。</span><span class="sxs-lookup"><span data-stu-id="6d7db-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="6d7db-173">如需完整的程式碼，請參閱 [HDRToneMappingCS11 範例](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx)中的 HDRFormats10 .cpp。</span><span class="sxs-lookup"><span data-stu-id="6d7db-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="6d7db-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d7db-174">Requirements</span></span>



| <span data-ttu-id="6d7db-175">需求</span><span class="sxs-lookup"><span data-stu-id="6d7db-175">Requirement</span></span> | <span data-ttu-id="6d7db-176">值</span><span class="sxs-lookup"><span data-stu-id="6d7db-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7db-177">標頭</span><span class="sxs-lookup"><span data-stu-id="6d7db-177">Header</span></span><br/> | <dl> <span data-ttu-id="6d7db-178"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d7db-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7db-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d7db-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7db-180">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="6d7db-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 


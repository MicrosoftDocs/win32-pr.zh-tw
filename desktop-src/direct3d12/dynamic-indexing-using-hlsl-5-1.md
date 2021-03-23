---
title: 使用 HLSL 5.1 的動態索引
description: D3D12DynamicIndexing 範例示範一些可在著色器模型5.1 中使用的新 HLSL 功能（特別是動態索引和未系結的陣列），以轉譯相同的網格多次，每次轉譯時都有動態選取的材質。 使用動態索引時，著色器現在可以在陣列中編制索引，而不需要在編譯時期知道索引的值。 當結合未系結的陣列時，這會為著色器作者和美工圖案增加另一層間接取值和彈性。
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e41892e7deff23c8d11f8be1c38dac3fcba1de9
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548391"
---
# <a name="dynamic-indexing-using-hlsl-51"></a><span data-ttu-id="544a3-105">使用 HLSL 5.1 的動態索引</span><span class="sxs-lookup"><span data-stu-id="544a3-105">Dynamic Indexing using HLSL 5.1</span></span>

<span data-ttu-id="544a3-106">**D3D12DynamicIndexing** 範例示範一些可在著色器模型5.1 中使用的新 HLSL 功能（特別是動態索引和未系結的陣列），以轉譯相同的網格多次，每次轉譯時都有動態選取的材質。</span><span class="sxs-lookup"><span data-stu-id="544a3-106">The **D3D12DynamicIndexing** sample demonstrates some of the new HLSL features available in Shader Model 5.1 - particularly dynamic indexing and unbounded arrays - to render the same mesh multiple times, each time rendering it with a dynamically selected material.</span></span> <span data-ttu-id="544a3-107">使用動態索引時，著色器現在可以在陣列中編制索引，而不需要在編譯時期知道索引的值。</span><span class="sxs-lookup"><span data-stu-id="544a3-107">With dynamic indexing, shaders can now index into an array without knowing the value of the index at compile time.</span></span> <span data-ttu-id="544a3-108">當結合未系結的陣列時，這會為著色器作者和美工圖案增加另一層間接取值和彈性。</span><span class="sxs-lookup"><span data-stu-id="544a3-108">When combined with unbounded arrays, this adds another level of indirection and flexibility for shader authors and art pipelines.</span></span>

-   [<span data-ttu-id="544a3-109">設定圖元著色器</span><span class="sxs-lookup"><span data-stu-id="544a3-109">Set up the pixel shader</span></span>](#set-up-the-pixel-shader)
-   [<span data-ttu-id="544a3-110">設定根簽章</span><span class="sxs-lookup"><span data-stu-id="544a3-110">Set up the root signature</span></span>](#set-up-the-root-signature)
-   [<span data-ttu-id="544a3-111">建立紋理</span><span class="sxs-lookup"><span data-stu-id="544a3-111">Create the textures</span></span>](#create-the-textures)
-   [<span data-ttu-id="544a3-112">上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="544a3-112">Upload the texture data</span></span>](#upload-the-texture-data)
-   [<span data-ttu-id="544a3-113">載入擴散材質</span><span class="sxs-lookup"><span data-stu-id="544a3-113">Load the diffuse texture</span></span>](#load-the-diffuse-texture)
-   [<span data-ttu-id="544a3-114">建立取樣器</span><span class="sxs-lookup"><span data-stu-id="544a3-114">Create a sampler</span></span>](#create-a-sampler)
-   [<span data-ttu-id="544a3-115">動態變更根參數索引</span><span class="sxs-lookup"><span data-stu-id="544a3-115">Dynamically change the root parameter index</span></span>](#dynamically-change-the-root-parameter-index)
-   [<span data-ttu-id="544a3-116">執行範例</span><span class="sxs-lookup"><span data-stu-id="544a3-116">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="544a3-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="544a3-117">Related topics</span></span>](#related-topics)

## <a name="set-up-the-pixel-shader"></a><span data-ttu-id="544a3-118">設定圖元著色器</span><span class="sxs-lookup"><span data-stu-id="544a3-118">Set up the pixel shader</span></span>

<span data-ttu-id="544a3-119">讓我們先看看著色器本身，此範例是圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="544a3-119">Let's first look at the shader itself, which for this sample is a pixel shader.</span></span>

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

<span data-ttu-id="544a3-120">陣列會說明未系結的陣列功能， `g_txMats[]` 因為它不會指定陣列大小。</span><span class="sxs-lookup"><span data-stu-id="544a3-120">The unbounded array feature is illustrated by the `g_txMats[]` array as it does not specify an array size.</span></span> <span data-ttu-id="544a3-121">動態索引是用來建立與的索引 `g_txMats[]` `matIndex` ，其定義為根常數。</span><span class="sxs-lookup"><span data-stu-id="544a3-121">Dynamic indexing is used to index into `g_txMats[]` with `matIndex`, which is defined as a root constant.</span></span> <span data-ttu-id="544a3-122">著色器在編譯時期不知道大小或陣列或索引的值。</span><span class="sxs-lookup"><span data-stu-id="544a3-122">The shader has no knowledge of the size or the array or the value of the index at compile-time.</span></span> <span data-ttu-id="544a3-123">這兩個屬性都是在與著色器搭配使用之管線狀態物件的根簽章中定義。</span><span class="sxs-lookup"><span data-stu-id="544a3-123">Both attributes are defined in the root signature of the pipeline state object used with the shader.</span></span>

<span data-ttu-id="544a3-124">若要利用 HLSL 中的動態索引功能，需要使用 SM 5.1 來編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="544a3-124">To take advantage of the dynamic indexing features in HLSL requires that the shader be compiled with SM 5.1.</span></span> <span data-ttu-id="544a3-125">此外，若要利用未系結的陣列，也必須使用/enable 未系結的 **\_ 描述元 \_ \_ 資料表** 旗標。</span><span class="sxs-lookup"><span data-stu-id="544a3-125">Additionally, to make use of unbounded arrays, the **/enable\_unbounded\_descriptor\_tables** flag must also be used.</span></span> <span data-ttu-id="544a3-126">下列命令列選項可用來使用 [效果編譯器工具](/windows/desktop/direct3dtools/fxc) (fxc.exe) 來編譯此著色器：</span><span class="sxs-lookup"><span data-stu-id="544a3-126">The following command line options are used to compile this shader with the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC):</span></span>

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a><span data-ttu-id="544a3-127">設定根簽章</span><span class="sxs-lookup"><span data-stu-id="544a3-127">Set up the root signature</span></span>

<span data-ttu-id="544a3-128">現在，讓我們看看根簽章定義，尤其是我們如何定義未系結陣列的大小，以及將根常數連結至 `matIndex` 。</span><span class="sxs-lookup"><span data-stu-id="544a3-128">Now, let's look at the root signature definition, particularly, how we define the size of the unbounded array and link a root constant to `matIndex`.</span></span> <span data-ttu-id="544a3-129">針對圖元著色器，我們會定義三個專案： SRVs 的描述項資料表 (我們的 Texture2Ds) 、取樣器的描述中繼資料表，以及單一根常數。</span><span class="sxs-lookup"><span data-stu-id="544a3-129">For the pixel shader, we define three things: a descriptor table for SRVs (our Texture2Ds), a descriptor table for Samplers and a single root constant.</span></span> <span data-ttu-id="544a3-130">SRVs 的描述項資料表包含 `CityMaterialCount + 1` 專案。</span><span class="sxs-lookup"><span data-stu-id="544a3-130">The descriptor table for our SRVs contains `CityMaterialCount + 1` entries.</span></span> <span data-ttu-id="544a3-131">`CityMaterialCount` 這是定義長度的常數， `g_txMats[]` + 1 是的 `g_txDiffuse` 。</span><span class="sxs-lookup"><span data-stu-id="544a3-131">`CityMaterialCount` is a constant that defines the length of `g_txMats[]` and the + 1 is for `g_txDiffuse`.</span></span> <span data-ttu-id="544a3-132">取樣器的描述中繼資料表只包含一個專案，而我們只會在 **LoadAssets** 方法中透過 **InitAsConstants** ( ... ) 來定義 1 32 位的根常數值。</span><span class="sxs-lookup"><span data-stu-id="544a3-132">The descriptor table for our Samplers contains only one entry and we only define one 32-bit root constant value via **InitAsConstants**(…)., in the **LoadAssets** method.</span></span>

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| <span data-ttu-id="544a3-133">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-133">Call flow</span></span>                                                             | <span data-ttu-id="544a3-134">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-134">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="544a3-135">**CD3DX12 \_ 描述元 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="544a3-135">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="544a3-136">**D3D12 \_ 描述項 \_ 範圍 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="544a3-136">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="544a3-137">**CD3DX12 \_ 根 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="544a3-137">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="544a3-138">**D3D12 \_ 著色器 \_ 可見度**</span><span class="sxs-lookup"><span data-stu-id="544a3-138">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="544a3-139">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="544a3-139">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="544a3-140">**D3D12 \_ 根簽章 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="544a3-140">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="544a3-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="544a3-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="544a3-142">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="544a3-142">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="544a3-143">**D3D \_ 根簽章 \_ \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="544a3-143">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="544a3-144">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="544a3-144">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a><span data-ttu-id="544a3-145">建立紋理</span><span class="sxs-lookup"><span data-stu-id="544a3-145">Create the textures</span></span>

<span data-ttu-id="544a3-146">的內容 `g_txMats[]` 是在 **LoadAssets** 中建立的 cti 產生紋理。</span><span class="sxs-lookup"><span data-stu-id="544a3-146">The contents of `g_txMats[]` are procedurally generated textures created in **LoadAssets**.</span></span> <span data-ttu-id="544a3-147">在場景中轉譯的每個城市都會共用相同的擴散材質，但每個城市也都有自己的 cti 產生材質。</span><span class="sxs-lookup"><span data-stu-id="544a3-147">Each city rendered in the scene shares the same diffuse texture but each also has its own procedurally generated texture.</span></span> <span data-ttu-id="544a3-148">紋理的陣列橫跨彩虹頻譜，可輕鬆地將索引技術視覺化。</span><span class="sxs-lookup"><span data-stu-id="544a3-148">The array of textures span the rainbow spectrum to easily visualize the indexing technique.</span></span>

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="544a3-149">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-149">Call flow</span></span></th>
<th><span data-ttu-id="544a3-150">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-150">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="544a3-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="544a3-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="544a3-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) </span><span class="sxs-lookup"><span data-stu-id="544a3-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="544a3-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="544a3-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="544a3-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) </span><span class="sxs-lookup"><span data-stu-id="544a3-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br /><span data-ttu-id="544a3-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="544a3-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) </span><span class="sxs-lookup"><span data-stu-id="544a3-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span></span><br /><span data-ttu-id="544a3-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>] (/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb) </span><span class="sxs-lookup"><span data-stu-id="544a3-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>](/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a><span data-ttu-id="544a3-164">上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="544a3-164">Upload the texture data</span></span>

<span data-ttu-id="544a3-165">透過上傳堆積將材質資料上傳至 GPU，並為每個資料集建立 SRVs，並儲存在 SRV 描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="544a3-165">Texture data is uploaded to the GPU via an upload heap and SRVs are created for each and stored in an SRV descriptor heap.</span></span>

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="544a3-166">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-166">Call flow</span></span></th>
<th><span data-ttu-id="544a3-167">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-167">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="544a3-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="544a3-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="544a3-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="544a3-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="544a3-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="544a3-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="544a3-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="544a3-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a><span data-ttu-id="544a3-180">載入擴散材質</span><span class="sxs-lookup"><span data-stu-id="544a3-180">Load the diffuse texture</span></span>

<span data-ttu-id="544a3-181">擴散材質 g \_ `txDiffuse` 會以類似的方式上傳，而且也會取得自己的 SRV，但材質資料已在 occcity 中定義。</span><span class="sxs-lookup"><span data-stu-id="544a3-181">The diffuse texture, g\_`txDiffuse`, is uploaded in a similar manner and also gets its own SRV, but the texture data is already defined in occcity.bin.</span></span>

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="544a3-182">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-182">Call flow</span></span></th>
<th><span data-ttu-id="544a3-183">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-183">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="544a3-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="544a3-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="544a3-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="544a3-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="544a3-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="544a3-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="544a3-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="544a3-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="544a3-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="544a3-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="544a3-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="544a3-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="544a3-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="544a3-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a><span data-ttu-id="544a3-204">建立取樣器</span><span class="sxs-lookup"><span data-stu-id="544a3-204">Create a sampler</span></span>

<span data-ttu-id="544a3-205">最後， **LoadAssets** 會從擴散材質或紋理陣列建立單一取樣器來進行取樣。</span><span class="sxs-lookup"><span data-stu-id="544a3-205">Finally for **LoadAssets**, a single sampler is created to sample from either the diffuse texture or the texture array.</span></span>

``` syntax
 // Describe and create a sampler.
        D3D12_SAMPLER_DESC samplerDesc = {};
        samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
        samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.MinLOD = 0;
        samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
        samplerDesc.MipLODBias = 0.0f;
        samplerDesc.MaxAnisotropy = 1;
        samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
        m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="544a3-206">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-206">Call flow</span></span></th>
<th><span data-ttu-id="544a3-207">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-207">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="544a3-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span></span><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
<span data-ttu-id="544a3-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>常數</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="544a3-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>Constants</strong></a>)</span></span><br /><span data-ttu-id="544a3-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="544a3-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="544a3-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="544a3-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="544a3-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="544a3-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="544a3-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="544a3-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="544a3-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="544a3-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="544a3-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="544a3-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="544a3-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a><span data-ttu-id="544a3-224">動態變更根參數索引</span><span class="sxs-lookup"><span data-stu-id="544a3-224">Dynamically change the root parameter index</span></span>

<span data-ttu-id="544a3-225">如果我們現在要轉譯場景，所有城市都會相同，因為我們沒有設定根常數的值 `matIndex` 。</span><span class="sxs-lookup"><span data-stu-id="544a3-225">If we were to render the scene now, all of the cities would appear the same, because we have not set the value of our root constant, `matIndex`.</span></span> <span data-ttu-id="544a3-226">每個圖元著色器都會在的第0個位置編制索引 `g_txMats` ，而場景看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="544a3-226">Each pixel shader would index into the 0th slot of `g_txMats` and the scene would look like this:</span></span>

![所有城市都會顯示相同的色彩](images/dynamicindexing-image1.png)

<span data-ttu-id="544a3-228">根常數的值是在 **FrameResource：:P opulatecommandlists** 中設定。</span><span class="sxs-lookup"><span data-stu-id="544a3-228">The value of the root constant is set in **FrameResource::PopulateCommandLists**.</span></span> <span data-ttu-id="544a3-229">在針對每個城市記錄 draw 命令 **的雙精度** 浮點數中，我們會記錄 [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) 的呼叫，並在根簽章中指定我們的根參數索引（在此案例中為3–動態索引的值和位移）（在此案例中為0）。</span><span class="sxs-lookup"><span data-stu-id="544a3-229">In the double **for** loop where a draw command is recorded for each city, we record a call to [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) specifying our root parameter index in regards to the root signature – in this case 3 – the value of the dynamic index and an offset – in this case 0.</span></span> <span data-ttu-id="544a3-230">由於的長度 `g_txMats` 等於我們轉譯的城市數目，因此會以累加方式為每個城市設定索引的值。</span><span class="sxs-lookup"><span data-stu-id="544a3-230">Since the length of `g_txMats` is equal to the number of cities we render, the value of the index is incrementally set for each city.</span></span>

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| <span data-ttu-id="544a3-231">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="544a3-231">Call flow</span></span>                                                                                          | <span data-ttu-id="544a3-232">參數</span><span class="sxs-lookup"><span data-stu-id="544a3-232">Parameters</span></span> |
|----------------------------------------------------------------------------------------------------|------------|
| [<span data-ttu-id="544a3-233">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="544a3-233">**SetPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [<span data-ttu-id="544a3-234">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="544a3-234">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [<span data-ttu-id="544a3-235">**SetGraphicsRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="544a3-235">**SetGraphicsRootDescriptorTable**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [<span data-ttu-id="544a3-236">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="544a3-236">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a><span data-ttu-id="544a3-237">執行範例</span><span class="sxs-lookup"><span data-stu-id="544a3-237">Run the sample</span></span>

<span data-ttu-id="544a3-238">現在當我們轉譯場景時，每個城市都會有不同的值， `matIndex` 因此會查詢不同的材質， `g_txMats[]` 使場景看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="544a3-238">Now when we render the scene, each city will have a different value for `matIndex` and will thus look up a different texture from `g_txMats[]` making the scene look like this:</span></span>

![所有城市都會以不同的色彩顯示](images/dynamicindexing-image2.png)

## <a name="related-topics"></a><span data-ttu-id="544a3-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="544a3-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="544a3-241">D3D12 程式碼逐步解說-解說</span><span class="sxs-lookup"><span data-stu-id="544a3-241">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="544a3-242">效果-編譯器工具</span><span class="sxs-lookup"><span data-stu-id="544a3-242">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="544a3-243">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="544a3-243">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="544a3-244">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="544a3-244">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="544a3-245">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="544a3-245">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="544a3-246">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="544a3-246">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

---
description: DirectX SDK 中包含的 PRTDemo 範例和 PRTCmdLine 模擬器代表網格頂點的傳輸向量。
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: 使用 (Direct3D 9) 的材質表示 PRT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187547"
---
# <a name="representing-prt-with-textures-direct3d-9"></a><span data-ttu-id="99dd3-103">使用 (Direct3D 9) 的材質表示 PRT</span><span class="sxs-lookup"><span data-stu-id="99dd3-103">Representing PRT With Textures (Direct3D 9)</span></span>

<span data-ttu-id="99dd3-104">DirectX SDK 中包含的 PRTDemo 範例和 PRTCmdLine 模擬器代表網格頂點的傳輸向量。</span><span class="sxs-lookup"><span data-stu-id="99dd3-104">The PRTDemo sample and PRTCmdLine simulator included in the DirectX SDK represent transfer vectors at the vertices of a mesh.</span></span> <span data-ttu-id="99dd3-105">為了精確代表 PRT 的信號，這可能需要鑲嵌，對於目前的遊戲來說可能不切實際。</span><span class="sxs-lookup"><span data-stu-id="99dd3-105">In order to represent the PRT signal accurately, this can require tessellations that may be impractical for current games.</span></span> <span data-ttu-id="99dd3-106">代表材質地圖中的傳輸向量是替代方法，其資料成本與網格複雜度無關。</span><span class="sxs-lookup"><span data-stu-id="99dd3-106">Representing transfer vectors in texture maps is an alternative approach that has the same data cost independent of mesh complexity.</span></span> <span data-ttu-id="99dd3-107">有幾種方式可使用 D3DX PRT 程式庫產生傳輸向量紋理對應。</span><span class="sxs-lookup"><span data-stu-id="99dd3-107">There are several ways to generate transfer vector texture maps using the D3DX PRT Library.</span></span>

## <a name="precomputing-transfer-vectors"></a><span data-ttu-id="99dd3-108">一般來說傳輸向量</span><span class="sxs-lookup"><span data-stu-id="99dd3-108">Precomputing Transfer Vectors</span></span>

<span data-ttu-id="99dd3-109">其中一個方法是修改 PRTDemo 和 PRTCmdLine 範例，以在介面參數化中的每個材質計算傳輸向量。</span><span class="sxs-lookup"><span data-stu-id="99dd3-109">One approach would be to modify the PRTDemo and PRTCmdLine samples to compute a transfer vector at every texel in a parameterization of a surface.</span></span> <span data-ttu-id="99dd3-110">若要這樣做：</span><span class="sxs-lookup"><span data-stu-id="99dd3-110">To do this:</span></span>

1.  <span data-ttu-id="99dd3-111">修改 [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) 的呼叫，以從網格中解壓縮紋理座標 (ExtractUVs 必須是 **TRUE**) </span><span class="sxs-lookup"><span data-stu-id="99dd3-111">Modify the call to [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to extract texture coordinates from the mesh (ExtractUVs must be **TRUE**)</span></span>
2.  <span data-ttu-id="99dd3-112">使用相同的材質大小，以 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)取代 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="99dd3-112">Replace [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) calls with [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) using the same texture size.</span></span>

<span data-ttu-id="99dd3-113">所有 ID3DXPRTEngine 方法都適用于每個材質的模擬，但： ComputeBounceAdaptive、ComputeSSAdaptive、ComputeSS 和 ComputeDirectLightingSHAdaptive 除外。</span><span class="sxs-lookup"><span data-stu-id="99dd3-113">All ID3DXPRTEngine methods work with per-texel simulations except for: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS, and ComputeDirectLightingSHAdaptive.</span></span> <span data-ttu-id="99dd3-114">雖然材質空間模擬會產生正確的結果，但通常可能很慢，因為很可能會以高密度的方式計算傳輸向量。</span><span class="sxs-lookup"><span data-stu-id="99dd3-114">While texture-space simulation will generate the correct result, it can often be fairly slow since it will most likely be computing transfer vectors at a high density.</span></span>

<span data-ttu-id="99dd3-115">另一種方法是計算可調整的每個頂點 PRT 模擬 (以及將用於每個材質資料) 的材質座標，然後呼叫 [**ID3DXPRTEngine：： ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (使用以 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) 建立的輸出緩衝區（在適當的解析) 中）。</span><span class="sxs-lookup"><span data-stu-id="99dd3-115">Another approach is to compute an adaptive per-vertex PRT simulation (with texture coordinates that will be used for the per-texel data) and then call [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (using an output buffer created using [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) at the appropriate resolution).</span></span> <span data-ttu-id="99dd3-116">這適用于 SDK 中的所有 D3DX PRT 功能，而且通常會比直接計算每個材質傳輸緩衝區更有效率。</span><span class="sxs-lookup"><span data-stu-id="99dd3-116">This works with all D3DX PRT functionality in the SDK and can often be much more efficient than directly computing a per-texel transfer buffer.</span></span>

## <a name="runtime-calculations"></a><span data-ttu-id="99dd3-117">執行時間計算</span><span class="sxs-lookup"><span data-stu-id="99dd3-117">Runtime Calculations</span></span>

<span data-ttu-id="99dd3-118">如果使用單一叢集，則可以像任何其他材質一樣篩選和 mip 對應結果，而圖元著色器與 PRTDemo 隨附的頂點著色器程式碼相同。</span><span class="sxs-lookup"><span data-stu-id="99dd3-118">If a single cluster is used the results can be filtered and mip-mapped like any other texture and the pixel shader is identical to the vertex shader code that ships with PRTDemo.</span></span>

<span data-ttu-id="99dd3-119">如果壓縮產生多個叢集，您就無法篩選或 mipmap 資料，因為叢集索引不是連續的。</span><span class="sxs-lookup"><span data-stu-id="99dd3-119">If compression generates multiple clusters, you cannot filter or mipmap the data because clustering indexes are not continuous.</span></span> <span data-ttu-id="99dd3-120">以下是處理多叢集資料的一些替代方案：</span><span class="sxs-lookup"><span data-stu-id="99dd3-120">Here are some alternatives for handling multi-clustered data:</span></span>

-   <span data-ttu-id="99dd3-121">在圖元著色器中自行進行篩選。</span><span class="sxs-lookup"><span data-stu-id="99dd3-121">Do all of the filtering yourself in the pixel shader.</span></span> <span data-ttu-id="99dd3-122">可惜的是，基於效能的考慮，這通常是不切實際的。</span><span class="sxs-lookup"><span data-stu-id="99dd3-122">Unfortunately, this is generally impractical for performance reasons.</span></span>
-   <span data-ttu-id="99dd3-123">如果紋理是低解析度的非 mip 對應紋理 (ie：輕量地圖) ，只要直接在材質空間中計算光源（不會進行篩選），就可能更有效率，並以陰影材質呈現物件。</span><span class="sxs-lookup"><span data-stu-id="99dd3-123">If the textures are low resolution non mip-mapped textures (ie: light maps), it is most likely more efficient to just compute the lighting directly in texture space - where no filtering will occur, and render the object with a shaded texture.</span></span> <span data-ttu-id="99dd3-124">這基本上是完全在 GPU 上建立的動態燈光地圖。</span><span class="sxs-lookup"><span data-stu-id="99dd3-124">This is essentially a dynamic light map that is created entirely on the GPU.</span></span>
-   <span data-ttu-id="99dd3-125">如果使用了材質塔 (請參閱 [使用 UVAtlas (Direct3D 9) ](using-uvatlas.md)) ，您可以藉由將材質空間中已連接元件中的所有傳輸向量都在相同的叢集中，以手動方式叢集場景。</span><span class="sxs-lookup"><span data-stu-id="99dd3-125">If a texture atlas is used (see [Using UVAtlas (Direct3D 9)](using-uvatlas.md)), you could manually cluster the scene by having all transfer vectors in a connected component in texture space be in the same cluster.</span></span> <span data-ttu-id="99dd3-126">如此一來，您就可以篩選材質，因為所有存取的材質都是在相同的叢集中。</span><span class="sxs-lookup"><span data-stu-id="99dd3-126">This way you can filter the texture because all texels accessed would be in the same cluster by construction.</span></span> <span data-ttu-id="99dd3-127">指定臉部的叢集識別碼可以從頂點著色器傳播。</span><span class="sxs-lookup"><span data-stu-id="99dd3-127">The cluster ID for a given face could be propagated from the vertex shader.</span></span>

<span data-ttu-id="99dd3-128">圖元著色器的常數暫存器數目較少，因此圖元著色器與頂點著色器有點不同。</span><span class="sxs-lookup"><span data-stu-id="99dd3-128">Pixel shaders have much fewer constant registers that cannot be indexed, so the pixel shader is somewhat different than the vertex shader.</span></span> <span data-ttu-id="99dd3-129">將每個叢集的工作儲存在低解析度的動態材質中，並使用材質載入，會是使用多個叢集時最有效率的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="99dd3-129">Storing the per-cluster work in a low resolution dynamic texture and using texture loads would be the most efficient way to render when using multiple clusters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99dd3-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="99dd3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99dd3-131">預先計算 Radiance 傳輸</span><span class="sxs-lookup"><span data-stu-id="99dd3-131">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> <dt>

<span data-ttu-id="99dd3-132">[PRT 示範範例](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="99dd3-132">[PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span></span>
</dt> <dt>

<span data-ttu-id="99dd3-133">[PRT 模擬器 (prtcmdline.exe) ](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="99dd3-133">[PRT Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 




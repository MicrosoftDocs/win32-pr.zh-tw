---
title: 鑲嵌階段
description: Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "104316663"
---
# <a name="tessellation-stages"></a><span data-ttu-id="9df20-103">鑲嵌階段</span><span class="sxs-lookup"><span data-stu-id="9df20-103">Tessellation Stages</span></span>

<span data-ttu-id="9df20-104">Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。</span><span class="sxs-lookup"><span data-stu-id="9df20-104">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="9df20-105">鑲嵌並排顯示高位表面 (或將其分裂) 成為適合轉譯的結構。</span><span class="sxs-lookup"><span data-stu-id="9df20-105">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span>

<span data-ttu-id="9df20-106">藉由在硬體中實作鑲嵌，圖形管線可以評估較低細節的 (較少的多邊形數) 模型並以更高細節呈現。</span><span class="sxs-lookup"><span data-stu-id="9df20-106">By implementing tessellation in hardware, a graphics pipeline can evaluate lower detail (lower polygon count) models and render in higher detail.</span></span> <span data-ttu-id="9df20-107">雖然軟體鑲嵌是可做到的，但硬體實作的鑲嵌會產生不可思議的視覺細節數量 (包括位移對應的支援)，而不需要新增模型大小的視覺細節和造成運作癱瘓的更新頻率。</span><span class="sxs-lookup"><span data-stu-id="9df20-107">While software tessellation can be done, tessellation implemented by hardware can generate an incredible amount of visual detail (including support for displacement mapping) without adding the visual detail to the model sizes and paralyzing refresh rates.</span></span>

-   [<span data-ttu-id="9df20-108">鑲嵌式優點</span><span class="sxs-lookup"><span data-stu-id="9df20-108">Tessellation Benefits</span></span>](#tessellation-benefits)
-   [<span data-ttu-id="9df20-109">新管線階段</span><span class="sxs-lookup"><span data-stu-id="9df20-109">New Pipeline Stages</span></span>](#new-pipeline-stages)
    -   [<span data-ttu-id="9df20-110">輪廓-著色器階段</span><span class="sxs-lookup"><span data-stu-id="9df20-110">Hull-Shader Stage</span></span>](#hull-shader-stage)
    -   [<span data-ttu-id="9df20-111">鑲嵌階段</span><span class="sxs-lookup"><span data-stu-id="9df20-111">Tessellator Stage</span></span>](#tessellator-stage)
    -   [<span data-ttu-id="9df20-112">網域著色器階段</span><span class="sxs-lookup"><span data-stu-id="9df20-112">Domain-Shader Stage</span></span>](#domain-shader-stage)
-   [<span data-ttu-id="9df20-113">用於初始化鑲嵌階段的 Api</span><span class="sxs-lookup"><span data-stu-id="9df20-113">APIs for initializing Tessellation Stages</span></span>](#apis-for-initializing-tessellation-stages)
-   [<span data-ttu-id="9df20-114">作法：</span><span class="sxs-lookup"><span data-stu-id="9df20-114">How to's:</span></span>](#how-tos)
-   [<span data-ttu-id="9df20-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9df20-115">Related topics</span></span>](#related-topics)

## <a name="tessellation-benefits"></a><span data-ttu-id="9df20-116">鑲嵌式優點</span><span class="sxs-lookup"><span data-stu-id="9df20-116">Tessellation Benefits</span></span>

<span data-ttu-id="9df20-117">鑲嵌：</span><span class="sxs-lookup"><span data-stu-id="9df20-117">Tessellation:</span></span>

-   <span data-ttu-id="9df20-118">節省大量的記憶體和頻寬，讓應用程式能夠從低解析度模型轉譯更高的詳細表面。</span><span class="sxs-lookup"><span data-stu-id="9df20-118">Saves lots of memory and bandwidth, which allows an application to render higher detailed surfaces from low-resolution models.</span></span> <span data-ttu-id="9df20-119">在 Direct3D 11 管線中執行的鑲嵌技術也支援置換對應，這可能會產生出色數量的表面詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9df20-119">The tessellation technique implemented in the Direct3D 11 pipeline also supports displacement mapping, which can produce stunning amounts of surface detail.</span></span>
-   <span data-ttu-id="9df20-120">支援可擴充轉譯技術，例如可即時計算的連續或視野相依細節層級。</span><span class="sxs-lookup"><span data-stu-id="9df20-120">Supports scalable-rendering techniques, such as continuous or view dependent levels-of-detail which can be calculated on the fly.</span></span>
-   <span data-ttu-id="9df20-121">以較低頻率執行昂貴的計算 (在較低的詳細模型) 上執行計算，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="9df20-121">Improves performance by performing expensive computations at lower frequency (doing calculations on a lower-detail model).</span></span> <span data-ttu-id="9df20-122">這可能包括將混合形狀或變形目標 (morph target) 用於寫實動畫的混合計算，或用於撞擊偵測或軟體動力 (soft body dynamics) 的物理計算。</span><span class="sxs-lookup"><span data-stu-id="9df20-122">This could include blending calculations using blend shapes or morph targets for realistic animation or physics calculations for collision detection or soft body dynamics.</span></span>

<span data-ttu-id="9df20-123">Direct3D 11 管線可在硬體中實行鑲嵌式，以將 CPU 的工作從 CPU 載入至 GPU。</span><span class="sxs-lookup"><span data-stu-id="9df20-123">The Direct3D 11 pipeline implements tessellation in hardware, which off-loads the work from the CPU to the GPU.</span></span> <span data-ttu-id="9df20-124">如果應用程式實作大量變形目標和/或更加複雜的皮膚形變 (skinning)/變形模型，這可能會導致非常大的效能改進。</span><span class="sxs-lookup"><span data-stu-id="9df20-124">This can lead to very large performance improvements if an application implements large numbers of morph targets and/or more sophisticated skinning/deformation models.</span></span> <span data-ttu-id="9df20-125">若要存取新的鑲嵌式功能，您必須瞭解一些新的管線階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-125">To access the new tessellation features, you must learn about some new pipeline stages.</span></span>

## <a name="new-pipeline-stages"></a><span data-ttu-id="9df20-126">新管線階段</span><span class="sxs-lookup"><span data-stu-id="9df20-126">New Pipeline Stages</span></span>

<span data-ttu-id="9df20-127">鑲嵌使用 GPU，從四邊形塊面 (quad patch)、三角形塊面 (triangle patch) 或等高線 (isoline) 建構而來的表面計算更詳細的表面。</span><span class="sxs-lookup"><span data-stu-id="9df20-127">Tessellation uses the GPU to calculate a more detailed surface from a surface constructed from quad patches, triangle patches or isolines.</span></span> <span data-ttu-id="9df20-128">為了近似高位表面，每個塊面細分成三角形、點或使用鑲嵌因數的線。</span><span class="sxs-lookup"><span data-stu-id="9df20-128">To approximate the high-ordered surface, each patch is subdivided into triangles, points, or lines using tessellation factors.</span></span> <span data-ttu-id="9df20-129">Direct3D 11 管線會使用三個新的管線階段來實行鑲嵌：</span><span class="sxs-lookup"><span data-stu-id="9df20-129">The Direct3D 11 pipeline implements tessellation using three new pipeline stages:</span></span>

-   <span data-ttu-id="9df20-130">輪廓[-著色器階段](#hull-shader-stage)-一種可程式化的著色器階段，會產生幾何修補程式 (和修補常數，) 對應至每個輸入修補程式 (四、三角形或行) 。</span><span class="sxs-lookup"><span data-stu-id="9df20-130">[Hull-Shader Stage](#hull-shader-stage) - A programmable shader stage that produces a geometry patch (and patch constants) that correspond to each input patch (quad, triangle, or line).</span></span>
-   <span data-ttu-id="9df20-131">[鑲嵌階段](#tessellator-stage) -固定的函式管線階段，可建立代表幾何修補程式之定義域的取樣模式，並產生一組較小的物件， (三角形、點或線) 連接這些範例。</span><span class="sxs-lookup"><span data-stu-id="9df20-131">[Tessellator Stage](#tessellator-stage) - A fixed function pipeline stage that creates a sampling pattern of the domain that represents the geometry patch and generates a set of smaller objects (triangles, points, or lines) that connect these samples.</span></span>
-   <span data-ttu-id="9df20-132">[網域著色器階段](#domain-shader-stage) -可程式化的著色器階段，可計算對應至每個網域範例的頂點位置。</span><span class="sxs-lookup"><span data-stu-id="9df20-132">[Domain-Shader Stage](#domain-shader-stage) - A programmable shader stage that calculates the vertex position that corresponds to each domain sample.</span></span>

<span data-ttu-id="9df20-133">下圖強調 Direct3D 11 管線的新階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-133">The following diagram highlights the new stages of the Direct3D 11 pipeline.</span></span>

![direct3d 11 管線圖，反白顯示輪廓著色器、曲面細分器和網域著色器階段](images/d3d11-pipeline-stages-tessellation.png)

<span data-ttu-id="9df20-135">下圖顯示鑲嵌階段的進展。</span><span class="sxs-lookup"><span data-stu-id="9df20-135">The following diagram shows the progression through the tessellation stages.</span></span> <span data-ttu-id="9df20-136">從低細節的細分表面開始進展。</span><span class="sxs-lookup"><span data-stu-id="9df20-136">The progression starts with the low-detail subdivision surface.</span></span> <span data-ttu-id="9df20-137">進展接下來會使用對應幾何塊面、網域樣本，和連接這些樣本的三角形，反白顯示輸入塊面。</span><span class="sxs-lookup"><span data-stu-id="9df20-137">The progression next highlights the input patch with the corresponding geometry patch, domain samples, and triangles that connect these samples.</span></span> <span data-ttu-id="9df20-138">進展最後會反白顯示對應於這些樣本的頂點。</span><span class="sxs-lookup"><span data-stu-id="9df20-138">The progression finally highlights the vertices that correspond to these samples.</span></span>

![鑲嵌進展圖](images/tess-prog.png)

### <a name="hull-shader-stage"></a><span data-ttu-id="9df20-140">Hull-Shader 階段</span><span class="sxs-lookup"><span data-stu-id="9df20-140">Hull-Shader Stage</span></span>

<span data-ttu-id="9df20-141">輪廓著色器--每個修補程式都會叫用一次--將定義低序位表面的輸入控制點，轉換成構成修補程式的控制點。</span><span class="sxs-lookup"><span data-stu-id="9df20-141">A hull shader -- which is invoked once per patch -- transforms input control points that define a low-order surface into control points that make up a patch.</span></span> <span data-ttu-id="9df20-142">它也會執行一些每個修補程式計算，以提供鑲嵌階段和網域階段的資料。</span><span class="sxs-lookup"><span data-stu-id="9df20-142">It also does some per patch calculations to provide data for the tessellation stage and the domain stage.</span></span> <span data-ttu-id="9df20-143">在最簡單的黑箱層級中，輪廓著色器階段看起來會像下圖。</span><span class="sxs-lookup"><span data-stu-id="9df20-143">At the simplest black-box level, the hull-shader stage would look something like the following diagram.</span></span>

![輪廓著色器階段圖](images/d3d11-hull-shader.png)

<span data-ttu-id="9df20-145">輪廓著色器會使用 HLSL 函式來執行，並具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9df20-145">A hull shader is implemented with an HLSL function, and has the following properties:</span></span>

-   <span data-ttu-id="9df20-146">著色器輸入介於1到32的控制點之間。</span><span class="sxs-lookup"><span data-stu-id="9df20-146">The shader input is between 1 and 32 control points.</span></span>
-   <span data-ttu-id="9df20-147">著色器輸出介於 1 到 32 個控制點之間，無論鑲嵌係數的數目為何。</span><span class="sxs-lookup"><span data-stu-id="9df20-147">The shader output is between 1 and 32 control points, regardless of the number of tessellation factors.</span></span> <span data-ttu-id="9df20-148">輪廓著色器的控制點輸出可以由網域著色器階段取用。</span><span class="sxs-lookup"><span data-stu-id="9df20-148">The control-points output from a hull shader can be consumed by the domain-shader stage.</span></span> <span data-ttu-id="9df20-149">網域著色器可以使用修補程式常數資料;鑲嵌因數可由網域著色器和鑲嵌階段取用。</span><span class="sxs-lookup"><span data-stu-id="9df20-149">Patch constant data can be consumed by a domain shader; tessellation factors can be consumed by the domain shader and the tessellation stage.</span></span>
-   <span data-ttu-id="9df20-150">鑲嵌係數決定每個塊面要細分成多少數目。</span><span class="sxs-lookup"><span data-stu-id="9df20-150">Tessellation factors determine how much to subdivide each patch.</span></span>
-   <span data-ttu-id="9df20-151">著色器會宣告鑲嵌階段所需的狀態。</span><span class="sxs-lookup"><span data-stu-id="9df20-151">The shader declares the state required by the tessellator stage.</span></span> <span data-ttu-id="9df20-152">這些資訊包括控制點數目、塊面的類型，以及鑲嵌時分割使用的類型。</span><span class="sxs-lookup"><span data-stu-id="9df20-152">This includes information such as the number of control points, the type of patch face and the type of partitioning to use when tessellating.</span></span> <span data-ttu-id="9df20-153">這項資訊會顯示為宣告，通常是在著色器程式碼的前方。</span><span class="sxs-lookup"><span data-stu-id="9df20-153">This information appears as declarations typically at the front of the shader code.</span></span>
-   <span data-ttu-id="9df20-154">如果輪廓著色器階段將任何邊緣鑲嵌因數設定為 = 0 或 NaN，則會挑選修補程式。</span><span class="sxs-lookup"><span data-stu-id="9df20-154">If the hull-shader stage sets any edge tessellation factor to = 0 or NaN, the patch will be culled.</span></span> <span data-ttu-id="9df20-155">如此一來，曲面細分器階段就不一定會執行，網域著色器將不會執行，而該塊面也不會產生任何可見的輸出。</span><span class="sxs-lookup"><span data-stu-id="9df20-155">As a result, the tessellator stage may or may not run, the domain shader will not run, and no visible output will be produced for that patch.</span></span>

<span data-ttu-id="9df20-156">在更深入的層級中，輪廓著色器實際上是以兩個階段操作：一個控制點階段和一個修補程式常數階段，這些階段會由硬體平行執行。</span><span class="sxs-lookup"><span data-stu-id="9df20-156">At a deeper level, a hull-shader actually operates in two phases: a control-point phase and a patch-constant phase, which are run in parallel by the hardware.</span></span> <span data-ttu-id="9df20-157">HLSL 編譯器會擷取輪廓著色器中的平行處理原則，並將它編碼成驅動硬體的位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="9df20-157">The HLSL compiler extracts the parallelism in a hull shader and encodes it into bytecode that drives the hardware.</span></span>

-   <span data-ttu-id="9df20-158">控制點階段會針對每個控制點執行一次，讀取塊面的控制點，以及產生一個輸出控制點 (以 ControlPointID 識別)。</span><span class="sxs-lookup"><span data-stu-id="9df20-158">The control-point phase operates once for each control-point, reading the control points for a patch, and generating one output control point (identified by a ControlPointID).</span></span>
-   <span data-ttu-id="9df20-159">塊面常數階段會針對每個塊面執行一次，以產生邊緣鑲嵌係數，和其他每個塊面常數。</span><span class="sxs-lookup"><span data-stu-id="9df20-159">The patch-constant phase operates once per patch to generate edge tessellation factors and other per-patch constants.</span></span> <span data-ttu-id="9df20-160">在內部，許多塊面常數階段可能同時執行。</span><span class="sxs-lookup"><span data-stu-id="9df20-160">Internally, many patch-constant phases may run at the same time.</span></span> <span data-ttu-id="9df20-161">塊面常數階段對於所有輸入和輸出控制點有唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="9df20-161">The patch-constant phase has read-only access to all input and output control points.</span></span>

<span data-ttu-id="9df20-162">以下是輪廓著色器的範例：</span><span class="sxs-lookup"><span data-stu-id="9df20-162">Here's an example of a hull shader:</span></span>


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



<span data-ttu-id="9df20-163">如需建立輪廓著色器的範例，請參閱 [如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md)。</span><span class="sxs-lookup"><span data-stu-id="9df20-163">For an example that creates a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md).</span></span>

### <a name="tessellator-stage"></a><span data-ttu-id="9df20-164">鑲嵌階段</span><span class="sxs-lookup"><span data-stu-id="9df20-164">Tessellator Stage</span></span>

<span data-ttu-id="9df20-165">鑲嵌是藉由將輪廓著色器系結至管線來初始化的固定函式階段 (參閱 [如何：初始化鑲嵌階段](direct3d-11-advanced-stages-tessellator-initialize.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9df20-165">The tessellator is a fixed-function stage initialized by binding a hull shader to the pipeline (see [How To: Initialize the Tessellator Stage](direct3d-11-advanced-stages-tessellator-initialize.md)).</span></span> <span data-ttu-id="9df20-166">曲面細分器階段的目的是將網域 (四邊形、三角形或線) 細分成很多較小的物件 (三角形、點或線)。</span><span class="sxs-lookup"><span data-stu-id="9df20-166">The purpose of the tessellator stage is to subdivide a domain (quad, tri, or line) into many smaller objects (triangles, points or lines).</span></span> <span data-ttu-id="9df20-167">曲面細分器在標準化 (零到一) 座標系統中並排顯示標準網域。</span><span class="sxs-lookup"><span data-stu-id="9df20-167">The tessellator tiles a canonical domain in a normalized (zero-to-one) coordinate system.</span></span> <span data-ttu-id="9df20-168">例如，四邊形網域被鑲嵌為單位正方形。</span><span class="sxs-lookup"><span data-stu-id="9df20-168">For example, a quad domain is tessellated to a unit square.</span></span>

<span data-ttu-id="9df20-169">使用從輪廓著色器階段傳入的鑲嵌因數 (這指定網域被鑲嵌的細微程度) 和分割類型 (指定用於切割塊面的演算法)，曲面細分器每個塊面運作一次。</span><span class="sxs-lookup"><span data-stu-id="9df20-169">The tessellator operates once per patch using the tessellation factors (which specify how finely the domain will be tessellated) and the type of partitioning (which specifies the algorithm used to slice up a patch) that are passed in from the hull-shader stage.</span></span> <span data-ttu-id="9df20-170">曲面細分器輸出 uv (和選擇性 w) 座標及表面拓撲至網域著色器階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-170">The tessellator outputs uv (and optionally w) coordinates and the surface topology to the domain-shader stage.</span></span>

<span data-ttu-id="9df20-171">就內部而言，鑲嵌會以兩個階段運作：</span><span class="sxs-lookup"><span data-stu-id="9df20-171">Internally, the tessellator operates in two phases:</span></span>

-   <span data-ttu-id="9df20-172">第一相位處理鑲嵌因數、修正進位問題、處理非常小因數、降低並結合因數，使用 32 位元浮點算術。</span><span class="sxs-lookup"><span data-stu-id="9df20-172">The first phase processes the tessellation factors, fixing rounding problems, handling very small factors, reducing and combining factors, using 32-bit floating-point arithmetic.</span></span>
-   <span data-ttu-id="9df20-173">第二個相位根據所選分割的類型產生點或拓撲清單。</span><span class="sxs-lookup"><span data-stu-id="9df20-173">The second phase generates point or topology lists based on the type of partitioning selected.</span></span> <span data-ttu-id="9df20-174">這是曲面細分器階段的核心工作，並使用 16 位元分數搭配固定點算術。</span><span class="sxs-lookup"><span data-stu-id="9df20-174">This is the core task of the tessellator stage and uses 16-bit fractions with fixed-point arithmetic.</span></span> <span data-ttu-id="9df20-175">固定點算術允許硬體加速，同時維持可接受的精確度。</span><span class="sxs-lookup"><span data-stu-id="9df20-175">Fixed-point arithmetic allows hardware acceleration while maintaining acceptable precision.</span></span> <span data-ttu-id="9df20-176">例如，假設有 64 公尺寬塊面，這個精確度可以 2 公釐解析度放置點。</span><span class="sxs-lookup"><span data-stu-id="9df20-176">For example, given a 64 meter wide patch, this precision can place points at a 2 mm resolution.</span></span>



| <span data-ttu-id="9df20-177">分割類型</span><span class="sxs-lookup"><span data-stu-id="9df20-177">Type of Partitioning</span></span> | <span data-ttu-id="9df20-178">範圍</span><span class="sxs-lookup"><span data-stu-id="9df20-178">Range</span></span>                       |
|----------------------|-----------------------------|
| <span data-ttu-id="9df20-179">\_奇數小數</span><span class="sxs-lookup"><span data-stu-id="9df20-179">fractional\_odd</span></span>      | <span data-ttu-id="9df20-180">\[1 ... 63\]</span><span class="sxs-lookup"><span data-stu-id="9df20-180">\[1...63\]</span></span>                  |
| <span data-ttu-id="9df20-181">偶數的分數 \_</span><span class="sxs-lookup"><span data-stu-id="9df20-181">fractional\_even</span></span>     | <span data-ttu-id="9df20-182">TessFactor 範圍： \[ 2.. 64\]</span><span class="sxs-lookup"><span data-stu-id="9df20-182">TessFactor range: \[2..64\]</span></span> |
| <span data-ttu-id="9df20-183">整數</span><span class="sxs-lookup"><span data-stu-id="9df20-183">integer</span></span>              | <span data-ttu-id="9df20-184">TessFactor 範圍： \[ 1.. 64\]</span><span class="sxs-lookup"><span data-stu-id="9df20-184">TessFactor range: \[1..64\]</span></span> |
| <span data-ttu-id="9df20-185">pow2</span><span class="sxs-lookup"><span data-stu-id="9df20-185">pow2</span></span>                 | <span data-ttu-id="9df20-186">TessFactor 範圍： \[ 1.. 64\]</span><span class="sxs-lookup"><span data-stu-id="9df20-186">TessFactor range: \[1..64\]</span></span> |



 

### <a name="domain-shader-stage"></a><span data-ttu-id="9df20-187">Domain-Shader 階段</span><span class="sxs-lookup"><span data-stu-id="9df20-187">Domain-Shader Stage</span></span>

<span data-ttu-id="9df20-188">網域著色器會在輸出修補程式中計算細分點的頂點位置。</span><span class="sxs-lookup"><span data-stu-id="9df20-188">A domain shader calculates the vertex position of a subdivided point in the output patch.</span></span> <span data-ttu-id="9df20-189">每個鑲嵌階段輸出點都會執行一次網域著色器，並具有鑲嵌階段輸出 UV 座標、輪廓著色器輸出修補程式的唯讀存取權，以及輪廓著色器輸出修補程式常數，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="9df20-189">A domain shader is run once per tessellator stage output point and has read-only access to the tessellator stage output UV coordinates, the hull shader output patch, and the hull shader output patch constants, as the following diagram shows.</span></span>

![網域著色器階段圖](images/d3d11-domain-shader.png)

<span data-ttu-id="9df20-191">網域著色器的屬性包括：</span><span class="sxs-lookup"><span data-stu-id="9df20-191">Properties of the domain shader include:</span></span>

-   <span data-ttu-id="9df20-192">從鑲嵌階段，每個輸出座標都會叫用一次網域著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-192">A domain shader is invoked once per output coordinate from the tessellator stage.</span></span>
-   <span data-ttu-id="9df20-193">網域著色器會使用來自輪廓著色器階段的輸出控制點。</span><span class="sxs-lookup"><span data-stu-id="9df20-193">A domain shader consumes output control points from the hull-shader stage.</span></span>
-   <span data-ttu-id="9df20-194">網域著色器會輸出頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="9df20-194">A domain shader outputs the position of a vertex.</span></span>
-   <span data-ttu-id="9df20-195">輸入是輪廓著色器輸出，包括控制點、修補常數資料和鑲嵌式因素。</span><span class="sxs-lookup"><span data-stu-id="9df20-195">Inputs are the hull shader outputs including control points, patch constant data and tessellation factors.</span></span> <span data-ttu-id="9df20-196">鑲嵌式因素可以包含固定函式鑲嵌所使用的值，以及在依整數鑲嵌進行四捨五入之前 (的原始值，例如) ，以協助 geomorphing。</span><span class="sxs-lookup"><span data-stu-id="9df20-196">The tessellation factors can include the values used by the fixed function tessellator as well as the raw values (before rounding by integer tessellation, for example), which facilitates geomorphing, for example.</span></span>

<span data-ttu-id="9df20-197">在網域著色器完成後，鑲嵌完成，管線資料會繼續至下一個管線階段 (幾何著色器、圖元著色器等) 。</span><span class="sxs-lookup"><span data-stu-id="9df20-197">After the domain shader completes, tessellation is finished and pipeline data continues to the next pipeline stage (geometry shader, pixel shader etc).</span></span> <span data-ttu-id="9df20-198">預期相鄰基本類型 (例如每個三角形 6 個頂點) 在鑲嵌為使用中時無效 (這樣會導致未定義的行為，偵錯層將會抱怨此行為)。</span><span class="sxs-lookup"><span data-stu-id="9df20-198">A geometry shader that expects primitives with adjacency (for example, 6 vertices per triangle) is not valid when tessellation is active (this results in undefined behavior, which the debug layer will complain about).</span></span>

<span data-ttu-id="9df20-199">以下是網域著色器的範例：</span><span class="sxs-lookup"><span data-stu-id="9df20-199">Here is an example of a domain shader:</span></span>


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a><span data-ttu-id="9df20-200">用於初始化鑲嵌階段的 Api</span><span class="sxs-lookup"><span data-stu-id="9df20-200">APIs for initializing Tessellation Stages</span></span>

<span data-ttu-id="9df20-201">鑲嵌會使用兩個新的可程式化著色器階段來執行：輪廓著色器和網域著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-201">Tessellation is implemented with two new programmable shader stages: a hull shader and a domain shader.</span></span> <span data-ttu-id="9df20-202">這些新的著色器階段是使用著色器模型5中定義的 HLSL 程式碼進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="9df20-202">These new shader stages are programmed with HLSL code that is defined in shader model 5.</span></span> <span data-ttu-id="9df20-203">新的著色器目標為： hs \_ 5 \_ 0 和 ds \_ 5 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="9df20-203">The new shader targets are: hs\_5\_0 and ds\_5\_0.</span></span> <span data-ttu-id="9df20-204">就像所有的可程式化著色器階段一樣，當著色器使用 [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) 和 [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)等 api 系結至管線時，會從編譯的著色器中將硬體的程式碼解壓縮。</span><span class="sxs-lookup"><span data-stu-id="9df20-204">Like all programmable shader stages, code for the hardware is extracted from compiled shaders passed into the runtime when shaders are bound to the pipeline using APIs such as [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) and [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span> <span data-ttu-id="9df20-205">但首先，您必須使用 [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) 和 [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)等 api 來建立著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-205">But first, the shader must be created using APIs such as [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) and [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>

<span data-ttu-id="9df20-206">藉由建立輪廓著色器並將它繫結至輪廓著色器階段 (這會自動設定曲面細分器階段)，來啟用鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="9df20-206">Enable tessellation by creating a hull shader and binding it to the hull-shader stage (this automatically sets up the tessellator stage).</span></span> <span data-ttu-id="9df20-207">若要從鑲嵌塊面產生最終頂點位置，您也需要建立網域著色器並將其繫結至網域著色器階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-207">To generate the final vertex positions from the tessellated patches, you will also need to create a domain shader and bind it to the domain-shader stage.</span></span> <span data-ttu-id="9df20-208">啟用鑲嵌之後，輸入組合語言階段的資料輸入必須是修補資料。</span><span class="sxs-lookup"><span data-stu-id="9df20-208">Once tessellation is enabled, the data input to the input-assembler stage must be patch data.</span></span> <span data-ttu-id="9df20-209">也就是說，輸入組合語言拓撲必須是來自 [**D3D11 \_ 基本 \_ 拓撲**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) 設定 [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)的修補程式常數拓撲。</span><span class="sxs-lookup"><span data-stu-id="9df20-209">That is, the input assembler topology must be a patch constant topology from [**D3D11\_PRIMITIVE\_TOPOLOGY**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) set with [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).</span></span>

<span data-ttu-id="9df20-210">若要停用鑲嵌，將輪廓著色器和網域著色器設定為 **NULL**。</span><span class="sxs-lookup"><span data-stu-id="9df20-210">To disable tessellation, set the hull shader and the domain shader to **NULL**.</span></span> <span data-ttu-id="9df20-211">幾何著色器階段和資料流程輸出階段都不能讀取輪廓著色器的輸出控制點或修補資料。</span><span class="sxs-lookup"><span data-stu-id="9df20-211">Neither the geometry-shader stage nor the stream-output stage can read hull-shader output-control points or patch data.</span></span>

-   <span data-ttu-id="9df20-212">輸入組合語言階段的新拓撲，這是此列舉的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="9df20-212">New topologies for the input-assembler stage, which are extensions to this enumeration.</span></span>

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    <span data-ttu-id="9df20-213">拓撲會使用 IASetPrimitiveTopology 設定為輸入組合語言階段[ ](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)</span><span class="sxs-lookup"><span data-stu-id="9df20-213">The topology is set to the input-assembler stage using [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)</span></span>

-   <span data-ttu-id="9df20-214">當然，新的可程式化著色器階段需要設定其他狀態，以將常數緩衝區、樣本和著色器資源系結至適當的管線階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-214">Of course, the new programmable shader stages require other state to be set, to bind constant buffers, samples, and shader resources to the appropriate pipeline stages.</span></span> <span data-ttu-id="9df20-215">這些新的 ID3D11Device 方法會實作為設定此狀態。</span><span class="sxs-lookup"><span data-stu-id="9df20-215">These new ID3D11Device methods are implemented for setting this state.</span></span>
    -   [<span data-ttu-id="9df20-216">**DSGetConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="9df20-216">**DSGetConstantBuffers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [<span data-ttu-id="9df20-217">**DSGetSamplers**</span><span class="sxs-lookup"><span data-stu-id="9df20-217">**DSGetSamplers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [<span data-ttu-id="9df20-218">**DSGetShader**</span><span class="sxs-lookup"><span data-stu-id="9df20-218">**DSGetShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [<span data-ttu-id="9df20-219">**DSGetShaderResources**</span><span class="sxs-lookup"><span data-stu-id="9df20-219">**DSGetShaderResources**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [<span data-ttu-id="9df20-220">**DSSetConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="9df20-220">**DSSetConstantBuffers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [<span data-ttu-id="9df20-221">**DSSetSamplers**</span><span class="sxs-lookup"><span data-stu-id="9df20-221">**DSSetSamplers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [<span data-ttu-id="9df20-222">**DSSetShader**</span><span class="sxs-lookup"><span data-stu-id="9df20-222">**DSSetShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [<span data-ttu-id="9df20-223">**DSSetShaderResources**</span><span class="sxs-lookup"><span data-stu-id="9df20-223">**DSSetShaderResources**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [<span data-ttu-id="9df20-224">**HSGetConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="9df20-224">**HSGetConstantBuffers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [<span data-ttu-id="9df20-225">**HSGetShaderResources**</span><span class="sxs-lookup"><span data-stu-id="9df20-225">**HSGetShaderResources**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [<span data-ttu-id="9df20-226">**HSGetSamplers**</span><span class="sxs-lookup"><span data-stu-id="9df20-226">**HSGetSamplers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [<span data-ttu-id="9df20-227">**HSGetShader**</span><span class="sxs-lookup"><span data-stu-id="9df20-227">**HSGetShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [<span data-ttu-id="9df20-228">**HSSetConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="9df20-228">**HSSetConstantBuffers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [<span data-ttu-id="9df20-229">**HSSetSamplers**</span><span class="sxs-lookup"><span data-stu-id="9df20-229">**HSSetSamplers**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [<span data-ttu-id="9df20-230">**HSSetShader**</span><span class="sxs-lookup"><span data-stu-id="9df20-230">**HSSetShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [<span data-ttu-id="9df20-231">**HSSetShaderResources**</span><span class="sxs-lookup"><span data-stu-id="9df20-231">**HSSetShaderResources**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a><span data-ttu-id="9df20-232">作法：</span><span class="sxs-lookup"><span data-stu-id="9df20-232">How to's:</span></span>

<span data-ttu-id="9df20-233">此檔也包含初始化鑲嵌階段的範例。</span><span class="sxs-lookup"><span data-stu-id="9df20-233">The documentation also contains examples for initializing the tessellation stages.</span></span>



| <span data-ttu-id="9df20-234">項目</span><span class="sxs-lookup"><span data-stu-id="9df20-234">Item</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="9df20-235">描述</span><span class="sxs-lookup"><span data-stu-id="9df20-235">Description</span></span>                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="9df20-236"><span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-236"><span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md)</span></span><br/>                                                     | <span data-ttu-id="9df20-237">建立輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-237">Create a hull shader.</span></span><br/>              |
| <span data-ttu-id="9df20-238"><span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-238"><span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md)</span></span><br/>                                                     | <span data-ttu-id="9df20-239">設計輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-239">Design a hull shader.</span></span><br/>              |
| <span data-ttu-id="9df20-240"><span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[如何：初始化鑲嵌階段](direct3d-11-advanced-stages-tessellator-initialize.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-240"><span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[How To: Initialize the Tessellator Stage](direct3d-11-advanced-stages-tessellator-initialize.md)</span></span><br/> | <span data-ttu-id="9df20-241">初始化鑲嵌階段。</span><span class="sxs-lookup"><span data-stu-id="9df20-241">Initialize the tessellation stage.</span></span><br/> |
| <span data-ttu-id="9df20-242"><span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[如何：建立網域著色器](direct3d-11-advanced-stages-domain-shader-create.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-242"><span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[How To: Create a Domain Shader](direct3d-11-advanced-stages-domain-shader-create.md)</span></span><br/>                                           | <span data-ttu-id="9df20-243">建立網域著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-243">Create a domain shader.</span></span><br/>            |
| <span data-ttu-id="9df20-244"><span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[如何：設計定義域著色器](direct3d-11-advanced-stages-domain-shader-design.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-244"><span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md)</span></span><br/>                                           | <span data-ttu-id="9df20-245">建立網域著色器。</span><span class="sxs-lookup"><span data-stu-id="9df20-245">Create a domain shader.</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="9df20-246">相關主題</span><span class="sxs-lookup"><span data-stu-id="9df20-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9df20-247">圖形管線</span><span class="sxs-lookup"><span data-stu-id="9df20-247">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


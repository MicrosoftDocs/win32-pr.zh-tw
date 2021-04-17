---
description: '預先計算 Radiance Transfer (Direct3D 9) '
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: '預先計算 Radiance Transfer (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568203"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="65e8e-103">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="65e8e-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="65e8e-104">使用預先計算 Radiance 傳輸</span><span class="sxs-lookup"><span data-stu-id="65e8e-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="65e8e-105">有趣的場景中有數種形式的複雜度，包括光源環境的模型 (也就是，區域光源模型與點/方向一) ，以及模型化何種全域效果 (例如，遮蔽、interreflections、地下散佈。 ) 傳統的互動式轉譯技術模型，這是有限的複雜度。</span><span class="sxs-lookup"><span data-stu-id="65e8e-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="65e8e-106">PRT 可讓這些結果有一些重大限制：</span><span class="sxs-lookup"><span data-stu-id="65e8e-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="65e8e-107">物件會假設為固定 (也就是沒有 deformations) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="65e8e-108">它是以物件為中心的方法 (除非物件會一起移動，否則這些全域效果將不會在) 之間進行維護。</span><span class="sxs-lookup"><span data-stu-id="65e8e-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="65e8e-109">只有低頻率的光源會模型化 (產生軟陰影。 ) 高頻率的燈光 (清晰的陰影) ，則必須採用傳統的技巧。</span><span class="sxs-lookup"><span data-stu-id="65e8e-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="65e8e-110">PRT 需要下列其中一項，但不需要兩者：</span><span class="sxs-lookup"><span data-stu-id="65e8e-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="65e8e-111">高鑲嵌模型和 vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="65e8e-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="65e8e-112">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="65e8e-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="65e8e-113">標準漫射光源與 PRT</span><span class="sxs-lookup"><span data-stu-id="65e8e-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="65e8e-114">下圖是使用傳統 (n ·l) 光源模型。</span><span class="sxs-lookup"><span data-stu-id="65e8e-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="65e8e-115">您可以使用另一個 pass 和某種形式的遮蔽技術來啟用明確陰影， (陰影深度對應或陰影磁片區) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="65e8e-116">如果要使用 () 或更複雜的著色器，以使用傳統的技術，新增多個燈光會需要多個走。</span><span class="sxs-lookup"><span data-stu-id="65e8e-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![使用傳統光源模型所呈現之圖例的螢幕擷取畫面](images/prt-diffuse-cropped.png)

<span data-ttu-id="65e8e-118">下圖是使用 PRT 來呈現，並使用可解決的單一方向光源的最佳近似值。</span><span class="sxs-lookup"><span data-stu-id="65e8e-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="65e8e-119">這會導致不容易以傳統技術產生的軟陰影。</span><span class="sxs-lookup"><span data-stu-id="65e8e-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="65e8e-120">由於 PRT 一律會將已完成的照明環境模型加入多個燈光或使用環境對應，因此您只會變更 (的值，但不會變更著色器所使用的常數) 數目。</span><span class="sxs-lookup"><span data-stu-id="65e8e-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![使用 prt 所呈現圖例的螢幕擷取畫面](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="65e8e-122">使用 Interreflections 的 PRT</span><span class="sxs-lookup"><span data-stu-id="65e8e-122">PRT with Interreflections</span></span>

<span data-ttu-id="65e8e-123">直接光源會直接從燈光到達表面。</span><span class="sxs-lookup"><span data-stu-id="65e8e-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="65e8e-124">Interreflections 會在將某些其他介面彈到某些次數之後，觸及表面。</span><span class="sxs-lookup"><span data-stu-id="65e8e-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="65e8e-125">PRT 可以建立此行為的模型，而不需要在執行時間變更效能，只要使用不同的參數執行模擬器即可。</span><span class="sxs-lookup"><span data-stu-id="65e8e-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="65e8e-126">下圖僅使用 direct PRT 來建立， (0 彈跳而沒有 interreflections) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![僅使用直接 prt 所呈現之圖例的螢幕擷取畫面](images/prt-nointerreflections.png)

<span data-ttu-id="65e8e-128">下圖是使用 PRT 與 interreflections 建立的， (2 使用 interreflections) 彈跳。</span><span class="sxs-lookup"><span data-stu-id="65e8e-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![使用 prt 搭配 interreflections 所呈現圖例的螢幕擷取畫面](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="65e8e-130">使用地下散佈的 PRT</span><span class="sxs-lookup"><span data-stu-id="65e8e-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="65e8e-131">地下散佈是一種技術，可建立光線如何通過特定材質的模型。</span><span class="sxs-lookup"><span data-stu-id="65e8e-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="65e8e-132">例如，對您手的手掌按下亮燈。</span><span class="sxs-lookup"><span data-stu-id="65e8e-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="65e8e-133">這種光線的光線通過您的手， (變更程式) 中的色彩，然後離開您手的另一端。</span><span class="sxs-lookup"><span data-stu-id="65e8e-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="65e8e-134">這也可以使用模擬器的簡單變更來建立模型，而且不會變更執行時間。</span><span class="sxs-lookup"><span data-stu-id="65e8e-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="65e8e-135">下圖示范 PRT 與地下散佈。</span><span class="sxs-lookup"><span data-stu-id="65e8e-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![使用 prt 搭配地下散佈所呈現圖例的螢幕擷取畫面](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="65e8e-137">PRT 的運作方式</span><span class="sxs-lookup"><span data-stu-id="65e8e-137">How PRT Works</span></span>

<span data-ttu-id="65e8e-138">下列詞彙有助於瞭解 PRT 的運作方式，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="65e8e-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="65e8e-139">來源 Radiance：來源 Radiance 表示整個光源的環境。</span><span class="sxs-lookup"><span data-stu-id="65e8e-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="65e8e-140">在 PRT 中，使用球形調和來估算任意的環境，此光源會假設為相對於物件 (與使用環境對應所做的相同假設 ) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="65e8e-141">Exit Radiance： Exit Radiance 是離開介面上某個點的燈光，從任何可能的來源 (反映 Radiance、地下散佈、發射) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="65e8e-142">傳輸向量：將向量地圖來源 Radiance 轉換成 exit Radiance，並使用複雜的燈光傳輸模擬來預先計算離線。</span><span class="sxs-lookup"><span data-stu-id="65e8e-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![prt 運作方式的圖表](images/prt-lightingpicture.png)

<span data-ttu-id="65e8e-144">PRT 會將轉譯程式分為兩個階段，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="65e8e-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="65e8e-145">昂貴的輕量傳輸模擬 precomputes 可在執行時間使用的傳輸係數。</span><span class="sxs-lookup"><span data-stu-id="65e8e-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="65e8e-146">相對較輕量的執行時間階段會先接近使用球形調和的照明環境，然後使用這些光源係數和預先計算傳輸係數 (從第1階段) ，再加上一個簡單的著色器，因此會導致結束 radiance (光離開物件) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![prt 資料流程的圖表](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="65e8e-148">如何使用 PRT API</span><span class="sxs-lookup"><span data-stu-id="65e8e-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="65e8e-149">使用其中一個計算來計算傳輸向量 .。。 [**ID3DXPRTEngine**](id3dxprtengine.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="65e8e-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="65e8e-150">直接處理這些傳輸媒介需要大量的記憶體和著色器計算。</span><span class="sxs-lookup"><span data-stu-id="65e8e-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="65e8e-151">壓縮可大幅減少所需的記憶體和著色器計算量。</span><span class="sxs-lookup"><span data-stu-id="65e8e-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="65e8e-152">最後的光源值會在端點著色器中計算，以執行下列壓縮的轉譯方程式。</span><span class="sxs-lookup"><span data-stu-id="65e8e-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![prt 轉譯的方程式](images/prt-shaderequation.png)

    <span data-ttu-id="65e8e-154">其中：</span><span class="sxs-lookup"><span data-stu-id="65e8e-154">Where:</span></span>

    

    | <span data-ttu-id="65e8e-155">參數</span><span class="sxs-lookup"><span data-stu-id="65e8e-155">Parameter</span></span>      | <span data-ttu-id="65e8e-156">Description</span><span class="sxs-lookup"><span data-stu-id="65e8e-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="65e8e-157">Rp</span><span class="sxs-lookup"><span data-stu-id="65e8e-157">Rₚ</span></span>             | <span data-ttu-id="65e8e-158">在頂點 p 的結束 radiance 單一通道，會在網格上的每個頂點進行評估。</span><span class="sxs-lookup"><span data-stu-id="65e8e-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="65e8e-159">Mk</span><span class="sxs-lookup"><span data-stu-id="65e8e-159">Mₖ</span></span>             | <span data-ttu-id="65e8e-160">群集 k 的平均值。</span><span class="sxs-lookup"><span data-stu-id="65e8e-160">The mean for cluster k.</span></span> <span data-ttu-id="65e8e-161">這是係數的 Order ²向量。</span><span class="sxs-lookup"><span data-stu-id="65e8e-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="65e8e-162">k</span><span class="sxs-lookup"><span data-stu-id="65e8e-162">k</span></span>              | <span data-ttu-id="65e8e-163">頂點 p 的叢集識別碼。</span><span class="sxs-lookup"><span data-stu-id="65e8e-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="65e8e-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="65e8e-164">L<sup>'</sup></span></span>  | <span data-ttu-id="65e8e-165">來源 radiance 至 SH 基礎函數的近似值。</span><span class="sxs-lookup"><span data-stu-id="65e8e-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="65e8e-166">這是係數的 Order ²向量。</span><span class="sxs-lookup"><span data-stu-id="65e8e-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="65e8e-167">j</span><span class="sxs-lookup"><span data-stu-id="65e8e-167">j</span></span>              | <span data-ttu-id="65e8e-168">加總 PCA 向量數目的整數。</span><span class="sxs-lookup"><span data-stu-id="65e8e-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="65e8e-169">w<sub>pj</sub></span><span class="sxs-lookup"><span data-stu-id="65e8e-169">w<sub>pj</sub></span></span> | <span data-ttu-id="65e8e-170">點 p 的第 j 個 PCA 加權。</span><span class="sxs-lookup"><span data-stu-id="65e8e-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="65e8e-171">這是單一係數。</span><span class="sxs-lookup"><span data-stu-id="65e8e-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="65e8e-172">B<sub>kj</sub></span><span class="sxs-lookup"><span data-stu-id="65e8e-172">B<sub>kj</sub></span></span> | <span data-ttu-id="65e8e-173">適用于群集 k 的第 j 個 PCA 基礎向量。</span><span class="sxs-lookup"><span data-stu-id="65e8e-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="65e8e-174">這是係數的 Order ²向量。</span><span class="sxs-lookup"><span data-stu-id="65e8e-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="65e8e-175">解壓縮 .。。 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 方法可讓您從模擬存取壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="65e8e-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="65e8e-176">計算來源 radiance。</span><span class="sxs-lookup"><span data-stu-id="65e8e-176">Compute the source radiance.</span></span>

    <span data-ttu-id="65e8e-177">API 中有數個 helper 函式，可處理各種常見的光源案例。</span><span class="sxs-lookup"><span data-stu-id="65e8e-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="65e8e-178">函式</span><span class="sxs-lookup"><span data-stu-id="65e8e-178">Function</span></span>                                                         | <span data-ttu-id="65e8e-179">用途</span><span class="sxs-lookup"><span data-stu-id="65e8e-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="65e8e-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="65e8e-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="65e8e-181">近似于傳統的方向淺色。</span><span class="sxs-lookup"><span data-stu-id="65e8e-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="65e8e-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="65e8e-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="65e8e-183">近似于本機球形燈光來源。</span><span class="sxs-lookup"><span data-stu-id="65e8e-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="65e8e-184"> (請注意，PRT 僅適用于距離光源環境。 ) </span><span class="sxs-lookup"><span data-stu-id="65e8e-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="65e8e-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="65e8e-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="65e8e-186">近似于遠處區域光源。</span><span class="sxs-lookup"><span data-stu-id="65e8e-186">Approximates a distant area light source.</span></span> <span data-ttu-id="65e8e-187">例如，sun (非常小的錐形角度) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="65e8e-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="65e8e-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="65e8e-189">評估兩個色彩之間的線性插補， (球) 的每個極點。</span><span class="sxs-lookup"><span data-stu-id="65e8e-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="65e8e-190">計算 exit radiance。</span><span class="sxs-lookup"><span data-stu-id="65e8e-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="65e8e-191">現在必須使用頂點或圖元著色器在每個點上評估方程式1。</span><span class="sxs-lookup"><span data-stu-id="65e8e-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="65e8e-192">在評估著色器之前，必須先預先計算常數，並將其載入常數資料表 (如需詳細資料，請參閱 [PRT 示範範例](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)) 。</span><span class="sxs-lookup"><span data-stu-id="65e8e-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="65e8e-193">著色器本身是此方程式的直接執行。</span><span class="sxs-lookup"><span data-stu-id="65e8e-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="65e8e-194">參考資料</span><span class="sxs-lookup"><span data-stu-id="65e8e-194">References</span></span>

<span data-ttu-id="65e8e-195">如需 PRT 和球面諧波的詳細資訊，請參閱下列白皮書：</span><span class="sxs-lookup"><span data-stu-id="65e8e-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="65e8e-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="65e8e-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65e8e-197">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="65e8e-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="65e8e-198">PRT 方 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="65e8e-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="65e8e-199">使用 (Direct3D 9) 的材質表示 PRT </span><span class="sxs-lookup"><span data-stu-id="65e8e-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="65e8e-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="65e8e-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="65e8e-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="65e8e-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="65e8e-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="65e8e-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="65e8e-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="65e8e-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="65e8e-204">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="65e8e-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="65e8e-205">數學函數</span><span class="sxs-lookup"><span data-stu-id="65e8e-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




---
title: 重疊的陰影圖
description: 串聯陰影地圖 (網網的) ，是對抗其中一個最常見的錯誤與遮蔽的角度別名的最佳方式。
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/01/2021
ms.locfileid: "106981675"
---
# <a name="cascaded-shadow-maps"></a><span data-ttu-id="df7ee-103">重疊的陰影圖</span><span class="sxs-lookup"><span data-stu-id="df7ee-103">Cascaded Shadow Maps</span></span>

<span data-ttu-id="df7ee-104">串聯陰影地圖 (網網的) 是對抗其中一個最常見錯誤與遮蔽的最佳方式：透視別名。</span><span class="sxs-lookup"><span data-stu-id="df7ee-104">Cascaded shadow maps (CSMs) are the best way to combat one of the most prevalent errors with shadowing: perspective aliasing.</span></span> <span data-ttu-id="df7ee-105">這份技術檔（假設讀者已經熟悉陰影對應） esposito 著手處理了網的主題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-105">This technical article, which assumes the reader is familiar with shadow mapping, tackles the topic of CSMs.</span></span> <span data-ttu-id="df7ee-106">具體而言，它會：</span><span class="sxs-lookup"><span data-stu-id="df7ee-106">Specifically, it:</span></span>

-   <span data-ttu-id="df7ee-107">說明網網的複雜性;</span><span class="sxs-lookup"><span data-stu-id="df7ee-107">explains the complexity of CSMs;</span></span>
-   <span data-ttu-id="df7ee-108">提供 CSM 演算法可能變異的詳細資料;</span><span class="sxs-lookup"><span data-stu-id="df7ee-108">gives details on the possible variations of the CSM algorithms;</span></span>
-   <span data-ttu-id="df7ee-109">描述兩個最常見的篩選技術—在篩選 (PCF) ，以及使用差異陰影對應 (VSMs) ，來進行篩選;</span><span class="sxs-lookup"><span data-stu-id="df7ee-109">describes the two most common filtering techniques—percentage closer filtering (PCF) and filtering with variance shadow maps (VSMs);</span></span>
-   <span data-ttu-id="df7ee-110">識別並解決一些與新增篩選至網的常見錯誤相關的問題;和</span><span class="sxs-lookup"><span data-stu-id="df7ee-110">identifies and addresses some of the common pitfalls associated with adding filtering to CSMs; and</span></span>
-   <span data-ttu-id="df7ee-111">示範如何透過 Direct3D 11 硬體，將網達10網的網到 Direct3D 10。</span><span class="sxs-lookup"><span data-stu-id="df7ee-111">shows how to map CSMs to Direct3D 10 through Direct3D 11 hardware.</span></span>

<span data-ttu-id="df7ee-112">本文中所使用的程式碼可在 CascadedShadowMaps11 和 VarianceShadows11 範例中的 DirectX 軟體發展工具組 (SDK) 中找到。</span><span class="sxs-lookup"><span data-stu-id="df7ee-112">The code used in this article can be found in the DirectX Software Development Kit (SDK) in the CascadedShadowMaps11 and VarianceShadows11 samples.</span></span> <span data-ttu-id="df7ee-113">本文將在執行技術檔中涵蓋的技術文章、 [改善陰影深度對應的常用技巧，以](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)充分發揮最大效用。</span><span class="sxs-lookup"><span data-stu-id="df7ee-113">This article will prove most useful after implementing the techniques covered in the technical article, [Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), are implemented.</span></span>

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a><span data-ttu-id="df7ee-114">串聯陰影地圖和透視圖別名</span><span class="sxs-lookup"><span data-stu-id="df7ee-114">Cascaded Shadow Maps and Perspective Aliasing</span></span>

<span data-ttu-id="df7ee-115">陰影地圖中的觀點別名是最難克服的問題之一。</span><span class="sxs-lookup"><span data-stu-id="df7ee-115">Perspective aliasing in a shadow map is one of the most difficult problems to overcome.</span></span> <span data-ttu-id="df7ee-116">在技術檔中，改善陰影深度對應的常見技術，描述了觀點別名，而且有一些方法可減輕問題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-116">In the technical article, Common Techniques to Improve Shadow Depth Maps, perspective aliasing is described and some approaches to mitigate the problem are identified.</span></span> <span data-ttu-id="df7ee-117">在實務上，網達業界的解決方案通常是最適合的解決方案，而且通常會在新式遊戲中採用。</span><span class="sxs-lookup"><span data-stu-id="df7ee-117">In practice, CSMs tend to be the best solution, and are commonly employed in modern games.</span></span>

<span data-ttu-id="df7ee-118">網基礎網的基本概念很容易理解。</span><span class="sxs-lookup"><span data-stu-id="df7ee-118">The basic concept of CSMs is easy to understand.</span></span> <span data-ttu-id="df7ee-119">相機的不同區域必須具有不同解析度的陰影對應。</span><span class="sxs-lookup"><span data-stu-id="df7ee-119">Different areas of the camera frustum require shadow maps with different resolutions.</span></span> <span data-ttu-id="df7ee-120">最接近眼睛的物件所需的解析度，必須比更遠的物件更高。</span><span class="sxs-lookup"><span data-stu-id="df7ee-120">Objects nearest the eye require a higher resolution than do more distant objects.</span></span> <span data-ttu-id="df7ee-121">事實上，當眼睛非常接近幾何時，最接近眼睛的圖元可能需要這麼多的解析度，即使4096×4096陰影地圖也不夠。</span><span class="sxs-lookup"><span data-stu-id="df7ee-121">In fact, when the eye moves very close to the geometry, the pixels nearest the eye can require so much resolution that even a 4096 × 4096 shadow map is insufficient.</span></span>

<span data-ttu-id="df7ee-122">網基礎網的基本概念是將分割區分割成多個 frusta。</span><span class="sxs-lookup"><span data-stu-id="df7ee-122">The basic idea of CSMs is to partition the frustum into multiple frusta.</span></span> <span data-ttu-id="df7ee-123">針對每個 subfrustum 呈現陰影對應;然後，圖元著色器會從對應中最符合所需解析度的地圖取樣 (圖 2) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-123">A shadow map is rendered for each subfrustum; the pixel shader then samples from the map that most closely matches the required resolution (Figure 2).</span></span>

<span data-ttu-id="df7ee-124">**圖1。陰影對應涵蓋範圍**</span><span class="sxs-lookup"><span data-stu-id="df7ee-124">**Figure 1. Shadow map coverage**</span></span>

![陰影對應涵蓋範圍](images/shadow-map-coverage.png)

<span data-ttu-id="df7ee-126">在 [圖 1] 中，品質會顯示 (從最高到最低的) 向右。</span><span class="sxs-lookup"><span data-stu-id="df7ee-126">In Figure 1, quality is shown (left to right) from highest to lowest.</span></span> <span data-ttu-id="df7ee-127">代表陰影地圖的方格系列，以紅色的 (反轉錐形) 顯示圖元涵蓋範圍如何受到不同解析度陰影對應的影響。</span><span class="sxs-lookup"><span data-stu-id="df7ee-127">The series of grids representing shadow maps with a view frustum (inverted cone in red) shows how pixel coverage is affected with different resolution shadow maps.</span></span> <span data-ttu-id="df7ee-128">陰影為最高品質 (白色圖元) 當陰影地圖中的材質為亮空間的1:1 比率對應圖元時。</span><span class="sxs-lookup"><span data-stu-id="df7ee-128">Shadows are of the highest quality (white pixels) when there is a 1:1 ratio mapping pixels in light space to texels in the shadow map.</span></span> <span data-ttu-id="df7ee-129">以大型、blocky 材質地圖的形式來呈現外觀別名， (左影像) 當圖元數對應到相同的陰影材質時。</span><span class="sxs-lookup"><span data-stu-id="df7ee-129">Perspective aliasing occurs in the form of large, blocky texture maps (left image) when too many pixels map to the same shadow texel.</span></span> <span data-ttu-id="df7ee-130">當陰影地圖太大時，就會受到取樣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-130">When the shadow map is too large, it is under sampled.</span></span> <span data-ttu-id="df7ee-131">在此情況下，系統會略過材質、引進 shimmering 成品，並影響效能。</span><span class="sxs-lookup"><span data-stu-id="df7ee-131">In this case, texels are skipped, shimmering artifacts are introduced, and performance is affected.</span></span>

<span data-ttu-id="df7ee-132">**[圖 2]CSM 陰影品質**</span><span class="sxs-lookup"><span data-stu-id="df7ee-132">**Figure 2. CSM shadow quality**</span></span>

![csm 陰影品質](images/csm-shadow-quality.png)

<span data-ttu-id="df7ee-134">[圖 2] 顯示 [圖 1] 中每個陰影地圖中最高品質區段的切口。</span><span class="sxs-lookup"><span data-stu-id="df7ee-134">Figure 2 shows cutouts from the highest quality section in each shadow map in Figure 1.</span></span> <span data-ttu-id="df7ee-135">具有最接近放置圖元 (在頂點) 的陰影地圖最接近眼睛。</span><span class="sxs-lookup"><span data-stu-id="df7ee-135">The shadow map with the most closely placed pixels (at the apex) is nearest the eye.</span></span> <span data-ttu-id="df7ee-136">技術上來說，這些都是相同大小的地圖，使用白色和灰階來說明點串聯陰影地圖的成功。</span><span class="sxs-lookup"><span data-stu-id="df7ee-136">Technically, these are maps of the same size, with white and grey used to exemplify the success of the cascaded shadow map.</span></span> <span data-ttu-id="df7ee-137">白色很理想，因為它會顯示良好的涵蓋範圍，也就是眼睛空間圖元和陰影對應材質的1:1 比例。</span><span class="sxs-lookup"><span data-stu-id="df7ee-137">White is ideal because it shows good coverage—a 1:1 ratio for eye-space pixels and shadow-map texels.</span></span>

<span data-ttu-id="df7ee-138">網網的每個畫面都需要執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="df7ee-138">CSMs require the following steps per frame.</span></span>

1.  <span data-ttu-id="df7ee-139">將分割區分割成 subfrusta。</span><span class="sxs-lookup"><span data-stu-id="df7ee-139">Partition the frustum into subfrusta.</span></span>
2.  <span data-ttu-id="df7ee-140">計算每個 subfrustum 的正射投射。</span><span class="sxs-lookup"><span data-stu-id="df7ee-140">Compute an orthographic projection for each subfrustum.</span></span>
3.  <span data-ttu-id="df7ee-141">轉譯每個 subfrustum 的陰影對應。</span><span class="sxs-lookup"><span data-stu-id="df7ee-141">Render a shadow map for each subfrustum.</span></span>
4.  <span data-ttu-id="df7ee-142">呈現場景。</span><span class="sxs-lookup"><span data-stu-id="df7ee-142">Render the scene.</span></span>

    1.  <span data-ttu-id="df7ee-143">系結陰影對應和呈現。</span><span class="sxs-lookup"><span data-stu-id="df7ee-143">Bind the shadow maps and render.</span></span>
    2.  <span data-ttu-id="df7ee-144">頂點著色器會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="df7ee-144">The vertex shader does the following:</span></span>

        -   <span data-ttu-id="df7ee-145">計算每個淺色 subfrustum (的材質座標，除非在圖元著色器中計算所需的材質座標) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-145">Computes texture coordinates for each light subfrustum (unless the needed texture coordinate is calculated in the pixel shader).</span></span>
        -   <span data-ttu-id="df7ee-146">轉換和燈光頂點等等。</span><span class="sxs-lookup"><span data-stu-id="df7ee-146">Transforms and lights the vertex, and so on.</span></span>

    3.  <span data-ttu-id="df7ee-147">圖元著色器會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="df7ee-147">The pixel shader does the following:</span></span>

        -   <span data-ttu-id="df7ee-148">判斷適當的陰影對應。</span><span class="sxs-lookup"><span data-stu-id="df7ee-148">Determines the proper shadow map.</span></span>
        -   <span data-ttu-id="df7ee-149">視需要轉換材質座標。</span><span class="sxs-lookup"><span data-stu-id="df7ee-149">Transforms the texture coordinates if necessary.</span></span>
        -   <span data-ttu-id="df7ee-150">範例 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-150">Samples the cascade.</span></span>
        -   <span data-ttu-id="df7ee-151">燈光圖元。</span><span class="sxs-lookup"><span data-stu-id="df7ee-151">Lights the pixel.</span></span>

## <a name="partitioning-the-frustum"></a><span data-ttu-id="df7ee-152">分割分割區</span><span class="sxs-lookup"><span data-stu-id="df7ee-152">Partitioning the Frustum</span></span>

<span data-ttu-id="df7ee-153">分割分割區是建立 subfrusta 的動作。</span><span class="sxs-lookup"><span data-stu-id="df7ee-153">Partitioning the frustum is the act of creating subfrusta.</span></span> <span data-ttu-id="df7ee-154">分割分割的一項技術是以 Z 方向計算從零到100% 的間隔。</span><span class="sxs-lookup"><span data-stu-id="df7ee-154">One technique for splitting the frustum is to calculate intervals from zero percent to one hundred percent in the Z-direction.</span></span> <span data-ttu-id="df7ee-155">接著，每個間隔表示接近平面，而最接近平面的平面是以 Z 軸的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="df7ee-155">Each interval then represents a near plane and a far plane as a percentage of the Z-axis.</span></span>

<span data-ttu-id="df7ee-156">**圖3。查看任意分割的 frustums**</span><span class="sxs-lookup"><span data-stu-id="df7ee-156">**Figure 3. View frustums partitioned arbitrarily**</span></span>

![查看任意分割的 frustums](images/view-frustums-partitioned-arbitrarily.png)

<span data-ttu-id="df7ee-158">在實務上，重新計算每個畫面格的分割分割會導致陰影邊緣 shimmer。</span><span class="sxs-lookup"><span data-stu-id="df7ee-158">In practice, recalculating the frustum splits per frame causes shadow edges to shimmer.</span></span> <span data-ttu-id="df7ee-159">一般接受的作法是在每個案例中使用一組靜態串聯間隔。</span><span class="sxs-lookup"><span data-stu-id="df7ee-159">The generally accepted practice is to use a static set of cascade intervals per scenario.</span></span> <span data-ttu-id="df7ee-160">在此案例中，沿著 Z 軸的間隔會用來描述分割分割區時所發生的 subfrustum。</span><span class="sxs-lookup"><span data-stu-id="df7ee-160">In this scenario, the interval along the Z-axis is used to describe a subfrustum that occurs when partitioning the frustum.</span></span> <span data-ttu-id="df7ee-161">判斷指定場景的正確大小間隔取決於數個因素。</span><span class="sxs-lookup"><span data-stu-id="df7ee-161">Determining the correct size intervals for a given scene depends upon several factors.</span></span>

### <a name="orientation-of-the-scene-geometry"></a><span data-ttu-id="df7ee-162">場景幾何的方向</span><span class="sxs-lookup"><span data-stu-id="df7ee-162">Orientation of the Scene Geometry</span></span>

<span data-ttu-id="df7ee-163">至於場景幾何，相機方向會影響串聯間隔選取。</span><span class="sxs-lookup"><span data-stu-id="df7ee-163">With respect to scene geometry, camera orientation affects cascade interval selection.</span></span> <span data-ttu-id="df7ee-164">例如，像是足球遊戲中的地面鏡頭，它的一組靜態串聯間隔和天空中的攝影機不同。</span><span class="sxs-lookup"><span data-stu-id="df7ee-164">For example, a camera very near the ground, such as a ground camera in a football game, has a different static set of cascade intervals than a camera in the sky.</span></span>

<span data-ttu-id="df7ee-165">[圖 4] 顯示一些不同的攝影機和各自的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="df7ee-165">Figure 4 shows some different cameras and their respective partitions.</span></span> <span data-ttu-id="df7ee-166">當場景的 Z 範圍很大時，需要更多的分割平面。</span><span class="sxs-lookup"><span data-stu-id="df7ee-166">When the scene's Z-range is very large, more split planes are required.</span></span> <span data-ttu-id="df7ee-167">例如，當眼睛非常接近地面，但仍然可以看到遠的物件時，可能需要多個層級。</span><span class="sxs-lookup"><span data-stu-id="df7ee-167">For example, when the eye is very near the ground plane, but distant objects are still visible, multiple cascades can be necessary.</span></span> <span data-ttu-id="df7ee-168">分割分割，讓更多分割接近眼睛 (其中的觀點別名會變更最快的) 也很重要。</span><span class="sxs-lookup"><span data-stu-id="df7ee-168">Dividing the frustum so that more splits are near the eye (where perspective aliasing is changing the fastest) is also valuable.</span></span> <span data-ttu-id="df7ee-169">當大部分的幾何聚集到一個社區段時 (例如，額外負荷視圖或視圖分割的飛行模擬器) ，則需要較少的程式。</span><span class="sxs-lookup"><span data-stu-id="df7ee-169">When most of the geometry is clumped into a small section (such as an overhead view or a flight simulator) of the view frustum, fewer cascades are necessary.</span></span>

<span data-ttu-id="df7ee-170">**[圖 4]不同的設定需要不同的分割分割**</span><span class="sxs-lookup"><span data-stu-id="df7ee-170">**Figure 4. Different configurations require different frustum splits**</span></span>

![不同的設定需要不同的分割分割](images/different-configurations-require-different-frustum-splits.png)

<span data-ttu-id="df7ee-172">當幾何在 Z 中有很高的動態範圍時 (左) ，需要大量的多個級聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-172">(Left) When geometry has a high dynamic range in Z, lots of cascades are required.</span></span> <span data-ttu-id="df7ee-173"> (中心) 當幾何在 Z 中有低動態範圍時，多個 frustums 的優點很小。</span><span class="sxs-lookup"><span data-stu-id="df7ee-173">(Center) When the geometry has low dynamic range in Z, there is little benefit from multiple frustums.</span></span> <span data-ttu-id="df7ee-174"> (右) 當動態範圍為 [中] 時，只需要三個數據分割。</span><span class="sxs-lookup"><span data-stu-id="df7ee-174">(Right) Only three partitions are needed when the dynamic range is medium.</span></span>

### <a name="orientation-of-the-light-and-the-camera"></a><span data-ttu-id="df7ee-175">光線和相機的方向</span><span class="sxs-lookup"><span data-stu-id="df7ee-175">Orientation of the Light and the Camera</span></span>

<span data-ttu-id="df7ee-176">每一個串聯的投射矩陣都會緊密配合其對應的 subfrustum。</span><span class="sxs-lookup"><span data-stu-id="df7ee-176">Each cascade's projection matrix is fit tightly around its corresponding subfrustum.</span></span> <span data-ttu-id="df7ee-177">在觀看攝影機和燈光方向為正向的設定中，您可以在重迭的情況下緊密地配合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-177">In configurations where the view camera and the light directions are orthogonal, the cascades can be fit tightly with little overlap.</span></span> <span data-ttu-id="df7ee-178">重迭會變得更大，因為燈光和鏡頭相機會移至平行對齊 (圖 5) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-178">The overlap becomes larger as the light and the view camera move into parallel alignment (Figure 5).</span></span> <span data-ttu-id="df7ee-179">當光線和觀賞攝影機幾乎平行時，它稱為「dueling frusta」，這是大部分遮蔽演算法的很困難案例。</span><span class="sxs-lookup"><span data-stu-id="df7ee-179">When the light and the view camera are nearly parallel, it is called a "dueling frusta," and is a very hard scenario for most shadowing algorithms.</span></span> <span data-ttu-id="df7ee-180">將光源和相機限制為不會發生這種情況並不常見。</span><span class="sxs-lookup"><span data-stu-id="df7ee-180">It is not uncommon to constrain the light and camera so that this scenario does not occur.</span></span> <span data-ttu-id="df7ee-181">但是在此案例中，網網網的執行效能比其他許多演算法更好。</span><span class="sxs-lookup"><span data-stu-id="df7ee-181">CSMs, however, perform much better than many other algorithms in this scenario.</span></span>

<span data-ttu-id="df7ee-182">**[圖 5]。串聯重迭會隨著光線方向與相機方向平行變成平行**</span><span class="sxs-lookup"><span data-stu-id="df7ee-182">**Figure 5. Cascade overlap increases as light direction becomes parallel with camera direction**</span></span>

![串聯重迭會隨著光線方向與相機方向平行變成平行](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

<span data-ttu-id="df7ee-184">許多 CSM 的採用都使用固定大小的 frusta。</span><span class="sxs-lookup"><span data-stu-id="df7ee-184">Many CSM implementations use fixed-size frusta.</span></span> <span data-ttu-id="df7ee-185">當分割以固定大小的間隔分割時，圖元著色器可以使用 Z 深度來編制維陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="df7ee-185">The pixel shader can use the Z-depth to index into the array of cascades when the frustum is split in fixed-size intervals.</span></span>

## <a name="calculating-a-view-frustum-bound"></a><span data-ttu-id="df7ee-186">計算系結 View-Frustum</span><span class="sxs-lookup"><span data-stu-id="df7ee-186">Calculating a View-Frustum Bound</span></span>

<span data-ttu-id="df7ee-187">一旦選取了間隔間隔之後，就會使用下列兩種的其中一種來建立 subfrusta：適用于場景，並符合 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-187">Once the frustum intervals are selected, the subfrusta are created using one of two: fit to scene and fit to cascade.</span></span>

### <a name="fit-to-scene"></a><span data-ttu-id="df7ee-188">符合場景</span><span class="sxs-lookup"><span data-stu-id="df7ee-188">Fit to Scene</span></span>

<span data-ttu-id="df7ee-189">所有的 frusta 都可以使用相同的接近平面來建立。</span><span class="sxs-lookup"><span data-stu-id="df7ee-189">All of the frusta can be created with the same near plane.</span></span> <span data-ttu-id="df7ee-190">這會強制將串聯重迭。</span><span class="sxs-lookup"><span data-stu-id="df7ee-190">This forces the cascades to overlap.</span></span> <span data-ttu-id="df7ee-191">CascadedShadowMaps11 範例會針對場景呼叫這項技術。</span><span class="sxs-lookup"><span data-stu-id="df7ee-191">The CascadedShadowMaps11 sample calls this technique fit to scene.</span></span>

### <a name="fit-to-cascade"></a><span data-ttu-id="df7ee-192">符合 Cascade</span><span class="sxs-lookup"><span data-stu-id="df7ee-192">Fit to Cascade</span></span>

<span data-ttu-id="df7ee-193">或者，您可以使用實際的資料分割間隔來建立 frusta，以作為接近和遠的平面。</span><span class="sxs-lookup"><span data-stu-id="df7ee-193">Alternatively, frusta can be created with the actual partition interval being used as near and far planes.</span></span> <span data-ttu-id="df7ee-194">這會造成更緊密的配合，但會變質為適用于 dueling frusta 的場景。</span><span class="sxs-lookup"><span data-stu-id="df7ee-194">This causes a tighter fit, but degenerates to fit to scene in the case of dueling frusta.</span></span> <span data-ttu-id="df7ee-195">CascadedShadowMaps11 範例會將這項技術適當地呼叫，以進行串聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-195">The CascadedShadowMaps11 samples calls this technique fit to cascade.</span></span>

<span data-ttu-id="df7ee-196">圖6顯示這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="df7ee-196">These two methods are shown in Figure 6.</span></span> <span data-ttu-id="df7ee-197">配合串聯可減少解析度。</span><span class="sxs-lookup"><span data-stu-id="df7ee-197">Fit to cascade wastes less resolution.</span></span> <span data-ttu-id="df7ee-198">符合 cascade 的問題是，正向投射會根據視圖的錐的方向來放大和縮小。</span><span class="sxs-lookup"><span data-stu-id="df7ee-198">The problem with fit to cascade is that the orthographic projection grows and shrinks based on the orientation of the view frustum.</span></span> <span data-ttu-id="df7ee-199">「調整成場景」技術會以視圖的大小上限來填補正向投射，以移除在移動攝影機移動時所顯示的構件。</span><span class="sxs-lookup"><span data-stu-id="df7ee-199">The fit to scene technique pads the orthographic projection by the max size of the view frustum removing the artifacts that appear when the view-camera moves.</span></span> <span data-ttu-id="df7ee-200">[改善陰影深度對應的常見技術，可](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) 解決在「以材質大小遞增」一節中移動燈光時所顯示的構件。</span><span class="sxs-lookup"><span data-stu-id="df7ee-200">[Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) addresses the artifacts that appear when the light moves in the section "Moving the light in texel sized increments."</span></span>

<span data-ttu-id="df7ee-201">**[圖 6]。符合場景與縮放比例**</span><span class="sxs-lookup"><span data-stu-id="df7ee-201">**Figure 6. Fit to scene vs. fit to cascade**</span></span>

![符合場景或符合 cascade](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a><span data-ttu-id="df7ee-203">呈現陰影地圖</span><span class="sxs-lookup"><span data-stu-id="df7ee-203">Render the Shadow Map</span></span>

<span data-ttu-id="df7ee-204">CascadedShadowMaps11 範例會將陰影地圖轉譯成一個大型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="df7ee-204">The CascadedShadowMaps11 sample renders the shadow maps into one large buffer.</span></span> <span data-ttu-id="df7ee-205">這是因為材質陣列上的 PCF 是 Direct3D 10.1 功能。</span><span class="sxs-lookup"><span data-stu-id="df7ee-205">This is because PCF on texture arrays is a Direct3D 10.1 feature.</span></span> <span data-ttu-id="df7ee-206">針對每個串聯，會建立一個區域，其中涵蓋對應于該 cascade 的深度緩衝區區段。</span><span class="sxs-lookup"><span data-stu-id="df7ee-206">For every cascade, a viewport is created that covers the section of the depth buffer corresponding to that cascade.</span></span> <span data-ttu-id="df7ee-207">因為只需要深度，所以會系結 null 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="df7ee-207">A null pixel shader is bound because only the depth is needed.</span></span> <span data-ttu-id="df7ee-208">最後，會針對每個串聯設定正確的視口和陰影矩陣，因為深度對應會在一次轉譯成主要陰影緩衝區。</span><span class="sxs-lookup"><span data-stu-id="df7ee-208">Finally, the correct viewport and shadow matrix are set for each cascade as the depth maps are rendered one at a time into the main shadow buffer.</span></span>

## <a name="render-the-scene"></a><span data-ttu-id="df7ee-209">呈現場景</span><span class="sxs-lookup"><span data-stu-id="df7ee-209">Render the Scene</span></span>

<span data-ttu-id="df7ee-210">包含陰影的緩衝區現在已系結至圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="df7ee-210">The buffer containing the shadows is now bound to the pixel shader.</span></span> <span data-ttu-id="df7ee-211">有兩種方法可以選取在 CascadedShadowMaps11 範例中執行的 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-211">There are two methods for selecting the cascade implemented in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="df7ee-212">這兩個方法會使用著色器程式碼來說明。</span><span class="sxs-lookup"><span data-stu-id="df7ee-212">These two methods are explained with shader code.</span></span>

### <a name="interval-based-cascade-selection"></a><span data-ttu-id="df7ee-213">Interval-Based Cascade 選取範圍</span><span class="sxs-lookup"><span data-stu-id="df7ee-213">Interval-Based Cascade Selection</span></span>

<span data-ttu-id="df7ee-214">**[圖 7]。以間隔為基礎的 cascade 選取範圍**</span><span class="sxs-lookup"><span data-stu-id="df7ee-214">**Figure 7. Interval-based cascade selection**</span></span>

![以間隔為基礎的 cascade 選取範圍](images/interval-based-cascade-selection.jpg)

<span data-ttu-id="df7ee-216">在以間隔為基礎的選取 ([圖 7]) 中，頂點著色器會計算頂點世界空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="df7ee-216">In interval-based selection (Figure 7), the vertex shader computes the position in world-space of the vertex.</span></span>


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



<span data-ttu-id="df7ee-217">圖元著色器會接收插補深度。</span><span class="sxs-lookup"><span data-stu-id="df7ee-217">The pixel shader receives the interpolated depth.</span></span>


```C++
fCurrentPixelDepth = Input.vDepth;
```



<span data-ttu-id="df7ee-218">以間隔為基礎的串聯選取會使用向量比較和點乘積來判斷正確的 cacade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-218">Interval-based cascade selection uses a vector comparison and a dot product to determine the correct cacade.</span></span> <span data-ttu-id="df7ee-219">串聯 \_ 計數旗標會 \_ 指定 CASCADE 的數目。</span><span class="sxs-lookup"><span data-stu-id="df7ee-219">The CASCADE\_COUNT\_FLAG specifies the number of cascades.</span></span> <span data-ttu-id="df7ee-220">M \_ fCascadeFrustumsEyeSpaceDepths \_ 資料會限制視圖的分割分割區。</span><span class="sxs-lookup"><span data-stu-id="df7ee-220">The m\_fCascadeFrustumsEyeSpaceDepths\_data constrains the view frustum partitions.</span></span> <span data-ttu-id="df7ee-221">在比較之後，fComparison 會包含值1，其中目前的圖元大於關卡，而當目前的串聯較小時，則為0值。</span><span class="sxs-lookup"><span data-stu-id="df7ee-221">After the comparison, the fComparison contains a value of 1 where the current pixel is larger than the barrier, and a value of 0 when the current cascade is smaller.</span></span> <span data-ttu-id="df7ee-222">點乘積會將這些值加總成陣列索引。</span><span class="sxs-lookup"><span data-stu-id="df7ee-222">A dot product sums these values into an array index.</span></span>


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



<span data-ttu-id="df7ee-223">選取 cascade 之後，材質座標必須轉換成正確的 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-223">Once the cascade is selected, the texture coordinate must be transformed to the correct cascade.</span></span>


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



<span data-ttu-id="df7ee-224">接著會使用這個材質座標，利用 X 座標和 Y 座標來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="df7ee-224">This texture coordinate is then used to sample the texture with the X-coordinate and the Y-coordinate.</span></span> <span data-ttu-id="df7ee-225">Z 座標用於進行最後的深度比較。</span><span class="sxs-lookup"><span data-stu-id="df7ee-225">The Z-coordinate is used to do the final depth comparison.</span></span>

### <a name="map-based-cascade-selection"></a><span data-ttu-id="df7ee-226">Map-Based Cascade 選取範圍</span><span class="sxs-lookup"><span data-stu-id="df7ee-226">Map-Based Cascade Selection</span></span>

<span data-ttu-id="df7ee-227">以地圖為基礎的選取範圍 (圖 8) 測試，以進行串聯的四邊，以找出涵蓋特定圖元的嚴謹對應。</span><span class="sxs-lookup"><span data-stu-id="df7ee-227">Map-based selection (Figure 8) tests against the four sides of the cascades to find the tightest map that covers the specific pixel.</span></span> <span data-ttu-id="df7ee-228">頂點著色器會計算每個串聯的視圖空間位置，而不是計算世界空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="df7ee-228">Instead of calculating the position in world space, the vertex shader calculates the view-space position for every cascade.</span></span> <span data-ttu-id="df7ee-229">圖元著色器會反復查看整個層級，以便縮放和移動材質座標，使其索引目前的串聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-229">The pixel shader iterates over the cascades in order to scale and shift the texture coordinates so that they index the current cascade.</span></span> <span data-ttu-id="df7ee-230">然後，紋理座標會針對材質界限進行測試。</span><span class="sxs-lookup"><span data-stu-id="df7ee-230">The texture coordinate is then tested against the texture bounds.</span></span> <span data-ttu-id="df7ee-231">當材質座標的 X 和 Y 值落在 cascade 內時，會用來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="df7ee-231">When the X and Y values of the texture coordinate fall inside a cascade, they are used to sample the texture.</span></span> <span data-ttu-id="df7ee-232">Z 座標用於進行最後的深度比較。</span><span class="sxs-lookup"><span data-stu-id="df7ee-232">The Z-coordinate is used to do the final depth comparison.</span></span>

<span data-ttu-id="df7ee-233">**圖8。以地圖為基礎的 cascade 選取範圍**</span><span class="sxs-lookup"><span data-stu-id="df7ee-233">**Figure 8. Map-based cascade selection**</span></span>

![以地圖為基礎的 cascade 選取範圍](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a><span data-ttu-id="df7ee-235">Interval-Based 選取專案與 Map-Based 選取專案</span><span class="sxs-lookup"><span data-stu-id="df7ee-235">Interval-Based Selection vs. Map-Based Selection</span></span>

<span data-ttu-id="df7ee-236">以間隔為基礎的選取比以地圖為基礎的選擇稍微快一點，因為串聯選取可以直接完成。</span><span class="sxs-lookup"><span data-stu-id="df7ee-236">Interval-based selection is slightly faster than map-based selection because the cascade selection can be done directly.</span></span> <span data-ttu-id="df7ee-237">以地圖為基礎的選取範圍必須與具有串聯界限的材質座標相交。</span><span class="sxs-lookup"><span data-stu-id="df7ee-237">Map-based selection must intersect the texture coordinate with the cascade bounds.</span></span>

<span data-ttu-id="df7ee-238">當陰影地圖未完全對齊 (請參閱 [圖 8]) ，以地圖為基礎的選項更有效率地使用 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-238">Map-based selection uses the cascade more efficiently when shadow maps do not align perfectly (see Figure 8).</span></span>

## <a name="blend-between-cascades"></a><span data-ttu-id="df7ee-239">在級聯之間 Blend</span><span class="sxs-lookup"><span data-stu-id="df7ee-239">Blend between Cascades</span></span>

<span data-ttu-id="df7ee-240">本文稍後討論的 VSMs () 和篩選技術（例如 PCF）可以搭配低解析度網用來產生軟陰影。</span><span class="sxs-lookup"><span data-stu-id="df7ee-240">VSMs (discussed later in this article) and filtering techniques such as PCF can be used with low-resolution CSMs to produce soft shadows.</span></span> <span data-ttu-id="df7ee-241">可惜的是，這會導致在串聯圖層之間看到接合 (圖 9) ，因為解析度不相符。</span><span class="sxs-lookup"><span data-stu-id="df7ee-241">Unfortunately, this results in a visible seam (Figure 9) between cascade layers because the resolution does not match.</span></span> <span data-ttu-id="df7ee-242">解決方法是在陰影地圖之間建立陰影測試，以同時針對這兩個級聯的執行陰影測試。</span><span class="sxs-lookup"><span data-stu-id="df7ee-242">The solution is to create a band between shadow maps where the shadow test is performed for both cascades.</span></span> <span data-ttu-id="df7ee-243">著色器接著會根據 blend 波段中圖元的位置，以線性方式在兩個值之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="df7ee-243">The shader then linearly interpolates between the two values based on the pixel's location in the blend band.</span></span> <span data-ttu-id="df7ee-244">範例 CascadedShadowMaps11 和 VarianceShadows11 提供 GUI 滑杆，可用來增加和減少這個模糊頻外。</span><span class="sxs-lookup"><span data-stu-id="df7ee-244">The samples CascadedShadowMaps11 and VarianceShadows11 provide a GUI slider that can be used to increase and decrease this blur band.</span></span> <span data-ttu-id="df7ee-245">著色器會執行動態分支，因此大部分的圖元都只會從目前的串聯讀取。</span><span class="sxs-lookup"><span data-stu-id="df7ee-245">The shader performs a dynamic branch so that the vast majority of pixels only read from the current cascade.</span></span>

<span data-ttu-id="df7ee-246">**[圖 9]。串聯接縫**</span><span class="sxs-lookup"><span data-stu-id="df7ee-246">**Figure 9. Cascade seams**</span></span>

![串聯接縫](images/cascade-seams.jpg)

<span data-ttu-id="df7ee-248"> (左) 可在重迭的情況下看見可見的接合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-248">(Left) A visible seam can be seen where cascades overlap.</span></span> <span data-ttu-id="df7ee-249"> (右) 當串聯混合在一起時，不會發生接合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-249">(Right) When the cascades are blended between, no seam occurs.</span></span>

## <a name="filtering-shadow-maps"></a><span data-ttu-id="df7ee-250">篩選陰影對應</span><span class="sxs-lookup"><span data-stu-id="df7ee-250">Filtering Shadow Maps</span></span>

### <a name="pcf"></a><span data-ttu-id="df7ee-251">PCF</span><span class="sxs-lookup"><span data-stu-id="df7ee-251">PCF</span></span>

<span data-ttu-id="df7ee-252">篩選一般陰影對應不會產生軟性模糊的陰影。</span><span class="sxs-lookup"><span data-stu-id="df7ee-252">Filtering ordinary shadow maps does not produce soft, blurred shadows.</span></span> <span data-ttu-id="df7ee-253">篩選硬體會模糊深度值，然後將這些模糊的值與 [光線空間] 材質進行比較。</span><span class="sxs-lookup"><span data-stu-id="df7ee-253">The filtering hardware blurs the depth values, and then compares those blurred values to the light space texel.</span></span> <span data-ttu-id="df7ee-254">通過/失敗測試所產生的硬性邊緣仍然存在。</span><span class="sxs-lookup"><span data-stu-id="df7ee-254">The hard edge resulting from the pass/fail test still exists.</span></span> <span data-ttu-id="df7ee-255">模糊陰影對應只是為了錯誤地移動固定邊緣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-255">Blurring shadow maps only serves to erroneously move the hard edge.</span></span> <span data-ttu-id="df7ee-256">PCF 可篩選陰影對應。</span><span class="sxs-lookup"><span data-stu-id="df7ee-256">PCF enables filtering on shadow maps.</span></span> <span data-ttu-id="df7ee-257">PCF 的一般概念是根據 subsamples 總數通過深度測試的 subsamples 數目，來計算陰影中圖元的百分比。</span><span class="sxs-lookup"><span data-stu-id="df7ee-257">The general idea of PCF is to calculate a percentage of the pixel in shadow based on the number of subsamples that pass the depth test over the total number of subsamples.</span></span>

<span data-ttu-id="df7ee-258">Direct3D 10 和 Direct3D 11 硬體可以執行 PCF。</span><span class="sxs-lookup"><span data-stu-id="df7ee-258">Direct3D 10 and Direct3D 11 hardware can perform PCF.</span></span> <span data-ttu-id="df7ee-259">PCF 取樣器的輸入是由材質座標和比較深度值所組成。</span><span class="sxs-lookup"><span data-stu-id="df7ee-259">The input to a PCF sampler consists of the texture-coordinate and a comparison depth value.</span></span> <span data-ttu-id="df7ee-260">為了簡單起見，PCF 會以四分點的篩選來說明。</span><span class="sxs-lookup"><span data-stu-id="df7ee-260">For simplicity, PCF is explained with a four-tap filter.</span></span> <span data-ttu-id="df7ee-261">紋理取樣器會讀取紋理四次，類似于標準篩選。</span><span class="sxs-lookup"><span data-stu-id="df7ee-261">The texture sampler reads the texture four times, similar to a standard filter.</span></span> <span data-ttu-id="df7ee-262">不過，傳回的結果是通過深度測試的圖元百分比。</span><span class="sxs-lookup"><span data-stu-id="df7ee-262">However, the returned result is a percentage of the pixels that passed the depth test.</span></span> <span data-ttu-id="df7ee-263">[圖 10] 顯示在四個深度測試中通過的圖元如何以陰影顯示25%。</span><span class="sxs-lookup"><span data-stu-id="df7ee-263">Figure 10 shows how a pixel that passes one of the four depth tests is 25 percent in shadow.</span></span> <span data-ttu-id="df7ee-264">實際傳回的值是以材質讀取的 subtexel 座標為基礎的線性插補，以產生平滑漸層。</span><span class="sxs-lookup"><span data-stu-id="df7ee-264">The actual value returned is a linear interpolation based on the subtexel coordinates of the texture reads to produce a smooth gradient.</span></span> <span data-ttu-id="df7ee-265">如果沒有這個線性插補，四點點的 PCF 只能傳回五個值： {0.0、0.25、0.5、0.75、1.0}。</span><span class="sxs-lookup"><span data-stu-id="df7ee-265">Without this linear interpolation, the four-tap PCF would only be able to return five values: { 0.0, 0.25, 0.5, 0.75, 1.0 }.</span></span>

<span data-ttu-id="df7ee-266">**[圖 10]PCF 篩選影像，涵蓋所選圖元的25%**</span><span class="sxs-lookup"><span data-stu-id="df7ee-266">**Figure 10. PCF filtered image, with 25 percent of the selected pixel covered**</span></span>

![pcf 篩選影像，涵蓋所選圖元的25%](images/pcf-filtered-image.png)

<span data-ttu-id="df7ee-268">您也可以在沒有硬體支援的情況下進行 PCF，或將 PCF 延伸至較大的核心。</span><span class="sxs-lookup"><span data-stu-id="df7ee-268">It is also possible to do PCF without hardware support or extend PCF to larger kernels.</span></span> <span data-ttu-id="df7ee-269">有些技術甚至是具有加權核心的範例。</span><span class="sxs-lookup"><span data-stu-id="df7ee-269">Some techniques even sample with a weighted kernel.</span></span> <span data-ttu-id="df7ee-270">若要這樣做，請建立一個核心 (，例如 N × N 方格的高斯) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-270">To do this, create a kernel (such as a Gaussian) for an N × N grid.</span></span> <span data-ttu-id="df7ee-271">權數必須新增至1。</span><span class="sxs-lookup"><span data-stu-id="df7ee-271">The weights must add up to 1.</span></span> <span data-ttu-id="df7ee-272">然後紋理會取樣 N2 次。</span><span class="sxs-lookup"><span data-stu-id="df7ee-272">The texture is then sampled N2 times.</span></span> <span data-ttu-id="df7ee-273">每個範例都會依核心中的對應權數進行調整。</span><span class="sxs-lookup"><span data-stu-id="df7ee-273">Each sample is scaled by the corresponding weights in the kernel.</span></span> <span data-ttu-id="df7ee-274">CascadedShadowMaps11 範例會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="df7ee-274">The CascadedShadowMaps11 sample uses this approach.</span></span>

### <a name="depth-bias"></a><span data-ttu-id="df7ee-275">深度偏差</span><span class="sxs-lookup"><span data-stu-id="df7ee-275">Depth Bias</span></span>

<span data-ttu-id="df7ee-276">使用大型 PCF 核心時，深度偏差會變得更重要。</span><span class="sxs-lookup"><span data-stu-id="df7ee-276">Depth bias becomes even more important when large PCF kernels are used.</span></span> <span data-ttu-id="df7ee-277">它只有在比較圖元的亮空間深度與它在深度對應中所對應的圖元時才有效。</span><span class="sxs-lookup"><span data-stu-id="df7ee-277">It is only valid to compare a pixel's light-space depth against the pixel it maps to in the depth map.</span></span> <span data-ttu-id="df7ee-278">深度對應材質的相鄰位置參考不同的位置。</span><span class="sxs-lookup"><span data-stu-id="df7ee-278">The depth map texel's neighbors refer to a different position.</span></span> <span data-ttu-id="df7ee-279">此深度很可能很類似，但可能會因場景而有所不同。</span><span class="sxs-lookup"><span data-stu-id="df7ee-279">This depth is likely to be similar, but can be very different depending on the scene.</span></span> <span data-ttu-id="df7ee-280">[圖 11] 反白顯示發生的構件。</span><span class="sxs-lookup"><span data-stu-id="df7ee-280">Figure 11 highlights the artifacts that occur.</span></span> <span data-ttu-id="df7ee-281">單一深度會與陰影地圖中的三個相鄰材質比較。</span><span class="sxs-lookup"><span data-stu-id="df7ee-281">A single depth is compared to three neighboring texels in the shadow map.</span></span> <span data-ttu-id="df7ee-282">其中一個深度測試失敗，因為它的深度與目前幾何的計算出的光線空間深度沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-282">One of the depth tests erroneously fails because its depth does not correlate to the computed light-space depth of the current geometry.</span></span> <span data-ttu-id="df7ee-283">此問題的建議解決方案是使用較大的位移。</span><span class="sxs-lookup"><span data-stu-id="df7ee-283">The recommended solution to this problem is to use a larger offset.</span></span> <span data-ttu-id="df7ee-284">但位移過大，可能會導致 Peter 移動。</span><span class="sxs-lookup"><span data-stu-id="df7ee-284">Too large of an offset, however, can result in Peter Panning.</span></span> <span data-ttu-id="df7ee-285">計算緊密接近的平面和目前的平面有助於降低使用位移的效果。</span><span class="sxs-lookup"><span data-stu-id="df7ee-285">Calculating a tight near plane and far plane helps reduce the effects of using an offset.</span></span>

<span data-ttu-id="df7ee-286">**[圖 11]錯誤的自我遮蔽**</span><span class="sxs-lookup"><span data-stu-id="df7ee-286">**Figure 11. Erroneous self-shadowing**</span></span>

![錯誤的自我遮蔽](images/erroneous-self-shadowing.png)

<span data-ttu-id="df7ee-288">錯誤的自我遮蔽結果，是因為比較光線空間深度的圖元與陰影地圖中未相互關聯的材質。</span><span class="sxs-lookup"><span data-stu-id="df7ee-288">The erroneous self-shadowing results from comparing pixels in the light-space depth to the texels in the shadow map that do not correlate.</span></span> <span data-ttu-id="df7ee-289">輕量空間的深度會與深度對應中的陰影材質2相關聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-289">The depth in light-space correlates to shadow texel 2 in the depth map.</span></span> <span data-ttu-id="df7ee-290">材質1大於光空間深度，而2等於，3則較少。</span><span class="sxs-lookup"><span data-stu-id="df7ee-290">Texel 1 is greater than the light-space depth while 2 is equal and 3 is less.</span></span> <span data-ttu-id="df7ee-291">材質2和3通過深度測試，而材質1失敗。</span><span class="sxs-lookup"><span data-stu-id="df7ee-291">Texels 2 and 3 pass the depth test, while Texel 1 fails.</span></span>

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a><span data-ttu-id="df7ee-292">使用針對大型 PCFs 的 DDX 和 DDY 來計算 Per-Texel 深度偏差</span><span class="sxs-lookup"><span data-stu-id="df7ee-292">Calculating a Per-Texel Depth Bias with DDX and DDY for Large PCFs</span></span>

<span data-ttu-id="df7ee-293">使用 **ddx** 來計算每個材質深度偏差和大型 PCFs 的 **ddy** ，是針對相鄰陰影對應材質計算正確深度偏差（假設表面為平面）的技術。</span><span class="sxs-lookup"><span data-stu-id="df7ee-293">Calculating a per texel depth bias with **ddx** and **ddy** for large PCFs is a technique that calculates the correct depth bias—assuming the surface is planar—for the adjacent shadow map texel.</span></span>

<span data-ttu-id="df7ee-294">這項技術使用衍生資訊來配合平面的比較深度。</span><span class="sxs-lookup"><span data-stu-id="df7ee-294">This technique fits the comparison depth to a plane using the derivative information.</span></span> <span data-ttu-id="df7ee-295">由於這項技術的運算複雜度很複雜，因此只有在 GPU 有計算迴圈可供使用時，才應該使用此技術。</span><span class="sxs-lookup"><span data-stu-id="df7ee-295">Because this technique is computationally complex, it should be used only when a GPU has compute cycles to spare.</span></span> <span data-ttu-id="df7ee-296">使用非常大型的核心時，這可能是唯一能移除自行遮蔽成品，而不會造成 Peter 移動的技巧。</span><span class="sxs-lookup"><span data-stu-id="df7ee-296">When very large kernels are used, this may be the only technique that works to remove self-shadowing artifacts without causing Peter Panning.</span></span>

<span data-ttu-id="df7ee-297">[圖 12] 強調問題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-297">Figure 12 highlights the problem.</span></span> <span data-ttu-id="df7ee-298">針對正在比較的一個材質，已知空間的深度是已知的。</span><span class="sxs-lookup"><span data-stu-id="df7ee-298">The depth in light-space is known for the one texel that is being compared.</span></span> <span data-ttu-id="df7ee-299">對應至深度對應中相鄰材質的光線空間深度未知。</span><span class="sxs-lookup"><span data-stu-id="df7ee-299">The light-space depths that correspond to the neighboring texels in the depth map are unknown.</span></span>

<span data-ttu-id="df7ee-300">**[圖 12]場景和深度對應**</span><span class="sxs-lookup"><span data-stu-id="df7ee-300">**Figure 12. Scene and depth map**</span></span>

![場景和深度對應](images/scene-and-depth-map.png)

<span data-ttu-id="df7ee-302">轉譯的場景會顯示在左側，而具有範例材質區塊的深度對應會顯示在右側。</span><span class="sxs-lookup"><span data-stu-id="df7ee-302">The rendered scene is shown at left, and the depth map with a sample texel block is shown at right.</span></span> <span data-ttu-id="df7ee-303">眼睛空間材質會對應至區塊中央中標示為 D 的圖元。</span><span class="sxs-lookup"><span data-stu-id="df7ee-303">The eye-space texel maps to the pixel labeled D in the center of the block.</span></span> <span data-ttu-id="df7ee-304">這項比較是正確的。</span><span class="sxs-lookup"><span data-stu-id="df7ee-304">This comparison is accurate.</span></span> <span data-ttu-id="df7ee-305">眼睛空間的正確深度，與鄰近 D 未知的圖元相關聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-305">The correct depth in eye space correlating to the pixels that neighbor D is unknown.</span></span> <span data-ttu-id="df7ee-306">只有當我們假設圖元與 D 的相同三角形時，才可以將連續的材質對應回眼睛空間。</span><span class="sxs-lookup"><span data-stu-id="df7ee-306">Mapping the neighboring texels back to eye space is possible only if we assume the pixel pertains to the same triangle as D.</span></span>

<span data-ttu-id="df7ee-307">材質的深度已知可與光線空間位置相互關聯。</span><span class="sxs-lookup"><span data-stu-id="df7ee-307">The depth is known for the texel that correlates with the light-space position.</span></span> <span data-ttu-id="df7ee-308">深度對應中的鄰近材質深度未知。</span><span class="sxs-lookup"><span data-stu-id="df7ee-308">The depth is unknown for the neighboring texels in the depth map.</span></span>

<span data-ttu-id="df7ee-309">概括而言，這項技術會使用 **ddx** 和 **ddy** HLSL 作業來尋找亮空間位置的衍生。</span><span class="sxs-lookup"><span data-stu-id="df7ee-309">At a high level, this technique uses the **ddx** and **ddy** HLSL operations to find the derivative of the light-space position.</span></span> <span data-ttu-id="df7ee-310">這是重要的，因為衍生作業會傳回相對於螢幕空間的光線空間深度漸層。</span><span class="sxs-lookup"><span data-stu-id="df7ee-310">This is nontrivial because the derivative operations return the gradient of the light-space depth with respect to screen space.</span></span> <span data-ttu-id="df7ee-311">若要將此轉換為與光線空間相關的光線空間深度漸層，則必須計算轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-311">To convert this to a gradient of the light-space depth with respect to light space, a conversion matrix must be calculated.</span></span>

### <a name="explanation-with-shader-code"></a><span data-ttu-id="df7ee-312">著色器程式碼的說明</span><span class="sxs-lookup"><span data-stu-id="df7ee-312">Explanation with Shader Code</span></span>

<span data-ttu-id="df7ee-313">演算法其餘部分的詳細資料會提供給執行這項作業的著色器程式碼的說明。</span><span class="sxs-lookup"><span data-stu-id="df7ee-313">The details of the rest of the algorithm are given as an explanation of the shader code that performs this operation.</span></span> <span data-ttu-id="df7ee-314">您可以在 CascadedShadowMaps11 範例中找到此程式碼。</span><span class="sxs-lookup"><span data-stu-id="df7ee-314">This code can be found in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="df7ee-315">[圖 13] 顯示輕量材質座標如何對應至深度對應，以及如何使用 X 和 Y 中的衍生來建立轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-315">Figure 13 shows how the light-space texture coordinates map to the depth map and how the derivatives in X and Y can be used to create a transformation matrix.</span></span>

<span data-ttu-id="df7ee-316">**[圖 13]畫面-空間至淺色矩陣**</span><span class="sxs-lookup"><span data-stu-id="df7ee-316">**Figure 13. Screen-space to light-space matrix**</span></span>

![畫面-空間至淺色矩陣](images/screen-space-to-light-space-matrix.png)

<span data-ttu-id="df7ee-318">X 和 Y 中的輕量位置的衍生項會用來建立此矩陣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-318">The derivatives of the light-space position in X and Y are used to create this matrix.</span></span>

<span data-ttu-id="df7ee-319">第一個步驟是計算淺色視圖空間位置的衍生。</span><span class="sxs-lookup"><span data-stu-id="df7ee-319">The first step is to calculate the derivative of the light-view-space position.</span></span>


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



<span data-ttu-id="df7ee-320">Direct3D 11 類別 Gpu 會以平行方式執行2×2四個圖元的方式來計算這些衍生，並從 X **中的相鄰** 節點減去 **ddy** 的鄰近區的材質座標。</span><span class="sxs-lookup"><span data-stu-id="df7ee-320">Direct3D 11 class GPUs calculate these derivatives by running 2 × 2 quad of pixels in parallel and subtracting the texture coordinates from the neighbor in X for **ddx** and from the neighbor in Y for **ddy**.</span></span> <span data-ttu-id="df7ee-321">這兩個衍生項組成了2×2矩陣的資料列。</span><span class="sxs-lookup"><span data-stu-id="df7ee-321">These two derivatives make up the rows of a 2 × 2 matrix.</span></span> <span data-ttu-id="df7ee-322">在其目前的表單中，這個矩陣可用來將螢幕空間連續的圖元轉換成輕量傾斜。</span><span class="sxs-lookup"><span data-stu-id="df7ee-322">In its current form, this matrix could be used to convert screen-space neighboring pixels to light-space slopes.</span></span> <span data-ttu-id="df7ee-323">不過，需要這個矩陣的反向。</span><span class="sxs-lookup"><span data-stu-id="df7ee-323">However, the inverse of this matrix is needed.</span></span> <span data-ttu-id="df7ee-324">需要將亮空間相鄰圖元轉換成螢幕空間傾斜的矩陣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-324">A matrix that transforms light-space neighboring pixels to screen-space slopes is needed.</span></span>


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



<span data-ttu-id="df7ee-325">**圖14。輕量到螢幕空間**</span><span class="sxs-lookup"><span data-stu-id="df7ee-325">**Figure 14. Light-space to screen-space**</span></span>

![輕量到螢幕空間](images/light-space-to-screen-space.png)

<span data-ttu-id="df7ee-327">然後，這個矩陣會用來將上述兩個材質轉換成目前材質的右邊和右邊。</span><span class="sxs-lookup"><span data-stu-id="df7ee-327">This matrix is then used to transform the two texels above and to the right of the current texel.</span></span> <span data-ttu-id="df7ee-328">這些鄰近專案會表示為與目前材質的位移。</span><span class="sxs-lookup"><span data-stu-id="df7ee-328">These neighbors are represented as an offset from the current texel.</span></span>


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



<span data-ttu-id="df7ee-329">矩陣所建立的比率最後乘以深度衍生，以計算相鄰圖元的深度位移。</span><span class="sxs-lookup"><span data-stu-id="df7ee-329">The ratio that the matrix creates is finally multiplied by the depth derivatives to calculate the depth offsets for the neighboring pixels.</span></span>


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



<span data-ttu-id="df7ee-330">這些權數現在可用於 PCF 迴圈，以將位移新增至位置。</span><span class="sxs-lookup"><span data-stu-id="df7ee-330">These weights can now be used in a PCF loop to add an offset to the position.</span></span>


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a><span data-ttu-id="df7ee-331">PCF 和網達網</span><span class="sxs-lookup"><span data-stu-id="df7ee-331">PCF and CSMs</span></span>

<span data-ttu-id="df7ee-332">PCF 無法在 Direct3D 10 中的材質陣列上運作。</span><span class="sxs-lookup"><span data-stu-id="df7ee-332">PCF does not work on texture arrays in Direct3D 10.</span></span> <span data-ttu-id="df7ee-333">若要使用 PCF，所有的級聯都會儲存在一個大型材質塔中。</span><span class="sxs-lookup"><span data-stu-id="df7ee-333">To use PCF, all of the cascades are stored in one large texture atlas.</span></span>

### <a name="derivative-based-offset"></a><span data-ttu-id="df7ee-334">Derivative-Based 位移</span><span class="sxs-lookup"><span data-stu-id="df7ee-334">Derivative-Based Offset</span></span>

<span data-ttu-id="df7ee-335">新增網網的衍生式位移會帶來一些挑戰。</span><span class="sxs-lookup"><span data-stu-id="df7ee-335">Adding the derivative based offsets for CSMs presents some challenges.</span></span> <span data-ttu-id="df7ee-336">這是因為分歧的流程式控制制內的衍生計算所致。</span><span class="sxs-lookup"><span data-stu-id="df7ee-336">This is due to a derivative calculation within divergent flow control.</span></span> <span data-ttu-id="df7ee-337">此問題的發生原因是 Gpu 運作的基本方式。</span><span class="sxs-lookup"><span data-stu-id="df7ee-337">The problem occurs because of a fundamental way that GPUs operate.</span></span> <span data-ttu-id="df7ee-338">Direct3D11 Gpu 在2×2四邊形的圖元上運作。</span><span class="sxs-lookup"><span data-stu-id="df7ee-338">Direct3D11 GPUs operate on 2 × 2 quads of pixels.</span></span> <span data-ttu-id="df7ee-339">為了執行衍生，Gpu 通常會從該相同變數的相鄰圖元複本減去目前圖元的變數複本。</span><span class="sxs-lookup"><span data-stu-id="df7ee-339">To perform a derivative, GPUs generally subtract the current pixel's copy of a variable from the neighboring pixel's copy of that same variable.</span></span> <span data-ttu-id="df7ee-340">這種情況的發生方式會因 GPU 而異。</span><span class="sxs-lookup"><span data-stu-id="df7ee-340">How this happens varies from GPU to GPU.</span></span> <span data-ttu-id="df7ee-341">材質座標取決於以地圖為基礎或以間隔為基礎的 cascade 選取。</span><span class="sxs-lookup"><span data-stu-id="df7ee-341">The texture coordinates are determined by map-based or interval-based cascade selection.</span></span> <span data-ttu-id="df7ee-342">圖元中的某些圖元會選擇不同于圖元其餘部分的 cascade。</span><span class="sxs-lookup"><span data-stu-id="df7ee-342">Some pixels in a pixel quad choose a different cascade than the rest of the pixels.</span></span> <span data-ttu-id="df7ee-343">這會導致陰影地圖之間出現接縫，因為衍生的位移現在是完全錯誤的。</span><span class="sxs-lookup"><span data-stu-id="df7ee-343">This results in visible seams between shadow maps because the derivative-based offsets are now completely wrong.</span></span> <span data-ttu-id="df7ee-344">解決方法是在亮色空間材質座標上執行衍生。</span><span class="sxs-lookup"><span data-stu-id="df7ee-344">The solution is to perform the derivative on light-view space texture coordinates.</span></span> <span data-ttu-id="df7ee-345">這些座標組每個串聯都是相同的。</span><span class="sxs-lookup"><span data-stu-id="df7ee-345">These coordinates are the same for every cascade.</span></span>

### <a name="padding-for-pcf-kernels"></a><span data-ttu-id="df7ee-346">PCF 核心的填補</span><span class="sxs-lookup"><span data-stu-id="df7ee-346">Padding for PCF Kernels</span></span>

<span data-ttu-id="df7ee-347">如果未填補陰影緩衝區，則為串聯分割區以外的 PCF 核心索引。</span><span class="sxs-lookup"><span data-stu-id="df7ee-347">PCF kernels index outside of a cascade partition if the shadow buffer is not padded.</span></span> <span data-ttu-id="df7ee-348">解決方法是以 PCF 核心的一半大小來填補 cascade 的外緣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-348">The solution is to pad the outer rim of the cascade by one-half the size of the PCF kernel.</span></span> <span data-ttu-id="df7ee-349">這必須在著色器中執行，以選取要在投影矩陣中選取串聯和，且必須將框線轉譯得夠大，才能保留框線。</span><span class="sxs-lookup"><span data-stu-id="df7ee-349">This must be implemented in the shader that selects the cascade and in the projection matrix that must render the cascade large enough that the border is preserved.</span></span>

## <a name="variance-shadow-maps"></a><span data-ttu-id="df7ee-350">差異陰影對應</span><span class="sxs-lookup"><span data-stu-id="df7ee-350">Variance Shadow Maps</span></span>

<span data-ttu-id="df7ee-351">VSMs (如需詳細資訊，請參閱 Donnelly 和 Lauritzen 的變異數 [陰影](https://portal.acm.org/citation.cfm?doid=1111411.1111440) 對應，) 啟用直接陰影對應篩選。</span><span class="sxs-lookup"><span data-stu-id="df7ee-351">VSMs (see [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440) by Donnelly and Lauritzen for more information) enable direct shadow map filtering.</span></span> <span data-ttu-id="df7ee-352">使用 VSMs 時，可以使用材質篩選硬體的所有功能。</span><span class="sxs-lookup"><span data-stu-id="df7ee-352">When using VSMs, all of the power of the texture-filtering hardware can be used.</span></span> <span data-ttu-id="df7ee-353">三線性和各向異性 ([圖 15]) 篩選都可以使用。</span><span class="sxs-lookup"><span data-stu-id="df7ee-353">Trilinear and anisotropic (Figure 15) filtering can be used.</span></span> <span data-ttu-id="df7ee-354">此外，VSMs 也可以直接透過卷積來模糊。</span><span class="sxs-lookup"><span data-stu-id="df7ee-354">Additionally, VSMs can be blurred directly through convolution.</span></span> <span data-ttu-id="df7ee-355">VSMs 的確有一些缺點;您必須將兩個深度資料通道儲存 (深度和深度平方) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-355">VSMs do have some drawbacks; two channels of depth data must be stored (depth and depth squared).</span></span> <span data-ttu-id="df7ee-356">當陰影重迭時，輕不規則很常見。</span><span class="sxs-lookup"><span data-stu-id="df7ee-356">When shadows overlap, light-bleeding is common.</span></span> <span data-ttu-id="df7ee-357">不過，它們的運作方式很低，而且可以與網達網的結合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-357">They work well, however, with lower resolutions and can be combined with CSMs.</span></span>

<span data-ttu-id="df7ee-358">**[圖 15]各向異性篩選**</span><span class="sxs-lookup"><span data-stu-id="df7ee-358">**Figure 15. Anisotropic filtering**</span></span>

![各向異性篩選](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a><span data-ttu-id="df7ee-360">演算法詳細資料</span><span class="sxs-lookup"><span data-stu-id="df7ee-360">Algorithm Details</span></span>

<span data-ttu-id="df7ee-361">將深度和深度平方轉譯成雙聲道陰影地圖，以 VSMs 工作。</span><span class="sxs-lookup"><span data-stu-id="df7ee-361">VSMs work by rendering the depth and the depth squared to a two-channel shadow map.</span></span> <span data-ttu-id="df7ee-362">然後，這兩個通道的陰影地圖可以模糊並篩選，就像一般材質一樣。</span><span class="sxs-lookup"><span data-stu-id="df7ee-362">This two-channel shadow map can then be blurred and filtered just like a normal texture.</span></span> <span data-ttu-id="df7ee-363">然後，演算法會在圖元著色器中使用 Chebychev 的不相等，來估計會通過深度測試的圖元區域分數。</span><span class="sxs-lookup"><span data-stu-id="df7ee-363">The algorithm then uses Chebychev's Inequality in the pixel shader to estimate the fraction of pixel area that would pass the depth test.</span></span>

<span data-ttu-id="df7ee-364">圖元著色器會提取深度和深度平方值。</span><span class="sxs-lookup"><span data-stu-id="df7ee-364">The pixel shader fetches the depth and depth-squared values.</span></span>


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



<span data-ttu-id="df7ee-365">會執行深度比較。</span><span class="sxs-lookup"><span data-stu-id="df7ee-365">The depth comparison is performed.</span></span>


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



<span data-ttu-id="df7ee-366">如果深度比較失敗，則會預估光線的圖元百分比。</span><span class="sxs-lookup"><span data-stu-id="df7ee-366">If the depth comparison fails, the percentage of the pixel that is lit is estimated.</span></span> <span data-ttu-id="df7ee-367">變異數是以平均平方減去平均平方來計算。</span><span class="sxs-lookup"><span data-stu-id="df7ee-367">Variance is calculated as average-of-squares minus square-of-average.</span></span>


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



<span data-ttu-id="df7ee-368">FPercentLit 值是 Chebychev 不相等的估計值。</span><span class="sxs-lookup"><span data-stu-id="df7ee-368">The fPercentLit value is estimated with Chebychev's Inequality.</span></span>


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a><span data-ttu-id="df7ee-369">光線不規則</span><span class="sxs-lookup"><span data-stu-id="df7ee-369">Light Bleeding</span></span>

<span data-ttu-id="df7ee-370">VSMs 的最大缺點是淺不規則 (圖 16) 。</span><span class="sxs-lookup"><span data-stu-id="df7ee-370">The biggest drawback to VSMs is light bleeding (Figure 16).</span></span> <span data-ttu-id="df7ee-371">當多個陰影輪子彼此遮蔽時，就會發生輕微的不規則情形。</span><span class="sxs-lookup"><span data-stu-id="df7ee-371">Light bleeding occurs when multiple shadow casters occlude each other along edges.</span></span> <span data-ttu-id="df7ee-372">VSMs 會根據深度 disparities 來為陰影邊緣加上陰影。</span><span class="sxs-lookup"><span data-stu-id="df7ee-372">VSMs shade the edges of shadows based on depth disparities.</span></span> <span data-ttu-id="df7ee-373">當遮蔽互相重迭時，區域中間的深度差異會存在於應遮蔽的區域中。</span><span class="sxs-lookup"><span data-stu-id="df7ee-373">When shadows overlap each other, a depth disparity exists in the center of a region that should be shadowed.</span></span> <span data-ttu-id="df7ee-374">這是使用 VSM 演算法的問題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-374">This is a problem with using the VSM algorithm.</span></span>

<span data-ttu-id="df7ee-375">**[圖 16]VSM 光線不規則**</span><span class="sxs-lookup"><span data-stu-id="df7ee-375">**Figure 16. VSM light bleeding**</span></span>

![vsm 光線不規則](images/vsm-light-bleeding.png)

<span data-ttu-id="df7ee-377">問題的部分解決方法是將 fPercentLit 提升至電源。</span><span class="sxs-lookup"><span data-stu-id="df7ee-377">A partial solution to the problem is to raise the fPercentLit to a power.</span></span> <span data-ttu-id="df7ee-378">這有抑制模糊的效果，這可能會導致深度差異很小的構件。</span><span class="sxs-lookup"><span data-stu-id="df7ee-378">This has the effect of dampening the blur, which can cause artifacts where depth disparity is small.</span></span> <span data-ttu-id="df7ee-379">有時候會有可緩和問題的神奇值。</span><span class="sxs-lookup"><span data-stu-id="df7ee-379">Sometimes there exists a magical value that alleviates the problem.</span></span>


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



<span data-ttu-id="df7ee-380">提高乘冪百分比的替代方式是避免陰影重迭的設定。</span><span class="sxs-lookup"><span data-stu-id="df7ee-380">An alternative to raising the percent lit to a power is to avoid configurations where shadows overlap.</span></span> <span data-ttu-id="df7ee-381">甚至高度調整的陰影設定在燈光、攝影機和幾何上有數個限制。</span><span class="sxs-lookup"><span data-stu-id="df7ee-381">Even highly tuned shadow configurations have several constraints on light, camera, and geometry.</span></span> <span data-ttu-id="df7ee-382">使用較高解析度紋理也可減少輕量。</span><span class="sxs-lookup"><span data-stu-id="df7ee-382">Light bleeding is also lessened by using higher resolution textures.</span></span>

<span data-ttu-id="df7ee-383">分層變異數陰影對應 (LVSMs) 解決此問題，代價是將分割分解為與光線垂直的圖層。</span><span class="sxs-lookup"><span data-stu-id="df7ee-383">Layered variance shadow maps (LVSMs) solve the problem at the expense of breaking the frustum into layers that are perpendicular to the light.</span></span> <span data-ttu-id="df7ee-384">當您也使用了網達者時，所需的地圖數量會相當大。</span><span class="sxs-lookup"><span data-stu-id="df7ee-384">The number of maps required would be quite large when CSMs are also being used.</span></span>

<span data-ttu-id="df7ee-385">此外，Andrew Lauritzen 是 VSMs 的白皮書共同作者，以及 LVSMs 的作者，討論了如何將指數陰影地圖 (ESMs) 與 VSMs 結合，以在 [Beyond3D 論壇](https://forum.beyond3d.com/showthread.php?t=47427)中抵禦淺的混合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-385">Additionally, Andrew Lauritzen, co-author of the paper on VSMs, and author of a paper on LVSMs, discussed combining exponential shadow maps (ESMs) with VSMs to counteract light blending in a [Beyond3D Forum](https://forum.beyond3d.com/showthread.php?t=47427).</span></span>

## <a name="vsms-with-csms"></a><span data-ttu-id="df7ee-386">使用網 VSMs</span><span class="sxs-lookup"><span data-stu-id="df7ee-386">VSMs with CSMs</span></span>

<span data-ttu-id="df7ee-387">範例 VarianceShadow11 結合了 VSMs 和網。</span><span class="sxs-lookup"><span data-stu-id="df7ee-387">The sample VarianceShadow11 combines VSMs and CSMs.</span></span> <span data-ttu-id="df7ee-388">組合相當簡單。</span><span class="sxs-lookup"><span data-stu-id="df7ee-388">The combination is fairly straightforward.</span></span> <span data-ttu-id="df7ee-389">此範例會遵循與 CascadedShadowMaps11 範例相同的步驟。</span><span class="sxs-lookup"><span data-stu-id="df7ee-389">The sample follows the same steps as the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="df7ee-390">因為未使用 PCF，所以陰影在兩個可分隔的可分離的卷積中會模糊。</span><span class="sxs-lookup"><span data-stu-id="df7ee-390">Because PCF is not used, the shadows are blurred in a two-pass separable convolution.</span></span> <span data-ttu-id="df7ee-391">若未使用 PCF，也會讓範例使用材質陣列，而不是使用材質塔。</span><span class="sxs-lookup"><span data-stu-id="df7ee-391">Not using PCF also enables the sample to use texture arrays instead of a texture atlas.</span></span> <span data-ttu-id="df7ee-392">材質陣列上的 PCF 是 Direct3D 10.1 功能。</span><span class="sxs-lookup"><span data-stu-id="df7ee-392">PCF on texture arrays is a Direct3D 10.1 feature.</span></span>

### <a name="gradients-with-csms"></a><span data-ttu-id="df7ee-393">使用網網的漸層</span><span class="sxs-lookup"><span data-stu-id="df7ee-393">Gradients with CSMs</span></span>

<span data-ttu-id="df7ee-394">使用具有網的漸層時，可以在兩個層級的框線之間產生接合，如圖17所示。</span><span class="sxs-lookup"><span data-stu-id="df7ee-394">Using gradients with CSMs can produce a seam along the border between two cascades as seen in Figure 17.</span></span> <span data-ttu-id="df7ee-395">範例指令會使用圖元之間的衍生，來計算篩選所需的資訊，例如 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="df7ee-395">The sample instruction uses derivatives between pixels to calculate information, such as the mipmap level, needed by the filter.</span></span> <span data-ttu-id="df7ee-396">這會造成 mipmap 選擇或非特殊篩選的特殊問題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-396">This causes a problem in particular for mipmap selection or anisotropic filtering.</span></span> <span data-ttu-id="df7ee-397">當四個四個圖元在著色器中採用不同的分支時，GPU 硬體所計算的衍生衍生項就會無效。</span><span class="sxs-lookup"><span data-stu-id="df7ee-397">When pixels in a quad take different branches in the shader, the derivatives calculated by the GPU hardware are invalid.</span></span> <span data-ttu-id="df7ee-398">這會導致沿著陰影地圖的不規則接合。</span><span class="sxs-lookup"><span data-stu-id="df7ee-398">This results in a jagged seam along the shadow map.</span></span>

<span data-ttu-id="df7ee-399">**[圖 17]由於具有分歧流程式控制制的非等向篩選，因此出現串聯框線的接縫**</span><span class="sxs-lookup"><span data-stu-id="df7ee-399">**Figure 17. Seams on cascade borders due to anisotropic filtering with divergent flow control**</span></span>

![由於具有分歧流程式控制制的非等向篩選，因此出現串聯框線的接縫](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

<span data-ttu-id="df7ee-401">此問題的解決方式是在亮視野空間中的位置計算衍生的衍生項;輕量空間座標不是選取的串聯所特有。</span><span class="sxs-lookup"><span data-stu-id="df7ee-401">This problem is solved by computing the derivatives on the position in light-view space; the light-view space coordinate is not specific to the selected cascade.</span></span> <span data-ttu-id="df7ee-402">計算的衍生範圍可依投射紋理矩陣的縮放部分，調整為正確的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="df7ee-402">The computed derivatives can be scaled by the scale portion of the projection-texture matrix to the correct mipmap level.</span></span>


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a><span data-ttu-id="df7ee-403">VSMs 相較于具有 PCF 的標準陰影</span><span class="sxs-lookup"><span data-stu-id="df7ee-403">VSMs Compared to Standard Shadows with PCF</span></span>

<span data-ttu-id="df7ee-404">VSMs 和 PCF 都會嘗試接近將通過深度測試的圖元區域分數。</span><span class="sxs-lookup"><span data-stu-id="df7ee-404">Both VSMs and PCF attempt to approximate the fraction of pixel area that would pass the depth test.</span></span> <span data-ttu-id="df7ee-405">VSMs 使用篩選硬體，並可利用可分隔的核心加以模糊處理。</span><span class="sxs-lookup"><span data-stu-id="df7ee-405">VSMs work with filtering hardware and can be blurred with separable kernels.</span></span> <span data-ttu-id="df7ee-406">可分離的卷積核心比完整核心更便宜。</span><span class="sxs-lookup"><span data-stu-id="df7ee-406">Separable convolution kernels are considerably cheaper to implement than a full kernel.</span></span> <span data-ttu-id="df7ee-407">此外，VSMs 會比較一個光線空間深度與輕量空間深度對應中的一個值。</span><span class="sxs-lookup"><span data-stu-id="df7ee-407">Additionally, VSMs compare one light-space depth against one value in the light-space depth map.</span></span> <span data-ttu-id="df7ee-408">這表示 VSMs 與 PCF 沒有相同的位移問題。</span><span class="sxs-lookup"><span data-stu-id="df7ee-408">This means that VSMs do not have the same offset problems as PCF.</span></span> <span data-ttu-id="df7ee-409">技術上來說，VSMs 是較大區域的取樣深度，以及執行統計分析。</span><span class="sxs-lookup"><span data-stu-id="df7ee-409">Technically, VSMs are sampling depth over a greater area, as well as performing a statistical analysis.</span></span> <span data-ttu-id="df7ee-410">這比 PCF 更精確。</span><span class="sxs-lookup"><span data-stu-id="df7ee-410">This is less precise than PCF.</span></span> <span data-ttu-id="df7ee-411">在實務上，VSMs 會進行一項非常好的混合作業，這會導致需要的位移較少。</span><span class="sxs-lookup"><span data-stu-id="df7ee-411">In practice, VSMs do a very good job of blending, which results in less offset being necessary.</span></span> <span data-ttu-id="df7ee-412">如上所述，VSMs 的一種缺點是輕量。</span><span class="sxs-lookup"><span data-stu-id="df7ee-412">As described above, the number one drawback to VSMs is light bleeding.</span></span>

<span data-ttu-id="df7ee-413">VSMs 和 PCF 代表 GPU 計算能力和 GPU 材質頻寬之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="df7ee-413">VSMs and PCF represent a trade-off between GPU compute power and GPU texture bandwidth.</span></span> <span data-ttu-id="df7ee-414">VSMs 需要執行更多數學運算來計算變異數。</span><span class="sxs-lookup"><span data-stu-id="df7ee-414">VSMs require more math to be performed to calculate the variance.</span></span> <span data-ttu-id="df7ee-415">PCF 需要更多紋理記憶體頻寬。</span><span class="sxs-lookup"><span data-stu-id="df7ee-415">PCF requires more texture memory bandwidth.</span></span> <span data-ttu-id="df7ee-416">大型 PCF 核心可能會因為材質頻寬很快就會變成瓶頸。</span><span class="sxs-lookup"><span data-stu-id="df7ee-416">Large PCF kernels can quickly become bottlenecked by texture bandwidth.</span></span> <span data-ttu-id="df7ee-417">隨著 gpu 計算能力的成長速度比 GPU 頻寬更快，VSMs 會變得更實際的這兩種演算法。</span><span class="sxs-lookup"><span data-stu-id="df7ee-417">With GPU computation power growing more rapidly than GPU bandwidth, VSMs are becoming the more practical of the two algorithms.</span></span> <span data-ttu-id="df7ee-418">由於混合和篩選，VSMs 也能以較低解析度的陰影地圖呈現更好的效果。</span><span class="sxs-lookup"><span data-stu-id="df7ee-418">VSMs also look better with lower resolution shadow maps due to blending and filtering.</span></span>

## <a name="summary"></a><span data-ttu-id="df7ee-419">總結</span><span class="sxs-lookup"><span data-stu-id="df7ee-419">Summary</span></span>

<span data-ttu-id="df7ee-420">網網的解決方案提供了觀點別名問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="df7ee-420">CSMs offer a solution to the perspective aliasing problem.</span></span> <span data-ttu-id="df7ee-421">有幾個可能的設定可取得標題的需要視覺精確度。</span><span class="sxs-lookup"><span data-stu-id="df7ee-421">There are several possible configurations to get the needed visual fidelity for a title.</span></span> <span data-ttu-id="df7ee-422">PCF 和 VSMs 廣泛使用，且應與網合併以減少別名。</span><span class="sxs-lookup"><span data-stu-id="df7ee-422">PCF and VSMs are widely used and should be combined with CSMs to reduce aliasing.</span></span>

## <a name="references"></a><span data-ttu-id="df7ee-423">參考資料</span><span class="sxs-lookup"><span data-stu-id="df7ee-423">References</span></span>

<span data-ttu-id="df7ee-424">Donnelly、W. 和 Lauritzen，A. 變異數 [陰影對應](https://portal.acm.org/citation.cfm?doid=1111411.1111440)。</span><span class="sxs-lookup"><span data-stu-id="df7ee-424">Donnelly, W. and Lauritzen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440).</span></span> <span data-ttu-id="df7ee-425">在 SI3D ' 06：互動式3D 圖形和遊戲的 2006 symposium 的訴訟。</span><span class="sxs-lookup"><span data-stu-id="df7ee-425">In SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games.</span></span> <span data-ttu-id="df7ee-426">2006。</span><span class="sxs-lookup"><span data-stu-id="df7ee-426">2006.</span></span> <span data-ttu-id="df7ee-427">pp. 161-165。</span><span class="sxs-lookup"><span data-stu-id="df7ee-427">pp. 161–165.</span></span> <span data-ttu-id="df7ee-428">美國紐約州紐約市：執行長按。</span><span class="sxs-lookup"><span data-stu-id="df7ee-428">New York, NY, USA: ACM Press.</span></span>

<span data-ttu-id="df7ee-429">Lauritzen、Andrew 和 McCool、Michael。</span><span class="sxs-lookup"><span data-stu-id="df7ee-429">Lauritzen, Andrew and McCool, Michael.</span></span> <span data-ttu-id="df7ee-430">[分層變異數陰影對應](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992)。</span><span class="sxs-lookup"><span data-stu-id="df7ee-430">[Layered variance shadow maps](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992).</span></span> <span data-ttu-id="df7ee-431">圖形介面2008、5月28日、30、2008、Windsor、安大略省、加拿大的訴訟。</span><span class="sxs-lookup"><span data-stu-id="df7ee-431">Proceedings of graphics interface 2008, May 28–30, 2008, Windsor, Ontario, Canada.</span></span>

<span data-ttu-id="df7ee-432">Engel，Woflgang f. 第4節。</span><span class="sxs-lookup"><span data-stu-id="df7ee-432">Engel, Woflgang F. Section 4.</span></span> <span data-ttu-id="df7ee-433">串聯陰影地圖。</span><span class="sxs-lookup"><span data-stu-id="df7ee-433">Cascaded Shadow Maps.</span></span> <span data-ttu-id="df7ee-434">ShaderX5，Advanced 轉譯技巧，Wolfgang Engel，Ed。</span><span class="sxs-lookup"><span data-stu-id="df7ee-434">ShaderX5 , Advanced Rendering Techniques, Wolfgang F. Engel, Ed.</span></span> <span data-ttu-id="df7ee-435">麻塞諸塞州波士頓 Charles 河媒體。</span><span class="sxs-lookup"><span data-stu-id="df7ee-435">Charles River Media, Boston, Massachusetts.</span></span> <span data-ttu-id="df7ee-436">2006。</span><span class="sxs-lookup"><span data-stu-id="df7ee-436">2006.</span></span> <span data-ttu-id="df7ee-437">pp. 197 –206。</span><span class="sxs-lookup"><span data-stu-id="df7ee-437">pp. 197–206.</span></span>

 

 
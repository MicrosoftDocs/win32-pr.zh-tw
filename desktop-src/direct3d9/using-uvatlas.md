---
description: 許多轉譯和內容產生技巧都需要2D 信號 (的唯一、非重迭地圖，例如紋理) 到網格上。
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: '使用 UVAtlas (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826326"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="f2869-103">使用 UVAtlas (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="f2869-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="f2869-104">UVAtlas 最初是隨附于現已淘汰的 D3DX9 utilty 程式庫中。</span><span class="sxs-lookup"><span data-stu-id="f2869-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="f2869-105">您可以從 [UV 的 Command-Line 工具 (uvatlas.exe) ](https://github.com/Microsoft/UVAtlas)取得最新版本。</span><span class="sxs-lookup"><span data-stu-id="f2869-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="f2869-106">許多轉譯和內容產生技巧都需要2D 信號 (的唯一、非重迭地圖，例如紋理) 到網格上。</span><span class="sxs-lookup"><span data-stu-id="f2869-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="f2869-107">這類技術包括：</span><span class="sxs-lookup"><span data-stu-id="f2869-107">Such techniques include:</span></span>

-   <span data-ttu-id="f2869-108">標準/置換對應</span><span class="sxs-lookup"><span data-stu-id="f2869-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="f2869-109">材質空間 PRT 模擬和燈光地圖</span><span class="sxs-lookup"><span data-stu-id="f2869-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="f2869-110">表面繪製</span><span class="sxs-lookup"><span data-stu-id="f2869-110">Surface painting</span></span>
-   <span data-ttu-id="f2869-111">材質區域光源</span><span class="sxs-lookup"><span data-stu-id="f2869-111">Texture-space lighting</span></span>

<span data-ttu-id="f2869-112">手動產生唯一的 UV 對應通常很耗時且繁瑣。當輸入幾何很複雜，而且需要有效率/低扭曲的材質空間使用量時，更是如此。</span><span class="sxs-lookup"><span data-stu-id="f2869-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="f2869-113">下圖顯示範例網格及其對應的材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![顯示範例網格及其對應的材質塔。](images/uvatlas1.jpg)

<span data-ttu-id="f2869-115">此範例會在左邊的) 顯示網格 (，並在右) 上顯示對應的 UV 空間一般地圖 (。</span><span class="sxs-lookup"><span data-stu-id="f2869-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="f2869-116">請注意，材質塔包含數個群組或資料叢集;每個叢集都稱為「圖表」，而在上述範例中，顯示會包含網格部分的一般資料。</span><span class="sxs-lookup"><span data-stu-id="f2869-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="f2869-117">D3DX UVAtlas Api 會自動產生最佳、非重迭的材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="f2869-118">Api 提供的輸入參數可讓您：</span><span class="sxs-lookup"><span data-stu-id="f2869-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="f2869-119">將材質延展、扭曲和 undersampling 降至最低。</span><span class="sxs-lookup"><span data-stu-id="f2869-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="f2869-120">最大化材質空間封裝密度，以有效率地使用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f2869-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="f2869-121">提供跨網格的平均取樣，將取樣頻率的不連續降到最低。</span><span class="sxs-lookup"><span data-stu-id="f2869-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="f2869-122">UVAtlas 的運作方式</span><span class="sxs-lookup"><span data-stu-id="f2869-122">How UVAtlas Works</span></span>

<span data-ttu-id="f2869-123">UVAtlas Api (查看 [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式，) 透過將圖層分割成圖表並將圖表封裝成材質塔來產生材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="f2869-124">使用 [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) 和 [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) 分別執行這些步驟;或者，您可以使用 [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) ，在單一呼叫中進行資料分割、參數化和套件。</span><span class="sxs-lookup"><span data-stu-id="f2869-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="f2869-125">分割和參數化網格</span><span class="sxs-lookup"><span data-stu-id="f2869-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="f2869-126">使用整合式度量張量來控制參數化</span><span class="sxs-lookup"><span data-stu-id="f2869-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="f2869-127">針對使用者指定的 Creases 使用相鄰資料</span><span class="sxs-lookup"><span data-stu-id="f2869-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="f2869-128">將圖表封裝到塔</span><span class="sxs-lookup"><span data-stu-id="f2869-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="f2869-129">分割和參數化網格</span><span class="sxs-lookup"><span data-stu-id="f2869-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="f2869-130">首先，網格會分割成圖表，然後每個圖表會參數化為自己的 \[ 0、1個 \] UV 空間。</span><span class="sxs-lookup"><span data-stu-id="f2869-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="f2869-131">圓柱可由一個圖表參數化;另一方面，球體將需要兩個圖表，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f2869-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![分割成兩個圖表之球體的圖例](images/uvatlas3.jpg)

<span data-ttu-id="f2869-133">可以使用單一圖表參數化的網格會分類為「homeomorphic 至磁片」，這表示您可以將無限彈性、可無限延伸的磁片分散到圖表上，並完全涵蓋幾何。</span><span class="sxs-lookup"><span data-stu-id="f2869-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="f2869-134">這種延展功能（稱為 homeomorphism）是雙向函式;這表示您可以從一個參數化移至另一個參數，而不會遺失資訊。</span><span class="sxs-lookup"><span data-stu-id="f2869-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="f2869-135">很少的真實世界網格可以參數化為兩個維度，而不需要將網格分隔成叢集或圖表。</span><span class="sxs-lookup"><span data-stu-id="f2869-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="f2869-136">下圖顯示另一個範例網格及其對應的材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![顯示具有不同圖形及其對應材質塔的範例網格。](images/uvatlas2.jpg)

<span data-ttu-id="f2869-138">有兩個參數可決定所建立的圖表數目：</span><span class="sxs-lookup"><span data-stu-id="f2869-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="f2869-139">可供塔使用的圖表數目上限</span><span class="sxs-lookup"><span data-stu-id="f2869-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="f2869-140">每個圖表允許的最大延展量</span><span class="sxs-lookup"><span data-stu-id="f2869-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="f2869-141">延展量將會決定所產生的圖表數目，以及取樣的整體品質。</span><span class="sxs-lookup"><span data-stu-id="f2869-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="f2869-142">從0.0 延展範圍 (不會) 到 1.0 (任何延展) 量。</span><span class="sxs-lookup"><span data-stu-id="f2869-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="f2869-143">D3DXUVAtlasCreate 和 D3DXUVAtlasPartition 會傳回演算法產生的最大延展。</span><span class="sxs-lookup"><span data-stu-id="f2869-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="f2869-144">下圖顯示另一個範例網格及其對應的材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![範例網格及其對應的材質塔圖](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="f2869-146">使用整合式度量張量來控制參數化</span><span class="sxs-lookup"><span data-stu-id="f2869-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="f2869-147">您可以根據每個三角形來指定材質間距的優先順序。</span><span class="sxs-lookup"><span data-stu-id="f2869-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="f2869-148">您可以提供整合的度量張量，以控制在產生的材質空間塔中如何伸展三角形。</span><span class="sxs-lookup"><span data-stu-id="f2869-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="f2869-149">您可以使用 D3DX IMT 計算函數，直接指定 IMT 的，也可以根據輸入信號來計算。</span><span class="sxs-lookup"><span data-stu-id="f2869-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="f2869-150">整合式計量 tensor (或 IMT) 是對稱的2x2 矩陣，描述如何在塔中將三角形伸展。</span><span class="sxs-lookup"><span data-stu-id="f2869-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="f2869-151">每個 IMT 都是由3個浮點數定義， (a，b，c) 來呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="f2869-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="f2869-152">它們可以在對稱2x2 矩陣中排列，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f2869-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="f2869-153">然後，IMT 可以用來尋找兩個向量之間的距離。</span><span class="sxs-lookup"><span data-stu-id="f2869-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="f2869-154">假設有兩個向量 v1 和 v2，其中：</span><span class="sxs-lookup"><span data-stu-id="f2869-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="f2869-155">V1 與 v2 之間的距離可以計算如下：</span><span class="sxs-lookup"><span data-stu-id="f2869-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="f2869-156">換句話說，向量 (s，t) 可能是以 u-v 空間的任意方向延展的大小。</span><span class="sxs-lookup"><span data-stu-id="f2869-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="f2869-157">在此情況下，s 向量是從第一個頂點到第二個頂點的方向，而 t 是標準和 s 的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="f2869-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="f2869-158">例如：</span><span class="sxs-lookup"><span data-stu-id="f2869-158">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="f2869-159">您可以使用 D3DX IMT 計算函數（D3DXComputeIMTFromPerVertexSignal、D3DXComputeIMTFromPerTexelSignal、D3DXComputeIMTFromSignal 和 D3DXComputeIMTFromTexture 圖形），直接指定 IMT 的或根據輸入信號來計算 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f2869-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="f2869-160">如果您想要控制如何配置個別三角形的材質空間，請直接指定 IMT 資料。</span><span class="sxs-lookup"><span data-stu-id="f2869-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="f2869-161">如此一來，就能將塔中的更多區域配置至網格 (的重要區域，例如字元的臉部或胸標誌，或接近播放程式流覽路徑的場景區域) 。</span><span class="sxs-lookup"><span data-stu-id="f2869-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="f2869-162">藉由指定 IMT 做為識別矩陣的倍數，產生的三角形將會在材質空間中以一致的方式調整。</span><span class="sxs-lookup"><span data-stu-id="f2869-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="f2869-163">例如，假設有一個高解析度的一般地圖，您可以計算 IMT，以提供更多材質空間給標準地圖中較高頻率的範圍。</span><span class="sxs-lookup"><span data-stu-id="f2869-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="f2869-164">對應至原始一般地圖之固定區域的「一般」 (三角形) 將會收到較少的材質空間。</span><span class="sxs-lookup"><span data-stu-id="f2869-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="f2869-165">包含大量標準地圖詳細資料的三角形，在最終結果中會收到更多材質區域。</span><span class="sxs-lookup"><span data-stu-id="f2869-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="f2869-166">然後，您可以將一般地圖重新取樣為較小的材質，但維持詳細資料，或者您可以使用更理想的 UV 對應來重新計算一般地圖。</span><span class="sxs-lookup"><span data-stu-id="f2869-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="f2869-167">針對使用者指定的 Creases 使用相鄰資料</span><span class="sxs-lookup"><span data-stu-id="f2869-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="f2869-168">您可以將使用者定義的相鄰資訊提供給資料分割函數，以描述網格中預先定義的 creases，從而定義相鄰臉部之間的圖表界限。</span><span class="sxs-lookup"><span data-stu-id="f2869-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="f2869-169">這是一個簡單的方法，可讓呼叫者將自己的圖表分割指定為演算法的輸入，這會進一步修改圖表，以在允許的最大值下顯示延展。</span><span class="sxs-lookup"><span data-stu-id="f2869-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="f2869-170">範例</span><span class="sxs-lookup"><span data-stu-id="f2869-170">Example</span></span>

<span data-ttu-id="f2869-171">此範例說明如何使用 UVAtlas Api 和 DirectX 檢視器 (Dxviewer.exe) 在您的模型中尋找並修正可能會大幅影響材質塔大小的不連續。</span><span class="sxs-lookup"><span data-stu-id="f2869-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="f2869-172">您可以從 DirectX SDK 取得 Dxviewer.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2869-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="f2869-173">在2009年8月之後，Dxviewer.exe 已從 DirectX SDK 移除，因此若要取得此版本，您至少需要2009年8月的 DirectX SDK。</span><span class="sxs-lookup"><span data-stu-id="f2869-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="f2869-174">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="f2869-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="f2869-175">假設您在您最愛的內容產生軟體中開始使用一些模型 (此範例會使用 Maya) 中所建立的阻礙 head 模型。</span><span class="sxs-lookup"><span data-stu-id="f2869-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="f2869-176">將紋理模型匯出為. x 檔案，並使用 D3DXUVAtlasCreate 建立材質塔。</span><span class="sxs-lookup"><span data-stu-id="f2869-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="f2869-177">產生的材質塔看起來會像下圖。</span><span class="sxs-lookup"><span data-stu-id="f2869-177">The resulting texture atlas would look something like the following illustration.</span></span>

![阻礙模型的塔圖](images/uvatlas5.jpg)

<span data-ttu-id="f2869-179">塔有22個圖表和最大延展值0.994。</span><span class="sxs-lookup"><span data-stu-id="f2869-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="f2869-180">現在，請查看多紋理的模型，以查看材質塔與幾何的對應程度。</span><span class="sxs-lookup"><span data-stu-id="f2869-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="f2869-181">若要這樣做，請將模型載入檢視器工具中：</span><span class="sxs-lookup"><span data-stu-id="f2869-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="f2869-182">從 DirectX 公用程式開啟檢視器工具。</span><span class="sxs-lookup"><span data-stu-id="f2869-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="f2869-183">按一下 [開啟] 按鈕，載入. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="f2869-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="f2869-184">按一下 [流覽] 按鈕，然後從快顯視窗中選取 [Creases]，以啟用 [折痕] 觀看選項。</span><span class="sxs-lookup"><span data-stu-id="f2869-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="f2869-185">下圖顯示您應該會在檢視器工具中看到的內容。</span><span class="sxs-lookup"><span data-stu-id="f2869-185">The following illustration shows what you should see in the viewer tool.</span></span>

![檢視器工具中的紋理網格圖](images/uvatlas6c.jpg)

<span data-ttu-id="f2869-187">每一行都是一個折痕，也就是紋理塔中兩個圖表之間的相鄰邊緣。</span><span class="sxs-lookup"><span data-stu-id="f2869-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="f2869-188">演算法所產生的圖表數目是因為法線中的不連續所造成的微小差異。</span><span class="sxs-lookup"><span data-stu-id="f2869-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="f2869-189">這些小差異可透過焊接資料來減少，也就是強制幾乎等於相等的資料。</span><span class="sxs-lookup"><span data-stu-id="f2869-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="f2869-190">若要焊接法線和 skinweights：</span><span class="sxs-lookup"><span data-stu-id="f2869-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="f2869-191">在網格上使用下列命令列來執行 DirectX Ops (dxops.exe) 工具 (以您的模型名稱取代 ' modelName. x ') ：</span><span class="sxs-lookup"><span data-stu-id="f2869-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="f2869-192">這會比較法線和 skinweights，而在值之間的差異小於2.01，則會將資料設為相等。</span><span class="sxs-lookup"><span data-stu-id="f2869-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="f2869-193">下圖顯示在) 左焊接 (之前的 creases，以及在右) 上焊接 (之後的 creases：</span><span class="sxs-lookup"><span data-stu-id="f2869-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![焊接之前的 creases 圖例](images/uvatlas6a.jpg)![焊接之後的 creases 圖例](images/uvatlas6b.jpg)

<span data-ttu-id="f2869-196">圖7：使用焊接移除 creases</span><span class="sxs-lookup"><span data-stu-id="f2869-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="f2869-197">在此範例中，已從輸入網格移除86頂點。</span><span class="sxs-lookup"><span data-stu-id="f2869-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="f2869-198">在網格中使用較少的 creases 時，您可以重新產生塔，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f2869-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![已移除 creases 的新的塔圖](images/uvatlas8.jpg)

<span data-ttu-id="f2869-200">塔僅有7個圖表和大約0.0776 的最大延展。</span><span class="sxs-lookup"><span data-stu-id="f2869-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="f2869-201">新的塔現在適用于較小的材質 (此範例) 的大小大約為30%。</span><span class="sxs-lookup"><span data-stu-id="f2869-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="f2869-202">將圖表封裝到塔</span><span class="sxs-lookup"><span data-stu-id="f2869-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="f2869-203">一旦將網格分割成個別的參數化圖表，圖表就必須有效率地封裝成單一材質地圖。</span><span class="sxs-lookup"><span data-stu-id="f2869-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="f2869-204">這會以 D3DXUVAtlasCreate 的第二個步驟來執行，或可透過呼叫 D3DXUVAtlasPack 明確地叫用。</span><span class="sxs-lookup"><span data-stu-id="f2869-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="f2869-205">封裝的圖表會以使用者指定的裝訂邊寬度隔開。</span><span class="sxs-lookup"><span data-stu-id="f2869-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="f2869-206">裝訂邊寬度是圖表之間的區隔量，並允許雙線性插補和 mip 對應，以避免在圖表界限上呈現成品。</span><span class="sxs-lookup"><span data-stu-id="f2869-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="f2869-207">D3DX 會提供自動填入這些裝訂邊的介面，如需詳細資訊，請參閱 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2869-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="f2869-208">將 UVAtlas 整合到您的管線</span><span class="sxs-lookup"><span data-stu-id="f2869-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="f2869-209">除了在紋理繪製之前被叫用的演出者之外，這些函式也可以整合到自動化的美工圖案中。</span><span class="sxs-lookup"><span data-stu-id="f2869-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="f2869-210">例如，在執行 PRT 模擬或正常對應傳遞之前，您可以在資產更新後自動發出 UVAtlas 呼叫。</span><span class="sxs-lookup"><span data-stu-id="f2869-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="f2869-211">如果已修改網狀拓朴，這可避免需要手動手動修復物件的 UV 對應。</span><span class="sxs-lookup"><span data-stu-id="f2869-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="f2869-212">如需 UVAtlas 函式的使用方式，請參閱 [ (uvatlas.exe) 的 UV Command-Line 工具 ](https://github.com/Microsoft/UVAtlas) 。</span><span class="sxs-lookup"><span data-stu-id="f2869-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2869-213">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2869-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2869-214">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="f2869-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 

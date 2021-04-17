---
description: 深度緩衝區 (通常稱為 z 緩衝區或 w 緩衝區)，是裝置屬性，用來儲存深度資訊供 Direct3D 使用。
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: " (Direct3D 9) 的深度緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467649"
---
# <a name="depth-buffers-direct3d-9"></a><span data-ttu-id="1e938-103"> (Direct3D 9) 的深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="1e938-103">Depth Buffers (Direct3D 9)</span></span>

<span data-ttu-id="1e938-104">深度緩衝區 (通常稱為 z 緩衝區或 w 緩衝區)，是裝置屬性，用來儲存深度資訊供 Direct3D 使用。</span><span class="sxs-lookup"><span data-stu-id="1e938-104">A depth buffer, often called a z-buffer or a w-buffer, is a property of the device that stores depth information to be used by Direct3D.</span></span> <span data-ttu-id="1e938-105">當 Direct3D 將場景轉譯至目標表面時，它可以使用相關深度緩衝區表面中的記憶體做為工作區，來決定點陣化多邊形的像素如何彼此遮蓋。</span><span class="sxs-lookup"><span data-stu-id="1e938-105">When Direct3D renders a scene to a target surface, it can use the memory in an associated depth-buffer surface as a workspace to determine how the pixels of rasterized polygons occlude one another.</span></span> <span data-ttu-id="1e938-106">Direct3D 使用螢幕外的 Direct3D 表面做為目標，將最終色彩值寫入其中。</span><span class="sxs-lookup"><span data-stu-id="1e938-106">Direct3D uses an off-screen Direct3D surface as the target to which final color values are written.</span></span> <span data-ttu-id="1e938-107">與轉譯目標表面相關的深度緩衝區表面用來儲存深度資訊，告知 Direct3D 每一個可見像素在場景中的深度。</span><span class="sxs-lookup"><span data-stu-id="1e938-107">The depth-buffer surface that is associated with the render-target surface is used to store depth information that tells Direct3D how deep each visible pixel is in the scene.</span></span>

<span data-ttu-id="1e938-108">當場景點陣化並啟用深度緩衝處理時，轉譯表面上的每一個點都會經過測試。</span><span class="sxs-lookup"><span data-stu-id="1e938-108">When a scene is rasterized with depth buffering enabled, each point on the rendering surface is tested.</span></span> <span data-ttu-id="1e938-109">深度緩衝區中的值可以是點的 z 座標，或其同質 w 座標，來自投射空間中點的 (x,y,z,w) 位置。</span><span class="sxs-lookup"><span data-stu-id="1e938-109">The values in the depth buffer can be a point's z-coordinate or its homogeneous w-coordinate - from the point's (x,y,z,w) location in projection space.</span></span> <span data-ttu-id="1e938-110">使用 z 值的深度緩衝區通常稱為 z 緩衝區，使用 w 值的則稱為 w 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1e938-110">A depth buffer that uses z values is often called a z-buffer, and one that uses w values is called a w-buffer.</span></span> <span data-ttu-id="1e938-111">每一種深度緩衝區都有優點和缺點，將於稍後討論。</span><span class="sxs-lookup"><span data-stu-id="1e938-111">Each type of depth buffer has advantages and disadvantages, which are discussed later.</span></span>

<span data-ttu-id="1e938-112">在測試一開始，深度緩衝區中的深度值會設為場景的可能最大值。</span><span class="sxs-lookup"><span data-stu-id="1e938-112">At the beginning of the test, the depth value in the depth buffer is set to the largest possible value for the scene.</span></span> <span data-ttu-id="1e938-113">轉譯表面上的色彩值會設為該點的背景色彩值或背景紋理的色彩值。</span><span class="sxs-lookup"><span data-stu-id="1e938-113">The color value on the rendering surface is set to either the background color value or the color value of the background texture at that point.</span></span> <span data-ttu-id="1e938-114">場景中的每個多邊形都會經過測試，查看是否與轉譯表面上目前的座標 (x,y) 交集。</span><span class="sxs-lookup"><span data-stu-id="1e938-114">Each polygon in the scene is tested to see if it intersects with the current coordinate (x,y) on the rendering surface.</span></span> <span data-ttu-id="1e938-115">如果有，則會測試深度值（在 z 緩衝區中為 z 座標），並測試目前點的 w 座標（在目前點上為 w 座標），以查看它是否小於深度緩衝區中儲存的深度值。</span><span class="sxs-lookup"><span data-stu-id="1e938-115">If it does, the depth value - which will be the z coordinate in a z-buffer, and the w coordinate in a w-buffer - at the current point is tested to see if it is smaller than the depth value stored in the depth buffer.</span></span> <span data-ttu-id="1e938-116">如果多邊形值的深度較小，它會儲存在深度緩衝區中，來自多邊形的色彩值會寫入轉譯表面上目前的點。</span><span class="sxs-lookup"><span data-stu-id="1e938-116">If the depth of the polygon value is smaller, it is stored in the depth buffer and the color value from the polygon is written to the current point on the rendering surface.</span></span> <span data-ttu-id="1e938-117">如果該點上多邊形的深度值較大，則會測試清單中下一個多邊形。</span><span class="sxs-lookup"><span data-stu-id="1e938-117">If the depth value of the polygon at that point is larger, the next polygon in the list is tested.</span></span> <span data-ttu-id="1e938-118">此程序顯示在下圖。</span><span class="sxs-lookup"><span data-stu-id="1e938-118">This process is shown in the following diagram.</span></span>

![測試深度值的圖](images/zbuffer.png)

> [!Note]  
> <span data-ttu-id="1e938-120">雖然大部分應用程式不會使用此功能，但是您可以變更 Direct3D 用來判斷哪些值位於深度緩衝區中的比較，以及後續的轉譯目標表面。</span><span class="sxs-lookup"><span data-stu-id="1e938-120">Although most applications don't use this feature, you can change the comparison that Direct3D uses to determine which values are placed in the depth buffer and subsequently the render-target surface.</span></span> <span data-ttu-id="1e938-121">若要這樣做，請變更 D3DRS ZFUNC 轉譯 \_ 狀態的值。</span><span class="sxs-lookup"><span data-stu-id="1e938-121">To do so, change the value for the D3DRS\_ZFUNC render state.</span></span> <span data-ttu-id="1e938-122">在某些硬體上，變更比較功能可能會停用階層 z 測試。</span><span class="sxs-lookup"><span data-stu-id="1e938-122">On some hardware, changing the compare function may disable hierarchical z testing.</span></span>

 

<span data-ttu-id="1e938-123">市面上幾乎所有加速器都支援 z 緩衝，因此 z 緩衝區是目前最常見的深度緩衝區類型。</span><span class="sxs-lookup"><span data-stu-id="1e938-123">Nearly all accelerators on the market support z-buffering, making z-buffers the most common type of depth buffer today.</span></span> <span data-ttu-id="1e938-124">無論有多普遍，z 緩衝區仍有缺點。</span><span class="sxs-lookup"><span data-stu-id="1e938-124">However ubiquitous, z-buffers have their drawbacks.</span></span> <span data-ttu-id="1e938-125">由於涉及的數學計算，z 緩衝區中產生的 z 值較不平均分散在 z 緩衝區範圍中 (通常是 0.0 到 1.0 (含))。</span><span class="sxs-lookup"><span data-stu-id="1e938-125">Due to the mathematics involved, the generated z values in a z-buffer tend not to be distributed evenly across the z-buffer range (typically 0.0 to 1.0, inclusive).</span></span> <span data-ttu-id="1e938-126">具體而言，遠近裁剪平面之間的比例對 z 值分佈不平均影響很大。</span><span class="sxs-lookup"><span data-stu-id="1e938-126">Specifically, the ratio between the far and near clipping planes strongly affects how unevenly z values are distributed.</span></span> <span data-ttu-id="1e938-127">使用遠平面距離到近平面距離比例為 100、深度緩衝區範圍的 90% 會用在場景深度範圍的前 10%。</span><span class="sxs-lookup"><span data-stu-id="1e938-127">Using a far-plane distance to near-plane distance ratio of 100, 90 percent of the depth buffer range is spent on the first 10 percent of the scene depth range.</span></span> <span data-ttu-id="1e938-128">一般用於娛樂或視覺化模擬的應用程式含有外部場景，經常需要遠平面/近平面比例介於 1,000 到 10,000 之間。</span><span class="sxs-lookup"><span data-stu-id="1e938-128">Typical applications for entertainment or visual simulations with exterior scenes often require far-plane/near-plane ratios of anywhere between 1,000 to 10,000.</span></span> <span data-ttu-id="1e938-129">比例為 1,000 時，98% 的範圍會用在深度範圍的前 2%，分佈情形會比採用高比例時更糟。</span><span class="sxs-lookup"><span data-stu-id="1e938-129">At a ratio of 1,000, 98 percent of the range is spent on the first 2 percent of the depth range, and the distribution becomes worse with higher ratios.</span></span> <span data-ttu-id="1e938-130">這可能造成隱藏的表面成品在遠方物件中，尤其是使用 16 位元深度緩衝區時，這是最常見的支援位元深度。</span><span class="sxs-lookup"><span data-stu-id="1e938-130">This can cause hidden surface artifacts in distant objects, especially when using 16-bit depth buffers, the most commonly supported bit-depth.</span></span>

<span data-ttu-id="1e938-131">另一方面來說，w 型深度緩衝區通常比 z 緩衝區分佈較平均，在遠近裁剪平面之間。</span><span class="sxs-lookup"><span data-stu-id="1e938-131">A w-based depth buffer, on the other hand, is often more evenly distributed between the near and far clip planes than a z-buffer.</span></span> <span data-ttu-id="1e938-132">主要優點在於，遠近裁剪平面的距離比例不再是問題。</span><span class="sxs-lookup"><span data-stu-id="1e938-132">The key benefit is that the ratio of distances for the far and near clipping planes is no longer an issue.</span></span> <span data-ttu-id="1e938-133">這可讓應用程式支援大型最大範圍，同時仍讓相對精確的深度緩衝靠近眼睛視覺點。</span><span class="sxs-lookup"><span data-stu-id="1e938-133">This allows applications to support large maximum ranges, while still getting relatively accurate depth buffering close to the eye point.</span></span> <span data-ttu-id="1e938-134">w 型深度緩衝區並不完美，有時可能會呈現近的物件的隱藏表面成品。</span><span class="sxs-lookup"><span data-stu-id="1e938-134">A w-based depth buffer isn't perfect, and can sometimes exhibit hidden surface artifacts for near objects.</span></span> <span data-ttu-id="1e938-135">w 緩衝方法的另一個缺點與硬體支援相關：w 緩衝不如 z 緩衝一般在硬體之間廣受支援。</span><span class="sxs-lookup"><span data-stu-id="1e938-135">Another drawback to the w-buffered approach is related to hardware support: w-buffering isn't supported as widely in hardware as z-buffering.</span></span>

<span data-ttu-id="1e938-136">使用 z 緩衝區在轉譯時需要額外負荷。</span><span class="sxs-lookup"><span data-stu-id="1e938-136">Using a z-buffer requires overhead during rendering.</span></span> <span data-ttu-id="1e938-137">各種不同的技術都可用來最佳化使用 z 緩衝區時的轉譯。</span><span class="sxs-lookup"><span data-stu-id="1e938-137">Various techniques can be used to optimize rendering when using z-buffers.</span></span> <span data-ttu-id="1e938-138">如需詳細資訊，請參閱 [Z 緩衝區效能](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="1e938-138">For details, see [Z-Buffer Performance](performance-optimizations.md).</span></span>

> [!Note]  
> <span data-ttu-id="1e938-139">實際的深度值解譯為轉譯器特定。</span><span class="sxs-lookup"><span data-stu-id="1e938-139">The actual interpretation of a depth value is specific to the renderer.</span></span>

 

<span data-ttu-id="1e938-140">本節提供有關使用隱藏行和隱藏介面移除的深度緩衝區的資訊。</span><span class="sxs-lookup"><span data-stu-id="1e938-140">This section presents information about using depth buffers for hidden line and hidden surface removal.</span></span>

-   [<span data-ttu-id="1e938-141">查詢 (Direct3D 9) 的深度緩衝區支援 </span><span class="sxs-lookup"><span data-stu-id="1e938-141">Querying for Depth Buffer Support (Direct3D 9)</span></span>](querying-for-depth-buffer-support.md)
-   [<span data-ttu-id="1e938-142"> (Direct3D 9) 建立深度緩衝區 </span><span class="sxs-lookup"><span data-stu-id="1e938-142">Creating a Depth Buffer (Direct3D 9)</span></span>](creating-a-depth-buffer.md)
-   [<span data-ttu-id="1e938-143"> (Direct3D 9) 啟用深度緩衝 </span><span class="sxs-lookup"><span data-stu-id="1e938-143">Enabling Depth Buffering (Direct3D 9)</span></span>](enabling-depth-buffering.md)
-   [<span data-ttu-id="1e938-144">抓取 (Direct3D 9) 的深度緩衝區 </span><span class="sxs-lookup"><span data-stu-id="1e938-144">Retrieving a Depth Buffer (Direct3D 9)</span></span>](retrieving-a-depth-buffer.md)
-   [<span data-ttu-id="1e938-145"> (Direct3D 9) 清除深度緩衝區 </span><span class="sxs-lookup"><span data-stu-id="1e938-145">Clearing Depth Buffers (Direct3D 9)</span></span>](clearing-depth-buffers.md)
-   [<span data-ttu-id="1e938-146">變更深度緩衝區寫入存取 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1e938-146">Changing Depth Buffer Write Access (Direct3D 9)</span></span>](changing-depth-buffer-write-access.md)
-   [<span data-ttu-id="1e938-147">變更深度緩衝區比較函式 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1e938-147">Changing Depth Buffer Comparison Functions (Direct3D 9)</span></span>](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a><span data-ttu-id="1e938-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e938-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e938-149">Direct3D 轉譯</span><span class="sxs-lookup"><span data-stu-id="1e938-149">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 




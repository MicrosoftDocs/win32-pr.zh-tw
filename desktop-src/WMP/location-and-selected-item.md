---
title: 位置和選取的專案
description: 位置和選取的專案
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player 線上商店、位置
- 線上商店、位置
- 輸入1個線上商店、位置
- Windows Media Player 線上商店、程式庫位置
- 線上商店、程式庫位置
- 輸入1個線上商店、程式庫位置
- Windows Media Player 線上商店，選取的專案
- 線上商店、選取的專案
- 輸入1個線上商店、選取的專案
- Windows Media Player 程式庫，位置
- Windows Media Player 程式庫，選取的專案
- 程式庫，位置
- 程式庫，選取的專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183418"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="0a06a-116">位置和選取的專案</span><span class="sxs-lookup"><span data-stu-id="0a06a-116">Location and Selected Item</span></span>

<span data-ttu-id="0a06a-117">Windows Media Player 使用下列五個專案來描述其目前線上商店內容的觀點：</span><span class="sxs-lookup"><span data-stu-id="0a06a-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="0a06a-118">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="0a06a-118">task</span></span>
-   <span data-ttu-id="0a06a-119">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-119">library location type</span></span>
-   <span data-ttu-id="0a06a-120">程式庫位置識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-120">library location ID</span></span>
-   <span data-ttu-id="0a06a-121">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-121">selected item type</span></span>
-   <span data-ttu-id="0a06a-122">選取的專案識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-122">selected item ID</span></span>

<span data-ttu-id="0a06a-123">一般來說，您可以將 Windows Media Player 中的 view 視為專案的容器。</span><span class="sxs-lookup"><span data-stu-id="0a06a-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="0a06a-124">容器具有類型，而專案具有類型。</span><span class="sxs-lookup"><span data-stu-id="0a06a-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="0a06a-125">容器中的所有專案都有相同的類型。</span><span class="sxs-lookup"><span data-stu-id="0a06a-125">All the items in a container have the same type.</span></span> <span data-ttu-id="0a06a-126">位置類型和專案類型都是由連結 [庫位置常數](library-location-constants.md)指定。</span><span class="sxs-lookup"><span data-stu-id="0a06a-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="0a06a-127">例如，如果目前的視圖顯示個別的專輯，則程式庫位置類型為 CPAlbumID，而且因為專輯包含曲目，所以選取的專案類型為 CPTrackID。</span><span class="sxs-lookup"><span data-stu-id="0a06a-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="0a06a-128">下表顯示數個容器的位置和專案類型。</span><span class="sxs-lookup"><span data-stu-id="0a06a-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="0a06a-129">容器的描述</span><span class="sxs-lookup"><span data-stu-id="0a06a-129">Description of container</span></span>                              | <span data-ttu-id="0a06a-130">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-130">Library location type</span></span> | <span data-ttu-id="0a06a-131">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="0a06a-132">作為追蹤容器的專輯</span><span class="sxs-lookup"><span data-stu-id="0a06a-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="0a06a-133">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0a06a-133">CPAlbumID</span></span>             | <span data-ttu-id="0a06a-134">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="0a06a-134">CPTrackID</span></span>          |
| <span data-ttu-id="0a06a-135">作為追蹤容器的清單</span><span class="sxs-lookup"><span data-stu-id="0a06a-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="0a06a-136">CPListID</span><span class="sxs-lookup"><span data-stu-id="0a06a-136">CPListID</span></span>              | <span data-ttu-id="0a06a-137">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="0a06a-137">CPTrackID</span></span>          |
| <span data-ttu-id="0a06a-138">是專輯容器的清單</span><span class="sxs-lookup"><span data-stu-id="0a06a-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="0a06a-139">CPListID</span><span class="sxs-lookup"><span data-stu-id="0a06a-139">CPListID</span></span>              | <span data-ttu-id="0a06a-140">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0a06a-140">CPAlbumID</span></span>          |
| <span data-ttu-id="0a06a-141">作為清單容器的電臺電臺</span><span class="sxs-lookup"><span data-stu-id="0a06a-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="0a06a-142">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="0a06a-142">CPRadioID</span></span>             | <span data-ttu-id="0a06a-143">CPListID</span><span class="sxs-lookup"><span data-stu-id="0a06a-143">CPListID</span></span>           |
| <span data-ttu-id="0a06a-144">所有專輯的集合，也就是專輯的容器</span><span class="sxs-lookup"><span data-stu-id="0a06a-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="0a06a-145">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="0a06a-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="0a06a-146">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0a06a-146">CPAlbumID</span></span>          |
| <span data-ttu-id="0a06a-147">所有內容的集合，也就是內容的容器</span><span class="sxs-lookup"><span data-stu-id="0a06a-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="0a06a-148">AllCPGenreIDs</span><span class="sxs-lookup"><span data-stu-id="0a06a-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="0a06a-149">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="0a06a-149">CPGenreID</span></span>          |



 

<span data-ttu-id="0a06a-150">Windows Media Player 中的索引標籤代表不同的工作。</span><span class="sxs-lookup"><span data-stu-id="0a06a-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="0a06a-151">Player 會在三個不同的工作窗格中顯示線上商店內容： **媒體** 櫃、 **燒錄** 和 **同步**。[程式庫] 工作窗格也稱為 [ **流覽** 工作窗格]。</span><span class="sxs-lookup"><span data-stu-id="0a06a-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="0a06a-152">有時，工作窗格稱為 *功能*，因此您可能會在此檔中看到 [ *燒錄功能* 與 *同步* 處理] 等詞彙。</span><span class="sxs-lookup"><span data-stu-id="0a06a-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="0a06a-153">下列範例顯示 Windows Media Player 如何使用五項資訊， (工作、程式庫位置類型、程式庫位置識別碼、選取的專案類型、選取的專案識別碼) 來描述不同的視圖。</span><span class="sxs-lookup"><span data-stu-id="0a06a-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="0a06a-154">在 [ **燒錄** 工作] 窗格中，播放程式會將專輯顯示為曲目的容器。</span><span class="sxs-lookup"><span data-stu-id="0a06a-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="0a06a-155">專輯的識別碼為250。</span><span class="sxs-lookup"><span data-stu-id="0a06a-155">The album has an ID of 250.</span></span> <span data-ttu-id="0a06a-156">在此視圖中，選取的專案是識別碼為800的軌跡。</span><span class="sxs-lookup"><span data-stu-id="0a06a-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="0a06a-157">請注意，800是線上商店目錄中的曲目識別碼，不是專輯的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="0a06a-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="0a06a-158">Item</span><span class="sxs-lookup"><span data-stu-id="0a06a-158">Item</span></span>                  | <span data-ttu-id="0a06a-159">值</span><span class="sxs-lookup"><span data-stu-id="0a06a-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="0a06a-160">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="0a06a-160">task</span></span>                  | <span data-ttu-id="0a06a-161">燒錄</span><span class="sxs-lookup"><span data-stu-id="0a06a-161">Burn</span></span>      |
| <span data-ttu-id="0a06a-162">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-162">library location type</span></span> | <span data-ttu-id="0a06a-163">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0a06a-163">CPAlbumID</span></span> |
| <span data-ttu-id="0a06a-164">程式庫位置識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-164">library location ID</span></span>   | <span data-ttu-id="0a06a-165">250</span><span class="sxs-lookup"><span data-stu-id="0a06a-165">250</span></span>       |
| <span data-ttu-id="0a06a-166">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-166">selected item type</span></span>    | <span data-ttu-id="0a06a-167">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="0a06a-167">CPTrackID</span></span> |
| <span data-ttu-id="0a06a-168">選取的專案識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-168">selected item ID</span></span>      | <span data-ttu-id="0a06a-169">800</span><span class="sxs-lookup"><span data-stu-id="0a06a-169">800</span></span>       |



 

<span data-ttu-id="0a06a-170">在 [ **同步** 處理工作] 窗格中，播放程式會顯示所有專輯的集合，也就是專輯的容器。</span><span class="sxs-lookup"><span data-stu-id="0a06a-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="0a06a-171">在此視圖中，選取的專案是識別碼為300的專輯。</span><span class="sxs-lookup"><span data-stu-id="0a06a-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="0a06a-172">請注意，程式庫位置識別碼不適用於此視圖。</span><span class="sxs-lookup"><span data-stu-id="0a06a-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="0a06a-173">Item</span><span class="sxs-lookup"><span data-stu-id="0a06a-173">Item</span></span>                  | <span data-ttu-id="0a06a-174">值</span><span class="sxs-lookup"><span data-stu-id="0a06a-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="0a06a-175">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="0a06a-175">task</span></span>                  | <span data-ttu-id="0a06a-176">同步</span><span class="sxs-lookup"><span data-stu-id="0a06a-176">Sync</span></span>          |
| <span data-ttu-id="0a06a-177">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-177">library location type</span></span> | <span data-ttu-id="0a06a-178">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="0a06a-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="0a06a-179">程式庫位置識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-179">library location ID</span></span>   | <span data-ttu-id="0a06a-180">N/A</span><span class="sxs-lookup"><span data-stu-id="0a06a-180">N/A</span></span>           |
| <span data-ttu-id="0a06a-181">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-181">selected item type</span></span>    | <span data-ttu-id="0a06a-182">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0a06a-182">CPAlbumID</span></span>     |
| <span data-ttu-id="0a06a-183">選取的專案識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-183">selected item ID</span></span>      | <span data-ttu-id="0a06a-184">300</span><span class="sxs-lookup"><span data-stu-id="0a06a-184">300</span></span>           |



 

<span data-ttu-id="0a06a-185">在樹狀檢視控制項中，會選取線上商店的根節點。</span><span class="sxs-lookup"><span data-stu-id="0a06a-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="0a06a-186">在此情況下，沒有任何容器，因此沒有任何專案。</span><span class="sxs-lookup"><span data-stu-id="0a06a-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="0a06a-187">整個 [ **媒體** 櫃] 工作窗格都會顯示 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="0a06a-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="0a06a-188">Item</span><span class="sxs-lookup"><span data-stu-id="0a06a-188">Item</span></span>                  | <span data-ttu-id="0a06a-189">值</span><span class="sxs-lookup"><span data-stu-id="0a06a-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="0a06a-190">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="0a06a-190">task</span></span>                  | <span data-ttu-id="0a06a-191">瀏覽</span><span class="sxs-lookup"><span data-stu-id="0a06a-191">Browse</span></span>          |
| <span data-ttu-id="0a06a-192">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-192">library location type</span></span> | <span data-ttu-id="0a06a-193">RootLocation</span><span class="sxs-lookup"><span data-stu-id="0a06a-193">RootLocation</span></span>    |
| <span data-ttu-id="0a06a-194">程式庫位置識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-194">library location ID</span></span>   | <span data-ttu-id="0a06a-195">N/A</span><span class="sxs-lookup"><span data-stu-id="0a06a-195">N/A</span></span>             |
| <span data-ttu-id="0a06a-196">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-196">selected item type</span></span>    | <span data-ttu-id="0a06a-197">Unknownlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="0a06a-197">UnknownLocation</span></span> |
| <span data-ttu-id="0a06a-198">選取的專案識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-198">selected item ID</span></span>      | <span data-ttu-id="0a06a-199">N/A</span><span class="sxs-lookup"><span data-stu-id="0a06a-199">N/A</span></span>             |



 

<span data-ttu-id="0a06a-200">在 [ **同步** 處理工作] 窗格中，播放程式會將2002年份顯示為追蹤的容器。</span><span class="sxs-lookup"><span data-stu-id="0a06a-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="0a06a-201">在此視圖中，選取的專案是識別碼為450的軌跡。</span><span class="sxs-lookup"><span data-stu-id="0a06a-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="0a06a-202">Item</span><span class="sxs-lookup"><span data-stu-id="0a06a-202">Item</span></span>                  | <span data-ttu-id="0a06a-203">值</span><span class="sxs-lookup"><span data-stu-id="0a06a-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="0a06a-204">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="0a06a-204">task</span></span>                  | <span data-ttu-id="0a06a-205">同步</span><span class="sxs-lookup"><span data-stu-id="0a06a-205">Sync</span></span>            |
| <span data-ttu-id="0a06a-206">程式庫位置類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-206">library location type</span></span> | <span data-ttu-id="0a06a-207">ReleaseDateYear</span><span class="sxs-lookup"><span data-stu-id="0a06a-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="0a06a-208">程式庫位置識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-208">library location ID</span></span>   | <span data-ttu-id="0a06a-209">2002</span><span class="sxs-lookup"><span data-stu-id="0a06a-209">2002</span></span>            |
| <span data-ttu-id="0a06a-210">選取的專案類型</span><span class="sxs-lookup"><span data-stu-id="0a06a-210">selected item type</span></span>    | <span data-ttu-id="0a06a-211">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="0a06a-211">CPTrackID</span></span>       |
| <span data-ttu-id="0a06a-212">選取的專案識別碼</span><span class="sxs-lookup"><span data-stu-id="0a06a-212">selected item ID</span></span>      | <span data-ttu-id="0a06a-213">450</span><span class="sxs-lookup"><span data-stu-id="0a06a-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="0a06a-214">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a06a-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a06a-215">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="0a06a-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0a06a-216">**探索頁面**</span><span class="sxs-lookup"><span data-stu-id="0a06a-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 





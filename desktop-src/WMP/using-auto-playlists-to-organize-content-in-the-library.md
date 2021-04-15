---
title: 使用自動播放清單來組織文件庫中的內容
description: 使用自動播放清單來組織文件庫中的內容
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player 線上商店、自動播放清單
- 線上商店、自動播放清單
- 輸入1個線上商店、自動播放清單
- 輸入2個線上商店、自動播放清單
- Windows Media Player 線上商店、組織文件庫內容
- 線上商店、組織文件庫內容
- 輸入1個線上商店、組織文件庫內容
- 輸入2個線上商店、組織文件庫內容
- Windows Media Player 線上商店、文件庫內容組織
- 線上商店、文件庫內容組織
- 輸入1個線上商店、文件庫內容組織
- 輸入2個線上商店、文件庫內容組織
- 程式庫，組織內容
- 組織文件庫內容
- 自動播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507300"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="a4841-118">使用自動播放清單來組織文件庫中的內容</span><span class="sxs-lookup"><span data-stu-id="a4841-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="a4841-119">您可以使用自動播放清單來組織您所提供的 premium 內容。</span><span class="sxs-lookup"><span data-stu-id="a4841-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="a4841-120">例如，您可以使用 Windows Media Player 建立自動播放清單，其中只包含您所提供的內容，且使用者至少有四顆星的評等。</span><span class="sxs-lookup"><span data-stu-id="a4841-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="a4841-121">然後，您可以在 Windows Media Player 中將自動播放清單新增至媒體櫃，使其顯示在 [內容散發者] 節點下的 [已購買的音樂] 節點中。</span><span class="sxs-lookup"><span data-stu-id="a4841-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="a4841-122">若要這樣做，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a4841-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="a4841-123">建立自動播放清單。</span><span class="sxs-lookup"><span data-stu-id="a4841-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="a4841-124">使用 Windows 檔案總管，流覽至自動播放清單並取出 .wpl 檔案。</span><span class="sxs-lookup"><span data-stu-id="a4841-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="a4841-125">使用 Windows Media Player 物件模型，將自動播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="a4841-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="a4841-126">將播放清單的 **WM/ContentDistributor** 屬性設定為內容轉銷商金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="a4841-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="a4841-127">將播放清單的 [ **>synconly** ] 屬性設定為 [true]。</span><span class="sxs-lookup"><span data-stu-id="a4841-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="a4841-128">下列 JScript 範例程式碼顯示的函式會將名為「我的最愛點擊次數」的自動播放清單新增至程式庫中的 Proseware 節點：</span><span class="sxs-lookup"><span data-stu-id="a4841-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="a4841-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4841-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4841-130">關於程式庫整合</span><span class="sxs-lookup"><span data-stu-id="a4841-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="a4841-131">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="a4841-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a4841-132">**MediaCollection 新增**</span><span class="sxs-lookup"><span data-stu-id="a4841-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="a4841-133">**播放清單。 setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a4841-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a4841-134">**靜態和自動播放清單**</span><span class="sxs-lookup"><span data-stu-id="a4841-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="a4841-135">**>synconly 屬性**</span><span class="sxs-lookup"><span data-stu-id="a4841-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="a4841-136">**WM/ContentDistributor 屬性**</span><span class="sxs-lookup"><span data-stu-id="a4841-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="a4841-137">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="a4841-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 





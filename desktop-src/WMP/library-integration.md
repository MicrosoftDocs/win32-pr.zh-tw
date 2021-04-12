---
title: 程式庫整合
description: 程式庫整合
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player 線上商店、程式庫整合
- 線上商店，程式庫整合
- 輸入1個線上商店，程式庫整合
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 輸入1個線上商店、工作窗格
- Windows Media Player，工作窗格
- Windows Media Player 程式庫，整合
- 程式庫，整合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374483"
---
# <a name="library-integration"></a><span data-ttu-id="a3f7f-112">程式庫整合</span><span class="sxs-lookup"><span data-stu-id="a3f7f-112">Library Integration</span></span>

<span data-ttu-id="a3f7f-113">Windows Media Player 的使用者介面會組織成功能區，稱為工作 *窗格*，可封裝程式的各種高階功能。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-113">The Windows Media Player user interface is organized into feature areas, called *task panes*, which encapsulate the various high-level features of the program.</span></span> <span data-ttu-id="a3f7f-114">其中包括連結 **庫**、 **同步** 處理和 **燒錄** 工作窗格 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-114">These include the **Library**, **Sync**, and **Burn** task panes (among others).</span></span> <span data-ttu-id="a3f7f-115">[連結 **庫** ] 工作窗格可讓使用者使用程式庫;[ **同步** 工作] 窗格可讓使用者將數位媒體檔案同步到可攜式裝置;[ **燒錄** 工作] 窗格可讓使用者將數位媒體檔案燒錄到 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-115">The **Library** task pane enables users to work with the library; the **Sync** task pane enables users to synchronize digital media files to a portable device; and the **Burn** task pane enables users to burn digital media files to a CD or DVD.</span></span>

> [!Note]  
> <span data-ttu-id="a3f7f-116">[連結 **庫** ] 工作窗格有時稱為 [ **流覽** 工作窗格]。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-116">The **Library** task pane is sometimes called the **Browse** task pane.</span></span>

 

<span data-ttu-id="a3f7f-117">這些工作窗格中的每一個都有一些與程式庫的整合層級。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-117">Each of these task panes has some level of integration with the library.</span></span> <span data-ttu-id="a3f7f-118">例如，如果使用者想要將音樂燒錄至 CD，讓使用者藉由流覽程式庫並直接將媒體專案拖放至清單中，選擇要燒錄的音樂是合理的。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-118">For example, if the user wants to burn music to a CD, it makes sense to let the user choose the music to burn by browsing the library and simply dragging and dropping media items into a list.</span></span> <span data-ttu-id="a3f7f-119">這表示使用者可以在連結 **庫**、 **同步** 處理和 **燒錄** 工作窗格時，查看並使用已完全整合至程式庫的線上商店目錄。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-119">This means that users can view and use an online store catalog that is fully integrated into the library when working in the **Library**, **Sync**, and **Burn** task panes.</span></span> <span data-ttu-id="a3f7f-120">[WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype)列舉包含的值代表這三個工作窗格，因此可以透過程式設計方式加以識別。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-120">The [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) enumeration contains values that represent these three task panes so they can be identified programmatically.</span></span>

<span data-ttu-id="a3f7f-121">這三個工作窗格中的每一個都分成三個主要部分。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-121">Each of these three task panes is organized into three major parts.</span></span> <span data-ttu-id="a3f7f-122">第一個部分是程式庫樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-122">The first part is the library tree-view control.</span></span> <span data-ttu-id="a3f7f-123">此控制項可讓使用者以階層方式顯示 Windows Media Player 程式庫，包括依歌曲、演出者、專輯等分類功能。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-123">This control provides the user with a hierarchical view of the Windows Media Player library, including categorization features by song, artist, album, and so forth.</span></span> <span data-ttu-id="a3f7f-124">第二個工作窗格部分是 [詳細資料] 窗格。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-124">The second task pane part is the details pane.</span></span> <span data-ttu-id="a3f7f-125">這個窗格會根據 [程式庫] 樹狀檢視中目前選取的類別，提供詳細的資訊組織。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-125">This pane provides detailed information organized according to the category currently selected in the library tree-view control.</span></span> <span data-ttu-id="a3f7f-126">例如，如果使用者已按一下樹狀檢視中的 [ **歌曲** ]，[詳細資料] 窗格會顯示目前在文件庫中的歌曲標題，以及其他資訊，例如 [長度] 和 [專輯標題]。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-126">For example, if the user has clicked **Songs** in the tree view, the details pane will show the song titles currently in the library, along with other information such as length and album title.</span></span> <span data-ttu-id="a3f7f-127">第三個部分是 [清單] 窗格或 [ *購物籃*]。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-127">The third part is the list pane, or *basket*.</span></span> <span data-ttu-id="a3f7f-128">使用者可以將媒體專案拖放到購物籃上，以建立清單，例如播放清單、同步清單和燒錄清單。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-128">Users can drag and drop media items onto the basket to build lists, such as playlists, sync lists, and burn lists.</span></span>

<span data-ttu-id="a3f7f-129">當線上商店目錄與程式庫整合時，線上商店會顯示為 [程式庫] 樹狀檢視控制項中的最上層類別或 *節點*。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-129">When an online store catalog is integrated with the library, the online store appears as a top-level category, or *node*, in the library tree-view control.</span></span> <span data-ttu-id="a3f7f-130"> (一次只能有一位使用者看到一個線上商店目錄。 ) 當使用者按一下節點來選擇觀看線上商店目錄時，[詳細資料] 窗格會顯示線上商店目錄中音樂的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-130">(Only one online store catalog is visible to the user at a time.) When a user chooses to view the online store catalog by clicking the node, the details pane shows information about the music in the online store catalog.</span></span> <span data-ttu-id="a3f7f-131">這包括使用者已購買或出租的音樂，以及使用者尚未取得的音樂。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-131">This includes music the user has purchased or rented, and also music the user has not yet acquired.</span></span>

<span data-ttu-id="a3f7f-132">最上層的線上商店節點有一組由 Windows Media Player 提供的子節點。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-132">The top-level online store node has a set of child nodes provided by Windows Media Player.</span></span> <span data-ttu-id="a3f7f-133">例如，最上層的線上商店節點有收音機、演出者和專輯子節點，還有其他節點。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-133">For example, the top-level online store node has Radio, Artist, and Album child nodes, among others.</span></span> <span data-ttu-id="a3f7f-134">最上層的線上商店節點最多可以有8個線上商店提供的自訂子節點。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-134">The top-level online store node can also have up to eight custom child nodes provided by the online store.</span></span> <span data-ttu-id="a3f7f-135">Windows Media Player 會針對清單識別碼在0到7範圍內的任何清單建立自訂的子節點。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-135">Windows Media Player creates a custom child node for any list that has a list identifier in the range 0 through 7.</span></span> <span data-ttu-id="a3f7f-136">線上商店會在 [list.csv](list-csv.md) 檔案中指定屬於存放區類別目錄的清單識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-136">The online store specifies the identifier of a list in the [list.csv](list-csv.md) file that is part of the store's catalog.</span></span>

<span data-ttu-id="a3f7f-137">Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，並在 *bstrInfoName* 參數中傳遞 CPListIDIcon，以抓取每個線上商店的自訂樹狀節點的圖示。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-137">Windows Media Player retrieves an icon for each of the online store's custom tree nodes by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing CPListIDIcon in the *bstrInfoName* parameter.</span></span>

<span data-ttu-id="a3f7f-138">當使用者流覽目錄時，Windows Media Player 會呼叫 **IWMPContentPartner：： GetItemInfo** ，以從內容合作夥伴外掛程式取得使用者所選取之音樂專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-138">As the user navigates through the catalog, Windows Media Player makes calls to **IWMPContentPartner::GetItemInfo** to retrieve metadata from the content partner plug-in about the music items the user selects.</span></span> <span data-ttu-id="a3f7f-139">此中繼資料會提供資訊給播放程式，讓播放程式可以顯示類別目錄專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-139">This metadata provides information to the Player so that the Player can display details about the catalog items.</span></span> <span data-ttu-id="a3f7f-140">例如，如果使用者選取專輯，Windows Media Player 會抓取專輯封面 URL，讓使用者可以看到專輯封面。</span><span class="sxs-lookup"><span data-stu-id="a3f7f-140">For example, if the user selects an album, Windows Media Player retrieves the album art URL so that the user can see the album cover art.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3f7f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3f7f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f7f-142">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="a3f7f-142">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 





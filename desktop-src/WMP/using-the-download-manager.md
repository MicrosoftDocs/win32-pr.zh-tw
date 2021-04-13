---
title: 使用下載管理員
description: 使用下載管理員
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372641"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="9e413-109">使用下載管理員</span><span class="sxs-lookup"><span data-stu-id="9e413-109">Using the Download Manager</span></span>

<span data-ttu-id="9e413-110">Windows Media Player SDK 包含範例網頁，示範如何使用下載管理員將檔下載至使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="9e413-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="9e413-111">您可以在安裝 SDK 的名稱為網頁的資料夾中找到範例。</span><span class="sxs-lookup"><span data-stu-id="9e413-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="9e413-112">檔案的名稱是範例 .asp。</span><span class="sxs-lookup"><span data-stu-id="9e413-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="9e413-113">此範例提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="9e413-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="9e413-114">建立 **DownloadManager** 物件。</span><span class="sxs-lookup"><span data-stu-id="9e413-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="9e413-115">建立 **DownloadCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="9e413-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="9e413-116">當使用者按一下 [ **下載**] 時，就會開始下載五個檔案。</span><span class="sxs-lookup"><span data-stu-id="9e413-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="9e413-117">範例中提供預設檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="9e413-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="9e413-118">您應該以您自己的伺服器上的檔案位置取代這些預設路徑。</span><span class="sxs-lookup"><span data-stu-id="9e413-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="9e413-119">您可以藉由變更指派給名為 g sFiles 之全域陣列的值來變更路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9e413-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="9e413-120">顯示使用者選取時的下載狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9e413-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="9e413-121">提供用來暫停、繼續、取消和移除下載專案的控制項。</span><span class="sxs-lookup"><span data-stu-id="9e413-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="9e413-122">使用 cookie 維護會話之間的下載集合相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9e413-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="9e413-123">這點很重要，因為使用者可以隨時關閉播放程式。</span><span class="sxs-lookup"><span data-stu-id="9e413-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="9e413-124">此外，如果使用者在播放玩家切換工作窗格，線上商店會話就會結束。</span><span class="sxs-lookup"><span data-stu-id="9e413-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="9e413-125">預設會使用即時下載。</span><span class="sxs-lookup"><span data-stu-id="9e413-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="9e413-126">您可以變更名為 g sDLType 的變數值，將行為變更為背景下載 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9e413-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="9e413-127">背景下載可用於 Microsoft Windows XP 作業系統。</span><span class="sxs-lookup"><span data-stu-id="9e413-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="9e413-128">將背景色彩與播放機色彩同步處理。</span><span class="sxs-lookup"><span data-stu-id="9e413-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="9e413-129">您可以使用這項功能，在使用者選擇變更播放程式的色彩時，讓您的線上商店變更外觀。</span><span class="sxs-lookup"><span data-stu-id="9e413-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="9e413-130">下列各節提供詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="9e413-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="9e413-131">初始化頁面</span><span class="sxs-lookup"><span data-stu-id="9e413-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="9e413-132">開始下載</span><span class="sxs-lookup"><span data-stu-id="9e413-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="9e413-133">正在抓取狀態資訊</span><span class="sxs-lookup"><span data-stu-id="9e413-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="9e413-134">維護會話資訊</span><span class="sxs-lookup"><span data-stu-id="9e413-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="9e413-135">頁面的調試</span><span class="sxs-lookup"><span data-stu-id="9e413-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="9e413-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e413-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e413-137">**Type 2 線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="9e413-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 





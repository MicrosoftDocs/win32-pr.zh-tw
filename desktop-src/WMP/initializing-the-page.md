---
title: 初始化頁面
description: 初始化頁面
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，初始化頁面
- 線上商店，初始化頁面
- 輸入2個線上商店，初始化頁面
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 初始化頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183807"
---
# <a name="initializing-the-page"></a><span data-ttu-id="7fba3-113">初始化頁面</span><span class="sxs-lookup"><span data-stu-id="7fba3-113">Initializing the Page</span></span>

<span data-ttu-id="7fba3-114">當網頁載入時， **Init** 函式就會執行。</span><span class="sxs-lookup"><span data-stu-id="7fba3-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="7fba3-115">此程式碼會先抓取之前會話中儲存的任何資料。</span><span class="sxs-lookup"><span data-stu-id="7fba3-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="7fba3-116">如需詳細資訊，請參閱 [維護會話資訊](maintaining-session-information.md)。</span><span class="sxs-lookup"><span data-stu-id="7fba3-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="7fba3-117">然後，它會建立 **DownloadManager** 物件，並將它儲存在名為 g oManager 的全域變數中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fba3-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="7fba3-118">接著，函式會將 **OnColorChange** 事件連接到名為 **OnAppColor** 的函式，然後直接呼叫函式以初始化背景色彩。</span><span class="sxs-lookup"><span data-stu-id="7fba3-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="7fba3-119">請參閱 [符合 Windows Media Player 色彩](matching-the-windows-media-player-colors.md)。</span><span class="sxs-lookup"><span data-stu-id="7fba3-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="7fba3-120">最後，函式會以一秒的間隔啟動計時器，並初始化顯示暫止下載集合和下載專案的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="7fba3-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="7fba3-121">這點很重要，因為最後一次關閉線上商店時，可能已經有會話正在進行中，而且這項資訊必須再次顯示。</span><span class="sxs-lookup"><span data-stu-id="7fba3-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fba3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fba3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fba3-123">**使用下載管理員**</span><span class="sxs-lookup"><span data-stu-id="7fba3-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 





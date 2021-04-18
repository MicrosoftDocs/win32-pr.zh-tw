---
title: 第2型線上商店的購買整合
description: 第2型線上商店的購買整合
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player 線上商店、購買整合
- 線上商店、購買整合
- 類型2線上商店，購買整合
- Windows Media Player 線上商店，整合購買專案
- 線上商店，整合購買
- 輸入2個線上商店，整合購買
- Windows Media Player，購買整合
- Windows Media Player，整合購買
- 購買整合
- 整合購買
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964980"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="e287e-113">第2型線上商店的購買整合</span><span class="sxs-lookup"><span data-stu-id="e287e-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="e287e-114">當 Windows Media Player 播放數位媒體內容或使用者選擇 [ **尋找專輯資訊**] 時，播放程式會提供一個連結，讓使用者在有可用的連結時，購買內容所源自的 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="e287e-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="e287e-115">當使用者按一下連結時，會在目前的音樂商店上 Windows Media Player 10 或更新的呼叫，以處理購買要求。</span><span class="sxs-lookup"><span data-stu-id="e287e-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="e287e-116">發生這種情況時，播放程式會流覽至第一個服務工作窗格 (Windows Media Player 10) 或 Windows Media Player 11) 中的 [線上商店] 索引標籤 (，並顯示 ServiceInfo 檔之 **BuyCD** 元素的 **MediaPlayerURL** 屬性所指定的網頁。</span><span class="sxs-lookup"><span data-stu-id="e287e-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="e287e-117"> (**MediaCenterURL** 和 **BrowserURL** 屬性會以類似的方式使用，以處理來自 Windows xp Media Center EDITION 2004 和 windows xp Service Pack 2) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e287e-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="e287e-118">Windows Media Player 會將查詢字串附加至 URL，以提供有關使用者選擇要購買之內容的線上商店資訊。</span><span class="sxs-lookup"><span data-stu-id="e287e-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="e287e-119">查詢字串包含 **標題**、 **專輯** 和 **演出者** 等屬性，可供線上商店用來判斷要銷售的正確專輯。</span><span class="sxs-lookup"><span data-stu-id="e287e-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="e287e-120">**BuyCD** 元素的參考檔會提供查詢字串屬性及其描述的完整清單。</span><span class="sxs-lookup"><span data-stu-id="e287e-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="e287e-121">BuyCD 頁面的指導方針</span><span class="sxs-lookup"><span data-stu-id="e287e-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="e287e-122">建立 BuyCD 網頁時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="e287e-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="e287e-123">頁面必須清楚地識別提供資訊的線上商店。</span><span class="sxs-lookup"><span data-stu-id="e287e-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="e287e-124">例如，您可以藉由醒目顯示您的標誌來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="e287e-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="e287e-125">此頁面必須包含您公司隱私權聲明的連結。</span><span class="sxs-lookup"><span data-stu-id="e287e-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="e287e-126">最好提供初始購買資訊，而不需要使用者安裝程式或登入您的線上商店。</span><span class="sxs-lookup"><span data-stu-id="e287e-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e287e-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e287e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e287e-128">**關於 Type 2 線上商店**</span><span class="sxs-lookup"><span data-stu-id="e287e-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e287e-129">**BuyCD 元素**</span><span class="sxs-lookup"><span data-stu-id="e287e-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 





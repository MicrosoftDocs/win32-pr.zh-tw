---
title: 整合資訊中心視圖功能
description: 整合資訊中心視圖功能
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player 線上商店，整合資訊中心視圖
- 線上商店，整合資訊中心視圖
- 輸入1個線上商店，整合資訊中心視圖
- 輸入2個線上商店，整合資訊中心視圖
- Windows Media Player 線上商店，資訊中心視圖
- 線上商店，資訊中心視圖
- 輸入1個線上商店，資訊中心視圖
- 類型2線上商店，資訊中心視圖
- 整合資訊中心視圖
- 資訊中心視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965395"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="39054-113">整合資訊中心視圖功能</span><span class="sxs-lookup"><span data-stu-id="39054-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="39054-114">Windows Media Player 可讓使用者開啟和關閉資訊中心視圖功能。</span><span class="sxs-lookup"><span data-stu-id="39054-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="39054-115">資訊中心視圖是使用者預期尋找有關特定數位媒體內容之豐富、延伸資訊的功能。</span><span class="sxs-lookup"><span data-stu-id="39054-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="39054-116">當使用者選擇開啟資訊中心視圖時，Windows Media Player 在目前的音樂商店上進行呼叫，以顯示 ServiceInfo 檔的 **資訊中心** 元素的 **URL** 屬性所指定的資訊中心視圖網頁。</span><span class="sxs-lookup"><span data-stu-id="39054-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="39054-117">若要取得目前播放中數位媒體內容的相關資訊，您必須在網頁中內嵌 Windows Media Player 控制項的實例，並使用 Player 物件模型。</span><span class="sxs-lookup"><span data-stu-id="39054-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="39054-118">例如，若要取出標題，您可以使用下列 JScript 程式碼：</span><span class="sxs-lookup"><span data-stu-id="39054-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="39054-119">資訊中心視圖的指導方針</span><span class="sxs-lookup"><span data-stu-id="39054-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="39054-120">建立 **資訊中心視圖** 網頁時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="39054-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="39054-121">頁面必須清楚地識別提供資訊的線上商店。</span><span class="sxs-lookup"><span data-stu-id="39054-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="39054-122">例如，您可以藉由醒目顯示您的標誌來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="39054-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="39054-123">此頁面必須包含您公司隱私權聲明的連結。</span><span class="sxs-lookup"><span data-stu-id="39054-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="39054-124">請盡可能避免在資訊中心視圖功能內進行頁面導覽。</span><span class="sxs-lookup"><span data-stu-id="39054-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="39054-125">您應該流覽至您的線上商店以尋找大部分的活動。</span><span class="sxs-lookup"><span data-stu-id="39054-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="39054-126">最好提供寶貴的資訊，而不需要使用者安裝程式或登入您的線上商店。</span><span class="sxs-lookup"><span data-stu-id="39054-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39054-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="39054-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39054-128">**NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="39054-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="39054-129">**資訊中心元素**</span><span class="sxs-lookup"><span data-stu-id="39054-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="39054-130">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="39054-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="39054-131">**在 Web 網頁中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="39054-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





---
title: 專輯資訊整合
description: 專輯資訊整合
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player 線上商店，專輯資訊整合
- 線上商店，專輯資訊整合
- 類型2線上商店，專輯資訊整合
- Windows Media Player 線上商店，整合專輯資訊
- 線上商店，整合專輯資訊
- 輸入2個線上商店，整合專輯資訊
- Windows Media Player，整合專輯資訊
- Windows Media Player，專輯資訊整合
- 專輯資訊整合
- 整合專輯資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021367"
---
# <a name="album-info-integration"></a><span data-ttu-id="b9169-113">專輯資訊整合</span><span class="sxs-lookup"><span data-stu-id="b9169-113">Album Info Integration</span></span>

<span data-ttu-id="b9169-114">Windows Media Player 可讓使用者透過按一下按鈕（例如 **詳細資訊**），來要求數位媒體內容所產生的 CD 或 DVD 相關的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b9169-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="b9169-115">當使用者按一下按鈕時，Windows Media Player 10 或更新版本會在目前的音樂商店上進行呼叫，以顯示專輯詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b9169-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="b9169-116">當發生這種情況時，播放程式會開啟 [專輯資訊] 窗格，並顯示 ServiceInfo 檔中 **AlbumInfo** 元素的 [ **URL** ] 屬性所指定的網頁。</span><span class="sxs-lookup"><span data-stu-id="b9169-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="b9169-117">Windows Media Player 會將查詢字串附加至 URL，以提供有關使用者所要求內容的線上商店資訊。</span><span class="sxs-lookup"><span data-stu-id="b9169-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="b9169-118">查詢字串包含 **標題**、 **專輯** 和 **演出者** 等屬性，可供線上商店用來決定要顯示的正確專輯。</span><span class="sxs-lookup"><span data-stu-id="b9169-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="b9169-119">**AlbumInfo** 元素的參考檔會提供查詢字串屬性及其描述的完整清單。</span><span class="sxs-lookup"><span data-stu-id="b9169-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="b9169-120">專輯資訊的指導方針</span><span class="sxs-lookup"><span data-stu-id="b9169-120">Guidelines for Album Info</span></span>

<span data-ttu-id="b9169-121">建立您的專輯資訊網頁時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="b9169-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="b9169-122">頁面必須清楚地識別提供資訊的線上商店。</span><span class="sxs-lookup"><span data-stu-id="b9169-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="b9169-123">例如，您可以藉由醒目顯示您的標誌來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="b9169-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="b9169-124">此頁面必須包含您公司隱私權聲明的連結。</span><span class="sxs-lookup"><span data-stu-id="b9169-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="b9169-125">請盡可能避免在專輯資訊功能中進行頁面導覽。</span><span class="sxs-lookup"><span data-stu-id="b9169-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="b9169-126">您應該流覽至您的線上商店以尋找大部分的活動。</span><span class="sxs-lookup"><span data-stu-id="b9169-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="b9169-127">建議您提供寶貴的資訊，而不需要使用者安裝程式或登入您的線上商店。</span><span class="sxs-lookup"><span data-stu-id="b9169-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9169-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9169-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9169-129">**關於 Type 2 線上商店**</span><span class="sxs-lookup"><span data-stu-id="b9169-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b9169-130">**AlbumInfo 元素**</span><span class="sxs-lookup"><span data-stu-id="b9169-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 





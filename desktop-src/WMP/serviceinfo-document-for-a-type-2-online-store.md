---
title: 適用于 Type 2 線上商店的 ServiceInfo 檔
description: 適用于 Type 2 線上商店的 ServiceInfo 檔
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021593"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="6371c-107">適用于 Type 2 線上商店的 ServiceInfo 檔</span><span class="sxs-lookup"><span data-stu-id="6371c-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="6371c-108">Type 2 線上商店提供者必須為 Microsoft 提供描述線上商店之 XML 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="6371c-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="6371c-109">Windows Media Player 10 和 Windows Media Player 11 使用這份檔來決定如何設定使用者介面來裝載線上商店。</span><span class="sxs-lookup"><span data-stu-id="6371c-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="6371c-110">在 Windows Media Player 10 中，ServiceInfo 檔提供下列各項：</span><span class="sxs-lookup"><span data-stu-id="6371c-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="6371c-111">有關如何設定當線上商店處於作用中時，Windows Media Player 顯示的工作窗格的資訊。</span><span class="sxs-lookup"><span data-stu-id="6371c-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="6371c-112">線上商店可以有一個、兩個或三個工作窗格。</span><span class="sxs-lookup"><span data-stu-id="6371c-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="6371c-113">用來設定工作窗格按鈕的資訊，例如按鈕文字、按鈕色彩，以及按鈕的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6371c-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="6371c-114">Windows Media Player 顯示以識別線上商店的影像 Url。</span><span class="sxs-lookup"><span data-stu-id="6371c-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="6371c-115">線上商店提供的網頁 Url，Windows Media Player 裝載于其使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="6371c-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="6371c-116">Windows Media Player 安裝程式應該如何設定使用者看到的第一個線上商店的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6371c-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="6371c-117">在 Windows Media Player 11 中，ServiceInfo 檔提供下列各項：</span><span class="sxs-lookup"><span data-stu-id="6371c-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="6371c-118">用來設定 [線上商店] 索引標籤之按鈕的資訊，例如按鈕文字和按鈕的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6371c-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="6371c-119">Windows Media Player 顯示以識別線上商店的影像 Url。</span><span class="sxs-lookup"><span data-stu-id="6371c-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="6371c-120">線上商店提供的網頁 Url，Windows Media Player 裝載于其使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="6371c-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="6371c-121">當您開始開發線上商店時，必須向 Microsoft 提供 ServiceInfo 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="6371c-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="6371c-122">在開發階段，只有在設定特殊登錄機碼時，您的線上商店才會出現在 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="6371c-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="6371c-123">在您的線上商店發佈之後，ususal 案例是 Windows Media Player 會自動從 Web 抓取您的 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="6371c-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="6371c-124">不過，在某些情況下，Windows Media Player 會從使用者的電腦抓取 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="6371c-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="6371c-125">如需詳細資訊，請參閱 [設定初始線上商店](setting-the-initial-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="6371c-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="6371c-126">當 Windows Media Player 從 Web 抓取 ServiceInfo 檔時，會將查詢字串附加至 URL。</span><span class="sxs-lookup"><span data-stu-id="6371c-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="6371c-127">查詢字串包含的參數可提供使用者地區設定和 Windows Media Player 版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6371c-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="6371c-128">您可以建立靜態或動態 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="6371c-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="6371c-129">靜態 ServiceInfo 檔的副檔名為 .xml。</span><span class="sxs-lookup"><span data-stu-id="6371c-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="6371c-130">動態 ServiceInfo 檔是 ASP 網頁，而且副檔名為 .asp 或 .aspx。</span><span class="sxs-lookup"><span data-stu-id="6371c-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="6371c-131">並非所有可在 ServiceInfo 檔中使用的元素都可供每個線上商店使用，而某些元素對於所有線上商店都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6371c-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="6371c-132">如需您可以建立的線上商店類型，以及每種類型可用功能的相關資訊，請參閱 [Windows Media Player 線上商店](windows-media-player-online-stores.md)。</span><span class="sxs-lookup"><span data-stu-id="6371c-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6371c-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="6371c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6371c-134">**關於 Type 2 線上商店**</span><span class="sxs-lookup"><span data-stu-id="6371c-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6371c-135">**動態建立 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="6371c-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="6371c-136">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="6371c-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="6371c-137">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="6371c-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





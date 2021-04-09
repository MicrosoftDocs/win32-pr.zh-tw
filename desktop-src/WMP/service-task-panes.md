---
title: 服務工作窗格
description: 服務工作窗格
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player 線上商店、服務工作窗格
- 線上商店、服務工作窗格
- 輸入2個線上商店、服務工作窗格
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 類型2線上商店、工作窗格
- Windows Media Player，服務工作窗格
- Windows Media Player，工作窗格
- 服務工作窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021594"
---
# <a name="service-task-panes"></a><span data-ttu-id="e04f8-112">服務工作窗格</span><span class="sxs-lookup"><span data-stu-id="e04f8-112">Service Task Panes</span></span>

<span data-ttu-id="e04f8-113">在 Windows Media Player 10 中，線上商店提供者可以設定 Windows Media Player 顯示多達三個工作窗格，稱為「服務工作窗格」。</span><span class="sxs-lookup"><span data-stu-id="e04f8-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="e04f8-114">每個服務工作窗格會以可自訂的按鈕表示，Windows Media Player 在功能工作列右側顯示。</span><span class="sxs-lookup"><span data-stu-id="e04f8-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="e04f8-115">每個服務工作窗格都會裝載一個網頁，該網頁是特定線上商店功能的使用者介面。服務工作窗格的外觀是由 ServiceInfo XML 檔所定義。</span><span class="sxs-lookup"><span data-stu-id="e04f8-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="e04f8-116">在本檔中，服務工作窗格會以三個元素表示： **ServiceTask1**、 **ServiceTask2** 和 **ServiceTask3**。</span><span class="sxs-lookup"><span data-stu-id="e04f8-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="e04f8-117">這些服務工作窗格旨在提供下列各項：</span><span class="sxs-lookup"><span data-stu-id="e04f8-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="e04f8-118">音樂服務。</span><span class="sxs-lookup"><span data-stu-id="e04f8-118">A music service.</span></span>
-   <span data-ttu-id="e04f8-119">影片服務。</span><span class="sxs-lookup"><span data-stu-id="e04f8-119">A video service.</span></span>
-   <span data-ttu-id="e04f8-120">無線電服務。</span><span class="sxs-lookup"><span data-stu-id="e04f8-120">A radio service.</span></span>

<span data-ttu-id="e04f8-121">您可以依您想要的任何順序將這些功能放在 Windows Media Player 中，但 **ServiceTask1** 必須是參與商務工作的主要工作窗格。</span><span class="sxs-lookup"><span data-stu-id="e04f8-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="e04f8-122">裝載在每個服務工作窗格中的網頁可以存取 **外部** 物件。</span><span class="sxs-lookup"><span data-stu-id="e04f8-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="e04f8-123">這個物件會提供方法、屬性和事件，以提供 Windows Media Player 中網頁的特殊功能。</span><span class="sxs-lookup"><span data-stu-id="e04f8-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="e04f8-124">例如，您可以使用 **外部** 的事件和屬性，讓網頁的外觀符合使用者為 Windows Media Player 選擇的色彩配置。</span><span class="sxs-lookup"><span data-stu-id="e04f8-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="e04f8-125">在 Windows Media Player 11 中，沒有任何服務工作窗格。</span><span class="sxs-lookup"><span data-stu-id="e04f8-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="e04f8-126">相反地，有一個 [ **線上商店** ] 索引標籤，可裝載作用中線上商店的主要網頁。</span><span class="sxs-lookup"><span data-stu-id="e04f8-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="e04f8-127">在 ServiceInfo 檔中，[ **線上商店** ] 索引標籤會以 **ServiceTask1** 元素表示; **ServiceTask2** 和 **ServiceTask3** 元素會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e04f8-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e04f8-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e04f8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e04f8-129">**關於 Type 2 線上商店**</span><span class="sxs-lookup"><span data-stu-id="e04f8-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e04f8-130">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="e04f8-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e04f8-131">**適用于 Type 2 線上商店的 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="e04f8-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 





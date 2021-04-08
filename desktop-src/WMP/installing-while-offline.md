---
title: 離線時安裝
description: 離線時安裝
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player 線上商店，離線安裝
- 線上商店，離線安裝
- 輸入1個線上商店，離線安裝
- 輸入2個線上商店，離線安裝
- Windows Media Player 線上商店、離線安裝
- 線上商店、離線安裝
- 輸入1個線上商店、離線安裝
- 輸入2個線上商店、離線安裝
- 離線時安裝線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840248"
---
# <a name="installing-while-offline"></a><span data-ttu-id="b30a3-112">離線時安裝</span><span class="sxs-lookup"><span data-stu-id="b30a3-112">Installing While Offline</span></span>

<span data-ttu-id="b30a3-113">使用者可以在未連線到網際網路的情況下安裝 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="b30a3-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="b30a3-114">發生這種情況時，Windows Media Player 安裝程式會尋找 *ServiceInfo* 命令列參數所指定的 ServiceInfo.xml 檔。</span><span class="sxs-lookup"><span data-stu-id="b30a3-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="b30a3-115">如果索引 **鍵** 屬性符合 *DefaultService* 命令列參數，安裝程式會將下列元素的資訊套用至 Windows Media Player：</span><span class="sxs-lookup"><span data-stu-id="b30a3-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="b30a3-116">友好.</span><span class="sxs-lookup"><span data-stu-id="b30a3-116">FriendlyName.</span></span> <span data-ttu-id="b30a3-117">線上商店的易記名稱會顯示在 Windows Media Player 的使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="b30a3-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="b30a3-118">色彩。</span><span class="sxs-lookup"><span data-stu-id="b30a3-118">Color.</span></span> <span data-ttu-id="b30a3-119">指定的色彩會套用至工作列和按鈕。</span><span class="sxs-lookup"><span data-stu-id="b30a3-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="b30a3-120">ServiceTask1、ServiceTask2 和 ServiceTask3。</span><span class="sxs-lookup"><span data-stu-id="b30a3-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="b30a3-121">已設定 ButtonText 和 ButtonTip 子項目。</span><span class="sxs-lookup"><span data-stu-id="b30a3-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="b30a3-122">未設定 URL 屬性。</span><span class="sxs-lookup"><span data-stu-id="b30a3-122">The URL attribute is not set.</span></span> <span data-ttu-id="b30a3-123">當使用者連線到網際網路，且 Windows Media Player 以正常方式抓取其線上商店清單時，就會設定 URL。</span><span class="sxs-lookup"><span data-stu-id="b30a3-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="b30a3-124">影像。</span><span class="sxs-lookup"><span data-stu-id="b30a3-124">Image.</span></span> <span data-ttu-id="b30a3-125">MenuURL 和 ServiceLargeURL 屬性已設定。</span><span class="sxs-lookup"><span data-stu-id="b30a3-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="b30a3-126">這些 Url 必須指向您使用 file://通訊協定安裝在使用者硬碟上的映射。</span><span class="sxs-lookup"><span data-stu-id="b30a3-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="b30a3-127">當使用者嘗試觀看線上商店時，Windows Media Player 會顯示一則訊息，告知使用者需要網際網路連線。</span><span class="sxs-lookup"><span data-stu-id="b30a3-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b30a3-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b30a3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b30a3-129">**Color 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-130">**FriendlyName 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-131">**Image 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-132">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="b30a3-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b30a3-133">**ServiceInfo 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-134">**ServiceTask1 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-135">**ServiceTask2 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-136">**ServiceTask3 元素**</span><span class="sxs-lookup"><span data-stu-id="b30a3-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="b30a3-137">**設定初始線上商店**</span><span class="sxs-lookup"><span data-stu-id="b30a3-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="b30a3-138">**安裝線上商店的命令列參數**</span><span class="sxs-lookup"><span data-stu-id="b30a3-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 





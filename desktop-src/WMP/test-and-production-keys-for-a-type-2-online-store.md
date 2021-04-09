---
title: Type 2 線上商店的測試和生產金鑰
description: Type 2 線上商店的測試和生產金鑰
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player 線上商店，測試金鑰
- 線上商店、測試金鑰
- 輸入2個線上商店、測試金鑰
- Windows Media Player 線上商店、生產金鑰
- 線上商店、生產金鑰
- 類型2個線上商店、生產金鑰
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- 測試金鑰
- 生產金鑰
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932487"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a><span data-ttu-id="c060a-115">Type 2 線上商店的測試和生產金鑰</span><span class="sxs-lookup"><span data-stu-id="c060a-115">Test and Production Keys for a Type 2 Online Store</span></span>

<span data-ttu-id="c060a-116">當您開始開發線上商店時，Microsoft 會為您提供兩個數值金鑰：測試金鑰和生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="c060a-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="c060a-117">同時，您必須為 Microsoft 提供兩個 Url：一個指向您的測試 ServiceInfo 檔，另一個指向您的生產 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="c060a-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="c060a-118">在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，才會在 Windows Media Player 中看到您的線上商店。</span><span class="sxs-lookup"><span data-stu-id="c060a-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="c060a-119">如果您的測試機碼位於登錄中，Windows Media Player 會抓取您的測試 ServiceInfo 檔，指向您的測試存放區的外掛程式、網頁和影像。</span><span class="sxs-lookup"><span data-stu-id="c060a-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="c060a-120">如果您的生產金鑰位於登錄中，Windows Media Player 會抓取您的生產 ServiceInfo 檔，其指向外掛程式、網頁和屬於您生產環境存放區的映射。</span><span class="sxs-lookup"><span data-stu-id="c060a-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="c060a-121">您可以使用您認為有用的任何方式來使用您的測試和生產存放區。</span><span class="sxs-lookup"><span data-stu-id="c060a-121">You can use your test and production stores in any way you find useful.</span></span> <span data-ttu-id="c060a-122">但一般而言，差別如下：</span><span class="sxs-lookup"><span data-stu-id="c060a-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="c060a-123">您的測試存放區是您對外掛程式、網頁、影像和服務的其他元件進行每日變更的位置。</span><span class="sxs-lookup"><span data-stu-id="c060a-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="c060a-124">您的生產環境存放區是您保留服務穩定版本的位置，包括您的外掛程式、網頁、影像和其他元件。</span><span class="sxs-lookup"><span data-stu-id="c060a-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="c060a-125">在 Windows Media Player 中發佈您的線上商店之前，Microsoft 必須驗證您的服務是否正確執行。</span><span class="sxs-lookup"><span data-stu-id="c060a-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="c060a-126">在驗證階段，Microsoft 會使用您的生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="c060a-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="c060a-127">Microsoft 不會在驗證階段使用您的測試金鑰。</span><span class="sxs-lookup"><span data-stu-id="c060a-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="c060a-128">當您的生產線上商店成功完成驗證程式時，Microsoft 會發佈您的存放區，這表示您的生產環境存放區會在所有使用者的 Windows Media Player 中顯示，而不只是在登錄中有您實際執行金鑰的使用者。</span><span class="sxs-lookup"><span data-stu-id="c060a-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="c060a-129">發佈存放區之後，就不再需要測試和生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="c060a-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="c060a-130">使用者可能會猜測線上商店的測試或生產金鑰，並在開發期間查看您的商店。</span><span class="sxs-lookup"><span data-stu-id="c060a-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="c060a-131">在公開發行之前，您應該特別小心公開您想要保留秘密的功能。</span><span class="sxs-lookup"><span data-stu-id="c060a-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="c060a-132">如需有關如何將生產和測試金鑰放在使用者登錄中的詳細資訊，請參閱 [類型2線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-2-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="c060a-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c060a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="c060a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c060a-134">**關於 Type 2 線上商店**</span><span class="sxs-lookup"><span data-stu-id="c060a-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c060a-135">**類型2線上商店範例**</span><span class="sxs-lookup"><span data-stu-id="c060a-135">**Type 2 Online Store Samples**</span></span>](type-2-online-store-samples.md)
</dt> </dl>

 

 





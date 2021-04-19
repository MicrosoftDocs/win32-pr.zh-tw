---
title: 國際市場的考慮
description: 國際市場的考慮
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player 線上商店，國際市場
- 線上商店，國際市場
- 輸入1個線上商店，國際市場
- 輸入2個線上商店，國際市場
- 國際市場
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965380"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="8ff3d-113">國際市場的考慮</span><span class="sxs-lookup"><span data-stu-id="8ff3d-113">Considerations for International Markets</span></span>

<span data-ttu-id="8ff3d-114">如果您的公司建立多個市場的線上商店，您必須為每個市場提供 Microsoft ServiceInfo 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="8ff3d-115">您可以透過下列兩種方式之一來執行：</span><span class="sxs-lookup"><span data-stu-id="8ff3d-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="8ff3d-116">為每個市場建立個別的 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="8ff3d-117">在此情況下，您會為 Microsoft 提供指向每個市場中每個線上商店之個別 ServiceInfo 檔的 Url。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="8ff3d-118">為所有市場建立單一 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="8ff3d-119">當您這樣做時，您會為每個市場提供相同的 URL 給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="8ff3d-120">以 ASP 頁面的形式建立的 ServiceInfo 檔，可以根據查詢字串參數動態偵測使用者的位置。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="8ff3d-121">Windows Media Player 會將查詢字串附加至 ServiceInfo URL 要求，以提供使用者地區設定和位置設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="8ff3d-122">如果您的線上商店使用這項資訊來決定要顯示的內容，您應該以動態方式將這些值附加至 ServiceInfo 檔中的您自己的 Url。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="8ff3d-123">這是確保您的網頁 Url 一律會包含您預期之參數的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="8ff3d-124">一旦決定使用者的位置和語言喜好設定之後，您可能會想要在未來的會話中保存此資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="8ff3d-125">您可以使用您通常會在網頁中使用的任何技術，例如 cookie，或使用您的 COM 物件來執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="8ff3d-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ff3d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ff3d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ff3d-127">**動態建立 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="8ff3d-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="8ff3d-128">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="8ff3d-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8ff3d-129">**ServiceInfo 元素**</span><span class="sxs-lookup"><span data-stu-id="8ff3d-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 





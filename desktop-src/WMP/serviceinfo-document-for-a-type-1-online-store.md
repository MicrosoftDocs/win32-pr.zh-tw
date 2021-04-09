---
title: 類型1線上商店的 ServiceInfo 檔
description: 類型1線上商店的 ServiceInfo 檔
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021595"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="98a1c-107">類型1線上商店的 ServiceInfo 檔</span><span class="sxs-lookup"><span data-stu-id="98a1c-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="98a1c-108">輸入1線上商店必須為 Microsoft 提供描述線上商店之 XML 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="98a1c-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="98a1c-109">Windows Media Player 11 使用這份檔來決定如何設定使用者介面來裝載線上商店。</span><span class="sxs-lookup"><span data-stu-id="98a1c-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="98a1c-110">類型1存放區的 ServiceInfo 檔提供下列資訊給 Windows Media Player：</span><span class="sxs-lookup"><span data-stu-id="98a1c-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="98a1c-111">用來設定 [ **線上商店** ] 按鈕的資訊 (也稱為索引標籤) ，例如按鈕文字、按鈕色彩，以及按鈕的工具提示。</span><span class="sxs-lookup"><span data-stu-id="98a1c-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="98a1c-112">Windows Media Player 顯示以識別線上商店的影像 Url。</span><span class="sxs-lookup"><span data-stu-id="98a1c-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="98a1c-113">線上商店提供的網頁 Url，Windows Media Player 裝載于其使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="98a1c-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="98a1c-114">URL，其中 Windows Media Player 可以取得線上商店的外掛程式，以便將外掛程式安裝在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="98a1c-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="98a1c-115">當 Windows Media Player 從 Web 抓取 ServiceInfo 檔時，會將查詢字串附加至 URL。</span><span class="sxs-lookup"><span data-stu-id="98a1c-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="98a1c-116">查詢字串包含的參數可提供使用者地區設定和地理位置以及 Windows Media Player 版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98a1c-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98a1c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="98a1c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a1c-118">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="98a1c-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="98a1c-119">**動態建立 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="98a1c-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="98a1c-120">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="98a1c-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="98a1c-121">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="98a1c-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





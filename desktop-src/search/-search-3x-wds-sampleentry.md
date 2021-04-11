---
description: 本主題說明與 Windows Search 相關的技術。
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: 相關搜尋技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112472"
---
# <a name="related-search-technologies"></a><span data-ttu-id="c8816-103">相關搜尋技術</span><span class="sxs-lookup"><span data-stu-id="c8816-103">Related Search Technologies</span></span>

<span data-ttu-id="c8816-104">本主題說明與 [Windows Search](-search-3x-wds-overview.md)相關的技術。</span><span class="sxs-lookup"><span data-stu-id="c8816-104">This topic describes technologies that are related to [Windows Search](-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="c8816-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="c8816-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c8816-106">企業搜尋</span><span class="sxs-lookup"><span data-stu-id="c8816-106">Enterprise Search</span></span>](#enterprise-search)
    -   [<span data-ttu-id="c8816-107">SharePoint 企業搜尋</span><span class="sxs-lookup"><span data-stu-id="c8816-107">SharePoint Enterprise Search</span></span>](#sharepoint-enterprise-search)
-   [<span data-ttu-id="c8816-108">Windows 桌面搜尋2。x</span><span class="sxs-lookup"><span data-stu-id="c8816-108">Windows Desktop Search 2.x</span></span>](#windows-desktop-search-2x)
-   [<span data-ttu-id="c8816-109">Platform SDK：索引服務</span><span class="sxs-lookup"><span data-stu-id="c8816-109">Platform SDK: Indexing Service</span></span>](#platform-sdk-indexing-service)
-   [<span data-ttu-id="c8816-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8816-110">Related topics</span></span>](#related-topics)

## <a name="enterprise-search"></a><span data-ttu-id="c8816-111">企業搜尋</span><span class="sxs-lookup"><span data-stu-id="c8816-111">Enterprise Search</span></span>

<span data-ttu-id="c8816-112">如需 [Microsoft 企業搜尋](https://www.microsoft.com/enterprisesearch/en/us/default.aspx)的技術資源總覽，請參閱：</span><span class="sxs-lookup"><span data-stu-id="c8816-112">For an overview of technical resources for [Enterprise Search from Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), see:</span></span>

-   [<span data-ttu-id="c8816-113">企業搜尋資源中心</span><span class="sxs-lookup"><span data-stu-id="c8816-113">Enterprise Search Resource Center</span></span>](https://developer.microsoft.com/office/docs)
-   [<span data-ttu-id="c8816-114">Microsoft 企業搜尋的 Blog</span><span class="sxs-lookup"><span data-stu-id="c8816-114">Microsoft Enterprise Search Blog</span></span>](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a><span data-ttu-id="c8816-115">SharePoint 企業搜尋</span><span class="sxs-lookup"><span data-stu-id="c8816-115">SharePoint Enterprise Search</span></span>

<span data-ttu-id="c8816-116">SharePoint Foundation 2010 提供 [從伺服器端程式碼查詢](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) ，以及 [從用戶端程式代碼查詢](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14))的查詢。</span><span class="sxs-lookup"><span data-stu-id="c8816-116">SharePoint Foundation 2010 provides [querying from server-side code](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) and [querying from client-side code](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)).</span></span> <span data-ttu-id="c8816-117">如需有關查詢、搜尋新內容以及改善與 Sharepoint Server 2010 企業搜尋之相關性的詳細資訊，請參閱 [企業搜尋基礎](/previous-versions/office/ee554857(v=office.14))。</span><span class="sxs-lookup"><span data-stu-id="c8816-117">For more information on querying, searching for new content, and improving relevance with Sharepoint Server 2010 Enterprise Search, see [Enterprise Search Fundamentals](/previous-versions/office/ee554857(v=office.14)).</span></span>

<span data-ttu-id="c8816-118">Windows 7 搜尋支援使用 OpenSearch 技術來搜尋遠端資料存放區，讓使用者能夠從 Windows 檔案總管記憶體取遠端資料並與其互動。</span><span class="sxs-lookup"><span data-stu-id="c8816-118">Windows 7 Search supports search federation to remote data stores by using OpenSearch technologies, which enable users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="c8816-119">SharePoint Search Server 2008 和 MOSS 2007 SP2 也支援使用 OpenSearch 進行遠端伺服器的同盟搜尋。</span><span class="sxs-lookup"><span data-stu-id="c8816-119">SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search of remote servers using OpenSearch.</span></span> <span data-ttu-id="c8816-120">如需有關使用 Office SharePoint Server 2007 部署搜尋伺服器2008的詳細資訊，請參閱同盟[搜尋 \[ 搜尋伺服器 2008 \] ](/previous-versions/office/bb931109(v=office.14))。</span><span class="sxs-lookup"><span data-stu-id="c8816-120">For information about Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span> <span data-ttu-id="c8816-121">如需 MOSS 多面向搜尋的資訊，其中搜尋結果是依類別 refinded，請參閱 [Codeplex](https://www.codeplex.com/FacetedSearch)。</span><span class="sxs-lookup"><span data-stu-id="c8816-121">For information on MOSS Faceted Search, in which search results are refinded by category, see [Codeplex](https://www.codeplex.com/FacetedSearch).</span></span>

<span data-ttu-id="c8816-122">Windows Search 通訊協定處理常式會使用與 SharePoint Server 類似的設計規格，而且通常可以交換使用。</span><span class="sxs-lookup"><span data-stu-id="c8816-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="c8816-123">因此，當使用者需要搜尋舊版資料庫、電子郵件存放區或 Windows Search 不支援的其他資料結構時，您應該先判斷該資料存放區的通訊協定處理常式是否已存在，或許可以與其他應用程式（例如 SharePoint Server）一起使用。</span><span class="sxs-lookup"><span data-stu-id="c8816-123">Hence, when users need to search legacy databases, email stores or other data structures that are not supported by Windows Search, you should first determine whether a protocol handler already exists for that data store, perhaps for use with another application such as SharePoint Server.</span></span> <span data-ttu-id="c8816-124">若是如此，您可以在系統上安裝該通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="c8816-124">If so, you can install that protocol handler on the system.</span></span>

## <a name="windows-desktop-search-2x"></a><span data-ttu-id="c8816-125">Windows 桌面搜尋2。x</span><span class="sxs-lookup"><span data-stu-id="c8816-125">Windows Desktop Search 2.x</span></span>

<span data-ttu-id="c8816-126">強烈建議您不要使用和開發 Microsoft Windows 桌面搜尋)  (的2.x 版。</span><span class="sxs-lookup"><span data-stu-id="c8816-126">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged.</span></span> <span data-ttu-id="c8816-127">使用[Windows Search](-search-3x-wds-overview.md)和[Windows Search API](-search-reference-entry-page.md)，而不是使用[Windows Desktop Search](../lwef/-search-2x-wds-overview.md)2.x。</span><span class="sxs-lookup"><span data-stu-id="c8816-127">Instead of using [Windows Desktop Search 2.x](../lwef/-search-2x-wds-overview.md), use [Windows Search](-search-3x-wds-overview.md) and [Windows Search API](-search-reference-entry-page.md).</span></span>

## <a name="platform-sdk-indexing-service"></a><span data-ttu-id="c8816-128">Platform SDK：索引服務</span><span class="sxs-lookup"><span data-stu-id="c8816-128">Platform SDK: Indexing Service</span></span>

<span data-ttu-id="c8816-129">[PLATFORM SDK：索引服務](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) 已從 Windows XP 淘汰。</span><span class="sxs-lookup"><span data-stu-id="c8816-129">[Platform SDK: Indexing Service](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) is obsolete as of Windows XP.</span></span> <span data-ttu-id="c8816-130">請改為使用 [Windows Search](-search-3x-wds-overview.md) 並 [Windows Search API](-search-reference-entry-page.md)。</span><span class="sxs-lookup"><span data-stu-id="c8816-130">Instead, use [Windows Search](-search-3x-wds-overview.md) and [Windows Search API](-search-reference-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8816-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8816-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8816-132">Windows Search 概觀</span><span class="sxs-lookup"><span data-stu-id="c8816-132">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="c8816-133">Windows Search 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="c8816-133">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="c8816-134">Windows Search 參考</span><span class="sxs-lookup"><span data-stu-id="c8816-134">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="c8816-135">Windows Search 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="c8816-135">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="c8816-136">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="c8816-136">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="c8816-137">Windows Search 詞彙</span><span class="sxs-lookup"><span data-stu-id="c8816-137">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 

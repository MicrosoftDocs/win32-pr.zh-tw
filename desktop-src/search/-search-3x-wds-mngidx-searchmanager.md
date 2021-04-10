---
description: ISearchManager 介面提供在目錄之間進行變更的方法。
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: 使用搜尋管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943285"
---
# <a name="using-the-search-manager"></a><span data-ttu-id="7aaad-103">使用搜尋管理員</span><span class="sxs-lookup"><span data-stu-id="7aaad-103">Using the Search Manager</span></span>

<span data-ttu-id="7aaad-104">[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)介面提供在目錄之間進行變更的方法。</span><span class="sxs-lookup"><span data-stu-id="7aaad-104">The [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) interface provides methods that make changes across catalogs.</span></span> <span data-ttu-id="7aaad-105">在 **ISearchManager** 層級所做的變更會全域套用至索引子所使用的所有目錄，而在 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 層級所做的變更則適用于特定的目錄。</span><span class="sxs-lookup"><span data-stu-id="7aaad-105">Changes made at the **ISearchManager** level apply globally to all catalogs used by the indexer, while changes made at the [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) level apply to specific catalogs.</span></span> <span data-ttu-id="7aaad-106">不過，Windows Search 目前只使用一個目錄 SystemIndex。</span><span class="sxs-lookup"><span data-stu-id="7aaad-106">However, currently, Windows Search uses only one catalog, SystemIndex.</span></span> <span data-ttu-id="7aaad-107">您可以使用 [搜尋管理員] 執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7aaad-107">You can use the Search Manager to do the following:</span></span>

- <span data-ttu-id="7aaad-108">取得搜尋目錄的目錄管理員實例。</span><span class="sxs-lookup"><span data-stu-id="7aaad-108">Get an instance of the Catalog Manager for the search catalog.</span></span>
- <span data-ttu-id="7aaad-109">取得 Windows Search 引擎的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="7aaad-109">Get version information about the Windows Search engine.</span></span>

<span data-ttu-id="7aaad-110">[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)介面的下列方法可協助您管理搜尋目錄 (s) ：</span><span class="sxs-lookup"><span data-stu-id="7aaad-110">The following methods of the [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) interface can help you manage your search catalog(s):</span></span>

| <span data-ttu-id="7aaad-111">方法</span><span class="sxs-lookup"><span data-stu-id="7aaad-111">Method</span></span>                                                                      | <span data-ttu-id="7aaad-112">描述</span><span class="sxs-lookup"><span data-stu-id="7aaad-112">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aaad-113">**GetCatalog**</span><span class="sxs-lookup"><span data-stu-id="7aaad-113">**GetCatalog**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | <span data-ttu-id="7aaad-114">依名稱取得目錄，並傳回該目錄的 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 實例。</span><span class="sxs-lookup"><span data-stu-id="7aaad-114">Gets a catalog by name and returns an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) for that catalog.</span></span> <span data-ttu-id="7aaad-115">這可讓您管理個別的搜尋目錄。</span><span class="sxs-lookup"><span data-stu-id="7aaad-115">This enables you to manage an individual search catalog.</span></span>                                          |
| [<span data-ttu-id="7aaad-116">**GetIndexerVersion**</span><span class="sxs-lookup"><span data-stu-id="7aaad-116">**GetIndexerVersion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | <span data-ttu-id="7aaad-117">以兩個整數傳回索引子的版本：主要版本和次要版本。</span><span class="sxs-lookup"><span data-stu-id="7aaad-117">Returns the version of the indexer in two integers: major version and minor version.</span></span> <span data-ttu-id="7aaad-118">例如，Windows 10 搜尋的主要版本號碼為「10」，而次要版本號碼為「0」。</span><span class="sxs-lookup"><span data-stu-id="7aaad-118">For example, the major version number for Windows 10 Search is "10" and the minor version number is "0".</span></span> <span data-ttu-id="7aaad-119">在 Windows XP 上的 Windows Vista 搜尋和 Windows Search 3.0 的主要版本號碼為 "3"，而次要版本號碼為 "0"。</span><span class="sxs-lookup"><span data-stu-id="7aaad-119">For Windows Vista Search and Windows Search 3.0 on Windows XP the major version number is "3" and the minor version number is "0".</span></span> |
| [<span data-ttu-id="7aaad-120">**GetIndexerVersionStr**</span><span class="sxs-lookup"><span data-stu-id="7aaad-120">**GetIndexerVersionStr**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | <span data-ttu-id="7aaad-121">以字串形式傳回索引子的完整版本號碼：例如，"10.0.18309.1000"。</span><span class="sxs-lookup"><span data-stu-id="7aaad-121">Returns the complete version number of the indexer as a string: for example, "10.0.18309.1000".</span></span> <span data-ttu-id="7aaad-122">針對 Windows 10 這通常會符合作業系統版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7aaad-122">For Windows 10 this will typically match the OS version number.</span></span> <span data-ttu-id="7aaad-123">若是 Windows XP、Vista 和7，則會不同。</span><span class="sxs-lookup"><span data-stu-id="7aaad-123">For Windows XP, Vista, and 7 it will be different.</span></span>                                                                                                                                        |


<span data-ttu-id="7aaad-124">如需這些方法的詳細資訊，請參閱 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 檔。</span><span class="sxs-lookup"><span data-stu-id="7aaad-124">For more information about these methods, see the [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) documentation.</span></span>

<span data-ttu-id="7aaad-125">下列 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 方法會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="7aaad-125">The following [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) methods are reserved for future use.</span></span> <span data-ttu-id="7aaad-126">不過，它們會實並不會影響索引子或目錄，因為目前只有一個目錄用於 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="7aaad-126">They are, however, implemented and do not affect the indexer or catalog, as there is only one catalog for Windows Search at this time.</span></span>

- <span data-ttu-id="7aaad-127">**取得 \_ BypassList**</span><span class="sxs-lookup"><span data-stu-id="7aaad-127">**get\_BypassList**</span></span>
- <span data-ttu-id="7aaad-128">**取得 \_ LocalBypass**</span><span class="sxs-lookup"><span data-stu-id="7aaad-128">**get\_LocalBypass**</span></span>
- <span data-ttu-id="7aaad-129">**取得 \_ PortNumber**</span><span class="sxs-lookup"><span data-stu-id="7aaad-129">**get\_PortNumber**</span></span>
- <span data-ttu-id="7aaad-130">**取得 \_ ProxyName**</span><span class="sxs-lookup"><span data-stu-id="7aaad-130">**get\_ProxyName**</span></span>
- <span data-ttu-id="7aaad-131">**取得 \_ UseProxy**</span><span class="sxs-lookup"><span data-stu-id="7aaad-131">**get\_UseProxy**</span></span>
- <span data-ttu-id="7aaad-132">**取得 \_ UserAgent**</span><span class="sxs-lookup"><span data-stu-id="7aaad-132">**get\_UserAgent**</span></span>
- <span data-ttu-id="7aaad-133">**put \_ UserAgent**</span><span class="sxs-lookup"><span data-stu-id="7aaad-133">**put\_UserAgent**</span></span>
- <span data-ttu-id="7aaad-134">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="7aaad-134">**SetProxy**</span></span>

<span data-ttu-id="7aaad-135">**GetParameter** 和 **SetParameter** 也保留供日後使用，但不會執行。</span><span class="sxs-lookup"><span data-stu-id="7aaad-135">**GetParameter** and **SetParameter** are also reserved for future use but are not implemented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aaad-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="7aaad-136">Related topics</span></span>

[<span data-ttu-id="7aaad-137">管理索引</span><span class="sxs-lookup"><span data-stu-id="7aaad-137">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="7aaad-138">用於管理索引的介面</span><span class="sxs-lookup"><span data-stu-id="7aaad-138">Interfaces for Managing the Index</span></span>](interfaces-for-managing-the-index.md)

[<span data-ttu-id="7aaad-139">使用目錄管理員</span><span class="sxs-lookup"><span data-stu-id="7aaad-139">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="7aaad-140">使用編目範圍管理員</span><span class="sxs-lookup"><span data-stu-id="7aaad-140">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)

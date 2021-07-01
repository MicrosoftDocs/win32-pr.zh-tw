---
description: 瞭解 Windows Search 如何讓您使用搜尋管理員、目錄管理員和編目範圍管理員來管理 Windows Search 索引。
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: 用於管理索引的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120013"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="44f8f-103">用於管理索引的介面</span><span class="sxs-lookup"><span data-stu-id="44f8f-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="44f8f-104">Windows Search 可讓您使用三個主要元件來管理 Windows Search 索引：「搜尋管理員」、「目錄管理員」和編目範圍管理員。</span><span class="sxs-lookup"><span data-stu-id="44f8f-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="44f8f-105">其中一些管理介面可以搭配標準使用者權限使用，但變更索引狀態的那些管理介面需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="44f8f-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="44f8f-106">關於用來管理索引的介面</span><span class="sxs-lookup"><span data-stu-id="44f8f-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44f8f-107">元件</span><span class="sxs-lookup"><span data-stu-id="44f8f-107">Component</span></span></th>
<th><span data-ttu-id="44f8f-108">介面</span><span class="sxs-lookup"><span data-stu-id="44f8f-108">Interfaces</span></span></th>
<th><span data-ttu-id="44f8f-109">描述</span><span class="sxs-lookup"><span data-stu-id="44f8f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="44f8f-110">搜尋管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-110">Search Manager</span></span></td>
<td><span data-ttu-id="44f8f-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="44f8f-112">提供方法來取得和設定 Windows Search 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="44f8f-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="44f8f-113">取得特定目錄之目錄管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="44f8f-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="44f8f-114">取得或設定 proxy 資訊。</span><span class="sxs-lookup"><span data-stu-id="44f8f-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="44f8f-115">取得 Windows Search 引擎的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="44f8f-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="44f8f-116">如需詳細資訊，請參閱 <a href="-search-3x-wds-mngidx-searchmanager.md">使用搜尋管理員</a>。</span><span class="sxs-lookup"><span data-stu-id="44f8f-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44f8f-117">目錄管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="44f8f-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="44f8f-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="44f8f-120">提供管理個別搜尋目錄的方法，例如造成重新編制索引或設定超時時間。</span><span class="sxs-lookup"><span data-stu-id="44f8f-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="44f8f-121">此介面會在四個區域中管理目錄：</span><span class="sxs-lookup"><span data-stu-id="44f8f-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="44f8f-122">目錄內容-確保新的資料已編制索引，而且其他應用程式和元件可以正常運作，方法是強制重新編制所有或部分類別目錄的索引，或重設整個目錄。</span><span class="sxs-lookup"><span data-stu-id="44f8f-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="44f8f-123">目錄屬性-設定屬性，以決定當連接到通訊協定處理常式時，目錄如何管理時間超時，以及如何在搜尋中處理變音符號標記。</span><span class="sxs-lookup"><span data-stu-id="44f8f-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="44f8f-124">目錄狀態-取得目錄的相關資訊，包括狀態、大小和目前的活動狀態。</span><span class="sxs-lookup"><span data-stu-id="44f8f-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="44f8f-125">存取其他介面-抓取編目範圍管理員所需的其他搜尋相關介面、資料變更通知，以及 <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="44f8f-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="44f8f-126">如需詳細資訊，請參閱 <a href="-search-3x-wds-mngidx-catalog-manager.md">使用目錄管理員</a>。</span><span class="sxs-lookup"><span data-stu-id="44f8f-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44f8f-127">編目範圍管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="44f8f-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="44f8f-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="44f8f-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="44f8f-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="44f8f-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="44f8f-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="44f8f-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="44f8f-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="44f8f-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="44f8f-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="44f8f-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="44f8f-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="44f8f-135">提供方法來通知搜尋引擎有關要編目或監看的容器，以及要在索引中包含或排除的容器底下的專案。</span><span class="sxs-lookup"><span data-stu-id="44f8f-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="44f8f-136">您也可以查詢編目範圍管理員，以查看特定的 URL 是否在編目範圍中。</span><span class="sxs-lookup"><span data-stu-id="44f8f-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="44f8f-137">如需詳細資訊，請參閱 <a href="-search-3x-wds-extidx-csm.md">使用編目範圍管理員</a>。</span><span class="sxs-lookup"><span data-stu-id="44f8f-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="44f8f-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="44f8f-138">Related topics</span></span>

[<span data-ttu-id="44f8f-139">管理索引</span><span class="sxs-lookup"><span data-stu-id="44f8f-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="44f8f-140">使用搜尋管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="44f8f-141">使用目錄管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="44f8f-142">使用編目範圍管理員</span><span class="sxs-lookup"><span data-stu-id="44f8f-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)

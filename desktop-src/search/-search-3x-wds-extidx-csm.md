---
description: 編目範圍管理員 (CSM) 是一組介面，可提供方法來通知 Windows Search 引擎有關要將容器編目的容器，以及要在目錄中包含或排除的容器底下的專案。
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: 使用編目範圍管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112496"
---
# <a name="using-the-crawl-scope-manager"></a><span data-ttu-id="0d9f5-103">使用編目範圍管理員</span><span class="sxs-lookup"><span data-stu-id="0d9f5-103">Using the Crawl Scope Manager</span></span>

<span data-ttu-id="0d9f5-104">編目範圍管理員 (CSM) 是一組介面，可提供方法來通知 Windows Search 引擎有關要將容器編目的容器，以及要在目錄中包含或排除的容器底下的專案。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-104">The Crawl Scope Manager (CSM) is a set of interfaces that provides methods to inform the Windows Search engine about containers to crawl and items under those containers to include or exclude in the catalog.</span></span> <span data-ttu-id="0d9f5-105">開發人員可以使用 CSM，以程式設計方式為新的資料存放區或通訊協定處理常式定義編目範圍。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-105">Developers can use the CSM to define a crawl scope programmatically for a new data store or protocol handler.</span></span> <span data-ttu-id="0d9f5-106">系統管理員可以使用 CSM 來查看所有使用者的索引、搜尋根和範圍規則。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-106">Administrators can use the CSM to view all users' indexes, search roots, and scope rules.</span></span>

<span data-ttu-id="0d9f5-107">本節的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="0d9f5-107">This section is organized as follows:</span></span>

-   [<span data-ttu-id="0d9f5-108">什麼是編目範圍管理員？</span><span class="sxs-lookup"><span data-stu-id="0d9f5-108">What is the Crawl Scope Manager?</span></span>](#what-is-the-crawl-scope-manager)
-   [<span data-ttu-id="0d9f5-109">搜尋根和範圍規則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-109">Search Roots and Scope Rules</span></span>](#search-roots-and-scope-rules)
    -   [<span data-ttu-id="0d9f5-110">搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="0d9f5-110">Search Roots</span></span>](#search-roots-and-scope-rules)
    -   [<span data-ttu-id="0d9f5-111">範圍規則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-111">Scope Rules</span></span>](#scope-rules)
-   [<span data-ttu-id="0d9f5-112">編目範圍管理員支援的群組原則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-112">Group Policies Supported by the Crawl Scope Manager</span></span>](#group-policies-supported-by-the-crawl-scope-manager)
-   [<span data-ttu-id="0d9f5-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d9f5-113">Related topics</span></span>](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a><span data-ttu-id="0d9f5-114">什麼是編目範圍管理員？</span><span class="sxs-lookup"><span data-stu-id="0d9f5-114">What is the Crawl Scope Manager?</span></span>

<span data-ttu-id="0d9f5-115">若要瞭解編目範圍管理員，您必須瞭解下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="0d9f5-115">To understand the Crawl Scope Manager, you must understand the following terms:</span></span>

-   <span data-ttu-id="0d9f5-116">編目 *範圍* 是指向資料存放區或容器的一組 url (電子郵件資料存放區、資料庫、網路檔案共用等) ，索引子會進行編目以索引項目目。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-116">A *crawl scope* is a set of URLs pointing to data stores or containers (email data stores, databases, network file shares, and so on) that the indexer crawls to index items.</span></span> <span data-ttu-id="0d9f5-117">若為階層式資料存放區，編目範圍可以包含父 URL，但會排除子 URL，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-117">For a hierarchical data store, the crawl scope can include a parent URL but exclude a child URL and vice versa.</span></span> <span data-ttu-id="0d9f5-118">編目範圍內的專案會編制索引;系統會忽略編目範圍外的專案。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-118">Items within the crawl scope are indexed; items outside the crawl scope are ignored.</span></span>
-   <span data-ttu-id="0d9f5-119">*搜尋根目錄* 是識別與特定通訊協定處理常式相關聯之容器或資料存放區的最上層 URL。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-119">A *search root* is the top-level URL identifying a container or data store that is associated with a particular protocol handler.</span></span> <span data-ttu-id="0d9f5-120">搜尋根可以識別特定于使用者、位於遠端電腦上，或符合萬用字元模式的位置。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-120">Search roots can identify locations that are specific to a user, that are on a remote computer, or that match a wildcard pattern.</span></span> <span data-ttu-id="0d9f5-121">當您加入新的資料存放區或通訊協定處理常式時，您也應該在編目範圍中新增搜尋根。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-121">When you add a new data store or protocol handler, you should also add a search root to the crawl scope.</span></span>
-   <span data-ttu-id="0d9f5-122">*範圍規則* 是一種規則，包含或排除搜尋根內的 url，使其無法進行編目及編制索引。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-122">A *scope rule* is a rule that includes or excludes URLs within a search root from being crawled and indexed.</span></span> <span data-ttu-id="0d9f5-123">例如，假設您想要將 ProjectFiles 資料夾中的所有專案編制索引，但子資料夾原型除外。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-123">For example, suppose you want everything within the ProjectFiles folder indexed except for the subfolder Prototypes.</span></span> <span data-ttu-id="0d9f5-124">您需要 file:///C： WorkteamA ProjectFiles 的包含規則 \\ \\ \\ ，以及 File:///C： \\ WorkteamA ProjectFiles 原型的排除規則 \\ \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-124">You would need an inclusion rule for file:///C:\\WorkteamA\\ProjectFiles\\ and an exclusion rule for file:///C:\\WorkteamA\\ProjectFiles\\Prototypes\\.</span></span>

<span data-ttu-id="0d9f5-125">**編目範圍管理員 (CSM)** 是一組 api，可讓您新增、移除和列舉 Windows Search 索引子的搜尋根和範圍規則。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-125">The **Crawl Scope Manager (CSM)** is a set of APIs that lets you add, remove, and enumerate search roots and scope rules for the Windows Search indexer.</span></span> <span data-ttu-id="0d9f5-126">當您想要讓索引子開始編目新的容器時，您可以使用 CSM 來設定搜尋根目錄 (s) 和範圍規則，以尋找搜尋根 () 中的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-126">When you want the indexer to begin crawling a new container, you can use the CSM to set the search root(s) and scope rules for paths within the search root(s).</span></span> <span data-ttu-id="0d9f5-127">例如，如果您安裝新的通訊協定處理常式，您可以建立搜尋根，並新增一或多個包含規則。然後，索引子就可以開始進行初始索引編制的爬網。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-127">For example, if you install a new protocol handler, you can create a search root and add one or more inclusion rules; then the indexer can start a crawl for the initial indexing.</span></span> <span data-ttu-id="0d9f5-128">CSM 提供下列介面來協助您以程式設計方式執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-128">The CSM offers the following interfaces to help you do this programmatically.</span></span>

-   [<span data-ttu-id="0d9f5-129">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="0d9f5-129">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [<span data-ttu-id="0d9f5-130">IEnumSearchScopeRules</span><span class="sxs-lookup"><span data-stu-id="0d9f5-130">IEnumSearchScopeRules</span></span>](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [<span data-ttu-id="0d9f5-131">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="0d9f5-131">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [<span data-ttu-id="0d9f5-132">ISearchCrawlScopeManager2</span><span class="sxs-lookup"><span data-stu-id="0d9f5-132">ISearchCrawlScopeManager2</span></span>](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [<span data-ttu-id="0d9f5-133">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="0d9f5-133">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [<span data-ttu-id="0d9f5-134">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="0d9f5-134">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [<span data-ttu-id="0d9f5-135">ISearchItem</span><span class="sxs-lookup"><span data-stu-id="0d9f5-135">ISearchItem</span></span>](./-search-isearchitem.md)

<span data-ttu-id="0d9f5-136">雖然您可以使用 CSM Api 以程式設計方式定義編目範圍，但 CSM 也是設計來支援終端使用者。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-136">While you can use the CSM APIs to define a crawl scope programmatically, the CSM was designed to support end users as well.</span></span> <span data-ttu-id="0d9f5-137">例如，假設您已開發新資料存放區的通訊協定處理常式，而您想要讓使用者或系統管理員管理應該編制索引的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-137">For example, suppose you have developed a protocol handler for a new data store, and you want to let users or administrators manage which paths should be indexed.</span></span> <span data-ttu-id="0d9f5-138">您可以使用編目範圍管理員設定一或多個搜尋根 (例如，file:///C： \\ MyContainer \\) ，而設定索引編制選項的 Windows Search 使用者介面會顯示每個具有核取方塊的搜尋根。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-138">You can use the Crawl Scope Manager to set one or more search roots (for example, file:///C:\\MyContainer\\), and the Windows Search user interface for setting indexing options will display each search root with a check box.</span></span> <span data-ttu-id="0d9f5-139">然後，使用者可以包含或排除該路徑或該路徑的子系。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-139">Users can then include or exclude that path or children of that path.</span></span>

## <a name="search-roots-and-scope-rules"></a><span data-ttu-id="0d9f5-140">搜尋根和範圍規則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-140">Search Roots and Scope Rules</span></span>

<span data-ttu-id="0d9f5-141">搜尋根和範圍規則，並定義一組工作中的 Url，以組成索引子的編目範圍。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-141">Search roots and scope rules together define a working set of URLs that comprise the indexer's crawl scope.</span></span>

### <a name="search-roots"></a><span data-ttu-id="0d9f5-142">搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="0d9f5-142">Search Roots</span></span>

<span data-ttu-id="0d9f5-143">設定搜尋根目錄並不會指定應編制此存放區的哪些部分的索引;它只會指出內容存放區存在，且與已註冊的通訊協定處理常式相關聯。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-143">Setting a search root does not specify which parts of this store should be indexed; it merely signals that a content store exists and is associated with a registered protocol handler.</span></span> <span data-ttu-id="0d9f5-144">搜尋根目錄的語法包含通訊協定、網站或使用者安全識別碼，以及要進行編目之位置 () 的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-144">The syntax of a search root includes a protocol, a site or user security identifier, and a path to the location(s) to be crawled.</span></span>

<span data-ttu-id="0d9f5-145">當您執行下列動作時，您應該建立新的搜尋根目錄：</span><span class="sxs-lookup"><span data-stu-id="0d9f5-145">You should create new search roots when you:</span></span>

-   <span data-ttu-id="0d9f5-146">安裝通訊協定處理常式或</span><span class="sxs-lookup"><span data-stu-id="0d9f5-146">Install a protocol handler OR</span></span>
-   <span data-ttu-id="0d9f5-147">想要為新的資料存放區編制索引</span><span class="sxs-lookup"><span data-stu-id="0d9f5-147">Want to index a new data store</span></span>

<span data-ttu-id="0d9f5-148">AND</span><span class="sxs-lookup"><span data-stu-id="0d9f5-148">AND</span></span>

-   <span data-ttu-id="0d9f5-149">該資料存放區尚未存在於索引子的編目範圍中。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-149">that data store is not already in the indexer's crawl scope.</span></span>

<span data-ttu-id="0d9f5-150">如需新增、移除和列舉搜尋根的指示，請參閱 [管理搜尋根](-search-3x-wds-extidx-csm-searchroots.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-150">Refer to [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md) for instructions on adding, removing, and enumerating search roots.</span></span>

### <a name="scope-rules"></a><span data-ttu-id="0d9f5-151">範圍規則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-151">Scope Rules</span></span>

<span data-ttu-id="0d9f5-152">範圍規則包括或排除搜尋根內的 Url，使其無法進行編目及編制索引。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-152">Scope rules include or exclude URLs within a search root from being crawled and indexed.</span></span> <span data-ttu-id="0d9f5-153">範圍規則可以由終端使用者、群組原則或協力廠商開發人員設定。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-153">Scope rules can be set by end users, by group policy, or by third-party developers.</span></span> <span data-ttu-id="0d9f5-154">當您定義新的搜尋根目錄時，您應該以程式設計的方式定義範圍規則。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-154">You should define scope rules programmatically when you define a new search root.</span></span> <span data-ttu-id="0d9f5-155">您的搜尋根目錄和範圍規則，包含資料存放區和通訊協定處理常式的預設編目範圍。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-155">Your search roots and scope rules comprise the default crawl scope for your data store and protocol handler.</span></span>

> [!Note]  
> <span data-ttu-id="0d9f5-156">具有主控台存取權的使用者可以修改預設編目範圍。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-156">Users with access to Control Panel can modify the default crawl scope.</span></span> <span data-ttu-id="0d9f5-157">因此，任何提供範圍管理的應用程式都應該一律使用列舉方法，直接從 CSM 取得規則，而不是依賴其本身儲存的使用者規則複本。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-157">Therefore, any application that offers scope management should always get the rules directly from the CSM by using the enumeration methods instead of relying on its own saved copy of the user's rules.</span></span>

 

<span data-ttu-id="0d9f5-158">如需新增、移除、還原和列舉範圍規則的指示，請參閱 [管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-158">Refer to [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md) for instructions on adding, removing, reverting, and enumerating scope rules.</span></span>

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a><span data-ttu-id="0d9f5-159">編目範圍管理員支援的群組原則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-159">Group Policies Supported by the Crawl Scope Manager</span></span>

<span data-ttu-id="0d9f5-160">系統管理員可以使用群組原則來定義整個組織的編目範圍。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-160">System administrators can define crawl scopes across their organizations by using Group Policies.</span></span> <span data-ttu-id="0d9f5-161">這些群組原則規則也可以作為使用者可覆寫的預設規則。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-161">These group policy rules can also act as default rules, which users can override.</span></span> <span data-ttu-id="0d9f5-162">例如，您可以為一個使用者群組編制一組目錄，並為另一個使用者群組建立不同的集合，讓使用者可以取消選取這些預設值。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-162">For example, you can have one set of directories indexed for one group of users and a different set for another group of users, allowing the users to deselect these defaults.</span></span> <span data-ttu-id="0d9f5-163">群組原則規則也可以做為使用者無法覆寫的強制排除規則，以防止特定使用者編制特定網路共用的索引。</span><span class="sxs-lookup"><span data-stu-id="0d9f5-163">Group policy rules can also act as forced exclusion rules that users cannot override, preventing certain users from indexing certain network shares, for example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9f5-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d9f5-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9f5-165">管理搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="0d9f5-165">Managing Search Roots</span></span>](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[<span data-ttu-id="0d9f5-166">管理範圍規則</span><span class="sxs-lookup"><span data-stu-id="0d9f5-166">Managing Scope Rules</span></span>](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[<span data-ttu-id="0d9f5-167">索引處理常式</span><span class="sxs-lookup"><span data-stu-id="0d9f5-167">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> </dl>

 

 

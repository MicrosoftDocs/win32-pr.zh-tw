---
description: 編目範圍管理員 (CSM) 可讓您定義範圍規則，其中包含或排除來自 Windows Search 編目範圍的 Url。
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: 管理範圍規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d45199726cfe36dc1c4936e9ac7699a288c3ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112497"
---
# <a name="managing-scope-rules"></a><span data-ttu-id="3a07d-103">管理範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-103">Managing Scope Rules</span></span>

<span data-ttu-id="3a07d-104">編目範圍管理員 (CSM) 可讓您定義範圍規則，其中包含或排除來自 Windows Search 編目範圍的 Url。</span><span class="sxs-lookup"><span data-stu-id="3a07d-104">The Crawl Scope Manager (CSM) enables you define scope rules that include or exclude URLs from the Windows Search crawl scope.</span></span>

<span data-ttu-id="3a07d-105">CSM 可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="3a07d-105">The CSM lets you do the following:</span></span>

-   <span data-ttu-id="3a07d-106">將新的範圍規則新增至工作規則集</span><span class="sxs-lookup"><span data-stu-id="3a07d-106">Add new scope rules to the working rule set</span></span>
-   <span data-ttu-id="3a07d-107">移除現有的範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-107">Remove existing scope rules</span></span>
-   <span data-ttu-id="3a07d-108">列舉預設範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-108">Enumerate default scope rules</span></span>
-   <span data-ttu-id="3a07d-109">探索是否要在編目範圍中包含或排除特定的 URL，或具有父系或子範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-109">Discover whether a particular URL is included or excluded from the crawl scope or has a parent or child scope rule</span></span>

 

<span data-ttu-id="3a07d-110">本主題包含下列主旨：</span><span class="sxs-lookup"><span data-stu-id="3a07d-110">This topic includes the following subjects:</span></span>

-   [<span data-ttu-id="3a07d-111">關於範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-111">About Scope Rules</span></span>](#about-scope-rules)
-   [<span data-ttu-id="3a07d-112">開始之前</span><span class="sxs-lookup"><span data-stu-id="3a07d-112">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="3a07d-113">新增範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-113">Adding Scope Rules</span></span>](#adding-scope-rules)
    -   [<span data-ttu-id="3a07d-114">使用者規則的注意事項</span><span class="sxs-lookup"><span data-stu-id="3a07d-114">Notes on User Rules</span></span>](#notes-on-user-rules)
-   [<span data-ttu-id="3a07d-115">移除範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-115">Removing Scope Rules</span></span>](#removing-scope-rules)
-   [<span data-ttu-id="3a07d-116">還原為預設規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-116">Reverting to Default Rules</span></span>](#reverting-to-default-rules)
-   [<span data-ttu-id="3a07d-117">列舉範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-117">Enumerating Scope Rules</span></span>](#enumerating-scope-rules)
-   [<span data-ttu-id="3a07d-118">追蹤範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-118">Tracing Scope Rules</span></span>](#tracing-scope-rules)
-   [<span data-ttu-id="3a07d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a07d-119">Related topics</span></span>](#related-topics)

## <a name="about-scope-rules"></a><span data-ttu-id="3a07d-120">關於範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-120">About Scope Rules</span></span>

<span data-ttu-id="3a07d-121">範圍規則是一種規則，包含或排除搜尋根內的 Url，使其無法進行編目及編制索引。</span><span class="sxs-lookup"><span data-stu-id="3a07d-121">A scope rule is a rule that includes or excludes URLs within a search root from being crawled and indexed.</span></span> <span data-ttu-id="3a07d-122">包含規則會導致索引子將該 URL 包含在 scrawl 範圍內，而排除規則會導致索引子將該 URL 從編目範圍中排除 (與其子系) 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-122">Inclusion rules cause the indexer to include that URL in the scrawl scope, and exclusion rules cause the indexer exclude that URL (and its children) from the crawl scope.</span></span>

<span data-ttu-id="3a07d-123">例如，假設您已安裝新的應用程式，其資料檔案位於 \\ 本機電腦上的 WorkteamA ProjectFiles 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="3a07d-123">For example, suppose you've installed a new application whose data files are located in the folder WorkteamA\\ProjectFiles on a local computer.</span></span> <span data-ttu-id="3a07d-124">假設您想要將 ProjectFiles 資料夾中的所有專案編制索引，但子資料夾原型中的專案除外。</span><span class="sxs-lookup"><span data-stu-id="3a07d-124">Suppose you want everything within the ProjectFiles folder indexed except for items in the subfolder Prototypes.</span></span> <span data-ttu-id="3a07d-125">在這種情況下，您需要 myPH:///C： \\ WorkteamA ProjectFiles 的包含 \\ 規則 \\ ，以及 MyPH:///C： \\ WorkteamA \\ ProjectFiles 原型的排除 \\ 規則 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-125">In this situation, you would need an inclusion rule for myPH:///C:\\WorkteamA\\ProjectFiles\\ and an exclusion rule for myPH:///C:\\WorkteamA\\ProjectFiles\\Prototypes\\.</span></span>

<span data-ttu-id="3a07d-126">有三種類型的規則，優先順序如下：</span><span class="sxs-lookup"><span data-stu-id="3a07d-126">There are three types of rules, with the following order of precedence:</span></span>

1.  <span data-ttu-id="3a07d-127">群組原則規則是由系統管理員所設定，而且可以覆寫所有其他規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-127">Group Policy rules are set by administrators and can override all other rules.</span></span>
2.  <span data-ttu-id="3a07d-128">使用者規則是由使用者在 Windows Search options 使用者介面中修改範圍而設定。</span><span class="sxs-lookup"><span data-stu-id="3a07d-128">User rules are set by users modifying the scope in the Windows Search options user interface.</span></span> <span data-ttu-id="3a07d-129">使用者或其他應用程式可以移除所有的使用者規則，並還原為預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-129">Users or other applications can remove all user rules and revert to default rules.</span></span>
3.  <span data-ttu-id="3a07d-130">預設規則通常是由應用程式設定，以定義預設範圍。</span><span class="sxs-lookup"><span data-stu-id="3a07d-130">Default rules are typically set by an application to define a default scope.</span></span> <span data-ttu-id="3a07d-131">例如，當新的通訊協定處理常式或容器新增至系統時，可能會設定預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-131">For example, default rules might be set when a new protocol handler or container is added to the system.</span></span>

<span data-ttu-id="3a07d-132">這些類型的規則會一起組成編目範圍管理員 (CSM) 產生要編目之 Url 的完整清單的 *工作規則集* 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-132">Together, these types of rules comprise the *working rule set* from which the Crawl Scope Manager (CSM) generates the full list of URLs to crawl.</span></span> <span data-ttu-id="3a07d-133">雖然群組原則規則和使用者規則可以覆寫預設規則，但它們會保留在自己的預設規則集中，您隨時都可以將其還原。</span><span class="sxs-lookup"><span data-stu-id="3a07d-133">While default rules can be overridden by group policy rules and by user rules, they are maintained in their own default rule set, which you can revert to at any time.</span></span> <span data-ttu-id="3a07d-134">索引子會從工作規則集編目 Url，並將專案、屬性和內容新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="3a07d-134">The indexer crawls the URLs from the working rule set and adds items, properties, and content to the catalog.</span></span>

> [!Note]  
> <span data-ttu-id="3a07d-135">具有主控台存取權的使用者，可以透過該介面修改規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-135">Users with access to Control Panel can modify the rules through that interface.</span></span> <span data-ttu-id="3a07d-136">因此，提供範圍管理的應用程式應該一律使用列舉方法，直接從 CSM 取得規則，而不是依賴已儲存的使用者規則複本。</span><span class="sxs-lookup"><span data-stu-id="3a07d-136">Therefore, applications offering scope management should always get the rules directly from the CSM by using the enumeration methods instead of relying on a saved copy of user rules.</span></span>

 

<span data-ttu-id="3a07d-137">排除規則可以使用萬用字元 ' ' 定義模式 Url， \* 例如： file:///C： \\ ProjectA \\ \* \\ 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-137">Exclusion rules can define pattern URLs with the wildcard character '\*'; for example: file:///C:\\ProjectA\\\*\\.</span></span> <span data-ttu-id="3a07d-138">使用此模式的排除規則，可防止索引子將 ProjectA 目錄下的任何資料夾編目。</span><span class="sxs-lookup"><span data-stu-id="3a07d-138">An exclusion rule using this pattern prevents the indexer from crawling any folders under the ProjectA directory.</span></span> <span data-ttu-id="3a07d-139">針對較複雜的範例，假設有一個包含 file:///C： ProjectA 的規則 \\ \\ ，以及 file:///C： ProjectA 資料的排除模式 \\ 規則 \\ \* \\ \\ \* 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-139">For a more complicated example, suppose there is an inclusion rule for file:///C:\\ProjectA\\ and an exclusion pattern rule for file:///C:\\ProjectA\\\*\\data\\\*.</span></span> <span data-ttu-id="3a07d-140">在此情況下，索引子會編目中的專案：</span><span class="sxs-lookup"><span data-stu-id="3a07d-140">In this case, the indexer would crawl items in:</span></span>

-   <span data-ttu-id="3a07d-141">C： \\ ProjectA</span><span class="sxs-lookup"><span data-stu-id="3a07d-141">C:\\ProjectA</span></span>\\
-   <span data-ttu-id="3a07d-142">C： \\ ProjectA \\ **version1** \\ testfiles</span><span class="sxs-lookup"><span data-stu-id="3a07d-142">C:\\ProjectA\\**version1**\\testfiles</span></span>\\
-   <span data-ttu-id="3a07d-143">C： \\ ProjectA \\ **version1 \\ temp** \\ 資料</span><span class="sxs-lookup"><span data-stu-id="3a07d-143">C:\\ProjectA\\**version1\\temp**\\data</span></span>\\

<span data-ttu-id="3a07d-144">但是，索引子不會將中的專案編目：</span><span class="sxs-lookup"><span data-stu-id="3a07d-144">But the indexer would not crawl items in:</span></span>

-   <span data-ttu-id="3a07d-145">C： \\ ProjectA \\ **version1** \\ 資料</span><span class="sxs-lookup"><span data-stu-id="3a07d-145">C:\\ProjectA\\**version1**\\data</span></span>\\

 

## <a name="before-you-begin"></a><span data-ttu-id="3a07d-146">開始之前</span><span class="sxs-lookup"><span data-stu-id="3a07d-146">Before You Begin</span></span>

<span data-ttu-id="3a07d-147">使用任何編目範圍管理員介面之前，您必須執行下列必要條件步驟：</span><span class="sxs-lookup"><span data-stu-id="3a07d-147">Before you use any of the Crawl Scope Manager interfaces, you must perform the following prerequisite steps:</span></span>

1.  <span data-ttu-id="3a07d-148">建立 **CSearchManager** 物件，並取得其 **ISearchManager** 介面。</span><span class="sxs-lookup"><span data-stu-id="3a07d-148">Create the **CSearchManager** object and obtain its **ISearchManager** interface.</span></span>
2.  <span data-ttu-id="3a07d-149">針對 "SystemIndex" 呼叫 **ISearchManager：： GetCatalog** ，以取得 **ISearchCatalogManager** 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="3a07d-149">Call **ISearchManager::GetCatalog** for "SystemIndex" to obtain an instance of the **ISearchCatalogManager** interface.</span></span>
3.  <span data-ttu-id="3a07d-150">呼叫 **ISearchCatalogManager：： GetCrawlScopeManager** 來取得 **ISearchCrawlScopeManager** 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="3a07d-150">Call **ISearchCatalogManager::GetCrawlScopeManager** to obtain an instance of the **ISearchCrawlScopeManager** interface.</span></span>

<span data-ttu-id="3a07d-151">對編目範圍管理員進行任何變更之後，您必須呼叫 [**ISearchCrawlScopeManager：： SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) 方法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-151">After making any changes to the Crawl Scope Manager, you must call the [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) method.</span></span> <span data-ttu-id="3a07d-152">這個方法不接受任何參數，且 \_ 成功時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="3a07d-152">This method takes no parameters and returns S\_OK on success.</span></span>

 

## <a name="adding-scope-rules"></a><span data-ttu-id="3a07d-153">新增範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-153">Adding Scope Rules</span></span>

<span data-ttu-id="3a07d-154">CSM 的工作規則集包括使用者和預設規則，以及群組原則強制執行的任何規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-154">The working rules set for the CSM includes user and default rules, as well as any rules forced by group policy.</span></span> <span data-ttu-id="3a07d-155">使用者規則是由使用者在使用者介面中設定，而預設規則可以由下列任何一項設定：</span><span class="sxs-lookup"><span data-stu-id="3a07d-155">User rules are set up by users in a user interface, and default rules can be set by any of the following:</span></span>

-   <span data-ttu-id="3a07d-156">系統管理員所執行的群組原則 (這些不會使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="3a07d-156">Group policies implemented by a system administrator (These do not use the [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.)</span></span>
-   <span data-ttu-id="3a07d-157">應用程式的安裝或更新，例如 Windows Search 或通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="3a07d-157">The installation or update of an application like Windows Search or a protocol handler</span></span>
-   <span data-ttu-id="3a07d-158">新增資料存放區或容器的安裝應用程式</span><span class="sxs-lookup"><span data-stu-id="3a07d-158">A setup application for the addition of a new data store or container</span></span>

<span data-ttu-id="3a07d-159">[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)提供兩種方法來加入新的範圍規則，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="3a07d-159">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) provides two methods for adding new scope rules, as described in the following table.</span></span> <span data-ttu-id="3a07d-160">檔案系統的包含規則路徑結尾必須是反斜線 ' \\ ' (例如，file:///C： \\ files \\) ，而排除規則的路徑結尾必須是星號 (例如 file:///c： \\ files \\ \*) 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-160">Paths for inclusion rules for the file system must end with a backslash '\\' (for example, file:///C:\\files\\), and paths for exclusion rules must end with an asterisk (for example, file:///c:\\files\\\*).</span></span> <span data-ttu-id="3a07d-161">只有排除規則可以包含模式 Url。</span><span class="sxs-lookup"><span data-stu-id="3a07d-161">Only exclusion rules can contain pattern URLs.</span></span> <span data-ttu-id="3a07d-162">此外，我們建議您在路徑中包含使用者的安全識別碼 (Sid) ，以獲得更好的安全性。</span><span class="sxs-lookup"><span data-stu-id="3a07d-162">Furthermore, we recommend including users' security identifiers (SIDs) in paths, for better security.</span></span> <span data-ttu-id="3a07d-163">每個使用者的路徑更為安全，因為查詢會在每個使用者進程中執行，以確保某一位使用者看不到從另一個使用者的收件匣編制索引的專案。</span><span class="sxs-lookup"><span data-stu-id="3a07d-163">Per-user paths are more secure as queries would then run in a per-user process, ensuring that one user cannot see items indexed from another user's inbox, for example.</span></span>

<span data-ttu-id="3a07d-164">下表說明用來新增範圍規則之 ISearchCrawlScopeManager 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-164">The following table describes the methods of the ISearchCrawlScopeManager interface used for adding new scope rules.</span></span>



| <span data-ttu-id="3a07d-165">方法</span><span class="sxs-lookup"><span data-stu-id="3a07d-165">Method</span></span>                                                                              | <span data-ttu-id="3a07d-166">描述</span><span class="sxs-lookup"><span data-stu-id="3a07d-166">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a07d-167">**AddUserScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-167">**AddUserScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | <span data-ttu-id="3a07d-168">新增 URL 的規則，如同使用者所指定。</span><span class="sxs-lookup"><span data-stu-id="3a07d-168">Adds a rule for a URL, as specified by the user.</span></span> <span data-ttu-id="3a07d-169">這些規則會覆寫預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-169">These rules override default rules.</span></span> <span data-ttu-id="3a07d-170">如果您已執行使用者介面，讓使用者管理自己的範圍規則和 Url，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-170">Use this method if you have implemented a user interface that lets users manage their own scope rules and URLs.</span></span>                         |
| [<span data-ttu-id="3a07d-171">**AddDefaultScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-171">**AddDefaultScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | <span data-ttu-id="3a07d-172">新增 URL 的規則，如同其他應用程式（例如通訊協定處理常式）所指定。</span><span class="sxs-lookup"><span data-stu-id="3a07d-172">Adds a rule for a URL, as specified by another application like a protocol handler.</span></span> <span data-ttu-id="3a07d-173">當您已執行新的通訊協定處理常式，或加入新的資料存放區時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-173">Use this method when you have implemented a new protocol handler or added a new data store.</span></span> <span data-ttu-id="3a07d-174">這些規則可以由使用者規則覆寫。</span><span class="sxs-lookup"><span data-stu-id="3a07d-174">These rules can be overridden by user rules.</span></span> |



 

<span data-ttu-id="3a07d-175">每個方法都會取得可編制索引位置的 URL，以及決定是否應包含或排除 URL 的旗標。</span><span class="sxs-lookup"><span data-stu-id="3a07d-175">Each method takes a URL to an indexable location and flags that determine whether the URL should be included or excluded.</span></span> <span data-ttu-id="3a07d-176">*FFollowFlags* 參數已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3a07d-176">The *fFollowFlags* parameter is reserved for future use.</span></span> <span data-ttu-id="3a07d-177">當您加入新的範圍規則，且編目範圍管理員根據) 所提供的 URL 或模式來判斷規則已存在 (時，會更新工作規則集，如此一來， (1) 舊規則會被新規則取代， (2) 任何與其衝突的使用者規則都會被移除。</span><span class="sxs-lookup"><span data-stu-id="3a07d-177">When you add a new scope rule and the Crawl Scope Manager determines that the rule already exists (based on the URL or the pattern provided), the working rule set is updated so that (1) the old rule is replaced by the new rule and (2) any user rules that contradict it are removed.</span></span>

<span data-ttu-id="3a07d-178">**秘訣：** 雖然 file://根目錄預設包含在編目範圍中，但預設不會編制程式檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="3a07d-178">**Tip:** While the file:// root is included by default in the crawl scope, Program Files is not indexed by default.</span></span> <span data-ttu-id="3a07d-179">因此，將資料儲存至 [Program Files] 目錄的應用程式必須將其位置新增為預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-179">Therefore, applications with data saved to their Program Files directory need to add their location as a default rule.</span></span>

### <a name="notes-on-user-rules"></a><span data-ttu-id="3a07d-180">使用者規則的注意事項</span><span class="sxs-lookup"><span data-stu-id="3a07d-180">Notes on User Rules</span></span>

<span data-ttu-id="3a07d-181">如果新的使用者規則與現有的預設規則相同，則新的使用者規則會覆寫工作規則集中的預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-181">If a new user rule is the same as an existing default rule, the new user rule overrides the default rule in the working rule set.</span></span> <span data-ttu-id="3a07d-182">如果新的使用者規則與現有的使用者規則相同，則會取代舊的使用者規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-182">If the new user rule is the same as an existing user rule, the old user rule is replaced.</span></span>

<span data-ttu-id="3a07d-183">在工作規則集中設定旗標 *fOverrideChildren* 會產生下列結果：</span><span class="sxs-lookup"><span data-stu-id="3a07d-183">Setting the flag *fOverrideChildren* has the following results in the working rule set:</span></span>

-   <span data-ttu-id="3a07d-184">**TRUE** 會導致從工作規則集移除所有子規則， (使用者規則和預設規則) 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-184">**TRUE** results in the removal of all child rules from the working rule set (both user rules and default rules).</span></span>
-   <span data-ttu-id="3a07d-185">FALSE 會導致重新新增至工作規則，將所有預設規則設定為新使用者規則的子系。</span><span class="sxs-lookup"><span data-stu-id="3a07d-185">FALSE results in re-adding to the working rules set all the default rules that are children of the new user rule.</span></span> <span data-ttu-id="3a07d-186">如果子系預設規則為包含，而新的使用者規則為排除，則預設規則會變更為包含使用者規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-186">If a child default rule is an inclusion and the new user rule is an exclusion, the default rule is changed to an inclusion user rule.</span></span>

 

## <a name="removing-scope-rules"></a><span data-ttu-id="3a07d-187">移除範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-187">Removing Scope Rules</span></span>

<span data-ttu-id="3a07d-188">您可以使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面，從工作規則集移除範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-188">You can use the [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface to remove a scope rule from the working rule set.</span></span> <span data-ttu-id="3a07d-189">此介面提供下列兩個方法來移除範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-189">This interface provides the following two methods for removing scope rules.</span></span>



| <span data-ttu-id="3a07d-190">方法</span><span class="sxs-lookup"><span data-stu-id="3a07d-190">Method</span></span>                                                                                    | <span data-ttu-id="3a07d-191">描述</span><span class="sxs-lookup"><span data-stu-id="3a07d-191">Description</span></span>                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a07d-192">**RemoveScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-192">**RemoveScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | <span data-ttu-id="3a07d-193">從工作規則集中移除指定之 URL 的使用者規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-193">Removes a user rule for a specified URL from the working rule set.</span></span> <span data-ttu-id="3a07d-194">如果使用者規則是的重複項或覆寫預設規則，則預設規則會保留在工作規則集中。</span><span class="sxs-lookup"><span data-stu-id="3a07d-194">If the user rule is a duplicate of or overrides a default rule, the default rule remains in the working rule set.</span></span>                  |
| [<span data-ttu-id="3a07d-195">**RemoveDefaultScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-195">**RemoveDefaultScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | <span data-ttu-id="3a07d-196">從工作規則集和預設規則集移除指定 URL 的預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-196">Removes a default rule for a specified URL from both the working rule set and the default rule set.</span></span> <span data-ttu-id="3a07d-197">呼叫這個方法之後，您就無法使用 RevertToDefaultScopes 還原為此預設規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-197">After calling this method, you cannot revert to this default rule by using RevertToDefaultScopes.</span></span> |



 

<span data-ttu-id="3a07d-198">每個方法都會使用 URL 和旗標，指出要移除的規則是包含或排除規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-198">Each method takes a URL and a flag indicating whether the rule to be removed is an inclusion or exclusion rule.</span></span> <span data-ttu-id="3a07d-199">如果找不到具有該 URL 和包含/排除旗標的規則，則這些方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a07d-199">These methods returns an error if a rule with that URL and inclusion/exclusion flag is not found.</span></span>

<span data-ttu-id="3a07d-200">**秘訣：** 如果您想要完全移除編目範圍中的範圍，請使用 [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) 方法，此方法會移除搜尋根目錄和所有相關聯的範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-200">**Tip:** If you want to remove a scope from the crawl scope entirely, use the [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) method, which removes the search root and all associated scope rules.</span></span> <span data-ttu-id="3a07d-201">例如，在卸載時執行這項操作，被視為最佳做法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-201">Doing this while uninstalling, for example, is considered best practice.</span></span>

<span data-ttu-id="3a07d-202">您也可以移除搜尋根目錄的所有使用者設定覆寫，並還原為原始搜尋根目錄和預設範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-202">It is also possible to remove all user-set overrides of a search root and revert to the original search root and default scope rules.</span></span> <span data-ttu-id="3a07d-203">如需詳細資訊，請參閱下一節。</span><span class="sxs-lookup"><span data-stu-id="3a07d-203">For more information, refer to the next section.</span></span>

> [!Note]  
> <span data-ttu-id="3a07d-204">在 Windows Vista 中，如果使用者是透過主控台中的使用者設定檔移除，CSM 會移除所有包含其 SID 的規則和根，並從目錄移除其索引項目目。</span><span class="sxs-lookup"><span data-stu-id="3a07d-204">On Windows Vista, if users are removed through User Profiles in Control Panel, CSM removes all rules and roots that include their SID and removes their indexed items from the catalog.</span></span> <span data-ttu-id="3a07d-205">在 Windows XP 上，您必須手動移除使用者的根和規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-205">On Windows XP, you must remove the users' roots and rules manually.</span></span>

 

 

## <a name="reverting-to-default-rules"></a><span data-ttu-id="3a07d-206">還原為預設規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-206">Reverting to Default Rules</span></span>

<span data-ttu-id="3a07d-207">還原為預設規則會移除 URL 或根的所有使用者規則，並將所有預設規則還原至工作規則集。</span><span class="sxs-lookup"><span data-stu-id="3a07d-207">Reverting to default rules removes all user rules for a URL or root and restores all default rules to the working rule set.</span></span> <span data-ttu-id="3a07d-208">但是，它並不會移除群組原則所設定的規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-208">It does not, however, remove rules set by group policy.</span></span> <span data-ttu-id="3a07d-209">[**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes)方法不接受任何參數，如果無法還原為預設規則，則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3a07d-209">The [**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) method takes no parameters and returns an error code if it is unable to revert to default rules.</span></span>

 

## <a name="enumerating-scope-rules"></a><span data-ttu-id="3a07d-210">列舉範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-210">Enumerating Scope Rules</span></span>

<span data-ttu-id="3a07d-211">CSM 會使用標準的 COM 樣式列舉值介面 [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) 來列舉範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-211">The CSM enumerates scope rules by using a standard COM-style enumerator interface, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) .</span></span> <span data-ttu-id="3a07d-212">您可以使用此介面來列舉許多用途的範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-212">You can use this interface to enumerate scope rules for several purposes.</span></span> <span data-ttu-id="3a07d-213">例如，您可能想要在使用者介面中顯示整個工作規則集，或探索規則或規則的子系是否已在編目範圍中。</span><span class="sxs-lookup"><span data-stu-id="3a07d-213">For example, you might want to display the entire working rule set in a user interface, or discover whether a rule or the child of a rule is already in the crawl scope.</span></span>

 

## <a name="tracing-scope-rules"></a><span data-ttu-id="3a07d-214">追蹤範圍規則</span><span class="sxs-lookup"><span data-stu-id="3a07d-214">Tracing Scope Rules</span></span>

<span data-ttu-id="3a07d-215">CSM 也可讓您判斷指定的 URL 是否包含在編目範圍中，以及它是否具有父系或子系範圍規則。</span><span class="sxs-lookup"><span data-stu-id="3a07d-215">The CSM also enables you to determine whether a specified URL is included in the crawl scope and whether it has a parent or child scope rule.</span></span> <span data-ttu-id="3a07d-216">您也可以瞭解在編目範圍中包含或排除 URL 的原因。</span><span class="sxs-lookup"><span data-stu-id="3a07d-216">You can also find out why a URL is included or excluded from the crawl scope.</span></span> <span data-ttu-id="3a07d-217">這些方法不適合搭配使用模式 Url。</span><span class="sxs-lookup"><span data-stu-id="3a07d-217">These methods are not intended to be used with pattern URLs.</span></span>

<span data-ttu-id="3a07d-218">下表說明用來新增範圍規則的 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 方法。</span><span class="sxs-lookup"><span data-stu-id="3a07d-218">The following table describes the methods of [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) used for adding new scope rules.</span></span>



| <span data-ttu-id="3a07d-219">方法</span><span class="sxs-lookup"><span data-stu-id="3a07d-219">Method</span></span>                                                                                      | <span data-ttu-id="3a07d-220">描述</span><span class="sxs-lookup"><span data-stu-id="3a07d-220">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a07d-221">**GetParentScopeVersionId**</span><span class="sxs-lookup"><span data-stu-id="3a07d-221">**GetParentScopeVersionId**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | <span data-ttu-id="3a07d-222">取得父包含 URL 的版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a07d-222">Gets the version ID of the parent inclusion URL.</span></span> <span data-ttu-id="3a07d-223">您可以使用這個方法來查看父範圍自您上次檢查之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="3a07d-223">You can use this method to see if the parent scope has changed since the last time you checked it.</span></span><br/> <span data-ttu-id="3a07d-224">範例：如果郵件應用程式使用提供者管理的通知，它可能會在關閉之前取得父範圍版本，並在開啟時再次檢查版本。</span><span class="sxs-lookup"><span data-stu-id="3a07d-224">Example: If a mail application uses provider-managed notifications, it might get the parent scope version before it closes and check the version again when it opens.</span></span> <span data-ttu-id="3a07d-225">然後，應用程式可以判斷它是否需要將一組新的通知推送至索引子。</span><span class="sxs-lookup"><span data-stu-id="3a07d-225">Then the application can determine whether it needs to push a new set of notifications to the indexer.</span></span><br/> |
| [<span data-ttu-id="3a07d-226">**HasChildScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-226">**HasChildScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | <span data-ttu-id="3a07d-227">如果指定的 URL 具有子規則， (套用至其 URL 階層內任何層級之子系的規則，則傳回 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-227">Returns **TRUE** if the specified URL has a child rule (a rule applying to a child at any level within its URL hierarchy).</span></span> <br/> <span data-ttu-id="3a07d-228">範例：如果 URL 為 file:///C： \\ folder \\ ，則如果 CSM 有專門針對 File:///C： folder 子資料夾的範圍規則，則此方法會傳回 **TRUE** \\ \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-228">Example: If the URL is file:///C:\\Folder\\, this method returns **TRUE** if the CSM has a scope rule specifically for file:///C:\\Folder\\Subfolder\\.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="3a07d-229">**HasParentScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-229">**HasParentScopeRule**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | <span data-ttu-id="3a07d-230">如果指定的 URL 具有父規則 (套用至 URL 階層中任何層級之父系的規則，則傳回 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-230">Returns **TRUE** if the specified URL has a parent rule (a rule applying to a parent at any level in the URL hierarchy).</span></span><br/> <span data-ttu-id="3a07d-231">範例：如果 URL 是 file:///C： \\ folder \\ 子資料夾，則如果 CSM 有專門針對 File:///C： folder 的範圍規則，則這個方法會傳回 **TRUE** \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-231">Example: If the URL is file:///C:\\Folder\\Subfolder, this method returns **TRUE** if the CSM has a scope rule specifically for file:///C:\\Folder\\.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="3a07d-232">**IncludedInCrawlScope**</span><span class="sxs-lookup"><span data-stu-id="3a07d-232">**IncludedInCrawlScope**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | <span data-ttu-id="3a07d-233">如果指定的 URL 包含在編目範圍中，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-233">Returns **TRUE** if the specified URL is included in the crawl scope.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="3a07d-234">**IncludedInCrawlScopeEx**</span><span class="sxs-lookup"><span data-stu-id="3a07d-234">**IncludedInCrawlScopeEx**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | <span data-ttu-id="3a07d-235">傳回 [**CLUSION \_ REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) 列舉中的值，說明 url 包含在編目範圍中或從中排除的原因，如果 url 包含在編目範圍中，則抓取值 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3a07d-235">Returns a value from the [**CLUSION\_REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) enumeration explaining why the URL is included in or excluded from the crawl scope, and retrieves the value **TRUE** if the URL is included in the crawl scope.</span></span> <span data-ttu-id="3a07d-236">此方法可協助您識別工作規則集內的衝突。</span><span class="sxs-lookup"><span data-stu-id="3a07d-236">This method can help you identify conflicts in your working rule set.</span></span>                                                                                                                                       |



 

 

> [!Note]  
> <span data-ttu-id="3a07d-237">[**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)和 [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)方法會根據 CSM 中的規則，決定是否要將 URL 僅進行編目。</span><span class="sxs-lookup"><span data-stu-id="3a07d-237">The [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) and [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) methods determine whether the URL will be crawled based solely on the rules in the CSM.</span></span> <span data-ttu-id="3a07d-238">URL 未編目的原因可能有其他原因，例如設定的 FANCI 位 (也就是使用者在資料夾的 [屬性] 對話方塊中，不允許快速編制索引。 ) </span><span class="sxs-lookup"><span data-stu-id="3a07d-238">There can be other reasons that a URL is not crawled, such as the FANCI bit being set (that is, a user has disallowed fast indexing in the folder's Property dialog box.)</span></span>

 

<span data-ttu-id="3a07d-239">如果您認為應該排除檔案路徑，但它列為包含的，請確定排除規則的結尾為 " <path> \\ \* "。</span><span class="sxs-lookup"><span data-stu-id="3a07d-239">If you believe that a file path should be excluded, but it is listed as included, be sure that exclusion rules end with "<path>\\\*".</span></span> <span data-ttu-id="3a07d-240">如果您認為應該包含檔案或檔案路徑，但是它不是，請務必檢查檔案或路徑的 FANCI 位設定。</span><span class="sxs-lookup"><span data-stu-id="3a07d-240">If you believe that a file or file path should be included but it is not, be sure to check the FANCI bit setting for the file or path.</span></span> <span data-ttu-id="3a07d-241">若要這樣做，請以滑鼠右鍵按一下檔案或檔案路徑，然後選取 [ **屬性**]，然後確定已選取 [ **快速搜尋]、[允許編制索引服務來為此資料夾編制索引** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="3a07d-241">You can do this by right-clicking the file or file path and selecting **Properties**, then be sure the **For fast searching, allow Indexing Service to index this folder** checkbox is selected.</span></span> <span data-ttu-id="3a07d-242">如果檔案或檔案路徑未標示為要在這裡進行索引編制，就不會將它編制索引，即使它是在包含規則中也一樣。</span><span class="sxs-lookup"><span data-stu-id="3a07d-242">If the file or file path is not marked for indexing here, it will not be indexed even if it is in an inclusion rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a07d-243">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a07d-243">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3a07d-244">**參考**</span><span class="sxs-lookup"><span data-stu-id="3a07d-244">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a07d-245">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="3a07d-245">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[<span data-ttu-id="3a07d-246">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="3a07d-246">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[<span data-ttu-id="3a07d-247">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="3a07d-247">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[<span data-ttu-id="3a07d-248">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="3a07d-248">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

<span data-ttu-id="3a07d-249">**概念**</span><span class="sxs-lookup"><span data-stu-id="3a07d-249">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a07d-250">管理搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="3a07d-250">Managing Search Roots</span></span>](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 





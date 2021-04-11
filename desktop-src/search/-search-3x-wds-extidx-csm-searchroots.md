---
description: 編目範圍管理員 (CSM) 可讓您新增和移除資料存放區與 Windows Search 編目範圍之間的搜尋根。
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: 管理搜尋根目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191211"
---
# <a name="managing-search-roots"></a><span data-ttu-id="91153-103">管理搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="91153-103">Managing Search Roots</span></span>

<span data-ttu-id="91153-104">編目範圍管理員 (CSM) 可讓您新增和移除資料存放區與 Windows Search 編目範圍之間的搜尋根。</span><span class="sxs-lookup"><span data-stu-id="91153-104">The Crawl Scope Manager (CSM) enables you to add and remove search roots for your data stores to and from the Windows Search crawl scope.</span></span>

<span data-ttu-id="91153-105">本主題包含下列主旨：</span><span class="sxs-lookup"><span data-stu-id="91153-105">This topic includes the following subjects:</span></span>

-   [<span data-ttu-id="91153-106">關於搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="91153-106">About Search Roots</span></span>](#about-search-roots)
-   [<span data-ttu-id="91153-107">開始之前</span><span class="sxs-lookup"><span data-stu-id="91153-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="91153-108">Windows 7：新的編目範圍管理員 API</span><span class="sxs-lookup"><span data-stu-id="91153-108">Windows 7: New Crawl Scope Manager API</span></span>](#windows-7-new-crawl-scope-manager-api)
-   [<span data-ttu-id="91153-109">將根目錄新增至編目範圍</span><span class="sxs-lookup"><span data-stu-id="91153-109">Adding Roots to the Crawl Scope</span></span>](#adding-roots-to-the-crawl-scope)
-   [<span data-ttu-id="91153-110">從編目範圍中移除根目錄</span><span class="sxs-lookup"><span data-stu-id="91153-110">Removing Roots from the Crawl Scope</span></span>](#removing-roots-from-the-crawl-scope)
-   [<span data-ttu-id="91153-111">列舉編目範圍中的根</span><span class="sxs-lookup"><span data-stu-id="91153-111">Enumerating Roots in the Crawl Scope</span></span>](#enumerating-roots-in-the-crawl-scope)
-   [<span data-ttu-id="91153-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="91153-112">Related topics</span></span>](#related-topics)

 

## <a name="about-search-roots"></a><span data-ttu-id="91153-113">關於搜尋根目錄</span><span class="sxs-lookup"><span data-stu-id="91153-113">About Search Roots</span></span>

<span data-ttu-id="91153-114">搜尋根目錄會定義 Shell 命名空間的基底，其中可以包含或排除特定範圍，而且通常是可列舉的通訊協定中最高層級的容器。</span><span class="sxs-lookup"><span data-stu-id="91153-114">A search root defines the base of a Shell namespace where specific scopes could be included or excluded, and is usually the highest level container in a protocol that can be enumerated.</span></span> <span data-ttu-id="91153-115">它不會指定應該或不應該編制索引的這個存放區的哪些部分;它只會指出內容存放區存在，且與已註冊的通訊協定處理常式相關聯。</span><span class="sxs-lookup"><span data-stu-id="91153-115">It does not specify which parts of this store should or should not be indexed; it merely signals that a content store exists and is associated with a registered protocol handler.</span></span> <span data-ttu-id="91153-116">識別搜尋根 URL 的語法包含通訊協定、存放區或使用者的安全識別碼、路徑，以及選擇性的特定專案 (例如檔案) 。</span><span class="sxs-lookup"><span data-stu-id="91153-116">The syntax for identifying a search root URL includes the protocol, the store or user's security identifier, the path, and optionally a specific item (like a file).</span></span> <span data-ttu-id="91153-117">下列範例示範兩種形式的搜尋根目錄語法。</span><span class="sxs-lookup"><span data-stu-id="91153-117">The following examples show two forms of the syntax for a search root.</span></span>


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



<span data-ttu-id="91153-118"><protocol>區段後面必須接著兩個 (2) 正斜線 ( '/' ) ，除非它是 file： protocol， (file:///) 需要三個斜線。</span><span class="sxs-lookup"><span data-stu-id="91153-118">The <protocol> segment must be followed by two (2) forward slashes ('/') unless it is the file: protocol, which requires three slashes (file:///).</span></span> <span data-ttu-id="91153-119"><site or SID>如果搜尋根目錄必須是使用者特定的，則區段代表內容存放區或使用者安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="91153-119">The <site or SID> segment represents either a content store or a user security identifier if the search root is meant to be specific to the user.</span></span> <span data-ttu-id="91153-120"><path>區段是一組容器，例如目錄或資料夾，而且可以包含萬用字元 ' \* '。</span><span class="sxs-lookup"><span data-stu-id="91153-120">The <path> segment is a set of containers, like directories or folders, and can include the wildcard character '\*'.</span></span> <span data-ttu-id="91153-121">此</span><span class="sxs-lookup"><span data-stu-id="91153-121">The</span></span> <item> <span data-ttu-id="91153-122">區段是選擇性的，也可以包含萬用字元 ' \* '。</span><span class="sxs-lookup"><span data-stu-id="91153-122">segment is optional and can also include the wildcard character '\*'.</span></span> <span data-ttu-id="91153-123">如果您未包含專案，請務必使用斜線完成路徑區段，否則索引子會假設最後一個 subcontainer 是專案。</span><span class="sxs-lookup"><span data-stu-id="91153-123">If you do not include an item, be sure to finish your path segment with a slash or the indexer will assume that the last subcontainer is an item.</span></span>

<span data-ttu-id="91153-124">例如，假設您已執行通訊協定處理常式 (myPH) 來處理 \* 自訂應用程式的 myext 檔案。</span><span class="sxs-lookup"><span data-stu-id="91153-124">For example, suppose you have implemented a protocol handler (myPH) to handle files of type \*.myext for a custom application.</span></span> <span data-ttu-id="91153-125">所有這些檔案都位於 \\ 本機電腦上的 WorkteamA ProjectFiles 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="91153-125">All of these files will be located in the folder WorkteamA\\ProjectFiles on a local computer.</span></span> <span data-ttu-id="91153-126">的搜尋根可能看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="91153-126">The search root for that might look like this:</span></span>

-   <span data-ttu-id="91153-127">myPH:///C： \\ WorkteamA \\ ProjectFiles</span><span class="sxs-lookup"><span data-stu-id="91153-127">myPH:///C:\\WorkteamA\\ProjectFiles</span></span>\\

<span data-ttu-id="91153-128">假設您打算在索引中包含所有的 myext 檔案，但不包含任何其他容器。</span><span class="sxs-lookup"><span data-stu-id="91153-128">Suppose you are planning to include all .myext files but nothing else from that container in the index.</span></span> <span data-ttu-id="91153-129">的搜尋根可能看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="91153-129">The search root for that might look like this:</span></span>

-   <span data-ttu-id="91153-130">myPH:///C： \\ WorkteamA \\ ProjectFiles \\ \* . myext。</span><span class="sxs-lookup"><span data-stu-id="91153-130">myPH:///C:\\WorkteamA\\ProjectFiles\\\*.myext.</span></span>

<span data-ttu-id="91153-131">萬用字元模式會使用萬用字元 ' ' 定義 Url， \* 並將其視為模式而非 URL，但術語通常會交替使用。</span><span class="sxs-lookup"><span data-stu-id="91153-131">Wildcard patterns define URLs by using the wildcard character '\*' and are considered a pattern rather than a URL, but the terminology is often used interchangeably.</span></span> <span data-ttu-id="91153-132">例如，file:///C： \\ ProjectA \\ \* \\ 資料 \\ 會符合下列 url：</span><span class="sxs-lookup"><span data-stu-id="91153-132">For example, file:///C:\\ProjectA\\\*\\data\\ would match the following URLs:</span></span>

-   <span data-ttu-id="91153-133">C： \\ ProjectA \\ **version1** \\ 資料</span><span class="sxs-lookup"><span data-stu-id="91153-133">C:\\ProjectA\\**version1**\\data</span></span>\\
-   <span data-ttu-id="91153-134">C： \\ ProjectA \\ **version2** \\ 資料</span><span class="sxs-lookup"><span data-stu-id="91153-134">C:\\ProjectA\\**version2**\\data</span></span>\\

<span data-ttu-id="91153-135">但該模式不符合這個 URL：</span><span class="sxs-lookup"><span data-stu-id="91153-135">But that pattern would not match this URL:</span></span>

-   <span data-ttu-id="91153-136">C： \\ ProjectA \\ **version1 \\ temp** \\ 資料</span><span class="sxs-lookup"><span data-stu-id="91153-136">C:\\ProjectA\\**version1\\temp**\\data</span></span>\\

<span data-ttu-id="91153-137">您應該針對尚未在索引子的編目範圍中的容器建立新的搜尋根。</span><span class="sxs-lookup"><span data-stu-id="91153-137">You should create new search roots for containers that are not already in the crawl scope of the indexer.</span></span> <span data-ttu-id="91153-138">如果路徑 C： \\ ParentScope 已包含在編目範圍中， \\ \\ 除非您知道先前已排除子範圍，否則不需要為 C： ParentScope ChildScope 新增搜尋根目錄。</span><span class="sxs-lookup"><span data-stu-id="91153-138">If path C:\\ParentScope is already included in the crawl scope, you do not need to add a new search root for C:\\ParentScope\\ChildScope unless you know that the child scope was previously excluded.</span></span>

<span data-ttu-id="91153-139">設定 Windows Search 選項的使用者介面會向使用者顯示搜尋根，讓他們可以精簡搜尋的範圍規則。</span><span class="sxs-lookup"><span data-stu-id="91153-139">The user interface for setting Windows Search options displays search roots to users so they can refine the scope rules for their searches.</span></span> <span data-ttu-id="91153-140">在您的自訂通訊協定處理常式、容器及/或應用程式的安裝過程中，您可以使用包含和排除規則來定義預設編目範圍。</span><span class="sxs-lookup"><span data-stu-id="91153-140">As part of the installation process for your custom protocol handler, container, and/or application, you might define a default crawl scope, with inclusion and exclusion rules.</span></span> <span data-ttu-id="91153-141">這些規則會呈現給終端使用者作為位置。</span><span class="sxs-lookup"><span data-stu-id="91153-141">These rules are presented to end users as locations.</span></span> <span data-ttu-id="91153-142">使用者可以在預先定義之搜尋根目錄的子目錄中流覽，然後選取要包含在搜尋中的專案，或清除要排除的專案。</span><span class="sxs-lookup"><span data-stu-id="91153-142">Users can navigate within the subdirectories of your predefined search root and select the ones they want to include in searches or clear the ones they want to exclude.</span></span>

 

## <a name="before-you-begin"></a><span data-ttu-id="91153-143">開始之前</span><span class="sxs-lookup"><span data-stu-id="91153-143">Before You Begin</span></span>

<span data-ttu-id="91153-144">您必須執行下列必要條件步驟，才能使用任何編目範圍管理員 (CSM) 介面：</span><span class="sxs-lookup"><span data-stu-id="91153-144">Before you can use any of the Crawl Scope Manager (CSM) interfaces, you must perform the following prerequisite steps:</span></span>

1.  <span data-ttu-id="91153-145">建立 **CrawlSearchManager** 物件，並取得其 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="91153-145">Create the **CrawlSearchManager** object and obtain its [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) interface.</span></span>
2.  <span data-ttu-id="91153-146">針對 "SystemIndex" 呼叫 [**ISearchManager：： GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) ，以取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="91153-146">Call [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) for "SystemIndex" to obtain an instance of an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface.</span></span>
3.  <span data-ttu-id="91153-147">呼叫 [**ISearchCatalogManager：： GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) 來取得 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="91153-147">Call [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) to obtain an instance of [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span>

<span data-ttu-id="91153-148">對編目範圍管理員 (CSM) 進行任何變更之後，您必須呼叫 [**ISearchCrawlScopeManager：： SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall)。</span><span class="sxs-lookup"><span data-stu-id="91153-148">After making any changes to the Crawl Scope Manager (CSM), you must call [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall).</span></span> <span data-ttu-id="91153-149">這個方法不接受任何參數，且 \_ 成功時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="91153-149">This method takes no parameters and returns S\_OK on success.</span></span>

 

## <a name="windows-7-new-crawl-scope-manager-api"></a><span data-ttu-id="91153-150">Windows 7：新的編目範圍管理員 API</span><span class="sxs-lookup"><span data-stu-id="91153-150">Windows 7: New Crawl Scope Manager API</span></span>

<span data-ttu-id="91153-151">在 **Windows 7 和更新版本** 中， [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) 擴充了 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面的功能。</span><span class="sxs-lookup"><span data-stu-id="91153-151">In **Windows 7 and later**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends the functionality of the [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span> <span data-ttu-id="91153-152">[**ISearchCrawlScopeManager2：： GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion)方法會取得編目範圍管理員 (csm) 版本，這會在 csm 的狀態變更時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="91153-152">The [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method gets the Crawl Scope Manager (CSM) version, which informs clients if the state of the CSM has changed.</span></span> <span data-ttu-id="91153-153">**ISearchCrawlScopeManager2：： GetVersion** 不會產生跨進程呼叫。</span><span class="sxs-lookup"><span data-stu-id="91153-153">**ISearchCrawlScopeManager2::GetVersion** does not result in a cross-process call.</span></span> <span data-ttu-id="91153-154">如果函式成功，則傳回的指標會維持有效，直到用戶端在指標上呼叫 **UnmapViewOfFile** ，然後在傳回的控制碼上 **CloseHandle** 。</span><span class="sxs-lookup"><span data-stu-id="91153-154">If the function succeeds, then the pointer that is returned remains valid until the client calls **UnmapViewOfFile** on the pointer and **CloseHandle** on the returned handle.</span></span>

 

## <a name="adding-roots-to-the-crawl-scope"></a><span data-ttu-id="91153-155">將根目錄新增至編目範圍</span><span class="sxs-lookup"><span data-stu-id="91153-155">Adding Roots to the Crawl Scope</span></span>

<span data-ttu-id="91153-156">[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)會告知搜尋引擎有關要編目及/或監看的容器，以及要包含或排除的容器底下的專案。</span><span class="sxs-lookup"><span data-stu-id="91153-156">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) tells the search engine about containers to crawl and/or watch, and items under those containers to include or exclude.</span></span> <span data-ttu-id="91153-157">若要加入新的搜尋根目錄，請將 [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) 物件具現化、設定根屬性，然後呼叫 [**ISearchCrawlScopeManager：： AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) ，然後將指標傳遞至您的 **ISearchRoot** 物件。</span><span class="sxs-lookup"><span data-stu-id="91153-157">To add a new search root, instantiate an [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) object, set the root attributes, and then call [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) and pass it a pointer to your **ISearchRoot** object.</span></span> <span data-ttu-id="91153-158">搜尋根目錄 URL 會採用與先前所述搜尋根目錄相同的形式。</span><span class="sxs-lookup"><span data-stu-id="91153-158">The search root URL takes the same form as the search root described earlier.</span></span>

<span data-ttu-id="91153-159">下表描述 [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)的相關 put 方法;Windows Search 目前不使用介面的其他 put 方法。</span><span class="sxs-lookup"><span data-stu-id="91153-159">The following table describes the relevant put methods for [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); the interface's other put methods are not used currently by Windows Search.</span></span> <span data-ttu-id="91153-160">建議您將使用者的安全識別碼包含在所有根目錄 (Sid) ，以獲得更好的安全性。</span><span class="sxs-lookup"><span data-stu-id="91153-160">We recommend including the users' security identifiers (SIDs) in all roots for better security.</span></span> <span data-ttu-id="91153-161">每個使用者的根目錄比較安全，因為查詢是在每個使用者進程中執行，以確保某一位使用者看不到從另一個使用者的收件匣編制索引的專案。</span><span class="sxs-lookup"><span data-stu-id="91153-161">Per-user roots are more secure as queries are run in a per-user process, ensuring that one user cannot see items indexed from another user's inbox, for example.</span></span>



| <span data-ttu-id="91153-162">方法</span><span class="sxs-lookup"><span data-stu-id="91153-162">Method</span></span>                     | <span data-ttu-id="91153-163">描述</span><span class="sxs-lookup"><span data-stu-id="91153-163">Description</span></span>                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91153-164">put \_ ProvidesNotifications</span><span class="sxs-lookup"><span data-stu-id="91153-164">put\_ProvidesNotifications</span></span> | <span data-ttu-id="91153-165">如果通訊協定處理常式或其他應用程式將會通知搜尋引擎有關搜尋根目錄下的 Url 變更，則設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="91153-165">Set to **TRUE** if a protocol handler or other application will notify the search engine about changes to the URLs under the search root.</span></span> <span data-ttu-id="91153-166">通知會指出 Url 需要重新編制索引。</span><span class="sxs-lookup"><span data-stu-id="91153-166">The notification indicates that the URLs need reindexing.</span></span> |
| <span data-ttu-id="91153-167">put \_ RootURL</span><span class="sxs-lookup"><span data-stu-id="91153-167">put\_RootURL</span></span>               | <span data-ttu-id="91153-168">設定目前搜尋的根 URL。</span><span class="sxs-lookup"><span data-stu-id="91153-168">Sets the root URL of the current search.</span></span> <span data-ttu-id="91153-169">URL 會採用稍早所述的搜尋根表單。</span><span class="sxs-lookup"><span data-stu-id="91153-169">The URL takes the search root form described earlier.</span></span>                                                                                                      |



 

 

<span data-ttu-id="91153-170">依預設，當您新增搜尋根時，索引子不會將範圍編目。</span><span class="sxs-lookup"><span data-stu-id="91153-170">By default, the indexer does not crawl a scope when you add a search root.</span></span> <span data-ttu-id="91153-171">您也必須為根目錄新增包含規則。</span><span class="sxs-lookup"><span data-stu-id="91153-171">You must also add an include rule for the root.</span></span> <span data-ttu-id="91153-172">如果您想要為應用程式新增使用者專屬的根目錄，則應用程式會在應用程式啟動時，為新的使用者新增適當的根。</span><span class="sxs-lookup"><span data-stu-id="91153-172">If you want to add a user-specific root for an application, that application should add the appropriate roots for new users when the application starts.</span></span>

<span data-ttu-id="91153-173">若要為新使用者新增適當的根目錄：</span><span class="sxs-lookup"><span data-stu-id="91153-173">To add the appropriate roots for new users:</span></span>

1.  <span data-ttu-id="91153-174">取得使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="91153-174">Get the user's SID.</span></span>
2.  <span data-ttu-id="91153-175">列舉所有根目錄，以檢查此 SID 是否有一個。</span><span class="sxs-lookup"><span data-stu-id="91153-175">Enumerate all roots to check whether one exists for this SID.</span></span>
3.  <span data-ttu-id="91153-176">如有必要，請使用 SID 新增根。</span><span class="sxs-lookup"><span data-stu-id="91153-176">Add a new root, using the SID, if necessary.</span></span>

 

## <a name="removing-roots-from-the-crawl-scope"></a><span data-ttu-id="91153-177">從編目範圍中移除根目錄</span><span class="sxs-lookup"><span data-stu-id="91153-177">Removing Roots from the Crawl Scope</span></span>

<span data-ttu-id="91153-178">當您不再想要將該 URL 編制索引時，可以使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 從編目範圍中移除根。</span><span class="sxs-lookup"><span data-stu-id="91153-178">You can use [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) to remove a root from the crawl scope when you no longer want that URL indexed.</span></span> <span data-ttu-id="91153-179">移除根也會刪除該 URL 的所有範圍規則。</span><span class="sxs-lookup"><span data-stu-id="91153-179">Removing a root also deletes all scope rules for that URL.</span></span> <span data-ttu-id="91153-180">例如，假設您想要從系統卸載內容存放區和/或其通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="91153-180">For example, suppose you want to uninstall a content store and/or its protocol handler from a system.</span></span> <span data-ttu-id="91153-181">您可以卸載應用程式、移除所有資料，然後從編目範圍中移除搜尋根，而編目範圍管理員將會移除根目錄以及與根目錄相關聯的所有範圍規則。</span><span class="sxs-lookup"><span data-stu-id="91153-181">You can uninstall the application, remove all data, and then remove the search root from the crawl scope, and the Crawl Scope Manager will remove the root and all scope rules associated with the root.</span></span>

<span data-ttu-id="91153-182">若要移除現有的搜尋根目錄，請使用您想要移除的搜尋根來呼叫 [**ISearchCrawlScopeManager：： RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) 。</span><span class="sxs-lookup"><span data-stu-id="91153-182">To remove an existing search root, call [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) with the search root you want to remove.</span></span> <span data-ttu-id="91153-183">搜尋根目錄 URL 會採用與先前所述搜尋根目錄相同的形式。</span><span class="sxs-lookup"><span data-stu-id="91153-183">The search root URL takes the same form as the search root described earlier.</span></span> <span data-ttu-id="91153-184">如果找不到 \_ 根目錄，這個方法會傳回 FALSE，如果移除找到的根目錄時發生錯誤，則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="91153-184">This method returns S\_FALSE if the root is not found and an error code if there was an error removing a root that was found.</span></span>

<span data-ttu-id="91153-185">移除搜尋根也會從使用者介面移除 Windows Search 選項的 URL，因此使用者可能無法使用使用者介面重新新增該容器或位置。</span><span class="sxs-lookup"><span data-stu-id="91153-185">Removing a search root also removes the URL from the user interface for Windows Search options, so users may not be able to re-add that container or location using the user interface.</span></span> <span data-ttu-id="91153-186">您也可以移除搜尋根目錄的所有使用者設定覆寫，並還原為原始搜尋根目錄和範圍規則。</span><span class="sxs-lookup"><span data-stu-id="91153-186">It is also possible to remove all user-set overrides of a search root and revert to the original search root and scope rules.</span></span> <span data-ttu-id="91153-187">如需詳細資訊，請參閱 [管理領域規則](-search-3x-wds-extidx-csm-scoperules.md)。</span><span class="sxs-lookup"><span data-stu-id="91153-187">For more information, see [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md).</span></span>

> [!Note]  
> <span data-ttu-id="91153-188">在 Windows Vista 中，如果使用者是透過主控台中的使用者設定檔移除，則 CSM 會移除所有規則和根目錄及其 SID，並從目錄中移除其索引項目目。</span><span class="sxs-lookup"><span data-stu-id="91153-188">On Windows Vista, if users are removed through User Profiles in Control Panel, CSM removes all rules and roots with their SID and removes their indexed items from the catalog.</span></span> <span data-ttu-id="91153-189">在 Windows XP 上，您需要手動移除使用者的根和規則。</span><span class="sxs-lookup"><span data-stu-id="91153-189">On Windows XP, you need to remove the users' roots and rules manually.</span></span>

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a><span data-ttu-id="91153-190">列舉編目範圍中的根</span><span class="sxs-lookup"><span data-stu-id="91153-190">Enumerating Roots in the Crawl Scope</span></span>

<span data-ttu-id="91153-191">CSM 會使用標準的 COM 樣式列舉值介面 [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)來列舉搜尋根。</span><span class="sxs-lookup"><span data-stu-id="91153-191">The CSM enumerates search roots using a standard COM-style enumerator interface, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots).</span></span> <span data-ttu-id="91153-192">您可以使用此介面來列舉搜尋根的一些用途。</span><span class="sxs-lookup"><span data-stu-id="91153-192">You can use this interface to enumerate search roots for a number of purposes.</span></span> <span data-ttu-id="91153-193">例如，您可能想要在使用者介面中顯示整個編目範圍，或探索特定根或根項目是否已在編目範圍中。</span><span class="sxs-lookup"><span data-stu-id="91153-193">For example, you might want to display the entire crawl scope in a user interface, or discover whether a particular root or the child of a root is already in the crawl scope.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="91153-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="91153-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="91153-195">**參考**</span><span class="sxs-lookup"><span data-stu-id="91153-195">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91153-196">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="91153-196">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[<span data-ttu-id="91153-197">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="91153-197">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[<span data-ttu-id="91153-198">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="91153-198">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

<span data-ttu-id="91153-199">**概念**</span><span class="sxs-lookup"><span data-stu-id="91153-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="91153-200">使用編目範圍管理員</span><span class="sxs-lookup"><span data-stu-id="91153-200">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[<span data-ttu-id="91153-201">管理範圍規則</span><span class="sxs-lookup"><span data-stu-id="91153-201">Managing Scope Rules</span></span>](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 




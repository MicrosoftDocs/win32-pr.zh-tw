---
description: 安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置，然後透過登錄註冊通訊協定處理常式。
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: " (Windows Search) 安裝和註冊通訊協定處理常式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970146"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="25d69-103"> (Windows Search) 安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="25d69-104">安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置，然後透過登錄註冊通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="25d69-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="25d69-105">安裝應用程式也可以新增搜尋根和範圍規則，以定義 Shell 資料來源的預設編目範圍。</span><span class="sxs-lookup"><span data-stu-id="25d69-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="25d69-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="25d69-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="25d69-107">關於 Url</span><span class="sxs-lookup"><span data-stu-id="25d69-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="25d69-108">執行通訊協定處理常式介面</span><span class="sxs-lookup"><span data-stu-id="25d69-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="25d69-109">ISearchProtocol 和 ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="25d69-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="25d69-110">IUrlAccessor、IUrlAccessor2、IUrlAccessor3 和 IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="25d69-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="25d69-111">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="25d69-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="25d69-112">執行容器的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="25d69-113">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="25d69-114">註冊通訊協定處理常式的指導方針</span><span class="sxs-lookup"><span data-stu-id="25d69-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="25d69-115">註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="25d69-116">註冊通訊協定處理常式的檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="25d69-117">確保您的專案已編制索引</span><span class="sxs-lookup"><span data-stu-id="25d69-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="25d69-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="25d69-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="25d69-119">關於 Url</span><span class="sxs-lookup"><span data-stu-id="25d69-119">About URLs</span></span>

<span data-ttu-id="25d69-120">Windows Search 會使用 Url 來唯一識別 Shell 資料來源階層中的專案。</span><span class="sxs-lookup"><span data-stu-id="25d69-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="25d69-121">階層中第一個節點的 URL 稱為 [搜尋根目錄](-search-3x-wds-extidx-csm-searchroots.md);Windows Search 將在搜尋根目錄開始編制索引，要求通訊協定處理常式列舉每個 URL 的子連結。</span><span class="sxs-lookup"><span data-stu-id="25d69-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="25d69-122">一般的 URL 結構如下：</span><span class="sxs-lookup"><span data-stu-id="25d69-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="25d69-123">下表說明 URL 語法。</span><span class="sxs-lookup"><span data-stu-id="25d69-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="25d69-124">語法</span><span class="sxs-lookup"><span data-stu-id="25d69-124">Syntax</span></span>           | <span data-ttu-id="25d69-125">描述</span><span class="sxs-lookup"><span data-stu-id="25d69-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="25d69-126">識別要為 URL 叫用的通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="25d69-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="25d69-127">{使用者 SID}</span><span class="sxs-lookup"><span data-stu-id="25d69-127">{user SID}</span></span>       | <span data-ttu-id="25d69-128">識別用來呼叫通訊協定處理常式的使用者安全性內容。</span><span class="sxs-lookup"><span data-stu-id="25d69-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="25d69-129">如果找不到 (SID) 的使用者安全識別碼，則會在系統服務的安全性內容中呼叫通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="25d69-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="25d69-130">定義存放區的階層，其中每個正斜線 ( '/' ) 是資料夾名稱之間的分隔符號。</span><span class="sxs-lookup"><span data-stu-id="25d69-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="25d69-131">表示用來識別子專案 (的唯一字串，例如) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="25d69-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="25d69-132">Windows Search 索引子會從 Url 修剪最後一個斜線。</span><span class="sxs-lookup"><span data-stu-id="25d69-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="25d69-133">因此，您無法依賴最後一個斜線來識別目錄，而不是專案。</span><span class="sxs-lookup"><span data-stu-id="25d69-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="25d69-134">您的通訊協定處理常式必須能夠處理此 URL 語法。</span><span class="sxs-lookup"><span data-stu-id="25d69-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="25d69-135">確定您選取用來識別 Shell 資料來源的通訊協定名稱不會與目前的資料來源發生衝突。</span><span class="sxs-lookup"><span data-stu-id="25d69-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="25d69-136">我們建議採用此命名慣例： `companyName.scheme` 。</span><span class="sxs-lookup"><span data-stu-id="25d69-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="25d69-137">如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="25d69-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="25d69-138">執行通訊協定處理常式介面</span><span class="sxs-lookup"><span data-stu-id="25d69-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="25d69-139">建立通訊協定處理常式需要執行下列三個介面：</span><span class="sxs-lookup"><span data-stu-id="25d69-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="25d69-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) 可管理 UrlAccessor 物件。</span><span class="sxs-lookup"><span data-stu-id="25d69-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="25d69-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 可公開屬性，並針對 Shell 資料來源中的專案識別適當的篩選。</span><span class="sxs-lookup"><span data-stu-id="25d69-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="25d69-142">用來篩選專屬檔案或列舉和篩選以階層方式儲存之檔案的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="25d69-143">除了所列的三個強制介面以外，其他介面是選擇性的，而您可以自由地執行任何選用介面最適合用於手邊的工作。</span><span class="sxs-lookup"><span data-stu-id="25d69-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="25d69-144">ISearchProtocol 和 ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="25d69-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="25d69-145">SearchProtocol 介面會初始化並管理您的通訊協定處理常式 UrlAccessor 物件。</span><span class="sxs-lookup"><span data-stu-id="25d69-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="25d69-146">[**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)介面是 [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)的選擇性延伸模組，並且包含額外的方法，可指定使用者和專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="25d69-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="25d69-147">IUrlAccessor、IUrlAccessor2、IUrlAccessor3 和 IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="25d69-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="25d69-148">下表描述 [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 介面。</span><span class="sxs-lookup"><span data-stu-id="25d69-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="25d69-149">介面</span><span class="sxs-lookup"><span data-stu-id="25d69-149">Interface</span></span>                                                 | <span data-ttu-id="25d69-150">描述</span><span class="sxs-lookup"><span data-stu-id="25d69-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25d69-151">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="25d69-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="25d69-152">針對指定的 URL， [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 介面可讓您存取在 URL 中公開之專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="25d69-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="25d69-153">它也可以將這些屬性系結至通訊協定處理常式特定的篩選 (也就是與檔案名相關聯的篩選器，) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="25d69-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (選用) </span><span class="sxs-lookup"><span data-stu-id="25d69-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="25d69-155">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)介面會使用方法來擴充 [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) ，以取得專案的屬性和其顯示 url 的字碼頁，並在 URL 中取得專案類型 (檔或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="25d69-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (選用) </span><span class="sxs-lookup"><span data-stu-id="25d69-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="25d69-157">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3)介面會以取得使用者 sid 陣列的方法擴充 [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) ，讓搜尋通訊協定主機可以模擬這些使用者來為專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="25d69-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="25d69-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (選用) </span><span class="sxs-lookup"><span data-stu-id="25d69-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="25d69-159">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4)介面會使用可識別專案內容是否應該編制索引的方法，擴充 [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3)介面的功能。</span><span class="sxs-lookup"><span data-stu-id="25d69-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="25d69-160">UrlAccessor 物件是由 SearchProtocol 物件具現化並初始化。</span><span class="sxs-lookup"><span data-stu-id="25d69-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="25d69-161">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)介面透過下表所述的方法，提供重要資訊片段的存取權。</span><span class="sxs-lookup"><span data-stu-id="25d69-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="25d69-162">方法</span><span class="sxs-lookup"><span data-stu-id="25d69-162">Method</span></span>                                                                                        | <span data-ttu-id="25d69-163">描述</span><span class="sxs-lookup"><span data-stu-id="25d69-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25d69-164">**IUrlAccessor::GetLastModified**</span><span class="sxs-lookup"><span data-stu-id="25d69-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="25d69-165">傳回上次修改 URL 的時間。</span><span class="sxs-lookup"><span data-stu-id="25d69-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="25d69-166">如果這次比上次索引子處理這個 URL 的時間還新，就會呼叫 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面 (的篩選處理常式，) 呼叫以解壓縮 (可能) 變更該專案的資料。</span><span class="sxs-lookup"><span data-stu-id="25d69-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="25d69-167">系統會忽略目錄的修改時間。</span><span class="sxs-lookup"><span data-stu-id="25d69-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="25d69-168">**IUrlAccessor::IsDirectory**</span><span class="sxs-lookup"><span data-stu-id="25d69-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="25d69-169">識別 URL 是否代表包含子 Url 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="25d69-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="25d69-170">**IUrlAccessor::BindToStream**</span><span class="sxs-lookup"><span data-stu-id="25d69-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="25d69-171">系結至 [IStream 介面](/windows/win32/api/objidl/nn-objidl-istream) ，表示自訂資料存放區中的檔案資料。</span><span class="sxs-lookup"><span data-stu-id="25d69-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="25d69-172">**IUrlAccessor::BindToFilter**</span><span class="sxs-lookup"><span data-stu-id="25d69-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="25d69-173">系結至通訊協定處理常式特定的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)，可公開專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="25d69-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="25d69-174">**IUrlAccessor4::ShouldIndexItemContent**</span><span class="sxs-lookup"><span data-stu-id="25d69-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="25d69-175">識別是否應為專案的內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="25d69-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="25d69-176">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="25d69-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="25d69-177">[**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite)介面是用來具現化篩選器處理常式，此處理程式是在隔離的進程中裝載。</span><span class="sxs-lookup"><span data-stu-id="25d69-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="25d69-178">針對指定的持續性類別識別碼取得適當的篩選處理常式 (CLSID) 、檔儲存類別或副檔名。</span><span class="sxs-lookup"><span data-stu-id="25d69-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="25d69-179">要求主機進程系結至 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的好處是，主機進程可以管理尋找適當篩選處理常式的程式，以及控制呼叫處理常式的相關安全性。</span><span class="sxs-lookup"><span data-stu-id="25d69-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="25d69-180">執行容器的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="25d69-181">如果您要執行階層式通訊協定處理常式，則必須針對列舉子 Url 的容器執行篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="25d69-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="25d69-182">篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="25d69-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="25d69-183">透過 **ifilter 介面的** [**Ifilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)和 [**ifilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)方法，列舉程式是一種迴圈;每個子 URL 都會公開為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="25d69-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="25d69-184">[**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回容器的屬性。</span><span class="sxs-lookup"><span data-stu-id="25d69-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="25d69-185">為了列舉子 Url， **IFilter：： GetChunk** 會傳回下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="25d69-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="25d69-186">[PKEY \_搜尋 \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))：</span><span class="sxs-lookup"><span data-stu-id="25d69-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="25d69-187">專案的 URL，不含上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="25d69-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="25d69-188">[**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 傳回包含子 URL 的 PROPVARIANT。</span><span class="sxs-lookup"><span data-stu-id="25d69-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="25d69-189">[PKEY \_搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)：</span><span class="sxs-lookup"><span data-stu-id="25d69-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="25d69-190">URL 和上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="25d69-190">The URL and the last modified time.</span></span> <span data-ttu-id="25d69-191">[**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 傳回 PROPVARIANT，其中包含子 URL 的向量和上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="25d69-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="25d69-192">傳回 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 會更有效率，因為索引子可以立即判斷是否需要為專案編制索引，而不需要呼叫 [**ISearchProtocol：： CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) 和 [**IUrlAccessor：： GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) 方法。</span><span class="sxs-lookup"><span data-stu-id="25d69-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="25d69-193">下列範例程式碼示範如何傳回 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="25d69-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="25d69-194">Copyright (c) Microsoft Corporation。</span><span class="sxs-lookup"><span data-stu-id="25d69-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="25d69-195">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="25d69-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="25d69-196">容器 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 元件應該一律列舉所有的子 url，即使子 url 未變更，因為索引子會透過列舉進程偵測刪除。</span><span class="sxs-lookup"><span data-stu-id="25d69-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="25d69-197">如果 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 中的日期輸出指出資料尚未變更，則索引子不會更新該 URL 的資料。</span><span class="sxs-lookup"><span data-stu-id="25d69-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="25d69-198">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="25d69-199">安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 [Program Files] 目錄中的適當位置，然後 (s) 註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="25d69-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="25d69-200">通訊協定處理常式應該執行自我註冊以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="25d69-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="25d69-201">安裝應用程式也可以新增搜尋根目錄和範圍規則，以定義 Shell 資料來源的預設編目範圍，以 [確保您的專案會](#ensuring-that-your-items-are-indexed) 在本主題結尾進行索引。</span><span class="sxs-lookup"><span data-stu-id="25d69-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="25d69-202">註冊通訊協定處理常式的指導方針</span><span class="sxs-lookup"><span data-stu-id="25d69-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="25d69-203">註冊通訊協定處理常式時，您應該遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="25d69-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="25d69-204">安裝程式必須使用 EXE 或 MSI 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="25d69-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="25d69-205">必須提供版本資訊。</span><span class="sxs-lookup"><span data-stu-id="25d69-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="25d69-206">每個安裝的增益集都必須建立 [新增/移除程式] 專案。</span><span class="sxs-lookup"><span data-stu-id="25d69-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="25d69-207">安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。</span><span class="sxs-lookup"><span data-stu-id="25d69-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="25d69-208">如果先前的增益集遭到覆寫，安裝程式應通知使用者。</span><span class="sxs-lookup"><span data-stu-id="25d69-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="25d69-209">如果較新的增益集覆寫了先前的增益集，就應該能夠還原先前增益集的功能，並使它成為該檔案類型的預設增益集。</span><span class="sxs-lookup"><span data-stu-id="25d69-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="25d69-210">安裝程式應定義索引子的預設編目範圍，方法是新增搜尋根目錄和使用編目範圍管理員 (CSM) 的範圍規則。</span><span class="sxs-lookup"><span data-stu-id="25d69-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="25d69-211">註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="25d69-212">您必須在登錄中建立14個專案，以註冊通訊協定處理常式元件，其中：</span><span class="sxs-lookup"><span data-stu-id="25d69-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="25d69-213">*Ver \_Ind \_ ProgID* 是通訊協定處理常式執行的獨立 ProgID 版本。</span><span class="sxs-lookup"><span data-stu-id="25d69-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="25d69-214">*Ver \_Dep \_ ProgID* 是通訊協定處理常式執行的版本相依 ProgID。</span><span class="sxs-lookup"><span data-stu-id="25d69-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="25d69-215">*Clsid \_ 1* 是通訊協定處理常式執行的 clsid。</span><span class="sxs-lookup"><span data-stu-id="25d69-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="25d69-216">**註冊通訊協定處理常式：**</span><span class="sxs-lookup"><span data-stu-id="25d69-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="25d69-217">使用下列索引鍵和值註冊版本獨立 ProgID：</span><span class="sxs-lookup"><span data-stu-id="25d69-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="25d69-218">使用下列索引鍵和值註冊版本相依 ProgID：</span><span class="sxs-lookup"><span data-stu-id="25d69-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="25d69-219">使用下列索引鍵和值註冊通訊協定處理常式的 CLSID：</span><span class="sxs-lookup"><span data-stu-id="25d69-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="25d69-220">向 Windows Search 登錄通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="25d69-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="25d69-221">在下列範例中， <Protocol Name> 是通訊協定本身的名稱，例如 file、mapi 等等：</span><span class="sxs-lookup"><span data-stu-id="25d69-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="25d69-222">在 Windows Vista 之前：</span><span class="sxs-lookup"><span data-stu-id="25d69-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="25d69-223">註冊通訊協定處理常式的檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="25d69-224">您必須在登錄中建立兩個專案，以登錄通訊協定處理常式的檔案類型處理常式 (這也稱為 Shell 延伸模組) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="25d69-225">確保您的專案已編制索引</span><span class="sxs-lookup"><span data-stu-id="25d69-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="25d69-226">在您執行通訊協定處理常式之後，您必須指定通訊協定處理常式要編制索引的 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="25d69-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="25d69-227">您可以使用目錄管理員起始重新編制索引 (如需詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md)) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="25d69-228">或者，您也可以使用編目範圍管理員 (CSM) 來設定預設規則，指出您希望索引子進行編目的 Url (如需詳細資訊，請參閱 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md) 和 [管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md)) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="25d69-229">您也可以新增搜尋根目錄 (如需詳細資訊，請參閱 [管理搜尋根](-search-3x-wds-extidx-csm-searchroots.md)) 。</span><span class="sxs-lookup"><span data-stu-id="25d69-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="25d69-230">另一個可用的選項是依照 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)中的索引編制範例中的程式操作。</span><span class="sxs-lookup"><span data-stu-id="25d69-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="25d69-231">[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)介面提供的方法會通知容器的搜尋引擎進行編目及/或監看，以及在編目或監看時要包含或排除的容器底下的專案。</span><span class="sxs-lookup"><span data-stu-id="25d69-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="25d69-232">在 Windows 7 和更新版本中， [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)會以取得版本的 [**ISearchCrawlScopeManager2：： GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion)方法擴充 **ISearchCrawlScopeManager** ，此方法會通知用戶端 CSM 的狀態是否已變更。</span><span class="sxs-lookup"><span data-stu-id="25d69-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25d69-233">相關主題</span><span class="sxs-lookup"><span data-stu-id="25d69-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25d69-234">**概念**</span><span class="sxs-lookup"><span data-stu-id="25d69-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25d69-235">瞭解通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="25d69-236">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="25d69-237">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="25d69-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="25d69-238">新增圖示和快顯功能表</span><span class="sxs-lookup"><span data-stu-id="25d69-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="25d69-239">程式碼範例：通訊協定處理常式的 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="25d69-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="25d69-240">建立通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="25d69-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="25d69-241">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="25d69-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

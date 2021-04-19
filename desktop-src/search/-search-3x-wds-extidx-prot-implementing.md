---
description: 某些應用程式會將它們的專案儲存在資料庫或自訂檔案類型中。
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: 瞭解通訊協定處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970147"
---
# <a name="understanding-protocol-handlers"></a><span data-ttu-id="0101b-103">瞭解通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-103">Understanding Protocol Handlers</span></span>

<span data-ttu-id="0101b-104">某些應用程式會將它們的專案儲存在資料庫或自訂檔案類型中。</span><span class="sxs-lookup"><span data-stu-id="0101b-104">Some applications store their items in databases or custom file types.</span></span> <span data-ttu-id="0101b-105">雖然 Windows Search 可以為檔案的名稱和屬性編制索引，但 Windows 並不知道該檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0101b-105">While Windows Search can index the name and properties of the file, Windows has no knowledge of the content of the file.</span></span> <span data-ttu-id="0101b-106">如此一來，就無法在 Windows Shell 中建立索引或公開這類專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-106">As a result, such items cannot be indexed or exposed in the Windows Shell.</span></span> <span data-ttu-id="0101b-107">藉由建立通訊協定處理常式，您可以讓這些專案可供編制索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-107">By creating a protocol handler you can make these items available for indexing.</span></span> <span data-ttu-id="0101b-108">您也可以為複合檔案格式（例如 .zip 檔案）編制索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-108">You can also index a compound file format such as a .zip file.</span></span>

<span data-ttu-id="0101b-109">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="0101b-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0101b-110">使用通訊協定處理常式編制資料存放區索引</span><span class="sxs-lookup"><span data-stu-id="0101b-110">Indexing Data Stores with Protocol Handlers</span></span>](#indexing-data-stores-with-protocol-handlers)
    -   [<span data-ttu-id="0101b-111">Shell 資料存放區</span><span class="sxs-lookup"><span data-stu-id="0101b-111">Shell Data Stores</span></span>](#shell-data-stores)
    -   [<span data-ttu-id="0101b-112">通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-112">Protocol Handlers</span></span>](#protocol-handlers)
    -   [<span data-ttu-id="0101b-113">篩選和通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-113">Filters and Protocol Handlers</span></span>](#filters-and-protocol-handlers)
-   [<span data-ttu-id="0101b-114">為複合檔案格式編制索引</span><span class="sxs-lookup"><span data-stu-id="0101b-114">Indexing a Compound File Format</span></span>](#indexing-a-compound-file-format)
-   [<span data-ttu-id="0101b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="0101b-115">Related topics</span></span>](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a><span data-ttu-id="0101b-116">使用通訊協定處理常式編制資料存放區索引</span><span class="sxs-lookup"><span data-stu-id="0101b-116">Indexing Data Stores with Protocol Handlers</span></span>

<span data-ttu-id="0101b-117">當使用者需要搜尋舊版資料庫、電子郵件存放區或 Windows Search 不支援的其他資料結構時，您應該先判斷該資料存放區是否已經有通訊協定處理常式，可能與 SharePoint Server 之類的其他應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0101b-117">When users need to search legacy databases, email stores or other data structures that are not supported by Windows Search, you should first determine whether a protocol handler already exists for that data store, perhaps for use with another application such as SharePoint Server.</span></span> <span data-ttu-id="0101b-118">若是如此，您可以在系統上安裝該通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="0101b-118">If so, you can install that protocol handler on the system.</span></span> <span data-ttu-id="0101b-119">Windows Search 通訊協定處理常式會使用與 SharePoint Server 類似的設計規格，而且通常可以交換使用。</span><span class="sxs-lookup"><span data-stu-id="0101b-119">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span>

<span data-ttu-id="0101b-120">如需有關使用 Office SharePoint Server 2007 部署 Search Server 2008 的詳細資訊，請參閱同盟[搜尋 \[ 搜尋伺服器 2008 \] ](/previous-versions/office/bb931109(v=office.14))。</span><span class="sxs-lookup"><span data-stu-id="0101b-120">For more information about Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>

### <a name="shell-data-stores"></a><span data-ttu-id="0101b-121">Shell 資料存放區</span><span class="sxs-lookup"><span data-stu-id="0101b-121">Shell Data Stores</span></span>

<span data-ttu-id="0101b-122">在新檔案格式和資料存放區的協力廠商開發人員之前，您可以讓這些格式和存放區出現在 Windows 檔案總管的查詢結果中，開發人員必須執行 Shell 資料來源。</span><span class="sxs-lookup"><span data-stu-id="0101b-122">Before a third-party developer of new file formats and data stores can get those formats and stores to appear in query results in Windows Explorer, the developer must implement a Shell data source.</span></span> <span data-ttu-id="0101b-123">Shell 資料來源是一種元件，用來擴充 Shell 命名空間，並公開資料存放區中的專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-123">A Shell data source is a component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="0101b-124">資料存放區是資料的儲存機制。</span><span class="sxs-lookup"><span data-stu-id="0101b-124">A data store is a repository of data.</span></span> <span data-ttu-id="0101b-125">資料存放區可公開給 Shell 程式設計模型，作為使用 Shell 資料來源的容器。</span><span class="sxs-lookup"><span data-stu-id="0101b-125">A data store can be exposed to the Shell programming model as a container that uses a Shell data source.</span></span> <span data-ttu-id="0101b-126">您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-126">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span> <span data-ttu-id="0101b-127">通訊協定處理常式會執行以原生格式存取內容來源的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0101b-127">The protocol handler implements the protocol for accessing a content source in its native format.</span></span> <span data-ttu-id="0101b-128">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)和 [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)介面是用來執行自訂的通訊協定處理常式，以展開可編制索引的資料來源。</span><span class="sxs-lookup"><span data-stu-id="0101b-128">The [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) and [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interfaces are used to implement a custom protocol handler to expand the data sources that can be indexed.</span></span>

<span data-ttu-id="0101b-129">如果您希望查詢結果出現在 Windows 檔案總管中，您必須先執行 Shell 資料來源，才能建立通訊協定處理常式來擴充索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-129">If you want the query results to appear in Windows Explorer, you must implement a Shell data source before you can create a protocol handler to extend the index.</span></span> <span data-ttu-id="0101b-130">但是，如果所有查詢都是以程式設計方式 (透過 OLE DB 例如) ，並以應用程式的程式碼（而非 Shell）來解讀，則不一定需要使用 Shell 命名空間。</span><span class="sxs-lookup"><span data-stu-id="0101b-130">However, if all queries will be programmatic (through OLE DB for example) and interpreted by the application's code rather than the Shell, a Shell namespace while still preferred is not strictly required.</span></span>

> [!Note]  
> <span data-ttu-id="0101b-131">Shell 資料來源有時也稱為 Shell 命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="0101b-131">A Shell data source is sometimes known as a Shell namespace extension.</span></span> <span data-ttu-id="0101b-132">處理常式有時也稱為 Shell 擴充或 Shell 擴充處理常式。</span><span class="sxs-lookup"><span data-stu-id="0101b-132">A handler is sometimes known as a Shell extension or a Shell extension handler.</span></span>

 

<span data-ttu-id="0101b-133">如果您想要讓使用者從 Windows 檔案總管中查看其搜尋結果，您必須建立通訊協定處理常式，以及下列一或多個增益集：</span><span class="sxs-lookup"><span data-stu-id="0101b-133">If you want users to view their search results from within Windows Explorer, then you must create a protocol handler and one or more of the following add-ins:</span></span>

-   <span data-ttu-id="0101b-134">快速鍵功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-134">Shortcut menu handler</span></span>
-   <span data-ttu-id="0101b-135">圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-135">Icon handler</span></span>
-   <span data-ttu-id="0101b-136">其他類型的檔處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-136">Some other type of file handler</span></span>

<span data-ttu-id="0101b-137">如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 Windows Search 中的「處理常式總覽」 [作為開發平臺](-search-3x-wds-development-ovr.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-137">For a list of handlers identified by the developer scenario you are trying to achieve, see "Overview of Handlers" in [Windows Search as a Development Platform](-search-3x-wds-development-ovr.md).</span></span> <span data-ttu-id="0101b-138">如需建立處理常式的相關資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能、操作 [功能表](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))和 [檔案類型處理常式](../shell/fa-file-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-138">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [File Type Handlers](../shell/fa-file-extensions.md).</span></span>

### <a name="protocol-handlers"></a><span data-ttu-id="0101b-139">通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-139">Protocol Handlers</span></span>

<span data-ttu-id="0101b-140">如果資料存放區也是容器 (例如檔系統資料夾) ，您必須執行篩選以列舉容器中的 Url。</span><span class="sxs-lookup"><span data-stu-id="0101b-140">If the data store is also a container (such as a file system folder), you must implement a filter to enumerate the URLs in the container.</span></span> <span data-ttu-id="0101b-141">如果資料存放區包含 Windows Search 所支援的其中一種200檔案類型以外的資料或檔案類型，您必須執行篩選來存取和編制存放區中專案內容的索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-141">If the data store contains data or file types other than one of the 200 file types supported by Windows Search, you must implement a filter to access and index the contents of items in the store.</span></span> <span data-ttu-id="0101b-142">Windows Search 使用與 SharePoint 伺服器所使用的通訊協定處理常式和 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 技術類似。</span><span class="sxs-lookup"><span data-stu-id="0101b-142">Windows Search uses protocol handler and [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) technology similar to that used by SharePoint Server.</span></span> <span data-ttu-id="0101b-143">如果您已經在要編制索引的系統上安裝特定存放區和檔案類型的篩選器，Windows Search 可能可以使用現有的介面來為此資料編制索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-143">If you already have filters for a specific store and file type installed on the system being indexed, Windows Search may be able to use the existing interfaces to index this data.</span></span>

<span data-ttu-id="0101b-144">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="0101b-144">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span> <span data-ttu-id="0101b-145">如需篩選處理常式的概念資訊，請參閱 [開發篩選處理常式](-search-ifilter-conceptual.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-145">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>

### <a name="filters-and-protocol-handlers"></a><span data-ttu-id="0101b-146">篩選和通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-146">Filters and Protocol Handlers</span></span>

<span data-ttu-id="0101b-147">通訊協定處理常式會提供資料存放區的 Windows Search 索引子存取權，讓索引子可以編目資料存放區的節點，並將相關資訊解壓縮至索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-147">Protocol handlers give the Windows Search indexer access to data stores, enabling the indexer to crawl the nodes of a data store and extract relevant information to index.</span></span> <span data-ttu-id="0101b-148">例如，Windows Search 會隨附檔案系統存放區的通訊協定處理常式，以及 Microsoft Outlook 資料存放區的某些版本的通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="0101b-148">Windows Search, for example, ships with protocol handlers for file system stores and for some versions of both Microsoft Outlook data stores.</span></span> <span data-ttu-id="0101b-149">為 Outlook 電子郵件編制索引時，通訊協定處理常式會編目一組 Outlook 資料夾中的所有訊息，並從每個訊息和附件中解壓縮資訊。</span><span class="sxs-lookup"><span data-stu-id="0101b-149">When indexing Outlook email, the protocol handler crawls all messages in a set of Outlook folders and extracts information from each message and attachment.</span></span> <span data-ttu-id="0101b-150">這項資訊會傳遞給索引子，以便包含在 Windows Search 目錄中。</span><span class="sxs-lookup"><span data-stu-id="0101b-150">This information is passed to the indexer for inclusion in the Windows Search catalog.</span></span>

<span data-ttu-id="0101b-151">如需目錄管理員和編目範圍管理員 (CSM) 的總覽，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 並 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-151">For overviews of the Catalog Manager and Crawl Scope Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

## <a name="indexing-a-compound-file-format"></a><span data-ttu-id="0101b-152">為複合檔案格式編制索引</span><span class="sxs-lookup"><span data-stu-id="0101b-152">Indexing a Compound File Format</span></span>

<span data-ttu-id="0101b-153">您可以編制複合檔案格式的索引，以便將檔案中的個別專案當作個別結果來傳回。</span><span class="sxs-lookup"><span data-stu-id="0101b-153">A compound file format can be indexed so that individual items in the file can can be returned as individual results.</span></span> <span data-ttu-id="0101b-154">複合檔案格式（例如副檔名為 .zip 的壓縮檔）本質上是資料存放區，因此可視為索引用途。</span><span class="sxs-lookup"><span data-stu-id="0101b-154">A compound file format such as a compressed file with a .zip file name extension is essentially a data store and can be treated as such for indexing purposes.</span></span> <span data-ttu-id="0101b-155">下列範例會在檔案系統命名空間中顯示 .zip 檔案 (FILE://c:/test/test.zip) 其中同時有子資料夾和個別專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-155">The following example displays a .zip file in the file system namespace (FILE://c:/test/test.zip) in which there are both subfolders and individual items.</span></span>

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

<span data-ttu-id="0101b-156">檔案通訊協定處理常式會在透過監視檔案系統變更記錄檔 FILE://c:/test/test.zip 變更時進行探索，並在檔案變更時叫用針對該檔案的 .zip 檔案註冊的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ，但不知道 .zip 檔案本身的內部結構。</span><span class="sxs-lookup"><span data-stu-id="0101b-156">The FILE protocol handler discovers when FILE://c:/test/test.zip changes by monitoring file system change logs, and it will invoke an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registered for .zip files on that file when the file changes, but it has no knowledge of the internal structure of the .zip file itself.</span></span>

<span data-ttu-id="0101b-157">您必須通知索引子，複合檔案格式是資料存放區。</span><span class="sxs-lookup"><span data-stu-id="0101b-157">You must inform the indexer that the compound file format is a data store.</span></span> <span data-ttu-id="0101b-158">您必須針對個別專案編制索引，並將其視為唯一的實體來加以取出。</span><span class="sxs-lookup"><span data-stu-id="0101b-158">It is necessary to do so for individual items to be indexed and retrieved as unique entities.</span></span> <span data-ttu-id="0101b-159">在您執行 Shell 資料來源並執行下列步驟之後，您將會有一個通訊協定處理常式，該處理常式可處理複合檔案格式的資料，並將其公開 (.zip 檔案) 為個別專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-159">After you have implemented a Shell data source and performed the following steps, you will have a protocol handler that can process and expose the data from a compound file format (a .zip file) as individual items.</span></span>

<span data-ttu-id="0101b-160">**若要通知索引子有複合檔案是資料存放區：**</span><span class="sxs-lookup"><span data-stu-id="0101b-160">**To inform the indexer that a compound file is a data store:**</span></span>

1.  <span data-ttu-id="0101b-161">針對可系結至來源檔案的 .zip 檔案，使用 [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) 或 [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) 建立通訊協定處理常式 (。</span><span class="sxs-lookup"><span data-stu-id="0101b-161">Create a protocol handler (using [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) or [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) for .zip files that has the ability bind to the source file.</span></span> <span data-ttu-id="0101b-162">如需詳細資訊，請參閱 [安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-162">For more information, see [Installing and Registering Protocol Handlers](-search-3x-wds-ph-install-registration.md).</span></span>

    <span data-ttu-id="0101b-163">例如，您可以使用 .zip 檔案的轉義路徑作為根資料夾名稱，然後使用階層語法，就像任何其他檔案格式一樣。</span><span class="sxs-lookup"><span data-stu-id="0101b-163">For example, you could use an escaped path to the .zip file as the root folder name and then use a hierarchy syntax like any other file format.</span></span>

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    <span data-ttu-id="0101b-164">使用上述適用于 c： testtest.zip 的範例資料 \\ \\ ，唯一的 url 如下所示。</span><span class="sxs-lookup"><span data-stu-id="0101b-164">Using the above sample data for c:\\test\\test.zip, the unique URLs would be as follows.</span></span> <span data-ttu-id="0101b-165">使用這些 Url 時，通訊協定處理常式具有系結至 .zip 檔案所需的資訊，並且會列舉包含內部檔案的子 Url，使其可由 .doc 和 .txt 篩選器系結和編制索引。</span><span class="sxs-lookup"><span data-stu-id="0101b-165">With these URLs the protocol handler has the information necessary to bind to the .zip file and enumerate the child URLs including the inner files so that they can be bound to and indexed by the .doc and .txt filters.</span></span>

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  <span data-ttu-id="0101b-166">確定您的通訊協定處理常式符合下列兩個條件：</span><span class="sxs-lookup"><span data-stu-id="0101b-166">Ensure that your protocol handler meets the following two conditions:</span></span>
    -   <span data-ttu-id="0101b-167">.Zip 檔案的根目錄 Url 應該會將 PKEY \_ 搜尋 \_ IsClosedDirectory)  (system.string [](../properties/props-system-search-iscloseddirectory.md)發出至根目錄 .Zip 檔案 url 的 url。</span><span class="sxs-lookup"><span data-stu-id="0101b-167">The root URLs for a .zip file should emit PKEY\_Search\_IsClosedDirectory ([System.Search.IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) on the URLs that are the root .zip file URLs.</span></span> <span data-ttu-id="0101b-168">例如，. zip:///FILE:%2f%2f%2fc:%2ftest% 2ftest.zip/應該發出 IsClosedDirectory = **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0101b-168">For example, .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ should emit IsClosedDirectory = **TRUE**.</span></span> <span data-ttu-id="0101b-169">這會告知索引子，如果此 URL 上的日期未變更，則不需要處理任何子系 Url。</span><span class="sxs-lookup"><span data-stu-id="0101b-169">This tells the indexer that if the date on this URL has not changed, it does not need to process any of the child URLs.</span></span>
    -   <span data-ttu-id="0101b-170">該 URL 的每個子 URL 都應發出 PKEY \_ 搜尋 \_ IsFullyContained [](../properties/props-system-search-isfullycontained.md))  (System.string url 的子 url。</span><span class="sxs-lookup"><span data-stu-id="0101b-170">Every child URL for that URL should emit PKEY\_Search\_IsFullyContained ([System.Search.IsFullyContained](../properties/props-system-search-isfullycontained.md)) on the child URLs of the root .zip URL.</span></span> <span data-ttu-id="0101b-171">一般來說，在累加式編目結束時，索引子會將所有未抓取的 Url 視為應刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-171">Normally at the end of an incremental crawl, the indexer treats all unvisited URLs as items that should be deleted.</span></span> <span data-ttu-id="0101b-172">但因為沒有任何變更，所以根本的 .zip 檔案不應該處理根 Url。</span><span class="sxs-lookup"><span data-stu-id="0101b-172">But the root .zip file should not process root URLs because nothing has changed.</span></span> <span data-ttu-id="0101b-173">發出這個屬性為 **TRUE** 時，會告知索引子，如果這個 URL 尚未在遞增編目結束時處理，則不應將其刪除。</span><span class="sxs-lookup"><span data-stu-id="0101b-173">Emitting this property as **TRUE** tells the indexer that if this URL has not been processed at the end of an incremental crawl, it should not be deleted.</span></span> <span data-ttu-id="0101b-174">只有在根項目已變更且未造訪時，才會刪除此專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-174">It will only be deleted if the root item has changed and it is not visited.</span></span>

<span data-ttu-id="0101b-175">Windows Search 必須要有通訊協定的起始頁，才能知道要以累加方式編目的 Url，以及找到的 Url 應該被忽略。</span><span class="sxs-lookup"><span data-stu-id="0101b-175">Windows Search requires a start page for a protocol in order to know what URLs to crawl incrementally and which URLs should be ignored when they are found.</span></span> <span data-ttu-id="0101b-176">但我們無法從每個 .zip 檔案的 URL 開始，因為我們不知道每個 .zip 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="0101b-176">But we can't start with a URL for each .zip file, because we don't know where each .zip file is.</span></span> <span data-ttu-id="0101b-177">因此，.zip 通訊協定處理常式的起始頁 URL 必須能夠列舉所有 .zip 檔案之已轉義路徑根目錄中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="0101b-177">Hence, the .zip protocol handler's start page URL must be able to enumerate everything at the root of the escaped paths of all of the .zip files.</span></span> <span data-ttu-id="0101b-178">這些 .zip 檔案不一定是在 FILE：命名空間中，而且可能是以附件形式指向 .zip 檔案的 MAPI 類型 URL。</span><span class="sxs-lookup"><span data-stu-id="0101b-178">Those .zip files are not necessarily in the FILE: namespace and could be a MAPI type URL that points to a .zip file as an attachment, for example.</span></span>

<span data-ttu-id="0101b-179">**若要將根註冊為起始頁：**</span><span class="sxs-lookup"><span data-stu-id="0101b-179">**To register a root as a start page:**</span></span>

1.  <span data-ttu-id="0101b-180">將 zip:///之類的根目錄註冊為起始頁，如此一來，所有 .zip 檔案就會在那裡開始。</span><span class="sxs-lookup"><span data-stu-id="0101b-180">Register a root such as .zip:/// as a start page so that all .zip files start there, in effect.</span></span> <span data-ttu-id="0101b-181">處理跟 .zip： URL 時，您的通訊協定處理常式應該藉由查詢 Windows Search FileExtension = ".zip" 的所有 Url，來產生要發出的子 Url 清單。</span><span class="sxs-lookup"><span data-stu-id="0101b-181">When processing the root .zip: URL, your protocol handler should generate the list of child URLs to emit by querying Windows Search for all of the URLs with System.FileExtension = ".zip".</span></span>
2.  <span data-ttu-id="0101b-182">請將這些 Url 取消，以移除斜線並將其傳回做為子 Url。</span><span class="sxs-lookup"><span data-stu-id="0101b-182">Escape those URLs to remove the slashes and return them as child URLs.</span></span> <span data-ttu-id="0101b-183">取得您想要之類型的範例查詢可能看起來如下。</span><span class="sxs-lookup"><span data-stu-id="0101b-183">An example query to retrieve the types you want might look as follows.</span></span>

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  <span data-ttu-id="0101b-184">當 Windows Search 定期對您的 zip:///根目錄 URL 執行累加編目時，您必須反映 Windows Search 已經維持的 Url 清單，也就是 .zip Url。</span><span class="sxs-lookup"><span data-stu-id="0101b-184">When Windows Search periodically does an incremental crawl on your .zip:/// root URL, you must reflect back the list of URLs that Windows Search is already maintaining that are .zip URLs.</span></span> <span data-ttu-id="0101b-185">如果在儲存 .zip 檔案的原生存放區中發現刪除，則不會出現在您的列舉中，而且會移除 .zip 中的樹狀結構分支。</span><span class="sxs-lookup"><span data-stu-id="0101b-185">If a deletion is discovered in the native store where the .zip file is stored, it does not appear in your enumeration, and that branch of the tree in the .zip is removed.</span></span>
4.  <span data-ttu-id="0101b-186">若要系結至另一個通訊協定處理常式的 .zip 資料，您應該在理想的情況下，流覽該 URL 的 [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) ，以系結至物件的儲存區，而不是假設它一律為檔案。</span><span class="sxs-lookup"><span data-stu-id="0101b-186">To bind to the .zip data for another protocol handler, you should ideally go through the [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for that URL to bind to the storage of the object, and not assume it is always a file.</span></span> <span data-ttu-id="0101b-187">這樣做可讓您彈性地使用郵件存放區中的附件。</span><span class="sxs-lookup"><span data-stu-id="0101b-187">Doing so affords you the flexibility to work with attachments in mail stores, for example.</span></span>
5.  <span data-ttu-id="0101b-188">發出每個 .zip 檔案的子 Url 時，您應該使用 PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime ([URLTOINDEXWITHMODIFICATIONTIME](../properties/props-system-search-urltoindexwithmodificationtime.md)) 將 PKEY \_ DateModified ([system. DateModified](../properties/props-system-datemodified.md)) 傳遞給實際的 .zip 檔案，讓索引子只會在已變更時才編目 .zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="0101b-188">When emitting child URLs for each .zip file, you should use PKEY\_Search\_UrlToIndexWithModificationTime ([System.Search.UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) to pass PKEY\_DateModified ([System.DateModified](../properties/props-system-datemodified.md)) of the actual .zip file so that the indexer crawls the .zip file only if it has changed.</span></span>

<span data-ttu-id="0101b-189">若要在建立或修改 .zip Url 之後立即建立它們的索引，而不需要等候增量編目來探索其新狀態，您可以自行監視檔案系統是否有 .zip 檔案變更。</span><span class="sxs-lookup"><span data-stu-id="0101b-189">To have your .zip URLs indexed immediately after they are created or modified, and not have to wait for an incremental crawl to discover their new state, you could conceivably monitor the file system yourself for .zip file changes.</span></span> <span data-ttu-id="0101b-190">不過，這種方法對其他資料存放區（例如 MAPI）沒有作用。</span><span class="sxs-lookup"><span data-stu-id="0101b-190">However, such an approach would not work for other data stores such as MAPI.</span></span>

<span data-ttu-id="0101b-191">**若要在建立或修改 .zip url 時進行索引：**</span><span class="sxs-lookup"><span data-stu-id="0101b-191">**To have your .zip urls indexed when they are created or modified:**</span></span>

1.  <span data-ttu-id="0101b-192">針對 .ZIP 檔案類型建立 (和執行 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的篩選) 。</span><span class="sxs-lookup"><span data-stu-id="0101b-192">Create a filter (and implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) for the .zip file type.</span></span> <span data-ttu-id="0101b-193">如需詳細資訊，請參閱 [開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)。</span><span class="sxs-lookup"><span data-stu-id="0101b-193">For more information, see [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).</span></span>
2.  <span data-ttu-id="0101b-194">每次呼叫您的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 實作為時，都是因為已探索或變更該 URL。</span><span class="sxs-lookup"><span data-stu-id="0101b-194">Whenever your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementation is called, it is because that URL has been discovered or changed.</span></span> <span data-ttu-id="0101b-195">然後，透過 [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) 介面產生適用于來源 url 的 .zip url 事件。</span><span class="sxs-lookup"><span data-stu-id="0101b-195">Then, generate an event for the .zip URL appropriate for the source URL, through the [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) interface.</span></span> <span data-ttu-id="0101b-196">這樣做可讓您立即告知索引子有新的資料要編制索引，而不需要等候增量編目。</span><span class="sxs-lookup"><span data-stu-id="0101b-196">Doing so gives you the ability to immediately tell the indexer that there is new data to be indexed without having to wait for the incremental crawl.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0101b-197">相關主題</span><span class="sxs-lookup"><span data-stu-id="0101b-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0101b-198">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-198">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="0101b-199">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-199">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="0101b-200">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="0101b-200">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="0101b-201">新增圖示和快顯功能表</span><span class="sxs-lookup"><span data-stu-id="0101b-201">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="0101b-202">程式碼範例：通訊協定處理常式的 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="0101b-202">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="0101b-203">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-203">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="0101b-204">建立通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="0101b-204">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="0101b-205">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0101b-205">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

---
title: 開發通訊協定處理常式增益集
description: 您可以藉由執行自訂通訊協定處理常式，將 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的資料存放區。
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a8688621f7d2fda653d769c0e1dfdadd240f49
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507915"
---
# <a name="developing-protocol-handler-add-ins"></a><span data-ttu-id="54c4c-103">開發通訊協定處理常式增益集</span><span class="sxs-lookup"><span data-stu-id="54c4c-103">Developing Protocol Handler Add-ins</span></span>

> [!NOTE]
> <span data-ttu-id="54c4c-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="54c4c-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="54c4c-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="54c4c-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="54c4c-106">您可以藉由執行自訂通訊協定處理常式，將 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="54c4c-106">You can extend Microsoft Windows Desktop Search (WDS) to include new data stores by implementing a custom protocol handler.</span></span>

## <a name="indexing-data-stores-with-protocol-handlers"></a><span data-ttu-id="54c4c-107">使用通訊協定處理常式編制資料存放區索引</span><span class="sxs-lookup"><span data-stu-id="54c4c-107">Indexing Data Stores with Protocol Handlers</span></span>

<span data-ttu-id="54c4c-108">資料存放區是一個內容來源 (資料庫系統、目錄、儲存資料的檔案系統) ，而且可由 WDS 索引子進行編目。</span><span class="sxs-lookup"><span data-stu-id="54c4c-108">A data store is a content source (a database system, a directory, a file system) where data is stored and can be crawled by the WDS Indexer.</span></span> <span data-ttu-id="54c4c-109">存放區可以是階層式 (例如資料庫) 或以連結為基礎的 (，例如網站) 。</span><span class="sxs-lookup"><span data-stu-id="54c4c-109">The store can be hierarchical (like a database) or link-based (like a website).</span></span> <span data-ttu-id="54c4c-110">通訊協定處理常式可將 WDS 的索引編制為有系統地編目資料存放區的節點，以解壓縮要包含在索引中的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="54c4c-110">A protocol handler enables indexing applications like WDS to systematically crawl the nodes of a data store to extract relevant information to include in the index.</span></span> <span data-ttu-id="54c4c-111">每個通訊協定處理常式都是用來編制特定資料存放區類型的索引。</span><span class="sxs-lookup"><span data-stu-id="54c4c-111">Each protocol handler is used to index a specific type of data store.</span></span> <span data-ttu-id="54c4c-112">WDS 隨附的通訊協定處理常式適用于檔案系統存放區，以及 Microsoft Outlook 和 Microsoft Outlook Express 資料存放區 (電子郵件存放區。PST 檔案等) 。</span><span class="sxs-lookup"><span data-stu-id="54c4c-112">WDS ships with protocol handlers for file system stores and for both Microsoft Outlook and Microsoft Outlook Express data stores (email stores, .PST files, and so on).</span></span> <span data-ttu-id="54c4c-113">例如，在為 Outlook 電子郵件編制索引時，通訊協定處理常式會將所有資料夾中的所有訊息，從每個訊息和附件提取資訊。</span><span class="sxs-lookup"><span data-stu-id="54c4c-113">When indexing Outlook email, for example, the protocol handler crawls all messages in all folders extracting information from each message and attachment.</span></span> <span data-ttu-id="54c4c-114">這項資訊會傳遞至要包含在 WDS 目錄中的索引子。</span><span class="sxs-lookup"><span data-stu-id="54c4c-114">This information is passed to the Indexer to include in the WDS catalog.</span></span>

<span data-ttu-id="54c4c-115">使用者通常需要搜尋其他資料存放區，例如舊版資料庫、電子郵件存放區或 WDS 不支援的資料結構。</span><span class="sxs-lookup"><span data-stu-id="54c4c-115">Often users need to search other data stores such as legacy databases, email stores or data structures not supported by WDS.</span></span> <span data-ttu-id="54c4c-116">您可以使用或專門針對該資料存放區執行通訊協定處理常式，來擴充 WDS 以編目新的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="54c4c-116">You can extend WDS to crawl a new data store by using or implementing a protocol handler specifically for that data store.</span></span> <span data-ttu-id="54c4c-117">首先，您應該先判斷資料存放區的通訊協定處理常式是否已存在，或許可以與其他應用程式（例如 SharePoint Services）一起使用。</span><span class="sxs-lookup"><span data-stu-id="54c4c-117">First, you should first determine if a protocol handler already exists for your data store, perhaps for use with another application like SharePoint Services.</span></span> <span data-ttu-id="54c4c-118">若是如此，您可以在系統上安裝該通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="54c4c-118">If so, you can install that protocol handler on the system.</span></span> <span data-ttu-id="54c4c-119">但是，如果另一個通訊協定處理常式不存在，則您需要執行一個處理常式。</span><span class="sxs-lookup"><span data-stu-id="54c4c-119">If, however, another protocol handler does not exist, then you need to implement one.</span></span> <span data-ttu-id="54c4c-120">WDS 通訊協定處理常式會使用與 SharePoint 服務相同的設計規格，而且通常可以交換使用。</span><span class="sxs-lookup"><span data-stu-id="54c4c-120">WDS protocol handlers use the same design specifications as SharePoint Services, and they can often be used interchangeably.</span></span>

<span data-ttu-id="54c4c-121">此外，如果資料存放區包含 WDS 所支援的其中一種200檔案類型以外的資料或檔案類型，您也需要執行篩選來存取和編制存放區中專案內容的索引。</span><span class="sxs-lookup"><span data-stu-id="54c4c-121">Furthermore, if the data store contains data or file types other than one of the 200 file types supported by WDS, you also need to implement a filter to access and index the contents of items in the store.</span></span> <span data-ttu-id="54c4c-122">WDS 2.x 使用 SharePoint Services 所使用的通訊協定處理常式和 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)技術。</span><span class="sxs-lookup"><span data-stu-id="54c4c-122">WDS 2.x uses the protocol handler and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)technology used by SharePoint Services.</span></span> <span data-ttu-id="54c4c-123">如果您已經在要編制索引的系統上安裝特定存放區和檔案類型的篩選器，WDS 會使用現有的介面來為此資料編制索引。</span><span class="sxs-lookup"><span data-stu-id="54c4c-123">If you already have filters for a specific store and file type installed on the system being indexed, WDS uses the existing interfaces to index this data.</span></span>

 

## <a name="roadmap-to-adding-new-data-stores"></a><span data-ttu-id="54c4c-124">新增資料存放區的藍圖</span><span class="sxs-lookup"><span data-stu-id="54c4c-124">Roadmap to Adding New Data Stores</span></span>

<span data-ttu-id="54c4c-125">若要擴充 WDS 以編目新的資料存放區，您可以建立通訊協定處理常式，以及下列一或多個增益集：內容功能表處理常式、圖示處理常式和 SearchProtocolOptions 增益集。</span><span class="sxs-lookup"><span data-stu-id="54c4c-125">To extend WDS to crawl new data stores, you can create a protocol handler and one or more of the following add-ins: context menu handler, icon handler and a SearchProtocolOptions add-in.</span></span>

1.  <span data-ttu-id="54c4c-126">建立並註冊資料存放區的多執行緒通訊協定處理常式：</span><span class="sxs-lookup"><span data-stu-id="54c4c-126">Create and register a multithreaded protocol handler for the data store:</span></span>
    -   <span data-ttu-id="54c4c-127">**ISearchProtocol** -此介面會存取通訊協定，並將 URL 對應至 IUrlAccessor。</span><span class="sxs-lookup"><span data-stu-id="54c4c-127">**ISearchProtocol** - This interface accesses a protocol and maps a URL to an IUrlAccessor.</span></span>
    -   <span data-ttu-id="54c4c-128">**IUrlAccessor** -這是用來從內容來源存取專案，並將內容系結至適當篩選的主要介面。</span><span class="sxs-lookup"><span data-stu-id="54c4c-128">**IUrlAccessor** - This is the main interface used for accessing items from the content source and binding the content to appropriate filter.</span></span>
    -   <span data-ttu-id="54c4c-129">**IProtocolHandlerSite** -此介面可用來要求和載入其他篩選。</span><span class="sxs-lookup"><span data-stu-id="54c4c-129">**IProtocolHandlerSite** - This interface is used to request and load additional filters.</span></span>
    -   <span data-ttu-id="54c4c-130">**IFilter** -這個介面會傳回資料夾中每個專案的 URL，做為處理的值屬性。</span><span class="sxs-lookup"><span data-stu-id="54c4c-130">**IFilter** - This interface returns the URL of each item in a folder as value properties for processing.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="54c4c-131">從非階層式資料存放區傳回搜尋結果所需的最少增益集功能，是 ISearchProtocol 和 IUrlAccessor 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="54c4c-131">The minimum add-in functionality needed to return search results from a non-hierarchical data store is an implementation of ISearchProtocol and IUrlAccessor interfaces.</span></span>

     

2.  <span data-ttu-id="54c4c-132">執行 ISearchProtocolOptions 介面，以包含自訂的通訊協定處理常式選項，例如預先定義的起始頁 (s) ：</span><span class="sxs-lookup"><span data-stu-id="54c4c-132">Implement the ISearchProtocolOptions interface to include customized protocol handler options, like predefined start page(s):</span></span>
    -   <span data-ttu-id="54c4c-133">**ISearchProtocolOptions** -此介面會定義要處理的通訊協定處理常式的預設 url、判斷通訊協定處理常式的需求，並判斷指定的系統是否符合需求。</span><span class="sxs-lookup"><span data-stu-id="54c4c-133">**ISearchProtocolOptions** - This interface defines default URLs for the protocol handler to process, determines what the requirements are for a protocol handler, and determines whether the requirements have been met on a given system.</span></span>
3.  <span data-ttu-id="54c4c-134">藉由執行下列介面，擴充 Shell 以包含使用者介面專案，例如內容功能表和檔案特定圖示：</span><span class="sxs-lookup"><span data-stu-id="54c4c-134">Extend Shell to include user interface elements, like context menus and file-specific icons, by implementing the following interfaces:</span></span>
    -   <span data-ttu-id="54c4c-135">**IShellFolder** -這是用來管理資料夾的介面，必須提供新存放區中 URL 的 ICoNtextMenu 和 IExtractIcon 介面。</span><span class="sxs-lookup"><span data-stu-id="54c4c-135">**IShellFolder** - This interface, which is used to manage folders, is required to provide the IContextMenu and IExtractIcon interfaces for a URL in a new store.</span></span>
    -   <span data-ttu-id="54c4c-136">**IPersistFolder** -必須有這個介面，才能指示 Shell 資料夾物件初始化本身。</span><span class="sxs-lookup"><span data-stu-id="54c4c-136">**IPersistFolder** - This interface is required to instruct a Shell folder object to initialize itself.</span></span>
    -   <span data-ttu-id="54c4c-137">**IPersist** ：這個介面會提供物件的類別識別碼 (CLSID) ，而該物件可以持續儲存在系統中。</span><span class="sxs-lookup"><span data-stu-id="54c4c-137">**IPersist** - This interface supplies the class identifier (CLSID) of an object that can be stored persistently in the system.</span></span>
    -   <span data-ttu-id="54c4c-138">**ICoNtextMenu** -此介面會定義 URL 所指向之專案的滑鼠右鍵內容功能表。</span><span class="sxs-lookup"><span data-stu-id="54c4c-138">**IContextMenu** - This interface defines the right-click context menu for an item pointed to by URL.</span></span>
    -   <span data-ttu-id="54c4c-139">**IExtractIcon** -此介面會定義要針對 URL 所指向之專案顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="54c4c-139">**IExtractIcon** - This interface defines the icon to display for an item pointed to by URL.</span></span>
4.  <span data-ttu-id="54c4c-140">執行機制，以通知索引子變更您的資料存放區：</span><span class="sxs-lookup"><span data-stu-id="54c4c-140">Implement a mechanism to notify the Indexer of changes to your data store:</span></span>
    -   <span data-ttu-id="54c4c-141">**ISearchItemsChangedSink** -此介面可讓您的通訊協定處理常式通知索引資料存放區的變更。</span><span class="sxs-lookup"><span data-stu-id="54c4c-141">**ISearchItemsChangedSink** - This interface enables your protocol handler to notify the Index of changes to your data store.</span></span> <span data-ttu-id="54c4c-142">這可確保索引子不會在累加式索引上編目整個存放區，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="54c4c-142">This improves performance by ensuring the Indexer doesn't crawl the entire store on incremental indexes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54c4c-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="54c4c-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="54c4c-144">**參考**</span><span class="sxs-lookup"><span data-stu-id="54c4c-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54c4c-145">執行 WDS 的通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="54c4c-145">Implementing a Protocol Handler for WDS</span></span>](-search-2x-wds-phimplementing.md)
</dt> <dt>

[<span data-ttu-id="54c4c-146">使用 Shell 擴充功能新增圖示、預覽和內容功能表</span><span class="sxs-lookup"><span data-stu-id="54c4c-146">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="54c4c-147">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="54c4c-147">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="54c4c-148">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="54c4c-148">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 
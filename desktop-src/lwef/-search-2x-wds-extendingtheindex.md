---
title: " (舊版 Windows 環境功能擴充索引) "
description: 使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 Windows Search。
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093719"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="081fd-103"> (舊版 Windows 環境功能擴充索引) </span><span class="sxs-lookup"><span data-stu-id="081fd-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="081fd-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="081fd-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="081fd-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="081fd-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="081fd-106">使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 [Windows Search](../search/-search-3x-wds-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="081fd-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="081fd-107">您可以擴充 WDS 來為新檔案類型和資料存放區的內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="081fd-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="081fd-108">目前，WDS 2.x 包含超過200種專案類型的篩選 (包括 HTML、XML 和原始程式碼檔案等純文字專案) ，並使用與 SharePoint 服務相同的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)和通訊協定處理常式技術。</span><span class="sxs-lookup"><span data-stu-id="081fd-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="081fd-109">如果您已針對新的檔案類型安裝篩選器，WDS 可以使用現有的篩選介面來為此資料編制索引。</span><span class="sxs-lookup"><span data-stu-id="081fd-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="081fd-110">WDS 2.x 增益集可讓索引進行資料和資料結構的往返分析，以取得要新增至可搜尋目錄的資訊。</span><span class="sxs-lookup"><span data-stu-id="081fd-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="081fd-111">這些增益集也可以擴充 Windows Shell，將圖示和內容功能表處理常式與新的檔案類型和資料存放區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="081fd-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="081fd-112">若要在 WDS 目錄中包含新的檔案類型，增益集必須執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面。</span><span class="sxs-lookup"><span data-stu-id="081fd-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="081fd-113">若要加入新的資料存放區，增益集必須是通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="081fd-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="081fd-114">如果新的資料存放區包含內嵌檔案或新的檔案類型本身，您也必須撰寫適當的篩選。</span><span class="sxs-lookup"><span data-stu-id="081fd-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="081fd-115">篩選和通訊協定處理常式必須以機器碼撰寫，因為處理所有增益集時，可能發生 CLR 版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="081fd-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="081fd-116">將檔案類型新增至索引</span><span class="sxs-lookup"><span data-stu-id="081fd-116">Adding File Types to the Index</span></span>

<span data-ttu-id="081fd-117">增益集可以擴充 WDS 以建立新的或專屬檔案類型的索引，並將每個新的檔案類型與特定檔案的圖示或內容功能表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="081fd-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="081fd-118">若要這樣做，您可以建立並註冊增益集，以：</span><span class="sxs-lookup"><span data-stu-id="081fd-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="081fd-119">為每個檔案類型執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面，讓 WDS 可以存取和編制檔案類型的文字和中繼資料的索引。</span><span class="sxs-lookup"><span data-stu-id="081fd-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="081fd-120">會執行 **IExtractIcon** 和 **ICoNtextMenu** 介面，以新增圖示和內容功能表，以提供更好的整合和可用性。</span><span class="sxs-lookup"><span data-stu-id="081fd-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="081fd-121">如需有關如何執行篩選的討論，請參閱 [開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)。</span><span class="sxs-lookup"><span data-stu-id="081fd-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="081fd-122">將資料存放區加入至索引</span><span class="sxs-lookup"><span data-stu-id="081fd-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="081fd-123">增益集可以擴充 WDS 來建立新資料存放區的索引，並將檔案與檔案特定的圖示或內容功能表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="081fd-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="081fd-124">若要這樣做，您可以建立並註冊通訊協定處理常式，以：</span><span class="sxs-lookup"><span data-stu-id="081fd-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="081fd-125">會執行 **ISearchProtocol** 和 **IUrlAccessor** 介面，以處理和系結內容來源中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="081fd-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="081fd-126">WDS 會使用 Url 來唯一識別專案，不論這些專案是在檔案系統、類似資料庫的存放區內或在 Web 上。</span><span class="sxs-lookup"><span data-stu-id="081fd-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="081fd-127">會執行 **IPersistFolder** 介面和 **IShellFolder** 介面的部分，以新增圖示和內容功能表，以提供更好的整合和可用性。</span><span class="sxs-lookup"><span data-stu-id="081fd-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="081fd-128">如需有關如何執行通訊協定處理常式的討論，請參閱 [開發通訊協定處理常式](-search-2x-wds-phaddins.md)。</span><span class="sxs-lookup"><span data-stu-id="081fd-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="081fd-129">增益集安裝程式指導方針</span><span class="sxs-lookup"><span data-stu-id="081fd-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="081fd-130">增益集的安裝應遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="081fd-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="081fd-131">安裝程式必須使用 EXE 或 MSI 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="081fd-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="081fd-132">必須提供版本資訊。</span><span class="sxs-lookup"><span data-stu-id="081fd-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="081fd-133">每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。</span><span class="sxs-lookup"><span data-stu-id="081fd-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="081fd-134">安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。</span><span class="sxs-lookup"><span data-stu-id="081fd-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="081fd-135">如果先前的增益集遭到覆寫，安裝程式應通知使用者。</span><span class="sxs-lookup"><span data-stu-id="081fd-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="081fd-136">如果較新的增益集已覆寫先前的增益集，應該可以還原先前增益集的功能，並將它設為該檔案類型的預設增益集，或重新儲存。</span><span class="sxs-lookup"><span data-stu-id="081fd-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="081fd-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="081fd-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="081fd-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="081fd-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="081fd-139">開發 IFilter 增益集</span><span class="sxs-lookup"><span data-stu-id="081fd-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="081fd-140">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="081fd-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="081fd-141">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="081fd-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="081fd-142">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="081fd-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 

---
description: 註冊檔案類型是建立檔案關聯的第一個步驟，這會使該檔案類型 &\# 0034; 已知&\# 0034; 到 Shell。 但是，如果沒有檔案類型處理常式，Shell 就無法從和檔案公開資訊給使用者。
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: 檔案類型處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847915"
---
# <a name="file-type-handlers"></a><span data-ttu-id="75c7b-104">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="75c7b-104">File Type Handlers</span></span>

<span data-ttu-id="75c7b-105">[註冊檔案類型](fa-how-work.md) 是建立檔案關聯的第一個步驟，這會使該檔案類型「知道」至 Shell。</span><span class="sxs-lookup"><span data-stu-id="75c7b-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="75c7b-106">但是，如果沒有檔案類型處理常式，Shell 就無法從和檔案公開資訊給使用者。</span><span class="sxs-lookup"><span data-stu-id="75c7b-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="75c7b-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="75c7b-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="75c7b-108">使檔案類型知道 Shell</span><span class="sxs-lookup"><span data-stu-id="75c7b-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="75c7b-109">檔案類型處理常式描述</span><span class="sxs-lookup"><span data-stu-id="75c7b-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="75c7b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="75c7b-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="75c7b-111">使檔案類型知道 Shell</span><span class="sxs-lookup"><span data-stu-id="75c7b-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="75c7b-112">在下列 Windows 檔案總管的螢幕擷取畫面中，影像檔案 Desert 會出現在 [Shell **圖片** ] 媒體櫃中，而且只會與油漆應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="75c7b-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![顯示 explorer 開啟沒有檔案類型之影像的螢幕擷取畫面](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="75c7b-114">上一個螢幕擷取畫面中的 Desert 已知檔案缺少下列由檔案類型處理常式啟用的功能：</span><span class="sxs-lookup"><span data-stu-id="75c7b-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="75c7b-115">縮圖或預覽</span><span class="sxs-lookup"><span data-stu-id="75c7b-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="75c7b-116">快速鍵功能表中的影像特定動詞，例如：</span><span class="sxs-lookup"><span data-stu-id="75c7b-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="75c7b-117">輪替預覽</span><span class="sxs-lookup"><span data-stu-id="75c7b-117">Rotate Preview</span></span>
    -   <span data-ttu-id="75c7b-118">設定為桌面背景</span><span class="sxs-lookup"><span data-stu-id="75c7b-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="75c7b-119">列印</span><span class="sxs-lookup"><span data-stu-id="75c7b-119">Print</span></span>
-   <span data-ttu-id="75c7b-120">**詳細資料** 窗格中的影像特定屬性，例如：</span><span class="sxs-lookup"><span data-stu-id="75c7b-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="75c7b-121">拍攝日期</span><span class="sxs-lookup"><span data-stu-id="75c7b-121">Date Taken</span></span>
    -   <span data-ttu-id="75c7b-122">標籤</span><span class="sxs-lookup"><span data-stu-id="75c7b-122">Tags</span></span>
    -   <span data-ttu-id="75c7b-123">分級</span><span class="sxs-lookup"><span data-stu-id="75c7b-123">Rating</span></span>
-   <span data-ttu-id="75c7b-124">為檔案文字編制索引</span><span class="sxs-lookup"><span data-stu-id="75c7b-124">Indexing of file text</span></span>

<span data-ttu-id="75c7b-125">在下列螢幕擷取畫面中，相同的檔案 (Desert。已知的) 具有 .jpg 副檔名，也就是具有相關檔案類型處理常式的已註冊檔案類型，因此會顯示縮圖影像和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="75c7b-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![具有已註冊檔案類型和相關檔案類型處理常式的影像](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="75c7b-127">檔案類型處理常式描述</span><span class="sxs-lookup"><span data-stu-id="75c7b-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="75c7b-128">下表列出每個檔案類型處理常式所提供的功能：</span><span class="sxs-lookup"><span data-stu-id="75c7b-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="75c7b-129">處理常式</span><span class="sxs-lookup"><span data-stu-id="75c7b-129">Handler</span></span>                                                      | <span data-ttu-id="75c7b-130">描述</span><span class="sxs-lookup"><span data-stu-id="75c7b-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75c7b-131">快速鍵功能表</span><span class="sxs-lookup"><span data-stu-id="75c7b-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="75c7b-132">快捷方式功能表處理常式（有時稱為內容功能表處理常式）是一種檔案類型處理常式，可將命令新增至現有的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="75c7b-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="75c7b-133">這些處理常式會與特定檔案類型相關聯，並且在每次對檔案類型的成員顯示內容功能表時呼叫。</span><span class="sxs-lookup"><span data-stu-id="75c7b-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="75c7b-134">縮圖</span><span class="sxs-lookup"><span data-stu-id="75c7b-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="75c7b-135">提供影像以表示 Shell 專案的處理常式。</span><span class="sxs-lookup"><span data-stu-id="75c7b-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="75c7b-136">屬性</span><span class="sxs-lookup"><span data-stu-id="75c7b-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="75c7b-137">屬性處理常式，可存取 Windows Search、Windows 檔案總管和其他需要存取屬性之應用程式的專案屬性。</span><span class="sxs-lookup"><span data-stu-id="75c7b-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="75c7b-138">預覽</span><span class="sxs-lookup"><span data-stu-id="75c7b-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="75c7b-139">一個處理常式，可快速產生要在 Windows 檔案總管預覽窗格中顯示之專案的唯讀、簡單視圖。</span><span class="sxs-lookup"><span data-stu-id="75c7b-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="75c7b-140">篩選條件</span><span class="sxs-lookup"><span data-stu-id="75c7b-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="75c7b-141">此為 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行篩選，可掃描檔中的文字和屬性 (也稱為屬性) 。</span><span class="sxs-lookup"><span data-stu-id="75c7b-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="75c7b-142">它會從這些檔中解壓縮文字區塊，篩選出內嵌的格式，並保留文字位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="75c7b-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="75c7b-143">它也會解壓縮值的區塊，這些值是整份檔的屬性，或是檔的定義完善部分。</span><span class="sxs-lookup"><span data-stu-id="75c7b-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="75c7b-144">**IFilter** 提供建立高階應用程式的基礎，例如檔索引子和與應用程式無關的檢視器。</span><span class="sxs-lookup"><span data-stu-id="75c7b-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="75c7b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="75c7b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c7b-146">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="75c7b-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="75c7b-147">檔案類型</span><span class="sxs-lookup"><span data-stu-id="75c7b-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="75c7b-148">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="75c7b-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="75c7b-149">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="75c7b-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="75c7b-150">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="75c7b-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="75c7b-151">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="75c7b-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="75c7b-152">認知類型</span><span class="sxs-lookup"><span data-stu-id="75c7b-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="75c7b-153">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="75c7b-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 

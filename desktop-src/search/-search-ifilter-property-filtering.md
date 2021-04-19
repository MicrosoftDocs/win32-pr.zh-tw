---
description: 您可以使用已註冊的屬性處理常式，或使用針對特定檔案類型註冊的篩選，從專案中解壓縮屬性。 篩選處理常式 (IFilter 介面的執行) 可以用任意數量的方式解讀檔案類型的內容。
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: 從篩選處理常式傳回屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966686"
---
# <a name="returning-properties-from-a-filter-handler"></a><span data-ttu-id="e54e2-104">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="e54e2-104">Returning Properties from a Filter Handler</span></span>

<span data-ttu-id="e54e2-105">您可以使用已註冊的屬性處理常式，或使用針對特定檔案類型註冊的篩選，從專案中解壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-105">Properties are extracted from items using registered property handlers, or using filters registered for specific file types.</span></span> <span data-ttu-id="e54e2-106">篩選處理常式 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行) 可以用任意數量的方式解讀檔案類型的內容。</span><span class="sxs-lookup"><span data-stu-id="e54e2-106">A filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) can interpret the contents of a file type in any number of ways.</span></span>

<span data-ttu-id="e54e2-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="e54e2-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="e54e2-108">屬性篩選</span><span class="sxs-lookup"><span data-stu-id="e54e2-108">Property Filtering</span></span>](#returning-properties-from-a-filter-handler)
  - [<span data-ttu-id="e54e2-109">屬性大小限制</span><span class="sxs-lookup"><span data-stu-id="e54e2-109">Property Size Limitations</span></span>](#property-size-limitations)
- [<span data-ttu-id="e54e2-110">其他資源</span><span class="sxs-lookup"><span data-stu-id="e54e2-110">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="e54e2-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e54e2-111">Related topics</span></span>](#related-topics)

## <a name="property-filtering"></a><span data-ttu-id="e54e2-112">屬性篩選</span><span class="sxs-lookup"><span data-stu-id="e54e2-112">Property Filtering</span></span>

<span data-ttu-id="e54e2-113">下表列出屬性篩選的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="e54e2-113">Best practices for property filtering are listed in the following table.</span></span>

| <span data-ttu-id="e54e2-114">方法</span><span class="sxs-lookup"><span data-stu-id="e54e2-114">Method</span></span>                                                | <span data-ttu-id="e54e2-115">描述</span><span class="sxs-lookup"><span data-stu-id="e54e2-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e54e2-116">**IFilter：： Init**</span><span class="sxs-lookup"><span data-stu-id="e54e2-116">**IFilter::Init**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-init)      | <span data-ttu-id="e54e2-117">傳回 [**IFILTER \_ 旗標**](/windows/win32/api/filter/ne-filter-ifilter_flags) 列舉。</span><span class="sxs-lookup"><span data-stu-id="e54e2-117">Returns the [**IFILTER\_FLAGS**](/windows/win32/api/filter/ne-filter-ifilter_flags) enumeration.</span></span> <span data-ttu-id="e54e2-118">如果此列舉的 *IFILTER \_ 旗標 \_ OLE \_ 屬性* 成員設定為一個，則 Windows Search 會使用 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 和 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 介面介面來列舉和存取外部數值型別屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-118">If the *IFILTER\_FLAGS\_OLE\_PROPERTIES* member of this enumeration is set to one, then Windows Search uses the [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) and [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) interfaces interfaces to enumerate and access external value-type properties.</span></span> |
| [<span data-ttu-id="e54e2-119">**IFilter：： GetChunk**</span><span class="sxs-lookup"><span data-stu-id="e54e2-119">**IFilter::GetChunk**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | <span data-ttu-id="e54e2-120">從具有區塊類型 (文字或值) 、名稱和地區設定的「區塊」中的檔傳回信息。</span><span class="sxs-lookup"><span data-stu-id="e54e2-120">Returns information from a document in "chunks" with chunk type (text or value), name, and locale.</span></span> <span data-ttu-id="e54e2-121">區塊包含一個 document 屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-121">A chunk contains one document property.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="e54e2-122">**IFilter：： GetText**</span><span class="sxs-lookup"><span data-stu-id="e54e2-122">**IFilter::GetText**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | <span data-ttu-id="e54e2-123">從區塊取得文字型別屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-123">Gets a text-type property from a chunk.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e54e2-124">**IFilter：： GetValue**</span><span class="sxs-lookup"><span data-stu-id="e54e2-124">**IFilter::GetValue**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | <span data-ttu-id="e54e2-125">從區塊取得數值型別屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-125">Gets a value-type property from a chunk.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |

<span data-ttu-id="e54e2-126">下圖顯示範例檔。</span><span class="sxs-lookup"><span data-stu-id="e54e2-126">The following illustration shows an example document.</span></span> <span data-ttu-id="e54e2-127">外部實數值型別屬性 `DocTitle` (使用 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 和 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 介面的方法取得) 和內部實數值型別屬性 `Book` (取得作為自訂 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 執行的結果，) 描述整份檔。</span><span class="sxs-lookup"><span data-stu-id="e54e2-127">The external value-type property `DocTitle` (obtained using methods of the [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) and [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) interfaces) and the internal value-type property `Book` (obtained as a result of a custom [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementation) describe the document as a whole.</span></span> <span data-ttu-id="e54e2-128">文字類型屬性 `Contents` 和 `Chapter` 描述檔的內容。</span><span class="sxs-lookup"><span data-stu-id="e54e2-128">The text-type properties `Contents` and `Chapter` describe the content of the document.</span></span> <span data-ttu-id="e54e2-129">處理此檔時，篩選處理常式 (**IFilter** 介面的執行) 識別和解壓縮這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e54e2-129">When processing this document, the filter handler (an implementation of the **IFilter** interface) identifies and extracts these properties.</span></span>

![顯示一般檔元素的圖表](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a><span data-ttu-id="e54e2-131">屬性大小限制</span><span class="sxs-lookup"><span data-stu-id="e54e2-131">Property Size Limitations</span></span>

<span data-ttu-id="e54e2-132">屬性大小有兩個可能的限制：</span><span class="sxs-lookup"><span data-stu-id="e54e2-132">There are two potential limitations to property size:</span></span>

- <span data-ttu-id="e54e2-133">Windows Search 接受每個檔案的資料大小上限。</span><span class="sxs-lookup"><span data-stu-id="e54e2-133">The maximum size of data that Windows Search accepts per file.</span></span>
- <span data-ttu-id="e54e2-134">屬性描述檔案中定義之每個屬性的大小上限。</span><span class="sxs-lookup"><span data-stu-id="e54e2-134">The maximum size per property as defined in the property description file.</span></span>

<span data-ttu-id="e54e2-135">目前，Windows Search 在計算從專案接受的資料量時，不會使用已定義的屬性大小。</span><span class="sxs-lookup"><span data-stu-id="e54e2-135">Currently, Windows Search does not use the defined property size when calculating the amount of data it accepts from an item.</span></span> <span data-ttu-id="e54e2-136">相反地，Windows Search 使用的限制是檔案大小的產品，而 (的檔案 `MaxGrowFactor` 大小 N \* MaxGrowFactor) 從登錄中讀取。</span><span class="sxs-lookup"><span data-stu-id="e54e2-136">Instead, the limit Windows Search uses is the product of the size of the file and the `MaxGrowFactor` (file size N \* MaxGrowFactor) read from the registry.</span></span> <span data-ttu-id="e54e2-137">預設值 `MaxGrowFactor` 為四。</span><span class="sxs-lookup"><span data-stu-id="e54e2-137">The default `MaxGrowFactor` is four.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

<span data-ttu-id="e54e2-138">因此，如果您的檔案類型通常較小，但具有較大的屬性，Windows Search 可能不會接受您要發出的所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="e54e2-138">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="e54e2-139">不過，您可以增加 `MaxGrowFactor` 以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="e54e2-139">However, you can increase the `MaxGrowFactor` to suit your needs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e54e2-140">其他資源</span><span class="sxs-lookup"><span data-stu-id="e54e2-140">Additional Resources</span></span>

- <span data-ttu-id="e54e2-141">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。</span><span class="sxs-lookup"><span data-stu-id="e54e2-141">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="e54e2-142">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="e54e2-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="e54e2-143">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="e54e2-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="e54e2-144">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e54e2-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
- <span data-ttu-id="e54e2-145">如需屬性和屬性處理常式的總覽，以及可用於檔案格式的系統屬性清單，請參閱 [開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)。</span><span class="sxs-lookup"><span data-stu-id="e54e2-145">For an overview of properties and property handlers, and a list of system properties that you can use for your file formats, see [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e54e2-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="e54e2-146">Related topics</span></span>

[<span data-ttu-id="e54e2-147">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-147">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="e54e2-148">關於 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-148">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="e54e2-149">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="e54e2-149">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="e54e2-150">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-150">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="e54e2-151">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-151">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="e54e2-152">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-152">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="e54e2-153">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e54e2-153">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

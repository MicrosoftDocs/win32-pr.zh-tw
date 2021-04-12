---
description: 本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: 屬性處理常式的最佳作法和常見問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5188e66f08f3c6cf449f8bc61feb6aac829d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194847"
---
# <a name="property-handler-best-practices-and-faq"></a><span data-ttu-id="6ec12-103">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="6ec12-103">Property Handler Best Practices and FAQ</span></span>

<span data-ttu-id="6ec12-104">本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6ec12-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="6ec12-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="6ec12-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6ec12-106">最佳作法</span><span class="sxs-lookup"><span data-stu-id="6ec12-106">Best Practices</span></span>](#property-handler-best-practices-and-faq)
    -   [<span data-ttu-id="6ec12-107">覆寫檔案系統屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-107">Overriding File System Properties</span></span>](#overriding-file-system-properties)
    -   [<span data-ttu-id="6ec12-108">以 XML 為基礎的檔案格式儲存屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-108">Storing Properties in XML-based File Formats</span></span>](#storing-properties-in-xml-based-file-formats)
    -   [<span data-ttu-id="6ec12-109">計算的屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-109">Computed Properties</span></span>](#computed-properties)
-   [<span data-ttu-id="6ec12-110">常見問題集</span><span class="sxs-lookup"><span data-stu-id="6ec12-110">Frequently Asked Questions</span></span>](#property-handler-best-practices-and-faq)
-   [<span data-ttu-id="6ec12-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ec12-111">Related topics</span></span>](#related-topics)

## <a name="best-practices"></a><span data-ttu-id="6ec12-112">最佳做法</span><span class="sxs-lookup"><span data-stu-id="6ec12-112">Best Practices</span></span>

<span data-ttu-id="6ec12-113">此處所述的最佳作法提供實用的執行秘訣。</span><span class="sxs-lookup"><span data-stu-id="6ec12-113">The best practices outlined here provide useful implementation tips.</span></span>

### <a name="overriding-file-system-properties"></a><span data-ttu-id="6ec12-114">覆寫檔案系統屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-114">Overriding File System Properties</span></span>

<span data-ttu-id="6ec12-115">檔案系統資料來源會提供檔案的部分屬性，例如：</span><span class="sxs-lookup"><span data-stu-id="6ec12-115">Some properties for files are provided by the file system data source, such as:</span></span>

-   <span data-ttu-id="6ec12-116">PKEY \_ 檔案名</span><span class="sxs-lookup"><span data-stu-id="6ec12-116">PKEY\_FileName</span></span>
-   <span data-ttu-id="6ec12-117">PKEY \_ 延伸模組</span><span class="sxs-lookup"><span data-stu-id="6ec12-117">PKEY\_Extension</span></span>
-   <span data-ttu-id="6ec12-118">PKEY \_ column.modifiedtime</span><span class="sxs-lookup"><span data-stu-id="6ec12-118">PKEY\_ModifiedTime</span></span>

<span data-ttu-id="6ec12-119">一般而言，屬性處理常式無法提供這些屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-119">In general, property handlers cannot provide values for these properties.</span></span> <span data-ttu-id="6ec12-120">不過，在某些情況下，可以根據屬性處理常式所提供的註冊資訊來覆寫這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-120">However, in some cases these properties can be overridden based on registration information provided by the property handler.</span></span> <span data-ttu-id="6ec12-121">屬性處理常式會以要覆寫的屬性名稱填入 **HKEY \_ 類別的 \_ 根** \\ **CLSID** \\ *{handler clsid}* \\ **OverrideFileSystemProperties** 。</span><span class="sxs-lookup"><span data-stu-id="6ec12-121">Property handlers populate **HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{handler clsid}*\\**OverrideFileSystemProperties** with the names of properties that they want to override.</span></span> <span data-ttu-id="6ec12-122">這僅限於系統有知識的下列清單中所顯示的一組固定屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-122">This is limited to a fixed set of properties shown in the following list of which the system has knowledge.</span></span>

<span data-ttu-id="6ec12-123">下列屬性值支援覆寫：</span><span class="sxs-lookup"><span data-stu-id="6ec12-123">Overriding is supported for the following property values:</span></span>

-   [<span data-ttu-id="6ec12-124">System.string</span><span class="sxs-lookup"><span data-stu-id="6ec12-124">System.Kind</span></span>](./props-system-kind.md)
-   [<span data-ttu-id="6ec12-125">System.string</span><span class="sxs-lookup"><span data-stu-id="6ec12-125">System.FileName</span></span>](./props-system-filename.md)
-   [<span data-ttu-id="6ec12-126">System. IsPinnedToNameSpaceTree</span><span class="sxs-lookup"><span data-stu-id="6ec12-126">System.IsPinnedToNameSpaceTree</span></span>](./props-system-ispinnedtonamespacetree.md)
-   [<span data-ttu-id="6ec12-127">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="6ec12-127">System.ItemNameDisplay</span></span>](./props-system-itemnamedisplay.md)
-   [<span data-ttu-id="6ec12-128">System. SFGAOFlags</span><span class="sxs-lookup"><span data-stu-id="6ec12-128">System.SFGAOFlags</span></span>](./props-system-sfgaoflags.md)
-   [<span data-ttu-id="6ec12-129">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="6ec12-129">System.ItemPathDisplay</span></span>](./props-system-itempathdisplay.md)
-   [<span data-ttu-id="6ec12-130">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="6ec12-130">System.ItemPathDisplayNarrow</span></span>](./props-system-itempathdisplaynarrow.md)
-   [<span data-ttu-id="6ec12-131">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="6ec12-131">System.ItemFolderNameDisplay</span></span>](./props-system-itemfoldernamedisplay.md)
-   [<span data-ttu-id="6ec12-132">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="6ec12-132">System.ItemFolderPathDisplay</span></span>](./props-system-itemfolderpathdisplay.md)
-   [<span data-ttu-id="6ec12-133">System. ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="6ec12-133">System.ItemFolderPathDisplayNarrow</span></span>](./props-system-itemfolderpathdisplaynarrow.md)

<span data-ttu-id="6ec12-134">如需所有 Shell 屬性的完整清單，請參閱 [Shell 屬性](./props.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec12-134">For a full list of all Shell properties, see [Shell Properties](./props.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ec12-135">只有在為檔案編制索引時，才會使用覆寫的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-135">The overridden property values are used only when the files are indexed.</span></span> <span data-ttu-id="6ec12-136">因此，從檔案系統資料來源流覽檔案並不會顯示覆寫的值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-136">Thus, browsing files from the file system data source does not reveal the overridden values.</span></span>

 

### <a name="storing-properties-in-xml-based-file-formats"></a><span data-ttu-id="6ec12-137">以 XML 為基礎的檔案格式儲存屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-137">Storing Properties in XML-based File Formats</span></span>

<span data-ttu-id="6ec12-138">有兩個基本選項可用來儲存以 XML 為基礎的檔案格式的屬性：</span><span class="sxs-lookup"><span data-stu-id="6ec12-138">There are two basic options available for storing properties in XML-based file formats:</span></span>

-   <span data-ttu-id="6ec12-139">根據檔的 XML 架構，使用 XML 元素和屬性來儲存每個屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-139">Store each property using XML elements and attributes according to the XML schema of the document.</span></span> <span data-ttu-id="6ec12-140">這種方法比較「XML 易記」。</span><span class="sxs-lookup"><span data-stu-id="6ec12-140">This approach is more "XML friendly".</span></span>
-   <span data-ttu-id="6ec12-141">將整個屬性存放區序列化為記憶體二進位大型物件 (BLOB) ，將 BLOB 轉換為 base64 編碼的字串，然後將該字串儲存在 XML 中。</span><span class="sxs-lookup"><span data-stu-id="6ec12-141">Serialize the entire property store into a memory Binary large object (BLOB), convert the BLOB into a base64-encoded string, and then store that string in the XML.</span></span> <span data-ttu-id="6ec12-142">這是這兩種方法中較簡單的方法，可用來完整提供開啟中繼資料的支援。</span><span class="sxs-lookup"><span data-stu-id="6ec12-142">This is the simpler of the two approaches and can be used to trivially provide support for open metadata.</span></span>

<span data-ttu-id="6ec12-143">某些處理常式可能會結合這些方法，以標準 XML 格式儲存一些重要的值，並將其餘部分儲存在 BLOB 中，例如。</span><span class="sxs-lookup"><span data-stu-id="6ec12-143">Some handlers might combine these approaches, storing some important values in standard XML format and storing the rest in a BLOB, for example.</span></span>

### <a name="computed-properties"></a><span data-ttu-id="6ec12-144">計算的屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-144">Computed Properties</span></span>

<span data-ttu-id="6ec12-145">有些屬性是衍生自檔案的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-145">Some properties are derived from specific attributes of a file.</span></span> <span data-ttu-id="6ec12-146">例如， [system.object](./props-system-image-dimensions.md) 屬性是由影像檔案中影像的實際維度所決定。</span><span class="sxs-lookup"><span data-stu-id="6ec12-146">For example, the [System.Image.Dimensions](./props-system-image-dimensions.md) property is determined by the actual dimensions of the image in an image file.</span></span> <span data-ttu-id="6ec12-147">因為屬性處理常式無法變更這類屬性值，所以會 `isInnate="true"` 在屬性描述中標示它們。</span><span class="sxs-lookup"><span data-stu-id="6ec12-147">Because such property values cannot be changed by the property handler, they are thus marked `isInnate="true"` in the property description.</span></span> <span data-ttu-id="6ec12-148">其他屬性是從特定屬性的一部分或藉由匯總多個屬性的值來計算。</span><span class="sxs-lookup"><span data-stu-id="6ec12-148">Other properties are computed from a part of a specific property or by aggregating the values of multiple properties.</span></span> <span data-ttu-id="6ec12-149">由於這些「計算」屬性的更新會造成「來源」值的變更方式不明確，因此應該在屬性描述中標示計算屬性，或將其 `isInnate="true"` 報告為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6ec12-149">Because updates to these "computed" properties would create ambiguity as to how the "source" values should be changed, computed properties should be marked `isInnate="true"` in the property description or reported as read-only.</span></span> <span data-ttu-id="6ec12-150">第二個選項是藉由指示處理常式 \_ 從 [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)傳回 S FALSE 來提供。</span><span class="sxs-lookup"><span data-stu-id="6ec12-150">The latter option is available by instructing the handler to return S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6ec12-151">常見問題集</span><span class="sxs-lookup"><span data-stu-id="6ec12-151">Frequently Asked Questions</span></span>

<span data-ttu-id="6ec12-152">本節提供有關屬性和屬性處理常式之常見問題的解答，以及伴隨的解答。</span><span class="sxs-lookup"><span data-stu-id="6ec12-152">This section provides answers to frequently asked questions about properties and property handlers, and accompanying answers.</span></span>

-   <span data-ttu-id="6ec12-153">**問題：** 為什麼 Windows Search 索引子載入我的屬性處理常式？</span><span class="sxs-lookup"><span data-stu-id="6ec12-153">**Question:** Why isn't my property handler being loaded by the Windows Search indexer?</span></span>

    <span data-ttu-id="6ec12-154">Windows Search 索引子會以系統服務的形式執行，而且無法載入儲存在使用者設定檔目錄中的 Dll。</span><span class="sxs-lookup"><span data-stu-id="6ec12-154">The Windows Search indexer runs as a system service and cannot load DLLs that are stored in the user profile directory.</span></span> <span data-ttu-id="6ec12-155">如果您要使用 Microsoft Visual Studio 建立和偵錯工具，它會將 DLL 放在您的使用者設定檔中 (，因此索引子) 不會載入它。</span><span class="sxs-lookup"><span data-stu-id="6ec12-155">If you are building and debugging using Microsoft Visual Studio, it will place the DLL in your user profile (and therefore it won't be loaded by the indexer).</span></span> <span data-ttu-id="6ec12-156">若要解決此問題，請將您的 DLL 複製到您的設定檔資料夾外 (例如，將它複製到 **C： \\ Program Files \\ >yourappname**) ，然後在該處進行註冊。</span><span class="sxs-lookup"><span data-stu-id="6ec12-156">To work around this, copy your DLL outside of your profile folder (for example, into **C:\\Program Files\\YourAppName**) and register it there.</span></span>

    <span data-ttu-id="6ec12-157">如需開發屬性處理常式以使用 Windows Search 索引子的特定指引，請參閱 [開發 Windows Search 的屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec12-157">For more specific guidance on developing property handlers to work with the Windows Search indexer, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

-   <span data-ttu-id="6ec12-158">**問題：** 透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 列舉方法可探索哪些屬性？</span><span class="sxs-lookup"><span data-stu-id="6ec12-158">**Question:** Which properties should be discoverable through the [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) enumeration methods?</span></span>

    <span data-ttu-id="6ec12-159">並非所有屬性存放區物件的用戶端都會使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="6ec12-159">Not all clients of property store objects use these methods.</span></span> <span data-ttu-id="6ec12-160">某些用戶端會察覺它們打算直接要求 (PKEY name) 的屬性，或是透過屬性描述清單來接收屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="6ec12-160">Some clients are aware of the properties they plan to request directly (by PKEY name), or receive property information through a property description list.</span></span> <span data-ttu-id="6ec12-161">屬性探索方法會支援其他數個案例。</span><span class="sxs-lookup"><span data-stu-id="6ec12-161">The property discovery methods suppport several other scenarios.</span></span> <span data-ttu-id="6ec12-162">如果屬性不需要參與這些案例，就不需要列舉。</span><span class="sxs-lookup"><span data-stu-id="6ec12-162">If a property does not need to participate in these scenarios, it does not need to be enumerated.</span></span> <span data-ttu-id="6ec12-163">因此，屬性處理常式可以 \_ 針對未透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 方法探索的屬性產生非 VT 空白值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-163">Hence, a property handler can produce a non-VT\_EMPTY value for properties that are not discovered through the [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) methods.</span></span>

    <span data-ttu-id="6ec12-164">不過，若符合下列任一條件，則應該透過這些方法來顯示內容：</span><span class="sxs-lookup"><span data-stu-id="6ec12-164">However, properties should be visible via these methods if any of the following conditions are met:</span></span>

    -   <span data-ttu-id="6ec12-165">**如果屬性已編制索引，使其可供搜尋：** 這表示它包含在 Windows Search 屬性存放區中， (`isColumn = "true"` 以屬性描述架構中的表示，) 或可用於全文檢索搜尋 (`inInvertedIndex = "true"`) 。</span><span class="sxs-lookup"><span data-stu-id="6ec12-165">**If the property is indexed so that it is searchable:** This means it is included in the Windows Search property store (denoted by `isColumn = "true"` in the property description schema) or available for full text searches (`inInvertedIndex = "true"`).</span></span> <span data-ttu-id="6ec12-166">如果沒有這些旗標或沒有屬性描述，則會自動將類型 "string" 的屬性新增至反向索引，以啟用搜尋。</span><span class="sxs-lookup"><span data-stu-id="6ec12-166">In the absence of these flags or the absence of a property description, properties of type "string" will be added automatically to the inverted index to enable searching.</span></span> <span data-ttu-id="6ec12-167">由於已知屬性的清單 (屬性系統中具有已安裝屬性描述的) ， (超過800個屬性) ，因此不會對屬性系統中所註冊的每個屬性詢問每個屬性處理常式是不切實際的。</span><span class="sxs-lookup"><span data-stu-id="6ec12-167">Because the list of known properties (those with installed property descriptions) in the property system is very large (more than 800 properties), it would be impractical to ask every property handler for every property registered in the property system.</span></span> <span data-ttu-id="6ec12-168">相反地，索引程式會列舉其索引之每個專案的屬性處理常式中的相關屬性，並使用列舉屬性的值來建立全文檢索索引。</span><span class="sxs-lookup"><span data-stu-id="6ec12-168">Instead, the indexing process enumerates the relevant properties from the property handler for each item it indexes, and it uses the values of the enumerated properties to build the full text index.</span></span>
    -   <span data-ttu-id="6ec12-169">**如果在專案的屬性集重複時，應該複製屬性：** 若要執行「複製屬性集」函式，來源專案會讓應該複製的屬性透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 方法來顯示。</span><span class="sxs-lookup"><span data-stu-id="6ec12-169">**If the property should be copied when the item's property set is duplicated:** To implement a "copy a property set" function, the source item makes the properties that should be copied visible through the [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) methods.</span></span> <span data-ttu-id="6ec12-170">不需要複製或不需要複製任何意義的屬性，也不應該納入。</span><span class="sxs-lookup"><span data-stu-id="6ec12-170">Properties that do not need to be copied or do not make sense being copied should not be included.</span></span>
    -   <span data-ttu-id="6ec12-171">**如果屬性值不是空的 (VT \_空白) ：** 空白的屬性值對於用戶端來說並不有用。</span><span class="sxs-lookup"><span data-stu-id="6ec12-171">**If the property value is not empty (VT\_EMPTY):** Property values that are empty are not useful for clients.</span></span> <span data-ttu-id="6ec12-172">當用戶端嘗試傳回空的屬性值時， \_ 會傳回 VT 空白的值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-172">When clients attempt to return empty property values, a value of VT\_EMPTY is returned.</span></span> <span data-ttu-id="6ec12-173">因此，不應該列舉具有空白值的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-173">Thus, properties with empty values should not be enumerated.</span></span>
    -   <span data-ttu-id="6ec12-174">**如果叫用 "remove properties" 函式時應移除屬性：** 這項功能的存在是為了保護隱私權;它會透過列舉來探索屬性處理常式中的所有值，並移除每一個選取供使用者移除的值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-174">**If the property should be removed when invoking the "remove properties" function:** This feature exists to protect privacy; it discovers all values from the property handler through enumeration and removes each one selected for removal by the user.</span></span>
        > [!Note]  
        > <span data-ttu-id="6ec12-175">如果處理常式支援固定的架構 (而非開啟的中繼資料) ，則列舉屬性不會傳達特定屬性處理常式支援的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="6ec12-175">Enumerating properties does not communicate the set of properties that a particular property handler supports if the handler supports a fixed schema (and not open metadata).</span></span> <span data-ttu-id="6ec12-176">相反地，這類處理常式應該記錄其所支援的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="6ec12-176">Instead, such handlers should document the set of properties that they support.</span></span>

         

-   <span data-ttu-id="6ec12-177">**問題：** 如何? 知道哪些檔案格式支援開放中繼資料？</span><span class="sxs-lookup"><span data-stu-id="6ec12-177">**Question:** How do I know which file formats support open metadata?</span></span>

    <span data-ttu-id="6ec12-178">如需開啟中繼資料支援的相關資訊，請參閱 [檔案類型](../shell/fa-file-types.md)中的「支援開放中繼資料的檔案類型」。</span><span class="sxs-lookup"><span data-stu-id="6ec12-178">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

-   <span data-ttu-id="6ec12-179">**問題：** 是否可以 \_ 使用屬性處理常式來儲存 VT Null 值？</span><span class="sxs-lookup"><span data-stu-id="6ec12-179">**Question:** Can VT\_NULL values be stored using a property handler?</span></span>

    <span data-ttu-id="6ec12-180">不會。</span><span class="sxs-lookup"><span data-stu-id="6ec12-180">No.</span></span> <span data-ttu-id="6ec12-181">\_ \_ 在 [**IPropertyStore：： GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))和 [**IPropertyStore：： SETVALUE**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))的呼叫上，VT Null 值會轉換成 vt 空白。</span><span class="sxs-lookup"><span data-stu-id="6ec12-181">VT\_NULL values will be converted to VT\_EMPTY on calls to [**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) and [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).</span></span>

-   <span data-ttu-id="6ec12-182">**問題：**[**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype)函數支援哪些日期字串格式？</span><span class="sxs-lookup"><span data-stu-id="6ec12-182">**Question:** Which date string formats are supported by the [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) function?</span></span>

    <span data-ttu-id="6ec12-183">一般而言，表示日期/時間值的屬性應該使用 VT FILETIME 表示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6ec12-183">Generally, properties that represent date/time values should be represented using VT\_FILETIME.</span></span> <span data-ttu-id="6ec12-184">但是，許多資料來源會以字串形式提供此資訊。</span><span class="sxs-lookup"><span data-stu-id="6ec12-184">However, many data sources provide this information in string form.</span></span> <span data-ttu-id="6ec12-185">[**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) helper API 支援將某些字串日期格式強制轉成 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="6ec12-185">The [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) helper API supports coercing some string date formats into [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) values, as shown in the following table.</span></span>

    

    | <span data-ttu-id="6ec12-186">格式</span><span class="sxs-lookup"><span data-stu-id="6ec12-186">Format</span></span>                  | <span data-ttu-id="6ec12-187">Windows Vista、Windows XP 和 Microsoft Windows 桌面搜尋 (WDS) </span><span class="sxs-lookup"><span data-stu-id="6ec12-187">Windows Vista, Windows XP, and Microsoft Windows Desktop Search (WDS)</span></span> | <span data-ttu-id="6ec12-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ec12-188">Windows 7</span></span> | <span data-ttu-id="6ec12-189">備註</span><span class="sxs-lookup"><span data-stu-id="6ec12-189">Notes</span></span>                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6ec12-190">yyyy/mm/dd： hh： mm： ss. uuu</span><span class="sxs-lookup"><span data-stu-id="6ec12-190">yyyy/mm/dd:hh:mm:ss.uuu</span></span> | <span data-ttu-id="6ec12-191">是</span><span class="sxs-lookup"><span data-stu-id="6ec12-191">Yes</span></span>                                                                   | <span data-ttu-id="6ec12-192">是</span><span class="sxs-lookup"><span data-stu-id="6ec12-192">Yes</span></span>       | <span data-ttu-id="6ec12-193">UTCy = year、m = month、d = date、h = hours (24 小時制) 、m = 分鐘、s = 秒、u = 微秒</span><span class="sxs-lookup"><span data-stu-id="6ec12-193">UTC; y=year, m=month, d=date, h=hours (24-hour clock), m=minutes, s=seconds, u=microseconds</span></span>                                                                                                           |
    | <span data-ttu-id="6ec12-194">yyyy-mm-dd-ddThh： mm： ssZ</span><span class="sxs-lookup"><span data-stu-id="6ec12-194">yyyy-mm-ddThh:mm:ssZ</span></span>    | <span data-ttu-id="6ec12-195">否</span><span class="sxs-lookup"><span data-stu-id="6ec12-195">No</span></span>                                                                    | <span data-ttu-id="6ec12-196">是</span><span class="sxs-lookup"><span data-stu-id="6ec12-196">Yes</span></span>       | <span data-ttu-id="6ec12-197">**ISO8601 格式規格** UTC (以 ' Z ' 時區指標表示) ;y = year、m = month、d = date、h = hours (24 小時制) 、m = 分鐘、s = 秒;T ' 是時間部分的分隔符號。</span><span class="sxs-lookup"><span data-stu-id="6ec12-197">**ISO8601 format specification** UTC (denoted by 'Z' time zone indicator); y=year, m=month, d=date, h=hours (24-hour clock), m=minutes, s=seconds; 'T' is a delimiter for the time portion.</span></span><br/> |

    

     

-   <span data-ttu-id="6ec12-198">**問題：** 是否可以建立唯讀屬性處理常式？</span><span class="sxs-lookup"><span data-stu-id="6ec12-198">**Question:** Is it possible to create a read-only property handler?</span></span>

    <span data-ttu-id="6ec12-199">是。</span><span class="sxs-lookup"><span data-stu-id="6ec12-199">Yes.</span></span> <span data-ttu-id="6ec12-200">某些屬性處理常式的執行不支援寫入屬性值。</span><span class="sxs-lookup"><span data-stu-id="6ec12-200">Some property handler implementations do not support writing of property values.</span></span> <span data-ttu-id="6ec12-201">這些屬性處理常式應該會 \_ 傳回 STGM E \_ ACCESSDENIED 呼叫 **IInitializeXXX：： Initialize** 的呼叫，該呼叫會通過 STGM \_ READWRITE 或對 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))的任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="6ec12-201">These property handlers should return STGM\_E\_ACCESSDENIED on calls to **IInitializeXXX::Initialize** that pass STGM\_READWRITE, or on any call to [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).</span></span>

    <span data-ttu-id="6ec12-202">所有以 STGM READ 模式開啟的屬性處理常式 \_ ，都應該 \_ \_ 在呼叫 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))時傳回 STGM E ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="6ec12-202">All property handlers opened in STGM\_READ mode should return STGM\_E\_ACCESSDENIED on calls to [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).</span></span>

-   <span data-ttu-id="6ec12-203">**問題：** 屬性處理常式可以將屬性視為唯讀，即使架構指出該屬性可寫入？</span><span class="sxs-lookup"><span data-stu-id="6ec12-203">**Question:** Can a property handler treat a property as read-only, even if the schema indicates that the property is writeable?</span></span>

    <span data-ttu-id="6ec12-204">是。</span><span class="sxs-lookup"><span data-stu-id="6ec12-204">Yes.</span></span> <span data-ttu-id="6ec12-205">在架構系統中，會將屬性標注為唯讀 (包括具有 `isInnate = "true"`) 或讀取/寫入的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-205">In the schema system, properties are annotated as read-only (including those with `isInnate = "true"`) or read/write.</span></span> <span data-ttu-id="6ec12-206">不支援寫入架構所示之特定屬性的屬性處理常式應為該屬性的 [](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) \_ [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)呼叫執行 IPropertyStoreCapabilities 並傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="6ec12-206">Property handlers that do not support writing a particular property that the schema says should be writeable should implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) and return S\_FALSE on calls to [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) for that property.</span></span> <span data-ttu-id="6ec12-207">這表示在此處理程式和這個檔案的內容中，無法寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec12-207">This indicates that in the context of this handler and this file, the property is not writeable.</span></span>

    > [!Note]  
    > <span data-ttu-id="6ec12-208">無法進行反向動作。</span><span class="sxs-lookup"><span data-stu-id="6ec12-208">The reverse action is not possible.</span></span> <span data-ttu-id="6ec12-209">您無法啟用屬性處理常式來撰寫在架構中標示為唯讀的屬性</span><span class="sxs-lookup"><span data-stu-id="6ec12-209">You cannot enable a property handler to write a property that is marked as read-only in the schema</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="6ec12-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ec12-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec12-211">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="6ec12-211">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="6ec12-212">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="6ec12-212">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="6ec12-213">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="6ec12-213">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="6ec12-214">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="6ec12-214">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="6ec12-215">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="6ec12-215">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> </dl>

 

 

---
description: Microsoft Windows Search 使用屬性處理常式從專案中將屬性值解壓縮，並使用屬性系統架構來決定應該如何編制特定屬性的索引。
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: 開發 Windows Search 的屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191209"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="62632-103">開發 Windows Search 的屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="62632-104">Microsoft Windows Search 使用屬性處理常式從專案中將屬性值解壓縮，並使用屬性系統架構來決定應該如何編制特定屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="62632-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="62632-105">若要讀取和編制屬性值的索引，Windows Search 來叫用跨進程的屬性處理常式，以提升安全性和穩定性。</span><span class="sxs-lookup"><span data-stu-id="62632-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="62632-106">相反地，屬性處理常式會由 Windows 檔案總管在進程中叫用，以讀取和寫入屬性值。</span><span class="sxs-lookup"><span data-stu-id="62632-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="62632-107">本主題會使用 Windows Search 的特定資訊來補充 [屬性系統](../properties/building-property-handlers.md) 主題，並包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="62632-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="62632-108">屬性處理常式的設計決策</span><span class="sxs-lookup"><span data-stu-id="62632-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="62632-109">屬性決策</span><span class="sxs-lookup"><span data-stu-id="62632-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="62632-110">全文檢索支援</span><span class="sxs-lookup"><span data-stu-id="62632-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="62632-111">作業系統 Implementatation 考慮</span><span class="sxs-lookup"><span data-stu-id="62632-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="62632-112">寫入屬性描述檔</span><span class="sxs-lookup"><span data-stu-id="62632-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="62632-113">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="62632-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="62632-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="62632-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="62632-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="62632-116">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="62632-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="62632-117">確保您的專案獲得索引</span><span class="sxs-lookup"><span data-stu-id="62632-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="62632-118">安裝和註冊屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="62632-119">測試和疑難排解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="62632-120">安裝和設定測試</span><span class="sxs-lookup"><span data-stu-id="62632-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="62632-121">針對屬性處理常式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="62632-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="62632-122">使用 System-Supplied 屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="62632-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="62632-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="62632-124">屬性處理常式的設計決策</span><span class="sxs-lookup"><span data-stu-id="62632-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="62632-125">執行屬性處理常式涉及下列步驟：</span><span class="sxs-lookup"><span data-stu-id="62632-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="62632-126">針對您想要支援的屬性做出設計決策。</span><span class="sxs-lookup"><span data-stu-id="62632-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="62632-127">針對尚未存在於屬性系統中的屬性，建立屬性描述 ( propdesc) 檔。</span><span class="sxs-lookup"><span data-stu-id="62632-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="62632-128">執行和測試屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="62632-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="62632-129">安裝和註冊屬性處理常式和屬性描述檔。</span><span class="sxs-lookup"><span data-stu-id="62632-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="62632-130">測試屬性處理常式的安裝和註冊。</span><span class="sxs-lookup"><span data-stu-id="62632-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="62632-131">開始之前，您必須考慮下列設計問題：</span><span class="sxs-lookup"><span data-stu-id="62632-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="62632-132">檔案格式支援哪些屬性（property）？</span><span class="sxs-lookup"><span data-stu-id="62632-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="62632-133">這些屬性是否已存在於系統架構中？</span><span class="sxs-lookup"><span data-stu-id="62632-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="62632-134">我可以使用現有的系統提供的屬性處理常式嗎？</span><span class="sxs-lookup"><span data-stu-id="62632-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="62632-135">哪些屬性可以顯示給終端使用者？</span><span class="sxs-lookup"><span data-stu-id="62632-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="62632-136">使用者可以編輯哪些屬性？</span><span class="sxs-lookup"><span data-stu-id="62632-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="62632-137">全文檢索搜尋是否應該支援來自屬性處理常式或篩選準則？</span><span class="sxs-lookup"><span data-stu-id="62632-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="62632-138">我是否需要支援繼承應用程式？</span><span class="sxs-lookup"><span data-stu-id="62632-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="62632-139">如果是，該如何實行？</span><span class="sxs-lookup"><span data-stu-id="62632-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="62632-140">繼續之前，請參閱 [使用 System-Supplied 屬性處理常式](#using-system-supplied-property-handlers) 來查看您是否可以使用系統提供的屬性處理常式，同時為您節省時間和開發資源。</span><span class="sxs-lookup"><span data-stu-id="62632-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="62632-141">完成這些決策之後，您可以撰寫自訂屬性的正式描述，讓 Windows Search 引擎可以開始編制檔案和屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="62632-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="62632-142">這些正式描述是 XML 檔案，如 [屬性描述架構](/previous-versions//cc144127(v=vs.85))中所述。</span><span class="sxs-lookup"><span data-stu-id="62632-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="62632-143">屬性決策</span><span class="sxs-lookup"><span data-stu-id="62632-143">Property Decisions</span></span>

<span data-ttu-id="62632-144">當考慮要支援哪些屬性時，您應該找出使用者的索引編制和搜尋需求。</span><span class="sxs-lookup"><span data-stu-id="62632-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="62632-145">例如，您可以為您的檔案類型找出100可能有用的屬性，但使用者可能只想要搜尋少數內容。</span><span class="sxs-lookup"><span data-stu-id="62632-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="62632-146">此外，您可能會想要對 Windows 檔案總管中的使用者顯示不同、較大或較小的屬性群組，並允許使用者只編輯顯示的部分屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="62632-147">您的檔案類型可以支援您所定義的任何自訂屬性，以及一組系統定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="62632-148">在您建立自訂屬性之前，請先檢查 [系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) ，以查看您要支援的屬性是否已由系統屬性定義。</span><span class="sxs-lookup"><span data-stu-id="62632-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="62632-149">務必確定您支援最重要的系統定義屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="62632-150">我們建議使用矩陣來協助您設計屬性：</span><span class="sxs-lookup"><span data-stu-id="62632-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="62632-151">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="62632-151">Property name</span></span> | <span data-ttu-id="62632-152">可編制索引嗎？</span><span class="sxs-lookup"><span data-stu-id="62632-152">Is indexable?</span></span> | <span data-ttu-id="62632-153">可顯示嗎？</span><span class="sxs-lookup"><span data-stu-id="62632-153">Is displayable?</span></span> | <span data-ttu-id="62632-154">是否可編輯？</span><span class="sxs-lookup"><span data-stu-id="62632-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="62632-155">property1</span><span class="sxs-lookup"><span data-stu-id="62632-155">property1</span></span>     | <span data-ttu-id="62632-156">Y</span><span class="sxs-lookup"><span data-stu-id="62632-156">Y</span></span>             | <span data-ttu-id="62632-157">Y</span><span class="sxs-lookup"><span data-stu-id="62632-157">Y</span></span>               | <span data-ttu-id="62632-158">N</span><span class="sxs-lookup"><span data-stu-id="62632-158">N</span></span>            |
| <span data-ttu-id="62632-159">財產。。。</span><span class="sxs-lookup"><span data-stu-id="62632-159">property...</span></span>   | <span data-ttu-id="62632-160">Y</span><span class="sxs-lookup"><span data-stu-id="62632-160">Y</span></span>             | <span data-ttu-id="62632-161">Y</span><span class="sxs-lookup"><span data-stu-id="62632-161">Y</span></span>               | <span data-ttu-id="62632-162">N</span><span class="sxs-lookup"><span data-stu-id="62632-162">N</span></span>            |
| <span data-ttu-id="62632-163">propertyn</span><span class="sxs-lookup"><span data-stu-id="62632-163">propertyn</span></span>     | <span data-ttu-id="62632-164">N</span><span class="sxs-lookup"><span data-stu-id="62632-164">N</span></span>             | <span data-ttu-id="62632-165">N</span><span class="sxs-lookup"><span data-stu-id="62632-165">N</span></span>               | <span data-ttu-id="62632-166">N</span><span class="sxs-lookup"><span data-stu-id="62632-166">N</span></span>            |



 

<span data-ttu-id="62632-167">針對上述每個屬性，您必須決定應該擁有哪些屬性，然後在屬性描述 XML 檔案 ( propdesc) 中正式描述這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="62632-168">屬性包含屬性的資料類型、標籤、說明字串等等。</span><span class="sxs-lookup"><span data-stu-id="62632-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="62632-169">針對可編制索引的屬性，您應該特別注意在屬性描述檔的 [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML 元素中找到的下列屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62632-170">屬性</span><span class="sxs-lookup"><span data-stu-id="62632-170">Attribute</span></span></th>
<th><span data-ttu-id="62632-171">描述</span><span class="sxs-lookup"><span data-stu-id="62632-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62632-172">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="62632-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="62632-173">選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-173">Optional.</span></span> <span data-ttu-id="62632-174">指出是否應該將字串屬性值分成單字，並將每個單字儲存在反向索引中。</span><span class="sxs-lookup"><span data-stu-id="62632-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="62632-175">反向索引可讓您有效率地使用 CONTAINS 或 FREETEXT (的屬性值搜尋單字和片語，例如，SELECT .。。其中包含 &quot; sometext &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="62632-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="62632-176">如果設定為 <strong>FALSE</strong>，則會對整個字串執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="62632-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="62632-177">大部分的字串屬性都必須設為 <strong>TRUE</strong>。非字串屬性的值應該設定為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="62632-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="62632-178">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="62632-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62632-179">isColumn</span><span class="sxs-lookup"><span data-stu-id="62632-179">isColumn</span></span></td>
<td><span data-ttu-id="62632-180">選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-180">Optional.</span></span> <span data-ttu-id="62632-181">指出屬性是否應該以資料行的形式儲存在 Windows Search 資料庫中。</span><span class="sxs-lookup"><span data-stu-id="62632-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="62632-182">將屬性儲存為數據行可讓您使用任何述詞來進行抓取、排序、分組和篩選 (也就是在整個資料行值上使用 CONTAINS 或 FREETEXT) 以外的任何述詞。</span><span class="sxs-lookup"><span data-stu-id="62632-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="62632-183">顯示給使用者的屬性應該設定為 [ <strong>TRUE</strong> ]，除非它是非常大的文字屬性 (像是要在反向索引中搜尋之檔) 的主體。</span><span class="sxs-lookup"><span data-stu-id="62632-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="62632-184">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="62632-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62632-185">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="62632-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="62632-186">選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-186">Optional.</span></span> <span data-ttu-id="62632-187">指出如果值為 <strong>Null</strong>時，屬性是否不使用空格。</span><span class="sxs-lookup"><span data-stu-id="62632-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="62632-188">非 sparse 屬性會針對每個專案採用空間，即使值為 <strong>Null</strong>也是一樣。</span><span class="sxs-lookup"><span data-stu-id="62632-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="62632-189">如果屬性是多重值，則這個屬性一律 <strong>為 TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="62632-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="62632-190">只有在每個專案都有值時，這個屬性才會是 <strong>FALSE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="62632-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="62632-191">預設值為 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="62632-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62632-192">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="62632-192">columnIndexType</span></span></td>
<td><span data-ttu-id="62632-193">選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-193">Optional.</span></span> <span data-ttu-id="62632-194">為了優化查詢，Windows Search 引擎可以針對具有 isColumn =<strong>TRUE</strong>的屬性建立次要索引。</span><span class="sxs-lookup"><span data-stu-id="62632-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="62632-195">在編制索引期間，這需要更多處理和磁碟空間，但在查詢期間可改善效能。</span><span class="sxs-lookup"><span data-stu-id="62632-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="62632-196">如果屬性通常會排序、分組或篩選 (也就是使用 =、！ =、<、>，例如，會比對使用者經常) ，則此屬性應該設定為 &quot; OnDisk &quot; 。</span><span class="sxs-lookup"><span data-stu-id="62632-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="62632-197">預設值為 &quot; NotIndexed &quot; 。</span><span class="sxs-lookup"><span data-stu-id="62632-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="62632-198">下列是有效值：</span><span class="sxs-lookup"><span data-stu-id="62632-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="62632-199">NotIndexed：未建立次要索引。</span><span class="sxs-lookup"><span data-stu-id="62632-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="62632-200">OnDisk：在磁片上建立並儲存次要索引。</span><span class="sxs-lookup"><span data-stu-id="62632-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62632-201">maxSize</span><span class="sxs-lookup"><span data-stu-id="62632-201">maxSize</span></span></td>
<td><span data-ttu-id="62632-202">選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-202">Optional.</span></span> <span data-ttu-id="62632-203">指出儲存在 Windows 搜尋資料庫中的屬性值所允許的大小上限。</span><span class="sxs-lookup"><span data-stu-id="62632-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="62632-204">這項限制適用于向量的 indvidual 元素，而不是整個向量。</span><span class="sxs-lookup"><span data-stu-id="62632-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="62632-205">超出此大小的值會被截斷。</span><span class="sxs-lookup"><span data-stu-id="62632-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="62632-206">預設值為 &quot; 128 &quot; (bytes) 。</span><span class="sxs-lookup"><span data-stu-id="62632-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="62632-207">目前，Windows Search 在計算從檔案接受的資料量時，不會使用 maxSize。</span><span class="sxs-lookup"><span data-stu-id="62632-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="62632-208">相反地，Windows Search 使用的限制是檔案大小的產品，而 MaxGrowFactor (檔案大小 N \* MaxGrowFactor) 從登錄的 HKEY_LOCAL_MACHINE >軟體 >>Windows Search >>。</span><span class="sxs-lookup"><span data-stu-id="62632-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="62632-209">預設 MaxGrowFactor 為四個 (4) 。</span><span class="sxs-lookup"><span data-stu-id="62632-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="62632-210">因此，如果您的檔案類型通常較小，但具有較大的屬性，Windows Search 可能不會接受您要發出的所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="62632-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="62632-211">不過，您可以增加 MaxGrowFactor 以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="62632-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="62632-212">在 columnIndexType 屬性中，更快速的查詢優點需要針對次要索引可能產生的較高索引時間和空間成本進行權衡。</span><span class="sxs-lookup"><span data-stu-id="62632-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="62632-213">不過，此成本只會針對具有非 **null** 值的專案付費，因此大部分屬性都可以將此屬性設定為 "OnDisk"。</span><span class="sxs-lookup"><span data-stu-id="62632-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="62632-214">全文檢索支援</span><span class="sxs-lookup"><span data-stu-id="62632-214">Full-Text Support</span></span>

<span data-ttu-id="62632-215">一般來說，稱為 [篩選器](-search-3x-wds-extidx-filters.md)的元件支援全文檢索搜尋;不過，對於以非使用檔案格式的文字型檔案類型而言，屬性處理常式可能會以較少的開發工作來提供此功能。</span><span class="sxs-lookup"><span data-stu-id="62632-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="62632-216">您應參閱 [全文檢索內容](../properties/building-property-handlers-property-handlers.md) 一節，以取得篩選和屬性處理常式功能的比較，以協助您決定最適合您的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="62632-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="62632-217">特別重要的是，篩選器可以處理多個語言程式碼識別碼 (Lcid) 每個檔案，而屬性處理常式則無法處理。</span><span class="sxs-lookup"><span data-stu-id="62632-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="62632-218">由於屬性處理常式無法以篩選器的方式來將內容區塊，因此大型檔案 (即使它們是簡單的檔案格式) 必須完全載入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="62632-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="62632-219">作業系統 Implementatation 考慮</span><span class="sxs-lookup"><span data-stu-id="62632-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="62632-220">Windows 7 的執行資訊</span><span class="sxs-lookup"><span data-stu-id="62632-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="62632-221">在 Windows 7 和更新版本中，註冊屬性處理常式、 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)或新的擴充功能時，會有新的行為。</span><span class="sxs-lookup"><span data-stu-id="62632-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="62632-222">當安裝新的屬性處理常式和（或） **IFilter** 時，會自動重新建立索引具有對應副檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="62632-223">在 Windows 7 中，建議您將 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 與其對應的屬性處理常式一起安裝，並在屬性處理常式之前註冊 **ifilter** 。</span><span class="sxs-lookup"><span data-stu-id="62632-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="62632-224">註冊屬性處理常式時，會立即開始重新編制先前索引檔案的索引，而不需要重新開機，而且會利用任何先前註冊的 IFilter (s) 來進行內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="62632-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="62632-225">如果只安裝了 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) （沒有對應的屬性處理常式），則會在重新開機索引服務或系統重新開機之後，自動重新建立索引。</span><span class="sxs-lookup"><span data-stu-id="62632-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="62632-226">如需 Windows 7 特有的屬性描述旗標，請參閱下列參考主題：</span><span class="sxs-lookup"><span data-stu-id="62632-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="62632-227">GETPROPERTYSTOREFLAGS</span><span class="sxs-lookup"><span data-stu-id="62632-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="62632-228">PROPDESC \_ COLUMNINDEX \_ 類型</span><span class="sxs-lookup"><span data-stu-id="62632-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="62632-229">PROPDESC \_ SEARCHINFO \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="62632-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="62632-230">Windows Vista 及更早版本的執行資訊</span><span class="sxs-lookup"><span data-stu-id="62632-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="62632-231">在 Windows Vista 之前，篩選器提供了剖析和列舉檔案內容和屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="62632-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="62632-232">隨著屬性系統的推出，屬性處理常式會在篩選處理檔案內容時，處理檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="62632-233">針對 Windows Vista，您只需要在與屬性處理常式協調的情況下開發 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的部分執行，如在 [Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)所述。</span><span class="sxs-lookup"><span data-stu-id="62632-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="62632-234">雖然屬性系統也隨附于 Windows XP 的 Windows Search 安裝，但協力廠商和繼承應用程式可能會要求篩選器同時處理內容和屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="62632-235">因此，如果您是在 Windows XP 平臺上進行開發，則應該提供完整的篩選器，以及檔案類型或自訂屬性的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="62632-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="62632-236">寫入屬性描述檔</span><span class="sxs-lookup"><span data-stu-id="62632-236">Writing Property Description Files</span></span>

<span data-ttu-id="62632-237">Propdesc) 屬性描述 ( XML 檔案的結構會在 [propertyDescription](../properties/propdesc-schema-propertydescription.md) 主題中說明。</span><span class="sxs-lookup"><span data-stu-id="62632-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="62632-238">搜尋的特殊興趣是 [searchInfo](../properties/propdesc-schema-searchinfo.md) 元素的屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="62632-239">一旦決定要支援哪些屬性之後，您必須為每個屬性建立並註冊屬性描述檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="62632-240">當您註冊 propdesc 檔案時，這些檔案會包含在架構的屬性描述清單中，並成為搜尋引擎屬性存放區中的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="62632-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="62632-241">您可以使用 [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) 函式（呼叫架構子系統的 IPropertySystem：： RegisterPropertySchema 的包裝函式 API）來註冊自訂屬性描述。</span><span class="sxs-lookup"><span data-stu-id="62632-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="62632-242">此函式會通知架構子系統新增屬性描述架構 (. propdesc) 檔案，使用檔案路徑 (s) 至本機電腦上 (的 propdesc 檔案，通常是應用程式在 [Program Files] 下的安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="62632-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="62632-243">一般而言，安裝程式或應用程式 (例如，您的屬性處理常式安裝程式) 會在安裝 propdesc 檔 (s) 之後，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="62632-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="62632-244">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-244">Implementing Property Handlers</span></span>

<span data-ttu-id="62632-245">開發屬性處理常式牽涉到執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="62632-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="62632-246">IInitialzeWithStream：為您的屬性處理常式提供以資料流程為基礎的初始化。</span><span class="sxs-lookup"><span data-stu-id="62632-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="62632-247">IPropertyStore：列舉、取得和設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="62632-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="62632-248">IPropertyStoreCapabilities：選擇性。</span><span class="sxs-lookup"><span data-stu-id="62632-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="62632-249">識別使用者是否可以從使用者介面編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="62632-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="62632-250">IInitializeWithStream</span></span>

<span data-ttu-id="62632-251">如 [屬性系統](../properties/building-property-handlers.md) 主題所述，我們強烈建議使用 **IInitializeWithStream** 執行屬性處理常式，以執行以資料流程為基礎的初始化。</span><span class="sxs-lookup"><span data-stu-id="62632-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="62632-252">如果您選擇不執行 IInitializeWithStream，屬性處理常式必須在屬性處理常式的登錄機碼上設定 DisableProcessIsolation 旗標，以選擇不在隔離程式中執行。</span><span class="sxs-lookup"><span data-stu-id="62632-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="62632-253">停用進程隔離通常僅適用于舊版的屬性處理常式，而任何新的程式碼都應避免 strenuously。</span><span class="sxs-lookup"><span data-stu-id="62632-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="62632-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="62632-254">IPropertyStore</span></span>

<span data-ttu-id="62632-255">若要建立屬性處理常式，您必須使用下列方法來執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面。</span><span class="sxs-lookup"><span data-stu-id="62632-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="62632-256">方法</span><span class="sxs-lookup"><span data-stu-id="62632-256">Method</span></span>   | <span data-ttu-id="62632-257">描述</span><span class="sxs-lookup"><span data-stu-id="62632-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="62632-258">Commit</span><span class="sxs-lookup"><span data-stu-id="62632-258">Commit</span></span>   | <span data-ttu-id="62632-259">將屬性變更儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="62632-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="62632-260">GetAt</span></span>    | <span data-ttu-id="62632-261">從專案的屬性陣列抓取屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="62632-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="62632-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="62632-262">GetCount</span></span> | <span data-ttu-id="62632-263">取得附加至檔案的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="62632-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="62632-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="62632-264">GetValue</span></span> | <span data-ttu-id="62632-265">捕獲特定屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="62632-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="62632-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="62632-266">SetValue</span></span> | <span data-ttu-id="62632-267">設定新的屬性值，或取代或移除現有的值。</span><span class="sxs-lookup"><span data-stu-id="62632-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="62632-268">[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)檔中包含執行此介面的重要考慮。</span><span class="sxs-lookup"><span data-stu-id="62632-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="62632-269">如果您的屬性處理常式針對指定的專案發出相同屬性的多個值，則只會將最後發出的值儲存在目錄中。</span><span class="sxs-lookup"><span data-stu-id="62632-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="62632-270">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="62632-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="62632-271">屬性處理常式可以選擇性地執行此介面，以停用使用者編輯特定屬性的能力。</span><span class="sxs-lookup"><span data-stu-id="62632-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="62632-272">這些屬性通常可在 [詳細資料] 頁面和窗格中編輯，但在 [執行] 屬性處理常式下不允許編輯這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="62632-273">正確地執行此介面可提供比替代程式更好的使用者體驗，這是來自 Shell 的簡單執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="62632-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="62632-274">確保您的專案獲得索引</span><span class="sxs-lookup"><span data-stu-id="62632-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="62632-275">既然您已完成屬性處理常式，您會想要確定您的處理常式已註冊為取得索引的專案。</span><span class="sxs-lookup"><span data-stu-id="62632-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="62632-276">您可以使用 [目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 來起始重新建立索引，也可以使用 [編目範圍管理員](-search-3x-wds-extidx-csm.md) 設定預設規則，指出您想要讓索引子編目的 url。</span><span class="sxs-lookup"><span data-stu-id="62632-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="62632-277">另一個選項是遵循 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)中的重新索引程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="62632-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="62632-278">如需詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 和 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。</span><span class="sxs-lookup"><span data-stu-id="62632-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="62632-279">安裝和註冊屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="62632-280">在實作為屬性處理常式的情況下，必須註冊它以及與處理常式相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="62632-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="62632-281">下列範例會顯示執行此動作所需的登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="62632-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="62632-282">測試和疑難排解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="62632-283">下列清單提供您應該執行的測試類型的建議：</span><span class="sxs-lookup"><span data-stu-id="62632-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="62632-284">測試是否從檔案類型所支援的每個單一屬性取得輸出。</span><span class="sxs-lookup"><span data-stu-id="62632-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="62632-285">例如，使用大屬性值（例如，在 HTML 檔案中使用大型 metatag）。</span><span class="sxs-lookup"><span data-stu-id="62632-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="62632-286">從屬性處理常式取得輸出之後，或使用像是在列舉檔案屬性之前和之後的 oh.exe 之類的工具，檢查屬性處理常式是否未洩漏檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="62632-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="62632-287">測試與屬性處理常式相關聯的所有檔案類型。</span><span class="sxs-lookup"><span data-stu-id="62632-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="62632-288">例如，請檢查 HTML 篩選準則是否適用 .htm 和 .html 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="62632-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="62632-289">使用損毀的檔案進行測試。</span><span class="sxs-lookup"><span data-stu-id="62632-289">Test with corrupted files.</span></span> <span data-ttu-id="62632-290">屬性處理常式應該會正常失敗。</span><span class="sxs-lookup"><span data-stu-id="62632-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="62632-291">如果應用程式支援加密，請測試屬性處理常式是否未輸出加密文字。</span><span class="sxs-lookup"><span data-stu-id="62632-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="62632-292">如果您的屬性處理常式支援全文檢索搜尋：</span><span class="sxs-lookup"><span data-stu-id="62632-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="62632-293">在檔案內容中使用多個特殊的 Unicode 字元，並測試其輸出。</span><span class="sxs-lookup"><span data-stu-id="62632-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="62632-294">測試非常大型檔的處理，以確保屬性處理常式能如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="62632-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="62632-295">安裝和設定測試</span><span class="sxs-lookup"><span data-stu-id="62632-295">Installation and Setup Tests</span></span>

<span data-ttu-id="62632-296">最後，您需要測試安裝和卸載常式。</span><span class="sxs-lookup"><span data-stu-id="62632-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="62632-297">安裝必須從失敗的安裝復原 (例如，從取消並重新啟動安裝) 。</span><span class="sxs-lookup"><span data-stu-id="62632-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="62632-298">卸載必須刪除與屬性處理常式相關聯的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="62632-299">卸載不能刪除與屬性處理常式安裝相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="62632-300">卸載時，與屬性處理常式相關聯的登錄機碼必須移除。</span><span class="sxs-lookup"><span data-stu-id="62632-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="62632-301">即使已從安裝目錄中刪除檔案，也必須使用卸載。</span><span class="sxs-lookup"><span data-stu-id="62632-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="62632-302">針對屬性處理常式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="62632-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="62632-303">以下是開發屬性處理常式時所做的一些常見錯誤：</span><span class="sxs-lookup"><span data-stu-id="62632-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="62632-304">在使用者目錄下安裝 propdesc 檔案或 Dll。</span><span class="sxs-lookup"><span data-stu-id="62632-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="62632-305">使用相對路徑註冊元件。</span><span class="sxs-lookup"><span data-stu-id="62632-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="62632-306">在 HKEY CURRENT USER 下註冊元件 \_ \_ ，而不是在 HKEY \_ 本機電腦上註冊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="62632-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="62632-307">忘記為非資料流程處理常式設定 DisableProcessIsolation。</span><span class="sxs-lookup"><span data-stu-id="62632-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="62632-308">將測試檔案放在未編制索引的位置。</span><span class="sxs-lookup"><span data-stu-id="62632-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="62632-309">如果您在取得屬性處理常式時遇到問題，以下是一些可協助您進行疑難排解的秘訣：</span><span class="sxs-lookup"><span data-stu-id="62632-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="62632-310">確認 ( 的屬性描述) 標記為 isColumn = "**true**"、isViewable = "**True**" 和 isQueryable = "**true**"。</span><span class="sxs-lookup"><span data-stu-id="62632-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="62632-311">確認您的 propdesc 檔案位於全域位置。</span><span class="sxs-lookup"><span data-stu-id="62632-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="62632-312">確認您已使用絕對路徑註冊您的 propdesc 檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="62632-313">確認事件記錄檔未記錄 propdesc 檔案的註冊失敗。</span><span class="sxs-lookup"><span data-stu-id="62632-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="62632-314">確認您的 Dll 位於全域位置 (而不是在您的使用者設定檔) 。</span><span class="sxs-lookup"><span data-stu-id="62632-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="62632-315">確認 Dll 已在 HKEY \_ 本機 \_ 電腦 \\ 軟體類別下註冊 \\ 。</span><span class="sxs-lookup"><span data-stu-id="62632-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="62632-316">請確認您的 Dll 是使用完整路徑註冊 (或 REG 會 \_ \_ 使用系統帳戶) 已知的環境變數，展開擴充至絕對路徑的 SZ 字串。</span><span class="sxs-lookup"><span data-stu-id="62632-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="62632-317">確認您的屬性處理常式在 Windows 檔案總管下運作。</span><span class="sxs-lookup"><span data-stu-id="62632-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="62632-318">雖然我們建議使用 IInitializeWithStream，但如果您必須使用 IInitializeWithFile 或 IInitializeWithItem，請確認您指定的是 DisableProcessIsolation。</span><span class="sxs-lookup"><span data-stu-id="62632-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="62632-319">確認 [索引選項主控台] 將您的檔案類型列為已編制索引的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="62632-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="62632-320">確認測試檔案位於索引位置。</span><span class="sxs-lookup"><span data-stu-id="62632-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="62632-321">確認自您安裝屬性處理常式之後，已修改過測試檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="62632-322">如果您的測試檔案位於索引位置，而索引子已經將該位置編目，您需要以某種方式修改檔案，以觸發檔案的重新編制索引。</span><span class="sxs-lookup"><span data-stu-id="62632-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="62632-323">使用 System-Supplied 屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="62632-324">Windows 包含許多系統提供的屬性處理常式，如果您的檔案類型格式相容，您可以使用這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="62632-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="62632-325">如果您定義的新副檔名使用這些格式的其中一種，您可以註冊處理常式類別識別碼 (CLSID) 的副檔名，以使用系統提供的處理常式。</span><span class="sxs-lookup"><span data-stu-id="62632-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="62632-326">您可以使用下表所列的 CLSID，針對您的檔案格式類型註冊系統提供的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="62632-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="62632-327">格式</span><span class="sxs-lookup"><span data-stu-id="62632-327">Format</span></span>          | <span data-ttu-id="62632-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="62632-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="62632-329">OLE e</span><span class="sxs-lookup"><span data-stu-id="62632-329">OLE DocFile</span></span>     | <span data-ttu-id="62632-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="62632-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="62632-331">儲存遊戲 XML</span><span class="sxs-lookup"><span data-stu-id="62632-331">Save Game XML</span></span>   | <span data-ttu-id="62632-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="62632-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="62632-333">XPS/OPC 處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-333">XPS/OPC handler</span></span> | <span data-ttu-id="62632-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="62632-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="62632-335">XML</span><span class="sxs-lookup"><span data-stu-id="62632-335">XML</span></span>             | <span data-ttu-id="62632-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="62632-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="62632-337">在建立自訂屬性之前，您應該確定沒有可改用的系統定義屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="62632-338">您可以藉由呼叫 [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) 或使用 prop.exe 命令列工具來列舉系統定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="62632-339">系統架構會定義這些屬性如何與索引子互動，而且您無法變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="62632-340">此外，您用來建立、編輯及儲存檔案類型的應用程式也必須符合特定行為。</span><span class="sxs-lookup"><span data-stu-id="62632-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="62632-341">例如，如果應用程式會執行安全儲存 (在編輯期間建立暫存檔案，然後使用 ReplaceFile () 來交換舊) 的新版本，則必須將原始檔案的所有屬性傳送至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="62632-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="62632-342">失敗的原因表示檔案遺失使用者或其他應用程式所新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="62632-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="62632-343">**範例**</span><span class="sxs-lookup"><span data-stu-id="62632-343">**Example**</span></span>

<span data-ttu-id="62632-344">下圖顯示使用之檔案類型的系統提供的 OLE e 處理常式註冊。OLEDocFile 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="62632-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="62632-345">下圖顯示內容清單資訊的註冊，以及的屬性。OLEDocFile 檔案會顯示在 [詳細資料] 索引標籤和窗格上。</span><span class="sxs-lookup"><span data-stu-id="62632-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="62632-346">相關主題</span><span class="sxs-lookup"><span data-stu-id="62632-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62632-347">**參考**</span><span class="sxs-lookup"><span data-stu-id="62632-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62632-348">屬性對應</span><span class="sxs-lookup"><span data-stu-id="62632-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="62632-349">**概念**</span><span class="sxs-lookup"><span data-stu-id="62632-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62632-350">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="62632-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="62632-351">索引處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="62632-352">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="62632-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="62632-353">自訂檔案格式的系統定義屬性</span><span class="sxs-lookup"><span data-stu-id="62632-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="62632-354">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="62632-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="62632-355">屬性系統</span><span class="sxs-lookup"><span data-stu-id="62632-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="62632-356">[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="62632-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="62632-357">Windows Search SDK 範例</span><span class="sxs-lookup"><span data-stu-id="62632-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 

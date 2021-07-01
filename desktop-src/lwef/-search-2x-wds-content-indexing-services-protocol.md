---
title: 內容索引服務通訊協定
description: 本檔是內容索引服務通訊協定的規格。
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119733"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="88b6c-103">內容索引服務通訊協定</span><span class="sxs-lookup"><span data-stu-id="88b6c-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="88b6c-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="88b6c-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="88b6c-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="88b6c-106">通訊協定規格，版本0.12</span><span class="sxs-lookup"><span data-stu-id="88b6c-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="88b6c-107">1簡介</span><span class="sxs-lookup"><span data-stu-id="88b6c-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="88b6c-108">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="88b6c-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="88b6c-109">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="88b6c-110">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="88b6c-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="88b6c-111">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="88b6c-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="88b6c-112">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="88b6c-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="88b6c-113">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="88b6c-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="88b6c-114">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="88b6c-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="88b6c-115">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="88b6c-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="88b6c-116">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="88b6c-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="88b6c-117">2 訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="88b6c-118">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="88b6c-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="88b6c-119">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="88b6c-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="88b6c-120">3 通訊協定詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="88b6c-121">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="88b6c-122">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="88b6c-123">4 通訊協定範例</span><span class="sxs-lookup"><span data-stu-id="88b6c-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="88b6c-124">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="88b6c-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="88b6c-125">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="88b6c-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="88b6c-126">5 安全性</span><span class="sxs-lookup"><span data-stu-id="88b6c-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="88b6c-127">5.1 實作者的安全性考量</span><span class="sxs-lookup"><span data-stu-id="88b6c-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="88b6c-128">5.2 安全性參數的索引</span><span class="sxs-lookup"><span data-stu-id="88b6c-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="88b6c-129">6個版本特定行為的索引</span><span class="sxs-lookup"><span data-stu-id="88b6c-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="88b6c-130">本檔是內容索引服務通訊協定的規格。</span><span class="sxs-lookup"><span data-stu-id="88b6c-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="88b6c-131">工作組伺服器通訊協定程式 (WSPP) 檔集適用于搭配公用標準檔、網路程式設計藝術以及 Windows 工作組分散式系統概念，並假設讀者已熟悉上述的材質或立即存取它。</span><span class="sxs-lookup"><span data-stu-id="88b6c-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="88b6c-132">WSPP 通訊協定規格不需要使用 Microsoft 程式設計工具或程式設計環境，才能讓授權者開發執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="88b6c-133">擁有 Microsoft 程式設計工具和環境存取權的授權人可自由利用這些工具。</span><span class="sxs-lookup"><span data-stu-id="88b6c-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="88b6c-134">1 簡介</span><span class="sxs-lookup"><span data-stu-id="88b6c-134">1 Introduction</span></span>

-   [<span data-ttu-id="88b6c-135">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="88b6c-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="88b6c-136">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="88b6c-137">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="88b6c-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="88b6c-138">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="88b6c-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="88b6c-139">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="88b6c-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="88b6c-140">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="88b6c-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="88b6c-141">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="88b6c-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="88b6c-142">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="88b6c-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="88b6c-143">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="88b6c-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="88b6c-144">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="88b6c-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="88b6c-145">下列詞彙定義于 MS-SYS 的詞彙區段中 \[ \] ：</span><span class="sxs-lookup"><span data-stu-id="88b6c-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="88b6c-146">GUID</span><span class="sxs-lookup"><span data-stu-id="88b6c-146">GUID</span></span>
> -   <span data-ttu-id="88b6c-147">位元組由小到小</span><span class="sxs-lookup"><span data-stu-id="88b6c-147">Little Endian</span></span>
> -   <span data-ttu-id="88b6c-148">具名管道</span><span class="sxs-lookup"><span data-stu-id="88b6c-148">Named Pipe</span></span>
> -   <span data-ttu-id="88b6c-149">路徑</span><span class="sxs-lookup"><span data-stu-id="88b6c-149">Path</span></span>

 

<span data-ttu-id="88b6c-150">**Binding**：在傳回的資料 **列** 集中包含特定資料 **行** 的要求。</span><span class="sxs-lookup"><span data-stu-id="88b6c-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="88b6c-151">系結會指定要包含在搜尋結果 **中的屬性** 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="88b6c-152">**書簽**：在一組資料列中唯一識別資料列的標記。</span><span class="sxs-lookup"><span data-stu-id="88b6c-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="88b6c-153">**目錄**：索引服務中最高層級的組織單位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="88b6c-154">它代表一組已編制索引的檔，可讓您使用「內容索引服務」通訊協定來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="88b6c-155">**Category**：階層式資料列群組。</span><span class="sxs-lookup"><span data-stu-id="88b6c-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="88b6c-156">例如，包含 author 和 title 資料行的查詢結果可以根據作者分類。</span><span class="sxs-lookup"><span data-stu-id="88b6c-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="88b6c-157">每一組包含相同作者值的資料列都會構成一個類別目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="88b6c-158">**章節**：一組 **資料列內** 的資料 **列** 範圍。</span><span class="sxs-lookup"><span data-stu-id="88b6c-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="88b6c-159">資料 **行**：資料 **列** 中單一類型資訊的容器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="88b6c-160">資料行會對應至屬性名稱，並指定搜尋查詢的 **命令\*\*\*\*樹** 元素所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="88b6c-161">**命令樹**：為搜尋查詢指定的 **限制** 、 **類別** 和 **排序次序** 的組合。</span><span class="sxs-lookup"><span data-stu-id="88b6c-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="88b6c-162">資料 **指標**：一個實體，用來做為在結果集中傳回的一組資料中，一次處理一個資料 **列** 或小型資料 **列** 區塊的機制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="88b6c-163">資料 **指標** 位於結果集內的單一資料 **列** 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="88b6c-164">將資料 **指標** 置於資料列之後，就可以在該資料 **列** 或從該位置開始的資料 **列** 區塊上執行作業。</span><span class="sxs-lookup"><span data-stu-id="88b6c-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="88b6c-165">**控制碼**：可以用來識別及存取資料 **指標** 、 **章節** 和 **書簽** 的權杖。</span><span class="sxs-lookup"><span data-stu-id="88b6c-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="88b6c-166">**Index**：持續性結構，包含 **索引服務** 所提取的文字內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="88b6c-167">這包含單字清單，這些字組會與包含的檔案名、單字位置和 **地區** 設定一起儲存。</span><span class="sxs-lookup"><span data-stu-id="88b6c-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="88b6c-168">**索引**：從檔案中解壓縮文字和屬性，以及將解壓縮的值儲存到文字) 的 **索引** (，以及) 屬性的 **屬性** 快取 (的程式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="88b6c-169">**索引服務**：為檔案系統的內容和屬性建立索引 **目錄** 的服務。</span><span class="sxs-lookup"><span data-stu-id="88b6c-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="88b6c-170">應用程式可以在目錄中搜尋已編制索引之檔案系統上的檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="88b6c-171">**地區** 設定：以 GPSI 附錄 A 指定的識別碼，可 \[ \] 指定與語言相關的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="88b6c-172">這些喜好設定會指出如何格式化日期和時間、依字母順序排序專案、要比較的字串等等。</span><span class="sxs-lookup"><span data-stu-id="88b6c-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="88b6c-173">**自然語言查詢**：使用人類語言而非查詢語法所建立的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="88b6c-174">非搜尋 **字**：索引服務在針對搜尋查詢所指定的 **限制** 中出現時，會忽略該單字，因為它的歧視性值很小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="88b6c-175">英文範例包括「a」、「和」和「」。</span><span class="sxs-lookup"><span data-stu-id="88b6c-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="88b6c-176">**屬性** 快取： **索引服務** 所解壓縮檔案屬性的快取。</span><span class="sxs-lookup"><span data-stu-id="88b6c-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="88b6c-177">**屬性編制索引**：建立檔之實 **數值型別屬性\*\*\*\*索引** 的程式，包括作者、主旨、類型、字數統計、列印的頁面計數，以及任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="88b6c-178">**限制**：檔案必須符合才能包含在 **索引服務** 所傳回之搜尋結果中的一組條件，以回應搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="88b6c-179">**限制** 可縮小搜尋查詢的焦點，將 **索引服務** 只會包含在搜尋結果中的檔案，限制為符合條件的檔案。</span><span class="sxs-lookup"><span data-stu-id="88b6c-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="88b6c-180">**Row**：資料行的 **集合，其中** 包含的屬性值會描述一組檔案中的單一檔案，這些檔案會與提交給 **索引服務** 的搜尋查詢中所指定的 **限制** 相符。</span><span class="sxs-lookup"><span data-stu-id="88b6c-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="88b6c-181">資料列 **集**：在搜尋結果中傳回的一組資料 **列**。</span><span class="sxs-lookup"><span data-stu-id="88b6c-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="88b6c-182">**排序次序**：搜尋查詢中定義搜尋結果中資料列順序的規則集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="88b6c-183">每個規則都包含一個屬性 (名稱、大小等等 ) 以及排序 (遞增或遞減) 的方向。</span><span class="sxs-lookup"><span data-stu-id="88b6c-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="88b6c-184">順序套用多個規則</span><span class="sxs-lookup"><span data-stu-id="88b6c-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="88b6c-185">**文字類型屬性**：描述檔內容的屬性，而且只有未格式化的文字與其名稱相關聯。</span><span class="sxs-lookup"><span data-stu-id="88b6c-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="88b6c-186">**數值型別屬性**：描述整份檔之單一屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="88b6c-187">實數值型別屬性具有資料類型識別碼，以及與其名稱相關聯之資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="88b6c-188">**虛擬根目錄**：資料夾的替代路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="88b6c-189">實體資料夾可以有零或多個虛擬根目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="88b6c-190">以虛擬根目錄開頭的路徑稱為虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="88b6c-191">例如，/server/vanityroot 可能是 C： \\ IIS web folder1 的虛擬根目錄 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="88b6c-192">然後 file C： \\ IIS \\ web \\ folder1 \\default.htm 會有/server/vanityroot/default.htm 的虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="88b6c-193">「不得」、「**不得**」、「不得」、「不得」：這些詞彙 (在所有 caps) 中，如 RFC2119 中所述 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="88b6c-194">選擇性行為的所有陳述均使用「可能」、「應該」或「不應」。</span><span class="sxs-lookup"><span data-stu-id="88b6c-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="88b6c-195">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="88b6c-196">1.2.1 標準參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-196">1.2.1 Normative References</span></span>

<span data-ttu-id="88b6c-197">\[IEEE754 \] 協會的電子和電子工程師「標準的二進位 Floating-Point 算術標準」、IEEE 754-1985、1985年10月 https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="88b6c-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="88b6c-198">\[MS DCOM \] Microsoft Corporation，「分散式元件物件模型遠端通訊協定」，2006年6月。</span><span class="sxs-lookup"><span data-stu-id="88b6c-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="88b6c-199">\[GPSI Microsoft Corporation 「 \] 群組原則軟體安裝延伸模組」，2006年6月。</span><span class="sxs-lookup"><span data-stu-id="88b6c-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="88b6c-200">\[MS SMB \] Microsoft Corporation 「Microsoft Server Message Block (SMB) 通訊協定和延伸模組」，可能是2006。</span><span class="sxs-lookup"><span data-stu-id="88b6c-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="88b6c-201">\[MS SYS \] Microsoft Corporation "System 總覽 v4"，2006年7月。</span><span class="sxs-lookup"><span data-stu-id="88b6c-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="88b6c-202">\[SALTON \] SALTON，G.，"自動文字處理：依電腦的轉換剖析和抓取資訊"，1988，ISBN 0-201-2227-8。</span><span class="sxs-lookup"><span data-stu-id="88b6c-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="88b6c-203">\[Unicode \] 協會： "Unicode Standard，Version 2.0"，1996， https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="88b6c-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="88b6c-204">1.2.2 資訊參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-204">1.2.2 Informative References</span></span>

<span data-ttu-id="88b6c-205">\[MSDN-OLEDB \] Microsoft Corporation，OLE DB https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="88b6c-206">\[MSDN-QUERYERR \] Microsoft Corporation、Query-Execution 值、 https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="88b6c-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="88b6c-207">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="88b6c-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="88b6c-208">內容 **編制索引服務** 有助於有效率地組織檔集合的已解壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="88b6c-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="88b6c-209">內容編制索引服務通訊協定 (CISP) 可讓用戶端與裝載索引服務的伺服器進行通訊，以發出查詢並允許系統管理員管理索引伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="88b6c-210">處理檔案時，索引服務會分析一組檔，並重新組織其內容，如此一來，這些檔的 **屬性** 就可以有效率地傳回以回應查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="88b6c-211">可以查詢的檔集合包含 **目錄** 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="88b6c-212">目錄可以包含 **索引** (，以快速參考文字) 和 **屬性** 快取 (來快速抓取屬性值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="88b6c-213">就概念而言，目錄是由具有文字或值的屬性邏輯「資料表」，以及儲存在資料表資料 **行** 中的對應地區設定所組成。</span><span class="sxs-lookup"><span data-stu-id="88b6c-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="88b6c-214">資料表的每個「資料列」會對應至目錄範圍中的個別檔，而資料表的每個「資料行」會對應至屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="88b6c-215">CISP 執行的特定工作分為兩個功能區域：</span><span class="sxs-lookup"><span data-stu-id="88b6c-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="88b6c-216">索引服務目錄的遠端系統管理</span><span class="sxs-lookup"><span data-stu-id="88b6c-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="88b6c-217">遠端查詢索引服務目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="88b6c-218">1.3.1 遠端系統管理工作</span><span class="sxs-lookup"><span data-stu-id="88b6c-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="88b6c-219">CISP 可讓用戶端進行下列索引編制服務類別目錄管理工作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="88b6c-220">查詢伺服器上索引服務類別目錄的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="88b6c-221">更新索引服務類別目錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="88b6c-222">啟動一組特定檔案的編制索引程式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="88b6c-223">起始索引的優化，以便改善查詢效能。</span><span class="sxs-lookup"><span data-stu-id="88b6c-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="88b6c-224">所有遠端系統管理工作都遵循簡單的要求/回應模型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="88b6c-225">用戶端不會在任何系統管理呼叫中維護任何狀態，而且系統會以任何順序進行管理呼叫。</span><span class="sxs-lookup"><span data-stu-id="88b6c-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="88b6c-226">1.3.2 遠端查詢</span><span class="sxs-lookup"><span data-stu-id="88b6c-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="88b6c-227">CISP 可讓用戶端對裝載索引服務的遠端伺服器執行搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="88b6c-228">傳送搜尋查詢是由用戶端所起始的多步驟處理常式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="88b6c-229">步驟如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="88b6c-230">用戶端要求連接到裝載索引服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="88b6c-231">用戶端會傳送搜尋查詢的參數，包括：</span><span class="sxs-lookup"><span data-stu-id="88b6c-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="88b6c-232">指定要在搜尋結果中包含及/或排除哪些檔的 **限制** 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="88b6c-233">傳回搜尋結果的順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="88b6c-234">要在結果集中傳回的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="88b6c-235">應針對查詢傳回的最大資料 **列** 數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="88b6c-236">查詢執行的最長時間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="88b6c-237">一旦伺服器已確認用戶端起始查詢的要求，用戶端就可以要求有關查詢的狀態資訊，但這不是必要的步驟。</span><span class="sxs-lookup"><span data-stu-id="88b6c-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="88b6c-238">用戶端接著會指定伺服器應包含在搜尋結果中的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="88b6c-239">用戶端會向伺服器要求結果集，而伺服器會透過傳送用戶端搜尋查詢結果中所包含之檔案的屬性值來回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="88b6c-240">如果屬性值太大而無法放入單一回應緩衝區中，伺服器將不會傳送屬性，而是會將屬性狀態設定為 [已延後]。</span><span class="sxs-lookup"><span data-stu-id="88b6c-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="88b6c-241">然後，用戶端會使用一系列的連續值區塊來個別要求屬性值，然後再繼續要求其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="88b6c-242">一旦用戶端使用搜尋查詢完成，且不再需要額外的結果，用戶端會與伺服器聯繫以釋出查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="88b6c-243">一旦伺服器釋出查詢之後，用戶端可能會傳送要求，以便中斷與伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="88b6c-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="88b6c-244">然後連接會關閉。</span><span class="sxs-lookup"><span data-stu-id="88b6c-244">The connection is then closed.</span></span> <span data-ttu-id="88b6c-245">或者，用戶端可能會發出另一個查詢，並重複步驟2中的順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="88b6c-246">Windows 行為：此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="88b6c-247">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="88b6c-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="88b6c-248">CISP 依賴 SMB \[ MS smb \] 通訊協定來傳輸訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="88b6c-249">沒有其他通訊協定直接相依于內容編制索引服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="88b6c-250">*Windows 行為：應用程式通常會與 OLE DB 介面包裝函 \[ 式 MSDN-OLEDB \] (，例如通訊協定用戶端) ，而不是直接與通訊協定互動。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="88b6c-251">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="88b6c-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="88b6c-252">假設用戶端在叫用此通訊協定之前，已取得伺服器的名稱和目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="88b6c-253">用戶端如何進行這項規格的範圍之外。</span><span class="sxs-lookup"><span data-stu-id="88b6c-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="88b6c-254">也假設用戶端和伺服器具有可與具名管道 MS SMB 搭配使用的安全性關聯 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="88b6c-255">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="88b6c-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="88b6c-256">CISP 是設計用來從用戶端查詢及管理遠端伺服器上的目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="88b6c-257">CISP 已在 Windows Vista 上淘汰。</span><span class="sxs-lookup"><span data-stu-id="88b6c-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="88b6c-258">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="88b6c-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="88b6c-259">此通訊協定沒有任何版本控制或功能協商機制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="88b6c-260">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="88b6c-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="88b6c-261">此通訊協定會使用可延伸廠商的 Hresult。</span><span class="sxs-lookup"><span data-stu-id="88b6c-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="88b6c-262">您可以針對此欄位自由選擇自己的值，只要 C 位 (0x20000000) 設定為在 MS-SYS 的區段4.1.1 中指定 \[ \] ，表示它是客戶程式碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="88b6c-263">此通訊協定也會使用取自在 Ms-chap 中定義之 NTSTATUS 網際空間的 NTSTATUS 值 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="88b6c-264">廠商應以其指定的意義重複使用這些值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="88b6c-265">選擇任何其他值，就會在未來發生衝突的風險。</span><span class="sxs-lookup"><span data-stu-id="88b6c-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="88b6c-266">*Windows 行為： Windows 只會使用4.1.3 的區段中指定的值 \[ \] 。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="88b6c-267">1.8.1 屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="88b6c-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="88b6c-268">屬性是由稱為屬性識別碼的識別碼來表示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="88b6c-269">每個屬性都必須有全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="88b6c-270">此識別碼是由 GUID 所組成，此 **GUID** 代表稱為屬性集的屬性集合，加上字串或32位整數，以識別集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="88b6c-271">如果使用整數形式的識別碼，則會將0x00000000、0xFFFFFFFF 和0xFFFFFFFE 值視為無效。</span><span class="sxs-lookup"><span data-stu-id="88b6c-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="88b6c-272">廠商可以將屬性放在其本身的 GUID 所定義的屬性集中，以保證其屬性是唯一的定義。</span><span class="sxs-lookup"><span data-stu-id="88b6c-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="88b6c-273">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="88b6c-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="88b6c-274">此通訊協定不會指派標準，而只會使用其他通訊協定中指定的配置程式來進行 Microsoft 所做的私用指派。</span><span class="sxs-lookup"><span data-stu-id="88b6c-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="88b6c-275">Microsoft 已將此通訊協定配置給以 MS SMB 指定的具名管道 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="88b6c-276">指派為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-276">The assignment is:</span></span>



| <span data-ttu-id="88b6c-277">參數</span><span class="sxs-lookup"><span data-stu-id="88b6c-277">Parameter</span></span> | <span data-ttu-id="88b6c-278">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-278">Value</span></span>             | <span data-ttu-id="88b6c-279">參考</span><span class="sxs-lookup"><span data-stu-id="88b6c-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="88b6c-280">管道名稱</span><span class="sxs-lookup"><span data-stu-id="88b6c-280">Pipe name</span></span> | <span data-ttu-id="88b6c-281">\\管道 \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="88b6c-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="88b6c-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="88b6c-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="88b6c-283">2 訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-283">2 Messages</span></span>

-   [<span data-ttu-id="88b6c-284">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="88b6c-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="88b6c-285">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="88b6c-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="88b6c-286">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="88b6c-286">2.1 Transport</span></span>

<span data-ttu-id="88b6c-287">所有訊息都必須使用具名管道來傳輸（如 MS SMB 中所指定） \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="88b6c-288">使用的管道名稱如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="88b6c-289">\\管道 \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="88b6c-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="88b6c-290">此通訊協定會使用基礎 SMB 具名管道通訊協定，來抓取進行連接的呼叫端身分識別，如 MS-SMB 的區段2.2.8 中所指定 \[ \] ; 用戶端必須將安全性 \_ 識別設定為要求中的 ImpersonationLevel，才能開啟具名管道。</span><span class="sxs-lookup"><span data-stu-id="88b6c-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="88b6c-291">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="88b6c-291">2.2 Message Syntax</span></span>

<span data-ttu-id="88b6c-292">下列各節中的數個結構和訊息是指章節或書簽控制碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="88b6c-293">控制碼是可唯一識別章節或書簽的32位長透明結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="88b6c-294">一般而言，用戶端應用程式會透過方法呼叫來接收控制碼值;不過，有幾個已知的值不需要從伺服器取得，其意義如下表所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="88b6c-295">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-295">Value</span></span>                         | <span data-ttu-id="88b6c-296">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-297">DB \_ Null \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="88b6c-298">Unchaptered 資料列集的章節控制碼，其中包含所有查詢結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="88b6c-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="88b6c-300">書簽的書簽控制碼，這個書簽會識別資料列集中的第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="88b6c-301">DBBMK \_ 最後的0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="88b6c-302">書簽的書簽控制碼，這個書簽會識別資料列集中的最後一個資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="88b6c-303">2.2.1 結構</span><span class="sxs-lookup"><span data-stu-id="88b6c-303">2.2.1 Structures</span></span>

<span data-ttu-id="88b6c-304">本節詳細說明 CISP 所定義和使用的資料結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="88b6c-305">下列結構中的所有2、4和8位元組的帶正負號和不帶正負號的整數都必須以位元組由小到大的順序傳送。</span><span class="sxs-lookup"><span data-stu-id="88b6c-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="88b6c-306">下表摘要說明此區段中定義的資料結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="88b6c-307">結構</span><span class="sxs-lookup"><span data-stu-id="88b6c-307">Structure</span></span>                    | <span data-ttu-id="88b6c-308">描述</span><span class="sxs-lookup"><span data-stu-id="88b6c-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="88b6c-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="88b6c-310">包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="88b6c-311">SAFEARRAY、SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="88b6c-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="88b6c-312">包含多維陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="88b6c-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="88b6c-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="88b6c-314">表示 SAFEARRAY 結構中所指定之陣列維度的界限。</span><span class="sxs-lookup"><span data-stu-id="88b6c-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="88b6c-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-315">CFullPropSpec</span></span>                | <span data-ttu-id="88b6c-316">包含屬性規格。</span><span class="sxs-lookup"><span data-stu-id="88b6c-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="88b6c-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-317">CContentRestriction</span></span>          | <span data-ttu-id="88b6c-318">包含屬性（property）快取中的屬性值所要比對的字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="88b6c-319">CKey</span><span class="sxs-lookup"><span data-stu-id="88b6c-319">CKey</span></span>                         | <span data-ttu-id="88b6c-320">包含屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="88b6c-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="88b6c-322">包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="88b6c-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="88b6c-324">包含屬性的自然語言查詢相符項。</span><span class="sxs-lookup"><span data-stu-id="88b6c-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="88b6c-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-325">CNodeRestriction</span></span>             | <span data-ttu-id="88b6c-326">包含指定查詢限制的命令樹節點陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="88b6c-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-327">COccRestriction</span></span>              | <span data-ttu-id="88b6c-328">包含單字在片語中的位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="88b6c-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-329">CPropertyRestriction</span></span>         | <span data-ttu-id="88b6c-330">包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="88b6c-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-331">CRangeRestriction</span></span>            | <span data-ttu-id="88b6c-332">包含值範圍的限制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="88b6c-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-333">CScopeRestriction</span></span>            | <span data-ttu-id="88b6c-334">包含要搜尋之檔案的限制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="88b6c-335">CSort</span><span class="sxs-lookup"><span data-stu-id="88b6c-335">CSort</span></span>                        | <span data-ttu-id="88b6c-336">識別要排序的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-337">CSynRestriction</span></span>              | <span data-ttu-id="88b6c-338">包含查詢片語的單字或其同義字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="88b6c-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-339">CVectorRestriction</span></span>           | <span data-ttu-id="88b6c-340">包含命令樹節點上的加權或運算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="88b6c-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-341">CWordRestriction</span></span>             | <span data-ttu-id="88b6c-342">包含查詢片語的單字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="88b6c-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-343">CRestriction</span></span>                 | <span data-ttu-id="88b6c-344">包含查詢命令樹的節點。</span><span class="sxs-lookup"><span data-stu-id="88b6c-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="88b6c-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-345">CColumnSet</span></span>                   | <span data-ttu-id="88b6c-346">指出要傳回的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="88b6c-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-347">CCategorizationSet</span></span>           | <span data-ttu-id="88b6c-348">包含一組查詢結果群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="88b6c-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-349">CCategorizationSpec</span></span>          | <span data-ttu-id="88b6c-350">包含分類的定義，查詢結果將分類至其中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="88b6c-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="88b6c-351">CDbColId</span></span>                     | <span data-ttu-id="88b6c-352">包含資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="88b6c-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="88b6c-353">CDbProp</span></span>                      | <span data-ttu-id="88b6c-354">包含屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="88b6c-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-355">CDbPropSet</span></span>                   | <span data-ttu-id="88b6c-356">包含一組屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="88b6c-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="88b6c-357">CPidMapper</span></span>                   | <span data-ttu-id="88b6c-358">包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="88b6c-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="88b6c-359">CRowSeekAt</span></span>                   | <span data-ttu-id="88b6c-360">包含要在 CPMGetRowsIn 訊息中取得資料列的位移</span><span class="sxs-lookup"><span data-stu-id="88b6c-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="88b6c-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="88b6c-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="88b6c-362">識別開始抓取 CPMGetRowsIn 訊息的起點。</span><span class="sxs-lookup"><span data-stu-id="88b6c-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="88b6c-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="88b6c-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="88b6c-364">識別要從中取出 CPMGetRowsIn 訊息之資料列的書簽。</span><span class="sxs-lookup"><span data-stu-id="88b6c-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="88b6c-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="88b6c-365">CRowSeekNext</span></span>                 | <span data-ttu-id="88b6c-366">包含要在 CPMGetRowsIn 訊息中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="88b6c-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="88b6c-367">CRowsetProperties</span></span>            | <span data-ttu-id="88b6c-368">包含查詢的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="88b6c-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-369">CSortSet</span></span>                     | <span data-ttu-id="88b6c-370">包含查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="88b6c-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="88b6c-371">CTableColumn</span></span>                 | <span data-ttu-id="88b6c-372">包含 CPMSetBindings 訊息的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="88b6c-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="88b6c-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="88b6c-374">包含序列化值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="88b6c-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="88b6c-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="88b6c-376">CBaseStorageVariant 結構包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="88b6c-377">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-377">0</span></span>

<span data-ttu-id="88b6c-378">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-378">1</span></span>

<span data-ttu-id="88b6c-379">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-379">2</span></span>

<span data-ttu-id="88b6c-380">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-380">3</span></span>

<span data-ttu-id="88b6c-381">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-381">4</span></span>

<span data-ttu-id="88b6c-382">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-382">5</span></span>

<span data-ttu-id="88b6c-383">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-383">6</span></span>

<span data-ttu-id="88b6c-384">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-384">7</span></span>

<span data-ttu-id="88b6c-385">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-385">8</span></span>

<span data-ttu-id="88b6c-386">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-386">9</span></span>

<span data-ttu-id="88b6c-387">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-387">1</span></span><br/> <span data-ttu-id="88b6c-388">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-388">0</span></span><br/>

<span data-ttu-id="88b6c-389">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-389">1</span></span>

<span data-ttu-id="88b6c-390">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-390">2</span></span>

<span data-ttu-id="88b6c-391">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-391">3</span></span>

<span data-ttu-id="88b6c-392">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-392">4</span></span>

<span data-ttu-id="88b6c-393">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-393">5</span></span>

<span data-ttu-id="88b6c-394">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-394">6</span></span>

<span data-ttu-id="88b6c-395">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-395">7</span></span>

<span data-ttu-id="88b6c-396">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-396">8</span></span>

<span data-ttu-id="88b6c-397">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-397">9</span></span>

<span data-ttu-id="88b6c-398">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-398">2</span></span><br/> <span data-ttu-id="88b6c-399">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-399">0</span></span><br/>

<span data-ttu-id="88b6c-400">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-400">1</span></span>

<span data-ttu-id="88b6c-401">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-401">2</span></span>

<span data-ttu-id="88b6c-402">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-402">3</span></span>

<span data-ttu-id="88b6c-403">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-403">4</span></span>

<span data-ttu-id="88b6c-404">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-404">5</span></span>

<span data-ttu-id="88b6c-405">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-405">6</span></span>

<span data-ttu-id="88b6c-406">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-406">7</span></span>

<span data-ttu-id="88b6c-407">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-407">8</span></span>

<span data-ttu-id="88b6c-408">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-408">9</span></span>

<span data-ttu-id="88b6c-409">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-409">3</span></span><br/> <span data-ttu-id="88b6c-410">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-410">0</span></span><br/>

<span data-ttu-id="88b6c-411">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-411">1</span></span>

<span data-ttu-id="88b6c-412">vType</span><span class="sxs-lookup"><span data-stu-id="88b6c-412">vType</span></span>

<span data-ttu-id="88b6c-413">vData1</span><span class="sxs-lookup"><span data-stu-id="88b6c-413">vData1</span></span>

<span data-ttu-id="88b6c-414">vData2</span><span class="sxs-lookup"><span data-stu-id="88b6c-414">vData2</span></span>

<span data-ttu-id="88b6c-415">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-415">vValue (variable)</span></span>



 

<span data-ttu-id="88b6c-416">**vType**：類型指標，表示 vValue 的類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="88b6c-417">它必須是下表中指定的其中一個 VARENUM 值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="88b6c-418">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-418">Value</span></span>                 | <span data-ttu-id="88b6c-419">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-420">VT \_ 空白 (0x0000) </span><span class="sxs-lookup"><span data-stu-id="88b6c-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="88b6c-421">vValue 不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="88b6c-422">VT \_ Null (0x0001) </span><span class="sxs-lookup"><span data-stu-id="88b6c-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="88b6c-423">vValue 不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="88b6c-424">VT \_ I1 (0x0010) </span><span class="sxs-lookup"><span data-stu-id="88b6c-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="88b6c-425">1 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="88b6c-426">VT \_ UI1 (0x0011) </span><span class="sxs-lookup"><span data-stu-id="88b6c-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="88b6c-427">1 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="88b6c-428">VT \_ I2 (0x0002) </span><span class="sxs-lookup"><span data-stu-id="88b6c-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="88b6c-429">2 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="88b6c-430">VT \_ UI2 (0x0012) </span><span class="sxs-lookup"><span data-stu-id="88b6c-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="88b6c-431">2 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="88b6c-432">VT \_ BOOL (0x000B) </span><span class="sxs-lookup"><span data-stu-id="88b6c-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="88b6c-433">布林值;雙位元組整數，其中包含 0x0000 (FALSE) 或 0xFFFF (TRUE) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="88b6c-434">VT \_ I4 (0x0003) </span><span class="sxs-lookup"><span data-stu-id="88b6c-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="88b6c-435">4 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="88b6c-436">VT \_ UI4 (0x0013) </span><span class="sxs-lookup"><span data-stu-id="88b6c-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="88b6c-437">4 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="88b6c-438">VT \_ R4 (0x0004) </span><span class="sxs-lookup"><span data-stu-id="88b6c-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="88b6c-439">IEEE 32 位浮點數，如 IEEE754 中所定義 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="88b6c-440">VT \_ INT (0x0016) </span><span class="sxs-lookup"><span data-stu-id="88b6c-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="88b6c-441">4 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="88b6c-442">VT \_ UINT (0x0017) </span><span class="sxs-lookup"><span data-stu-id="88b6c-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="88b6c-443">4 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="88b6c-444">VT \_ 錯誤 (0x000A) </span><span class="sxs-lookup"><span data-stu-id="88b6c-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="88b6c-445">包含 HRESULT 的4位元組不帶正負號的整數，如 Ms-chap 中所指定 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="88b6c-446">VT \_ I8 (0x0014) </span><span class="sxs-lookup"><span data-stu-id="88b6c-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="88b6c-447">8位元組帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="88b6c-448">VT \_ UI8 (0x0015) </span><span class="sxs-lookup"><span data-stu-id="88b6c-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="88b6c-449">8 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="88b6c-450">VT \_ R8 (0x0005) </span><span class="sxs-lookup"><span data-stu-id="88b6c-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="88b6c-451">IEEE754 中定義的 IEEE 64 位浮點數 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="88b6c-452">VT \_ CY (0x0006) </span><span class="sxs-lookup"><span data-stu-id="88b6c-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="88b6c-453">8個位元組的補數整數 (由 10000) 調整。</span><span class="sxs-lookup"><span data-stu-id="88b6c-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="88b6c-454">VT \_ DATE (0x0007) </span><span class="sxs-lookup"><span data-stu-id="88b6c-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="88b6c-455">64位浮點數，代表自00:00:00 年12月31日起算的天數（1899 (國際標準時間) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="88b6c-456">VT \_ FILETIME (0x0040) </span><span class="sxs-lookup"><span data-stu-id="88b6c-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="88b6c-457">64位整數，表示自年1月 1 1601 日起00:00:00 的100秒間隔數， (國際標準時間) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="88b6c-458">VT \_ DECIMAL (0x000E) </span><span class="sxs-lookup"><span data-stu-id="88b6c-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="88b6c-459">2.2.1.1.1.1 一節中所指定的十進位結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="88b6c-460">VT \_ CLSID (0x0048) </span><span class="sxs-lookup"><span data-stu-id="88b6c-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="88b6c-461">包含 GUID 的16位元組二進位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="88b6c-462">VT \_ BLOB (0x0041) </span><span class="sxs-lookup"><span data-stu-id="88b6c-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="88b6c-463">Blob 中4位元組不帶正負號的整數的位元組計數，後面接著該資料的多個位元組。</span><span class="sxs-lookup"><span data-stu-id="88b6c-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="88b6c-464">VT \_ BSTR (0x0008) </span><span class="sxs-lookup"><span data-stu-id="88b6c-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="88b6c-465">字串中4位元組不帶正負號的整數的位元組計數，後面接著字串，如以下所示 vValue 下所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="88b6c-466">VT \_ LPSTR (0x001E) </span><span class="sxs-lookup"><span data-stu-id="88b6c-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="88b6c-467">以 null 結束的 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="88b6c-468">VT \_ LPWSTR (0x001F) </span><span class="sxs-lookup"><span data-stu-id="88b6c-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="88b6c-469">以 null 結尾的 Unicode \[ \] 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="88b6c-470">VT \_ 變異 (0x000C) </span><span class="sxs-lookup"><span data-stu-id="88b6c-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="88b6c-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="88b6c-471">CBaseStorageVariant.</span></span> <span data-ttu-id="88b6c-472">必須與 VT \_ 陣列或 vt 向量的類型修飾詞結合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="88b6c-473">下表指定 vType 的類型修飾詞。</span><span class="sxs-lookup"><span data-stu-id="88b6c-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="88b6c-474">類型修飾詞可以是具有 vType 的二進位 Or 運算，用以變更 vValue 的意義，表示它是兩個可能陣列類型的其中一個。</span><span class="sxs-lookup"><span data-stu-id="88b6c-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="88b6c-475">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-475">Value</span></span>               | <span data-ttu-id="88b6c-476">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-477">VT \_ 向量 (0x1000) </span><span class="sxs-lookup"><span data-stu-id="88b6c-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="88b6c-478">如果類型指標是 \_ 使用 OR 運算子與 VT 向量結合，則 vValue 是所指定類型之值的計數陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="88b6c-479">如需詳細資訊，請參閱2.2.1.1.1.2 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="88b6c-480">此類型修飾詞不能與下列類型結合： VT \_ INT、VT \_ UINT、vt \_ DECIMAL、VT \_ blob、vt \_ blob \_ 物件。</span><span class="sxs-lookup"><span data-stu-id="88b6c-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="88b6c-481">VT \_ 陣列 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="88b6c-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="88b6c-482">如果類型指標是 \_ 由 OR 運算子與 VT 陣列結合，則此值為 SAFEARRAY (，如區段 2.2.1.1.1.3) 中所指定，其中包含指定之類型的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="88b6c-483">此類型修飾詞不能與下列類型結合： VT \_ I8、vt \_ UI8、vt \_ FILETIME、VT \_ CLSID、vt \_ blob、vt \_ BLOB \_ 物件、vt \_ LPSTR、vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="88b6c-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="88b6c-484">**vData1**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 [小數位數] 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="88b6c-485">若為所有其他 vTypes，此值必須設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="88b6c-486">**vData2**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 Sign 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="88b6c-487">若為所有其他 vTypes，此值必須設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="88b6c-488">**vValue**：相符運算的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="88b6c-489">語法必須如 vType 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="88b6c-490">下表摘要說明 vValue 欄位的大小，其相依于固定長度資料類型的 vType 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="88b6c-491">大小是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-491">The size is in bytes.</span></span>



| <span data-ttu-id="88b6c-492">vType</span><span class="sxs-lookup"><span data-stu-id="88b6c-492">vType</span></span>                                                   | <span data-ttu-id="88b6c-493">大小</span><span class="sxs-lookup"><span data-stu-id="88b6c-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="88b6c-494">VT \_ I1、vt、 \_ UI1</span><span class="sxs-lookup"><span data-stu-id="88b6c-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="88b6c-495">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-495">1</span></span>    |
| <span data-ttu-id="88b6c-496">VT \_ I2，vt \_ UI2，vt \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="88b6c-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="88b6c-497">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-497">2</span></span>    |
| <span data-ttu-id="88b6c-498">VT \_ I4，vt \_ UI4，vt \_ R4，VT \_ INT，vt \_ UINT，VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="88b6c-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="88b6c-499">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-499">4</span></span>    |
| <span data-ttu-id="88b6c-500">VT \_ I8、vt \_ UI8、vt \_ R8、VT \_ CY、vt \_ DATE、vt \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="88b6c-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="88b6c-501">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-501">8</span></span>    |
| <span data-ttu-id="88b6c-502">VT \_ DECIMAL、VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="88b6c-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="88b6c-503">16</span><span class="sxs-lookup"><span data-stu-id="88b6c-503">16</span></span>   |



 

<span data-ttu-id="88b6c-504">如果 vType 設定為 VT \_ BLOB、vt \_ BSTR 或 vt LPSTR，則 \_ vValue 的結構會在下圖中指定：</span><span class="sxs-lookup"><span data-stu-id="88b6c-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="88b6c-505">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-505">0</span></span>

<span data-ttu-id="88b6c-506">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-506">1</span></span>

<span data-ttu-id="88b6c-507">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-507">2</span></span>

<span data-ttu-id="88b6c-508">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-508">3</span></span>

<span data-ttu-id="88b6c-509">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-509">4</span></span>

<span data-ttu-id="88b6c-510">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-510">5</span></span>

<span data-ttu-id="88b6c-511">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-511">6</span></span>

<span data-ttu-id="88b6c-512">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-512">7</span></span>

<span data-ttu-id="88b6c-513">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-513">8</span></span>

<span data-ttu-id="88b6c-514">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-514">9</span></span>

<span data-ttu-id="88b6c-515">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-515">1</span></span><br/> <span data-ttu-id="88b6c-516">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-516">0</span></span><br/>

<span data-ttu-id="88b6c-517">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-517">1</span></span>

<span data-ttu-id="88b6c-518">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-518">2</span></span>

<span data-ttu-id="88b6c-519">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-519">3</span></span>

<span data-ttu-id="88b6c-520">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-520">4</span></span>

<span data-ttu-id="88b6c-521">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-521">5</span></span>

<span data-ttu-id="88b6c-522">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-522">6</span></span>

<span data-ttu-id="88b6c-523">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-523">7</span></span>

<span data-ttu-id="88b6c-524">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-524">8</span></span>

<span data-ttu-id="88b6c-525">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-525">9</span></span>

<span data-ttu-id="88b6c-526">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-526">2</span></span><br/> <span data-ttu-id="88b6c-527">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-527">0</span></span><br/>

<span data-ttu-id="88b6c-528">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-528">1</span></span>

<span data-ttu-id="88b6c-529">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-529">2</span></span>

<span data-ttu-id="88b6c-530">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-530">3</span></span>

<span data-ttu-id="88b6c-531">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-531">4</span></span>

<span data-ttu-id="88b6c-532">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-532">5</span></span>

<span data-ttu-id="88b6c-533">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-533">6</span></span>

<span data-ttu-id="88b6c-534">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-534">7</span></span>

<span data-ttu-id="88b6c-535">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-535">8</span></span>

<span data-ttu-id="88b6c-536">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-536">9</span></span>

<span data-ttu-id="88b6c-537">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-537">3</span></span><br/> <span data-ttu-id="88b6c-538">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-538">0</span></span><br/>

<span data-ttu-id="88b6c-539">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-539">1</span></span>

<span data-ttu-id="88b6c-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="88b6c-540">cbSize</span></span>

<span data-ttu-id="88b6c-541">blobData (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="88b6c-542">**cbSize**：不帶正負號的32位整數，表示 blobData 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="88b6c-543">如果 vType 設定為 VT \_ BSTR 或 vt \_ LPSTR，則當表示的字串為空字串時，cbSize 必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="88b6c-544">**blobData**：必須是 cbSize 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="88b6c-545">針對設定為 VT blob 的 vType \_ ，此欄位是不透明的二進位 blob 資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="88b6c-546">針對設定為 VT BSTR 的 vType \_ ，此欄位是 OEM 所選取字元集中的一組字元。</span><span class="sxs-lookup"><span data-stu-id="88b6c-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="88b6c-547">用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="88b6c-548">不需要以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="88b6c-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="88b6c-549">若 vType 設為 VT \_ LPSTR，此欄位是 OEM 所選取字元集中以 null 結束的字元字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="88b6c-550">用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="88b6c-551">如果 vType 設定為 VT LPWSTR，則 \_ vValue 的結構會在下圖中指定：</span><span class="sxs-lookup"><span data-stu-id="88b6c-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="88b6c-552">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-552">0</span></span>

<span data-ttu-id="88b6c-553">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-553">1</span></span>

<span data-ttu-id="88b6c-554">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-554">2</span></span>

<span data-ttu-id="88b6c-555">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-555">3</span></span>

<span data-ttu-id="88b6c-556">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-556">4</span></span>

<span data-ttu-id="88b6c-557">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-557">5</span></span>

<span data-ttu-id="88b6c-558">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-558">6</span></span>

<span data-ttu-id="88b6c-559">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-559">7</span></span>

<span data-ttu-id="88b6c-560">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-560">8</span></span>

<span data-ttu-id="88b6c-561">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-561">9</span></span>

<span data-ttu-id="88b6c-562">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-562">1</span></span><br/> <span data-ttu-id="88b6c-563">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-563">0</span></span><br/>

<span data-ttu-id="88b6c-564">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-564">1</span></span>

<span data-ttu-id="88b6c-565">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-565">2</span></span>

<span data-ttu-id="88b6c-566">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-566">3</span></span>

<span data-ttu-id="88b6c-567">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-567">4</span></span>

<span data-ttu-id="88b6c-568">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-568">5</span></span>

<span data-ttu-id="88b6c-569">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-569">6</span></span>

<span data-ttu-id="88b6c-570">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-570">7</span></span>

<span data-ttu-id="88b6c-571">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-571">8</span></span>

<span data-ttu-id="88b6c-572">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-572">9</span></span>

<span data-ttu-id="88b6c-573">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-573">2</span></span><br/> <span data-ttu-id="88b6c-574">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-574">0</span></span><br/>

<span data-ttu-id="88b6c-575">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-575">1</span></span>

<span data-ttu-id="88b6c-576">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-576">2</span></span>

<span data-ttu-id="88b6c-577">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-577">3</span></span>

<span data-ttu-id="88b6c-578">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-578">4</span></span>

<span data-ttu-id="88b6c-579">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-579">5</span></span>

<span data-ttu-id="88b6c-580">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-580">6</span></span>

<span data-ttu-id="88b6c-581">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-581">7</span></span>

<span data-ttu-id="88b6c-582">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-582">8</span></span>

<span data-ttu-id="88b6c-583">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-583">9</span></span>

<span data-ttu-id="88b6c-584">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-584">3</span></span><br/> <span data-ttu-id="88b6c-585">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-585">0</span></span><br/>

<span data-ttu-id="88b6c-586">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-586">1</span></span>

<span data-ttu-id="88b6c-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="88b6c-587">ccLen</span></span>

<span data-ttu-id="88b6c-588">字串 (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-588">string (variable, optional)</span></span>



 

<span data-ttu-id="88b6c-589">**ccLen**：不帶正負號的32位整數，表示字串欄位的大小（以 Unicode 字元表示）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="88b6c-590">若為空字串，則必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="88b6c-591">**字串**：以 Null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="88b6c-592">2.2.1.1.1 CBaseStorageVariant 結構</span><span class="sxs-lookup"><span data-stu-id="88b6c-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="88b6c-593">下列結構會在 CBaseStorageVariant 結構中使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="88b6c-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="88b6c-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="88b6c-595">DECIMAL 用來表示具有固定有效位數和固定小數位數的精確數值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="88b6c-596">當 vType 設定為 VT \_ DECIMAL (0x0000E) 時，CBaseStorageVariant 的 vData1 和 vData2 欄位必須解釋如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="88b6c-597">**vData1**：小數點右邊的位數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="88b6c-598">必須在0到28的範圍內。</span><span class="sxs-lookup"><span data-stu-id="88b6c-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="88b6c-599">**vData2**：數位值的正負號。</span><span class="sxs-lookup"><span data-stu-id="88b6c-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="88b6c-600">如果是正數，則設定為0x00，如果是負數，則為0x80。</span><span class="sxs-lookup"><span data-stu-id="88b6c-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="88b6c-601">VValue 欄位的格式為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-601">The format of the vValue field is:</span></span>



<span data-ttu-id="88b6c-602">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-602">0</span></span>

<span data-ttu-id="88b6c-603">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-603">1</span></span>

<span data-ttu-id="88b6c-604">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-604">2</span></span>

<span data-ttu-id="88b6c-605">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-605">3</span></span>

<span data-ttu-id="88b6c-606">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-606">4</span></span>

<span data-ttu-id="88b6c-607">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-607">5</span></span>

<span data-ttu-id="88b6c-608">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-608">6</span></span>

<span data-ttu-id="88b6c-609">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-609">7</span></span>

<span data-ttu-id="88b6c-610">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-610">8</span></span>

<span data-ttu-id="88b6c-611">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-611">9</span></span>

<span data-ttu-id="88b6c-612">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-612">1</span></span><br/> <span data-ttu-id="88b6c-613">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-613">0</span></span><br/>

<span data-ttu-id="88b6c-614">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-614">1</span></span>

<span data-ttu-id="88b6c-615">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-615">2</span></span>

<span data-ttu-id="88b6c-616">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-616">3</span></span>

<span data-ttu-id="88b6c-617">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-617">4</span></span>

<span data-ttu-id="88b6c-618">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-618">5</span></span>

<span data-ttu-id="88b6c-619">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-619">6</span></span>

<span data-ttu-id="88b6c-620">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-620">7</span></span>

<span data-ttu-id="88b6c-621">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-621">8</span></span>

<span data-ttu-id="88b6c-622">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-622">9</span></span>

<span data-ttu-id="88b6c-623">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-623">2</span></span><br/> <span data-ttu-id="88b6c-624">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-624">0</span></span><br/>

<span data-ttu-id="88b6c-625">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-625">1</span></span>

<span data-ttu-id="88b6c-626">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-626">2</span></span>

<span data-ttu-id="88b6c-627">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-627">3</span></span>

<span data-ttu-id="88b6c-628">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-628">4</span></span>

<span data-ttu-id="88b6c-629">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-629">5</span></span>

<span data-ttu-id="88b6c-630">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-630">6</span></span>

<span data-ttu-id="88b6c-631">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-631">7</span></span>

<span data-ttu-id="88b6c-632">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-632">8</span></span>

<span data-ttu-id="88b6c-633">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-633">9</span></span>

<span data-ttu-id="88b6c-634">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-634">3</span></span><br/> <span data-ttu-id="88b6c-635">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-635">0</span></span><br/>

<span data-ttu-id="88b6c-636">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-636">1</span></span>

<span data-ttu-id="88b6c-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="88b6c-637">Hi32</span></span>

<span data-ttu-id="88b6c-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="88b6c-638">Lo32</span></span>

<span data-ttu-id="88b6c-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="88b6c-639">Mid32</span></span>



 

<span data-ttu-id="88b6c-640">**Hi32**：96位整數的最高32位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="88b6c-641">**Lo32**：96位整數的最低32位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="88b6c-642">**Mid32**：96位整數的中間32位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="88b6c-643">2.2.1.1.1.2 VT \_ 向量</span><span class="sxs-lookup"><span data-stu-id="88b6c-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="88b6c-644">VT \_ 向量用來傳遞一維陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="88b6c-645">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-645">0</span></span>

<span data-ttu-id="88b6c-646">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-646">1</span></span>

<span data-ttu-id="88b6c-647">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-647">2</span></span>

<span data-ttu-id="88b6c-648">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-648">3</span></span>

<span data-ttu-id="88b6c-649">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-649">4</span></span>

<span data-ttu-id="88b6c-650">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-650">5</span></span>

<span data-ttu-id="88b6c-651">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-651">6</span></span>

<span data-ttu-id="88b6c-652">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-652">7</span></span>

<span data-ttu-id="88b6c-653">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-653">8</span></span>

<span data-ttu-id="88b6c-654">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-654">9</span></span>

<span data-ttu-id="88b6c-655">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-655">1</span></span><br/> <span data-ttu-id="88b6c-656">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-656">0</span></span><br/>

<span data-ttu-id="88b6c-657">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-657">1</span></span>

<span data-ttu-id="88b6c-658">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-658">2</span></span>

<span data-ttu-id="88b6c-659">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-659">3</span></span>

<span data-ttu-id="88b6c-660">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-660">4</span></span>

<span data-ttu-id="88b6c-661">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-661">5</span></span>

<span data-ttu-id="88b6c-662">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-662">6</span></span>

<span data-ttu-id="88b6c-663">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-663">7</span></span>

<span data-ttu-id="88b6c-664">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-664">8</span></span>

<span data-ttu-id="88b6c-665">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-665">9</span></span>

<span data-ttu-id="88b6c-666">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-666">2</span></span><br/> <span data-ttu-id="88b6c-667">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-667">0</span></span><br/>

<span data-ttu-id="88b6c-668">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-668">1</span></span>

<span data-ttu-id="88b6c-669">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-669">2</span></span>

<span data-ttu-id="88b6c-670">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-670">3</span></span>

<span data-ttu-id="88b6c-671">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-671">4</span></span>

<span data-ttu-id="88b6c-672">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-672">5</span></span>

<span data-ttu-id="88b6c-673">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-673">6</span></span>

<span data-ttu-id="88b6c-674">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-674">7</span></span>

<span data-ttu-id="88b6c-675">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-675">8</span></span>

<span data-ttu-id="88b6c-676">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-676">9</span></span>

<span data-ttu-id="88b6c-677">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-677">3</span></span><br/> <span data-ttu-id="88b6c-678">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-678">0</span></span><br/>

<span data-ttu-id="88b6c-679">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-679">1</span></span>

<span data-ttu-id="88b6c-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="88b6c-680">vVectorElements</span></span>

<span data-ttu-id="88b6c-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="88b6c-681">vVectorData</span></span>



 

<span data-ttu-id="88b6c-682">**vVectorElements**：不帶正負號的32位整數，指出 vVectorData 欄位中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="88b6c-683">**vVectorData**：專案的陣列，其中包含已清除0x1000 位之 vType 所指出的型別。</span><span class="sxs-lookup"><span data-stu-id="88b6c-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="88b6c-684">您可以從固定長度的資料類型資料表取得個別固定長度專案的大小，如2.2.1.1 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="88b6c-685">這個欄位的長度（以位元組為單位）可以藉由將 vVectorElements 乘以個別專案的大小來計算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="88b6c-686">針對可變長度的資料類型，vVectorData 包含一連串連續封送處理的簡單類型，其中的類型是由 vType （已清除0x1000 位）所表示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="88b6c-687">這包括以 vType VT ARRAY VT VARIANT 表示的特殊案例 \_ \| \_ (例如 0x100C) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="88b6c-688">VVectorData 欄位中的元素必須以0到3個填補位元組分隔，讓每個專案從包含這個陣列的訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="88b6c-689">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="88b6c-690">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-691">如果 vType 設定為 VT \_ ARRAY \| vt \_ VARIANT，則此序列中的專案類型為 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="88b6c-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="88b6c-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="88b6c-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="88b6c-693">SAFEARRAY 用來傳遞多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="88b6c-694">結構包含陣列大小資訊，以及陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="88b6c-695">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-695">0</span></span>

<span data-ttu-id="88b6c-696">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-696">1</span></span>

<span data-ttu-id="88b6c-697">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-697">2</span></span>

<span data-ttu-id="88b6c-698">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-698">3</span></span>

<span data-ttu-id="88b6c-699">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-699">4</span></span>

<span data-ttu-id="88b6c-700">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-700">5</span></span>

<span data-ttu-id="88b6c-701">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-701">6</span></span>

<span data-ttu-id="88b6c-702">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-702">7</span></span>

<span data-ttu-id="88b6c-703">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-703">8</span></span>

<span data-ttu-id="88b6c-704">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-704">9</span></span>

<span data-ttu-id="88b6c-705">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-705">1</span></span><br/> <span data-ttu-id="88b6c-706">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-706">0</span></span><br/>

<span data-ttu-id="88b6c-707">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-707">1</span></span>

<span data-ttu-id="88b6c-708">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-708">2</span></span>

<span data-ttu-id="88b6c-709">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-709">3</span></span>

<span data-ttu-id="88b6c-710">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-710">4</span></span>

<span data-ttu-id="88b6c-711">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-711">5</span></span>

<span data-ttu-id="88b6c-712">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-712">6</span></span>

<span data-ttu-id="88b6c-713">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-713">7</span></span>

<span data-ttu-id="88b6c-714">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-714">8</span></span>

<span data-ttu-id="88b6c-715">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-715">9</span></span>

<span data-ttu-id="88b6c-716">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-716">2</span></span><br/> <span data-ttu-id="88b6c-717">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-717">0</span></span><br/>

<span data-ttu-id="88b6c-718">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-718">1</span></span>

<span data-ttu-id="88b6c-719">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-719">2</span></span>

<span data-ttu-id="88b6c-720">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-720">3</span></span>

<span data-ttu-id="88b6c-721">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-721">4</span></span>

<span data-ttu-id="88b6c-722">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-722">5</span></span>

<span data-ttu-id="88b6c-723">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-723">6</span></span>

<span data-ttu-id="88b6c-724">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-724">7</span></span>

<span data-ttu-id="88b6c-725">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-725">8</span></span>

<span data-ttu-id="88b6c-726">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-726">9</span></span>

<span data-ttu-id="88b6c-727">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-727">3</span></span><br/> <span data-ttu-id="88b6c-728">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-728">0</span></span><br/>

<span data-ttu-id="88b6c-729">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-729">1</span></span>

<span data-ttu-id="88b6c-730">cDims</span><span class="sxs-lookup"><span data-stu-id="88b6c-730">cDims</span></span>

<span data-ttu-id="88b6c-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="88b6c-731">fFeatures</span></span>

<span data-ttu-id="88b6c-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="88b6c-732">cbElements</span></span>

<span data-ttu-id="88b6c-733">Rgsabound (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-733">Rgsabound (variable)</span></span>

<span data-ttu-id="88b6c-734">vData (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-734">vData (variable)</span></span>



 

<span data-ttu-id="88b6c-735">**cDims**：不帶正負號的16位整數，表示多維陣列的維度數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="88b6c-736">**fFeatures**：16位位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="88b6c-737">這些值代表由上層應用程式定義的功能，必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-738">**cbElements**：32位不帶正負號的整數，指定陣列中每個元素的大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="88b6c-739">**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，此結構是在 SAFEARRAY 的每個維度的區段2.2.1.1.1.4 中指定的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="88b6c-740">這個陣列的第一個是最左邊的維度，最後是最右邊的維度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="88b6c-741">**vData**：特定類型之封送處理專案的向量，由包含 CBaseStorageVariant 的 vType 所表示，並已清除位0x2000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="88b6c-742">vData 的封送處理方式類似于 VT \_ 向量（如區段2.2.1.1.1.2 中所指定），差別在於專案數不會儲存在向量前方。</span><span class="sxs-lookup"><span data-stu-id="88b6c-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="88b6c-743">而是將 cElements 值乘以 Rgsabound 欄位中提供的所有安全陣列界限，來計算專案數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="88b6c-744">專案會以維度的順序儲存在向量中，並以最右邊的維度開始反覆運算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="88b6c-745">下圖以視覺方式呈現二維陣列範例。</span><span class="sxs-lookup"><span data-stu-id="88b6c-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="88b6c-746">第一個維度的 cElements 等於 4 (水準表示) ，而 lLbound 等於0，而第二個維度的 cElements 等於 2 (表示垂直) ，lLbound 等於0。</span><span class="sxs-lookup"><span data-stu-id="88b6c-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="88b6c-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="88b6c-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="88b6c-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="88b6c-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="88b6c-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="88b6c-751">：： row：：：</span><span class="sxs-lookup"><span data-stu-id="88b6c-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="88b6c-752">使用上圖，vData 將包含下列順序：0x00000001、0x00000007、0x00000002、0x00000011、0x00000003、0x00000013、0x00000005、0x00000017 (先逐一查看最右邊的維度，然後再遞增下一個維度) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="88b6c-753">上述 Rgsabound (會記錄 cElements 和 Lbound) 為：0x00000004、0x00000000、0x00000002、0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="88b6c-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="88b6c-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="88b6c-755">SAFEARRAYBOUND 結構代表 SAFEARRAY 或 SAFEARRAY2 之一維度的範圍。</span><span class="sxs-lookup"><span data-stu-id="88b6c-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="88b6c-756">其格式為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-756">Its format is:</span></span>



<span data-ttu-id="88b6c-757">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-757">0</span></span>

<span data-ttu-id="88b6c-758">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-758">1</span></span>

<span data-ttu-id="88b6c-759">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-759">2</span></span>

<span data-ttu-id="88b6c-760">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-760">3</span></span>

<span data-ttu-id="88b6c-761">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-761">4</span></span>

<span data-ttu-id="88b6c-762">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-762">5</span></span>

<span data-ttu-id="88b6c-763">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-763">6</span></span>

<span data-ttu-id="88b6c-764">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-764">7</span></span>

<span data-ttu-id="88b6c-765">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-765">8</span></span>

<span data-ttu-id="88b6c-766">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-766">9</span></span>

<span data-ttu-id="88b6c-767">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-767">1</span></span><br/> <span data-ttu-id="88b6c-768">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-768">0</span></span><br/>

<span data-ttu-id="88b6c-769">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-769">1</span></span>

<span data-ttu-id="88b6c-770">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-770">2</span></span>

<span data-ttu-id="88b6c-771">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-771">3</span></span>

<span data-ttu-id="88b6c-772">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-772">4</span></span>

<span data-ttu-id="88b6c-773">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-773">5</span></span>

<span data-ttu-id="88b6c-774">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-774">6</span></span>

<span data-ttu-id="88b6c-775">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-775">7</span></span>

<span data-ttu-id="88b6c-776">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-776">8</span></span>

<span data-ttu-id="88b6c-777">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-777">9</span></span>

<span data-ttu-id="88b6c-778">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-778">2</span></span><br/> <span data-ttu-id="88b6c-779">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-779">0</span></span><br/>

<span data-ttu-id="88b6c-780">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-780">1</span></span>

<span data-ttu-id="88b6c-781">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-781">2</span></span>

<span data-ttu-id="88b6c-782">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-782">3</span></span>

<span data-ttu-id="88b6c-783">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-783">4</span></span>

<span data-ttu-id="88b6c-784">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-784">5</span></span>

<span data-ttu-id="88b6c-785">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-785">6</span></span>

<span data-ttu-id="88b6c-786">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-786">7</span></span>

<span data-ttu-id="88b6c-787">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-787">8</span></span>

<span data-ttu-id="88b6c-788">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-788">9</span></span>

<span data-ttu-id="88b6c-789">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-789">3</span></span><br/> <span data-ttu-id="88b6c-790">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-790">0</span></span><br/>

<span data-ttu-id="88b6c-791">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-791">1</span></span>

<span data-ttu-id="88b6c-792">cElements</span><span class="sxs-lookup"><span data-stu-id="88b6c-792">cElements</span></span>

<span data-ttu-id="88b6c-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="88b6c-793">lLbound</span></span>



 

<span data-ttu-id="88b6c-794">**cElements**：32位不帶正負號的整數，指定維度中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="88b6c-795">**lLbound**：32位不帶正負號的整數，指定維度的下限。</span><span class="sxs-lookup"><span data-stu-id="88b6c-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="88b6c-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="88b6c-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="88b6c-797">SAFEARRAY2 用來傳遞 SERIALIZEDPROPERTYVALUE 中的多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="88b6c-798">結構包含界限資訊和資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="88b6c-799">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-799">0</span></span>

<span data-ttu-id="88b6c-800">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-800">1</span></span>

<span data-ttu-id="88b6c-801">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-801">2</span></span>

<span data-ttu-id="88b6c-802">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-802">3</span></span>

<span data-ttu-id="88b6c-803">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-803">4</span></span>

<span data-ttu-id="88b6c-804">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-804">5</span></span>

<span data-ttu-id="88b6c-805">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-805">6</span></span>

<span data-ttu-id="88b6c-806">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-806">7</span></span>

<span data-ttu-id="88b6c-807">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-807">8</span></span>

<span data-ttu-id="88b6c-808">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-808">9</span></span>

<span data-ttu-id="88b6c-809">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-809">1</span></span><br/> <span data-ttu-id="88b6c-810">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-810">0</span></span><br/>

<span data-ttu-id="88b6c-811">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-811">1</span></span>

<span data-ttu-id="88b6c-812">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-812">2</span></span>

<span data-ttu-id="88b6c-813">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-813">3</span></span>

<span data-ttu-id="88b6c-814">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-814">4</span></span>

<span data-ttu-id="88b6c-815">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-815">5</span></span>

<span data-ttu-id="88b6c-816">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-816">6</span></span>

<span data-ttu-id="88b6c-817">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-817">7</span></span>

<span data-ttu-id="88b6c-818">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-818">8</span></span>

<span data-ttu-id="88b6c-819">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-819">9</span></span>

<span data-ttu-id="88b6c-820">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-820">2</span></span><br/> <span data-ttu-id="88b6c-821">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-821">0</span></span><br/>

<span data-ttu-id="88b6c-822">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-822">1</span></span>

<span data-ttu-id="88b6c-823">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-823">2</span></span>

<span data-ttu-id="88b6c-824">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-824">3</span></span>

<span data-ttu-id="88b6c-825">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-825">4</span></span>

<span data-ttu-id="88b6c-826">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-826">5</span></span>

<span data-ttu-id="88b6c-827">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-827">6</span></span>

<span data-ttu-id="88b6c-828">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-828">7</span></span>

<span data-ttu-id="88b6c-829">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-829">8</span></span>

<span data-ttu-id="88b6c-830">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-830">9</span></span>

<span data-ttu-id="88b6c-831">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-831">3</span></span><br/> <span data-ttu-id="88b6c-832">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-832">0</span></span><br/>

<span data-ttu-id="88b6c-833">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-833">1</span></span>

<span data-ttu-id="88b6c-834">cDims</span><span class="sxs-lookup"><span data-stu-id="88b6c-834">cDims</span></span>

<span data-ttu-id="88b6c-835">Rgsabound (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-835">Rgsabound (variable)</span></span>

<span data-ttu-id="88b6c-836">vData (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-836">vData (variable)</span></span>



 

<span data-ttu-id="88b6c-837">**cDims**：不帶正負號的32位整數，表示 SAFEARRAY2 的維度數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="88b6c-838">**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，如 SAFEARRAY2 中每個維度的區段2.2.1.1.1.4 所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="88b6c-839">這個陣列的第一個是最左邊的維度，最後是最右邊的維度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="88b6c-840">**vData**：特定類型之封送處理專案的向量，由包含 SERIALIZEDPROPERTYVALUE 的 dwType 所表示，並已清除位0x2000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="88b6c-841">VData 的格式與在區段2.2.1.1.1.3 中針對 SAFEARRAY 的 vData 欄位指定的格式相同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="88b6c-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="88b6c-843">CFullPropSpec 結構包含屬性集 GUID 和屬性識別碼，可唯一識別屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="88b6c-844">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-844">0</span></span>

<span data-ttu-id="88b6c-845">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-845">1</span></span>

<span data-ttu-id="88b6c-846">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-846">2</span></span>

<span data-ttu-id="88b6c-847">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-847">3</span></span>

<span data-ttu-id="88b6c-848">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-848">4</span></span>

<span data-ttu-id="88b6c-849">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-849">5</span></span>

<span data-ttu-id="88b6c-850">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-850">6</span></span>

<span data-ttu-id="88b6c-851">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-851">7</span></span>

<span data-ttu-id="88b6c-852">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-852">8</span></span>

<span data-ttu-id="88b6c-853">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-853">9</span></span>

<span data-ttu-id="88b6c-854">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-854">1</span></span><br/> <span data-ttu-id="88b6c-855">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-855">0</span></span><br/>

<span data-ttu-id="88b6c-856">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-856">1</span></span>

<span data-ttu-id="88b6c-857">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-857">2</span></span>

<span data-ttu-id="88b6c-858">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-858">3</span></span>

<span data-ttu-id="88b6c-859">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-859">4</span></span>

<span data-ttu-id="88b6c-860">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-860">5</span></span>

<span data-ttu-id="88b6c-861">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-861">6</span></span>

<span data-ttu-id="88b6c-862">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-862">7</span></span>

<span data-ttu-id="88b6c-863">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-863">8</span></span>

<span data-ttu-id="88b6c-864">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-864">9</span></span>

<span data-ttu-id="88b6c-865">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-865">2</span></span><br/> <span data-ttu-id="88b6c-866">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-866">0</span></span><br/>

<span data-ttu-id="88b6c-867">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-867">1</span></span>

<span data-ttu-id="88b6c-868">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-868">2</span></span>

<span data-ttu-id="88b6c-869">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-869">3</span></span>

<span data-ttu-id="88b6c-870">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-870">4</span></span>

<span data-ttu-id="88b6c-871">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-871">5</span></span>

<span data-ttu-id="88b6c-872">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-872">6</span></span>

<span data-ttu-id="88b6c-873">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-873">7</span></span>

<span data-ttu-id="88b6c-874">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-874">8</span></span>

<span data-ttu-id="88b6c-875">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-875">9</span></span>

<span data-ttu-id="88b6c-876">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-876">3</span></span><br/> <span data-ttu-id="88b6c-877">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-877">0</span></span><br/>

<span data-ttu-id="88b6c-878">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-878">1</span></span>

<span data-ttu-id="88b6c-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-879">\_guidPropSet</span></span>

<span data-ttu-id="88b6c-880">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-880">...</span></span>

<span data-ttu-id="88b6c-881">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-881">...</span></span>

<span data-ttu-id="88b6c-882">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-882">...</span></span>

<span data-ttu-id="88b6c-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="88b6c-883">ulKind</span></span>

<span data-ttu-id="88b6c-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-884">PrSpec</span></span>

<span data-ttu-id="88b6c-885">屬性名稱 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-885">Property name (variable)</span></span>



 

<span data-ttu-id="88b6c-886">**\_ guidPropSet**：屬性所屬之屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="88b6c-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="88b6c-887">**ulKind**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-888">下列其中一個值，表示 PrSpec 的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="88b6c-889">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-889">Value</span></span>                                            | <span data-ttu-id="88b6c-890">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-891">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="88b6c-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="88b6c-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-892">0x00000000</span></span><br/> | <span data-ttu-id="88b6c-893">PrSpec 欄位會指定 [屬性名稱] 欄位中的非 Null 字元數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="88b6c-894">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="88b6c-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="88b6c-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-895">0x00000001</span></span><br/>  | <span data-ttu-id="88b6c-896">PrSpec 欄位會指定屬性識別碼 (PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="88b6c-897">**PrSpec**：具有意義的32位不帶正負號整數，如 ulKind 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="88b6c-898">**屬性名稱**：如果 ulKind 設為 PRSPEC \_ PROPID，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="88b6c-899">如果 ulKind 設定為 PRSPEC \_ LPWSTR，則這個欄位必須包含 PRSPEC 非 Null Unicode 字元的不區分大小寫陣列，其中包含屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="88b6c-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="88b6c-901">CContentRestriction 結構包含要與屬性快取中的屬性相符的字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="88b6c-902">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-902">0</span></span>

<span data-ttu-id="88b6c-903">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-903">1</span></span>

<span data-ttu-id="88b6c-904">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-904">2</span></span>

<span data-ttu-id="88b6c-905">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-905">3</span></span>

<span data-ttu-id="88b6c-906">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-906">4</span></span>

<span data-ttu-id="88b6c-907">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-907">5</span></span>

<span data-ttu-id="88b6c-908">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-908">6</span></span>

<span data-ttu-id="88b6c-909">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-909">7</span></span>

<span data-ttu-id="88b6c-910">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-910">8</span></span>

<span data-ttu-id="88b6c-911">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-911">9</span></span>

<span data-ttu-id="88b6c-912">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-912">1</span></span><br/> <span data-ttu-id="88b6c-913">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-913">0</span></span><br/>

<span data-ttu-id="88b6c-914">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-914">1</span></span>

<span data-ttu-id="88b6c-915">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-915">2</span></span>

<span data-ttu-id="88b6c-916">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-916">3</span></span>

<span data-ttu-id="88b6c-917">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-917">4</span></span>

<span data-ttu-id="88b6c-918">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-918">5</span></span>

<span data-ttu-id="88b6c-919">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-919">6</span></span>

<span data-ttu-id="88b6c-920">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-920">7</span></span>

<span data-ttu-id="88b6c-921">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-921">8</span></span>

<span data-ttu-id="88b6c-922">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-922">9</span></span>

<span data-ttu-id="88b6c-923">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-923">2</span></span><br/> <span data-ttu-id="88b6c-924">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-924">0</span></span><br/>

<span data-ttu-id="88b6c-925">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-925">1</span></span>

<span data-ttu-id="88b6c-926">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-926">2</span></span>

<span data-ttu-id="88b6c-927">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-927">3</span></span>

<span data-ttu-id="88b6c-928">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-928">4</span></span>

<span data-ttu-id="88b6c-929">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-929">5</span></span>

<span data-ttu-id="88b6c-930">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-930">6</span></span>

<span data-ttu-id="88b6c-931">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-931">7</span></span>

<span data-ttu-id="88b6c-932">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-932">8</span></span>

<span data-ttu-id="88b6c-933">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-933">9</span></span>

<span data-ttu-id="88b6c-934">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-934">3</span></span><br/> <span data-ttu-id="88b6c-935">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-935">0</span></span><br/>

<span data-ttu-id="88b6c-936">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-936">1</span></span>

<span data-ttu-id="88b6c-937">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-937">\_Property (variable)</span></span>

<span data-ttu-id="88b6c-938">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-938">...</span></span>

<span data-ttu-id="88b6c-939">Padding1 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-939">Padding1 (variable)</span></span>

<span data-ttu-id="88b6c-940">副本</span><span class="sxs-lookup"><span data-stu-id="88b6c-940">Cc</span></span>

<span data-ttu-id="88b6c-941">\_pwcsPhrase (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="88b6c-942">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-942">...</span></span>

<span data-ttu-id="88b6c-943">Padding2 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-943">Padding2 (variable)</span></span>

<span data-ttu-id="88b6c-944">lcid</span><span class="sxs-lookup"><span data-stu-id="88b6c-944">lcid</span></span>

<span data-ttu-id="88b6c-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="88b6c-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="88b6c-946">**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.2 中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="88b6c-947">這個欄位指出要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="88b6c-948">**Padding1**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-949">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-950">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-951">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-952">**Cc**：32位不帶正負號的整數，指定 pwcsPhrase 欄位中的字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="88b6c-953">**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="88b6c-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="88b6c-954">此欄位不得為空白。</span><span class="sxs-lookup"><span data-stu-id="88b6c-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="88b6c-955">Cc 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="88b6c-956">**Padding2**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-957">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-958">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-959">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-960">**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="88b6c-961">**\_ ulGenerateMethod**：32位不帶正負號的整數，指定產生替代字表單時要使用的方法</span><span class="sxs-lookup"><span data-stu-id="88b6c-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="88b6c-962">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-962">Value</span></span>                                                       | <span data-ttu-id="88b6c-963">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-964">產生 \_ 精確的方法 \_</span><span class="sxs-lookup"><span data-stu-id="88b6c-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="88b6c-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-965">0x00000000</span></span><br/>    | <span data-ttu-id="88b6c-966">完全相符。</span><span class="sxs-lookup"><span data-stu-id="88b6c-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="88b6c-967">產生 \_ 方法 \_ 前置詞</span><span class="sxs-lookup"><span data-stu-id="88b6c-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="88b6c-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-968">0x00000001</span></span> <br/>  | <span data-ttu-id="88b6c-969">前置詞相符。</span><span class="sxs-lookup"><span data-stu-id="88b6c-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="88b6c-970">產生 \_ 方法 \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="88b6c-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="88b6c-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-971">0x00000002</span></span><br/> | <span data-ttu-id="88b6c-972">符合單字的 inflections。</span><span class="sxs-lookup"><span data-stu-id="88b6c-972">Matches inflections of a word.</span></span> <span data-ttu-id="88b6c-973">單字的變化是已根據指定語言的語言規則修改過的相同語音部分中的根字組變數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="88b6c-974">例如，以英文的動詞「泳道」（inflections）包含「泳道」、「游泳」、「游泳」和「swam」。</span><span class="sxs-lookup"><span data-stu-id="88b6c-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="88b6c-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="88b6c-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="88b6c-976">CKey 結構包含屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="88b6c-977">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-977">0</span></span>

<span data-ttu-id="88b6c-978">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-978">1</span></span>

<span data-ttu-id="88b6c-979">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-979">2</span></span>

<span data-ttu-id="88b6c-980">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-980">3</span></span>

<span data-ttu-id="88b6c-981">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-981">4</span></span>

<span data-ttu-id="88b6c-982">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-982">5</span></span>

<span data-ttu-id="88b6c-983">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-983">6</span></span>

<span data-ttu-id="88b6c-984">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-984">7</span></span>

<span data-ttu-id="88b6c-985">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-985">8</span></span>

<span data-ttu-id="88b6c-986">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-986">9</span></span>

<span data-ttu-id="88b6c-987">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-987">1</span></span><br/> <span data-ttu-id="88b6c-988">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-988">0</span></span><br/>

<span data-ttu-id="88b6c-989">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-989">1</span></span>

<span data-ttu-id="88b6c-990">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-990">2</span></span>

<span data-ttu-id="88b6c-991">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-991">3</span></span>

<span data-ttu-id="88b6c-992">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-992">4</span></span>

<span data-ttu-id="88b6c-993">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-993">5</span></span>

<span data-ttu-id="88b6c-994">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-994">6</span></span>

<span data-ttu-id="88b6c-995">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-995">7</span></span>

<span data-ttu-id="88b6c-996">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-996">8</span></span>

<span data-ttu-id="88b6c-997">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-997">9</span></span>

<span data-ttu-id="88b6c-998">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-998">2</span></span><br/> <span data-ttu-id="88b6c-999">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-999">0</span></span><br/>

<span data-ttu-id="88b6c-1000">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1000">1</span></span>

<span data-ttu-id="88b6c-1001">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1001">2</span></span>

<span data-ttu-id="88b6c-1002">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1002">3</span></span>

<span data-ttu-id="88b6c-1003">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1003">4</span></span>

<span data-ttu-id="88b6c-1004">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1004">5</span></span>

<span data-ttu-id="88b6c-1005">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1005">6</span></span>

<span data-ttu-id="88b6c-1006">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1006">7</span></span>

<span data-ttu-id="88b6c-1007">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1007">8</span></span>

<span data-ttu-id="88b6c-1008">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1008">9</span></span>

<span data-ttu-id="88b6c-1009">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1009">3</span></span><br/> <span data-ttu-id="88b6c-1010">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1010">0</span></span><br/>

<span data-ttu-id="88b6c-1011">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1011">1</span></span>

<span data-ttu-id="88b6c-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="88b6c-1012">PROPID</span></span>

<span data-ttu-id="88b6c-1013">Cb</span><span class="sxs-lookup"><span data-stu-id="88b6c-1013">Cb</span></span>

<span data-ttu-id="88b6c-1014">buf (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1014">buf (variable)</span></span>



 

<span data-ttu-id="88b6c-1015">**PROPID**：32位不帶正負號的整數，表示如1.8.1 小節中所討論的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="88b6c-1016">已知的值為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-1016">Well-known values are:</span></span>



| <span data-ttu-id="88b6c-1017">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1017">Value</span></span>      | <span data-ttu-id="88b6c-1018">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="88b6c-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="88b6c-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="88b6c-1020">代表不正確屬性識別碼，不可使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="88b6c-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="88b6c-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="88b6c-1022">代表不正確屬性識別碼，不可使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="88b6c-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1023">0x00000000</span></span> | <span data-ttu-id="88b6c-1024">表示任何屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="88b6c-1025">**Cb**：32位不帶正負號的整數，其中包含 buf 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="88b6c-1026">**buf**：代表屬性值的位元組序列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="88b6c-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="88b6c-1028">CInternalPropertyRestriction 結構包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="88b6c-1029">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1029">0</span></span>

<span data-ttu-id="88b6c-1030">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1030">1</span></span>

<span data-ttu-id="88b6c-1031">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1031">2</span></span>

<span data-ttu-id="88b6c-1032">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1032">3</span></span>

<span data-ttu-id="88b6c-1033">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1033">4</span></span>

<span data-ttu-id="88b6c-1034">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1034">5</span></span>

<span data-ttu-id="88b6c-1035">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1035">6</span></span>

<span data-ttu-id="88b6c-1036">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1036">7</span></span>

<span data-ttu-id="88b6c-1037">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1037">8</span></span>

<span data-ttu-id="88b6c-1038">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1038">9</span></span>

<span data-ttu-id="88b6c-1039">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1039">1</span></span><br/> <span data-ttu-id="88b6c-1040">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1040">0</span></span><br/>

<span data-ttu-id="88b6c-1041">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1041">1</span></span>

<span data-ttu-id="88b6c-1042">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1042">2</span></span>

<span data-ttu-id="88b6c-1043">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1043">3</span></span>

<span data-ttu-id="88b6c-1044">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1044">4</span></span>

<span data-ttu-id="88b6c-1045">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1045">5</span></span>

<span data-ttu-id="88b6c-1046">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1046">6</span></span>

<span data-ttu-id="88b6c-1047">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1047">7</span></span>

<span data-ttu-id="88b6c-1048">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1048">8</span></span>

<span data-ttu-id="88b6c-1049">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1049">9</span></span>

<span data-ttu-id="88b6c-1050">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1050">2</span></span><br/> <span data-ttu-id="88b6c-1051">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1051">0</span></span><br/>

<span data-ttu-id="88b6c-1052">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1052">1</span></span>

<span data-ttu-id="88b6c-1053">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1053">2</span></span>

<span data-ttu-id="88b6c-1054">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1054">3</span></span>

<span data-ttu-id="88b6c-1055">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1055">4</span></span>

<span data-ttu-id="88b6c-1056">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1056">5</span></span>

<span data-ttu-id="88b6c-1057">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1057">6</span></span>

<span data-ttu-id="88b6c-1058">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1058">7</span></span>

<span data-ttu-id="88b6c-1059">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1059">8</span></span>

<span data-ttu-id="88b6c-1060">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1060">9</span></span>

<span data-ttu-id="88b6c-1061">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1061">3</span></span><br/> <span data-ttu-id="88b6c-1062">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1062">0</span></span><br/>

<span data-ttu-id="88b6c-1063">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1063">1</span></span>

<span data-ttu-id="88b6c-1064">\_relop</span><span class="sxs-lookup"><span data-stu-id="88b6c-1064">\_relop</span></span>

<span data-ttu-id="88b6c-1065">\_pid</span><span class="sxs-lookup"><span data-stu-id="88b6c-1065">\_pid</span></span>

<span data-ttu-id="88b6c-1066">\_prval (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1066">\_prval (variable)</span></span>

<span data-ttu-id="88b6c-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="88b6c-1067">restrictionPresent</span></span>

<span data-ttu-id="88b6c-1068">nextRestriction (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="88b6c-1069">**\_ relop**：32位整數，指定要在屬性上執行的關聯性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="88b6c-1070">必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="88b6c-1071">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1071">Value</span></span>                 | <span data-ttu-id="88b6c-1072">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1073">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="88b6c-1074">小於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1075">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="88b6c-1076">小於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="88b6c-1077">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="88b6c-1078">大於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="88b6c-1079">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="88b6c-1080">大於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="88b6c-1081">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="88b6c-1082">相等比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1083">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="88b6c-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="88b6c-1084">不相等的比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1085">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="88b6c-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="88b6c-1086">正則運算式比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="88b6c-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="88b6c-1088">傳回右運算元的位 AND。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="88b6c-1089">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="88b6c-1090">傳回非零值的位 AND。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="88b6c-1091">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="88b6c-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="88b6c-1092">作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="88b6c-1093">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="88b6c-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="88b6c-1094">作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="88b6c-1095">**\_ pid**：32位不帶正負號的整數，代表屬性識別碼 (請參閱2.2.1.4 一節中的 PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="88b6c-1096">**\_ prval**：包含與屬性相關之值的 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="88b6c-1097">**restrictionPresent**：指出 nextRestriction 欄位是否存在的位元組值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="88b6c-1098">必須設定為0x00 或0x01。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="88b6c-1099">如果設定為0x01，restrictionPresent 會指出 nextRestriction 欄位存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="88b6c-1100">如果設定為0x00，restrictionPresent 會指出 nextRestriction 欄位不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="88b6c-1101">**nextRestriction**： CRestriction 結構，如2.2.1.16 一節中所指定，指定進一步的限制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="88b6c-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="88b6c-1103">CNatLanguageRestriction 結構包含屬性的 **自然語言查詢** 相符項。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="88b6c-1104">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1104">0</span></span>

<span data-ttu-id="88b6c-1105">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1105">1</span></span>

<span data-ttu-id="88b6c-1106">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1106">2</span></span>

<span data-ttu-id="88b6c-1107">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1107">3</span></span>

<span data-ttu-id="88b6c-1108">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1108">4</span></span>

<span data-ttu-id="88b6c-1109">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1109">5</span></span>

<span data-ttu-id="88b6c-1110">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1110">6</span></span>

<span data-ttu-id="88b6c-1111">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1111">7</span></span>

<span data-ttu-id="88b6c-1112">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1112">8</span></span>

<span data-ttu-id="88b6c-1113">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1113">9</span></span>

<span data-ttu-id="88b6c-1114">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1114">1</span></span><br/> <span data-ttu-id="88b6c-1115">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1115">0</span></span><br/>

<span data-ttu-id="88b6c-1116">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1116">1</span></span>

<span data-ttu-id="88b6c-1117">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1117">2</span></span>

<span data-ttu-id="88b6c-1118">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1118">3</span></span>

<span data-ttu-id="88b6c-1119">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1119">4</span></span>

<span data-ttu-id="88b6c-1120">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1120">5</span></span>

<span data-ttu-id="88b6c-1121">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1121">6</span></span>

<span data-ttu-id="88b6c-1122">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1122">7</span></span>

<span data-ttu-id="88b6c-1123">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1123">8</span></span>

<span data-ttu-id="88b6c-1124">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1124">9</span></span>

<span data-ttu-id="88b6c-1125">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1125">2</span></span><br/> <span data-ttu-id="88b6c-1126">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1126">0</span></span><br/>

<span data-ttu-id="88b6c-1127">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1127">1</span></span>

<span data-ttu-id="88b6c-1128">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1128">2</span></span>

<span data-ttu-id="88b6c-1129">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1129">3</span></span>

<span data-ttu-id="88b6c-1130">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1130">4</span></span>

<span data-ttu-id="88b6c-1131">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1131">5</span></span>

<span data-ttu-id="88b6c-1132">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1132">6</span></span>

<span data-ttu-id="88b6c-1133">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1133">7</span></span>

<span data-ttu-id="88b6c-1134">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1134">8</span></span>

<span data-ttu-id="88b6c-1135">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1135">9</span></span>

<span data-ttu-id="88b6c-1136">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1136">3</span></span><br/> <span data-ttu-id="88b6c-1137">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1137">0</span></span><br/>

<span data-ttu-id="88b6c-1138">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1138">1</span></span>

<span data-ttu-id="88b6c-1139">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1139">\_Property (variable)</span></span>

<span data-ttu-id="88b6c-1140">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1140">...</span></span>

<span data-ttu-id="88b6c-1141">\_填補 \_ cc (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="88b6c-1142">副本</span><span class="sxs-lookup"><span data-stu-id="88b6c-1142">Cc</span></span>

<span data-ttu-id="88b6c-1143">\_pwcsPhrase (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="88b6c-1144">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1144">...</span></span>

<span data-ttu-id="88b6c-1145">\_填補 \_ lcid (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="88b6c-1146">Lcid</span><span class="sxs-lookup"><span data-stu-id="88b6c-1146">Lcid</span></span>



 

<span data-ttu-id="88b6c-1147">**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.3 中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="88b6c-1148">這個欄位指出要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="88b6c-1149">**\_ 填補 \_** 副本：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-1150">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-1151">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-1152">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-1153">**Cc**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1154">PwcsPhrase 欄位中的字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="88b6c-1155">**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="88b6c-1156">不得為空白。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1156">MUST NOT be empty.</span></span> <span data-ttu-id="88b6c-1157">Cc 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="88b6c-1158">**\_ 填補 \_ lcid**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-1159">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-1160">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-1161">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-1162">**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="88b6c-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="88b6c-1164">CNodeRestriction 結構包含指定查詢限制的 **命令樹** 節點陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="88b6c-1165">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1165">0</span></span>

<span data-ttu-id="88b6c-1166">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1166">1</span></span>

<span data-ttu-id="88b6c-1167">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1167">2</span></span>

<span data-ttu-id="88b6c-1168">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1168">3</span></span>

<span data-ttu-id="88b6c-1169">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1169">4</span></span>

<span data-ttu-id="88b6c-1170">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1170">5</span></span>

<span data-ttu-id="88b6c-1171">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1171">6</span></span>

<span data-ttu-id="88b6c-1172">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1172">7</span></span>

<span data-ttu-id="88b6c-1173">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1173">8</span></span>

<span data-ttu-id="88b6c-1174">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1174">9</span></span>

<span data-ttu-id="88b6c-1175">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1175">1</span></span><br/> <span data-ttu-id="88b6c-1176">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1176">0</span></span><br/>

<span data-ttu-id="88b6c-1177">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1177">1</span></span>

<span data-ttu-id="88b6c-1178">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1178">2</span></span>

<span data-ttu-id="88b6c-1179">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1179">3</span></span>

<span data-ttu-id="88b6c-1180">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1180">4</span></span>

<span data-ttu-id="88b6c-1181">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1181">5</span></span>

<span data-ttu-id="88b6c-1182">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1182">6</span></span>

<span data-ttu-id="88b6c-1183">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1183">7</span></span>

<span data-ttu-id="88b6c-1184">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1184">8</span></span>

<span data-ttu-id="88b6c-1185">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1185">9</span></span>

<span data-ttu-id="88b6c-1186">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1186">2</span></span><br/> <span data-ttu-id="88b6c-1187">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1187">0</span></span><br/>

<span data-ttu-id="88b6c-1188">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1188">1</span></span>

<span data-ttu-id="88b6c-1189">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1189">2</span></span>

<span data-ttu-id="88b6c-1190">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1190">3</span></span>

<span data-ttu-id="88b6c-1191">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1191">4</span></span>

<span data-ttu-id="88b6c-1192">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1192">5</span></span>

<span data-ttu-id="88b6c-1193">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1193">6</span></span>

<span data-ttu-id="88b6c-1194">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1194">7</span></span>

<span data-ttu-id="88b6c-1195">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1195">8</span></span>

<span data-ttu-id="88b6c-1196">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1196">9</span></span>

<span data-ttu-id="88b6c-1197">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1197">3</span></span><br/> <span data-ttu-id="88b6c-1198">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1198">0</span></span><br/>

<span data-ttu-id="88b6c-1199">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1199">1</span></span>

<span data-ttu-id="88b6c-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="88b6c-1200">\_cNode</span></span>

<span data-ttu-id="88b6c-1201">\_paNode (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="88b6c-1202">**\_ cNode**：32位不帶正負號的整數，指定 paNode 欄位中包含的 CRestriction 結構數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="88b6c-1203">**\_ PaNode**： CRestriction 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="88b6c-1204">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="88b6c-1205">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="88b6c-1206">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="88b6c-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="88b6c-1208">COccRestriction 結構包含單字在片語中的位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="88b6c-1209">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1209">0</span></span>

<span data-ttu-id="88b6c-1210">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1210">1</span></span>

<span data-ttu-id="88b6c-1211">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1211">2</span></span>

<span data-ttu-id="88b6c-1212">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1212">3</span></span>

<span data-ttu-id="88b6c-1213">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1213">4</span></span>

<span data-ttu-id="88b6c-1214">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1214">5</span></span>

<span data-ttu-id="88b6c-1215">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1215">6</span></span>

<span data-ttu-id="88b6c-1216">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1216">7</span></span>

<span data-ttu-id="88b6c-1217">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1217">8</span></span>

<span data-ttu-id="88b6c-1218">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1218">9</span></span>

<span data-ttu-id="88b6c-1219">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1219">1</span></span><br/> <span data-ttu-id="88b6c-1220">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1220">0</span></span><br/>

<span data-ttu-id="88b6c-1221">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1221">1</span></span>

<span data-ttu-id="88b6c-1222">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1222">2</span></span>

<span data-ttu-id="88b6c-1223">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1223">3</span></span>

<span data-ttu-id="88b6c-1224">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1224">4</span></span>

<span data-ttu-id="88b6c-1225">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1225">5</span></span>

<span data-ttu-id="88b6c-1226">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1226">6</span></span>

<span data-ttu-id="88b6c-1227">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1227">7</span></span>

<span data-ttu-id="88b6c-1228">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1228">8</span></span>

<span data-ttu-id="88b6c-1229">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1229">9</span></span>

<span data-ttu-id="88b6c-1230">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1230">2</span></span><br/> <span data-ttu-id="88b6c-1231">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1231">0</span></span><br/>

<span data-ttu-id="88b6c-1232">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1232">1</span></span>

<span data-ttu-id="88b6c-1233">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1233">2</span></span>

<span data-ttu-id="88b6c-1234">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1234">3</span></span>

<span data-ttu-id="88b6c-1235">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1235">4</span></span>

<span data-ttu-id="88b6c-1236">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1236">5</span></span>

<span data-ttu-id="88b6c-1237">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1237">6</span></span>

<span data-ttu-id="88b6c-1238">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1238">7</span></span>

<span data-ttu-id="88b6c-1239">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1239">8</span></span>

<span data-ttu-id="88b6c-1240">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1240">9</span></span>

<span data-ttu-id="88b6c-1241">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1241">3</span></span><br/> <span data-ttu-id="88b6c-1242">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1242">0</span></span><br/>

<span data-ttu-id="88b6c-1243">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1243">1</span></span>

<span data-ttu-id="88b6c-1244">\_Occ</span><span class="sxs-lookup"><span data-stu-id="88b6c-1244">\_occ</span></span>

<span data-ttu-id="88b6c-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="88b6c-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="88b6c-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="88b6c-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="88b6c-1247">**\_ occ**：32位不帶正負號的整數，指定查詢字串中的單字位移（以單字為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="88b6c-1248">此規格中使用的單字是具有意義的任何地區設定中的語言單位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="88b6c-1249">**\_ cPrevNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中前一個單字之間出現的非搜尋 **字** 數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="88b6c-1250">**\_ cNextNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中下一個單字之間出現的非搜尋字數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="88b6c-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="88b6c-1252">CPropertyRestriction 結構包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="88b6c-1253">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1253">0</span></span>

<span data-ttu-id="88b6c-1254">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1254">1</span></span>

<span data-ttu-id="88b6c-1255">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1255">2</span></span>

<span data-ttu-id="88b6c-1256">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1256">3</span></span>

<span data-ttu-id="88b6c-1257">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1257">4</span></span>

<span data-ttu-id="88b6c-1258">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1258">5</span></span>

<span data-ttu-id="88b6c-1259">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1259">6</span></span>

<span data-ttu-id="88b6c-1260">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1260">7</span></span>

<span data-ttu-id="88b6c-1261">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1261">8</span></span>

<span data-ttu-id="88b6c-1262">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1262">9</span></span>

<span data-ttu-id="88b6c-1263">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1263">1</span></span><br/> <span data-ttu-id="88b6c-1264">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1264">0</span></span><br/>

<span data-ttu-id="88b6c-1265">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1265">1</span></span>

<span data-ttu-id="88b6c-1266">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1266">2</span></span>

<span data-ttu-id="88b6c-1267">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1267">3</span></span>

<span data-ttu-id="88b6c-1268">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1268">4</span></span>

<span data-ttu-id="88b6c-1269">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1269">5</span></span>

<span data-ttu-id="88b6c-1270">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1270">6</span></span>

<span data-ttu-id="88b6c-1271">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1271">7</span></span>

<span data-ttu-id="88b6c-1272">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1272">8</span></span>

<span data-ttu-id="88b6c-1273">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1273">9</span></span>

<span data-ttu-id="88b6c-1274">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1274">2</span></span><br/> <span data-ttu-id="88b6c-1275">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1275">0</span></span><br/>

<span data-ttu-id="88b6c-1276">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1276">1</span></span>

<span data-ttu-id="88b6c-1277">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1277">2</span></span>

<span data-ttu-id="88b6c-1278">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1278">3</span></span>

<span data-ttu-id="88b6c-1279">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1279">4</span></span>

<span data-ttu-id="88b6c-1280">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1280">5</span></span>

<span data-ttu-id="88b6c-1281">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1281">6</span></span>

<span data-ttu-id="88b6c-1282">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1282">7</span></span>

<span data-ttu-id="88b6c-1283">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1283">8</span></span>

<span data-ttu-id="88b6c-1284">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1284">9</span></span>

<span data-ttu-id="88b6c-1285">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1285">3</span></span><br/> <span data-ttu-id="88b6c-1286">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1286">0</span></span><br/>

<span data-ttu-id="88b6c-1287">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1287">1</span></span>

<span data-ttu-id="88b6c-1288">\_relop</span><span class="sxs-lookup"><span data-stu-id="88b6c-1288">\_relop</span></span>

<span data-ttu-id="88b6c-1289">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1289">\_Property (variable)</span></span>

<span data-ttu-id="88b6c-1290">\_prval (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="88b6c-1291">**\_ relop**：32位不帶正負號的整數，指定要在屬性上執行的關聯性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="88b6c-1292">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="88b6c-1293">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1293">Value</span></span>                 | <span data-ttu-id="88b6c-1294">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1295">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="88b6c-1296">小於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1297">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="88b6c-1298">小於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="88b6c-1299">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="88b6c-1300">大於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="88b6c-1301">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="88b6c-1302">大於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="88b6c-1303">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="88b6c-1304">相等比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1305">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="88b6c-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="88b6c-1306">不相等的比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="88b6c-1307">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="88b6c-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="88b6c-1308">正則運算式比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="88b6c-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="88b6c-1310">傳回右運算元的位 AND。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="88b6c-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="88b6c-1312">傳回非零值的位 AND。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="88b6c-1313">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="88b6c-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="88b6c-1314">作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="88b6c-1315">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="88b6c-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="88b6c-1316">作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="88b6c-1317">**\_ 屬性**： CFullPropSpec 結構（如區段2.2.1.2 中所指定），表示要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="88b6c-1318">**\_ prval**：在區段2.2.1.1 中指定的 CBaseStorageVariant 結構，其中包含與屬性相關的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="88b6c-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="88b6c-1320">CRangeRestriction 結構包含值範圍的限制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="88b6c-1321">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1321">0</span></span>

<span data-ttu-id="88b6c-1322">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1322">1</span></span>

<span data-ttu-id="88b6c-1323">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1323">2</span></span>

<span data-ttu-id="88b6c-1324">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1324">3</span></span>

<span data-ttu-id="88b6c-1325">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1325">4</span></span>

<span data-ttu-id="88b6c-1326">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1326">5</span></span>

<span data-ttu-id="88b6c-1327">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1327">6</span></span>

<span data-ttu-id="88b6c-1328">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1328">7</span></span>

<span data-ttu-id="88b6c-1329">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1329">8</span></span>

<span data-ttu-id="88b6c-1330">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1330">9</span></span>

<span data-ttu-id="88b6c-1331">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1331">1</span></span><br/> <span data-ttu-id="88b6c-1332">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1332">0</span></span><br/>

<span data-ttu-id="88b6c-1333">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1333">1</span></span>

<span data-ttu-id="88b6c-1334">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1334">2</span></span>

<span data-ttu-id="88b6c-1335">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1335">3</span></span>

<span data-ttu-id="88b6c-1336">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1336">4</span></span>

<span data-ttu-id="88b6c-1337">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1337">5</span></span>

<span data-ttu-id="88b6c-1338">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1338">6</span></span>

<span data-ttu-id="88b6c-1339">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1339">7</span></span>

<span data-ttu-id="88b6c-1340">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1340">8</span></span>

<span data-ttu-id="88b6c-1341">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1341">9</span></span>

<span data-ttu-id="88b6c-1342">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1342">2</span></span><br/> <span data-ttu-id="88b6c-1343">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1343">0</span></span><br/>

<span data-ttu-id="88b6c-1344">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1344">1</span></span>

<span data-ttu-id="88b6c-1345">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1345">2</span></span>

<span data-ttu-id="88b6c-1346">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1346">3</span></span>

<span data-ttu-id="88b6c-1347">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1347">4</span></span>

<span data-ttu-id="88b6c-1348">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1348">5</span></span>

<span data-ttu-id="88b6c-1349">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1349">6</span></span>

<span data-ttu-id="88b6c-1350">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1350">7</span></span>

<span data-ttu-id="88b6c-1351">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1351">8</span></span>

<span data-ttu-id="88b6c-1352">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1352">9</span></span>

<span data-ttu-id="88b6c-1353">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1353">3</span></span><br/> <span data-ttu-id="88b6c-1354">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1354">0</span></span><br/>

<span data-ttu-id="88b6c-1355">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1355">1</span></span>

<span data-ttu-id="88b6c-1356">\_keyStart (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="88b6c-1357">\_keyEnd (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="88b6c-1358">**\_ keyStart**：2.2.1.4 區段中指定的 CKey 結構，其中包含範圍的開頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="88b6c-1359">**\_ keyEnd**：包含範圍結尾的 CKey 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="88b6c-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="88b6c-1361">CScopeRestriction 結構包含要搜尋之檔案的限制</span><span class="sxs-lookup"><span data-stu-id="88b6c-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="88b6c-1362">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1362">0</span></span>

<span data-ttu-id="88b6c-1363">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1363">1</span></span>

<span data-ttu-id="88b6c-1364">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1364">2</span></span>

<span data-ttu-id="88b6c-1365">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1365">3</span></span>

<span data-ttu-id="88b6c-1366">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1366">4</span></span>

<span data-ttu-id="88b6c-1367">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1367">5</span></span>

<span data-ttu-id="88b6c-1368">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1368">6</span></span>

<span data-ttu-id="88b6c-1369">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1369">7</span></span>

<span data-ttu-id="88b6c-1370">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1370">8</span></span>

<span data-ttu-id="88b6c-1371">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1371">9</span></span>

<span data-ttu-id="88b6c-1372">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1372">1</span></span><br/> <span data-ttu-id="88b6c-1373">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1373">0</span></span><br/>

<span data-ttu-id="88b6c-1374">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1374">1</span></span>

<span data-ttu-id="88b6c-1375">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1375">2</span></span>

<span data-ttu-id="88b6c-1376">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1376">3</span></span>

<span data-ttu-id="88b6c-1377">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1377">4</span></span>

<span data-ttu-id="88b6c-1378">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1378">5</span></span>

<span data-ttu-id="88b6c-1379">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1379">6</span></span>

<span data-ttu-id="88b6c-1380">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1380">7</span></span>

<span data-ttu-id="88b6c-1381">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1381">8</span></span>

<span data-ttu-id="88b6c-1382">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1382">9</span></span>

<span data-ttu-id="88b6c-1383">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1383">2</span></span><br/> <span data-ttu-id="88b6c-1384">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1384">0</span></span><br/>

<span data-ttu-id="88b6c-1385">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1385">1</span></span>

<span data-ttu-id="88b6c-1386">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1386">2</span></span>

<span data-ttu-id="88b6c-1387">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1387">3</span></span>

<span data-ttu-id="88b6c-1388">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1388">4</span></span>

<span data-ttu-id="88b6c-1389">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1389">5</span></span>

<span data-ttu-id="88b6c-1390">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1390">6</span></span>

<span data-ttu-id="88b6c-1391">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1391">7</span></span>

<span data-ttu-id="88b6c-1392">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1392">8</span></span>

<span data-ttu-id="88b6c-1393">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1393">9</span></span>

<span data-ttu-id="88b6c-1394">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1394">3</span></span><br/> <span data-ttu-id="88b6c-1395">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1395">0</span></span><br/>

<span data-ttu-id="88b6c-1396">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1396">1</span></span>

<span data-ttu-id="88b6c-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="88b6c-1397">CcLowerPath</span></span>

<span data-ttu-id="88b6c-1398">\_lowerPath (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="88b6c-1399">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1399">...</span></span>

<span data-ttu-id="88b6c-1400">\_填補 ( 變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1400">\_padding ( variable)</span></span>

<span data-ttu-id="88b6c-1401">\_長度</span><span class="sxs-lookup"><span data-stu-id="88b6c-1401">\_length</span></span>

<span data-ttu-id="88b6c-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="88b6c-1402">\_fRecursive</span></span>

<span data-ttu-id="88b6c-1403">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="88b6c-1403">\_fVirtual</span></span>



 

<span data-ttu-id="88b6c-1404">**CcLowerPath**：32位不帶正負號的整數，其中包含 lowerPath 欄位中的 Unicode 字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="88b6c-1405">**\_ lowerPath**：非以 Null 終止的 Unicode 字串，表示應限制查詢的 **路徑**。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="88b6c-1406">CcLowerPath 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="88b6c-1407">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-1408">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-1409">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-1410">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-1411">**\_ 長度**：32位不帶正負號的整數，其中包含 lowerPath 的長度 \_ （以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="88b6c-1412">這必須與 CcLowerPath 的值相同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="88b6c-1413">**\_ fRecursive**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1414">必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="88b6c-1415">如果設定為0x00000001，伺服器就會以遞迴方式檢查路徑的所有子目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="88b6c-1416">如果設定為0x00000000，則伺服器不會檢查任何子目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="88b6c-1417">**\_ fVirtual**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1418">必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="88b6c-1419">如果設定為0x00000001， \_ lowerPath 就是 (統一資源定位器 (URL) 的虛擬路徑，與網站檔案系統) 上的實體目錄相關聯。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="88b6c-1420">如果設定為0x00000000， \_ lowerPath 就是檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="88b6c-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="88b6c-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="88b6c-1422">CSort 結構會識別要排序的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="88b6c-1423">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1423">0</span></span>

<span data-ttu-id="88b6c-1424">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1424">1</span></span>

<span data-ttu-id="88b6c-1425">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1425">2</span></span>

<span data-ttu-id="88b6c-1426">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1426">3</span></span>

<span data-ttu-id="88b6c-1427">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1427">4</span></span>

<span data-ttu-id="88b6c-1428">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1428">5</span></span>

<span data-ttu-id="88b6c-1429">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1429">6</span></span>

<span data-ttu-id="88b6c-1430">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1430">7</span></span>

<span data-ttu-id="88b6c-1431">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1431">8</span></span>

<span data-ttu-id="88b6c-1432">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1432">9</span></span>

<span data-ttu-id="88b6c-1433">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1433">1</span></span><br/> <span data-ttu-id="88b6c-1434">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1434">0</span></span><br/>

<span data-ttu-id="88b6c-1435">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1435">1</span></span>

<span data-ttu-id="88b6c-1436">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1436">2</span></span>

<span data-ttu-id="88b6c-1437">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1437">3</span></span>

<span data-ttu-id="88b6c-1438">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1438">4</span></span>

<span data-ttu-id="88b6c-1439">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1439">5</span></span>

<span data-ttu-id="88b6c-1440">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1440">6</span></span>

<span data-ttu-id="88b6c-1441">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1441">7</span></span>

<span data-ttu-id="88b6c-1442">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1442">8</span></span>

<span data-ttu-id="88b6c-1443">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1443">9</span></span>

<span data-ttu-id="88b6c-1444">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1444">2</span></span><br/> <span data-ttu-id="88b6c-1445">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1445">0</span></span><br/>

<span data-ttu-id="88b6c-1446">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1446">1</span></span>

<span data-ttu-id="88b6c-1447">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1447">2</span></span>

<span data-ttu-id="88b6c-1448">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1448">3</span></span>

<span data-ttu-id="88b6c-1449">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1449">4</span></span>

<span data-ttu-id="88b6c-1450">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1450">5</span></span>

<span data-ttu-id="88b6c-1451">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1451">6</span></span>

<span data-ttu-id="88b6c-1452">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1452">7</span></span>

<span data-ttu-id="88b6c-1453">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1453">8</span></span>

<span data-ttu-id="88b6c-1454">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1454">9</span></span>

<span data-ttu-id="88b6c-1455">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1455">3</span></span><br/> <span data-ttu-id="88b6c-1456">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1456">0</span></span><br/>

<span data-ttu-id="88b6c-1457">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1457">1</span></span>

<span data-ttu-id="88b6c-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="88b6c-1458">pidColumn</span></span>

<span data-ttu-id="88b6c-1459">dwOrder</span><span class="sxs-lookup"><span data-stu-id="88b6c-1459">dwOrder</span></span>

<span data-ttu-id="88b6c-1460">locale</span><span class="sxs-lookup"><span data-stu-id="88b6c-1460">locale</span></span>



 

<span data-ttu-id="88b6c-1461">**pidColumn**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1462">排序依據的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="88b6c-1463">**dwOrder**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1464">必須是下列其中一個值，指定如何根據資料行排序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="88b6c-1465">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1465">Value</span></span>                        | <span data-ttu-id="88b6c-1466">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1467">查詢 \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="88b6c-1468">資料列會根據指定之資料行中的值，以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="88b6c-1469">查詢下降 \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="88b6c-1470">資料列會根據指定之資料行中的值，以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="88b6c-1471">**地區** 設定：32位不帶正負號的整數，指出資料行的地區設定（如 \[ GPSI \] 附錄 A 所指定）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="88b6c-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="88b6c-1473">CSynRestriction 結構包含查詢片語的單字或其同義字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="88b6c-1474">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1474">0</span></span>

<span data-ttu-id="88b6c-1475">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1475">1</span></span>

<span data-ttu-id="88b6c-1476">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1476">2</span></span>

<span data-ttu-id="88b6c-1477">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1477">3</span></span>

<span data-ttu-id="88b6c-1478">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1478">4</span></span>

<span data-ttu-id="88b6c-1479">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1479">5</span></span>

<span data-ttu-id="88b6c-1480">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1480">6</span></span>

<span data-ttu-id="88b6c-1481">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1481">7</span></span>

<span data-ttu-id="88b6c-1482">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1482">8</span></span>

<span data-ttu-id="88b6c-1483">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1483">9</span></span>

<span data-ttu-id="88b6c-1484">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1484">1</span></span><br/> <span data-ttu-id="88b6c-1485">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1485">0</span></span><br/>

<span data-ttu-id="88b6c-1486">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1486">1</span></span>

<span data-ttu-id="88b6c-1487">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1487">2</span></span>

<span data-ttu-id="88b6c-1488">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1488">3</span></span>

<span data-ttu-id="88b6c-1489">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1489">4</span></span>

<span data-ttu-id="88b6c-1490">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1490">5</span></span>

<span data-ttu-id="88b6c-1491">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1491">6</span></span>

<span data-ttu-id="88b6c-1492">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1492">7</span></span>

<span data-ttu-id="88b6c-1493">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1493">8</span></span>

<span data-ttu-id="88b6c-1494">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1494">9</span></span>

<span data-ttu-id="88b6c-1495">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1495">2</span></span><br/> <span data-ttu-id="88b6c-1496">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1496">0</span></span><br/>

<span data-ttu-id="88b6c-1497">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1497">1</span></span>

<span data-ttu-id="88b6c-1498">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1498">2</span></span>

<span data-ttu-id="88b6c-1499">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1499">3</span></span>

<span data-ttu-id="88b6c-1500">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1500">4</span></span>

<span data-ttu-id="88b6c-1501">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1501">5</span></span>

<span data-ttu-id="88b6c-1502">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1502">6</span></span>

<span data-ttu-id="88b6c-1503">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1503">7</span></span>

<span data-ttu-id="88b6c-1504">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1504">8</span></span>

<span data-ttu-id="88b6c-1505">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1505">9</span></span>

<span data-ttu-id="88b6c-1506">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1506">3</span></span><br/> <span data-ttu-id="88b6c-1507">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1507">0</span></span><br/>

<span data-ttu-id="88b6c-1508">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1508">1</span></span>

<span data-ttu-id="88b6c-1509">限制</span><span class="sxs-lookup"><span data-stu-id="88b6c-1509">Restriction</span></span>

<span data-ttu-id="88b6c-1510">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1510">...</span></span>

<span data-ttu-id="88b6c-1511">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1511">...</span></span>

<span data-ttu-id="88b6c-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="88b6c-1512">cKey</span></span>

<span data-ttu-id="88b6c-1513">\_keyArray (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="88b6c-1514">\_isRange</span><span class="sxs-lookup"><span data-stu-id="88b6c-1514">\_isRange</span></span>



 

<span data-ttu-id="88b6c-1515">**限制**：指定單字位置的 COccRestriction 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="88b6c-1516">**cKey**：32位不帶正負號的整數，指定 keyArray 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="88b6c-1517">**\_ keyArray**：指定單字及其同義字的 CKey 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="88b6c-1518">**\_ isRange**：如果設定為0x01，索引鍵會是要比對的首碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="88b6c-1519">如果設定為0x00，索引鍵會是要比對的精確值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="88b6c-1520">\_isRange 不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="88b6c-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="88b6c-1522">CVectorRestriction 結構包含命令樹節點上的加權或運算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="88b6c-1523">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1523">0</span></span>

<span data-ttu-id="88b6c-1524">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1524">1</span></span>

<span data-ttu-id="88b6c-1525">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1525">2</span></span>

<span data-ttu-id="88b6c-1526">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1526">3</span></span>

<span data-ttu-id="88b6c-1527">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1527">4</span></span>

<span data-ttu-id="88b6c-1528">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1528">5</span></span>

<span data-ttu-id="88b6c-1529">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1529">6</span></span>

<span data-ttu-id="88b6c-1530">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1530">7</span></span>

<span data-ttu-id="88b6c-1531">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1531">8</span></span>

<span data-ttu-id="88b6c-1532">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1532">9</span></span>

<span data-ttu-id="88b6c-1533">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1533">1</span></span><br/> <span data-ttu-id="88b6c-1534">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1534">0</span></span><br/>

<span data-ttu-id="88b6c-1535">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1535">1</span></span>

<span data-ttu-id="88b6c-1536">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1536">2</span></span>

<span data-ttu-id="88b6c-1537">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1537">3</span></span>

<span data-ttu-id="88b6c-1538">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1538">4</span></span>

<span data-ttu-id="88b6c-1539">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1539">5</span></span>

<span data-ttu-id="88b6c-1540">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1540">6</span></span>

<span data-ttu-id="88b6c-1541">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1541">7</span></span>

<span data-ttu-id="88b6c-1542">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1542">8</span></span>

<span data-ttu-id="88b6c-1543">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1543">9</span></span>

<span data-ttu-id="88b6c-1544">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1544">2</span></span><br/> <span data-ttu-id="88b6c-1545">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1545">0</span></span><br/>

<span data-ttu-id="88b6c-1546">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1546">1</span></span>

<span data-ttu-id="88b6c-1547">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1547">2</span></span>

<span data-ttu-id="88b6c-1548">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1548">3</span></span>

<span data-ttu-id="88b6c-1549">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1549">4</span></span>

<span data-ttu-id="88b6c-1550">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1550">5</span></span>

<span data-ttu-id="88b6c-1551">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1551">6</span></span>

<span data-ttu-id="88b6c-1552">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1552">7</span></span>

<span data-ttu-id="88b6c-1553">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1553">8</span></span>

<span data-ttu-id="88b6c-1554">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1554">9</span></span>

<span data-ttu-id="88b6c-1555">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1555">3</span></span><br/> <span data-ttu-id="88b6c-1556">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1556">0</span></span><br/>

<span data-ttu-id="88b6c-1557">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1557">1</span></span>

<span data-ttu-id="88b6c-1558">\_按 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1558">\_pres (variable)</span></span>

<span data-ttu-id="88b6c-1559">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1559">...</span></span>

<span data-ttu-id="88b6c-1560">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1560">\_padding (variable)</span></span>

<span data-ttu-id="88b6c-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="88b6c-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="88b6c-1562">**\_ 按**：要執行排名或運算的 CNodeRestriction 命令樹。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="88b6c-1563">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-1564">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-1565">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-1566">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-1567">**\_ ulRankMethod**：指定排名演算法的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="88b6c-1568">必須設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="88b6c-1569">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1569">Value</span></span>                            | <span data-ttu-id="88b6c-1570">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="88b6c-1571">向量 \_ 排名 \_ 最小0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="88b6c-1572">使用最小演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="88b6c-1573">向量順 \_ 位 \_ 最大值0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="88b6c-1574">使用最大演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="88b6c-1575">向量 \_ 排名 \_ 內部0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="88b6c-1576">使用內部產品演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="88b6c-1577">向量順 \_ 位 \_ 骰子0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="88b6c-1578">使用骰子係數演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="88b6c-1579">向量順 \_ 位 \_ JACCARD 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="88b6c-1580">使用 Jaccard 係數演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="88b6c-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="88b6c-1582">CWordRestriction 結構包含查詢片語的單字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="88b6c-1583">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1583">0</span></span>

<span data-ttu-id="88b6c-1584">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1584">1</span></span>

<span data-ttu-id="88b6c-1585">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1585">2</span></span>

<span data-ttu-id="88b6c-1586">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1586">3</span></span>

<span data-ttu-id="88b6c-1587">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1587">4</span></span>

<span data-ttu-id="88b6c-1588">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1588">5</span></span>

<span data-ttu-id="88b6c-1589">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1589">6</span></span>

<span data-ttu-id="88b6c-1590">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1590">7</span></span>

<span data-ttu-id="88b6c-1591">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1591">8</span></span>

<span data-ttu-id="88b6c-1592">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1592">9</span></span>

<span data-ttu-id="88b6c-1593">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1593">1</span></span><br/> <span data-ttu-id="88b6c-1594">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1594">0</span></span><br/>

<span data-ttu-id="88b6c-1595">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1595">1</span></span>

<span data-ttu-id="88b6c-1596">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1596">2</span></span>

<span data-ttu-id="88b6c-1597">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1597">3</span></span>

<span data-ttu-id="88b6c-1598">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1598">4</span></span>

<span data-ttu-id="88b6c-1599">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1599">5</span></span>

<span data-ttu-id="88b6c-1600">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1600">6</span></span>

<span data-ttu-id="88b6c-1601">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1601">7</span></span>

<span data-ttu-id="88b6c-1602">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1602">8</span></span>

<span data-ttu-id="88b6c-1603">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1603">9</span></span>

<span data-ttu-id="88b6c-1604">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1604">2</span></span><br/> <span data-ttu-id="88b6c-1605">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1605">0</span></span><br/>

<span data-ttu-id="88b6c-1606">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1606">1</span></span>

<span data-ttu-id="88b6c-1607">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1607">2</span></span>

<span data-ttu-id="88b6c-1608">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1608">3</span></span>

<span data-ttu-id="88b6c-1609">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1609">4</span></span>

<span data-ttu-id="88b6c-1610">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1610">5</span></span>

<span data-ttu-id="88b6c-1611">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1611">6</span></span>

<span data-ttu-id="88b6c-1612">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1612">7</span></span>

<span data-ttu-id="88b6c-1613">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1613">8</span></span>

<span data-ttu-id="88b6c-1614">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1614">9</span></span>

<span data-ttu-id="88b6c-1615">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1615">3</span></span><br/> <span data-ttu-id="88b6c-1616">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1616">0</span></span><br/>

<span data-ttu-id="88b6c-1617">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1617">1</span></span>

<span data-ttu-id="88b6c-1618">限制</span><span class="sxs-lookup"><span data-stu-id="88b6c-1618">restriction</span></span>

<span data-ttu-id="88b6c-1619">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1619">...</span></span>

<span data-ttu-id="88b6c-1620">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1620">...</span></span>

<span data-ttu-id="88b6c-1621">\_key (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1621">\_key (variable)</span></span>

<span data-ttu-id="88b6c-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="88b6c-1622">\_isRange</span></span>



 

<span data-ttu-id="88b6c-1623">**限制**：指定單字位置的 COccRestriction 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="88b6c-1624">**\_ key**：指定單字的 CKey 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="88b6c-1625">**\_ isRange**：如果設定為0x01，則索引鍵是要比對的前置詞。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="88b6c-1626">如果設定為0x00，則索引鍵是要比對的精確值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="88b6c-1627">\_isRange 不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="88b6c-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="88b6c-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="88b6c-1629">CRestriction 結構包含查詢命令樹的節點。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="88b6c-1630">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1630">0</span></span>

<span data-ttu-id="88b6c-1631">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1631">1</span></span>

<span data-ttu-id="88b6c-1632">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1632">2</span></span>

<span data-ttu-id="88b6c-1633">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1633">3</span></span>

<span data-ttu-id="88b6c-1634">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1634">4</span></span>

<span data-ttu-id="88b6c-1635">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1635">5</span></span>

<span data-ttu-id="88b6c-1636">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1636">6</span></span>

<span data-ttu-id="88b6c-1637">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1637">7</span></span>

<span data-ttu-id="88b6c-1638">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1638">8</span></span>

<span data-ttu-id="88b6c-1639">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1639">9</span></span>

<span data-ttu-id="88b6c-1640">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1640">1</span></span><br/> <span data-ttu-id="88b6c-1641">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1641">0</span></span><br/>

<span data-ttu-id="88b6c-1642">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1642">1</span></span>

<span data-ttu-id="88b6c-1643">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1643">2</span></span>

<span data-ttu-id="88b6c-1644">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1644">3</span></span>

<span data-ttu-id="88b6c-1645">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1645">4</span></span>

<span data-ttu-id="88b6c-1646">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1646">5</span></span>

<span data-ttu-id="88b6c-1647">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1647">6</span></span>

<span data-ttu-id="88b6c-1648">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1648">7</span></span>

<span data-ttu-id="88b6c-1649">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1649">8</span></span>

<span data-ttu-id="88b6c-1650">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1650">9</span></span>

<span data-ttu-id="88b6c-1651">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1651">2</span></span><br/> <span data-ttu-id="88b6c-1652">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1652">0</span></span><br/>

<span data-ttu-id="88b6c-1653">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1653">1</span></span>

<span data-ttu-id="88b6c-1654">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1654">2</span></span>

<span data-ttu-id="88b6c-1655">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1655">3</span></span>

<span data-ttu-id="88b6c-1656">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1656">4</span></span>

<span data-ttu-id="88b6c-1657">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1657">5</span></span>

<span data-ttu-id="88b6c-1658">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1658">6</span></span>

<span data-ttu-id="88b6c-1659">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1659">7</span></span>

<span data-ttu-id="88b6c-1660">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1660">8</span></span>

<span data-ttu-id="88b6c-1661">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1661">9</span></span>

<span data-ttu-id="88b6c-1662">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1662">3</span></span><br/> <span data-ttu-id="88b6c-1663">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1663">0</span></span><br/>

<span data-ttu-id="88b6c-1664">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1664">1</span></span>

<span data-ttu-id="88b6c-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="88b6c-1665">\_ulType</span></span>

<span data-ttu-id="88b6c-1666">Weight</span><span class="sxs-lookup"><span data-stu-id="88b6c-1666">Weight</span></span>

<span data-ttu-id="88b6c-1667">限制</span><span class="sxs-lookup"><span data-stu-id="88b6c-1667">Restriction</span></span>



 

<span data-ttu-id="88b6c-1668">**\_ ulType**：32位不帶正負號的整數，表示用於命令樹節點的限制類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="88b6c-1669">必須設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="88b6c-1670">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1670">Value</span></span>                    | <span data-ttu-id="88b6c-1671">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="88b6c-1673">節點代表向量查詢中的非搜尋字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="88b6c-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="88b6c-1675">節點包含要在其上執行邏輯 AND 運算的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="88b6c-1676">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="88b6c-1677">節點包含要在其上執行邏輯 OR 運算的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="88b6c-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="88b6c-1679">節點包含不會執行任何作業的 CRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="88b6c-1680">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="88b6c-1681">節點包含 CContentRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="88b6c-1682">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="88b6c-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="88b6c-1683">節點包含 CPropertyRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="88b6c-1684">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="88b6c-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="88b6c-1685">節點包含要執行鄰近排名的 CNodeRestriction，</span><span class="sxs-lookup"><span data-stu-id="88b6c-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="88b6c-1686">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="88b6c-1687">節點包含 CVectorRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="88b6c-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="88b6c-1689">節點包含 CNatLanguageRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="88b6c-1690">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="88b6c-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="88b6c-1691">節點包含 CScopeRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="88b6c-1692">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="88b6c-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="88b6c-1693">節點包含 CInternalPropertyRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="88b6c-1694">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="88b6c-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="88b6c-1695">節點包含 CRangeRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="88b6c-1696">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="88b6c-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="88b6c-1697">節點包含要執行片語相符的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="88b6c-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="88b6c-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="88b6c-1699">節點包含 CSynRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="88b6c-1700">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="88b6c-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="88b6c-1701">節點包含 CWordRestriction。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="88b6c-1702">**權數**：代表節點權數的32位不帶正負號整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="88b6c-1703">權數表示相對於查詢命令樹中其他節點的節點重要性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="88b6c-1704">較高的權數值更重要。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="88b6c-1705">**限制**：命令樹節點的限制類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="88b6c-1706">語法必須如 \_ ulType 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="88b6c-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="88b6c-1708">CColumnSet 結構會指定要傳回的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="88b6c-1709">此結構一律用於參考特定的 CPidMapper 結構， (區段 2.2.1.23) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="88b6c-1710">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1710">0</span></span>

<span data-ttu-id="88b6c-1711">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1711">1</span></span>

<span data-ttu-id="88b6c-1712">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1712">2</span></span>

<span data-ttu-id="88b6c-1713">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1713">3</span></span>

<span data-ttu-id="88b6c-1714">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1714">4</span></span>

<span data-ttu-id="88b6c-1715">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1715">5</span></span>

<span data-ttu-id="88b6c-1716">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1716">6</span></span>

<span data-ttu-id="88b6c-1717">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1717">7</span></span>

<span data-ttu-id="88b6c-1718">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1718">8</span></span>

<span data-ttu-id="88b6c-1719">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1719">9</span></span>

<span data-ttu-id="88b6c-1720">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1720">1</span></span><br/> <span data-ttu-id="88b6c-1721">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1721">0</span></span><br/>

<span data-ttu-id="88b6c-1722">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1722">1</span></span>

<span data-ttu-id="88b6c-1723">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1723">2</span></span>

<span data-ttu-id="88b6c-1724">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1724">3</span></span>

<span data-ttu-id="88b6c-1725">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1725">4</span></span>

<span data-ttu-id="88b6c-1726">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1726">5</span></span>

<span data-ttu-id="88b6c-1727">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1727">6</span></span>

<span data-ttu-id="88b6c-1728">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1728">7</span></span>

<span data-ttu-id="88b6c-1729">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1729">8</span></span>

<span data-ttu-id="88b6c-1730">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1730">9</span></span>

<span data-ttu-id="88b6c-1731">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1731">2</span></span><br/> <span data-ttu-id="88b6c-1732">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1732">0</span></span><br/>

<span data-ttu-id="88b6c-1733">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1733">1</span></span>

<span data-ttu-id="88b6c-1734">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1734">2</span></span>

<span data-ttu-id="88b6c-1735">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1735">3</span></span>

<span data-ttu-id="88b6c-1736">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1736">4</span></span>

<span data-ttu-id="88b6c-1737">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1737">5</span></span>

<span data-ttu-id="88b6c-1738">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1738">6</span></span>

<span data-ttu-id="88b6c-1739">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1739">7</span></span>

<span data-ttu-id="88b6c-1740">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1740">8</span></span>

<span data-ttu-id="88b6c-1741">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1741">9</span></span>

<span data-ttu-id="88b6c-1742">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1742">3</span></span><br/> <span data-ttu-id="88b6c-1743">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1743">0</span></span><br/>

<span data-ttu-id="88b6c-1744">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1744">1</span></span>

<span data-ttu-id="88b6c-1745">計數</span><span class="sxs-lookup"><span data-stu-id="88b6c-1745">count</span></span>

<span data-ttu-id="88b6c-1746"> (變數的索引) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1746">indexes (variable)</span></span>



 

<span data-ttu-id="88b6c-1747">**計數**：指定索引陣列中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="88b6c-1748">**索引**：4位元組不帶正負號的整數的陣列，代表對應 CPidMapper 結構中 aPropSpec 陣列的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="88b6c-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="88b6c-1750">CCategorizationSet 結構包含有關查詢結果集群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="88b6c-1751">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1751">0</span></span>

<span data-ttu-id="88b6c-1752">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1752">1</span></span>

<span data-ttu-id="88b6c-1753">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1753">2</span></span>

<span data-ttu-id="88b6c-1754">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1754">3</span></span>

<span data-ttu-id="88b6c-1755">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1755">4</span></span>

<span data-ttu-id="88b6c-1756">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1756">5</span></span>

<span data-ttu-id="88b6c-1757">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1757">6</span></span>

<span data-ttu-id="88b6c-1758">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1758">7</span></span>

<span data-ttu-id="88b6c-1759">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1759">8</span></span>

<span data-ttu-id="88b6c-1760">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1760">9</span></span>

<span data-ttu-id="88b6c-1761">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1761">1</span></span><br/> <span data-ttu-id="88b6c-1762">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1762">0</span></span><br/>

<span data-ttu-id="88b6c-1763">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1763">1</span></span>

<span data-ttu-id="88b6c-1764">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1764">2</span></span>

<span data-ttu-id="88b6c-1765">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1765">3</span></span>

<span data-ttu-id="88b6c-1766">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1766">4</span></span>

<span data-ttu-id="88b6c-1767">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1767">5</span></span>

<span data-ttu-id="88b6c-1768">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1768">6</span></span>

<span data-ttu-id="88b6c-1769">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1769">7</span></span>

<span data-ttu-id="88b6c-1770">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1770">8</span></span>

<span data-ttu-id="88b6c-1771">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1771">9</span></span>

<span data-ttu-id="88b6c-1772">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1772">2</span></span><br/> <span data-ttu-id="88b6c-1773">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1773">0</span></span><br/>

<span data-ttu-id="88b6c-1774">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1774">1</span></span>

<span data-ttu-id="88b6c-1775">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1775">2</span></span>

<span data-ttu-id="88b6c-1776">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1776">3</span></span>

<span data-ttu-id="88b6c-1777">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1777">4</span></span>

<span data-ttu-id="88b6c-1778">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1778">5</span></span>

<span data-ttu-id="88b6c-1779">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1779">6</span></span>

<span data-ttu-id="88b6c-1780">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1780">7</span></span>

<span data-ttu-id="88b6c-1781">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1781">8</span></span>

<span data-ttu-id="88b6c-1782">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1782">9</span></span>

<span data-ttu-id="88b6c-1783">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1783">3</span></span><br/> <span data-ttu-id="88b6c-1784">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1784">0</span></span><br/>

<span data-ttu-id="88b6c-1785">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1785">1</span></span>

<span data-ttu-id="88b6c-1786">計數</span><span class="sxs-lookup"><span data-stu-id="88b6c-1786">count</span></span>

<span data-ttu-id="88b6c-1787">類別 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1787">categories (variable)</span></span>



 

<span data-ttu-id="88b6c-1788">**計數**：32位不帶正負號的整數，其中包含分類陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="88b6c-1789">**類別**：指定查詢群組的 CCategorizationSpec 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="88b6c-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="88b6c-1791">CCategorizationSpec 結構包含查詢結果集的群組。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="88b6c-1792">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1792">0</span></span>

<span data-ttu-id="88b6c-1793">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1793">1</span></span>

<span data-ttu-id="88b6c-1794">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1794">2</span></span>

<span data-ttu-id="88b6c-1795">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1795">3</span></span>

<span data-ttu-id="88b6c-1796">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1796">4</span></span>

<span data-ttu-id="88b6c-1797">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1797">5</span></span>

<span data-ttu-id="88b6c-1798">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1798">6</span></span>

<span data-ttu-id="88b6c-1799">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1799">7</span></span>

<span data-ttu-id="88b6c-1800">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1800">8</span></span>

<span data-ttu-id="88b6c-1801">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1801">9</span></span>

<span data-ttu-id="88b6c-1802">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1802">1</span></span><br/> <span data-ttu-id="88b6c-1803">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1803">0</span></span><br/>

<span data-ttu-id="88b6c-1804">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1804">1</span></span>

<span data-ttu-id="88b6c-1805">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1805">2</span></span>

<span data-ttu-id="88b6c-1806">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1806">3</span></span>

<span data-ttu-id="88b6c-1807">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1807">4</span></span>

<span data-ttu-id="88b6c-1808">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1808">5</span></span>

<span data-ttu-id="88b6c-1809">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1809">6</span></span>

<span data-ttu-id="88b6c-1810">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1810">7</span></span>

<span data-ttu-id="88b6c-1811">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1811">8</span></span>

<span data-ttu-id="88b6c-1812">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1812">9</span></span>

<span data-ttu-id="88b6c-1813">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1813">2</span></span><br/> <span data-ttu-id="88b6c-1814">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1814">0</span></span><br/>

<span data-ttu-id="88b6c-1815">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1815">1</span></span>

<span data-ttu-id="88b6c-1816">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1816">2</span></span>

<span data-ttu-id="88b6c-1817">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1817">3</span></span>

<span data-ttu-id="88b6c-1818">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1818">4</span></span>

<span data-ttu-id="88b6c-1819">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1819">5</span></span>

<span data-ttu-id="88b6c-1820">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1820">6</span></span>

<span data-ttu-id="88b6c-1821">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1821">7</span></span>

<span data-ttu-id="88b6c-1822">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1822">8</span></span>

<span data-ttu-id="88b6c-1823">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1823">9</span></span>

<span data-ttu-id="88b6c-1824">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1824">3</span></span><br/> <span data-ttu-id="88b6c-1825">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1825">0</span></span><br/>

<span data-ttu-id="88b6c-1826">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1826">1</span></span>

<span data-ttu-id="88b6c-1827">\_csColumns (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="88b6c-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="88b6c-1828">\_ulCategType</span></span>



 

<span data-ttu-id="88b6c-1829">**\_ CsColumns**： CColumnSet 結構，指出用來將查詢分組的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="88b6c-1830">**\_ ulCategType**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-1831">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="88b6c-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="88b6c-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="88b6c-1833">CDbColId 結構包含資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="88b6c-1834">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1834">0</span></span>

<span data-ttu-id="88b6c-1835">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1835">1</span></span>

<span data-ttu-id="88b6c-1836">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1836">2</span></span>

<span data-ttu-id="88b6c-1837">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1837">3</span></span>

<span data-ttu-id="88b6c-1838">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1838">4</span></span>

<span data-ttu-id="88b6c-1839">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1839">5</span></span>

<span data-ttu-id="88b6c-1840">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1840">6</span></span>

<span data-ttu-id="88b6c-1841">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1841">7</span></span>

<span data-ttu-id="88b6c-1842">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1842">8</span></span>

<span data-ttu-id="88b6c-1843">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1843">9</span></span>

<span data-ttu-id="88b6c-1844">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1844">1</span></span><br/> <span data-ttu-id="88b6c-1845">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1845">0</span></span><br/>

<span data-ttu-id="88b6c-1846">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1846">1</span></span>

<span data-ttu-id="88b6c-1847">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1847">2</span></span>

<span data-ttu-id="88b6c-1848">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1848">3</span></span>

<span data-ttu-id="88b6c-1849">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1849">4</span></span>

<span data-ttu-id="88b6c-1850">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1850">5</span></span>

<span data-ttu-id="88b6c-1851">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1851">6</span></span>

<span data-ttu-id="88b6c-1852">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1852">7</span></span>

<span data-ttu-id="88b6c-1853">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1853">8</span></span>

<span data-ttu-id="88b6c-1854">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1854">9</span></span>

<span data-ttu-id="88b6c-1855">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1855">2</span></span><br/> <span data-ttu-id="88b6c-1856">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1856">0</span></span><br/>

<span data-ttu-id="88b6c-1857">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1857">1</span></span>

<span data-ttu-id="88b6c-1858">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1858">2</span></span>

<span data-ttu-id="88b6c-1859">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1859">3</span></span>

<span data-ttu-id="88b6c-1860">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1860">4</span></span>

<span data-ttu-id="88b6c-1861">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1861">5</span></span>

<span data-ttu-id="88b6c-1862">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1862">6</span></span>

<span data-ttu-id="88b6c-1863">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1863">7</span></span>

<span data-ttu-id="88b6c-1864">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1864">8</span></span>

<span data-ttu-id="88b6c-1865">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1865">9</span></span>

<span data-ttu-id="88b6c-1866">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1866">3</span></span><br/> <span data-ttu-id="88b6c-1867">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1867">0</span></span><br/>

<span data-ttu-id="88b6c-1868">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1868">1</span></span>

<span data-ttu-id="88b6c-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="88b6c-1869">eKind</span></span>

<span data-ttu-id="88b6c-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="88b6c-1870">GUID</span></span>

<span data-ttu-id="88b6c-1871">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1871">...</span></span>

<span data-ttu-id="88b6c-1872">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1872">...</span></span>

<span data-ttu-id="88b6c-1873">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-1873">...</span></span>

<span data-ttu-id="88b6c-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="88b6c-1874">ulId</span></span>

<span data-ttu-id="88b6c-1875">vString (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1875">vString (variable)</span></span>



 

<span data-ttu-id="88b6c-1876">**eKind**：必須設定為下列其中一個值，以指出 GUID 和 vValue 的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="88b6c-1877">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1877">Value</span></span>                            | <span data-ttu-id="88b6c-1878">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1879">DBKIND \_ GUID \_ 名稱0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="88b6c-1880">vString 包含屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="88b6c-1881">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="88b6c-1882">ulId 包含4個位元組的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="88b6c-1883">DBKIND \_ PGUID \_ NAME 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="88b6c-1884">vString 包含屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1884">vString contains a property name.</span></span> <span data-ttu-id="88b6c-1885">必須將此值視為與 DBKIND \_ GUID 名稱相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="88b6c-1886">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="88b6c-1887">ulId 包含4個位元組的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="88b6c-1888">此值必須與 DBKIND \_ GUID \_ PROPID 相同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="88b6c-1889">**Guid**：屬性 guid。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="88b6c-1890">**ulId**：如果 EKIND 為 DBKIND \_ GUID \_ PROPID 或 DBKIND \_ PGUID \_ PROPID，則此欄位包含不帶正負號的整數，並指定屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="88b6c-1891">如果 eKind 為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID \_ NAME，則此欄位包含一個不帶正負號的整數，指定 vString 欄位中包含的 Unicode 字元數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="88b6c-1892">**vString**：表示屬性名稱的非 Null 終止 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="88b6c-1893">除非 eKind 欄位設定為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID NAME，否則必須省略它 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="88b6c-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="88b6c-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="88b6c-1895">CDbProp 結構包含屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="88b6c-1896">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1896">0</span></span>

<span data-ttu-id="88b6c-1897">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1897">1</span></span>

<span data-ttu-id="88b6c-1898">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1898">2</span></span>

<span data-ttu-id="88b6c-1899">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1899">3</span></span>

<span data-ttu-id="88b6c-1900">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1900">4</span></span>

<span data-ttu-id="88b6c-1901">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1901">5</span></span>

<span data-ttu-id="88b6c-1902">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1902">6</span></span>

<span data-ttu-id="88b6c-1903">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1903">7</span></span>

<span data-ttu-id="88b6c-1904">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1904">8</span></span>

<span data-ttu-id="88b6c-1905">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1905">9</span></span>

<span data-ttu-id="88b6c-1906">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1906">1</span></span><br/> <span data-ttu-id="88b6c-1907">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1907">0</span></span><br/>

<span data-ttu-id="88b6c-1908">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1908">1</span></span>

<span data-ttu-id="88b6c-1909">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1909">2</span></span>

<span data-ttu-id="88b6c-1910">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1910">3</span></span>

<span data-ttu-id="88b6c-1911">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1911">4</span></span>

<span data-ttu-id="88b6c-1912">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1912">5</span></span>

<span data-ttu-id="88b6c-1913">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1913">6</span></span>

<span data-ttu-id="88b6c-1914">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1914">7</span></span>

<span data-ttu-id="88b6c-1915">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1915">8</span></span>

<span data-ttu-id="88b6c-1916">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1916">9</span></span>

<span data-ttu-id="88b6c-1917">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1917">2</span></span><br/> <span data-ttu-id="88b6c-1918">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1918">0</span></span><br/>

<span data-ttu-id="88b6c-1919">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1919">1</span></span>

<span data-ttu-id="88b6c-1920">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-1920">2</span></span>

<span data-ttu-id="88b6c-1921">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1921">3</span></span>

<span data-ttu-id="88b6c-1922">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-1922">4</span></span>

<span data-ttu-id="88b6c-1923">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-1923">5</span></span>

<span data-ttu-id="88b6c-1924">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-1924">6</span></span>

<span data-ttu-id="88b6c-1925">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-1925">7</span></span>

<span data-ttu-id="88b6c-1926">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-1926">8</span></span>

<span data-ttu-id="88b6c-1927">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-1927">9</span></span>

<span data-ttu-id="88b6c-1928">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-1928">3</span></span><br/> <span data-ttu-id="88b6c-1929">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-1929">0</span></span><br/>

<span data-ttu-id="88b6c-1930">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-1930">1</span></span>

<span data-ttu-id="88b6c-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="88b6c-1931">DBPROPID</span></span>

<span data-ttu-id="88b6c-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="88b6c-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="88b6c-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="88b6c-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="88b6c-1934">colid (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1934">colid (variable)</span></span>

<span data-ttu-id="88b6c-1935">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-1935">vValue (variable)</span></span>



 

<span data-ttu-id="88b6c-1936">**DBPROPID**：32位不帶正負號的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="88b6c-1937">**DBPROPOPTIONS** ：必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="88b6c-1938">**DBPROPSTATUS**：必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="88b6c-1939">**colid**： CDbColId 結構（如區段2.2.1.20 所指定），表示要套用屬性的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="88b6c-1940">**vValue**：包含屬性值的 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="88b6c-1941">2.2.1.21.1 屬性</span><span class="sxs-lookup"><span data-stu-id="88b6c-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="88b6c-1942">本節將詳細說明 CISP 所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="88b6c-1943">這些屬性會分成三個屬性集，也就是 CDbPropSet 結構的 guidPropertySet 欄位中的 ident 2.2.1.21.1 ified， (區段 2.2.1.22) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="88b6c-1944">下表列出屬於 DBPROPSET \_ FSCIFRMWRK \_ EXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="88b6c-1945">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1945">Value</span></span>                                  | <span data-ttu-id="88b6c-1946">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1947">DBPROP \_ CI \_ 目錄 \_ 名稱0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="88b6c-1948">指定要查詢的目錄或目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="88b6c-1949">值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="88b6c-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="88b6c-1950">DBPROP \_ CI \_ 包括 \_ 範圍0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="88b6c-1951">指定要包含在查詢中的一或多個路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="88b6c-1952">值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="88b6c-1953">DBPROP \_ CI \_ 範圍 \_ 旗標0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="88b6c-1954">指定 \_ 要如何處理 DBPROP CI \_ 包含範圍屬性所指定的路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="88b6c-1955">值必須是 VT \_ I4 或 vt \_ 向量 \| vt \_ I4。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="88b6c-1956">DBPROP \_ CI \_ 查詢 \_ 類型0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="88b6c-1957">指定查詢的類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1957">Specifies the type of query.</span></span> <span data-ttu-id="88b6c-1958">CDbColId 必須設定為資料庫 \_ NullID。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="88b6c-1959">下表列出 DBPROP \_ CI \_ 範圍 \_ 旗標屬性的旗標：</span><span class="sxs-lookup"><span data-stu-id="88b6c-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="88b6c-1960">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1960">Value</span></span>                     | <span data-ttu-id="88b6c-1961">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1962">查詢 \_ 深度0x01</span><span class="sxs-lookup"><span data-stu-id="88b6c-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="88b6c-1963">如果設定，表示範圍目錄和所有子目錄中的檔案都會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="88b6c-1964">如果清除，只有範圍目錄中的檔案才會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="88b6c-1965">不得與查詢 \_ 深度合併。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="88b6c-1966">查詢 \_ 虛擬 \_ 路徑0x02</span><span class="sxs-lookup"><span data-stu-id="88b6c-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="88b6c-1967">如果設定，則表示範圍是虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="88b6c-1968">如果清除，表示範圍是實體目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="88b6c-1969">下表列出 [DBPROP \_ CI \_ 查詢類型] 屬性的查詢類型 \_ ：</span><span class="sxs-lookup"><span data-stu-id="88b6c-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="88b6c-1970">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1970">Value</span></span>                     | <span data-ttu-id="88b6c-1971">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="88b6c-1973">一般查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="88b6c-1974">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="88b6c-1975">查詢正在要求目錄的虛擬根目錄清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="88b6c-1976">此值需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="88b6c-1977">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="88b6c-1978">查詢正在要求索引服務所支援的所有屬性清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="88b6c-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="88b6c-1980">查詢是系統管理作業。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1980">The query is an administrative operation.</span></span> <span data-ttu-id="88b6c-1981">此值需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="88b6c-1982">下表列出屬於 DBPROPSET \_ QUERYEXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="88b6c-1983">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-1983">Value</span></span>                                      | <span data-ttu-id="88b6c-1984">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="88b6c-1986">指定索引服務處理緩慢查詢的方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="88b6c-1987">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="88b6c-1988">若為 TRUE，則允許伺服器讓這些查詢失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="88b6c-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="88b6c-1990">指出索引服務是否要執行結果修剪。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="88b6c-1991">若為 TRUE，則伺服器會考慮以將回應時間優化至用戶端的方式來執行結果修剪。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="88b6c-1992">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="88b6c-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="88b6c-1994">指出用戶端是否支援 VT \_ 向量資料類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="88b6c-1995">若為 TRUE，則表示用戶端支援 VT \_ 向量; 如果為 FALSE，則伺服器會將 VT \_ 向量資料類型轉換成 vt \_ 陣列資料類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="88b6c-1996">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="88b6c-1997">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="88b6c-1998">表示要傳回的資料列相符專案。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="88b6c-1999">若為 TRUE，則伺服器會傳回一組相符的資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="88b6c-2000">如果為 FALSE，則應該傳回最符合的資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="88b6c-2001">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="88b6c-2002">下表列出屬於 DBPROPSET \_ CIFRMWRKCORE \_ EXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="88b6c-2003">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="88b6c-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="88b6c-2004">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-2005">DBPROP \_ 機器0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="88b6c-2006">指定要處理查詢 (s) 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="88b6c-2007">值必須是 VT \_ bstr 或 vt \_ 陣列 \| VT \_ BSTR。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="88b6c-2008">DBPROP \_ 用戶端 \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="88b6c-2009">指定索引服務的連接常數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="88b6c-2010">此值必須是 \_ 包含0x2A4880706FD911D0A80800A0C906241A 的 VT CLSID。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="88b6c-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="88b6c-2012">CDbPropSet 結構包含一組屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="88b6c-2013">請注意，第一個欄位是固定大小，但可能無法對齊包含此結構之訊息開頭的4位元組倍數的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="88b6c-2014">不過，cProperties 欄位會對齊，因此格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="88b6c-2015">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2015">0</span></span>

<span data-ttu-id="88b6c-2016">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2016">1</span></span>

<span data-ttu-id="88b6c-2017">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2017">2</span></span>

<span data-ttu-id="88b6c-2018">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2018">3</span></span>

<span data-ttu-id="88b6c-2019">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2019">4</span></span>

<span data-ttu-id="88b6c-2020">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2020">5</span></span>

<span data-ttu-id="88b6c-2021">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2021">6</span></span>

<span data-ttu-id="88b6c-2022">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2022">7</span></span>

<span data-ttu-id="88b6c-2023">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2023">8</span></span>

<span data-ttu-id="88b6c-2024">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2024">9</span></span>

<span data-ttu-id="88b6c-2025">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2025">1</span></span><br/> <span data-ttu-id="88b6c-2026">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2026">0</span></span><br/>

<span data-ttu-id="88b6c-2027">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2027">1</span></span>

<span data-ttu-id="88b6c-2028">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2028">2</span></span>

<span data-ttu-id="88b6c-2029">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2029">3</span></span>

<span data-ttu-id="88b6c-2030">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2030">4</span></span>

<span data-ttu-id="88b6c-2031">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2031">5</span></span>

<span data-ttu-id="88b6c-2032">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2032">6</span></span>

<span data-ttu-id="88b6c-2033">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2033">7</span></span>

<span data-ttu-id="88b6c-2034">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2034">8</span></span>

<span data-ttu-id="88b6c-2035">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2035">9</span></span>

<span data-ttu-id="88b6c-2036">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2036">2</span></span><br/> <span data-ttu-id="88b6c-2037">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2037">0</span></span><br/>

<span data-ttu-id="88b6c-2038">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2038">1</span></span>

<span data-ttu-id="88b6c-2039">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2039">2</span></span>

<span data-ttu-id="88b6c-2040">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2040">3</span></span>

<span data-ttu-id="88b6c-2041">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2041">4</span></span>

<span data-ttu-id="88b6c-2042">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2042">5</span></span>

<span data-ttu-id="88b6c-2043">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2043">6</span></span>

<span data-ttu-id="88b6c-2044">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2044">7</span></span>

<span data-ttu-id="88b6c-2045">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2045">8</span></span>

<span data-ttu-id="88b6c-2046">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2046">9</span></span>

<span data-ttu-id="88b6c-2047">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2047">3</span></span><br/> <span data-ttu-id="88b6c-2048">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2048">0</span></span><br/>

<span data-ttu-id="88b6c-2049">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2049">1</span></span>

<span data-ttu-id="88b6c-2050">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="88b6c-2050">guidPropertySet</span></span>

<span data-ttu-id="88b6c-2051">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-2051">...</span></span>

<span data-ttu-id="88b6c-2052">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-2052">...</span></span>

<span data-ttu-id="88b6c-2053">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-2053">...</span></span>

<span data-ttu-id="88b6c-2054">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-2054">...</span></span>

<span data-ttu-id="88b6c-2055">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2055">\_padding (variable)</span></span>

<span data-ttu-id="88b6c-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="88b6c-2056">cProperties</span></span>

<span data-ttu-id="88b6c-2057">aProps (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2057">aProps (variable)</span></span>



 

<span data-ttu-id="88b6c-2058">**guidPropertySet**：識別屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="88b6c-2059">必須設定為對應到下列其中一個值的二進位格式 (以字串表示表單) 顯示，識別 aProps 欄位中包含之屬性的屬性集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="88b6c-2060">值/GUID</span><span class="sxs-lookup"><span data-stu-id="88b6c-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="88b6c-2061">Name</span><span class="sxs-lookup"><span data-stu-id="88b6c-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="88b6c-2062">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="88b6c-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="88b6c-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="88b6c-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="88b6c-2064">檔案系統內容索引架構屬性集</span><span class="sxs-lookup"><span data-stu-id="88b6c-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="88b6c-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="88b6c-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="88b6c-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="88b6c-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="88b6c-2067">查詢延伸模組屬性集</span><span class="sxs-lookup"><span data-stu-id="88b6c-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="88b6c-2068">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="88b6c-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="88b6c-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="88b6c-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="88b6c-2070">內容索引架構核心屬性集</span><span class="sxs-lookup"><span data-stu-id="88b6c-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="88b6c-2071">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="88b6c-2072">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="88b6c-2073">如果這個欄位存在 (亦即，長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="88b6c-2074">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-2075">**cProperties**：32位不帶正負號的整數，其中包含 aProps 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="88b6c-2076">**aProps**： CDbProp 結構的陣列，如區段0中所指定，包含屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="88b6c-2077">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="88b6c-2078">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="88b6c-2079">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="88b6c-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="88b6c-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="88b6c-2081">CPidMapper 結構包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="88b6c-2082">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2082">0</span></span>

<span data-ttu-id="88b6c-2083">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2083">1</span></span>

<span data-ttu-id="88b6c-2084">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2084">2</span></span>

<span data-ttu-id="88b6c-2085">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2085">3</span></span>

<span data-ttu-id="88b6c-2086">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2086">4</span></span>

<span data-ttu-id="88b6c-2087">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2087">5</span></span>

<span data-ttu-id="88b6c-2088">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2088">6</span></span>

<span data-ttu-id="88b6c-2089">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2089">7</span></span>

<span data-ttu-id="88b6c-2090">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2090">8</span></span>

<span data-ttu-id="88b6c-2091">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2091">9</span></span>

<span data-ttu-id="88b6c-2092">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2092">1</span></span><br/> <span data-ttu-id="88b6c-2093">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2093">0</span></span><br/>

<span data-ttu-id="88b6c-2094">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2094">1</span></span>

<span data-ttu-id="88b6c-2095">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2095">2</span></span>

<span data-ttu-id="88b6c-2096">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2096">3</span></span>

<span data-ttu-id="88b6c-2097">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2097">4</span></span>

<span data-ttu-id="88b6c-2098">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2098">5</span></span>

<span data-ttu-id="88b6c-2099">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2099">6</span></span>

<span data-ttu-id="88b6c-2100">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2100">7</span></span>

<span data-ttu-id="88b6c-2101">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2101">8</span></span>

<span data-ttu-id="88b6c-2102">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2102">9</span></span>

<span data-ttu-id="88b6c-2103">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2103">2</span></span><br/> <span data-ttu-id="88b6c-2104">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2104">0</span></span><br/>

<span data-ttu-id="88b6c-2105">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2105">1</span></span>

<span data-ttu-id="88b6c-2106">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2106">2</span></span>

<span data-ttu-id="88b6c-2107">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2107">3</span></span>

<span data-ttu-id="88b6c-2108">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2108">4</span></span>

<span data-ttu-id="88b6c-2109">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2109">5</span></span>

<span data-ttu-id="88b6c-2110">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2110">6</span></span>

<span data-ttu-id="88b6c-2111">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2111">7</span></span>

<span data-ttu-id="88b6c-2112">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2112">8</span></span>

<span data-ttu-id="88b6c-2113">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2113">9</span></span>

<span data-ttu-id="88b6c-2114">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2114">3</span></span><br/> <span data-ttu-id="88b6c-2115">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2115">0</span></span><br/>

<span data-ttu-id="88b6c-2116">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2116">1</span></span>

<span data-ttu-id="88b6c-2117">計數</span><span class="sxs-lookup"><span data-stu-id="88b6c-2117">count</span></span>

<span data-ttu-id="88b6c-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-2118">aPropSpec</span></span>

<span data-ttu-id="88b6c-2119">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2119">... (variable)</span></span>



 

<span data-ttu-id="88b6c-2120">**count**：包含 aPropSpec 陣列中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="88b6c-2121">**aPropSpec**： CFullPropSpec 結構的陣列，表示要傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="88b6c-2122">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="88b6c-2123">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="88b6c-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="88b6c-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="88b6c-2125">CRowSeekAt 結構包含在 CPMGetRowsIn 訊息中取得資料列的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="88b6c-2126">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2126">0</span></span>

<span data-ttu-id="88b6c-2127">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2127">1</span></span>

<span data-ttu-id="88b6c-2128">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2128">2</span></span>

<span data-ttu-id="88b6c-2129">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2129">3</span></span>

<span data-ttu-id="88b6c-2130">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2130">4</span></span>

<span data-ttu-id="88b6c-2131">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2131">5</span></span>

<span data-ttu-id="88b6c-2132">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2132">6</span></span>

<span data-ttu-id="88b6c-2133">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2133">7</span></span>

<span data-ttu-id="88b6c-2134">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2134">8</span></span>

<span data-ttu-id="88b6c-2135">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2135">9</span></span>

<span data-ttu-id="88b6c-2136">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2136">1</span></span><br/> <span data-ttu-id="88b6c-2137">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2137">0</span></span><br/>

<span data-ttu-id="88b6c-2138">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2138">1</span></span>

<span data-ttu-id="88b6c-2139">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2139">2</span></span>

<span data-ttu-id="88b6c-2140">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2140">3</span></span>

<span data-ttu-id="88b6c-2141">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2141">4</span></span>

<span data-ttu-id="88b6c-2142">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2142">5</span></span>

<span data-ttu-id="88b6c-2143">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2143">6</span></span>

<span data-ttu-id="88b6c-2144">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2144">7</span></span>

<span data-ttu-id="88b6c-2145">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2145">8</span></span>

<span data-ttu-id="88b6c-2146">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2146">9</span></span>

<span data-ttu-id="88b6c-2147">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2147">2</span></span><br/> <span data-ttu-id="88b6c-2148">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2148">0</span></span><br/>

<span data-ttu-id="88b6c-2149">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2149">1</span></span>

<span data-ttu-id="88b6c-2150">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2150">2</span></span>

<span data-ttu-id="88b6c-2151">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2151">3</span></span>

<span data-ttu-id="88b6c-2152">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2152">4</span></span>

<span data-ttu-id="88b6c-2153">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2153">5</span></span>

<span data-ttu-id="88b6c-2154">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2154">6</span></span>

<span data-ttu-id="88b6c-2155">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2155">7</span></span>

<span data-ttu-id="88b6c-2156">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2156">8</span></span>

<span data-ttu-id="88b6c-2157">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2157">9</span></span>

<span data-ttu-id="88b6c-2158">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2158">3</span></span><br/> <span data-ttu-id="88b6c-2159">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2159">0</span></span><br/>

<span data-ttu-id="88b6c-2160">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2160">1</span></span>

<span data-ttu-id="88b6c-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="88b6c-2161">\_hRegion</span></span>

<span data-ttu-id="88b6c-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="88b6c-2162">\_cskip</span></span>

<span data-ttu-id="88b6c-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="88b6c-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="88b6c-2164">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2165">**\_ cskip**：32位不帶正負號的整數，其中包含要在資料列集中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="88b6c-2166">**\_ bmkOffset**：代表 **書簽** 控制碼的32位值，表示在開始抓取之前，要從中略過 cskip 中指定之資料列數的起始位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="88b6c-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="88b6c-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="88b6c-2168">CRowSeekAtRatio 結構會識別開始抓取 CPMGetRowsIn 訊息的起點。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="88b6c-2169">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2169">0</span></span>

<span data-ttu-id="88b6c-2170">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2170">1</span></span>

<span data-ttu-id="88b6c-2171">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2171">2</span></span>

<span data-ttu-id="88b6c-2172">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2172">3</span></span>

<span data-ttu-id="88b6c-2173">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2173">4</span></span>

<span data-ttu-id="88b6c-2174">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2174">5</span></span>

<span data-ttu-id="88b6c-2175">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2175">6</span></span>

<span data-ttu-id="88b6c-2176">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2176">7</span></span>

<span data-ttu-id="88b6c-2177">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2177">8</span></span>

<span data-ttu-id="88b6c-2178">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2178">9</span></span>

<span data-ttu-id="88b6c-2179">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2179">1</span></span><br/> <span data-ttu-id="88b6c-2180">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2180">0</span></span><br/>

<span data-ttu-id="88b6c-2181">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2181">1</span></span>

<span data-ttu-id="88b6c-2182">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2182">2</span></span>

<span data-ttu-id="88b6c-2183">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2183">3</span></span>

<span data-ttu-id="88b6c-2184">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2184">4</span></span>

<span data-ttu-id="88b6c-2185">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2185">5</span></span>

<span data-ttu-id="88b6c-2186">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2186">6</span></span>

<span data-ttu-id="88b6c-2187">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2187">7</span></span>

<span data-ttu-id="88b6c-2188">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2188">8</span></span>

<span data-ttu-id="88b6c-2189">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2189">9</span></span>

<span data-ttu-id="88b6c-2190">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2190">2</span></span><br/> <span data-ttu-id="88b6c-2191">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2191">0</span></span><br/>

<span data-ttu-id="88b6c-2192">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2192">1</span></span>

<span data-ttu-id="88b6c-2193">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2193">2</span></span>

<span data-ttu-id="88b6c-2194">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2194">3</span></span>

<span data-ttu-id="88b6c-2195">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2195">4</span></span>

<span data-ttu-id="88b6c-2196">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2196">5</span></span>

<span data-ttu-id="88b6c-2197">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2197">6</span></span>

<span data-ttu-id="88b6c-2198">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2198">7</span></span>

<span data-ttu-id="88b6c-2199">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2199">8</span></span>

<span data-ttu-id="88b6c-2200">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2200">9</span></span>

<span data-ttu-id="88b6c-2201">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2201">3</span></span><br/> <span data-ttu-id="88b6c-2202">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2202">0</span></span><br/>

<span data-ttu-id="88b6c-2203">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2203">1</span></span>

<span data-ttu-id="88b6c-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-2204">CiTblChapt</span></span>

<span data-ttu-id="88b6c-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="88b6c-2205">\_hRegion</span></span>

<span data-ttu-id="88b6c-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="88b6c-2206">\_ulNumerator</span></span>

<span data-ttu-id="88b6c-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="88b6c-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="88b6c-2208">**CiTblChapt**：32位不帶正負號的整數，表示要從中取出資料列的資料列集章節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="88b6c-2209">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2210">**\_ ulNumerator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分子。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="88b6c-2211">**\_ ulDenominator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分母。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="88b6c-2212">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="88b6c-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="88b6c-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="88b6c-2214">CRowSeekByBookmark 結構會識別要從中開始抓取 CPMGetRowsIn 訊息之資料列的書簽。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="88b6c-2215">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2215">0</span></span>

<span data-ttu-id="88b6c-2216">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2216">1</span></span>

<span data-ttu-id="88b6c-2217">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2217">2</span></span>

<span data-ttu-id="88b6c-2218">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2218">3</span></span>

<span data-ttu-id="88b6c-2219">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2219">4</span></span>

<span data-ttu-id="88b6c-2220">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2220">5</span></span>

<span data-ttu-id="88b6c-2221">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2221">6</span></span>

<span data-ttu-id="88b6c-2222">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2222">7</span></span>

<span data-ttu-id="88b6c-2223">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2223">8</span></span>

<span data-ttu-id="88b6c-2224">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2224">9</span></span>

<span data-ttu-id="88b6c-2225">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2225">1</span></span><br/> <span data-ttu-id="88b6c-2226">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2226">0</span></span><br/>

<span data-ttu-id="88b6c-2227">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2227">1</span></span>

<span data-ttu-id="88b6c-2228">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2228">2</span></span>

<span data-ttu-id="88b6c-2229">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2229">3</span></span>

<span data-ttu-id="88b6c-2230">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2230">4</span></span>

<span data-ttu-id="88b6c-2231">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2231">5</span></span>

<span data-ttu-id="88b6c-2232">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2232">6</span></span>

<span data-ttu-id="88b6c-2233">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2233">7</span></span>

<span data-ttu-id="88b6c-2234">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2234">8</span></span>

<span data-ttu-id="88b6c-2235">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2235">9</span></span>

<span data-ttu-id="88b6c-2236">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2236">2</span></span><br/> <span data-ttu-id="88b6c-2237">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2237">0</span></span><br/>

<span data-ttu-id="88b6c-2238">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2238">1</span></span>

<span data-ttu-id="88b6c-2239">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2239">2</span></span>

<span data-ttu-id="88b6c-2240">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2240">3</span></span>

<span data-ttu-id="88b6c-2241">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2241">4</span></span>

<span data-ttu-id="88b6c-2242">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2242">5</span></span>

<span data-ttu-id="88b6c-2243">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2243">6</span></span>

<span data-ttu-id="88b6c-2244">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2244">7</span></span>

<span data-ttu-id="88b6c-2245">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2245">8</span></span>

<span data-ttu-id="88b6c-2246">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2246">9</span></span>

<span data-ttu-id="88b6c-2247">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2247">3</span></span><br/> <span data-ttu-id="88b6c-2248">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2248">0</span></span><br/>

<span data-ttu-id="88b6c-2249">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2249">1</span></span>

<span data-ttu-id="88b6c-2250">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="88b6c-2250">\_hRegion</span></span>

<span data-ttu-id="88b6c-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="88b6c-2251">\_cBookmarks</span></span>

<span data-ttu-id="88b6c-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="88b6c-2252">\_maxRet</span></span>

<span data-ttu-id="88b6c-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="88b6c-2253">\_cValidRet</span></span>

<span data-ttu-id="88b6c-2254">\_aBookmarks (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="88b6c-2255">\_ascRet (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="88b6c-2256">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2257">**\_ cBookmarks**：不帶正負號的32位整數，代表 aBookmarks 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="88b6c-2258">**\_ maxRet**：不帶正負號的32位整數，代表 ascRet 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="88b6c-2259">**\_ cValidRet**：不帶正負號的32位整數，代表 ascRet 陣列中有效的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="88b6c-2260">陣列中已定義有效的元素，但不正確元素未定義。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="88b6c-2261">**\_ aBookmarks**：書簽的陣列 (每個) 以4個位元組表示，如同從 CPMGetRowsOut 訊息取得的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="88b6c-2262">**\_ ASCRET**： HRESULT 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="88b6c-2263">將 CRowSeekByBookMark 當作 CPMGetRowsIn 要求的一部分傳送時，陣列中的專案數目必須等於 \_ cBookMarks。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="88b6c-2264">當用戶端傳送時，值必須設定為零，而且伺服器必須忽略陣列的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="88b6c-2265">當伺服器 (傳送) CPMGetRowsOut 訊息的一部分時，陣列中的值會指出每個資料列抓取的結果狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="88b6c-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="88b6c-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="88b6c-2267">CRowSeekNext 結構包含要在 CPMGetRowsIn 訊息中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="88b6c-2268">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2268">0</span></span>

<span data-ttu-id="88b6c-2269">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2269">1</span></span>

<span data-ttu-id="88b6c-2270">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2270">2</span></span>

<span data-ttu-id="88b6c-2271">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2271">3</span></span>

<span data-ttu-id="88b6c-2272">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2272">4</span></span>

<span data-ttu-id="88b6c-2273">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2273">5</span></span>

<span data-ttu-id="88b6c-2274">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2274">6</span></span>

<span data-ttu-id="88b6c-2275">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2275">7</span></span>

<span data-ttu-id="88b6c-2276">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2276">8</span></span>

<span data-ttu-id="88b6c-2277">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2277">9</span></span>

<span data-ttu-id="88b6c-2278">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2278">1</span></span><br/> <span data-ttu-id="88b6c-2279">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2279">0</span></span><br/>

<span data-ttu-id="88b6c-2280">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2280">1</span></span>

<span data-ttu-id="88b6c-2281">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2281">2</span></span>

<span data-ttu-id="88b6c-2282">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2282">3</span></span>

<span data-ttu-id="88b6c-2283">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2283">4</span></span>

<span data-ttu-id="88b6c-2284">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2284">5</span></span>

<span data-ttu-id="88b6c-2285">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2285">6</span></span>

<span data-ttu-id="88b6c-2286">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2286">7</span></span>

<span data-ttu-id="88b6c-2287">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2287">8</span></span>

<span data-ttu-id="88b6c-2288">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2288">9</span></span>

<span data-ttu-id="88b6c-2289">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2289">2</span></span><br/> <span data-ttu-id="88b6c-2290">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2290">0</span></span><br/>

<span data-ttu-id="88b6c-2291">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2291">1</span></span>

<span data-ttu-id="88b6c-2292">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2292">2</span></span>

<span data-ttu-id="88b6c-2293">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2293">3</span></span>

<span data-ttu-id="88b6c-2294">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2294">4</span></span>

<span data-ttu-id="88b6c-2295">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2295">5</span></span>

<span data-ttu-id="88b6c-2296">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2296">6</span></span>

<span data-ttu-id="88b6c-2297">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2297">7</span></span>

<span data-ttu-id="88b6c-2298">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2298">8</span></span>

<span data-ttu-id="88b6c-2299">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2299">9</span></span>

<span data-ttu-id="88b6c-2300">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2300">3</span></span><br/> <span data-ttu-id="88b6c-2301">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2301">0</span></span><br/>

<span data-ttu-id="88b6c-2302">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2302">1</span></span>

<span data-ttu-id="88b6c-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-2303">CiTblChapt</span></span>

<span data-ttu-id="88b6c-2304">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="88b6c-2304">\_hRegion</span></span>

<span data-ttu-id="88b6c-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="88b6c-2305">\_cskip</span></span>



 

<span data-ttu-id="88b6c-2306">**CiTblChapt**：不帶正負號的32位整數，指定要從中取得資料列的資料列集章節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="88b6c-2307">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2308">**\_ cskip**：不帶正負號的32位整數，代表要在資料列集中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="88b6c-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="88b6c-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="88b6c-2310">CRowsetProperties 結構包含查詢的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="88b6c-2311">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2311">0</span></span>

<span data-ttu-id="88b6c-2312">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2312">1</span></span>

<span data-ttu-id="88b6c-2313">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2313">2</span></span>

<span data-ttu-id="88b6c-2314">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2314">3</span></span>

<span data-ttu-id="88b6c-2315">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2315">4</span></span>

<span data-ttu-id="88b6c-2316">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2316">5</span></span>

<span data-ttu-id="88b6c-2317">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2317">6</span></span>

<span data-ttu-id="88b6c-2318">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2318">7</span></span>

<span data-ttu-id="88b6c-2319">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2319">8</span></span>

<span data-ttu-id="88b6c-2320">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2320">9</span></span>

<span data-ttu-id="88b6c-2321">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2321">1</span></span><br/> <span data-ttu-id="88b6c-2322">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2322">0</span></span><br/>

<span data-ttu-id="88b6c-2323">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2323">1</span></span>

<span data-ttu-id="88b6c-2324">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2324">2</span></span>

<span data-ttu-id="88b6c-2325">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2325">3</span></span>

<span data-ttu-id="88b6c-2326">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2326">4</span></span>

<span data-ttu-id="88b6c-2327">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2327">5</span></span>

<span data-ttu-id="88b6c-2328">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2328">6</span></span>

<span data-ttu-id="88b6c-2329">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2329">7</span></span>

<span data-ttu-id="88b6c-2330">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2330">8</span></span>

<span data-ttu-id="88b6c-2331">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2331">9</span></span>

<span data-ttu-id="88b6c-2332">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2332">2</span></span><br/> <span data-ttu-id="88b6c-2333">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2333">0</span></span><br/>

<span data-ttu-id="88b6c-2334">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2334">1</span></span>

<span data-ttu-id="88b6c-2335">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2335">2</span></span>

<span data-ttu-id="88b6c-2336">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2336">3</span></span>

<span data-ttu-id="88b6c-2337">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2337">4</span></span>

<span data-ttu-id="88b6c-2338">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2338">5</span></span>

<span data-ttu-id="88b6c-2339">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2339">6</span></span>

<span data-ttu-id="88b6c-2340">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2340">7</span></span>

<span data-ttu-id="88b6c-2341">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2341">8</span></span>

<span data-ttu-id="88b6c-2342">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2342">9</span></span>

<span data-ttu-id="88b6c-2343">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2343">3</span></span><br/> <span data-ttu-id="88b6c-2344">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2344">0</span></span><br/>

<span data-ttu-id="88b6c-2345">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2345">1</span></span>

<span data-ttu-id="88b6c-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="88b6c-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="88b6c-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="88b6c-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="88b6c-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="88b6c-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="88b6c-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="88b6c-2349">\_cMaxResults</span></span>

<span data-ttu-id="88b6c-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="88b6c-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="88b6c-2351">**\_ uBooleanOptions**：此欄位最小的3位必須包含下列三個值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="88b6c-2352">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2352">Value</span></span>                  | <span data-ttu-id="88b6c-2353">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88b6c-2354">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="88b6c-2355">資料指標只能向前移動。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="88b6c-2356">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="88b6c-2357">資料指標可移至任何位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="88b6c-2358">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="88b6c-2359">您可以將游標移至任何位置，並以任何方向提取。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="88b6c-2360">其餘的位可能是明確的，或設定為邏輯或的任何下列值組合：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="88b6c-2361">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2361">Value</span></span>                     | <span data-ttu-id="88b6c-2362">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="88b6c-2364">用戶端不會等待執行完成。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="88b6c-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="88b6c-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="88b6c-2366">傳回所遇到的第一個資料列，而不是最符合的專案。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="88b6c-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="88b6c-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="88b6c-2368">在使用查詢完成用戶端之前，伺服器不能捨棄資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="88b6c-2369">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="88b6c-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="88b6c-2370">資料列集支援章節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="88b6c-2371">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="88b6c-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="88b6c-2372">請只從索引（而不是檔案系統）回答查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="88b6c-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="88b6c-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="88b6c-2374">索引服務是在執行移除結果時，考慮將回應時間優化到用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="88b6c-2375">**\_ ulMaxOpenRows**：不帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="88b6c-2376">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="88b6c-2377">未使用且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2378">**\_ ulMemoryUsage**：不帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="88b6c-2379">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="88b6c-2380">未使用且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-2381">**\_ cMaxResults**：32位不帶正負號的整數，指定要針對查詢傳回的最大資料列數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="88b6c-2382">**\_ cCmdTimeout**：32位不帶正負號的整數，指定查詢開始時間和自動終止的秒數，從查詢在伺服器上開始執行的時間算起。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="88b6c-2383">值為0x00000000 表示查詢不會超時。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="88b6c-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="88b6c-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="88b6c-2385">CRowVariant 結構包含儲存在 CPMGetRowsOut 訊息中之可變長度資料類型的固定大小部分。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="88b6c-2386">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2386">0</span></span>

<span data-ttu-id="88b6c-2387">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2387">1</span></span>

<span data-ttu-id="88b6c-2388">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2388">2</span></span>

<span data-ttu-id="88b6c-2389">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2389">3</span></span>

<span data-ttu-id="88b6c-2390">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2390">4</span></span>

<span data-ttu-id="88b6c-2391">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2391">5</span></span>

<span data-ttu-id="88b6c-2392">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2392">6</span></span>

<span data-ttu-id="88b6c-2393">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2393">7</span></span>

<span data-ttu-id="88b6c-2394">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2394">8</span></span>

<span data-ttu-id="88b6c-2395">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2395">9</span></span>

<span data-ttu-id="88b6c-2396">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2396">1</span></span><br/> <span data-ttu-id="88b6c-2397">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2397">0</span></span><br/>

<span data-ttu-id="88b6c-2398">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2398">1</span></span>

<span data-ttu-id="88b6c-2399">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2399">2</span></span>

<span data-ttu-id="88b6c-2400">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2400">3</span></span>

<span data-ttu-id="88b6c-2401">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2401">4</span></span>

<span data-ttu-id="88b6c-2402">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2402">5</span></span>

<span data-ttu-id="88b6c-2403">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2403">6</span></span>

<span data-ttu-id="88b6c-2404">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2404">7</span></span>

<span data-ttu-id="88b6c-2405">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2405">8</span></span>

<span data-ttu-id="88b6c-2406">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2406">9</span></span>

<span data-ttu-id="88b6c-2407">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2407">2</span></span><br/> <span data-ttu-id="88b6c-2408">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2408">0</span></span><br/>

<span data-ttu-id="88b6c-2409">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2409">1</span></span>

<span data-ttu-id="88b6c-2410">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2410">2</span></span>

<span data-ttu-id="88b6c-2411">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2411">3</span></span>

<span data-ttu-id="88b6c-2412">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2412">4</span></span>

<span data-ttu-id="88b6c-2413">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2413">5</span></span>

<span data-ttu-id="88b6c-2414">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2414">6</span></span>

<span data-ttu-id="88b6c-2415">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2415">7</span></span>

<span data-ttu-id="88b6c-2416">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2416">8</span></span>

<span data-ttu-id="88b6c-2417">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2417">9</span></span>

<span data-ttu-id="88b6c-2418">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2418">3</span></span><br/> <span data-ttu-id="88b6c-2419">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2419">0</span></span><br/>

<span data-ttu-id="88b6c-2420">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2420">1</span></span>

<span data-ttu-id="88b6c-2421">vType</span><span class="sxs-lookup"><span data-stu-id="88b6c-2421">vType</span></span>

<span data-ttu-id="88b6c-2422">reserved1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2422">reserved1</span></span>

<span data-ttu-id="88b6c-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2423">reserved2</span></span>

<span data-ttu-id="88b6c-2424"> (選擇性) 位移</span><span class="sxs-lookup"><span data-stu-id="88b6c-2424">Offset (optional)</span></span>



 

<span data-ttu-id="88b6c-2425">**vType**：類型指標，表示 vValue 的類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="88b6c-2426">它必須是2.2.1.1 區段中所指定的其中一個 VARENUM 值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="88b6c-2427">**reserved1**：未使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="88b6c-2428">值可以設定為任何任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="88b6c-2429">**reserved2**：未使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="88b6c-2430">值可以設定為任何任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="88b6c-2431">**Offset**：變數長度資料的位移 (例如字串) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="88b6c-2432">這必須是32位值 (4 個位元組長) 如果32位位移是使用於區段 2.2.3.16) 中的規則 (，或64位元組的值 (8 個位元組長) 如果使用的是64位位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="88b6c-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="88b6c-2434">CSortSet 結構包含查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="88b6c-2435">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2435">0</span></span>

<span data-ttu-id="88b6c-2436">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2436">1</span></span>

<span data-ttu-id="88b6c-2437">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2437">2</span></span>

<span data-ttu-id="88b6c-2438">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2438">3</span></span>

<span data-ttu-id="88b6c-2439">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2439">4</span></span>

<span data-ttu-id="88b6c-2440">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2440">5</span></span>

<span data-ttu-id="88b6c-2441">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2441">6</span></span>

<span data-ttu-id="88b6c-2442">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2442">7</span></span>

<span data-ttu-id="88b6c-2443">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2443">8</span></span>

<span data-ttu-id="88b6c-2444">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2444">9</span></span>

<span data-ttu-id="88b6c-2445">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2445">1</span></span><br/> <span data-ttu-id="88b6c-2446">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2446">0</span></span><br/>

<span data-ttu-id="88b6c-2447">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2447">1</span></span>

<span data-ttu-id="88b6c-2448">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2448">2</span></span>

<span data-ttu-id="88b6c-2449">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2449">3</span></span>

<span data-ttu-id="88b6c-2450">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2450">4</span></span>

<span data-ttu-id="88b6c-2451">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2451">5</span></span>

<span data-ttu-id="88b6c-2452">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2452">6</span></span>

<span data-ttu-id="88b6c-2453">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2453">7</span></span>

<span data-ttu-id="88b6c-2454">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2454">8</span></span>

<span data-ttu-id="88b6c-2455">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2455">9</span></span>

<span data-ttu-id="88b6c-2456">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2456">2</span></span><br/> <span data-ttu-id="88b6c-2457">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2457">0</span></span><br/>

<span data-ttu-id="88b6c-2458">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2458">1</span></span>

<span data-ttu-id="88b6c-2459">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2459">2</span></span>

<span data-ttu-id="88b6c-2460">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2460">3</span></span>

<span data-ttu-id="88b6c-2461">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2461">4</span></span>

<span data-ttu-id="88b6c-2462">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2462">5</span></span>

<span data-ttu-id="88b6c-2463">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2463">6</span></span>

<span data-ttu-id="88b6c-2464">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2464">7</span></span>

<span data-ttu-id="88b6c-2465">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2465">8</span></span>

<span data-ttu-id="88b6c-2466">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2466">9</span></span>

<span data-ttu-id="88b6c-2467">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2467">3</span></span><br/> <span data-ttu-id="88b6c-2468">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2468">0</span></span><br/>

<span data-ttu-id="88b6c-2469">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2469">1</span></span>

<span data-ttu-id="88b6c-2470">Count</span><span class="sxs-lookup"><span data-stu-id="88b6c-2470">Count</span></span>

<span data-ttu-id="88b6c-2471">sortArray (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="88b6c-2472">**計數**：指定 sortArray 中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="88b6c-2473">**sortArray**： CSort 結構的陣列，描述排序查詢結果的順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="88b6c-2474">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="88b6c-2475">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="88b6c-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="88b6c-2477">CTableColumn 結構包含 CPMSetBindingsIn 訊息的資料行</span><span class="sxs-lookup"><span data-stu-id="88b6c-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="88b6c-2478">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2478">0</span></span>

<span data-ttu-id="88b6c-2479">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2479">1</span></span>

<span data-ttu-id="88b6c-2480">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2480">2</span></span>

<span data-ttu-id="88b6c-2481">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2481">3</span></span>

<span data-ttu-id="88b6c-2482">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2482">4</span></span>

<span data-ttu-id="88b6c-2483">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2483">5</span></span>

<span data-ttu-id="88b6c-2484">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2484">6</span></span>

<span data-ttu-id="88b6c-2485">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2485">7</span></span>

<span data-ttu-id="88b6c-2486">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2486">8</span></span>

<span data-ttu-id="88b6c-2487">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2487">9</span></span>

<span data-ttu-id="88b6c-2488">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2488">1</span></span><br/> <span data-ttu-id="88b6c-2489">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2489">0</span></span><br/>

<span data-ttu-id="88b6c-2490">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2490">1</span></span>

<span data-ttu-id="88b6c-2491">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2491">2</span></span>

<span data-ttu-id="88b6c-2492">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2492">3</span></span>

<span data-ttu-id="88b6c-2493">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2493">4</span></span>

<span data-ttu-id="88b6c-2494">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2494">5</span></span>

<span data-ttu-id="88b6c-2495">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2495">6</span></span>

<span data-ttu-id="88b6c-2496">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2496">7</span></span>

<span data-ttu-id="88b6c-2497">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2497">8</span></span>

<span data-ttu-id="88b6c-2498">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2498">9</span></span>

<span data-ttu-id="88b6c-2499">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2499">2</span></span><br/> <span data-ttu-id="88b6c-2500">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2500">0</span></span><br/>

<span data-ttu-id="88b6c-2501">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2501">1</span></span>

<span data-ttu-id="88b6c-2502">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2502">2</span></span>

<span data-ttu-id="88b6c-2503">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2503">3</span></span>

<span data-ttu-id="88b6c-2504">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2504">4</span></span>

<span data-ttu-id="88b6c-2505">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2505">5</span></span>

<span data-ttu-id="88b6c-2506">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2506">6</span></span>

<span data-ttu-id="88b6c-2507">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2507">7</span></span>

<span data-ttu-id="88b6c-2508">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2508">8</span></span>

<span data-ttu-id="88b6c-2509">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2509">9</span></span>

<span data-ttu-id="88b6c-2510">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2510">3</span></span><br/> <span data-ttu-id="88b6c-2511">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2511">0</span></span><br/>

<span data-ttu-id="88b6c-2512">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2512">1</span></span>

<span data-ttu-id="88b6c-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-2513">PropSpec</span></span>

<span data-ttu-id="88b6c-2514">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2514">...(variable)</span></span>

<span data-ttu-id="88b6c-2515">vType</span><span class="sxs-lookup"><span data-stu-id="88b6c-2515">vType</span></span>

<span data-ttu-id="88b6c-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="88b6c-2516">ValueUsed</span></span>

<span data-ttu-id="88b6c-2517">\_padding1 (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="88b6c-2518">ValueOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="88b6c-2519">ValueSize (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2519">ValueSize (optional)</span></span>

<span data-ttu-id="88b6c-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="88b6c-2520">StatusUsed</span></span>

<span data-ttu-id="88b6c-2521">\_padding2 (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="88b6c-2522">StatusOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="88b6c-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="88b6c-2523">LengthUsed</span></span>

<span data-ttu-id="88b6c-2524">\_padding3 (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="88b6c-2525">LengthOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="88b6c-2526">**PropSpec**：在區段2.2.1.3 中指定的 CFullPropSpec 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="88b6c-2527">**vType**：指定包含在資料行中的資料數值型別。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="88b6c-2528">如需此欄位的值清單，請參閱2.2.1.1 一節中的 vType 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="88b6c-2529">**ValueUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="88b6c-2530">如果設定為0x01，資料行會在固定大小的資料列內傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="88b6c-2531">如果設定為0x00，則資料行的值會在緩衝區結尾的可變長度區段中傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="88b6c-2532">**\_ padding1**：一個位元組欄位必須在 ValueOffset 之前插入，如果沒有，則 ValueOffset 不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="88b6c-2533">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="88b6c-2534">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2535">**ValueOffset**：不帶正負號的2位元組整數，指定資料列中資料行值的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="88b6c-2536">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2537">**ValueSize**：不帶正負號的2位元組整數，指定資料行值的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="88b6c-2538">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2539">**StatusUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="88b6c-2540">如果設定為0x01，資料行的狀態就會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="88b6c-2541">若為0x00，則資料行的狀態不會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="88b6c-2542">**\_ padding2**：一個位元組欄位必須在 StatusOffset 之前插入，如果沒有此欄位，StatusOffset 欄位就不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="88b6c-2543">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="88b6c-2544">如果 StatusUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2545">**StatusOffset**：不帶正負號的2位元組整數，指定資料列中資料行狀態的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="88b6c-2546">如果 StatusUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2547">**LengthUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="88b6c-2548">如果設定為0x01，資料行的長度會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="88b6c-2549">如果0x00，則資料行的長度不能在資料列內傳輸。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="88b6c-2550">**\_ padding3**：一個位元組欄位必須在 LengthOffset 之前插入，如果沒有，則 LengthOffset 不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="88b6c-2551">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="88b6c-2552">如果 LengthUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="88b6c-2553">**LengthOffset**：不帶正負號的2位元組整數，指定資料列中資料行長度的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="88b6c-2554">如果 LengthUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="88b6c-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="88b6c-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="88b6c-2556">SERIALIZEDPROPERTYVALUE 結構包含序列化值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="88b6c-2557">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2557">0</span></span>

<span data-ttu-id="88b6c-2558">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2558">1</span></span>

<span data-ttu-id="88b6c-2559">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2559">2</span></span>

<span data-ttu-id="88b6c-2560">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2560">3</span></span>

<span data-ttu-id="88b6c-2561">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2561">4</span></span>

<span data-ttu-id="88b6c-2562">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2562">5</span></span>

<span data-ttu-id="88b6c-2563">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2563">6</span></span>

<span data-ttu-id="88b6c-2564">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2564">7</span></span>

<span data-ttu-id="88b6c-2565">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2565">8</span></span>

<span data-ttu-id="88b6c-2566">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2566">9</span></span>

<span data-ttu-id="88b6c-2567">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2567">1</span></span><br/> <span data-ttu-id="88b6c-2568">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2568">0</span></span><br/>

<span data-ttu-id="88b6c-2569">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2569">1</span></span>

<span data-ttu-id="88b6c-2570">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2570">2</span></span>

<span data-ttu-id="88b6c-2571">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2571">3</span></span>

<span data-ttu-id="88b6c-2572">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2572">4</span></span>

<span data-ttu-id="88b6c-2573">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2573">5</span></span>

<span data-ttu-id="88b6c-2574">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2574">6</span></span>

<span data-ttu-id="88b6c-2575">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2575">7</span></span>

<span data-ttu-id="88b6c-2576">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2576">8</span></span>

<span data-ttu-id="88b6c-2577">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2577">9</span></span>

<span data-ttu-id="88b6c-2578">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2578">2</span></span><br/> <span data-ttu-id="88b6c-2579">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2579">0</span></span><br/>

<span data-ttu-id="88b6c-2580">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2580">1</span></span>

<span data-ttu-id="88b6c-2581">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2581">2</span></span>

<span data-ttu-id="88b6c-2582">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2582">3</span></span>

<span data-ttu-id="88b6c-2583">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2583">4</span></span>

<span data-ttu-id="88b6c-2584">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2584">5</span></span>

<span data-ttu-id="88b6c-2585">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2585">6</span></span>

<span data-ttu-id="88b6c-2586">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2586">7</span></span>

<span data-ttu-id="88b6c-2587">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2587">8</span></span>

<span data-ttu-id="88b6c-2588">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2588">9</span></span>

<span data-ttu-id="88b6c-2589">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2589">3</span></span><br/> <span data-ttu-id="88b6c-2590">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2590">0</span></span><br/>

<span data-ttu-id="88b6c-2591">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2591">1</span></span>

<span data-ttu-id="88b6c-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="88b6c-2592">dwType</span></span>

<span data-ttu-id="88b6c-2593">rgb (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2593">rgb (variable)</span></span>



 

<span data-ttu-id="88b6c-2594">**dwType**：在 section 2.2.1.1 中定義的其中一個 variant 類型，可以與 variant 類型修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="88b6c-2595">針對所有 variant 類型，除了與 VT 陣列結合的類型之外， \_ SERIALIZEDPROPERTYVALUE 具有與 CBaseStorageVariant 相同的版面配置，如2.2.1.1 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="88b6c-2596">如果 variant 類型與 VT \_ 陣列類型修飾詞結合，則會使用 SAFEARRAY2 （在2.2.1.2.1.1 區段中指定），而不是 CBaseStorageVariant 的 vValue 欄位中的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="88b6c-2597">**rgb**：序列化值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="88b6c-2598">請參閱2.2.1.1 中 vValue 的序列化詳細資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="88b6c-2599">2.2.2 訊息標頭</span><span class="sxs-lookup"><span data-stu-id="88b6c-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="88b6c-2600">所有內容索引服務通訊協定訊息都有16位元組的標頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="88b6c-2601">以下是顯示內容索引服務通訊協定訊息標頭格式的圖表。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="88b6c-2602">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2602">0</span></span>

<span data-ttu-id="88b6c-2603">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2603">1</span></span>

<span data-ttu-id="88b6c-2604">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2604">2</span></span>

<span data-ttu-id="88b6c-2605">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2605">3</span></span>

<span data-ttu-id="88b6c-2606">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2606">4</span></span>

<span data-ttu-id="88b6c-2607">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2607">5</span></span>

<span data-ttu-id="88b6c-2608">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2608">6</span></span>

<span data-ttu-id="88b6c-2609">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2609">7</span></span>

<span data-ttu-id="88b6c-2610">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2610">8</span></span>

<span data-ttu-id="88b6c-2611">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2611">9</span></span>

<span data-ttu-id="88b6c-2612">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2612">1</span></span><br/> <span data-ttu-id="88b6c-2613">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2613">0</span></span><br/>

<span data-ttu-id="88b6c-2614">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2614">1</span></span>

<span data-ttu-id="88b6c-2615">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2615">2</span></span>

<span data-ttu-id="88b6c-2616">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2616">3</span></span>

<span data-ttu-id="88b6c-2617">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2617">4</span></span>

<span data-ttu-id="88b6c-2618">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2618">5</span></span>

<span data-ttu-id="88b6c-2619">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2619">6</span></span>

<span data-ttu-id="88b6c-2620">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2620">7</span></span>

<span data-ttu-id="88b6c-2621">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2621">8</span></span>

<span data-ttu-id="88b6c-2622">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2622">9</span></span>

<span data-ttu-id="88b6c-2623">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2623">2</span></span><br/> <span data-ttu-id="88b6c-2624">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2624">0</span></span><br/>

<span data-ttu-id="88b6c-2625">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2625">1</span></span>

<span data-ttu-id="88b6c-2626">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2626">2</span></span>

<span data-ttu-id="88b6c-2627">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2627">3</span></span>

<span data-ttu-id="88b6c-2628">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2628">4</span></span>

<span data-ttu-id="88b6c-2629">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2629">5</span></span>

<span data-ttu-id="88b6c-2630">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2630">6</span></span>

<span data-ttu-id="88b6c-2631">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2631">7</span></span>

<span data-ttu-id="88b6c-2632">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2632">8</span></span>

<span data-ttu-id="88b6c-2633">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2633">9</span></span>

<span data-ttu-id="88b6c-2634">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2634">3</span></span><br/> <span data-ttu-id="88b6c-2635">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2635">0</span></span><br/>

<span data-ttu-id="88b6c-2636">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2636">1</span></span>

<span data-ttu-id="88b6c-2637">\_msg</span><span class="sxs-lookup"><span data-stu-id="88b6c-2637">\_msg</span></span>

<span data-ttu-id="88b6c-2638">\_地位</span><span class="sxs-lookup"><span data-stu-id="88b6c-2638">\_status</span></span>

<span data-ttu-id="88b6c-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="88b6c-2639">\_ulChecksum</span></span>

<span data-ttu-id="88b6c-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="88b6c-2641">\_**msg**：識別標頭後面之訊息類型的32位整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="88b6c-2642">下表列出內容索引服務的通訊協定訊息，以及為每個訊息指定的整數值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="88b6c-2643">如下表所示，某些值會識別資料表中的2個訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="88b6c-2644">在這些情況下，可透過訊息流程的方向識別標頭後面的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="88b6c-2645">如果方向是 [用戶端至伺服器]，則會指出訊息名稱後面附加有 "In" 的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="88b6c-2646">如果方向為 [伺服器至用戶端]，則會指出訊息名稱後面附加有 "Out" 的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="88b6c-2647">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2647">Value</span></span>      | <span data-ttu-id="88b6c-2648">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="88b6c-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2649">0x000000C8</span></span> | <span data-ttu-id="88b6c-2650">CPMConnectIn 或 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="88b6c-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2651">0x000000C9</span></span> | <span data-ttu-id="88b6c-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="88b6c-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="88b6c-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="88b6c-2653">0x000000CA</span></span> | <span data-ttu-id="88b6c-2654">CPMCreateQueryIn 或 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="88b6c-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="88b6c-2655">0x000000CB</span></span> | <span data-ttu-id="88b6c-2656">CPMFreeCursorIn 或 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="88b6c-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="88b6c-2657">0x000000CC</span></span> | <span data-ttu-id="88b6c-2658">CPMGetRowsIn 或 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="88b6c-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="88b6c-2659">0x000000CD</span></span> | <span data-ttu-id="88b6c-2660">CPMRatioFinishedIn 或 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="88b6c-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="88b6c-2661">0x000000CE</span></span> | <span data-ttu-id="88b6c-2662">CPMCompareBmkIn 或 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="88b6c-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="88b6c-2663">0x000000CF</span></span> | <span data-ttu-id="88b6c-2664">CPMGetApproximatePositionIn 或 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="88b6c-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2665">0x000000D0</span></span> | <span data-ttu-id="88b6c-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="88b6c-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2667">0x000000D1</span></span> | <span data-ttu-id="88b6c-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="88b6c-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="88b6c-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2669">0x000000D2</span></span> | <span data-ttu-id="88b6c-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="88b6c-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2671">0x000000D7</span></span> | <span data-ttu-id="88b6c-2672">CPMGetQueryStatusIn 或 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="88b6c-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2673">0x000000D9</span></span> | <span data-ttu-id="88b6c-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="88b6c-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2675">0x000000E1</span></span> | <span data-ttu-id="88b6c-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="88b6c-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2677">0x000000E4</span></span> | <span data-ttu-id="88b6c-2678">CPMFetchValueIn 或 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="88b6c-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2679">0x000000E6</span></span> | <span data-ttu-id="88b6c-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="88b6c-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2681">0x000000E7</span></span> | <span data-ttu-id="88b6c-2682">CPMGetQueryStatusExIn 或 PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="88b6c-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2683">0x000000E8</span></span> | <span data-ttu-id="88b6c-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="88b6c-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2685">0x000000E9</span></span> | <span data-ttu-id="88b6c-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="88b6c-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="88b6c-2687">0x000000EC</span></span> | <span data-ttu-id="88b6c-2688">CPMSetCatStateIn 或 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="88b6c-2689">\_**狀態**： HRESULT \[ ms-chap \] ，指出要求之作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="88b6c-2690">*Windows 行為：用戶端一律將 \_ status 欄位設定為0x00000000。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="88b6c-2691">**\_ ulChecksum**： \_ ULCHECKSUM 的計算方式必須如下列訊息的區段3.2.4 所指定：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="88b6c-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="88b6c-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="88b6c-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="88b6c-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="88b6c-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="88b6c-2697">若為所有其他訊息， \_ ULCHECKSUM 必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="88b6c-2698">用戶端必須忽略 \_ ulChecksum 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="88b6c-2699">**\_ ulReserved2**：必須設定為0，而且接收者會忽略它。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="88b6c-2700">2.2.3 訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="88b6c-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="88b6c-2702">CPMCiStateInOut 訊息包含索引服務狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="88b6c-2703">標頭後面的 CPMCiStateInOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-2704">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2704">0</span></span>

<span data-ttu-id="88b6c-2705">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2705">1</span></span>

<span data-ttu-id="88b6c-2706">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2706">2</span></span>

<span data-ttu-id="88b6c-2707">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2707">3</span></span>

<span data-ttu-id="88b6c-2708">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2708">4</span></span>

<span data-ttu-id="88b6c-2709">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2709">5</span></span>

<span data-ttu-id="88b6c-2710">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2710">6</span></span>

<span data-ttu-id="88b6c-2711">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2711">7</span></span>

<span data-ttu-id="88b6c-2712">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2712">8</span></span>

<span data-ttu-id="88b6c-2713">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2713">9</span></span>

<span data-ttu-id="88b6c-2714">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2714">1</span></span><br/> <span data-ttu-id="88b6c-2715">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2715">0</span></span><br/>

<span data-ttu-id="88b6c-2716">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2716">1</span></span>

<span data-ttu-id="88b6c-2717">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2717">2</span></span>

<span data-ttu-id="88b6c-2718">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2718">3</span></span>

<span data-ttu-id="88b6c-2719">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2719">4</span></span>

<span data-ttu-id="88b6c-2720">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2720">5</span></span>

<span data-ttu-id="88b6c-2721">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2721">6</span></span>

<span data-ttu-id="88b6c-2722">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2722">7</span></span>

<span data-ttu-id="88b6c-2723">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2723">8</span></span>

<span data-ttu-id="88b6c-2724">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2724">9</span></span>

<span data-ttu-id="88b6c-2725">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2725">2</span></span><br/> <span data-ttu-id="88b6c-2726">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2726">0</span></span><br/>

<span data-ttu-id="88b6c-2727">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2727">1</span></span>

<span data-ttu-id="88b6c-2728">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2728">2</span></span>

<span data-ttu-id="88b6c-2729">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2729">3</span></span>

<span data-ttu-id="88b6c-2730">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2730">4</span></span>

<span data-ttu-id="88b6c-2731">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2731">5</span></span>

<span data-ttu-id="88b6c-2732">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2732">6</span></span>

<span data-ttu-id="88b6c-2733">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2733">7</span></span>

<span data-ttu-id="88b6c-2734">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2734">8</span></span>

<span data-ttu-id="88b6c-2735">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2735">9</span></span>

<span data-ttu-id="88b6c-2736">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2736">3</span></span><br/> <span data-ttu-id="88b6c-2737">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2737">0</span></span><br/>

<span data-ttu-id="88b6c-2738">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2738">1</span></span>

<span data-ttu-id="88b6c-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="88b6c-2739">cbStruct</span></span>

<span data-ttu-id="88b6c-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="88b6c-2740">cWordList</span></span>

<span data-ttu-id="88b6c-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="88b6c-2741">cPersistentIndex</span></span>

<span data-ttu-id="88b6c-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="88b6c-2742">cQueries</span></span>

<span data-ttu-id="88b6c-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="88b6c-2743">cDocuments</span></span>

<span data-ttu-id="88b6c-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="88b6c-2744">cFreshTest</span></span>

<span data-ttu-id="88b6c-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="88b6c-2745">dwMergeProgress</span></span>

<span data-ttu-id="88b6c-2746">eState</span><span class="sxs-lookup"><span data-stu-id="88b6c-2746">eState</span></span>

<span data-ttu-id="88b6c-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="88b6c-2747">cFilteredDocuments</span></span>

<span data-ttu-id="88b6c-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="88b6c-2748">cTotalDocuments</span></span>

<span data-ttu-id="88b6c-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="88b6c-2749">cPendingScans</span></span>

<span data-ttu-id="88b6c-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="88b6c-2750">dwIndexSize</span></span>

<span data-ttu-id="88b6c-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="88b6c-2751">cUniqueKeys</span></span>

<span data-ttu-id="88b6c-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="88b6c-2752">cSecQDocuments</span></span>

<span data-ttu-id="88b6c-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="88b6c-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="88b6c-2754">**cbStruct**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="88b6c-2755">此訊息的大小（以位元組為單位） (不包括通用標頭) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="88b6c-2756">必須設為0x0000003C。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="88b6c-2757">**cWordList**：32位不帶正負號的整數，表示為最近編制索引的檔所建立的初始索引計數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="88b6c-2758">**cPersistentIndex**：32位不帶正負號的整數，表示持續性索引的計數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="88b6c-2759">**cQueries**：32位不帶正負號的整數，表示正在執行的查詢數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="88b6c-2760">**cDocuments**：32位不帶正負號的整數，指出等候編制索引的檔總數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="88b6c-2761">**cFreshTest**：32位不帶正負號的整數，指出未針對效能進行完整優化的唯一檔數目，以及索引中的資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="88b6c-2762">**dwMergeProgress**：不帶正負號的32位整數，指定目前的索引完整優化的完成百分比（如果目前正在進行優化）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="88b6c-2763">必須小於或等於100。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="88b6c-2764">**資產**：依 \_ \_ \* 下表所定義的一或多個 CI 狀態常數所提供的內容編制索引狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="88b6c-2765">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2765">Value</span></span>                                         | <span data-ttu-id="88b6c-2766">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-2767">CI \_ 狀態 \_ 陰影 \_ 合併0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="88b6c-2768">索引服務正在優化某些索引，以降低記憶體使用量並提升查詢效能。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="88b6c-2769">CI \_ 狀態 \_ 主要 \_ 合併0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="88b6c-2770">索引服務正在進行所有索引的完整優化處理。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="88b6c-2771">CI \_ 狀態 \_ 內容 \_ 掃描 \_ 所需的0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="88b6c-2772">索引中的某些檔已變更，而索引服務需要判斷已新增、變更或刪除的檔。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="88b6c-2773">CI \_ 狀態 \_ 鍛煉 \_ 合併0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="88b6c-2774">索引服務正在將索引優化，以降低記憶體使用量並提升查詢效能。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="88b6c-2775">此程式比 CI 狀態陰影合併值所識別的程式更完整 \_ \_ \_ ，但不像 ci \_ 狀態 \_ 主要合併值所指定的完整 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="88b6c-2776">這類優化是實作為特定的，因為它們相依于內部儲存資料的方式;優化不會以回應時間以外的任何方式影響通訊協定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="88b6c-2777">CI \_ 狀態 \_ 掃描0x00000010</span><span class="sxs-lookup"><span data-stu-id="88b6c-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="88b6c-2778">索引服務正在檢查目錄或一組目錄，以查看自上次索引目錄之後，是否已新增、刪除或更新任何檔案。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="88b6c-2779">CI \_ 狀態 \_ 復原0x00000020</span><span class="sxs-lookup"><span data-stu-id="88b6c-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="88b6c-2780">服務從上次儲存的狀態開始，而且正在復原。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="88b6c-2781">CI \_ 狀態 \_ 低 \_ 記憶體0x00000080</span><span class="sxs-lookup"><span data-stu-id="88b6c-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="88b6c-2782">伺服器的大部分虛擬記憶體正在使用中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="88b6c-2783">CI \_ 狀態 \_ 高 \_ IO 0x00000100</span><span class="sxs-lookup"><span data-stu-id="88b6c-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="88b6c-2784">伺服器上的輸入/輸出 (i/o) 活動的層級相對較高。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="88b6c-2785">CI \_ 狀態 \_ 主要 \_ 合併已 \_ 暫停0x00000200</span><span class="sxs-lookup"><span data-stu-id="88b6c-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="88b6c-2786">所有進行中之索引的完整優化程式都已暫停。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="88b6c-2787">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="88b6c-2788">CI \_ 狀態 \_ 唯讀 \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="88b6c-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="88b6c-2789">將新檔挑選至索引的索引服務部分已暫停。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="88b6c-2790">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="88b6c-2791">CI \_ 狀態 \_ 電池 \_ 電力0x00000800</span><span class="sxs-lookup"><span data-stu-id="88b6c-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="88b6c-2792">將新檔挑選至索引的索引服務部分已暫停，以節省電池存留期，但仍會回復查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="88b6c-2793">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="88b6c-2794">CI \_ 狀態 \_ 使用者使用中 \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="88b6c-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="88b6c-2795">將新檔挑選至索引的索引服務部分，因為使用者 (鍵盤或滑鼠) 的高度活動，但仍在回復查詢，所以已暫停。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="88b6c-2796">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="88b6c-2797">CI \_ 狀態 \_ 開始0x00002000</span><span class="sxs-lookup"><span data-stu-id="88b6c-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="88b6c-2798">服務正在啟動。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2798">The service is starting.</span></span> <span data-ttu-id="88b6c-2799">您可以執行查詢，但尚未啟用掃描和通知。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="88b6c-2800">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="88b6c-2801">\_ \_ 讀取 \_ USN 0x00004000 的 CI 狀態</span><span class="sxs-lookup"><span data-stu-id="88b6c-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="88b6c-2802">服務未讀取檔案系統所保留的記錄檔，以追蹤磁片區中檔案或目錄的變更，因此索引可能不是最新狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="88b6c-2803">**cFilteredDocuments**：32位不帶正負號整數，指出自開始編制內容索引之後編制索引的檔數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="88b6c-2804">**cTotalDocuments**：32位不帶正負號的整數，表示系統中的檔總數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="88b6c-2805">**cPendingScans**：32位不帶正負號的整數，表示暫止高階索引編制作業的數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="88b6c-2806">此值的意義是提供者專屬的，但預期會有較大的數位，以表示保留更多索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="88b6c-2807">*Windows 行為*：此值通常是零，但在開始編制索引之後，或在通知佇列溢出之後立即發生。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="88b6c-2808">**dwIndexSize**：32位不帶正負號的整數，表示索引的大小（以 mb 為單位） (不包括屬性快取) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="88b6c-2809">**cUniqueKeys**：32位不帶正負號的整數，表示目錄中唯一索引鍵的大約數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="88b6c-2810">**cSecQDocuments**：32位不帶正負號的整數，指出索引服務將重新嘗試編制索引的檔數目，因為初始索引嘗試期間發生失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="88b6c-2811">**dwPropCacheSize**：32位不帶正負號的整數，表示屬性快取的大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="88b6c-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="88b6c-2813">CPMSetCatStateIn 訊息會設定目錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="88b6c-2814">標頭後面的 CPMSetCatStateIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-2815">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2815">0</span></span>

<span data-ttu-id="88b6c-2816">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2816">1</span></span>

<span data-ttu-id="88b6c-2817">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2817">2</span></span>

<span data-ttu-id="88b6c-2818">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2818">3</span></span>

<span data-ttu-id="88b6c-2819">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2819">4</span></span>

<span data-ttu-id="88b6c-2820">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2820">5</span></span>

<span data-ttu-id="88b6c-2821">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2821">6</span></span>

<span data-ttu-id="88b6c-2822">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2822">7</span></span>

<span data-ttu-id="88b6c-2823">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2823">8</span></span>

<span data-ttu-id="88b6c-2824">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2824">9</span></span>

<span data-ttu-id="88b6c-2825">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2825">1</span></span><br/> <span data-ttu-id="88b6c-2826">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2826">0</span></span><br/>

<span data-ttu-id="88b6c-2827">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2827">1</span></span>

<span data-ttu-id="88b6c-2828">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2828">2</span></span>

<span data-ttu-id="88b6c-2829">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2829">3</span></span>

<span data-ttu-id="88b6c-2830">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2830">4</span></span>

<span data-ttu-id="88b6c-2831">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2831">5</span></span>

<span data-ttu-id="88b6c-2832">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2832">6</span></span>

<span data-ttu-id="88b6c-2833">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2833">7</span></span>

<span data-ttu-id="88b6c-2834">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2834">8</span></span>

<span data-ttu-id="88b6c-2835">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2835">9</span></span>

<span data-ttu-id="88b6c-2836">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2836">2</span></span><br/> <span data-ttu-id="88b6c-2837">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2837">0</span></span><br/>

<span data-ttu-id="88b6c-2838">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2838">1</span></span>

<span data-ttu-id="88b6c-2839">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2839">2</span></span>

<span data-ttu-id="88b6c-2840">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2840">3</span></span>

<span data-ttu-id="88b6c-2841">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2841">4</span></span>

<span data-ttu-id="88b6c-2842">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2842">5</span></span>

<span data-ttu-id="88b6c-2843">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2843">6</span></span>

<span data-ttu-id="88b6c-2844">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2844">7</span></span>

<span data-ttu-id="88b6c-2845">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2845">8</span></span>

<span data-ttu-id="88b6c-2846">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2846">9</span></span>

<span data-ttu-id="88b6c-2847">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2847">3</span></span><br/> <span data-ttu-id="88b6c-2848">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2848">0</span></span><br/>

<span data-ttu-id="88b6c-2849">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2849">1</span></span>

<span data-ttu-id="88b6c-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="88b6c-2850">\_partID</span></span>

<span data-ttu-id="88b6c-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="88b6c-2851">\_dwNewState</span></span>

<span data-ttu-id="88b6c-2852">\_CatName (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="88b6c-2853">**\_ partID**：必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="88b6c-2854">**\_ dwNewState**：必須設定為下列其中一個值，表示目錄的新狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="88b6c-2855">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2855">Value</span></span>                         | <span data-ttu-id="88b6c-2856">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-2857">CICAT \_ 停止的0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="88b6c-2858">目錄已停止。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2858">The catalog is stopped.</span></span> <span data-ttu-id="88b6c-2859">此狀態表示不會編制任何新檔案的索引，也不會處理任何搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="88b6c-2860">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="88b6c-2861">目錄是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2861">The catalog is read-only.</span></span> <span data-ttu-id="88b6c-2862">不會為任何新檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="88b6c-2863">CICAT \_ 可寫入的0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="88b6c-2864">目錄是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2864">The catalog is writable.</span></span> <span data-ttu-id="88b6c-2865">您可以建立新檔案的索引，並處理搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="88b6c-2866">CICAT \_ 沒有 \_ 查詢0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="88b6c-2867">目錄無法供查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="88b6c-2868">CICAT \_ 取得 \_ 狀態0x00000010</span><span class="sxs-lookup"><span data-stu-id="88b6c-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="88b6c-2869">目錄的狀態不會變更，只會進行取出。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="88b6c-2870">CICAT \_ 所有 \_ 開啟的0x00000020</span><span class="sxs-lookup"><span data-stu-id="88b6c-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="88b6c-2871">查看是否已啟動所有目錄的檢查。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="88b6c-2872">若是如此， \_ 在 CPMSetCatStateOut 回復中傳送給此訊息的 dwOldState 欄位將會報告為非零。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="88b6c-2873">**\_ CatName**：要修改其狀態的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="88b6c-2874">名稱必須是以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="88b6c-2875">如果 \_ dwNewState 設定為 CICAT 全部開啟，則必須省略此欄位 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="88b6c-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="88b6c-2877">CPMSetCatStateOut 訊息是具有類別目錄舊狀態的 CPMSetCatStateIn 訊息回復。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="88b6c-2878">標頭後面的 CPMSetCatStateOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-2879">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2879">0</span></span>

<span data-ttu-id="88b6c-2880">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2880">1</span></span>

<span data-ttu-id="88b6c-2881">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2881">2</span></span>

<span data-ttu-id="88b6c-2882">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2882">3</span></span>

<span data-ttu-id="88b6c-2883">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2883">4</span></span>

<span data-ttu-id="88b6c-2884">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2884">5</span></span>

<span data-ttu-id="88b6c-2885">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2885">6</span></span>

<span data-ttu-id="88b6c-2886">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2886">7</span></span>

<span data-ttu-id="88b6c-2887">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2887">8</span></span>

<span data-ttu-id="88b6c-2888">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2888">9</span></span>

<span data-ttu-id="88b6c-2889">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2889">1</span></span><br/> <span data-ttu-id="88b6c-2890">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2890">0</span></span><br/>

<span data-ttu-id="88b6c-2891">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2891">1</span></span>

<span data-ttu-id="88b6c-2892">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2892">2</span></span>

<span data-ttu-id="88b6c-2893">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2893">3</span></span>

<span data-ttu-id="88b6c-2894">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2894">4</span></span>

<span data-ttu-id="88b6c-2895">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2895">5</span></span>

<span data-ttu-id="88b6c-2896">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2896">6</span></span>

<span data-ttu-id="88b6c-2897">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2897">7</span></span>

<span data-ttu-id="88b6c-2898">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2898">8</span></span>

<span data-ttu-id="88b6c-2899">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2899">9</span></span>

<span data-ttu-id="88b6c-2900">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2900">2</span></span><br/> <span data-ttu-id="88b6c-2901">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2901">0</span></span><br/>

<span data-ttu-id="88b6c-2902">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2902">1</span></span>

<span data-ttu-id="88b6c-2903">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2903">2</span></span>

<span data-ttu-id="88b6c-2904">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2904">3</span></span>

<span data-ttu-id="88b6c-2905">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2905">4</span></span>

<span data-ttu-id="88b6c-2906">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2906">5</span></span>

<span data-ttu-id="88b6c-2907">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2907">6</span></span>

<span data-ttu-id="88b6c-2908">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2908">7</span></span>

<span data-ttu-id="88b6c-2909">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2909">8</span></span>

<span data-ttu-id="88b6c-2910">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2910">9</span></span>

<span data-ttu-id="88b6c-2911">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2911">3</span></span><br/> <span data-ttu-id="88b6c-2912">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2912">0</span></span><br/>

<span data-ttu-id="88b6c-2913">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2913">1</span></span>

<span data-ttu-id="88b6c-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="88b6c-2914">\_dwOldState</span></span>



 

<span data-ttu-id="88b6c-2915">**\_ dwOldState**：下列其中一個值，表示目錄的舊狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="88b6c-2916">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2916">Value</span></span>                       | <span data-ttu-id="88b6c-2917">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="88b6c-2918">CICAT \_ 停止的0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="88b6c-2919">目錄已停止。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="88b6c-2920">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="88b6c-2921">目錄是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="88b6c-2922">CICAT \_ 可寫入的0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="88b6c-2923">目錄是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="88b6c-2924">CICAT \_ 沒有 \_ 查詢0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="88b6c-2925">目錄無法供查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="88b6c-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="88b6c-2927">CPMUpdateDocumentsIn 訊息會指示伺服器為指定的路徑編制索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="88b6c-2928">伺服器將會使用 CPMUpdateDocumentsOut 訊息的訊息標頭來回複，並將要求的結果包含在 \_ 訊息標頭的 [狀態] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="88b6c-2929">標頭後面的 CPMUpdateDocumentsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-2930">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2930">0</span></span>

<span data-ttu-id="88b6c-2931">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2931">1</span></span>

<span data-ttu-id="88b6c-2932">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2932">2</span></span>

<span data-ttu-id="88b6c-2933">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2933">3</span></span>

<span data-ttu-id="88b6c-2934">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2934">4</span></span>

<span data-ttu-id="88b6c-2935">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2935">5</span></span>

<span data-ttu-id="88b6c-2936">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2936">6</span></span>

<span data-ttu-id="88b6c-2937">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2937">7</span></span>

<span data-ttu-id="88b6c-2938">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2938">8</span></span>

<span data-ttu-id="88b6c-2939">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2939">9</span></span>

<span data-ttu-id="88b6c-2940">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2940">1</span></span><br/> <span data-ttu-id="88b6c-2941">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2941">0</span></span><br/>

<span data-ttu-id="88b6c-2942">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2942">1</span></span>

<span data-ttu-id="88b6c-2943">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2943">2</span></span>

<span data-ttu-id="88b6c-2944">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2944">3</span></span>

<span data-ttu-id="88b6c-2945">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2945">4</span></span>

<span data-ttu-id="88b6c-2946">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2946">5</span></span>

<span data-ttu-id="88b6c-2947">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2947">6</span></span>

<span data-ttu-id="88b6c-2948">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2948">7</span></span>

<span data-ttu-id="88b6c-2949">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2949">8</span></span>

<span data-ttu-id="88b6c-2950">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2950">9</span></span>

<span data-ttu-id="88b6c-2951">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2951">2</span></span><br/> <span data-ttu-id="88b6c-2952">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2952">0</span></span><br/>

<span data-ttu-id="88b6c-2953">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2953">1</span></span>

<span data-ttu-id="88b6c-2954">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2954">2</span></span>

<span data-ttu-id="88b6c-2955">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2955">3</span></span>

<span data-ttu-id="88b6c-2956">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2956">4</span></span>

<span data-ttu-id="88b6c-2957">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2957">5</span></span>

<span data-ttu-id="88b6c-2958">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2958">6</span></span>

<span data-ttu-id="88b6c-2959">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2959">7</span></span>

<span data-ttu-id="88b6c-2960">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-2960">8</span></span>

<span data-ttu-id="88b6c-2961">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-2961">9</span></span>

<span data-ttu-id="88b6c-2962">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2962">3</span></span><br/> <span data-ttu-id="88b6c-2963">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2963">0</span></span><br/>

<span data-ttu-id="88b6c-2964">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2964">1</span></span>

<span data-ttu-id="88b6c-2965">\_ (選擇性的旗標) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2965">\_flag (optional)</span></span>

<span data-ttu-id="88b6c-2966">\_fRootPath (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="88b6c-2967">RootPath (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="88b6c-2968">**\_ 旗** 標：要執行的更新類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="88b6c-2969">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="88b6c-2970">此欄位必須設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="88b6c-2971">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-2971">Value</span></span>                  | <span data-ttu-id="88b6c-2972">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="88b6c-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="88b6c-2974">要執行累加式更新。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="88b6c-2975">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="88b6c-2976">要執行完整更新。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="88b6c-2977">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="88b6c-2978">要執行新的初始化。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="88b6c-2979">**\_ fRootPath**：布林值，指出 RootPath 欄位是否指定要執行更新的路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="88b6c-2980">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="88b6c-2981">此欄位必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="88b6c-2982">如果設定為0x00000001，則 RootPath 中會包含要執行更新的路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="88b6c-2983">如果設定為0x00000000，則會在所有已編制索引的路徑上執行更新。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="88b6c-2984">**RootPath**：要更新的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="88b6c-2985">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="88b6c-2986">名稱必須是以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="88b6c-2987">如果 fRootPath 設定為0x00000000，則必須省略此欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="88b6c-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="88b6c-2989">CPMForceMergeIn 訊息要求伺服器執行任何必要的維護，以改善查詢效能。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="88b6c-2990">伺服器將會使用 CPMForceMergeIn 訊息的訊息標頭來回複，並在 [狀態] 欄位中包含要求的結果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="88b6c-2991">標頭後面的 CPMForceMergeIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-2992">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-2992">0</span></span>

<span data-ttu-id="88b6c-2993">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-2993">1</span></span>

<span data-ttu-id="88b6c-2994">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-2994">2</span></span>

<span data-ttu-id="88b6c-2995">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-2995">3</span></span>

<span data-ttu-id="88b6c-2996">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-2996">4</span></span>

<span data-ttu-id="88b6c-2997">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-2997">5</span></span>

<span data-ttu-id="88b6c-2998">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-2998">6</span></span>

<span data-ttu-id="88b6c-2999">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-2999">7</span></span>

<span data-ttu-id="88b6c-3000">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3000">8</span></span>

<span data-ttu-id="88b6c-3001">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3001">9</span></span>

<span data-ttu-id="88b6c-3002">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3002">1</span></span><br/> <span data-ttu-id="88b6c-3003">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3003">0</span></span><br/>

<span data-ttu-id="88b6c-3004">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3004">1</span></span>

<span data-ttu-id="88b6c-3005">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3005">2</span></span>

<span data-ttu-id="88b6c-3006">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3006">3</span></span>

<span data-ttu-id="88b6c-3007">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3007">4</span></span>

<span data-ttu-id="88b6c-3008">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3008">5</span></span>

<span data-ttu-id="88b6c-3009">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3009">6</span></span>

<span data-ttu-id="88b6c-3010">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3010">7</span></span>

<span data-ttu-id="88b6c-3011">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3011">8</span></span>

<span data-ttu-id="88b6c-3012">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3012">9</span></span>

<span data-ttu-id="88b6c-3013">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3013">2</span></span><br/> <span data-ttu-id="88b6c-3014">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3014">0</span></span><br/>

<span data-ttu-id="88b6c-3015">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3015">1</span></span>

<span data-ttu-id="88b6c-3016">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3016">2</span></span>

<span data-ttu-id="88b6c-3017">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3017">3</span></span>

<span data-ttu-id="88b6c-3018">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3018">4</span></span>

<span data-ttu-id="88b6c-3019">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3019">5</span></span>

<span data-ttu-id="88b6c-3020">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3020">6</span></span>

<span data-ttu-id="88b6c-3021">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3021">7</span></span>

<span data-ttu-id="88b6c-3022">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3022">8</span></span>

<span data-ttu-id="88b6c-3023">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3023">9</span></span>

<span data-ttu-id="88b6c-3024">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3024">3</span></span><br/> <span data-ttu-id="88b6c-3025">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3025">0</span></span><br/>

<span data-ttu-id="88b6c-3026">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3026">1</span></span>

<span data-ttu-id="88b6c-3027">\_partID (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="88b6c-3028">**\_ partID**：當用戶端傳送訊息時，此欄位必須存在，而且當伺服器傳送訊息時必須不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="88b6c-3029">當這個欄位存在時，必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="88b6c-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="88b6c-3031">CPMConnectIn 訊息會開始用戶端與伺服器之間的會話。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="88b6c-3032">標頭後面的 CPMConnectIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3033">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3033">0</span></span>

<span data-ttu-id="88b6c-3034">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3034">1</span></span>

<span data-ttu-id="88b6c-3035">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3035">2</span></span>

<span data-ttu-id="88b6c-3036">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3036">3</span></span>

<span data-ttu-id="88b6c-3037">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3037">4</span></span>

<span data-ttu-id="88b6c-3038">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3038">5</span></span>

<span data-ttu-id="88b6c-3039">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3039">6</span></span>

<span data-ttu-id="88b6c-3040">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3040">7</span></span>

<span data-ttu-id="88b6c-3041">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3041">8</span></span>

<span data-ttu-id="88b6c-3042">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3042">9</span></span>

<span data-ttu-id="88b6c-3043">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3043">1</span></span><br/> <span data-ttu-id="88b6c-3044">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3044">0</span></span><br/>

<span data-ttu-id="88b6c-3045">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3045">1</span></span>

<span data-ttu-id="88b6c-3046">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3046">2</span></span>

<span data-ttu-id="88b6c-3047">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3047">3</span></span>

<span data-ttu-id="88b6c-3048">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3048">4</span></span>

<span data-ttu-id="88b6c-3049">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3049">5</span></span>

<span data-ttu-id="88b6c-3050">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3050">6</span></span>

<span data-ttu-id="88b6c-3051">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3051">7</span></span>

<span data-ttu-id="88b6c-3052">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3052">8</span></span>

<span data-ttu-id="88b6c-3053">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3053">9</span></span>

<span data-ttu-id="88b6c-3054">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3054">2</span></span><br/> <span data-ttu-id="88b6c-3055">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3055">0</span></span><br/>

<span data-ttu-id="88b6c-3056">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3056">1</span></span>

<span data-ttu-id="88b6c-3057">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3057">2</span></span>

<span data-ttu-id="88b6c-3058">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3058">3</span></span>

<span data-ttu-id="88b6c-3059">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3059">4</span></span>

<span data-ttu-id="88b6c-3060">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3060">5</span></span>

<span data-ttu-id="88b6c-3061">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3061">6</span></span>

<span data-ttu-id="88b6c-3062">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3062">7</span></span>

<span data-ttu-id="88b6c-3063">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3063">8</span></span>

<span data-ttu-id="88b6c-3064">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3064">9</span></span>

<span data-ttu-id="88b6c-3065">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3065">3</span></span><br/> <span data-ttu-id="88b6c-3066">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3066">0</span></span><br/>

<span data-ttu-id="88b6c-3067">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3067">1</span></span>

<span data-ttu-id="88b6c-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="88b6c-3068">\_iClientVersion</span></span>

<span data-ttu-id="88b6c-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="88b6c-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="88b6c-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3070">\_cbBlob1</span></span>

<span data-ttu-id="88b6c-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3071">\_cbBlob2</span></span>

<span data-ttu-id="88b6c-3072">\_填充</span><span class="sxs-lookup"><span data-stu-id="88b6c-3072">\_padding</span></span>

<span data-ttu-id="88b6c-3073">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3073">...</span></span>

<span data-ttu-id="88b6c-3074">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3074">...</span></span>

<span data-ttu-id="88b6c-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="88b6c-3075">MachineName</span></span>

<span data-ttu-id="88b6c-3076">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3076">... (variable)</span></span>

<span data-ttu-id="88b6c-3077">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="88b6c-3077">UserName</span></span>

<span data-ttu-id="88b6c-3078">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3078">... (variable)</span></span>

<span data-ttu-id="88b6c-3079">\_paddingcPropSets (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="88b6c-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="88b6c-3080">cPropSets</span></span>

<span data-ttu-id="88b6c-3081">PropertySet1 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="88b6c-3082">PropertySet2 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="88b6c-3083">\_paddingExtPropset (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="88b6c-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="88b6c-3084">cExtPropSet</span></span>

<span data-ttu-id="88b6c-3085">aPropertySets (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="88b6c-3086">**\_ iClientVersion**：32位整數，指出伺服器是否要驗證訊息標頭的 ulChecksum 欄位中所指定的總和檢查碼值是否 \_ 為用戶端所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="88b6c-3087">如果 \_ iClientVersion 欄位設定為0x00000008 或更高，則伺服器必須驗證 \_ 下列訊息的 ulChecksum 域值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="88b6c-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="88b6c-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="88b6c-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="88b6c-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="88b6c-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="88b6c-3093">如需有關伺服器如何針對上方所列訊息的 ulChecksum 欄位驗證用戶端所指定值的詳細資訊，請參閱3.2.5 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="88b6c-3094">如果值大於0x00000008，則會假設用戶端能夠處理 CPMGetRowsOut 訊息中的64位位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="88b6c-3095">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="88b6c-3096">*Windows 行為：在 windows 用戶端上，iClientVersion 的設定* 如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="88b6c-3097">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-3097">Value</span></span>      | <span data-ttu-id="88b6c-3098">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="88b6c-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="88b6c-3099">0x00000005</span></span> | <span data-ttu-id="88b6c-3100">用戶端作業系統是 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="88b6c-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="88b6c-3101">0x00000008</span></span> | <span data-ttu-id="88b6c-3102">用戶端作業系統可能是32位的 Windows XP 或32位 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="88b6c-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="88b6c-3103">0x00010008</span></span> | <span data-ttu-id="88b6c-3104">用戶端作業系統可能是64位的 Windows XP 或64位 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="88b6c-3105">\_**fClientIsRemote**：布林值，指出用戶端是否正在與伺服器不同的電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="88b6c-3106">必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="88b6c-3107">\_**cbBlob1**：32位不帶正負號的整數，表示 CPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="88b6c-3108">\_**cbBlob2**：32位不帶正負號的整數，表示 CExPropSet 和 aPropertySet 欄位的大小（以位元組為單位），結合起來。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="88b6c-3109">\_**填補**：可以包含任意值的12個位元組填補，而且必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="88b6c-3110">**MachineName**：用戶端的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="88b6c-3111">名稱字串必須是小於512個 Unicode 字元的 null 終止陣列，包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="88b6c-3112">**UserName**：代表正在執行叫用此通訊協定之應用程式之人員的使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="88b6c-3113">當與 MachineName 串連時，名稱字串必須是小於512的 Unicode 字元之以 null 結束的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="88b6c-3114">**\_ paddingcPropSets**：此欄位的長度必須介於0到7個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="88b6c-3115">位元組數必須是將 cPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="88b6c-3116">位元組的值可以是任意值，而且接收者必須忽略此值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-3117">**cPropSets**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="88b6c-3118">此值必須設為0x0000002。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="88b6c-3119">**PropertySet1**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ FSCIFRMWRK \_ EXT (請參閱 2.2.1.22) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="88b6c-3120">**PropertySet2**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ CIFRMWRKCORE \_ EXT (請參閱 2.2.1.22) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="88b6c-3121">\_**PaddingExtPropset**：此欄位的長度必須介於0到7個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="88b6c-3122">位元組數必須是將 cExtPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="88b6c-3123">位元組的值可以是任意值，而且接收者必須忽略此值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-3124">**cExtPropSet**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="88b6c-3125">**aPropertySets**：指定其他屬性之 CDbPropSet 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="88b6c-3126">此陣列中的元素數目必須等於 cExtPropSet。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="88b6c-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="88b6c-3128">CPMConnectOut 訊息包含 CPMConnectIn 訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="88b6c-3129">標頭後面的 CPMConnectOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3130">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3130">0</span></span>

<span data-ttu-id="88b6c-3131">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3131">1</span></span>

<span data-ttu-id="88b6c-3132">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3132">2</span></span>

<span data-ttu-id="88b6c-3133">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3133">3</span></span>

<span data-ttu-id="88b6c-3134">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3134">4</span></span>

<span data-ttu-id="88b6c-3135">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3135">5</span></span>

<span data-ttu-id="88b6c-3136">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3136">6</span></span>

<span data-ttu-id="88b6c-3137">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3137">7</span></span>

<span data-ttu-id="88b6c-3138">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3138">8</span></span>

<span data-ttu-id="88b6c-3139">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3139">9</span></span>

<span data-ttu-id="88b6c-3140">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3140">1</span></span><br/> <span data-ttu-id="88b6c-3141">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3141">0</span></span><br/>

<span data-ttu-id="88b6c-3142">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3142">1</span></span>

<span data-ttu-id="88b6c-3143">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3143">2</span></span>

<span data-ttu-id="88b6c-3144">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3144">3</span></span>

<span data-ttu-id="88b6c-3145">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3145">4</span></span>

<span data-ttu-id="88b6c-3146">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3146">5</span></span>

<span data-ttu-id="88b6c-3147">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3147">6</span></span>

<span data-ttu-id="88b6c-3148">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3148">7</span></span>

<span data-ttu-id="88b6c-3149">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3149">8</span></span>

<span data-ttu-id="88b6c-3150">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3150">9</span></span>

<span data-ttu-id="88b6c-3151">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3151">2</span></span><br/> <span data-ttu-id="88b6c-3152">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3152">0</span></span><br/>

<span data-ttu-id="88b6c-3153">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3153">1</span></span>

<span data-ttu-id="88b6c-3154">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3154">2</span></span>

<span data-ttu-id="88b6c-3155">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3155">3</span></span>

<span data-ttu-id="88b6c-3156">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3156">4</span></span>

<span data-ttu-id="88b6c-3157">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3157">5</span></span>

<span data-ttu-id="88b6c-3158">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3158">6</span></span>

<span data-ttu-id="88b6c-3159">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3159">7</span></span>

<span data-ttu-id="88b6c-3160">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3160">8</span></span>

<span data-ttu-id="88b6c-3161">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3161">9</span></span>

<span data-ttu-id="88b6c-3162">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3162">3</span></span><br/> <span data-ttu-id="88b6c-3163">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3163">0</span></span><br/>

<span data-ttu-id="88b6c-3164">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3164">1</span></span>

<span data-ttu-id="88b6c-3165">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="88b6c-3165">\_serverVersion</span></span>

<span data-ttu-id="88b6c-3166">\_保留的 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="88b6c-3167">**\_ serverVersion**：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="88b6c-3168">32位整數，表示伺服器是否可支援64位位移 *。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="88b6c-3169">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="88b6c-3170">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-3170">Value</span></span>      | <span data-ttu-id="88b6c-3171">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="88b6c-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="88b6c-3172">0x00000007</span></span> | <span data-ttu-id="88b6c-3173">伺服器只能傳送32位的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="88b6c-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="88b6c-3174">0x00010007</span></span> | <span data-ttu-id="88b6c-3175">伺服器可以傳送32或64位位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="88b6c-3176">**\_ reserved**： reserved。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="88b6c-3177">伺服器可能會傳送任意數目的任意值，而且用戶端必須忽略這些值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="88b6c-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="88b6c-3179">CPMCreateQueryIn 訊息會建立新的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="88b6c-3180">標頭後面的 CPMCreateQueryIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3181">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3181">0</span></span>

<span data-ttu-id="88b6c-3182">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3182">1</span></span>

<span data-ttu-id="88b6c-3183">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3183">2</span></span>

<span data-ttu-id="88b6c-3184">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3184">3</span></span>

<span data-ttu-id="88b6c-3185">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3185">4</span></span>

<span data-ttu-id="88b6c-3186">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3186">5</span></span>

<span data-ttu-id="88b6c-3187">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3187">6</span></span>

<span data-ttu-id="88b6c-3188">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3188">7</span></span>

<span data-ttu-id="88b6c-3189">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3189">8</span></span>

<span data-ttu-id="88b6c-3190">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3190">9</span></span>

<span data-ttu-id="88b6c-3191">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3191">1</span></span><br/> <span data-ttu-id="88b6c-3192">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3192">0</span></span><br/>

<span data-ttu-id="88b6c-3193">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3193">1</span></span>

<span data-ttu-id="88b6c-3194">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3194">2</span></span>

<span data-ttu-id="88b6c-3195">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3195">3</span></span>

<span data-ttu-id="88b6c-3196">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3196">4</span></span>

<span data-ttu-id="88b6c-3197">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3197">5</span></span>

<span data-ttu-id="88b6c-3198">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3198">6</span></span>

<span data-ttu-id="88b6c-3199">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3199">7</span></span>

<span data-ttu-id="88b6c-3200">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3200">8</span></span>

<span data-ttu-id="88b6c-3201">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3201">9</span></span>

<span data-ttu-id="88b6c-3202">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3202">2</span></span><br/> <span data-ttu-id="88b6c-3203">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3203">0</span></span><br/>

<span data-ttu-id="88b6c-3204">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3204">1</span></span>

<span data-ttu-id="88b6c-3205">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3205">2</span></span>

<span data-ttu-id="88b6c-3206">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3206">3</span></span>

<span data-ttu-id="88b6c-3207">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3207">4</span></span>

<span data-ttu-id="88b6c-3208">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3208">5</span></span>

<span data-ttu-id="88b6c-3209">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3209">6</span></span>

<span data-ttu-id="88b6c-3210">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3210">7</span></span>

<span data-ttu-id="88b6c-3211">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3211">8</span></span>

<span data-ttu-id="88b6c-3212">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3212">9</span></span>

<span data-ttu-id="88b6c-3213">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3213">3</span></span><br/> <span data-ttu-id="88b6c-3214">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3214">0</span></span><br/>

<span data-ttu-id="88b6c-3215">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3215">1</span></span>

<span data-ttu-id="88b6c-3216">大小</span><span class="sxs-lookup"><span data-stu-id="88b6c-3216">Size</span></span>

<span data-ttu-id="88b6c-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="88b6c-3217">CColumnSetPresent</span></span>

<span data-ttu-id="88b6c-3218">ColumnSet (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="88b6c-3219">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3219">... (variable)</span></span>

<span data-ttu-id="88b6c-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="88b6c-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="88b6c-3221">限制 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3221">Restriction (optional)</span></span>

<span data-ttu-id="88b6c-3222">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3222">... (variable)</span></span>

<span data-ttu-id="88b6c-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="88b6c-3223">CSortSetPresent</span></span>

<span data-ttu-id="88b6c-3224">SortSet (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3224">SortSet (optional)</span></span>

<span data-ttu-id="88b6c-3225">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3225">... (variable)</span></span>

<span data-ttu-id="88b6c-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="88b6c-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="88b6c-3227">CategorizationSet (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="88b6c-3228">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3228">... (variable)</span></span>

<span data-ttu-id="88b6c-3229">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="88b6c-3229">RowSetProperties</span></span>

<span data-ttu-id="88b6c-3230">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3230">...</span></span>

<span data-ttu-id="88b6c-3231">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3231">...</span></span>

<span data-ttu-id="88b6c-3232">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3232">...</span></span>

<span data-ttu-id="88b6c-3233">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3233">...</span></span>

<span data-ttu-id="88b6c-3234">PidMapper (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="88b6c-3235">**大小**：32位不帶正負號的整數，表示從這個欄位開頭到訊息結尾的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="88b6c-3236">**CColumnSetPresent**：指出 ColumnSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="88b6c-3237">此欄位必須設定為0x01 或0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="88b6c-3238">如果設定為0x01，則必須有 CColumnSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="88b6c-3239">如果設定為0x00，則必須不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="88b6c-3240">**ColumnSet**： CColumnSet 結構，其中包含要傳回 CPidMapper 屬性的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="88b6c-3241">**CRestrictionPresent**：一個位元組欄位，指出限制欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="88b6c-3242">如果設定為任何非零值，則限制欄位必須存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="88b6c-3243">如果設定為0x00，則限制必須不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="88b6c-3244">**限制**： CRestriction 結構，其中包含查詢的命令樹。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="88b6c-3245">**CSortSetPresent**：指出 SortSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="88b6c-3246">如果設定為任何非零值，則必須有 SortSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="88b6c-3247">如果設定為0x00，則 SortSet 必須不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="88b6c-3248">**SortSet**： CSortSet 結構，指出查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="88b6c-3249">**CCategorizationSetPresent**：指出 CCategorizationSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="88b6c-3250">如果設定為任何非零值，則必須有 CCategorizationSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="88b6c-3251">如果設定為0x00，則 CCategorizationSet 必須不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="88b6c-3252">**CCategorizationSet**：包含查詢群組的 CCategorizationSet 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="88b6c-3253">**RowSetProperties**：提供查詢設定資訊的 CRowsetProperties 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="88b6c-3254">**PidMapper**： CPidMapper 結構，其中包含要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="88b6c-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="88b6c-3256">CPMCreateQueryOut 訊息包含 CPMCreateQueryIn 訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="88b6c-3257">標頭後面的 CPMCreateQueryOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3258">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3258">0</span></span>

<span data-ttu-id="88b6c-3259">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3259">1</span></span>

<span data-ttu-id="88b6c-3260">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3260">2</span></span>

<span data-ttu-id="88b6c-3261">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3261">3</span></span>

<span data-ttu-id="88b6c-3262">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3262">4</span></span>

<span data-ttu-id="88b6c-3263">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3263">5</span></span>

<span data-ttu-id="88b6c-3264">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3264">6</span></span>

<span data-ttu-id="88b6c-3265">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3265">7</span></span>

<span data-ttu-id="88b6c-3266">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3266">8</span></span>

<span data-ttu-id="88b6c-3267">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3267">9</span></span>

<span data-ttu-id="88b6c-3268">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3268">1</span></span><br/> <span data-ttu-id="88b6c-3269">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3269">0</span></span><br/>

<span data-ttu-id="88b6c-3270">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3270">1</span></span>

<span data-ttu-id="88b6c-3271">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3271">2</span></span>

<span data-ttu-id="88b6c-3272">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3272">3</span></span>

<span data-ttu-id="88b6c-3273">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3273">4</span></span>

<span data-ttu-id="88b6c-3274">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3274">5</span></span>

<span data-ttu-id="88b6c-3275">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3275">6</span></span>

<span data-ttu-id="88b6c-3276">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3276">7</span></span>

<span data-ttu-id="88b6c-3277">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3277">8</span></span>

<span data-ttu-id="88b6c-3278">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3278">9</span></span>

<span data-ttu-id="88b6c-3279">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3279">2</span></span><br/> <span data-ttu-id="88b6c-3280">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3280">0</span></span><br/>

<span data-ttu-id="88b6c-3281">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3281">1</span></span>

<span data-ttu-id="88b6c-3282">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3282">2</span></span>

<span data-ttu-id="88b6c-3283">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3283">3</span></span>

<span data-ttu-id="88b6c-3284">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3284">4</span></span>

<span data-ttu-id="88b6c-3285">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3285">5</span></span>

<span data-ttu-id="88b6c-3286">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3286">6</span></span>

<span data-ttu-id="88b6c-3287">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3287">7</span></span>

<span data-ttu-id="88b6c-3288">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3288">8</span></span>

<span data-ttu-id="88b6c-3289">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3289">9</span></span>

<span data-ttu-id="88b6c-3290">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3290">3</span></span><br/> <span data-ttu-id="88b6c-3291">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3291">0</span></span><br/>

<span data-ttu-id="88b6c-3292">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3292">1</span></span>

<span data-ttu-id="88b6c-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="88b6c-3293">\_fTrueSequential</span></span>

<span data-ttu-id="88b6c-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="88b6c-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="88b6c-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="88b6c-3295">aCursors</span></span>



 

<span data-ttu-id="88b6c-3296">**\_ fTrueSequential**：資訊性布林值，指出查詢是否可預期更快提供結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="88b6c-3297">當針對 CPMCreateQueryIn 中提供的查詢設定為0x00000001 時，伺服器可以使用索引，因為這樣可能會更快傳遞查詢結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="88b6c-3298">當設定為0x00000000 時，傳遞查詢結果會有較大的延遲。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="88b6c-3299">不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="88b6c-3300">**\_ fWorkIdUnique**：布林值，指出資料指標所指向的檔識別碼在查詢結果中是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="88b6c-3301">如果設定為0x00000001，則識別碼是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="88b6c-3302">如果設定為0x00000000，則只有在整個資料列集中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="88b6c-3303">**aCursors**：32位不帶正負號整數的陣列，代表資料指標的控制碼，其中專案數等於 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中的類別目錄數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="88b6c-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="88b6c-3305">CPMGetQueryStatusIn 訊息會要求查詢的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="88b6c-3306">標頭後面的 CPMGetQueryStatusIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3307">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3307">0</span></span>

<span data-ttu-id="88b6c-3308">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3308">1</span></span>

<span data-ttu-id="88b6c-3309">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3309">2</span></span>

<span data-ttu-id="88b6c-3310">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3310">3</span></span>

<span data-ttu-id="88b6c-3311">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3311">4</span></span>

<span data-ttu-id="88b6c-3312">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3312">5</span></span>

<span data-ttu-id="88b6c-3313">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3313">6</span></span>

<span data-ttu-id="88b6c-3314">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3314">7</span></span>

<span data-ttu-id="88b6c-3315">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3315">8</span></span>

<span data-ttu-id="88b6c-3316">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3316">9</span></span>

<span data-ttu-id="88b6c-3317">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3317">1</span></span><br/> <span data-ttu-id="88b6c-3318">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3318">0</span></span><br/>

<span data-ttu-id="88b6c-3319">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3319">1</span></span>

<span data-ttu-id="88b6c-3320">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3320">2</span></span>

<span data-ttu-id="88b6c-3321">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3321">3</span></span>

<span data-ttu-id="88b6c-3322">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3322">4</span></span>

<span data-ttu-id="88b6c-3323">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3323">5</span></span>

<span data-ttu-id="88b6c-3324">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3324">6</span></span>

<span data-ttu-id="88b6c-3325">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3325">7</span></span>

<span data-ttu-id="88b6c-3326">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3326">8</span></span>

<span data-ttu-id="88b6c-3327">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3327">9</span></span>

<span data-ttu-id="88b6c-3328">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3328">2</span></span><br/> <span data-ttu-id="88b6c-3329">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3329">0</span></span><br/>

<span data-ttu-id="88b6c-3330">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3330">1</span></span>

<span data-ttu-id="88b6c-3331">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3331">2</span></span>

<span data-ttu-id="88b6c-3332">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3332">3</span></span>

<span data-ttu-id="88b6c-3333">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3333">4</span></span>

<span data-ttu-id="88b6c-3334">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3334">5</span></span>

<span data-ttu-id="88b6c-3335">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3335">6</span></span>

<span data-ttu-id="88b6c-3336">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3336">7</span></span>

<span data-ttu-id="88b6c-3337">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3337">8</span></span>

<span data-ttu-id="88b6c-3338">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3338">9</span></span>

<span data-ttu-id="88b6c-3339">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3339">3</span></span><br/> <span data-ttu-id="88b6c-3340">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3340">0</span></span><br/>

<span data-ttu-id="88b6c-3341">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3341">1</span></span>

<span data-ttu-id="88b6c-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-3342">\_hCursor</span></span>



 

<span data-ttu-id="88b6c-3343">**\_ hCursor**：32位不帶正負號的整數，代表 CPMCreateQueryOut 訊息中的控制碼，該控制碼會識別要取得其狀態資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="88b6c-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="88b6c-3345">CPMGetQueryStatusOut 訊息會以查詢的狀態回復 CPMGetQueryStatusIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="88b6c-3346">標頭後面的 CPMGetQueryStatusOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3347">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3347">0</span></span>

<span data-ttu-id="88b6c-3348">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3348">1</span></span>

<span data-ttu-id="88b6c-3349">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3349">2</span></span>

<span data-ttu-id="88b6c-3350">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3350">3</span></span>

<span data-ttu-id="88b6c-3351">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3351">4</span></span>

<span data-ttu-id="88b6c-3352">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3352">5</span></span>

<span data-ttu-id="88b6c-3353">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3353">6</span></span>

<span data-ttu-id="88b6c-3354">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3354">7</span></span>

<span data-ttu-id="88b6c-3355">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3355">8</span></span>

<span data-ttu-id="88b6c-3356">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3356">9</span></span>

<span data-ttu-id="88b6c-3357">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3357">1</span></span><br/> <span data-ttu-id="88b6c-3358">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3358">0</span></span><br/>

<span data-ttu-id="88b6c-3359">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3359">1</span></span>

<span data-ttu-id="88b6c-3360">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3360">2</span></span>

<span data-ttu-id="88b6c-3361">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3361">3</span></span>

<span data-ttu-id="88b6c-3362">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3362">4</span></span>

<span data-ttu-id="88b6c-3363">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3363">5</span></span>

<span data-ttu-id="88b6c-3364">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3364">6</span></span>

<span data-ttu-id="88b6c-3365">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3365">7</span></span>

<span data-ttu-id="88b6c-3366">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3366">8</span></span>

<span data-ttu-id="88b6c-3367">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3367">9</span></span>

<span data-ttu-id="88b6c-3368">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3368">2</span></span><br/> <span data-ttu-id="88b6c-3369">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3369">0</span></span><br/>

<span data-ttu-id="88b6c-3370">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3370">1</span></span>

<span data-ttu-id="88b6c-3371">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3371">2</span></span>

<span data-ttu-id="88b6c-3372">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3372">3</span></span>

<span data-ttu-id="88b6c-3373">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3373">4</span></span>

<span data-ttu-id="88b6c-3374">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3374">5</span></span>

<span data-ttu-id="88b6c-3375">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3375">6</span></span>

<span data-ttu-id="88b6c-3376">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3376">7</span></span>

<span data-ttu-id="88b6c-3377">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3377">8</span></span>

<span data-ttu-id="88b6c-3378">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3378">9</span></span>

<span data-ttu-id="88b6c-3379">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3379">3</span></span><br/> <span data-ttu-id="88b6c-3380">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3380">0</span></span><br/>

<span data-ttu-id="88b6c-3381">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3381">1</span></span>

<span data-ttu-id="88b6c-3382">\_狀態</span><span class="sxs-lookup"><span data-stu-id="88b6c-3382">\_Status</span></span>



 

<span data-ttu-id="88b6c-3383">**\_ 狀態**：下表中定義的值位元遮罩，可描述查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="88b6c-3384">下表列出透過 \_ \* 0x00000007 對狀態執行位 and 運算所取得的 STAT 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="88b6c-3385">結果必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="88b6c-3386">常數</span><span class="sxs-lookup"><span data-stu-id="88b6c-3386">Constant</span></span>                 | <span data-ttu-id="88b6c-3387">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-3388">STAT \_ 忙碌0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="88b6c-3389">非同步查詢仍在執行中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="88b6c-3390">STAT \_ 錯誤0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="88b6c-3391">查詢處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="88b6c-3392">STAT \_ 完成0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="88b6c-3393">查詢已完成。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="88b6c-3394">STAT \_ REFRESH 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="88b6c-3395">查詢已完成，但更新會導致額外的查詢計算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="88b6c-3396">下表列出 \_ \* 可以獨立設定的其他 STAT 位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="88b6c-3397">常數</span><span class="sxs-lookup"><span data-stu-id="88b6c-3397">Constant</span></span>                                    | <span data-ttu-id="88b6c-3398">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6c-3399">STAT 非搜尋 \_ \_ 字0x00000010</span><span class="sxs-lookup"><span data-stu-id="88b6c-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="88b6c-3400">在內容查詢中，以萬用字元取代非搜尋字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="88b6c-3401">\_新的 STAT 內容已 \_ 過期 \_ \_</span><span class="sxs-lookup"><span data-stu-id="88b6c-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="88b6c-3402">查詢的結果可能不正確，因為涉及修改但未建立索引的檔案。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="88b6c-3403">STAT 重新整理 \_ \_ 未完成0x00000040</span><span class="sxs-lookup"><span data-stu-id="88b6c-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="88b6c-3404">查詢的結果可能不正確，因為涉及修改的查詢和重新編制索引的檔案不包含內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="88b6c-3405">STAT \_ 內容 \_ 查詢 \_ 未完成0x00000080</span><span class="sxs-lookup"><span data-stu-id="88b6c-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="88b6c-3406">內容查詢太複雜而無法完成或需要列舉，而不是使用內容索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="88b6c-3407">已 \_ 超過 STAT 時間 \_ 限制 \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="88b6c-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="88b6c-3408">查詢的結果可能不正確，因為查詢執行時間達到允許的時間上限。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="88b6c-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="88b6c-3410">CPMGetQueryStatusExIn 訊息會要求查詢的狀態和其他資訊，例如已編制索引的檔數目、剩下要編制索引的檔數目等等。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="88b6c-3411">標頭後面的 CPMGetQueryStatusExIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3412">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3412">0</span></span>

<span data-ttu-id="88b6c-3413">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3413">1</span></span>

<span data-ttu-id="88b6c-3414">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3414">2</span></span>

<span data-ttu-id="88b6c-3415">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3415">3</span></span>

<span data-ttu-id="88b6c-3416">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3416">4</span></span>

<span data-ttu-id="88b6c-3417">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3417">5</span></span>

<span data-ttu-id="88b6c-3418">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3418">6</span></span>

<span data-ttu-id="88b6c-3419">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3419">7</span></span>

<span data-ttu-id="88b6c-3420">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3420">8</span></span>

<span data-ttu-id="88b6c-3421">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3421">9</span></span>

<span data-ttu-id="88b6c-3422">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3422">1</span></span><br/> <span data-ttu-id="88b6c-3423">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3423">0</span></span><br/>

<span data-ttu-id="88b6c-3424">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3424">1</span></span>

<span data-ttu-id="88b6c-3425">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3425">2</span></span>

<span data-ttu-id="88b6c-3426">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3426">3</span></span>

<span data-ttu-id="88b6c-3427">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3427">4</span></span>

<span data-ttu-id="88b6c-3428">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3428">5</span></span>

<span data-ttu-id="88b6c-3429">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3429">6</span></span>

<span data-ttu-id="88b6c-3430">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3430">7</span></span>

<span data-ttu-id="88b6c-3431">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3431">8</span></span>

<span data-ttu-id="88b6c-3432">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3432">9</span></span>

<span data-ttu-id="88b6c-3433">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3433">2</span></span><br/> <span data-ttu-id="88b6c-3434">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3434">0</span></span><br/>

<span data-ttu-id="88b6c-3435">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3435">1</span></span>

<span data-ttu-id="88b6c-3436">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3436">2</span></span>

<span data-ttu-id="88b6c-3437">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3437">3</span></span>

<span data-ttu-id="88b6c-3438">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3438">4</span></span>

<span data-ttu-id="88b6c-3439">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3439">5</span></span>

<span data-ttu-id="88b6c-3440">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3440">6</span></span>

<span data-ttu-id="88b6c-3441">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3441">7</span></span>

<span data-ttu-id="88b6c-3442">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3442">8</span></span>

<span data-ttu-id="88b6c-3443">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3443">9</span></span>

<span data-ttu-id="88b6c-3444">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3444">3</span></span><br/> <span data-ttu-id="88b6c-3445">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3445">0</span></span><br/>

<span data-ttu-id="88b6c-3446">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3446">1</span></span>

<span data-ttu-id="88b6c-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-3447">\_hCursor</span></span>

<span data-ttu-id="88b6c-3448">\_bmk</span><span class="sxs-lookup"><span data-stu-id="88b6c-3448">\_bmk</span></span>



 

<span data-ttu-id="88b6c-3449">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得狀態資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="88b6c-3450">**\_ bmk**：代表應抓取其位置之書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="88b6c-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="88b6c-3452">CPMGetQueryStatusExOut 訊息會以查詢的狀態和其他狀態資訊回復 CPMGetQueryStatusExIn 訊息，如下圖所述。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="88b6c-3453">標頭後面的 CPMGetQueryStatusExOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3454">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3454">0</span></span>

<span data-ttu-id="88b6c-3455">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3455">1</span></span>

<span data-ttu-id="88b6c-3456">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3456">2</span></span>

<span data-ttu-id="88b6c-3457">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3457">3</span></span>

<span data-ttu-id="88b6c-3458">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3458">4</span></span>

<span data-ttu-id="88b6c-3459">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3459">5</span></span>

<span data-ttu-id="88b6c-3460">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3460">6</span></span>

<span data-ttu-id="88b6c-3461">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3461">7</span></span>

<span data-ttu-id="88b6c-3462">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3462">8</span></span>

<span data-ttu-id="88b6c-3463">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3463">9</span></span>

<span data-ttu-id="88b6c-3464">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3464">1</span></span><br/> <span data-ttu-id="88b6c-3465">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3465">0</span></span><br/>

<span data-ttu-id="88b6c-3466">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3466">1</span></span>

<span data-ttu-id="88b6c-3467">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3467">2</span></span>

<span data-ttu-id="88b6c-3468">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3468">3</span></span>

<span data-ttu-id="88b6c-3469">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3469">4</span></span>

<span data-ttu-id="88b6c-3470">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3470">5</span></span>

<span data-ttu-id="88b6c-3471">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3471">6</span></span>

<span data-ttu-id="88b6c-3472">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3472">7</span></span>

<span data-ttu-id="88b6c-3473">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3473">8</span></span>

<span data-ttu-id="88b6c-3474">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3474">9</span></span>

<span data-ttu-id="88b6c-3475">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3475">2</span></span><br/> <span data-ttu-id="88b6c-3476">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3476">0</span></span><br/>

<span data-ttu-id="88b6c-3477">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3477">1</span></span>

<span data-ttu-id="88b6c-3478">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3478">2</span></span>

<span data-ttu-id="88b6c-3479">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3479">3</span></span>

<span data-ttu-id="88b6c-3480">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3480">4</span></span>

<span data-ttu-id="88b6c-3481">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3481">5</span></span>

<span data-ttu-id="88b6c-3482">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3482">6</span></span>

<span data-ttu-id="88b6c-3483">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3483">7</span></span>

<span data-ttu-id="88b6c-3484">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3484">8</span></span>

<span data-ttu-id="88b6c-3485">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3485">9</span></span>

<span data-ttu-id="88b6c-3486">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3486">3</span></span><br/> <span data-ttu-id="88b6c-3487">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3487">0</span></span><br/>

<span data-ttu-id="88b6c-3488">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3488">1</span></span>

<span data-ttu-id="88b6c-3489">\_狀態</span><span class="sxs-lookup"><span data-stu-id="88b6c-3489">\_Status</span></span>

<span data-ttu-id="88b6c-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="88b6c-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="88b6c-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="88b6c-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="88b6c-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="88b6c-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="88b6c-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="88b6c-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="88b6c-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="88b6c-3494">\_iRowBmk</span></span>

<span data-ttu-id="88b6c-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="88b6c-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="88b6c-3496">**\_ 狀態**：其中一個 STAT \_ \*在區段2.2.3.11 中指定的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="88b6c-3497">**\_ cFilteredDocuments**：32位不帶正負號的整數，表示已編制索引的檔數目</span><span class="sxs-lookup"><span data-stu-id="88b6c-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="88b6c-3498">**\_ cDocumentsToFilter**：32位不帶正負號的整數，表示仍維持編制索引的檔數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="88b6c-3499">**\_ dwRatioFinishedDenominator**：32位不帶正負號的整數，表示查詢已完成處理之檔比例的分母。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="88b6c-3500">**\_ dwRatioFinishedNumerator**：32位不帶正負號的整數，表示查詢完成處理之檔的比率分子。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="88b6c-3501">**\_ iRowBmk**：32位不帶正負號的整數，指出資料列集中書簽的大概位置（以資料列為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="88b6c-3502">**\_ cRowsTotal**：32位不帶正負號的整數，指定資料列集中的資料列總數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="88b6c-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="88b6c-3504">CPMSetBindingsIn 訊息會要求將資料行系結至資料列集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="88b6c-3505">伺服器將會使用 CPMBindingsIn 訊息的標頭區段，以及 [狀態] 欄位中包含的要求結果來回複 CPMSetBindingsIn 要求訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="88b6c-3506">標頭後面的 CPMSetBindingsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3507">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3507">0</span></span>

<span data-ttu-id="88b6c-3508">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3508">1</span></span>

<span data-ttu-id="88b6c-3509">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3509">2</span></span>

<span data-ttu-id="88b6c-3510">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3510">3</span></span>

<span data-ttu-id="88b6c-3511">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3511">4</span></span>

<span data-ttu-id="88b6c-3512">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3512">5</span></span>

<span data-ttu-id="88b6c-3513">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3513">6</span></span>

<span data-ttu-id="88b6c-3514">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3514">7</span></span>

<span data-ttu-id="88b6c-3515">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3515">8</span></span>

<span data-ttu-id="88b6c-3516">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3516">9</span></span>

<span data-ttu-id="88b6c-3517">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3517">1</span></span><br/> <span data-ttu-id="88b6c-3518">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3518">0</span></span><br/>

<span data-ttu-id="88b6c-3519">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3519">1</span></span>

<span data-ttu-id="88b6c-3520">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3520">2</span></span>

<span data-ttu-id="88b6c-3521">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3521">3</span></span>

<span data-ttu-id="88b6c-3522">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3522">4</span></span>

<span data-ttu-id="88b6c-3523">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3523">5</span></span>

<span data-ttu-id="88b6c-3524">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3524">6</span></span>

<span data-ttu-id="88b6c-3525">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3525">7</span></span>

<span data-ttu-id="88b6c-3526">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3526">8</span></span>

<span data-ttu-id="88b6c-3527">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3527">9</span></span>

<span data-ttu-id="88b6c-3528">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3528">2</span></span><br/> <span data-ttu-id="88b6c-3529">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3529">0</span></span><br/>

<span data-ttu-id="88b6c-3530">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3530">1</span></span>

<span data-ttu-id="88b6c-3531">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3531">2</span></span>

<span data-ttu-id="88b6c-3532">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3532">3</span></span>

<span data-ttu-id="88b6c-3533">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3533">4</span></span>

<span data-ttu-id="88b6c-3534">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3534">5</span></span>

<span data-ttu-id="88b6c-3535">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3535">6</span></span>

<span data-ttu-id="88b6c-3536">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3536">7</span></span>

<span data-ttu-id="88b6c-3537">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3537">8</span></span>

<span data-ttu-id="88b6c-3538">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3538">9</span></span>

<span data-ttu-id="88b6c-3539">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3539">3</span></span><br/> <span data-ttu-id="88b6c-3540">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3540">0</span></span><br/>

<span data-ttu-id="88b6c-3541">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3541">1</span></span>

<span data-ttu-id="88b6c-3542">\_hCursor (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="88b6c-3543">\_cbRow (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="88b6c-3544">\_cbBindingDesc (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="88b6c-3545">\_虛擬 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3545">\_dummy (optional)</span></span>

<span data-ttu-id="88b6c-3546">cColumns (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3546">cColumns (optional)</span></span>

<span data-ttu-id="88b6c-3547">aColumns (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="88b6c-3548">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，可識別要設定系結的資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="88b6c-3549">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-3550">**\_ cbRow**：32位不帶正負號的整數，表示資料列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="88b6c-3551">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-3552">**\_ cbBindingDesc**：32位不帶正負號的整數，表示在虛擬欄位之後的欄位長度（以位元組為單位） \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="88b6c-3553">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-3554">**\_ 虛擬**：此欄位未使用，必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="88b6c-3555">可以設定為任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="88b6c-3556">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-3557">**cColumns**：32位不帶正負號的整數，表示 aColumns 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="88b6c-3558">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-3559">**aColumns**： CTableColumn 結構的陣列，描述資料列集中資料列的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="88b6c-3560">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="88b6c-3561">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="88b6c-3562">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="88b6c-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="88b6c-3564">CPMGetRowsIn 訊息會要求查詢中的資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="88b6c-3565">標頭後面的 CPMGetRowsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3566">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3566">0</span></span>

<span data-ttu-id="88b6c-3567">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3567">1</span></span>

<span data-ttu-id="88b6c-3568">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3568">2</span></span>

<span data-ttu-id="88b6c-3569">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3569">3</span></span>

<span data-ttu-id="88b6c-3570">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3570">4</span></span>

<span data-ttu-id="88b6c-3571">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3571">5</span></span>

<span data-ttu-id="88b6c-3572">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3572">6</span></span>

<span data-ttu-id="88b6c-3573">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3573">7</span></span>

<span data-ttu-id="88b6c-3574">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3574">8</span></span>

<span data-ttu-id="88b6c-3575">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3575">9</span></span>

<span data-ttu-id="88b6c-3576">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3576">1</span></span><br/> <span data-ttu-id="88b6c-3577">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3577">0</span></span><br/>

<span data-ttu-id="88b6c-3578">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3578">1</span></span>

<span data-ttu-id="88b6c-3579">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3579">2</span></span>

<span data-ttu-id="88b6c-3580">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3580">3</span></span>

<span data-ttu-id="88b6c-3581">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3581">4</span></span>

<span data-ttu-id="88b6c-3582">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3582">5</span></span>

<span data-ttu-id="88b6c-3583">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3583">6</span></span>

<span data-ttu-id="88b6c-3584">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3584">7</span></span>

<span data-ttu-id="88b6c-3585">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3585">8</span></span>

<span data-ttu-id="88b6c-3586">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3586">9</span></span>

<span data-ttu-id="88b6c-3587">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3587">2</span></span><br/> <span data-ttu-id="88b6c-3588">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3588">0</span></span><br/>

<span data-ttu-id="88b6c-3589">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3589">1</span></span>

<span data-ttu-id="88b6c-3590">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3590">2</span></span>

<span data-ttu-id="88b6c-3591">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3591">3</span></span>

<span data-ttu-id="88b6c-3592">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3592">4</span></span>

<span data-ttu-id="88b6c-3593">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3593">5</span></span>

<span data-ttu-id="88b6c-3594">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3594">6</span></span>

<span data-ttu-id="88b6c-3595">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3595">7</span></span>

<span data-ttu-id="88b6c-3596">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3596">8</span></span>

<span data-ttu-id="88b6c-3597">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3597">9</span></span>

<span data-ttu-id="88b6c-3598">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3598">3</span></span><br/> <span data-ttu-id="88b6c-3599">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3599">0</span></span><br/>

<span data-ttu-id="88b6c-3600">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3600">1</span></span>

<span data-ttu-id="88b6c-3601">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-3601">\_hCursor</span></span>

<span data-ttu-id="88b6c-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="88b6c-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="88b6c-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="88b6c-3603">\_cbRowWidth</span></span>

<span data-ttu-id="88b6c-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="88b6c-3604">\_cbSeek</span></span>

<span data-ttu-id="88b6c-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="88b6c-3605">\_cbReserved</span></span>

<span data-ttu-id="88b6c-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="88b6c-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="88b6c-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="88b6c-3607">\_ulClientBase</span></span>

<span data-ttu-id="88b6c-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="88b6c-3608">\_fBwdFetch</span></span>

<span data-ttu-id="88b6c-3609">eType</span><span class="sxs-lookup"><span data-stu-id="88b6c-3609">eType</span></span>

<span data-ttu-id="88b6c-3610">\_chapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-3610">\_chapt</span></span>

<span data-ttu-id="88b6c-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="88b6c-3611">SeekDescription</span></span>

<span data-ttu-id="88b6c-3612">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3612">...</span></span>

<span data-ttu-id="88b6c-3613">... (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3613">... (variable)</span></span>



 

<span data-ttu-id="88b6c-3614">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得資料列的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="88b6c-3615">**\_ cRowsToTransfer**：32位不帶正負號的整數，指出用戶端想要接收以回應此訊息的最大資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="88b6c-3616">**\_ cbRowWidth**：32位不帶正負號的整數，表示資料列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="88b6c-3617">**\_ cbSeek**：32位不帶正負號的整數，表示以 eType 開頭的訊息大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="88b6c-3618">**\_ cbReserved**：32位不帶正負號的整數，指出 CPMGetRowsOut 訊息的大小（以位元組為單位）， (不含資料列和 SeekDescriptions 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="88b6c-3619">這個欄位中的這個值會加入至 \_ cbSeek 欄位的值，然後用來計算 CPMGetRowsOut 訊息中資料欄欄位的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="88b6c-3620">**\_ cbReadBuffer**：32位不帶正負號的整數，必須設定為 cRowsToTransfer 的值 \_ cbRowWidth 或1000倍的最大值 \_ ，舍入到最接近的512位元組倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="88b6c-3621">此值不得超過0x00004000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="88b6c-3622">**\_ ulClientBase**：32位不帶正負號的整數，表示要用於資料列緩衝區中指標計算的基底值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="88b6c-3623">如果使用的是64位位移，則會使用訊息標頭的 reserved2 欄位作為上層32位，並使用 \_ ulClientBase 作為64位值的低32位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="88b6c-3624">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="88b6c-3625">**\_ fBwdFetch**：32位不帶正負號的整數，表示提取資料列的順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="88b6c-3626">如果設定為0x00000001，則會以反向順序提取資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="88b6c-3627">如果設定為0x00000000，則會以正向順序提取資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="88b6c-3628">不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="88b6c-3629">**eType**：32位不帶正負號的整數，其中包含下列其中一個值，表示要執行的作業類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="88b6c-3630">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-3630">Value</span></span>                         | <span data-ttu-id="88b6c-3631">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="88b6c-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="88b6c-3633">SeekDescription 包含 CRowSeekNext 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="88b6c-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="88b6c-3635">SeekDescription 包含 CRowSeekAt 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="88b6c-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="88b6c-3637">SeekDescription 包含 CRowSeekAtRatio 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="88b6c-3638">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="88b6c-3639">SeekDescription 包含 CRowSeekByBookmark 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="88b6c-3640">**\_ chapt**：代表資料列集章節之控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="88b6c-3641">**SeekDescription**：這個欄位必須包含 eType 值所指定之類型的結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="88b6c-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="88b6c-3643">CPMGetRowsOut 訊息會以查詢的資料列回復 CPMGetRowsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="88b6c-3644">伺服器必須在 [資料列] 欄位中將位移格式化為可變長度資料類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="88b6c-3645">用戶端表示它是32位系統 (0x00000008 或更少在 CPMConnectIn) 的 iClientVersion 欄位中：位移是32位整數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="88b6c-3646">用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是32位系統 (\_ serverVersion 設定為0x00000007 中的 CPMConnectOut) ：位移是32位整數</span><span class="sxs-lookup"><span data-stu-id="88b6c-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="88b6c-3647">用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是64位系統 (\_ serverVersion 設定為0x00010007 中的 CPMConnectOut) ：位移是64位整數</span><span class="sxs-lookup"><span data-stu-id="88b6c-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="88b6c-3648">標頭後面的 CPMGetRowsOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3649">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3649">0</span></span>

<span data-ttu-id="88b6c-3650">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3650">1</span></span>

<span data-ttu-id="88b6c-3651">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3651">2</span></span>

<span data-ttu-id="88b6c-3652">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3652">3</span></span>

<span data-ttu-id="88b6c-3653">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3653">4</span></span>

<span data-ttu-id="88b6c-3654">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3654">5</span></span>

<span data-ttu-id="88b6c-3655">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3655">6</span></span>

<span data-ttu-id="88b6c-3656">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3656">7</span></span>

<span data-ttu-id="88b6c-3657">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3657">8</span></span>

<span data-ttu-id="88b6c-3658">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3658">9</span></span>

<span data-ttu-id="88b6c-3659">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3659">1</span></span><br/> <span data-ttu-id="88b6c-3660">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3660">0</span></span><br/>

<span data-ttu-id="88b6c-3661">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3661">1</span></span>

<span data-ttu-id="88b6c-3662">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3662">2</span></span>

<span data-ttu-id="88b6c-3663">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3663">3</span></span>

<span data-ttu-id="88b6c-3664">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3664">4</span></span>

<span data-ttu-id="88b6c-3665">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3665">5</span></span>

<span data-ttu-id="88b6c-3666">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3666">6</span></span>

<span data-ttu-id="88b6c-3667">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3667">7</span></span>

<span data-ttu-id="88b6c-3668">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3668">8</span></span>

<span data-ttu-id="88b6c-3669">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3669">9</span></span>

<span data-ttu-id="88b6c-3670">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3670">2</span></span><br/> <span data-ttu-id="88b6c-3671">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3671">0</span></span><br/>

<span data-ttu-id="88b6c-3672">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3672">1</span></span>

<span data-ttu-id="88b6c-3673">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3673">2</span></span>

<span data-ttu-id="88b6c-3674">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3674">3</span></span>

<span data-ttu-id="88b6c-3675">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3675">4</span></span>

<span data-ttu-id="88b6c-3676">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3676">5</span></span>

<span data-ttu-id="88b6c-3677">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3677">6</span></span>

<span data-ttu-id="88b6c-3678">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3678">7</span></span>

<span data-ttu-id="88b6c-3679">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3679">8</span></span>

<span data-ttu-id="88b6c-3680">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3680">9</span></span>

<span data-ttu-id="88b6c-3681">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3681">3</span></span><br/> <span data-ttu-id="88b6c-3682">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3682">0</span></span><br/>

<span data-ttu-id="88b6c-3683">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3683">1</span></span>

<span data-ttu-id="88b6c-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="88b6c-3684">\_cRowsReturned</span></span>

<span data-ttu-id="88b6c-3685">eType</span><span class="sxs-lookup"><span data-stu-id="88b6c-3685">eType</span></span>

<span data-ttu-id="88b6c-3686">\_chapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-3686">\_chapt</span></span>

<span data-ttu-id="88b6c-3687">SeekDescription (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="88b6c-3688">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3688">...</span></span>

<span data-ttu-id="88b6c-3689">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3689">...</span></span>

<span data-ttu-id="88b6c-3690">paddingRows (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="88b6c-3691">資料列</span><span class="sxs-lookup"><span data-stu-id="88b6c-3691">Rows</span></span>



 

<span data-ttu-id="88b6c-3692">**\_ cRowsReturned**：32位不帶正負號的整數，指出資料列中傳回的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="88b6c-3693">**eType**：32位不帶正負號的整數，其中包含下列其中一個值，以指出要執行的 rowseek 作業類型</span><span class="sxs-lookup"><span data-stu-id="88b6c-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="88b6c-3694">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-3694">Value</span></span>                         | <span data-ttu-id="88b6c-3695">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="88b6c-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="88b6c-3697">無 SeekDescription，忽略 SeekDescription 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="88b6c-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="88b6c-3699">SeekDescription 包含 CRowSeekNext 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="88b6c-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="88b6c-3701">SeekDescription 包含 CRowSeekAt 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="88b6c-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="88b6c-3703">SeekDescription 包含 CRowSeekAtRatio 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="88b6c-3704">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="88b6c-3705">SeekDescription 包含 CRowSeekByBookmark 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="88b6c-3706">**\_ chapt**：代表資料列集章節之控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="88b6c-3707">**SeekDescription**：此欄位必須包含 eType 欄位所表示之類型的結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="88b6c-3708">**paddingRows**：此欄位必須有足夠的長度 (0 到 \_ cbReserved-1 個位元組) 為了將資料欄欄位填補至 \_ 從訊息開頭 cbReserved 的位移，其中 \_ cbReserved 是 CPMGetRowsIn 訊息中的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="88b6c-3709">此欄位中使用的填補位元組可以是任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="88b6c-3710">接收者必須忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="88b6c-3711">資料列：資料列資料的格式設定為最近 CPMSetBindingsIn 訊息中的 **資料行資訊**。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="88b6c-3712">資料列必須以轉寄順序儲存 (例如，資料列2之前的資料列 1) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="88b6c-3713">固定大小的資料行必須儲存在最新 CPMSetBindingsIn 訊息所指定的位移上。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="88b6c-3714">可變大小的資料行 (例如，字串) 必須依照下列方式儲存：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="88b6c-3715">變數資料本身 (例如，字串) 會以遞減 (順序儲存在緩衝區結尾，例如，資料列1的所有變數資料的集合在結尾、第2列最接近的位置，) 依此類推。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="88b6c-3716">在資料列緩衝區開頭的固定大社區域 (，) 必須包含每個資料行的 CRowVariant，這些資料行會儲存在最新 CPMSetBindingsIn 訊息中指定的位移。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="88b6c-3717">vType 必須包含資料類型 (例如： VT \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="88b6c-3718">若為，則在使用32位位移時，CRowVariant 中的位移欄位必須包含32位值，這是從 CPMGetRowsOut 訊息的開頭算起的變數資料位移，加上 \_ 最新 CPMGetRowsIn 訊息中指定的 ulClientBase 的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="88b6c-3719">如果使用的是64位位移，則 CRowVariant 中的位移欄位必須包含64位值，該值是 CPMGetRowsOut 訊息開頭的位移，並新增至使用 \_ ulClientBase 做為低32位和 \_ ulReserved2 為高32位所組成的64位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="88b6c-3720">例如，如果 CPMSetBindingsIn 訊息指定了兩個數據行大小 (VT \_ I4) 和 Title (vt \_ LPWSTR) -and \_ ulClientBase from CPMGetRowsIn was 0x10000，則兩個數據列會如下所示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="88b6c-3721">以灰色標示的區段是緩衝區的固定長度部分。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![cpmsetbindingsin 訊息範例](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="88b6c-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="88b6c-3724">CPMRatioFinishedIn 訊息會要求查詢的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="88b6c-3725">標頭後面的 CPMRatioFinishedIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3726">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3726">0</span></span>

<span data-ttu-id="88b6c-3727">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3727">1</span></span>

<span data-ttu-id="88b6c-3728">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3728">2</span></span>

<span data-ttu-id="88b6c-3729">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3729">3</span></span>

<span data-ttu-id="88b6c-3730">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3730">4</span></span>

<span data-ttu-id="88b6c-3731">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3731">5</span></span>

<span data-ttu-id="88b6c-3732">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3732">6</span></span>

<span data-ttu-id="88b6c-3733">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3733">7</span></span>

<span data-ttu-id="88b6c-3734">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3734">8</span></span>

<span data-ttu-id="88b6c-3735">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3735">9</span></span>

<span data-ttu-id="88b6c-3736">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3736">1</span></span><br/> <span data-ttu-id="88b6c-3737">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3737">0</span></span><br/>

<span data-ttu-id="88b6c-3738">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3738">1</span></span>

<span data-ttu-id="88b6c-3739">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3739">2</span></span>

<span data-ttu-id="88b6c-3740">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3740">3</span></span>

<span data-ttu-id="88b6c-3741">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3741">4</span></span>

<span data-ttu-id="88b6c-3742">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3742">5</span></span>

<span data-ttu-id="88b6c-3743">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3743">6</span></span>

<span data-ttu-id="88b6c-3744">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3744">7</span></span>

<span data-ttu-id="88b6c-3745">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3745">8</span></span>

<span data-ttu-id="88b6c-3746">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3746">9</span></span>

<span data-ttu-id="88b6c-3747">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3747">2</span></span><br/> <span data-ttu-id="88b6c-3748">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3748">0</span></span><br/>

<span data-ttu-id="88b6c-3749">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3749">1</span></span>

<span data-ttu-id="88b6c-3750">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3750">2</span></span>

<span data-ttu-id="88b6c-3751">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3751">3</span></span>

<span data-ttu-id="88b6c-3752">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3752">4</span></span>

<span data-ttu-id="88b6c-3753">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3753">5</span></span>

<span data-ttu-id="88b6c-3754">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3754">6</span></span>

<span data-ttu-id="88b6c-3755">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3755">7</span></span>

<span data-ttu-id="88b6c-3756">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3756">8</span></span>

<span data-ttu-id="88b6c-3757">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3757">9</span></span>

<span data-ttu-id="88b6c-3758">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3758">3</span></span><br/> <span data-ttu-id="88b6c-3759">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3759">0</span></span><br/>

<span data-ttu-id="88b6c-3760">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3760">1</span></span>

<span data-ttu-id="88b6c-3761">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-3761">\_hCursor</span></span>

<span data-ttu-id="88b6c-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="88b6c-3762">\_fQuick</span></span>



 

<span data-ttu-id="88b6c-3763">**\_ HCursor**： CPMCreateQueryOut 訊息的控制碼，識別要要求完成資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="88b6c-3764">**\_ fQuick**：必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="88b6c-3765">如果未使用，則伺服器必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="88b6c-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="88b6c-3767">CPMRatioFinishedOut 訊息會以查詢的完成率回復 CPMRatioFinishedIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="88b6c-3768">標頭後面的 CPMRatioFinishedOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3769">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3769">0</span></span>

<span data-ttu-id="88b6c-3770">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3770">1</span></span>

<span data-ttu-id="88b6c-3771">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3771">2</span></span>

<span data-ttu-id="88b6c-3772">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3772">3</span></span>

<span data-ttu-id="88b6c-3773">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3773">4</span></span>

<span data-ttu-id="88b6c-3774">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3774">5</span></span>

<span data-ttu-id="88b6c-3775">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3775">6</span></span>

<span data-ttu-id="88b6c-3776">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3776">7</span></span>

<span data-ttu-id="88b6c-3777">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3777">8</span></span>

<span data-ttu-id="88b6c-3778">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3778">9</span></span>

<span data-ttu-id="88b6c-3779">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3779">1</span></span><br/> <span data-ttu-id="88b6c-3780">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3780">0</span></span><br/>

<span data-ttu-id="88b6c-3781">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3781">1</span></span>

<span data-ttu-id="88b6c-3782">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3782">2</span></span>

<span data-ttu-id="88b6c-3783">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3783">3</span></span>

<span data-ttu-id="88b6c-3784">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3784">4</span></span>

<span data-ttu-id="88b6c-3785">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3785">5</span></span>

<span data-ttu-id="88b6c-3786">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3786">6</span></span>

<span data-ttu-id="88b6c-3787">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3787">7</span></span>

<span data-ttu-id="88b6c-3788">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3788">8</span></span>

<span data-ttu-id="88b6c-3789">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3789">9</span></span>

<span data-ttu-id="88b6c-3790">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3790">2</span></span><br/> <span data-ttu-id="88b6c-3791">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3791">0</span></span><br/>

<span data-ttu-id="88b6c-3792">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3792">1</span></span>

<span data-ttu-id="88b6c-3793">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3793">2</span></span>

<span data-ttu-id="88b6c-3794">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3794">3</span></span>

<span data-ttu-id="88b6c-3795">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3795">4</span></span>

<span data-ttu-id="88b6c-3796">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3796">5</span></span>

<span data-ttu-id="88b6c-3797">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3797">6</span></span>

<span data-ttu-id="88b6c-3798">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3798">7</span></span>

<span data-ttu-id="88b6c-3799">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3799">8</span></span>

<span data-ttu-id="88b6c-3800">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3800">9</span></span>

<span data-ttu-id="88b6c-3801">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3801">3</span></span><br/> <span data-ttu-id="88b6c-3802">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3802">0</span></span><br/>

<span data-ttu-id="88b6c-3803">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3803">1</span></span>

<span data-ttu-id="88b6c-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="88b6c-3804">\_ ulNumerator</span></span>

<span data-ttu-id="88b6c-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="88b6c-3805">\_ulDenominator</span></span>

<span data-ttu-id="88b6c-3806">\_烏鴉</span><span class="sxs-lookup"><span data-stu-id="88b6c-3806">\_cRows</span></span>

<span data-ttu-id="88b6c-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="88b6c-3807">\_fNewRows</span></span>



 

<span data-ttu-id="88b6c-3808">**\_ ulNumerator**：32位不帶正負號的整數，指出完成比率的分子（以資料列數為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="88b6c-3809">**\_ ulDenominator**：32位不帶正負號整數，指出完成比率的分母（以資料列為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="88b6c-3810">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="88b6c-3811">**\_ >crows**：32位不帶正負號的整數，指出查詢的資料列總數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="88b6c-3812">**\_ fNewRows**：布林值，指出是否有新的資料列可用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="88b6c-3813">值為0x00000001 表示資料列集內有新的資料列可用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="88b6c-3814">值為0x00000000 表示資料列集不包含任何新的資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="88b6c-3815">這個欄位不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="88b6c-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="88b6c-3817">CPMFetchValueIn 訊息要求的屬性值太大而無法在資料列集中傳回。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="88b6c-3818">如3.2.4.2.5 一節中所指定，此訊息會重複傳送以抓取屬性的所有位元組，並為 \_ 每個位元組更新 cbSoFar，直到 \_ CPMFetchValueOut 訊息的 fMoreExists 欄位設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="88b6c-3819">標頭後面的 CPMFetchValueIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3820">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3820">0</span></span>

<span data-ttu-id="88b6c-3821">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3821">1</span></span>

<span data-ttu-id="88b6c-3822">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3822">2</span></span>

<span data-ttu-id="88b6c-3823">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3823">3</span></span>

<span data-ttu-id="88b6c-3824">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3824">4</span></span>

<span data-ttu-id="88b6c-3825">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3825">5</span></span>

<span data-ttu-id="88b6c-3826">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3826">6</span></span>

<span data-ttu-id="88b6c-3827">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3827">7</span></span>

<span data-ttu-id="88b6c-3828">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3828">8</span></span>

<span data-ttu-id="88b6c-3829">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3829">9</span></span>

<span data-ttu-id="88b6c-3830">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3830">1</span></span><br/> <span data-ttu-id="88b6c-3831">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3831">0</span></span><br/>

<span data-ttu-id="88b6c-3832">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3832">1</span></span>

<span data-ttu-id="88b6c-3833">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3833">2</span></span>

<span data-ttu-id="88b6c-3834">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3834">3</span></span>

<span data-ttu-id="88b6c-3835">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3835">4</span></span>

<span data-ttu-id="88b6c-3836">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3836">5</span></span>

<span data-ttu-id="88b6c-3837">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3837">6</span></span>

<span data-ttu-id="88b6c-3838">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3838">7</span></span>

<span data-ttu-id="88b6c-3839">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3839">8</span></span>

<span data-ttu-id="88b6c-3840">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3840">9</span></span>

<span data-ttu-id="88b6c-3841">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3841">2</span></span><br/> <span data-ttu-id="88b6c-3842">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3842">0</span></span><br/>

<span data-ttu-id="88b6c-3843">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3843">1</span></span>

<span data-ttu-id="88b6c-3844">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3844">2</span></span>

<span data-ttu-id="88b6c-3845">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3845">3</span></span>

<span data-ttu-id="88b6c-3846">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3846">4</span></span>

<span data-ttu-id="88b6c-3847">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3847">5</span></span>

<span data-ttu-id="88b6c-3848">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3848">6</span></span>

<span data-ttu-id="88b6c-3849">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3849">7</span></span>

<span data-ttu-id="88b6c-3850">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3850">8</span></span>

<span data-ttu-id="88b6c-3851">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3851">9</span></span>

<span data-ttu-id="88b6c-3852">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3852">3</span></span><br/> <span data-ttu-id="88b6c-3853">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3853">0</span></span><br/>

<span data-ttu-id="88b6c-3854">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3854">1</span></span>

<span data-ttu-id="88b6c-3855">\_Wid</span><span class="sxs-lookup"><span data-stu-id="88b6c-3855">\_wid</span></span>

<span data-ttu-id="88b6c-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="88b6c-3856">\_cbSoFar</span></span>

<span data-ttu-id="88b6c-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="88b6c-3857">\_cbPropSpec</span></span>

<span data-ttu-id="88b6c-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="88b6c-3858">\_cbChunk</span></span>

<span data-ttu-id="88b6c-3859">PropSpec (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3859">PropSpec (variable)</span></span>

<span data-ttu-id="88b6c-3860">...</span><span class="sxs-lookup"><span data-stu-id="88b6c-3860">...</span></span>

<span data-ttu-id="88b6c-3861">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="88b6c-3862">**\_ wid**：32位不帶正負號的整數，其中包含可識別應提取屬性之檔識別碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="88b6c-3863">**\_ cbSoFar**：32位不帶正負號的整數，其中包含先前針對此屬性傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="88b6c-3864">在第一則訊息中必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="88b6c-3865">**\_ cbPropSpec**：32位不帶正負號的整數，其中包含 PropSpec 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="88b6c-3866">**\_ cbChunk**：32位不帶正負號的整數，其中包含傳送者可在 CPMFetchValueOut 訊息中接受的位元組數目上限。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="88b6c-3867">*Windows 行為：此欄位會設定為所有 Windows 版本的0x00004000。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="88b6c-3868">**PropSpec**：指定要取得之屬性的 CFullPropSpec 結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="88b6c-3869">**\_ 填補**：此欄位必須是必要的長度 (0 至3個位元組) 將訊息填補至4個位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="88b6c-3870">填補位元組的值可以是任意值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="88b6c-3871">接收者必須忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="88b6c-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="88b6c-3873">CPMFetchValueOut 訊息會使用前一個查詢的屬性值回復 CPMFetchValueIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="88b6c-3874">如3.1.5.2.8 一節中所指定，此訊息會在每個 CPMFetchValueIn 訊息之後傳送，直到屬性的所有位元組都經過傳送為止。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="88b6c-3875">標頭後面的 CPMFetchValueOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3876">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3876">0</span></span>

<span data-ttu-id="88b6c-3877">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3877">1</span></span>

<span data-ttu-id="88b6c-3878">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3878">2</span></span>

<span data-ttu-id="88b6c-3879">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3879">3</span></span>

<span data-ttu-id="88b6c-3880">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3880">4</span></span>

<span data-ttu-id="88b6c-3881">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3881">5</span></span>

<span data-ttu-id="88b6c-3882">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3882">6</span></span>

<span data-ttu-id="88b6c-3883">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3883">7</span></span>

<span data-ttu-id="88b6c-3884">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3884">8</span></span>

<span data-ttu-id="88b6c-3885">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3885">9</span></span>

<span data-ttu-id="88b6c-3886">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3886">1</span></span><br/> <span data-ttu-id="88b6c-3887">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3887">0</span></span><br/>

<span data-ttu-id="88b6c-3888">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3888">1</span></span>

<span data-ttu-id="88b6c-3889">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3889">2</span></span>

<span data-ttu-id="88b6c-3890">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3890">3</span></span>

<span data-ttu-id="88b6c-3891">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3891">4</span></span>

<span data-ttu-id="88b6c-3892">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3892">5</span></span>

<span data-ttu-id="88b6c-3893">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3893">6</span></span>

<span data-ttu-id="88b6c-3894">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3894">7</span></span>

<span data-ttu-id="88b6c-3895">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3895">8</span></span>

<span data-ttu-id="88b6c-3896">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3896">9</span></span>

<span data-ttu-id="88b6c-3897">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3897">2</span></span><br/> <span data-ttu-id="88b6c-3898">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3898">0</span></span><br/>

<span data-ttu-id="88b6c-3899">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3899">1</span></span>

<span data-ttu-id="88b6c-3900">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3900">2</span></span>

<span data-ttu-id="88b6c-3901">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3901">3</span></span>

<span data-ttu-id="88b6c-3902">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3902">4</span></span>

<span data-ttu-id="88b6c-3903">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3903">5</span></span>

<span data-ttu-id="88b6c-3904">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3904">6</span></span>

<span data-ttu-id="88b6c-3905">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3905">7</span></span>

<span data-ttu-id="88b6c-3906">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3906">8</span></span>

<span data-ttu-id="88b6c-3907">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3907">9</span></span>

<span data-ttu-id="88b6c-3908">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3908">3</span></span><br/> <span data-ttu-id="88b6c-3909">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3909">0</span></span><br/>

<span data-ttu-id="88b6c-3910">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3910">1</span></span>

<span data-ttu-id="88b6c-3911">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="88b6c-3911">\_cbValue</span></span>

<span data-ttu-id="88b6c-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="88b6c-3912">\_fMoreExists</span></span>

<span data-ttu-id="88b6c-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="88b6c-3913">\_fValueExists</span></span>

<span data-ttu-id="88b6c-3914">vType</span><span class="sxs-lookup"><span data-stu-id="88b6c-3914">vType</span></span>

<span data-ttu-id="88b6c-3915">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="88b6c-3915">vValue (variable)</span></span>



 

<span data-ttu-id="88b6c-3916">**\_ cbValue**：32位不帶正負號的整數，其中包含總大小（以位元組為單位） vValue。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="88b6c-3917">**\_ fMoreExists**：布林值，指出是否有其他可用的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="88b6c-3918">如果設定為0x00000001，則會有額外的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="88b6c-3919">如果設定為0x00000000，則沒有其他可用的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="88b6c-3920">**\_ fValueExists**：布林值，指出屬性是否有值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="88b6c-3921">如果設定為0x00000001，屬性的值就會存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="88b6c-3922">如果設定為0x00000000，則屬性的值不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="88b6c-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span><span class="sxs-lookup"><span data-stu-id="88b6c-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="88b6c-3924">**vValue**：位元組陣列的一部分，其中包含2.2.1.32 區段中指定的 SERIALIZEDPROPERTYVALUE 結構，其中部分開頭的位移是 \_ CPMFetchValueIn 中 cbSoFar 的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="88b6c-3925">\_如果 fMoreExists 設定為0x00000001，部分的長度（以 cbValue 欄位表示）必須等於 \_ CPMFetchValueIn 中 cbChunk 的值， \_ 否則必須小於或等於 cbChunk 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="88b6c-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="88b6c-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="88b6c-3927">CPMGetNotify 訊息會要求用戶端想要收到資料列集變更的通知。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="88b6c-3928">訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="88b6c-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="88b6c-3930">CPMSendNotifyOut 訊息會通知用戶端查詢結果的變更。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="88b6c-3931">只有在發生變更時，才會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="88b6c-3932">標頭後面的 CPMSendNotifyOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3933">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3933">0</span></span>

<span data-ttu-id="88b6c-3934">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3934">1</span></span>

<span data-ttu-id="88b6c-3935">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3935">2</span></span>

<span data-ttu-id="88b6c-3936">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3936">3</span></span>

<span data-ttu-id="88b6c-3937">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3937">4</span></span>

<span data-ttu-id="88b6c-3938">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3938">5</span></span>

<span data-ttu-id="88b6c-3939">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3939">6</span></span>

<span data-ttu-id="88b6c-3940">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3940">7</span></span>

<span data-ttu-id="88b6c-3941">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3941">8</span></span>

<span data-ttu-id="88b6c-3942">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3942">9</span></span>

<span data-ttu-id="88b6c-3943">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3943">1</span></span><br/> <span data-ttu-id="88b6c-3944">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3944">0</span></span><br/>

<span data-ttu-id="88b6c-3945">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3945">1</span></span>

<span data-ttu-id="88b6c-3946">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3946">2</span></span>

<span data-ttu-id="88b6c-3947">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3947">3</span></span>

<span data-ttu-id="88b6c-3948">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3948">4</span></span>

<span data-ttu-id="88b6c-3949">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3949">5</span></span>

<span data-ttu-id="88b6c-3950">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3950">6</span></span>

<span data-ttu-id="88b6c-3951">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3951">7</span></span>

<span data-ttu-id="88b6c-3952">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3952">8</span></span>

<span data-ttu-id="88b6c-3953">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3953">9</span></span>

<span data-ttu-id="88b6c-3954">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3954">2</span></span><br/> <span data-ttu-id="88b6c-3955">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3955">0</span></span><br/>

<span data-ttu-id="88b6c-3956">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3956">1</span></span>

<span data-ttu-id="88b6c-3957">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3957">2</span></span>

<span data-ttu-id="88b6c-3958">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3958">3</span></span>

<span data-ttu-id="88b6c-3959">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3959">4</span></span>

<span data-ttu-id="88b6c-3960">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3960">5</span></span>

<span data-ttu-id="88b6c-3961">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3961">6</span></span>

<span data-ttu-id="88b6c-3962">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3962">7</span></span>

<span data-ttu-id="88b6c-3963">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3963">8</span></span>

<span data-ttu-id="88b6c-3964">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3964">9</span></span>

<span data-ttu-id="88b6c-3965">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3965">3</span></span><br/> <span data-ttu-id="88b6c-3966">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3966">0</span></span><br/>

<span data-ttu-id="88b6c-3967">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3967">1</span></span>

<span data-ttu-id="88b6c-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="88b6c-3968">\_watchNotify</span></span>



 

<span data-ttu-id="88b6c-3969">**\_ watchNotify**：對查詢的變更。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="88b6c-3970">它必須是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="88b6c-3971">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-3971">Value</span></span>                                     | <span data-ttu-id="88b6c-3972">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="88b6c-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="88b6c-3974">查詢資料列集中的資料列數目已變更。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="88b6c-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="88b6c-3976">查詢已完成。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="88b6c-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="88b6c-3978">已重新執行查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="88b6c-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="88b6c-3980">CPMGetApproximatePositionIn 訊息會要求某一章中書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="88b6c-3981">標頭後面的 CPMGetApproximatePositionIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-3982">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3982">0</span></span>

<span data-ttu-id="88b6c-3983">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3983">1</span></span>

<span data-ttu-id="88b6c-3984">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3984">2</span></span>

<span data-ttu-id="88b6c-3985">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3985">3</span></span>

<span data-ttu-id="88b6c-3986">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3986">4</span></span>

<span data-ttu-id="88b6c-3987">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3987">5</span></span>

<span data-ttu-id="88b6c-3988">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3988">6</span></span>

<span data-ttu-id="88b6c-3989">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-3989">7</span></span>

<span data-ttu-id="88b6c-3990">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-3990">8</span></span>

<span data-ttu-id="88b6c-3991">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-3991">9</span></span>

<span data-ttu-id="88b6c-3992">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3992">1</span></span><br/> <span data-ttu-id="88b6c-3993">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-3993">0</span></span><br/>

<span data-ttu-id="88b6c-3994">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-3994">1</span></span>

<span data-ttu-id="88b6c-3995">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-3995">2</span></span>

<span data-ttu-id="88b6c-3996">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-3996">3</span></span>

<span data-ttu-id="88b6c-3997">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-3997">4</span></span>

<span data-ttu-id="88b6c-3998">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-3998">5</span></span>

<span data-ttu-id="88b6c-3999">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-3999">6</span></span>

<span data-ttu-id="88b6c-4000">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4000">7</span></span>

<span data-ttu-id="88b6c-4001">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4001">8</span></span>

<span data-ttu-id="88b6c-4002">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4002">9</span></span>

<span data-ttu-id="88b6c-4003">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4003">2</span></span><br/> <span data-ttu-id="88b6c-4004">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4004">0</span></span><br/>

<span data-ttu-id="88b6c-4005">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4005">1</span></span>

<span data-ttu-id="88b6c-4006">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4006">2</span></span>

<span data-ttu-id="88b6c-4007">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4007">3</span></span>

<span data-ttu-id="88b6c-4008">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4008">4</span></span>

<span data-ttu-id="88b6c-4009">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4009">5</span></span>

<span data-ttu-id="88b6c-4010">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4010">6</span></span>

<span data-ttu-id="88b6c-4011">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4011">7</span></span>

<span data-ttu-id="88b6c-4012">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4012">8</span></span>

<span data-ttu-id="88b6c-4013">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4013">9</span></span>

<span data-ttu-id="88b6c-4014">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4014">3</span></span><br/> <span data-ttu-id="88b6c-4015">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4015">0</span></span><br/>

<span data-ttu-id="88b6c-4016">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4016">1</span></span>

<span data-ttu-id="88b6c-4017">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-4017">\_hCursor</span></span>

<span data-ttu-id="88b6c-4018">\_chapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-4018">\_chapt</span></span>

<span data-ttu-id="88b6c-4019">\_bmk</span><span class="sxs-lookup"><span data-stu-id="88b6c-4019">\_bmk</span></span>



 

<span data-ttu-id="88b6c-4020">**\_ hCursor**：代表從 CPMCreateQueryOut 針對包含書簽的資料列集取得之查詢資料指標的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="88b6c-4021">**\_ chapt**：代表包含書簽之章節控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="88b6c-4022">**\_ bmk**：代表要取得其近似位置之書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="88b6c-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="88b6c-4024">CPMGetApproximatePositionOut 訊息會回復 CPMGetApproximatePositionIn 訊息，其中描述章節中書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="88b6c-4025">標頭後面的 CPMGetApproximatePositionOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4026">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4026">0</span></span>

<span data-ttu-id="88b6c-4027">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4027">1</span></span>

<span data-ttu-id="88b6c-4028">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4028">2</span></span>

<span data-ttu-id="88b6c-4029">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4029">3</span></span>

<span data-ttu-id="88b6c-4030">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4030">4</span></span>

<span data-ttu-id="88b6c-4031">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4031">5</span></span>

<span data-ttu-id="88b6c-4032">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4032">6</span></span>

<span data-ttu-id="88b6c-4033">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4033">7</span></span>

<span data-ttu-id="88b6c-4034">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4034">8</span></span>

<span data-ttu-id="88b6c-4035">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4035">9</span></span>

<span data-ttu-id="88b6c-4036">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4036">1</span></span><br/> <span data-ttu-id="88b6c-4037">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4037">0</span></span><br/>

<span data-ttu-id="88b6c-4038">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4038">1</span></span>

<span data-ttu-id="88b6c-4039">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4039">2</span></span>

<span data-ttu-id="88b6c-4040">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4040">3</span></span>

<span data-ttu-id="88b6c-4041">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4041">4</span></span>

<span data-ttu-id="88b6c-4042">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4042">5</span></span>

<span data-ttu-id="88b6c-4043">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4043">6</span></span>

<span data-ttu-id="88b6c-4044">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4044">7</span></span>

<span data-ttu-id="88b6c-4045">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4045">8</span></span>

<span data-ttu-id="88b6c-4046">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4046">9</span></span>

<span data-ttu-id="88b6c-4047">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4047">2</span></span><br/> <span data-ttu-id="88b6c-4048">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4048">0</span></span><br/>

<span data-ttu-id="88b6c-4049">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4049">1</span></span>

<span data-ttu-id="88b6c-4050">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4050">2</span></span>

<span data-ttu-id="88b6c-4051">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4051">3</span></span>

<span data-ttu-id="88b6c-4052">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4052">4</span></span>

<span data-ttu-id="88b6c-4053">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4053">5</span></span>

<span data-ttu-id="88b6c-4054">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4054">6</span></span>

<span data-ttu-id="88b6c-4055">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4055">7</span></span>

<span data-ttu-id="88b6c-4056">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4056">8</span></span>

<span data-ttu-id="88b6c-4057">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4057">9</span></span>

<span data-ttu-id="88b6c-4058">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4058">3</span></span><br/> <span data-ttu-id="88b6c-4059">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4059">0</span></span><br/>

<span data-ttu-id="88b6c-4060">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4060">1</span></span>

<span data-ttu-id="88b6c-4061">\_分子</span><span class="sxs-lookup"><span data-stu-id="88b6c-4061">\_numerator</span></span>

<span data-ttu-id="88b6c-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="88b6c-4062">\_denominator</span></span>



 

<span data-ttu-id="88b6c-4063">**\_ 分子**：32位不帶正負號的整數，其中包含資料列集中書簽的資料列編號。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="88b6c-4064">如果沒有任何資料列，則此欄位必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="88b6c-4065">**\_ 分母**：32位不帶正負號的整數，其中包含資料列集中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="88b6c-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="88b6c-4067">CPMCompareBmkIn 訊息會要求一章中兩個書簽的比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="88b6c-4068">標頭後面的 CPMCompareBmkIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4069">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4069">0</span></span>

<span data-ttu-id="88b6c-4070">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4070">1</span></span>

<span data-ttu-id="88b6c-4071">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4071">2</span></span>

<span data-ttu-id="88b6c-4072">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4072">3</span></span>

<span data-ttu-id="88b6c-4073">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4073">4</span></span>

<span data-ttu-id="88b6c-4074">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4074">5</span></span>

<span data-ttu-id="88b6c-4075">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4075">6</span></span>

<span data-ttu-id="88b6c-4076">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4076">7</span></span>

<span data-ttu-id="88b6c-4077">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4077">8</span></span>

<span data-ttu-id="88b6c-4078">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4078">9</span></span>

<span data-ttu-id="88b6c-4079">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4079">1</span></span><br/> <span data-ttu-id="88b6c-4080">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4080">0</span></span><br/>

<span data-ttu-id="88b6c-4081">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4081">1</span></span>

<span data-ttu-id="88b6c-4082">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4082">2</span></span>

<span data-ttu-id="88b6c-4083">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4083">3</span></span>

<span data-ttu-id="88b6c-4084">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4084">4</span></span>

<span data-ttu-id="88b6c-4085">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4085">5</span></span>

<span data-ttu-id="88b6c-4086">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4086">6</span></span>

<span data-ttu-id="88b6c-4087">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4087">7</span></span>

<span data-ttu-id="88b6c-4088">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4088">8</span></span>

<span data-ttu-id="88b6c-4089">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4089">9</span></span>

<span data-ttu-id="88b6c-4090">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4090">2</span></span><br/> <span data-ttu-id="88b6c-4091">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4091">0</span></span><br/>

<span data-ttu-id="88b6c-4092">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4092">1</span></span>

<span data-ttu-id="88b6c-4093">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4093">2</span></span>

<span data-ttu-id="88b6c-4094">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4094">3</span></span>

<span data-ttu-id="88b6c-4095">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4095">4</span></span>

<span data-ttu-id="88b6c-4096">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4096">5</span></span>

<span data-ttu-id="88b6c-4097">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4097">6</span></span>

<span data-ttu-id="88b6c-4098">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4098">7</span></span>

<span data-ttu-id="88b6c-4099">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4099">8</span></span>

<span data-ttu-id="88b6c-4100">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4100">9</span></span>

<span data-ttu-id="88b6c-4101">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4101">3</span></span><br/> <span data-ttu-id="88b6c-4102">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4102">0</span></span><br/>

<span data-ttu-id="88b6c-4103">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4103">1</span></span>

<span data-ttu-id="88b6c-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-4104">\_hCursor</span></span>

<span data-ttu-id="88b6c-4105">\_chapt</span><span class="sxs-lookup"><span data-stu-id="88b6c-4105">\_chapt</span></span>

<span data-ttu-id="88b6c-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="88b6c-4106">\_bmkFirst</span></span>

<span data-ttu-id="88b6c-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="88b6c-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="88b6c-4108">\_**hCursor**：代表包含書簽之資料列集之 CPMCreateQueryOut 訊息控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="88b6c-4109">\_**chapt**：代表章節之控制碼的32位值，其中包含要比較的書簽。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="88b6c-4110">\_**bmkFirst**：代表要比較之第一個書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="88b6c-4111">\_**bmkSecond**：代表要比較之第二個書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="88b6c-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="88b6c-4113">CPMCompareBmkOut 訊息會使用一章中兩個書簽的比較來回複 CPMCompareBmkIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="88b6c-4114">標頭後面的 CPMCompareBmkOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4115">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4115">0</span></span>

<span data-ttu-id="88b6c-4116">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4116">1</span></span>

<span data-ttu-id="88b6c-4117">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4117">2</span></span>

<span data-ttu-id="88b6c-4118">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4118">3</span></span>

<span data-ttu-id="88b6c-4119">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4119">4</span></span>

<span data-ttu-id="88b6c-4120">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4120">5</span></span>

<span data-ttu-id="88b6c-4121">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4121">6</span></span>

<span data-ttu-id="88b6c-4122">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4122">7</span></span>

<span data-ttu-id="88b6c-4123">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4123">8</span></span>

<span data-ttu-id="88b6c-4124">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4124">9</span></span>

<span data-ttu-id="88b6c-4125">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4125">1</span></span><br/> <span data-ttu-id="88b6c-4126">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4126">0</span></span><br/>

<span data-ttu-id="88b6c-4127">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4127">1</span></span>

<span data-ttu-id="88b6c-4128">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4128">2</span></span>

<span data-ttu-id="88b6c-4129">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4129">3</span></span>

<span data-ttu-id="88b6c-4130">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4130">4</span></span>

<span data-ttu-id="88b6c-4131">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4131">5</span></span>

<span data-ttu-id="88b6c-4132">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4132">6</span></span>

<span data-ttu-id="88b6c-4133">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4133">7</span></span>

<span data-ttu-id="88b6c-4134">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4134">8</span></span>

<span data-ttu-id="88b6c-4135">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4135">9</span></span>

<span data-ttu-id="88b6c-4136">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4136">2</span></span><br/> <span data-ttu-id="88b6c-4137">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4137">0</span></span><br/>

<span data-ttu-id="88b6c-4138">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4138">1</span></span>

<span data-ttu-id="88b6c-4139">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4139">2</span></span>

<span data-ttu-id="88b6c-4140">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4140">3</span></span>

<span data-ttu-id="88b6c-4141">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4141">4</span></span>

<span data-ttu-id="88b6c-4142">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4142">5</span></span>

<span data-ttu-id="88b6c-4143">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4143">6</span></span>

<span data-ttu-id="88b6c-4144">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4144">7</span></span>

<span data-ttu-id="88b6c-4145">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4145">8</span></span>

<span data-ttu-id="88b6c-4146">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4146">9</span></span>

<span data-ttu-id="88b6c-4147">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4147">3</span></span><br/> <span data-ttu-id="88b6c-4148">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4148">0</span></span><br/>

<span data-ttu-id="88b6c-4149">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4149">1</span></span>

<span data-ttu-id="88b6c-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="88b6c-4150">\_dwComparison</span></span>



 

<span data-ttu-id="88b6c-4151">\_**dwComparison**：下列其中一個值，表示章節中兩個書簽的相對位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="88b6c-4152">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-4152">Value</span></span>                               | <span data-ttu-id="88b6c-4153">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="88b6c-4154">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="88b6c-4155">第一個書簽位於第二個。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="88b6c-4156">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b6c-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="88b6c-4157">第一個書簽的位置與第二個相同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="88b6c-4158">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b6c-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="88b6c-4159">第一個書簽的位置是在第二個。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="88b6c-4160">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="88b6c-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="88b6c-4161">第一個書簽的位置與第二個不同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="88b6c-4162">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="88b6c-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="88b6c-4163">第一個書簽無法與第二個書簽比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="88b6c-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="88b6c-4165">CPMRestartPositionIn 訊息會將資料指標的提取位置移至章節的開頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="88b6c-4166">如3.1.5.2.12 一節中所指定，伺服器將使用相同的訊息來回複，並將要求的結果包含在 \_ CISP 標頭的 status 欄位中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="88b6c-4167">標頭後面的 CPMRestartPositionIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4168">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4168">0</span></span>

<span data-ttu-id="88b6c-4169">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4169">1</span></span>

<span data-ttu-id="88b6c-4170">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4170">2</span></span>

<span data-ttu-id="88b6c-4171">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4171">3</span></span>

<span data-ttu-id="88b6c-4172">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4172">4</span></span>

<span data-ttu-id="88b6c-4173">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4173">5</span></span>

<span data-ttu-id="88b6c-4174">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4174">6</span></span>

<span data-ttu-id="88b6c-4175">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4175">7</span></span>

<span data-ttu-id="88b6c-4176">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4176">8</span></span>

<span data-ttu-id="88b6c-4177">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4177">9</span></span>

<span data-ttu-id="88b6c-4178">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4178">1</span></span><br/> <span data-ttu-id="88b6c-4179">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4179">0</span></span><br/>

<span data-ttu-id="88b6c-4180">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4180">1</span></span>

<span data-ttu-id="88b6c-4181">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4181">2</span></span>

<span data-ttu-id="88b6c-4182">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4182">3</span></span>

<span data-ttu-id="88b6c-4183">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4183">4</span></span>

<span data-ttu-id="88b6c-4184">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4184">5</span></span>

<span data-ttu-id="88b6c-4185">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4185">6</span></span>

<span data-ttu-id="88b6c-4186">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4186">7</span></span>

<span data-ttu-id="88b6c-4187">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4187">8</span></span>

<span data-ttu-id="88b6c-4188">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4188">9</span></span>

<span data-ttu-id="88b6c-4189">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4189">2</span></span><br/> <span data-ttu-id="88b6c-4190">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4190">0</span></span><br/>

<span data-ttu-id="88b6c-4191">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4191">1</span></span>

<span data-ttu-id="88b6c-4192">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4192">2</span></span>

<span data-ttu-id="88b6c-4193">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4193">3</span></span>

<span data-ttu-id="88b6c-4194">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4194">4</span></span>

<span data-ttu-id="88b6c-4195">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4195">5</span></span>

<span data-ttu-id="88b6c-4196">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4196">6</span></span>

<span data-ttu-id="88b6c-4197">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4197">7</span></span>

<span data-ttu-id="88b6c-4198">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4198">8</span></span>

<span data-ttu-id="88b6c-4199">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4199">9</span></span>

<span data-ttu-id="88b6c-4200">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4200">3</span></span><br/> <span data-ttu-id="88b6c-4201">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4201">0</span></span><br/>

<span data-ttu-id="88b6c-4202">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4202">1</span></span>

<span data-ttu-id="88b6c-4203">\_hCursor (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="88b6c-4204">\_chapt (選用) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="88b6c-4205">**\_ hCursor**：代表從 CPMCreateQueryOut 訊息取得之控制碼的32位值，識別要重新開機位置的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="88b6c-4206">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="88b6c-4207">**\_ chapt**：代表從中取出資料列之章節控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="88b6c-4208">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="88b6c-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="88b6c-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="88b6c-4210">CPMFreeCursorIn 訊息會要求資料指標的版本。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="88b6c-4211">標頭後面的 CPMFreeCursorIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4212">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4212">0</span></span>

<span data-ttu-id="88b6c-4213">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4213">1</span></span>

<span data-ttu-id="88b6c-4214">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4214">2</span></span>

<span data-ttu-id="88b6c-4215">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4215">3</span></span>

<span data-ttu-id="88b6c-4216">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4216">4</span></span>

<span data-ttu-id="88b6c-4217">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4217">5</span></span>

<span data-ttu-id="88b6c-4218">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4218">6</span></span>

<span data-ttu-id="88b6c-4219">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4219">7</span></span>

<span data-ttu-id="88b6c-4220">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4220">8</span></span>

<span data-ttu-id="88b6c-4221">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4221">9</span></span>

<span data-ttu-id="88b6c-4222">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4222">1</span></span><br/> <span data-ttu-id="88b6c-4223">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4223">0</span></span><br/>

<span data-ttu-id="88b6c-4224">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4224">1</span></span>

<span data-ttu-id="88b6c-4225">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4225">2</span></span>

<span data-ttu-id="88b6c-4226">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4226">3</span></span>

<span data-ttu-id="88b6c-4227">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4227">4</span></span>

<span data-ttu-id="88b6c-4228">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4228">5</span></span>

<span data-ttu-id="88b6c-4229">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4229">6</span></span>

<span data-ttu-id="88b6c-4230">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4230">7</span></span>

<span data-ttu-id="88b6c-4231">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4231">8</span></span>

<span data-ttu-id="88b6c-4232">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4232">9</span></span>

<span data-ttu-id="88b6c-4233">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4233">2</span></span><br/> <span data-ttu-id="88b6c-4234">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4234">0</span></span><br/>

<span data-ttu-id="88b6c-4235">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4235">1</span></span>

<span data-ttu-id="88b6c-4236">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4236">2</span></span>

<span data-ttu-id="88b6c-4237">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4237">3</span></span>

<span data-ttu-id="88b6c-4238">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4238">4</span></span>

<span data-ttu-id="88b6c-4239">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4239">5</span></span>

<span data-ttu-id="88b6c-4240">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4240">6</span></span>

<span data-ttu-id="88b6c-4241">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4241">7</span></span>

<span data-ttu-id="88b6c-4242">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4242">8</span></span>

<span data-ttu-id="88b6c-4243">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4243">9</span></span>

<span data-ttu-id="88b6c-4244">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4244">3</span></span><br/> <span data-ttu-id="88b6c-4245">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4245">0</span></span><br/>

<span data-ttu-id="88b6c-4246">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4246">1</span></span>

<span data-ttu-id="88b6c-4247">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="88b6c-4247">\_hCursor</span></span>



 

<span data-ttu-id="88b6c-4248">**\_ hCursor**：代表要釋放之 CPMCreateQueryOut 訊息中資料指標控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="88b6c-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="88b6c-4250">CPMFreeCursorOut 訊息會回復 CPMFreeCursorIn 訊息，其中包含釋出資料指標的結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="88b6c-4251">標頭後面的 CPMFreeCursorOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="88b6c-4252">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4252">0</span></span>

<span data-ttu-id="88b6c-4253">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4253">1</span></span>

<span data-ttu-id="88b6c-4254">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4254">2</span></span>

<span data-ttu-id="88b6c-4255">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4255">3</span></span>

<span data-ttu-id="88b6c-4256">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4256">4</span></span>

<span data-ttu-id="88b6c-4257">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4257">5</span></span>

<span data-ttu-id="88b6c-4258">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4258">6</span></span>

<span data-ttu-id="88b6c-4259">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4259">7</span></span>

<span data-ttu-id="88b6c-4260">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4260">8</span></span>

<span data-ttu-id="88b6c-4261">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4261">9</span></span>

<span data-ttu-id="88b6c-4262">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4262">1</span></span><br/> <span data-ttu-id="88b6c-4263">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4263">0</span></span><br/>

<span data-ttu-id="88b6c-4264">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4264">1</span></span>

<span data-ttu-id="88b6c-4265">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4265">2</span></span>

<span data-ttu-id="88b6c-4266">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4266">3</span></span>

<span data-ttu-id="88b6c-4267">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4267">4</span></span>

<span data-ttu-id="88b6c-4268">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4268">5</span></span>

<span data-ttu-id="88b6c-4269">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4269">6</span></span>

<span data-ttu-id="88b6c-4270">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4270">7</span></span>

<span data-ttu-id="88b6c-4271">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4271">8</span></span>

<span data-ttu-id="88b6c-4272">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4272">9</span></span>

<span data-ttu-id="88b6c-4273">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4273">2</span></span><br/> <span data-ttu-id="88b6c-4274">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4274">0</span></span><br/>

<span data-ttu-id="88b6c-4275">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4275">1</span></span>

<span data-ttu-id="88b6c-4276">2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4276">2</span></span>

<span data-ttu-id="88b6c-4277">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4277">3</span></span>

<span data-ttu-id="88b6c-4278">4</span><span class="sxs-lookup"><span data-stu-id="88b6c-4278">4</span></span>

<span data-ttu-id="88b6c-4279">5</span><span class="sxs-lookup"><span data-stu-id="88b6c-4279">5</span></span>

<span data-ttu-id="88b6c-4280">6</span><span class="sxs-lookup"><span data-stu-id="88b6c-4280">6</span></span>

<span data-ttu-id="88b6c-4281">7</span><span class="sxs-lookup"><span data-stu-id="88b6c-4281">7</span></span>

<span data-ttu-id="88b6c-4282">8</span><span class="sxs-lookup"><span data-stu-id="88b6c-4282">8</span></span>

<span data-ttu-id="88b6c-4283">9</span><span class="sxs-lookup"><span data-stu-id="88b6c-4283">9</span></span>

<span data-ttu-id="88b6c-4284">3</span><span class="sxs-lookup"><span data-stu-id="88b6c-4284">3</span></span><br/> <span data-ttu-id="88b6c-4285">0</span><span class="sxs-lookup"><span data-stu-id="88b6c-4285">0</span></span><br/>

<span data-ttu-id="88b6c-4286">1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4286">1</span></span>

<span data-ttu-id="88b6c-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="88b6c-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="88b6c-4288">**\_ cCursorsRemaining**：32位不帶正負號的整數，表示仍在查詢中使用的資料指標數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="88b6c-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="88b6c-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="88b6c-4290">CPMDisconnect 訊息會結束與伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="88b6c-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="88b6c-4291">訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="88b6c-4292">2.2.4 錯誤</span><span class="sxs-lookup"><span data-stu-id="88b6c-4292">2.2.4 Errors</span></span>

<span data-ttu-id="88b6c-4293">所有內容索引服務通訊協定訊息都必須在成功時傳回 0x00000000;否則，它們會傳回32位非零的錯誤碼，此錯誤碼可以是 HRESULT 或 NTSTATUS 值 (請參閱 1.8) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="88b6c-4294">如果緩衝區太小而無法符合結果，就必須傳回狀態為 [ \_ 資源不足] (0xC0000009A) 的狀態碼， \_ 而且應該以較大的緩衝區重試失敗的作業。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="88b6c-4295">所有其他錯誤值都必須視為相同。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="88b6c-4296"> (請注意，除非具有相同意義的值，否則目前的 HRESULT 和 NTSTATUS 編號空間不會重迭，但即使它們在未來會發生衝突，也不會造成任何通訊協定問題，只要狀態不足的資源值仍維持唯一的值，就不會造成任何通訊協定問題 \_ \_ ，因為所有其他錯誤值的處理方式都相同。 ) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="88b6c-4297">3 通訊協定詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="88b6c-4298">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="88b6c-4299">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="88b6c-4300">從遠端查詢索引服務目錄的 CISP 訊息要求不需要任何特定的順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="88b6c-4301">建議您將較高的層級導向至有意義的訊息順序，不過，就像是從這個序列或使用不正確資料收到的訊息一樣，伺服器將會以錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="88b6c-4302">某些訊息也會相依于更高的層級，以提供在序列稍早的訊息中收到的有效資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="88b6c-4303">下圖說明從用戶端到遠端電腦的簡單查詢的一般訊息順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![簡單查詢的訊息順序](images/protocoldetails.jpg)

<span data-ttu-id="88b6c-4305">上圖所示的訊息代表用來查詢遠端索引服務類別目錄的所有 CISP 訊息子集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="88b6c-4306">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="88b6c-4307">3.1.1 抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="88b6c-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="88b6c-4308">下一節指定 CISP 伺服器所維護的資料和狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="88b6c-4309">此處提供的資料可協助說明通訊協定的運作方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="88b6c-4310">本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="88b6c-4311">執行 CISP 的索引服務必須維護下列抽象資料元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="88b6c-4312">連線到伺服器的用戶端清單</span><span class="sxs-lookup"><span data-stu-id="88b6c-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="88b6c-4313">每個用戶端的相關資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="88b6c-4314">用戶端的版本 (，如區段2.2.3.6 中指定的 CPMConnectIn 訊息所示) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="88b6c-4315">CPMConnectIn 訊息 (與用戶端相關聯的目錄) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="88b6c-4316">2.2.1.21.1 一節中所指定的其他用戶端屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="88b6c-4317">用戶端的搜尋查詢</span><span class="sxs-lookup"><span data-stu-id="88b6c-4317">Client's search query</span></span>
    -   <span data-ttu-id="88b6c-4318">查詢的資料指標控制碼清單以及每個控制碼的結果集中的位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="88b6c-4319">目前的系結集合</span><span class="sxs-lookup"><span data-stu-id="88b6c-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="88b6c-4320">查詢的目前狀態，其中包含每個資料指標) 的 (：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="88b6c-4321">查詢結果中的資料列數目</span><span class="sxs-lookup"><span data-stu-id="88b6c-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="88b6c-4322">查詢完成的分子和分母</span><span class="sxs-lookup"><span data-stu-id="88b6c-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="88b6c-4323">最後一個資料列數目，由這個資料指標的最新 CPMRatioFinishedOut 訊息所報告</span><span class="sxs-lookup"><span data-stu-id="88b6c-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="88b6c-4324">無論查詢是否由伺服器監視查詢結果的變更，以及它是否受到監視，查詢結果中的變更會在查詢結果中變更，因為它上次回報給用戶端的 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="88b6c-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="88b6c-4325">此查詢對用戶端提供的章節控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="88b6c-4326">此查詢對用戶端提供之每個資料指標的書簽控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="88b6c-4327">索引服務目前的狀態，可能是「未初始化」、「執行中」或「正在關機」。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="88b6c-4328">請注意，大部分的時間伺服器處於「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="88b6c-4329">以下是伺服器的狀態機器圖表：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4329">Following is the state machine diagram for the server:</span></span>

    ![索引服務伺服器的狀態機器圖表](images/abstractdatamodel.jpg)

-   <span data-ttu-id="88b6c-4331">每個目錄資訊：已編制索引的檔數目、索引的大小、唯一索引鍵的數目等 (請參閱 < 完整清單 () 的2.2.3.1 一節，其中對應至區段 2.2.3.2) 中 dwNewState 的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="88b6c-4332">針對每個支援的語言，如2.2.1.3 一節中所討論的單字變化資料庫。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="88b6c-4333">3.1.2 計時器</span><span class="sxs-lookup"><span data-stu-id="88b6c-4333">3.1.2 Timers</span></span>

<span data-ttu-id="88b6c-4334">不需要任何通訊協定計時器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="88b6c-4335">3.1.3 初始化</span><span class="sxs-lookup"><span data-stu-id="88b6c-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="88b6c-4336">初始化時，伺服器必須將其狀態設定為 [未初始化]，並開始接聽區段1.9 中指定之具名管道上的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="88b6c-4337">進行任何其他內部初始化之後，它必須轉換成「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="88b6c-4338">3.1.4 較高層級觸發事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="88b6c-4339">無。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="88b6c-4340">3.1.5 訊息處理和排序規則</span><span class="sxs-lookup"><span data-stu-id="88b6c-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="88b6c-4341">當處理用戶端傳送的訊息期間發生錯誤時，伺服器必須向用戶端報告錯誤，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="88b6c-4342">停止處理用戶端傳送的訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="88b6c-4343">以訊息標頭回應 (只有用戶端傳送的訊息) ，讓 \_ msg 欄位保持不變。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="88b6c-4344">將 [ \_ 狀態] 欄位設定為錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="88b6c-4345">當訊息抵達時，伺服器必須檢查 \_ msg 域值，以查看它是否為已知的類型 (請參閱第2.2.2 節) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="88b6c-4346">如果類型未知，則必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="88b6c-4347">\_如果訊息類型是下列其中一項，則伺服器必須驗證 ulChecksum 域值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="88b6c-4348">CPMConnectIn (0x000000C8) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="88b6c-4349">CPMCreateQueryIn (0x000000CA) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="88b6c-4350">CPMSetBindingsIn (0x000000D0) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="88b6c-4351">CPMGetRowsIn (0x000000CC) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="88b6c-4352">CPMFetchValueIn (0x000000E4) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="88b6c-4353">若要驗證 \_ ulChecksum 域值，伺服器必須檢查用戶端在 CPMConnectIn 訊息的 iClientVersion 欄位中指定的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="88b6c-4354">如果 [ \_ iClientVersion] 欄位未設定為 [0x00000008]，且 [ \_ ulChecksum] 欄位未設定為0x00000000，則伺服器必須回報狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="88b6c-4355">伺服器不能驗證 \_ 用戶端的 ulChecksum 欄位將 \_ iClientVersion 欄位設定為小於0x00000008 的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="88b6c-4356">如果 \_ iClientVersionfield 域值為0x00000008 或更大，則伺服器必須驗證 \_ ulChecksum 欄位的計算方式是在 [3.2.4] 區段中指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="88b6c-4357">如果 \_ ulChecksum 值無效，伺服器必須報告狀態不正確參數， \_ \_ (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="88b6c-4358">接著，伺服器會檢查其中的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="88b6c-4359">如果其狀態為 [未初始化]，伺服器必須報告 CI \_ E \_ 未 \_ 初始化 (0x8004180B) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="88b6c-4360">如果狀態為「關閉」，伺服器必須報告 CI \_ E \_ SHUTDOWN (0x80041812) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="88b6c-4361">一旦將標頭判斷為有效且伺服器處於「執行中」狀態之後，就必須依照下列各節所指定的方式來執行進一步的訊息特定處理。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="88b6c-4362">3.1.5.1 遠端索引服務目錄管理</span><span class="sxs-lookup"><span data-stu-id="88b6c-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="88b6c-4363">3.1.5.1.1 接收 CPMCiStateInOut 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="88b6c-4364">當伺服器收到來自用戶端的 CPMCIStateInOut 訊息要求時，伺服器必須先檢查用戶端是否在已連線的用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="88b6c-4365">如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="88b6c-4366">否則，它必須以 CPMCIStateInOut 訊息回應用戶端，並使用與2.2.3.1 小節中所指定的用戶端相關聯的目錄相關資訊來填入。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="88b6c-4367">3.1.5.1.2 接收 CPMSetCatStateIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="88b6c-4368">當伺服器收到來自用戶端的 CPMSetCatStateIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4369">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4369">Check that client has administrative access.</span></span> <span data-ttu-id="88b6c-4370">如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="88b6c-4371">如果 \_ dwNewState 不等於 CICAT ALL 會 \_ \_ 開啟，則變更 CatName 欄位中指定的目錄狀態，如 \_ dwNewState 欄位所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="88b6c-4372">如需詳細資訊，請參閱2.2.3.2 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="88b6c-4373">如果伺服器未在 CatName 欄位中找到具有指定名稱的目錄，伺服器必須傳回狀態 \_ 不正確 \_ 參數， (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4374">以 CPMSetCatStateOut 訊息回應用戶端，其中 \_ DWOLDSTATE 必須設定為目錄的先前狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="88b6c-4375">如果 \_ dwNewState 等於 CICAT， \_ 則所有 \_ 開啟的伺服器都必須檢查所有目錄的狀態，如果全部都已啟動，就必須將 \_ dwOldState 設定為0x00000001，否則請將 \_ dwOldState 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="88b6c-4376">3.1.5.1.3 接收 CPMUpdateDocumentsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="88b6c-4377">當伺服器收到 CPMUpdateDocumentsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4378">檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="88b6c-4379">如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4380">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4380">Check that client has administrative access.</span></span> <span data-ttu-id="88b6c-4381">如果用戶端沒有伺服器的系統管理存取權，則伺服器必須回報狀態 \_ \_ 拒絕存取 (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="88b6c-4382">根據 CPMUpdateDocumentsIn 訊息中的旗標欄位，開始建立用戶端所指定路徑的索引編制程式、執行完整或增量掃描 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="88b6c-4383">如果路徑先前未建立索引，則必須將它加入至索引位置的集合，並執行完整掃描。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="88b6c-4384">如果指定了不合法的 \_ 旗標欄位值，伺服器必須 \_ 將旗標設為 UPD \_ INIT 並執行完整掃描。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="88b6c-4385">這項作業必須在與用戶端相關聯的目錄中執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="88b6c-4386">使用 CPMUpdateDocumentsIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="88b6c-4387">3.1.5.1.4 接收 CPMForceMergeIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="88b6c-4388">當伺服器收到 CPMForceMergeIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4389">檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="88b6c-4390">如果用戶端不在清單中，伺服器必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4391">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4391">Check that client has administrative access.</span></span> <span data-ttu-id="88b6c-4392">如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="88b6c-4393">開始在與用戶端相關聯的目錄上改善查詢效能所需的維護流程。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="88b6c-4394">使用 CPMForceMergeIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="88b6c-4395">請注意，維護程式是非同步，而且可以在用戶端收到回應訊息之後繼續進行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="88b6c-4396">此程式不會直接影響通訊協定， (回應時間) 以外的任何方式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="88b6c-4397">3.1.5.2 遠端索引服務查詢</span><span class="sxs-lookup"><span data-stu-id="88b6c-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="88b6c-4398">3.1.5.2.1 接收 CPMConnectIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="88b6c-4399">當伺服器收到來自用戶端的 CPMConnectIn 要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4400">檢查用戶端是否在已連線用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="88b6c-4401">如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4402">檢查指定的目錄是否存在，而不是處於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="88b6c-4403">如果不是這種情況，伺服器就必須要有報表 CI \_ E \_ NO \_ CATALOG (0x8004181D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="88b6c-4404">將用戶端新增至已連線的用戶端清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="88b6c-4405">將目錄與用戶端產生關聯。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="88b6c-4406">將 CPMConnectIn 訊息中傳遞的資訊儲存 (例如目錄名稱、用戶端版本等 ) 處於用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="88b6c-4407">以 CPMConnectOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="88b6c-4408">3.1.5.2.2 接收 CPMCreateQueryIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="88b6c-4409">當伺服器收到來自用戶端的 CPMCreateQueryIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4410">檢查用戶端是否在已連線用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="88b6c-4411">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4412">檢查用戶端是否已經有與其相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="88b6c-4413">如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4414">檢查與用戶端相關聯的目錄是否處於狀態，以允許處理查詢 (CICAT \_ READONLY 或 CICAT \_ 可寫入) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="88b6c-4415">如果不是這種情況，伺服器就必須回報查詢 \_ S 查詢 \_ \_ (0x8004160C) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="88b6c-4416">剖析查詢中指定的限制集、排序次序和群組。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="88b6c-4417">如果伺服器發生錯誤，則必須報告適當的錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="88b6c-4418">如果此步驟因為任何其他原因而失敗，則伺服器必須報告所遇到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="88b6c-4419">如需索引服務查詢錯誤的詳細資訊，請參閱 \[ MSDN-QUERYERR \] 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="88b6c-4420">將搜尋查詢儲存為用戶端的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="88b6c-4421">根據 CPMCreateQueryIn 訊息) 中傳遞的資訊，進行將資料列提供給用戶端所需的準備工作，並將查詢與適當的資料指標控制碼產生關聯 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="88b6c-4422">將這些控制碼新增至用戶端的資料指標控制碼清單，然後初始化章節控制碼和書簽的清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="88b6c-4423">將此查詢中每個資料指標的章節控制碼清單初始化為 DB \_ Null \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="88b6c-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="88b6c-4424">將此查詢中每個資料指標的書簽控制碼清單，初始化為一組 DBBMK \_ FIRST 和 DBBMK \_ LAST。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="88b6c-4425">將查詢標示為未監視變更。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="88b6c-4426">將資料列的數目初始化為目前計算的資料列數目 (如果查詢無法開始執行，則可以是0，如果查詢是在執行) 的進程中，則為某個數位，然後初始化查詢完成的分子和分母。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="88b6c-4427">以 CPMCreateQueryOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="88b6c-4428">3.1.5.2.3 接收 CPMGetQueryStatusIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="88b6c-4429">當伺服器收到來自用戶端的 CPMGetQueryStatusIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4430">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="88b6c-4431">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4432">檢查游標控制碼是否位於用戶端的資料指標控制碼清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="88b6c-4433">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4434">準備 CPMGetQueryStatusOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="88b6c-4435">伺服器必須抓取目前的查詢狀態，並在 [QStatus] 欄位中設定它 (如需 \_ 可能的值) ，請參閱2.2.3.11。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="88b6c-4436">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="88b6c-4437">以 CPMGetQueryStatusOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="88b6c-4438">3.1.5.2.4 接收 CPMGetQueryStatusExIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="88b6c-4439">當伺服器收到來自用戶端的 CPMGetQueryStatusExIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4440">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4441">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4442">檢查傳遞的資料指標控制碼是否位於用戶端的資料指標控制碼清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="88b6c-4443">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4444">準備 CPMGetQueryStatusExOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="88b6c-4445">伺服器必須抓取目前的查詢狀態和查詢進度，並設定 QStatus (如需可能的值，請分別參閱 2.2.3.11) 、 \_ dwRatioFinishedDenominator 和 \_ dwRatioFinishedNumerator。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="88b6c-4446">然後，它必須將查詢結果中的資料列數目設定為 \_ cRowsTotal。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="88b6c-4447">如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4448">取得用戶端類別目錄的相關資訊，並填寫 \_ cFilteredDocuments 和 \_ cDocumentsToFilter。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="88b6c-4449">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4450">取出 bmk 欄位中的控制碼所指定之書簽的位置 \_ ，然後在 CPMGetQueryStatusExOut 訊息中填滿其餘的 \_ iRowBmk 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="88b6c-4451">如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4452">以 CPMGetQueryStatusExOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="88b6c-4453">3.1.5.2.5 接收 CPMRatioFinishedIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="88b6c-4454">當伺服器收到來自用戶端的 CPMRatioFinishedIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4455">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="88b6c-4456">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4457">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="88b6c-4458">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4459">準備 CPMRatioFinishedOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="88b6c-4460">伺服器必須抓取用戶端的查詢狀態，並填寫 \_ ulNumerator、 \_ ulDenominator 和 \_ >crows 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="88b6c-4461">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4462">如果 \_ >crows 等於此查詢最後報告的資料列數目，請將 \_ fNewRows 設定為0x00000000，否則請將其設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="88b6c-4463">將此查詢最後報告的資料列數更新為 >crows 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="88b6c-4464">以 CPMRatioFinishedOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="88b6c-4465">3.1.5.2.6 接收 CPMSetBindingsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="88b6c-4466">當伺服器收到來自用戶端的 CPMSetBindingsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4467">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4468">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4469">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="88b6c-4470">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4471">確認系結資訊有效 (亦即，資料行至少指定要傳回的值、長度或狀態;值、長度或狀態的系結中沒有重迭以及符合指定之資料列大小的值、長度和狀態) 以及如果未報告 DB \_ E \_ BADBINDINFO (0x80040E08) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="88b6c-4472">儲存與 aColumns 欄位中指定之資料行相關聯的系結資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="88b6c-4473">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4474">使用訊息標頭來回應用戶端 (只) \_ 將 msg 設定為 CPMSetBindingsIn，並 \_ 將狀態設定為指定之系結的結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="88b6c-4475">3.1.5.2.7 接收 CPMGetRowsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="88b6c-4476">當伺服器收到來自用戶端的 CPMGetRowsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4477">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="88b6c-4478">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4479">檢查傳遞的資料指標控制碼是否在用戶端資料指標控制碼的 athelist 中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="88b6c-4480">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4481">檢查用戶端是否有一組目前的系結。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="88b6c-4482">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4483">準備 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="88b6c-4484">伺服器必須將游標放在查詢結果中，如搜尋描述所指示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="88b6c-4485">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4486">提取最適合緩衝區的資料列數目，其大小會以 \_ cbReadBuffer 表示，但不能超過 cRowsToTransfer 的指示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="88b6c-4487">提取資料列時，伺服器必須將每個選取的資料行的屬性值類型，與用戶端目前的系結集合中指定的型別進行比較 (區段 3.1.1) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="88b6c-4488">如果系結中的型別不是 VT \_ 變異，伺服器必須嘗試將資料行的屬性值轉換為該型別。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="88b6c-4489">否則，如果在 \_ 用戶端的 DBPROPSET QUERYEXT 屬性集中設定 DBPROP USEEXTENDEDDBTYPES 旗標 \_ ，或如果資料行的屬性值不是 VT \_ 向量類型，則必須以其一般型別傳回屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="88b6c-4490">如果這兩種情況都沒有 (也就是伺服器有 VT \_ 向量類型，而用戶端不支援 vt \_ 向量) ，則伺服器必須嘗試將它轉換成 vt 陣列類型，如下所示 \_ ： VT \_ I8、vt \_ UI8、vt \_ FILETIME 和 vt \_ CLSID 陣列元素無法轉換，而是無法轉換;VT \_ LPSTR 和 vt \_ LPWSTR 陣列元素必須轉換成 vt \_ BSTR; 所有其他類型的陣列元素都必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="88b6c-4491">最後，如果資料列資料行包含章節控制碼或書簽控點，則伺服器必須更新對應的清單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="88b6c-4492">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="88b6c-4493">儲存 cRowsReturned 中提取的實際資料列數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="88b6c-4494">將 [搜尋描述] 和 [章節] 欄位從 CPMGetRowsIn 複製到要傳送的 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="88b6c-4495">在 [資料列] 欄位中儲存提取的資料列 (請參閱下方的 [狀態位元組] 和 [資料列的結構] 欄位) 的 [2.2.3.16] 區段。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="88b6c-4496">以 CPMGetRowsOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="88b6c-4497">[狀態位元組] 欄位上的附注：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4497">Note on status byte field:</span></span>

<span data-ttu-id="88b6c-4498">如果資料行的 CPMSetBindingIn 訊息 CTableColumn 中的 StatusUsed 設定為0x01，則伺服器必須將從這個資料行的資料列開頭) 的狀態位元組 (設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="88b6c-4499">值</span><span class="sxs-lookup"><span data-stu-id="88b6c-4499">Value</span></span> | <span data-ttu-id="88b6c-4500">意義</span><span class="sxs-lookup"><span data-stu-id="88b6c-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="88b6c-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="88b6c-4501">0x00</span></span>  | <span data-ttu-id="88b6c-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="88b6c-4502">StatusOK</span></span>       |
| <span data-ttu-id="88b6c-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="88b6c-4503">0x01</span></span>  | <span data-ttu-id="88b6c-4504">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="88b6c-4504">StatusDeferred</span></span> |
| <span data-ttu-id="88b6c-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="88b6c-4505">0x02</span></span>  | <span data-ttu-id="88b6c-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="88b6c-4506">StatusNull</span></span>     |



 

<span data-ttu-id="88b6c-4507">如果此資料列的屬性值不存在，伺服器必須將狀態位元組設定為 StatusNull。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="88b6c-4508">如果值太大而無法在 CPMGetRowsOut 訊息中傳送，伺服器必須將狀態位元組設定為 StatusDeferred。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="88b6c-4509">否則伺服器必須將狀態位元組設為 StatusOK。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="88b6c-4510">3.1.5.2.8 接收 CPMFetchValueIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="88b6c-4511">當伺服器收到來自用戶端的 CPMFetchValueIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4512">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="88b6c-4513">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4514">準備 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="88b6c-4515">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="88b6c-4516">尋找 wid 欄位所指出的檔 \_ ，並檢查此檔的屬性識別碼 (稍後稱為「屬性值」，此用戶端可以使用 PropSpec 結構所指出的「屬性值」 ) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="88b6c-4517">如果無法使用此值，伺服器必須將 \_ fValueExists 設定為0x00000000，否則請將 \_ fValueExists 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="88b6c-4518">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="88b6c-4519">如果 \_ fValueExists 等於0x00000001，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="88b6c-4520">將屬性值序列化為 SERIALIZEDPROPERTYVALUE 結構，並從 cbSoFar 位移開始複製（ \_ 最多 \_ cbChunk 個位元組） (但不超過序列化屬性) 到 vValue 欄位的結尾。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="88b6c-4521">如果此步驟因為任何原因而失敗，伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="88b6c-4522">將 \_ cbValue 設定為上一個步驟中複製的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="88b6c-4523">將 vType 設定為屬性值的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="88b6c-4524">如果序列化屬性的長度大於 \_ cbSoFar 新增至 \_ cbValue，則將 \_ fMoreExists 設定為0x00000001，否則請將其設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="88b6c-4525">以 CPMFetchValueOut 訊息回應用戶端</span><span class="sxs-lookup"><span data-stu-id="88b6c-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="88b6c-4526">3.1.5.2.9 接收 CPMGetNotify 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="88b6c-4527">當伺服器收到來自用戶端的 CPMGetNotify 訊息時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4528">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="88b6c-4529">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4530">如果自這個用戶端的最後一個 CPMSendNotifyOut 訊息之後，查詢結果集內沒有任何變更，或者查詢目前未監視結果集內的變更，則伺服器必須回應 CPMGetNotify 訊息，並開始監視查詢結果集的變更。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="88b6c-4531">如果稍後在查詢結果集中有變更，伺服器必須只傳送一個 CPMSendNotifyOut 訊息給用戶端，而且必須在 [watchNotify] 欄位中指定變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="88b6c-4532">如果自上次 CPMSendNotifyOut 訊息之後，查詢結果集的變更，伺服器必須以 CPMSendNotifyOut 回復，而且必須在 [watchNotify] 欄位中指定變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="88b6c-4533">請注意，在查詢結果的許多變更時，DBWATCHNOTIFY \_ ROWSCHANGED 會採用優先權 (也就是，如果查詢已完成、重新執行，然後變更資料列的數目，然後再次執行查詢，則回報的事件會是 DBWATCHNOTIFY \_ ROWSCHANGED) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="88b6c-4534">3.1.5.2.10 接收 CPMGetApproximatePositionIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="88b6c-4535">當伺服器收到來自用戶端的 CPMGetApproximatePositionIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4536">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4537">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4538">檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="88b6c-4539">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4540">在查詢結果中尋找與書簽控制碼相關聯的資料列，並估計資料列集中的資料列位置（由章節控點參考），並決定該位置的分子和分母。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="88b6c-4541">請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="88b6c-4542">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="88b6c-4543">以 CPMFetchValueOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="88b6c-4544">3.1.5.2.11 接收 CPMCompareBmkIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="88b6c-4545">當伺服器收到來自用戶端的 CPMCompareBmkIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4546">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4547">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4548">檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="88b6c-4549">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4550">準備 CPMCompareBmkOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="88b6c-4551">如果書簽控制碼相等，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ EQ。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="88b6c-4552">否則，如果其中一個書簽控制碼是 DBBMK \_ FIRST 或 DBBMK \_ LAST，則 \_ dwComparison 必須設定為 DBCOMPARE \_ NE。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="88b6c-4553">否則伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="88b6c-4554">尋找查詢結果中每個書簽控制碼所參考的資料列</span><span class="sxs-lookup"><span data-stu-id="88b6c-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="88b6c-4555">如果有任何一個資料列不在 CPMCompareBmkIn 的章節控制碼所指示的章節中，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ NOTCOMPARABLE。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="88b6c-4556">否則，當兩個數據列都位於相同的章節時，伺服器必須近似于本章節的控制碼所參考的資料列集中的資料列位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="88b6c-4557">然後，如果第一個資料列的位置小於第二個數據列的位置，則它必須比較位置值，並將 \_ dwComparison 設定為 DBCOMPARE \_ LT; 否則 \_ dwComparison 必須設定為 DBCOMPARE \_ GT。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="88b6c-4558">使用已填滿的 CPMCompareBmkOut 訊息來回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="88b6c-4559">3.1.5.2.12 接收 CPMRestartPositionIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="88b6c-4560">當伺服器收到來自用戶端的 CPMRestartPositionIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4561">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4562">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4563">檢查游標控制碼和傳遞的章節控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="88b6c-4564">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4565">將游標移至章節的開頭，以章節控點來識別。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="88b6c-4566">請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="88b6c-4567">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="88b6c-4568">以 CPMRestartPositionIn 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="88b6c-4569">3.1.5.2.13 接收 CPMFreeCursorIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="88b6c-4570">當伺服器收到來自用戶端的 CPMFreeCursorIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4571">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="88b6c-4572">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="88b6c-4573">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="88b6c-4574">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="88b6c-4575">釋出資料指標和相關聯的資源 (如需此資料指標控制碼的完整清單) ，請參閱3.1.1 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="88b6c-4576">從該用戶端的資料指標清單中移除資料指標。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="88b6c-4577">以 CPMFreeCursorOut 訊息回應， \_ 並以剩餘的資料指標數目設定 cCursorsRemaining 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="88b6c-4578">在此用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4578">in this client's list.</span></span>
-   <span data-ttu-id="88b6c-4579">如果此用戶端沒有其他資料指標，則伺服器必須釋放查詢和相關聯的資源 (請參閱 3.1.1) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="88b6c-4580">3.1.5.2.14 接收 CPMDisconnect 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="88b6c-4581">當伺服器收到來自用戶端的 CPMDisconnect 訊息要求時，伺服器必須從連線的用戶端清單中移除用戶端，並釋放與用戶端相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="88b6c-4582">3.1.6 計時器事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="88b6c-4583">無。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="88b6c-4584">3.1.7 其他本機事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="88b6c-4585">當伺服器停止時，它必須先轉換成「正在關機」狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="88b6c-4586">然後，它必須停止接聽管道、執行任何其他執行特定的關機工作，然後轉換成「已停止」狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="88b6c-4587">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="88b6c-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="88b6c-4588">3.2.1 抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="88b6c-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="88b6c-4589">下一節會指定內容索引服務通訊協定用戶端所維護的資料和狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="88b6c-4590">提供的資料是為了促進通訊協定運作方式的說明。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="88b6c-4591">本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="88b6c-4592">用戶端具有下列抽象狀態：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="88b6c-4593">**最後傳送的訊息**：最後傳送至伺服器的訊息複本。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="88b6c-4594">**目前的屬性值**：「已延後」屬性的部分值，此為正在抓取的進程中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="88b6c-4595">**目前接收的位元組** 數：目前為止針對目前屬性值所接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="88b6c-4596">**具名管道連接狀態**：與伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="88b6c-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="88b6c-4597">3.2.2 計時器</span><span class="sxs-lookup"><span data-stu-id="88b6c-4597">3.2.2 Timers</span></span>

<span data-ttu-id="88b6c-4598">不需要任何通訊協定計時器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="88b6c-4599">3.2.3 初始化</span><span class="sxs-lookup"><span data-stu-id="88b6c-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="88b6c-4600">在收到較高層級的要求之前，不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="88b6c-4601">3.2.4 Higher-Layer 觸發的事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="88b6c-4602">從較高的層收到要求時，用戶端必須使用2.1 節中指定的詳細資料，建立與伺服器的具名管道連接。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="88b6c-4603">如果無法這麼做，則更高的層級要求必須失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="88b6c-4604">亦即，如果連線失敗，則需要較高層級的責任才能重試。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="88b6c-4605">標頭必須預先暫止，並設定為從2.2.2 節中指定的欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="88b6c-4606">如果是指定為需要非零總和檢查碼的訊息，則 \_ 必須計算 ulChecksum 值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="88b6c-4607">訊息 \_ 標頭中的 ulReserved2 欄位之後的訊息內容必須解釋為32位整數的序列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="88b6c-4608">用戶端必須計算這些整數所指定之數值的總和。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="88b6c-4609">使用0x59533959 計算此值的位 XOR。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="88b6c-4610">\_從位 XOR 產生的值減去 msg 提供的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="88b6c-4611">3.2.4.1 遠端索引服務目錄管理</span><span class="sxs-lookup"><span data-stu-id="88b6c-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="88b6c-4612">每個訊息都是由較高層的要求所觸發。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="88b6c-4613">用戶端不會針對遠端系統管理目錄的 CISP 訊息要求強制執行訊息順序，但是 (除了 CPMSetCatStateIn) 訊息之外，伺服器只會在用戶端先前透過 CPMConnectIn 訊息連接時才回復成功。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="88b6c-4614">3.2.4.1.1 傳送 CPMCiStateInOut 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="88b6c-4615">一般而言，較高的層級會要求通訊協定用戶端在需要伺服器上索引服務的相關資訊時，傳送 CPMCiStateInOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="88b6c-4616">當要求傳送此訊息時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4617">將區段2.2.3.1 中指定的 CPMCiStateInOut 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="88b6c-4618">等候接收來自伺服器的 CPMCiStateInOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4619">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則會將資訊結構傳回至較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="88b6c-4620">3.2.4.1.2 傳送 CPMSetCatStateIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="88b6c-4621">一般而言，較高的層級會要求通訊協定用戶端在需要類別目錄或所有目錄的資訊時傳送 CPMSetCatStateIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="88b6c-4622">在此訊息中，較高層必須為通訊協定用戶端提供 dwNewState 的值， \_ 並視需要提供類別目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="88b6c-4623">當要求傳送此訊息時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4624">將2.2.3.2 中所指定的 CPMSetCatStateIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="88b6c-4625">等候接收來自伺服器的 CPMSetCatStateOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4626">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ dwOldState 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="88b6c-4627">3.2.4.1.3 傳送 CPMUpdateDocumentsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="88b6c-4628">如果需要在現有的路徑中更新檔，或將新的檔案路徑加入至索引，則較高的層通常會要求傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="88b6c-4629">因此，較高的層級是提供掃描的路徑和類型，其指定方式是在2.2.3.4 的區段中指定，其中增量或完整更新適用于現有的路徑，而新的初始化則適用于新的路徑。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="88b6c-4630">為了提供更高的層級要求，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4631">將區段2.2.3.4 中指定的 CPMUpdateDocumentsIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="88b6c-4632">等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4633">將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="88b6c-4634">3.2.4.1.4 傳送 CPMForceMergeIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="88b6c-4635">一般來說，如果需要改善查詢效能，或是已排程的索引服務維護，則傳送此訊息的層級要求越高。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="88b6c-4636">為了提供更高層級的服務，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4637">依區段2.2.3.5 的指定將 CPMForceMergeIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="88b6c-4638">等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4639">將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="88b6c-4640">3.2.4.2 遠端索引服務目錄查詢訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="88b6c-4641">除了 CPMGetRowsIn/CPMGetRowsOut、CPMFetchValueIn/CPMFetchValueOut，CISP 訊息和更高層級的要求之間有一對一的關聯性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="88b6c-4642">針對上述兩個例外狀況，用戶端可能會產生多個訊息來滿足大小需求，或取得完整的屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="88b6c-4643">較高層級通常會追蹤所有查詢特定的資訊 (例如開啟的資料指標控制碼、書簽和章節控制碼的合法值、延遲屬性值的 wid 值等等 ) ，也會追蹤用戶端是否處於連接狀態，但不會由用戶端以任何方式強制執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="88b6c-4644">為了方便說明，第3節中的圖表用戶端部分會說明這種簡單的索引服務查詢順序。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="88b6c-4645">3.2.4.2.1 傳送 CPMConnectIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="88b6c-4646">這則訊息通常是較高層級的第一個要求 (如同用戶端未連線一樣，伺服器將會失敗大部分的訊息，但 CPMSetCatStateIn) 除外。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="88b6c-4647">較高層級會為通訊協定用戶端提供連接所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="88b6c-4648">為了提供更高的層級，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4649">填寫訊息，使用更高層級用戶端所提供的資訊 (請參閱 \_ iClientVersion、MachineName、UserName、PropertySet1、PropertySet2 和 aPropertySet 中的 2.2.3.6) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="88b6c-4650">設定 \_ fClientIsRemote、 \_ cbBlob、 \_ cbBlob2、cPropSet 和 cExtPropSet，如2.2.3.6 中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="88b6c-4651">在 [ulChecksum] 欄位中設定總和檢查碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="88b6c-4652">將 CPMConnectIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="88b6c-4653">等候接收來自伺服器的 CPMConnectOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4654">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ serverVersion 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="88b6c-4655">基於資訊的目的，較高層級通常會在連接成功時執行下列動作，但 CISP 用戶端不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="88b6c-4656">使用遠端索引服務目錄管理訊息進行系統管理工作</span><span class="sxs-lookup"><span data-stu-id="88b6c-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="88b6c-4657">使用 CPMCreateQueryIn 要求建立搜尋查詢，其目的是要從目錄中抓取結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="88b6c-4658">3.2.4.2.2 傳送 CPMCreateQueryIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="88b6c-4659">當通訊協定用戶端連線之後，較高層級通常會提供查詢建立的資訊。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="88b6c-4660">較高的層級會為用戶端提供限制設定、資料行集、排序次序規則和分類集 (可以省略) 、資料列集屬性和屬性識別碼對應程式結構。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="88b6c-4661">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4662">準備 CPMCreateQueryOut，如下所示。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="88b6c-4663">如果有資料行集存在，請將 CColumnsSetPreset 設定為0x01 並填滿 ColumnsSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="88b6c-4664">如果有限制，請將 CRestrictionPresent 設定為0x01 並填滿限制欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="88b6c-4665">如果有排序集存在，請填入 SortSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="88b6c-4666">如果有分類集存在，請將 CSortSetPresent 設定為0x01 並填滿 CategorizationSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="88b6c-4667">設定2.2.3.8 中指定的剩餘欄位</span><span class="sxs-lookup"><span data-stu-id="88b6c-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="88b6c-4668">計算 \_ 標頭中的 ulCheckSum 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="88b6c-4669">將 CPMCreateQueryIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="88b6c-4670">等候接收 CPMCreateQueryOut 訊息 (請參閱3.2.5.1.1 一節中的詳細資料) ，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="88b6c-4671">報告回應的 [狀態] 欄位的值， \_ 如果成功，則會將資料指標控制碼的陣列和資訊性布林值 (指定在 2.2.3.9) 回到較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="88b6c-4672">3.2.4.2.3 傳送 CPMSetBindingsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="88b6c-4673">一般來說， (當資料列已成功接收 CPMCreateQueryOut 之後，資料列中的每個資料行的系結將會被傳回，請參閱 3.2.5.1.1) 一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="88b6c-4674">較高的預期會提供 CTableColumn 結構的陣列，如2.2.4.31 中所指定的 aColumns 欄位和有效的資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="88b6c-4675">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4676">計算 aColumns 陣列中的 CTableColumn 結構數目，並將 cColumns 欄位設定為此值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="88b6c-4677">計算 cColumns 和 aColumns 欄位的總大小（以位元組為單位），並將 \_ cbBindingDesc 欄位設定為此值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="88b6c-4678">在 CPMSetBindingsIn 訊息中，將指定的欄位設定為較高的應用層所提供的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="88b6c-4679">將 [ \_ ulChecksum] 欄位設定為 [3.2.5] 區段中所指定的計算值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="88b6c-4680">將已完成的 CPMSetBindignsIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="88b6c-4681">等候接收來自伺服器的 CPMSetBindingsIn 訊息，並捨棄其他訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="88b6c-4682">從回應的 [狀態] 欄位中，指出 \_ 對較高層的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="88b6c-4683">基於資訊的目的，較高層級通常會要求用戶端傳送 CPMGetRowsIn 訊息，但不會由內容編制索引服務通訊協定強制執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="88b6c-4684">3.2.4.2.4 傳送 CPMGetRowsIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="88b6c-4685">當較高的層級即將接收資料列資訊時，它會提供具有有效資料指標和章節控制碼的通訊協定用戶端，並提供適當的搜尋描述。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="88b6c-4686">一般來說，當它有有效的資料指標和/或章節控制碼，且系結已設定了 CPMSetBindingsIn 訊息時，就會需要較高層級的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="88b6c-4687">若要存取章節中的資料列集，較高的層級是在先前的 CPMGetRowsOut 訊息中使用從伺服器收到的章節控制碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="88b6c-4688">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4689">判斷要為 cbReadBuffer 欄位指定的不帶正負號的整數值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="88b6c-4690">若要判斷此值，用戶端必須採用下列值的最大值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="88b6c-4691">C RowsToTransfer 欄位值的1000倍 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="88b6c-4692">CbRowWidth 的值 \_ ，進位至最接近的512位元組倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="88b6c-4693">將這兩個值的較高，最多可達16K 限制。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="88b6c-4694">在單一資料列大於16K 的情況下，伺服器無法將結果傳回此查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="88b6c-4695">在 ulClientBase 欄位的用戶端位址空間中，為可變大小的資料列資料指定用戶端基底 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="88b6c-4696">*Windows 行為：對於與32位伺服器通訊的32位用戶端，或與64位伺服器通訊的64位用戶端，此值會設定為應用程式進程中接收緩衝區的記憶體位址。這允許在用戶端應用程式進程中，以 CPMGetRowsOut 的資料欄欄位中收到的指標為正確的記憶體指標。否則，它會設定為0x00000000。*</span><span class="sxs-lookup"><span data-stu-id="88b6c-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="88b6c-4697">計算 [搜尋描述] 的大小，並在 [cbSeek] 欄位中進行設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="88b6c-4698">設定 cbReserved (的值，此值會作為資料列的位移開始) \_ cbSeek plus 0x14 的值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="88b6c-4699">將2.2.3.15 中所指定的 CPMConnectIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="88b6c-4700">3.2.4.2.5 傳送 CPMFetchValueIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="88b6c-4701">如果用戶端收到來自伺服器的 CPMGetRowsOut 回應，且資料行的 Status 欄位設定為 StatusDeferred (0x01) 這表示屬性值未包含在 CPMGetRowsOut 訊息的 Rows 欄位中。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="88b6c-4702">在此情況下，較高層級通常會要求通訊協定用戶端透過 CPMFetchValueIn 訊息來取得值，並提供延遲屬性的 PropSpec 和 \_ wid 值（通訊協定用戶端必須在第一個 CPMFetchValueIn 訊息中使用）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="88b6c-4703">如果這是用戶端傳送的第一個 CPMFetchValueIn 訊息，要求指定的屬性，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4704">設定訊息中的所有欄位，如2.2.3.19 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="88b6c-4705">將 \_ cbSoFar 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="88b6c-4706">將接收的目前位元組設定為0。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="88b6c-4707">將 CPMFetchValueIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="88b6c-4708">3.2.4.2.6 傳送 CPMFreeCursorIn 要求</span><span class="sxs-lookup"><span data-stu-id="88b6c-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="88b6c-4709">一旦較高層級不再使用搜尋查詢，它就可以要求用戶端傳送 CPMFreeCursorIn 訊息，以釋放伺服器上的資源。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="88b6c-4710">收到此要求時，用戶端必須將2.2.3.28 中所指定的 CPMFreeCursorIn 訊息傳送至伺服器，其中包含上層所指定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="88b6c-4711">3.2.4.2.7 傳送 CPMDisconnect 訊息</span><span class="sxs-lookup"><span data-stu-id="88b6c-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="88b6c-4712">如果較高層級的索引服務沒有其他查詢，則若要釋出更多伺服器資源，應用程式可能會要求用戶端將 CPMDisconnect 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="88b6c-4713">收到此查詢時，用戶端必須直接以要求的方式傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="88b6c-4714">伺服器不會回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="88b6c-4715">3.2.5 訊息處理和排序規則</span><span class="sxs-lookup"><span data-stu-id="88b6c-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="88b6c-4716">當用戶端收到來自伺服器的訊息回應時，用戶端必須使用最後傳送的訊息，判斷從伺服器接收的訊息是否為用戶端所預期的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="88b6c-4717">與 \_ [msg] 欄位不同的所有訊息都必須被忽略。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="88b6c-4718">3.2.5.1 接收 CPMCreateQueryOut 回應</span><span class="sxs-lookup"><span data-stu-id="88b6c-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="88b6c-4719">當用戶端收到來自伺服器的 CPMCreateQueryOut 訊息回應時，用戶端必須 \_ 傳回狀態 (，而且如果狀態成功) 資料指標控制碼值傳回至較高的層級，用戶端就必須傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="88b6c-4720">任何進一步的動作都是最高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="88b6c-4721">因為較高的層級知道查詢結構，所以一定會在 CPMCreateOueryOut 訊息中傳回正確的資料指標控制碼數目。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="88b6c-4722">資料指標控制碼會以下列順序傳回：第一個控制碼是 unchaptered 資料列集，第二個控制碼是第一個章節的資料列集 (這是根據 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中指定的第一個類別的結果群組。 ) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="88b6c-4723">基於資訊的目的，較高層級必須執行下列動作，但 CISP 用戶端並不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="88b6c-4724">使用 CPMSetBindingsIn 來設定個別資料行的系結，並對查詢路徑執行任何後續的動作</span><span class="sxs-lookup"><span data-stu-id="88b6c-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="88b6c-4725">使用 CPMGetQueryStatusIn 來檢查查詢的執行進度。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="88b6c-4726">使用 CPMRatioFinishedIn 來要求查詢的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="88b6c-4727">3.2.5.2 接收 CPMGetRowsOut 回應</span><span class="sxs-lookup"><span data-stu-id="88b6c-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="88b6c-4728">當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4729">檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="88b6c-4730">如果 \_ status 值為 status \_ 緩衝區 \_ 太 \_ 小 (0xC0000023) ，用戶端必須檢查最後一個訊息傳送狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="88b6c-4731">如果未包含 CPMGetRowsIn 訊息，則必須以無訊息方式忽略接收的訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="88b6c-4732">否則，用戶端必須將新的 CPMGetRowsIn 訊息傳送至伺服器，其中所有欄位都與儲存的欄位相同，不同之處在于 \_ CBREADBUFFER 必須增加 512 (但不能大於 0x4000) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="88b6c-4733">如果 \_ 狀態 \_ 緩衝區 \_ 太 \_ 小 (0XC0000023) ，而且最後傳送的訊息已 \_ cbReadBuffer 等於0X4000 用戶端，則必須將錯誤回報到較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="88b6c-4734">如果 \_ 狀態值為任何其他錯誤值，用戶端必須指出最高層級的失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="88b6c-4735">如果 \_ 狀態值表示成功，則結果必須指出最高的層級要求資訊，而進一步的動作則是最高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="88b6c-4736">基於資訊的目的，較高層級通常會執行下列動作，但內容索引服務通訊協定用戶端不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="88b6c-4737">如果資料列中的值代表檔識別碼、章節或書簽控點，則較高層通常會儲存它們，以便在牽涉到有效檔識別碼、章節或書簽控制碼的後續作業中使用。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="88b6c-4738">較高的圖層通常會儲存或顯示資料，或以其他方式使用資料行值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="88b6c-4739">針對標示為 [延後] 較高層的值，將會使用 CPMFetchValueIn 訊息來提取值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="88b6c-4740">搜尋描述也會傳回至較高的層級，而且可以由較高的圖層重複使用或檢查。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="88b6c-4741">基於資訊的目的，如果較高層要求的控制碼是在資料列中收到的章節和書簽，則可能會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="88b6c-4742">使用 CPMGetQueryStatusExIn 來檢查查詢的執行進度，以及其他狀態資訊，例如已篩選的檔數目、要篩選的檔、查詢所處理的檔比例、查詢中的資料列總數，以及書簽在資料列集中的位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="88b6c-4743">使用 CPMGetNotify 來要求伺服器通知資料列集變更的用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="88b6c-4744">使用 CPMGetApproximatePositionIn，在章節中要求書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="88b6c-4745">使用 CPMCompareBmkIn 來要求一章中兩個書簽的比較。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="88b6c-4746">使用 CPMRestartPositionIn 將資料指標的位置變更為資料列集的開頭。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="88b6c-4747">3.2.5.3 接收 CPMFetchValueOut 回應</span><span class="sxs-lookup"><span data-stu-id="88b6c-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="88b6c-4748">當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="88b6c-4749">檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="88b6c-4750">在失敗案例中，請通知較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="88b6c-4751">否則，請繼續下一節。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="88b6c-4752">檢查 \_ fValueExist，如果設定為0x00000000，則會通知較高的圖層，指出找不到此值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="88b6c-4753">否則 \_ ，請將 cbValue 的位元組從 vValue 附加至目前的屬性值。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="88b6c-4754">如果 \_ \_ fMoreExists 設定為0x00000001，然後將 \_ cbValue 所接收的目前位元組遞增， \_ 並將 CPMFetchValueIn 訊息傳送至伺服器，請將 \_ cbSoFar 設定為目前接收的位元組值， \_ cbPropSpec 為零，而 \_ cbChunk 為較高層所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="88b6c-4755">如果 \_ fMoreExists 設定為0x00000000，則會將目前屬性值的屬性值指定為較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="88b6c-4756">3.2.5.4 接收 CPMFreeCursorOut 回應</span><span class="sxs-lookup"><span data-stu-id="88b6c-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="88b6c-4757">當用戶端從伺服器收到成功的 CPMFreeCursorOut 訊息回應時，用戶端必須將 \_ cCursorsRemaining 值傳回至較高的層級。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="88b6c-4758">下列資訊僅供參考之用，不會由 CISP 用戶端強制執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="88b6c-4759">較高的層級預期會追蹤資料指標控制碼，而不是使用已釋放的資料指標。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="88b6c-4760">一旦 cCursorsRemaining 的數目 \_ 等於0x00000000，較高的層級就可以使用此連接來指定另一個查詢 (使用 CPMCreateQueryIn 訊息) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="88b6c-4761">3.2.6 計時器事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="88b6c-4762">無。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="88b6c-4763">3.2.7 其他本機事件</span><span class="sxs-lookup"><span data-stu-id="88b6c-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="88b6c-4764">無。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="88b6c-4765">4 通訊協定範例</span><span class="sxs-lookup"><span data-stu-id="88b6c-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="88b6c-4766">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="88b6c-4767">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="88b6c-4768">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="88b6c-4768">4.1 Example 1</span></span>

<span data-ttu-id="88b6c-4769">在下列範例中，我們假設電腦 A 上的使用者 JOHN 想要從儲存在伺服器 X 上的檔集的目錄系統中，取得包含 "Microsoft" 這個字的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="88b6c-4770">讓我們假設電腦 A 正在執行32位的 Windows XP 作業系統，而電腦 X 正在執行32位的 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="88b6c-4771">使用者啟動搜尋應用程式，並輸入搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="88b6c-4772">接著，應用程式會將搜尋查詢傳遞給通訊協定用戶端。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="88b6c-4773">通訊協定用戶端建立與索引伺服器 X 的連接。通訊協定用戶端使用具名管道 \\ 管道 \\ CI \_ SKADS，透過 SMB 連線到伺服器 X。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="88b6c-4774">然後，通訊協定用戶端會使用下列值來準備 CPMConnectIn 訊息：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="88b6c-4775">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4776">**\_ msg** 設定為0x000000C8，表示這是 CPMConnectIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="88b6c-4777">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4778">**\_ ulChecksum** 包含總和檢查碼，依3.2.4 區段中的指定進行計算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="88b6c-4779">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="88b6c-4780">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4781">**\_ iClientVersion** 設定為0x00000008，表示伺服器要驗證總和檢查碼欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="88b6c-4782">**\_ fClientIsRemote** 設定為0x00000001，表示伺服器是遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="88b6c-4783">**\_ cbBlob1** 會設定為結合 cPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="88b6c-4784">**\_ cbBlob2** 設定為 0x00000004 (表示沒有任何額外的屬性集) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="88b6c-4785">**MachineName** 設定為。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="88b6c-4786">**UserName** 設定為 JOHN。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="88b6c-4787">**cPropSets** 設定為0x00000002。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="88b6c-4788">**PropertySet1** 欄位的類型為 CDbPropSet。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="88b6c-4789">組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="88b6c-4790">**GuidPropSet** 欄位設定為 A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="88b6c-4791">**cProperties** 欄位設定為0x00000004。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="88b6c-4792">**aProps** 欄位是 CDbProp 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="88b6c-4793">針對 **aProps \[ 0 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="88b6c-4794">**PropId** 會設定為 0X00000002 (DBPROP \_ CI \_ 類別目錄 \_ 名稱) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="88b6c-4795">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="88b6c-4796">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4797">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="88b6c-4798">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="88b6c-4799">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="88b6c-4800">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4801">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="88b6c-4802">**vType** 設定為 0X001F (VT \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="88b6c-4803">**vValue** 會設定為 "SYSTEM"，也就是所需的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="88b6c-4804">針對 **aProps \[ 1 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="88b6c-4805">**PropId** 設定為 0X00000007 (DBPROP \_ CI \_ 查詢 \_ 類型) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="88b6c-4806">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="88b6c-4807">**DBPROPSTATUS** 是設定為 to0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4808">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="88b6c-4809">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="88b6c-4810">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="88b6c-4811">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4812">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="88b6c-4813">**vType** 設定為 0X0003 (VT \_ I4) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="88b6c-4814">**vValue** 會設定為 0X00000000 (CiNormal) ，這表示它是一般查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="88b6c-4815">針對 **aProps \[ 2 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="88b6c-4816">**PropId** 會設定為 0X00000004 (DBPROP \_ CI \_ 範圍 \_ 旗標) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="88b6c-4817">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="88b6c-4818">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4819">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="88b6c-4820">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="88b6c-4821">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="88b6c-4822">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4823">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="88b6c-4824">**vType**： 0X1003 (VT \_ 向量 \| VT \_ I4) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="88b6c-4825">**vValue**： 0x00000001/0x00000001 (一個具有值 1) 的元素，這表示搜尋子資料夾</span><span class="sxs-lookup"><span data-stu-id="88b6c-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="88b6c-4826">針對 **aProps \[ 3 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="88b6c-4827">**PropId**： 0X00000003 (DBPROP \_ CI \_ 包含 \_ 範圍) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="88b6c-4828">**DBPROPOPTIONS**：0x0000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="88b6c-4829">**DBPROPSTATUS**：0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="88b6c-4830">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="88b6c-4831">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="88b6c-4832">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="88b6c-4833">**ulID** 設定為0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="88b6c-4834">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="88b6c-4835">**vType** 設定為 0X101F (VT \_ VECTOR \| vt \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="88b6c-4836">**vValue** 設定為 0x00000001/0x00000002/" \\ " (一個元素，其中有2個字元的 null 終止字串) ，亦即根範圍。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="88b6c-4837">**PropertySet2** 欄位的類型為 CDbPropSet。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="88b6c-4838">組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="88b6c-4839">**GuidPropSet** 設定為 AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="88b6c-4840">**cProperties** 欄位設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="88b6c-4841">**AProps** 欄位是 CDbProp 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="88b6c-4842">針對 **aProps \[ 0 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="88b6c-4843">**PropId** 會設定為 0X00000002 (DBPROP \_ 機) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="88b6c-4844">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="88b6c-4845">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4846">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="88b6c-4847">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) ，</span><span class="sxs-lookup"><span data-stu-id="88b6c-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="88b6c-4848">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="88b6c-4849">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4850">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="88b6c-4851">**vType**： 0X0008 (VT \_ BSTR) </span><span class="sxs-lookup"><span data-stu-id="88b6c-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="88b6c-4852">**vValue**： 0x04/"X" (4 個位元組/以 null 結束的 Unicode 字串) ，表示 "X"-伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="88b6c-4853">**cExtPropSet** 欄位設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4854">**aPropertySets** 陣列不存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="88b6c-4855">視需要填入各種填補欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="88b6c-4856">訊息會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="88b6c-4857">伺服器會驗證 **\_ ulChecksum** 是否正確、確認使用者已獲授權提出此要求，並以 CPMConnectOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="88b6c-4858">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4859">**\_ msg** 設定為0x000000C8，表示這是 CPMConnectOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="88b6c-4860">**\_ 狀態** 會設為0X0000000，表示成功。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="88b6c-4861">**\_ ulChecksum** 設定為0。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="88b6c-4862">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="88b6c-4863">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4864">**\_ serverVersion** 欄位設定為 0x00000007 (32 位 windows XP 或32位 windows Server 2003) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="88b6c-4865">**\_ 保留** 的欄位會填入任意資料。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="88b6c-4866">用戶端會準備 CPMCreateQueryIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="88b6c-4867">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4868">**\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="88b6c-4869">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4870">**\_ ulChecksum** 包含總和檢查碼，根據3.2.5 計算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="88b6c-4871">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="88b6c-4872">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4873">[**大小**] 欄位設定為訊息其餘部分的大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="88b6c-4874">**CColumnSetPresent** 欄位設定為0x01。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="88b6c-4875">**ColumnSet** 欄位的類型為 CColumnSet。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="88b6c-4876">組成此欄位的 CColumnSet 結構設定如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="88b6c-4877">**\_ count** 欄位設定為0x00000001，表示傳回一個資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="88b6c-4878">**索引** 陣列是0x00000000，表示 aPropSpec 中的第一個專案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="88b6c-4879">**CRestrictionPresent** 欄位設定為0x01，表示 **限制** 欄位存在。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="88b6c-4880">**限制** 欄位的類型為 CRestriction，且設定為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="88b6c-4881">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="88b6c-4882">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4883">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="88b6c-4884">PRSPEC 的屬性設定為 GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13，代表檔主體。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="88b6c-4885">**\_ Cc** 設為0x00000009。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="88b6c-4886">**\_ pwcsphrase** 會設定為字串 "Microsoft"。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="88b6c-4887">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="88b6c-4888">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="88b6c-4889">**CSortPresent** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="88b6c-4890">**CCategorizationSetPresent** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="88b6c-4891">**RowSetProperties** 的設定如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="88b6c-4892">**\_ uBooleanOptions** 會設定為 0x00000001 (順序) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="88b6c-4893">**\_ ulMaxOpenRows** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4894">**\_ ulMemoryUsage** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4895">\_**cMaxResults** 設定為 0x00000100 (最多傳回256個數據列) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="88b6c-4896">**\_ cCmdTimeOut** 設定為 0x00000000 (不會) 超時。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="88b6c-4897">**PidMapper** 設定為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="88b6c-4898">**\_ count** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="88b6c-4899">**\_ aPropSpec** 設定為 02608C9EEBAC \_ 的 GUID B725F130-47EF-101A-A5-F1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="88b6c-4900">伺服器會處理它，並以 CPMCreateQueryOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="88b6c-4901">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4902">**\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="88b6c-4903">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="88b6c-4904">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="88b6c-4905">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="88b6c-4906">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4907">**\_ fTrueSeqeuntial** 設定為0x00000000，表示查詢可以使用索引。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="88b6c-4908">**\_ fWorkIdUnique** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="88b6c-4909">**ACursors** 陣列只包含一個元素，代表這個查詢的資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="88b6c-4910">此值取決於伺服器的狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="88b6c-4911">讓我們假設傳回的值為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="88b6c-4912">用戶端發出 CPMSetBindingsIn 要求訊息來定義資料列的格式。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="88b6c-4913">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4914">**\_ msg** 設定為0x000000D0，表示這是 CPMSetBindingsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="88b6c-4915">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="88b6c-4916">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="88b6c-4917">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="88b6c-4918">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4919">**\_ hCursor** 設定為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="88b6c-4920">**\_ cbRow** 設定為 0x10 (夠大，足以容納) 的資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="88b6c-4921">**\_ cbBindingDesc** 會設定為結合的 **\_ cColumns** 和 **\_ aColumns** 欄位大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="88b6c-4922">**\_ cColumns** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="88b6c-4923">**\_ aColumns** 陣列設定為包含一個 CTableColumn 結構，其中包含：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="88b6c-4924">**\_ PropSpec** 設定為 02608c9eebac \_ 的 GUID b725f130-47ef-101a-a5-f1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="88b6c-4925">**\_ vType** 設定為 0x0015 (VT \_UI8) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="88b6c-4926">**\_ ValueUsed** 會設定為在資料列) 中傳輸的 0x01 (資料行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="88b6c-4927">**\_ ValueOffset** 會在資料列) 的開頭設定為 0x0002 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="88b6c-4928">**\_ ValueSize** 設定為 0x08 (VT \_ 的大小UI8) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="88b6c-4929">**\_ StatusUsed** 設定為0x01。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="88b6c-4930">**\_ StatusOffset** 設定為0x0A。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="88b6c-4931">**\_ LengthUsed** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="88b6c-4932">伺服器會處理它，並以 CPMSetBindingsIn 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="88b6c-4933">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4934">**\_ msg** 設定為0x000000D0。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="88b6c-4935">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="88b6c-4936">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="88b6c-4937">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="88b6c-4938">用戶端發出 CPMGetRowsIn 要求訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="88b6c-4939">讓我們假設用戶端已準備好接受100個數據列，而且想要以遞增的順序進行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="88b6c-4940">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4941">**\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="88b6c-4942">**\_ 狀態** 設定為0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b6c-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="88b6c-4943">**\_ ulChecksum** 包含總和檢查碼，依區段0計算。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="88b6c-4944">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="88b6c-4945">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4946">**\_ hCursor** 設定為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="88b6c-4947">**\_ cRowsToTransfer** 設定為0x00000064。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="88b6c-4948">從) 的系結中， **\_ cRowWidth** 設為 0x00000010 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="88b6c-4949">**\_ cbSeek** 會設定為0x14，也就是結合 eType、 \_ chapt 和 CRowSeekNext 欄位的大小。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="88b6c-4950">**\_ cbReserved** 設定為 0x18 (0x14 plus \_ cbSeek) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="88b6c-4951">**\_ cbReadBuffer** 設定為 0x800 (0x64 \* 0x10 進位到下一個 0x200) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="88b6c-4952">**\_ ulClientBase** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4953">**\_ fBwdfetch** 設定為0x00000000，表示資料列會以正向順序提取。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="88b6c-4954">**eType** 設定為0x0000001，表示用戶端需要下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="88b6c-4955">**\_ chapt** 設定為 0 (不是) 的章節化結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="88b6c-4956">**SeekDescription** 設定為 CRowSeekNext。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="88b6c-4957">CRowSeekNext 結構包含下列值：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="88b6c-4958">**CiTblChapt** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4959">**\_ hRegion** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4960">**\_ cSkip** 設定為0，表示用戶端不想略過資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="88b6c-4961">伺服器會處理它，並以 CPMGetRowsOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="88b6c-4962">讓我們假設伺服器找到的100檔中包含 "Microsoft" 這個字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="88b6c-4963">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4964">**\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="88b6c-4965">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="88b6c-4966">**\_ ulChecksum** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4967">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="88b6c-4968">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4969">**\_ CRowsReturned** 設定為0x00000064。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="88b6c-4970">**eType** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="88b6c-4971">**\_ chapt** 設定為 0x00000000 (不是) 的章節化結果。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="88b6c-4972">**SeekDescription** 包含 CRowSeekNext 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="88b6c-4973">**CiTblChapt** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4974">**\_ hRegion** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="88b6c-4975">**\_ cSkip** 設定為0，表示用戶端不想略過資料列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="88b6c-4976">資料 **列** 包含100檔的大小，其中包含 "Microsoft" 這個字。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="88b6c-4977">由於這是固定大小的資料，因此它只會以100、8位元組不帶正負號的整數的清單結構化。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="88b6c-4978">用戶端會傳送 CPMDisconnect 訊息來結束連接。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="88b6c-4979">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="88b6c-4980">**\_ msg** 設定為0x000000C9，表示這是 CPMDisconnect 訊息。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="88b6c-4981">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="88b6c-4982">**\_ ulChecksum** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="88b6c-4983">伺服器會處理訊息，並移除所有的用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="88b6c-4984">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="88b6c-4984">4.2 Example 2</span></span>

<span data-ttu-id="88b6c-4985">在上述範例中，查詢相當簡單。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="88b6c-4986">現在讓我們考慮稍微複雜一點的查詢。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="88b6c-4987">讓我們假設使用者想要取出包含下列兩個字的檔案大小： "Microsoft" 和 "Office"。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="88b6c-4988">這是藉由變更在步驟5中傳送的 CPMCreateQueryIn 訊息所包含的限制欄位來指定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="88b6c-4989">**限制** 欄位的類型為 CRestriction，且設定為：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="88b6c-4990">**\_ ulType** 設定為 0x00000004 (RTAnd) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="88b6c-4991">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="88b6c-4992">欄位的其餘部分包含 CNodeRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="88b6c-4993">**\_ cNode** 設定為0X00000002，表示 paNode 陣列中有兩個節點。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="88b6c-4994">**\_ PaNode** 欄位是兩個 CRestriction 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="88b6c-4995">**\_ paNode \[ 0 \]** 包含：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="88b6c-4996">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="88b6c-4997">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-4998">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="88b6c-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="88b6c-4999">PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。</span><span class="sxs-lookup"><span data-stu-id="88b6c-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="88b6c-5000">**\_ Cc** 設為0x00000009。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="88b6c-5001">**\_ pwcsphrase** 會設定為字串 "Microsoft"。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="88b6c-5002">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="88b6c-5003">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="88b6c-5004">**\_ paNode \[ 1 \]** 包含：</span><span class="sxs-lookup"><span data-stu-id="88b6c-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="88b6c-5005">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="88b6c-5006">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="88b6c-5007">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="88b6c-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="88b6c-5008">PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="88b6c-5009">**\_ Cc** 設為0x00000006。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="88b6c-5010">**\_ pwcsphrase** 會設定為 "Office" 字串。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="88b6c-5011">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="88b6c-5012">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="88b6c-5013">5 安全性</span><span class="sxs-lookup"><span data-stu-id="88b6c-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="88b6c-5014">5.1 實作者的安全性考量</span><span class="sxs-lookup"><span data-stu-id="88b6c-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="88b6c-5015">索引安全內容的索引編制可考慮使用 SMB Ms-chap 提供的使用者內容 \[ \] 來修剪搜尋結果，並且只傳回呼叫者可存取的內容。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="88b6c-5016">5.2 安全性參數的索引</span><span class="sxs-lookup"><span data-stu-id="88b6c-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="88b6c-5017">安全性參數</span><span class="sxs-lookup"><span data-stu-id="88b6c-5017">Security Parameter</span></span>  | <span data-ttu-id="88b6c-5018">區段</span><span class="sxs-lookup"><span data-stu-id="88b6c-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="88b6c-5019">模擬等級</span><span class="sxs-lookup"><span data-stu-id="88b6c-5019">Impersonation level</span></span> | <span data-ttu-id="88b6c-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="88b6c-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="88b6c-5021">6個版本特定行為的索引</span><span class="sxs-lookup"><span data-stu-id="88b6c-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="88b6c-5022">版本特定行為</span><span class="sxs-lookup"><span data-stu-id="88b6c-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="88b6c-5023">區段</span><span class="sxs-lookup"><span data-stu-id="88b6c-5023">Section</span></span>   | <span data-ttu-id="88b6c-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="88b6c-5024">Windows 2000</span></span> | <span data-ttu-id="88b6c-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="88b6c-5025">Windows XP</span></span> | <span data-ttu-id="88b6c-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88b6c-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="88b6c-5027">此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="88b6c-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="88b6c-5028">1.3.2</span></span>     | <span data-ttu-id="88b6c-5029">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5029">X</span></span>            | <span data-ttu-id="88b6c-5030">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5030">X</span></span>          | <span data-ttu-id="88b6c-5031">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5031">X</span></span>                   |
| <span data-ttu-id="88b6c-5032">應用程式通常會與 OLE DB 介面包裝函式互動</span><span class="sxs-lookup"><span data-stu-id="88b6c-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="88b6c-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="88b6c-5033">1.4</span></span>       | <span data-ttu-id="88b6c-5034">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5034">X</span></span>            | <span data-ttu-id="88b6c-5035">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5035">X</span></span>          | <span data-ttu-id="88b6c-5036">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5036">X</span></span>                   |
| <span data-ttu-id="88b6c-5037">NTSTATUS 值</span><span class="sxs-lookup"><span data-stu-id="88b6c-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="88b6c-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="88b6c-5038">1.8</span></span>       | <span data-ttu-id="88b6c-5039">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5039">X</span></span>            | <span data-ttu-id="88b6c-5040">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5040">X</span></span>          | <span data-ttu-id="88b6c-5041">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5041">X</span></span>                   |
| <span data-ttu-id="88b6c-5042">用戶端會 \_ 在每個訊息標頭中設定 [狀態] 欄位。</span><span class="sxs-lookup"><span data-stu-id="88b6c-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="88b6c-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="88b6c-5043">2.2.2</span></span>     | <span data-ttu-id="88b6c-5044">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5044">X</span></span>            | <span data-ttu-id="88b6c-5045">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5045">X</span></span>          | <span data-ttu-id="88b6c-5046">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5046">X</span></span>                   |
| <span data-ttu-id="88b6c-5047">cPendingScans 值通常是零</span><span class="sxs-lookup"><span data-stu-id="88b6c-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="88b6c-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="88b6c-5048">2.2.3.1</span></span>   | <span data-ttu-id="88b6c-5049">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5049">X</span></span>            | <span data-ttu-id="88b6c-5050">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5050">X</span></span>          | <span data-ttu-id="88b6c-5051">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5051">X</span></span>                   |
| <span data-ttu-id="88b6c-5052">iClientVersion 值</span><span class="sxs-lookup"><span data-stu-id="88b6c-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="88b6c-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="88b6c-5053">2.2.3.6</span></span>   | <span data-ttu-id="88b6c-5054">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5054">X</span></span>            | <span data-ttu-id="88b6c-5055">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5055">X</span></span>          | <span data-ttu-id="88b6c-5056">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5056">X</span></span>                   |
| <span data-ttu-id="88b6c-5057">\_cbChunk 值</span><span class="sxs-lookup"><span data-stu-id="88b6c-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="88b6c-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="88b6c-5058">2.2.3.19</span></span>  | <span data-ttu-id="88b6c-5059">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5059">X</span></span>            | <span data-ttu-id="88b6c-5060">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5060">X</span></span>          | <span data-ttu-id="88b6c-5061">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5061">X</span></span>                   |
| <span data-ttu-id="88b6c-5062">32位和64位的記憶體位址</span><span class="sxs-lookup"><span data-stu-id="88b6c-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="88b6c-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="88b6c-5063">3.2.4.2.4</span></span> | <span data-ttu-id="88b6c-5064">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5064">X</span></span>            | <span data-ttu-id="88b6c-5065">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5065">X</span></span>          | <span data-ttu-id="88b6c-5066">X</span><span class="sxs-lookup"><span data-stu-id="88b6c-5066">X</span></span>                   |



 

 

 






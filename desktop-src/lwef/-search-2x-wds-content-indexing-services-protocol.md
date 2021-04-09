---
title: 內容索引服務通訊協定
description: 本檔是內容索引服務通訊協定的規格。
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "103681589"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="36def-103">內容索引服務通訊協定</span><span class="sxs-lookup"><span data-stu-id="36def-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="36def-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="36def-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="36def-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="36def-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="36def-106">通訊協定規格，版本0.12</span><span class="sxs-lookup"><span data-stu-id="36def-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="36def-107">1簡介</span><span class="sxs-lookup"><span data-stu-id="36def-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="36def-108">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="36def-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="36def-109">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="36def-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="36def-110">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="36def-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="36def-111">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="36def-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="36def-112">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="36def-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="36def-113">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="36def-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="36def-114">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="36def-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="36def-115">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="36def-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="36def-116">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="36def-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="36def-117">2 訊息</span><span class="sxs-lookup"><span data-stu-id="36def-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="36def-118">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="36def-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="36def-119">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="36def-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="36def-120">3 通訊協定詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="36def-121">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="36def-122">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="36def-123">4 通訊協定範例</span><span class="sxs-lookup"><span data-stu-id="36def-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="36def-124">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="36def-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="36def-125">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="36def-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="36def-126">5 安全性</span><span class="sxs-lookup"><span data-stu-id="36def-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="36def-127">5.1 實作者的安全性考量</span><span class="sxs-lookup"><span data-stu-id="36def-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="36def-128">5.2 安全性參數的索引</span><span class="sxs-lookup"><span data-stu-id="36def-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="36def-129">6個版本特定行為的索引</span><span class="sxs-lookup"><span data-stu-id="36def-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="36def-130">本檔是內容索引服務通訊協定的規格。</span><span class="sxs-lookup"><span data-stu-id="36def-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="36def-131">工作組伺服器通訊協定程式 (WSPP) 檔集適用于搭配公用標準檔、網路程式設計藝術以及 Windows 工作組分散式系統概念，並假設讀者已熟悉上述的材質或立即存取它。</span><span class="sxs-lookup"><span data-stu-id="36def-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="36def-132">WSPP 通訊協定規格不需要使用 Microsoft 程式設計工具或程式設計環境，才能讓授權者開發執行。</span><span class="sxs-lookup"><span data-stu-id="36def-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="36def-133">擁有 Microsoft 程式設計工具和環境存取權的授權人可自由利用這些工具。</span><span class="sxs-lookup"><span data-stu-id="36def-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="36def-134">1 簡介</span><span class="sxs-lookup"><span data-stu-id="36def-134">1 Introduction</span></span>

-   [<span data-ttu-id="36def-135">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="36def-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="36def-136">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="36def-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="36def-137">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="36def-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="36def-138">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="36def-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="36def-139">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="36def-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="36def-140">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="36def-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="36def-141">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="36def-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="36def-142">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="36def-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="36def-143">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="36def-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="36def-144">1.1 詞彙</span><span class="sxs-lookup"><span data-stu-id="36def-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="36def-145">下列詞彙定義于 MS-SYS 的詞彙區段中 \[ \] ：</span><span class="sxs-lookup"><span data-stu-id="36def-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="36def-146">GUID</span><span class="sxs-lookup"><span data-stu-id="36def-146">GUID</span></span>
> -   <span data-ttu-id="36def-147">位元組由小到小</span><span class="sxs-lookup"><span data-stu-id="36def-147">Little Endian</span></span>
> -   <span data-ttu-id="36def-148">具名管道</span><span class="sxs-lookup"><span data-stu-id="36def-148">Named Pipe</span></span>
> -   <span data-ttu-id="36def-149">路徑</span><span class="sxs-lookup"><span data-stu-id="36def-149">Path</span></span>

 

<span data-ttu-id="36def-150">**Binding**：在傳回的資料 **列** 集中包含特定資料 **行** 的要求。</span><span class="sxs-lookup"><span data-stu-id="36def-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="36def-151">系結會指定要包含在搜尋結果 **中的屬性** 。</span><span class="sxs-lookup"><span data-stu-id="36def-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="36def-152">**書簽**：在一組資料列中唯一識別資料列的標記。</span><span class="sxs-lookup"><span data-stu-id="36def-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="36def-153">**目錄**：索引服務中最高層級的組織單位。</span><span class="sxs-lookup"><span data-stu-id="36def-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="36def-154">它代表一組已編制索引的檔，可讓您使用「內容索引服務」通訊協定來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="36def-155">**Category**：階層式資料列群組。</span><span class="sxs-lookup"><span data-stu-id="36def-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="36def-156">例如，包含 author 和 title 資料行的查詢結果可以根據作者分類。</span><span class="sxs-lookup"><span data-stu-id="36def-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="36def-157">每一組包含相同作者值的資料列都會構成一個類別目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="36def-158">**章節**：一組 **資料列內** 的資料 **列** 範圍。</span><span class="sxs-lookup"><span data-stu-id="36def-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="36def-159">資料 **行**：資料 **列** 中單一類型資訊的容器。</span><span class="sxs-lookup"><span data-stu-id="36def-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="36def-160">資料行會對應至屬性名稱，並指定搜尋查詢的 **命令\*\*\*\*樹** 元素所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="36def-161">**命令樹**：為搜尋查詢指定的 **限制** 、 **類別** 和 **排序次序** 的組合。</span><span class="sxs-lookup"><span data-stu-id="36def-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="36def-162">資料 **指標**：一個實體，用來做為在結果集中傳回的一組資料中，一次處理一個資料 **列** 或小型資料 **列** 區塊的機制。</span><span class="sxs-lookup"><span data-stu-id="36def-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="36def-163">資料 **指標** 位於結果集內的單一資料 **列** 。</span><span class="sxs-lookup"><span data-stu-id="36def-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="36def-164">將資料 **指標** 置於資料列之後，就可以在該資料 **列** 或從該位置開始的資料 **列** 區塊上執行作業。</span><span class="sxs-lookup"><span data-stu-id="36def-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="36def-165">**控制碼**：可以用來識別及存取資料 **指標** 、 **章節** 和 **書簽** 的權杖。</span><span class="sxs-lookup"><span data-stu-id="36def-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="36def-166">**Index**：持續性結構，包含 **索引服務** 所提取的文字內容。</span><span class="sxs-lookup"><span data-stu-id="36def-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="36def-167">這包含單字清單，這些字組會與包含的檔案名、單字位置和 **地區** 設定一起儲存。</span><span class="sxs-lookup"><span data-stu-id="36def-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="36def-168">**索引**：從檔案中解壓縮文字和屬性，以及將解壓縮的值儲存到文字) 的 **索引** (，以及) 屬性的 **屬性** 快取 (的程式。</span><span class="sxs-lookup"><span data-stu-id="36def-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="36def-169">**索引服務**：為檔案系統的內容和屬性建立索引 **目錄** 的服務。</span><span class="sxs-lookup"><span data-stu-id="36def-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="36def-170">應用程式可以在目錄中搜尋已編制索引之檔案系統上的檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="36def-171">**地區** 設定：以 GPSI 附錄 A 指定的識別碼，可 \[ \] 指定與語言相關的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="36def-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="36def-172">這些喜好設定會指出如何格式化日期和時間、依字母順序排序專案、要比較的字串等等。</span><span class="sxs-lookup"><span data-stu-id="36def-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="36def-173">**自然語言查詢**：使用人類語言而非查詢語法所建立的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="36def-174">非搜尋 **字**：索引服務在針對搜尋查詢所指定的 **限制** 中出現時，會忽略該單字，因為它的歧視性值很小。</span><span class="sxs-lookup"><span data-stu-id="36def-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="36def-175">英文範例包括「a」、「和」和「」。</span><span class="sxs-lookup"><span data-stu-id="36def-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="36def-176">**屬性** 快取： **索引服務** 所解壓縮檔案屬性的快取。</span><span class="sxs-lookup"><span data-stu-id="36def-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="36def-177">**屬性編制索引**：建立檔之實 **數值型別屬性\*\*\*\*索引** 的程式，包括作者、主旨、類型、字數統計、列印的頁面計數，以及任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="36def-178">**限制**：檔案必須符合才能包含在 **索引服務** 所傳回之搜尋結果中的一組條件，以回應搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="36def-179">**限制** 可縮小搜尋查詢的焦點，將 **索引服務** 只會包含在搜尋結果中的檔案，限制為符合條件的檔案。</span><span class="sxs-lookup"><span data-stu-id="36def-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="36def-180">**Row**：資料行的 **集合，其中** 包含的屬性值會描述一組檔案中的單一檔案，這些檔案會與提交給 **索引服務** 的搜尋查詢中所指定的 **限制** 相符。</span><span class="sxs-lookup"><span data-stu-id="36def-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="36def-181">資料列 **集**：在搜尋結果中傳回的一組資料 **列**。</span><span class="sxs-lookup"><span data-stu-id="36def-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="36def-182">**排序次序**：搜尋查詢中定義搜尋結果中資料列順序的規則集。</span><span class="sxs-lookup"><span data-stu-id="36def-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="36def-183">每個規則都包含一個屬性 (名稱、大小等等 ) 以及排序 (遞增或遞減) 的方向。</span><span class="sxs-lookup"><span data-stu-id="36def-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="36def-184">順序套用多個規則</span><span class="sxs-lookup"><span data-stu-id="36def-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="36def-185">**文字類型屬性**：描述檔內容的屬性，而且只有未格式化的文字與其名稱相關聯。</span><span class="sxs-lookup"><span data-stu-id="36def-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="36def-186">**數值型別屬性**：描述整份檔之單一屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="36def-187">實數值型別屬性具有資料類型識別碼，以及與其名稱相關聯之資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="36def-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="36def-188">**虛擬根目錄**：資料夾的替代路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="36def-189">實體資料夾可以有零或多個虛擬根目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="36def-190">以虛擬根目錄開頭的路徑稱為虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="36def-191">例如，/server/vanityroot 可能是 C： \\ IIS web folder1 的虛擬根目錄 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="36def-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="36def-192">然後 file C： \\ IIS \\ web \\ folder1 \\default.htm 會有/server/vanityroot/default.htm 的虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="36def-193">「不得」、「**不得**」、「不得」、「不得」：這些詞彙 (在所有 caps) 中，如 RFC2119 中所述 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="36def-194">選擇性行為的所有陳述均使用「可能」、「應該」或「不應」。</span><span class="sxs-lookup"><span data-stu-id="36def-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="36def-195">1.2 參考</span><span class="sxs-lookup"><span data-stu-id="36def-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="36def-196">1.2.1 標準參考</span><span class="sxs-lookup"><span data-stu-id="36def-196">1.2.1 Normative References</span></span>

<span data-ttu-id="36def-197">\[IEEE754 \] 協會的電子和電子工程師「標準的二進位 Floating-Point 算術標準」、IEEE 754-1985、1985年10月 https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="36def-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="36def-198">\[MS DCOM \] Microsoft Corporation，「分散式元件物件模型遠端通訊協定」，2006年6月。</span><span class="sxs-lookup"><span data-stu-id="36def-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="36def-199">\[GPSI Microsoft Corporation 「 \] 群組原則軟體安裝延伸模組」，2006年6月。</span><span class="sxs-lookup"><span data-stu-id="36def-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="36def-200">\[MS SMB \] Microsoft Corporation 「Microsoft Server Message Block (SMB) 通訊協定和延伸模組」，可能是2006。</span><span class="sxs-lookup"><span data-stu-id="36def-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="36def-201">\[MS SYS \] Microsoft Corporation "System 總覽 v4"，2006年7月。</span><span class="sxs-lookup"><span data-stu-id="36def-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="36def-202">\[SALTON \] SALTON，G.，"自動文字處理：依電腦的轉換剖析和抓取資訊"，1988，ISBN 0-201-2227-8。</span><span class="sxs-lookup"><span data-stu-id="36def-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="36def-203">\[Unicode \] 協會： "Unicode Standard，Version 2.0"，1996， https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="36def-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="36def-204">1.2.2 資訊參考</span><span class="sxs-lookup"><span data-stu-id="36def-204">1.2.2 Informative References</span></span>

<span data-ttu-id="36def-205">\[MSDN-OLEDB \] Microsoft Corporation，OLE DB https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp 。</span><span class="sxs-lookup"><span data-stu-id="36def-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="36def-206">\[MSDN-QUERYERR \] Microsoft Corporation、Query-Execution 值、 https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="36def-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="36def-207">1.3 通訊協定總覽 (概要) </span><span class="sxs-lookup"><span data-stu-id="36def-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="36def-208">內容 **編制索引服務** 有助於有效率地組織檔集合的已解壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="36def-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="36def-209">內容編制索引服務通訊協定 (CISP) 可讓用戶端與裝載索引服務的伺服器進行通訊，以發出查詢並允許系統管理員管理索引伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="36def-210">處理檔案時，索引服務會分析一組檔，並重新組織其內容，如此一來，這些檔的 **屬性** 就可以有效率地傳回以回應查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="36def-211">可以查詢的檔集合包含 **目錄** 。</span><span class="sxs-lookup"><span data-stu-id="36def-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="36def-212">目錄可以包含 **索引** (，以快速參考文字) 和 **屬性** 快取 (來快速抓取屬性值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="36def-213">就概念而言，目錄是由具有文字或值的屬性邏輯「資料表」，以及儲存在資料表資料 **行** 中的對應地區設定所組成。</span><span class="sxs-lookup"><span data-stu-id="36def-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="36def-214">資料表的每個「資料列」會對應至目錄範圍中的個別檔，而資料表的每個「資料行」會對應至屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="36def-215">CISP 執行的特定工作分為兩個功能區域：</span><span class="sxs-lookup"><span data-stu-id="36def-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="36def-216">索引服務目錄的遠端系統管理</span><span class="sxs-lookup"><span data-stu-id="36def-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="36def-217">遠端查詢索引服務目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="36def-218">1.3.1 遠端系統管理工作</span><span class="sxs-lookup"><span data-stu-id="36def-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="36def-219">CISP 可讓用戶端進行下列索引編制服務類別目錄管理工作：</span><span class="sxs-lookup"><span data-stu-id="36def-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="36def-220">查詢伺服器上索引服務類別目錄的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="36def-221">更新索引服務類別目錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="36def-222">啟動一組特定檔案的編制索引程式。</span><span class="sxs-lookup"><span data-stu-id="36def-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="36def-223">起始索引的優化，以便改善查詢效能。</span><span class="sxs-lookup"><span data-stu-id="36def-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="36def-224">所有遠端系統管理工作都遵循簡單的要求/回應模型。</span><span class="sxs-lookup"><span data-stu-id="36def-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="36def-225">用戶端不會在任何系統管理呼叫中維護任何狀態，而且系統會以任何順序進行管理呼叫。</span><span class="sxs-lookup"><span data-stu-id="36def-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="36def-226">1.3.2 遠端查詢</span><span class="sxs-lookup"><span data-stu-id="36def-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="36def-227">CISP 可讓用戶端對裝載索引服務的遠端伺服器執行搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="36def-228">傳送搜尋查詢是由用戶端所起始的多步驟處理常式。</span><span class="sxs-lookup"><span data-stu-id="36def-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="36def-229">步驟如下：</span><span class="sxs-lookup"><span data-stu-id="36def-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="36def-230">用戶端要求連接到裝載索引服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="36def-231">用戶端會傳送搜尋查詢的參數，包括：</span><span class="sxs-lookup"><span data-stu-id="36def-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="36def-232">指定要在搜尋結果中包含及/或排除哪些檔的 **限制** 。</span><span class="sxs-lookup"><span data-stu-id="36def-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="36def-233">傳回搜尋結果的順序。</span><span class="sxs-lookup"><span data-stu-id="36def-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="36def-234">要在結果集中傳回的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="36def-235">應針對查詢傳回的最大資料 **列** 數。</span><span class="sxs-lookup"><span data-stu-id="36def-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="36def-236">查詢執行的最長時間。</span><span class="sxs-lookup"><span data-stu-id="36def-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="36def-237">一旦伺服器已確認用戶端起始查詢的要求，用戶端就可以要求有關查詢的狀態資訊，但這不是必要的步驟。</span><span class="sxs-lookup"><span data-stu-id="36def-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="36def-238">用戶端接著會指定伺服器應包含在搜尋結果中的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="36def-239">用戶端會向伺服器要求結果集，而伺服器會透過傳送用戶端搜尋查詢結果中所包含之檔案的屬性值來回應。</span><span class="sxs-lookup"><span data-stu-id="36def-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="36def-240">如果屬性值太大而無法放入單一回應緩衝區中，伺服器將不會傳送屬性，而是會將屬性狀態設定為 [已延後]。</span><span class="sxs-lookup"><span data-stu-id="36def-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="36def-241">然後，用戶端會使用一系列的連續值區塊來個別要求屬性值，然後再繼續要求其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="36def-242">一旦用戶端使用搜尋查詢完成，且不再需要額外的結果，用戶端會與伺服器聯繫以釋出查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="36def-243">一旦伺服器釋出查詢之後，用戶端可能會傳送要求，以便中斷與伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="36def-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="36def-244">然後連接會關閉。</span><span class="sxs-lookup"><span data-stu-id="36def-244">The connection is then closed.</span></span> <span data-ttu-id="36def-245">或者，用戶端可能會發出另一個查詢，並重複步驟2中的順序。</span><span class="sxs-lookup"><span data-stu-id="36def-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="36def-246">Windows 行為：此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。</span><span class="sxs-lookup"><span data-stu-id="36def-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="36def-247">1.4 與通訊協定的關聯性</span><span class="sxs-lookup"><span data-stu-id="36def-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="36def-248">CISP 依賴 SMB \[ MS smb \] 通訊協定來傳輸訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="36def-249">沒有其他通訊協定直接相依于內容編制索引服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="36def-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="36def-250">*Windows 行為：應用程式通常會與 OLE DB 介面包裝函 \[ 式 MSDN-OLEDB \] (，例如通訊協定用戶端) ，而不是直接與通訊協定互動。*</span><span class="sxs-lookup"><span data-stu-id="36def-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="36def-251">1.5 必要條件和前置條件</span><span class="sxs-lookup"><span data-stu-id="36def-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="36def-252">假設用戶端在叫用此通訊協定之前，已取得伺服器的名稱和目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="36def-253">用戶端如何進行這項規格的範圍之外。</span><span class="sxs-lookup"><span data-stu-id="36def-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="36def-254">也假設用戶端和伺服器具有可與具名管道 MS SMB 搭配使用的安全性關聯 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="36def-255">1.6 適用性陳述</span><span class="sxs-lookup"><span data-stu-id="36def-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="36def-256">CISP 是設計用來從用戶端查詢及管理遠端伺服器上的目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="36def-257">CISP 已在 Windows Vista 上淘汰。</span><span class="sxs-lookup"><span data-stu-id="36def-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="36def-258">1.7 版本設定和功能交涉</span><span class="sxs-lookup"><span data-stu-id="36def-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="36def-259">此通訊協定沒有任何版本控制或功能協商機制。</span><span class="sxs-lookup"><span data-stu-id="36def-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="36def-260">1.8 廠商可延伸欄位</span><span class="sxs-lookup"><span data-stu-id="36def-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="36def-261">此通訊協定會使用可延伸廠商的 Hresult。</span><span class="sxs-lookup"><span data-stu-id="36def-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="36def-262">您可以針對此欄位自由選擇自己的值，只要 C 位 (0x20000000) 設定為在 MS-SYS 的區段4.1.1 中指定 \[ \] ，表示它是客戶程式碼。</span><span class="sxs-lookup"><span data-stu-id="36def-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="36def-263">此通訊協定也會使用取自在 Ms-chap 中定義之 NTSTATUS 網際空間的 NTSTATUS 值 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="36def-264">廠商應以其指定的意義重複使用這些值。</span><span class="sxs-lookup"><span data-stu-id="36def-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="36def-265">選擇任何其他值，就會在未來發生衝突的風險。</span><span class="sxs-lookup"><span data-stu-id="36def-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="36def-266">*Windows 行為： Windows 只會使用4.1.3 的區段中指定的值 \[ \] 。*</span><span class="sxs-lookup"><span data-stu-id="36def-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="36def-267">1.8.1 屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="36def-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="36def-268">屬性是由稱為屬性識別碼的識別碼來表示。</span><span class="sxs-lookup"><span data-stu-id="36def-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="36def-269">每個屬性都必須有全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="36def-270">此識別碼是由 GUID 所組成，此 **GUID** 代表稱為屬性集的屬性集合，加上字串或32位整數，以識別集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="36def-271">如果使用整數形式的識別碼，則會將0x00000000、0xFFFFFFFF 和0xFFFFFFFE 值視為無效。</span><span class="sxs-lookup"><span data-stu-id="36def-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="36def-272">廠商可以將屬性放在其本身的 GUID 所定義的屬性集中，以保證其屬性是唯一的定義。</span><span class="sxs-lookup"><span data-stu-id="36def-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="36def-273">1.9 標準指派</span><span class="sxs-lookup"><span data-stu-id="36def-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="36def-274">此通訊協定不會指派標準，而只會使用其他通訊協定中指定的配置程式來進行 Microsoft 所做的私用指派。</span><span class="sxs-lookup"><span data-stu-id="36def-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="36def-275">Microsoft 已將此通訊協定配置給以 MS SMB 指定的具名管道 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="36def-276">指派為：</span><span class="sxs-lookup"><span data-stu-id="36def-276">The assignment is:</span></span>



| <span data-ttu-id="36def-277">參數</span><span class="sxs-lookup"><span data-stu-id="36def-277">Parameter</span></span> | <span data-ttu-id="36def-278">值</span><span class="sxs-lookup"><span data-stu-id="36def-278">Value</span></span>             | <span data-ttu-id="36def-279">參考</span><span class="sxs-lookup"><span data-stu-id="36def-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="36def-280">管道名稱</span><span class="sxs-lookup"><span data-stu-id="36def-280">Pipe name</span></span> | <span data-ttu-id="36def-281">\\管道 \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="36def-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="36def-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="36def-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="36def-283">2 訊息</span><span class="sxs-lookup"><span data-stu-id="36def-283">2 Messages</span></span>

-   [<span data-ttu-id="36def-284">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="36def-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="36def-285">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="36def-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="36def-286">2.1 傳輸</span><span class="sxs-lookup"><span data-stu-id="36def-286">2.1 Transport</span></span>

<span data-ttu-id="36def-287">所有訊息都必須使用具名管道來傳輸（如 MS SMB 中所指定） \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="36def-288">使用的管道名稱如下：</span><span class="sxs-lookup"><span data-stu-id="36def-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="36def-289">\\管道 \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="36def-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="36def-290">此通訊協定會使用基礎 SMB 具名管道通訊協定，來抓取進行連接的呼叫端身分識別，如 MS-SMB 的區段2.2.8 中所指定 \[ \] ; 用戶端必須將安全性 \_ 識別設定為要求中的 ImpersonationLevel，才能開啟具名管道。</span><span class="sxs-lookup"><span data-stu-id="36def-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="36def-291">2.2 訊息語法</span><span class="sxs-lookup"><span data-stu-id="36def-291">2.2 Message Syntax</span></span>

<span data-ttu-id="36def-292">下列各節中的數個結構和訊息是指章節或書簽控制碼。</span><span class="sxs-lookup"><span data-stu-id="36def-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="36def-293">控制碼是可唯一識別章節或書簽的32位長透明結構。</span><span class="sxs-lookup"><span data-stu-id="36def-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="36def-294">一般而言，用戶端應用程式會透過方法呼叫來接收控制碼值;不過，有幾個已知的值不需要從伺服器取得，其意義如下表所示：</span><span class="sxs-lookup"><span data-stu-id="36def-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="36def-295">值</span><span class="sxs-lookup"><span data-stu-id="36def-295">Value</span></span>                         | <span data-ttu-id="36def-296">意義</span><span class="sxs-lookup"><span data-stu-id="36def-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="36def-297">DB \_ Null \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="36def-298">Unchaptered 資料列集的章節控制碼，其中包含所有查詢結果。</span><span class="sxs-lookup"><span data-stu-id="36def-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="36def-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="36def-300">書簽的書簽控制碼，這個書簽會識別資料列集中的第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="36def-301">DBBMK \_ 最後的0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="36def-302">書簽的書簽控制碼，這個書簽會識別資料列集中的最後一個資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="36def-303">2.2.1 結構</span><span class="sxs-lookup"><span data-stu-id="36def-303">2.2.1 Structures</span></span>

<span data-ttu-id="36def-304">本節詳細說明 CISP 所定義和使用的資料結構。</span><span class="sxs-lookup"><span data-stu-id="36def-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="36def-305">下列結構中的所有2、4和8位元組的帶正負號和不帶正負號的整數都必須以位元組由小到大的順序傳送。</span><span class="sxs-lookup"><span data-stu-id="36def-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="36def-306">下表摘要說明此區段中定義的資料結構。</span><span class="sxs-lookup"><span data-stu-id="36def-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="36def-307">結構</span><span class="sxs-lookup"><span data-stu-id="36def-307">Structure</span></span>                    | <span data-ttu-id="36def-308">Description</span><span class="sxs-lookup"><span data-stu-id="36def-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="36def-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="36def-310">包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。</span><span class="sxs-lookup"><span data-stu-id="36def-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="36def-311">SAFEARRAY、SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="36def-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="36def-312">包含多維陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="36def-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="36def-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="36def-314">表示 SAFEARRAY 結構中所指定之陣列維度的界限。</span><span class="sxs-lookup"><span data-stu-id="36def-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="36def-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="36def-315">CFullPropSpec</span></span>                | <span data-ttu-id="36def-316">包含屬性規格。</span><span class="sxs-lookup"><span data-stu-id="36def-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="36def-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-317">CContentRestriction</span></span>          | <span data-ttu-id="36def-318">包含屬性（property）快取中的屬性值所要比對的字串。</span><span class="sxs-lookup"><span data-stu-id="36def-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="36def-319">CKey</span><span class="sxs-lookup"><span data-stu-id="36def-319">CKey</span></span>                         | <span data-ttu-id="36def-320">包含屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="36def-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="36def-322">包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="36def-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="36def-324">包含屬性的自然語言查詢相符項。</span><span class="sxs-lookup"><span data-stu-id="36def-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="36def-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-325">CNodeRestriction</span></span>             | <span data-ttu-id="36def-326">包含指定查詢限制的命令樹節點陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="36def-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-327">COccRestriction</span></span>              | <span data-ttu-id="36def-328">包含單字在片語中的位置。</span><span class="sxs-lookup"><span data-stu-id="36def-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="36def-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-329">CPropertyRestriction</span></span>         | <span data-ttu-id="36def-330">包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="36def-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-331">CRangeRestriction</span></span>            | <span data-ttu-id="36def-332">包含值範圍的限制。</span><span class="sxs-lookup"><span data-stu-id="36def-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="36def-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-333">CScopeRestriction</span></span>            | <span data-ttu-id="36def-334">包含要搜尋之檔案的限制。</span><span class="sxs-lookup"><span data-stu-id="36def-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="36def-335">CSort</span><span class="sxs-lookup"><span data-stu-id="36def-335">CSort</span></span>                        | <span data-ttu-id="36def-336">識別要排序的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="36def-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-337">CSynRestriction</span></span>              | <span data-ttu-id="36def-338">包含查詢片語的單字或其同義字。</span><span class="sxs-lookup"><span data-stu-id="36def-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="36def-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-339">CVectorRestriction</span></span>           | <span data-ttu-id="36def-340">包含命令樹節點上的加權或運算。</span><span class="sxs-lookup"><span data-stu-id="36def-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="36def-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-341">CWordRestriction</span></span>             | <span data-ttu-id="36def-342">包含查詢片語的單字。</span><span class="sxs-lookup"><span data-stu-id="36def-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="36def-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-343">CRestriction</span></span>                 | <span data-ttu-id="36def-344">包含查詢命令樹的節點。</span><span class="sxs-lookup"><span data-stu-id="36def-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="36def-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="36def-345">CColumnSet</span></span>                   | <span data-ttu-id="36def-346">指出要傳回的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="36def-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="36def-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="36def-347">CCategorizationSet</span></span>           | <span data-ttu-id="36def-348">包含一組查詢結果群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="36def-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="36def-349">CCategorizationSpec</span></span>          | <span data-ttu-id="36def-350">包含分類的定義，查詢結果將分類至其中。</span><span class="sxs-lookup"><span data-stu-id="36def-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="36def-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="36def-351">CDbColId</span></span>                     | <span data-ttu-id="36def-352">包含資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="36def-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="36def-353">CDbProp</span></span>                      | <span data-ttu-id="36def-354">包含屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="36def-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="36def-355">CDbPropSet</span></span>                   | <span data-ttu-id="36def-356">包含一組屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="36def-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="36def-357">CPidMapper</span></span>                   | <span data-ttu-id="36def-358">包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="36def-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="36def-359">CRowSeekAt</span></span>                   | <span data-ttu-id="36def-360">包含要在 CPMGetRowsIn 訊息中取得資料列的位移</span><span class="sxs-lookup"><span data-stu-id="36def-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="36def-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="36def-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="36def-362">識別開始抓取 CPMGetRowsIn 訊息的起點。</span><span class="sxs-lookup"><span data-stu-id="36def-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="36def-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="36def-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="36def-364">識別要從中取出 CPMGetRowsIn 訊息之資料列的書簽。</span><span class="sxs-lookup"><span data-stu-id="36def-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="36def-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="36def-365">CRowSeekNext</span></span>                 | <span data-ttu-id="36def-366">包含要在 CPMGetRowsIn 訊息中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="36def-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="36def-367">CRowsetProperties</span></span>            | <span data-ttu-id="36def-368">包含查詢的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="36def-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="36def-369">CSortSet</span></span>                     | <span data-ttu-id="36def-370">包含查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="36def-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="36def-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="36def-371">CTableColumn</span></span>                 | <span data-ttu-id="36def-372">包含 CPMSetBindings 訊息的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="36def-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="36def-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="36def-374">包含序列化值。</span><span class="sxs-lookup"><span data-stu-id="36def-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="36def-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="36def-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="36def-376">CBaseStorageVariant 結構包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。</span><span class="sxs-lookup"><span data-stu-id="36def-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="36def-377">0</span><span class="sxs-lookup"><span data-stu-id="36def-377">0</span></span>

<span data-ttu-id="36def-378">1</span><span class="sxs-lookup"><span data-stu-id="36def-378">1</span></span>

<span data-ttu-id="36def-379">2</span><span class="sxs-lookup"><span data-stu-id="36def-379">2</span></span>

<span data-ttu-id="36def-380">3</span><span class="sxs-lookup"><span data-stu-id="36def-380">3</span></span>

<span data-ttu-id="36def-381">4</span><span class="sxs-lookup"><span data-stu-id="36def-381">4</span></span>

<span data-ttu-id="36def-382">5</span><span class="sxs-lookup"><span data-stu-id="36def-382">5</span></span>

<span data-ttu-id="36def-383">6</span><span class="sxs-lookup"><span data-stu-id="36def-383">6</span></span>

<span data-ttu-id="36def-384">7</span><span class="sxs-lookup"><span data-stu-id="36def-384">7</span></span>

<span data-ttu-id="36def-385">8</span><span class="sxs-lookup"><span data-stu-id="36def-385">8</span></span>

<span data-ttu-id="36def-386">9</span><span class="sxs-lookup"><span data-stu-id="36def-386">9</span></span>

<span data-ttu-id="36def-387">1</span><span class="sxs-lookup"><span data-stu-id="36def-387">1</span></span><br/> <span data-ttu-id="36def-388">0</span><span class="sxs-lookup"><span data-stu-id="36def-388">0</span></span><br/>

<span data-ttu-id="36def-389">1</span><span class="sxs-lookup"><span data-stu-id="36def-389">1</span></span>

<span data-ttu-id="36def-390">2</span><span class="sxs-lookup"><span data-stu-id="36def-390">2</span></span>

<span data-ttu-id="36def-391">3</span><span class="sxs-lookup"><span data-stu-id="36def-391">3</span></span>

<span data-ttu-id="36def-392">4</span><span class="sxs-lookup"><span data-stu-id="36def-392">4</span></span>

<span data-ttu-id="36def-393">5</span><span class="sxs-lookup"><span data-stu-id="36def-393">5</span></span>

<span data-ttu-id="36def-394">6</span><span class="sxs-lookup"><span data-stu-id="36def-394">6</span></span>

<span data-ttu-id="36def-395">7</span><span class="sxs-lookup"><span data-stu-id="36def-395">7</span></span>

<span data-ttu-id="36def-396">8</span><span class="sxs-lookup"><span data-stu-id="36def-396">8</span></span>

<span data-ttu-id="36def-397">9</span><span class="sxs-lookup"><span data-stu-id="36def-397">9</span></span>

<span data-ttu-id="36def-398">2</span><span class="sxs-lookup"><span data-stu-id="36def-398">2</span></span><br/> <span data-ttu-id="36def-399">0</span><span class="sxs-lookup"><span data-stu-id="36def-399">0</span></span><br/>

<span data-ttu-id="36def-400">1</span><span class="sxs-lookup"><span data-stu-id="36def-400">1</span></span>

<span data-ttu-id="36def-401">2</span><span class="sxs-lookup"><span data-stu-id="36def-401">2</span></span>

<span data-ttu-id="36def-402">3</span><span class="sxs-lookup"><span data-stu-id="36def-402">3</span></span>

<span data-ttu-id="36def-403">4</span><span class="sxs-lookup"><span data-stu-id="36def-403">4</span></span>

<span data-ttu-id="36def-404">5</span><span class="sxs-lookup"><span data-stu-id="36def-404">5</span></span>

<span data-ttu-id="36def-405">6</span><span class="sxs-lookup"><span data-stu-id="36def-405">6</span></span>

<span data-ttu-id="36def-406">7</span><span class="sxs-lookup"><span data-stu-id="36def-406">7</span></span>

<span data-ttu-id="36def-407">8</span><span class="sxs-lookup"><span data-stu-id="36def-407">8</span></span>

<span data-ttu-id="36def-408">9</span><span class="sxs-lookup"><span data-stu-id="36def-408">9</span></span>

<span data-ttu-id="36def-409">3</span><span class="sxs-lookup"><span data-stu-id="36def-409">3</span></span><br/> <span data-ttu-id="36def-410">0</span><span class="sxs-lookup"><span data-stu-id="36def-410">0</span></span><br/>

<span data-ttu-id="36def-411">1</span><span class="sxs-lookup"><span data-stu-id="36def-411">1</span></span>

<span data-ttu-id="36def-412">vType</span><span class="sxs-lookup"><span data-stu-id="36def-412">vType</span></span>

<span data-ttu-id="36def-413">vData1</span><span class="sxs-lookup"><span data-stu-id="36def-413">vData1</span></span>

<span data-ttu-id="36def-414">vData2</span><span class="sxs-lookup"><span data-stu-id="36def-414">vData2</span></span>

<span data-ttu-id="36def-415">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-415">vValue (variable)</span></span>



 

<span data-ttu-id="36def-416">**vType**：類型指標，表示 vValue 的類型。</span><span class="sxs-lookup"><span data-stu-id="36def-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="36def-417">它必須是下表中指定的其中一個 VARENUM 值。</span><span class="sxs-lookup"><span data-stu-id="36def-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="36def-418">值</span><span class="sxs-lookup"><span data-stu-id="36def-418">Value</span></span>                 | <span data-ttu-id="36def-419">意義</span><span class="sxs-lookup"><span data-stu-id="36def-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-420">VT \_ 空白 (0x0000) </span><span class="sxs-lookup"><span data-stu-id="36def-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="36def-421">vValue 不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="36def-422">VT \_ Null (0x0001) </span><span class="sxs-lookup"><span data-stu-id="36def-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="36def-423">vValue 不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="36def-424">VT \_ I1 (0x0010) </span><span class="sxs-lookup"><span data-stu-id="36def-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="36def-425">1 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="36def-426">VT \_ UI1 (0x0011) </span><span class="sxs-lookup"><span data-stu-id="36def-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="36def-427">1 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="36def-428">VT \_ I2 (0x0002) </span><span class="sxs-lookup"><span data-stu-id="36def-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="36def-429">2 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="36def-430">VT \_ UI2 (0x0012) </span><span class="sxs-lookup"><span data-stu-id="36def-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="36def-431">2 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="36def-432">VT \_ BOOL (0x000B) </span><span class="sxs-lookup"><span data-stu-id="36def-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="36def-433">布林值;雙位元組整數，其中包含 0x0000 (FALSE) 或 0xFFFF (TRUE) 。</span><span class="sxs-lookup"><span data-stu-id="36def-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="36def-434">VT \_ I4 (0x0003) </span><span class="sxs-lookup"><span data-stu-id="36def-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="36def-435">4 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="36def-436">VT \_ UI4 (0x0013) </span><span class="sxs-lookup"><span data-stu-id="36def-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="36def-437">4 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="36def-438">VT \_ R4 (0x0004) </span><span class="sxs-lookup"><span data-stu-id="36def-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="36def-439">IEEE 32 位浮點數，如 IEEE754 中所定義 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="36def-440">VT \_ INT (0x0016) </span><span class="sxs-lookup"><span data-stu-id="36def-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="36def-441">4 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="36def-442">VT \_ UINT (0x0017) </span><span class="sxs-lookup"><span data-stu-id="36def-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="36def-443">4 位元組不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="36def-444">VT \_ 錯誤 (0x000A) </span><span class="sxs-lookup"><span data-stu-id="36def-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="36def-445">包含 HRESULT 的4位元組不帶正負號的整數，如 Ms-chap 中所指定 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="36def-446">VT \_ I8 (0x0014) </span><span class="sxs-lookup"><span data-stu-id="36def-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="36def-447">8位元組帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="36def-448">VT \_ UI8 (0x0015) </span><span class="sxs-lookup"><span data-stu-id="36def-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="36def-449">8 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="36def-450">VT \_ R8 (0x0005) </span><span class="sxs-lookup"><span data-stu-id="36def-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="36def-451">IEEE754 中定義的 IEEE 64 位浮點數 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="36def-452">VT \_ CY (0x0006) </span><span class="sxs-lookup"><span data-stu-id="36def-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="36def-453">8個位元組的補數整數 (由 10000) 調整。</span><span class="sxs-lookup"><span data-stu-id="36def-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="36def-454">VT \_ DATE (0x0007) </span><span class="sxs-lookup"><span data-stu-id="36def-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="36def-455">64位浮點數，代表自00:00:00 年12月31日起算的天數（1899 (國際標準時間) 。</span><span class="sxs-lookup"><span data-stu-id="36def-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="36def-456">VT \_ FILETIME (0x0040) </span><span class="sxs-lookup"><span data-stu-id="36def-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="36def-457">64位整數，表示自年1月 1 1601 日起00:00:00 的100秒間隔數， (國際標準時間) 。</span><span class="sxs-lookup"><span data-stu-id="36def-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="36def-458">VT \_ DECIMAL (0x000E) </span><span class="sxs-lookup"><span data-stu-id="36def-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="36def-459">2.2.1.1.1.1 一節中所指定的十進位結構。</span><span class="sxs-lookup"><span data-stu-id="36def-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="36def-460">VT \_ CLSID (0x0048) </span><span class="sxs-lookup"><span data-stu-id="36def-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="36def-461">包含 GUID 的16位元組二進位值。</span><span class="sxs-lookup"><span data-stu-id="36def-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="36def-462">VT \_ BLOB (0x0041) </span><span class="sxs-lookup"><span data-stu-id="36def-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="36def-463">Blob 中4位元組不帶正負號的整數的位元組計數，後面接著該資料的多個位元組。</span><span class="sxs-lookup"><span data-stu-id="36def-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="36def-464">VT \_ BSTR (0x0008) </span><span class="sxs-lookup"><span data-stu-id="36def-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="36def-465">字串中4位元組不帶正負號的整數的位元組計數，後面接著字串，如以下所示 vValue 下所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="36def-466">VT \_ LPSTR (0x001E) </span><span class="sxs-lookup"><span data-stu-id="36def-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="36def-467">以 null 結束的 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="36def-468">VT \_ LPWSTR (0x001F) </span><span class="sxs-lookup"><span data-stu-id="36def-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="36def-469">以 null 結尾的 Unicode \[ \] 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="36def-470">VT \_ 變異 (0x000C) </span><span class="sxs-lookup"><span data-stu-id="36def-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="36def-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="36def-471">CBaseStorageVariant.</span></span> <span data-ttu-id="36def-472">必須與 VT \_ 陣列或 vt 向量的類型修飾詞結合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="36def-473">下表指定 vType 的類型修飾詞。</span><span class="sxs-lookup"><span data-stu-id="36def-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="36def-474">類型修飾詞可以是具有 vType 的二進位 Or 運算，用以變更 vValue 的意義，表示它是兩個可能陣列類型的其中一個。</span><span class="sxs-lookup"><span data-stu-id="36def-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="36def-475">值</span><span class="sxs-lookup"><span data-stu-id="36def-475">Value</span></span>               | <span data-ttu-id="36def-476">意義</span><span class="sxs-lookup"><span data-stu-id="36def-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-477">VT \_ 向量 (0x1000) </span><span class="sxs-lookup"><span data-stu-id="36def-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="36def-478">如果類型指標是 \_ 使用 OR 運算子與 VT 向量結合，則 vValue 是所指定類型之值的計數陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="36def-479">如需詳細資訊，請參閱2.2.1.1.1.2 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="36def-480">此類型修飾詞不能與下列類型結合： VT \_ INT、VT \_ UINT、vt \_ DECIMAL、VT \_ blob、vt \_ blob \_ 物件。</span><span class="sxs-lookup"><span data-stu-id="36def-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="36def-481">VT \_ 陣列 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="36def-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="36def-482">如果類型指標是 \_ 由 OR 運算子與 VT 陣列結合，則此值為 SAFEARRAY (，如區段 2.2.1.1.1.3) 中所指定，其中包含指定之類型的值。</span><span class="sxs-lookup"><span data-stu-id="36def-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="36def-483">此類型修飾詞不能與下列類型結合： VT \_ I8、vt \_ UI8、vt \_ FILETIME、VT \_ CLSID、vt \_ blob、vt \_ BLOB \_ 物件、vt \_ LPSTR、vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="36def-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="36def-484">**vData1**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 [小數位數] 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="36def-485">若為所有其他 vTypes，此值必須設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="36def-486">**vData2**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 Sign 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="36def-487">若為所有其他 vTypes，此值必須設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="36def-488">**vValue**：相符運算的值。</span><span class="sxs-lookup"><span data-stu-id="36def-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="36def-489">語法必須如 vType 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="36def-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="36def-490">下表摘要說明 vValue 欄位的大小，其相依于固定長度資料類型的 vType 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="36def-491">大小是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="36def-491">The size is in bytes.</span></span>



| <span data-ttu-id="36def-492">vType</span><span class="sxs-lookup"><span data-stu-id="36def-492">vType</span></span>                                                   | <span data-ttu-id="36def-493">大小</span><span class="sxs-lookup"><span data-stu-id="36def-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="36def-494">VT \_ I1、vt、 \_ UI1</span><span class="sxs-lookup"><span data-stu-id="36def-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="36def-495">1</span><span class="sxs-lookup"><span data-stu-id="36def-495">1</span></span>    |
| <span data-ttu-id="36def-496">VT \_ I2，vt \_ UI2，vt \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="36def-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="36def-497">2</span><span class="sxs-lookup"><span data-stu-id="36def-497">2</span></span>    |
| <span data-ttu-id="36def-498">VT \_ I4，vt \_ UI4，vt \_ R4，VT \_ INT，vt \_ UINT，VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="36def-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="36def-499">4</span><span class="sxs-lookup"><span data-stu-id="36def-499">4</span></span>    |
| <span data-ttu-id="36def-500">VT \_ I8、vt \_ UI8、vt \_ R8、VT \_ CY、vt \_ DATE、vt \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="36def-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="36def-501">8</span><span class="sxs-lookup"><span data-stu-id="36def-501">8</span></span>    |
| <span data-ttu-id="36def-502">VT \_ DECIMAL、VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="36def-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="36def-503">16</span><span class="sxs-lookup"><span data-stu-id="36def-503">16</span></span>   |



 

<span data-ttu-id="36def-504">如果 vType 設定為 VT \_ BLOB、vt \_ BSTR 或 vt LPSTR，則 \_ vValue 的結構會在下圖中指定：</span><span class="sxs-lookup"><span data-stu-id="36def-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="36def-505">0</span><span class="sxs-lookup"><span data-stu-id="36def-505">0</span></span>

<span data-ttu-id="36def-506">1</span><span class="sxs-lookup"><span data-stu-id="36def-506">1</span></span>

<span data-ttu-id="36def-507">2</span><span class="sxs-lookup"><span data-stu-id="36def-507">2</span></span>

<span data-ttu-id="36def-508">3</span><span class="sxs-lookup"><span data-stu-id="36def-508">3</span></span>

<span data-ttu-id="36def-509">4</span><span class="sxs-lookup"><span data-stu-id="36def-509">4</span></span>

<span data-ttu-id="36def-510">5</span><span class="sxs-lookup"><span data-stu-id="36def-510">5</span></span>

<span data-ttu-id="36def-511">6</span><span class="sxs-lookup"><span data-stu-id="36def-511">6</span></span>

<span data-ttu-id="36def-512">7</span><span class="sxs-lookup"><span data-stu-id="36def-512">7</span></span>

<span data-ttu-id="36def-513">8</span><span class="sxs-lookup"><span data-stu-id="36def-513">8</span></span>

<span data-ttu-id="36def-514">9</span><span class="sxs-lookup"><span data-stu-id="36def-514">9</span></span>

<span data-ttu-id="36def-515">1</span><span class="sxs-lookup"><span data-stu-id="36def-515">1</span></span><br/> <span data-ttu-id="36def-516">0</span><span class="sxs-lookup"><span data-stu-id="36def-516">0</span></span><br/>

<span data-ttu-id="36def-517">1</span><span class="sxs-lookup"><span data-stu-id="36def-517">1</span></span>

<span data-ttu-id="36def-518">2</span><span class="sxs-lookup"><span data-stu-id="36def-518">2</span></span>

<span data-ttu-id="36def-519">3</span><span class="sxs-lookup"><span data-stu-id="36def-519">3</span></span>

<span data-ttu-id="36def-520">4</span><span class="sxs-lookup"><span data-stu-id="36def-520">4</span></span>

<span data-ttu-id="36def-521">5</span><span class="sxs-lookup"><span data-stu-id="36def-521">5</span></span>

<span data-ttu-id="36def-522">6</span><span class="sxs-lookup"><span data-stu-id="36def-522">6</span></span>

<span data-ttu-id="36def-523">7</span><span class="sxs-lookup"><span data-stu-id="36def-523">7</span></span>

<span data-ttu-id="36def-524">8</span><span class="sxs-lookup"><span data-stu-id="36def-524">8</span></span>

<span data-ttu-id="36def-525">9</span><span class="sxs-lookup"><span data-stu-id="36def-525">9</span></span>

<span data-ttu-id="36def-526">2</span><span class="sxs-lookup"><span data-stu-id="36def-526">2</span></span><br/> <span data-ttu-id="36def-527">0</span><span class="sxs-lookup"><span data-stu-id="36def-527">0</span></span><br/>

<span data-ttu-id="36def-528">1</span><span class="sxs-lookup"><span data-stu-id="36def-528">1</span></span>

<span data-ttu-id="36def-529">2</span><span class="sxs-lookup"><span data-stu-id="36def-529">2</span></span>

<span data-ttu-id="36def-530">3</span><span class="sxs-lookup"><span data-stu-id="36def-530">3</span></span>

<span data-ttu-id="36def-531">4</span><span class="sxs-lookup"><span data-stu-id="36def-531">4</span></span>

<span data-ttu-id="36def-532">5</span><span class="sxs-lookup"><span data-stu-id="36def-532">5</span></span>

<span data-ttu-id="36def-533">6</span><span class="sxs-lookup"><span data-stu-id="36def-533">6</span></span>

<span data-ttu-id="36def-534">7</span><span class="sxs-lookup"><span data-stu-id="36def-534">7</span></span>

<span data-ttu-id="36def-535">8</span><span class="sxs-lookup"><span data-stu-id="36def-535">8</span></span>

<span data-ttu-id="36def-536">9</span><span class="sxs-lookup"><span data-stu-id="36def-536">9</span></span>

<span data-ttu-id="36def-537">3</span><span class="sxs-lookup"><span data-stu-id="36def-537">3</span></span><br/> <span data-ttu-id="36def-538">0</span><span class="sxs-lookup"><span data-stu-id="36def-538">0</span></span><br/>

<span data-ttu-id="36def-539">1</span><span class="sxs-lookup"><span data-stu-id="36def-539">1</span></span>

<span data-ttu-id="36def-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="36def-540">cbSize</span></span>

<span data-ttu-id="36def-541">blobData (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="36def-542">**cbSize**：不帶正負號的32位整數，表示 blobData 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="36def-543">如果 vType 設定為 VT \_ BSTR 或 vt \_ LPSTR，則當表示的字串為空字串時，cbSize 必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="36def-544">**blobData**：必須是 cbSize 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="36def-545">針對設定為 VT blob 的 vType \_ ，此欄位是不透明的二進位 blob 資料。</span><span class="sxs-lookup"><span data-stu-id="36def-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="36def-546">針對設定為 VT BSTR 的 vType \_ ，此欄位是 OEM 所選取字元集中的一組字元。</span><span class="sxs-lookup"><span data-stu-id="36def-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="36def-547">用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。</span><span class="sxs-lookup"><span data-stu-id="36def-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="36def-548">不需要以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="36def-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="36def-549">若 vType 設為 VT \_ LPSTR，此欄位是 OEM 所選取字元集中以 null 結束的字元字串。</span><span class="sxs-lookup"><span data-stu-id="36def-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="36def-550">用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。</span><span class="sxs-lookup"><span data-stu-id="36def-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="36def-551">如果 vType 設定為 VT LPWSTR，則 \_ vValue 的結構會在下圖中指定：</span><span class="sxs-lookup"><span data-stu-id="36def-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="36def-552">0</span><span class="sxs-lookup"><span data-stu-id="36def-552">0</span></span>

<span data-ttu-id="36def-553">1</span><span class="sxs-lookup"><span data-stu-id="36def-553">1</span></span>

<span data-ttu-id="36def-554">2</span><span class="sxs-lookup"><span data-stu-id="36def-554">2</span></span>

<span data-ttu-id="36def-555">3</span><span class="sxs-lookup"><span data-stu-id="36def-555">3</span></span>

<span data-ttu-id="36def-556">4</span><span class="sxs-lookup"><span data-stu-id="36def-556">4</span></span>

<span data-ttu-id="36def-557">5</span><span class="sxs-lookup"><span data-stu-id="36def-557">5</span></span>

<span data-ttu-id="36def-558">6</span><span class="sxs-lookup"><span data-stu-id="36def-558">6</span></span>

<span data-ttu-id="36def-559">7</span><span class="sxs-lookup"><span data-stu-id="36def-559">7</span></span>

<span data-ttu-id="36def-560">8</span><span class="sxs-lookup"><span data-stu-id="36def-560">8</span></span>

<span data-ttu-id="36def-561">9</span><span class="sxs-lookup"><span data-stu-id="36def-561">9</span></span>

<span data-ttu-id="36def-562">1</span><span class="sxs-lookup"><span data-stu-id="36def-562">1</span></span><br/> <span data-ttu-id="36def-563">0</span><span class="sxs-lookup"><span data-stu-id="36def-563">0</span></span><br/>

<span data-ttu-id="36def-564">1</span><span class="sxs-lookup"><span data-stu-id="36def-564">1</span></span>

<span data-ttu-id="36def-565">2</span><span class="sxs-lookup"><span data-stu-id="36def-565">2</span></span>

<span data-ttu-id="36def-566">3</span><span class="sxs-lookup"><span data-stu-id="36def-566">3</span></span>

<span data-ttu-id="36def-567">4</span><span class="sxs-lookup"><span data-stu-id="36def-567">4</span></span>

<span data-ttu-id="36def-568">5</span><span class="sxs-lookup"><span data-stu-id="36def-568">5</span></span>

<span data-ttu-id="36def-569">6</span><span class="sxs-lookup"><span data-stu-id="36def-569">6</span></span>

<span data-ttu-id="36def-570">7</span><span class="sxs-lookup"><span data-stu-id="36def-570">7</span></span>

<span data-ttu-id="36def-571">8</span><span class="sxs-lookup"><span data-stu-id="36def-571">8</span></span>

<span data-ttu-id="36def-572">9</span><span class="sxs-lookup"><span data-stu-id="36def-572">9</span></span>

<span data-ttu-id="36def-573">2</span><span class="sxs-lookup"><span data-stu-id="36def-573">2</span></span><br/> <span data-ttu-id="36def-574">0</span><span class="sxs-lookup"><span data-stu-id="36def-574">0</span></span><br/>

<span data-ttu-id="36def-575">1</span><span class="sxs-lookup"><span data-stu-id="36def-575">1</span></span>

<span data-ttu-id="36def-576">2</span><span class="sxs-lookup"><span data-stu-id="36def-576">2</span></span>

<span data-ttu-id="36def-577">3</span><span class="sxs-lookup"><span data-stu-id="36def-577">3</span></span>

<span data-ttu-id="36def-578">4</span><span class="sxs-lookup"><span data-stu-id="36def-578">4</span></span>

<span data-ttu-id="36def-579">5</span><span class="sxs-lookup"><span data-stu-id="36def-579">5</span></span>

<span data-ttu-id="36def-580">6</span><span class="sxs-lookup"><span data-stu-id="36def-580">6</span></span>

<span data-ttu-id="36def-581">7</span><span class="sxs-lookup"><span data-stu-id="36def-581">7</span></span>

<span data-ttu-id="36def-582">8</span><span class="sxs-lookup"><span data-stu-id="36def-582">8</span></span>

<span data-ttu-id="36def-583">9</span><span class="sxs-lookup"><span data-stu-id="36def-583">9</span></span>

<span data-ttu-id="36def-584">3</span><span class="sxs-lookup"><span data-stu-id="36def-584">3</span></span><br/> <span data-ttu-id="36def-585">0</span><span class="sxs-lookup"><span data-stu-id="36def-585">0</span></span><br/>

<span data-ttu-id="36def-586">1</span><span class="sxs-lookup"><span data-stu-id="36def-586">1</span></span>

<span data-ttu-id="36def-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="36def-587">ccLen</span></span>

<span data-ttu-id="36def-588">字串 (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-588">string (variable, optional)</span></span>



 

<span data-ttu-id="36def-589">**ccLen**：不帶正負號的32位整數，表示字串欄位的大小（以 Unicode 字元表示）。</span><span class="sxs-lookup"><span data-stu-id="36def-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="36def-590">若為空字串，則必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="36def-591">**字串**：以 Null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="36def-592">2.2.1.1.1 CBaseStorageVariant 結構</span><span class="sxs-lookup"><span data-stu-id="36def-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="36def-593">下列結構會在 CBaseStorageVariant 結構中使用。</span><span class="sxs-lookup"><span data-stu-id="36def-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="36def-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="36def-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="36def-595">DECIMAL 用來表示具有固定有效位數和固定小數位數的精確數值。</span><span class="sxs-lookup"><span data-stu-id="36def-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="36def-596">當 vType 設定為 VT \_ DECIMAL (0x0000E) 時，CBaseStorageVariant 的 vData1 和 vData2 欄位必須解釋如下：</span><span class="sxs-lookup"><span data-stu-id="36def-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="36def-597">**vData1**：小數點右邊的位數。</span><span class="sxs-lookup"><span data-stu-id="36def-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="36def-598">必須在0到28的範圍內。</span><span class="sxs-lookup"><span data-stu-id="36def-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="36def-599">**vData2**：數位值的正負號。</span><span class="sxs-lookup"><span data-stu-id="36def-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="36def-600">如果是正數，則設定為0x00，如果是負數，則為0x80。</span><span class="sxs-lookup"><span data-stu-id="36def-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="36def-601">VValue 欄位的格式為：</span><span class="sxs-lookup"><span data-stu-id="36def-601">The format of the vValue field is:</span></span>



<span data-ttu-id="36def-602">0</span><span class="sxs-lookup"><span data-stu-id="36def-602">0</span></span>

<span data-ttu-id="36def-603">1</span><span class="sxs-lookup"><span data-stu-id="36def-603">1</span></span>

<span data-ttu-id="36def-604">2</span><span class="sxs-lookup"><span data-stu-id="36def-604">2</span></span>

<span data-ttu-id="36def-605">3</span><span class="sxs-lookup"><span data-stu-id="36def-605">3</span></span>

<span data-ttu-id="36def-606">4</span><span class="sxs-lookup"><span data-stu-id="36def-606">4</span></span>

<span data-ttu-id="36def-607">5</span><span class="sxs-lookup"><span data-stu-id="36def-607">5</span></span>

<span data-ttu-id="36def-608">6</span><span class="sxs-lookup"><span data-stu-id="36def-608">6</span></span>

<span data-ttu-id="36def-609">7</span><span class="sxs-lookup"><span data-stu-id="36def-609">7</span></span>

<span data-ttu-id="36def-610">8</span><span class="sxs-lookup"><span data-stu-id="36def-610">8</span></span>

<span data-ttu-id="36def-611">9</span><span class="sxs-lookup"><span data-stu-id="36def-611">9</span></span>

<span data-ttu-id="36def-612">1</span><span class="sxs-lookup"><span data-stu-id="36def-612">1</span></span><br/> <span data-ttu-id="36def-613">0</span><span class="sxs-lookup"><span data-stu-id="36def-613">0</span></span><br/>

<span data-ttu-id="36def-614">1</span><span class="sxs-lookup"><span data-stu-id="36def-614">1</span></span>

<span data-ttu-id="36def-615">2</span><span class="sxs-lookup"><span data-stu-id="36def-615">2</span></span>

<span data-ttu-id="36def-616">3</span><span class="sxs-lookup"><span data-stu-id="36def-616">3</span></span>

<span data-ttu-id="36def-617">4</span><span class="sxs-lookup"><span data-stu-id="36def-617">4</span></span>

<span data-ttu-id="36def-618">5</span><span class="sxs-lookup"><span data-stu-id="36def-618">5</span></span>

<span data-ttu-id="36def-619">6</span><span class="sxs-lookup"><span data-stu-id="36def-619">6</span></span>

<span data-ttu-id="36def-620">7</span><span class="sxs-lookup"><span data-stu-id="36def-620">7</span></span>

<span data-ttu-id="36def-621">8</span><span class="sxs-lookup"><span data-stu-id="36def-621">8</span></span>

<span data-ttu-id="36def-622">9</span><span class="sxs-lookup"><span data-stu-id="36def-622">9</span></span>

<span data-ttu-id="36def-623">2</span><span class="sxs-lookup"><span data-stu-id="36def-623">2</span></span><br/> <span data-ttu-id="36def-624">0</span><span class="sxs-lookup"><span data-stu-id="36def-624">0</span></span><br/>

<span data-ttu-id="36def-625">1</span><span class="sxs-lookup"><span data-stu-id="36def-625">1</span></span>

<span data-ttu-id="36def-626">2</span><span class="sxs-lookup"><span data-stu-id="36def-626">2</span></span>

<span data-ttu-id="36def-627">3</span><span class="sxs-lookup"><span data-stu-id="36def-627">3</span></span>

<span data-ttu-id="36def-628">4</span><span class="sxs-lookup"><span data-stu-id="36def-628">4</span></span>

<span data-ttu-id="36def-629">5</span><span class="sxs-lookup"><span data-stu-id="36def-629">5</span></span>

<span data-ttu-id="36def-630">6</span><span class="sxs-lookup"><span data-stu-id="36def-630">6</span></span>

<span data-ttu-id="36def-631">7</span><span class="sxs-lookup"><span data-stu-id="36def-631">7</span></span>

<span data-ttu-id="36def-632">8</span><span class="sxs-lookup"><span data-stu-id="36def-632">8</span></span>

<span data-ttu-id="36def-633">9</span><span class="sxs-lookup"><span data-stu-id="36def-633">9</span></span>

<span data-ttu-id="36def-634">3</span><span class="sxs-lookup"><span data-stu-id="36def-634">3</span></span><br/> <span data-ttu-id="36def-635">0</span><span class="sxs-lookup"><span data-stu-id="36def-635">0</span></span><br/>

<span data-ttu-id="36def-636">1</span><span class="sxs-lookup"><span data-stu-id="36def-636">1</span></span>

<span data-ttu-id="36def-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="36def-637">Hi32</span></span>

<span data-ttu-id="36def-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="36def-638">Lo32</span></span>

<span data-ttu-id="36def-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="36def-639">Mid32</span></span>



 

<span data-ttu-id="36def-640">**Hi32**：96位整數的最高32位。</span><span class="sxs-lookup"><span data-stu-id="36def-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="36def-641">**Lo32**：96位整數的最低32位。</span><span class="sxs-lookup"><span data-stu-id="36def-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="36def-642">**Mid32**：96位整數的中間32位。</span><span class="sxs-lookup"><span data-stu-id="36def-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="36def-643">2.2.1.1.1.2 VT \_ 向量</span><span class="sxs-lookup"><span data-stu-id="36def-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="36def-644">VT \_ 向量用來傳遞一維陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="36def-645">0</span><span class="sxs-lookup"><span data-stu-id="36def-645">0</span></span>

<span data-ttu-id="36def-646">1</span><span class="sxs-lookup"><span data-stu-id="36def-646">1</span></span>

<span data-ttu-id="36def-647">2</span><span class="sxs-lookup"><span data-stu-id="36def-647">2</span></span>

<span data-ttu-id="36def-648">3</span><span class="sxs-lookup"><span data-stu-id="36def-648">3</span></span>

<span data-ttu-id="36def-649">4</span><span class="sxs-lookup"><span data-stu-id="36def-649">4</span></span>

<span data-ttu-id="36def-650">5</span><span class="sxs-lookup"><span data-stu-id="36def-650">5</span></span>

<span data-ttu-id="36def-651">6</span><span class="sxs-lookup"><span data-stu-id="36def-651">6</span></span>

<span data-ttu-id="36def-652">7</span><span class="sxs-lookup"><span data-stu-id="36def-652">7</span></span>

<span data-ttu-id="36def-653">8</span><span class="sxs-lookup"><span data-stu-id="36def-653">8</span></span>

<span data-ttu-id="36def-654">9</span><span class="sxs-lookup"><span data-stu-id="36def-654">9</span></span>

<span data-ttu-id="36def-655">1</span><span class="sxs-lookup"><span data-stu-id="36def-655">1</span></span><br/> <span data-ttu-id="36def-656">0</span><span class="sxs-lookup"><span data-stu-id="36def-656">0</span></span><br/>

<span data-ttu-id="36def-657">1</span><span class="sxs-lookup"><span data-stu-id="36def-657">1</span></span>

<span data-ttu-id="36def-658">2</span><span class="sxs-lookup"><span data-stu-id="36def-658">2</span></span>

<span data-ttu-id="36def-659">3</span><span class="sxs-lookup"><span data-stu-id="36def-659">3</span></span>

<span data-ttu-id="36def-660">4</span><span class="sxs-lookup"><span data-stu-id="36def-660">4</span></span>

<span data-ttu-id="36def-661">5</span><span class="sxs-lookup"><span data-stu-id="36def-661">5</span></span>

<span data-ttu-id="36def-662">6</span><span class="sxs-lookup"><span data-stu-id="36def-662">6</span></span>

<span data-ttu-id="36def-663">7</span><span class="sxs-lookup"><span data-stu-id="36def-663">7</span></span>

<span data-ttu-id="36def-664">8</span><span class="sxs-lookup"><span data-stu-id="36def-664">8</span></span>

<span data-ttu-id="36def-665">9</span><span class="sxs-lookup"><span data-stu-id="36def-665">9</span></span>

<span data-ttu-id="36def-666">2</span><span class="sxs-lookup"><span data-stu-id="36def-666">2</span></span><br/> <span data-ttu-id="36def-667">0</span><span class="sxs-lookup"><span data-stu-id="36def-667">0</span></span><br/>

<span data-ttu-id="36def-668">1</span><span class="sxs-lookup"><span data-stu-id="36def-668">1</span></span>

<span data-ttu-id="36def-669">2</span><span class="sxs-lookup"><span data-stu-id="36def-669">2</span></span>

<span data-ttu-id="36def-670">3</span><span class="sxs-lookup"><span data-stu-id="36def-670">3</span></span>

<span data-ttu-id="36def-671">4</span><span class="sxs-lookup"><span data-stu-id="36def-671">4</span></span>

<span data-ttu-id="36def-672">5</span><span class="sxs-lookup"><span data-stu-id="36def-672">5</span></span>

<span data-ttu-id="36def-673">6</span><span class="sxs-lookup"><span data-stu-id="36def-673">6</span></span>

<span data-ttu-id="36def-674">7</span><span class="sxs-lookup"><span data-stu-id="36def-674">7</span></span>

<span data-ttu-id="36def-675">8</span><span class="sxs-lookup"><span data-stu-id="36def-675">8</span></span>

<span data-ttu-id="36def-676">9</span><span class="sxs-lookup"><span data-stu-id="36def-676">9</span></span>

<span data-ttu-id="36def-677">3</span><span class="sxs-lookup"><span data-stu-id="36def-677">3</span></span><br/> <span data-ttu-id="36def-678">0</span><span class="sxs-lookup"><span data-stu-id="36def-678">0</span></span><br/>

<span data-ttu-id="36def-679">1</span><span class="sxs-lookup"><span data-stu-id="36def-679">1</span></span>

<span data-ttu-id="36def-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="36def-680">vVectorElements</span></span>

<span data-ttu-id="36def-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="36def-681">vVectorData</span></span>



 

<span data-ttu-id="36def-682">**vVectorElements**：不帶正負號的32位整數，指出 vVectorData 欄位中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36def-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="36def-683">**vVectorData**：專案的陣列，其中包含已清除0x1000 位之 vType 所指出的型別。</span><span class="sxs-lookup"><span data-stu-id="36def-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="36def-684">您可以從固定長度的資料類型資料表取得個別固定長度專案的大小，如2.2.1.1 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="36def-685">這個欄位的長度（以位元組為單位）可以藉由將 vVectorElements 乘以個別專案的大小來計算。</span><span class="sxs-lookup"><span data-stu-id="36def-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="36def-686">針對可變長度的資料類型，vVectorData 包含一連串連續封送處理的簡單類型，其中的類型是由 vType （已清除0x1000 位）所表示。</span><span class="sxs-lookup"><span data-stu-id="36def-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="36def-687">這包括以 vType VT ARRAY VT VARIANT 表示的特殊案例 \_ \| \_ (例如 0x100C) 。</span><span class="sxs-lookup"><span data-stu-id="36def-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="36def-688">VVectorData 欄位中的元素必須以0到3個填補位元組分隔，讓每個專案從包含這個陣列的訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="36def-689">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="36def-690">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-691">如果 vType 設定為 VT \_ ARRAY \| vt \_ VARIANT，則此序列中的專案類型為 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="36def-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="36def-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="36def-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="36def-693">SAFEARRAY 用來傳遞多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="36def-694">結構包含陣列大小資訊，以及陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="36def-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="36def-695">0</span><span class="sxs-lookup"><span data-stu-id="36def-695">0</span></span>

<span data-ttu-id="36def-696">1</span><span class="sxs-lookup"><span data-stu-id="36def-696">1</span></span>

<span data-ttu-id="36def-697">2</span><span class="sxs-lookup"><span data-stu-id="36def-697">2</span></span>

<span data-ttu-id="36def-698">3</span><span class="sxs-lookup"><span data-stu-id="36def-698">3</span></span>

<span data-ttu-id="36def-699">4</span><span class="sxs-lookup"><span data-stu-id="36def-699">4</span></span>

<span data-ttu-id="36def-700">5</span><span class="sxs-lookup"><span data-stu-id="36def-700">5</span></span>

<span data-ttu-id="36def-701">6</span><span class="sxs-lookup"><span data-stu-id="36def-701">6</span></span>

<span data-ttu-id="36def-702">7</span><span class="sxs-lookup"><span data-stu-id="36def-702">7</span></span>

<span data-ttu-id="36def-703">8</span><span class="sxs-lookup"><span data-stu-id="36def-703">8</span></span>

<span data-ttu-id="36def-704">9</span><span class="sxs-lookup"><span data-stu-id="36def-704">9</span></span>

<span data-ttu-id="36def-705">1</span><span class="sxs-lookup"><span data-stu-id="36def-705">1</span></span><br/> <span data-ttu-id="36def-706">0</span><span class="sxs-lookup"><span data-stu-id="36def-706">0</span></span><br/>

<span data-ttu-id="36def-707">1</span><span class="sxs-lookup"><span data-stu-id="36def-707">1</span></span>

<span data-ttu-id="36def-708">2</span><span class="sxs-lookup"><span data-stu-id="36def-708">2</span></span>

<span data-ttu-id="36def-709">3</span><span class="sxs-lookup"><span data-stu-id="36def-709">3</span></span>

<span data-ttu-id="36def-710">4</span><span class="sxs-lookup"><span data-stu-id="36def-710">4</span></span>

<span data-ttu-id="36def-711">5</span><span class="sxs-lookup"><span data-stu-id="36def-711">5</span></span>

<span data-ttu-id="36def-712">6</span><span class="sxs-lookup"><span data-stu-id="36def-712">6</span></span>

<span data-ttu-id="36def-713">7</span><span class="sxs-lookup"><span data-stu-id="36def-713">7</span></span>

<span data-ttu-id="36def-714">8</span><span class="sxs-lookup"><span data-stu-id="36def-714">8</span></span>

<span data-ttu-id="36def-715">9</span><span class="sxs-lookup"><span data-stu-id="36def-715">9</span></span>

<span data-ttu-id="36def-716">2</span><span class="sxs-lookup"><span data-stu-id="36def-716">2</span></span><br/> <span data-ttu-id="36def-717">0</span><span class="sxs-lookup"><span data-stu-id="36def-717">0</span></span><br/>

<span data-ttu-id="36def-718">1</span><span class="sxs-lookup"><span data-stu-id="36def-718">1</span></span>

<span data-ttu-id="36def-719">2</span><span class="sxs-lookup"><span data-stu-id="36def-719">2</span></span>

<span data-ttu-id="36def-720">3</span><span class="sxs-lookup"><span data-stu-id="36def-720">3</span></span>

<span data-ttu-id="36def-721">4</span><span class="sxs-lookup"><span data-stu-id="36def-721">4</span></span>

<span data-ttu-id="36def-722">5</span><span class="sxs-lookup"><span data-stu-id="36def-722">5</span></span>

<span data-ttu-id="36def-723">6</span><span class="sxs-lookup"><span data-stu-id="36def-723">6</span></span>

<span data-ttu-id="36def-724">7</span><span class="sxs-lookup"><span data-stu-id="36def-724">7</span></span>

<span data-ttu-id="36def-725">8</span><span class="sxs-lookup"><span data-stu-id="36def-725">8</span></span>

<span data-ttu-id="36def-726">9</span><span class="sxs-lookup"><span data-stu-id="36def-726">9</span></span>

<span data-ttu-id="36def-727">3</span><span class="sxs-lookup"><span data-stu-id="36def-727">3</span></span><br/> <span data-ttu-id="36def-728">0</span><span class="sxs-lookup"><span data-stu-id="36def-728">0</span></span><br/>

<span data-ttu-id="36def-729">1</span><span class="sxs-lookup"><span data-stu-id="36def-729">1</span></span>

<span data-ttu-id="36def-730">cDims</span><span class="sxs-lookup"><span data-stu-id="36def-730">cDims</span></span>

<span data-ttu-id="36def-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="36def-731">fFeatures</span></span>

<span data-ttu-id="36def-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="36def-732">cbElements</span></span>

<span data-ttu-id="36def-733">Rgsabound (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-733">Rgsabound (variable)</span></span>

<span data-ttu-id="36def-734">vData (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-734">vData (variable)</span></span>



 

<span data-ttu-id="36def-735">**cDims**：不帶正負號的16位整數，表示多維陣列的維度數目。</span><span class="sxs-lookup"><span data-stu-id="36def-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="36def-736">**fFeatures**：16位位。</span><span class="sxs-lookup"><span data-stu-id="36def-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="36def-737">這些值代表由上層應用程式定義的功能，必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="36def-738">**cbElements**：32位不帶正負號的整數，指定陣列中每個元素的大小。</span><span class="sxs-lookup"><span data-stu-id="36def-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="36def-739">**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，此結構是在 SAFEARRAY 的每個維度的區段2.2.1.1.1.4 中指定的。</span><span class="sxs-lookup"><span data-stu-id="36def-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="36def-740">這個陣列的第一個是最左邊的維度，最後是最右邊的維度。</span><span class="sxs-lookup"><span data-stu-id="36def-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="36def-741">**vData**：特定類型之封送處理專案的向量，由包含 CBaseStorageVariant 的 vType 所表示，並已清除位0x2000。</span><span class="sxs-lookup"><span data-stu-id="36def-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="36def-742">vData 的封送處理方式類似于 VT \_ 向量（如區段2.2.1.1.1.2 中所指定），差別在於專案數不會儲存在向量前方。</span><span class="sxs-lookup"><span data-stu-id="36def-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="36def-743">而是將 cElements 值乘以 Rgsabound 欄位中提供的所有安全陣列界限，來計算專案數。</span><span class="sxs-lookup"><span data-stu-id="36def-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="36def-744">專案會以維度的順序儲存在向量中，並以最右邊的維度開始反覆運算。</span><span class="sxs-lookup"><span data-stu-id="36def-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="36def-745">下圖以視覺方式呈現二維陣列範例。</span><span class="sxs-lookup"><span data-stu-id="36def-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="36def-746">第一個維度的 cElements 等於 4 (水準表示) ，而 lLbound 等於0，而第二個維度的 cElements 等於 2 (表示垂直) ，lLbound 等於0。</span><span class="sxs-lookup"><span data-stu-id="36def-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="36def-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-747">0x00000001</span></span> | <span data-ttu-id="36def-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-748">0x00000002</span></span> | <span data-ttu-id="36def-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-749">0x00000003</span></span> | <span data-ttu-id="36def-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="36def-750">0x00000005</span></span> |
| <span data-ttu-id="36def-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-751">0x00000007</span></span> | <span data-ttu-id="36def-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="36def-752">0x00000011</span></span> | <span data-ttu-id="36def-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="36def-753">0x00000013</span></span> | <span data-ttu-id="36def-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="36def-754">0x00000017</span></span> |



 

<span data-ttu-id="36def-755">使用上圖，vData 將包含下列順序：0x00000001、0x00000007、0x00000002、0x00000011、0x00000003、0x00000013、0x00000005、0x00000017 (先逐一查看最右邊的維度，然後再遞增下一個維度) 。</span><span class="sxs-lookup"><span data-stu-id="36def-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="36def-756">上述 Rgsabound (會記錄 cElements 和 Lbound) 為：0x00000004、0x00000000、0x00000002、0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="36def-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="36def-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="36def-758">SAFEARRAYBOUND 結構代表 SAFEARRAY 或 SAFEARRAY2 之一維度的範圍。</span><span class="sxs-lookup"><span data-stu-id="36def-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="36def-759">其格式為：</span><span class="sxs-lookup"><span data-stu-id="36def-759">Its format is:</span></span>



<span data-ttu-id="36def-760">0</span><span class="sxs-lookup"><span data-stu-id="36def-760">0</span></span>

<span data-ttu-id="36def-761">1</span><span class="sxs-lookup"><span data-stu-id="36def-761">1</span></span>

<span data-ttu-id="36def-762">2</span><span class="sxs-lookup"><span data-stu-id="36def-762">2</span></span>

<span data-ttu-id="36def-763">3</span><span class="sxs-lookup"><span data-stu-id="36def-763">3</span></span>

<span data-ttu-id="36def-764">4</span><span class="sxs-lookup"><span data-stu-id="36def-764">4</span></span>

<span data-ttu-id="36def-765">5</span><span class="sxs-lookup"><span data-stu-id="36def-765">5</span></span>

<span data-ttu-id="36def-766">6</span><span class="sxs-lookup"><span data-stu-id="36def-766">6</span></span>

<span data-ttu-id="36def-767">7</span><span class="sxs-lookup"><span data-stu-id="36def-767">7</span></span>

<span data-ttu-id="36def-768">8</span><span class="sxs-lookup"><span data-stu-id="36def-768">8</span></span>

<span data-ttu-id="36def-769">9</span><span class="sxs-lookup"><span data-stu-id="36def-769">9</span></span>

<span data-ttu-id="36def-770">1</span><span class="sxs-lookup"><span data-stu-id="36def-770">1</span></span><br/> <span data-ttu-id="36def-771">0</span><span class="sxs-lookup"><span data-stu-id="36def-771">0</span></span><br/>

<span data-ttu-id="36def-772">1</span><span class="sxs-lookup"><span data-stu-id="36def-772">1</span></span>

<span data-ttu-id="36def-773">2</span><span class="sxs-lookup"><span data-stu-id="36def-773">2</span></span>

<span data-ttu-id="36def-774">3</span><span class="sxs-lookup"><span data-stu-id="36def-774">3</span></span>

<span data-ttu-id="36def-775">4</span><span class="sxs-lookup"><span data-stu-id="36def-775">4</span></span>

<span data-ttu-id="36def-776">5</span><span class="sxs-lookup"><span data-stu-id="36def-776">5</span></span>

<span data-ttu-id="36def-777">6</span><span class="sxs-lookup"><span data-stu-id="36def-777">6</span></span>

<span data-ttu-id="36def-778">7</span><span class="sxs-lookup"><span data-stu-id="36def-778">7</span></span>

<span data-ttu-id="36def-779">8</span><span class="sxs-lookup"><span data-stu-id="36def-779">8</span></span>

<span data-ttu-id="36def-780">9</span><span class="sxs-lookup"><span data-stu-id="36def-780">9</span></span>

<span data-ttu-id="36def-781">2</span><span class="sxs-lookup"><span data-stu-id="36def-781">2</span></span><br/> <span data-ttu-id="36def-782">0</span><span class="sxs-lookup"><span data-stu-id="36def-782">0</span></span><br/>

<span data-ttu-id="36def-783">1</span><span class="sxs-lookup"><span data-stu-id="36def-783">1</span></span>

<span data-ttu-id="36def-784">2</span><span class="sxs-lookup"><span data-stu-id="36def-784">2</span></span>

<span data-ttu-id="36def-785">3</span><span class="sxs-lookup"><span data-stu-id="36def-785">3</span></span>

<span data-ttu-id="36def-786">4</span><span class="sxs-lookup"><span data-stu-id="36def-786">4</span></span>

<span data-ttu-id="36def-787">5</span><span class="sxs-lookup"><span data-stu-id="36def-787">5</span></span>

<span data-ttu-id="36def-788">6</span><span class="sxs-lookup"><span data-stu-id="36def-788">6</span></span>

<span data-ttu-id="36def-789">7</span><span class="sxs-lookup"><span data-stu-id="36def-789">7</span></span>

<span data-ttu-id="36def-790">8</span><span class="sxs-lookup"><span data-stu-id="36def-790">8</span></span>

<span data-ttu-id="36def-791">9</span><span class="sxs-lookup"><span data-stu-id="36def-791">9</span></span>

<span data-ttu-id="36def-792">3</span><span class="sxs-lookup"><span data-stu-id="36def-792">3</span></span><br/> <span data-ttu-id="36def-793">0</span><span class="sxs-lookup"><span data-stu-id="36def-793">0</span></span><br/>

<span data-ttu-id="36def-794">1</span><span class="sxs-lookup"><span data-stu-id="36def-794">1</span></span>

<span data-ttu-id="36def-795">cElements</span><span class="sxs-lookup"><span data-stu-id="36def-795">cElements</span></span>

<span data-ttu-id="36def-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="36def-796">lLbound</span></span>



 

<span data-ttu-id="36def-797">**cElements**：32位不帶正負號的整數，指定維度中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36def-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="36def-798">**lLbound**：32位不帶正負號的整數，指定維度的下限。</span><span class="sxs-lookup"><span data-stu-id="36def-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="36def-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="36def-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="36def-800">SAFEARRAY2 用來傳遞 SERIALIZEDPROPERTYVALUE 中的多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="36def-801">結構包含界限資訊和資料。</span><span class="sxs-lookup"><span data-stu-id="36def-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="36def-802">0</span><span class="sxs-lookup"><span data-stu-id="36def-802">0</span></span>

<span data-ttu-id="36def-803">1</span><span class="sxs-lookup"><span data-stu-id="36def-803">1</span></span>

<span data-ttu-id="36def-804">2</span><span class="sxs-lookup"><span data-stu-id="36def-804">2</span></span>

<span data-ttu-id="36def-805">3</span><span class="sxs-lookup"><span data-stu-id="36def-805">3</span></span>

<span data-ttu-id="36def-806">4</span><span class="sxs-lookup"><span data-stu-id="36def-806">4</span></span>

<span data-ttu-id="36def-807">5</span><span class="sxs-lookup"><span data-stu-id="36def-807">5</span></span>

<span data-ttu-id="36def-808">6</span><span class="sxs-lookup"><span data-stu-id="36def-808">6</span></span>

<span data-ttu-id="36def-809">7</span><span class="sxs-lookup"><span data-stu-id="36def-809">7</span></span>

<span data-ttu-id="36def-810">8</span><span class="sxs-lookup"><span data-stu-id="36def-810">8</span></span>

<span data-ttu-id="36def-811">9</span><span class="sxs-lookup"><span data-stu-id="36def-811">9</span></span>

<span data-ttu-id="36def-812">1</span><span class="sxs-lookup"><span data-stu-id="36def-812">1</span></span><br/> <span data-ttu-id="36def-813">0</span><span class="sxs-lookup"><span data-stu-id="36def-813">0</span></span><br/>

<span data-ttu-id="36def-814">1</span><span class="sxs-lookup"><span data-stu-id="36def-814">1</span></span>

<span data-ttu-id="36def-815">2</span><span class="sxs-lookup"><span data-stu-id="36def-815">2</span></span>

<span data-ttu-id="36def-816">3</span><span class="sxs-lookup"><span data-stu-id="36def-816">3</span></span>

<span data-ttu-id="36def-817">4</span><span class="sxs-lookup"><span data-stu-id="36def-817">4</span></span>

<span data-ttu-id="36def-818">5</span><span class="sxs-lookup"><span data-stu-id="36def-818">5</span></span>

<span data-ttu-id="36def-819">6</span><span class="sxs-lookup"><span data-stu-id="36def-819">6</span></span>

<span data-ttu-id="36def-820">7</span><span class="sxs-lookup"><span data-stu-id="36def-820">7</span></span>

<span data-ttu-id="36def-821">8</span><span class="sxs-lookup"><span data-stu-id="36def-821">8</span></span>

<span data-ttu-id="36def-822">9</span><span class="sxs-lookup"><span data-stu-id="36def-822">9</span></span>

<span data-ttu-id="36def-823">2</span><span class="sxs-lookup"><span data-stu-id="36def-823">2</span></span><br/> <span data-ttu-id="36def-824">0</span><span class="sxs-lookup"><span data-stu-id="36def-824">0</span></span><br/>

<span data-ttu-id="36def-825">1</span><span class="sxs-lookup"><span data-stu-id="36def-825">1</span></span>

<span data-ttu-id="36def-826">2</span><span class="sxs-lookup"><span data-stu-id="36def-826">2</span></span>

<span data-ttu-id="36def-827">3</span><span class="sxs-lookup"><span data-stu-id="36def-827">3</span></span>

<span data-ttu-id="36def-828">4</span><span class="sxs-lookup"><span data-stu-id="36def-828">4</span></span>

<span data-ttu-id="36def-829">5</span><span class="sxs-lookup"><span data-stu-id="36def-829">5</span></span>

<span data-ttu-id="36def-830">6</span><span class="sxs-lookup"><span data-stu-id="36def-830">6</span></span>

<span data-ttu-id="36def-831">7</span><span class="sxs-lookup"><span data-stu-id="36def-831">7</span></span>

<span data-ttu-id="36def-832">8</span><span class="sxs-lookup"><span data-stu-id="36def-832">8</span></span>

<span data-ttu-id="36def-833">9</span><span class="sxs-lookup"><span data-stu-id="36def-833">9</span></span>

<span data-ttu-id="36def-834">3</span><span class="sxs-lookup"><span data-stu-id="36def-834">3</span></span><br/> <span data-ttu-id="36def-835">0</span><span class="sxs-lookup"><span data-stu-id="36def-835">0</span></span><br/>

<span data-ttu-id="36def-836">1</span><span class="sxs-lookup"><span data-stu-id="36def-836">1</span></span>

<span data-ttu-id="36def-837">cDims</span><span class="sxs-lookup"><span data-stu-id="36def-837">cDims</span></span>

<span data-ttu-id="36def-838">Rgsabound (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-838">Rgsabound (variable)</span></span>

<span data-ttu-id="36def-839">vData (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-839">vData (variable)</span></span>



 

<span data-ttu-id="36def-840">**cDims**：不帶正負號的32位整數，表示 SAFEARRAY2 的維度數目。</span><span class="sxs-lookup"><span data-stu-id="36def-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="36def-841">**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，如 SAFEARRAY2 中每個維度的區段2.2.1.1.1.4 所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="36def-842">這個陣列的第一個是最左邊的維度，最後是最右邊的維度。</span><span class="sxs-lookup"><span data-stu-id="36def-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="36def-843">**vData**：特定類型之封送處理專案的向量，由包含 SERIALIZEDPROPERTYVALUE 的 dwType 所表示，並已清除位0x2000。</span><span class="sxs-lookup"><span data-stu-id="36def-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="36def-844">VData 的格式與在區段2.2.1.1.1.3 中針對 SAFEARRAY 的 vData 欄位指定的格式相同。</span><span class="sxs-lookup"><span data-stu-id="36def-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="36def-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="36def-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="36def-846">CFullPropSpec 結構包含屬性集 GUID 和屬性識別碼，可唯一識別屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="36def-847">0</span><span class="sxs-lookup"><span data-stu-id="36def-847">0</span></span>

<span data-ttu-id="36def-848">1</span><span class="sxs-lookup"><span data-stu-id="36def-848">1</span></span>

<span data-ttu-id="36def-849">2</span><span class="sxs-lookup"><span data-stu-id="36def-849">2</span></span>

<span data-ttu-id="36def-850">3</span><span class="sxs-lookup"><span data-stu-id="36def-850">3</span></span>

<span data-ttu-id="36def-851">4</span><span class="sxs-lookup"><span data-stu-id="36def-851">4</span></span>

<span data-ttu-id="36def-852">5</span><span class="sxs-lookup"><span data-stu-id="36def-852">5</span></span>

<span data-ttu-id="36def-853">6</span><span class="sxs-lookup"><span data-stu-id="36def-853">6</span></span>

<span data-ttu-id="36def-854">7</span><span class="sxs-lookup"><span data-stu-id="36def-854">7</span></span>

<span data-ttu-id="36def-855">8</span><span class="sxs-lookup"><span data-stu-id="36def-855">8</span></span>

<span data-ttu-id="36def-856">9</span><span class="sxs-lookup"><span data-stu-id="36def-856">9</span></span>

<span data-ttu-id="36def-857">1</span><span class="sxs-lookup"><span data-stu-id="36def-857">1</span></span><br/> <span data-ttu-id="36def-858">0</span><span class="sxs-lookup"><span data-stu-id="36def-858">0</span></span><br/>

<span data-ttu-id="36def-859">1</span><span class="sxs-lookup"><span data-stu-id="36def-859">1</span></span>

<span data-ttu-id="36def-860">2</span><span class="sxs-lookup"><span data-stu-id="36def-860">2</span></span>

<span data-ttu-id="36def-861">3</span><span class="sxs-lookup"><span data-stu-id="36def-861">3</span></span>

<span data-ttu-id="36def-862">4</span><span class="sxs-lookup"><span data-stu-id="36def-862">4</span></span>

<span data-ttu-id="36def-863">5</span><span class="sxs-lookup"><span data-stu-id="36def-863">5</span></span>

<span data-ttu-id="36def-864">6</span><span class="sxs-lookup"><span data-stu-id="36def-864">6</span></span>

<span data-ttu-id="36def-865">7</span><span class="sxs-lookup"><span data-stu-id="36def-865">7</span></span>

<span data-ttu-id="36def-866">8</span><span class="sxs-lookup"><span data-stu-id="36def-866">8</span></span>

<span data-ttu-id="36def-867">9</span><span class="sxs-lookup"><span data-stu-id="36def-867">9</span></span>

<span data-ttu-id="36def-868">2</span><span class="sxs-lookup"><span data-stu-id="36def-868">2</span></span><br/> <span data-ttu-id="36def-869">0</span><span class="sxs-lookup"><span data-stu-id="36def-869">0</span></span><br/>

<span data-ttu-id="36def-870">1</span><span class="sxs-lookup"><span data-stu-id="36def-870">1</span></span>

<span data-ttu-id="36def-871">2</span><span class="sxs-lookup"><span data-stu-id="36def-871">2</span></span>

<span data-ttu-id="36def-872">3</span><span class="sxs-lookup"><span data-stu-id="36def-872">3</span></span>

<span data-ttu-id="36def-873">4</span><span class="sxs-lookup"><span data-stu-id="36def-873">4</span></span>

<span data-ttu-id="36def-874">5</span><span class="sxs-lookup"><span data-stu-id="36def-874">5</span></span>

<span data-ttu-id="36def-875">6</span><span class="sxs-lookup"><span data-stu-id="36def-875">6</span></span>

<span data-ttu-id="36def-876">7</span><span class="sxs-lookup"><span data-stu-id="36def-876">7</span></span>

<span data-ttu-id="36def-877">8</span><span class="sxs-lookup"><span data-stu-id="36def-877">8</span></span>

<span data-ttu-id="36def-878">9</span><span class="sxs-lookup"><span data-stu-id="36def-878">9</span></span>

<span data-ttu-id="36def-879">3</span><span class="sxs-lookup"><span data-stu-id="36def-879">3</span></span><br/> <span data-ttu-id="36def-880">0</span><span class="sxs-lookup"><span data-stu-id="36def-880">0</span></span><br/>

<span data-ttu-id="36def-881">1</span><span class="sxs-lookup"><span data-stu-id="36def-881">1</span></span>

<span data-ttu-id="36def-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="36def-882">\_guidPropSet</span></span>

<span data-ttu-id="36def-883">...</span><span class="sxs-lookup"><span data-stu-id="36def-883">...</span></span>

<span data-ttu-id="36def-884">...</span><span class="sxs-lookup"><span data-stu-id="36def-884">...</span></span>

<span data-ttu-id="36def-885">...</span><span class="sxs-lookup"><span data-stu-id="36def-885">...</span></span>

<span data-ttu-id="36def-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="36def-886">ulKind</span></span>

<span data-ttu-id="36def-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="36def-887">PrSpec</span></span>

<span data-ttu-id="36def-888">屬性名稱 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-888">Property name (variable)</span></span>



 

<span data-ttu-id="36def-889">**\_ guidPropSet**：屬性所屬之屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="36def-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="36def-890">**ulKind**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-891">下列其中一個值，表示 PrSpec 的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="36def-892">值</span><span class="sxs-lookup"><span data-stu-id="36def-892">Value</span></span>                                            | <span data-ttu-id="36def-893">意義</span><span class="sxs-lookup"><span data-stu-id="36def-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-894">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="36def-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="36def-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-895">0x00000000</span></span><br/> | <span data-ttu-id="36def-896">PrSpec 欄位會指定 [屬性名稱] 欄位中的非 Null 字元數目。</span><span class="sxs-lookup"><span data-stu-id="36def-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="36def-897">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="36def-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="36def-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-898">0x00000001</span></span><br/>  | <span data-ttu-id="36def-899">PrSpec 欄位會指定屬性識別碼 (PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="36def-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="36def-900">**PrSpec**：具有意義的32位不帶正負號整數，如 ulKind 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="36def-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="36def-901">**屬性名稱**：如果 ulKind 設為 PRSPEC \_ PROPID，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="36def-902">如果 ulKind 設定為 PRSPEC \_ LPWSTR，則這個欄位必須包含 PRSPEC 非 Null Unicode 字元的不區分大小寫陣列，其中包含屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="36def-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="36def-904">CContentRestriction 結構包含要與屬性快取中的屬性相符的字串。</span><span class="sxs-lookup"><span data-stu-id="36def-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="36def-905">0</span><span class="sxs-lookup"><span data-stu-id="36def-905">0</span></span>

<span data-ttu-id="36def-906">1</span><span class="sxs-lookup"><span data-stu-id="36def-906">1</span></span>

<span data-ttu-id="36def-907">2</span><span class="sxs-lookup"><span data-stu-id="36def-907">2</span></span>

<span data-ttu-id="36def-908">3</span><span class="sxs-lookup"><span data-stu-id="36def-908">3</span></span>

<span data-ttu-id="36def-909">4</span><span class="sxs-lookup"><span data-stu-id="36def-909">4</span></span>

<span data-ttu-id="36def-910">5</span><span class="sxs-lookup"><span data-stu-id="36def-910">5</span></span>

<span data-ttu-id="36def-911">6</span><span class="sxs-lookup"><span data-stu-id="36def-911">6</span></span>

<span data-ttu-id="36def-912">7</span><span class="sxs-lookup"><span data-stu-id="36def-912">7</span></span>

<span data-ttu-id="36def-913">8</span><span class="sxs-lookup"><span data-stu-id="36def-913">8</span></span>

<span data-ttu-id="36def-914">9</span><span class="sxs-lookup"><span data-stu-id="36def-914">9</span></span>

<span data-ttu-id="36def-915">1</span><span class="sxs-lookup"><span data-stu-id="36def-915">1</span></span><br/> <span data-ttu-id="36def-916">0</span><span class="sxs-lookup"><span data-stu-id="36def-916">0</span></span><br/>

<span data-ttu-id="36def-917">1</span><span class="sxs-lookup"><span data-stu-id="36def-917">1</span></span>

<span data-ttu-id="36def-918">2</span><span class="sxs-lookup"><span data-stu-id="36def-918">2</span></span>

<span data-ttu-id="36def-919">3</span><span class="sxs-lookup"><span data-stu-id="36def-919">3</span></span>

<span data-ttu-id="36def-920">4</span><span class="sxs-lookup"><span data-stu-id="36def-920">4</span></span>

<span data-ttu-id="36def-921">5</span><span class="sxs-lookup"><span data-stu-id="36def-921">5</span></span>

<span data-ttu-id="36def-922">6</span><span class="sxs-lookup"><span data-stu-id="36def-922">6</span></span>

<span data-ttu-id="36def-923">7</span><span class="sxs-lookup"><span data-stu-id="36def-923">7</span></span>

<span data-ttu-id="36def-924">8</span><span class="sxs-lookup"><span data-stu-id="36def-924">8</span></span>

<span data-ttu-id="36def-925">9</span><span class="sxs-lookup"><span data-stu-id="36def-925">9</span></span>

<span data-ttu-id="36def-926">2</span><span class="sxs-lookup"><span data-stu-id="36def-926">2</span></span><br/> <span data-ttu-id="36def-927">0</span><span class="sxs-lookup"><span data-stu-id="36def-927">0</span></span><br/>

<span data-ttu-id="36def-928">1</span><span class="sxs-lookup"><span data-stu-id="36def-928">1</span></span>

<span data-ttu-id="36def-929">2</span><span class="sxs-lookup"><span data-stu-id="36def-929">2</span></span>

<span data-ttu-id="36def-930">3</span><span class="sxs-lookup"><span data-stu-id="36def-930">3</span></span>

<span data-ttu-id="36def-931">4</span><span class="sxs-lookup"><span data-stu-id="36def-931">4</span></span>

<span data-ttu-id="36def-932">5</span><span class="sxs-lookup"><span data-stu-id="36def-932">5</span></span>

<span data-ttu-id="36def-933">6</span><span class="sxs-lookup"><span data-stu-id="36def-933">6</span></span>

<span data-ttu-id="36def-934">7</span><span class="sxs-lookup"><span data-stu-id="36def-934">7</span></span>

<span data-ttu-id="36def-935">8</span><span class="sxs-lookup"><span data-stu-id="36def-935">8</span></span>

<span data-ttu-id="36def-936">9</span><span class="sxs-lookup"><span data-stu-id="36def-936">9</span></span>

<span data-ttu-id="36def-937">3</span><span class="sxs-lookup"><span data-stu-id="36def-937">3</span></span><br/> <span data-ttu-id="36def-938">0</span><span class="sxs-lookup"><span data-stu-id="36def-938">0</span></span><br/>

<span data-ttu-id="36def-939">1</span><span class="sxs-lookup"><span data-stu-id="36def-939">1</span></span>

<span data-ttu-id="36def-940">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-940">\_Property (variable)</span></span>

<span data-ttu-id="36def-941">...</span><span class="sxs-lookup"><span data-stu-id="36def-941">...</span></span>

<span data-ttu-id="36def-942">Padding1 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-942">Padding1 (variable)</span></span>

<span data-ttu-id="36def-943">副本</span><span class="sxs-lookup"><span data-stu-id="36def-943">Cc</span></span>

<span data-ttu-id="36def-944">\_pwcsPhrase (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="36def-945">...</span><span class="sxs-lookup"><span data-stu-id="36def-945">...</span></span>

<span data-ttu-id="36def-946">Padding2 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-946">Padding2 (variable)</span></span>

<span data-ttu-id="36def-947">lcid</span><span class="sxs-lookup"><span data-stu-id="36def-947">lcid</span></span>

<span data-ttu-id="36def-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="36def-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="36def-949">**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.2 中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="36def-950">這個欄位指出要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="36def-951">**Padding1**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-952">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-953">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-954">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-955">**Cc**：32位不帶正負號的整數，指定 pwcsPhrase 欄位中的字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="36def-956">**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="36def-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="36def-957">此欄位不得為空白。</span><span class="sxs-lookup"><span data-stu-id="36def-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="36def-958">Cc 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="36def-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="36def-959">**Padding2**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-960">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-961">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-962">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-963">**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="36def-964">**\_ ulGenerateMethod**：32位不帶正負號的整數，指定產生替代字表單時要使用的方法</span><span class="sxs-lookup"><span data-stu-id="36def-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="36def-965">值</span><span class="sxs-lookup"><span data-stu-id="36def-965">Value</span></span>                                                       | <span data-ttu-id="36def-966">意義</span><span class="sxs-lookup"><span data-stu-id="36def-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-967">產生 \_ 精確的方法 \_</span><span class="sxs-lookup"><span data-stu-id="36def-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="36def-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-968">0x00000000</span></span><br/>    | <span data-ttu-id="36def-969">完全相符。</span><span class="sxs-lookup"><span data-stu-id="36def-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="36def-970">產生 \_ 方法 \_ 前置詞</span><span class="sxs-lookup"><span data-stu-id="36def-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="36def-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-971">0x00000001</span></span> <br/>  | <span data-ttu-id="36def-972">前置詞相符。</span><span class="sxs-lookup"><span data-stu-id="36def-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="36def-973">產生 \_ 方法 \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="36def-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="36def-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-974">0x00000002</span></span><br/> | <span data-ttu-id="36def-975">符合單字的 inflections。</span><span class="sxs-lookup"><span data-stu-id="36def-975">Matches inflections of a word.</span></span> <span data-ttu-id="36def-976">單字的變化是已根據指定語言的語言規則修改過的相同語音部分中的根字組變數。</span><span class="sxs-lookup"><span data-stu-id="36def-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="36def-977">例如，以英文的動詞「泳道」（inflections）包含「泳道」、「游泳」、「游泳」和「swam」。</span><span class="sxs-lookup"><span data-stu-id="36def-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="36def-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="36def-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="36def-979">CKey 結構包含屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="36def-980">0</span><span class="sxs-lookup"><span data-stu-id="36def-980">0</span></span>

<span data-ttu-id="36def-981">1</span><span class="sxs-lookup"><span data-stu-id="36def-981">1</span></span>

<span data-ttu-id="36def-982">2</span><span class="sxs-lookup"><span data-stu-id="36def-982">2</span></span>

<span data-ttu-id="36def-983">3</span><span class="sxs-lookup"><span data-stu-id="36def-983">3</span></span>

<span data-ttu-id="36def-984">4</span><span class="sxs-lookup"><span data-stu-id="36def-984">4</span></span>

<span data-ttu-id="36def-985">5</span><span class="sxs-lookup"><span data-stu-id="36def-985">5</span></span>

<span data-ttu-id="36def-986">6</span><span class="sxs-lookup"><span data-stu-id="36def-986">6</span></span>

<span data-ttu-id="36def-987">7</span><span class="sxs-lookup"><span data-stu-id="36def-987">7</span></span>

<span data-ttu-id="36def-988">8</span><span class="sxs-lookup"><span data-stu-id="36def-988">8</span></span>

<span data-ttu-id="36def-989">9</span><span class="sxs-lookup"><span data-stu-id="36def-989">9</span></span>

<span data-ttu-id="36def-990">1</span><span class="sxs-lookup"><span data-stu-id="36def-990">1</span></span><br/> <span data-ttu-id="36def-991">0</span><span class="sxs-lookup"><span data-stu-id="36def-991">0</span></span><br/>

<span data-ttu-id="36def-992">1</span><span class="sxs-lookup"><span data-stu-id="36def-992">1</span></span>

<span data-ttu-id="36def-993">2</span><span class="sxs-lookup"><span data-stu-id="36def-993">2</span></span>

<span data-ttu-id="36def-994">3</span><span class="sxs-lookup"><span data-stu-id="36def-994">3</span></span>

<span data-ttu-id="36def-995">4</span><span class="sxs-lookup"><span data-stu-id="36def-995">4</span></span>

<span data-ttu-id="36def-996">5</span><span class="sxs-lookup"><span data-stu-id="36def-996">5</span></span>

<span data-ttu-id="36def-997">6</span><span class="sxs-lookup"><span data-stu-id="36def-997">6</span></span>

<span data-ttu-id="36def-998">7</span><span class="sxs-lookup"><span data-stu-id="36def-998">7</span></span>

<span data-ttu-id="36def-999">8</span><span class="sxs-lookup"><span data-stu-id="36def-999">8</span></span>

<span data-ttu-id="36def-1000">9</span><span class="sxs-lookup"><span data-stu-id="36def-1000">9</span></span>

<span data-ttu-id="36def-1001">2</span><span class="sxs-lookup"><span data-stu-id="36def-1001">2</span></span><br/> <span data-ttu-id="36def-1002">0</span><span class="sxs-lookup"><span data-stu-id="36def-1002">0</span></span><br/>

<span data-ttu-id="36def-1003">1</span><span class="sxs-lookup"><span data-stu-id="36def-1003">1</span></span>

<span data-ttu-id="36def-1004">2</span><span class="sxs-lookup"><span data-stu-id="36def-1004">2</span></span>

<span data-ttu-id="36def-1005">3</span><span class="sxs-lookup"><span data-stu-id="36def-1005">3</span></span>

<span data-ttu-id="36def-1006">4</span><span class="sxs-lookup"><span data-stu-id="36def-1006">4</span></span>

<span data-ttu-id="36def-1007">5</span><span class="sxs-lookup"><span data-stu-id="36def-1007">5</span></span>

<span data-ttu-id="36def-1008">6</span><span class="sxs-lookup"><span data-stu-id="36def-1008">6</span></span>

<span data-ttu-id="36def-1009">7</span><span class="sxs-lookup"><span data-stu-id="36def-1009">7</span></span>

<span data-ttu-id="36def-1010">8</span><span class="sxs-lookup"><span data-stu-id="36def-1010">8</span></span>

<span data-ttu-id="36def-1011">9</span><span class="sxs-lookup"><span data-stu-id="36def-1011">9</span></span>

<span data-ttu-id="36def-1012">3</span><span class="sxs-lookup"><span data-stu-id="36def-1012">3</span></span><br/> <span data-ttu-id="36def-1013">0</span><span class="sxs-lookup"><span data-stu-id="36def-1013">0</span></span><br/>

<span data-ttu-id="36def-1014">1</span><span class="sxs-lookup"><span data-stu-id="36def-1014">1</span></span>

<span data-ttu-id="36def-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="36def-1015">PROPID</span></span>

<span data-ttu-id="36def-1016">Cb</span><span class="sxs-lookup"><span data-stu-id="36def-1016">Cb</span></span>

<span data-ttu-id="36def-1017">buf (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1017">buf (variable)</span></span>



 

<span data-ttu-id="36def-1018">**PROPID**：32位不帶正負號的整數，表示如1.8.1 小節中所討論的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="36def-1019">已知的值為：</span><span class="sxs-lookup"><span data-stu-id="36def-1019">Well-known values are:</span></span>



| <span data-ttu-id="36def-1020">值</span><span class="sxs-lookup"><span data-stu-id="36def-1020">Value</span></span>      | <span data-ttu-id="36def-1021">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="36def-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="36def-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="36def-1023">代表不正確屬性識別碼，不可使用。</span><span class="sxs-lookup"><span data-stu-id="36def-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="36def-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="36def-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="36def-1025">代表不正確屬性識別碼，不可使用。</span><span class="sxs-lookup"><span data-stu-id="36def-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="36def-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1026">0x00000000</span></span> | <span data-ttu-id="36def-1027">表示任何屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="36def-1028">**Cb**：32位不帶正負號的整數，其中包含 buf 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="36def-1029">**buf**：代表屬性值的位元組序列。</span><span class="sxs-lookup"><span data-stu-id="36def-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="36def-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="36def-1031">CInternalPropertyRestriction 結構包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="36def-1032">0</span><span class="sxs-lookup"><span data-stu-id="36def-1032">0</span></span>

<span data-ttu-id="36def-1033">1</span><span class="sxs-lookup"><span data-stu-id="36def-1033">1</span></span>

<span data-ttu-id="36def-1034">2</span><span class="sxs-lookup"><span data-stu-id="36def-1034">2</span></span>

<span data-ttu-id="36def-1035">3</span><span class="sxs-lookup"><span data-stu-id="36def-1035">3</span></span>

<span data-ttu-id="36def-1036">4</span><span class="sxs-lookup"><span data-stu-id="36def-1036">4</span></span>

<span data-ttu-id="36def-1037">5</span><span class="sxs-lookup"><span data-stu-id="36def-1037">5</span></span>

<span data-ttu-id="36def-1038">6</span><span class="sxs-lookup"><span data-stu-id="36def-1038">6</span></span>

<span data-ttu-id="36def-1039">7</span><span class="sxs-lookup"><span data-stu-id="36def-1039">7</span></span>

<span data-ttu-id="36def-1040">8</span><span class="sxs-lookup"><span data-stu-id="36def-1040">8</span></span>

<span data-ttu-id="36def-1041">9</span><span class="sxs-lookup"><span data-stu-id="36def-1041">9</span></span>

<span data-ttu-id="36def-1042">1</span><span class="sxs-lookup"><span data-stu-id="36def-1042">1</span></span><br/> <span data-ttu-id="36def-1043">0</span><span class="sxs-lookup"><span data-stu-id="36def-1043">0</span></span><br/>

<span data-ttu-id="36def-1044">1</span><span class="sxs-lookup"><span data-stu-id="36def-1044">1</span></span>

<span data-ttu-id="36def-1045">2</span><span class="sxs-lookup"><span data-stu-id="36def-1045">2</span></span>

<span data-ttu-id="36def-1046">3</span><span class="sxs-lookup"><span data-stu-id="36def-1046">3</span></span>

<span data-ttu-id="36def-1047">4</span><span class="sxs-lookup"><span data-stu-id="36def-1047">4</span></span>

<span data-ttu-id="36def-1048">5</span><span class="sxs-lookup"><span data-stu-id="36def-1048">5</span></span>

<span data-ttu-id="36def-1049">6</span><span class="sxs-lookup"><span data-stu-id="36def-1049">6</span></span>

<span data-ttu-id="36def-1050">7</span><span class="sxs-lookup"><span data-stu-id="36def-1050">7</span></span>

<span data-ttu-id="36def-1051">8</span><span class="sxs-lookup"><span data-stu-id="36def-1051">8</span></span>

<span data-ttu-id="36def-1052">9</span><span class="sxs-lookup"><span data-stu-id="36def-1052">9</span></span>

<span data-ttu-id="36def-1053">2</span><span class="sxs-lookup"><span data-stu-id="36def-1053">2</span></span><br/> <span data-ttu-id="36def-1054">0</span><span class="sxs-lookup"><span data-stu-id="36def-1054">0</span></span><br/>

<span data-ttu-id="36def-1055">1</span><span class="sxs-lookup"><span data-stu-id="36def-1055">1</span></span>

<span data-ttu-id="36def-1056">2</span><span class="sxs-lookup"><span data-stu-id="36def-1056">2</span></span>

<span data-ttu-id="36def-1057">3</span><span class="sxs-lookup"><span data-stu-id="36def-1057">3</span></span>

<span data-ttu-id="36def-1058">4</span><span class="sxs-lookup"><span data-stu-id="36def-1058">4</span></span>

<span data-ttu-id="36def-1059">5</span><span class="sxs-lookup"><span data-stu-id="36def-1059">5</span></span>

<span data-ttu-id="36def-1060">6</span><span class="sxs-lookup"><span data-stu-id="36def-1060">6</span></span>

<span data-ttu-id="36def-1061">7</span><span class="sxs-lookup"><span data-stu-id="36def-1061">7</span></span>

<span data-ttu-id="36def-1062">8</span><span class="sxs-lookup"><span data-stu-id="36def-1062">8</span></span>

<span data-ttu-id="36def-1063">9</span><span class="sxs-lookup"><span data-stu-id="36def-1063">9</span></span>

<span data-ttu-id="36def-1064">3</span><span class="sxs-lookup"><span data-stu-id="36def-1064">3</span></span><br/> <span data-ttu-id="36def-1065">0</span><span class="sxs-lookup"><span data-stu-id="36def-1065">0</span></span><br/>

<span data-ttu-id="36def-1066">1</span><span class="sxs-lookup"><span data-stu-id="36def-1066">1</span></span>

<span data-ttu-id="36def-1067">\_relop</span><span class="sxs-lookup"><span data-stu-id="36def-1067">\_relop</span></span>

<span data-ttu-id="36def-1068">\_pid</span><span class="sxs-lookup"><span data-stu-id="36def-1068">\_pid</span></span>

<span data-ttu-id="36def-1069">\_prval (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1069">\_prval (variable)</span></span>

<span data-ttu-id="36def-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="36def-1070">restrictionPresent</span></span>

<span data-ttu-id="36def-1071">nextRestriction (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="36def-1072">**\_ relop**：32位整數，指定要在屬性上執行的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36def-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="36def-1073">必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="36def-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="36def-1074">值</span><span class="sxs-lookup"><span data-stu-id="36def-1074">Value</span></span>                 | <span data-ttu-id="36def-1075">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="36def-1077">小於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1078">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="36def-1079">小於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="36def-1080">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="36def-1081">大於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="36def-1082">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="36def-1083">大於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="36def-1084">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="36def-1085">相等比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="36def-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="36def-1087">不相等的比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="36def-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="36def-1089">正則運算式比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="36def-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="36def-1091">傳回右運算元的位 AND。</span><span class="sxs-lookup"><span data-stu-id="36def-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="36def-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="36def-1093">傳回非零值的位 AND。</span><span class="sxs-lookup"><span data-stu-id="36def-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="36def-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="36def-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="36def-1095">作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。</span><span class="sxs-lookup"><span data-stu-id="36def-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="36def-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="36def-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="36def-1097">作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="36def-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="36def-1098">**\_ pid**：32位不帶正負號的整數，代表屬性識別碼 (請參閱2.2.1.4 一節中的 PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="36def-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="36def-1099">**\_ prval**：包含與屬性相關之值的 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="36def-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="36def-1100">**restrictionPresent**：指出 nextRestriction 欄位是否存在的位元組值。</span><span class="sxs-lookup"><span data-stu-id="36def-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="36def-1101">必須設定為0x00 或0x01。</span><span class="sxs-lookup"><span data-stu-id="36def-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="36def-1102">如果設定為0x01，restrictionPresent 會指出 nextRestriction 欄位存在。</span><span class="sxs-lookup"><span data-stu-id="36def-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="36def-1103">如果設定為0x00，restrictionPresent 會指出 nextRestriction 欄位不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="36def-1104">**nextRestriction**： CRestriction 結構，如2.2.1.16 一節中所指定，指定進一步的限制。</span><span class="sxs-lookup"><span data-stu-id="36def-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="36def-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="36def-1106">CNatLanguageRestriction 結構包含屬性的 **自然語言查詢** 相符項。</span><span class="sxs-lookup"><span data-stu-id="36def-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="36def-1107">0</span><span class="sxs-lookup"><span data-stu-id="36def-1107">0</span></span>

<span data-ttu-id="36def-1108">1</span><span class="sxs-lookup"><span data-stu-id="36def-1108">1</span></span>

<span data-ttu-id="36def-1109">2</span><span class="sxs-lookup"><span data-stu-id="36def-1109">2</span></span>

<span data-ttu-id="36def-1110">3</span><span class="sxs-lookup"><span data-stu-id="36def-1110">3</span></span>

<span data-ttu-id="36def-1111">4</span><span class="sxs-lookup"><span data-stu-id="36def-1111">4</span></span>

<span data-ttu-id="36def-1112">5</span><span class="sxs-lookup"><span data-stu-id="36def-1112">5</span></span>

<span data-ttu-id="36def-1113">6</span><span class="sxs-lookup"><span data-stu-id="36def-1113">6</span></span>

<span data-ttu-id="36def-1114">7</span><span class="sxs-lookup"><span data-stu-id="36def-1114">7</span></span>

<span data-ttu-id="36def-1115">8</span><span class="sxs-lookup"><span data-stu-id="36def-1115">8</span></span>

<span data-ttu-id="36def-1116">9</span><span class="sxs-lookup"><span data-stu-id="36def-1116">9</span></span>

<span data-ttu-id="36def-1117">1</span><span class="sxs-lookup"><span data-stu-id="36def-1117">1</span></span><br/> <span data-ttu-id="36def-1118">0</span><span class="sxs-lookup"><span data-stu-id="36def-1118">0</span></span><br/>

<span data-ttu-id="36def-1119">1</span><span class="sxs-lookup"><span data-stu-id="36def-1119">1</span></span>

<span data-ttu-id="36def-1120">2</span><span class="sxs-lookup"><span data-stu-id="36def-1120">2</span></span>

<span data-ttu-id="36def-1121">3</span><span class="sxs-lookup"><span data-stu-id="36def-1121">3</span></span>

<span data-ttu-id="36def-1122">4</span><span class="sxs-lookup"><span data-stu-id="36def-1122">4</span></span>

<span data-ttu-id="36def-1123">5</span><span class="sxs-lookup"><span data-stu-id="36def-1123">5</span></span>

<span data-ttu-id="36def-1124">6</span><span class="sxs-lookup"><span data-stu-id="36def-1124">6</span></span>

<span data-ttu-id="36def-1125">7</span><span class="sxs-lookup"><span data-stu-id="36def-1125">7</span></span>

<span data-ttu-id="36def-1126">8</span><span class="sxs-lookup"><span data-stu-id="36def-1126">8</span></span>

<span data-ttu-id="36def-1127">9</span><span class="sxs-lookup"><span data-stu-id="36def-1127">9</span></span>

<span data-ttu-id="36def-1128">2</span><span class="sxs-lookup"><span data-stu-id="36def-1128">2</span></span><br/> <span data-ttu-id="36def-1129">0</span><span class="sxs-lookup"><span data-stu-id="36def-1129">0</span></span><br/>

<span data-ttu-id="36def-1130">1</span><span class="sxs-lookup"><span data-stu-id="36def-1130">1</span></span>

<span data-ttu-id="36def-1131">2</span><span class="sxs-lookup"><span data-stu-id="36def-1131">2</span></span>

<span data-ttu-id="36def-1132">3</span><span class="sxs-lookup"><span data-stu-id="36def-1132">3</span></span>

<span data-ttu-id="36def-1133">4</span><span class="sxs-lookup"><span data-stu-id="36def-1133">4</span></span>

<span data-ttu-id="36def-1134">5</span><span class="sxs-lookup"><span data-stu-id="36def-1134">5</span></span>

<span data-ttu-id="36def-1135">6</span><span class="sxs-lookup"><span data-stu-id="36def-1135">6</span></span>

<span data-ttu-id="36def-1136">7</span><span class="sxs-lookup"><span data-stu-id="36def-1136">7</span></span>

<span data-ttu-id="36def-1137">8</span><span class="sxs-lookup"><span data-stu-id="36def-1137">8</span></span>

<span data-ttu-id="36def-1138">9</span><span class="sxs-lookup"><span data-stu-id="36def-1138">9</span></span>

<span data-ttu-id="36def-1139">3</span><span class="sxs-lookup"><span data-stu-id="36def-1139">3</span></span><br/> <span data-ttu-id="36def-1140">0</span><span class="sxs-lookup"><span data-stu-id="36def-1140">0</span></span><br/>

<span data-ttu-id="36def-1141">1</span><span class="sxs-lookup"><span data-stu-id="36def-1141">1</span></span>

<span data-ttu-id="36def-1142">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1142">\_Property (variable)</span></span>

<span data-ttu-id="36def-1143">...</span><span class="sxs-lookup"><span data-stu-id="36def-1143">...</span></span>

<span data-ttu-id="36def-1144">\_填補 \_ cc (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="36def-1145">副本</span><span class="sxs-lookup"><span data-stu-id="36def-1145">Cc</span></span>

<span data-ttu-id="36def-1146">\_pwcsPhrase (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="36def-1147">...</span><span class="sxs-lookup"><span data-stu-id="36def-1147">...</span></span>

<span data-ttu-id="36def-1148">\_填補 \_ lcid (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="36def-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="36def-1149">Lcid</span></span>



 

<span data-ttu-id="36def-1150">**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.3 中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="36def-1151">這個欄位指出要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="36def-1152">**\_ 填補 \_** 副本：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-1153">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-1154">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-1155">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-1156">**Cc**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1157">PwcsPhrase 欄位中的字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="36def-1158">**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="36def-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="36def-1159">不得為空白。</span><span class="sxs-lookup"><span data-stu-id="36def-1159">MUST NOT be empty.</span></span> <span data-ttu-id="36def-1160">Cc 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="36def-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="36def-1161">**\_ 填補 \_ lcid**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-1162">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-1163">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-1164">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-1165">**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="36def-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="36def-1167">CNodeRestriction 結構包含指定查詢限制的 **命令樹** 節點陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="36def-1168">0</span><span class="sxs-lookup"><span data-stu-id="36def-1168">0</span></span>

<span data-ttu-id="36def-1169">1</span><span class="sxs-lookup"><span data-stu-id="36def-1169">1</span></span>

<span data-ttu-id="36def-1170">2</span><span class="sxs-lookup"><span data-stu-id="36def-1170">2</span></span>

<span data-ttu-id="36def-1171">3</span><span class="sxs-lookup"><span data-stu-id="36def-1171">3</span></span>

<span data-ttu-id="36def-1172">4</span><span class="sxs-lookup"><span data-stu-id="36def-1172">4</span></span>

<span data-ttu-id="36def-1173">5</span><span class="sxs-lookup"><span data-stu-id="36def-1173">5</span></span>

<span data-ttu-id="36def-1174">6</span><span class="sxs-lookup"><span data-stu-id="36def-1174">6</span></span>

<span data-ttu-id="36def-1175">7</span><span class="sxs-lookup"><span data-stu-id="36def-1175">7</span></span>

<span data-ttu-id="36def-1176">8</span><span class="sxs-lookup"><span data-stu-id="36def-1176">8</span></span>

<span data-ttu-id="36def-1177">9</span><span class="sxs-lookup"><span data-stu-id="36def-1177">9</span></span>

<span data-ttu-id="36def-1178">1</span><span class="sxs-lookup"><span data-stu-id="36def-1178">1</span></span><br/> <span data-ttu-id="36def-1179">0</span><span class="sxs-lookup"><span data-stu-id="36def-1179">0</span></span><br/>

<span data-ttu-id="36def-1180">1</span><span class="sxs-lookup"><span data-stu-id="36def-1180">1</span></span>

<span data-ttu-id="36def-1181">2</span><span class="sxs-lookup"><span data-stu-id="36def-1181">2</span></span>

<span data-ttu-id="36def-1182">3</span><span class="sxs-lookup"><span data-stu-id="36def-1182">3</span></span>

<span data-ttu-id="36def-1183">4</span><span class="sxs-lookup"><span data-stu-id="36def-1183">4</span></span>

<span data-ttu-id="36def-1184">5</span><span class="sxs-lookup"><span data-stu-id="36def-1184">5</span></span>

<span data-ttu-id="36def-1185">6</span><span class="sxs-lookup"><span data-stu-id="36def-1185">6</span></span>

<span data-ttu-id="36def-1186">7</span><span class="sxs-lookup"><span data-stu-id="36def-1186">7</span></span>

<span data-ttu-id="36def-1187">8</span><span class="sxs-lookup"><span data-stu-id="36def-1187">8</span></span>

<span data-ttu-id="36def-1188">9</span><span class="sxs-lookup"><span data-stu-id="36def-1188">9</span></span>

<span data-ttu-id="36def-1189">2</span><span class="sxs-lookup"><span data-stu-id="36def-1189">2</span></span><br/> <span data-ttu-id="36def-1190">0</span><span class="sxs-lookup"><span data-stu-id="36def-1190">0</span></span><br/>

<span data-ttu-id="36def-1191">1</span><span class="sxs-lookup"><span data-stu-id="36def-1191">1</span></span>

<span data-ttu-id="36def-1192">2</span><span class="sxs-lookup"><span data-stu-id="36def-1192">2</span></span>

<span data-ttu-id="36def-1193">3</span><span class="sxs-lookup"><span data-stu-id="36def-1193">3</span></span>

<span data-ttu-id="36def-1194">4</span><span class="sxs-lookup"><span data-stu-id="36def-1194">4</span></span>

<span data-ttu-id="36def-1195">5</span><span class="sxs-lookup"><span data-stu-id="36def-1195">5</span></span>

<span data-ttu-id="36def-1196">6</span><span class="sxs-lookup"><span data-stu-id="36def-1196">6</span></span>

<span data-ttu-id="36def-1197">7</span><span class="sxs-lookup"><span data-stu-id="36def-1197">7</span></span>

<span data-ttu-id="36def-1198">8</span><span class="sxs-lookup"><span data-stu-id="36def-1198">8</span></span>

<span data-ttu-id="36def-1199">9</span><span class="sxs-lookup"><span data-stu-id="36def-1199">9</span></span>

<span data-ttu-id="36def-1200">3</span><span class="sxs-lookup"><span data-stu-id="36def-1200">3</span></span><br/> <span data-ttu-id="36def-1201">0</span><span class="sxs-lookup"><span data-stu-id="36def-1201">0</span></span><br/>

<span data-ttu-id="36def-1202">1</span><span class="sxs-lookup"><span data-stu-id="36def-1202">1</span></span>

<span data-ttu-id="36def-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="36def-1203">\_cNode</span></span>

<span data-ttu-id="36def-1204">\_paNode (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="36def-1205">**\_ cNode**：32位不帶正負號的整數，指定 paNode 欄位中包含的 CRestriction 結構數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="36def-1206">**\_ PaNode**： CRestriction 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="36def-1207">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="36def-1208">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="36def-1209">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="36def-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="36def-1211">COccRestriction 結構包含單字在片語中的位置。</span><span class="sxs-lookup"><span data-stu-id="36def-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="36def-1212">0</span><span class="sxs-lookup"><span data-stu-id="36def-1212">0</span></span>

<span data-ttu-id="36def-1213">1</span><span class="sxs-lookup"><span data-stu-id="36def-1213">1</span></span>

<span data-ttu-id="36def-1214">2</span><span class="sxs-lookup"><span data-stu-id="36def-1214">2</span></span>

<span data-ttu-id="36def-1215">3</span><span class="sxs-lookup"><span data-stu-id="36def-1215">3</span></span>

<span data-ttu-id="36def-1216">4</span><span class="sxs-lookup"><span data-stu-id="36def-1216">4</span></span>

<span data-ttu-id="36def-1217">5</span><span class="sxs-lookup"><span data-stu-id="36def-1217">5</span></span>

<span data-ttu-id="36def-1218">6</span><span class="sxs-lookup"><span data-stu-id="36def-1218">6</span></span>

<span data-ttu-id="36def-1219">7</span><span class="sxs-lookup"><span data-stu-id="36def-1219">7</span></span>

<span data-ttu-id="36def-1220">8</span><span class="sxs-lookup"><span data-stu-id="36def-1220">8</span></span>

<span data-ttu-id="36def-1221">9</span><span class="sxs-lookup"><span data-stu-id="36def-1221">9</span></span>

<span data-ttu-id="36def-1222">1</span><span class="sxs-lookup"><span data-stu-id="36def-1222">1</span></span><br/> <span data-ttu-id="36def-1223">0</span><span class="sxs-lookup"><span data-stu-id="36def-1223">0</span></span><br/>

<span data-ttu-id="36def-1224">1</span><span class="sxs-lookup"><span data-stu-id="36def-1224">1</span></span>

<span data-ttu-id="36def-1225">2</span><span class="sxs-lookup"><span data-stu-id="36def-1225">2</span></span>

<span data-ttu-id="36def-1226">3</span><span class="sxs-lookup"><span data-stu-id="36def-1226">3</span></span>

<span data-ttu-id="36def-1227">4</span><span class="sxs-lookup"><span data-stu-id="36def-1227">4</span></span>

<span data-ttu-id="36def-1228">5</span><span class="sxs-lookup"><span data-stu-id="36def-1228">5</span></span>

<span data-ttu-id="36def-1229">6</span><span class="sxs-lookup"><span data-stu-id="36def-1229">6</span></span>

<span data-ttu-id="36def-1230">7</span><span class="sxs-lookup"><span data-stu-id="36def-1230">7</span></span>

<span data-ttu-id="36def-1231">8</span><span class="sxs-lookup"><span data-stu-id="36def-1231">8</span></span>

<span data-ttu-id="36def-1232">9</span><span class="sxs-lookup"><span data-stu-id="36def-1232">9</span></span>

<span data-ttu-id="36def-1233">2</span><span class="sxs-lookup"><span data-stu-id="36def-1233">2</span></span><br/> <span data-ttu-id="36def-1234">0</span><span class="sxs-lookup"><span data-stu-id="36def-1234">0</span></span><br/>

<span data-ttu-id="36def-1235">1</span><span class="sxs-lookup"><span data-stu-id="36def-1235">1</span></span>

<span data-ttu-id="36def-1236">2</span><span class="sxs-lookup"><span data-stu-id="36def-1236">2</span></span>

<span data-ttu-id="36def-1237">3</span><span class="sxs-lookup"><span data-stu-id="36def-1237">3</span></span>

<span data-ttu-id="36def-1238">4</span><span class="sxs-lookup"><span data-stu-id="36def-1238">4</span></span>

<span data-ttu-id="36def-1239">5</span><span class="sxs-lookup"><span data-stu-id="36def-1239">5</span></span>

<span data-ttu-id="36def-1240">6</span><span class="sxs-lookup"><span data-stu-id="36def-1240">6</span></span>

<span data-ttu-id="36def-1241">7</span><span class="sxs-lookup"><span data-stu-id="36def-1241">7</span></span>

<span data-ttu-id="36def-1242">8</span><span class="sxs-lookup"><span data-stu-id="36def-1242">8</span></span>

<span data-ttu-id="36def-1243">9</span><span class="sxs-lookup"><span data-stu-id="36def-1243">9</span></span>

<span data-ttu-id="36def-1244">3</span><span class="sxs-lookup"><span data-stu-id="36def-1244">3</span></span><br/> <span data-ttu-id="36def-1245">0</span><span class="sxs-lookup"><span data-stu-id="36def-1245">0</span></span><br/>

<span data-ttu-id="36def-1246">1</span><span class="sxs-lookup"><span data-stu-id="36def-1246">1</span></span>

<span data-ttu-id="36def-1247">\_Occ</span><span class="sxs-lookup"><span data-stu-id="36def-1247">\_occ</span></span>

<span data-ttu-id="36def-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="36def-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="36def-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="36def-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="36def-1250">**\_ occ**：32位不帶正負號的整數，指定查詢字串中的單字位移（以單字為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="36def-1251">此規格中使用的單字是具有意義的任何地區設定中的語言單位。</span><span class="sxs-lookup"><span data-stu-id="36def-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="36def-1252">**\_ cPrevNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中前一個單字之間出現的非搜尋 **字** 數目。</span><span class="sxs-lookup"><span data-stu-id="36def-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="36def-1253">**\_ cNextNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中下一個單字之間出現的非搜尋字數目。</span><span class="sxs-lookup"><span data-stu-id="36def-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="36def-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="36def-1255">CPropertyRestriction 結構包含要與作業相符的屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="36def-1256">0</span><span class="sxs-lookup"><span data-stu-id="36def-1256">0</span></span>

<span data-ttu-id="36def-1257">1</span><span class="sxs-lookup"><span data-stu-id="36def-1257">1</span></span>

<span data-ttu-id="36def-1258">2</span><span class="sxs-lookup"><span data-stu-id="36def-1258">2</span></span>

<span data-ttu-id="36def-1259">3</span><span class="sxs-lookup"><span data-stu-id="36def-1259">3</span></span>

<span data-ttu-id="36def-1260">4</span><span class="sxs-lookup"><span data-stu-id="36def-1260">4</span></span>

<span data-ttu-id="36def-1261">5</span><span class="sxs-lookup"><span data-stu-id="36def-1261">5</span></span>

<span data-ttu-id="36def-1262">6</span><span class="sxs-lookup"><span data-stu-id="36def-1262">6</span></span>

<span data-ttu-id="36def-1263">7</span><span class="sxs-lookup"><span data-stu-id="36def-1263">7</span></span>

<span data-ttu-id="36def-1264">8</span><span class="sxs-lookup"><span data-stu-id="36def-1264">8</span></span>

<span data-ttu-id="36def-1265">9</span><span class="sxs-lookup"><span data-stu-id="36def-1265">9</span></span>

<span data-ttu-id="36def-1266">1</span><span class="sxs-lookup"><span data-stu-id="36def-1266">1</span></span><br/> <span data-ttu-id="36def-1267">0</span><span class="sxs-lookup"><span data-stu-id="36def-1267">0</span></span><br/>

<span data-ttu-id="36def-1268">1</span><span class="sxs-lookup"><span data-stu-id="36def-1268">1</span></span>

<span data-ttu-id="36def-1269">2</span><span class="sxs-lookup"><span data-stu-id="36def-1269">2</span></span>

<span data-ttu-id="36def-1270">3</span><span class="sxs-lookup"><span data-stu-id="36def-1270">3</span></span>

<span data-ttu-id="36def-1271">4</span><span class="sxs-lookup"><span data-stu-id="36def-1271">4</span></span>

<span data-ttu-id="36def-1272">5</span><span class="sxs-lookup"><span data-stu-id="36def-1272">5</span></span>

<span data-ttu-id="36def-1273">6</span><span class="sxs-lookup"><span data-stu-id="36def-1273">6</span></span>

<span data-ttu-id="36def-1274">7</span><span class="sxs-lookup"><span data-stu-id="36def-1274">7</span></span>

<span data-ttu-id="36def-1275">8</span><span class="sxs-lookup"><span data-stu-id="36def-1275">8</span></span>

<span data-ttu-id="36def-1276">9</span><span class="sxs-lookup"><span data-stu-id="36def-1276">9</span></span>

<span data-ttu-id="36def-1277">2</span><span class="sxs-lookup"><span data-stu-id="36def-1277">2</span></span><br/> <span data-ttu-id="36def-1278">0</span><span class="sxs-lookup"><span data-stu-id="36def-1278">0</span></span><br/>

<span data-ttu-id="36def-1279">1</span><span class="sxs-lookup"><span data-stu-id="36def-1279">1</span></span>

<span data-ttu-id="36def-1280">2</span><span class="sxs-lookup"><span data-stu-id="36def-1280">2</span></span>

<span data-ttu-id="36def-1281">3</span><span class="sxs-lookup"><span data-stu-id="36def-1281">3</span></span>

<span data-ttu-id="36def-1282">4</span><span class="sxs-lookup"><span data-stu-id="36def-1282">4</span></span>

<span data-ttu-id="36def-1283">5</span><span class="sxs-lookup"><span data-stu-id="36def-1283">5</span></span>

<span data-ttu-id="36def-1284">6</span><span class="sxs-lookup"><span data-stu-id="36def-1284">6</span></span>

<span data-ttu-id="36def-1285">7</span><span class="sxs-lookup"><span data-stu-id="36def-1285">7</span></span>

<span data-ttu-id="36def-1286">8</span><span class="sxs-lookup"><span data-stu-id="36def-1286">8</span></span>

<span data-ttu-id="36def-1287">9</span><span class="sxs-lookup"><span data-stu-id="36def-1287">9</span></span>

<span data-ttu-id="36def-1288">3</span><span class="sxs-lookup"><span data-stu-id="36def-1288">3</span></span><br/> <span data-ttu-id="36def-1289">0</span><span class="sxs-lookup"><span data-stu-id="36def-1289">0</span></span><br/>

<span data-ttu-id="36def-1290">1</span><span class="sxs-lookup"><span data-stu-id="36def-1290">1</span></span>

<span data-ttu-id="36def-1291">\_relop</span><span class="sxs-lookup"><span data-stu-id="36def-1291">\_relop</span></span>

<span data-ttu-id="36def-1292">\_屬性 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1292">\_Property (variable)</span></span>

<span data-ttu-id="36def-1293">\_prval (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="36def-1294">**\_ relop**：32位不帶正負號的整數，指定要在屬性上執行的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36def-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="36def-1295">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36def-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="36def-1296">值</span><span class="sxs-lookup"><span data-stu-id="36def-1296">Value</span></span>                 | <span data-ttu-id="36def-1297">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="36def-1299">小於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1300">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="36def-1301">小於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="36def-1302">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="36def-1303">大於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="36def-1304">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="36def-1305">大於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="36def-1306">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="36def-1307">相等比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="36def-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="36def-1309">不相等的比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="36def-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="36def-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="36def-1311">正則運算式比較。</span><span class="sxs-lookup"><span data-stu-id="36def-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="36def-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="36def-1313">傳回右運算元的位 AND。</span><span class="sxs-lookup"><span data-stu-id="36def-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="36def-1314">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="36def-1315">傳回非零值的位 AND。</span><span class="sxs-lookup"><span data-stu-id="36def-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="36def-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="36def-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="36def-1317">作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。</span><span class="sxs-lookup"><span data-stu-id="36def-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="36def-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="36def-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="36def-1319">作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="36def-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="36def-1320">**\_ 屬性**： CFullPropSpec 結構（如區段2.2.1.2 中所指定），表示要執行比對作業的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="36def-1321">**\_ prval**：在區段2.2.1.1 中指定的 CBaseStorageVariant 結構，其中包含與屬性相關的值。</span><span class="sxs-lookup"><span data-stu-id="36def-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="36def-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="36def-1323">CRangeRestriction 結構包含值範圍的限制。</span><span class="sxs-lookup"><span data-stu-id="36def-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="36def-1324">0</span><span class="sxs-lookup"><span data-stu-id="36def-1324">0</span></span>

<span data-ttu-id="36def-1325">1</span><span class="sxs-lookup"><span data-stu-id="36def-1325">1</span></span>

<span data-ttu-id="36def-1326">2</span><span class="sxs-lookup"><span data-stu-id="36def-1326">2</span></span>

<span data-ttu-id="36def-1327">3</span><span class="sxs-lookup"><span data-stu-id="36def-1327">3</span></span>

<span data-ttu-id="36def-1328">4</span><span class="sxs-lookup"><span data-stu-id="36def-1328">4</span></span>

<span data-ttu-id="36def-1329">5</span><span class="sxs-lookup"><span data-stu-id="36def-1329">5</span></span>

<span data-ttu-id="36def-1330">6</span><span class="sxs-lookup"><span data-stu-id="36def-1330">6</span></span>

<span data-ttu-id="36def-1331">7</span><span class="sxs-lookup"><span data-stu-id="36def-1331">7</span></span>

<span data-ttu-id="36def-1332">8</span><span class="sxs-lookup"><span data-stu-id="36def-1332">8</span></span>

<span data-ttu-id="36def-1333">9</span><span class="sxs-lookup"><span data-stu-id="36def-1333">9</span></span>

<span data-ttu-id="36def-1334">1</span><span class="sxs-lookup"><span data-stu-id="36def-1334">1</span></span><br/> <span data-ttu-id="36def-1335">0</span><span class="sxs-lookup"><span data-stu-id="36def-1335">0</span></span><br/>

<span data-ttu-id="36def-1336">1</span><span class="sxs-lookup"><span data-stu-id="36def-1336">1</span></span>

<span data-ttu-id="36def-1337">2</span><span class="sxs-lookup"><span data-stu-id="36def-1337">2</span></span>

<span data-ttu-id="36def-1338">3</span><span class="sxs-lookup"><span data-stu-id="36def-1338">3</span></span>

<span data-ttu-id="36def-1339">4</span><span class="sxs-lookup"><span data-stu-id="36def-1339">4</span></span>

<span data-ttu-id="36def-1340">5</span><span class="sxs-lookup"><span data-stu-id="36def-1340">5</span></span>

<span data-ttu-id="36def-1341">6</span><span class="sxs-lookup"><span data-stu-id="36def-1341">6</span></span>

<span data-ttu-id="36def-1342">7</span><span class="sxs-lookup"><span data-stu-id="36def-1342">7</span></span>

<span data-ttu-id="36def-1343">8</span><span class="sxs-lookup"><span data-stu-id="36def-1343">8</span></span>

<span data-ttu-id="36def-1344">9</span><span class="sxs-lookup"><span data-stu-id="36def-1344">9</span></span>

<span data-ttu-id="36def-1345">2</span><span class="sxs-lookup"><span data-stu-id="36def-1345">2</span></span><br/> <span data-ttu-id="36def-1346">0</span><span class="sxs-lookup"><span data-stu-id="36def-1346">0</span></span><br/>

<span data-ttu-id="36def-1347">1</span><span class="sxs-lookup"><span data-stu-id="36def-1347">1</span></span>

<span data-ttu-id="36def-1348">2</span><span class="sxs-lookup"><span data-stu-id="36def-1348">2</span></span>

<span data-ttu-id="36def-1349">3</span><span class="sxs-lookup"><span data-stu-id="36def-1349">3</span></span>

<span data-ttu-id="36def-1350">4</span><span class="sxs-lookup"><span data-stu-id="36def-1350">4</span></span>

<span data-ttu-id="36def-1351">5</span><span class="sxs-lookup"><span data-stu-id="36def-1351">5</span></span>

<span data-ttu-id="36def-1352">6</span><span class="sxs-lookup"><span data-stu-id="36def-1352">6</span></span>

<span data-ttu-id="36def-1353">7</span><span class="sxs-lookup"><span data-stu-id="36def-1353">7</span></span>

<span data-ttu-id="36def-1354">8</span><span class="sxs-lookup"><span data-stu-id="36def-1354">8</span></span>

<span data-ttu-id="36def-1355">9</span><span class="sxs-lookup"><span data-stu-id="36def-1355">9</span></span>

<span data-ttu-id="36def-1356">3</span><span class="sxs-lookup"><span data-stu-id="36def-1356">3</span></span><br/> <span data-ttu-id="36def-1357">0</span><span class="sxs-lookup"><span data-stu-id="36def-1357">0</span></span><br/>

<span data-ttu-id="36def-1358">1</span><span class="sxs-lookup"><span data-stu-id="36def-1358">1</span></span>

<span data-ttu-id="36def-1359">\_keyStart (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="36def-1360">\_keyEnd (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="36def-1361">**\_ keyStart**：2.2.1.4 區段中指定的 CKey 結構，其中包含範圍的開頭。</span><span class="sxs-lookup"><span data-stu-id="36def-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="36def-1362">**\_ keyEnd**：包含範圍結尾的 CKey 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="36def-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="36def-1364">CScopeRestriction 結構包含要搜尋之檔案的限制</span><span class="sxs-lookup"><span data-stu-id="36def-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="36def-1365">0</span><span class="sxs-lookup"><span data-stu-id="36def-1365">0</span></span>

<span data-ttu-id="36def-1366">1</span><span class="sxs-lookup"><span data-stu-id="36def-1366">1</span></span>

<span data-ttu-id="36def-1367">2</span><span class="sxs-lookup"><span data-stu-id="36def-1367">2</span></span>

<span data-ttu-id="36def-1368">3</span><span class="sxs-lookup"><span data-stu-id="36def-1368">3</span></span>

<span data-ttu-id="36def-1369">4</span><span class="sxs-lookup"><span data-stu-id="36def-1369">4</span></span>

<span data-ttu-id="36def-1370">5</span><span class="sxs-lookup"><span data-stu-id="36def-1370">5</span></span>

<span data-ttu-id="36def-1371">6</span><span class="sxs-lookup"><span data-stu-id="36def-1371">6</span></span>

<span data-ttu-id="36def-1372">7</span><span class="sxs-lookup"><span data-stu-id="36def-1372">7</span></span>

<span data-ttu-id="36def-1373">8</span><span class="sxs-lookup"><span data-stu-id="36def-1373">8</span></span>

<span data-ttu-id="36def-1374">9</span><span class="sxs-lookup"><span data-stu-id="36def-1374">9</span></span>

<span data-ttu-id="36def-1375">1</span><span class="sxs-lookup"><span data-stu-id="36def-1375">1</span></span><br/> <span data-ttu-id="36def-1376">0</span><span class="sxs-lookup"><span data-stu-id="36def-1376">0</span></span><br/>

<span data-ttu-id="36def-1377">1</span><span class="sxs-lookup"><span data-stu-id="36def-1377">1</span></span>

<span data-ttu-id="36def-1378">2</span><span class="sxs-lookup"><span data-stu-id="36def-1378">2</span></span>

<span data-ttu-id="36def-1379">3</span><span class="sxs-lookup"><span data-stu-id="36def-1379">3</span></span>

<span data-ttu-id="36def-1380">4</span><span class="sxs-lookup"><span data-stu-id="36def-1380">4</span></span>

<span data-ttu-id="36def-1381">5</span><span class="sxs-lookup"><span data-stu-id="36def-1381">5</span></span>

<span data-ttu-id="36def-1382">6</span><span class="sxs-lookup"><span data-stu-id="36def-1382">6</span></span>

<span data-ttu-id="36def-1383">7</span><span class="sxs-lookup"><span data-stu-id="36def-1383">7</span></span>

<span data-ttu-id="36def-1384">8</span><span class="sxs-lookup"><span data-stu-id="36def-1384">8</span></span>

<span data-ttu-id="36def-1385">9</span><span class="sxs-lookup"><span data-stu-id="36def-1385">9</span></span>

<span data-ttu-id="36def-1386">2</span><span class="sxs-lookup"><span data-stu-id="36def-1386">2</span></span><br/> <span data-ttu-id="36def-1387">0</span><span class="sxs-lookup"><span data-stu-id="36def-1387">0</span></span><br/>

<span data-ttu-id="36def-1388">1</span><span class="sxs-lookup"><span data-stu-id="36def-1388">1</span></span>

<span data-ttu-id="36def-1389">2</span><span class="sxs-lookup"><span data-stu-id="36def-1389">2</span></span>

<span data-ttu-id="36def-1390">3</span><span class="sxs-lookup"><span data-stu-id="36def-1390">3</span></span>

<span data-ttu-id="36def-1391">4</span><span class="sxs-lookup"><span data-stu-id="36def-1391">4</span></span>

<span data-ttu-id="36def-1392">5</span><span class="sxs-lookup"><span data-stu-id="36def-1392">5</span></span>

<span data-ttu-id="36def-1393">6</span><span class="sxs-lookup"><span data-stu-id="36def-1393">6</span></span>

<span data-ttu-id="36def-1394">7</span><span class="sxs-lookup"><span data-stu-id="36def-1394">7</span></span>

<span data-ttu-id="36def-1395">8</span><span class="sxs-lookup"><span data-stu-id="36def-1395">8</span></span>

<span data-ttu-id="36def-1396">9</span><span class="sxs-lookup"><span data-stu-id="36def-1396">9</span></span>

<span data-ttu-id="36def-1397">3</span><span class="sxs-lookup"><span data-stu-id="36def-1397">3</span></span><br/> <span data-ttu-id="36def-1398">0</span><span class="sxs-lookup"><span data-stu-id="36def-1398">0</span></span><br/>

<span data-ttu-id="36def-1399">1</span><span class="sxs-lookup"><span data-stu-id="36def-1399">1</span></span>

<span data-ttu-id="36def-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="36def-1400">CcLowerPath</span></span>

<span data-ttu-id="36def-1401">\_lowerPath (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="36def-1402">...</span><span class="sxs-lookup"><span data-stu-id="36def-1402">...</span></span>

<span data-ttu-id="36def-1403">\_填補 ( 變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1403">\_padding ( variable)</span></span>

<span data-ttu-id="36def-1404">\_長度</span><span class="sxs-lookup"><span data-stu-id="36def-1404">\_length</span></span>

<span data-ttu-id="36def-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="36def-1405">\_fRecursive</span></span>

<span data-ttu-id="36def-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="36def-1406">\_fVirtual</span></span>



 

<span data-ttu-id="36def-1407">**CcLowerPath**：32位不帶正負號的整數，其中包含 lowerPath 欄位中的 Unicode 字元數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="36def-1408">**\_ lowerPath**：非以 Null 終止的 Unicode 字串，表示應限制查詢的 **路徑**。</span><span class="sxs-lookup"><span data-stu-id="36def-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="36def-1409">CcLowerPath 欄位包含字串的長度。</span><span class="sxs-lookup"><span data-stu-id="36def-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="36def-1410">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-1411">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-1412">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-1413">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-1414">**\_ 長度**：32位不帶正負號的整數，其中包含 lowerPath 的長度 \_ （以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="36def-1415">這必須與 CcLowerPath 的值相同。</span><span class="sxs-lookup"><span data-stu-id="36def-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="36def-1416">**\_ fRecursive**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1417">必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="36def-1418">如果設定為0x00000001，伺服器就會以遞迴方式檢查路徑的所有子目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="36def-1419">如果設定為0x00000000，則伺服器不會檢查任何子目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="36def-1420">**\_ fVirtual**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1421">必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="36def-1422">如果設定為0x00000001， \_ lowerPath 就是 (統一資源定位器 (URL) 的虛擬路徑，與網站檔案系統) 上的實體目錄相關聯。</span><span class="sxs-lookup"><span data-stu-id="36def-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="36def-1423">如果設定為0x00000000， \_ lowerPath 就是檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="36def-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="36def-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="36def-1425">CSort 結構會識別要排序的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="36def-1426">0</span><span class="sxs-lookup"><span data-stu-id="36def-1426">0</span></span>

<span data-ttu-id="36def-1427">1</span><span class="sxs-lookup"><span data-stu-id="36def-1427">1</span></span>

<span data-ttu-id="36def-1428">2</span><span class="sxs-lookup"><span data-stu-id="36def-1428">2</span></span>

<span data-ttu-id="36def-1429">3</span><span class="sxs-lookup"><span data-stu-id="36def-1429">3</span></span>

<span data-ttu-id="36def-1430">4</span><span class="sxs-lookup"><span data-stu-id="36def-1430">4</span></span>

<span data-ttu-id="36def-1431">5</span><span class="sxs-lookup"><span data-stu-id="36def-1431">5</span></span>

<span data-ttu-id="36def-1432">6</span><span class="sxs-lookup"><span data-stu-id="36def-1432">6</span></span>

<span data-ttu-id="36def-1433">7</span><span class="sxs-lookup"><span data-stu-id="36def-1433">7</span></span>

<span data-ttu-id="36def-1434">8</span><span class="sxs-lookup"><span data-stu-id="36def-1434">8</span></span>

<span data-ttu-id="36def-1435">9</span><span class="sxs-lookup"><span data-stu-id="36def-1435">9</span></span>

<span data-ttu-id="36def-1436">1</span><span class="sxs-lookup"><span data-stu-id="36def-1436">1</span></span><br/> <span data-ttu-id="36def-1437">0</span><span class="sxs-lookup"><span data-stu-id="36def-1437">0</span></span><br/>

<span data-ttu-id="36def-1438">1</span><span class="sxs-lookup"><span data-stu-id="36def-1438">1</span></span>

<span data-ttu-id="36def-1439">2</span><span class="sxs-lookup"><span data-stu-id="36def-1439">2</span></span>

<span data-ttu-id="36def-1440">3</span><span class="sxs-lookup"><span data-stu-id="36def-1440">3</span></span>

<span data-ttu-id="36def-1441">4</span><span class="sxs-lookup"><span data-stu-id="36def-1441">4</span></span>

<span data-ttu-id="36def-1442">5</span><span class="sxs-lookup"><span data-stu-id="36def-1442">5</span></span>

<span data-ttu-id="36def-1443">6</span><span class="sxs-lookup"><span data-stu-id="36def-1443">6</span></span>

<span data-ttu-id="36def-1444">7</span><span class="sxs-lookup"><span data-stu-id="36def-1444">7</span></span>

<span data-ttu-id="36def-1445">8</span><span class="sxs-lookup"><span data-stu-id="36def-1445">8</span></span>

<span data-ttu-id="36def-1446">9</span><span class="sxs-lookup"><span data-stu-id="36def-1446">9</span></span>

<span data-ttu-id="36def-1447">2</span><span class="sxs-lookup"><span data-stu-id="36def-1447">2</span></span><br/> <span data-ttu-id="36def-1448">0</span><span class="sxs-lookup"><span data-stu-id="36def-1448">0</span></span><br/>

<span data-ttu-id="36def-1449">1</span><span class="sxs-lookup"><span data-stu-id="36def-1449">1</span></span>

<span data-ttu-id="36def-1450">2</span><span class="sxs-lookup"><span data-stu-id="36def-1450">2</span></span>

<span data-ttu-id="36def-1451">3</span><span class="sxs-lookup"><span data-stu-id="36def-1451">3</span></span>

<span data-ttu-id="36def-1452">4</span><span class="sxs-lookup"><span data-stu-id="36def-1452">4</span></span>

<span data-ttu-id="36def-1453">5</span><span class="sxs-lookup"><span data-stu-id="36def-1453">5</span></span>

<span data-ttu-id="36def-1454">6</span><span class="sxs-lookup"><span data-stu-id="36def-1454">6</span></span>

<span data-ttu-id="36def-1455">7</span><span class="sxs-lookup"><span data-stu-id="36def-1455">7</span></span>

<span data-ttu-id="36def-1456">8</span><span class="sxs-lookup"><span data-stu-id="36def-1456">8</span></span>

<span data-ttu-id="36def-1457">9</span><span class="sxs-lookup"><span data-stu-id="36def-1457">9</span></span>

<span data-ttu-id="36def-1458">3</span><span class="sxs-lookup"><span data-stu-id="36def-1458">3</span></span><br/> <span data-ttu-id="36def-1459">0</span><span class="sxs-lookup"><span data-stu-id="36def-1459">0</span></span><br/>

<span data-ttu-id="36def-1460">1</span><span class="sxs-lookup"><span data-stu-id="36def-1460">1</span></span>

<span data-ttu-id="36def-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="36def-1461">pidColumn</span></span>

<span data-ttu-id="36def-1462">dwOrder</span><span class="sxs-lookup"><span data-stu-id="36def-1462">dwOrder</span></span>

<span data-ttu-id="36def-1463">地區設定</span><span class="sxs-lookup"><span data-stu-id="36def-1463">locale</span></span>



 

<span data-ttu-id="36def-1464">**pidColumn**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1465">排序依據的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="36def-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="36def-1466">**dwOrder**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1467">必須是下列其中一個值，指定如何根據資料行排序。</span><span class="sxs-lookup"><span data-stu-id="36def-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="36def-1468">值</span><span class="sxs-lookup"><span data-stu-id="36def-1468">Value</span></span>                        | <span data-ttu-id="36def-1469">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1470">查詢 \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="36def-1471">資料列會根據指定之資料行中的值，以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="36def-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="36def-1472">查詢下降 \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="36def-1473">資料列會根據指定之資料行中的值，以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="36def-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="36def-1474">**地區** 設定：32位不帶正負號的整數，指出資料行的地區設定（如 \[ GPSI \] 附錄 A 所指定）。</span><span class="sxs-lookup"><span data-stu-id="36def-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="36def-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="36def-1476">CSynRestriction 結構包含查詢片語的單字或其同義字。</span><span class="sxs-lookup"><span data-stu-id="36def-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="36def-1477">0</span><span class="sxs-lookup"><span data-stu-id="36def-1477">0</span></span>

<span data-ttu-id="36def-1478">1</span><span class="sxs-lookup"><span data-stu-id="36def-1478">1</span></span>

<span data-ttu-id="36def-1479">2</span><span class="sxs-lookup"><span data-stu-id="36def-1479">2</span></span>

<span data-ttu-id="36def-1480">3</span><span class="sxs-lookup"><span data-stu-id="36def-1480">3</span></span>

<span data-ttu-id="36def-1481">4</span><span class="sxs-lookup"><span data-stu-id="36def-1481">4</span></span>

<span data-ttu-id="36def-1482">5</span><span class="sxs-lookup"><span data-stu-id="36def-1482">5</span></span>

<span data-ttu-id="36def-1483">6</span><span class="sxs-lookup"><span data-stu-id="36def-1483">6</span></span>

<span data-ttu-id="36def-1484">7</span><span class="sxs-lookup"><span data-stu-id="36def-1484">7</span></span>

<span data-ttu-id="36def-1485">8</span><span class="sxs-lookup"><span data-stu-id="36def-1485">8</span></span>

<span data-ttu-id="36def-1486">9</span><span class="sxs-lookup"><span data-stu-id="36def-1486">9</span></span>

<span data-ttu-id="36def-1487">1</span><span class="sxs-lookup"><span data-stu-id="36def-1487">1</span></span><br/> <span data-ttu-id="36def-1488">0</span><span class="sxs-lookup"><span data-stu-id="36def-1488">0</span></span><br/>

<span data-ttu-id="36def-1489">1</span><span class="sxs-lookup"><span data-stu-id="36def-1489">1</span></span>

<span data-ttu-id="36def-1490">2</span><span class="sxs-lookup"><span data-stu-id="36def-1490">2</span></span>

<span data-ttu-id="36def-1491">3</span><span class="sxs-lookup"><span data-stu-id="36def-1491">3</span></span>

<span data-ttu-id="36def-1492">4</span><span class="sxs-lookup"><span data-stu-id="36def-1492">4</span></span>

<span data-ttu-id="36def-1493">5</span><span class="sxs-lookup"><span data-stu-id="36def-1493">5</span></span>

<span data-ttu-id="36def-1494">6</span><span class="sxs-lookup"><span data-stu-id="36def-1494">6</span></span>

<span data-ttu-id="36def-1495">7</span><span class="sxs-lookup"><span data-stu-id="36def-1495">7</span></span>

<span data-ttu-id="36def-1496">8</span><span class="sxs-lookup"><span data-stu-id="36def-1496">8</span></span>

<span data-ttu-id="36def-1497">9</span><span class="sxs-lookup"><span data-stu-id="36def-1497">9</span></span>

<span data-ttu-id="36def-1498">2</span><span class="sxs-lookup"><span data-stu-id="36def-1498">2</span></span><br/> <span data-ttu-id="36def-1499">0</span><span class="sxs-lookup"><span data-stu-id="36def-1499">0</span></span><br/>

<span data-ttu-id="36def-1500">1</span><span class="sxs-lookup"><span data-stu-id="36def-1500">1</span></span>

<span data-ttu-id="36def-1501">2</span><span class="sxs-lookup"><span data-stu-id="36def-1501">2</span></span>

<span data-ttu-id="36def-1502">3</span><span class="sxs-lookup"><span data-stu-id="36def-1502">3</span></span>

<span data-ttu-id="36def-1503">4</span><span class="sxs-lookup"><span data-stu-id="36def-1503">4</span></span>

<span data-ttu-id="36def-1504">5</span><span class="sxs-lookup"><span data-stu-id="36def-1504">5</span></span>

<span data-ttu-id="36def-1505">6</span><span class="sxs-lookup"><span data-stu-id="36def-1505">6</span></span>

<span data-ttu-id="36def-1506">7</span><span class="sxs-lookup"><span data-stu-id="36def-1506">7</span></span>

<span data-ttu-id="36def-1507">8</span><span class="sxs-lookup"><span data-stu-id="36def-1507">8</span></span>

<span data-ttu-id="36def-1508">9</span><span class="sxs-lookup"><span data-stu-id="36def-1508">9</span></span>

<span data-ttu-id="36def-1509">3</span><span class="sxs-lookup"><span data-stu-id="36def-1509">3</span></span><br/> <span data-ttu-id="36def-1510">0</span><span class="sxs-lookup"><span data-stu-id="36def-1510">0</span></span><br/>

<span data-ttu-id="36def-1511">1</span><span class="sxs-lookup"><span data-stu-id="36def-1511">1</span></span>

<span data-ttu-id="36def-1512">限制</span><span class="sxs-lookup"><span data-stu-id="36def-1512">Restriction</span></span>

<span data-ttu-id="36def-1513">...</span><span class="sxs-lookup"><span data-stu-id="36def-1513">...</span></span>

<span data-ttu-id="36def-1514">...</span><span class="sxs-lookup"><span data-stu-id="36def-1514">...</span></span>

<span data-ttu-id="36def-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="36def-1515">cKey</span></span>

<span data-ttu-id="36def-1516">\_keyArray (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="36def-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="36def-1517">\_isRange</span></span>



 

<span data-ttu-id="36def-1518">**限制**：指定單字位置的 COccRestriction 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="36def-1519">**cKey**：32位不帶正負號的整數，指定 keyArray 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="36def-1520">**\_ keyArray**：指定單字及其同義字的 CKey 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="36def-1521">**\_ isRange**：如果設定為0x01，索引鍵會是要比對的首碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="36def-1522">如果設定為0x00，索引鍵會是要比對的精確值。</span><span class="sxs-lookup"><span data-stu-id="36def-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="36def-1523">\_isRange 不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="36def-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="36def-1525">CVectorRestriction 結構包含命令樹節點上的加權或運算。</span><span class="sxs-lookup"><span data-stu-id="36def-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="36def-1526">0</span><span class="sxs-lookup"><span data-stu-id="36def-1526">0</span></span>

<span data-ttu-id="36def-1527">1</span><span class="sxs-lookup"><span data-stu-id="36def-1527">1</span></span>

<span data-ttu-id="36def-1528">2</span><span class="sxs-lookup"><span data-stu-id="36def-1528">2</span></span>

<span data-ttu-id="36def-1529">3</span><span class="sxs-lookup"><span data-stu-id="36def-1529">3</span></span>

<span data-ttu-id="36def-1530">4</span><span class="sxs-lookup"><span data-stu-id="36def-1530">4</span></span>

<span data-ttu-id="36def-1531">5</span><span class="sxs-lookup"><span data-stu-id="36def-1531">5</span></span>

<span data-ttu-id="36def-1532">6</span><span class="sxs-lookup"><span data-stu-id="36def-1532">6</span></span>

<span data-ttu-id="36def-1533">7</span><span class="sxs-lookup"><span data-stu-id="36def-1533">7</span></span>

<span data-ttu-id="36def-1534">8</span><span class="sxs-lookup"><span data-stu-id="36def-1534">8</span></span>

<span data-ttu-id="36def-1535">9</span><span class="sxs-lookup"><span data-stu-id="36def-1535">9</span></span>

<span data-ttu-id="36def-1536">1</span><span class="sxs-lookup"><span data-stu-id="36def-1536">1</span></span><br/> <span data-ttu-id="36def-1537">0</span><span class="sxs-lookup"><span data-stu-id="36def-1537">0</span></span><br/>

<span data-ttu-id="36def-1538">1</span><span class="sxs-lookup"><span data-stu-id="36def-1538">1</span></span>

<span data-ttu-id="36def-1539">2</span><span class="sxs-lookup"><span data-stu-id="36def-1539">2</span></span>

<span data-ttu-id="36def-1540">3</span><span class="sxs-lookup"><span data-stu-id="36def-1540">3</span></span>

<span data-ttu-id="36def-1541">4</span><span class="sxs-lookup"><span data-stu-id="36def-1541">4</span></span>

<span data-ttu-id="36def-1542">5</span><span class="sxs-lookup"><span data-stu-id="36def-1542">5</span></span>

<span data-ttu-id="36def-1543">6</span><span class="sxs-lookup"><span data-stu-id="36def-1543">6</span></span>

<span data-ttu-id="36def-1544">7</span><span class="sxs-lookup"><span data-stu-id="36def-1544">7</span></span>

<span data-ttu-id="36def-1545">8</span><span class="sxs-lookup"><span data-stu-id="36def-1545">8</span></span>

<span data-ttu-id="36def-1546">9</span><span class="sxs-lookup"><span data-stu-id="36def-1546">9</span></span>

<span data-ttu-id="36def-1547">2</span><span class="sxs-lookup"><span data-stu-id="36def-1547">2</span></span><br/> <span data-ttu-id="36def-1548">0</span><span class="sxs-lookup"><span data-stu-id="36def-1548">0</span></span><br/>

<span data-ttu-id="36def-1549">1</span><span class="sxs-lookup"><span data-stu-id="36def-1549">1</span></span>

<span data-ttu-id="36def-1550">2</span><span class="sxs-lookup"><span data-stu-id="36def-1550">2</span></span>

<span data-ttu-id="36def-1551">3</span><span class="sxs-lookup"><span data-stu-id="36def-1551">3</span></span>

<span data-ttu-id="36def-1552">4</span><span class="sxs-lookup"><span data-stu-id="36def-1552">4</span></span>

<span data-ttu-id="36def-1553">5</span><span class="sxs-lookup"><span data-stu-id="36def-1553">5</span></span>

<span data-ttu-id="36def-1554">6</span><span class="sxs-lookup"><span data-stu-id="36def-1554">6</span></span>

<span data-ttu-id="36def-1555">7</span><span class="sxs-lookup"><span data-stu-id="36def-1555">7</span></span>

<span data-ttu-id="36def-1556">8</span><span class="sxs-lookup"><span data-stu-id="36def-1556">8</span></span>

<span data-ttu-id="36def-1557">9</span><span class="sxs-lookup"><span data-stu-id="36def-1557">9</span></span>

<span data-ttu-id="36def-1558">3</span><span class="sxs-lookup"><span data-stu-id="36def-1558">3</span></span><br/> <span data-ttu-id="36def-1559">0</span><span class="sxs-lookup"><span data-stu-id="36def-1559">0</span></span><br/>

<span data-ttu-id="36def-1560">1</span><span class="sxs-lookup"><span data-stu-id="36def-1560">1</span></span>

<span data-ttu-id="36def-1561">\_按 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1561">\_pres (variable)</span></span>

<span data-ttu-id="36def-1562">...</span><span class="sxs-lookup"><span data-stu-id="36def-1562">...</span></span>

<span data-ttu-id="36def-1563">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1563">\_padding (variable)</span></span>

<span data-ttu-id="36def-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="36def-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="36def-1565">**\_ 按**：要執行排名或運算的 CNodeRestriction 命令樹。</span><span class="sxs-lookup"><span data-stu-id="36def-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="36def-1566">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-1567">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-1568">如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-1569">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-1570">**\_ ulRankMethod**：指定排名演算法的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="36def-1571">必須設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36def-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="36def-1572">值</span><span class="sxs-lookup"><span data-stu-id="36def-1572">Value</span></span>                            | <span data-ttu-id="36def-1573">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="36def-1574">向量 \_ 排名 \_ 最小0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="36def-1575">使用最小演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="36def-1576">向量順 \_ 位 \_ 最大值0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="36def-1577">使用最大演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="36def-1578">向量 \_ 排名 \_ 內部0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="36def-1579">使用內部產品演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="36def-1580">向量順 \_ 位 \_ 骰子0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="36def-1581">使用骰子係數演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="36def-1582">向量順 \_ 位 \_ JACCARD 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="36def-1583">使用 Jaccard 係數演算法 \[ SALTON \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="36def-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="36def-1585">CWordRestriction 結構包含查詢片語的單字。</span><span class="sxs-lookup"><span data-stu-id="36def-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="36def-1586">0</span><span class="sxs-lookup"><span data-stu-id="36def-1586">0</span></span>

<span data-ttu-id="36def-1587">1</span><span class="sxs-lookup"><span data-stu-id="36def-1587">1</span></span>

<span data-ttu-id="36def-1588">2</span><span class="sxs-lookup"><span data-stu-id="36def-1588">2</span></span>

<span data-ttu-id="36def-1589">3</span><span class="sxs-lookup"><span data-stu-id="36def-1589">3</span></span>

<span data-ttu-id="36def-1590">4</span><span class="sxs-lookup"><span data-stu-id="36def-1590">4</span></span>

<span data-ttu-id="36def-1591">5</span><span class="sxs-lookup"><span data-stu-id="36def-1591">5</span></span>

<span data-ttu-id="36def-1592">6</span><span class="sxs-lookup"><span data-stu-id="36def-1592">6</span></span>

<span data-ttu-id="36def-1593">7</span><span class="sxs-lookup"><span data-stu-id="36def-1593">7</span></span>

<span data-ttu-id="36def-1594">8</span><span class="sxs-lookup"><span data-stu-id="36def-1594">8</span></span>

<span data-ttu-id="36def-1595">9</span><span class="sxs-lookup"><span data-stu-id="36def-1595">9</span></span>

<span data-ttu-id="36def-1596">1</span><span class="sxs-lookup"><span data-stu-id="36def-1596">1</span></span><br/> <span data-ttu-id="36def-1597">0</span><span class="sxs-lookup"><span data-stu-id="36def-1597">0</span></span><br/>

<span data-ttu-id="36def-1598">1</span><span class="sxs-lookup"><span data-stu-id="36def-1598">1</span></span>

<span data-ttu-id="36def-1599">2</span><span class="sxs-lookup"><span data-stu-id="36def-1599">2</span></span>

<span data-ttu-id="36def-1600">3</span><span class="sxs-lookup"><span data-stu-id="36def-1600">3</span></span>

<span data-ttu-id="36def-1601">4</span><span class="sxs-lookup"><span data-stu-id="36def-1601">4</span></span>

<span data-ttu-id="36def-1602">5</span><span class="sxs-lookup"><span data-stu-id="36def-1602">5</span></span>

<span data-ttu-id="36def-1603">6</span><span class="sxs-lookup"><span data-stu-id="36def-1603">6</span></span>

<span data-ttu-id="36def-1604">7</span><span class="sxs-lookup"><span data-stu-id="36def-1604">7</span></span>

<span data-ttu-id="36def-1605">8</span><span class="sxs-lookup"><span data-stu-id="36def-1605">8</span></span>

<span data-ttu-id="36def-1606">9</span><span class="sxs-lookup"><span data-stu-id="36def-1606">9</span></span>

<span data-ttu-id="36def-1607">2</span><span class="sxs-lookup"><span data-stu-id="36def-1607">2</span></span><br/> <span data-ttu-id="36def-1608">0</span><span class="sxs-lookup"><span data-stu-id="36def-1608">0</span></span><br/>

<span data-ttu-id="36def-1609">1</span><span class="sxs-lookup"><span data-stu-id="36def-1609">1</span></span>

<span data-ttu-id="36def-1610">2</span><span class="sxs-lookup"><span data-stu-id="36def-1610">2</span></span>

<span data-ttu-id="36def-1611">3</span><span class="sxs-lookup"><span data-stu-id="36def-1611">3</span></span>

<span data-ttu-id="36def-1612">4</span><span class="sxs-lookup"><span data-stu-id="36def-1612">4</span></span>

<span data-ttu-id="36def-1613">5</span><span class="sxs-lookup"><span data-stu-id="36def-1613">5</span></span>

<span data-ttu-id="36def-1614">6</span><span class="sxs-lookup"><span data-stu-id="36def-1614">6</span></span>

<span data-ttu-id="36def-1615">7</span><span class="sxs-lookup"><span data-stu-id="36def-1615">7</span></span>

<span data-ttu-id="36def-1616">8</span><span class="sxs-lookup"><span data-stu-id="36def-1616">8</span></span>

<span data-ttu-id="36def-1617">9</span><span class="sxs-lookup"><span data-stu-id="36def-1617">9</span></span>

<span data-ttu-id="36def-1618">3</span><span class="sxs-lookup"><span data-stu-id="36def-1618">3</span></span><br/> <span data-ttu-id="36def-1619">0</span><span class="sxs-lookup"><span data-stu-id="36def-1619">0</span></span><br/>

<span data-ttu-id="36def-1620">1</span><span class="sxs-lookup"><span data-stu-id="36def-1620">1</span></span>

<span data-ttu-id="36def-1621">限制</span><span class="sxs-lookup"><span data-stu-id="36def-1621">restriction</span></span>

<span data-ttu-id="36def-1622">...</span><span class="sxs-lookup"><span data-stu-id="36def-1622">...</span></span>

<span data-ttu-id="36def-1623">...</span><span class="sxs-lookup"><span data-stu-id="36def-1623">...</span></span>

<span data-ttu-id="36def-1624">\_key (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1624">\_key (variable)</span></span>

<span data-ttu-id="36def-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="36def-1625">\_isRange</span></span>



 

<span data-ttu-id="36def-1626">**限制**：指定單字位置的 COccRestriction 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="36def-1627">**\_ key**：指定單字的 CKey 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="36def-1628">**\_ isRange**：如果設定為0x01，則索引鍵是要比對的前置詞。</span><span class="sxs-lookup"><span data-stu-id="36def-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="36def-1629">如果設定為0x00，則索引鍵是要比對的精確值。</span><span class="sxs-lookup"><span data-stu-id="36def-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="36def-1630">\_isRange 不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="36def-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="36def-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="36def-1632">CRestriction 結構包含查詢命令樹的節點。</span><span class="sxs-lookup"><span data-stu-id="36def-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="36def-1633">0</span><span class="sxs-lookup"><span data-stu-id="36def-1633">0</span></span>

<span data-ttu-id="36def-1634">1</span><span class="sxs-lookup"><span data-stu-id="36def-1634">1</span></span>

<span data-ttu-id="36def-1635">2</span><span class="sxs-lookup"><span data-stu-id="36def-1635">2</span></span>

<span data-ttu-id="36def-1636">3</span><span class="sxs-lookup"><span data-stu-id="36def-1636">3</span></span>

<span data-ttu-id="36def-1637">4</span><span class="sxs-lookup"><span data-stu-id="36def-1637">4</span></span>

<span data-ttu-id="36def-1638">5</span><span class="sxs-lookup"><span data-stu-id="36def-1638">5</span></span>

<span data-ttu-id="36def-1639">6</span><span class="sxs-lookup"><span data-stu-id="36def-1639">6</span></span>

<span data-ttu-id="36def-1640">7</span><span class="sxs-lookup"><span data-stu-id="36def-1640">7</span></span>

<span data-ttu-id="36def-1641">8</span><span class="sxs-lookup"><span data-stu-id="36def-1641">8</span></span>

<span data-ttu-id="36def-1642">9</span><span class="sxs-lookup"><span data-stu-id="36def-1642">9</span></span>

<span data-ttu-id="36def-1643">1</span><span class="sxs-lookup"><span data-stu-id="36def-1643">1</span></span><br/> <span data-ttu-id="36def-1644">0</span><span class="sxs-lookup"><span data-stu-id="36def-1644">0</span></span><br/>

<span data-ttu-id="36def-1645">1</span><span class="sxs-lookup"><span data-stu-id="36def-1645">1</span></span>

<span data-ttu-id="36def-1646">2</span><span class="sxs-lookup"><span data-stu-id="36def-1646">2</span></span>

<span data-ttu-id="36def-1647">3</span><span class="sxs-lookup"><span data-stu-id="36def-1647">3</span></span>

<span data-ttu-id="36def-1648">4</span><span class="sxs-lookup"><span data-stu-id="36def-1648">4</span></span>

<span data-ttu-id="36def-1649">5</span><span class="sxs-lookup"><span data-stu-id="36def-1649">5</span></span>

<span data-ttu-id="36def-1650">6</span><span class="sxs-lookup"><span data-stu-id="36def-1650">6</span></span>

<span data-ttu-id="36def-1651">7</span><span class="sxs-lookup"><span data-stu-id="36def-1651">7</span></span>

<span data-ttu-id="36def-1652">8</span><span class="sxs-lookup"><span data-stu-id="36def-1652">8</span></span>

<span data-ttu-id="36def-1653">9</span><span class="sxs-lookup"><span data-stu-id="36def-1653">9</span></span>

<span data-ttu-id="36def-1654">2</span><span class="sxs-lookup"><span data-stu-id="36def-1654">2</span></span><br/> <span data-ttu-id="36def-1655">0</span><span class="sxs-lookup"><span data-stu-id="36def-1655">0</span></span><br/>

<span data-ttu-id="36def-1656">1</span><span class="sxs-lookup"><span data-stu-id="36def-1656">1</span></span>

<span data-ttu-id="36def-1657">2</span><span class="sxs-lookup"><span data-stu-id="36def-1657">2</span></span>

<span data-ttu-id="36def-1658">3</span><span class="sxs-lookup"><span data-stu-id="36def-1658">3</span></span>

<span data-ttu-id="36def-1659">4</span><span class="sxs-lookup"><span data-stu-id="36def-1659">4</span></span>

<span data-ttu-id="36def-1660">5</span><span class="sxs-lookup"><span data-stu-id="36def-1660">5</span></span>

<span data-ttu-id="36def-1661">6</span><span class="sxs-lookup"><span data-stu-id="36def-1661">6</span></span>

<span data-ttu-id="36def-1662">7</span><span class="sxs-lookup"><span data-stu-id="36def-1662">7</span></span>

<span data-ttu-id="36def-1663">8</span><span class="sxs-lookup"><span data-stu-id="36def-1663">8</span></span>

<span data-ttu-id="36def-1664">9</span><span class="sxs-lookup"><span data-stu-id="36def-1664">9</span></span>

<span data-ttu-id="36def-1665">3</span><span class="sxs-lookup"><span data-stu-id="36def-1665">3</span></span><br/> <span data-ttu-id="36def-1666">0</span><span class="sxs-lookup"><span data-stu-id="36def-1666">0</span></span><br/>

<span data-ttu-id="36def-1667">1</span><span class="sxs-lookup"><span data-stu-id="36def-1667">1</span></span>

<span data-ttu-id="36def-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="36def-1668">\_ulType</span></span>

<span data-ttu-id="36def-1669">Weight</span><span class="sxs-lookup"><span data-stu-id="36def-1669">Weight</span></span>

<span data-ttu-id="36def-1670">限制</span><span class="sxs-lookup"><span data-stu-id="36def-1670">Restriction</span></span>



 

<span data-ttu-id="36def-1671">**\_ ulType**：32位不帶正負號的整數，表示用於命令樹節點的限制類型。</span><span class="sxs-lookup"><span data-stu-id="36def-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="36def-1672">必須設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36def-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="36def-1673">值</span><span class="sxs-lookup"><span data-stu-id="36def-1673">Value</span></span>                    | <span data-ttu-id="36def-1674">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="36def-1676">節點代表向量查詢中的非搜尋字。</span><span class="sxs-lookup"><span data-stu-id="36def-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="36def-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="36def-1678">節點包含要在其上執行邏輯 AND 運算的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="36def-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="36def-1680">節點包含要在其上執行邏輯 OR 運算的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="36def-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="36def-1682">節點包含不會執行任何作業的 CRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="36def-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="36def-1684">節點包含 CContentRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="36def-1685">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="36def-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="36def-1686">節點包含 CPropertyRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="36def-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="36def-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="36def-1688">節點包含要執行鄰近排名的 CNodeRestriction，</span><span class="sxs-lookup"><span data-stu-id="36def-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="36def-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="36def-1690">節點包含 CVectorRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="36def-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="36def-1692">節點包含 CNatLanguageRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="36def-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="36def-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="36def-1694">節點包含 CScopeRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="36def-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="36def-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="36def-1696">節點包含 CInternalPropertyRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="36def-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="36def-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="36def-1698">節點包含 CRangeRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="36def-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="36def-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="36def-1700">節點包含要執行片語相符的 CNodeRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="36def-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="36def-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="36def-1702">節點包含 CSynRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="36def-1703">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="36def-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="36def-1704">節點包含 CWordRestriction。</span><span class="sxs-lookup"><span data-stu-id="36def-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="36def-1705">**權數**：代表節點權數的32位不帶正負號整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="36def-1706">權數表示相對於查詢命令樹中其他節點的節點重要性。</span><span class="sxs-lookup"><span data-stu-id="36def-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="36def-1707">較高的權數值更重要。</span><span class="sxs-lookup"><span data-stu-id="36def-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="36def-1708">**限制**：命令樹節點的限制類型。</span><span class="sxs-lookup"><span data-stu-id="36def-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="36def-1709">語法必須如 \_ ulType 欄位所示。</span><span class="sxs-lookup"><span data-stu-id="36def-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="36def-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="36def-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="36def-1711">CColumnSet 結構會指定要傳回的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="36def-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="36def-1712">此結構一律用於參考特定的 CPidMapper 結構， (區段 2.2.1.23) 。</span><span class="sxs-lookup"><span data-stu-id="36def-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="36def-1713">0</span><span class="sxs-lookup"><span data-stu-id="36def-1713">0</span></span>

<span data-ttu-id="36def-1714">1</span><span class="sxs-lookup"><span data-stu-id="36def-1714">1</span></span>

<span data-ttu-id="36def-1715">2</span><span class="sxs-lookup"><span data-stu-id="36def-1715">2</span></span>

<span data-ttu-id="36def-1716">3</span><span class="sxs-lookup"><span data-stu-id="36def-1716">3</span></span>

<span data-ttu-id="36def-1717">4</span><span class="sxs-lookup"><span data-stu-id="36def-1717">4</span></span>

<span data-ttu-id="36def-1718">5</span><span class="sxs-lookup"><span data-stu-id="36def-1718">5</span></span>

<span data-ttu-id="36def-1719">6</span><span class="sxs-lookup"><span data-stu-id="36def-1719">6</span></span>

<span data-ttu-id="36def-1720">7</span><span class="sxs-lookup"><span data-stu-id="36def-1720">7</span></span>

<span data-ttu-id="36def-1721">8</span><span class="sxs-lookup"><span data-stu-id="36def-1721">8</span></span>

<span data-ttu-id="36def-1722">9</span><span class="sxs-lookup"><span data-stu-id="36def-1722">9</span></span>

<span data-ttu-id="36def-1723">1</span><span class="sxs-lookup"><span data-stu-id="36def-1723">1</span></span><br/> <span data-ttu-id="36def-1724">0</span><span class="sxs-lookup"><span data-stu-id="36def-1724">0</span></span><br/>

<span data-ttu-id="36def-1725">1</span><span class="sxs-lookup"><span data-stu-id="36def-1725">1</span></span>

<span data-ttu-id="36def-1726">2</span><span class="sxs-lookup"><span data-stu-id="36def-1726">2</span></span>

<span data-ttu-id="36def-1727">3</span><span class="sxs-lookup"><span data-stu-id="36def-1727">3</span></span>

<span data-ttu-id="36def-1728">4</span><span class="sxs-lookup"><span data-stu-id="36def-1728">4</span></span>

<span data-ttu-id="36def-1729">5</span><span class="sxs-lookup"><span data-stu-id="36def-1729">5</span></span>

<span data-ttu-id="36def-1730">6</span><span class="sxs-lookup"><span data-stu-id="36def-1730">6</span></span>

<span data-ttu-id="36def-1731">7</span><span class="sxs-lookup"><span data-stu-id="36def-1731">7</span></span>

<span data-ttu-id="36def-1732">8</span><span class="sxs-lookup"><span data-stu-id="36def-1732">8</span></span>

<span data-ttu-id="36def-1733">9</span><span class="sxs-lookup"><span data-stu-id="36def-1733">9</span></span>

<span data-ttu-id="36def-1734">2</span><span class="sxs-lookup"><span data-stu-id="36def-1734">2</span></span><br/> <span data-ttu-id="36def-1735">0</span><span class="sxs-lookup"><span data-stu-id="36def-1735">0</span></span><br/>

<span data-ttu-id="36def-1736">1</span><span class="sxs-lookup"><span data-stu-id="36def-1736">1</span></span>

<span data-ttu-id="36def-1737">2</span><span class="sxs-lookup"><span data-stu-id="36def-1737">2</span></span>

<span data-ttu-id="36def-1738">3</span><span class="sxs-lookup"><span data-stu-id="36def-1738">3</span></span>

<span data-ttu-id="36def-1739">4</span><span class="sxs-lookup"><span data-stu-id="36def-1739">4</span></span>

<span data-ttu-id="36def-1740">5</span><span class="sxs-lookup"><span data-stu-id="36def-1740">5</span></span>

<span data-ttu-id="36def-1741">6</span><span class="sxs-lookup"><span data-stu-id="36def-1741">6</span></span>

<span data-ttu-id="36def-1742">7</span><span class="sxs-lookup"><span data-stu-id="36def-1742">7</span></span>

<span data-ttu-id="36def-1743">8</span><span class="sxs-lookup"><span data-stu-id="36def-1743">8</span></span>

<span data-ttu-id="36def-1744">9</span><span class="sxs-lookup"><span data-stu-id="36def-1744">9</span></span>

<span data-ttu-id="36def-1745">3</span><span class="sxs-lookup"><span data-stu-id="36def-1745">3</span></span><br/> <span data-ttu-id="36def-1746">0</span><span class="sxs-lookup"><span data-stu-id="36def-1746">0</span></span><br/>

<span data-ttu-id="36def-1747">1</span><span class="sxs-lookup"><span data-stu-id="36def-1747">1</span></span>

<span data-ttu-id="36def-1748">count</span><span class="sxs-lookup"><span data-stu-id="36def-1748">count</span></span>

<span data-ttu-id="36def-1749"> (變數的索引) </span><span class="sxs-lookup"><span data-stu-id="36def-1749">indexes (variable)</span></span>



 

<span data-ttu-id="36def-1750">**計數**：指定索引陣列中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="36def-1751">**索引**：4位元組不帶正負號的整數的陣列，代表對應 CPidMapper 結構中 aPropSpec 陣列的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="36def-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="36def-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="36def-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="36def-1753">CCategorizationSet 結構包含有關查詢結果集群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="36def-1754">0</span><span class="sxs-lookup"><span data-stu-id="36def-1754">0</span></span>

<span data-ttu-id="36def-1755">1</span><span class="sxs-lookup"><span data-stu-id="36def-1755">1</span></span>

<span data-ttu-id="36def-1756">2</span><span class="sxs-lookup"><span data-stu-id="36def-1756">2</span></span>

<span data-ttu-id="36def-1757">3</span><span class="sxs-lookup"><span data-stu-id="36def-1757">3</span></span>

<span data-ttu-id="36def-1758">4</span><span class="sxs-lookup"><span data-stu-id="36def-1758">4</span></span>

<span data-ttu-id="36def-1759">5</span><span class="sxs-lookup"><span data-stu-id="36def-1759">5</span></span>

<span data-ttu-id="36def-1760">6</span><span class="sxs-lookup"><span data-stu-id="36def-1760">6</span></span>

<span data-ttu-id="36def-1761">7</span><span class="sxs-lookup"><span data-stu-id="36def-1761">7</span></span>

<span data-ttu-id="36def-1762">8</span><span class="sxs-lookup"><span data-stu-id="36def-1762">8</span></span>

<span data-ttu-id="36def-1763">9</span><span class="sxs-lookup"><span data-stu-id="36def-1763">9</span></span>

<span data-ttu-id="36def-1764">1</span><span class="sxs-lookup"><span data-stu-id="36def-1764">1</span></span><br/> <span data-ttu-id="36def-1765">0</span><span class="sxs-lookup"><span data-stu-id="36def-1765">0</span></span><br/>

<span data-ttu-id="36def-1766">1</span><span class="sxs-lookup"><span data-stu-id="36def-1766">1</span></span>

<span data-ttu-id="36def-1767">2</span><span class="sxs-lookup"><span data-stu-id="36def-1767">2</span></span>

<span data-ttu-id="36def-1768">3</span><span class="sxs-lookup"><span data-stu-id="36def-1768">3</span></span>

<span data-ttu-id="36def-1769">4</span><span class="sxs-lookup"><span data-stu-id="36def-1769">4</span></span>

<span data-ttu-id="36def-1770">5</span><span class="sxs-lookup"><span data-stu-id="36def-1770">5</span></span>

<span data-ttu-id="36def-1771">6</span><span class="sxs-lookup"><span data-stu-id="36def-1771">6</span></span>

<span data-ttu-id="36def-1772">7</span><span class="sxs-lookup"><span data-stu-id="36def-1772">7</span></span>

<span data-ttu-id="36def-1773">8</span><span class="sxs-lookup"><span data-stu-id="36def-1773">8</span></span>

<span data-ttu-id="36def-1774">9</span><span class="sxs-lookup"><span data-stu-id="36def-1774">9</span></span>

<span data-ttu-id="36def-1775">2</span><span class="sxs-lookup"><span data-stu-id="36def-1775">2</span></span><br/> <span data-ttu-id="36def-1776">0</span><span class="sxs-lookup"><span data-stu-id="36def-1776">0</span></span><br/>

<span data-ttu-id="36def-1777">1</span><span class="sxs-lookup"><span data-stu-id="36def-1777">1</span></span>

<span data-ttu-id="36def-1778">2</span><span class="sxs-lookup"><span data-stu-id="36def-1778">2</span></span>

<span data-ttu-id="36def-1779">3</span><span class="sxs-lookup"><span data-stu-id="36def-1779">3</span></span>

<span data-ttu-id="36def-1780">4</span><span class="sxs-lookup"><span data-stu-id="36def-1780">4</span></span>

<span data-ttu-id="36def-1781">5</span><span class="sxs-lookup"><span data-stu-id="36def-1781">5</span></span>

<span data-ttu-id="36def-1782">6</span><span class="sxs-lookup"><span data-stu-id="36def-1782">6</span></span>

<span data-ttu-id="36def-1783">7</span><span class="sxs-lookup"><span data-stu-id="36def-1783">7</span></span>

<span data-ttu-id="36def-1784">8</span><span class="sxs-lookup"><span data-stu-id="36def-1784">8</span></span>

<span data-ttu-id="36def-1785">9</span><span class="sxs-lookup"><span data-stu-id="36def-1785">9</span></span>

<span data-ttu-id="36def-1786">3</span><span class="sxs-lookup"><span data-stu-id="36def-1786">3</span></span><br/> <span data-ttu-id="36def-1787">0</span><span class="sxs-lookup"><span data-stu-id="36def-1787">0</span></span><br/>

<span data-ttu-id="36def-1788">1</span><span class="sxs-lookup"><span data-stu-id="36def-1788">1</span></span>

<span data-ttu-id="36def-1789">count</span><span class="sxs-lookup"><span data-stu-id="36def-1789">count</span></span>

<span data-ttu-id="36def-1790">類別 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1790">categories (variable)</span></span>



 

<span data-ttu-id="36def-1791">**計數**：32位不帶正負號的整數，其中包含分類陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36def-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="36def-1792">**類別**：指定查詢群組的 CCategorizationSpec 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="36def-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="36def-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="36def-1794">CCategorizationSpec 結構包含查詢結果集的群組。</span><span class="sxs-lookup"><span data-stu-id="36def-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="36def-1795">0</span><span class="sxs-lookup"><span data-stu-id="36def-1795">0</span></span>

<span data-ttu-id="36def-1796">1</span><span class="sxs-lookup"><span data-stu-id="36def-1796">1</span></span>

<span data-ttu-id="36def-1797">2</span><span class="sxs-lookup"><span data-stu-id="36def-1797">2</span></span>

<span data-ttu-id="36def-1798">3</span><span class="sxs-lookup"><span data-stu-id="36def-1798">3</span></span>

<span data-ttu-id="36def-1799">4</span><span class="sxs-lookup"><span data-stu-id="36def-1799">4</span></span>

<span data-ttu-id="36def-1800">5</span><span class="sxs-lookup"><span data-stu-id="36def-1800">5</span></span>

<span data-ttu-id="36def-1801">6</span><span class="sxs-lookup"><span data-stu-id="36def-1801">6</span></span>

<span data-ttu-id="36def-1802">7</span><span class="sxs-lookup"><span data-stu-id="36def-1802">7</span></span>

<span data-ttu-id="36def-1803">8</span><span class="sxs-lookup"><span data-stu-id="36def-1803">8</span></span>

<span data-ttu-id="36def-1804">9</span><span class="sxs-lookup"><span data-stu-id="36def-1804">9</span></span>

<span data-ttu-id="36def-1805">1</span><span class="sxs-lookup"><span data-stu-id="36def-1805">1</span></span><br/> <span data-ttu-id="36def-1806">0</span><span class="sxs-lookup"><span data-stu-id="36def-1806">0</span></span><br/>

<span data-ttu-id="36def-1807">1</span><span class="sxs-lookup"><span data-stu-id="36def-1807">1</span></span>

<span data-ttu-id="36def-1808">2</span><span class="sxs-lookup"><span data-stu-id="36def-1808">2</span></span>

<span data-ttu-id="36def-1809">3</span><span class="sxs-lookup"><span data-stu-id="36def-1809">3</span></span>

<span data-ttu-id="36def-1810">4</span><span class="sxs-lookup"><span data-stu-id="36def-1810">4</span></span>

<span data-ttu-id="36def-1811">5</span><span class="sxs-lookup"><span data-stu-id="36def-1811">5</span></span>

<span data-ttu-id="36def-1812">6</span><span class="sxs-lookup"><span data-stu-id="36def-1812">6</span></span>

<span data-ttu-id="36def-1813">7</span><span class="sxs-lookup"><span data-stu-id="36def-1813">7</span></span>

<span data-ttu-id="36def-1814">8</span><span class="sxs-lookup"><span data-stu-id="36def-1814">8</span></span>

<span data-ttu-id="36def-1815">9</span><span class="sxs-lookup"><span data-stu-id="36def-1815">9</span></span>

<span data-ttu-id="36def-1816">2</span><span class="sxs-lookup"><span data-stu-id="36def-1816">2</span></span><br/> <span data-ttu-id="36def-1817">0</span><span class="sxs-lookup"><span data-stu-id="36def-1817">0</span></span><br/>

<span data-ttu-id="36def-1818">1</span><span class="sxs-lookup"><span data-stu-id="36def-1818">1</span></span>

<span data-ttu-id="36def-1819">2</span><span class="sxs-lookup"><span data-stu-id="36def-1819">2</span></span>

<span data-ttu-id="36def-1820">3</span><span class="sxs-lookup"><span data-stu-id="36def-1820">3</span></span>

<span data-ttu-id="36def-1821">4</span><span class="sxs-lookup"><span data-stu-id="36def-1821">4</span></span>

<span data-ttu-id="36def-1822">5</span><span class="sxs-lookup"><span data-stu-id="36def-1822">5</span></span>

<span data-ttu-id="36def-1823">6</span><span class="sxs-lookup"><span data-stu-id="36def-1823">6</span></span>

<span data-ttu-id="36def-1824">7</span><span class="sxs-lookup"><span data-stu-id="36def-1824">7</span></span>

<span data-ttu-id="36def-1825">8</span><span class="sxs-lookup"><span data-stu-id="36def-1825">8</span></span>

<span data-ttu-id="36def-1826">9</span><span class="sxs-lookup"><span data-stu-id="36def-1826">9</span></span>

<span data-ttu-id="36def-1827">3</span><span class="sxs-lookup"><span data-stu-id="36def-1827">3</span></span><br/> <span data-ttu-id="36def-1828">0</span><span class="sxs-lookup"><span data-stu-id="36def-1828">0</span></span><br/>

<span data-ttu-id="36def-1829">1</span><span class="sxs-lookup"><span data-stu-id="36def-1829">1</span></span>

<span data-ttu-id="36def-1830">\_csColumns (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="36def-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="36def-1831">\_ulCategType</span></span>



 

<span data-ttu-id="36def-1832">**\_ CsColumns**： CColumnSet 結構，指出用來將查詢分組的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="36def-1833">**\_ ulCategType**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-1834">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="36def-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="36def-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="36def-1836">CDbColId 結構包含資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="36def-1837">0</span><span class="sxs-lookup"><span data-stu-id="36def-1837">0</span></span>

<span data-ttu-id="36def-1838">1</span><span class="sxs-lookup"><span data-stu-id="36def-1838">1</span></span>

<span data-ttu-id="36def-1839">2</span><span class="sxs-lookup"><span data-stu-id="36def-1839">2</span></span>

<span data-ttu-id="36def-1840">3</span><span class="sxs-lookup"><span data-stu-id="36def-1840">3</span></span>

<span data-ttu-id="36def-1841">4</span><span class="sxs-lookup"><span data-stu-id="36def-1841">4</span></span>

<span data-ttu-id="36def-1842">5</span><span class="sxs-lookup"><span data-stu-id="36def-1842">5</span></span>

<span data-ttu-id="36def-1843">6</span><span class="sxs-lookup"><span data-stu-id="36def-1843">6</span></span>

<span data-ttu-id="36def-1844">7</span><span class="sxs-lookup"><span data-stu-id="36def-1844">7</span></span>

<span data-ttu-id="36def-1845">8</span><span class="sxs-lookup"><span data-stu-id="36def-1845">8</span></span>

<span data-ttu-id="36def-1846">9</span><span class="sxs-lookup"><span data-stu-id="36def-1846">9</span></span>

<span data-ttu-id="36def-1847">1</span><span class="sxs-lookup"><span data-stu-id="36def-1847">1</span></span><br/> <span data-ttu-id="36def-1848">0</span><span class="sxs-lookup"><span data-stu-id="36def-1848">0</span></span><br/>

<span data-ttu-id="36def-1849">1</span><span class="sxs-lookup"><span data-stu-id="36def-1849">1</span></span>

<span data-ttu-id="36def-1850">2</span><span class="sxs-lookup"><span data-stu-id="36def-1850">2</span></span>

<span data-ttu-id="36def-1851">3</span><span class="sxs-lookup"><span data-stu-id="36def-1851">3</span></span>

<span data-ttu-id="36def-1852">4</span><span class="sxs-lookup"><span data-stu-id="36def-1852">4</span></span>

<span data-ttu-id="36def-1853">5</span><span class="sxs-lookup"><span data-stu-id="36def-1853">5</span></span>

<span data-ttu-id="36def-1854">6</span><span class="sxs-lookup"><span data-stu-id="36def-1854">6</span></span>

<span data-ttu-id="36def-1855">7</span><span class="sxs-lookup"><span data-stu-id="36def-1855">7</span></span>

<span data-ttu-id="36def-1856">8</span><span class="sxs-lookup"><span data-stu-id="36def-1856">8</span></span>

<span data-ttu-id="36def-1857">9</span><span class="sxs-lookup"><span data-stu-id="36def-1857">9</span></span>

<span data-ttu-id="36def-1858">2</span><span class="sxs-lookup"><span data-stu-id="36def-1858">2</span></span><br/> <span data-ttu-id="36def-1859">0</span><span class="sxs-lookup"><span data-stu-id="36def-1859">0</span></span><br/>

<span data-ttu-id="36def-1860">1</span><span class="sxs-lookup"><span data-stu-id="36def-1860">1</span></span>

<span data-ttu-id="36def-1861">2</span><span class="sxs-lookup"><span data-stu-id="36def-1861">2</span></span>

<span data-ttu-id="36def-1862">3</span><span class="sxs-lookup"><span data-stu-id="36def-1862">3</span></span>

<span data-ttu-id="36def-1863">4</span><span class="sxs-lookup"><span data-stu-id="36def-1863">4</span></span>

<span data-ttu-id="36def-1864">5</span><span class="sxs-lookup"><span data-stu-id="36def-1864">5</span></span>

<span data-ttu-id="36def-1865">6</span><span class="sxs-lookup"><span data-stu-id="36def-1865">6</span></span>

<span data-ttu-id="36def-1866">7</span><span class="sxs-lookup"><span data-stu-id="36def-1866">7</span></span>

<span data-ttu-id="36def-1867">8</span><span class="sxs-lookup"><span data-stu-id="36def-1867">8</span></span>

<span data-ttu-id="36def-1868">9</span><span class="sxs-lookup"><span data-stu-id="36def-1868">9</span></span>

<span data-ttu-id="36def-1869">3</span><span class="sxs-lookup"><span data-stu-id="36def-1869">3</span></span><br/> <span data-ttu-id="36def-1870">0</span><span class="sxs-lookup"><span data-stu-id="36def-1870">0</span></span><br/>

<span data-ttu-id="36def-1871">1</span><span class="sxs-lookup"><span data-stu-id="36def-1871">1</span></span>

<span data-ttu-id="36def-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="36def-1872">eKind</span></span>

<span data-ttu-id="36def-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="36def-1873">GUID</span></span>

<span data-ttu-id="36def-1874">...</span><span class="sxs-lookup"><span data-stu-id="36def-1874">...</span></span>

<span data-ttu-id="36def-1875">...</span><span class="sxs-lookup"><span data-stu-id="36def-1875">...</span></span>

<span data-ttu-id="36def-1876">...</span><span class="sxs-lookup"><span data-stu-id="36def-1876">...</span></span>

<span data-ttu-id="36def-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="36def-1877">ulId</span></span>

<span data-ttu-id="36def-1878">vString (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1878">vString (variable)</span></span>



 

<span data-ttu-id="36def-1879">**eKind**：必須設定為下列其中一個值，以指出 GUID 和 vValue 的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="36def-1880">值</span><span class="sxs-lookup"><span data-stu-id="36def-1880">Value</span></span>                            | <span data-ttu-id="36def-1881">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1882">DBKIND \_ GUID \_ 名稱0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="36def-1883">vString 包含屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="36def-1884">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="36def-1885">ulId 包含4個位元組的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="36def-1886">DBKIND \_ PGUID \_ NAME 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="36def-1887">vString 包含屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-1887">vString contains a property name.</span></span> <span data-ttu-id="36def-1888">必須將此值視為與 DBKIND \_ GUID 名稱相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="36def-1889">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="36def-1890">ulId 包含4個位元組的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="36def-1891">此值必須與 DBKIND \_ GUID \_ PROPID 相同。</span><span class="sxs-lookup"><span data-stu-id="36def-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="36def-1892">**Guid**：屬性 guid。</span><span class="sxs-lookup"><span data-stu-id="36def-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="36def-1893">**ulId**：如果 EKIND 為 DBKIND \_ GUID \_ PROPID 或 DBKIND \_ PGUID \_ PROPID，則此欄位包含不帶正負號的整數，並指定屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="36def-1894">如果 eKind 為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID \_ NAME，則此欄位包含一個不帶正負號的整數，指定 vString 欄位中包含的 Unicode 字元數。</span><span class="sxs-lookup"><span data-stu-id="36def-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="36def-1895">**vString**：表示屬性名稱的非 Null 終止 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="36def-1896">除非 eKind 欄位設定為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID NAME，否則必須省略它 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="36def-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="36def-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="36def-1898">CDbProp 結構包含屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="36def-1899">0</span><span class="sxs-lookup"><span data-stu-id="36def-1899">0</span></span>

<span data-ttu-id="36def-1900">1</span><span class="sxs-lookup"><span data-stu-id="36def-1900">1</span></span>

<span data-ttu-id="36def-1901">2</span><span class="sxs-lookup"><span data-stu-id="36def-1901">2</span></span>

<span data-ttu-id="36def-1902">3</span><span class="sxs-lookup"><span data-stu-id="36def-1902">3</span></span>

<span data-ttu-id="36def-1903">4</span><span class="sxs-lookup"><span data-stu-id="36def-1903">4</span></span>

<span data-ttu-id="36def-1904">5</span><span class="sxs-lookup"><span data-stu-id="36def-1904">5</span></span>

<span data-ttu-id="36def-1905">6</span><span class="sxs-lookup"><span data-stu-id="36def-1905">6</span></span>

<span data-ttu-id="36def-1906">7</span><span class="sxs-lookup"><span data-stu-id="36def-1906">7</span></span>

<span data-ttu-id="36def-1907">8</span><span class="sxs-lookup"><span data-stu-id="36def-1907">8</span></span>

<span data-ttu-id="36def-1908">9</span><span class="sxs-lookup"><span data-stu-id="36def-1908">9</span></span>

<span data-ttu-id="36def-1909">1</span><span class="sxs-lookup"><span data-stu-id="36def-1909">1</span></span><br/> <span data-ttu-id="36def-1910">0</span><span class="sxs-lookup"><span data-stu-id="36def-1910">0</span></span><br/>

<span data-ttu-id="36def-1911">1</span><span class="sxs-lookup"><span data-stu-id="36def-1911">1</span></span>

<span data-ttu-id="36def-1912">2</span><span class="sxs-lookup"><span data-stu-id="36def-1912">2</span></span>

<span data-ttu-id="36def-1913">3</span><span class="sxs-lookup"><span data-stu-id="36def-1913">3</span></span>

<span data-ttu-id="36def-1914">4</span><span class="sxs-lookup"><span data-stu-id="36def-1914">4</span></span>

<span data-ttu-id="36def-1915">5</span><span class="sxs-lookup"><span data-stu-id="36def-1915">5</span></span>

<span data-ttu-id="36def-1916">6</span><span class="sxs-lookup"><span data-stu-id="36def-1916">6</span></span>

<span data-ttu-id="36def-1917">7</span><span class="sxs-lookup"><span data-stu-id="36def-1917">7</span></span>

<span data-ttu-id="36def-1918">8</span><span class="sxs-lookup"><span data-stu-id="36def-1918">8</span></span>

<span data-ttu-id="36def-1919">9</span><span class="sxs-lookup"><span data-stu-id="36def-1919">9</span></span>

<span data-ttu-id="36def-1920">2</span><span class="sxs-lookup"><span data-stu-id="36def-1920">2</span></span><br/> <span data-ttu-id="36def-1921">0</span><span class="sxs-lookup"><span data-stu-id="36def-1921">0</span></span><br/>

<span data-ttu-id="36def-1922">1</span><span class="sxs-lookup"><span data-stu-id="36def-1922">1</span></span>

<span data-ttu-id="36def-1923">2</span><span class="sxs-lookup"><span data-stu-id="36def-1923">2</span></span>

<span data-ttu-id="36def-1924">3</span><span class="sxs-lookup"><span data-stu-id="36def-1924">3</span></span>

<span data-ttu-id="36def-1925">4</span><span class="sxs-lookup"><span data-stu-id="36def-1925">4</span></span>

<span data-ttu-id="36def-1926">5</span><span class="sxs-lookup"><span data-stu-id="36def-1926">5</span></span>

<span data-ttu-id="36def-1927">6</span><span class="sxs-lookup"><span data-stu-id="36def-1927">6</span></span>

<span data-ttu-id="36def-1928">7</span><span class="sxs-lookup"><span data-stu-id="36def-1928">7</span></span>

<span data-ttu-id="36def-1929">8</span><span class="sxs-lookup"><span data-stu-id="36def-1929">8</span></span>

<span data-ttu-id="36def-1930">9</span><span class="sxs-lookup"><span data-stu-id="36def-1930">9</span></span>

<span data-ttu-id="36def-1931">3</span><span class="sxs-lookup"><span data-stu-id="36def-1931">3</span></span><br/> <span data-ttu-id="36def-1932">0</span><span class="sxs-lookup"><span data-stu-id="36def-1932">0</span></span><br/>

<span data-ttu-id="36def-1933">1</span><span class="sxs-lookup"><span data-stu-id="36def-1933">1</span></span>

<span data-ttu-id="36def-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="36def-1934">DBPROPID</span></span>

<span data-ttu-id="36def-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="36def-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="36def-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="36def-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="36def-1937">colid (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1937">colid (variable)</span></span>

<span data-ttu-id="36def-1938">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-1938">vValue (variable)</span></span>



 

<span data-ttu-id="36def-1939">**DBPROPID**：32位不帶正負號的整數，表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="36def-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="36def-1940">**DBPROPOPTIONS** ：必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="36def-1941">**DBPROPSTATUS**：必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="36def-1942">**colid**： CDbColId 結構（如區段2.2.1.20 所指定），表示要套用屬性的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="36def-1943">**vValue**：包含屬性值的 CBaseStorageVariant。</span><span class="sxs-lookup"><span data-stu-id="36def-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="36def-1944">2.2.1.21.1 屬性</span><span class="sxs-lookup"><span data-stu-id="36def-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="36def-1945">本節將詳細說明 CISP 所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="36def-1946">這些屬性會分成三個屬性集，也就是 CDbPropSet 結構的 guidPropertySet 欄位中的 ident 2.2.1.21.1 ified， (區段 2.2.1.22) 。</span><span class="sxs-lookup"><span data-stu-id="36def-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="36def-1947">下表列出屬於 DBPROPSET \_ FSCIFRMWRK \_ EXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="36def-1948">值</span><span class="sxs-lookup"><span data-stu-id="36def-1948">Value</span></span>                                  | <span data-ttu-id="36def-1949">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1950">DBPROP \_ CI \_ 目錄 \_ 名稱0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="36def-1951">指定要查詢的目錄或目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="36def-1952">值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="36def-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="36def-1953">DBPROP \_ CI \_ 包括 \_ 範圍0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="36def-1954">指定要包含在查詢中的一或多個路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="36def-1955">值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="36def-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="36def-1956">DBPROP \_ CI \_ 範圍 \_ 旗標0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="36def-1957">指定 \_ 要如何處理 DBPROP CI \_ 包含範圍屬性所指定的路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="36def-1958">值必須是 VT \_ I4 或 vt \_ 向量 \| vt \_ I4。</span><span class="sxs-lookup"><span data-stu-id="36def-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="36def-1959">DBPROP \_ CI \_ 查詢 \_ 類型0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="36def-1960">指定查詢的類型。</span><span class="sxs-lookup"><span data-stu-id="36def-1960">Specifies the type of query.</span></span> <span data-ttu-id="36def-1961">CDbColId 必須設定為資料庫 \_ NullID。</span><span class="sxs-lookup"><span data-stu-id="36def-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="36def-1962">下表列出 DBPROP \_ CI \_ 範圍 \_ 旗標屬性的旗標：</span><span class="sxs-lookup"><span data-stu-id="36def-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="36def-1963">值</span><span class="sxs-lookup"><span data-stu-id="36def-1963">Value</span></span>                     | <span data-ttu-id="36def-1964">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1965">查詢 \_ 深度0x01</span><span class="sxs-lookup"><span data-stu-id="36def-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="36def-1966">如果設定，表示範圍目錄和所有子目錄中的檔案都會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="36def-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="36def-1967">如果清除，只有範圍目錄中的檔案才會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="36def-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="36def-1968">不得與查詢 \_ 深度合併。</span><span class="sxs-lookup"><span data-stu-id="36def-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="36def-1969">查詢 \_ 虛擬 \_ 路徑0x02</span><span class="sxs-lookup"><span data-stu-id="36def-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="36def-1970">如果設定，則表示範圍是虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="36def-1971">如果清除，表示範圍是實體目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="36def-1972">下表列出 [DBPROP \_ CI \_ 查詢類型] 屬性的查詢類型 \_ ：</span><span class="sxs-lookup"><span data-stu-id="36def-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="36def-1973">值</span><span class="sxs-lookup"><span data-stu-id="36def-1973">Value</span></span>                     | <span data-ttu-id="36def-1974">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="36def-1976">一般查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="36def-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="36def-1978">查詢正在要求目錄的虛擬根目錄清單。</span><span class="sxs-lookup"><span data-stu-id="36def-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="36def-1979">此值需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="36def-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="36def-1980">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="36def-1981">查詢正在要求索引服務所支援的所有屬性清單。</span><span class="sxs-lookup"><span data-stu-id="36def-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="36def-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="36def-1983">查詢是系統管理作業。</span><span class="sxs-lookup"><span data-stu-id="36def-1983">The query is an administrative operation.</span></span> <span data-ttu-id="36def-1984">此值需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="36def-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="36def-1985">下表列出屬於 DBPROPSET \_ QUERYEXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="36def-1986">值</span><span class="sxs-lookup"><span data-stu-id="36def-1986">Value</span></span>                                      | <span data-ttu-id="36def-1987">意義</span><span class="sxs-lookup"><span data-stu-id="36def-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="36def-1989">指定索引服務處理緩慢查詢的方式。</span><span class="sxs-lookup"><span data-stu-id="36def-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="36def-1990">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="36def-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="36def-1991">若為 TRUE，則允許伺服器讓這些查詢失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="36def-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="36def-1993">指出索引服務是否要執行結果修剪。</span><span class="sxs-lookup"><span data-stu-id="36def-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="36def-1994">若為 TRUE，則伺服器會考慮以將回應時間優化至用戶端的方式來執行結果修剪。</span><span class="sxs-lookup"><span data-stu-id="36def-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="36def-1995">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="36def-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="36def-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="36def-1997">指出用戶端是否支援 VT \_ 向量資料類型。</span><span class="sxs-lookup"><span data-stu-id="36def-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="36def-1998">若為 TRUE，則表示用戶端支援 VT \_ 向量; 如果為 FALSE，則伺服器會將 VT \_ 向量資料類型轉換成 vt \_ 陣列資料類型。</span><span class="sxs-lookup"><span data-stu-id="36def-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="36def-1999">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="36def-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="36def-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="36def-2001">表示要傳回的資料列相符專案。</span><span class="sxs-lookup"><span data-stu-id="36def-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="36def-2002">若為 TRUE，則伺服器會傳回一組相符的資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="36def-2003">如果為 FALSE，則應該傳回最符合的資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="36def-2004">值必須是 VT \_ BOOL。</span><span class="sxs-lookup"><span data-stu-id="36def-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="36def-2005">下表列出屬於 DBPROPSET \_ CIFRMWRKCORE \_ EXT 屬性集一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="36def-2006">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="36def-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="36def-2007">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-2008">DBPROP \_ 機器0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="36def-2009">指定要處理查詢 (s) 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="36def-2010">值必須是 VT \_ bstr 或 vt \_ 陣列 \| VT \_ BSTR。</span><span class="sxs-lookup"><span data-stu-id="36def-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="36def-2011">DBPROP \_ 用戶端 \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="36def-2012">指定索引服務的連接常數。</span><span class="sxs-lookup"><span data-stu-id="36def-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="36def-2013">此值必須是 \_ 包含0x2A4880706FD911D0A80800A0C906241A 的 VT CLSID。</span><span class="sxs-lookup"><span data-stu-id="36def-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="36def-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="36def-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="36def-2015">CDbPropSet 結構包含一組屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="36def-2016">請注意，第一個欄位是固定大小，但可能無法對齊包含此結構之訊息開頭的4位元組倍數的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="36def-2017">不過，cProperties 欄位會對齊，因此格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="36def-2018">0</span><span class="sxs-lookup"><span data-stu-id="36def-2018">0</span></span>

<span data-ttu-id="36def-2019">1</span><span class="sxs-lookup"><span data-stu-id="36def-2019">1</span></span>

<span data-ttu-id="36def-2020">2</span><span class="sxs-lookup"><span data-stu-id="36def-2020">2</span></span>

<span data-ttu-id="36def-2021">3</span><span class="sxs-lookup"><span data-stu-id="36def-2021">3</span></span>

<span data-ttu-id="36def-2022">4</span><span class="sxs-lookup"><span data-stu-id="36def-2022">4</span></span>

<span data-ttu-id="36def-2023">5</span><span class="sxs-lookup"><span data-stu-id="36def-2023">5</span></span>

<span data-ttu-id="36def-2024">6</span><span class="sxs-lookup"><span data-stu-id="36def-2024">6</span></span>

<span data-ttu-id="36def-2025">7</span><span class="sxs-lookup"><span data-stu-id="36def-2025">7</span></span>

<span data-ttu-id="36def-2026">8</span><span class="sxs-lookup"><span data-stu-id="36def-2026">8</span></span>

<span data-ttu-id="36def-2027">9</span><span class="sxs-lookup"><span data-stu-id="36def-2027">9</span></span>

<span data-ttu-id="36def-2028">1</span><span class="sxs-lookup"><span data-stu-id="36def-2028">1</span></span><br/> <span data-ttu-id="36def-2029">0</span><span class="sxs-lookup"><span data-stu-id="36def-2029">0</span></span><br/>

<span data-ttu-id="36def-2030">1</span><span class="sxs-lookup"><span data-stu-id="36def-2030">1</span></span>

<span data-ttu-id="36def-2031">2</span><span class="sxs-lookup"><span data-stu-id="36def-2031">2</span></span>

<span data-ttu-id="36def-2032">3</span><span class="sxs-lookup"><span data-stu-id="36def-2032">3</span></span>

<span data-ttu-id="36def-2033">4</span><span class="sxs-lookup"><span data-stu-id="36def-2033">4</span></span>

<span data-ttu-id="36def-2034">5</span><span class="sxs-lookup"><span data-stu-id="36def-2034">5</span></span>

<span data-ttu-id="36def-2035">6</span><span class="sxs-lookup"><span data-stu-id="36def-2035">6</span></span>

<span data-ttu-id="36def-2036">7</span><span class="sxs-lookup"><span data-stu-id="36def-2036">7</span></span>

<span data-ttu-id="36def-2037">8</span><span class="sxs-lookup"><span data-stu-id="36def-2037">8</span></span>

<span data-ttu-id="36def-2038">9</span><span class="sxs-lookup"><span data-stu-id="36def-2038">9</span></span>

<span data-ttu-id="36def-2039">2</span><span class="sxs-lookup"><span data-stu-id="36def-2039">2</span></span><br/> <span data-ttu-id="36def-2040">0</span><span class="sxs-lookup"><span data-stu-id="36def-2040">0</span></span><br/>

<span data-ttu-id="36def-2041">1</span><span class="sxs-lookup"><span data-stu-id="36def-2041">1</span></span>

<span data-ttu-id="36def-2042">2</span><span class="sxs-lookup"><span data-stu-id="36def-2042">2</span></span>

<span data-ttu-id="36def-2043">3</span><span class="sxs-lookup"><span data-stu-id="36def-2043">3</span></span>

<span data-ttu-id="36def-2044">4</span><span class="sxs-lookup"><span data-stu-id="36def-2044">4</span></span>

<span data-ttu-id="36def-2045">5</span><span class="sxs-lookup"><span data-stu-id="36def-2045">5</span></span>

<span data-ttu-id="36def-2046">6</span><span class="sxs-lookup"><span data-stu-id="36def-2046">6</span></span>

<span data-ttu-id="36def-2047">7</span><span class="sxs-lookup"><span data-stu-id="36def-2047">7</span></span>

<span data-ttu-id="36def-2048">8</span><span class="sxs-lookup"><span data-stu-id="36def-2048">8</span></span>

<span data-ttu-id="36def-2049">9</span><span class="sxs-lookup"><span data-stu-id="36def-2049">9</span></span>

<span data-ttu-id="36def-2050">3</span><span class="sxs-lookup"><span data-stu-id="36def-2050">3</span></span><br/> <span data-ttu-id="36def-2051">0</span><span class="sxs-lookup"><span data-stu-id="36def-2051">0</span></span><br/>

<span data-ttu-id="36def-2052">1</span><span class="sxs-lookup"><span data-stu-id="36def-2052">1</span></span>

<span data-ttu-id="36def-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="36def-2053">guidPropertySet</span></span>

<span data-ttu-id="36def-2054">...</span><span class="sxs-lookup"><span data-stu-id="36def-2054">...</span></span>

<span data-ttu-id="36def-2055">...</span><span class="sxs-lookup"><span data-stu-id="36def-2055">...</span></span>

<span data-ttu-id="36def-2056">...</span><span class="sxs-lookup"><span data-stu-id="36def-2056">...</span></span>

<span data-ttu-id="36def-2057">...</span><span class="sxs-lookup"><span data-stu-id="36def-2057">...</span></span>

<span data-ttu-id="36def-2058">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2058">\_padding (variable)</span></span>

<span data-ttu-id="36def-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="36def-2059">cProperties</span></span>

<span data-ttu-id="36def-2060">aProps (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2060">aProps (variable)</span></span>



 

<span data-ttu-id="36def-2061">**guidPropertySet**：識別屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="36def-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="36def-2062">必須設定為對應到下列其中一個值的二進位格式 (以字串表示表單) 顯示，識別 aProps 欄位中包含之屬性的屬性集。</span><span class="sxs-lookup"><span data-stu-id="36def-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="36def-2063">值/GUID</span><span class="sxs-lookup"><span data-stu-id="36def-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="36def-2064">Name</span><span class="sxs-lookup"><span data-stu-id="36def-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="36def-2065">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="36def-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="36def-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="36def-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="36def-2067">檔案系統內容索引架構屬性集</span><span class="sxs-lookup"><span data-stu-id="36def-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="36def-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="36def-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="36def-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="36def-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="36def-2070">查詢延伸模組屬性集</span><span class="sxs-lookup"><span data-stu-id="36def-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="36def-2071">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="36def-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="36def-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="36def-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="36def-2073">內容索引架構核心屬性集</span><span class="sxs-lookup"><span data-stu-id="36def-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="36def-2074">**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="36def-2075">這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。</span><span class="sxs-lookup"><span data-stu-id="36def-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="36def-2076">如果這個欄位存在 (亦即，長度非零) ，它所包含的值是任意的。</span><span class="sxs-lookup"><span data-stu-id="36def-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="36def-2077">接收者必須忽略此欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-2078">**cProperties**：32位不帶正負號的整數，其中包含 aProps 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="36def-2079">**aProps**： CDbProp 結構的陣列，如區段0中所指定，包含屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="36def-2080">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="36def-2081">如果有填補位元組存在，它們所包含的值就是任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="36def-2082">接收者必須忽略填補位元組的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="36def-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="36def-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="36def-2084">CPidMapper 結構包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="36def-2085">0</span><span class="sxs-lookup"><span data-stu-id="36def-2085">0</span></span>

<span data-ttu-id="36def-2086">1</span><span class="sxs-lookup"><span data-stu-id="36def-2086">1</span></span>

<span data-ttu-id="36def-2087">2</span><span class="sxs-lookup"><span data-stu-id="36def-2087">2</span></span>

<span data-ttu-id="36def-2088">3</span><span class="sxs-lookup"><span data-stu-id="36def-2088">3</span></span>

<span data-ttu-id="36def-2089">4</span><span class="sxs-lookup"><span data-stu-id="36def-2089">4</span></span>

<span data-ttu-id="36def-2090">5</span><span class="sxs-lookup"><span data-stu-id="36def-2090">5</span></span>

<span data-ttu-id="36def-2091">6</span><span class="sxs-lookup"><span data-stu-id="36def-2091">6</span></span>

<span data-ttu-id="36def-2092">7</span><span class="sxs-lookup"><span data-stu-id="36def-2092">7</span></span>

<span data-ttu-id="36def-2093">8</span><span class="sxs-lookup"><span data-stu-id="36def-2093">8</span></span>

<span data-ttu-id="36def-2094">9</span><span class="sxs-lookup"><span data-stu-id="36def-2094">9</span></span>

<span data-ttu-id="36def-2095">1</span><span class="sxs-lookup"><span data-stu-id="36def-2095">1</span></span><br/> <span data-ttu-id="36def-2096">0</span><span class="sxs-lookup"><span data-stu-id="36def-2096">0</span></span><br/>

<span data-ttu-id="36def-2097">1</span><span class="sxs-lookup"><span data-stu-id="36def-2097">1</span></span>

<span data-ttu-id="36def-2098">2</span><span class="sxs-lookup"><span data-stu-id="36def-2098">2</span></span>

<span data-ttu-id="36def-2099">3</span><span class="sxs-lookup"><span data-stu-id="36def-2099">3</span></span>

<span data-ttu-id="36def-2100">4</span><span class="sxs-lookup"><span data-stu-id="36def-2100">4</span></span>

<span data-ttu-id="36def-2101">5</span><span class="sxs-lookup"><span data-stu-id="36def-2101">5</span></span>

<span data-ttu-id="36def-2102">6</span><span class="sxs-lookup"><span data-stu-id="36def-2102">6</span></span>

<span data-ttu-id="36def-2103">7</span><span class="sxs-lookup"><span data-stu-id="36def-2103">7</span></span>

<span data-ttu-id="36def-2104">8</span><span class="sxs-lookup"><span data-stu-id="36def-2104">8</span></span>

<span data-ttu-id="36def-2105">9</span><span class="sxs-lookup"><span data-stu-id="36def-2105">9</span></span>

<span data-ttu-id="36def-2106">2</span><span class="sxs-lookup"><span data-stu-id="36def-2106">2</span></span><br/> <span data-ttu-id="36def-2107">0</span><span class="sxs-lookup"><span data-stu-id="36def-2107">0</span></span><br/>

<span data-ttu-id="36def-2108">1</span><span class="sxs-lookup"><span data-stu-id="36def-2108">1</span></span>

<span data-ttu-id="36def-2109">2</span><span class="sxs-lookup"><span data-stu-id="36def-2109">2</span></span>

<span data-ttu-id="36def-2110">3</span><span class="sxs-lookup"><span data-stu-id="36def-2110">3</span></span>

<span data-ttu-id="36def-2111">4</span><span class="sxs-lookup"><span data-stu-id="36def-2111">4</span></span>

<span data-ttu-id="36def-2112">5</span><span class="sxs-lookup"><span data-stu-id="36def-2112">5</span></span>

<span data-ttu-id="36def-2113">6</span><span class="sxs-lookup"><span data-stu-id="36def-2113">6</span></span>

<span data-ttu-id="36def-2114">7</span><span class="sxs-lookup"><span data-stu-id="36def-2114">7</span></span>

<span data-ttu-id="36def-2115">8</span><span class="sxs-lookup"><span data-stu-id="36def-2115">8</span></span>

<span data-ttu-id="36def-2116">9</span><span class="sxs-lookup"><span data-stu-id="36def-2116">9</span></span>

<span data-ttu-id="36def-2117">3</span><span class="sxs-lookup"><span data-stu-id="36def-2117">3</span></span><br/> <span data-ttu-id="36def-2118">0</span><span class="sxs-lookup"><span data-stu-id="36def-2118">0</span></span><br/>

<span data-ttu-id="36def-2119">1</span><span class="sxs-lookup"><span data-stu-id="36def-2119">1</span></span>

<span data-ttu-id="36def-2120">count</span><span class="sxs-lookup"><span data-stu-id="36def-2120">count</span></span>

<span data-ttu-id="36def-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="36def-2121">aPropSpec</span></span>

<span data-ttu-id="36def-2122">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2122">... (variable)</span></span>



 

<span data-ttu-id="36def-2123">**count**：包含 aPropSpec 陣列中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="36def-2124">**aPropSpec**： CFullPropSpec 結構的陣列，表示要傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="36def-2125">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="36def-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="36def-2126">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="36def-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="36def-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="36def-2128">CRowSeekAt 結構包含在 CPMGetRowsIn 訊息中取得資料列的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="36def-2129">0</span><span class="sxs-lookup"><span data-stu-id="36def-2129">0</span></span>

<span data-ttu-id="36def-2130">1</span><span class="sxs-lookup"><span data-stu-id="36def-2130">1</span></span>

<span data-ttu-id="36def-2131">2</span><span class="sxs-lookup"><span data-stu-id="36def-2131">2</span></span>

<span data-ttu-id="36def-2132">3</span><span class="sxs-lookup"><span data-stu-id="36def-2132">3</span></span>

<span data-ttu-id="36def-2133">4</span><span class="sxs-lookup"><span data-stu-id="36def-2133">4</span></span>

<span data-ttu-id="36def-2134">5</span><span class="sxs-lookup"><span data-stu-id="36def-2134">5</span></span>

<span data-ttu-id="36def-2135">6</span><span class="sxs-lookup"><span data-stu-id="36def-2135">6</span></span>

<span data-ttu-id="36def-2136">7</span><span class="sxs-lookup"><span data-stu-id="36def-2136">7</span></span>

<span data-ttu-id="36def-2137">8</span><span class="sxs-lookup"><span data-stu-id="36def-2137">8</span></span>

<span data-ttu-id="36def-2138">9</span><span class="sxs-lookup"><span data-stu-id="36def-2138">9</span></span>

<span data-ttu-id="36def-2139">1</span><span class="sxs-lookup"><span data-stu-id="36def-2139">1</span></span><br/> <span data-ttu-id="36def-2140">0</span><span class="sxs-lookup"><span data-stu-id="36def-2140">0</span></span><br/>

<span data-ttu-id="36def-2141">1</span><span class="sxs-lookup"><span data-stu-id="36def-2141">1</span></span>

<span data-ttu-id="36def-2142">2</span><span class="sxs-lookup"><span data-stu-id="36def-2142">2</span></span>

<span data-ttu-id="36def-2143">3</span><span class="sxs-lookup"><span data-stu-id="36def-2143">3</span></span>

<span data-ttu-id="36def-2144">4</span><span class="sxs-lookup"><span data-stu-id="36def-2144">4</span></span>

<span data-ttu-id="36def-2145">5</span><span class="sxs-lookup"><span data-stu-id="36def-2145">5</span></span>

<span data-ttu-id="36def-2146">6</span><span class="sxs-lookup"><span data-stu-id="36def-2146">6</span></span>

<span data-ttu-id="36def-2147">7</span><span class="sxs-lookup"><span data-stu-id="36def-2147">7</span></span>

<span data-ttu-id="36def-2148">8</span><span class="sxs-lookup"><span data-stu-id="36def-2148">8</span></span>

<span data-ttu-id="36def-2149">9</span><span class="sxs-lookup"><span data-stu-id="36def-2149">9</span></span>

<span data-ttu-id="36def-2150">2</span><span class="sxs-lookup"><span data-stu-id="36def-2150">2</span></span><br/> <span data-ttu-id="36def-2151">0</span><span class="sxs-lookup"><span data-stu-id="36def-2151">0</span></span><br/>

<span data-ttu-id="36def-2152">1</span><span class="sxs-lookup"><span data-stu-id="36def-2152">1</span></span>

<span data-ttu-id="36def-2153">2</span><span class="sxs-lookup"><span data-stu-id="36def-2153">2</span></span>

<span data-ttu-id="36def-2154">3</span><span class="sxs-lookup"><span data-stu-id="36def-2154">3</span></span>

<span data-ttu-id="36def-2155">4</span><span class="sxs-lookup"><span data-stu-id="36def-2155">4</span></span>

<span data-ttu-id="36def-2156">5</span><span class="sxs-lookup"><span data-stu-id="36def-2156">5</span></span>

<span data-ttu-id="36def-2157">6</span><span class="sxs-lookup"><span data-stu-id="36def-2157">6</span></span>

<span data-ttu-id="36def-2158">7</span><span class="sxs-lookup"><span data-stu-id="36def-2158">7</span></span>

<span data-ttu-id="36def-2159">8</span><span class="sxs-lookup"><span data-stu-id="36def-2159">8</span></span>

<span data-ttu-id="36def-2160">9</span><span class="sxs-lookup"><span data-stu-id="36def-2160">9</span></span>

<span data-ttu-id="36def-2161">3</span><span class="sxs-lookup"><span data-stu-id="36def-2161">3</span></span><br/> <span data-ttu-id="36def-2162">0</span><span class="sxs-lookup"><span data-stu-id="36def-2162">0</span></span><br/>

<span data-ttu-id="36def-2163">1</span><span class="sxs-lookup"><span data-stu-id="36def-2163">1</span></span>

<span data-ttu-id="36def-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="36def-2164">\_hRegion</span></span>

<span data-ttu-id="36def-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="36def-2165">\_cskip</span></span>

<span data-ttu-id="36def-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="36def-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="36def-2167">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="36def-2168">**\_ cskip**：32位不帶正負號的整數，其中包含要在資料列集中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="36def-2169">**\_ bmkOffset**：代表 **書簽** 控制碼的32位值，表示在開始抓取之前，要從中略過 cskip 中指定之資料列數的起始位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="36def-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="36def-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="36def-2171">CRowSeekAtRatio 結構會識別開始抓取 CPMGetRowsIn 訊息的起點。</span><span class="sxs-lookup"><span data-stu-id="36def-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="36def-2172">0</span><span class="sxs-lookup"><span data-stu-id="36def-2172">0</span></span>

<span data-ttu-id="36def-2173">1</span><span class="sxs-lookup"><span data-stu-id="36def-2173">1</span></span>

<span data-ttu-id="36def-2174">2</span><span class="sxs-lookup"><span data-stu-id="36def-2174">2</span></span>

<span data-ttu-id="36def-2175">3</span><span class="sxs-lookup"><span data-stu-id="36def-2175">3</span></span>

<span data-ttu-id="36def-2176">4</span><span class="sxs-lookup"><span data-stu-id="36def-2176">4</span></span>

<span data-ttu-id="36def-2177">5</span><span class="sxs-lookup"><span data-stu-id="36def-2177">5</span></span>

<span data-ttu-id="36def-2178">6</span><span class="sxs-lookup"><span data-stu-id="36def-2178">6</span></span>

<span data-ttu-id="36def-2179">7</span><span class="sxs-lookup"><span data-stu-id="36def-2179">7</span></span>

<span data-ttu-id="36def-2180">8</span><span class="sxs-lookup"><span data-stu-id="36def-2180">8</span></span>

<span data-ttu-id="36def-2181">9</span><span class="sxs-lookup"><span data-stu-id="36def-2181">9</span></span>

<span data-ttu-id="36def-2182">1</span><span class="sxs-lookup"><span data-stu-id="36def-2182">1</span></span><br/> <span data-ttu-id="36def-2183">0</span><span class="sxs-lookup"><span data-stu-id="36def-2183">0</span></span><br/>

<span data-ttu-id="36def-2184">1</span><span class="sxs-lookup"><span data-stu-id="36def-2184">1</span></span>

<span data-ttu-id="36def-2185">2</span><span class="sxs-lookup"><span data-stu-id="36def-2185">2</span></span>

<span data-ttu-id="36def-2186">3</span><span class="sxs-lookup"><span data-stu-id="36def-2186">3</span></span>

<span data-ttu-id="36def-2187">4</span><span class="sxs-lookup"><span data-stu-id="36def-2187">4</span></span>

<span data-ttu-id="36def-2188">5</span><span class="sxs-lookup"><span data-stu-id="36def-2188">5</span></span>

<span data-ttu-id="36def-2189">6</span><span class="sxs-lookup"><span data-stu-id="36def-2189">6</span></span>

<span data-ttu-id="36def-2190">7</span><span class="sxs-lookup"><span data-stu-id="36def-2190">7</span></span>

<span data-ttu-id="36def-2191">8</span><span class="sxs-lookup"><span data-stu-id="36def-2191">8</span></span>

<span data-ttu-id="36def-2192">9</span><span class="sxs-lookup"><span data-stu-id="36def-2192">9</span></span>

<span data-ttu-id="36def-2193">2</span><span class="sxs-lookup"><span data-stu-id="36def-2193">2</span></span><br/> <span data-ttu-id="36def-2194">0</span><span class="sxs-lookup"><span data-stu-id="36def-2194">0</span></span><br/>

<span data-ttu-id="36def-2195">1</span><span class="sxs-lookup"><span data-stu-id="36def-2195">1</span></span>

<span data-ttu-id="36def-2196">2</span><span class="sxs-lookup"><span data-stu-id="36def-2196">2</span></span>

<span data-ttu-id="36def-2197">3</span><span class="sxs-lookup"><span data-stu-id="36def-2197">3</span></span>

<span data-ttu-id="36def-2198">4</span><span class="sxs-lookup"><span data-stu-id="36def-2198">4</span></span>

<span data-ttu-id="36def-2199">5</span><span class="sxs-lookup"><span data-stu-id="36def-2199">5</span></span>

<span data-ttu-id="36def-2200">6</span><span class="sxs-lookup"><span data-stu-id="36def-2200">6</span></span>

<span data-ttu-id="36def-2201">7</span><span class="sxs-lookup"><span data-stu-id="36def-2201">7</span></span>

<span data-ttu-id="36def-2202">8</span><span class="sxs-lookup"><span data-stu-id="36def-2202">8</span></span>

<span data-ttu-id="36def-2203">9</span><span class="sxs-lookup"><span data-stu-id="36def-2203">9</span></span>

<span data-ttu-id="36def-2204">3</span><span class="sxs-lookup"><span data-stu-id="36def-2204">3</span></span><br/> <span data-ttu-id="36def-2205">0</span><span class="sxs-lookup"><span data-stu-id="36def-2205">0</span></span><br/>

<span data-ttu-id="36def-2206">1</span><span class="sxs-lookup"><span data-stu-id="36def-2206">1</span></span>

<span data-ttu-id="36def-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="36def-2207">CiTblChapt</span></span>

<span data-ttu-id="36def-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="36def-2208">\_hRegion</span></span>

<span data-ttu-id="36def-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="36def-2209">\_ulNumerator</span></span>

<span data-ttu-id="36def-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="36def-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="36def-2211">**CiTblChapt**：32位不帶正負號的整數，表示要從中取出資料列的資料列集章節。</span><span class="sxs-lookup"><span data-stu-id="36def-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="36def-2212">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="36def-2213">**\_ ulNumerator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分子。</span><span class="sxs-lookup"><span data-stu-id="36def-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="36def-2214">**\_ ulDenominator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分母。</span><span class="sxs-lookup"><span data-stu-id="36def-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="36def-2215">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="36def-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="36def-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="36def-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="36def-2217">CRowSeekByBookmark 結構會識別要從中開始抓取 CPMGetRowsIn 訊息之資料列的書簽。</span><span class="sxs-lookup"><span data-stu-id="36def-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="36def-2218">0</span><span class="sxs-lookup"><span data-stu-id="36def-2218">0</span></span>

<span data-ttu-id="36def-2219">1</span><span class="sxs-lookup"><span data-stu-id="36def-2219">1</span></span>

<span data-ttu-id="36def-2220">2</span><span class="sxs-lookup"><span data-stu-id="36def-2220">2</span></span>

<span data-ttu-id="36def-2221">3</span><span class="sxs-lookup"><span data-stu-id="36def-2221">3</span></span>

<span data-ttu-id="36def-2222">4</span><span class="sxs-lookup"><span data-stu-id="36def-2222">4</span></span>

<span data-ttu-id="36def-2223">5</span><span class="sxs-lookup"><span data-stu-id="36def-2223">5</span></span>

<span data-ttu-id="36def-2224">6</span><span class="sxs-lookup"><span data-stu-id="36def-2224">6</span></span>

<span data-ttu-id="36def-2225">7</span><span class="sxs-lookup"><span data-stu-id="36def-2225">7</span></span>

<span data-ttu-id="36def-2226">8</span><span class="sxs-lookup"><span data-stu-id="36def-2226">8</span></span>

<span data-ttu-id="36def-2227">9</span><span class="sxs-lookup"><span data-stu-id="36def-2227">9</span></span>

<span data-ttu-id="36def-2228">1</span><span class="sxs-lookup"><span data-stu-id="36def-2228">1</span></span><br/> <span data-ttu-id="36def-2229">0</span><span class="sxs-lookup"><span data-stu-id="36def-2229">0</span></span><br/>

<span data-ttu-id="36def-2230">1</span><span class="sxs-lookup"><span data-stu-id="36def-2230">1</span></span>

<span data-ttu-id="36def-2231">2</span><span class="sxs-lookup"><span data-stu-id="36def-2231">2</span></span>

<span data-ttu-id="36def-2232">3</span><span class="sxs-lookup"><span data-stu-id="36def-2232">3</span></span>

<span data-ttu-id="36def-2233">4</span><span class="sxs-lookup"><span data-stu-id="36def-2233">4</span></span>

<span data-ttu-id="36def-2234">5</span><span class="sxs-lookup"><span data-stu-id="36def-2234">5</span></span>

<span data-ttu-id="36def-2235">6</span><span class="sxs-lookup"><span data-stu-id="36def-2235">6</span></span>

<span data-ttu-id="36def-2236">7</span><span class="sxs-lookup"><span data-stu-id="36def-2236">7</span></span>

<span data-ttu-id="36def-2237">8</span><span class="sxs-lookup"><span data-stu-id="36def-2237">8</span></span>

<span data-ttu-id="36def-2238">9</span><span class="sxs-lookup"><span data-stu-id="36def-2238">9</span></span>

<span data-ttu-id="36def-2239">2</span><span class="sxs-lookup"><span data-stu-id="36def-2239">2</span></span><br/> <span data-ttu-id="36def-2240">0</span><span class="sxs-lookup"><span data-stu-id="36def-2240">0</span></span><br/>

<span data-ttu-id="36def-2241">1</span><span class="sxs-lookup"><span data-stu-id="36def-2241">1</span></span>

<span data-ttu-id="36def-2242">2</span><span class="sxs-lookup"><span data-stu-id="36def-2242">2</span></span>

<span data-ttu-id="36def-2243">3</span><span class="sxs-lookup"><span data-stu-id="36def-2243">3</span></span>

<span data-ttu-id="36def-2244">4</span><span class="sxs-lookup"><span data-stu-id="36def-2244">4</span></span>

<span data-ttu-id="36def-2245">5</span><span class="sxs-lookup"><span data-stu-id="36def-2245">5</span></span>

<span data-ttu-id="36def-2246">6</span><span class="sxs-lookup"><span data-stu-id="36def-2246">6</span></span>

<span data-ttu-id="36def-2247">7</span><span class="sxs-lookup"><span data-stu-id="36def-2247">7</span></span>

<span data-ttu-id="36def-2248">8</span><span class="sxs-lookup"><span data-stu-id="36def-2248">8</span></span>

<span data-ttu-id="36def-2249">9</span><span class="sxs-lookup"><span data-stu-id="36def-2249">9</span></span>

<span data-ttu-id="36def-2250">3</span><span class="sxs-lookup"><span data-stu-id="36def-2250">3</span></span><br/> <span data-ttu-id="36def-2251">0</span><span class="sxs-lookup"><span data-stu-id="36def-2251">0</span></span><br/>

<span data-ttu-id="36def-2252">1</span><span class="sxs-lookup"><span data-stu-id="36def-2252">1</span></span>

<span data-ttu-id="36def-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="36def-2253">\_hRegion</span></span>

<span data-ttu-id="36def-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="36def-2254">\_cBookmarks</span></span>

<span data-ttu-id="36def-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="36def-2255">\_maxRet</span></span>

<span data-ttu-id="36def-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="36def-2256">\_cValidRet</span></span>

<span data-ttu-id="36def-2257">\_aBookmarks (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="36def-2258">\_ascRet (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="36def-2259">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="36def-2260">**\_ cBookmarks**：不帶正負號的32位整數，代表 aBookmarks 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="36def-2261">**\_ maxRet**：不帶正負號的32位整數，代表 ascRet 陣列中的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="36def-2262">**\_ cValidRet**：不帶正負號的32位整數，代表 ascRet 陣列中有效的元素數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="36def-2263">陣列中已定義有效的元素，但不正確元素未定義。</span><span class="sxs-lookup"><span data-stu-id="36def-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="36def-2264">**\_ aBookmarks**：書簽的陣列 (每個) 以4個位元組表示，如同從 CPMGetRowsOut 訊息取得的。</span><span class="sxs-lookup"><span data-stu-id="36def-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="36def-2265">**\_ ASCRET**： HRESULT 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="36def-2266">將 CRowSeekByBookMark 當作 CPMGetRowsIn 要求的一部分傳送時，陣列中的專案數目必須等於 \_ cBookMarks。</span><span class="sxs-lookup"><span data-stu-id="36def-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="36def-2267">當用戶端傳送時，值必須設定為零，而且伺服器必須忽略陣列的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="36def-2268">當伺服器 (傳送) CPMGetRowsOut 訊息的一部分時，陣列中的值會指出每個資料列抓取的結果狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="36def-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="36def-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="36def-2270">CRowSeekNext 結構包含要在 CPMGetRowsIn 訊息中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="36def-2271">0</span><span class="sxs-lookup"><span data-stu-id="36def-2271">0</span></span>

<span data-ttu-id="36def-2272">1</span><span class="sxs-lookup"><span data-stu-id="36def-2272">1</span></span>

<span data-ttu-id="36def-2273">2</span><span class="sxs-lookup"><span data-stu-id="36def-2273">2</span></span>

<span data-ttu-id="36def-2274">3</span><span class="sxs-lookup"><span data-stu-id="36def-2274">3</span></span>

<span data-ttu-id="36def-2275">4</span><span class="sxs-lookup"><span data-stu-id="36def-2275">4</span></span>

<span data-ttu-id="36def-2276">5</span><span class="sxs-lookup"><span data-stu-id="36def-2276">5</span></span>

<span data-ttu-id="36def-2277">6</span><span class="sxs-lookup"><span data-stu-id="36def-2277">6</span></span>

<span data-ttu-id="36def-2278">7</span><span class="sxs-lookup"><span data-stu-id="36def-2278">7</span></span>

<span data-ttu-id="36def-2279">8</span><span class="sxs-lookup"><span data-stu-id="36def-2279">8</span></span>

<span data-ttu-id="36def-2280">9</span><span class="sxs-lookup"><span data-stu-id="36def-2280">9</span></span>

<span data-ttu-id="36def-2281">1</span><span class="sxs-lookup"><span data-stu-id="36def-2281">1</span></span><br/> <span data-ttu-id="36def-2282">0</span><span class="sxs-lookup"><span data-stu-id="36def-2282">0</span></span><br/>

<span data-ttu-id="36def-2283">1</span><span class="sxs-lookup"><span data-stu-id="36def-2283">1</span></span>

<span data-ttu-id="36def-2284">2</span><span class="sxs-lookup"><span data-stu-id="36def-2284">2</span></span>

<span data-ttu-id="36def-2285">3</span><span class="sxs-lookup"><span data-stu-id="36def-2285">3</span></span>

<span data-ttu-id="36def-2286">4</span><span class="sxs-lookup"><span data-stu-id="36def-2286">4</span></span>

<span data-ttu-id="36def-2287">5</span><span class="sxs-lookup"><span data-stu-id="36def-2287">5</span></span>

<span data-ttu-id="36def-2288">6</span><span class="sxs-lookup"><span data-stu-id="36def-2288">6</span></span>

<span data-ttu-id="36def-2289">7</span><span class="sxs-lookup"><span data-stu-id="36def-2289">7</span></span>

<span data-ttu-id="36def-2290">8</span><span class="sxs-lookup"><span data-stu-id="36def-2290">8</span></span>

<span data-ttu-id="36def-2291">9</span><span class="sxs-lookup"><span data-stu-id="36def-2291">9</span></span>

<span data-ttu-id="36def-2292">2</span><span class="sxs-lookup"><span data-stu-id="36def-2292">2</span></span><br/> <span data-ttu-id="36def-2293">0</span><span class="sxs-lookup"><span data-stu-id="36def-2293">0</span></span><br/>

<span data-ttu-id="36def-2294">1</span><span class="sxs-lookup"><span data-stu-id="36def-2294">1</span></span>

<span data-ttu-id="36def-2295">2</span><span class="sxs-lookup"><span data-stu-id="36def-2295">2</span></span>

<span data-ttu-id="36def-2296">3</span><span class="sxs-lookup"><span data-stu-id="36def-2296">3</span></span>

<span data-ttu-id="36def-2297">4</span><span class="sxs-lookup"><span data-stu-id="36def-2297">4</span></span>

<span data-ttu-id="36def-2298">5</span><span class="sxs-lookup"><span data-stu-id="36def-2298">5</span></span>

<span data-ttu-id="36def-2299">6</span><span class="sxs-lookup"><span data-stu-id="36def-2299">6</span></span>

<span data-ttu-id="36def-2300">7</span><span class="sxs-lookup"><span data-stu-id="36def-2300">7</span></span>

<span data-ttu-id="36def-2301">8</span><span class="sxs-lookup"><span data-stu-id="36def-2301">8</span></span>

<span data-ttu-id="36def-2302">9</span><span class="sxs-lookup"><span data-stu-id="36def-2302">9</span></span>

<span data-ttu-id="36def-2303">3</span><span class="sxs-lookup"><span data-stu-id="36def-2303">3</span></span><br/> <span data-ttu-id="36def-2304">0</span><span class="sxs-lookup"><span data-stu-id="36def-2304">0</span></span><br/>

<span data-ttu-id="36def-2305">1</span><span class="sxs-lookup"><span data-stu-id="36def-2305">1</span></span>

<span data-ttu-id="36def-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="36def-2306">CiTblChapt</span></span>

<span data-ttu-id="36def-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="36def-2307">\_hRegion</span></span>

<span data-ttu-id="36def-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="36def-2308">\_cskip</span></span>



 

<span data-ttu-id="36def-2309">**CiTblChapt**：不帶正負號的32位整數，指定要從中取得資料列的資料列集章節。</span><span class="sxs-lookup"><span data-stu-id="36def-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="36def-2310">**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="36def-2311">**\_ cskip**：不帶正負號的32位整數，代表要在資料列集中略過的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="36def-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="36def-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="36def-2313">CRowsetProperties 結構包含查詢的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="36def-2314">0</span><span class="sxs-lookup"><span data-stu-id="36def-2314">0</span></span>

<span data-ttu-id="36def-2315">1</span><span class="sxs-lookup"><span data-stu-id="36def-2315">1</span></span>

<span data-ttu-id="36def-2316">2</span><span class="sxs-lookup"><span data-stu-id="36def-2316">2</span></span>

<span data-ttu-id="36def-2317">3</span><span class="sxs-lookup"><span data-stu-id="36def-2317">3</span></span>

<span data-ttu-id="36def-2318">4</span><span class="sxs-lookup"><span data-stu-id="36def-2318">4</span></span>

<span data-ttu-id="36def-2319">5</span><span class="sxs-lookup"><span data-stu-id="36def-2319">5</span></span>

<span data-ttu-id="36def-2320">6</span><span class="sxs-lookup"><span data-stu-id="36def-2320">6</span></span>

<span data-ttu-id="36def-2321">7</span><span class="sxs-lookup"><span data-stu-id="36def-2321">7</span></span>

<span data-ttu-id="36def-2322">8</span><span class="sxs-lookup"><span data-stu-id="36def-2322">8</span></span>

<span data-ttu-id="36def-2323">9</span><span class="sxs-lookup"><span data-stu-id="36def-2323">9</span></span>

<span data-ttu-id="36def-2324">1</span><span class="sxs-lookup"><span data-stu-id="36def-2324">1</span></span><br/> <span data-ttu-id="36def-2325">0</span><span class="sxs-lookup"><span data-stu-id="36def-2325">0</span></span><br/>

<span data-ttu-id="36def-2326">1</span><span class="sxs-lookup"><span data-stu-id="36def-2326">1</span></span>

<span data-ttu-id="36def-2327">2</span><span class="sxs-lookup"><span data-stu-id="36def-2327">2</span></span>

<span data-ttu-id="36def-2328">3</span><span class="sxs-lookup"><span data-stu-id="36def-2328">3</span></span>

<span data-ttu-id="36def-2329">4</span><span class="sxs-lookup"><span data-stu-id="36def-2329">4</span></span>

<span data-ttu-id="36def-2330">5</span><span class="sxs-lookup"><span data-stu-id="36def-2330">5</span></span>

<span data-ttu-id="36def-2331">6</span><span class="sxs-lookup"><span data-stu-id="36def-2331">6</span></span>

<span data-ttu-id="36def-2332">7</span><span class="sxs-lookup"><span data-stu-id="36def-2332">7</span></span>

<span data-ttu-id="36def-2333">8</span><span class="sxs-lookup"><span data-stu-id="36def-2333">8</span></span>

<span data-ttu-id="36def-2334">9</span><span class="sxs-lookup"><span data-stu-id="36def-2334">9</span></span>

<span data-ttu-id="36def-2335">2</span><span class="sxs-lookup"><span data-stu-id="36def-2335">2</span></span><br/> <span data-ttu-id="36def-2336">0</span><span class="sxs-lookup"><span data-stu-id="36def-2336">0</span></span><br/>

<span data-ttu-id="36def-2337">1</span><span class="sxs-lookup"><span data-stu-id="36def-2337">1</span></span>

<span data-ttu-id="36def-2338">2</span><span class="sxs-lookup"><span data-stu-id="36def-2338">2</span></span>

<span data-ttu-id="36def-2339">3</span><span class="sxs-lookup"><span data-stu-id="36def-2339">3</span></span>

<span data-ttu-id="36def-2340">4</span><span class="sxs-lookup"><span data-stu-id="36def-2340">4</span></span>

<span data-ttu-id="36def-2341">5</span><span class="sxs-lookup"><span data-stu-id="36def-2341">5</span></span>

<span data-ttu-id="36def-2342">6</span><span class="sxs-lookup"><span data-stu-id="36def-2342">6</span></span>

<span data-ttu-id="36def-2343">7</span><span class="sxs-lookup"><span data-stu-id="36def-2343">7</span></span>

<span data-ttu-id="36def-2344">8</span><span class="sxs-lookup"><span data-stu-id="36def-2344">8</span></span>

<span data-ttu-id="36def-2345">9</span><span class="sxs-lookup"><span data-stu-id="36def-2345">9</span></span>

<span data-ttu-id="36def-2346">3</span><span class="sxs-lookup"><span data-stu-id="36def-2346">3</span></span><br/> <span data-ttu-id="36def-2347">0</span><span class="sxs-lookup"><span data-stu-id="36def-2347">0</span></span><br/>

<span data-ttu-id="36def-2348">1</span><span class="sxs-lookup"><span data-stu-id="36def-2348">1</span></span>

<span data-ttu-id="36def-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="36def-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="36def-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="36def-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="36def-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="36def-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="36def-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="36def-2352">\_cMaxResults</span></span>

<span data-ttu-id="36def-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="36def-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="36def-2354">**\_ uBooleanOptions**：此欄位最小的3位必須包含下列三個值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="36def-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="36def-2355">值</span><span class="sxs-lookup"><span data-stu-id="36def-2355">Value</span></span>                  | <span data-ttu-id="36def-2356">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="36def-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="36def-2358">資料指標只能向前移動。</span><span class="sxs-lookup"><span data-stu-id="36def-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="36def-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="36def-2360">資料指標可移至任何位置。</span><span class="sxs-lookup"><span data-stu-id="36def-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="36def-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="36def-2362">您可以將游標移至任何位置，並以任何方向提取。</span><span class="sxs-lookup"><span data-stu-id="36def-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="36def-2363">其餘的位可能是明確的，或設定為邏輯或的任何下列值組合：</span><span class="sxs-lookup"><span data-stu-id="36def-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="36def-2364">值</span><span class="sxs-lookup"><span data-stu-id="36def-2364">Value</span></span>                     | <span data-ttu-id="36def-2365">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="36def-2367">用戶端不會等待執行完成。</span><span class="sxs-lookup"><span data-stu-id="36def-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="36def-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="36def-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="36def-2369">傳回所遇到的第一個資料列，而不是最符合的專案。</span><span class="sxs-lookup"><span data-stu-id="36def-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="36def-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="36def-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="36def-2371">在使用查詢完成用戶端之前，伺服器不能捨棄資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="36def-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="36def-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="36def-2373">資料列集支援章節。</span><span class="sxs-lookup"><span data-stu-id="36def-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="36def-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="36def-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="36def-2375">請只從索引（而不是檔案系統）回答查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="36def-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="36def-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="36def-2377">索引服務是在執行移除結果時，考慮將回應時間優化到用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="36def-2378">**\_ ulMaxOpenRows**：不帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="36def-2379">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="36def-2380">未使用且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="36def-2381">**\_ ulMemoryUsage**：不帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="36def-2382">必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="36def-2383">未使用且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="36def-2384">**\_ cMaxResults**：32位不帶正負號的整數，指定要針對查詢傳回的最大資料列數。</span><span class="sxs-lookup"><span data-stu-id="36def-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="36def-2385">**\_ cCmdTimeout**：32位不帶正負號的整數，指定查詢開始時間和自動終止的秒數，從查詢在伺服器上開始執行的時間算起。</span><span class="sxs-lookup"><span data-stu-id="36def-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="36def-2386">值為0x00000000 表示查詢不會超時。</span><span class="sxs-lookup"><span data-stu-id="36def-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="36def-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="36def-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="36def-2388">CRowVariant 結構包含儲存在 CPMGetRowsOut 訊息中之可變長度資料類型的固定大小部分。</span><span class="sxs-lookup"><span data-stu-id="36def-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="36def-2389">0</span><span class="sxs-lookup"><span data-stu-id="36def-2389">0</span></span>

<span data-ttu-id="36def-2390">1</span><span class="sxs-lookup"><span data-stu-id="36def-2390">1</span></span>

<span data-ttu-id="36def-2391">2</span><span class="sxs-lookup"><span data-stu-id="36def-2391">2</span></span>

<span data-ttu-id="36def-2392">3</span><span class="sxs-lookup"><span data-stu-id="36def-2392">3</span></span>

<span data-ttu-id="36def-2393">4</span><span class="sxs-lookup"><span data-stu-id="36def-2393">4</span></span>

<span data-ttu-id="36def-2394">5</span><span class="sxs-lookup"><span data-stu-id="36def-2394">5</span></span>

<span data-ttu-id="36def-2395">6</span><span class="sxs-lookup"><span data-stu-id="36def-2395">6</span></span>

<span data-ttu-id="36def-2396">7</span><span class="sxs-lookup"><span data-stu-id="36def-2396">7</span></span>

<span data-ttu-id="36def-2397">8</span><span class="sxs-lookup"><span data-stu-id="36def-2397">8</span></span>

<span data-ttu-id="36def-2398">9</span><span class="sxs-lookup"><span data-stu-id="36def-2398">9</span></span>

<span data-ttu-id="36def-2399">1</span><span class="sxs-lookup"><span data-stu-id="36def-2399">1</span></span><br/> <span data-ttu-id="36def-2400">0</span><span class="sxs-lookup"><span data-stu-id="36def-2400">0</span></span><br/>

<span data-ttu-id="36def-2401">1</span><span class="sxs-lookup"><span data-stu-id="36def-2401">1</span></span>

<span data-ttu-id="36def-2402">2</span><span class="sxs-lookup"><span data-stu-id="36def-2402">2</span></span>

<span data-ttu-id="36def-2403">3</span><span class="sxs-lookup"><span data-stu-id="36def-2403">3</span></span>

<span data-ttu-id="36def-2404">4</span><span class="sxs-lookup"><span data-stu-id="36def-2404">4</span></span>

<span data-ttu-id="36def-2405">5</span><span class="sxs-lookup"><span data-stu-id="36def-2405">5</span></span>

<span data-ttu-id="36def-2406">6</span><span class="sxs-lookup"><span data-stu-id="36def-2406">6</span></span>

<span data-ttu-id="36def-2407">7</span><span class="sxs-lookup"><span data-stu-id="36def-2407">7</span></span>

<span data-ttu-id="36def-2408">8</span><span class="sxs-lookup"><span data-stu-id="36def-2408">8</span></span>

<span data-ttu-id="36def-2409">9</span><span class="sxs-lookup"><span data-stu-id="36def-2409">9</span></span>

<span data-ttu-id="36def-2410">2</span><span class="sxs-lookup"><span data-stu-id="36def-2410">2</span></span><br/> <span data-ttu-id="36def-2411">0</span><span class="sxs-lookup"><span data-stu-id="36def-2411">0</span></span><br/>

<span data-ttu-id="36def-2412">1</span><span class="sxs-lookup"><span data-stu-id="36def-2412">1</span></span>

<span data-ttu-id="36def-2413">2</span><span class="sxs-lookup"><span data-stu-id="36def-2413">2</span></span>

<span data-ttu-id="36def-2414">3</span><span class="sxs-lookup"><span data-stu-id="36def-2414">3</span></span>

<span data-ttu-id="36def-2415">4</span><span class="sxs-lookup"><span data-stu-id="36def-2415">4</span></span>

<span data-ttu-id="36def-2416">5</span><span class="sxs-lookup"><span data-stu-id="36def-2416">5</span></span>

<span data-ttu-id="36def-2417">6</span><span class="sxs-lookup"><span data-stu-id="36def-2417">6</span></span>

<span data-ttu-id="36def-2418">7</span><span class="sxs-lookup"><span data-stu-id="36def-2418">7</span></span>

<span data-ttu-id="36def-2419">8</span><span class="sxs-lookup"><span data-stu-id="36def-2419">8</span></span>

<span data-ttu-id="36def-2420">9</span><span class="sxs-lookup"><span data-stu-id="36def-2420">9</span></span>

<span data-ttu-id="36def-2421">3</span><span class="sxs-lookup"><span data-stu-id="36def-2421">3</span></span><br/> <span data-ttu-id="36def-2422">0</span><span class="sxs-lookup"><span data-stu-id="36def-2422">0</span></span><br/>

<span data-ttu-id="36def-2423">1</span><span class="sxs-lookup"><span data-stu-id="36def-2423">1</span></span>

<span data-ttu-id="36def-2424">vType</span><span class="sxs-lookup"><span data-stu-id="36def-2424">vType</span></span>

<span data-ttu-id="36def-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="36def-2425">reserved1</span></span>

<span data-ttu-id="36def-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="36def-2426">reserved2</span></span>

<span data-ttu-id="36def-2427"> (選擇性) 位移</span><span class="sxs-lookup"><span data-stu-id="36def-2427">Offset (optional)</span></span>



 

<span data-ttu-id="36def-2428">**vType**：類型指標，表示 vValue 的類型。</span><span class="sxs-lookup"><span data-stu-id="36def-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="36def-2429">它必須是2.2.1.1 區段中所指定的其中一個 VARENUM 值。</span><span class="sxs-lookup"><span data-stu-id="36def-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="36def-2430">**reserved1**：未使用。</span><span class="sxs-lookup"><span data-stu-id="36def-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="36def-2431">值可以設定為任何任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="36def-2432">**reserved2**：未使用。</span><span class="sxs-lookup"><span data-stu-id="36def-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="36def-2433">值可以設定為任何任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="36def-2434">**Offset**：變數長度資料的位移 (例如字串) 。</span><span class="sxs-lookup"><span data-stu-id="36def-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="36def-2435">這必須是32位值 (4 個位元組長) 如果32位位移是使用於區段 2.2.3.16) 中的規則 (，或64位元組的值 (8 個位元組長) 如果使用的是64位位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="36def-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="36def-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="36def-2437">CSortSet 結構包含查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="36def-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="36def-2438">0</span><span class="sxs-lookup"><span data-stu-id="36def-2438">0</span></span>

<span data-ttu-id="36def-2439">1</span><span class="sxs-lookup"><span data-stu-id="36def-2439">1</span></span>

<span data-ttu-id="36def-2440">2</span><span class="sxs-lookup"><span data-stu-id="36def-2440">2</span></span>

<span data-ttu-id="36def-2441">3</span><span class="sxs-lookup"><span data-stu-id="36def-2441">3</span></span>

<span data-ttu-id="36def-2442">4</span><span class="sxs-lookup"><span data-stu-id="36def-2442">4</span></span>

<span data-ttu-id="36def-2443">5</span><span class="sxs-lookup"><span data-stu-id="36def-2443">5</span></span>

<span data-ttu-id="36def-2444">6</span><span class="sxs-lookup"><span data-stu-id="36def-2444">6</span></span>

<span data-ttu-id="36def-2445">7</span><span class="sxs-lookup"><span data-stu-id="36def-2445">7</span></span>

<span data-ttu-id="36def-2446">8</span><span class="sxs-lookup"><span data-stu-id="36def-2446">8</span></span>

<span data-ttu-id="36def-2447">9</span><span class="sxs-lookup"><span data-stu-id="36def-2447">9</span></span>

<span data-ttu-id="36def-2448">1</span><span class="sxs-lookup"><span data-stu-id="36def-2448">1</span></span><br/> <span data-ttu-id="36def-2449">0</span><span class="sxs-lookup"><span data-stu-id="36def-2449">0</span></span><br/>

<span data-ttu-id="36def-2450">1</span><span class="sxs-lookup"><span data-stu-id="36def-2450">1</span></span>

<span data-ttu-id="36def-2451">2</span><span class="sxs-lookup"><span data-stu-id="36def-2451">2</span></span>

<span data-ttu-id="36def-2452">3</span><span class="sxs-lookup"><span data-stu-id="36def-2452">3</span></span>

<span data-ttu-id="36def-2453">4</span><span class="sxs-lookup"><span data-stu-id="36def-2453">4</span></span>

<span data-ttu-id="36def-2454">5</span><span class="sxs-lookup"><span data-stu-id="36def-2454">5</span></span>

<span data-ttu-id="36def-2455">6</span><span class="sxs-lookup"><span data-stu-id="36def-2455">6</span></span>

<span data-ttu-id="36def-2456">7</span><span class="sxs-lookup"><span data-stu-id="36def-2456">7</span></span>

<span data-ttu-id="36def-2457">8</span><span class="sxs-lookup"><span data-stu-id="36def-2457">8</span></span>

<span data-ttu-id="36def-2458">9</span><span class="sxs-lookup"><span data-stu-id="36def-2458">9</span></span>

<span data-ttu-id="36def-2459">2</span><span class="sxs-lookup"><span data-stu-id="36def-2459">2</span></span><br/> <span data-ttu-id="36def-2460">0</span><span class="sxs-lookup"><span data-stu-id="36def-2460">0</span></span><br/>

<span data-ttu-id="36def-2461">1</span><span class="sxs-lookup"><span data-stu-id="36def-2461">1</span></span>

<span data-ttu-id="36def-2462">2</span><span class="sxs-lookup"><span data-stu-id="36def-2462">2</span></span>

<span data-ttu-id="36def-2463">3</span><span class="sxs-lookup"><span data-stu-id="36def-2463">3</span></span>

<span data-ttu-id="36def-2464">4</span><span class="sxs-lookup"><span data-stu-id="36def-2464">4</span></span>

<span data-ttu-id="36def-2465">5</span><span class="sxs-lookup"><span data-stu-id="36def-2465">5</span></span>

<span data-ttu-id="36def-2466">6</span><span class="sxs-lookup"><span data-stu-id="36def-2466">6</span></span>

<span data-ttu-id="36def-2467">7</span><span class="sxs-lookup"><span data-stu-id="36def-2467">7</span></span>

<span data-ttu-id="36def-2468">8</span><span class="sxs-lookup"><span data-stu-id="36def-2468">8</span></span>

<span data-ttu-id="36def-2469">9</span><span class="sxs-lookup"><span data-stu-id="36def-2469">9</span></span>

<span data-ttu-id="36def-2470">3</span><span class="sxs-lookup"><span data-stu-id="36def-2470">3</span></span><br/> <span data-ttu-id="36def-2471">0</span><span class="sxs-lookup"><span data-stu-id="36def-2471">0</span></span><br/>

<span data-ttu-id="36def-2472">1</span><span class="sxs-lookup"><span data-stu-id="36def-2472">1</span></span>

<span data-ttu-id="36def-2473">Count</span><span class="sxs-lookup"><span data-stu-id="36def-2473">Count</span></span>

<span data-ttu-id="36def-2474">sortArray (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="36def-2475">**計數**：指定 sortArray 中元素數目的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="36def-2476">**sortArray**： CSort 結構的陣列，描述排序查詢結果的順序。</span><span class="sxs-lookup"><span data-stu-id="36def-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="36def-2477">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="36def-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="36def-2478">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="36def-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="36def-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="36def-2480">CTableColumn 結構包含 CPMSetBindingsIn 訊息的資料行</span><span class="sxs-lookup"><span data-stu-id="36def-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="36def-2481">0</span><span class="sxs-lookup"><span data-stu-id="36def-2481">0</span></span>

<span data-ttu-id="36def-2482">1</span><span class="sxs-lookup"><span data-stu-id="36def-2482">1</span></span>

<span data-ttu-id="36def-2483">2</span><span class="sxs-lookup"><span data-stu-id="36def-2483">2</span></span>

<span data-ttu-id="36def-2484">3</span><span class="sxs-lookup"><span data-stu-id="36def-2484">3</span></span>

<span data-ttu-id="36def-2485">4</span><span class="sxs-lookup"><span data-stu-id="36def-2485">4</span></span>

<span data-ttu-id="36def-2486">5</span><span class="sxs-lookup"><span data-stu-id="36def-2486">5</span></span>

<span data-ttu-id="36def-2487">6</span><span class="sxs-lookup"><span data-stu-id="36def-2487">6</span></span>

<span data-ttu-id="36def-2488">7</span><span class="sxs-lookup"><span data-stu-id="36def-2488">7</span></span>

<span data-ttu-id="36def-2489">8</span><span class="sxs-lookup"><span data-stu-id="36def-2489">8</span></span>

<span data-ttu-id="36def-2490">9</span><span class="sxs-lookup"><span data-stu-id="36def-2490">9</span></span>

<span data-ttu-id="36def-2491">1</span><span class="sxs-lookup"><span data-stu-id="36def-2491">1</span></span><br/> <span data-ttu-id="36def-2492">0</span><span class="sxs-lookup"><span data-stu-id="36def-2492">0</span></span><br/>

<span data-ttu-id="36def-2493">1</span><span class="sxs-lookup"><span data-stu-id="36def-2493">1</span></span>

<span data-ttu-id="36def-2494">2</span><span class="sxs-lookup"><span data-stu-id="36def-2494">2</span></span>

<span data-ttu-id="36def-2495">3</span><span class="sxs-lookup"><span data-stu-id="36def-2495">3</span></span>

<span data-ttu-id="36def-2496">4</span><span class="sxs-lookup"><span data-stu-id="36def-2496">4</span></span>

<span data-ttu-id="36def-2497">5</span><span class="sxs-lookup"><span data-stu-id="36def-2497">5</span></span>

<span data-ttu-id="36def-2498">6</span><span class="sxs-lookup"><span data-stu-id="36def-2498">6</span></span>

<span data-ttu-id="36def-2499">7</span><span class="sxs-lookup"><span data-stu-id="36def-2499">7</span></span>

<span data-ttu-id="36def-2500">8</span><span class="sxs-lookup"><span data-stu-id="36def-2500">8</span></span>

<span data-ttu-id="36def-2501">9</span><span class="sxs-lookup"><span data-stu-id="36def-2501">9</span></span>

<span data-ttu-id="36def-2502">2</span><span class="sxs-lookup"><span data-stu-id="36def-2502">2</span></span><br/> <span data-ttu-id="36def-2503">0</span><span class="sxs-lookup"><span data-stu-id="36def-2503">0</span></span><br/>

<span data-ttu-id="36def-2504">1</span><span class="sxs-lookup"><span data-stu-id="36def-2504">1</span></span>

<span data-ttu-id="36def-2505">2</span><span class="sxs-lookup"><span data-stu-id="36def-2505">2</span></span>

<span data-ttu-id="36def-2506">3</span><span class="sxs-lookup"><span data-stu-id="36def-2506">3</span></span>

<span data-ttu-id="36def-2507">4</span><span class="sxs-lookup"><span data-stu-id="36def-2507">4</span></span>

<span data-ttu-id="36def-2508">5</span><span class="sxs-lookup"><span data-stu-id="36def-2508">5</span></span>

<span data-ttu-id="36def-2509">6</span><span class="sxs-lookup"><span data-stu-id="36def-2509">6</span></span>

<span data-ttu-id="36def-2510">7</span><span class="sxs-lookup"><span data-stu-id="36def-2510">7</span></span>

<span data-ttu-id="36def-2511">8</span><span class="sxs-lookup"><span data-stu-id="36def-2511">8</span></span>

<span data-ttu-id="36def-2512">9</span><span class="sxs-lookup"><span data-stu-id="36def-2512">9</span></span>

<span data-ttu-id="36def-2513">3</span><span class="sxs-lookup"><span data-stu-id="36def-2513">3</span></span><br/> <span data-ttu-id="36def-2514">0</span><span class="sxs-lookup"><span data-stu-id="36def-2514">0</span></span><br/>

<span data-ttu-id="36def-2515">1</span><span class="sxs-lookup"><span data-stu-id="36def-2515">1</span></span>

<span data-ttu-id="36def-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="36def-2516">PropSpec</span></span>

<span data-ttu-id="36def-2517">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2517">...(variable)</span></span>

<span data-ttu-id="36def-2518">vType</span><span class="sxs-lookup"><span data-stu-id="36def-2518">vType</span></span>

<span data-ttu-id="36def-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="36def-2519">ValueUsed</span></span>

<span data-ttu-id="36def-2520">\_padding1 (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="36def-2521">ValueOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="36def-2522">ValueSize (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2522">ValueSize (optional)</span></span>

<span data-ttu-id="36def-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="36def-2523">StatusUsed</span></span>

<span data-ttu-id="36def-2524">\_padding2 (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="36def-2525">StatusOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="36def-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="36def-2526">LengthUsed</span></span>

<span data-ttu-id="36def-2527">\_padding3 (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="36def-2528">LengthOffset (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="36def-2529">**PropSpec**：在區段2.2.1.3 中指定的 CFullPropSpec 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="36def-2530">**vType**：指定包含在資料行中的資料數值型別。</span><span class="sxs-lookup"><span data-stu-id="36def-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="36def-2531">如需此欄位的值清單，請參閱2.2.1.1 一節中的 vType 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="36def-2532">**ValueUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="36def-2533">如果設定為0x01，資料行會在固定大小的資料列內傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="36def-2534">如果設定為0x00，則資料行的值會在緩衝區結尾的可變長度區段中傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="36def-2535">**\_ padding1**：一個位元組欄位必須在 ValueOffset 之前插入，如果沒有，則 ValueOffset 不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="36def-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="36def-2536">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="36def-2537">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2538">**ValueOffset**：不帶正負號的2位元組整數，指定資料列中資料行值的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="36def-2539">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2540">**ValueSize**：不帶正負號的2位元組整數，指定資料行值的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="36def-2541">如果 ValueUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2542">**StatusUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="36def-2543">如果設定為0x01，資料行的狀態就會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="36def-2544">若為0x00，則資料行的狀態不會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="36def-2545">**\_ padding2**：一個位元組欄位必須在 StatusOffset 之前插入，如果沒有此欄位，StatusOffset 欄位就不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="36def-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="36def-2546">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="36def-2547">如果 StatusUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2548">**StatusOffset**：不帶正負號的2位元組整數，指定資料列中資料行狀態的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="36def-2549">如果 StatusUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2550">**LengthUsed**：必須設定為0x01 或0x00 的一個位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="36def-2551">如果設定為0x01，資料行的長度會在資料列中傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="36def-2552">如果0x00，則資料行的長度不能在資料列內傳輸。</span><span class="sxs-lookup"><span data-stu-id="36def-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="36def-2553">**\_ padding3**：一個位元組欄位必須在 LengthOffset 之前插入，如果沒有，則 LengthOffset 不會從訊息開頭的平均位移開始。</span><span class="sxs-lookup"><span data-stu-id="36def-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="36def-2554">此位元組的值是任意的，且必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="36def-2555">如果 LengthUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="36def-2556">**LengthOffset**：不帶正負號的2位元組整數，指定資料列中資料行長度的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="36def-2557">如果 LengthUsed 設定為0x00，就不能有此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="36def-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="36def-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="36def-2559">SERIALIZEDPROPERTYVALUE 結構包含序列化值。</span><span class="sxs-lookup"><span data-stu-id="36def-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="36def-2560">0</span><span class="sxs-lookup"><span data-stu-id="36def-2560">0</span></span>

<span data-ttu-id="36def-2561">1</span><span class="sxs-lookup"><span data-stu-id="36def-2561">1</span></span>

<span data-ttu-id="36def-2562">2</span><span class="sxs-lookup"><span data-stu-id="36def-2562">2</span></span>

<span data-ttu-id="36def-2563">3</span><span class="sxs-lookup"><span data-stu-id="36def-2563">3</span></span>

<span data-ttu-id="36def-2564">4</span><span class="sxs-lookup"><span data-stu-id="36def-2564">4</span></span>

<span data-ttu-id="36def-2565">5</span><span class="sxs-lookup"><span data-stu-id="36def-2565">5</span></span>

<span data-ttu-id="36def-2566">6</span><span class="sxs-lookup"><span data-stu-id="36def-2566">6</span></span>

<span data-ttu-id="36def-2567">7</span><span class="sxs-lookup"><span data-stu-id="36def-2567">7</span></span>

<span data-ttu-id="36def-2568">8</span><span class="sxs-lookup"><span data-stu-id="36def-2568">8</span></span>

<span data-ttu-id="36def-2569">9</span><span class="sxs-lookup"><span data-stu-id="36def-2569">9</span></span>

<span data-ttu-id="36def-2570">1</span><span class="sxs-lookup"><span data-stu-id="36def-2570">1</span></span><br/> <span data-ttu-id="36def-2571">0</span><span class="sxs-lookup"><span data-stu-id="36def-2571">0</span></span><br/>

<span data-ttu-id="36def-2572">1</span><span class="sxs-lookup"><span data-stu-id="36def-2572">1</span></span>

<span data-ttu-id="36def-2573">2</span><span class="sxs-lookup"><span data-stu-id="36def-2573">2</span></span>

<span data-ttu-id="36def-2574">3</span><span class="sxs-lookup"><span data-stu-id="36def-2574">3</span></span>

<span data-ttu-id="36def-2575">4</span><span class="sxs-lookup"><span data-stu-id="36def-2575">4</span></span>

<span data-ttu-id="36def-2576">5</span><span class="sxs-lookup"><span data-stu-id="36def-2576">5</span></span>

<span data-ttu-id="36def-2577">6</span><span class="sxs-lookup"><span data-stu-id="36def-2577">6</span></span>

<span data-ttu-id="36def-2578">7</span><span class="sxs-lookup"><span data-stu-id="36def-2578">7</span></span>

<span data-ttu-id="36def-2579">8</span><span class="sxs-lookup"><span data-stu-id="36def-2579">8</span></span>

<span data-ttu-id="36def-2580">9</span><span class="sxs-lookup"><span data-stu-id="36def-2580">9</span></span>

<span data-ttu-id="36def-2581">2</span><span class="sxs-lookup"><span data-stu-id="36def-2581">2</span></span><br/> <span data-ttu-id="36def-2582">0</span><span class="sxs-lookup"><span data-stu-id="36def-2582">0</span></span><br/>

<span data-ttu-id="36def-2583">1</span><span class="sxs-lookup"><span data-stu-id="36def-2583">1</span></span>

<span data-ttu-id="36def-2584">2</span><span class="sxs-lookup"><span data-stu-id="36def-2584">2</span></span>

<span data-ttu-id="36def-2585">3</span><span class="sxs-lookup"><span data-stu-id="36def-2585">3</span></span>

<span data-ttu-id="36def-2586">4</span><span class="sxs-lookup"><span data-stu-id="36def-2586">4</span></span>

<span data-ttu-id="36def-2587">5</span><span class="sxs-lookup"><span data-stu-id="36def-2587">5</span></span>

<span data-ttu-id="36def-2588">6</span><span class="sxs-lookup"><span data-stu-id="36def-2588">6</span></span>

<span data-ttu-id="36def-2589">7</span><span class="sxs-lookup"><span data-stu-id="36def-2589">7</span></span>

<span data-ttu-id="36def-2590">8</span><span class="sxs-lookup"><span data-stu-id="36def-2590">8</span></span>

<span data-ttu-id="36def-2591">9</span><span class="sxs-lookup"><span data-stu-id="36def-2591">9</span></span>

<span data-ttu-id="36def-2592">3</span><span class="sxs-lookup"><span data-stu-id="36def-2592">3</span></span><br/> <span data-ttu-id="36def-2593">0</span><span class="sxs-lookup"><span data-stu-id="36def-2593">0</span></span><br/>

<span data-ttu-id="36def-2594">1</span><span class="sxs-lookup"><span data-stu-id="36def-2594">1</span></span>

<span data-ttu-id="36def-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="36def-2595">dwType</span></span>

<span data-ttu-id="36def-2596">rgb (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-2596">rgb (variable)</span></span>



 

<span data-ttu-id="36def-2597">**dwType**：在 section 2.2.1.1 中定義的其中一個 variant 類型，可以與 variant 類型修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="36def-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="36def-2598">針對所有 variant 類型，除了與 VT 陣列結合的類型之外， \_ SERIALIZEDPROPERTYVALUE 具有與 CBaseStorageVariant 相同的版面配置，如2.2.1.1 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="36def-2599">如果 variant 類型與 VT \_ 陣列類型修飾詞結合，則會使用 SAFEARRAY2 （在2.2.1.2.1.1 區段中指定），而不是 CBaseStorageVariant 的 vValue 欄位中的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="36def-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="36def-2600">**rgb**：序列化值。</span><span class="sxs-lookup"><span data-stu-id="36def-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="36def-2601">請參閱2.2.1.1 中 vValue 的序列化詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36def-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="36def-2602">2.2.2 訊息標頭</span><span class="sxs-lookup"><span data-stu-id="36def-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="36def-2603">所有內容索引服務通訊協定訊息都有16位元組的標頭。</span><span class="sxs-lookup"><span data-stu-id="36def-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="36def-2604">以下是顯示內容索引服務通訊協定訊息標頭格式的圖表。</span><span class="sxs-lookup"><span data-stu-id="36def-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="36def-2605">0</span><span class="sxs-lookup"><span data-stu-id="36def-2605">0</span></span>

<span data-ttu-id="36def-2606">1</span><span class="sxs-lookup"><span data-stu-id="36def-2606">1</span></span>

<span data-ttu-id="36def-2607">2</span><span class="sxs-lookup"><span data-stu-id="36def-2607">2</span></span>

<span data-ttu-id="36def-2608">3</span><span class="sxs-lookup"><span data-stu-id="36def-2608">3</span></span>

<span data-ttu-id="36def-2609">4</span><span class="sxs-lookup"><span data-stu-id="36def-2609">4</span></span>

<span data-ttu-id="36def-2610">5</span><span class="sxs-lookup"><span data-stu-id="36def-2610">5</span></span>

<span data-ttu-id="36def-2611">6</span><span class="sxs-lookup"><span data-stu-id="36def-2611">6</span></span>

<span data-ttu-id="36def-2612">7</span><span class="sxs-lookup"><span data-stu-id="36def-2612">7</span></span>

<span data-ttu-id="36def-2613">8</span><span class="sxs-lookup"><span data-stu-id="36def-2613">8</span></span>

<span data-ttu-id="36def-2614">9</span><span class="sxs-lookup"><span data-stu-id="36def-2614">9</span></span>

<span data-ttu-id="36def-2615">1</span><span class="sxs-lookup"><span data-stu-id="36def-2615">1</span></span><br/> <span data-ttu-id="36def-2616">0</span><span class="sxs-lookup"><span data-stu-id="36def-2616">0</span></span><br/>

<span data-ttu-id="36def-2617">1</span><span class="sxs-lookup"><span data-stu-id="36def-2617">1</span></span>

<span data-ttu-id="36def-2618">2</span><span class="sxs-lookup"><span data-stu-id="36def-2618">2</span></span>

<span data-ttu-id="36def-2619">3</span><span class="sxs-lookup"><span data-stu-id="36def-2619">3</span></span>

<span data-ttu-id="36def-2620">4</span><span class="sxs-lookup"><span data-stu-id="36def-2620">4</span></span>

<span data-ttu-id="36def-2621">5</span><span class="sxs-lookup"><span data-stu-id="36def-2621">5</span></span>

<span data-ttu-id="36def-2622">6</span><span class="sxs-lookup"><span data-stu-id="36def-2622">6</span></span>

<span data-ttu-id="36def-2623">7</span><span class="sxs-lookup"><span data-stu-id="36def-2623">7</span></span>

<span data-ttu-id="36def-2624">8</span><span class="sxs-lookup"><span data-stu-id="36def-2624">8</span></span>

<span data-ttu-id="36def-2625">9</span><span class="sxs-lookup"><span data-stu-id="36def-2625">9</span></span>

<span data-ttu-id="36def-2626">2</span><span class="sxs-lookup"><span data-stu-id="36def-2626">2</span></span><br/> <span data-ttu-id="36def-2627">0</span><span class="sxs-lookup"><span data-stu-id="36def-2627">0</span></span><br/>

<span data-ttu-id="36def-2628">1</span><span class="sxs-lookup"><span data-stu-id="36def-2628">1</span></span>

<span data-ttu-id="36def-2629">2</span><span class="sxs-lookup"><span data-stu-id="36def-2629">2</span></span>

<span data-ttu-id="36def-2630">3</span><span class="sxs-lookup"><span data-stu-id="36def-2630">3</span></span>

<span data-ttu-id="36def-2631">4</span><span class="sxs-lookup"><span data-stu-id="36def-2631">4</span></span>

<span data-ttu-id="36def-2632">5</span><span class="sxs-lookup"><span data-stu-id="36def-2632">5</span></span>

<span data-ttu-id="36def-2633">6</span><span class="sxs-lookup"><span data-stu-id="36def-2633">6</span></span>

<span data-ttu-id="36def-2634">7</span><span class="sxs-lookup"><span data-stu-id="36def-2634">7</span></span>

<span data-ttu-id="36def-2635">8</span><span class="sxs-lookup"><span data-stu-id="36def-2635">8</span></span>

<span data-ttu-id="36def-2636">9</span><span class="sxs-lookup"><span data-stu-id="36def-2636">9</span></span>

<span data-ttu-id="36def-2637">3</span><span class="sxs-lookup"><span data-stu-id="36def-2637">3</span></span><br/> <span data-ttu-id="36def-2638">0</span><span class="sxs-lookup"><span data-stu-id="36def-2638">0</span></span><br/>

<span data-ttu-id="36def-2639">1</span><span class="sxs-lookup"><span data-stu-id="36def-2639">1</span></span>

<span data-ttu-id="36def-2640">\_msg</span><span class="sxs-lookup"><span data-stu-id="36def-2640">\_msg</span></span>

<span data-ttu-id="36def-2641">\_地位</span><span class="sxs-lookup"><span data-stu-id="36def-2641">\_status</span></span>

<span data-ttu-id="36def-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="36def-2642">\_ulChecksum</span></span>

<span data-ttu-id="36def-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="36def-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="36def-2644">\_**msg**：識別標頭後面之訊息類型的32位整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="36def-2645">下表列出內容索引服務的通訊協定訊息，以及為每個訊息指定的整數值。</span><span class="sxs-lookup"><span data-stu-id="36def-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="36def-2646">如下表所示，某些值會識別資料表中的2個訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="36def-2647">在這些情況下，可透過訊息流程的方向識別標頭後面的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="36def-2648">如果方向是 [用戶端至伺服器]，則會指出訊息名稱後面附加有 "In" 的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="36def-2649">如果方向為 [伺服器至用戶端]，則會指出訊息名稱後面附加有 "Out" 的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="36def-2650">值</span><span class="sxs-lookup"><span data-stu-id="36def-2650">Value</span></span>      | <span data-ttu-id="36def-2651">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="36def-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="36def-2652">0x000000C8</span></span> | <span data-ttu-id="36def-2653">CPMConnectIn 或 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="36def-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="36def-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="36def-2654">0x000000C9</span></span> | <span data-ttu-id="36def-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="36def-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="36def-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="36def-2656">0x000000CA</span></span> | <span data-ttu-id="36def-2657">CPMCreateQueryIn 或 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="36def-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="36def-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="36def-2658">0x000000CB</span></span> | <span data-ttu-id="36def-2659">CPMFreeCursorIn 或 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="36def-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="36def-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="36def-2660">0x000000CC</span></span> | <span data-ttu-id="36def-2661">CPMGetRowsIn 或 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="36def-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="36def-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="36def-2662">0x000000CD</span></span> | <span data-ttu-id="36def-2663">CPMRatioFinishedIn 或 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="36def-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="36def-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="36def-2664">0x000000CE</span></span> | <span data-ttu-id="36def-2665">CPMCompareBmkIn 或 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="36def-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="36def-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="36def-2666">0x000000CF</span></span> | <span data-ttu-id="36def-2667">CPMGetApproximatePositionIn 或 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="36def-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="36def-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="36def-2668">0x000000D0</span></span> | <span data-ttu-id="36def-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="36def-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="36def-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="36def-2670">0x000000D1</span></span> | <span data-ttu-id="36def-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="36def-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="36def-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="36def-2672">0x000000D2</span></span> | <span data-ttu-id="36def-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="36def-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="36def-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="36def-2674">0x000000D7</span></span> | <span data-ttu-id="36def-2675">CPMGetQueryStatusIn 或 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="36def-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="36def-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="36def-2676">0x000000D9</span></span> | <span data-ttu-id="36def-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="36def-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="36def-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="36def-2678">0x000000E1</span></span> | <span data-ttu-id="36def-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="36def-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="36def-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="36def-2680">0x000000E4</span></span> | <span data-ttu-id="36def-2681">CPMFetchValueIn 或 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="36def-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="36def-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="36def-2682">0x000000E6</span></span> | <span data-ttu-id="36def-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="36def-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="36def-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="36def-2684">0x000000E7</span></span> | <span data-ttu-id="36def-2685">CPMGetQueryStatusExIn 或 PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="36def-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="36def-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="36def-2686">0x000000E8</span></span> | <span data-ttu-id="36def-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="36def-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="36def-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="36def-2688">0x000000E9</span></span> | <span data-ttu-id="36def-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="36def-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="36def-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="36def-2690">0x000000EC</span></span> | <span data-ttu-id="36def-2691">CPMSetCatStateIn 或 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="36def-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="36def-2692">\_**狀態**： HRESULT \[ ms-chap \] ，指出要求之作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="36def-2693">*Windows 行為：用戶端一律將 \_ status 欄位設定為0x00000000。*</span><span class="sxs-lookup"><span data-stu-id="36def-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="36def-2694">**\_ ulChecksum**： \_ ULCHECKSUM 的計算方式必須如下列訊息的區段3.2.4 所指定：</span><span class="sxs-lookup"><span data-stu-id="36def-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="36def-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="36def-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="36def-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="36def-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="36def-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="36def-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="36def-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="36def-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="36def-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="36def-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="36def-2700">若為所有其他訊息， \_ ULCHECKSUM 必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="36def-2701">用戶端必須忽略 \_ ulChecksum 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="36def-2702">**\_ ulReserved2**：必須設定為0，而且接收者會忽略它。</span><span class="sxs-lookup"><span data-stu-id="36def-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="36def-2703">2.2.3 訊息</span><span class="sxs-lookup"><span data-stu-id="36def-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="36def-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="36def-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="36def-2705">CPMCiStateInOut 訊息包含索引服務狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="36def-2706">標頭後面的 CPMCiStateInOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="36def-2707">0</span><span class="sxs-lookup"><span data-stu-id="36def-2707">0</span></span>

<span data-ttu-id="36def-2708">1</span><span class="sxs-lookup"><span data-stu-id="36def-2708">1</span></span>

<span data-ttu-id="36def-2709">2</span><span class="sxs-lookup"><span data-stu-id="36def-2709">2</span></span>

<span data-ttu-id="36def-2710">3</span><span class="sxs-lookup"><span data-stu-id="36def-2710">3</span></span>

<span data-ttu-id="36def-2711">4</span><span class="sxs-lookup"><span data-stu-id="36def-2711">4</span></span>

<span data-ttu-id="36def-2712">5</span><span class="sxs-lookup"><span data-stu-id="36def-2712">5</span></span>

<span data-ttu-id="36def-2713">6</span><span class="sxs-lookup"><span data-stu-id="36def-2713">6</span></span>

<span data-ttu-id="36def-2714">7</span><span class="sxs-lookup"><span data-stu-id="36def-2714">7</span></span>

<span data-ttu-id="36def-2715">8</span><span class="sxs-lookup"><span data-stu-id="36def-2715">8</span></span>

<span data-ttu-id="36def-2716">9</span><span class="sxs-lookup"><span data-stu-id="36def-2716">9</span></span>

<span data-ttu-id="36def-2717">1</span><span class="sxs-lookup"><span data-stu-id="36def-2717">1</span></span><br/> <span data-ttu-id="36def-2718">0</span><span class="sxs-lookup"><span data-stu-id="36def-2718">0</span></span><br/>

<span data-ttu-id="36def-2719">1</span><span class="sxs-lookup"><span data-stu-id="36def-2719">1</span></span>

<span data-ttu-id="36def-2720">2</span><span class="sxs-lookup"><span data-stu-id="36def-2720">2</span></span>

<span data-ttu-id="36def-2721">3</span><span class="sxs-lookup"><span data-stu-id="36def-2721">3</span></span>

<span data-ttu-id="36def-2722">4</span><span class="sxs-lookup"><span data-stu-id="36def-2722">4</span></span>

<span data-ttu-id="36def-2723">5</span><span class="sxs-lookup"><span data-stu-id="36def-2723">5</span></span>

<span data-ttu-id="36def-2724">6</span><span class="sxs-lookup"><span data-stu-id="36def-2724">6</span></span>

<span data-ttu-id="36def-2725">7</span><span class="sxs-lookup"><span data-stu-id="36def-2725">7</span></span>

<span data-ttu-id="36def-2726">8</span><span class="sxs-lookup"><span data-stu-id="36def-2726">8</span></span>

<span data-ttu-id="36def-2727">9</span><span class="sxs-lookup"><span data-stu-id="36def-2727">9</span></span>

<span data-ttu-id="36def-2728">2</span><span class="sxs-lookup"><span data-stu-id="36def-2728">2</span></span><br/> <span data-ttu-id="36def-2729">0</span><span class="sxs-lookup"><span data-stu-id="36def-2729">0</span></span><br/>

<span data-ttu-id="36def-2730">1</span><span class="sxs-lookup"><span data-stu-id="36def-2730">1</span></span>

<span data-ttu-id="36def-2731">2</span><span class="sxs-lookup"><span data-stu-id="36def-2731">2</span></span>

<span data-ttu-id="36def-2732">3</span><span class="sxs-lookup"><span data-stu-id="36def-2732">3</span></span>

<span data-ttu-id="36def-2733">4</span><span class="sxs-lookup"><span data-stu-id="36def-2733">4</span></span>

<span data-ttu-id="36def-2734">5</span><span class="sxs-lookup"><span data-stu-id="36def-2734">5</span></span>

<span data-ttu-id="36def-2735">6</span><span class="sxs-lookup"><span data-stu-id="36def-2735">6</span></span>

<span data-ttu-id="36def-2736">7</span><span class="sxs-lookup"><span data-stu-id="36def-2736">7</span></span>

<span data-ttu-id="36def-2737">8</span><span class="sxs-lookup"><span data-stu-id="36def-2737">8</span></span>

<span data-ttu-id="36def-2738">9</span><span class="sxs-lookup"><span data-stu-id="36def-2738">9</span></span>

<span data-ttu-id="36def-2739">3</span><span class="sxs-lookup"><span data-stu-id="36def-2739">3</span></span><br/> <span data-ttu-id="36def-2740">0</span><span class="sxs-lookup"><span data-stu-id="36def-2740">0</span></span><br/>

<span data-ttu-id="36def-2741">1</span><span class="sxs-lookup"><span data-stu-id="36def-2741">1</span></span>

<span data-ttu-id="36def-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="36def-2742">cbStruct</span></span>

<span data-ttu-id="36def-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="36def-2743">cWordList</span></span>

<span data-ttu-id="36def-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="36def-2744">cPersistentIndex</span></span>

<span data-ttu-id="36def-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="36def-2745">cQueries</span></span>

<span data-ttu-id="36def-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="36def-2746">cDocuments</span></span>

<span data-ttu-id="36def-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="36def-2747">cFreshTest</span></span>

<span data-ttu-id="36def-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="36def-2748">dwMergeProgress</span></span>

<span data-ttu-id="36def-2749">eState</span><span class="sxs-lookup"><span data-stu-id="36def-2749">eState</span></span>

<span data-ttu-id="36def-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="36def-2750">cFilteredDocuments</span></span>

<span data-ttu-id="36def-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="36def-2751">cTotalDocuments</span></span>

<span data-ttu-id="36def-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="36def-2752">cPendingScans</span></span>

<span data-ttu-id="36def-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="36def-2753">dwIndexSize</span></span>

<span data-ttu-id="36def-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="36def-2754">cUniqueKeys</span></span>

<span data-ttu-id="36def-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="36def-2755">cSecQDocuments</span></span>

<span data-ttu-id="36def-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="36def-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="36def-2757">**cbStruct**：32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="36def-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="36def-2758">此訊息的大小（以位元組為單位） (不包括通用標頭) 。</span><span class="sxs-lookup"><span data-stu-id="36def-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="36def-2759">必須設為0x0000003C。</span><span class="sxs-lookup"><span data-stu-id="36def-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="36def-2760">**cWordList**：32位不帶正負號的整數，表示為最近編制索引的檔所建立的初始索引計數。</span><span class="sxs-lookup"><span data-stu-id="36def-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="36def-2761">**cPersistentIndex**：32位不帶正負號的整數，表示持續性索引的計數。</span><span class="sxs-lookup"><span data-stu-id="36def-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="36def-2762">**cQueries**：32位不帶正負號的整數，表示正在執行的查詢數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="36def-2763">**cDocuments**：32位不帶正負號的整數，指出等候編制索引的檔總數。</span><span class="sxs-lookup"><span data-stu-id="36def-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="36def-2764">**cFreshTest**：32位不帶正負號的整數，指出未針對效能進行完整優化的唯一檔數目，以及索引中的資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="36def-2765">**dwMergeProgress**：不帶正負號的32位整數，指定目前的索引完整優化的完成百分比（如果目前正在進行優化）。</span><span class="sxs-lookup"><span data-stu-id="36def-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="36def-2766">必須小於或等於100。</span><span class="sxs-lookup"><span data-stu-id="36def-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="36def-2767">**資產**：依 \_ \_ \* 下表所定義的一或多個 CI 狀態常數所提供的內容編制索引狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="36def-2768">值</span><span class="sxs-lookup"><span data-stu-id="36def-2768">Value</span></span>                                         | <span data-ttu-id="36def-2769">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-2770">CI \_ 狀態 \_ 陰影 \_ 合併0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="36def-2771">索引服務正在優化某些索引，以降低記憶體使用量並提升查詢效能。</span><span class="sxs-lookup"><span data-stu-id="36def-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="36def-2772">CI \_ 狀態 \_ 主要 \_ 合併0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="36def-2773">索引服務正在進行所有索引的完整優化處理。</span><span class="sxs-lookup"><span data-stu-id="36def-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="36def-2774">CI \_ 狀態 \_ 內容 \_ 掃描 \_ 所需的0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="36def-2775">索引中的某些檔已變更，而索引服務需要判斷已新增、變更或刪除的檔。</span><span class="sxs-lookup"><span data-stu-id="36def-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="36def-2776">CI \_ 狀態 \_ 鍛煉 \_ 合併0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="36def-2777">索引服務正在將索引優化，以降低記憶體使用量並提升查詢效能。</span><span class="sxs-lookup"><span data-stu-id="36def-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="36def-2778">此程式比 CI 狀態陰影合併值所識別的程式更完整 \_ \_ \_ ，但不像 ci \_ 狀態 \_ 主要合併值所指定的完整 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="36def-2779">這類優化是實作為特定的，因為它們相依于內部儲存資料的方式;優化不會以回應時間以外的任何方式影響通訊協定。</span><span class="sxs-lookup"><span data-stu-id="36def-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="36def-2780">CI \_ 狀態 \_ 掃描0x00000010</span><span class="sxs-lookup"><span data-stu-id="36def-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="36def-2781">索引服務正在檢查目錄或一組目錄，以查看自上次索引目錄之後，是否已新增、刪除或更新任何檔案。</span><span class="sxs-lookup"><span data-stu-id="36def-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="36def-2782">CI \_ 狀態 \_ 復原0x00000020</span><span class="sxs-lookup"><span data-stu-id="36def-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="36def-2783">服務從上次儲存的狀態開始，而且正在復原。</span><span class="sxs-lookup"><span data-stu-id="36def-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="36def-2784">CI \_ 狀態 \_ 低 \_ 記憶體0x00000080</span><span class="sxs-lookup"><span data-stu-id="36def-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="36def-2785">伺服器的大部分虛擬記憶體正在使用中。</span><span class="sxs-lookup"><span data-stu-id="36def-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="36def-2786">CI \_ 狀態 \_ 高 \_ IO 0x00000100</span><span class="sxs-lookup"><span data-stu-id="36def-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="36def-2787">伺服器上的輸入/輸出 (i/o) 活動的層級相對較高。</span><span class="sxs-lookup"><span data-stu-id="36def-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="36def-2788">CI \_ 狀態 \_ 主要 \_ 合併已 \_ 暫停0x00000200</span><span class="sxs-lookup"><span data-stu-id="36def-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="36def-2789">所有進行中之索引的完整優化程式都已暫停。</span><span class="sxs-lookup"><span data-stu-id="36def-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="36def-2790">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="36def-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="36def-2791">CI \_ 狀態 \_ 唯讀 \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="36def-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="36def-2792">將新檔挑選至索引的索引服務部分已暫停。</span><span class="sxs-lookup"><span data-stu-id="36def-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="36def-2793">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="36def-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="36def-2794">CI \_ 狀態 \_ 電池 \_ 電力0x00000800</span><span class="sxs-lookup"><span data-stu-id="36def-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="36def-2795">將新檔挑選至索引的索引服務部分已暫停，以節省電池存留期，但仍會回復查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="36def-2796">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="36def-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="36def-2797">CI \_ 狀態 \_ 使用者使用中 \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="36def-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="36def-2798">將新檔挑選至索引的索引服務部分，因為使用者 (鍵盤或滑鼠) 的高度活動，但仍在回復查詢，所以已暫停。</span><span class="sxs-lookup"><span data-stu-id="36def-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="36def-2799">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="36def-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="36def-2800">CI \_ 狀態 \_ 開始0x00002000</span><span class="sxs-lookup"><span data-stu-id="36def-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="36def-2801">服務正在啟動。</span><span class="sxs-lookup"><span data-stu-id="36def-2801">The service is starting.</span></span> <span data-ttu-id="36def-2802">您可以執行查詢，但尚未啟用掃描和通知。</span><span class="sxs-lookup"><span data-stu-id="36def-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="36def-2803">這僅供提供資訊之用，並不會影響 CISP。</span><span class="sxs-lookup"><span data-stu-id="36def-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="36def-2804">\_ \_ 讀取 \_ USN 0x00004000 的 CI 狀態</span><span class="sxs-lookup"><span data-stu-id="36def-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="36def-2805">服務未讀取檔案系統所保留的記錄檔，以追蹤磁片區中檔案或目錄的變更，因此索引可能不是最新狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="36def-2806">**cFilteredDocuments**：32位不帶正負號整數，指出自開始編制內容索引之後編制索引的檔數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="36def-2807">**cTotalDocuments**：32位不帶正負號的整數，表示系統中的檔總數。</span><span class="sxs-lookup"><span data-stu-id="36def-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="36def-2808">**cPendingScans**：32位不帶正負號的整數，表示暫止高階索引編制作業的數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="36def-2809">此值的意義是提供者專屬的，但預期會有較大的數位，以表示保留更多索引。</span><span class="sxs-lookup"><span data-stu-id="36def-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="36def-2810">*Windows 行為*：此值通常是零，但在開始編制索引之後，或在通知佇列溢出之後立即發生。</span><span class="sxs-lookup"><span data-stu-id="36def-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="36def-2811">**dwIndexSize**：32位不帶正負號的整數，表示索引的大小（以 mb 為單位） (不包括屬性快取) 。</span><span class="sxs-lookup"><span data-stu-id="36def-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="36def-2812">**cUniqueKeys**：32位不帶正負號的整數，表示目錄中唯一索引鍵的大約數目。</span><span class="sxs-lookup"><span data-stu-id="36def-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="36def-2813">**cSecQDocuments**：32位不帶正負號的整數，指出索引服務將重新嘗試編制索引的檔數目，因為初始索引嘗試期間發生失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="36def-2814">**dwPropCacheSize**：32位不帶正負號的整數，表示屬性快取的大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="36def-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="36def-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="36def-2816">CPMSetCatStateIn 訊息會設定目錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="36def-2817">標頭後面的 CPMSetCatStateIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="36def-2818">0</span><span class="sxs-lookup"><span data-stu-id="36def-2818">0</span></span>

<span data-ttu-id="36def-2819">1</span><span class="sxs-lookup"><span data-stu-id="36def-2819">1</span></span>

<span data-ttu-id="36def-2820">2</span><span class="sxs-lookup"><span data-stu-id="36def-2820">2</span></span>

<span data-ttu-id="36def-2821">3</span><span class="sxs-lookup"><span data-stu-id="36def-2821">3</span></span>

<span data-ttu-id="36def-2822">4</span><span class="sxs-lookup"><span data-stu-id="36def-2822">4</span></span>

<span data-ttu-id="36def-2823">5</span><span class="sxs-lookup"><span data-stu-id="36def-2823">5</span></span>

<span data-ttu-id="36def-2824">6</span><span class="sxs-lookup"><span data-stu-id="36def-2824">6</span></span>

<span data-ttu-id="36def-2825">7</span><span class="sxs-lookup"><span data-stu-id="36def-2825">7</span></span>

<span data-ttu-id="36def-2826">8</span><span class="sxs-lookup"><span data-stu-id="36def-2826">8</span></span>

<span data-ttu-id="36def-2827">9</span><span class="sxs-lookup"><span data-stu-id="36def-2827">9</span></span>

<span data-ttu-id="36def-2828">1</span><span class="sxs-lookup"><span data-stu-id="36def-2828">1</span></span><br/> <span data-ttu-id="36def-2829">0</span><span class="sxs-lookup"><span data-stu-id="36def-2829">0</span></span><br/>

<span data-ttu-id="36def-2830">1</span><span class="sxs-lookup"><span data-stu-id="36def-2830">1</span></span>

<span data-ttu-id="36def-2831">2</span><span class="sxs-lookup"><span data-stu-id="36def-2831">2</span></span>

<span data-ttu-id="36def-2832">3</span><span class="sxs-lookup"><span data-stu-id="36def-2832">3</span></span>

<span data-ttu-id="36def-2833">4</span><span class="sxs-lookup"><span data-stu-id="36def-2833">4</span></span>

<span data-ttu-id="36def-2834">5</span><span class="sxs-lookup"><span data-stu-id="36def-2834">5</span></span>

<span data-ttu-id="36def-2835">6</span><span class="sxs-lookup"><span data-stu-id="36def-2835">6</span></span>

<span data-ttu-id="36def-2836">7</span><span class="sxs-lookup"><span data-stu-id="36def-2836">7</span></span>

<span data-ttu-id="36def-2837">8</span><span class="sxs-lookup"><span data-stu-id="36def-2837">8</span></span>

<span data-ttu-id="36def-2838">9</span><span class="sxs-lookup"><span data-stu-id="36def-2838">9</span></span>

<span data-ttu-id="36def-2839">2</span><span class="sxs-lookup"><span data-stu-id="36def-2839">2</span></span><br/> <span data-ttu-id="36def-2840">0</span><span class="sxs-lookup"><span data-stu-id="36def-2840">0</span></span><br/>

<span data-ttu-id="36def-2841">1</span><span class="sxs-lookup"><span data-stu-id="36def-2841">1</span></span>

<span data-ttu-id="36def-2842">2</span><span class="sxs-lookup"><span data-stu-id="36def-2842">2</span></span>

<span data-ttu-id="36def-2843">3</span><span class="sxs-lookup"><span data-stu-id="36def-2843">3</span></span>

<span data-ttu-id="36def-2844">4</span><span class="sxs-lookup"><span data-stu-id="36def-2844">4</span></span>

<span data-ttu-id="36def-2845">5</span><span class="sxs-lookup"><span data-stu-id="36def-2845">5</span></span>

<span data-ttu-id="36def-2846">6</span><span class="sxs-lookup"><span data-stu-id="36def-2846">6</span></span>

<span data-ttu-id="36def-2847">7</span><span class="sxs-lookup"><span data-stu-id="36def-2847">7</span></span>

<span data-ttu-id="36def-2848">8</span><span class="sxs-lookup"><span data-stu-id="36def-2848">8</span></span>

<span data-ttu-id="36def-2849">9</span><span class="sxs-lookup"><span data-stu-id="36def-2849">9</span></span>

<span data-ttu-id="36def-2850">3</span><span class="sxs-lookup"><span data-stu-id="36def-2850">3</span></span><br/> <span data-ttu-id="36def-2851">0</span><span class="sxs-lookup"><span data-stu-id="36def-2851">0</span></span><br/>

<span data-ttu-id="36def-2852">1</span><span class="sxs-lookup"><span data-stu-id="36def-2852">1</span></span>

<span data-ttu-id="36def-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="36def-2853">\_partID</span></span>

<span data-ttu-id="36def-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="36def-2854">\_dwNewState</span></span>

<span data-ttu-id="36def-2855">\_CatName (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="36def-2856">**\_ partID**：必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="36def-2857">**\_ dwNewState**：必須設定為下列其中一個值，表示目錄的新狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="36def-2858">值</span><span class="sxs-lookup"><span data-stu-id="36def-2858">Value</span></span>                         | <span data-ttu-id="36def-2859">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-2860">CICAT \_ 停止的0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="36def-2861">目錄已停止。</span><span class="sxs-lookup"><span data-stu-id="36def-2861">The catalog is stopped.</span></span> <span data-ttu-id="36def-2862">此狀態表示不會編制任何新檔案的索引，也不會處理任何搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="36def-2863">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="36def-2864">目錄是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="36def-2864">The catalog is read-only.</span></span> <span data-ttu-id="36def-2865">不會為任何新檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="36def-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="36def-2866">CICAT \_ 可寫入的0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="36def-2867">目錄是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="36def-2867">The catalog is writable.</span></span> <span data-ttu-id="36def-2868">您可以建立新檔案的索引，並處理搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="36def-2869">CICAT \_ 沒有 \_ 查詢0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="36def-2870">目錄無法供查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="36def-2871">CICAT \_ 取得 \_ 狀態0x00000010</span><span class="sxs-lookup"><span data-stu-id="36def-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="36def-2872">目錄的狀態不會變更，只會進行取出。</span><span class="sxs-lookup"><span data-stu-id="36def-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="36def-2873">CICAT \_ 所有 \_ 開啟的0x00000020</span><span class="sxs-lookup"><span data-stu-id="36def-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="36def-2874">查看是否已啟動所有目錄的檢查。</span><span class="sxs-lookup"><span data-stu-id="36def-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="36def-2875">若是如此， \_ 在 CPMSetCatStateOut 回復中傳送給此訊息的 dwOldState 欄位將會報告為非零。</span><span class="sxs-lookup"><span data-stu-id="36def-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="36def-2876">**\_ CatName**：要修改其狀態的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="36def-2877">名稱必須是以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="36def-2878">如果 \_ dwNewState 設定為 CICAT 全部開啟，則必須省略此欄位 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="36def-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="36def-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="36def-2880">CPMSetCatStateOut 訊息是具有類別目錄舊狀態的 CPMSetCatStateIn 訊息回復。</span><span class="sxs-lookup"><span data-stu-id="36def-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="36def-2881">標頭後面的 CPMSetCatStateOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="36def-2882">0</span><span class="sxs-lookup"><span data-stu-id="36def-2882">0</span></span>

<span data-ttu-id="36def-2883">1</span><span class="sxs-lookup"><span data-stu-id="36def-2883">1</span></span>

<span data-ttu-id="36def-2884">2</span><span class="sxs-lookup"><span data-stu-id="36def-2884">2</span></span>

<span data-ttu-id="36def-2885">3</span><span class="sxs-lookup"><span data-stu-id="36def-2885">3</span></span>

<span data-ttu-id="36def-2886">4</span><span class="sxs-lookup"><span data-stu-id="36def-2886">4</span></span>

<span data-ttu-id="36def-2887">5</span><span class="sxs-lookup"><span data-stu-id="36def-2887">5</span></span>

<span data-ttu-id="36def-2888">6</span><span class="sxs-lookup"><span data-stu-id="36def-2888">6</span></span>

<span data-ttu-id="36def-2889">7</span><span class="sxs-lookup"><span data-stu-id="36def-2889">7</span></span>

<span data-ttu-id="36def-2890">8</span><span class="sxs-lookup"><span data-stu-id="36def-2890">8</span></span>

<span data-ttu-id="36def-2891">9</span><span class="sxs-lookup"><span data-stu-id="36def-2891">9</span></span>

<span data-ttu-id="36def-2892">1</span><span class="sxs-lookup"><span data-stu-id="36def-2892">1</span></span><br/> <span data-ttu-id="36def-2893">0</span><span class="sxs-lookup"><span data-stu-id="36def-2893">0</span></span><br/>

<span data-ttu-id="36def-2894">1</span><span class="sxs-lookup"><span data-stu-id="36def-2894">1</span></span>

<span data-ttu-id="36def-2895">2</span><span class="sxs-lookup"><span data-stu-id="36def-2895">2</span></span>

<span data-ttu-id="36def-2896">3</span><span class="sxs-lookup"><span data-stu-id="36def-2896">3</span></span>

<span data-ttu-id="36def-2897">4</span><span class="sxs-lookup"><span data-stu-id="36def-2897">4</span></span>

<span data-ttu-id="36def-2898">5</span><span class="sxs-lookup"><span data-stu-id="36def-2898">5</span></span>

<span data-ttu-id="36def-2899">6</span><span class="sxs-lookup"><span data-stu-id="36def-2899">6</span></span>

<span data-ttu-id="36def-2900">7</span><span class="sxs-lookup"><span data-stu-id="36def-2900">7</span></span>

<span data-ttu-id="36def-2901">8</span><span class="sxs-lookup"><span data-stu-id="36def-2901">8</span></span>

<span data-ttu-id="36def-2902">9</span><span class="sxs-lookup"><span data-stu-id="36def-2902">9</span></span>

<span data-ttu-id="36def-2903">2</span><span class="sxs-lookup"><span data-stu-id="36def-2903">2</span></span><br/> <span data-ttu-id="36def-2904">0</span><span class="sxs-lookup"><span data-stu-id="36def-2904">0</span></span><br/>

<span data-ttu-id="36def-2905">1</span><span class="sxs-lookup"><span data-stu-id="36def-2905">1</span></span>

<span data-ttu-id="36def-2906">2</span><span class="sxs-lookup"><span data-stu-id="36def-2906">2</span></span>

<span data-ttu-id="36def-2907">3</span><span class="sxs-lookup"><span data-stu-id="36def-2907">3</span></span>

<span data-ttu-id="36def-2908">4</span><span class="sxs-lookup"><span data-stu-id="36def-2908">4</span></span>

<span data-ttu-id="36def-2909">5</span><span class="sxs-lookup"><span data-stu-id="36def-2909">5</span></span>

<span data-ttu-id="36def-2910">6</span><span class="sxs-lookup"><span data-stu-id="36def-2910">6</span></span>

<span data-ttu-id="36def-2911">7</span><span class="sxs-lookup"><span data-stu-id="36def-2911">7</span></span>

<span data-ttu-id="36def-2912">8</span><span class="sxs-lookup"><span data-stu-id="36def-2912">8</span></span>

<span data-ttu-id="36def-2913">9</span><span class="sxs-lookup"><span data-stu-id="36def-2913">9</span></span>

<span data-ttu-id="36def-2914">3</span><span class="sxs-lookup"><span data-stu-id="36def-2914">3</span></span><br/> <span data-ttu-id="36def-2915">0</span><span class="sxs-lookup"><span data-stu-id="36def-2915">0</span></span><br/>

<span data-ttu-id="36def-2916">1</span><span class="sxs-lookup"><span data-stu-id="36def-2916">1</span></span>

<span data-ttu-id="36def-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="36def-2917">\_dwOldState</span></span>



 

<span data-ttu-id="36def-2918">**\_ dwOldState**：下列其中一個值，表示目錄的舊狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="36def-2919">值</span><span class="sxs-lookup"><span data-stu-id="36def-2919">Value</span></span>                       | <span data-ttu-id="36def-2920">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="36def-2921">CICAT \_ 停止的0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="36def-2922">目錄已停止。</span><span class="sxs-lookup"><span data-stu-id="36def-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="36def-2923">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="36def-2924">目錄是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="36def-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="36def-2925">CICAT \_ 可寫入的0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="36def-2926">目錄是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="36def-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="36def-2927">CICAT \_ 沒有 \_ 查詢0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="36def-2928">目錄無法供查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="36def-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="36def-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="36def-2930">CPMUpdateDocumentsIn 訊息會指示伺服器為指定的路徑編制索引。</span><span class="sxs-lookup"><span data-stu-id="36def-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="36def-2931">伺服器將會使用 CPMUpdateDocumentsOut 訊息的訊息標頭來回複，並將要求的結果包含在 \_ 訊息標頭的 [狀態] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="36def-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="36def-2932">標頭後面的 CPMUpdateDocumentsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="36def-2933">0</span><span class="sxs-lookup"><span data-stu-id="36def-2933">0</span></span>

<span data-ttu-id="36def-2934">1</span><span class="sxs-lookup"><span data-stu-id="36def-2934">1</span></span>

<span data-ttu-id="36def-2935">2</span><span class="sxs-lookup"><span data-stu-id="36def-2935">2</span></span>

<span data-ttu-id="36def-2936">3</span><span class="sxs-lookup"><span data-stu-id="36def-2936">3</span></span>

<span data-ttu-id="36def-2937">4</span><span class="sxs-lookup"><span data-stu-id="36def-2937">4</span></span>

<span data-ttu-id="36def-2938">5</span><span class="sxs-lookup"><span data-stu-id="36def-2938">5</span></span>

<span data-ttu-id="36def-2939">6</span><span class="sxs-lookup"><span data-stu-id="36def-2939">6</span></span>

<span data-ttu-id="36def-2940">7</span><span class="sxs-lookup"><span data-stu-id="36def-2940">7</span></span>

<span data-ttu-id="36def-2941">8</span><span class="sxs-lookup"><span data-stu-id="36def-2941">8</span></span>

<span data-ttu-id="36def-2942">9</span><span class="sxs-lookup"><span data-stu-id="36def-2942">9</span></span>

<span data-ttu-id="36def-2943">1</span><span class="sxs-lookup"><span data-stu-id="36def-2943">1</span></span><br/> <span data-ttu-id="36def-2944">0</span><span class="sxs-lookup"><span data-stu-id="36def-2944">0</span></span><br/>

<span data-ttu-id="36def-2945">1</span><span class="sxs-lookup"><span data-stu-id="36def-2945">1</span></span>

<span data-ttu-id="36def-2946">2</span><span class="sxs-lookup"><span data-stu-id="36def-2946">2</span></span>

<span data-ttu-id="36def-2947">3</span><span class="sxs-lookup"><span data-stu-id="36def-2947">3</span></span>

<span data-ttu-id="36def-2948">4</span><span class="sxs-lookup"><span data-stu-id="36def-2948">4</span></span>

<span data-ttu-id="36def-2949">5</span><span class="sxs-lookup"><span data-stu-id="36def-2949">5</span></span>

<span data-ttu-id="36def-2950">6</span><span class="sxs-lookup"><span data-stu-id="36def-2950">6</span></span>

<span data-ttu-id="36def-2951">7</span><span class="sxs-lookup"><span data-stu-id="36def-2951">7</span></span>

<span data-ttu-id="36def-2952">8</span><span class="sxs-lookup"><span data-stu-id="36def-2952">8</span></span>

<span data-ttu-id="36def-2953">9</span><span class="sxs-lookup"><span data-stu-id="36def-2953">9</span></span>

<span data-ttu-id="36def-2954">2</span><span class="sxs-lookup"><span data-stu-id="36def-2954">2</span></span><br/> <span data-ttu-id="36def-2955">0</span><span class="sxs-lookup"><span data-stu-id="36def-2955">0</span></span><br/>

<span data-ttu-id="36def-2956">1</span><span class="sxs-lookup"><span data-stu-id="36def-2956">1</span></span>

<span data-ttu-id="36def-2957">2</span><span class="sxs-lookup"><span data-stu-id="36def-2957">2</span></span>

<span data-ttu-id="36def-2958">3</span><span class="sxs-lookup"><span data-stu-id="36def-2958">3</span></span>

<span data-ttu-id="36def-2959">4</span><span class="sxs-lookup"><span data-stu-id="36def-2959">4</span></span>

<span data-ttu-id="36def-2960">5</span><span class="sxs-lookup"><span data-stu-id="36def-2960">5</span></span>

<span data-ttu-id="36def-2961">6</span><span class="sxs-lookup"><span data-stu-id="36def-2961">6</span></span>

<span data-ttu-id="36def-2962">7</span><span class="sxs-lookup"><span data-stu-id="36def-2962">7</span></span>

<span data-ttu-id="36def-2963">8</span><span class="sxs-lookup"><span data-stu-id="36def-2963">8</span></span>

<span data-ttu-id="36def-2964">9</span><span class="sxs-lookup"><span data-stu-id="36def-2964">9</span></span>

<span data-ttu-id="36def-2965">3</span><span class="sxs-lookup"><span data-stu-id="36def-2965">3</span></span><br/> <span data-ttu-id="36def-2966">0</span><span class="sxs-lookup"><span data-stu-id="36def-2966">0</span></span><br/>

<span data-ttu-id="36def-2967">1</span><span class="sxs-lookup"><span data-stu-id="36def-2967">1</span></span>

<span data-ttu-id="36def-2968">\_ (選擇性的旗標) </span><span class="sxs-lookup"><span data-stu-id="36def-2968">\_flag (optional)</span></span>

<span data-ttu-id="36def-2969">\_fRootPath (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="36def-2970">RootPath (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="36def-2971">**\_ 旗** 標：要執行的更新類型。</span><span class="sxs-lookup"><span data-stu-id="36def-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="36def-2972">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="36def-2973">此欄位必須設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="36def-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="36def-2974">值</span><span class="sxs-lookup"><span data-stu-id="36def-2974">Value</span></span>                  | <span data-ttu-id="36def-2975">意義</span><span class="sxs-lookup"><span data-stu-id="36def-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36def-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="36def-2977">要執行累加式更新。</span><span class="sxs-lookup"><span data-stu-id="36def-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="36def-2978">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="36def-2979">要執行完整更新。</span><span class="sxs-lookup"><span data-stu-id="36def-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="36def-2980">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="36def-2981">要執行新的初始化。</span><span class="sxs-lookup"><span data-stu-id="36def-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="36def-2982">**\_ fRootPath**：布林值，指出 RootPath 欄位是否指定要執行更新的路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="36def-2983">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="36def-2984">此欄位必須設定為0x00000001 或0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="36def-2985">如果設定為0x00000001，則 RootPath 中會包含要執行更新的路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="36def-2986">如果設定為0x00000000，則會在所有已編制索引的路徑上執行更新。</span><span class="sxs-lookup"><span data-stu-id="36def-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="36def-2987">**RootPath**：要更新的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="36def-2988">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="36def-2989">名稱必須是以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="36def-2990">如果 fRootPath 設定為0x00000000，則必須省略此欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="36def-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="36def-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="36def-2992">CPMForceMergeIn 訊息要求伺服器執行任何必要的維護，以改善查詢效能。</span><span class="sxs-lookup"><span data-stu-id="36def-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="36def-2993">伺服器將會使用 CPMForceMergeIn 訊息的訊息標頭來回複，並在 [狀態] 欄位中包含要求的結果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="36def-2994">標頭後面的 CPMForceMergeIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="36def-2995">0</span><span class="sxs-lookup"><span data-stu-id="36def-2995">0</span></span>

<span data-ttu-id="36def-2996">1</span><span class="sxs-lookup"><span data-stu-id="36def-2996">1</span></span>

<span data-ttu-id="36def-2997">2</span><span class="sxs-lookup"><span data-stu-id="36def-2997">2</span></span>

<span data-ttu-id="36def-2998">3</span><span class="sxs-lookup"><span data-stu-id="36def-2998">3</span></span>

<span data-ttu-id="36def-2999">4</span><span class="sxs-lookup"><span data-stu-id="36def-2999">4</span></span>

<span data-ttu-id="36def-3000">5</span><span class="sxs-lookup"><span data-stu-id="36def-3000">5</span></span>

<span data-ttu-id="36def-3001">6</span><span class="sxs-lookup"><span data-stu-id="36def-3001">6</span></span>

<span data-ttu-id="36def-3002">7</span><span class="sxs-lookup"><span data-stu-id="36def-3002">7</span></span>

<span data-ttu-id="36def-3003">8</span><span class="sxs-lookup"><span data-stu-id="36def-3003">8</span></span>

<span data-ttu-id="36def-3004">9</span><span class="sxs-lookup"><span data-stu-id="36def-3004">9</span></span>

<span data-ttu-id="36def-3005">1</span><span class="sxs-lookup"><span data-stu-id="36def-3005">1</span></span><br/> <span data-ttu-id="36def-3006">0</span><span class="sxs-lookup"><span data-stu-id="36def-3006">0</span></span><br/>

<span data-ttu-id="36def-3007">1</span><span class="sxs-lookup"><span data-stu-id="36def-3007">1</span></span>

<span data-ttu-id="36def-3008">2</span><span class="sxs-lookup"><span data-stu-id="36def-3008">2</span></span>

<span data-ttu-id="36def-3009">3</span><span class="sxs-lookup"><span data-stu-id="36def-3009">3</span></span>

<span data-ttu-id="36def-3010">4</span><span class="sxs-lookup"><span data-stu-id="36def-3010">4</span></span>

<span data-ttu-id="36def-3011">5</span><span class="sxs-lookup"><span data-stu-id="36def-3011">5</span></span>

<span data-ttu-id="36def-3012">6</span><span class="sxs-lookup"><span data-stu-id="36def-3012">6</span></span>

<span data-ttu-id="36def-3013">7</span><span class="sxs-lookup"><span data-stu-id="36def-3013">7</span></span>

<span data-ttu-id="36def-3014">8</span><span class="sxs-lookup"><span data-stu-id="36def-3014">8</span></span>

<span data-ttu-id="36def-3015">9</span><span class="sxs-lookup"><span data-stu-id="36def-3015">9</span></span>

<span data-ttu-id="36def-3016">2</span><span class="sxs-lookup"><span data-stu-id="36def-3016">2</span></span><br/> <span data-ttu-id="36def-3017">0</span><span class="sxs-lookup"><span data-stu-id="36def-3017">0</span></span><br/>

<span data-ttu-id="36def-3018">1</span><span class="sxs-lookup"><span data-stu-id="36def-3018">1</span></span>

<span data-ttu-id="36def-3019">2</span><span class="sxs-lookup"><span data-stu-id="36def-3019">2</span></span>

<span data-ttu-id="36def-3020">3</span><span class="sxs-lookup"><span data-stu-id="36def-3020">3</span></span>

<span data-ttu-id="36def-3021">4</span><span class="sxs-lookup"><span data-stu-id="36def-3021">4</span></span>

<span data-ttu-id="36def-3022">5</span><span class="sxs-lookup"><span data-stu-id="36def-3022">5</span></span>

<span data-ttu-id="36def-3023">6</span><span class="sxs-lookup"><span data-stu-id="36def-3023">6</span></span>

<span data-ttu-id="36def-3024">7</span><span class="sxs-lookup"><span data-stu-id="36def-3024">7</span></span>

<span data-ttu-id="36def-3025">8</span><span class="sxs-lookup"><span data-stu-id="36def-3025">8</span></span>

<span data-ttu-id="36def-3026">9</span><span class="sxs-lookup"><span data-stu-id="36def-3026">9</span></span>

<span data-ttu-id="36def-3027">3</span><span class="sxs-lookup"><span data-stu-id="36def-3027">3</span></span><br/> <span data-ttu-id="36def-3028">0</span><span class="sxs-lookup"><span data-stu-id="36def-3028">0</span></span><br/>

<span data-ttu-id="36def-3029">1</span><span class="sxs-lookup"><span data-stu-id="36def-3029">1</span></span>

<span data-ttu-id="36def-3030">\_partID (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="36def-3031">**\_ partID**：當用戶端傳送訊息時，此欄位必須存在，而且當伺服器傳送訊息時必須不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="36def-3032">當這個欄位存在時，必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="36def-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="36def-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="36def-3034">CPMConnectIn 訊息會開始用戶端與伺服器之間的會話。</span><span class="sxs-lookup"><span data-stu-id="36def-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="36def-3035">標頭後面的 CPMConnectIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3036">0</span><span class="sxs-lookup"><span data-stu-id="36def-3036">0</span></span>

<span data-ttu-id="36def-3037">1</span><span class="sxs-lookup"><span data-stu-id="36def-3037">1</span></span>

<span data-ttu-id="36def-3038">2</span><span class="sxs-lookup"><span data-stu-id="36def-3038">2</span></span>

<span data-ttu-id="36def-3039">3</span><span class="sxs-lookup"><span data-stu-id="36def-3039">3</span></span>

<span data-ttu-id="36def-3040">4</span><span class="sxs-lookup"><span data-stu-id="36def-3040">4</span></span>

<span data-ttu-id="36def-3041">5</span><span class="sxs-lookup"><span data-stu-id="36def-3041">5</span></span>

<span data-ttu-id="36def-3042">6</span><span class="sxs-lookup"><span data-stu-id="36def-3042">6</span></span>

<span data-ttu-id="36def-3043">7</span><span class="sxs-lookup"><span data-stu-id="36def-3043">7</span></span>

<span data-ttu-id="36def-3044">8</span><span class="sxs-lookup"><span data-stu-id="36def-3044">8</span></span>

<span data-ttu-id="36def-3045">9</span><span class="sxs-lookup"><span data-stu-id="36def-3045">9</span></span>

<span data-ttu-id="36def-3046">1</span><span class="sxs-lookup"><span data-stu-id="36def-3046">1</span></span><br/> <span data-ttu-id="36def-3047">0</span><span class="sxs-lookup"><span data-stu-id="36def-3047">0</span></span><br/>

<span data-ttu-id="36def-3048">1</span><span class="sxs-lookup"><span data-stu-id="36def-3048">1</span></span>

<span data-ttu-id="36def-3049">2</span><span class="sxs-lookup"><span data-stu-id="36def-3049">2</span></span>

<span data-ttu-id="36def-3050">3</span><span class="sxs-lookup"><span data-stu-id="36def-3050">3</span></span>

<span data-ttu-id="36def-3051">4</span><span class="sxs-lookup"><span data-stu-id="36def-3051">4</span></span>

<span data-ttu-id="36def-3052">5</span><span class="sxs-lookup"><span data-stu-id="36def-3052">5</span></span>

<span data-ttu-id="36def-3053">6</span><span class="sxs-lookup"><span data-stu-id="36def-3053">6</span></span>

<span data-ttu-id="36def-3054">7</span><span class="sxs-lookup"><span data-stu-id="36def-3054">7</span></span>

<span data-ttu-id="36def-3055">8</span><span class="sxs-lookup"><span data-stu-id="36def-3055">8</span></span>

<span data-ttu-id="36def-3056">9</span><span class="sxs-lookup"><span data-stu-id="36def-3056">9</span></span>

<span data-ttu-id="36def-3057">2</span><span class="sxs-lookup"><span data-stu-id="36def-3057">2</span></span><br/> <span data-ttu-id="36def-3058">0</span><span class="sxs-lookup"><span data-stu-id="36def-3058">0</span></span><br/>

<span data-ttu-id="36def-3059">1</span><span class="sxs-lookup"><span data-stu-id="36def-3059">1</span></span>

<span data-ttu-id="36def-3060">2</span><span class="sxs-lookup"><span data-stu-id="36def-3060">2</span></span>

<span data-ttu-id="36def-3061">3</span><span class="sxs-lookup"><span data-stu-id="36def-3061">3</span></span>

<span data-ttu-id="36def-3062">4</span><span class="sxs-lookup"><span data-stu-id="36def-3062">4</span></span>

<span data-ttu-id="36def-3063">5</span><span class="sxs-lookup"><span data-stu-id="36def-3063">5</span></span>

<span data-ttu-id="36def-3064">6</span><span class="sxs-lookup"><span data-stu-id="36def-3064">6</span></span>

<span data-ttu-id="36def-3065">7</span><span class="sxs-lookup"><span data-stu-id="36def-3065">7</span></span>

<span data-ttu-id="36def-3066">8</span><span class="sxs-lookup"><span data-stu-id="36def-3066">8</span></span>

<span data-ttu-id="36def-3067">9</span><span class="sxs-lookup"><span data-stu-id="36def-3067">9</span></span>

<span data-ttu-id="36def-3068">3</span><span class="sxs-lookup"><span data-stu-id="36def-3068">3</span></span><br/> <span data-ttu-id="36def-3069">0</span><span class="sxs-lookup"><span data-stu-id="36def-3069">0</span></span><br/>

<span data-ttu-id="36def-3070">1</span><span class="sxs-lookup"><span data-stu-id="36def-3070">1</span></span>

<span data-ttu-id="36def-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="36def-3071">\_iClientVersion</span></span>

<span data-ttu-id="36def-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="36def-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="36def-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="36def-3073">\_cbBlob1</span></span>

<span data-ttu-id="36def-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="36def-3074">\_cbBlob2</span></span>

<span data-ttu-id="36def-3075">\_填充</span><span class="sxs-lookup"><span data-stu-id="36def-3075">\_padding</span></span>

<span data-ttu-id="36def-3076">...</span><span class="sxs-lookup"><span data-stu-id="36def-3076">...</span></span>

<span data-ttu-id="36def-3077">...</span><span class="sxs-lookup"><span data-stu-id="36def-3077">...</span></span>

<span data-ttu-id="36def-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="36def-3078">MachineName</span></span>

<span data-ttu-id="36def-3079">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3079">... (variable)</span></span>

<span data-ttu-id="36def-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="36def-3080">UserName</span></span>

<span data-ttu-id="36def-3081">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3081">... (variable)</span></span>

<span data-ttu-id="36def-3082">\_paddingcPropSets (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="36def-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="36def-3083">cPropSets</span></span>

<span data-ttu-id="36def-3084">PropertySet1 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="36def-3085">PropertySet2 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="36def-3086">\_paddingExtPropset (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="36def-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="36def-3087">cExtPropSet</span></span>

<span data-ttu-id="36def-3088">aPropertySets (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="36def-3089">**\_ iClientVersion**：32位整數，指出伺服器是否要驗證訊息標頭的 ulChecksum 欄位中所指定的總和檢查碼值是否 \_ 為用戶端所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="36def-3090">如果 \_ iClientVersion 欄位設定為0x00000008 或更高，則伺服器必須驗證 \_ 下列訊息的 ulChecksum 域值：</span><span class="sxs-lookup"><span data-stu-id="36def-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="36def-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="36def-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="36def-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="36def-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="36def-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="36def-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="36def-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="36def-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="36def-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="36def-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="36def-3096">如需有關伺服器如何針對上方所列訊息的 ulChecksum 欄位驗證用戶端所指定值的詳細資訊，請參閱3.2.5 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="36def-3097">如果值大於0x00000008，則會假設用戶端能夠處理 CPMGetRowsOut 訊息中的64位位移。</span><span class="sxs-lookup"><span data-stu-id="36def-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="36def-3098">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="36def-3099">*Windows 行為：在 windows 用戶端上，iClientVersion 的設定* 如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="36def-3100">值</span><span class="sxs-lookup"><span data-stu-id="36def-3100">Value</span></span>      | <span data-ttu-id="36def-3101">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="36def-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="36def-3102">0x00000005</span></span> | <span data-ttu-id="36def-3103">用戶端作業系統是 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="36def-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="36def-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="36def-3104">0x00000008</span></span> | <span data-ttu-id="36def-3105">用戶端作業系統可能是32位的 Windows XP 或32位 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="36def-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="36def-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="36def-3106">0x00010008</span></span> | <span data-ttu-id="36def-3107">用戶端作業系統可能是64位的 Windows XP 或64位 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="36def-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="36def-3108">\_**fClientIsRemote**：布林值，指出用戶端是否正在與伺服器不同的電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="36def-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="36def-3109">必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="36def-3110">\_**cbBlob1**：32位不帶正負號的整數，表示 CPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="36def-3111">\_**cbBlob2**：32位不帶正負號的整數，表示 CExPropSet 和 aPropertySet 欄位的大小（以位元組為單位），結合起來。</span><span class="sxs-lookup"><span data-stu-id="36def-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="36def-3112">\_**填補**：可以包含任意值的12個位元組填補，而且必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="36def-3113">**MachineName**：用戶端的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="36def-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="36def-3114">名稱字串必須是小於512個 Unicode 字元的 null 終止陣列，包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="36def-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="36def-3115">**UserName**：代表正在執行叫用此通訊協定之應用程式之人員的使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="36def-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="36def-3116">當與 MachineName 串連時，名稱字串必須是小於512的 Unicode 字元之以 null 結束的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="36def-3117">**\_ paddingcPropSets**：此欄位的長度必須介於0到7個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="36def-3118">位元組數必須是將 cPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="36def-3119">位元組的值可以是任意值，而且接收者必須忽略此值。</span><span class="sxs-lookup"><span data-stu-id="36def-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-3120">**cPropSets**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="36def-3121">此值必須設為0x0000002。</span><span class="sxs-lookup"><span data-stu-id="36def-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="36def-3122">**PropertySet1**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ FSCIFRMWRK \_ EXT (請參閱 2.2.1.22) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="36def-3123">**PropertySet2**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ CIFRMWRKCORE \_ EXT (請參閱 2.2.1.22) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="36def-3124">\_**PaddingExtPropset**：此欄位的長度必須介於0到7個位元組之間。</span><span class="sxs-lookup"><span data-stu-id="36def-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="36def-3125">位元組數必須是將 cExtPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="36def-3126">位元組的值可以是任意值，而且接收者必須忽略此值。</span><span class="sxs-lookup"><span data-stu-id="36def-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-3127">**cExtPropSet**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="36def-3128">**aPropertySets**：指定其他屬性之 CDbPropSet 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="36def-3129">此陣列中的元素數目必須等於 cExtPropSet。</span><span class="sxs-lookup"><span data-stu-id="36def-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="36def-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="36def-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="36def-3131">CPMConnectOut 訊息包含 CPMConnectIn 訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="36def-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="36def-3132">標頭後面的 CPMConnectOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3133">0</span><span class="sxs-lookup"><span data-stu-id="36def-3133">0</span></span>

<span data-ttu-id="36def-3134">1</span><span class="sxs-lookup"><span data-stu-id="36def-3134">1</span></span>

<span data-ttu-id="36def-3135">2</span><span class="sxs-lookup"><span data-stu-id="36def-3135">2</span></span>

<span data-ttu-id="36def-3136">3</span><span class="sxs-lookup"><span data-stu-id="36def-3136">3</span></span>

<span data-ttu-id="36def-3137">4</span><span class="sxs-lookup"><span data-stu-id="36def-3137">4</span></span>

<span data-ttu-id="36def-3138">5</span><span class="sxs-lookup"><span data-stu-id="36def-3138">5</span></span>

<span data-ttu-id="36def-3139">6</span><span class="sxs-lookup"><span data-stu-id="36def-3139">6</span></span>

<span data-ttu-id="36def-3140">7</span><span class="sxs-lookup"><span data-stu-id="36def-3140">7</span></span>

<span data-ttu-id="36def-3141">8</span><span class="sxs-lookup"><span data-stu-id="36def-3141">8</span></span>

<span data-ttu-id="36def-3142">9</span><span class="sxs-lookup"><span data-stu-id="36def-3142">9</span></span>

<span data-ttu-id="36def-3143">1</span><span class="sxs-lookup"><span data-stu-id="36def-3143">1</span></span><br/> <span data-ttu-id="36def-3144">0</span><span class="sxs-lookup"><span data-stu-id="36def-3144">0</span></span><br/>

<span data-ttu-id="36def-3145">1</span><span class="sxs-lookup"><span data-stu-id="36def-3145">1</span></span>

<span data-ttu-id="36def-3146">2</span><span class="sxs-lookup"><span data-stu-id="36def-3146">2</span></span>

<span data-ttu-id="36def-3147">3</span><span class="sxs-lookup"><span data-stu-id="36def-3147">3</span></span>

<span data-ttu-id="36def-3148">4</span><span class="sxs-lookup"><span data-stu-id="36def-3148">4</span></span>

<span data-ttu-id="36def-3149">5</span><span class="sxs-lookup"><span data-stu-id="36def-3149">5</span></span>

<span data-ttu-id="36def-3150">6</span><span class="sxs-lookup"><span data-stu-id="36def-3150">6</span></span>

<span data-ttu-id="36def-3151">7</span><span class="sxs-lookup"><span data-stu-id="36def-3151">7</span></span>

<span data-ttu-id="36def-3152">8</span><span class="sxs-lookup"><span data-stu-id="36def-3152">8</span></span>

<span data-ttu-id="36def-3153">9</span><span class="sxs-lookup"><span data-stu-id="36def-3153">9</span></span>

<span data-ttu-id="36def-3154">2</span><span class="sxs-lookup"><span data-stu-id="36def-3154">2</span></span><br/> <span data-ttu-id="36def-3155">0</span><span class="sxs-lookup"><span data-stu-id="36def-3155">0</span></span><br/>

<span data-ttu-id="36def-3156">1</span><span class="sxs-lookup"><span data-stu-id="36def-3156">1</span></span>

<span data-ttu-id="36def-3157">2</span><span class="sxs-lookup"><span data-stu-id="36def-3157">2</span></span>

<span data-ttu-id="36def-3158">3</span><span class="sxs-lookup"><span data-stu-id="36def-3158">3</span></span>

<span data-ttu-id="36def-3159">4</span><span class="sxs-lookup"><span data-stu-id="36def-3159">4</span></span>

<span data-ttu-id="36def-3160">5</span><span class="sxs-lookup"><span data-stu-id="36def-3160">5</span></span>

<span data-ttu-id="36def-3161">6</span><span class="sxs-lookup"><span data-stu-id="36def-3161">6</span></span>

<span data-ttu-id="36def-3162">7</span><span class="sxs-lookup"><span data-stu-id="36def-3162">7</span></span>

<span data-ttu-id="36def-3163">8</span><span class="sxs-lookup"><span data-stu-id="36def-3163">8</span></span>

<span data-ttu-id="36def-3164">9</span><span class="sxs-lookup"><span data-stu-id="36def-3164">9</span></span>

<span data-ttu-id="36def-3165">3</span><span class="sxs-lookup"><span data-stu-id="36def-3165">3</span></span><br/> <span data-ttu-id="36def-3166">0</span><span class="sxs-lookup"><span data-stu-id="36def-3166">0</span></span><br/>

<span data-ttu-id="36def-3167">1</span><span class="sxs-lookup"><span data-stu-id="36def-3167">1</span></span>

<span data-ttu-id="36def-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="36def-3168">\_serverVersion</span></span>

<span data-ttu-id="36def-3169">\_保留的 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="36def-3170">**\_ serverVersion**：</span><span class="sxs-lookup"><span data-stu-id="36def-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="36def-3171">32位整數，表示伺服器是否可支援64位位移 *。*</span><span class="sxs-lookup"><span data-stu-id="36def-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="36def-3172">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="36def-3173">值</span><span class="sxs-lookup"><span data-stu-id="36def-3173">Value</span></span>      | <span data-ttu-id="36def-3174">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="36def-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="36def-3175">0x00000007</span></span> | <span data-ttu-id="36def-3176">伺服器只能傳送32位的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="36def-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="36def-3177">0x00010007</span></span> | <span data-ttu-id="36def-3178">伺服器可以傳送32或64位位移。</span><span class="sxs-lookup"><span data-stu-id="36def-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="36def-3179">**\_ reserved**： reserved。</span><span class="sxs-lookup"><span data-stu-id="36def-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="36def-3180">伺服器可能會傳送任意數目的任意值，而且用戶端必須忽略這些值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="36def-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="36def-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="36def-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="36def-3182">CPMCreateQueryIn 訊息會建立新的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="36def-3183">標頭後面的 CPMCreateQueryIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3184">0</span><span class="sxs-lookup"><span data-stu-id="36def-3184">0</span></span>

<span data-ttu-id="36def-3185">1</span><span class="sxs-lookup"><span data-stu-id="36def-3185">1</span></span>

<span data-ttu-id="36def-3186">2</span><span class="sxs-lookup"><span data-stu-id="36def-3186">2</span></span>

<span data-ttu-id="36def-3187">3</span><span class="sxs-lookup"><span data-stu-id="36def-3187">3</span></span>

<span data-ttu-id="36def-3188">4</span><span class="sxs-lookup"><span data-stu-id="36def-3188">4</span></span>

<span data-ttu-id="36def-3189">5</span><span class="sxs-lookup"><span data-stu-id="36def-3189">5</span></span>

<span data-ttu-id="36def-3190">6</span><span class="sxs-lookup"><span data-stu-id="36def-3190">6</span></span>

<span data-ttu-id="36def-3191">7</span><span class="sxs-lookup"><span data-stu-id="36def-3191">7</span></span>

<span data-ttu-id="36def-3192">8</span><span class="sxs-lookup"><span data-stu-id="36def-3192">8</span></span>

<span data-ttu-id="36def-3193">9</span><span class="sxs-lookup"><span data-stu-id="36def-3193">9</span></span>

<span data-ttu-id="36def-3194">1</span><span class="sxs-lookup"><span data-stu-id="36def-3194">1</span></span><br/> <span data-ttu-id="36def-3195">0</span><span class="sxs-lookup"><span data-stu-id="36def-3195">0</span></span><br/>

<span data-ttu-id="36def-3196">1</span><span class="sxs-lookup"><span data-stu-id="36def-3196">1</span></span>

<span data-ttu-id="36def-3197">2</span><span class="sxs-lookup"><span data-stu-id="36def-3197">2</span></span>

<span data-ttu-id="36def-3198">3</span><span class="sxs-lookup"><span data-stu-id="36def-3198">3</span></span>

<span data-ttu-id="36def-3199">4</span><span class="sxs-lookup"><span data-stu-id="36def-3199">4</span></span>

<span data-ttu-id="36def-3200">5</span><span class="sxs-lookup"><span data-stu-id="36def-3200">5</span></span>

<span data-ttu-id="36def-3201">6</span><span class="sxs-lookup"><span data-stu-id="36def-3201">6</span></span>

<span data-ttu-id="36def-3202">7</span><span class="sxs-lookup"><span data-stu-id="36def-3202">7</span></span>

<span data-ttu-id="36def-3203">8</span><span class="sxs-lookup"><span data-stu-id="36def-3203">8</span></span>

<span data-ttu-id="36def-3204">9</span><span class="sxs-lookup"><span data-stu-id="36def-3204">9</span></span>

<span data-ttu-id="36def-3205">2</span><span class="sxs-lookup"><span data-stu-id="36def-3205">2</span></span><br/> <span data-ttu-id="36def-3206">0</span><span class="sxs-lookup"><span data-stu-id="36def-3206">0</span></span><br/>

<span data-ttu-id="36def-3207">1</span><span class="sxs-lookup"><span data-stu-id="36def-3207">1</span></span>

<span data-ttu-id="36def-3208">2</span><span class="sxs-lookup"><span data-stu-id="36def-3208">2</span></span>

<span data-ttu-id="36def-3209">3</span><span class="sxs-lookup"><span data-stu-id="36def-3209">3</span></span>

<span data-ttu-id="36def-3210">4</span><span class="sxs-lookup"><span data-stu-id="36def-3210">4</span></span>

<span data-ttu-id="36def-3211">5</span><span class="sxs-lookup"><span data-stu-id="36def-3211">5</span></span>

<span data-ttu-id="36def-3212">6</span><span class="sxs-lookup"><span data-stu-id="36def-3212">6</span></span>

<span data-ttu-id="36def-3213">7</span><span class="sxs-lookup"><span data-stu-id="36def-3213">7</span></span>

<span data-ttu-id="36def-3214">8</span><span class="sxs-lookup"><span data-stu-id="36def-3214">8</span></span>

<span data-ttu-id="36def-3215">9</span><span class="sxs-lookup"><span data-stu-id="36def-3215">9</span></span>

<span data-ttu-id="36def-3216">3</span><span class="sxs-lookup"><span data-stu-id="36def-3216">3</span></span><br/> <span data-ttu-id="36def-3217">0</span><span class="sxs-lookup"><span data-stu-id="36def-3217">0</span></span><br/>

<span data-ttu-id="36def-3218">1</span><span class="sxs-lookup"><span data-stu-id="36def-3218">1</span></span>

<span data-ttu-id="36def-3219">大小</span><span class="sxs-lookup"><span data-stu-id="36def-3219">Size</span></span>

<span data-ttu-id="36def-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="36def-3220">CColumnSetPresent</span></span>

<span data-ttu-id="36def-3221">ColumnSet (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="36def-3222">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3222">... (variable)</span></span>

<span data-ttu-id="36def-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="36def-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="36def-3224">限制 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-3224">Restriction (optional)</span></span>

<span data-ttu-id="36def-3225">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3225">... (variable)</span></span>

<span data-ttu-id="36def-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="36def-3226">CSortSetPresent</span></span>

<span data-ttu-id="36def-3227">SortSet (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3227">SortSet (optional)</span></span>

<span data-ttu-id="36def-3228">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3228">... (variable)</span></span>

<span data-ttu-id="36def-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="36def-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="36def-3230">CategorizationSet (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="36def-3231">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3231">... (variable)</span></span>

<span data-ttu-id="36def-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="36def-3232">RowSetProperties</span></span>

<span data-ttu-id="36def-3233">...</span><span class="sxs-lookup"><span data-stu-id="36def-3233">...</span></span>

<span data-ttu-id="36def-3234">...</span><span class="sxs-lookup"><span data-stu-id="36def-3234">...</span></span>

<span data-ttu-id="36def-3235">...</span><span class="sxs-lookup"><span data-stu-id="36def-3235">...</span></span>

<span data-ttu-id="36def-3236">...</span><span class="sxs-lookup"><span data-stu-id="36def-3236">...</span></span>

<span data-ttu-id="36def-3237">PidMapper (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="36def-3238">**大小**：32位不帶正負號的整數，表示從這個欄位開頭到訊息結尾的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="36def-3239">**CColumnSetPresent**：指出 ColumnSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="36def-3240">此欄位必須設定為0x01 或0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="36def-3241">如果設定為0x01，則必須有 CColumnSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="36def-3242">如果設定為0x00，則必須不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="36def-3243">**ColumnSet**： CColumnSet 結構，其中包含要傳回 CPidMapper 屬性的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="36def-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="36def-3244">**CRestrictionPresent**：一個位元組欄位，指出限制欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="36def-3245">如果設定為任何非零值，則限制欄位必須存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="36def-3246">如果設定為0x00，則限制必須不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="36def-3247">**限制**： CRestriction 結構，其中包含查詢的命令樹。</span><span class="sxs-lookup"><span data-stu-id="36def-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="36def-3248">**CSortSetPresent**：指出 SortSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="36def-3249">如果設定為任何非零值，則必須有 SortSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="36def-3250">如果設定為0x00，則 SortSet 必須不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="36def-3251">**SortSet**： CSortSet 結構，指出查詢的排序次序。</span><span class="sxs-lookup"><span data-stu-id="36def-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="36def-3252">**CCategorizationSetPresent**：指出 CCategorizationSet 欄位是否存在的位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="36def-3253">如果設定為任何非零值，則必須有 CCategorizationSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="36def-3254">如果設定為0x00，則 CCategorizationSet 必須不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="36def-3255">**CCategorizationSet**：包含查詢群組的 CCategorizationSet 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="36def-3256">**RowSetProperties**：提供查詢設定資訊的 CRowsetProperties 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="36def-3257">**PidMapper**： CPidMapper 結構，其中包含要在資料列集中傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="36def-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="36def-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="36def-3259">CPMCreateQueryOut 訊息包含 CPMCreateQueryIn 訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="36def-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="36def-3260">標頭後面的 CPMCreateQueryOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3261">0</span><span class="sxs-lookup"><span data-stu-id="36def-3261">0</span></span>

<span data-ttu-id="36def-3262">1</span><span class="sxs-lookup"><span data-stu-id="36def-3262">1</span></span>

<span data-ttu-id="36def-3263">2</span><span class="sxs-lookup"><span data-stu-id="36def-3263">2</span></span>

<span data-ttu-id="36def-3264">3</span><span class="sxs-lookup"><span data-stu-id="36def-3264">3</span></span>

<span data-ttu-id="36def-3265">4</span><span class="sxs-lookup"><span data-stu-id="36def-3265">4</span></span>

<span data-ttu-id="36def-3266">5</span><span class="sxs-lookup"><span data-stu-id="36def-3266">5</span></span>

<span data-ttu-id="36def-3267">6</span><span class="sxs-lookup"><span data-stu-id="36def-3267">6</span></span>

<span data-ttu-id="36def-3268">7</span><span class="sxs-lookup"><span data-stu-id="36def-3268">7</span></span>

<span data-ttu-id="36def-3269">8</span><span class="sxs-lookup"><span data-stu-id="36def-3269">8</span></span>

<span data-ttu-id="36def-3270">9</span><span class="sxs-lookup"><span data-stu-id="36def-3270">9</span></span>

<span data-ttu-id="36def-3271">1</span><span class="sxs-lookup"><span data-stu-id="36def-3271">1</span></span><br/> <span data-ttu-id="36def-3272">0</span><span class="sxs-lookup"><span data-stu-id="36def-3272">0</span></span><br/>

<span data-ttu-id="36def-3273">1</span><span class="sxs-lookup"><span data-stu-id="36def-3273">1</span></span>

<span data-ttu-id="36def-3274">2</span><span class="sxs-lookup"><span data-stu-id="36def-3274">2</span></span>

<span data-ttu-id="36def-3275">3</span><span class="sxs-lookup"><span data-stu-id="36def-3275">3</span></span>

<span data-ttu-id="36def-3276">4</span><span class="sxs-lookup"><span data-stu-id="36def-3276">4</span></span>

<span data-ttu-id="36def-3277">5</span><span class="sxs-lookup"><span data-stu-id="36def-3277">5</span></span>

<span data-ttu-id="36def-3278">6</span><span class="sxs-lookup"><span data-stu-id="36def-3278">6</span></span>

<span data-ttu-id="36def-3279">7</span><span class="sxs-lookup"><span data-stu-id="36def-3279">7</span></span>

<span data-ttu-id="36def-3280">8</span><span class="sxs-lookup"><span data-stu-id="36def-3280">8</span></span>

<span data-ttu-id="36def-3281">9</span><span class="sxs-lookup"><span data-stu-id="36def-3281">9</span></span>

<span data-ttu-id="36def-3282">2</span><span class="sxs-lookup"><span data-stu-id="36def-3282">2</span></span><br/> <span data-ttu-id="36def-3283">0</span><span class="sxs-lookup"><span data-stu-id="36def-3283">0</span></span><br/>

<span data-ttu-id="36def-3284">1</span><span class="sxs-lookup"><span data-stu-id="36def-3284">1</span></span>

<span data-ttu-id="36def-3285">2</span><span class="sxs-lookup"><span data-stu-id="36def-3285">2</span></span>

<span data-ttu-id="36def-3286">3</span><span class="sxs-lookup"><span data-stu-id="36def-3286">3</span></span>

<span data-ttu-id="36def-3287">4</span><span class="sxs-lookup"><span data-stu-id="36def-3287">4</span></span>

<span data-ttu-id="36def-3288">5</span><span class="sxs-lookup"><span data-stu-id="36def-3288">5</span></span>

<span data-ttu-id="36def-3289">6</span><span class="sxs-lookup"><span data-stu-id="36def-3289">6</span></span>

<span data-ttu-id="36def-3290">7</span><span class="sxs-lookup"><span data-stu-id="36def-3290">7</span></span>

<span data-ttu-id="36def-3291">8</span><span class="sxs-lookup"><span data-stu-id="36def-3291">8</span></span>

<span data-ttu-id="36def-3292">9</span><span class="sxs-lookup"><span data-stu-id="36def-3292">9</span></span>

<span data-ttu-id="36def-3293">3</span><span class="sxs-lookup"><span data-stu-id="36def-3293">3</span></span><br/> <span data-ttu-id="36def-3294">0</span><span class="sxs-lookup"><span data-stu-id="36def-3294">0</span></span><br/>

<span data-ttu-id="36def-3295">1</span><span class="sxs-lookup"><span data-stu-id="36def-3295">1</span></span>

<span data-ttu-id="36def-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="36def-3296">\_fTrueSequential</span></span>

<span data-ttu-id="36def-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="36def-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="36def-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="36def-3298">aCursors</span></span>



 

<span data-ttu-id="36def-3299">**\_ fTrueSequential**：資訊性布林值，指出查詢是否可預期更快提供結果。</span><span class="sxs-lookup"><span data-stu-id="36def-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="36def-3300">當針對 CPMCreateQueryIn 中提供的查詢設定為0x00000001 時，伺服器可以使用索引，因為這樣可能會更快傳遞查詢結果。</span><span class="sxs-lookup"><span data-stu-id="36def-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="36def-3301">當設定為0x00000000 時，傳遞查詢結果會有較大的延遲。</span><span class="sxs-lookup"><span data-stu-id="36def-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="36def-3302">不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="36def-3303">**\_ fWorkIdUnique**：布林值，指出資料指標所指向的檔識別碼在查詢結果中是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="36def-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="36def-3304">如果設定為0x00000001，則識別碼是唯一的。</span><span class="sxs-lookup"><span data-stu-id="36def-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="36def-3305">如果設定為0x00000000，則只有在整個資料列集中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="36def-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="36def-3306">**aCursors**：32位不帶正負號整數的陣列，代表資料指標的控制碼，其中專案數等於 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中的類別目錄數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="36def-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="36def-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="36def-3308">CPMGetQueryStatusIn 訊息會要求查詢的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="36def-3309">標頭後面的 CPMGetQueryStatusIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3310">0</span><span class="sxs-lookup"><span data-stu-id="36def-3310">0</span></span>

<span data-ttu-id="36def-3311">1</span><span class="sxs-lookup"><span data-stu-id="36def-3311">1</span></span>

<span data-ttu-id="36def-3312">2</span><span class="sxs-lookup"><span data-stu-id="36def-3312">2</span></span>

<span data-ttu-id="36def-3313">3</span><span class="sxs-lookup"><span data-stu-id="36def-3313">3</span></span>

<span data-ttu-id="36def-3314">4</span><span class="sxs-lookup"><span data-stu-id="36def-3314">4</span></span>

<span data-ttu-id="36def-3315">5</span><span class="sxs-lookup"><span data-stu-id="36def-3315">5</span></span>

<span data-ttu-id="36def-3316">6</span><span class="sxs-lookup"><span data-stu-id="36def-3316">6</span></span>

<span data-ttu-id="36def-3317">7</span><span class="sxs-lookup"><span data-stu-id="36def-3317">7</span></span>

<span data-ttu-id="36def-3318">8</span><span class="sxs-lookup"><span data-stu-id="36def-3318">8</span></span>

<span data-ttu-id="36def-3319">9</span><span class="sxs-lookup"><span data-stu-id="36def-3319">9</span></span>

<span data-ttu-id="36def-3320">1</span><span class="sxs-lookup"><span data-stu-id="36def-3320">1</span></span><br/> <span data-ttu-id="36def-3321">0</span><span class="sxs-lookup"><span data-stu-id="36def-3321">0</span></span><br/>

<span data-ttu-id="36def-3322">1</span><span class="sxs-lookup"><span data-stu-id="36def-3322">1</span></span>

<span data-ttu-id="36def-3323">2</span><span class="sxs-lookup"><span data-stu-id="36def-3323">2</span></span>

<span data-ttu-id="36def-3324">3</span><span class="sxs-lookup"><span data-stu-id="36def-3324">3</span></span>

<span data-ttu-id="36def-3325">4</span><span class="sxs-lookup"><span data-stu-id="36def-3325">4</span></span>

<span data-ttu-id="36def-3326">5</span><span class="sxs-lookup"><span data-stu-id="36def-3326">5</span></span>

<span data-ttu-id="36def-3327">6</span><span class="sxs-lookup"><span data-stu-id="36def-3327">6</span></span>

<span data-ttu-id="36def-3328">7</span><span class="sxs-lookup"><span data-stu-id="36def-3328">7</span></span>

<span data-ttu-id="36def-3329">8</span><span class="sxs-lookup"><span data-stu-id="36def-3329">8</span></span>

<span data-ttu-id="36def-3330">9</span><span class="sxs-lookup"><span data-stu-id="36def-3330">9</span></span>

<span data-ttu-id="36def-3331">2</span><span class="sxs-lookup"><span data-stu-id="36def-3331">2</span></span><br/> <span data-ttu-id="36def-3332">0</span><span class="sxs-lookup"><span data-stu-id="36def-3332">0</span></span><br/>

<span data-ttu-id="36def-3333">1</span><span class="sxs-lookup"><span data-stu-id="36def-3333">1</span></span>

<span data-ttu-id="36def-3334">2</span><span class="sxs-lookup"><span data-stu-id="36def-3334">2</span></span>

<span data-ttu-id="36def-3335">3</span><span class="sxs-lookup"><span data-stu-id="36def-3335">3</span></span>

<span data-ttu-id="36def-3336">4</span><span class="sxs-lookup"><span data-stu-id="36def-3336">4</span></span>

<span data-ttu-id="36def-3337">5</span><span class="sxs-lookup"><span data-stu-id="36def-3337">5</span></span>

<span data-ttu-id="36def-3338">6</span><span class="sxs-lookup"><span data-stu-id="36def-3338">6</span></span>

<span data-ttu-id="36def-3339">7</span><span class="sxs-lookup"><span data-stu-id="36def-3339">7</span></span>

<span data-ttu-id="36def-3340">8</span><span class="sxs-lookup"><span data-stu-id="36def-3340">8</span></span>

<span data-ttu-id="36def-3341">9</span><span class="sxs-lookup"><span data-stu-id="36def-3341">9</span></span>

<span data-ttu-id="36def-3342">3</span><span class="sxs-lookup"><span data-stu-id="36def-3342">3</span></span><br/> <span data-ttu-id="36def-3343">0</span><span class="sxs-lookup"><span data-stu-id="36def-3343">0</span></span><br/>

<span data-ttu-id="36def-3344">1</span><span class="sxs-lookup"><span data-stu-id="36def-3344">1</span></span>

<span data-ttu-id="36def-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-3345">\_hCursor</span></span>



 

<span data-ttu-id="36def-3346">**\_ hCursor**：32位不帶正負號的整數，代表 CPMCreateQueryOut 訊息中的控制碼，該控制碼會識別要取得其狀態資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="36def-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="36def-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="36def-3348">CPMGetQueryStatusOut 訊息會以查詢的狀態回復 CPMGetQueryStatusIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="36def-3349">標頭後面的 CPMGetQueryStatusOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3350">0</span><span class="sxs-lookup"><span data-stu-id="36def-3350">0</span></span>

<span data-ttu-id="36def-3351">1</span><span class="sxs-lookup"><span data-stu-id="36def-3351">1</span></span>

<span data-ttu-id="36def-3352">2</span><span class="sxs-lookup"><span data-stu-id="36def-3352">2</span></span>

<span data-ttu-id="36def-3353">3</span><span class="sxs-lookup"><span data-stu-id="36def-3353">3</span></span>

<span data-ttu-id="36def-3354">4</span><span class="sxs-lookup"><span data-stu-id="36def-3354">4</span></span>

<span data-ttu-id="36def-3355">5</span><span class="sxs-lookup"><span data-stu-id="36def-3355">5</span></span>

<span data-ttu-id="36def-3356">6</span><span class="sxs-lookup"><span data-stu-id="36def-3356">6</span></span>

<span data-ttu-id="36def-3357">7</span><span class="sxs-lookup"><span data-stu-id="36def-3357">7</span></span>

<span data-ttu-id="36def-3358">8</span><span class="sxs-lookup"><span data-stu-id="36def-3358">8</span></span>

<span data-ttu-id="36def-3359">9</span><span class="sxs-lookup"><span data-stu-id="36def-3359">9</span></span>

<span data-ttu-id="36def-3360">1</span><span class="sxs-lookup"><span data-stu-id="36def-3360">1</span></span><br/> <span data-ttu-id="36def-3361">0</span><span class="sxs-lookup"><span data-stu-id="36def-3361">0</span></span><br/>

<span data-ttu-id="36def-3362">1</span><span class="sxs-lookup"><span data-stu-id="36def-3362">1</span></span>

<span data-ttu-id="36def-3363">2</span><span class="sxs-lookup"><span data-stu-id="36def-3363">2</span></span>

<span data-ttu-id="36def-3364">3</span><span class="sxs-lookup"><span data-stu-id="36def-3364">3</span></span>

<span data-ttu-id="36def-3365">4</span><span class="sxs-lookup"><span data-stu-id="36def-3365">4</span></span>

<span data-ttu-id="36def-3366">5</span><span class="sxs-lookup"><span data-stu-id="36def-3366">5</span></span>

<span data-ttu-id="36def-3367">6</span><span class="sxs-lookup"><span data-stu-id="36def-3367">6</span></span>

<span data-ttu-id="36def-3368">7</span><span class="sxs-lookup"><span data-stu-id="36def-3368">7</span></span>

<span data-ttu-id="36def-3369">8</span><span class="sxs-lookup"><span data-stu-id="36def-3369">8</span></span>

<span data-ttu-id="36def-3370">9</span><span class="sxs-lookup"><span data-stu-id="36def-3370">9</span></span>

<span data-ttu-id="36def-3371">2</span><span class="sxs-lookup"><span data-stu-id="36def-3371">2</span></span><br/> <span data-ttu-id="36def-3372">0</span><span class="sxs-lookup"><span data-stu-id="36def-3372">0</span></span><br/>

<span data-ttu-id="36def-3373">1</span><span class="sxs-lookup"><span data-stu-id="36def-3373">1</span></span>

<span data-ttu-id="36def-3374">2</span><span class="sxs-lookup"><span data-stu-id="36def-3374">2</span></span>

<span data-ttu-id="36def-3375">3</span><span class="sxs-lookup"><span data-stu-id="36def-3375">3</span></span>

<span data-ttu-id="36def-3376">4</span><span class="sxs-lookup"><span data-stu-id="36def-3376">4</span></span>

<span data-ttu-id="36def-3377">5</span><span class="sxs-lookup"><span data-stu-id="36def-3377">5</span></span>

<span data-ttu-id="36def-3378">6</span><span class="sxs-lookup"><span data-stu-id="36def-3378">6</span></span>

<span data-ttu-id="36def-3379">7</span><span class="sxs-lookup"><span data-stu-id="36def-3379">7</span></span>

<span data-ttu-id="36def-3380">8</span><span class="sxs-lookup"><span data-stu-id="36def-3380">8</span></span>

<span data-ttu-id="36def-3381">9</span><span class="sxs-lookup"><span data-stu-id="36def-3381">9</span></span>

<span data-ttu-id="36def-3382">3</span><span class="sxs-lookup"><span data-stu-id="36def-3382">3</span></span><br/> <span data-ttu-id="36def-3383">0</span><span class="sxs-lookup"><span data-stu-id="36def-3383">0</span></span><br/>

<span data-ttu-id="36def-3384">1</span><span class="sxs-lookup"><span data-stu-id="36def-3384">1</span></span>

<span data-ttu-id="36def-3385">\_狀態</span><span class="sxs-lookup"><span data-stu-id="36def-3385">\_Status</span></span>



 

<span data-ttu-id="36def-3386">**\_ 狀態**：下表中定義的值位元遮罩，可描述查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="36def-3387">下表列出透過 \_ \* 0x00000007 對狀態執行位 and 運算所取得的 STAT 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="36def-3388">結果必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="36def-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="36def-3389">常數</span><span class="sxs-lookup"><span data-stu-id="36def-3389">Constant</span></span>                 | <span data-ttu-id="36def-3390">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="36def-3391">STAT \_ 忙碌0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="36def-3392">非同步查詢仍在執行中。</span><span class="sxs-lookup"><span data-stu-id="36def-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="36def-3393">STAT \_ 錯誤0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="36def-3394">查詢處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="36def-3395">STAT \_ 完成0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="36def-3396">查詢已完成。</span><span class="sxs-lookup"><span data-stu-id="36def-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="36def-3397">STAT \_ REFRESH 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="36def-3398">查詢已完成，但更新會導致額外的查詢計算。</span><span class="sxs-lookup"><span data-stu-id="36def-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="36def-3399">下表列出 \_ \* 可以獨立設定的其他 STAT 位。</span><span class="sxs-lookup"><span data-stu-id="36def-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="36def-3400">常數</span><span class="sxs-lookup"><span data-stu-id="36def-3400">Constant</span></span>                                    | <span data-ttu-id="36def-3401">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36def-3402">STAT 非搜尋 \_ \_ 字0x00000010</span><span class="sxs-lookup"><span data-stu-id="36def-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="36def-3403">在內容查詢中，以萬用字元取代非搜尋字。</span><span class="sxs-lookup"><span data-stu-id="36def-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="36def-3404">\_新的 STAT 內容已 \_ 過期 \_ \_</span><span class="sxs-lookup"><span data-stu-id="36def-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="36def-3405">查詢的結果可能不正確，因為涉及修改但未建立索引的檔案。</span><span class="sxs-lookup"><span data-stu-id="36def-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="36def-3406">STAT 重新整理 \_ \_ 未完成0x00000040</span><span class="sxs-lookup"><span data-stu-id="36def-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="36def-3407">查詢的結果可能不正確，因為涉及修改的查詢和重新編制索引的檔案不包含內容。</span><span class="sxs-lookup"><span data-stu-id="36def-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="36def-3408">STAT \_ 內容 \_ 查詢 \_ 未完成0x00000080</span><span class="sxs-lookup"><span data-stu-id="36def-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="36def-3409">內容查詢太複雜而無法完成或需要列舉，而不是使用內容索引。</span><span class="sxs-lookup"><span data-stu-id="36def-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="36def-3410">已 \_ 超過 STAT 時間 \_ 限制 \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="36def-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="36def-3411">查詢的結果可能不正確，因為查詢執行時間達到允許的時間上限。</span><span class="sxs-lookup"><span data-stu-id="36def-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="36def-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="36def-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="36def-3413">CPMGetQueryStatusExIn 訊息會要求查詢的狀態和其他資訊，例如已編制索引的檔數目、剩下要編制索引的檔數目等等。</span><span class="sxs-lookup"><span data-stu-id="36def-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="36def-3414">標頭後面的 CPMGetQueryStatusExIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3415">0</span><span class="sxs-lookup"><span data-stu-id="36def-3415">0</span></span>

<span data-ttu-id="36def-3416">1</span><span class="sxs-lookup"><span data-stu-id="36def-3416">1</span></span>

<span data-ttu-id="36def-3417">2</span><span class="sxs-lookup"><span data-stu-id="36def-3417">2</span></span>

<span data-ttu-id="36def-3418">3</span><span class="sxs-lookup"><span data-stu-id="36def-3418">3</span></span>

<span data-ttu-id="36def-3419">4</span><span class="sxs-lookup"><span data-stu-id="36def-3419">4</span></span>

<span data-ttu-id="36def-3420">5</span><span class="sxs-lookup"><span data-stu-id="36def-3420">5</span></span>

<span data-ttu-id="36def-3421">6</span><span class="sxs-lookup"><span data-stu-id="36def-3421">6</span></span>

<span data-ttu-id="36def-3422">7</span><span class="sxs-lookup"><span data-stu-id="36def-3422">7</span></span>

<span data-ttu-id="36def-3423">8</span><span class="sxs-lookup"><span data-stu-id="36def-3423">8</span></span>

<span data-ttu-id="36def-3424">9</span><span class="sxs-lookup"><span data-stu-id="36def-3424">9</span></span>

<span data-ttu-id="36def-3425">1</span><span class="sxs-lookup"><span data-stu-id="36def-3425">1</span></span><br/> <span data-ttu-id="36def-3426">0</span><span class="sxs-lookup"><span data-stu-id="36def-3426">0</span></span><br/>

<span data-ttu-id="36def-3427">1</span><span class="sxs-lookup"><span data-stu-id="36def-3427">1</span></span>

<span data-ttu-id="36def-3428">2</span><span class="sxs-lookup"><span data-stu-id="36def-3428">2</span></span>

<span data-ttu-id="36def-3429">3</span><span class="sxs-lookup"><span data-stu-id="36def-3429">3</span></span>

<span data-ttu-id="36def-3430">4</span><span class="sxs-lookup"><span data-stu-id="36def-3430">4</span></span>

<span data-ttu-id="36def-3431">5</span><span class="sxs-lookup"><span data-stu-id="36def-3431">5</span></span>

<span data-ttu-id="36def-3432">6</span><span class="sxs-lookup"><span data-stu-id="36def-3432">6</span></span>

<span data-ttu-id="36def-3433">7</span><span class="sxs-lookup"><span data-stu-id="36def-3433">7</span></span>

<span data-ttu-id="36def-3434">8</span><span class="sxs-lookup"><span data-stu-id="36def-3434">8</span></span>

<span data-ttu-id="36def-3435">9</span><span class="sxs-lookup"><span data-stu-id="36def-3435">9</span></span>

<span data-ttu-id="36def-3436">2</span><span class="sxs-lookup"><span data-stu-id="36def-3436">2</span></span><br/> <span data-ttu-id="36def-3437">0</span><span class="sxs-lookup"><span data-stu-id="36def-3437">0</span></span><br/>

<span data-ttu-id="36def-3438">1</span><span class="sxs-lookup"><span data-stu-id="36def-3438">1</span></span>

<span data-ttu-id="36def-3439">2</span><span class="sxs-lookup"><span data-stu-id="36def-3439">2</span></span>

<span data-ttu-id="36def-3440">3</span><span class="sxs-lookup"><span data-stu-id="36def-3440">3</span></span>

<span data-ttu-id="36def-3441">4</span><span class="sxs-lookup"><span data-stu-id="36def-3441">4</span></span>

<span data-ttu-id="36def-3442">5</span><span class="sxs-lookup"><span data-stu-id="36def-3442">5</span></span>

<span data-ttu-id="36def-3443">6</span><span class="sxs-lookup"><span data-stu-id="36def-3443">6</span></span>

<span data-ttu-id="36def-3444">7</span><span class="sxs-lookup"><span data-stu-id="36def-3444">7</span></span>

<span data-ttu-id="36def-3445">8</span><span class="sxs-lookup"><span data-stu-id="36def-3445">8</span></span>

<span data-ttu-id="36def-3446">9</span><span class="sxs-lookup"><span data-stu-id="36def-3446">9</span></span>

<span data-ttu-id="36def-3447">3</span><span class="sxs-lookup"><span data-stu-id="36def-3447">3</span></span><br/> <span data-ttu-id="36def-3448">0</span><span class="sxs-lookup"><span data-stu-id="36def-3448">0</span></span><br/>

<span data-ttu-id="36def-3449">1</span><span class="sxs-lookup"><span data-stu-id="36def-3449">1</span></span>

<span data-ttu-id="36def-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-3450">\_hCursor</span></span>

<span data-ttu-id="36def-3451">\_bmk</span><span class="sxs-lookup"><span data-stu-id="36def-3451">\_bmk</span></span>



 

<span data-ttu-id="36def-3452">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得狀態資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="36def-3453">**\_ bmk**：代表應抓取其位置之書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="36def-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="36def-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="36def-3455">CPMGetQueryStatusExOut 訊息會以查詢的狀態和其他狀態資訊回復 CPMGetQueryStatusExIn 訊息，如下圖所述。</span><span class="sxs-lookup"><span data-stu-id="36def-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="36def-3456">標頭後面的 CPMGetQueryStatusExOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3457">0</span><span class="sxs-lookup"><span data-stu-id="36def-3457">0</span></span>

<span data-ttu-id="36def-3458">1</span><span class="sxs-lookup"><span data-stu-id="36def-3458">1</span></span>

<span data-ttu-id="36def-3459">2</span><span class="sxs-lookup"><span data-stu-id="36def-3459">2</span></span>

<span data-ttu-id="36def-3460">3</span><span class="sxs-lookup"><span data-stu-id="36def-3460">3</span></span>

<span data-ttu-id="36def-3461">4</span><span class="sxs-lookup"><span data-stu-id="36def-3461">4</span></span>

<span data-ttu-id="36def-3462">5</span><span class="sxs-lookup"><span data-stu-id="36def-3462">5</span></span>

<span data-ttu-id="36def-3463">6</span><span class="sxs-lookup"><span data-stu-id="36def-3463">6</span></span>

<span data-ttu-id="36def-3464">7</span><span class="sxs-lookup"><span data-stu-id="36def-3464">7</span></span>

<span data-ttu-id="36def-3465">8</span><span class="sxs-lookup"><span data-stu-id="36def-3465">8</span></span>

<span data-ttu-id="36def-3466">9</span><span class="sxs-lookup"><span data-stu-id="36def-3466">9</span></span>

<span data-ttu-id="36def-3467">1</span><span class="sxs-lookup"><span data-stu-id="36def-3467">1</span></span><br/> <span data-ttu-id="36def-3468">0</span><span class="sxs-lookup"><span data-stu-id="36def-3468">0</span></span><br/>

<span data-ttu-id="36def-3469">1</span><span class="sxs-lookup"><span data-stu-id="36def-3469">1</span></span>

<span data-ttu-id="36def-3470">2</span><span class="sxs-lookup"><span data-stu-id="36def-3470">2</span></span>

<span data-ttu-id="36def-3471">3</span><span class="sxs-lookup"><span data-stu-id="36def-3471">3</span></span>

<span data-ttu-id="36def-3472">4</span><span class="sxs-lookup"><span data-stu-id="36def-3472">4</span></span>

<span data-ttu-id="36def-3473">5</span><span class="sxs-lookup"><span data-stu-id="36def-3473">5</span></span>

<span data-ttu-id="36def-3474">6</span><span class="sxs-lookup"><span data-stu-id="36def-3474">6</span></span>

<span data-ttu-id="36def-3475">7</span><span class="sxs-lookup"><span data-stu-id="36def-3475">7</span></span>

<span data-ttu-id="36def-3476">8</span><span class="sxs-lookup"><span data-stu-id="36def-3476">8</span></span>

<span data-ttu-id="36def-3477">9</span><span class="sxs-lookup"><span data-stu-id="36def-3477">9</span></span>

<span data-ttu-id="36def-3478">2</span><span class="sxs-lookup"><span data-stu-id="36def-3478">2</span></span><br/> <span data-ttu-id="36def-3479">0</span><span class="sxs-lookup"><span data-stu-id="36def-3479">0</span></span><br/>

<span data-ttu-id="36def-3480">1</span><span class="sxs-lookup"><span data-stu-id="36def-3480">1</span></span>

<span data-ttu-id="36def-3481">2</span><span class="sxs-lookup"><span data-stu-id="36def-3481">2</span></span>

<span data-ttu-id="36def-3482">3</span><span class="sxs-lookup"><span data-stu-id="36def-3482">3</span></span>

<span data-ttu-id="36def-3483">4</span><span class="sxs-lookup"><span data-stu-id="36def-3483">4</span></span>

<span data-ttu-id="36def-3484">5</span><span class="sxs-lookup"><span data-stu-id="36def-3484">5</span></span>

<span data-ttu-id="36def-3485">6</span><span class="sxs-lookup"><span data-stu-id="36def-3485">6</span></span>

<span data-ttu-id="36def-3486">7</span><span class="sxs-lookup"><span data-stu-id="36def-3486">7</span></span>

<span data-ttu-id="36def-3487">8</span><span class="sxs-lookup"><span data-stu-id="36def-3487">8</span></span>

<span data-ttu-id="36def-3488">9</span><span class="sxs-lookup"><span data-stu-id="36def-3488">9</span></span>

<span data-ttu-id="36def-3489">3</span><span class="sxs-lookup"><span data-stu-id="36def-3489">3</span></span><br/> <span data-ttu-id="36def-3490">0</span><span class="sxs-lookup"><span data-stu-id="36def-3490">0</span></span><br/>

<span data-ttu-id="36def-3491">1</span><span class="sxs-lookup"><span data-stu-id="36def-3491">1</span></span>

<span data-ttu-id="36def-3492">\_狀態</span><span class="sxs-lookup"><span data-stu-id="36def-3492">\_Status</span></span>

<span data-ttu-id="36def-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="36def-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="36def-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="36def-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="36def-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="36def-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="36def-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="36def-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="36def-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="36def-3497">\_iRowBmk</span></span>

<span data-ttu-id="36def-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="36def-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="36def-3499">**\_ 狀態**：其中一個 STAT \_ \*在區段2.2.3.11 中指定的值。</span><span class="sxs-lookup"><span data-stu-id="36def-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="36def-3500">**\_ cFilteredDocuments**：32位不帶正負號的整數，表示已編制索引的檔數目</span><span class="sxs-lookup"><span data-stu-id="36def-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="36def-3501">**\_ cDocumentsToFilter**：32位不帶正負號的整數，表示仍維持編制索引的檔數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="36def-3502">**\_ dwRatioFinishedDenominator**：32位不帶正負號的整數，表示查詢已完成處理之檔比例的分母。</span><span class="sxs-lookup"><span data-stu-id="36def-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="36def-3503">**\_ dwRatioFinishedNumerator**：32位不帶正負號的整數，表示查詢完成處理之檔的比率分子。</span><span class="sxs-lookup"><span data-stu-id="36def-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="36def-3504">**\_ iRowBmk**：32位不帶正負號的整數，指出資料列集中書簽的大概位置（以資料列為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="36def-3505">**\_ cRowsTotal**：32位不帶正負號的整數，指定資料列集中的資料列總數。</span><span class="sxs-lookup"><span data-stu-id="36def-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="36def-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="36def-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="36def-3507">CPMSetBindingsIn 訊息會要求將資料行系結至資料列集。</span><span class="sxs-lookup"><span data-stu-id="36def-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="36def-3508">伺服器將會使用 CPMBindingsIn 訊息的標頭區段，以及 [狀態] 欄位中包含的要求結果來回複 CPMSetBindingsIn 要求訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="36def-3509">標頭後面的 CPMSetBindingsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3510">0</span><span class="sxs-lookup"><span data-stu-id="36def-3510">0</span></span>

<span data-ttu-id="36def-3511">1</span><span class="sxs-lookup"><span data-stu-id="36def-3511">1</span></span>

<span data-ttu-id="36def-3512">2</span><span class="sxs-lookup"><span data-stu-id="36def-3512">2</span></span>

<span data-ttu-id="36def-3513">3</span><span class="sxs-lookup"><span data-stu-id="36def-3513">3</span></span>

<span data-ttu-id="36def-3514">4</span><span class="sxs-lookup"><span data-stu-id="36def-3514">4</span></span>

<span data-ttu-id="36def-3515">5</span><span class="sxs-lookup"><span data-stu-id="36def-3515">5</span></span>

<span data-ttu-id="36def-3516">6</span><span class="sxs-lookup"><span data-stu-id="36def-3516">6</span></span>

<span data-ttu-id="36def-3517">7</span><span class="sxs-lookup"><span data-stu-id="36def-3517">7</span></span>

<span data-ttu-id="36def-3518">8</span><span class="sxs-lookup"><span data-stu-id="36def-3518">8</span></span>

<span data-ttu-id="36def-3519">9</span><span class="sxs-lookup"><span data-stu-id="36def-3519">9</span></span>

<span data-ttu-id="36def-3520">1</span><span class="sxs-lookup"><span data-stu-id="36def-3520">1</span></span><br/> <span data-ttu-id="36def-3521">0</span><span class="sxs-lookup"><span data-stu-id="36def-3521">0</span></span><br/>

<span data-ttu-id="36def-3522">1</span><span class="sxs-lookup"><span data-stu-id="36def-3522">1</span></span>

<span data-ttu-id="36def-3523">2</span><span class="sxs-lookup"><span data-stu-id="36def-3523">2</span></span>

<span data-ttu-id="36def-3524">3</span><span class="sxs-lookup"><span data-stu-id="36def-3524">3</span></span>

<span data-ttu-id="36def-3525">4</span><span class="sxs-lookup"><span data-stu-id="36def-3525">4</span></span>

<span data-ttu-id="36def-3526">5</span><span class="sxs-lookup"><span data-stu-id="36def-3526">5</span></span>

<span data-ttu-id="36def-3527">6</span><span class="sxs-lookup"><span data-stu-id="36def-3527">6</span></span>

<span data-ttu-id="36def-3528">7</span><span class="sxs-lookup"><span data-stu-id="36def-3528">7</span></span>

<span data-ttu-id="36def-3529">8</span><span class="sxs-lookup"><span data-stu-id="36def-3529">8</span></span>

<span data-ttu-id="36def-3530">9</span><span class="sxs-lookup"><span data-stu-id="36def-3530">9</span></span>

<span data-ttu-id="36def-3531">2</span><span class="sxs-lookup"><span data-stu-id="36def-3531">2</span></span><br/> <span data-ttu-id="36def-3532">0</span><span class="sxs-lookup"><span data-stu-id="36def-3532">0</span></span><br/>

<span data-ttu-id="36def-3533">1</span><span class="sxs-lookup"><span data-stu-id="36def-3533">1</span></span>

<span data-ttu-id="36def-3534">2</span><span class="sxs-lookup"><span data-stu-id="36def-3534">2</span></span>

<span data-ttu-id="36def-3535">3</span><span class="sxs-lookup"><span data-stu-id="36def-3535">3</span></span>

<span data-ttu-id="36def-3536">4</span><span class="sxs-lookup"><span data-stu-id="36def-3536">4</span></span>

<span data-ttu-id="36def-3537">5</span><span class="sxs-lookup"><span data-stu-id="36def-3537">5</span></span>

<span data-ttu-id="36def-3538">6</span><span class="sxs-lookup"><span data-stu-id="36def-3538">6</span></span>

<span data-ttu-id="36def-3539">7</span><span class="sxs-lookup"><span data-stu-id="36def-3539">7</span></span>

<span data-ttu-id="36def-3540">8</span><span class="sxs-lookup"><span data-stu-id="36def-3540">8</span></span>

<span data-ttu-id="36def-3541">9</span><span class="sxs-lookup"><span data-stu-id="36def-3541">9</span></span>

<span data-ttu-id="36def-3542">3</span><span class="sxs-lookup"><span data-stu-id="36def-3542">3</span></span><br/> <span data-ttu-id="36def-3543">0</span><span class="sxs-lookup"><span data-stu-id="36def-3543">0</span></span><br/>

<span data-ttu-id="36def-3544">1</span><span class="sxs-lookup"><span data-stu-id="36def-3544">1</span></span>

<span data-ttu-id="36def-3545">\_hCursor (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="36def-3546">\_cbRow (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="36def-3547">\_cbBindingDesc (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="36def-3548">\_虛擬 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-3548">\_dummy (optional)</span></span>

<span data-ttu-id="36def-3549">cColumns (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-3549">cColumns (optional)</span></span>

<span data-ttu-id="36def-3550">aColumns (變數，選擇性) </span><span class="sxs-lookup"><span data-stu-id="36def-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="36def-3551">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，可識別要設定系結的資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="36def-3552">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-3553">**\_ cbRow**：32位不帶正負號的整數，表示資料列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="36def-3554">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-3555">**\_ cbBindingDesc**：32位不帶正負號的整數，表示在虛擬欄位之後的欄位長度（以位元組為單位） \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="36def-3556">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-3557">**\_ 虛擬**：此欄位未使用，必須予以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="36def-3558">可以設定為任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="36def-3559">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-3560">**cColumns**：32位不帶正負號的整數，表示 aColumns 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="36def-3561">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-3562">**aColumns**： CTableColumn 結構的陣列，描述資料列集中資料列的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="36def-3563">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="36def-3564">陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="36def-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="36def-3565">這類填補位元組可以是任意值，而且必須在收到時忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="36def-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="36def-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="36def-3567">CPMGetRowsIn 訊息會要求查詢中的資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="36def-3568">標頭後面的 CPMGetRowsIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3569">0</span><span class="sxs-lookup"><span data-stu-id="36def-3569">0</span></span>

<span data-ttu-id="36def-3570">1</span><span class="sxs-lookup"><span data-stu-id="36def-3570">1</span></span>

<span data-ttu-id="36def-3571">2</span><span class="sxs-lookup"><span data-stu-id="36def-3571">2</span></span>

<span data-ttu-id="36def-3572">3</span><span class="sxs-lookup"><span data-stu-id="36def-3572">3</span></span>

<span data-ttu-id="36def-3573">4</span><span class="sxs-lookup"><span data-stu-id="36def-3573">4</span></span>

<span data-ttu-id="36def-3574">5</span><span class="sxs-lookup"><span data-stu-id="36def-3574">5</span></span>

<span data-ttu-id="36def-3575">6</span><span class="sxs-lookup"><span data-stu-id="36def-3575">6</span></span>

<span data-ttu-id="36def-3576">7</span><span class="sxs-lookup"><span data-stu-id="36def-3576">7</span></span>

<span data-ttu-id="36def-3577">8</span><span class="sxs-lookup"><span data-stu-id="36def-3577">8</span></span>

<span data-ttu-id="36def-3578">9</span><span class="sxs-lookup"><span data-stu-id="36def-3578">9</span></span>

<span data-ttu-id="36def-3579">1</span><span class="sxs-lookup"><span data-stu-id="36def-3579">1</span></span><br/> <span data-ttu-id="36def-3580">0</span><span class="sxs-lookup"><span data-stu-id="36def-3580">0</span></span><br/>

<span data-ttu-id="36def-3581">1</span><span class="sxs-lookup"><span data-stu-id="36def-3581">1</span></span>

<span data-ttu-id="36def-3582">2</span><span class="sxs-lookup"><span data-stu-id="36def-3582">2</span></span>

<span data-ttu-id="36def-3583">3</span><span class="sxs-lookup"><span data-stu-id="36def-3583">3</span></span>

<span data-ttu-id="36def-3584">4</span><span class="sxs-lookup"><span data-stu-id="36def-3584">4</span></span>

<span data-ttu-id="36def-3585">5</span><span class="sxs-lookup"><span data-stu-id="36def-3585">5</span></span>

<span data-ttu-id="36def-3586">6</span><span class="sxs-lookup"><span data-stu-id="36def-3586">6</span></span>

<span data-ttu-id="36def-3587">7</span><span class="sxs-lookup"><span data-stu-id="36def-3587">7</span></span>

<span data-ttu-id="36def-3588">8</span><span class="sxs-lookup"><span data-stu-id="36def-3588">8</span></span>

<span data-ttu-id="36def-3589">9</span><span class="sxs-lookup"><span data-stu-id="36def-3589">9</span></span>

<span data-ttu-id="36def-3590">2</span><span class="sxs-lookup"><span data-stu-id="36def-3590">2</span></span><br/> <span data-ttu-id="36def-3591">0</span><span class="sxs-lookup"><span data-stu-id="36def-3591">0</span></span><br/>

<span data-ttu-id="36def-3592">1</span><span class="sxs-lookup"><span data-stu-id="36def-3592">1</span></span>

<span data-ttu-id="36def-3593">2</span><span class="sxs-lookup"><span data-stu-id="36def-3593">2</span></span>

<span data-ttu-id="36def-3594">3</span><span class="sxs-lookup"><span data-stu-id="36def-3594">3</span></span>

<span data-ttu-id="36def-3595">4</span><span class="sxs-lookup"><span data-stu-id="36def-3595">4</span></span>

<span data-ttu-id="36def-3596">5</span><span class="sxs-lookup"><span data-stu-id="36def-3596">5</span></span>

<span data-ttu-id="36def-3597">6</span><span class="sxs-lookup"><span data-stu-id="36def-3597">6</span></span>

<span data-ttu-id="36def-3598">7</span><span class="sxs-lookup"><span data-stu-id="36def-3598">7</span></span>

<span data-ttu-id="36def-3599">8</span><span class="sxs-lookup"><span data-stu-id="36def-3599">8</span></span>

<span data-ttu-id="36def-3600">9</span><span class="sxs-lookup"><span data-stu-id="36def-3600">9</span></span>

<span data-ttu-id="36def-3601">3</span><span class="sxs-lookup"><span data-stu-id="36def-3601">3</span></span><br/> <span data-ttu-id="36def-3602">0</span><span class="sxs-lookup"><span data-stu-id="36def-3602">0</span></span><br/>

<span data-ttu-id="36def-3603">1</span><span class="sxs-lookup"><span data-stu-id="36def-3603">1</span></span>

<span data-ttu-id="36def-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-3604">\_hCursor</span></span>

<span data-ttu-id="36def-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="36def-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="36def-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="36def-3606">\_cbRowWidth</span></span>

<span data-ttu-id="36def-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="36def-3607">\_cbSeek</span></span>

<span data-ttu-id="36def-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="36def-3608">\_cbReserved</span></span>

<span data-ttu-id="36def-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="36def-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="36def-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="36def-3610">\_ulClientBase</span></span>

<span data-ttu-id="36def-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="36def-3611">\_fBwdFetch</span></span>

<span data-ttu-id="36def-3612">eType</span><span class="sxs-lookup"><span data-stu-id="36def-3612">eType</span></span>

<span data-ttu-id="36def-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="36def-3613">\_chapt</span></span>

<span data-ttu-id="36def-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="36def-3614">SeekDescription</span></span>

<span data-ttu-id="36def-3615">...</span><span class="sxs-lookup"><span data-stu-id="36def-3615">...</span></span>

<span data-ttu-id="36def-3616">... (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3616">... (variable)</span></span>



 

<span data-ttu-id="36def-3617">**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得資料列的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="36def-3618">**\_ cRowsToTransfer**：32位不帶正負號的整數，指出用戶端想要接收以回應此訊息的最大資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="36def-3619">**\_ cbRowWidth**：32位不帶正負號的整數，表示資料列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="36def-3620">**\_ cbSeek**：32位不帶正負號的整數，表示以 eType 開頭的訊息大小。</span><span class="sxs-lookup"><span data-stu-id="36def-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="36def-3621">**\_ cbReserved**：32位不帶正負號的整數，指出 CPMGetRowsOut 訊息的大小（以位元組為單位）， (不含資料列和 SeekDescriptions 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="36def-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="36def-3622">這個欄位中的這個值會加入至 \_ cbSeek 欄位的值，然後用來計算 CPMGetRowsOut 訊息中資料欄欄位的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="36def-3623">**\_ cbReadBuffer**：32位不帶正負號的整數，必須設定為 cRowsToTransfer 的值 \_ cbRowWidth 或1000倍的最大值 \_ ，舍入到最接近的512位元組倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="36def-3624">此值不得超過0x00004000。</span><span class="sxs-lookup"><span data-stu-id="36def-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="36def-3625">**\_ ulClientBase**：32位不帶正負號的整數，表示要用於資料列緩衝區中指標計算的基底值。</span><span class="sxs-lookup"><span data-stu-id="36def-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="36def-3626">如果使用的是64位位移，則會使用訊息標頭的 reserved2 欄位作為上層32位，並使用 \_ ulClientBase 作為64位值的低32位。</span><span class="sxs-lookup"><span data-stu-id="36def-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="36def-3627">如需詳細資訊，請參閱2.2.3.16 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="36def-3628">**\_ fBwdFetch**：32位不帶正負號的整數，表示提取資料列的順序。</span><span class="sxs-lookup"><span data-stu-id="36def-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="36def-3629">如果設定為0x00000001，則會以反向順序提取資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="36def-3630">如果設定為0x00000000，則會以正向順序提取資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="36def-3631">不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="36def-3632">**eType**：32位不帶正負號的整數，其中包含下列其中一個值，表示要執行的作業類型。</span><span class="sxs-lookup"><span data-stu-id="36def-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="36def-3633">值</span><span class="sxs-lookup"><span data-stu-id="36def-3633">Value</span></span>                         | <span data-ttu-id="36def-3634">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="36def-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="36def-3636">SeekDescription 包含 CRowSeekNext 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="36def-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="36def-3638">SeekDescription 包含 CRowSeekAt 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="36def-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="36def-3640">SeekDescription 包含 CRowSeekAtRatio 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="36def-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="36def-3642">SeekDescription 包含 CRowSeekByBookmark 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="36def-3643">**\_ chapt**：代表資料列集章節之控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="36def-3644">**SeekDescription**：這個欄位必須包含 eType 值所指定之類型的結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="36def-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="36def-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="36def-3646">CPMGetRowsOut 訊息會以查詢的資料列回復 CPMGetRowsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="36def-3647">伺服器必須在 [資料列] 欄位中將位移格式化為可變長度資料類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="36def-3648">用戶端表示它是32位系統 (0x00000008 或更少在 CPMConnectIn) 的 iClientVersion 欄位中：位移是32位整數。</span><span class="sxs-lookup"><span data-stu-id="36def-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="36def-3649">用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是32位系統 (\_ serverVersion 設定為0x00000007 中的 CPMConnectOut) ：位移是32位整數</span><span class="sxs-lookup"><span data-stu-id="36def-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="36def-3650">用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是64位系統 (\_ serverVersion 設定為0x00010007 中的 CPMConnectOut) ：位移是64位整數</span><span class="sxs-lookup"><span data-stu-id="36def-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="36def-3651">標頭後面的 CPMGetRowsOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3652">0</span><span class="sxs-lookup"><span data-stu-id="36def-3652">0</span></span>

<span data-ttu-id="36def-3653">1</span><span class="sxs-lookup"><span data-stu-id="36def-3653">1</span></span>

<span data-ttu-id="36def-3654">2</span><span class="sxs-lookup"><span data-stu-id="36def-3654">2</span></span>

<span data-ttu-id="36def-3655">3</span><span class="sxs-lookup"><span data-stu-id="36def-3655">3</span></span>

<span data-ttu-id="36def-3656">4</span><span class="sxs-lookup"><span data-stu-id="36def-3656">4</span></span>

<span data-ttu-id="36def-3657">5</span><span class="sxs-lookup"><span data-stu-id="36def-3657">5</span></span>

<span data-ttu-id="36def-3658">6</span><span class="sxs-lookup"><span data-stu-id="36def-3658">6</span></span>

<span data-ttu-id="36def-3659">7</span><span class="sxs-lookup"><span data-stu-id="36def-3659">7</span></span>

<span data-ttu-id="36def-3660">8</span><span class="sxs-lookup"><span data-stu-id="36def-3660">8</span></span>

<span data-ttu-id="36def-3661">9</span><span class="sxs-lookup"><span data-stu-id="36def-3661">9</span></span>

<span data-ttu-id="36def-3662">1</span><span class="sxs-lookup"><span data-stu-id="36def-3662">1</span></span><br/> <span data-ttu-id="36def-3663">0</span><span class="sxs-lookup"><span data-stu-id="36def-3663">0</span></span><br/>

<span data-ttu-id="36def-3664">1</span><span class="sxs-lookup"><span data-stu-id="36def-3664">1</span></span>

<span data-ttu-id="36def-3665">2</span><span class="sxs-lookup"><span data-stu-id="36def-3665">2</span></span>

<span data-ttu-id="36def-3666">3</span><span class="sxs-lookup"><span data-stu-id="36def-3666">3</span></span>

<span data-ttu-id="36def-3667">4</span><span class="sxs-lookup"><span data-stu-id="36def-3667">4</span></span>

<span data-ttu-id="36def-3668">5</span><span class="sxs-lookup"><span data-stu-id="36def-3668">5</span></span>

<span data-ttu-id="36def-3669">6</span><span class="sxs-lookup"><span data-stu-id="36def-3669">6</span></span>

<span data-ttu-id="36def-3670">7</span><span class="sxs-lookup"><span data-stu-id="36def-3670">7</span></span>

<span data-ttu-id="36def-3671">8</span><span class="sxs-lookup"><span data-stu-id="36def-3671">8</span></span>

<span data-ttu-id="36def-3672">9</span><span class="sxs-lookup"><span data-stu-id="36def-3672">9</span></span>

<span data-ttu-id="36def-3673">2</span><span class="sxs-lookup"><span data-stu-id="36def-3673">2</span></span><br/> <span data-ttu-id="36def-3674">0</span><span class="sxs-lookup"><span data-stu-id="36def-3674">0</span></span><br/>

<span data-ttu-id="36def-3675">1</span><span class="sxs-lookup"><span data-stu-id="36def-3675">1</span></span>

<span data-ttu-id="36def-3676">2</span><span class="sxs-lookup"><span data-stu-id="36def-3676">2</span></span>

<span data-ttu-id="36def-3677">3</span><span class="sxs-lookup"><span data-stu-id="36def-3677">3</span></span>

<span data-ttu-id="36def-3678">4</span><span class="sxs-lookup"><span data-stu-id="36def-3678">4</span></span>

<span data-ttu-id="36def-3679">5</span><span class="sxs-lookup"><span data-stu-id="36def-3679">5</span></span>

<span data-ttu-id="36def-3680">6</span><span class="sxs-lookup"><span data-stu-id="36def-3680">6</span></span>

<span data-ttu-id="36def-3681">7</span><span class="sxs-lookup"><span data-stu-id="36def-3681">7</span></span>

<span data-ttu-id="36def-3682">8</span><span class="sxs-lookup"><span data-stu-id="36def-3682">8</span></span>

<span data-ttu-id="36def-3683">9</span><span class="sxs-lookup"><span data-stu-id="36def-3683">9</span></span>

<span data-ttu-id="36def-3684">3</span><span class="sxs-lookup"><span data-stu-id="36def-3684">3</span></span><br/> <span data-ttu-id="36def-3685">0</span><span class="sxs-lookup"><span data-stu-id="36def-3685">0</span></span><br/>

<span data-ttu-id="36def-3686">1</span><span class="sxs-lookup"><span data-stu-id="36def-3686">1</span></span>

<span data-ttu-id="36def-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="36def-3687">\_cRowsReturned</span></span>

<span data-ttu-id="36def-3688">eType</span><span class="sxs-lookup"><span data-stu-id="36def-3688">eType</span></span>

<span data-ttu-id="36def-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="36def-3689">\_chapt</span></span>

<span data-ttu-id="36def-3690">SeekDescription (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="36def-3691">...</span><span class="sxs-lookup"><span data-stu-id="36def-3691">...</span></span>

<span data-ttu-id="36def-3692">...</span><span class="sxs-lookup"><span data-stu-id="36def-3692">...</span></span>

<span data-ttu-id="36def-3693">paddingRows (選擇性、變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="36def-3694">資料列</span><span class="sxs-lookup"><span data-stu-id="36def-3694">Rows</span></span>



 

<span data-ttu-id="36def-3695">**\_ cRowsReturned**：32位不帶正負號的整數，指出資料列中傳回的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="36def-3696">**eType**：32位不帶正負號的整數，其中包含下列其中一個值，以指出要執行的 rowseek 作業類型</span><span class="sxs-lookup"><span data-stu-id="36def-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="36def-3697">值</span><span class="sxs-lookup"><span data-stu-id="36def-3697">Value</span></span>                         | <span data-ttu-id="36def-3698">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="36def-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="36def-3700">無 SeekDescription，忽略 SeekDescription 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="36def-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="36def-3702">SeekDescription 包含 CRowSeekNext 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="36def-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="36def-3704">SeekDescription 包含 CRowSeekAt 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="36def-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="36def-3706">SeekDescription 包含 CRowSeekAtRatio 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="36def-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="36def-3708">SeekDescription 包含 CRowSeekByBookmark 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="36def-3709">**\_ chapt**：代表資料列集章節之控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="36def-3710">**SeekDescription**：此欄位必須包含 eType 欄位所表示之類型的結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="36def-3711">**paddingRows**：此欄位必須有足夠的長度 (0 到 \_ cbReserved-1 個位元組) 為了將資料欄欄位填補至 \_ 從訊息開頭 cbReserved 的位移，其中 \_ cbReserved 是 CPMGetRowsIn 訊息中的值。</span><span class="sxs-lookup"><span data-stu-id="36def-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="36def-3712">此欄位中使用的填補位元組可以是任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="36def-3713">接收者必須忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="36def-3714">資料列：資料列資料的格式設定為最近 CPMSetBindingsIn 訊息中的 **資料行資訊**。</span><span class="sxs-lookup"><span data-stu-id="36def-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="36def-3715">資料列必須以轉寄順序儲存 (例如，資料列2之前的資料列 1) 。</span><span class="sxs-lookup"><span data-stu-id="36def-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="36def-3716">固定大小的資料行必須儲存在最新 CPMSetBindingsIn 訊息所指定的位移上。</span><span class="sxs-lookup"><span data-stu-id="36def-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="36def-3717">可變大小的資料行 (例如，字串) 必須依照下列方式儲存：</span><span class="sxs-lookup"><span data-stu-id="36def-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="36def-3718">變數資料本身 (例如，字串) 會以遞減 (順序儲存在緩衝區結尾，例如，資料列1的所有變數資料的集合在結尾、第2列最接近的位置，) 依此類推。</span><span class="sxs-lookup"><span data-stu-id="36def-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="36def-3719">在資料列緩衝區開頭的固定大社區域 (，) 必須包含每個資料行的 CRowVariant，這些資料行會儲存在最新 CPMSetBindingsIn 訊息中指定的位移。</span><span class="sxs-lookup"><span data-stu-id="36def-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="36def-3720">vType 必須包含資料類型 (例如： VT \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="36def-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="36def-3721">若為，則在使用32位位移時，CRowVariant 中的位移欄位必須包含32位值，這是從 CPMGetRowsOut 訊息的開頭算起的變數資料位移，加上 \_ 最新 CPMGetRowsIn 訊息中指定的 ulClientBase 的值。</span><span class="sxs-lookup"><span data-stu-id="36def-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="36def-3722">如果使用的是64位位移，則 CRowVariant 中的位移欄位必須包含64位值，該值是 CPMGetRowsOut 訊息開頭的位移，並新增至使用 \_ ulClientBase 做為低32位和 \_ ulReserved2 為高32位所組成的64位值。</span><span class="sxs-lookup"><span data-stu-id="36def-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="36def-3723">例如，如果 CPMSetBindingsIn 訊息指定了兩個數據行大小 (VT \_ I4) 和 Title (vt \_ LPWSTR) -and \_ ulClientBase from CPMGetRowsIn was 0x10000，則兩個數據列會如下所示。</span><span class="sxs-lookup"><span data-stu-id="36def-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="36def-3724">以灰色標示的區段是緩衝區的固定長度部分。</span><span class="sxs-lookup"><span data-stu-id="36def-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![cpmsetbindingsin 訊息範例](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="36def-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="36def-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="36def-3727">CPMRatioFinishedIn 訊息會要求查詢的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="36def-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="36def-3728">標頭後面的 CPMRatioFinishedIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3729">0</span><span class="sxs-lookup"><span data-stu-id="36def-3729">0</span></span>

<span data-ttu-id="36def-3730">1</span><span class="sxs-lookup"><span data-stu-id="36def-3730">1</span></span>

<span data-ttu-id="36def-3731">2</span><span class="sxs-lookup"><span data-stu-id="36def-3731">2</span></span>

<span data-ttu-id="36def-3732">3</span><span class="sxs-lookup"><span data-stu-id="36def-3732">3</span></span>

<span data-ttu-id="36def-3733">4</span><span class="sxs-lookup"><span data-stu-id="36def-3733">4</span></span>

<span data-ttu-id="36def-3734">5</span><span class="sxs-lookup"><span data-stu-id="36def-3734">5</span></span>

<span data-ttu-id="36def-3735">6</span><span class="sxs-lookup"><span data-stu-id="36def-3735">6</span></span>

<span data-ttu-id="36def-3736">7</span><span class="sxs-lookup"><span data-stu-id="36def-3736">7</span></span>

<span data-ttu-id="36def-3737">8</span><span class="sxs-lookup"><span data-stu-id="36def-3737">8</span></span>

<span data-ttu-id="36def-3738">9</span><span class="sxs-lookup"><span data-stu-id="36def-3738">9</span></span>

<span data-ttu-id="36def-3739">1</span><span class="sxs-lookup"><span data-stu-id="36def-3739">1</span></span><br/> <span data-ttu-id="36def-3740">0</span><span class="sxs-lookup"><span data-stu-id="36def-3740">0</span></span><br/>

<span data-ttu-id="36def-3741">1</span><span class="sxs-lookup"><span data-stu-id="36def-3741">1</span></span>

<span data-ttu-id="36def-3742">2</span><span class="sxs-lookup"><span data-stu-id="36def-3742">2</span></span>

<span data-ttu-id="36def-3743">3</span><span class="sxs-lookup"><span data-stu-id="36def-3743">3</span></span>

<span data-ttu-id="36def-3744">4</span><span class="sxs-lookup"><span data-stu-id="36def-3744">4</span></span>

<span data-ttu-id="36def-3745">5</span><span class="sxs-lookup"><span data-stu-id="36def-3745">5</span></span>

<span data-ttu-id="36def-3746">6</span><span class="sxs-lookup"><span data-stu-id="36def-3746">6</span></span>

<span data-ttu-id="36def-3747">7</span><span class="sxs-lookup"><span data-stu-id="36def-3747">7</span></span>

<span data-ttu-id="36def-3748">8</span><span class="sxs-lookup"><span data-stu-id="36def-3748">8</span></span>

<span data-ttu-id="36def-3749">9</span><span class="sxs-lookup"><span data-stu-id="36def-3749">9</span></span>

<span data-ttu-id="36def-3750">2</span><span class="sxs-lookup"><span data-stu-id="36def-3750">2</span></span><br/> <span data-ttu-id="36def-3751">0</span><span class="sxs-lookup"><span data-stu-id="36def-3751">0</span></span><br/>

<span data-ttu-id="36def-3752">1</span><span class="sxs-lookup"><span data-stu-id="36def-3752">1</span></span>

<span data-ttu-id="36def-3753">2</span><span class="sxs-lookup"><span data-stu-id="36def-3753">2</span></span>

<span data-ttu-id="36def-3754">3</span><span class="sxs-lookup"><span data-stu-id="36def-3754">3</span></span>

<span data-ttu-id="36def-3755">4</span><span class="sxs-lookup"><span data-stu-id="36def-3755">4</span></span>

<span data-ttu-id="36def-3756">5</span><span class="sxs-lookup"><span data-stu-id="36def-3756">5</span></span>

<span data-ttu-id="36def-3757">6</span><span class="sxs-lookup"><span data-stu-id="36def-3757">6</span></span>

<span data-ttu-id="36def-3758">7</span><span class="sxs-lookup"><span data-stu-id="36def-3758">7</span></span>

<span data-ttu-id="36def-3759">8</span><span class="sxs-lookup"><span data-stu-id="36def-3759">8</span></span>

<span data-ttu-id="36def-3760">9</span><span class="sxs-lookup"><span data-stu-id="36def-3760">9</span></span>

<span data-ttu-id="36def-3761">3</span><span class="sxs-lookup"><span data-stu-id="36def-3761">3</span></span><br/> <span data-ttu-id="36def-3762">0</span><span class="sxs-lookup"><span data-stu-id="36def-3762">0</span></span><br/>

<span data-ttu-id="36def-3763">1</span><span class="sxs-lookup"><span data-stu-id="36def-3763">1</span></span>

<span data-ttu-id="36def-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-3764">\_hCursor</span></span>

<span data-ttu-id="36def-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="36def-3765">\_fQuick</span></span>



 

<span data-ttu-id="36def-3766">**\_ HCursor**： CPMCreateQueryOut 訊息的控制碼，識別要要求完成資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="36def-3767">**\_ fQuick**：必須設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="36def-3768">如果未使用，則伺服器必須加以忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="36def-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="36def-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="36def-3770">CPMRatioFinishedOut 訊息會以查詢的完成率回復 CPMRatioFinishedIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="36def-3771">標頭後面的 CPMRatioFinishedOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3772">0</span><span class="sxs-lookup"><span data-stu-id="36def-3772">0</span></span>

<span data-ttu-id="36def-3773">1</span><span class="sxs-lookup"><span data-stu-id="36def-3773">1</span></span>

<span data-ttu-id="36def-3774">2</span><span class="sxs-lookup"><span data-stu-id="36def-3774">2</span></span>

<span data-ttu-id="36def-3775">3</span><span class="sxs-lookup"><span data-stu-id="36def-3775">3</span></span>

<span data-ttu-id="36def-3776">4</span><span class="sxs-lookup"><span data-stu-id="36def-3776">4</span></span>

<span data-ttu-id="36def-3777">5</span><span class="sxs-lookup"><span data-stu-id="36def-3777">5</span></span>

<span data-ttu-id="36def-3778">6</span><span class="sxs-lookup"><span data-stu-id="36def-3778">6</span></span>

<span data-ttu-id="36def-3779">7</span><span class="sxs-lookup"><span data-stu-id="36def-3779">7</span></span>

<span data-ttu-id="36def-3780">8</span><span class="sxs-lookup"><span data-stu-id="36def-3780">8</span></span>

<span data-ttu-id="36def-3781">9</span><span class="sxs-lookup"><span data-stu-id="36def-3781">9</span></span>

<span data-ttu-id="36def-3782">1</span><span class="sxs-lookup"><span data-stu-id="36def-3782">1</span></span><br/> <span data-ttu-id="36def-3783">0</span><span class="sxs-lookup"><span data-stu-id="36def-3783">0</span></span><br/>

<span data-ttu-id="36def-3784">1</span><span class="sxs-lookup"><span data-stu-id="36def-3784">1</span></span>

<span data-ttu-id="36def-3785">2</span><span class="sxs-lookup"><span data-stu-id="36def-3785">2</span></span>

<span data-ttu-id="36def-3786">3</span><span class="sxs-lookup"><span data-stu-id="36def-3786">3</span></span>

<span data-ttu-id="36def-3787">4</span><span class="sxs-lookup"><span data-stu-id="36def-3787">4</span></span>

<span data-ttu-id="36def-3788">5</span><span class="sxs-lookup"><span data-stu-id="36def-3788">5</span></span>

<span data-ttu-id="36def-3789">6</span><span class="sxs-lookup"><span data-stu-id="36def-3789">6</span></span>

<span data-ttu-id="36def-3790">7</span><span class="sxs-lookup"><span data-stu-id="36def-3790">7</span></span>

<span data-ttu-id="36def-3791">8</span><span class="sxs-lookup"><span data-stu-id="36def-3791">8</span></span>

<span data-ttu-id="36def-3792">9</span><span class="sxs-lookup"><span data-stu-id="36def-3792">9</span></span>

<span data-ttu-id="36def-3793">2</span><span class="sxs-lookup"><span data-stu-id="36def-3793">2</span></span><br/> <span data-ttu-id="36def-3794">0</span><span class="sxs-lookup"><span data-stu-id="36def-3794">0</span></span><br/>

<span data-ttu-id="36def-3795">1</span><span class="sxs-lookup"><span data-stu-id="36def-3795">1</span></span>

<span data-ttu-id="36def-3796">2</span><span class="sxs-lookup"><span data-stu-id="36def-3796">2</span></span>

<span data-ttu-id="36def-3797">3</span><span class="sxs-lookup"><span data-stu-id="36def-3797">3</span></span>

<span data-ttu-id="36def-3798">4</span><span class="sxs-lookup"><span data-stu-id="36def-3798">4</span></span>

<span data-ttu-id="36def-3799">5</span><span class="sxs-lookup"><span data-stu-id="36def-3799">5</span></span>

<span data-ttu-id="36def-3800">6</span><span class="sxs-lookup"><span data-stu-id="36def-3800">6</span></span>

<span data-ttu-id="36def-3801">7</span><span class="sxs-lookup"><span data-stu-id="36def-3801">7</span></span>

<span data-ttu-id="36def-3802">8</span><span class="sxs-lookup"><span data-stu-id="36def-3802">8</span></span>

<span data-ttu-id="36def-3803">9</span><span class="sxs-lookup"><span data-stu-id="36def-3803">9</span></span>

<span data-ttu-id="36def-3804">3</span><span class="sxs-lookup"><span data-stu-id="36def-3804">3</span></span><br/> <span data-ttu-id="36def-3805">0</span><span class="sxs-lookup"><span data-stu-id="36def-3805">0</span></span><br/>

<span data-ttu-id="36def-3806">1</span><span class="sxs-lookup"><span data-stu-id="36def-3806">1</span></span>

<span data-ttu-id="36def-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="36def-3807">\_ ulNumerator</span></span>

<span data-ttu-id="36def-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="36def-3808">\_ulDenominator</span></span>

<span data-ttu-id="36def-3809">\_烏鴉</span><span class="sxs-lookup"><span data-stu-id="36def-3809">\_cRows</span></span>

<span data-ttu-id="36def-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="36def-3810">\_fNewRows</span></span>



 

<span data-ttu-id="36def-3811">**\_ ulNumerator**：32位不帶正負號的整數，指出完成比率的分子（以資料列數為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="36def-3812">**\_ ulDenominator**：32位不帶正負號整數，指出完成比率的分母（以資料列為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="36def-3813">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="36def-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="36def-3814">**\_ >crows**：32位不帶正負號的整數，指出查詢的資料列總數。</span><span class="sxs-lookup"><span data-stu-id="36def-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="36def-3815">**\_ fNewRows**：布林值，指出是否有新的資料列可用。</span><span class="sxs-lookup"><span data-stu-id="36def-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="36def-3816">值為0x00000001 表示資料列集內有新的資料列可用。</span><span class="sxs-lookup"><span data-stu-id="36def-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="36def-3817">值為0x00000000 表示資料列集不包含任何新的資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="36def-3818">這個欄位不得設定為任何其他值。</span><span class="sxs-lookup"><span data-stu-id="36def-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="36def-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="36def-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="36def-3820">CPMFetchValueIn 訊息要求的屬性值太大而無法在資料列集中傳回。</span><span class="sxs-lookup"><span data-stu-id="36def-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="36def-3821">如3.2.4.2.5 一節中所指定，此訊息會重複傳送以抓取屬性的所有位元組，並為 \_ 每個位元組更新 cbSoFar，直到 \_ CPMFetchValueOut 訊息的 fMoreExists 欄位設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="36def-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="36def-3822">標頭後面的 CPMFetchValueIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3823">0</span><span class="sxs-lookup"><span data-stu-id="36def-3823">0</span></span>

<span data-ttu-id="36def-3824">1</span><span class="sxs-lookup"><span data-stu-id="36def-3824">1</span></span>

<span data-ttu-id="36def-3825">2</span><span class="sxs-lookup"><span data-stu-id="36def-3825">2</span></span>

<span data-ttu-id="36def-3826">3</span><span class="sxs-lookup"><span data-stu-id="36def-3826">3</span></span>

<span data-ttu-id="36def-3827">4</span><span class="sxs-lookup"><span data-stu-id="36def-3827">4</span></span>

<span data-ttu-id="36def-3828">5</span><span class="sxs-lookup"><span data-stu-id="36def-3828">5</span></span>

<span data-ttu-id="36def-3829">6</span><span class="sxs-lookup"><span data-stu-id="36def-3829">6</span></span>

<span data-ttu-id="36def-3830">7</span><span class="sxs-lookup"><span data-stu-id="36def-3830">7</span></span>

<span data-ttu-id="36def-3831">8</span><span class="sxs-lookup"><span data-stu-id="36def-3831">8</span></span>

<span data-ttu-id="36def-3832">9</span><span class="sxs-lookup"><span data-stu-id="36def-3832">9</span></span>

<span data-ttu-id="36def-3833">1</span><span class="sxs-lookup"><span data-stu-id="36def-3833">1</span></span><br/> <span data-ttu-id="36def-3834">0</span><span class="sxs-lookup"><span data-stu-id="36def-3834">0</span></span><br/>

<span data-ttu-id="36def-3835">1</span><span class="sxs-lookup"><span data-stu-id="36def-3835">1</span></span>

<span data-ttu-id="36def-3836">2</span><span class="sxs-lookup"><span data-stu-id="36def-3836">2</span></span>

<span data-ttu-id="36def-3837">3</span><span class="sxs-lookup"><span data-stu-id="36def-3837">3</span></span>

<span data-ttu-id="36def-3838">4</span><span class="sxs-lookup"><span data-stu-id="36def-3838">4</span></span>

<span data-ttu-id="36def-3839">5</span><span class="sxs-lookup"><span data-stu-id="36def-3839">5</span></span>

<span data-ttu-id="36def-3840">6</span><span class="sxs-lookup"><span data-stu-id="36def-3840">6</span></span>

<span data-ttu-id="36def-3841">7</span><span class="sxs-lookup"><span data-stu-id="36def-3841">7</span></span>

<span data-ttu-id="36def-3842">8</span><span class="sxs-lookup"><span data-stu-id="36def-3842">8</span></span>

<span data-ttu-id="36def-3843">9</span><span class="sxs-lookup"><span data-stu-id="36def-3843">9</span></span>

<span data-ttu-id="36def-3844">2</span><span class="sxs-lookup"><span data-stu-id="36def-3844">2</span></span><br/> <span data-ttu-id="36def-3845">0</span><span class="sxs-lookup"><span data-stu-id="36def-3845">0</span></span><br/>

<span data-ttu-id="36def-3846">1</span><span class="sxs-lookup"><span data-stu-id="36def-3846">1</span></span>

<span data-ttu-id="36def-3847">2</span><span class="sxs-lookup"><span data-stu-id="36def-3847">2</span></span>

<span data-ttu-id="36def-3848">3</span><span class="sxs-lookup"><span data-stu-id="36def-3848">3</span></span>

<span data-ttu-id="36def-3849">4</span><span class="sxs-lookup"><span data-stu-id="36def-3849">4</span></span>

<span data-ttu-id="36def-3850">5</span><span class="sxs-lookup"><span data-stu-id="36def-3850">5</span></span>

<span data-ttu-id="36def-3851">6</span><span class="sxs-lookup"><span data-stu-id="36def-3851">6</span></span>

<span data-ttu-id="36def-3852">7</span><span class="sxs-lookup"><span data-stu-id="36def-3852">7</span></span>

<span data-ttu-id="36def-3853">8</span><span class="sxs-lookup"><span data-stu-id="36def-3853">8</span></span>

<span data-ttu-id="36def-3854">9</span><span class="sxs-lookup"><span data-stu-id="36def-3854">9</span></span>

<span data-ttu-id="36def-3855">3</span><span class="sxs-lookup"><span data-stu-id="36def-3855">3</span></span><br/> <span data-ttu-id="36def-3856">0</span><span class="sxs-lookup"><span data-stu-id="36def-3856">0</span></span><br/>

<span data-ttu-id="36def-3857">1</span><span class="sxs-lookup"><span data-stu-id="36def-3857">1</span></span>

<span data-ttu-id="36def-3858">\_Wid</span><span class="sxs-lookup"><span data-stu-id="36def-3858">\_wid</span></span>

<span data-ttu-id="36def-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="36def-3859">\_cbSoFar</span></span>

<span data-ttu-id="36def-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="36def-3860">\_cbPropSpec</span></span>

<span data-ttu-id="36def-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="36def-3861">\_cbChunk</span></span>

<span data-ttu-id="36def-3862">PropSpec (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3862">PropSpec (variable)</span></span>

<span data-ttu-id="36def-3863">...</span><span class="sxs-lookup"><span data-stu-id="36def-3863">...</span></span>

<span data-ttu-id="36def-3864">\_填補 (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="36def-3865">**\_ wid**：代表檔識別碼的32位不帶正負號整數，該檔識別碼可識別應提取屬性的檔。</span><span class="sxs-lookup"><span data-stu-id="36def-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="36def-3866">**\_ cbSoFar**：32位不帶正負號的整數，其中包含先前針對此屬性傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="36def-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="36def-3867">在第一則訊息中必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="36def-3868">**\_ cbPropSpec**：32位不帶正負號的整數，其中包含 PropSpec 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="36def-3869">**\_ cbChunk**：32位不帶正負號的整數，其中包含傳送者可在 CPMFetchValueOut 訊息中接受的位元組數目上限。</span><span class="sxs-lookup"><span data-stu-id="36def-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="36def-3870">*Windows 行為：此欄位會設定為所有 Windows 版本的0x00004000。*</span><span class="sxs-lookup"><span data-stu-id="36def-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="36def-3871">**PropSpec**：指定要取得之屬性的 CFullPropSpec 結構。</span><span class="sxs-lookup"><span data-stu-id="36def-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="36def-3872">**\_ 填補**：此欄位必須是必要的長度 (0 至3個位元組) 將訊息填補至4個位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="36def-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="36def-3873">填補位元組的值可以是任意值。</span><span class="sxs-lookup"><span data-stu-id="36def-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="36def-3874">接收者必須忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="36def-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="36def-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="36def-3876">CPMFetchValueOut 訊息會使用前一個查詢的屬性值回復 CPMFetchValueIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="36def-3877">如3.1.5.2.8 一節中所指定，此訊息會在每個 CPMFetchValueIn 訊息之後傳送，直到屬性的所有位元組都經過傳送為止。</span><span class="sxs-lookup"><span data-stu-id="36def-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="36def-3878">標頭後面的 CPMFetchValueOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3879">0</span><span class="sxs-lookup"><span data-stu-id="36def-3879">0</span></span>

<span data-ttu-id="36def-3880">1</span><span class="sxs-lookup"><span data-stu-id="36def-3880">1</span></span>

<span data-ttu-id="36def-3881">2</span><span class="sxs-lookup"><span data-stu-id="36def-3881">2</span></span>

<span data-ttu-id="36def-3882">3</span><span class="sxs-lookup"><span data-stu-id="36def-3882">3</span></span>

<span data-ttu-id="36def-3883">4</span><span class="sxs-lookup"><span data-stu-id="36def-3883">4</span></span>

<span data-ttu-id="36def-3884">5</span><span class="sxs-lookup"><span data-stu-id="36def-3884">5</span></span>

<span data-ttu-id="36def-3885">6</span><span class="sxs-lookup"><span data-stu-id="36def-3885">6</span></span>

<span data-ttu-id="36def-3886">7</span><span class="sxs-lookup"><span data-stu-id="36def-3886">7</span></span>

<span data-ttu-id="36def-3887">8</span><span class="sxs-lookup"><span data-stu-id="36def-3887">8</span></span>

<span data-ttu-id="36def-3888">9</span><span class="sxs-lookup"><span data-stu-id="36def-3888">9</span></span>

<span data-ttu-id="36def-3889">1</span><span class="sxs-lookup"><span data-stu-id="36def-3889">1</span></span><br/> <span data-ttu-id="36def-3890">0</span><span class="sxs-lookup"><span data-stu-id="36def-3890">0</span></span><br/>

<span data-ttu-id="36def-3891">1</span><span class="sxs-lookup"><span data-stu-id="36def-3891">1</span></span>

<span data-ttu-id="36def-3892">2</span><span class="sxs-lookup"><span data-stu-id="36def-3892">2</span></span>

<span data-ttu-id="36def-3893">3</span><span class="sxs-lookup"><span data-stu-id="36def-3893">3</span></span>

<span data-ttu-id="36def-3894">4</span><span class="sxs-lookup"><span data-stu-id="36def-3894">4</span></span>

<span data-ttu-id="36def-3895">5</span><span class="sxs-lookup"><span data-stu-id="36def-3895">5</span></span>

<span data-ttu-id="36def-3896">6</span><span class="sxs-lookup"><span data-stu-id="36def-3896">6</span></span>

<span data-ttu-id="36def-3897">7</span><span class="sxs-lookup"><span data-stu-id="36def-3897">7</span></span>

<span data-ttu-id="36def-3898">8</span><span class="sxs-lookup"><span data-stu-id="36def-3898">8</span></span>

<span data-ttu-id="36def-3899">9</span><span class="sxs-lookup"><span data-stu-id="36def-3899">9</span></span>

<span data-ttu-id="36def-3900">2</span><span class="sxs-lookup"><span data-stu-id="36def-3900">2</span></span><br/> <span data-ttu-id="36def-3901">0</span><span class="sxs-lookup"><span data-stu-id="36def-3901">0</span></span><br/>

<span data-ttu-id="36def-3902">1</span><span class="sxs-lookup"><span data-stu-id="36def-3902">1</span></span>

<span data-ttu-id="36def-3903">2</span><span class="sxs-lookup"><span data-stu-id="36def-3903">2</span></span>

<span data-ttu-id="36def-3904">3</span><span class="sxs-lookup"><span data-stu-id="36def-3904">3</span></span>

<span data-ttu-id="36def-3905">4</span><span class="sxs-lookup"><span data-stu-id="36def-3905">4</span></span>

<span data-ttu-id="36def-3906">5</span><span class="sxs-lookup"><span data-stu-id="36def-3906">5</span></span>

<span data-ttu-id="36def-3907">6</span><span class="sxs-lookup"><span data-stu-id="36def-3907">6</span></span>

<span data-ttu-id="36def-3908">7</span><span class="sxs-lookup"><span data-stu-id="36def-3908">7</span></span>

<span data-ttu-id="36def-3909">8</span><span class="sxs-lookup"><span data-stu-id="36def-3909">8</span></span>

<span data-ttu-id="36def-3910">9</span><span class="sxs-lookup"><span data-stu-id="36def-3910">9</span></span>

<span data-ttu-id="36def-3911">3</span><span class="sxs-lookup"><span data-stu-id="36def-3911">3</span></span><br/> <span data-ttu-id="36def-3912">0</span><span class="sxs-lookup"><span data-stu-id="36def-3912">0</span></span><br/>

<span data-ttu-id="36def-3913">1</span><span class="sxs-lookup"><span data-stu-id="36def-3913">1</span></span>

<span data-ttu-id="36def-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="36def-3914">\_cbValue</span></span>

<span data-ttu-id="36def-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="36def-3915">\_fMoreExists</span></span>

<span data-ttu-id="36def-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="36def-3916">\_fValueExists</span></span>

<span data-ttu-id="36def-3917">vType</span><span class="sxs-lookup"><span data-stu-id="36def-3917">vType</span></span>

<span data-ttu-id="36def-3918">vValue (變數) </span><span class="sxs-lookup"><span data-stu-id="36def-3918">vValue (variable)</span></span>



 

<span data-ttu-id="36def-3919">**\_ cbValue**：32位不帶正負號的整數，其中包含總大小（以位元組為單位） vValue。</span><span class="sxs-lookup"><span data-stu-id="36def-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="36def-3920">**\_ fMoreExists**：布林值，指出是否有其他可用的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="36def-3921">如果設定為0x00000001，則會有額外的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="36def-3922">如果設定為0x00000000，則沒有其他可用的 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="36def-3923">**\_ fValueExists**：布林值，指出屬性是否有值。</span><span class="sxs-lookup"><span data-stu-id="36def-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="36def-3924">如果設定為0x00000001，屬性的值就會存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="36def-3925">如果設定為0x00000000，則屬性的值不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="36def-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span><span class="sxs-lookup"><span data-stu-id="36def-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="36def-3927">**vValue**：位元組陣列的一部分，其中包含2.2.1.32 區段中指定的 SERIALIZEDPROPERTYVALUE 結構，其中部分開頭的位移是 \_ CPMFetchValueIn 中 cbSoFar 的值。</span><span class="sxs-lookup"><span data-stu-id="36def-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="36def-3928">\_如果 fMoreExists 設定為0x00000001，部分的長度（以 cbValue 欄位表示）必須等於 \_ CPMFetchValueIn 中 cbChunk 的值， \_ 否則必須小於或等於 cbChunk 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="36def-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="36def-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="36def-3930">CPMGetNotify 訊息會要求用戶端想要收到資料列集變更的通知。</span><span class="sxs-lookup"><span data-stu-id="36def-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="36def-3931">訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。</span><span class="sxs-lookup"><span data-stu-id="36def-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="36def-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="36def-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="36def-3933">CPMSendNotifyOut 訊息會通知用戶端查詢結果的變更。</span><span class="sxs-lookup"><span data-stu-id="36def-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="36def-3934">只有在發生變更時，才會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="36def-3935">標頭後面的 CPMSendNotifyOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="36def-3936">0</span><span class="sxs-lookup"><span data-stu-id="36def-3936">0</span></span>

<span data-ttu-id="36def-3937">1</span><span class="sxs-lookup"><span data-stu-id="36def-3937">1</span></span>

<span data-ttu-id="36def-3938">2</span><span class="sxs-lookup"><span data-stu-id="36def-3938">2</span></span>

<span data-ttu-id="36def-3939">3</span><span class="sxs-lookup"><span data-stu-id="36def-3939">3</span></span>

<span data-ttu-id="36def-3940">4</span><span class="sxs-lookup"><span data-stu-id="36def-3940">4</span></span>

<span data-ttu-id="36def-3941">5</span><span class="sxs-lookup"><span data-stu-id="36def-3941">5</span></span>

<span data-ttu-id="36def-3942">6</span><span class="sxs-lookup"><span data-stu-id="36def-3942">6</span></span>

<span data-ttu-id="36def-3943">7</span><span class="sxs-lookup"><span data-stu-id="36def-3943">7</span></span>

<span data-ttu-id="36def-3944">8</span><span class="sxs-lookup"><span data-stu-id="36def-3944">8</span></span>

<span data-ttu-id="36def-3945">9</span><span class="sxs-lookup"><span data-stu-id="36def-3945">9</span></span>

<span data-ttu-id="36def-3946">1</span><span class="sxs-lookup"><span data-stu-id="36def-3946">1</span></span><br/> <span data-ttu-id="36def-3947">0</span><span class="sxs-lookup"><span data-stu-id="36def-3947">0</span></span><br/>

<span data-ttu-id="36def-3948">1</span><span class="sxs-lookup"><span data-stu-id="36def-3948">1</span></span>

<span data-ttu-id="36def-3949">2</span><span class="sxs-lookup"><span data-stu-id="36def-3949">2</span></span>

<span data-ttu-id="36def-3950">3</span><span class="sxs-lookup"><span data-stu-id="36def-3950">3</span></span>

<span data-ttu-id="36def-3951">4</span><span class="sxs-lookup"><span data-stu-id="36def-3951">4</span></span>

<span data-ttu-id="36def-3952">5</span><span class="sxs-lookup"><span data-stu-id="36def-3952">5</span></span>

<span data-ttu-id="36def-3953">6</span><span class="sxs-lookup"><span data-stu-id="36def-3953">6</span></span>

<span data-ttu-id="36def-3954">7</span><span class="sxs-lookup"><span data-stu-id="36def-3954">7</span></span>

<span data-ttu-id="36def-3955">8</span><span class="sxs-lookup"><span data-stu-id="36def-3955">8</span></span>

<span data-ttu-id="36def-3956">9</span><span class="sxs-lookup"><span data-stu-id="36def-3956">9</span></span>

<span data-ttu-id="36def-3957">2</span><span class="sxs-lookup"><span data-stu-id="36def-3957">2</span></span><br/> <span data-ttu-id="36def-3958">0</span><span class="sxs-lookup"><span data-stu-id="36def-3958">0</span></span><br/>

<span data-ttu-id="36def-3959">1</span><span class="sxs-lookup"><span data-stu-id="36def-3959">1</span></span>

<span data-ttu-id="36def-3960">2</span><span class="sxs-lookup"><span data-stu-id="36def-3960">2</span></span>

<span data-ttu-id="36def-3961">3</span><span class="sxs-lookup"><span data-stu-id="36def-3961">3</span></span>

<span data-ttu-id="36def-3962">4</span><span class="sxs-lookup"><span data-stu-id="36def-3962">4</span></span>

<span data-ttu-id="36def-3963">5</span><span class="sxs-lookup"><span data-stu-id="36def-3963">5</span></span>

<span data-ttu-id="36def-3964">6</span><span class="sxs-lookup"><span data-stu-id="36def-3964">6</span></span>

<span data-ttu-id="36def-3965">7</span><span class="sxs-lookup"><span data-stu-id="36def-3965">7</span></span>

<span data-ttu-id="36def-3966">8</span><span class="sxs-lookup"><span data-stu-id="36def-3966">8</span></span>

<span data-ttu-id="36def-3967">9</span><span class="sxs-lookup"><span data-stu-id="36def-3967">9</span></span>

<span data-ttu-id="36def-3968">3</span><span class="sxs-lookup"><span data-stu-id="36def-3968">3</span></span><br/> <span data-ttu-id="36def-3969">0</span><span class="sxs-lookup"><span data-stu-id="36def-3969">0</span></span><br/>

<span data-ttu-id="36def-3970">1</span><span class="sxs-lookup"><span data-stu-id="36def-3970">1</span></span>

<span data-ttu-id="36def-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="36def-3971">\_watchNotify</span></span>



 

<span data-ttu-id="36def-3972">**\_ watchNotify**：對查詢的變更。</span><span class="sxs-lookup"><span data-stu-id="36def-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="36def-3973">它必須是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="36def-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="36def-3974">值</span><span class="sxs-lookup"><span data-stu-id="36def-3974">Value</span></span>                                     | <span data-ttu-id="36def-3975">意義</span><span class="sxs-lookup"><span data-stu-id="36def-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="36def-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="36def-3977">查詢資料列集中的資料列數目已變更。</span><span class="sxs-lookup"><span data-stu-id="36def-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="36def-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="36def-3979">查詢已完成。</span><span class="sxs-lookup"><span data-stu-id="36def-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="36def-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="36def-3981">已重新執行查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="36def-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="36def-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="36def-3983">CPMGetApproximatePositionIn 訊息會要求某一章中書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="36def-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="36def-3984">標頭後面的 CPMGetApproximatePositionIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="36def-3985">0</span><span class="sxs-lookup"><span data-stu-id="36def-3985">0</span></span>

<span data-ttu-id="36def-3986">1</span><span class="sxs-lookup"><span data-stu-id="36def-3986">1</span></span>

<span data-ttu-id="36def-3987">2</span><span class="sxs-lookup"><span data-stu-id="36def-3987">2</span></span>

<span data-ttu-id="36def-3988">3</span><span class="sxs-lookup"><span data-stu-id="36def-3988">3</span></span>

<span data-ttu-id="36def-3989">4</span><span class="sxs-lookup"><span data-stu-id="36def-3989">4</span></span>

<span data-ttu-id="36def-3990">5</span><span class="sxs-lookup"><span data-stu-id="36def-3990">5</span></span>

<span data-ttu-id="36def-3991">6</span><span class="sxs-lookup"><span data-stu-id="36def-3991">6</span></span>

<span data-ttu-id="36def-3992">7</span><span class="sxs-lookup"><span data-stu-id="36def-3992">7</span></span>

<span data-ttu-id="36def-3993">8</span><span class="sxs-lookup"><span data-stu-id="36def-3993">8</span></span>

<span data-ttu-id="36def-3994">9</span><span class="sxs-lookup"><span data-stu-id="36def-3994">9</span></span>

<span data-ttu-id="36def-3995">1</span><span class="sxs-lookup"><span data-stu-id="36def-3995">1</span></span><br/> <span data-ttu-id="36def-3996">0</span><span class="sxs-lookup"><span data-stu-id="36def-3996">0</span></span><br/>

<span data-ttu-id="36def-3997">1</span><span class="sxs-lookup"><span data-stu-id="36def-3997">1</span></span>

<span data-ttu-id="36def-3998">2</span><span class="sxs-lookup"><span data-stu-id="36def-3998">2</span></span>

<span data-ttu-id="36def-3999">3</span><span class="sxs-lookup"><span data-stu-id="36def-3999">3</span></span>

<span data-ttu-id="36def-4000">4</span><span class="sxs-lookup"><span data-stu-id="36def-4000">4</span></span>

<span data-ttu-id="36def-4001">5</span><span class="sxs-lookup"><span data-stu-id="36def-4001">5</span></span>

<span data-ttu-id="36def-4002">6</span><span class="sxs-lookup"><span data-stu-id="36def-4002">6</span></span>

<span data-ttu-id="36def-4003">7</span><span class="sxs-lookup"><span data-stu-id="36def-4003">7</span></span>

<span data-ttu-id="36def-4004">8</span><span class="sxs-lookup"><span data-stu-id="36def-4004">8</span></span>

<span data-ttu-id="36def-4005">9</span><span class="sxs-lookup"><span data-stu-id="36def-4005">9</span></span>

<span data-ttu-id="36def-4006">2</span><span class="sxs-lookup"><span data-stu-id="36def-4006">2</span></span><br/> <span data-ttu-id="36def-4007">0</span><span class="sxs-lookup"><span data-stu-id="36def-4007">0</span></span><br/>

<span data-ttu-id="36def-4008">1</span><span class="sxs-lookup"><span data-stu-id="36def-4008">1</span></span>

<span data-ttu-id="36def-4009">2</span><span class="sxs-lookup"><span data-stu-id="36def-4009">2</span></span>

<span data-ttu-id="36def-4010">3</span><span class="sxs-lookup"><span data-stu-id="36def-4010">3</span></span>

<span data-ttu-id="36def-4011">4</span><span class="sxs-lookup"><span data-stu-id="36def-4011">4</span></span>

<span data-ttu-id="36def-4012">5</span><span class="sxs-lookup"><span data-stu-id="36def-4012">5</span></span>

<span data-ttu-id="36def-4013">6</span><span class="sxs-lookup"><span data-stu-id="36def-4013">6</span></span>

<span data-ttu-id="36def-4014">7</span><span class="sxs-lookup"><span data-stu-id="36def-4014">7</span></span>

<span data-ttu-id="36def-4015">8</span><span class="sxs-lookup"><span data-stu-id="36def-4015">8</span></span>

<span data-ttu-id="36def-4016">9</span><span class="sxs-lookup"><span data-stu-id="36def-4016">9</span></span>

<span data-ttu-id="36def-4017">3</span><span class="sxs-lookup"><span data-stu-id="36def-4017">3</span></span><br/> <span data-ttu-id="36def-4018">0</span><span class="sxs-lookup"><span data-stu-id="36def-4018">0</span></span><br/>

<span data-ttu-id="36def-4019">1</span><span class="sxs-lookup"><span data-stu-id="36def-4019">1</span></span>

<span data-ttu-id="36def-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-4020">\_hCursor</span></span>

<span data-ttu-id="36def-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="36def-4021">\_chapt</span></span>

<span data-ttu-id="36def-4022">\_bmk</span><span class="sxs-lookup"><span data-stu-id="36def-4022">\_bmk</span></span>



 

<span data-ttu-id="36def-4023">**\_ hCursor**：代表從 CPMCreateQueryOut 針對包含書簽的資料列集取得之查詢資料指標的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="36def-4024">**\_ chapt**：代表包含書簽之章節控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="36def-4025">**\_ bmk**：代表要取得其近似位置之書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="36def-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="36def-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="36def-4027">CPMGetApproximatePositionOut 訊息會回復 CPMGetApproximatePositionIn 訊息，其中描述章節中書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="36def-4028">標頭後面的 CPMGetApproximatePositionOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="36def-4029">0</span><span class="sxs-lookup"><span data-stu-id="36def-4029">0</span></span>

<span data-ttu-id="36def-4030">1</span><span class="sxs-lookup"><span data-stu-id="36def-4030">1</span></span>

<span data-ttu-id="36def-4031">2</span><span class="sxs-lookup"><span data-stu-id="36def-4031">2</span></span>

<span data-ttu-id="36def-4032">3</span><span class="sxs-lookup"><span data-stu-id="36def-4032">3</span></span>

<span data-ttu-id="36def-4033">4</span><span class="sxs-lookup"><span data-stu-id="36def-4033">4</span></span>

<span data-ttu-id="36def-4034">5</span><span class="sxs-lookup"><span data-stu-id="36def-4034">5</span></span>

<span data-ttu-id="36def-4035">6</span><span class="sxs-lookup"><span data-stu-id="36def-4035">6</span></span>

<span data-ttu-id="36def-4036">7</span><span class="sxs-lookup"><span data-stu-id="36def-4036">7</span></span>

<span data-ttu-id="36def-4037">8</span><span class="sxs-lookup"><span data-stu-id="36def-4037">8</span></span>

<span data-ttu-id="36def-4038">9</span><span class="sxs-lookup"><span data-stu-id="36def-4038">9</span></span>

<span data-ttu-id="36def-4039">1</span><span class="sxs-lookup"><span data-stu-id="36def-4039">1</span></span><br/> <span data-ttu-id="36def-4040">0</span><span class="sxs-lookup"><span data-stu-id="36def-4040">0</span></span><br/>

<span data-ttu-id="36def-4041">1</span><span class="sxs-lookup"><span data-stu-id="36def-4041">1</span></span>

<span data-ttu-id="36def-4042">2</span><span class="sxs-lookup"><span data-stu-id="36def-4042">2</span></span>

<span data-ttu-id="36def-4043">3</span><span class="sxs-lookup"><span data-stu-id="36def-4043">3</span></span>

<span data-ttu-id="36def-4044">4</span><span class="sxs-lookup"><span data-stu-id="36def-4044">4</span></span>

<span data-ttu-id="36def-4045">5</span><span class="sxs-lookup"><span data-stu-id="36def-4045">5</span></span>

<span data-ttu-id="36def-4046">6</span><span class="sxs-lookup"><span data-stu-id="36def-4046">6</span></span>

<span data-ttu-id="36def-4047">7</span><span class="sxs-lookup"><span data-stu-id="36def-4047">7</span></span>

<span data-ttu-id="36def-4048">8</span><span class="sxs-lookup"><span data-stu-id="36def-4048">8</span></span>

<span data-ttu-id="36def-4049">9</span><span class="sxs-lookup"><span data-stu-id="36def-4049">9</span></span>

<span data-ttu-id="36def-4050">2</span><span class="sxs-lookup"><span data-stu-id="36def-4050">2</span></span><br/> <span data-ttu-id="36def-4051">0</span><span class="sxs-lookup"><span data-stu-id="36def-4051">0</span></span><br/>

<span data-ttu-id="36def-4052">1</span><span class="sxs-lookup"><span data-stu-id="36def-4052">1</span></span>

<span data-ttu-id="36def-4053">2</span><span class="sxs-lookup"><span data-stu-id="36def-4053">2</span></span>

<span data-ttu-id="36def-4054">3</span><span class="sxs-lookup"><span data-stu-id="36def-4054">3</span></span>

<span data-ttu-id="36def-4055">4</span><span class="sxs-lookup"><span data-stu-id="36def-4055">4</span></span>

<span data-ttu-id="36def-4056">5</span><span class="sxs-lookup"><span data-stu-id="36def-4056">5</span></span>

<span data-ttu-id="36def-4057">6</span><span class="sxs-lookup"><span data-stu-id="36def-4057">6</span></span>

<span data-ttu-id="36def-4058">7</span><span class="sxs-lookup"><span data-stu-id="36def-4058">7</span></span>

<span data-ttu-id="36def-4059">8</span><span class="sxs-lookup"><span data-stu-id="36def-4059">8</span></span>

<span data-ttu-id="36def-4060">9</span><span class="sxs-lookup"><span data-stu-id="36def-4060">9</span></span>

<span data-ttu-id="36def-4061">3</span><span class="sxs-lookup"><span data-stu-id="36def-4061">3</span></span><br/> <span data-ttu-id="36def-4062">0</span><span class="sxs-lookup"><span data-stu-id="36def-4062">0</span></span><br/>

<span data-ttu-id="36def-4063">1</span><span class="sxs-lookup"><span data-stu-id="36def-4063">1</span></span>

<span data-ttu-id="36def-4064">\_分子</span><span class="sxs-lookup"><span data-stu-id="36def-4064">\_numerator</span></span>

<span data-ttu-id="36def-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="36def-4065">\_denominator</span></span>



 

<span data-ttu-id="36def-4066">**\_ 分子**：32位不帶正負號的整數，其中包含資料列集中書簽的資料列編號。</span><span class="sxs-lookup"><span data-stu-id="36def-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="36def-4067">如果沒有任何資料列，則此欄位必須設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="36def-4068">**\_ 分母**：32位不帶正負號的整數，其中包含資料列集中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="36def-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="36def-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="36def-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="36def-4070">CPMCompareBmkIn 訊息會要求一章中兩個書簽的比較。</span><span class="sxs-lookup"><span data-stu-id="36def-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="36def-4071">標頭後面的 CPMCompareBmkIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="36def-4072">0</span><span class="sxs-lookup"><span data-stu-id="36def-4072">0</span></span>

<span data-ttu-id="36def-4073">1</span><span class="sxs-lookup"><span data-stu-id="36def-4073">1</span></span>

<span data-ttu-id="36def-4074">2</span><span class="sxs-lookup"><span data-stu-id="36def-4074">2</span></span>

<span data-ttu-id="36def-4075">3</span><span class="sxs-lookup"><span data-stu-id="36def-4075">3</span></span>

<span data-ttu-id="36def-4076">4</span><span class="sxs-lookup"><span data-stu-id="36def-4076">4</span></span>

<span data-ttu-id="36def-4077">5</span><span class="sxs-lookup"><span data-stu-id="36def-4077">5</span></span>

<span data-ttu-id="36def-4078">6</span><span class="sxs-lookup"><span data-stu-id="36def-4078">6</span></span>

<span data-ttu-id="36def-4079">7</span><span class="sxs-lookup"><span data-stu-id="36def-4079">7</span></span>

<span data-ttu-id="36def-4080">8</span><span class="sxs-lookup"><span data-stu-id="36def-4080">8</span></span>

<span data-ttu-id="36def-4081">9</span><span class="sxs-lookup"><span data-stu-id="36def-4081">9</span></span>

<span data-ttu-id="36def-4082">1</span><span class="sxs-lookup"><span data-stu-id="36def-4082">1</span></span><br/> <span data-ttu-id="36def-4083">0</span><span class="sxs-lookup"><span data-stu-id="36def-4083">0</span></span><br/>

<span data-ttu-id="36def-4084">1</span><span class="sxs-lookup"><span data-stu-id="36def-4084">1</span></span>

<span data-ttu-id="36def-4085">2</span><span class="sxs-lookup"><span data-stu-id="36def-4085">2</span></span>

<span data-ttu-id="36def-4086">3</span><span class="sxs-lookup"><span data-stu-id="36def-4086">3</span></span>

<span data-ttu-id="36def-4087">4</span><span class="sxs-lookup"><span data-stu-id="36def-4087">4</span></span>

<span data-ttu-id="36def-4088">5</span><span class="sxs-lookup"><span data-stu-id="36def-4088">5</span></span>

<span data-ttu-id="36def-4089">6</span><span class="sxs-lookup"><span data-stu-id="36def-4089">6</span></span>

<span data-ttu-id="36def-4090">7</span><span class="sxs-lookup"><span data-stu-id="36def-4090">7</span></span>

<span data-ttu-id="36def-4091">8</span><span class="sxs-lookup"><span data-stu-id="36def-4091">8</span></span>

<span data-ttu-id="36def-4092">9</span><span class="sxs-lookup"><span data-stu-id="36def-4092">9</span></span>

<span data-ttu-id="36def-4093">2</span><span class="sxs-lookup"><span data-stu-id="36def-4093">2</span></span><br/> <span data-ttu-id="36def-4094">0</span><span class="sxs-lookup"><span data-stu-id="36def-4094">0</span></span><br/>

<span data-ttu-id="36def-4095">1</span><span class="sxs-lookup"><span data-stu-id="36def-4095">1</span></span>

<span data-ttu-id="36def-4096">2</span><span class="sxs-lookup"><span data-stu-id="36def-4096">2</span></span>

<span data-ttu-id="36def-4097">3</span><span class="sxs-lookup"><span data-stu-id="36def-4097">3</span></span>

<span data-ttu-id="36def-4098">4</span><span class="sxs-lookup"><span data-stu-id="36def-4098">4</span></span>

<span data-ttu-id="36def-4099">5</span><span class="sxs-lookup"><span data-stu-id="36def-4099">5</span></span>

<span data-ttu-id="36def-4100">6</span><span class="sxs-lookup"><span data-stu-id="36def-4100">6</span></span>

<span data-ttu-id="36def-4101">7</span><span class="sxs-lookup"><span data-stu-id="36def-4101">7</span></span>

<span data-ttu-id="36def-4102">8</span><span class="sxs-lookup"><span data-stu-id="36def-4102">8</span></span>

<span data-ttu-id="36def-4103">9</span><span class="sxs-lookup"><span data-stu-id="36def-4103">9</span></span>

<span data-ttu-id="36def-4104">3</span><span class="sxs-lookup"><span data-stu-id="36def-4104">3</span></span><br/> <span data-ttu-id="36def-4105">0</span><span class="sxs-lookup"><span data-stu-id="36def-4105">0</span></span><br/>

<span data-ttu-id="36def-4106">1</span><span class="sxs-lookup"><span data-stu-id="36def-4106">1</span></span>

<span data-ttu-id="36def-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-4107">\_hCursor</span></span>

<span data-ttu-id="36def-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="36def-4108">\_chapt</span></span>

<span data-ttu-id="36def-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="36def-4109">\_bmkFirst</span></span>

<span data-ttu-id="36def-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="36def-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="36def-4111">\_**hCursor**：代表包含書簽之資料列集之 CPMCreateQueryOut 訊息控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="36def-4112">\_**chapt**：代表章節之控制碼的32位值，其中包含要比較的書簽。</span><span class="sxs-lookup"><span data-stu-id="36def-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="36def-4113">\_**bmkFirst**：代表要比較之第一個書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="36def-4114">\_**bmkSecond**：代表要比較之第二個書簽控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="36def-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="36def-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="36def-4116">CPMCompareBmkOut 訊息會使用一章中兩個書簽的比較來回複 CPMCompareBmkIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="36def-4117">標頭後面的 CPMCompareBmkOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="36def-4118">0</span><span class="sxs-lookup"><span data-stu-id="36def-4118">0</span></span>

<span data-ttu-id="36def-4119">1</span><span class="sxs-lookup"><span data-stu-id="36def-4119">1</span></span>

<span data-ttu-id="36def-4120">2</span><span class="sxs-lookup"><span data-stu-id="36def-4120">2</span></span>

<span data-ttu-id="36def-4121">3</span><span class="sxs-lookup"><span data-stu-id="36def-4121">3</span></span>

<span data-ttu-id="36def-4122">4</span><span class="sxs-lookup"><span data-stu-id="36def-4122">4</span></span>

<span data-ttu-id="36def-4123">5</span><span class="sxs-lookup"><span data-stu-id="36def-4123">5</span></span>

<span data-ttu-id="36def-4124">6</span><span class="sxs-lookup"><span data-stu-id="36def-4124">6</span></span>

<span data-ttu-id="36def-4125">7</span><span class="sxs-lookup"><span data-stu-id="36def-4125">7</span></span>

<span data-ttu-id="36def-4126">8</span><span class="sxs-lookup"><span data-stu-id="36def-4126">8</span></span>

<span data-ttu-id="36def-4127">9</span><span class="sxs-lookup"><span data-stu-id="36def-4127">9</span></span>

<span data-ttu-id="36def-4128">1</span><span class="sxs-lookup"><span data-stu-id="36def-4128">1</span></span><br/> <span data-ttu-id="36def-4129">0</span><span class="sxs-lookup"><span data-stu-id="36def-4129">0</span></span><br/>

<span data-ttu-id="36def-4130">1</span><span class="sxs-lookup"><span data-stu-id="36def-4130">1</span></span>

<span data-ttu-id="36def-4131">2</span><span class="sxs-lookup"><span data-stu-id="36def-4131">2</span></span>

<span data-ttu-id="36def-4132">3</span><span class="sxs-lookup"><span data-stu-id="36def-4132">3</span></span>

<span data-ttu-id="36def-4133">4</span><span class="sxs-lookup"><span data-stu-id="36def-4133">4</span></span>

<span data-ttu-id="36def-4134">5</span><span class="sxs-lookup"><span data-stu-id="36def-4134">5</span></span>

<span data-ttu-id="36def-4135">6</span><span class="sxs-lookup"><span data-stu-id="36def-4135">6</span></span>

<span data-ttu-id="36def-4136">7</span><span class="sxs-lookup"><span data-stu-id="36def-4136">7</span></span>

<span data-ttu-id="36def-4137">8</span><span class="sxs-lookup"><span data-stu-id="36def-4137">8</span></span>

<span data-ttu-id="36def-4138">9</span><span class="sxs-lookup"><span data-stu-id="36def-4138">9</span></span>

<span data-ttu-id="36def-4139">2</span><span class="sxs-lookup"><span data-stu-id="36def-4139">2</span></span><br/> <span data-ttu-id="36def-4140">0</span><span class="sxs-lookup"><span data-stu-id="36def-4140">0</span></span><br/>

<span data-ttu-id="36def-4141">1</span><span class="sxs-lookup"><span data-stu-id="36def-4141">1</span></span>

<span data-ttu-id="36def-4142">2</span><span class="sxs-lookup"><span data-stu-id="36def-4142">2</span></span>

<span data-ttu-id="36def-4143">3</span><span class="sxs-lookup"><span data-stu-id="36def-4143">3</span></span>

<span data-ttu-id="36def-4144">4</span><span class="sxs-lookup"><span data-stu-id="36def-4144">4</span></span>

<span data-ttu-id="36def-4145">5</span><span class="sxs-lookup"><span data-stu-id="36def-4145">5</span></span>

<span data-ttu-id="36def-4146">6</span><span class="sxs-lookup"><span data-stu-id="36def-4146">6</span></span>

<span data-ttu-id="36def-4147">7</span><span class="sxs-lookup"><span data-stu-id="36def-4147">7</span></span>

<span data-ttu-id="36def-4148">8</span><span class="sxs-lookup"><span data-stu-id="36def-4148">8</span></span>

<span data-ttu-id="36def-4149">9</span><span class="sxs-lookup"><span data-stu-id="36def-4149">9</span></span>

<span data-ttu-id="36def-4150">3</span><span class="sxs-lookup"><span data-stu-id="36def-4150">3</span></span><br/> <span data-ttu-id="36def-4151">0</span><span class="sxs-lookup"><span data-stu-id="36def-4151">0</span></span><br/>

<span data-ttu-id="36def-4152">1</span><span class="sxs-lookup"><span data-stu-id="36def-4152">1</span></span>

<span data-ttu-id="36def-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="36def-4153">\_dwComparison</span></span>



 

<span data-ttu-id="36def-4154">\_**dwComparison**：下列其中一個值，表示章節中兩個書簽的相對位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="36def-4155">值</span><span class="sxs-lookup"><span data-stu-id="36def-4155">Value</span></span>                               | <span data-ttu-id="36def-4156">意義</span><span class="sxs-lookup"><span data-stu-id="36def-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="36def-4157">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="36def-4158">第一個書簽位於第二個。</span><span class="sxs-lookup"><span data-stu-id="36def-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="36def-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="36def-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="36def-4160">第一個書簽的位置與第二個相同。</span><span class="sxs-lookup"><span data-stu-id="36def-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="36def-4161">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="36def-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="36def-4162">第一個書簽的位置是在第二個。</span><span class="sxs-lookup"><span data-stu-id="36def-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="36def-4163">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="36def-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="36def-4164">第一個書簽的位置與第二個不同。</span><span class="sxs-lookup"><span data-stu-id="36def-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="36def-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="36def-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="36def-4166">第一個書簽無法與第二個書簽比較。</span><span class="sxs-lookup"><span data-stu-id="36def-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="36def-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="36def-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="36def-4168">CPMRestartPositionIn 訊息會將資料指標的提取位置移至章節的開頭。</span><span class="sxs-lookup"><span data-stu-id="36def-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="36def-4169">如3.1.5.2.12 一節中所指定，伺服器將使用相同的訊息來回複，並將要求的結果包含在 \_ CISP 標頭的 status 欄位中。</span><span class="sxs-lookup"><span data-stu-id="36def-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="36def-4170">標頭後面的 CPMRestartPositionIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="36def-4171">0</span><span class="sxs-lookup"><span data-stu-id="36def-4171">0</span></span>

<span data-ttu-id="36def-4172">1</span><span class="sxs-lookup"><span data-stu-id="36def-4172">1</span></span>

<span data-ttu-id="36def-4173">2</span><span class="sxs-lookup"><span data-stu-id="36def-4173">2</span></span>

<span data-ttu-id="36def-4174">3</span><span class="sxs-lookup"><span data-stu-id="36def-4174">3</span></span>

<span data-ttu-id="36def-4175">4</span><span class="sxs-lookup"><span data-stu-id="36def-4175">4</span></span>

<span data-ttu-id="36def-4176">5</span><span class="sxs-lookup"><span data-stu-id="36def-4176">5</span></span>

<span data-ttu-id="36def-4177">6</span><span class="sxs-lookup"><span data-stu-id="36def-4177">6</span></span>

<span data-ttu-id="36def-4178">7</span><span class="sxs-lookup"><span data-stu-id="36def-4178">7</span></span>

<span data-ttu-id="36def-4179">8</span><span class="sxs-lookup"><span data-stu-id="36def-4179">8</span></span>

<span data-ttu-id="36def-4180">9</span><span class="sxs-lookup"><span data-stu-id="36def-4180">9</span></span>

<span data-ttu-id="36def-4181">1</span><span class="sxs-lookup"><span data-stu-id="36def-4181">1</span></span><br/> <span data-ttu-id="36def-4182">0</span><span class="sxs-lookup"><span data-stu-id="36def-4182">0</span></span><br/>

<span data-ttu-id="36def-4183">1</span><span class="sxs-lookup"><span data-stu-id="36def-4183">1</span></span>

<span data-ttu-id="36def-4184">2</span><span class="sxs-lookup"><span data-stu-id="36def-4184">2</span></span>

<span data-ttu-id="36def-4185">3</span><span class="sxs-lookup"><span data-stu-id="36def-4185">3</span></span>

<span data-ttu-id="36def-4186">4</span><span class="sxs-lookup"><span data-stu-id="36def-4186">4</span></span>

<span data-ttu-id="36def-4187">5</span><span class="sxs-lookup"><span data-stu-id="36def-4187">5</span></span>

<span data-ttu-id="36def-4188">6</span><span class="sxs-lookup"><span data-stu-id="36def-4188">6</span></span>

<span data-ttu-id="36def-4189">7</span><span class="sxs-lookup"><span data-stu-id="36def-4189">7</span></span>

<span data-ttu-id="36def-4190">8</span><span class="sxs-lookup"><span data-stu-id="36def-4190">8</span></span>

<span data-ttu-id="36def-4191">9</span><span class="sxs-lookup"><span data-stu-id="36def-4191">9</span></span>

<span data-ttu-id="36def-4192">2</span><span class="sxs-lookup"><span data-stu-id="36def-4192">2</span></span><br/> <span data-ttu-id="36def-4193">0</span><span class="sxs-lookup"><span data-stu-id="36def-4193">0</span></span><br/>

<span data-ttu-id="36def-4194">1</span><span class="sxs-lookup"><span data-stu-id="36def-4194">1</span></span>

<span data-ttu-id="36def-4195">2</span><span class="sxs-lookup"><span data-stu-id="36def-4195">2</span></span>

<span data-ttu-id="36def-4196">3</span><span class="sxs-lookup"><span data-stu-id="36def-4196">3</span></span>

<span data-ttu-id="36def-4197">4</span><span class="sxs-lookup"><span data-stu-id="36def-4197">4</span></span>

<span data-ttu-id="36def-4198">5</span><span class="sxs-lookup"><span data-stu-id="36def-4198">5</span></span>

<span data-ttu-id="36def-4199">6</span><span class="sxs-lookup"><span data-stu-id="36def-4199">6</span></span>

<span data-ttu-id="36def-4200">7</span><span class="sxs-lookup"><span data-stu-id="36def-4200">7</span></span>

<span data-ttu-id="36def-4201">8</span><span class="sxs-lookup"><span data-stu-id="36def-4201">8</span></span>

<span data-ttu-id="36def-4202">9</span><span class="sxs-lookup"><span data-stu-id="36def-4202">9</span></span>

<span data-ttu-id="36def-4203">3</span><span class="sxs-lookup"><span data-stu-id="36def-4203">3</span></span><br/> <span data-ttu-id="36def-4204">0</span><span class="sxs-lookup"><span data-stu-id="36def-4204">0</span></span><br/>

<span data-ttu-id="36def-4205">1</span><span class="sxs-lookup"><span data-stu-id="36def-4205">1</span></span>

<span data-ttu-id="36def-4206">\_hCursor (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="36def-4207">\_chapt (選用) </span><span class="sxs-lookup"><span data-stu-id="36def-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="36def-4208">**\_ hCursor**：代表從 CPMCreateQueryOut 訊息取得之控制碼的32位值，識別要重新開機位置的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="36def-4209">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="36def-4210">**\_ chapt**：代表從中取出資料列之章節控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="36def-4211">當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="36def-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="36def-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="36def-4213">CPMFreeCursorIn 訊息會要求資料指標的版本。</span><span class="sxs-lookup"><span data-stu-id="36def-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="36def-4214">標頭後面的 CPMFreeCursorIn 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="36def-4215">0</span><span class="sxs-lookup"><span data-stu-id="36def-4215">0</span></span>

<span data-ttu-id="36def-4216">1</span><span class="sxs-lookup"><span data-stu-id="36def-4216">1</span></span>

<span data-ttu-id="36def-4217">2</span><span class="sxs-lookup"><span data-stu-id="36def-4217">2</span></span>

<span data-ttu-id="36def-4218">3</span><span class="sxs-lookup"><span data-stu-id="36def-4218">3</span></span>

<span data-ttu-id="36def-4219">4</span><span class="sxs-lookup"><span data-stu-id="36def-4219">4</span></span>

<span data-ttu-id="36def-4220">5</span><span class="sxs-lookup"><span data-stu-id="36def-4220">5</span></span>

<span data-ttu-id="36def-4221">6</span><span class="sxs-lookup"><span data-stu-id="36def-4221">6</span></span>

<span data-ttu-id="36def-4222">7</span><span class="sxs-lookup"><span data-stu-id="36def-4222">7</span></span>

<span data-ttu-id="36def-4223">8</span><span class="sxs-lookup"><span data-stu-id="36def-4223">8</span></span>

<span data-ttu-id="36def-4224">9</span><span class="sxs-lookup"><span data-stu-id="36def-4224">9</span></span>

<span data-ttu-id="36def-4225">1</span><span class="sxs-lookup"><span data-stu-id="36def-4225">1</span></span><br/> <span data-ttu-id="36def-4226">0</span><span class="sxs-lookup"><span data-stu-id="36def-4226">0</span></span><br/>

<span data-ttu-id="36def-4227">1</span><span class="sxs-lookup"><span data-stu-id="36def-4227">1</span></span>

<span data-ttu-id="36def-4228">2</span><span class="sxs-lookup"><span data-stu-id="36def-4228">2</span></span>

<span data-ttu-id="36def-4229">3</span><span class="sxs-lookup"><span data-stu-id="36def-4229">3</span></span>

<span data-ttu-id="36def-4230">4</span><span class="sxs-lookup"><span data-stu-id="36def-4230">4</span></span>

<span data-ttu-id="36def-4231">5</span><span class="sxs-lookup"><span data-stu-id="36def-4231">5</span></span>

<span data-ttu-id="36def-4232">6</span><span class="sxs-lookup"><span data-stu-id="36def-4232">6</span></span>

<span data-ttu-id="36def-4233">7</span><span class="sxs-lookup"><span data-stu-id="36def-4233">7</span></span>

<span data-ttu-id="36def-4234">8</span><span class="sxs-lookup"><span data-stu-id="36def-4234">8</span></span>

<span data-ttu-id="36def-4235">9</span><span class="sxs-lookup"><span data-stu-id="36def-4235">9</span></span>

<span data-ttu-id="36def-4236">2</span><span class="sxs-lookup"><span data-stu-id="36def-4236">2</span></span><br/> <span data-ttu-id="36def-4237">0</span><span class="sxs-lookup"><span data-stu-id="36def-4237">0</span></span><br/>

<span data-ttu-id="36def-4238">1</span><span class="sxs-lookup"><span data-stu-id="36def-4238">1</span></span>

<span data-ttu-id="36def-4239">2</span><span class="sxs-lookup"><span data-stu-id="36def-4239">2</span></span>

<span data-ttu-id="36def-4240">3</span><span class="sxs-lookup"><span data-stu-id="36def-4240">3</span></span>

<span data-ttu-id="36def-4241">4</span><span class="sxs-lookup"><span data-stu-id="36def-4241">4</span></span>

<span data-ttu-id="36def-4242">5</span><span class="sxs-lookup"><span data-stu-id="36def-4242">5</span></span>

<span data-ttu-id="36def-4243">6</span><span class="sxs-lookup"><span data-stu-id="36def-4243">6</span></span>

<span data-ttu-id="36def-4244">7</span><span class="sxs-lookup"><span data-stu-id="36def-4244">7</span></span>

<span data-ttu-id="36def-4245">8</span><span class="sxs-lookup"><span data-stu-id="36def-4245">8</span></span>

<span data-ttu-id="36def-4246">9</span><span class="sxs-lookup"><span data-stu-id="36def-4246">9</span></span>

<span data-ttu-id="36def-4247">3</span><span class="sxs-lookup"><span data-stu-id="36def-4247">3</span></span><br/> <span data-ttu-id="36def-4248">0</span><span class="sxs-lookup"><span data-stu-id="36def-4248">0</span></span><br/>

<span data-ttu-id="36def-4249">1</span><span class="sxs-lookup"><span data-stu-id="36def-4249">1</span></span>

<span data-ttu-id="36def-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="36def-4250">\_hCursor</span></span>



 

<span data-ttu-id="36def-4251">**\_ hCursor**：代表要釋放之 CPMCreateQueryOut 訊息中資料指標控制碼的32位值。</span><span class="sxs-lookup"><span data-stu-id="36def-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="36def-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="36def-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="36def-4253">CPMFreeCursorOut 訊息會回復 CPMFreeCursorIn 訊息，其中包含釋出資料指標的結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="36def-4254">標頭後面的 CPMFreeCursorOut 訊息格式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="36def-4255">0</span><span class="sxs-lookup"><span data-stu-id="36def-4255">0</span></span>

<span data-ttu-id="36def-4256">1</span><span class="sxs-lookup"><span data-stu-id="36def-4256">1</span></span>

<span data-ttu-id="36def-4257">2</span><span class="sxs-lookup"><span data-stu-id="36def-4257">2</span></span>

<span data-ttu-id="36def-4258">3</span><span class="sxs-lookup"><span data-stu-id="36def-4258">3</span></span>

<span data-ttu-id="36def-4259">4</span><span class="sxs-lookup"><span data-stu-id="36def-4259">4</span></span>

<span data-ttu-id="36def-4260">5</span><span class="sxs-lookup"><span data-stu-id="36def-4260">5</span></span>

<span data-ttu-id="36def-4261">6</span><span class="sxs-lookup"><span data-stu-id="36def-4261">6</span></span>

<span data-ttu-id="36def-4262">7</span><span class="sxs-lookup"><span data-stu-id="36def-4262">7</span></span>

<span data-ttu-id="36def-4263">8</span><span class="sxs-lookup"><span data-stu-id="36def-4263">8</span></span>

<span data-ttu-id="36def-4264">9</span><span class="sxs-lookup"><span data-stu-id="36def-4264">9</span></span>

<span data-ttu-id="36def-4265">1</span><span class="sxs-lookup"><span data-stu-id="36def-4265">1</span></span><br/> <span data-ttu-id="36def-4266">0</span><span class="sxs-lookup"><span data-stu-id="36def-4266">0</span></span><br/>

<span data-ttu-id="36def-4267">1</span><span class="sxs-lookup"><span data-stu-id="36def-4267">1</span></span>

<span data-ttu-id="36def-4268">2</span><span class="sxs-lookup"><span data-stu-id="36def-4268">2</span></span>

<span data-ttu-id="36def-4269">3</span><span class="sxs-lookup"><span data-stu-id="36def-4269">3</span></span>

<span data-ttu-id="36def-4270">4</span><span class="sxs-lookup"><span data-stu-id="36def-4270">4</span></span>

<span data-ttu-id="36def-4271">5</span><span class="sxs-lookup"><span data-stu-id="36def-4271">5</span></span>

<span data-ttu-id="36def-4272">6</span><span class="sxs-lookup"><span data-stu-id="36def-4272">6</span></span>

<span data-ttu-id="36def-4273">7</span><span class="sxs-lookup"><span data-stu-id="36def-4273">7</span></span>

<span data-ttu-id="36def-4274">8</span><span class="sxs-lookup"><span data-stu-id="36def-4274">8</span></span>

<span data-ttu-id="36def-4275">9</span><span class="sxs-lookup"><span data-stu-id="36def-4275">9</span></span>

<span data-ttu-id="36def-4276">2</span><span class="sxs-lookup"><span data-stu-id="36def-4276">2</span></span><br/> <span data-ttu-id="36def-4277">0</span><span class="sxs-lookup"><span data-stu-id="36def-4277">0</span></span><br/>

<span data-ttu-id="36def-4278">1</span><span class="sxs-lookup"><span data-stu-id="36def-4278">1</span></span>

<span data-ttu-id="36def-4279">2</span><span class="sxs-lookup"><span data-stu-id="36def-4279">2</span></span>

<span data-ttu-id="36def-4280">3</span><span class="sxs-lookup"><span data-stu-id="36def-4280">3</span></span>

<span data-ttu-id="36def-4281">4</span><span class="sxs-lookup"><span data-stu-id="36def-4281">4</span></span>

<span data-ttu-id="36def-4282">5</span><span class="sxs-lookup"><span data-stu-id="36def-4282">5</span></span>

<span data-ttu-id="36def-4283">6</span><span class="sxs-lookup"><span data-stu-id="36def-4283">6</span></span>

<span data-ttu-id="36def-4284">7</span><span class="sxs-lookup"><span data-stu-id="36def-4284">7</span></span>

<span data-ttu-id="36def-4285">8</span><span class="sxs-lookup"><span data-stu-id="36def-4285">8</span></span>

<span data-ttu-id="36def-4286">9</span><span class="sxs-lookup"><span data-stu-id="36def-4286">9</span></span>

<span data-ttu-id="36def-4287">3</span><span class="sxs-lookup"><span data-stu-id="36def-4287">3</span></span><br/> <span data-ttu-id="36def-4288">0</span><span class="sxs-lookup"><span data-stu-id="36def-4288">0</span></span><br/>

<span data-ttu-id="36def-4289">1</span><span class="sxs-lookup"><span data-stu-id="36def-4289">1</span></span>

<span data-ttu-id="36def-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="36def-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="36def-4291">**\_ cCursorsRemaining**：32位不帶正負號的整數，表示仍在查詢中使用的資料指標數目。</span><span class="sxs-lookup"><span data-stu-id="36def-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="36def-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="36def-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="36def-4293">CPMDisconnect 訊息會結束與伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="36def-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="36def-4294">訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。</span><span class="sxs-lookup"><span data-stu-id="36def-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="36def-4295">2.2.4 錯誤</span><span class="sxs-lookup"><span data-stu-id="36def-4295">2.2.4 Errors</span></span>

<span data-ttu-id="36def-4296">所有內容索引服務通訊協定訊息都必須在成功時傳回 0x00000000;否則，它們會傳回32位非零的錯誤碼，此錯誤碼可以是 HRESULT 或 NTSTATUS 值 (請參閱 1.8) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="36def-4297">如果緩衝區太小而無法符合結果，就必須傳回狀態為 [ \_ 資源不足] (0xC0000009A) 的狀態碼， \_ 而且應該以較大的緩衝區重試失敗的作業。</span><span class="sxs-lookup"><span data-stu-id="36def-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="36def-4298">所有其他錯誤值都必須視為相同。</span><span class="sxs-lookup"><span data-stu-id="36def-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="36def-4299"> (請注意，除非具有相同意義的值，否則目前的 HRESULT 和 NTSTATUS 編號空間不會重迭，但即使它們在未來會發生衝突，也不會造成任何通訊協定問題，只要狀態不足的資源值仍維持唯一的值，就不會造成任何通訊協定問題 \_ \_ ，因為所有其他錯誤值的處理方式都相同。 ) </span><span class="sxs-lookup"><span data-stu-id="36def-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="36def-4300">3 通訊協定詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="36def-4301">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="36def-4302">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="36def-4303">從遠端查詢索引服務目錄的 CISP 訊息要求不需要任何特定的順序。</span><span class="sxs-lookup"><span data-stu-id="36def-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="36def-4304">建議您將較高的層級導向至有意義的訊息順序，不過，就像是從這個序列或使用不正確資料收到的訊息一樣，伺服器將會以錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="36def-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="36def-4305">某些訊息也會相依于更高的層級，以提供在序列稍早的訊息中收到的有效資料。</span><span class="sxs-lookup"><span data-stu-id="36def-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="36def-4306">下圖說明從用戶端到遠端電腦的簡單查詢的一般訊息順序。</span><span class="sxs-lookup"><span data-stu-id="36def-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![簡單查詢的訊息順序](images/protocoldetails.jpg)

<span data-ttu-id="36def-4308">上圖所示的訊息代表用來查詢遠端索引服務類別目錄的所有 CISP 訊息子集。</span><span class="sxs-lookup"><span data-stu-id="36def-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="36def-4309">3.1 伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="36def-4310">3.1.1 抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="36def-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="36def-4311">下一節指定 CISP 伺服器所維護的資料和狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="36def-4312">此處提供的資料可協助說明通訊協定的運作方式。</span><span class="sxs-lookup"><span data-stu-id="36def-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="36def-4313">本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。</span><span class="sxs-lookup"><span data-stu-id="36def-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="36def-4314">執行 CISP 的索引服務必須維護下列抽象資料元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="36def-4315">連線到伺服器的用戶端清單</span><span class="sxs-lookup"><span data-stu-id="36def-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="36def-4316">每個用戶端的相關資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="36def-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="36def-4317">用戶端的版本 (，如區段2.2.3.6 中指定的 CPMConnectIn 訊息所示) </span><span class="sxs-lookup"><span data-stu-id="36def-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="36def-4318">CPMConnectIn 訊息 (與用戶端相關聯的目錄) </span><span class="sxs-lookup"><span data-stu-id="36def-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="36def-4319">2.2.1.21.1 一節中所指定的其他用戶端屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="36def-4320">用戶端的搜尋查詢</span><span class="sxs-lookup"><span data-stu-id="36def-4320">Client's search query</span></span>
    -   <span data-ttu-id="36def-4321">查詢的資料指標控制碼清單以及每個控制碼的結果集中的位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="36def-4322">目前的系結集合</span><span class="sxs-lookup"><span data-stu-id="36def-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="36def-4323">查詢的目前狀態，其中包含每個資料指標) 的 (：</span><span class="sxs-lookup"><span data-stu-id="36def-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="36def-4324">查詢結果中的資料列數目</span><span class="sxs-lookup"><span data-stu-id="36def-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="36def-4325">查詢完成的分子和分母</span><span class="sxs-lookup"><span data-stu-id="36def-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="36def-4326">最後一個資料列數目，由這個資料指標的最新 CPMRatioFinishedOut 訊息所報告</span><span class="sxs-lookup"><span data-stu-id="36def-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="36def-4327">無論查詢是否由伺服器監視查詢結果的變更，以及它是否受到監視，查詢結果中的變更會在查詢結果中變更，因為它上次回報給用戶端的 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="36def-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="36def-4328">此查詢對用戶端提供的章節控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="36def-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="36def-4329">此查詢對用戶端提供之每個資料指標的書簽控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="36def-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="36def-4330">索引服務目前的狀態，可能是「未初始化」、「執行中」或「正在關機」。</span><span class="sxs-lookup"><span data-stu-id="36def-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="36def-4331">請注意，大部分的時間伺服器處於「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="36def-4332">以下是伺服器的狀態機器圖表：</span><span class="sxs-lookup"><span data-stu-id="36def-4332">Following is the state machine diagram for the server:</span></span>

    ![索引服務伺服器的狀態機器圖表](images/abstractdatamodel.jpg)

-   <span data-ttu-id="36def-4334">每個目錄資訊：已編制索引的檔數目、索引的大小、唯一索引鍵的數目等 (請參閱 < 完整清單 () 的2.2.3.1 一節，其中對應至區段 2.2.3.2) 中 dwNewState 的值。</span><span class="sxs-lookup"><span data-stu-id="36def-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="36def-4335">針對每個支援的語言，如2.2.1.3 一節中所討論的單字變化資料庫。</span><span class="sxs-lookup"><span data-stu-id="36def-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="36def-4336">3.1.2 計時器</span><span class="sxs-lookup"><span data-stu-id="36def-4336">3.1.2 Timers</span></span>

<span data-ttu-id="36def-4337">不需要任何通訊協定計時器。</span><span class="sxs-lookup"><span data-stu-id="36def-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="36def-4338">3.1.3 初始化</span><span class="sxs-lookup"><span data-stu-id="36def-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="36def-4339">初始化時，伺服器必須將其狀態設定為 [未初始化]，並開始接聽區段1.9 中指定之具名管道上的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="36def-4340">進行任何其他內部初始化之後，它必須轉換成「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="36def-4341">3.1.4 較高層級觸發事件</span><span class="sxs-lookup"><span data-stu-id="36def-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="36def-4342">無。</span><span class="sxs-lookup"><span data-stu-id="36def-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="36def-4343">3.1.5 訊息處理和排序規則</span><span class="sxs-lookup"><span data-stu-id="36def-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="36def-4344">當處理用戶端傳送的訊息期間發生錯誤時，伺服器必須向用戶端報告錯誤，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="36def-4345">停止處理用戶端傳送的訊息</span><span class="sxs-lookup"><span data-stu-id="36def-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="36def-4346">以訊息標頭回應 (只有用戶端傳送的訊息) ，讓 \_ msg 欄位保持不變。</span><span class="sxs-lookup"><span data-stu-id="36def-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="36def-4347">將 [ \_ 狀態] 欄位設定為錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="36def-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="36def-4348">當訊息抵達時，伺服器必須檢查 \_ msg 域值，以查看它是否為已知的類型 (請參閱第2.2.2 節) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="36def-4349">如果類型未知，則必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="36def-4350">\_如果訊息類型是下列其中一項，則伺服器必須驗證 ulChecksum 域值：</span><span class="sxs-lookup"><span data-stu-id="36def-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="36def-4351">CPMConnectIn (0x000000C8) </span><span class="sxs-lookup"><span data-stu-id="36def-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="36def-4352">CPMCreateQueryIn (0x000000CA) </span><span class="sxs-lookup"><span data-stu-id="36def-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="36def-4353">CPMSetBindingsIn (0x000000D0) </span><span class="sxs-lookup"><span data-stu-id="36def-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="36def-4354">CPMGetRowsIn (0x000000CC) </span><span class="sxs-lookup"><span data-stu-id="36def-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="36def-4355">CPMFetchValueIn (0x000000E4) </span><span class="sxs-lookup"><span data-stu-id="36def-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="36def-4356">若要驗證 \_ ulChecksum 域值，伺服器必須檢查用戶端在 CPMConnectIn 訊息的 iClientVersion 欄位中指定的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="36def-4357">如果 [ \_ iClientVersion] 欄位未設定為 [0x00000008]，且 [ \_ ulChecksum] 欄位未設定為0x00000000，則伺服器必須回報狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="36def-4358">伺服器不能驗證 \_ 用戶端的 ulChecksum 欄位將 \_ iClientVersion 欄位設定為小於0x00000008 的值。</span><span class="sxs-lookup"><span data-stu-id="36def-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="36def-4359">如果 \_ iClientVersionfield 域值為0x00000008 或更大，則伺服器必須驗證 \_ ulChecksum 欄位的計算方式是在 [3.2.4] 區段中指定。</span><span class="sxs-lookup"><span data-stu-id="36def-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="36def-4360">如果 \_ ulChecksum 值無效，伺服器必須報告狀態不正確參數， \_ \_ (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="36def-4361">接著，伺服器會檢查其中的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="36def-4362">如果其狀態為 [未初始化]，伺服器必須報告 CI \_ E \_ 未 \_ 初始化 (0x8004180B) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="36def-4363">如果狀態為「關閉」，伺服器必須報告 CI \_ E \_ SHUTDOWN (0x80041812) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="36def-4364">一旦將標頭判斷為有效且伺服器處於「執行中」狀態之後，就必須依照下列各節所指定的方式來執行進一步的訊息特定處理。</span><span class="sxs-lookup"><span data-stu-id="36def-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="36def-4365">3.1.5.1 遠端索引服務目錄管理</span><span class="sxs-lookup"><span data-stu-id="36def-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="36def-4366">3.1.5.1.1 接收 CPMCiStateInOut 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="36def-4367">當伺服器收到來自用戶端的 CPMCIStateInOut 訊息要求時，伺服器必須先檢查用戶端是否在已連線的用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="36def-4368">如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="36def-4369">否則，它必須以 CPMCIStateInOut 訊息回應用戶端，並使用與2.2.3.1 小節中所指定的用戶端相關聯的目錄相關資訊來填入。</span><span class="sxs-lookup"><span data-stu-id="36def-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="36def-4370">3.1.5.1.2 接收 CPMSetCatStateIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="36def-4371">當伺服器收到來自用戶端的 CPMSetCatStateIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4372">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="36def-4372">Check that client has administrative access.</span></span> <span data-ttu-id="36def-4373">如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="36def-4374">如果 \_ dwNewState 不等於 CICAT ALL 會 \_ \_ 開啟，則變更 CatName 欄位中指定的目錄狀態，如 \_ dwNewState 欄位所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="36def-4375">如需詳細資訊，請參閱2.2.3.2 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="36def-4376">如果伺服器未在 CatName 欄位中找到具有指定名稱的目錄，伺服器必須傳回狀態 \_ 不正確 \_ 參數， (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4377">以 CPMSetCatStateOut 訊息回應用戶端，其中 \_ DWOLDSTATE 必須設定為目錄的先前狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="36def-4378">如果 \_ dwNewState 等於 CICAT， \_ 則所有 \_ 開啟的伺服器都必須檢查所有目錄的狀態，如果全部都已啟動，就必須將 \_ dwOldState 設定為0x00000001，否則請將 \_ dwOldState 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="36def-4379">3.1.5.1.3 接收 CPMUpdateDocumentsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="36def-4380">當伺服器收到 CPMUpdateDocumentsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4381">檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="36def-4382">如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4383">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="36def-4383">Check that client has administrative access.</span></span> <span data-ttu-id="36def-4384">如果用戶端沒有伺服器的系統管理存取權，則伺服器必須回報狀態 \_ \_ 拒絕存取 (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="36def-4385">根據 CPMUpdateDocumentsIn 訊息中的旗標欄位，開始建立用戶端所指定路徑的索引編制程式、執行完整或增量掃描 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="36def-4386">如果路徑先前未建立索引，則必須將它加入至索引位置的集合，並執行完整掃描。</span><span class="sxs-lookup"><span data-stu-id="36def-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="36def-4387">如果指定了不合法的 \_ 旗標欄位值，伺服器必須 \_ 將旗標設為 UPD \_ INIT 並執行完整掃描。</span><span class="sxs-lookup"><span data-stu-id="36def-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="36def-4388">這項作業必須在與用戶端相關聯的目錄中執行。</span><span class="sxs-lookup"><span data-stu-id="36def-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="36def-4389">使用 CPMUpdateDocumentsIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="36def-4390">3.1.5.1.4 接收 CPMForceMergeIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="36def-4391">當伺服器收到 CPMForceMergeIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4392">檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。</span><span class="sxs-lookup"><span data-stu-id="36def-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="36def-4393">如果用戶端不在清單中，伺服器必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4394">檢查用戶端是否具有系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="36def-4394">Check that client has administrative access.</span></span> <span data-ttu-id="36def-4395">如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="36def-4396">開始在與用戶端相關聯的目錄上改善查詢效能所需的維護流程。</span><span class="sxs-lookup"><span data-stu-id="36def-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="36def-4397">使用 CPMForceMergeIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="36def-4398">請注意，維護程式是非同步，而且可以在用戶端收到回應訊息之後繼續進行。</span><span class="sxs-lookup"><span data-stu-id="36def-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="36def-4399">此程式不會直接影響通訊協定， (回應時間) 以外的任何方式。</span><span class="sxs-lookup"><span data-stu-id="36def-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="36def-4400">3.1.5.2 遠端索引服務查詢</span><span class="sxs-lookup"><span data-stu-id="36def-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="36def-4401">3.1.5.2.1 接收 CPMConnectIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="36def-4402">當伺服器收到來自用戶端的 CPMConnectIn 要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4403">檢查用戶端是否在已連線用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="36def-4404">如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4405">檢查指定的目錄是否存在，而不是處於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="36def-4406">如果不是這種情況，伺服器就必須要有報表 CI \_ E \_ NO \_ CATALOG (0x8004181D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="36def-4407">將用戶端新增至已連線的用戶端清單。</span><span class="sxs-lookup"><span data-stu-id="36def-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="36def-4408">將目錄與用戶端產生關聯。</span><span class="sxs-lookup"><span data-stu-id="36def-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="36def-4409">將 CPMConnectIn 訊息中傳遞的資訊儲存 (例如目錄名稱、用戶端版本等 ) 處於用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="36def-4410">以 CPMConnectOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="36def-4411">3.1.5.2.2 接收 CPMCreateQueryIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="36def-4412">當伺服器收到來自用戶端的 CPMCreateQueryIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4413">檢查用戶端是否在已連線用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="36def-4414">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4415">檢查用戶端是否已經有與其相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="36def-4416">如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4417">檢查與用戶端相關聯的目錄是否處於狀態，以允許處理查詢 (CICAT \_ READONLY 或 CICAT \_ 可寫入) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="36def-4418">如果不是這種情況，伺服器就必須回報查詢 \_ S 查詢 \_ \_ (0x8004160C) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="36def-4419">剖析查詢中指定的限制集、排序次序和群組。</span><span class="sxs-lookup"><span data-stu-id="36def-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="36def-4420">如果伺服器發生錯誤，則必須報告適當的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="36def-4421">如果此步驟因為任何其他原因而失敗，則伺服器必須報告所遇到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="36def-4422">如需索引服務查詢錯誤的詳細資訊，請參閱 \[ MSDN-QUERYERR \] 。</span><span class="sxs-lookup"><span data-stu-id="36def-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="36def-4423">將搜尋查詢儲存為用戶端的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="36def-4424">根據 CPMCreateQueryIn 訊息) 中傳遞的資訊，進行將資料列提供給用戶端所需的準備工作，並將查詢與適當的資料指標控制碼產生關聯 (。</span><span class="sxs-lookup"><span data-stu-id="36def-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="36def-4425">將這些控制碼新增至用戶端的資料指標控制碼清單，然後初始化章節控制碼和書簽的清單。</span><span class="sxs-lookup"><span data-stu-id="36def-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="36def-4426">將此查詢中每個資料指標的章節控制碼清單初始化為 DB \_ Null \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="36def-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="36def-4427">將此查詢中每個資料指標的書簽控制碼清單，初始化為一組 DBBMK \_ FIRST 和 DBBMK \_ LAST。</span><span class="sxs-lookup"><span data-stu-id="36def-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="36def-4428">將查詢標示為未監視變更。</span><span class="sxs-lookup"><span data-stu-id="36def-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="36def-4429">將資料列的數目初始化為目前計算的資料列數目 (如果查詢無法開始執行，則可以是0，如果查詢是在執行) 的進程中，則為某個數位，然後初始化查詢完成的分子和分母。</span><span class="sxs-lookup"><span data-stu-id="36def-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="36def-4430">以 CPMCreateQueryOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="36def-4431">3.1.5.2.3 接收 CPMGetQueryStatusIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="36def-4432">當伺服器收到來自用戶端的 CPMGetQueryStatusIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4433">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="36def-4434">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4435">檢查游標控制碼是否位於用戶端的資料指標控制碼清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="36def-4436">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4437">準備 CPMGetQueryStatusOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="36def-4438">伺服器必須抓取目前的查詢狀態，並在 [QStatus] 欄位中設定它 (如需 \_ 可能的值) ，請參閱2.2.3.11。</span><span class="sxs-lookup"><span data-stu-id="36def-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="36def-4439">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="36def-4440">以 CPMGetQueryStatusOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="36def-4441">3.1.5.2.4 接收 CPMGetQueryStatusExIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="36def-4442">當伺服器收到來自用戶端的 CPMGetQueryStatusExIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4443">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4444">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4445">檢查傳遞的資料指標控制碼是否位於用戶端的資料指標控制碼清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="36def-4446">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4447">準備 CPMGetQueryStatusExOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="36def-4448">伺服器必須抓取目前的查詢狀態和查詢進度，並設定 QStatus (如需可能的值，請分別參閱 2.2.3.11) 、 \_ dwRatioFinishedDenominator 和 \_ dwRatioFinishedNumerator。</span><span class="sxs-lookup"><span data-stu-id="36def-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="36def-4449">然後，它必須將查詢結果中的資料列數目設定為 \_ cRowsTotal。</span><span class="sxs-lookup"><span data-stu-id="36def-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="36def-4450">如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4451">取得用戶端類別目錄的相關資訊，並填寫 \_ cFilteredDocuments 和 \_ cDocumentsToFilter。</span><span class="sxs-lookup"><span data-stu-id="36def-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="36def-4452">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4453">取出 bmk 欄位中的控制碼所指定之書簽的位置 \_ ，然後在 CPMGetQueryStatusExOut 訊息中填滿其餘的 \_ iRowBmk 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="36def-4454">如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4455">以 CPMGetQueryStatusExOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="36def-4456">3.1.5.2.5 接收 CPMRatioFinishedIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="36def-4457">當伺服器收到來自用戶端的 CPMRatioFinishedIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4458">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="36def-4459">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4460">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="36def-4461">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4462">準備 CPMRatioFinishedOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="36def-4463">伺服器必須抓取用戶端的查詢狀態，並填寫 \_ ulNumerator、 \_ ulDenominator 和 \_ >crows 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="36def-4464">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4465">如果 \_ >crows 等於此查詢最後報告的資料列數目，請將 \_ fNewRows 設定為0x00000000，否則請將其設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="36def-4466">將此查詢最後報告的資料列數更新為 >crows 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="36def-4467">以 CPMRatioFinishedOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="36def-4468">3.1.5.2.6 接收 CPMSetBindingsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="36def-4469">當伺服器收到來自用戶端的 CPMSetBindingsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4470">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4471">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4472">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="36def-4473">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4474">確認系結資訊有效 (亦即，資料行至少指定要傳回的值、長度或狀態;值、長度或狀態的系結中沒有重迭以及符合指定之資料列大小的值、長度和狀態) 以及如果未報告 DB \_ E \_ BADBINDINFO (0x80040E08) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="36def-4475">儲存與 aColumns 欄位中指定之資料行相關聯的系結資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="36def-4476">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4477">使用訊息標頭來回應用戶端 (只) \_ 將 msg 設定為 CPMSetBindingsIn，並 \_ 將狀態設定為指定之系結的結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="36def-4478">3.1.5.2.7 接收 CPMGetRowsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="36def-4479">當伺服器收到來自用戶端的 CPMGetRowsIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4480">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="36def-4481">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4482">檢查傳遞的資料指標控制碼是否在用戶端資料指標控制碼的 athelist 中。</span><span class="sxs-lookup"><span data-stu-id="36def-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="36def-4483">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4484">檢查用戶端是否有一組目前的系結。</span><span class="sxs-lookup"><span data-stu-id="36def-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="36def-4485">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4486">準備 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="36def-4487">伺服器必須將游標放在查詢結果中，如搜尋描述所指示。</span><span class="sxs-lookup"><span data-stu-id="36def-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="36def-4488">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4489">提取最適合緩衝區的資料列數目，其大小會以 \_ cbReadBuffer 表示，但不能超過 cRowsToTransfer 的指示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="36def-4490">提取資料列時，伺服器必須將每個選取的資料行的屬性值類型，與用戶端目前的系結集合中指定的型別進行比較 (區段 3.1.1) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="36def-4491">如果系結中的型別不是 VT \_ 變異，伺服器必須嘗試將資料行的屬性值轉換為該型別。</span><span class="sxs-lookup"><span data-stu-id="36def-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="36def-4492">否則，如果在 \_ 用戶端的 DBPROPSET QUERYEXT 屬性集中設定 DBPROP USEEXTENDEDDBTYPES 旗標 \_ ，或如果資料行的屬性值不是 VT \_ 向量類型，則必須以其一般型別傳回屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="36def-4493">如果這兩種情況都沒有 (也就是伺服器有 VT \_ 向量類型，而用戶端不支援 vt \_ 向量) ，則伺服器必須嘗試將它轉換成 vt 陣列類型，如下所示 \_ ： VT \_ I8、vt \_ UI8、vt \_ FILETIME 和 vt \_ CLSID 陣列元素無法轉換，而是無法轉換;VT \_ LPSTR 和 vt \_ LPWSTR 陣列元素必須轉換成 vt \_ BSTR; 所有其他類型的陣列元素都必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="36def-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="36def-4494">最後，如果資料列資料行包含章節控制碼或書簽控點，則伺服器必須更新對應的清單。</span><span class="sxs-lookup"><span data-stu-id="36def-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="36def-4495">如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="36def-4496">儲存 cRowsReturned 中提取的實際資料列數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="36def-4497">將 [搜尋描述] 和 [章節] 欄位從 CPMGetRowsIn 複製到要傳送的 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="36def-4498">在 [資料列] 欄位中儲存提取的資料列 (請參閱下方的 [狀態位元組] 和 [資料列的結構] 欄位) 的 [2.2.3.16] 區段。</span><span class="sxs-lookup"><span data-stu-id="36def-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="36def-4499">以 CPMGetRowsOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="36def-4500">[狀態位元組] 欄位上的附注：</span><span class="sxs-lookup"><span data-stu-id="36def-4500">Note on status byte field:</span></span>

<span data-ttu-id="36def-4501">如果資料行的 CPMSetBindingIn 訊息 CTableColumn 中的 StatusUsed 設定為0x01，則伺服器必須將從這個資料行的資料列開頭) 的狀態位元組 (設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="36def-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="36def-4502">值</span><span class="sxs-lookup"><span data-stu-id="36def-4502">Value</span></span> | <span data-ttu-id="36def-4503">意義</span><span class="sxs-lookup"><span data-stu-id="36def-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="36def-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="36def-4504">0x00</span></span>  | <span data-ttu-id="36def-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="36def-4505">StatusOK</span></span>       |
| <span data-ttu-id="36def-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="36def-4506">0x01</span></span>  | <span data-ttu-id="36def-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="36def-4507">StatusDeferred</span></span> |
| <span data-ttu-id="36def-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="36def-4508">0x02</span></span>  | <span data-ttu-id="36def-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="36def-4509">StatusNull</span></span>     |



 

<span data-ttu-id="36def-4510">如果此資料列的屬性值不存在，伺服器必須將狀態位元組設定為 StatusNull。</span><span class="sxs-lookup"><span data-stu-id="36def-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="36def-4511">如果值太大而無法在 CPMGetRowsOut 訊息中傳送，伺服器必須將狀態位元組設定為 StatusDeferred。</span><span class="sxs-lookup"><span data-stu-id="36def-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="36def-4512">否則伺服器必須將狀態位元組設為 StatusOK。</span><span class="sxs-lookup"><span data-stu-id="36def-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="36def-4513">3.1.5.2.8 接收 CPMFetchValueIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="36def-4514">當伺服器收到來自用戶端的 CPMFetchValueIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4515">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="36def-4516">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4517">準備 CPMFetchValueOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="36def-4518">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="36def-4519">尋找 wid 欄位所指出的檔 \_ ，並檢查此檔的屬性識別碼 (稍後稱為「屬性值」，此用戶端可以使用 PropSpec 結構所指出的「屬性值」 ) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="36def-4520">如果無法使用此值，伺服器必須將 \_ fValueExists 設定為0x00000000，否則請將 \_ fValueExists 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="36def-4521">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="36def-4522">如果 \_ fValueExists 等於0x00000001，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="36def-4523">將屬性值序列化為 SERIALIZEDPROPERTYVALUE 結構，並從 cbSoFar 位移開始複製（ \_ 最多 \_ cbChunk 個位元組） (但不超過序列化屬性) 到 vValue 欄位的結尾。</span><span class="sxs-lookup"><span data-stu-id="36def-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="36def-4524">如果此步驟因為任何原因而失敗，伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="36def-4525">將 \_ cbValue 設定為上一個步驟中複製的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="36def-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="36def-4526">將 vType 設定為屬性值的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="36def-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="36def-4527">如果序列化屬性的長度大於 \_ cbSoFar 新增至 \_ cbValue，則將 \_ fMoreExists 設定為0x00000001，否則請將其設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="36def-4528">以 CPMFetchValueOut 訊息回應用戶端</span><span class="sxs-lookup"><span data-stu-id="36def-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="36def-4529">3.1.5.2.9 接收 CPMGetNotify 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="36def-4530">當伺服器收到來自用戶端的 CPMGetNotify 訊息時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4531">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="36def-4532">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4533">如果自這個用戶端的最後一個 CPMSendNotifyOut 訊息之後，查詢結果集內沒有任何變更，或者查詢目前未監視結果集內的變更，則伺服器必須回應 CPMGetNotify 訊息，並開始監視查詢結果集的變更。</span><span class="sxs-lookup"><span data-stu-id="36def-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="36def-4534">如果稍後在查詢結果集中有變更，伺服器必須只傳送一個 CPMSendNotifyOut 訊息給用戶端，而且必須在 [watchNotify] 欄位中指定變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="36def-4535">如果自上次 CPMSendNotifyOut 訊息之後，查詢結果集的變更，伺服器必須以 CPMSendNotifyOut 回復，而且必須在 [watchNotify] 欄位中指定變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="36def-4536">請注意，在查詢結果的許多變更時，DBWATCHNOTIFY \_ ROWSCHANGED 會採用優先權 (也就是，如果查詢已完成、重新執行，然後變更資料列的數目，然後再次執行查詢，則回報的事件會是 DBWATCHNOTIFY \_ ROWSCHANGED) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="36def-4537">3.1.5.2.10 接收 CPMGetApproximatePositionIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="36def-4538">當伺服器收到來自用戶端的 CPMGetApproximatePositionIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4539">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4540">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4541">檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="36def-4542">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4543">在查詢結果中尋找與書簽控制碼相關聯的資料列，並估計資料列集中的資料列位置（由章節控點參考），並決定該位置的分子和分母。</span><span class="sxs-lookup"><span data-stu-id="36def-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="36def-4544">請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。</span><span class="sxs-lookup"><span data-stu-id="36def-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="36def-4545">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="36def-4546">以 CPMFetchValueOut 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="36def-4547">3.1.5.2.11 接收 CPMCompareBmkIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="36def-4548">當伺服器收到來自用戶端的 CPMCompareBmkIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4549">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4550">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4551">檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="36def-4552">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4553">準備 CPMCompareBmkOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="36def-4554">如果書簽控制碼相等，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ EQ。</span><span class="sxs-lookup"><span data-stu-id="36def-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="36def-4555">否則，如果其中一個書簽控制碼是 DBBMK \_ FIRST 或 DBBMK \_ LAST，則 \_ dwComparison 必須設定為 DBCOMPARE \_ NE。</span><span class="sxs-lookup"><span data-stu-id="36def-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="36def-4556">否則伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="36def-4557">尋找查詢結果中每個書簽控制碼所參考的資料列</span><span class="sxs-lookup"><span data-stu-id="36def-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="36def-4558">如果有任何一個資料列不在 CPMCompareBmkIn 的章節控制碼所指示的章節中，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ NOTCOMPARABLE。</span><span class="sxs-lookup"><span data-stu-id="36def-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="36def-4559">否則，當兩個數據列都位於相同的章節時，伺服器必須近似于本章節的控制碼所參考的資料列集中的資料列位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="36def-4560">然後，如果第一個資料列的位置小於第二個數據列的位置，則它必須比較位置值，並將 \_ dwComparison 設定為 DBCOMPARE \_ LT; 否則 \_ dwComparison 必須設定為 DBCOMPARE \_ GT。</span><span class="sxs-lookup"><span data-stu-id="36def-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="36def-4561">使用已填滿的 CPMCompareBmkOut 訊息來回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="36def-4562">3.1.5.2.12 接收 CPMRestartPositionIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="36def-4563">當伺服器收到來自用戶端的 CPMRestartPositionIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4564">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4565">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4566">檢查游標控制碼和傳遞的章節控制碼是否在對應的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="36def-4567">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4568">將游標移至章節的開頭，以章節控點來識別。</span><span class="sxs-lookup"><span data-stu-id="36def-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="36def-4569">請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。</span><span class="sxs-lookup"><span data-stu-id="36def-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="36def-4570">如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="36def-4571">以 CPMRestartPositionIn 訊息回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="36def-4572">3.1.5.2.13 接收 CPMFreeCursorIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="36def-4573">當伺服器收到來自用戶端的 CPMFreeCursorIn 訊息要求時，伺服器必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="36def-4574">檢查用戶端是否有相關聯的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="36def-4575">如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36def-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="36def-4576">檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="36def-4577">如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="36def-4578">釋出資料指標和相關聯的資源 (如需此資料指標控制碼的完整清單) ，請參閱3.1.1 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="36def-4579">從該用戶端的資料指標清單中移除資料指標。</span><span class="sxs-lookup"><span data-stu-id="36def-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="36def-4580">以 CPMFreeCursorOut 訊息回應， \_ 並以剩餘的資料指標數目設定 cCursorsRemaining 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="36def-4581">在此用戶端清單中。</span><span class="sxs-lookup"><span data-stu-id="36def-4581">in this client's list.</span></span>
-   <span data-ttu-id="36def-4582">如果此用戶端沒有其他資料指標，則伺服器必須釋放查詢和相關聯的資源 (請參閱 3.1.1) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="36def-4583">3.1.5.2.14 接收 CPMDisconnect 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="36def-4584">當伺服器收到來自用戶端的 CPMDisconnect 訊息要求時，伺服器必須從連線的用戶端清單中移除用戶端，並釋放與用戶端相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="36def-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="36def-4585">3.1.6 計時器事件</span><span class="sxs-lookup"><span data-stu-id="36def-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="36def-4586">無。</span><span class="sxs-lookup"><span data-stu-id="36def-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="36def-4587">3.1.7 其他本機事件</span><span class="sxs-lookup"><span data-stu-id="36def-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="36def-4588">當伺服器停止時，它必須先轉換成「正在關機」狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="36def-4589">然後，它必須停止接聽管道、執行任何其他執行特定的關機工作，然後轉換成「已停止」狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="36def-4590">3.2 用戶端詳細資料</span><span class="sxs-lookup"><span data-stu-id="36def-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="36def-4591">3.2.1 抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="36def-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="36def-4592">下一節會指定內容索引服務通訊協定用戶端所維護的資料和狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="36def-4593">提供的資料是為了促進通訊協定運作方式的說明。</span><span class="sxs-lookup"><span data-stu-id="36def-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="36def-4594">本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。</span><span class="sxs-lookup"><span data-stu-id="36def-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="36def-4595">用戶端具有下列抽象狀態：</span><span class="sxs-lookup"><span data-stu-id="36def-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="36def-4596">**最後傳送的訊息**：最後傳送至伺服器的訊息複本。</span><span class="sxs-lookup"><span data-stu-id="36def-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="36def-4597">**目前的屬性值**：「已延後」屬性的部分值，此為正在抓取的進程中。</span><span class="sxs-lookup"><span data-stu-id="36def-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="36def-4598">**目前接收的位元組** 數：目前為止針對目前屬性值所接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="36def-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="36def-4599">**具名管道連接狀態**：與伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="36def-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="36def-4600">3.2.2 計時器</span><span class="sxs-lookup"><span data-stu-id="36def-4600">3.2.2 Timers</span></span>

<span data-ttu-id="36def-4601">不需要任何通訊協定計時器。</span><span class="sxs-lookup"><span data-stu-id="36def-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="36def-4602">3.2.3 初始化</span><span class="sxs-lookup"><span data-stu-id="36def-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="36def-4603">在收到較高層級的要求之前，不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="36def-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="36def-4604">3.2.4 Higher-Layer 觸發的事件</span><span class="sxs-lookup"><span data-stu-id="36def-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="36def-4605">從較高的層收到要求時，用戶端必須使用2.1 節中指定的詳細資料，建立與伺服器的具名管道連接。</span><span class="sxs-lookup"><span data-stu-id="36def-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="36def-4606">如果無法這麼做，則更高的層級要求必須失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="36def-4607">亦即，如果連線失敗，則需要較高層級的責任才能重試。</span><span class="sxs-lookup"><span data-stu-id="36def-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="36def-4608">標頭必須預先暫止，並設定為從2.2.2 節中指定的欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="36def-4609">如果是指定為需要非零總和檢查碼的訊息，則 \_ 必須計算 ulChecksum 值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="36def-4610">訊息 \_ 標頭中的 ulReserved2 欄位之後的訊息內容必須解釋為32位整數的序列。</span><span class="sxs-lookup"><span data-stu-id="36def-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="36def-4611">用戶端必須計算這些整數所指定之數值的總和。</span><span class="sxs-lookup"><span data-stu-id="36def-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="36def-4612">使用0x59533959 計算此值的位 XOR。</span><span class="sxs-lookup"><span data-stu-id="36def-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="36def-4613">\_從位 XOR 產生的值減去 msg 提供的值。</span><span class="sxs-lookup"><span data-stu-id="36def-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="36def-4614">3.2.4.1 遠端索引服務目錄管理</span><span class="sxs-lookup"><span data-stu-id="36def-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="36def-4615">每個訊息都是由較高層的要求所觸發。</span><span class="sxs-lookup"><span data-stu-id="36def-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="36def-4616">用戶端不會針對遠端系統管理目錄的 CISP 訊息要求強制執行訊息順序，但是 (除了 CPMSetCatStateIn) 訊息之外，伺服器只會在用戶端先前透過 CPMConnectIn 訊息連接時才回復成功。</span><span class="sxs-lookup"><span data-stu-id="36def-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="36def-4617">3.2.4.1.1 傳送 CPMCiStateInOut 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="36def-4618">一般而言，較高的層級會要求通訊協定用戶端在需要伺服器上索引服務的相關資訊時，傳送 CPMCiStateInOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="36def-4619">當要求傳送此訊息時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4620">將區段2.2.3.1 中指定的 CPMCiStateInOut 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="36def-4621">等候接收來自伺服器的 CPMCiStateInOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4622">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則會將資訊結構傳回至較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="36def-4623">3.2.4.1.2 傳送 CPMSetCatStateIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="36def-4624">一般而言，較高的層級會要求通訊協定用戶端在需要類別目錄或所有目錄的資訊時傳送 CPMSetCatStateIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="36def-4625">在此訊息中，較高層必須為通訊協定用戶端提供 dwNewState 的值， \_ 並視需要提供類別目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="36def-4626">當要求傳送此訊息時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4627">將2.2.3.2 中所指定的 CPMSetCatStateIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="36def-4628">等候接收來自伺服器的 CPMSetCatStateOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4629">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ dwOldState 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="36def-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="36def-4630">3.2.4.1.3 傳送 CPMUpdateDocumentsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="36def-4631">如果需要在現有的路徑中更新檔，或將新的檔案路徑加入至索引，則較高的層通常會要求傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="36def-4632">因此，較高的層級是提供掃描的路徑和類型，其指定方式是在2.2.3.4 的區段中指定，其中增量或完整更新適用于現有的路徑，而新的初始化則適用于新的路徑。</span><span class="sxs-lookup"><span data-stu-id="36def-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="36def-4633">為了提供更高的層級要求，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4634">將區段2.2.3.4 中指定的 CPMUpdateDocumentsIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="36def-4635">等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4636">將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="36def-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="36def-4637">3.2.4.1.4 傳送 CPMForceMergeIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="36def-4638">一般來說，如果需要改善查詢效能，或是已排程的索引服務維護，則傳送此訊息的層級要求越高。</span><span class="sxs-lookup"><span data-stu-id="36def-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="36def-4639">為了提供更高層級的服務，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4640">依區段2.2.3.5 的指定將 CPMForceMergeIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="36def-4641">等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4642">將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="36def-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="36def-4643">3.2.4.2 遠端索引服務目錄查詢訊息</span><span class="sxs-lookup"><span data-stu-id="36def-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="36def-4644">除了 CPMGetRowsIn/CPMGetRowsOut、CPMFetchValueIn/CPMFetchValueOut，CISP 訊息和更高層級的要求之間有一對一的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36def-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="36def-4645">針對上述兩個例外狀況，用戶端可能會產生多個訊息來滿足大小需求，或取得完整的屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="36def-4646">較高層級通常會追蹤所有查詢特定的資訊 (例如開啟的資料指標控制碼、書簽和章節控制碼的合法值、延遲屬性值的 wid 值等等 ) ，也會追蹤用戶端是否處於連接狀態，但不會由用戶端以任何方式強制執行。</span><span class="sxs-lookup"><span data-stu-id="36def-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="36def-4647">為了方便說明，第3節中的圖表用戶端部分會說明這種簡單的索引服務查詢順序。</span><span class="sxs-lookup"><span data-stu-id="36def-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="36def-4648">3.2.4.2.1 傳送 CPMConnectIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="36def-4649">這則訊息通常是較高層級的第一個要求 (如同用戶端未連線一樣，伺服器將會失敗大部分的訊息，但 CPMSetCatStateIn) 除外。</span><span class="sxs-lookup"><span data-stu-id="36def-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="36def-4650">較高層級會為通訊協定用戶端提供連接所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="36def-4651">為了提供更高的層級，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4652">填寫訊息，使用更高層級用戶端所提供的資訊 (請參閱 \_ iClientVersion、MachineName、UserName、PropertySet1、PropertySet2 和 aPropertySet 中的 2.2.3.6) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="36def-4653">設定 \_ fClientIsRemote、 \_ cbBlob、 \_ cbBlob2、cPropSet 和 cExtPropSet，如2.2.3.6 中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="36def-4654">在 [ulChecksum] 欄位中設定總和檢查碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="36def-4655">將 CPMConnectIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="36def-4656">等候接收來自伺服器的 CPMConnectOut 訊息，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4657">報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ serverVersion 回較高的圖層。</span><span class="sxs-lookup"><span data-stu-id="36def-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="36def-4658">基於資訊的目的，較高層級通常會在連接成功時執行下列動作，但 CISP 用戶端不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="36def-4659">使用遠端索引服務目錄管理訊息進行系統管理工作</span><span class="sxs-lookup"><span data-stu-id="36def-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="36def-4660">使用 CPMCreateQueryIn 要求建立搜尋查詢，其目的是要從目錄中抓取結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="36def-4661">3.2.4.2.2 傳送 CPMCreateQueryIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="36def-4662">當通訊協定用戶端連線之後，較高層級通常會提供查詢建立的資訊。</span><span class="sxs-lookup"><span data-stu-id="36def-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="36def-4663">較高的層級會為用戶端提供限制設定、資料行集、排序次序規則和分類集 (可以省略) 、資料列集屬性和屬性識別碼對應程式結構。</span><span class="sxs-lookup"><span data-stu-id="36def-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="36def-4664">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4665">準備 CPMCreateQueryOut，如下所示。</span><span class="sxs-lookup"><span data-stu-id="36def-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="36def-4666">如果有資料行集存在，請將 CColumnsSetPreset 設定為0x01 並填滿 ColumnsSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="36def-4667">如果有限制，請將 CRestrictionPresent 設定為0x01 並填滿限制欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="36def-4668">如果有排序集存在，請填入 SortSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="36def-4669">如果有分類集存在，請將 CSortSetPresent 設定為0x01 並填滿 CategorizationSet 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="36def-4670">設定2.2.3.8 中指定的剩餘欄位</span><span class="sxs-lookup"><span data-stu-id="36def-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="36def-4671">計算 \_ 標頭中的 ulCheckSum 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="36def-4672">將 CPMCreateQueryIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="36def-4673">等候接收 CPMCreateQueryOut 訊息 (請參閱3.2.5.1.1 一節中的詳細資料) ，以無訊息方式捨棄所有其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="36def-4674">報告回應的 [狀態] 欄位的值， \_ 如果成功，則會將資料指標控制碼的陣列和資訊性布林值 (指定在 2.2.3.9) 回到較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="36def-4675">3.2.4.2.3 傳送 CPMSetBindingsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="36def-4676">一般來說， (當資料列已成功接收 CPMCreateQueryOut 之後，資料列中的每個資料行的系結將會被傳回，請參閱 3.2.5.1.1) 一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="36def-4677">較高的預期會提供 CTableColumn 結構的陣列，如2.2.4.31 中所指定的 aColumns 欄位和有效的資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="36def-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="36def-4678">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4679">計算 aColumns 陣列中的 CTableColumn 結構數目，並將 cColumns 欄位設定為此值。</span><span class="sxs-lookup"><span data-stu-id="36def-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="36def-4680">計算 cColumns 和 aColumns 欄位的總大小（以位元組為單位），並將 \_ cbBindingDesc 欄位設定為此值。</span><span class="sxs-lookup"><span data-stu-id="36def-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="36def-4681">在 CPMSetBindingsIn 訊息中，將指定的欄位設定為較高的應用層所提供的值。</span><span class="sxs-lookup"><span data-stu-id="36def-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="36def-4682">將 [ \_ ulChecksum] 欄位設定為 [3.2.5] 區段中所指定的計算值。</span><span class="sxs-lookup"><span data-stu-id="36def-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="36def-4683">將已完成的 CPMSetBindignsIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="36def-4684">等候接收來自伺服器的 CPMSetBindingsIn 訊息，並捨棄其他訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="36def-4685">從回應的 [狀態] 欄位中，指出 \_ 對較高層的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="36def-4686">基於資訊的目的，較高層級通常會要求用戶端傳送 CPMGetRowsIn 訊息，但不會由內容編制索引服務通訊協定強制執行。</span><span class="sxs-lookup"><span data-stu-id="36def-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="36def-4687">3.2.4.2.4 傳送 CPMGetRowsIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="36def-4688">當較高的層級即將接收資料列資訊時，它會提供具有有效資料指標和章節控制碼的通訊協定用戶端，並提供適當的搜尋描述。</span><span class="sxs-lookup"><span data-stu-id="36def-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="36def-4689">一般來說，當它有有效的資料指標和/或章節控制碼，且系結已設定了 CPMSetBindingsIn 訊息時，就會需要較高層級的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="36def-4690">若要存取章節中的資料列集，較高的層級是在先前的 CPMGetRowsOut 訊息中使用從伺服器收到的章節控制碼。</span><span class="sxs-lookup"><span data-stu-id="36def-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="36def-4691">從較高的層接收此要求時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4692">判斷要為 cbReadBuffer 欄位指定的不帶正負號的整數值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="36def-4693">若要判斷此值，用戶端必須採用下列值的最大值：</span><span class="sxs-lookup"><span data-stu-id="36def-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="36def-4694">C RowsToTransfer 欄位值的1000倍 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="36def-4695">CbRowWidth 的值 \_ ，進位至最接近的512位元組倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="36def-4696">將這兩個值的較高，最多可達16K 限制。</span><span class="sxs-lookup"><span data-stu-id="36def-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="36def-4697">在單一資料列大於16K 的情況下，伺服器無法將結果傳回此查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="36def-4698">在 ulClientBase 欄位的用戶端位址空間中，為可變大小的資料列資料指定用戶端基底 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="36def-4699">*Windows 行為：對於與32位伺服器通訊的32位用戶端，或與64位伺服器通訊的64位用戶端，此值會設定為應用程式進程中接收緩衝區的記憶體位址。這允許在用戶端應用程式進程中，以 CPMGetRowsOut 的資料欄欄位中收到的指標為正確的記憶體指標。否則，它會設定為0x00000000。*</span><span class="sxs-lookup"><span data-stu-id="36def-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="36def-4700">計算 [搜尋描述] 的大小，並在 [cbSeek] 欄位中進行設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="36def-4701">設定 cbReserved (的值，此值會作為資料列的位移開始) \_ cbSeek plus 0x14 的值。</span><span class="sxs-lookup"><span data-stu-id="36def-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="36def-4702">將2.2.3.15 中所指定的 CPMConnectIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="36def-4703">3.2.4.2.5 傳送 CPMFetchValueIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="36def-4704">如果用戶端收到來自伺服器的 CPMGetRowsOut 回應，且資料行的 Status 欄位設定為 StatusDeferred (0x01) 這表示屬性值未包含在 CPMGetRowsOut 訊息的 Rows 欄位中。</span><span class="sxs-lookup"><span data-stu-id="36def-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="36def-4705">在此情況下，較高層級通常會要求通訊協定用戶端透過 CPMFetchValueIn 訊息來取得值，並提供延遲屬性的 PropSpec 和 \_ wid 值（通訊協定用戶端必須在第一個 CPMFetchValueIn 訊息中使用）。</span><span class="sxs-lookup"><span data-stu-id="36def-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="36def-4706">如果這是用戶端傳送的第一個 CPMFetchValueIn 訊息，要求指定的屬性，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4707">設定訊息中的所有欄位，如2.2.3.19 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="36def-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="36def-4708">將 \_ cbSoFar 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="36def-4709">將接收的目前位元組設定為0。</span><span class="sxs-lookup"><span data-stu-id="36def-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="36def-4710">將 CPMFetchValueIn 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="36def-4711">3.2.4.2.6 傳送 CPMFreeCursorIn 要求</span><span class="sxs-lookup"><span data-stu-id="36def-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="36def-4712">一旦較高層級不再使用搜尋查詢，它就可以要求用戶端傳送 CPMFreeCursorIn 訊息，以釋放伺服器上的資源。</span><span class="sxs-lookup"><span data-stu-id="36def-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="36def-4713">收到此要求時，用戶端必須將2.2.3.28 中所指定的 CPMFreeCursorIn 訊息傳送至伺服器，其中包含上層所指定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36def-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="36def-4714">3.2.4.2.7 傳送 CPMDisconnect 訊息</span><span class="sxs-lookup"><span data-stu-id="36def-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="36def-4715">如果較高層級的索引服務沒有其他查詢，則若要釋出更多伺服器資源，應用程式可能會要求用戶端將 CPMDisconnect 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="36def-4716">收到此查詢時，用戶端必須直接以要求的方式傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="36def-4717">伺服器不會回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="36def-4718">3.2.5 訊息處理和排序規則</span><span class="sxs-lookup"><span data-stu-id="36def-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="36def-4719">當用戶端收到來自伺服器的訊息回應時，用戶端必須使用最後傳送的訊息，判斷從伺服器接收的訊息是否為用戶端所預期的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="36def-4720">與 \_ [msg] 欄位不同的所有訊息都必須被忽略。</span><span class="sxs-lookup"><span data-stu-id="36def-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="36def-4721">3.2.5.1 接收 CPMCreateQueryOut 回應</span><span class="sxs-lookup"><span data-stu-id="36def-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="36def-4722">當用戶端收到來自伺服器的 CPMCreateQueryOut 訊息回應時，用戶端必須 \_ 傳回狀態 (，而且如果狀態成功) 資料指標控制碼值傳回至較高的層級，用戶端就必須傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="36def-4723">任何進一步的動作都是最高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="36def-4724">因為較高的層級知道查詢結構，所以一定會在 CPMCreateOueryOut 訊息中傳回正確的資料指標控制碼數目。</span><span class="sxs-lookup"><span data-stu-id="36def-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="36def-4725">資料指標控制碼會以下列順序傳回：第一個控制碼是 unchaptered 資料列集，第二個控制碼是第一個章節的資料列集 (這是根據 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中指定的第一個類別的結果群組。 ) </span><span class="sxs-lookup"><span data-stu-id="36def-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="36def-4726">基於資訊的目的，較高層級必須執行下列動作，但 CISP 用戶端並不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="36def-4727">使用 CPMSetBindingsIn 來設定個別資料行的系結，並對查詢路徑執行任何後續的動作</span><span class="sxs-lookup"><span data-stu-id="36def-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="36def-4728">使用 CPMGetQueryStatusIn 來檢查查詢的執行進度。</span><span class="sxs-lookup"><span data-stu-id="36def-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="36def-4729">使用 CPMRatioFinishedIn 來要求查詢的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="36def-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="36def-4730">3.2.5.2 接收 CPMGetRowsOut 回應</span><span class="sxs-lookup"><span data-stu-id="36def-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="36def-4731">當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4732">檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="36def-4733">如果 \_ status 值為 status \_ 緩衝區 \_ 太 \_ 小 (0xC0000023) ，用戶端必須檢查最後一個訊息傳送狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="36def-4734">如果未包含 CPMGetRowsIn 訊息，則必須以無訊息方式忽略接收的訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="36def-4735">否則，用戶端必須將新的 CPMGetRowsIn 訊息傳送至伺服器，其中所有欄位都與儲存的欄位相同，不同之處在于 \_ CBREADBUFFER 必須增加 512 (但不能大於 0x4000) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="36def-4736">如果 \_ 狀態 \_ 緩衝區 \_ 太 \_ 小 (0XC0000023) ，而且最後傳送的訊息已 \_ cbReadBuffer 等於0X4000 用戶端，則必須將錯誤回報到較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="36def-4737">如果 \_ 狀態值為任何其他錯誤值，用戶端必須指出最高層級的失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="36def-4738">如果 \_ 狀態值表示成功，則結果必須指出最高的層級要求資訊，而進一步的動作則是最高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="36def-4739">基於資訊的目的，較高層級通常會執行下列動作，但內容索引服務通訊協定用戶端不會強制執行這些動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="36def-4740">如果資料列中的值代表檔識別碼、章節或書簽控點，則較高層通常會儲存它們，以便在牽涉到有效檔識別碼、章節或書簽控制碼的後續作業中使用。</span><span class="sxs-lookup"><span data-stu-id="36def-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="36def-4741">較高的圖層通常會儲存或顯示資料，或以其他方式使用資料行值。</span><span class="sxs-lookup"><span data-stu-id="36def-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="36def-4742">針對標示為 [延後] 較高層的值，將會使用 CPMFetchValueIn 訊息來提取值。</span><span class="sxs-lookup"><span data-stu-id="36def-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="36def-4743">搜尋描述也會傳回至較高的層級，而且可以由較高的圖層重複使用或檢查。</span><span class="sxs-lookup"><span data-stu-id="36def-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="36def-4744">基於資訊的目的，如果較高層要求的控制碼是在資料列中收到的章節和書簽，則可能會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="36def-4745">使用 CPMGetQueryStatusExIn 來檢查查詢的執行進度，以及其他狀態資訊，例如已篩選的檔數目、要篩選的檔、查詢所處理的檔比例、查詢中的資料列總數，以及書簽在資料列集中的位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="36def-4746">使用 CPMGetNotify 來要求伺服器通知資料列集變更的用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="36def-4747">使用 CPMGetApproximatePositionIn，在章節中要求書簽的大概位置。</span><span class="sxs-lookup"><span data-stu-id="36def-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="36def-4748">使用 CPMCompareBmkIn 來要求一章中兩個書簽的比較。</span><span class="sxs-lookup"><span data-stu-id="36def-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="36def-4749">使用 CPMRestartPositionIn 將資料指標的位置變更為資料列集的開頭。</span><span class="sxs-lookup"><span data-stu-id="36def-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="36def-4750">3.2.5.3 接收 CPMFetchValueOut 回應</span><span class="sxs-lookup"><span data-stu-id="36def-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="36def-4751">當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="36def-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="36def-4752">檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="36def-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="36def-4753">在失敗案例中，請通知較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="36def-4754">否則，請繼續下一節。</span><span class="sxs-lookup"><span data-stu-id="36def-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="36def-4755">檢查 \_ fValueExist，如果設定為0x00000000，則會通知較高的圖層，指出找不到此值。</span><span class="sxs-lookup"><span data-stu-id="36def-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="36def-4756">否則 \_ ，請將 cbValue 的位元組從 vValue 附加至目前的屬性值。</span><span class="sxs-lookup"><span data-stu-id="36def-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="36def-4757">如果 \_ \_ fMoreExists 設定為0x00000001，然後將 \_ cbValue 所接收的目前位元組遞增， \_ 並將 CPMFetchValueIn 訊息傳送至伺服器，請將 \_ cbSoFar 設定為目前接收的位元組值， \_ cbPropSpec 為零，而 \_ cbChunk 為較高層所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="36def-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="36def-4758">如果 \_ fMoreExists 設定為0x00000000，則會將目前屬性值的屬性值指定為較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="36def-4759">3.2.5.4 接收 CPMFreeCursorOut 回應</span><span class="sxs-lookup"><span data-stu-id="36def-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="36def-4760">當用戶端從伺服器收到成功的 CPMFreeCursorOut 訊息回應時，用戶端必須將 \_ cCursorsRemaining 值傳回至較高的層級。</span><span class="sxs-lookup"><span data-stu-id="36def-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="36def-4761">下列資訊僅供參考之用，不會由 CISP 用戶端強制執行。</span><span class="sxs-lookup"><span data-stu-id="36def-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="36def-4762">較高的層級預期會追蹤資料指標控制碼，而不是使用已釋放的資料指標。</span><span class="sxs-lookup"><span data-stu-id="36def-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="36def-4763">一旦 cCursorsRemaining 的數目 \_ 等於0x00000000，較高的層級就可以使用此連接來指定另一個查詢 (使用 CPMCreateQueryIn 訊息) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="36def-4764">3.2.6 計時器事件</span><span class="sxs-lookup"><span data-stu-id="36def-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="36def-4765">無。</span><span class="sxs-lookup"><span data-stu-id="36def-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="36def-4766">3.2.7 其他本機事件</span><span class="sxs-lookup"><span data-stu-id="36def-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="36def-4767">無。</span><span class="sxs-lookup"><span data-stu-id="36def-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="36def-4768">4 通訊協定範例</span><span class="sxs-lookup"><span data-stu-id="36def-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="36def-4769">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="36def-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="36def-4770">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="36def-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="36def-4771">4.1 範例1</span><span class="sxs-lookup"><span data-stu-id="36def-4771">4.1 Example 1</span></span>

<span data-ttu-id="36def-4772">在下列範例中，我們假設電腦 A 上的使用者 JOHN 想要從儲存在伺服器 X 上的檔集的目錄系統中，取得包含 "Microsoft" 這個字的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="36def-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="36def-4773">讓我們假設電腦 A 正在執行32位的 Windows XP 作業系統，而電腦 X 正在執行32位的 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="36def-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="36def-4774">使用者啟動搜尋應用程式，並輸入搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="36def-4775">接著，應用程式會將搜尋查詢傳遞給通訊協定用戶端。</span><span class="sxs-lookup"><span data-stu-id="36def-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="36def-4776">通訊協定用戶端建立與索引伺服器 X 的連接。通訊協定用戶端使用具名管道 \\ 管道 \\ CI \_ SKADS，透過 SMB 連線到伺服器 X。</span><span class="sxs-lookup"><span data-stu-id="36def-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="36def-4777">然後，通訊協定用戶端會使用下列值來準備 CPMConnectIn 訊息：</span><span class="sxs-lookup"><span data-stu-id="36def-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="36def-4778">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4779">**\_ msg** 設定為0x000000C8，表示這是 CPMConnectIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="36def-4780">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4781">**\_ ulChecksum** 包含總和檢查碼，依3.2.4 區段中的指定進行計算。</span><span class="sxs-lookup"><span data-stu-id="36def-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="36def-4782">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="36def-4783">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4784">**\_ iClientVersion** 設定為0x00000008，表示伺服器要驗證總和檢查碼欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="36def-4785">**\_ fClientIsRemote** 設定為0x00000001，表示伺服器是遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="36def-4786">**\_ cbBlob1** 會設定為結合 cPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36def-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="36def-4787">**\_ cbBlob2** 設定為 0x00000004 (表示沒有任何額外的屬性集) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="36def-4788">**MachineName** 設定為。</span><span class="sxs-lookup"><span data-stu-id="36def-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="36def-4789">**UserName** 設定為 JOHN。</span><span class="sxs-lookup"><span data-stu-id="36def-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="36def-4790">**cPropSets** 設定為0x00000002。</span><span class="sxs-lookup"><span data-stu-id="36def-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="36def-4791">**PropertySet1** 欄位的類型為 CDbPropSet。</span><span class="sxs-lookup"><span data-stu-id="36def-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="36def-4792">組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="36def-4793">**GuidPropSet** 欄位設定為 A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="36def-4794">**cProperties** 欄位設定為0x00000004。</span><span class="sxs-lookup"><span data-stu-id="36def-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="36def-4795">**aProps** 欄位是 CDbProp 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="36def-4796">針對 **aProps \[ 0 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="36def-4797">**PropId** 會設定為 0X00000002 (DBPROP \_ CI \_ 類別目錄 \_ 名稱) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="36def-4798">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="36def-4799">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4800">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="36def-4801">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) </span><span class="sxs-lookup"><span data-stu-id="36def-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="36def-4802">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="36def-4803">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4804">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="36def-4805">**vType** 設定為 0X001F (VT \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="36def-4806">**vValue** 會設定為 "SYSTEM"，也就是所需的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="36def-4807">針對 **aProps \[ 1 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="36def-4808">**PropId** 設定為 0X00000007 (DBPROP \_ CI \_ 查詢 \_ 類型) </span><span class="sxs-lookup"><span data-stu-id="36def-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="36def-4809">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="36def-4810">**DBPROPSTATUS** 是設定為 to0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="36def-4811">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="36def-4812">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="36def-4813">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="36def-4814">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4815">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="36def-4816">**vType** 設定為 0X0003 (VT \_ I4) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="36def-4817">**vValue** 會設定為 0X00000000 (CiNormal) ，這表示它是一般查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="36def-4818">針對 **aProps \[ 2 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="36def-4819">**PropId** 會設定為 0X00000004 (DBPROP \_ CI \_ 範圍 \_ 旗標) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="36def-4820">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="36def-4821">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4822">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="36def-4823">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="36def-4824">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="36def-4825">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4826">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="36def-4827">**vType**： 0X1003 (VT \_ 向量 \| VT \_ I4) </span><span class="sxs-lookup"><span data-stu-id="36def-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="36def-4828">**vValue**： 0x00000001/0x00000001 (一個具有值 1) 的元素，這表示搜尋子資料夾</span><span class="sxs-lookup"><span data-stu-id="36def-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="36def-4829">針對 **aProps \[ 3 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="36def-4830">**PropId**： 0X00000003 (DBPROP \_ CI \_ 包含 \_ 範圍) </span><span class="sxs-lookup"><span data-stu-id="36def-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="36def-4831">**DBPROPOPTIONS**：0x0000000</span><span class="sxs-lookup"><span data-stu-id="36def-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="36def-4832">**DBPROPSTATUS**：0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="36def-4833">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="36def-4834">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="36def-4835">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="36def-4836">**ulID** 設定為0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="36def-4837">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="36def-4838">**vType** 設定為 0X101F (VT \_ VECTOR \| vt \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="36def-4839">**vValue** 設定為 0x00000001/0x00000002/" \\ " (一個元素，其中有2個字元的 null 終止字串) ，亦即根範圍。</span><span class="sxs-lookup"><span data-stu-id="36def-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="36def-4840">**PropertySet2** 欄位的類型為 CDbPropSet。</span><span class="sxs-lookup"><span data-stu-id="36def-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="36def-4841">組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="36def-4842">**GuidPropSet** 設定為 AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="36def-4843">**cProperties** 欄位設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="36def-4844">**AProps** 欄位是 CDbProp 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="36def-4845">針對 **aProps \[ 0 \]** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="36def-4846">**PropId** 會設定為 0X00000002 (DBPROP \_ 機) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="36def-4847">**DBPROPOPTIONS** 設定為0x0000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="36def-4848">**DBPROPSTATUS** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4849">針對 **ColId** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="36def-4850">**eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) ，</span><span class="sxs-lookup"><span data-stu-id="36def-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="36def-4851">**GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="36def-4852">**ulID** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-4853">針對 **vValue** 元素：</span><span class="sxs-lookup"><span data-stu-id="36def-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="36def-4854">**vType**： 0X0008 (VT \_ BSTR) </span><span class="sxs-lookup"><span data-stu-id="36def-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="36def-4855">**vValue**： 0x04/"X" (4 個位元組/以 null 結束的 Unicode 字串) ，表示 "X"-伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="36def-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="36def-4856">**cExtPropSet** 欄位設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4857">**aPropertySets** 陣列不存在。</span><span class="sxs-lookup"><span data-stu-id="36def-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="36def-4858">視需要填入各種填補欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="36def-4859">訊息會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="36def-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="36def-4860">伺服器會驗證 **\_ ulChecksum** 是否正確、確認使用者已獲授權提出此要求，並以 CPMConnectOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="36def-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="36def-4861">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4862">**\_ msg** 設定為0x000000C8，表示這是 CPMConnectOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="36def-4863">**\_ 狀態** 會設為0X0000000，表示成功。</span><span class="sxs-lookup"><span data-stu-id="36def-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="36def-4864">**\_ ulChecksum** 設定為0。</span><span class="sxs-lookup"><span data-stu-id="36def-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="36def-4865">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="36def-4866">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4867">**\_ serverVersion** 欄位設定為 0x00000007 (32 位 windows XP 或32位 windows Server 2003) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="36def-4868">**\_ 保留** 的欄位會填入任意資料。</span><span class="sxs-lookup"><span data-stu-id="36def-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="36def-4869">用戶端會準備 CPMCreateQueryIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="36def-4870">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4871">**\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="36def-4872">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4873">**\_ ulChecksum** 包含總和檢查碼，根據3.2.5 計算。</span><span class="sxs-lookup"><span data-stu-id="36def-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="36def-4874">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="36def-4875">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4876">[**大小**] 欄位設定為訊息其餘部分的大小。</span><span class="sxs-lookup"><span data-stu-id="36def-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="36def-4877">**CColumnSetPresent** 欄位設定為0x01。</span><span class="sxs-lookup"><span data-stu-id="36def-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="36def-4878">**ColumnSet** 欄位的類型為 CColumnSet。</span><span class="sxs-lookup"><span data-stu-id="36def-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="36def-4879">組成此欄位的 CColumnSet 結構設定如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="36def-4880">**\_ count** 欄位設定為0x00000001，表示傳回一個資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="36def-4881">**索引** 陣列是0x00000000，表示 aPropSpec 中的第一個專案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36def-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="36def-4882">**CRestrictionPresent** 欄位設定為0x01，表示 **限制** 欄位存在。</span><span class="sxs-lookup"><span data-stu-id="36def-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="36def-4883">**限制** 欄位的類型為 CRestriction，且設定為：</span><span class="sxs-lookup"><span data-stu-id="36def-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="36def-4884">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="36def-4885">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4886">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="36def-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="36def-4887">PRSPEC 的屬性設定為 GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13，代表檔主體。</span><span class="sxs-lookup"><span data-stu-id="36def-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="36def-4888">**\_ Cc** 設為0x00000009。</span><span class="sxs-lookup"><span data-stu-id="36def-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="36def-4889">**\_ pwcsphrase** 會設定為字串 "Microsoft"。</span><span class="sxs-lookup"><span data-stu-id="36def-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="36def-4890">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="36def-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="36def-4891">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="36def-4892">**CSortPresent** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="36def-4893">**CCategorizationSetPresent** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="36def-4894">**RowSetProperties** 的設定如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="36def-4895">**\_ uBooleanOptions** 會設定為 0x00000001 (順序) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="36def-4896">**\_ ulMaxOpenRows** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4897">**\_ ulMemoryUsage** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4898">\_**cMaxResults** 設定為 0x00000100 (最多傳回256個數據列) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="36def-4899">**\_ cCmdTimeOut** 設定為 0x00000000 (不會) 超時。</span><span class="sxs-lookup"><span data-stu-id="36def-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="36def-4900">**PidMapper** 設定為：</span><span class="sxs-lookup"><span data-stu-id="36def-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="36def-4901">**\_ count** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="36def-4902">**\_ aPropSpec** 設定為 02608C9EEBAC \_ 的 GUID B725F130-47EF-101A-A5-F1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="36def-4903">伺服器會處理它，並以 CPMCreateQueryOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="36def-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="36def-4904">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4905">**\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="36def-4906">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="36def-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="36def-4907">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="36def-4908">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="36def-4909">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4910">**\_ fTrueSeqeuntial** 設定為0x00000000，表示查詢可以使用索引。</span><span class="sxs-lookup"><span data-stu-id="36def-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="36def-4911">**\_ fWorkIdUnique** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="36def-4912">**ACursors** 陣列只包含一個元素，代表這個查詢的資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="36def-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="36def-4913">此值取決於伺服器的狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="36def-4914">讓我們假設傳回的值為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="36def-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="36def-4915">用戶端發出 CPMSetBindingsIn 要求訊息來定義資料列的格式。</span><span class="sxs-lookup"><span data-stu-id="36def-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="36def-4916">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4917">**\_ msg** 設定為0x000000D0，表示這是 CPMSetBindingsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="36def-4918">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="36def-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="36def-4919">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="36def-4920">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="36def-4921">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4922">**\_ hCursor** 設定為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="36def-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="36def-4923">**\_ cbRow** 設定為 0x10 (夠大，足以容納) 的資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="36def-4924">**\_ cbBindingDesc** 會設定為結合的 **\_ cColumns** 和 **\_ aColumns** 欄位大小。</span><span class="sxs-lookup"><span data-stu-id="36def-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="36def-4925">**\_ cColumns** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="36def-4926">**\_ aColumns** 陣列設定為包含一個 CTableColumn 結構，其中包含：</span><span class="sxs-lookup"><span data-stu-id="36def-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="36def-4927">**\_ PropSpec** 設定為 02608c9eebac \_ 的 GUID b725f130-47ef-101a-a5-f1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。</span><span class="sxs-lookup"><span data-stu-id="36def-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="36def-4928">**\_ vType** 設定為 0x0015 (VT \_UI8) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="36def-4929">**\_ ValueUsed** 會設定為在資料列) 中傳輸的 0x01 (資料行。</span><span class="sxs-lookup"><span data-stu-id="36def-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="36def-4930">**\_ ValueOffset** 會在資料列) 的開頭設定為 0x0002 (。</span><span class="sxs-lookup"><span data-stu-id="36def-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="36def-4931">**\_ ValueSize** 設定為 0x08 (VT \_ 的大小UI8) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="36def-4932">**\_ StatusUsed** 設定為0x01。</span><span class="sxs-lookup"><span data-stu-id="36def-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="36def-4933">**\_ StatusOffset** 設定為0x0A。</span><span class="sxs-lookup"><span data-stu-id="36def-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="36def-4934">**\_ LengthUsed** 設定為0x00。</span><span class="sxs-lookup"><span data-stu-id="36def-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="36def-4935">伺服器會處理它，並以 CPMSetBindingsIn 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="36def-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="36def-4936">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4937">**\_ msg** 設定為0x000000D0。</span><span class="sxs-lookup"><span data-stu-id="36def-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="36def-4938">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="36def-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="36def-4939">**\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="36def-4940">**\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="36def-4941">用戶端發出 CPMGetRowsIn 要求訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="36def-4942">讓我們假設用戶端已準備好接受100個數據列，而且想要以遞增的順序進行。</span><span class="sxs-lookup"><span data-stu-id="36def-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="36def-4943">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4944">**\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsIn 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="36def-4945">**\_ 狀態** 設定為0x00000000</span><span class="sxs-lookup"><span data-stu-id="36def-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="36def-4946">**\_ ulChecksum** 包含總和檢查碼，依區段0計算。</span><span class="sxs-lookup"><span data-stu-id="36def-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="36def-4947">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="36def-4948">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4949">**\_ hCursor** 設定為0xAAAAAAAA。</span><span class="sxs-lookup"><span data-stu-id="36def-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="36def-4950">**\_ cRowsToTransfer** 設定為0x00000064。</span><span class="sxs-lookup"><span data-stu-id="36def-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="36def-4951">從) 的系結中， **\_ cRowWidth** 設為 0x00000010 (。</span><span class="sxs-lookup"><span data-stu-id="36def-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="36def-4952">**\_ cbSeek** 會設定為0x14，也就是結合 eType、 \_ chapt 和 CRowSeekNext 欄位的大小。</span><span class="sxs-lookup"><span data-stu-id="36def-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="36def-4953">**\_ cbReserved** 設定為 0x18 (0x14 plus \_ cbSeek) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="36def-4954">**\_ cbReadBuffer** 設定為 0x800 (0x64 \* 0x10 進位到下一個 0x200) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="36def-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="36def-4955">**\_ ulClientBase** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4956">**\_ fBwdfetch** 設定為0x00000000，表示資料列會以正向順序提取。</span><span class="sxs-lookup"><span data-stu-id="36def-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="36def-4957">**eType** 設定為0x0000001，表示用戶端需要下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="36def-4958">**\_ chapt** 設定為 0 (不是) 的章節化結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="36def-4959">**SeekDescription** 設定為 CRowSeekNext。</span><span class="sxs-lookup"><span data-stu-id="36def-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="36def-4960">CRowSeekNext 結構包含下列值：</span><span class="sxs-lookup"><span data-stu-id="36def-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="36def-4961">**CiTblChapt** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4962">**\_ hRegion** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4963">**\_ cSkip** 設定為0，表示用戶端不想略過資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="36def-4964">伺服器會處理它，並以 CPMGetRowsOut 訊息回應。</span><span class="sxs-lookup"><span data-stu-id="36def-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="36def-4965">讓我們假設伺服器找到的100檔中包含 "Microsoft" 這個字。</span><span class="sxs-lookup"><span data-stu-id="36def-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="36def-4966">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4967">**\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsOut 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="36def-4968">**\_ 狀態** 設定為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="36def-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="36def-4969">**\_ ulChecksum** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4970">**\_ ulReserved2** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="36def-4971">訊息本文的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4972">**\_ CRowsReturned** 設定為0x00000064。</span><span class="sxs-lookup"><span data-stu-id="36def-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="36def-4973">**eType** 設定為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="36def-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="36def-4974">**\_ chapt** 設定為 0x00000000 (不是) 的章節化結果。</span><span class="sxs-lookup"><span data-stu-id="36def-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="36def-4975">**SeekDescription** 包含 CRowSeekNext 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="36def-4976">**CiTblChapt** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4977">**\_ hRegion** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="36def-4978">**\_ cSkip** 設定為0，表示用戶端不想略過資料列。</span><span class="sxs-lookup"><span data-stu-id="36def-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="36def-4979">資料 **列** 包含100檔的大小，其中包含 "Microsoft" 這個字。</span><span class="sxs-lookup"><span data-stu-id="36def-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="36def-4980">由於這是固定大小的資料，因此它只會以100、8位元組不帶正負號的整數的清單結構化。</span><span class="sxs-lookup"><span data-stu-id="36def-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="36def-4981">用戶端會傳送 CPMDisconnect 訊息來結束連接。</span><span class="sxs-lookup"><span data-stu-id="36def-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="36def-4982">訊息標頭的填入方式如下：</span><span class="sxs-lookup"><span data-stu-id="36def-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="36def-4983">**\_ msg** 設定為0x000000C9，表示這是 CPMDisconnect 訊息。</span><span class="sxs-lookup"><span data-stu-id="36def-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="36def-4984">**\_ 狀態** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="36def-4985">**\_ ulChecksum** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="36def-4986">伺服器會處理訊息，並移除所有的用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="36def-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="36def-4987">4.2 範例2</span><span class="sxs-lookup"><span data-stu-id="36def-4987">4.2 Example 2</span></span>

<span data-ttu-id="36def-4988">在上述範例中，查詢相當簡單。</span><span class="sxs-lookup"><span data-stu-id="36def-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="36def-4989">現在讓我們考慮稍微複雜一點的查詢。</span><span class="sxs-lookup"><span data-stu-id="36def-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="36def-4990">讓我們假設使用者想要取出包含下列兩個字的檔案大小： "Microsoft" 和 "Office"。</span><span class="sxs-lookup"><span data-stu-id="36def-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="36def-4991">這是藉由變更在步驟5中傳送的 CPMCreateQueryIn 訊息所包含的限制欄位來指定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36def-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="36def-4992">**限制** 欄位的類型為 CRestriction，且設定為：</span><span class="sxs-lookup"><span data-stu-id="36def-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="36def-4993">**\_ ulType** 設定為 0x00000004 (RTAnd) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="36def-4994">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="36def-4995">欄位的其餘部分包含 CNodeRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="36def-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="36def-4996">**\_ cNode** 設定為0X00000002，表示 paNode 陣列中有兩個節點。</span><span class="sxs-lookup"><span data-stu-id="36def-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="36def-4997">**\_ PaNode** 欄位是兩個 CRestriction 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="36def-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="36def-4998">**\_ paNode \[ 0 \]** 包含：</span><span class="sxs-lookup"><span data-stu-id="36def-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="36def-4999">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="36def-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="36def-5000">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-5001">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="36def-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="36def-5002">PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。</span><span class="sxs-lookup"><span data-stu-id="36def-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="36def-5003">**\_ Cc** 設為0x00000009。</span><span class="sxs-lookup"><span data-stu-id="36def-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="36def-5004">**\_ pwcsphrase** 會設定為字串 "Microsoft"。</span><span class="sxs-lookup"><span data-stu-id="36def-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="36def-5005">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="36def-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="36def-5006">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="36def-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="36def-5007">**\_ paNode \[ 1 \]** 包含：</span><span class="sxs-lookup"><span data-stu-id="36def-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="36def-5008">**\_ ulType** 設定為 0x00000004 (RTContent) 。</span><span class="sxs-lookup"><span data-stu-id="36def-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="36def-5009">**\_ 權數** 設定為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="36def-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="36def-5010">欄位的其餘部分包含 CContentRestriction 結構：</span><span class="sxs-lookup"><span data-stu-id="36def-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="36def-5011">PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。</span><span class="sxs-lookup"><span data-stu-id="36def-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="36def-5012">**\_ Cc** 設為0x00000006。</span><span class="sxs-lookup"><span data-stu-id="36def-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="36def-5013">**\_ pwcsphrase** 會設定為 "Office" 字串。</span><span class="sxs-lookup"><span data-stu-id="36def-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="36def-5014">針對英文) ， **\_ lcid** 設定為 0x409 (。</span><span class="sxs-lookup"><span data-stu-id="36def-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="36def-5015">**\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。</span><span class="sxs-lookup"><span data-stu-id="36def-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="36def-5016">5 安全性</span><span class="sxs-lookup"><span data-stu-id="36def-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="36def-5017">5.1 實作者的安全性考量</span><span class="sxs-lookup"><span data-stu-id="36def-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="36def-5018">索引安全內容的索引編制可考慮使用 SMB Ms-chap 提供的使用者內容 \[ \] 來修剪搜尋結果，並且只傳回呼叫者可存取的內容。</span><span class="sxs-lookup"><span data-stu-id="36def-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="36def-5019">5.2 安全性參數的索引</span><span class="sxs-lookup"><span data-stu-id="36def-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="36def-5020">安全性參數</span><span class="sxs-lookup"><span data-stu-id="36def-5020">Security Parameter</span></span>  | <span data-ttu-id="36def-5021">區段</span><span class="sxs-lookup"><span data-stu-id="36def-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="36def-5022">模擬等級</span><span class="sxs-lookup"><span data-stu-id="36def-5022">Impersonation level</span></span> | <span data-ttu-id="36def-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="36def-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="36def-5024">6個版本特定行為的索引</span><span class="sxs-lookup"><span data-stu-id="36def-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="36def-5025">版本特定行為</span><span class="sxs-lookup"><span data-stu-id="36def-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="36def-5026">區段</span><span class="sxs-lookup"><span data-stu-id="36def-5026">Section</span></span>   | <span data-ttu-id="36def-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="36def-5027">Windows 2000</span></span> | <span data-ttu-id="36def-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="36def-5028">Windows XP</span></span> | <span data-ttu-id="36def-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36def-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="36def-5030">此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。</span><span class="sxs-lookup"><span data-stu-id="36def-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="36def-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="36def-5031">1.3.2</span></span>     | <span data-ttu-id="36def-5032">X</span><span class="sxs-lookup"><span data-stu-id="36def-5032">X</span></span>            | <span data-ttu-id="36def-5033">X</span><span class="sxs-lookup"><span data-stu-id="36def-5033">X</span></span>          | <span data-ttu-id="36def-5034">X</span><span class="sxs-lookup"><span data-stu-id="36def-5034">X</span></span>                   |
| <span data-ttu-id="36def-5035">應用程式通常會與 OLE DB 介面包裝函式互動</span><span class="sxs-lookup"><span data-stu-id="36def-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="36def-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="36def-5036">1.4</span></span>       | <span data-ttu-id="36def-5037">X</span><span class="sxs-lookup"><span data-stu-id="36def-5037">X</span></span>            | <span data-ttu-id="36def-5038">X</span><span class="sxs-lookup"><span data-stu-id="36def-5038">X</span></span>          | <span data-ttu-id="36def-5039">X</span><span class="sxs-lookup"><span data-stu-id="36def-5039">X</span></span>                   |
| <span data-ttu-id="36def-5040">NTSTATUS 值</span><span class="sxs-lookup"><span data-stu-id="36def-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="36def-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="36def-5041">1.8</span></span>       | <span data-ttu-id="36def-5042">X</span><span class="sxs-lookup"><span data-stu-id="36def-5042">X</span></span>            | <span data-ttu-id="36def-5043">X</span><span class="sxs-lookup"><span data-stu-id="36def-5043">X</span></span>          | <span data-ttu-id="36def-5044">X</span><span class="sxs-lookup"><span data-stu-id="36def-5044">X</span></span>                   |
| <span data-ttu-id="36def-5045">用戶端會 \_ 在每個訊息標頭中設定 [狀態] 欄位。</span><span class="sxs-lookup"><span data-stu-id="36def-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="36def-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="36def-5046">2.2.2</span></span>     | <span data-ttu-id="36def-5047">X</span><span class="sxs-lookup"><span data-stu-id="36def-5047">X</span></span>            | <span data-ttu-id="36def-5048">X</span><span class="sxs-lookup"><span data-stu-id="36def-5048">X</span></span>          | <span data-ttu-id="36def-5049">X</span><span class="sxs-lookup"><span data-stu-id="36def-5049">X</span></span>                   |
| <span data-ttu-id="36def-5050">cPendingScans 值通常是零</span><span class="sxs-lookup"><span data-stu-id="36def-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="36def-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="36def-5051">2.2.3.1</span></span>   | <span data-ttu-id="36def-5052">X</span><span class="sxs-lookup"><span data-stu-id="36def-5052">X</span></span>            | <span data-ttu-id="36def-5053">X</span><span class="sxs-lookup"><span data-stu-id="36def-5053">X</span></span>          | <span data-ttu-id="36def-5054">X</span><span class="sxs-lookup"><span data-stu-id="36def-5054">X</span></span>                   |
| <span data-ttu-id="36def-5055">iClientVersion 值</span><span class="sxs-lookup"><span data-stu-id="36def-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="36def-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="36def-5056">2.2.3.6</span></span>   | <span data-ttu-id="36def-5057">X</span><span class="sxs-lookup"><span data-stu-id="36def-5057">X</span></span>            | <span data-ttu-id="36def-5058">X</span><span class="sxs-lookup"><span data-stu-id="36def-5058">X</span></span>          | <span data-ttu-id="36def-5059">X</span><span class="sxs-lookup"><span data-stu-id="36def-5059">X</span></span>                   |
| <span data-ttu-id="36def-5060">\_cbChunk 值</span><span class="sxs-lookup"><span data-stu-id="36def-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="36def-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="36def-5061">2.2.3.19</span></span>  | <span data-ttu-id="36def-5062">X</span><span class="sxs-lookup"><span data-stu-id="36def-5062">X</span></span>            | <span data-ttu-id="36def-5063">X</span><span class="sxs-lookup"><span data-stu-id="36def-5063">X</span></span>          | <span data-ttu-id="36def-5064">X</span><span class="sxs-lookup"><span data-stu-id="36def-5064">X</span></span>                   |
| <span data-ttu-id="36def-5065">32位和64位的記憶體位址</span><span class="sxs-lookup"><span data-stu-id="36def-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="36def-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="36def-5066">3.2.4.2.4</span></span> | <span data-ttu-id="36def-5067">X</span><span class="sxs-lookup"><span data-stu-id="36def-5067">X</span></span>            | <span data-ttu-id="36def-5068">X</span><span class="sxs-lookup"><span data-stu-id="36def-5068">X</span></span>          | <span data-ttu-id="36def-5069">X</span><span class="sxs-lookup"><span data-stu-id="36def-5069">X</span></span>                   |



 

 

 






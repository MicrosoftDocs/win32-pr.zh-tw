---
description: Advanced Query 語法 (AQS) 是 Windows Search 用來查詢索引以及精簡和縮小搜尋參數的預設查詢語法。
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: 以程式設計方式使用 Advanced 查詢語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970384"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="7e109-103">以程式設計方式使用 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="7e109-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="7e109-104">Advanced Query 語法 (AQS) 是 Windows Search 用來查詢索引以及精簡和縮小搜尋參數的預設查詢語法。</span><span class="sxs-lookup"><span data-stu-id="7e109-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="7e109-105">開發人員會採用 AQS 來以程式設計方式建立查詢， (以及使用者將其搜尋參數縮小) 。</span><span class="sxs-lookup"><span data-stu-id="7e109-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="7e109-106">標準 AQS 是在 Windows 7 中引進的，而且必須在 Windows 7 和更新版本中用來以程式設計方式產生 AQS 查詢。</span><span class="sxs-lookup"><span data-stu-id="7e109-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="7e109-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="7e109-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7e109-108">關於 Advanced Query 語法</span><span class="sxs-lookup"><span data-stu-id="7e109-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="7e109-109">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="7e109-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7e109-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="7e109-111">以當地語言使用關鍵字</span><span class="sxs-lookup"><span data-stu-id="7e109-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="7e109-112">Windows 7 中的標準 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="7e109-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="7e109-113">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="7e109-114">查詢運算子</span><span class="sxs-lookup"><span data-stu-id="7e109-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="7e109-115">查詢值</span><span class="sxs-lookup"><span data-stu-id="7e109-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="7e109-116">範圍限制</span><span class="sxs-lookup"><span data-stu-id="7e109-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="7e109-117">其他資源</span><span class="sxs-lookup"><span data-stu-id="7e109-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7e109-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e109-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="7e109-119">關於 Advanced Query 語法</span><span class="sxs-lookup"><span data-stu-id="7e109-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="7e109-120">查詢是由與 AND、OR 和 NOT 連接的基本查詢所組成，如下列範例語法所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="7e109-121">AQS 不區分大小寫，但 AND、OR 和 NOT 除外，其必須全部為大寫。</span><span class="sxs-lookup"><span data-stu-id="7e109-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="7e109-122">如果查詢有兩個以上的使用和或或，則不論是 AND 或 OR，它們都會從左至右系結。</span><span class="sxs-lookup"><span data-stu-id="7e109-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="7e109-123">也就是說，查詢 "apple AND 梨 OR 梅紅" 將會被解釋為 " (apple AND 梨) 或梅紅"，而查詢 "apple OR 梨 AND 梅紅" 將會被視為撰寫為「 (apple 或梨) 和梅紅」。</span><span class="sxs-lookup"><span data-stu-id="7e109-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="7e109-124">因此，如果檔包含梅紅這個字，但不是 apple，也不是使用梨，則第一個查詢會傳回它，但第二個查詢則不會傳回。</span><span class="sxs-lookup"><span data-stu-id="7e109-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="7e109-125">因此，我們建議您針對任何混合和和或的查詢使用明確括弧，以避免發生錯誤或誤解。</span><span class="sxs-lookup"><span data-stu-id="7e109-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="7e109-126">基本查詢會搜尋符合屬性之限制的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="7e109-127">基本查詢的唯一必要部分是限制或搜尋值。</span><span class="sxs-lookup"><span data-stu-id="7e109-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="7e109-128">如果您未指定屬性，Windows Search 會搜尋所有屬性。</span><span class="sxs-lookup"><span data-stu-id="7e109-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="7e109-129"><restr> 表示搜尋限制。</span><span class="sxs-lookup"><span data-stu-id="7e109-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="7e109-130">以下是適用于基本查詢的表單：</span><span class="sxs-lookup"><span data-stu-id="7e109-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="7e109-131">屬性是由關鍵字（例如作者或大小）或標準屬性名稱（例如 [DateModified](../properties/props-system-datemodified.md)）所指定。</span><span class="sxs-lookup"><span data-stu-id="7e109-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="7e109-132">屬性的有效表單如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="7e109-133">運算子表示作業，例如 < 或 =。</span><span class="sxs-lookup"><span data-stu-id="7e109-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="7e109-134">如需有效運算子的清單，請參閱本主題稍後的「查詢運算子」一節。</span><span class="sxs-lookup"><span data-stu-id="7e109-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="7e109-135">基本限制是可在不使用括弧撰寫的屬性上進行簡單的限制：</span><span class="sxs-lookup"><span data-stu-id="7e109-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="7e109-136">限制是搜尋值，例如數值或字串值（選擇性地使用運算子）。</span><span class="sxs-lookup"><span data-stu-id="7e109-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="7e109-137">有效的限制表單如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="7e109-138">如果您未指定運算子，Windows Search 會為您的查詢選擇最適當的運算子：</span><span class="sxs-lookup"><span data-stu-id="7e109-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="7e109-139">若為字串屬性，則 \_ 會假設為 COP 單字 \_ STARTSWITH $< 運算子。</span><span class="sxs-lookup"><span data-stu-id="7e109-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="7e109-140">若為其他所有屬性，則 \_ 會假設 COP 等於 = 運算子。</span><span class="sxs-lookup"><span data-stu-id="7e109-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="7e109-141">若要以程式設計方式使用 AQS，建議您一律具有明確的運算子。</span><span class="sxs-lookup"><span data-stu-id="7e109-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="7e109-142">搜尋簡單值或值範圍的有效表單如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="7e109-143">簡單的值可以包含下列任何一種類型：</span><span class="sxs-lookup"><span data-stu-id="7e109-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="7e109-144">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-144">Examples</span></span>

<span data-ttu-id="7e109-145">此查詢會搜尋包含「上一季」、Theresa 或授權作者所撰寫的檔，並將其儲存到資料夾 MyDocs 的查詢，其中結合了三個基本查詢，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="7e109-146">三個基本查詢如下：</span><span class="sxs-lookup"><span data-stu-id="7e109-146">The three basic queries are:</span></span>

-   <span data-ttu-id="7e109-147">「上一季」</span><span class="sxs-lookup"><span data-stu-id="7e109-147">"last quarter"</span></span>
-   <span data-ttu-id="7e109-148">作者： (theresa 或授權) </span><span class="sxs-lookup"><span data-stu-id="7e109-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="7e109-149">資料夾： MyDocs</span><span class="sxs-lookup"><span data-stu-id="7e109-149">folder:MyDocs</span></span>

<span data-ttu-id="7e109-150">使用標準語法的基本查詢為：</span><span class="sxs-lookup"><span data-stu-id="7e109-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="7e109-151">屬性</span><span class="sxs-lookup"><span data-stu-id="7e109-151">Properties</span></span>

<span data-ttu-id="7e109-152">屬性是由關鍵字所參考，可以是 Windows 7 和更新版本中的標準屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7e109-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="7e109-153">Windows UI 中的 AQS 可以使用標籤，而不是 [標準的屬性](../properties/props-system-author.md)名稱，例如作者，而不是 author。</span><span class="sxs-lookup"><span data-stu-id="7e109-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="7e109-154">在 Windows Vista 及更早版本中，不論 UI 語言為何，都可以使用英文標籤。</span><span class="sxs-lookup"><span data-stu-id="7e109-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="7e109-155">在 Windows 7 和更新版本中，Windows Search 只能辨識目前預設 UI 語言中的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="7e109-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="7e109-156">自訂屬性的支援</span><span class="sxs-lookup"><span data-stu-id="7e109-156">Support for Custom Properties</span></span>

<span data-ttu-id="7e109-157">在 Windows Vista 及更早版本中，AQS 中無法使用自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="7e109-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="7e109-158">在 Windows 7 和更新版本中，AQS 會使用向屬性系統註冊的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="7e109-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="7e109-159">如需有關建立自訂屬性的詳細資訊，請參閱 [屬性系統](../properties/building-property-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="7e109-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="7e109-160">Windows 8 中的日期時間屬性</span><span class="sxs-lookup"><span data-stu-id="7e109-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="7e109-161">從 Windows 8 開始，DateTime 屬性 (如 [DateModified](../properties/props-system-datemodified.md)) 支援 [ISO-8601](https://www.w3.org/TR/NOTE-datetime)指定的標準日期和時間格式，選擇性地包括 UTC 時區。</span><span class="sxs-lookup"><span data-stu-id="7e109-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="7e109-162">**Windows 8 及更早版本，不含 UTC 時區的日期時間：** *YYYY* - *MM* - *DDThh*：*MM*：*ss*</span><span class="sxs-lookup"><span data-stu-id="7e109-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="7e109-163">無論使用者或系統的地區設定為何，此格式都會指定本地時間。</span><span class="sxs-lookup"><span data-stu-id="7e109-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="7e109-164">**Windows 8，日期時間（UTC 時區）：** *YYYY* - *MM* - *DDThh*：*MM*：*ssTZD*</span><span class="sxs-lookup"><span data-stu-id="7e109-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="7e109-165">此格式會指定指定之 UTC 時區的時間。</span><span class="sxs-lookup"><span data-stu-id="7e109-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="7e109-166">以當地語言使用關鍵字</span><span class="sxs-lookup"><span data-stu-id="7e109-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="7e109-167">在 Windows 7 （含）以後版本中，助憶鍵關鍵字僅適用于系統語言，例如德文關鍵字（僅限德文版作業系統）和英文關鍵字（僅限英文版作業系統）。</span><span class="sxs-lookup"><span data-stu-id="7e109-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="7e109-168">[System. author](../properties/props-system-author.md) 是標準關鍵字，而 system.string 屬性的助憶鍵值為 author，例如。</span><span class="sxs-lookup"><span data-stu-id="7e109-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="7e109-169">引進標準關鍵字可彌補在所有作業系統上（不論語言為何）都不能完全辨識英文助憶鍵關鍵字的事實，就像是 Windows Vista 和更早版本中的情況一樣。</span><span class="sxs-lookup"><span data-stu-id="7e109-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="7e109-170">在 Windows 7 和更新版本中，Windows Search 只會辨識目前預設語言的關鍵字，而不是以英文為目前的預設值。</span><span class="sxs-lookup"><span data-stu-id="7e109-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="7e109-171">我們建議開發人員一律使用標準語法，讓其應用程式不會有關鍵詞的語言問題。</span><span class="sxs-lookup"><span data-stu-id="7e109-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="7e109-172">Windows 7 中的標準 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="7e109-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="7e109-173">Windows 7 中的關鍵字已引進標準語法。</span><span class="sxs-lookup"><span data-stu-id="7e109-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="7e109-174">具有標準屬性的查詢範例為 `System.Message.FromAddress:=me@microsoft.com` 。</span><span class="sxs-lookup"><span data-stu-id="7e109-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="7e109-175">在 Windows 7 和更新版本上執行的應用程式中撰寫查詢程式碼時，您必須使用標準語法以程式設計方式產生 AQS 查詢。</span><span class="sxs-lookup"><span data-stu-id="7e109-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="7e109-176">如果您未使用標準語法，而您的應用程式是以與應用程式程式碼語言不同的地區設定或 UI 語言進行部署，您的查詢將不會正確地解讀。</span><span class="sxs-lookup"><span data-stu-id="7e109-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="7e109-177">標準關鍵字語法的慣例如下：</span><span class="sxs-lookup"><span data-stu-id="7e109-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="7e109-178">屬性的標準語法是其標準名稱，例如 `System.Photo.LightSource` 。</span><span class="sxs-lookup"><span data-stu-id="7e109-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="7e109-179">標準名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7e109-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="7e109-180">布林運算子的標準語法是由關鍵字 AND、OR 和 NOT 組成，全部都是大寫。</span><span class="sxs-lookup"><span data-stu-id="7e109-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="7e109-181">運算子 <、>、= 等等都不會當地語系化，因此也是標準語法的一部分。</span><span class="sxs-lookup"><span data-stu-id="7e109-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="7e109-182">如果屬性 `P` 有列舉值或名為 N ₁至 nk.bin 的範圍，則 *I* 值或範圍的標準語法是 P 的正式名稱，後面接著字元 \# ，後面接著 N <sub>I</sub>，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="7e109-183">`System.Photo.LightSource#Daylight`等等 `System.Photo.LightSource#StandardA` 。</span><span class="sxs-lookup"><span data-stu-id="7e109-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="7e109-184">若為具有值或範圍名稱為 N ₁至 Nk.bin 的已定義語義型別 T， *I* 值或範圍的標準語法為 t 的正式名稱，後面接著字元 \# ，後面接著 N <sub>I</sub>，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="7e109-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="7e109-185">針對文字值（例如單字或片語），標準語法與一般語法相同。</span><span class="sxs-lookup"><span data-stu-id="7e109-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="7e109-186">標準語法中具有常值的查詢範例如下：</span><span class="sxs-lookup"><span data-stu-id="7e109-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="7e109-187">在 Windows 7 和更新版本中，沒有適用于數位的標準語法。</span><span class="sxs-lookup"><span data-stu-id="7e109-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="7e109-188">因為浮點數格式會因地區設定而異，所以不支援使用包含浮點常數的標準查詢。</span><span class="sxs-lookup"><span data-stu-id="7e109-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="7e109-189">相反地，整數常數只能使用數位來撰寫 (千位) 的分隔符號，並可在 Windows 7 和更新版本的標準查詢中安全地使用。</span><span class="sxs-lookup"><span data-stu-id="7e109-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="7e109-190">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-190">Examples</span></span>

<span data-ttu-id="7e109-191">下表顯示標準屬性的一些範例，以及使用它們的語法。</span><span class="sxs-lookup"><span data-stu-id="7e109-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="7e109-192">標準屬性的類型</span><span class="sxs-lookup"><span data-stu-id="7e109-192">Type of canonical property</span></span> | <span data-ttu-id="7e109-193">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-193">Example</span></span>                                                                                     | <span data-ttu-id="7e109-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e109-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e109-195">字串值</span><span class="sxs-lookup"><span data-stu-id="7e109-195">String value</span></span>               | [<span data-ttu-id="7e109-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="7e109-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="7e109-197">在 author 屬性中搜尋字串值：</span><span class="sxs-lookup"><span data-stu-id="7e109-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="7e109-198">列舉範圍</span><span class="sxs-lookup"><span data-stu-id="7e109-198">Enumeration range</span></span>          | [<span data-ttu-id="7e109-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="7e109-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="7e109-200">Priority 屬性的值範圍可以是數值：</span><span class="sxs-lookup"><span data-stu-id="7e109-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="7e109-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="7e109-201">Boolean</span></span>                    | [<span data-ttu-id="7e109-202">System. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="7e109-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="7e109-203">布林值可以搭配任何布林值屬性使用：</span><span class="sxs-lookup"><span data-stu-id="7e109-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="7e109-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`和 `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="7e109-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="7e109-205">數值</span><span class="sxs-lookup"><span data-stu-id="7e109-205">Numerical</span></span>                  | [<span data-ttu-id="7e109-206">System. Size</span><span class="sxs-lookup"><span data-stu-id="7e109-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="7e109-207">您無法安全地撰寫牽涉到浮點常數的標準查詢，因為浮點數格式會因地區設定而異。</span><span class="sxs-lookup"><span data-stu-id="7e109-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="7e109-208">您必須撰寫整數，但不能為千位分隔符號。</span><span class="sxs-lookup"><span data-stu-id="7e109-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="7e109-209">例如：</span><span class="sxs-lookup"><span data-stu-id="7e109-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="7e109-210">如需標準屬性和屬性系統的一般詳細資訊，請參閱 [系統屬性](../properties/props.md)。</span><span class="sxs-lookup"><span data-stu-id="7e109-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="7e109-211">或者，請參閱公用標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7e109-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="7e109-212">查詢運算子</span><span class="sxs-lookup"><span data-stu-id="7e109-212">Query Operators</span></span>

<span data-ttu-id="7e109-213">如果屬性 p 具有某個專案的多個值，則 p：的 AQS 查詢會傳回 <restr> 專案，如果 <restr> 至少有一個值為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="7e109-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="7e109-214"> (<restr> 代表限制。 ) </span><span class="sxs-lookup"><span data-stu-id="7e109-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="7e109-215">下表所列的語法包含運算子、運算子符號、範例和範例描述。</span><span class="sxs-lookup"><span data-stu-id="7e109-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="7e109-216">運算子和符號可以用在任何語言中，並包含在任何查詢中。</span><span class="sxs-lookup"><span data-stu-id="7e109-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="7e109-217">請勿使用 COP \_ 隱含或 COP \_ 應用程式 \_ 特定的運算子。</span><span class="sxs-lookup"><span data-stu-id="7e109-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="7e109-218">某些運算子具有可互換的符號。</span><span class="sxs-lookup"><span data-stu-id="7e109-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e109-219">運算子</span><span class="sxs-lookup"><span data-stu-id="7e109-219">Operator</span></span></th>
<th><span data-ttu-id="7e109-220">符號</span><span class="sxs-lookup"><span data-stu-id="7e109-220">Symbol</span></span></th>
<th><span data-ttu-id="7e109-221">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-221">Example</span></span></th>
<th><span data-ttu-id="7e109-222">描述</span><span class="sxs-lookup"><span data-stu-id="7e109-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e109-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="7e109-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="7e109-224">System. FileExtension： = &quot; .txt&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-225">此值為字串 &quot; <em>.txt</em> &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="7e109-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="7e109-227">≠</span><span class="sxs-lookup"><span data-stu-id="7e109-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="7e109-228">NOT</span><span class="sxs-lookup"><span data-stu-id="7e109-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="7e109-229">System.string：≠ picture</span><span class="sxs-lookup"><span data-stu-id="7e109-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="7e109-230">DateTaken：-[] ¹</span><span class="sxs-lookup"><span data-stu-id="7e109-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="7e109-231">系統種類： &lt; &gt; 圖片</span><span class="sxs-lookup"><span data-stu-id="7e109-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="7e109-232">System.object：不是圖片</span><span class="sxs-lookup"><span data-stu-id="7e109-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="7e109-233">System.object：--圖片</span><span class="sxs-lookup"><span data-stu-id="7e109-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="7e109-234"><a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。</span><span class="sxs-lookup"><span data-stu-id="7e109-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="7e109-235"><a href="/windows/desktop/properties/props-system-photo-datetaken">DateTaken</a>屬性具有值。</span><span class="sxs-lookup"><span data-stu-id="7e109-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="7e109-236"><a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。</span><span class="sxs-lookup"><span data-stu-id="7e109-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="7e109-237"><a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。</span><span class="sxs-lookup"><span data-stu-id="7e109-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="7e109-238">未套用至相同屬性的雙重運算子不會取消。因此，system.string：--picture 相當於 System.object：-picture 和 system.string： NOT picture。</span><span class="sxs-lookup"><span data-stu-id="7e109-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="7e109-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="7e109-240">System. Size： &lt; 1kb</span><span class="sxs-lookup"><span data-stu-id="7e109-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="7e109-241">此值小於 <em>1kb</em>。</span><span class="sxs-lookup"><span data-stu-id="7e109-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="7e109-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="7e109-243">ItemDate： &gt; StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="7e109-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="7e109-244">此值大於 <em>今天</em>。</span><span class="sxs-lookup"><span data-stu-id="7e109-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="7e109-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="7e109-246">≤</span><span class="sxs-lookup"><span data-stu-id="7e109-246">≤</span></span><br/></td>
<td><span data-ttu-id="7e109-247">System. Size： &lt; = 1kb</span><span class="sxs-lookup"><span data-stu-id="7e109-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="7e109-248">這個值小於或等於 <em>1kb</em>。</span><span class="sxs-lookup"><span data-stu-id="7e109-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="7e109-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="7e109-250">≥</span><span class="sxs-lookup"><span data-stu-id="7e109-250">≥</span></span><br/></td>
<td><span data-ttu-id="7e109-251">System. Size： &gt; = 1kb</span><span class="sxs-lookup"><span data-stu-id="7e109-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="7e109-252">此值等於或大於 <em>1kb</em>。</span><span class="sxs-lookup"><span data-stu-id="7e109-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="7e109-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="7e109-254">System.string： ~ &lt; &quot; c + + 入門&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-255">尋找檔案名以 &quot; <em>c + + 入門</em>字元開頭的專案 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="7e109-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="7e109-257">CameraModel： ~ &gt; 非</span><span class="sxs-lookup"><span data-stu-id="7e109-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="7e109-258">尋找屬性值結尾為 <em>非</em>字元的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="7e109-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="7e109-260">System.object. ~ = round</span><span class="sxs-lookup"><span data-stu-id="7e109-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="7e109-261">Autosummary： ~ ~ round</span><span class="sxs-lookup"><span data-stu-id="7e109-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="7e109-262">在主旨中尋找具有這個字串的訊息，並將符合 &quot; g<em>四捨五入</em> 規則 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="7e109-263">尋找包含 Autosummary 的所有專案，其中包含 <em>四捨五入</em>的字元。</span><span class="sxs-lookup"><span data-stu-id="7e109-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="7e109-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="7e109-265">~!</span><span class="sxs-lookup"><span data-stu-id="7e109-265">~!</span></span><br/></td>
<td><span data-ttu-id="7e109-266">System. Author： ~！ &quot;桑傑&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-267">尋找未 &quot; 在其中<em>sanjay</em>字元順序的作者 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="7e109-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="7e109-269">System.string： ~ &quot; Mic？ Osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-270">尋找檔案名以 <em>Mic</em>開頭的檔案，後面接著一些字元，後面接著 <em>osoft w</em>，後面接著以 <em>d</em>結尾的任何字元。</span><span class="sxs-lookup"><span data-stu-id="7e109-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="7e109-271">？</span><span class="sxs-lookup"><span data-stu-id="7e109-271">The ?</span></span> <span data-ttu-id="7e109-272">和 \* 字元不會以逐字的方式解讀，而且可以像 DOS 樣式的萬用字元一樣運作：</span><span class="sxs-lookup"><span data-stu-id="7e109-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="7e109-273">?</span><span class="sxs-lookup"><span data-stu-id="7e109-273">?</span></span> <span data-ttu-id="7e109-274">符合一個任一字元。</span><span class="sxs-lookup"><span data-stu-id="7e109-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="7e109-275">\* 符合零或多個任一字元。</span><span class="sxs-lookup"><span data-stu-id="7e109-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="7e109-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="7e109-277">StructuredQuery： $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-278">適用于 Windows 7 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="7e109-278">For Windows 7 and later.</span></span> <span data-ttu-id="7e109-279">在 [屬性] 中尋找 [ &quot; <em>Sanjay Jacobs</em> ] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="7e109-280"><em>Sanjay</em>字後面必須接著<em>Jacobs</em>這個字。</span><span class="sxs-lookup"><span data-stu-id="7e109-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="7e109-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="7e109-282">System. Author： $</span><span class="sxs-lookup"><span data-stu-id="7e109-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="7e109-283">適用于 Windows 7 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="7e109-283">For Windows 7 and later.</span></span> <span data-ttu-id="7e109-284">尋找作者包含開頭為字元 San 之單字的任何專案 &quot; <em></em> &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7e109-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="7e109-285">尋找檔案名中包含以 <em>微型</em>開頭之單字的任何檔案，後面接著以 <em>exe</em>開頭的單字。</span><span class="sxs-lookup"><span data-stu-id="7e109-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e109-286">¹空的方括弧 (\[ \]) 表示「沒有值」。</span><span class="sxs-lookup"><span data-stu-id="7e109-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="7e109-287">若為字串屬性，預設作業會是 COP \_ word \_ 開頭 \_ ，或 COP \_ 單字 \_ 等於。</span><span class="sxs-lookup"><span data-stu-id="7e109-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="7e109-288">查詢值</span><span class="sxs-lookup"><span data-stu-id="7e109-288">Query Values</span></span>

<span data-ttu-id="7e109-289">下表列出如何限制查詢值的實用範例。</span><span class="sxs-lookup"><span data-stu-id="7e109-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e109-290">值/符號</span><span class="sxs-lookup"><span data-stu-id="7e109-290">Value/symbol</span></span></th>
<th><span data-ttu-id="7e109-291">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-291">Examples</span></span></th>
<th><span data-ttu-id="7e109-292">描述</span><span class="sxs-lookup"><span data-stu-id="7e109-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e109-293">String</span><span class="sxs-lookup"><span data-stu-id="7e109-293">String</span></span></td>
<td><span data-ttu-id="7e109-294">自動</span><span class="sxs-lookup"><span data-stu-id="7e109-294">auto</span></span><br/></td>
<td><span data-ttu-id="7e109-295">可以搜尋的任何字元序列。</span><span class="sxs-lookup"><span data-stu-id="7e109-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="7e109-296">字串不能包含屬於語法一部分的空白字元或字元組合。</span><span class="sxs-lookup"><span data-stu-id="7e109-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="7e109-297">此範例會搜尋以 <em>auto</em>開頭的單字。</span><span class="sxs-lookup"><span data-stu-id="7e109-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-298">加上引號的字串 &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="7e109-299">&quot;結論：有效 &quot; &quot; 的 &quot; &quot; blue &quot; &quot; team&quot;</span><span class="sxs-lookup"><span data-stu-id="7e109-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="7e109-300">任何字元序列。</span><span class="sxs-lookup"><span data-stu-id="7e109-300">Any sequence of characters.</span></span> <span data-ttu-id="7e109-301">字串不會被解釋為語法的一部分。</span><span class="sxs-lookup"><span data-stu-id="7e109-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="7e109-302">如果查詢成對，引號可以包含在查詢中。</span><span class="sxs-lookup"><span data-stu-id="7e109-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="7e109-303">此範例會搜尋 <em> &quot; blue &quot; team</em>。</span><span class="sxs-lookup"><span data-stu-id="7e109-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-304">整數</span><span class="sxs-lookup"><span data-stu-id="7e109-304">Integer</span></span></td>
<td><span data-ttu-id="7e109-305">5678</span><span class="sxs-lookup"><span data-stu-id="7e109-305">5678</span></span><br/></td>
<td><span data-ttu-id="7e109-306">只使用整數的數位。</span><span class="sxs-lookup"><span data-stu-id="7e109-306">Use only digits for integers.</span></span> <span data-ttu-id="7e109-307">請勿使用任何分隔符號作為千位。</span><span class="sxs-lookup"><span data-stu-id="7e109-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-308">浮點數</span><span class="sxs-lookup"><span data-stu-id="7e109-308">Floating point number</span></span></td>
<td><span data-ttu-id="7e109-309">5678.1234</span><span class="sxs-lookup"><span data-stu-id="7e109-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="7e109-310">因為浮點數格式會因地區設定而異，所以標準查詢無法使用浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="7e109-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="7e109-311">使用具有浮點數的標準語法不是當地語系化安全的。</span><span class="sxs-lookup"><span data-stu-id="7e109-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-312">布林<strong>值 true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="7e109-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="7e109-313">IsRead： = StructuredQueryType。布林值 # True</span><span class="sxs-lookup"><span data-stu-id="7e109-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="7e109-314">IsEncrypted：-System.object. StructuredQueryType。布林值 # False</span><span class="sxs-lookup"><span data-stu-id="7e109-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="7e109-315"><strong>TRUE</strong>布林值。</span><span class="sxs-lookup"><span data-stu-id="7e109-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="7e109-316"><strong>FALSE</strong>布林值。</span><span class="sxs-lookup"><span data-stu-id="7e109-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-317">[]</span><span class="sxs-lookup"><span data-stu-id="7e109-317">[]</span></span></td>
<td><span data-ttu-id="7e109-318">System.string： = []</span><span class="sxs-lookup"><span data-stu-id="7e109-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="7e109-319">空白方括弧表示沒有任何值。</span><span class="sxs-lookup"><span data-stu-id="7e109-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="7e109-320">這個範例會尋找尚未標記的所有專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-321">絕對日期</span><span class="sxs-lookup"><span data-stu-id="7e109-321">Absolute dates</span></span></td>
<td><span data-ttu-id="7e109-322">System. ItemDate： 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="7e109-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="7e109-323">SystemDateModified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="7e109-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="7e109-324">尋找日期為2010年1月26日的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="7e109-325">尋找于2002年10月15日至19:00:00 與19:00:59 之間修改的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e109-326">由於日期格式 (類似浮點數格式) 不同的地區設定，因此不支援使用具有絕對日期的標準語法，而且不是當地語系化的安全。</span><span class="sxs-lookup"><span data-stu-id="7e109-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e109-327">相對日期</span><span class="sxs-lookup"><span data-stu-id="7e109-327">Relative dates</span></span></td>
<td><span data-ttu-id="7e109-328">ItemDate： StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="7e109-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="7e109-329">DateAcquired： System. StructuredQueryType. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="7e109-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="7e109-330">DateReceived： StructuredQueryType. DateTime # LastYear</span><span class="sxs-lookup"><span data-stu-id="7e109-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="7e109-331">尋找今天日期的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="7e109-332">在下個月尋找具有日期的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="7e109-333">尋找過去一年中日期的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e109-334">除了搜尋特定日期和日期範圍之外，AQS 還可辨識相對日期值 (例如 <em>today</em>、 <em>明天</em>、 <em>nextweek</em>、 <em>nextmonth</em>) 和 day (例如 <em>星期二</em> 或 <em>星期一。星期三</em>) 和 month (<em>二月</em>) 。</span><span class="sxs-lookup"><span data-stu-id="7e109-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e109-335">..</span><span class="sxs-lookup"><span data-stu-id="7e109-335">..</span></span></td>
<td><span data-ttu-id="7e109-336">ItemDate： 11/05/04. 11/10/04 系統。大小：5kb。10kb</span><span class="sxs-lookup"><span data-stu-id="7e109-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="7e109-337">雙句點表示值範圍。</span><span class="sxs-lookup"><span data-stu-id="7e109-337">Double periods indicate a value range.</span></span> <span data-ttu-id="7e109-338">尋找日期介於11/05/04 和11/10/04 （含）之間的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="7e109-339">尋找大小介於5和10kb 之間的專案。</span><span class="sxs-lookup"><span data-stu-id="7e109-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="7e109-340">範圍限制</span><span class="sxs-lookup"><span data-stu-id="7e109-340">Scope Restrictions</span></span>

<span data-ttu-id="7e109-341">使用者可以將搜尋範圍限制在特定資料夾位置或資料存放區。</span><span class="sxs-lookup"><span data-stu-id="7e109-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="7e109-342">例如，如果您使用數個電子郵件帳戶，而您想要將查詢限制為 Microsoft Outlook 或 Microsoft Outlook Express，則可以使用 `System.Search.Store:mapi` 或分別使用或 `System.Search.Store:oe` 。</span><span class="sxs-lookup"><span data-stu-id="7e109-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="7e109-343">下表說明如何依資料存放區限制搜尋的一些範例。</span><span class="sxs-lookup"><span data-stu-id="7e109-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="7e109-344">依資料存放區限制搜尋</span><span class="sxs-lookup"><span data-stu-id="7e109-344">Restrict search by data store</span></span>  | <span data-ttu-id="7e109-345">關鍵字</span><span class="sxs-lookup"><span data-stu-id="7e109-345">Keyword</span></span> | <span data-ttu-id="7e109-346">範例</span><span class="sxs-lookup"><span data-stu-id="7e109-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="7e109-347">檔案</span><span class="sxs-lookup"><span data-stu-id="7e109-347">Files</span></span>                          | <span data-ttu-id="7e109-348">file</span><span class="sxs-lookup"><span data-stu-id="7e109-348">file</span></span>    | <span data-ttu-id="7e109-349">System. Store： file</span><span class="sxs-lookup"><span data-stu-id="7e109-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="7e109-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="7e109-350">Outlook</span></span>                        | <span data-ttu-id="7e109-351">Mapi</span><span class="sxs-lookup"><span data-stu-id="7e109-351">mapi</span></span>    | <span data-ttu-id="7e109-352">System. Store： mapi</span><span class="sxs-lookup"><span data-stu-id="7e109-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="7e109-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="7e109-353">Outlook Express</span></span>                | <span data-ttu-id="7e109-354">Oe</span><span class="sxs-lookup"><span data-stu-id="7e109-354">oe</span></span>      | <span data-ttu-id="7e109-355">System. Store： oe</span><span class="sxs-lookup"><span data-stu-id="7e109-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="7e109-356">離線檔案</span><span class="sxs-lookup"><span data-stu-id="7e109-356">Offline files</span></span>                  | <span data-ttu-id="7e109-357">Csc</span><span class="sxs-lookup"><span data-stu-id="7e109-357">csc</span></span>     | <span data-ttu-id="7e109-358">System. Store： csc</span><span class="sxs-lookup"><span data-stu-id="7e109-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="7e109-359">本機磁片磁碟機上的特定資料夾</span><span class="sxs-lookup"><span data-stu-id="7e109-359">Specific folder on local drive</span></span> | <span data-ttu-id="7e109-360">folder</span><span class="sxs-lookup"><span data-stu-id="7e109-360">folder</span></span>  | <span data-ttu-id="7e109-361">ItemFolderNameDisplay： C： " \\ MyFolder"</span><span class="sxs-lookup"><span data-stu-id="7e109-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="7e109-362">其他資源</span><span class="sxs-lookup"><span data-stu-id="7e109-362">Additional Resources</span></span>

-   <span data-ttu-id="7e109-363">在 Windows 7 （含）以後版本中，您可以根據是否符合 AQS 條件來使用快捷方式功能表選項。</span><span class="sxs-lookup"><span data-stu-id="7e109-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="7e109-364">如需詳細資訊，請參閱 [建立快捷方式功能表處理常式](../shell/context-menu-handlers.md)中的「使用 Advanced Query 語法取得靜態動詞的動態行為」。</span><span class="sxs-lookup"><span data-stu-id="7e109-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="7e109-365">AQS 查詢可以限制為特定類型的檔案，也就是所謂的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="7e109-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="7e109-366">如需詳細資訊，請參閱 [檔案類型和關聯](../shell/fa-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="7e109-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="7e109-367">如需屬性參考 [檔，請參閱 system.string](../properties/props-system-kind.md)和 [system. KindText](../properties/props-system-kindtext.md)。</span><span class="sxs-lookup"><span data-stu-id="7e109-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e109-368">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e109-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e109-369">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="7e109-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="7e109-370">使用 SQL 和 AQS 方法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7e109-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="7e109-371">使用 ISearchQueryHelper 查詢索引</span><span class="sxs-lookup"><span data-stu-id="7e109-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="7e109-372">使用搜尋-ms 通訊協定來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7e109-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="7e109-373">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7e109-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

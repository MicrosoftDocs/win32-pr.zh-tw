---
title: 建立查詢篩選
description: 查詢篩選準則會指示 Active Directory Domain Services 在 LDAP 查詢語法中尋找資料。 在選擇搜尋技術主題中所列的所有指定資料存取技術都支援 LDAP 查詢語法。
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，建立查詢篩選器
- 查詢篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839087"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="a429e-106">建立查詢篩選</span><span class="sxs-lookup"><span data-stu-id="a429e-106">Creating a Query Filter</span></span>

<span data-ttu-id="a429e-107">查詢篩選準則會指示 Active Directory Domain Services 在 LDAP 查詢語法中尋找資料。</span><span class="sxs-lookup"><span data-stu-id="a429e-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="a429e-108">在 [選擇搜尋技術](choosing-the-search-technology.md) 主題中所列的所有指定資料存取技術都支援 LDAP 查詢語法。</span><span class="sxs-lookup"><span data-stu-id="a429e-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="a429e-109">LDAP 查詢語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="a429e-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="a429e-110">篩選可包含一或多個運算式。</span><span class="sxs-lookup"><span data-stu-id="a429e-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="a429e-111">運算式的格式如下：</span><span class="sxs-lookup"><span data-stu-id="a429e-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="a429e-112">其中 " &lt; logicaloperator &gt; " 是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="a429e-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="a429e-113">運算子</span><span class="sxs-lookup"><span data-stu-id="a429e-113">Operator</span></span>        | <span data-ttu-id="a429e-114">說明</span><span class="sxs-lookup"><span data-stu-id="a429e-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="a429e-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="a429e-115">"\|"</span></span><br/> | <span data-ttu-id="a429e-116">邏輯 **OR**</span><span class="sxs-lookup"><span data-stu-id="a429e-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="a429e-117">"&"</span><span class="sxs-lookup"><span data-stu-id="a429e-117">"&"</span></span><br/>  | <span data-ttu-id="a429e-118">邏輯 **AND**</span><span class="sxs-lookup"><span data-stu-id="a429e-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="a429e-119">"!"</span><span class="sxs-lookup"><span data-stu-id="a429e-119">"!"</span></span><br/>  | <span data-ttu-id="a429e-120">邏輯 **NOT**</span><span class="sxs-lookup"><span data-stu-id="a429e-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="a429e-121">和「 &lt; 比較」 &gt; 如下：</span><span class="sxs-lookup"><span data-stu-id="a429e-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="a429e-122">其中 " &lt; attribute &gt; " 是要評估的屬性 **lDAPDisplayName** ，「值」 &lt; &gt; 是要比較的值，而「 &lt; 運算子」 &gt; 是下列其中一個比較運算子。</span><span class="sxs-lookup"><span data-stu-id="a429e-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="a429e-123">運算子</span><span class="sxs-lookup"><span data-stu-id="a429e-123">Operator</span></span>           | <span data-ttu-id="a429e-124">描述</span><span class="sxs-lookup"><span data-stu-id="a429e-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="a429e-125">"="</span><span class="sxs-lookup"><span data-stu-id="a429e-125">"="</span></span><br/>     | <span data-ttu-id="a429e-126">等於</span><span class="sxs-lookup"><span data-stu-id="a429e-126">Equals</span></span><br/>                   |
| <span data-ttu-id="a429e-127">"~="</span><span class="sxs-lookup"><span data-stu-id="a429e-127">"~="</span></span><br/>    | <span data-ttu-id="a429e-128">大約等於</span><span class="sxs-lookup"><span data-stu-id="a429e-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="a429e-129">"<="</span><span class="sxs-lookup"><span data-stu-id="a429e-129">"<="</span></span><br/> | <span data-ttu-id="a429e-130">小於或等於</span><span class="sxs-lookup"><span data-stu-id="a429e-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="a429e-131">">="</span><span class="sxs-lookup"><span data-stu-id="a429e-131">">="</span></span><br/> | <span data-ttu-id="a429e-132">大於或等於</span><span class="sxs-lookup"><span data-stu-id="a429e-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="a429e-133">此外，根據屬性語法，" &lt; value &gt; " 可以包含萬用字元符號 ( " \* " ) 。</span><span class="sxs-lookup"><span data-stu-id="a429e-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="a429e-134">&lt;包含萬用字元的「值」 &gt; 會檢查 "attribute" 中是否有任何值存在 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="a429e-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="a429e-135">如果未設定 " &lt; attribute" 的值 &gt; ，測試將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a429e-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="a429e-136">如果下列任何特殊字元必須以常值形式出現在查詢篩選中，則必須以所列的 escape 順序取代這些特殊字元。</span><span class="sxs-lookup"><span data-stu-id="a429e-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="a429e-137">ASCII 字元</span><span class="sxs-lookup"><span data-stu-id="a429e-137">ASCII character</span></span>    | <span data-ttu-id="a429e-138">換用換用順序</span><span class="sxs-lookup"><span data-stu-id="a429e-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="a429e-139">" \\ 2a"</span><span class="sxs-lookup"><span data-stu-id="a429e-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="a429e-140">(</span><span class="sxs-lookup"><span data-stu-id="a429e-140">(</span></span><br/>       | <span data-ttu-id="a429e-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="a429e-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="a429e-142">)</span><span class="sxs-lookup"><span data-stu-id="a429e-142">)</span></span><br/>       | <span data-ttu-id="a429e-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="a429e-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="a429e-144">" \\ 5c"</span><span class="sxs-lookup"><span data-stu-id="a429e-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="a429e-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="a429e-145">**NUL**</span></span><br/> | <span data-ttu-id="a429e-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="a429e-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="a429e-147">此外，您可以使用 escape 順序語法來表示任意的二進位資料，方法是將二進位資料的每個位元組編碼為反斜線，後面接著兩個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="a429e-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="a429e-148">例如，四位元組值的 0x00000004 \\ 在篩選字串中會編碼為 "00 \\ 00 \\ 00 \\ 04"。</span><span class="sxs-lookup"><span data-stu-id="a429e-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="a429e-149">範例</span><span class="sxs-lookup"><span data-stu-id="a429e-149">Examples</span></span>

<span data-ttu-id="a429e-150">下列查詢字串會搜尋 "computer" 類型的所有物件。</span><span class="sxs-lookup"><span data-stu-id="a429e-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="a429e-151">下列查詢字串會搜尋 "computer" 類型的所有物件，其名稱開頭為 "desktop"。</span><span class="sxs-lookup"><span data-stu-id="a429e-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="a429e-152">下列查詢字串會搜尋 "computer" 類型的所有物件，其名稱開頭為 "desktop" 或開頭為 "筆記本" 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a429e-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="a429e-153">下列查詢字串會搜尋 "user" 類型的所有物件，其具有 home 電話號碼。</span><span class="sxs-lookup"><span data-stu-id="a429e-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="a429e-154">如需查詢篩選字串和使用方式範例的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="a429e-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="a429e-155">依類別尋找物件</span><span class="sxs-lookup"><span data-stu-id="a429e-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="a429e-156">依名稱尋找物件</span><span class="sxs-lookup"><span data-stu-id="a429e-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="a429e-157">尋找要查詢的屬性清單</span><span class="sxs-lookup"><span data-stu-id="a429e-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="a429e-158">檢查查詢篩選語法</span><span class="sxs-lookup"><span data-stu-id="a429e-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="a429e-159">如何指定比較值</span><span class="sxs-lookup"><span data-stu-id="a429e-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 






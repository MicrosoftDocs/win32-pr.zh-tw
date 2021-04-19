---
title: 搜尋篩選語法
description: 搜尋篩選器可讓您定義搜尋條件，並提供更有效率且更有效率的搜尋。
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- 搜尋篩選語法 ADSI
- 查詢，搜尋篩選語法
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106994919"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="1b101-105">搜尋篩選語法</span><span class="sxs-lookup"><span data-stu-id="1b101-105">Search Filter Syntax</span></span>

<span data-ttu-id="1b101-106">搜尋篩選器可讓您定義搜尋條件，並提供更有效率且更有效率的搜尋。</span><span class="sxs-lookup"><span data-stu-id="1b101-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="1b101-107">ADSI 支援 RFC2254 中定義的 LDAP 搜尋篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1b101-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="1b101-108">這些搜尋篩選器會以 Unicode 字串表示。</span><span class="sxs-lookup"><span data-stu-id="1b101-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="1b101-109">下表列出 LDAP 搜尋篩選準則的一些範例。</span><span class="sxs-lookup"><span data-stu-id="1b101-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="1b101-110">搜尋篩選</span><span class="sxs-lookup"><span data-stu-id="1b101-110">Search filter</span></span>                                                               | <span data-ttu-id="1b101-111">Description</span><span class="sxs-lookup"><span data-stu-id="1b101-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b101-112">" (objectClass = \*) "</span><span class="sxs-lookup"><span data-stu-id="1b101-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="1b101-113">所有物件。</span><span class="sxs-lookup"><span data-stu-id="1b101-113">All objects.</span></span>                                               |
| <span data-ttu-id="1b101-114">" (& (objectCategory = person)  (objectClass = user)  (！ (cn =) ) ) "</span><span class="sxs-lookup"><span data-stu-id="1b101-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="1b101-115">所有使用者物件，但「會」。</span><span class="sxs-lookup"><span data-stu-id="1b101-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="1b101-116">" (sn = sm \*) "</span><span class="sxs-lookup"><span data-stu-id="1b101-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="1b101-117">姓氏開頭為 "sm" 的所有物件。</span><span class="sxs-lookup"><span data-stu-id="1b101-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="1b101-118">" (& (objectCategory = person)  (objectClass = contact)  (\| (sn = Smith)  (sn = Johnson) ) ) "</span><span class="sxs-lookup"><span data-stu-id="1b101-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="1b101-119">姓氏等於 "Smith" 或 "Johnson" 的所有連絡人。</span><span class="sxs-lookup"><span data-stu-id="1b101-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="1b101-120">這些搜尋篩選器會使用下列其中一種格式。</span><span class="sxs-lookup"><span data-stu-id="1b101-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="1b101-121">或</span><span class="sxs-lookup"><span data-stu-id="1b101-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="1b101-122">ADSI 搜尋篩選器的使用方式有兩種。</span><span class="sxs-lookup"><span data-stu-id="1b101-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="1b101-123">它們構成了 LDAP 方言的一部分，可透過 OLE DB 提供者提交查詢。</span><span class="sxs-lookup"><span data-stu-id="1b101-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="1b101-124">它們也會搭配 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="1b101-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="1b101-125">運算子</span><span class="sxs-lookup"><span data-stu-id="1b101-125">Operators</span></span>

<span data-ttu-id="1b101-126">下表列出常用的搜尋篩選運算子。</span><span class="sxs-lookup"><span data-stu-id="1b101-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="1b101-127">邏輯運算子</span><span class="sxs-lookup"><span data-stu-id="1b101-127">Logical operator</span></span> | <span data-ttu-id="1b101-128">描述</span><span class="sxs-lookup"><span data-stu-id="1b101-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="1b101-129">等於</span><span class="sxs-lookup"><span data-stu-id="1b101-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="1b101-130">大約等於</span><span class="sxs-lookup"><span data-stu-id="1b101-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="1b101-131">詞典編纂小於或等於</span><span class="sxs-lookup"><span data-stu-id="1b101-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="1b101-132">詞典編纂大於或等於</span><span class="sxs-lookup"><span data-stu-id="1b101-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="1b101-133">AND</span><span class="sxs-lookup"><span data-stu-id="1b101-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="1b101-134">OR</span><span class="sxs-lookup"><span data-stu-id="1b101-134">OR</span></span>                                         |
| <span data-ttu-id="1b101-135">!</span><span class="sxs-lookup"><span data-stu-id="1b101-135">!</span></span>                | <span data-ttu-id="1b101-136">NOT</span><span class="sxs-lookup"><span data-stu-id="1b101-136">NOT</span></span>                                        |



 

<span data-ttu-id="1b101-137">除了上述運算子之外，LDAP 還會定義兩個相符的規則物件識別碼 (Oid) ，可用來執行數值的位比較。</span><span class="sxs-lookup"><span data-stu-id="1b101-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="1b101-138">比對規則具有下列語法。</span><span class="sxs-lookup"><span data-stu-id="1b101-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="1b101-139">「 &lt; 屬性名稱」 &gt; 是屬性（attribute）的 **lDAPDisplayName** ，「 &lt; 規則 OID」 &gt; 是比對規則的 OID，而「 &lt; 值」 &gt; 則是要用於比較的值。</span><span class="sxs-lookup"><span data-stu-id="1b101-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="1b101-140">請注意，這個字串中不能使用空格。</span><span class="sxs-lookup"><span data-stu-id="1b101-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="1b101-141">「 &lt; 值」 &gt; 必須是十進位數，不可以是十六進位數位或常數名稱，例如 **\_ 啟用 ADS 群組 \_ 類型 \_ 安全性 \_**。</span><span class="sxs-lookup"><span data-stu-id="1b101-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="1b101-142">如需可用 Active Directory 屬性的詳細資訊，請參閱 [所有屬性](/windows/desktop/ADSchema/attributes-all)。</span><span class="sxs-lookup"><span data-stu-id="1b101-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="1b101-143">下表列出 LDAP 所執行的相符規則 Oid。</span><span class="sxs-lookup"><span data-stu-id="1b101-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="1b101-144">符合規則 OID</span><span class="sxs-lookup"><span data-stu-id="1b101-144">Matching rule OID</span></span>       | <span data-ttu-id="1b101-145">從 Ntldap (的字串識別碼) </span><span class="sxs-lookup"><span data-stu-id="1b101-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="1b101-146">Description</span><span class="sxs-lookup"><span data-stu-id="1b101-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b101-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="1b101-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="1b101-148">**LDAP \_ \_ 比對規則 \_ 位 \_ 和**</span><span class="sxs-lookup"><span data-stu-id="1b101-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="1b101-149">只有當屬性中的所有位都符合值時，才會找到相符的。</span><span class="sxs-lookup"><span data-stu-id="1b101-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="1b101-150">這項規則相當於位 **and** 運算子。</span><span class="sxs-lookup"><span data-stu-id="1b101-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="1b101-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="1b101-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="1b101-152">**LDAP \_ \_ 比對規則 \_ 位 \_ 或**</span><span class="sxs-lookup"><span data-stu-id="1b101-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="1b101-153">如果屬性中的任何位符合值，就會找到相符的結果。</span><span class="sxs-lookup"><span data-stu-id="1b101-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="1b101-154">這項規則相當於位 **or** 運算子。</span><span class="sxs-lookup"><span data-stu-id="1b101-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="1b101-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="1b101-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="1b101-156">**\_ \_ \_ 鏈中的 LDAP 比對規則 \_**</span><span class="sxs-lookup"><span data-stu-id="1b101-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="1b101-157">此規則僅限於適用于 DN 的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1b101-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="1b101-158">這是特殊的「擴充」比對運算子，會將物件中的上階鏈一直指向根目錄，直到找到相符的結果為止。</span><span class="sxs-lookup"><span data-stu-id="1b101-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="1b101-159">下列查詢字串範例會搜尋已設定 **ADS \_ 群組 \_ 類型 \_ \_ 啟用安全性** 旗標的群組物件。</span><span class="sxs-lookup"><span data-stu-id="1b101-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="1b101-160">請注意， **\_ \_ \_ \_ 已啟用 ADS 群組型別安全性** 的 decimal 值 (0x80000000 = 2147483648) 用於比較值。</span><span class="sxs-lookup"><span data-stu-id="1b101-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="1b101-161">**\_ \_ \_ \_ CHAIN 中的 LDAP** 比對規則是一種比對規則 OID，其設計目的是要提供方法來查詢物件的上階。</span><span class="sxs-lookup"><span data-stu-id="1b101-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="1b101-162">使用 AD 和 AD LDS 的許多應用程式通常會使用階層式資料，而這些資料是以父子式關聯性來排序。</span><span class="sxs-lookup"><span data-stu-id="1b101-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="1b101-163">之前，應用程式執行了可轉移的群組延伸，以找出使用太多網路頻寬的群組成員資格;應用程式需要進行多次往返，以找出某個物件在鏈中是否有「在鏈中」的情況。</span><span class="sxs-lookup"><span data-stu-id="1b101-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="1b101-164">這類查詢的其中一個範例是設計來檢查使用者 "user1" 是否為群組 "group1" 的成員。</span><span class="sxs-lookup"><span data-stu-id="1b101-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="1b101-165">您會將基底設定為 [使用者 DN] `(cn=user1, cn=users, dc=x)` 和 [範圍] `base` ，然後使用下列查詢。</span><span class="sxs-lookup"><span data-stu-id="1b101-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="1b101-166">同樣地，若要尋找 "user1" 為其成員的所有群組，請將基底設定為群組容器 DN;例如， `(OU=groupsOU, dc=x)` 將範圍設為 `subtree` ，並使用下列篩選。</span><span class="sxs-lookup"><span data-stu-id="1b101-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="1b101-167">請注意， **\_ \_ \_ 在 \_ CHAIN 中使用 LDAP** 比對規則時，範圍不會受到限制，其可以是 `base` 、 `one-level` 或 `subtree` 。</span><span class="sxs-lookup"><span data-stu-id="1b101-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="1b101-168">子樹上的某些這類查詢可能會耗用更多處理器，例如，使用高展開連結的追蹤連結;也就是，列出使用者所屬的所有群組。</span><span class="sxs-lookup"><span data-stu-id="1b101-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="1b101-169">無效率的搜尋會記錄適當的事件記錄檔訊息，就像任何其他類型的查詢一樣。</span><span class="sxs-lookup"><span data-stu-id="1b101-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="1b101-170">萬用字元</span><span class="sxs-lookup"><span data-stu-id="1b101-170">Wildcards</span></span>

<span data-ttu-id="1b101-171">您也可以將萬用字元和條件新增至 LDAP 搜尋篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1b101-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="1b101-172">下列範例顯示可以用來搜尋目錄的子字串。</span><span class="sxs-lookup"><span data-stu-id="1b101-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="1b101-173">取得所有專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="1b101-174">在一般名稱中的某個位置取得包含 "bob" 的專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="1b101-175">取得一般名稱大於或等於 "bob" 的專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="1b101-176">取得具有電子郵件屬性的所有使用者：</span><span class="sxs-lookup"><span data-stu-id="1b101-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="1b101-177">取得電子郵件屬性和姓氏等於 "smith" 的所有使用者專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="1b101-178">取得一般名稱開頭為 "margaret"、"steve" 或 "" 的所有使用者專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="1b101-179">取得沒有電子郵件屬性的所有專案：</span><span class="sxs-lookup"><span data-stu-id="1b101-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="1b101-180">搜尋篩選準則的正式定義如下 (從 [RFC 2254](https://tools.ietf.org/html/rfc2254)) ：</span><span class="sxs-lookup"><span data-stu-id="1b101-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="1b101-181">Token &lt; attr &gt; 是代表 AttributeType 的字串。</span><span class="sxs-lookup"><span data-stu-id="1b101-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="1b101-182">Token &lt; 值 &gt; 是代表 AttributeValue 的字串，其格式是由基礎目錄服務所定義。</span><span class="sxs-lookup"><span data-stu-id="1b101-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="1b101-183">如果 &lt; 值 &gt; 必須包含星號 (\*) 、左括弧 ( () 或右括弧 () ) 字元，則字元前面必須加上反斜線 escape 字元 (\\) 。</span><span class="sxs-lookup"><span data-stu-id="1b101-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="1b101-184">特殊字元</span><span class="sxs-lookup"><span data-stu-id="1b101-184">Special Characters</span></span>

<span data-ttu-id="1b101-185">如果下列任何特殊字元必須以常值形式出現在搜尋篩選中，則必須以所列的 escape 順序取代這些特殊字元。</span><span class="sxs-lookup"><span data-stu-id="1b101-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="1b101-186">ASCII 字元</span><span class="sxs-lookup"><span data-stu-id="1b101-186">ASCII character</span></span> | <span data-ttu-id="1b101-187">換用換用順序</span><span class="sxs-lookup"><span data-stu-id="1b101-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="1b101-188">\\之</span><span class="sxs-lookup"><span data-stu-id="1b101-188">\\2a</span></span>                       |
| <span data-ttu-id="1b101-189">(</span><span class="sxs-lookup"><span data-stu-id="1b101-189">(</span></span>               | <span data-ttu-id="1b101-190">\\日</span><span class="sxs-lookup"><span data-stu-id="1b101-190">\\28</span></span>                       |
| <span data-ttu-id="1b101-191">)</span><span class="sxs-lookup"><span data-stu-id="1b101-191">)</span></span>               | <span data-ttu-id="1b101-192">\\29</span><span class="sxs-lookup"><span data-stu-id="1b101-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="1b101-193">\\5c</span><span class="sxs-lookup"><span data-stu-id="1b101-193">\\5c</span></span>                       |
| <span data-ttu-id="1b101-194">NUL</span><span class="sxs-lookup"><span data-stu-id="1b101-194">NUL</span></span>             | <span data-ttu-id="1b101-195">\\演講</span><span class="sxs-lookup"><span data-stu-id="1b101-195">\\00</span></span>                       |
| /               | <span data-ttu-id="1b101-196">\\2f</span><span class="sxs-lookup"><span data-stu-id="1b101-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="1b101-197">在使用多位元組字元集的情況下，如果 ADO 使用 SQL 方言執行搜尋，就必須使用上列的 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="1b101-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="1b101-198">此外，您可以使用 escape 順序語法來表示任意二進位資料，方法是使用反斜線 (\\) 後接兩個十六進位數位來編碼每個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="1b101-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="1b101-199">例如，四位元組值的 0x00000004 \\ \\ \\ 在篩選字串中會編碼為 00 00 00 \\ 04。</span><span class="sxs-lookup"><span data-stu-id="1b101-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b101-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b101-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b101-201">LDAP 方言</span><span class="sxs-lookup"><span data-stu-id="1b101-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="1b101-202">SQL 方言</span><span class="sxs-lookup"><span data-stu-id="1b101-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="1b101-203">使用 >idirectorysearch 介面搜尋</span><span class="sxs-lookup"><span data-stu-id="1b101-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="1b101-204">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="1b101-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="1b101-205">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="1b101-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 

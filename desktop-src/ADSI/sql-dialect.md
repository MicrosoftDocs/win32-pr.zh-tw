---
title: SQL 方言
description: 從結構化查詢語言 (SQL) 衍生的 SQL 方言會使用人類可讀取的運算式來定義查詢語句。
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL 方言 ADSI
- 方言 ADSI，SQL 方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969020"
---
# <a name="sql-dialect"></a><span data-ttu-id="56466-105">SQL 方言</span><span class="sxs-lookup"><span data-stu-id="56466-105">SQL Dialect</span></span>

<span data-ttu-id="56466-106">從結構化查詢語言 (SQL) 衍生的 SQL 方言會使用人類可讀取的運算式來定義查詢語句。</span><span class="sxs-lookup"><span data-stu-id="56466-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="56466-107">使用 SQL 查詢語句搭配下列 ADSI 搜尋介面：</span><span class="sxs-lookup"><span data-stu-id="56466-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="56466-108">[ActiveX Data 物件 (ADO) ](searching-with-activex-data-objects-ado.md)介面，這是使用 OLE DB 的自動化介面。</span><span class="sxs-lookup"><span data-stu-id="56466-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="56466-109">[OLE DB](searching-with-ole-db.md)，這是一組用來查詢資料庫的 c/c + + 介面。</span><span class="sxs-lookup"><span data-stu-id="56466-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="56466-110">SQL 語句需要下列語法。</span><span class="sxs-lookup"><span data-stu-id="56466-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="56466-111">下表列出 SQL 查詢語句關鍵字。</span><span class="sxs-lookup"><span data-stu-id="56466-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="56466-112">關鍵字</span><span class="sxs-lookup"><span data-stu-id="56466-112">Keyword</span></span>  | <span data-ttu-id="56466-113">描述</span><span class="sxs-lookup"><span data-stu-id="56466-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56466-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="56466-114">SELECT</span></span>   | <span data-ttu-id="56466-115">指定要針對每個物件取出的屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="56466-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="56466-116">如果您指定 \* ，查詢只會抓取每個物件的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="56466-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="56466-117">FROM</span><span class="sxs-lookup"><span data-stu-id="56466-117">FROM</span></span>     | <span data-ttu-id="56466-118">指定搜尋基底的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="56466-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="56466-119">例如，Active Directory 網域中的 [使用者] 容器的 ADsPath 可能是 [LDAP：//CN = Users，DC = Fabrikam，DC = COM]。</span><span class="sxs-lookup"><span data-stu-id="56466-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="56466-120">請注意，路徑是以一對單引號括住 ( ' ) 。</span><span class="sxs-lookup"><span data-stu-id="56466-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="56466-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="56466-121">WHERE</span></span>    | <span data-ttu-id="56466-122">指定查詢篩選的選擇性關鍵字。</span><span class="sxs-lookup"><span data-stu-id="56466-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="56466-123">排序依據</span><span class="sxs-lookup"><span data-stu-id="56466-123">ORDER BY</span></span> | <span data-ttu-id="56466-124">選擇性的關鍵字，如果伺服器支援 LDAP 排序控制項，則會產生伺服器端排序。</span><span class="sxs-lookup"><span data-stu-id="56466-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="56466-125">Active Directory 支援排序控制項，但可能會影響伺服器效能，特別是當結果集很大時。</span><span class="sxs-lookup"><span data-stu-id="56466-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="56466-126">排序清單是用來排序的屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="56466-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="56466-127">請注意，Active Directory 只支援單一排序索引鍵。</span><span class="sxs-lookup"><span data-stu-id="56466-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="56466-128">您可以使用選擇性的 ASC 和 DESC 關鍵字來指定遞增或遞減排序次序。預設值為遞增。</span><span class="sxs-lookup"><span data-stu-id="56466-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="56466-129">ORDER BY 關鍵字會覆寫任何以 ADO 命令物件的「排序依據」屬性指定的排序索引鍵。</span><span class="sxs-lookup"><span data-stu-id="56466-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="56466-130">在使用多位元組字元集的情況下，如果使用 SQL 方言以 ADO 執行搜尋，則不能使用反斜線來將字元換用。</span><span class="sxs-lookup"><span data-stu-id="56466-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="56466-131">相反地，必須使用以 [特殊字元](search-filter-syntax.md) 列出的 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="56466-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="56466-132">例如，針對使用語法 "samAccountName = Test" 的語句（ \( 使用反斜線 " \\ "）來 escape 左括弧 " ("，改為使用特殊字元 "28" 來取代反斜線，如下所示 \\ ： "samaccountname = \\ 28Test"。</span><span class="sxs-lookup"><span data-stu-id="56466-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="56466-133">下列查詢語句是 ADSI 中的 SQL 方言範例。</span><span class="sxs-lookup"><span data-stu-id="56466-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="56466-134">以搜尋所有群組物件。</span><span class="sxs-lookup"><span data-stu-id="56466-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="56466-135">搜尋姓氏以字母 H 開頭的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="56466-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="56466-136">下列程式碼範例定義了 SQL 查詢的正式文法。</span><span class="sxs-lookup"><span data-stu-id="56466-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="56466-137">所有關鍵詞都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="56466-137">All keywords are case-insensitive.</span></span>


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



<span data-ttu-id="56466-138">Active Directory 的 OLE DB 提供者不支援 SQL 內部聯結，但您可以使用 SQL 來聯結 SQL 和 Active Directory 資料。</span><span class="sxs-lookup"><span data-stu-id="56466-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="56466-139">如需詳細資訊，請參閱 [建立 SQL Server 與 Active Directory 之間的異類聯結](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)。</span><span class="sxs-lookup"><span data-stu-id="56466-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56466-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="56466-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56466-141">搜尋篩選語法</span><span class="sxs-lookup"><span data-stu-id="56466-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="56466-142">LDAP 方言</span><span class="sxs-lookup"><span data-stu-id="56466-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="56466-143">使用 >idirectorysearch 介面搜尋</span><span class="sxs-lookup"><span data-stu-id="56466-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="56466-144">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="56466-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="56466-145">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="56466-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 





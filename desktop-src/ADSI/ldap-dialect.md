---
title: LDAP 方言
description: LDAP 方言是使用 LDAP 搜尋篩選語法的查詢語句格式。
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- LDAP 方言 ADSI
- 方言 ADSI，LDAP 方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839172"
---
# <a name="ldap-dialect"></a><span data-ttu-id="84c67-105">LDAP 方言</span><span class="sxs-lookup"><span data-stu-id="84c67-105">LDAP Dialect</span></span>

<span data-ttu-id="84c67-106">LDAP 方言是使用 [LDAP 搜尋篩選語法](search-filter-syntax.md)的查詢語句格式。</span><span class="sxs-lookup"><span data-stu-id="84c67-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="84c67-107">使用 LDAP 查詢語句搭配下列 ADSI 搜尋介面：</span><span class="sxs-lookup"><span data-stu-id="84c67-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="84c67-108">[ActiveX Data 物件 (ADO) ](searching-with-activex-data-objects-ado.md)介面，這是使用 OLE DB 的自動化介面。</span><span class="sxs-lookup"><span data-stu-id="84c67-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="84c67-109">[OLE DB](searching-with-ole-db.md)，這是一組用來查詢資料庫的 c/c + + 介面。</span><span class="sxs-lookup"><span data-stu-id="84c67-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="84c67-110">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)，這是 Active Directory 的 c/c + + 介面。</span><span class="sxs-lookup"><span data-stu-id="84c67-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="84c67-111">LDAP 方言字串是由四個以分號分隔的部分所組成 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="84c67-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="84c67-112">基底分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="84c67-112">Base distinguished name.</span></span> <span data-ttu-id="84c67-113">例如：</span><span class="sxs-lookup"><span data-stu-id="84c67-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="84c67-114">LDAP 搜尋篩選準則。</span><span class="sxs-lookup"><span data-stu-id="84c67-114">LDAP search filters.</span></span> <span data-ttu-id="84c67-115">如需搜尋篩選準則的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="84c67-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="84c67-116">要取得之屬性的 LDAP 顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="84c67-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="84c67-117">多個屬性會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="84c67-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="84c67-118">指定搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="84c67-118">Specifies the scope of the search.</span></span> <span data-ttu-id="84c67-119">有效的值為 "base"、"onelevel" 和 "子樹"。</span><span class="sxs-lookup"><span data-stu-id="84c67-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="84c67-120">LDAP 查詢字串中指定的範圍會覆寫以 ADO 命令物件的 "SearchScope" 屬性指定的任何搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="84c67-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="84c67-121">以下是 ADSI 中的 LDAP 方言的程式碼範例，可搜尋子樹中的所有物件。</span><span class="sxs-lookup"><span data-stu-id="84c67-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="84c67-122">並非所有搜尋選項 (搜尋頁面大小，例如) 可以用 LDAP 方言表示，因此您必須在實際查詢執行開始之前設定這些選項。</span><span class="sxs-lookup"><span data-stu-id="84c67-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="84c67-123">執行 LDAP 查詢的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="84c67-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="84c67-124">下列程式碼範例顯示如何使用 LDAP 查詢</span><span class="sxs-lookup"><span data-stu-id="84c67-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="84c67-125">如需有關查詢語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="84c67-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84c67-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="84c67-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c67-127">搜尋篩選語法</span><span class="sxs-lookup"><span data-stu-id="84c67-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="84c67-128">SQL 方言</span><span class="sxs-lookup"><span data-stu-id="84c67-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="84c67-129">使用 >idirectorysearch 介面搜尋</span><span class="sxs-lookup"><span data-stu-id="84c67-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="84c67-130">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="84c67-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="84c67-131">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="84c67-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 





---
title: 聯結異質資料
description: 一般組織會將資料儲存在多個異質資料庫中。 人力資源資料可能儲存在 SQL Server 中，而帳戶管理資料則儲存在目錄中。 其他資料可能會以專屬格式儲存。
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314611"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="2e714-105">聯結異質資料</span><span class="sxs-lookup"><span data-stu-id="2e714-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="2e714-106">一般組織會將資料儲存在多個異質資料庫中。</span><span class="sxs-lookup"><span data-stu-id="2e714-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="2e714-107">人力資源資料可能儲存在 SQL Server 中，而帳戶管理資料則儲存在目錄中。</span><span class="sxs-lookup"><span data-stu-id="2e714-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="2e714-108">其他資料可能會以專屬格式儲存。</span><span class="sxs-lookup"><span data-stu-id="2e714-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="2e714-109">利用、SQL Server 7.0、ADSI 和 OLE DB 提供者，您可以將資料從 Active Directory 聯結至 SQL Server 中的資料，並建立聯結資料的觀點。</span><span class="sxs-lookup"><span data-stu-id="2e714-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="2e714-110">**使用 SQL Server 資料聯結 Active Directory 資料**</span><span class="sxs-lookup"><span data-stu-id="2e714-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="2e714-111">執行 **SQL 查詢分析器** (啟動 \| 程式 \| Microsoft SQL Server 7.0) </span><span class="sxs-lookup"><span data-stu-id="2e714-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="2e714-112">登入 SQL Server 電腦。</span><span class="sxs-lookup"><span data-stu-id="2e714-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="2e714-113">藉由反白顯示並按下 CTRL + E)  (來執行下行：</span><span class="sxs-lookup"><span data-stu-id="2e714-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="2e714-114">在這一行中， [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式的引數如下所示：</span><span class="sxs-lookup"><span data-stu-id="2e714-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="2e714-115">"ADSI" 是 **伺服器** 引數，它將是這個連結伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e714-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="2e714-116">"Active Directory Services" 是 **srvproduct** 引數，這是您要新增為連結伺服器的 OLE DB 資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="2e714-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="2e714-117">"ADSDSOObject" 是 **provider \_ name** 引數，表示您使用 OLE DB 提供者。</span><span class="sxs-lookup"><span data-stu-id="2e714-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="2e714-118">"adsdatasource" 是 **資料 \_ 源引數**，這是 OLE DB 提供者所解釋的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="2e714-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="2e714-119">您現在可以使用連結的伺服器，從 SQL Server 存取 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="2e714-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="2e714-120">下一個範例會使用 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="2e714-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="2e714-121">這個語句有兩個引數： ADSI，也就是您剛才建立的連結伺服器名稱，以及一個查詢語句。</span><span class="sxs-lookup"><span data-stu-id="2e714-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="2e714-122">查詢語句包含下列專案：</span><span class="sxs-lookup"><span data-stu-id="2e714-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="2e714-123">[SELECT](https://msdn.microsoft.com/library/Aa259187.aspx)語句包含將從目錄服務取得的資料清單。</span><span class="sxs-lookup"><span data-stu-id="2e714-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="2e714-124">您將需要使用 LDAP 顯示名稱來指出您要搜尋的資料。</span><span class="sxs-lookup"><span data-stu-id="2e714-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="2e714-125">[From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含將從中取得這項資訊的連結目錄伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2e714-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="2e714-126">[WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。</span><span class="sxs-lookup"><span data-stu-id="2e714-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="2e714-127">在此範例中，它會搜尋使用者。</span><span class="sxs-lookup"><span data-stu-id="2e714-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="2e714-128">輸入並執行：</span><span class="sxs-lookup"><span data-stu-id="2e714-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="2e714-129">您也可以使用 ADSI [LDAP 方言](ldap-dialect.md)。</span><span class="sxs-lookup"><span data-stu-id="2e714-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="2e714-130">例如：</span><span class="sxs-lookup"><span data-stu-id="2e714-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="2e714-131">在上述範例中，LDAP 查詢有四個部分：</span><span class="sxs-lookup"><span data-stu-id="2e714-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="2e714-132">" \<LDAP://DC=Fabrikam,DC=COM> " 是要搜尋之目錄伺服器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="2e714-132">"\<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="2e714-133">「 (& (objectCategory = Person)  (objectClass = user) ) 」是 LDAP 搜尋篩選 (查看 [搜尋篩選語法](search-filter-syntax.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2e714-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="2e714-134">「名稱，adspath」是使用 LDAP 顯示名稱格式 (的名稱，) 要取出的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e714-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="2e714-135">「子樹」表示搜尋的 [範圍](scope-of-query.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e714-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e714-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e714-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e714-137">建立和執行視圖</span><span class="sxs-lookup"><span data-stu-id="2e714-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 





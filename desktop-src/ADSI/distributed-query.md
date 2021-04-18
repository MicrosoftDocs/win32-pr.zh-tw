---
title: Distributed Query
description: 因為 ADSI 是 OLE DB 的提供者，所以可以參與 Microsoft SQL Server 7.0 中引進的分散式查詢。
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- 查詢 ADSI、分散式查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106968888"
---
# <a name="distributed-query"></a><span data-ttu-id="c91ef-104">Distributed Query</span><span class="sxs-lookup"><span data-stu-id="c91ef-104">Distributed Query</span></span>

<span data-ttu-id="c91ef-105">因為 ADSI 是 OLE DB 的提供者，所以可以參與 Microsoft SQL Server 7.0 中引進的分散式查詢。</span><span class="sxs-lookup"><span data-stu-id="c91ef-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="c91ef-106">可能的案例如下：</span><span class="sxs-lookup"><span data-stu-id="c91ef-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="c91ef-107">聯結具有 SQL Server 資料的 Active Directory 物件。</span><span class="sxs-lookup"><span data-stu-id="c91ef-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="c91ef-108">正在更新 Active Directory 物件中的 SQL 資料。</span><span class="sxs-lookup"><span data-stu-id="c91ef-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="c91ef-109">建立與其他 OLE DB 提供者的三向或四向聯結。</span><span class="sxs-lookup"><span data-stu-id="c91ef-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="c91ef-110">例如，Index Server、SQL Server 和 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="c91ef-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="c91ef-111">OLE DB 提供者支援兩種命令方言（LDAP 和 SQL）來存取目錄服務，並以表格形式傳回結果，可以使用 SQL Server 的分散式查詢進行查詢。</span><span class="sxs-lookup"><span data-stu-id="c91ef-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="c91ef-112">**若要啟動 SQL Query Analyzer**</span><span class="sxs-lookup"><span data-stu-id="c91ef-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="c91ef-113">首先，在連結到目錄服務的 SQL Server 上開啟 [SQL 查詢分析器](https://msdn.microsoft.com/library/Aa216983.aspx) ， (參閱建立連結的伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="c91ef-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="c91ef-114">執行 **SQL 查詢分析器** (啟動 \| 程式 \| Microsoft SQL Server 7.0) </span><span class="sxs-lookup"><span data-stu-id="c91ef-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="c91ef-115">登入 SQL Server 電腦。</span><span class="sxs-lookup"><span data-stu-id="c91ef-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="c91ef-116">在 [查詢] 視窗的編輯器窗格中輸入 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="c91ef-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="c91ef-117">按 F5 執行查詢。</span><span class="sxs-lookup"><span data-stu-id="c91ef-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="c91ef-118">下列各節提供更多詳細資料：</span><span class="sxs-lookup"><span data-stu-id="c91ef-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="c91ef-119">建立連結的伺服器</span><span class="sxs-lookup"><span data-stu-id="c91ef-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="c91ef-120">建立 SQL Server 驗證的登入</span><span class="sxs-lookup"><span data-stu-id="c91ef-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="c91ef-121">查詢目錄服務</span><span class="sxs-lookup"><span data-stu-id="c91ef-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="c91ef-122">建立連結的伺服器</span><span class="sxs-lookup"><span data-stu-id="c91ef-122">Creating a Linked Server</span></span>

<span data-ttu-id="c91ef-123">若要在 Windows 2000 伺服器目錄服務上設定分散式聯結，請建立連結的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c91ef-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="c91ef-124">若要這樣做，請使用 [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式來設定 ADSI 對應。</span><span class="sxs-lookup"><span data-stu-id="c91ef-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="c91ef-125">此程式會將名稱連結至 OLE DB 提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="c91ef-126">在下列範例中，請注意，與 [sp \_ Addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) 系統預存程式搭配使用的數個引數如下：</span><span class="sxs-lookup"><span data-stu-id="c91ef-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="c91ef-127">"ADSI" 是 **伺服器** 引數，而且將是這個連結伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="c91ef-128">"Active Directory Services 2.5" 是 **srvproduct** 引數，這是您要新增為連結伺服器的 OLE DB 資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="c91ef-129">"ADSDSOObject" 是 **提供者 \_ 名稱** 引數。</span><span class="sxs-lookup"><span data-stu-id="c91ef-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="c91ef-130">"adsdatasource" 是 **資料 \_ 源** 引數，這是 OLE DB 提供者所解釋的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="c91ef-131">[EXEC](https://msdn.microsoft.com/library/Aa258848.aspx)命令是用來執行系統預存程式。</span><span class="sxs-lookup"><span data-stu-id="c91ef-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="c91ef-132">若為 Windows 驗證的登入，自我對應就足以存取 SQL Server 安全性委派的目錄。</span><span class="sxs-lookup"><span data-stu-id="c91ef-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="c91ef-133">由於預設會針對透過 [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx)建立的連結伺服器建立自我對應，因此不需要其他登入對應。</span><span class="sxs-lookup"><span data-stu-id="c91ef-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="c91ef-134">針對 SQL Server 驗證的登入，您可以使用 [sp \_ Addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) 系統預存程式設定適當的登入和密碼，以便連接到目錄服務。</span><span class="sxs-lookup"><span data-stu-id="c91ef-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="c91ef-135">盡可能使用 Windows 驗證。</span><span class="sxs-lookup"><span data-stu-id="c91ef-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="c91ef-136">建立 SQL Server 驗證的登入</span><span class="sxs-lookup"><span data-stu-id="c91ef-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="c91ef-137">如果您想要使用 SQL Server 驗證的登入，而非 Windows 驗證，請將登入加入至連結的伺服器， (參閱上一節) 。</span><span class="sxs-lookup"><span data-stu-id="c91ef-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="c91ef-138">若要這樣做，請使用 [sp \_ Addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) 系統預存程式。</span><span class="sxs-lookup"><span data-stu-id="c91ef-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="c91ef-139">在下列範例中，有數個與 [sp \_ Addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) 系統預存程式搭配使用的引數：</span><span class="sxs-lookup"><span data-stu-id="c91ef-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="c91ef-140">"ADSI" 是 **rmtsvrname** 引數，這是在上一個範例中建立的連結伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="c91ef-141">"Fabrikam \\ Administrator" 是 **locallogin** 引數，這是本機伺服器上的登入，可以是 SQL Server 登入或 Windows NT 使用者。</span><span class="sxs-lookup"><span data-stu-id="c91ef-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="c91ef-142">"CN = Administrator，OU = Sales，DC = activeds，DC = Fabrikam，DC = com" 是 **rmtuser** 引數，這是您用來連接的使用者名稱，因為 **useself** 為 **false**。</span><span class="sxs-lookup"><span data-stu-id="c91ef-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="c91ef-143">"secret \* \* 2000" 是 **rmtpassword**，這是與 **rmtuser** 相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="c91ef-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="c91ef-144">[EXEC](https://msdn.microsoft.com/library/Aa258848.aspx)命令是用來執行系統預存程式。</span><span class="sxs-lookup"><span data-stu-id="c91ef-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="c91ef-145">查詢目錄服務</span><span class="sxs-lookup"><span data-stu-id="c91ef-145">Querying the Directory Service</span></span>

<span data-ttu-id="c91ef-146">當您建立連結的伺服器之後，請使用 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句將查詢傳送到目錄服務。</span><span class="sxs-lookup"><span data-stu-id="c91ef-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="c91ef-147">下列 SQL 查詢會使用 [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) 語句來建立虛擬資料表，以保存您的查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c91ef-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="c91ef-148">建立的視圖會命名為 "viewADContacts"。</span><span class="sxs-lookup"><span data-stu-id="c91ef-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="c91ef-149">第一個 [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句會定義從目錄服務查詢的資訊，並將其對應至資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="c91ef-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="c91ef-150">以方括弧括住的資訊表示放入虛擬資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="c91ef-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="c91ef-151">不在方括弧內的資訊代表從目錄服務中取出的資料。</span><span class="sxs-lookup"><span data-stu-id="c91ef-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="c91ef-152">請注意，從目錄服務抓取的資訊必須由其 LDAP 顯示名稱參考。</span><span class="sxs-lookup"><span data-stu-id="c91ef-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="c91ef-153">下一個語句是 [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) 語句。</span><span class="sxs-lookup"><span data-stu-id="c91ef-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="c91ef-154">這個語句有兩個引數： ADSI，也就是您所建立之連結伺服器的名稱，以及一個查詢語句。</span><span class="sxs-lookup"><span data-stu-id="c91ef-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="c91ef-155">查詢語句包含下列專案：</span><span class="sxs-lookup"><span data-stu-id="c91ef-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="c91ef-156">[SELECT](https://msdn.microsoft.com/library/Aa259187.aspx)語句包含將從目錄服務取得的資料清單。</span><span class="sxs-lookup"><span data-stu-id="c91ef-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="c91ef-157">您將需要使用 LDAP 顯示名稱來指出您要搜尋的資料。</span><span class="sxs-lookup"><span data-stu-id="c91ef-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="c91ef-158">[From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含將從中取得這項資訊的連結目錄伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c91ef-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="c91ef-159">[WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。</span><span class="sxs-lookup"><span data-stu-id="c91ef-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="c91ef-160">在此範例中，它會搜尋連絡人。</span><span class="sxs-lookup"><span data-stu-id="c91ef-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="c91ef-161">最後一個 [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句會用來從 view 中挑選要顯示的結果。</span><span class="sxs-lookup"><span data-stu-id="c91ef-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 





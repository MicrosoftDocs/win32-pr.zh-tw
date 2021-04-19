---
title: 使用 ActiveX Data Objects (ADO) 搜尋
description: " (ADO) 模型的 ActiveX 資料物件是由下表所列的物件所組成。"
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI，以 ADO 搜尋
- 使用 ActiveX Data Objects ADSI 搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969729"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="543e8-105">使用 ActiveX Data Objects (ADO) 搜尋</span><span class="sxs-lookup"><span data-stu-id="543e8-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="543e8-106"> (ADO) 模型的 ActiveX 資料物件是由下表所列的物件所組成。</span><span class="sxs-lookup"><span data-stu-id="543e8-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="543e8-107">Object</span><span class="sxs-lookup"><span data-stu-id="543e8-107">Object</span></span>         | <span data-ttu-id="543e8-108">描述</span><span class="sxs-lookup"><span data-stu-id="543e8-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543e8-109">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="543e8-109">**Connection**</span></span> | <span data-ttu-id="543e8-110">OLE DB 的資料來源（例如 ADSI）的開啟連接。</span><span class="sxs-lookup"><span data-stu-id="543e8-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="543e8-111">**命令**</span><span class="sxs-lookup"><span data-stu-id="543e8-111">**Command**</span></span>    | <span data-ttu-id="543e8-112">定義要針對資料來源執行的特定命令。</span><span class="sxs-lookup"><span data-stu-id="543e8-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="543e8-113">**參數**</span><span class="sxs-lookup"><span data-stu-id="543e8-113">**Parameter**</span></span>  | <span data-ttu-id="543e8-114">要提供給命令物件之任何參數的選擇性集合。</span><span class="sxs-lookup"><span data-stu-id="543e8-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="543e8-115">**記錄**</span><span class="sxs-lookup"><span data-stu-id="543e8-115">**RecordSet**</span></span>  | <span data-ttu-id="543e8-116">來自資料表、命令物件或 SQL 語法的一組記錄。</span><span class="sxs-lookup"><span data-stu-id="543e8-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="543e8-117">您可以建立不含任何基礎連線物件的記錄集。</span><span class="sxs-lookup"><span data-stu-id="543e8-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="543e8-118">**欄位**</span><span class="sxs-lookup"><span data-stu-id="543e8-118">**Field**</span></span>      | <span data-ttu-id="543e8-119">記錄集中資料的單一資料行。</span><span class="sxs-lookup"><span data-stu-id="543e8-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="543e8-120">**屬性**</span><span class="sxs-lookup"><span data-stu-id="543e8-120">**Property**</span></span>   | <span data-ttu-id="543e8-121">ADO 提供者所提供的值集合。</span><span class="sxs-lookup"><span data-stu-id="543e8-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="543e8-122">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="543e8-122">**Error**</span></span>      | <span data-ttu-id="543e8-123">包含有關資料存取錯誤的資料。</span><span class="sxs-lookup"><span data-stu-id="543e8-123">Contains data about data access errors.</span></span> <span data-ttu-id="543e8-124">當單一作業中發生錯誤時重新整理。</span><span class="sxs-lookup"><span data-stu-id="543e8-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="543e8-125">若要讓 ADO 與 ADSI 進行通訊，至少必須有兩個 ADO 物件： **連接** 和 **記錄集**。</span><span class="sxs-lookup"><span data-stu-id="543e8-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="543e8-126">這些 ADO 物件可分別用來驗證使用者和列舉結果。</span><span class="sxs-lookup"><span data-stu-id="543e8-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="543e8-127">一般而言，您也會使用 **Command** 物件來維護使用中的連接、指定查詢參數（例如頁面大小和搜尋範圍），以及執行查詢。</span><span class="sxs-lookup"><span data-stu-id="543e8-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="543e8-128">如需搜尋篩選語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="543e8-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="543e8-129">**Connection** 物件會載入 OLE DB 提供者，並驗證使用者認證。</span><span class="sxs-lookup"><span data-stu-id="543e8-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="543e8-130">在 Visual Basic 中，使用 "ADODB" 呼叫 **CreateObject** 函數。連接：建立 **連接** 物件的實例，然後將 **連接** 物件的 **提供者** 屬性設定為 "ADsDSOObject"。</span><span class="sxs-lookup"><span data-stu-id="543e8-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="543e8-131">ADODB.Connection」是 **連接** 物件的 ProgID，而 "ADsDSOObject" 是 ADSI 中 OLE DB 提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="543e8-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="543e8-132">如果未指定認證，則會使用目前登入之使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="543e8-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="543e8-133">下列程式碼範例顯示如何建立 **連接** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="543e8-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="543e8-134">下列程式碼範例顯示如何建立 **連接** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="543e8-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="543e8-135">下列程式碼範例顯示如何建立 **連接** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="543e8-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="543e8-136">請注意，您必須將 ADO 類型程式庫 (msadoXX.dll) 加入 Visual Basic 專案中的其中一個參考。</span><span class="sxs-lookup"><span data-stu-id="543e8-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="543e8-137">藉由設定 **連接** 物件的屬性來指定使用者驗證資料。</span><span class="sxs-lookup"><span data-stu-id="543e8-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="543e8-138">下表列出 ADSI 支援的使用者驗證屬性。</span><span class="sxs-lookup"><span data-stu-id="543e8-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="543e8-139">屬性</span><span class="sxs-lookup"><span data-stu-id="543e8-139">Property</span></span>           | <span data-ttu-id="543e8-140">描述</span><span class="sxs-lookup"><span data-stu-id="543e8-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543e8-141">「使用者識別碼」</span><span class="sxs-lookup"><span data-stu-id="543e8-141">"User ID"</span></span>          | <span data-ttu-id="543e8-142">字串，識別執行搜尋時所使用的安全性內容的使用者。</span><span class="sxs-lookup"><span data-stu-id="543e8-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="543e8-143">如需有關使用者名稱字串格式的詳細資訊，請參閱 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)。</span><span class="sxs-lookup"><span data-stu-id="543e8-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="543e8-144">如果未指定，則預設為已登入的使用者，或是由呼叫進程所模擬的使用者。</span><span class="sxs-lookup"><span data-stu-id="543e8-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="543e8-145">"Password"</span><span class="sxs-lookup"><span data-stu-id="543e8-145">"Password"</span></span>         | <span data-ttu-id="543e8-146">字串，指定使用者識別碼所識別之使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="543e8-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="543e8-147">「加密密碼」</span><span class="sxs-lookup"><span data-stu-id="543e8-147">"Encrypt Password"</span></span> | <span data-ttu-id="543e8-148">指定密碼是否經過加密的布林值。</span><span class="sxs-lookup"><span data-stu-id="543e8-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="543e8-149">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="543e8-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="543e8-150">"ADSI 旗標"</span><span class="sxs-lookup"><span data-stu-id="543e8-150">"ADSI Flag"</span></span>        | <span data-ttu-id="543e8-151">來自 [**ADS \_ 驗證 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) 列舉的一組旗標，可指定系結驗證選項。</span><span class="sxs-lookup"><span data-stu-id="543e8-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="543e8-152">預設值是零。</span><span class="sxs-lookup"><span data-stu-id="543e8-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="543e8-153">下列程式碼範例顯示如何在建立 **命令** 物件之前設定屬性。</span><span class="sxs-lookup"><span data-stu-id="543e8-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="543e8-154">第二個 ADO 物件是 **Command** 物件。</span><span class="sxs-lookup"><span data-stu-id="543e8-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="543e8-155">**命令** 物件的 ProgID 是 "ADODB"。</span><span class="sxs-lookup"><span data-stu-id="543e8-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="543e8-156">這個物件可讓您使用作用中連接將查詢語句和其他命令發出至 ADSI。</span><span class="sxs-lookup"><span data-stu-id="543e8-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="543e8-157">**命令** 物件會使用其 **ActiveConnection** 屬性來維護使用中的連接。</span><span class="sxs-lookup"><span data-stu-id="543e8-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="543e8-158">它也會維護 **CommandText** 屬性來保存使用者發出的查詢語句。</span><span class="sxs-lookup"><span data-stu-id="543e8-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="543e8-159">查詢語句會以 [SQL 方言](sql-dialect.md) 或 [LDAP 方言](ldap-dialect.md)表示。</span><span class="sxs-lookup"><span data-stu-id="543e8-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="543e8-160">下列程式碼範例示範如何建立 **命令** 物件。</span><span class="sxs-lookup"><span data-stu-id="543e8-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="543e8-161">在下列程式碼範例中，請將 ADO 類型程式庫 (msadoXX.dll) 包含為其中一個參考。</span><span class="sxs-lookup"><span data-stu-id="543e8-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="543e8-162">**命令** 物件的搜尋選項是藉由設定 **Properties** 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="543e8-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="543e8-163">下表列出 **屬性** 可接受的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="543e8-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="543e8-164">命名屬性</span><span class="sxs-lookup"><span data-stu-id="543e8-164">Named property</span></span>      | <span data-ttu-id="543e8-165">Description</span><span class="sxs-lookup"><span data-stu-id="543e8-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543e8-166">匿名</span><span class="sxs-lookup"><span data-stu-id="543e8-166">"Asynchronous"</span></span>      | <span data-ttu-id="543e8-167">指定搜尋為同步或非同步布林值。</span><span class="sxs-lookup"><span data-stu-id="543e8-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="543e8-168">預設值為 False (同步) 。</span><span class="sxs-lookup"><span data-stu-id="543e8-168">The default is False (synchronous).</span></span> <span data-ttu-id="543e8-169">同步搜尋會封鎖，直到伺服器傳回整個結果，或針對分頁搜尋（整頁）。</span><span class="sxs-lookup"><span data-stu-id="543e8-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="543e8-170">非同步搜尋會封鎖，直到搜尋結果的某個資料列可供使用，或直到 "Timeout" 屬性指定的時間已過為止。</span><span class="sxs-lookup"><span data-stu-id="543e8-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="543e8-171">「快取結果」</span><span class="sxs-lookup"><span data-stu-id="543e8-171">"Cache results"</span></span>     | <span data-ttu-id="543e8-172">指定是否應該在用戶端上快取結果的布林值。</span><span class="sxs-lookup"><span data-stu-id="543e8-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="543e8-173">預設值為 **true**;ADSI 會快取結果集。</span><span class="sxs-lookup"><span data-stu-id="543e8-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="543e8-174">針對大型結果集，可能需要關閉此選項。</span><span class="sxs-lookup"><span data-stu-id="543e8-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="543e8-175">「請參考參考」</span><span class="sxs-lookup"><span data-stu-id="543e8-175">"Chase referrals"</span></span>   | <span data-ttu-id="543e8-176">來自 ADS 的值會尋找指定搜尋一直追參考方式的 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) 。</span><span class="sxs-lookup"><span data-stu-id="543e8-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="543e8-177">預設值為 **ADS \_ \_ \_ 永遠不會進行參考**。如需此屬性的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。</span><span class="sxs-lookup"><span data-stu-id="543e8-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="543e8-178">「僅限資料行名稱」</span><span class="sxs-lookup"><span data-stu-id="543e8-178">"Column Names Only"</span></span> | <span data-ttu-id="543e8-179">布林值，表示搜尋只應取得已指派值之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="543e8-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="543e8-180">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="543e8-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="543e8-181">"Deref 別名"</span><span class="sxs-lookup"><span data-stu-id="543e8-181">"Deref Aliases"</span></span>     | <span data-ttu-id="543e8-182">布林值，指定是否解析找到之物件的別名。</span><span class="sxs-lookup"><span data-stu-id="543e8-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="543e8-183">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="543e8-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="543e8-184">[頁面大小]</span><span class="sxs-lookup"><span data-stu-id="543e8-184">"Page size"</span></span>         | <span data-ttu-id="543e8-185">整數值，這個值會開啟分頁，並指定要在結果集中傳回的最大物件數目。</span><span class="sxs-lookup"><span data-stu-id="543e8-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="543e8-186">預設值為 [無頁面大小]。</span><span class="sxs-lookup"><span data-stu-id="543e8-186">The default is no page size.</span></span> <span data-ttu-id="543e8-187">如需詳細資訊，請參閱 [取出大型結果集](retrieving-large-results-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="543e8-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="543e8-188">"SearchScope"</span><span class="sxs-lookup"><span data-stu-id="543e8-188">"SearchScope"</span></span>       | <span data-ttu-id="543e8-189">[**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)列舉中指定搜尋範圍的值。</span><span class="sxs-lookup"><span data-stu-id="543e8-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="543e8-190">預設值為 **ADS \_ 範圍 \_ 子樹**。</span><span class="sxs-lookup"><span data-stu-id="543e8-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="543e8-191">「大小限制」</span><span class="sxs-lookup"><span data-stu-id="543e8-191">"Size Limit"</span></span>        | <span data-ttu-id="543e8-192">指定搜尋大小限制的整數值。</span><span class="sxs-lookup"><span data-stu-id="543e8-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="543e8-193">針對 Active Directory，大小限制會指定傳回物件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="543e8-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="543e8-194">當達到大小限制時，伺服器會停止搜尋，並傳回累積的結果。</span><span class="sxs-lookup"><span data-stu-id="543e8-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="543e8-195">預設值為 [無限制]。</span><span class="sxs-lookup"><span data-stu-id="543e8-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="543e8-196">「排序依據」</span><span class="sxs-lookup"><span data-stu-id="543e8-196">"Sort on"</span></span>           | <span data-ttu-id="543e8-197">字串，指定用來做為排序關鍵字的屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="543e8-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="543e8-198">這個屬性只適用于支援 LDAP 控制項進行伺服器端排序的目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="543e8-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="543e8-199">Active Directory 支援排序控制項，但可能會影響伺服器效能，特別是當結果集很大時。</span><span class="sxs-lookup"><span data-stu-id="543e8-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="543e8-200">請注意，Active Directory 只支援單一排序索引鍵。</span><span class="sxs-lookup"><span data-stu-id="543e8-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="543e8-201">預設值為 [不排序]。</span><span class="sxs-lookup"><span data-stu-id="543e8-201">The default is no sorting.</span></span> |
| <span data-ttu-id="543e8-202">「時間限制」</span><span class="sxs-lookup"><span data-stu-id="543e8-202">"Time Limit"</span></span>        | <span data-ttu-id="543e8-203">整數值，指定搜尋的時間限制（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="543e8-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="543e8-204">到達時間限制時，伺服器會停止搜尋並傳回累積的結果。</span><span class="sxs-lookup"><span data-stu-id="543e8-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="543e8-205">預設值為 [無時間限制]。</span><span class="sxs-lookup"><span data-stu-id="543e8-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="543e8-206">中超</span><span class="sxs-lookup"><span data-stu-id="543e8-206">"Timeout"</span></span>           | <span data-ttu-id="543e8-207">指定用戶端超時值的整數值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="543e8-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="543e8-208">此值表示用戶端在停止搜尋之前等候伺服器結果的時間。</span><span class="sxs-lookup"><span data-stu-id="543e8-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="543e8-209">預設值為 [無時間輸出]。</span><span class="sxs-lookup"><span data-stu-id="543e8-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="543e8-210">下列程式碼範例顯示如何設定搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="543e8-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="543e8-211">第三個 ADO 物件是 **記錄集**。</span><span class="sxs-lookup"><span data-stu-id="543e8-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="543e8-212">當您在 **命令** 物件上叫用 **Execute** 方法時，就會取得這個物件。</span><span class="sxs-lookup"><span data-stu-id="543e8-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="543e8-213">**記錄集** 物件的主要功能是要列舉結果集並取得資料。</span><span class="sxs-lookup"><span data-stu-id="543e8-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="543e8-214">結果集可包含具有單一值或多個值的屬性值。</span><span class="sxs-lookup"><span data-stu-id="543e8-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="543e8-215">取得單一值屬性很簡單，類似于取得關係資料庫中的資料行值，例如：</span><span class="sxs-lookup"><span data-stu-id="543e8-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="543e8-216">不過，取得具有多個值的屬性比較有挑戰性。</span><span class="sxs-lookup"><span data-stu-id="543e8-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="543e8-217">在此情況下， **Field** 是陣列，而您必須檢查陣列的下限和上限，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="543e8-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="543e8-218">下列程式碼範例會停用 LDAP 伺服器上的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="543e8-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="543e8-219">如需 ADO 物件模型的詳細資訊，請參閱 [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15)。</span><span class="sxs-lookup"><span data-stu-id="543e8-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 


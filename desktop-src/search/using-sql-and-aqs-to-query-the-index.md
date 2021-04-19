---
description: 使用 Windows Search 來查詢索引的方式有好幾種。 本主題將概述 Advanced Query 語法 (AQS) 和結構化查詢語言 (SQL)  (SQL) 型方法。
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: 使用 SQL 和 AQS 方法來查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972178"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="10d5d-104">使用 SQL 和 AQS 方法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="10d5d-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="10d5d-105">使用 Windows Search 來查詢索引的方式有好幾種。</span><span class="sxs-lookup"><span data-stu-id="10d5d-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="10d5d-106">本主題將概述 Advanced Query 語法 (AQS) 和結構化查詢語言 (SQL)  (SQL) 型方法。</span><span class="sxs-lookup"><span data-stu-id="10d5d-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="10d5d-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="10d5d-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="10d5d-108">以 SQL 為基礎的查詢</span><span class="sxs-lookup"><span data-stu-id="10d5d-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="10d5d-109">使用 OLE DB</span><span class="sxs-lookup"><span data-stu-id="10d5d-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="10d5d-110">使用 ADO 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="10d5d-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="10d5d-111">在本機和遠端查詢中使用 SQL</span><span class="sxs-lookup"><span data-stu-id="10d5d-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="10d5d-112">以 AQS 為基礎的查詢</span><span class="sxs-lookup"><span data-stu-id="10d5d-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="10d5d-113">使用 ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="10d5d-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="10d5d-114">使用搜尋 ms 通訊協定</span><span class="sxs-lookup"><span data-stu-id="10d5d-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="10d5d-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="10d5d-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="10d5d-116">以 SQL 為基礎的查詢</span><span class="sxs-lookup"><span data-stu-id="10d5d-116">SQL Based Queries</span></span>

<span data-ttu-id="10d5d-117">SQL 是定義查詢的文字語言。</span><span class="sxs-lookup"><span data-stu-id="10d5d-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="10d5d-118">SQL 在許多不同的資料庫技術中都很常見。</span><span class="sxs-lookup"><span data-stu-id="10d5d-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="10d5d-119">Windows Search 會使用 SQL、執行它的子集，並藉由將專案加入至語言來延伸它。</span><span class="sxs-lookup"><span data-stu-id="10d5d-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="10d5d-120">Windows Search 所使用的 Windows Search SQL 會擴充部分的標準 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強它的實用性。</span><span class="sxs-lookup"><span data-stu-id="10d5d-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="10d5d-121">Windows Search SQL 的所有功能都與 Windows XP 和 Windows Server 2003 及更新版本上的 Windows Search 相容。</span><span class="sxs-lookup"><span data-stu-id="10d5d-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="10d5d-122">如需使用 SQL 語法 Windows Search 的詳細資訊，請參閱[WINDOWS SEARCH Sql 語法](-search-sql-ovwofsearchquery.md)的[Windows Search Sql 語法和總覽查詢索引](-search-sql-windowssearch-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="10d5d-123">下列查詢索引的方法是以 SQL 為基礎。</span><span class="sxs-lookup"><span data-stu-id="10d5d-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="10d5d-124">使用 OLE DB</span><span class="sxs-lookup"><span data-stu-id="10d5d-124">Using OLE DB</span></span>

<span data-ttu-id="10d5d-125">物件連結與嵌入資料庫 (OLE DB) 是 COM (API 的元件物件模型，可讓您以一致的方式存取不同類型的資料存放區，包括試算表之類的非關係資料庫。</span><span class="sxs-lookup"><span data-stu-id="10d5d-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="10d5d-126">OLE DB 會透過一組包含 Shell 資料來源、會話、命令和資料列集的抽象概念，將資料存放區與存取它的應用程式分開。</span><span class="sxs-lookup"><span data-stu-id="10d5d-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="10d5d-127">OLE DB 提供者是一種軟體元件，可執行 OLE DB 介面，從特定資料存放區提供資料給應用程式。</span><span class="sxs-lookup"><span data-stu-id="10d5d-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="10d5d-128">您可以使用 C 中的 OleDbConnection 和 OleDbSession 物件，以程式設計方式存取 Windows Search OLE DB 提供者 \# ，以及使用 c + + (中 Active Template Library) ATL (的 OLE DB 支援，) 透過 atlclidb. h。</span><span class="sxs-lookup"><span data-stu-id="10d5d-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="10d5d-129">唯一必須設定的屬性是提供者字串。</span><span class="sxs-lookup"><span data-stu-id="10d5d-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="10d5d-130">您可以使用下列字串：</span><span class="sxs-lookup"><span data-stu-id="10d5d-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="10d5d-131">或者，您可以藉由呼叫 [**ISearchQueryHelper：： get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)來取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="10d5d-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="10d5d-132">如需範例，請參閱使用 [ISearchQueryHelper](#using-isearchqueryhelper) 。</span><span class="sxs-lookup"><span data-stu-id="10d5d-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="10d5d-133">Windows Search OLE DB 提供者是唯讀的，而且支援 SELECT 和 GROUP ON 語句。</span><span class="sxs-lookup"><span data-stu-id="10d5d-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="10d5d-134">不支援 INSERT 和 DELETE 子句。</span><span class="sxs-lookup"><span data-stu-id="10d5d-134">INSERT and DELETE statements are not supported.</span></span>

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

<span data-ttu-id="10d5d-135">如需 OLE DB 的詳細資訊，請參閱 [OLE DB 程式設計總覽](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="10d5d-136">如需 OLE DB 之 .NET Framework Data Provider 的詳細資訊，請參閱 system.string [命名空間](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) 檔。</span><span class="sxs-lookup"><span data-stu-id="10d5d-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="10d5d-137">使用 ADO 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="10d5d-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="10d5d-138">Microsoft ActiveX Data Objects (ADO) 和 ADO.NET 可讓您撰寫用戶端應用程式，以透過提供者存取及操作資料庫伺服器中的資料。</span><span class="sxs-lookup"><span data-stu-id="10d5d-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="10d5d-139">Windows Search 是唯讀技術：您可以使用桌面搜尋來取出資料，但無法使用 Windows Search 來變更資料。</span><span class="sxs-lookup"><span data-stu-id="10d5d-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="10d5d-140">不過，您可以將搜尋結果傳遞給可以變更資料的技術。</span><span class="sxs-lookup"><span data-stu-id="10d5d-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="10d5d-141">下列程式碼範例示範如何開啟與資料來源的連接、使用 [Windows Search 的 SQL](-search-sql-ovwofsearchquery.md) SELECT 語句來建立和開啟記錄集，以及從索引取得五個最大檔案的 url。</span><span class="sxs-lookup"><span data-stu-id="10d5d-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="10d5d-142">如需如何取得連接字串的相關資訊，請參閱 [使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)和 [ISearchQueryHelper：： get \_ 連接字串](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="10d5d-143">ADO 和 VBScript</span><span class="sxs-lookup"><span data-stu-id="10d5d-143">ADO and VBScript</span></span>

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a><span data-ttu-id="10d5d-144">ADO 和 c + +</span><span class="sxs-lookup"><span data-stu-id="10d5d-144">ADO and C++</span></span>

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="10d5d-145">ADO 和</span><span class="sxs-lookup"><span data-stu-id="10d5d-145">ADO and VisualBasic</span></span>

<span data-ttu-id="10d5d-146">先在您的專案中加入 ADODB 的參考</span><span class="sxs-lookup"><span data-stu-id="10d5d-146">First add a reference to ADODB in your project</span></span>

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a><span data-ttu-id="10d5d-147">ADO.NET 和 C\#</span><span class="sxs-lookup"><span data-stu-id="10d5d-147">ADO.NET and C\#</span></span>

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="10d5d-148">在本機和遠端查詢中使用 SQL</span><span class="sxs-lookup"><span data-stu-id="10d5d-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="10d5d-149">您可以在本機或遠端執行查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="10d5d-150">下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的本機查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="10d5d-151">本機查詢只會查詢本機 SystemIndex 目錄。</span><span class="sxs-lookup"><span data-stu-id="10d5d-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="10d5d-152">下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的遠端查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="10d5d-153">加入 ComputerName 會將前一個範例轉換為遠端查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="10d5d-154">根據預設，Windows XP 和 Windows Server 2003 沒有安裝 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="10d5d-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="10d5d-155">只有 Windows Search 4 (WS4) 提供遠端查詢支援。</span><span class="sxs-lookup"><span data-stu-id="10d5d-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="10d5d-156">舊版的 Windows 桌面搜尋 (WDS) ，例如3.01 和更早版本，不支援遠端查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="10d5d-157">您可以使用 Windows 檔案總管來查詢遠端電腦的本機索引，以尋找 "file：" 通訊協定) 所處理的檔案系統專案 (專案。</span><span class="sxs-lookup"><span data-stu-id="10d5d-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="10d5d-158">若要透過遠端查詢取得專案，專案必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="10d5d-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="10d5d-159">可透過通用命名慣例 (UNC) 路徑來存取。</span><span class="sxs-lookup"><span data-stu-id="10d5d-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="10d5d-160">存在於用戶端可存取的遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="10d5d-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="10d5d-161">將其安全性設定為允許用戶端擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="10d5d-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="10d5d-162">Windows 檔案總管具有共用專案的功能，包括網路和共用中心中的「公用」共用 (的「公用」共用 \\ \\ \\ \\ ... ) ，以及「使用者」共用 (\\ \\ 電腦 \\ 使用者 \\ ... ) 透過共用嚮導共用的專案。</span><span class="sxs-lookup"><span data-stu-id="10d5d-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="10d5d-163">在您共用 (s) 的資料夾之後，您可以在 FROM 子句中指定遠端電腦的電腦名稱稱，並在範圍子句中的遠端電腦上指定 UNC 路徑，以查詢本機索引，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="10d5d-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="10d5d-164">以 AQS 為基礎的查詢</span><span class="sxs-lookup"><span data-stu-id="10d5d-164">AQS Based Queries</span></span>

<span data-ttu-id="10d5d-165">AQS 是 Windows Search 用來查詢索引，以及精簡和縮小搜尋參數的預設查詢語法。</span><span class="sxs-lookup"><span data-stu-id="10d5d-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="10d5d-166">雖然 AQS 主要是使用者面向，但可供開發人員用來以程式設計方式建立查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="10d5d-167">在 Windows 7 的標準 AQS 中引進，而且必須在 Windows 7 和更新版本中使用，以程式設計方式產生 AQS 查詢。</span><span class="sxs-lookup"><span data-stu-id="10d5d-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="10d5d-168">如需 AQS 的詳細資訊，請參閱以程式設計 [方式使用 Advanced Query 語法](-search-3x-advancedquerysyntax.md)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="10d5d-169">下列查詢索引的方法是以 AQS 為基礎。</span><span class="sxs-lookup"><span data-stu-id="10d5d-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="10d5d-170">使用 ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="10d5d-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="10d5d-171">您可以使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面開發元件或協助程式類別來查詢索引，此介面可讓您利用系統的一些功能，並簡化 Windows Search 的使用。</span><span class="sxs-lookup"><span data-stu-id="10d5d-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="10d5d-172">此介面可協助您：</span><span class="sxs-lookup"><span data-stu-id="10d5d-172">This interface helps you:</span></span>

- <span data-ttu-id="10d5d-173">取得連接到 Windows Search 資料庫 OLE DB 連接字串。</span><span class="sxs-lookup"><span data-stu-id="10d5d-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="10d5d-174">將使用者查詢從 AQS 轉換成 Windows Search SQL。</span><span class="sxs-lookup"><span data-stu-id="10d5d-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="10d5d-175">此介面會實作為 helper 類別以進行 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ，並藉由呼叫 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得，如下列 c + + 範例所示。</span><span class="sxs-lookup"><span data-stu-id="10d5d-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

<span data-ttu-id="10d5d-176">若要執行 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面，請參閱 [使用 ISearchQueryHelper 介面](-search-3x-wds-qryidx-searchqueryhelper.md) 和 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 參考主題。</span><span class="sxs-lookup"><span data-stu-id="10d5d-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="10d5d-177">舊版 Microsoft Windows 桌面搜尋 (WDS) 2x 相容性：在執行 Windows XP 和 Windows Server 2003 和更新版本的電腦上， [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) 已被取代。</span><span class="sxs-lookup"><span data-stu-id="10d5d-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="10d5d-178">相反地，開發人員應該使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 取得連接字串、將使用者的查詢剖析為 SQL，然後查詢 OLE DB。</span><span class="sxs-lookup"><span data-stu-id="10d5d-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="10d5d-179">使用搜尋 ms 通訊協定</span><span class="sxs-lookup"><span data-stu-id="10d5d-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="10d5d-180">**搜尋 ms** [應用程式協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是啟動應用程式（例如 Windows 檔案總管）以查詢 Windows Search 索引的慣例。</span><span class="sxs-lookup"><span data-stu-id="10d5d-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="10d5d-181">它可讓您使用參數值引數建立查詢，包括屬性引數、先前儲存的搜尋、先進的查詢語法 (AQS) 、自然查詢語法 (NQS) ，以及索引子和查詢本身的語言代碼識別碼 (Lcid) 。</span><span class="sxs-lookup"><span data-stu-id="10d5d-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="10d5d-182">如需搜尋 ms 通訊協定語法的詳細資訊，請參閱 [使用搜尋 Ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10d5d-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="10d5d-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d5d-184">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="10d5d-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="10d5d-185">使用 ISearchQueryHelper 查詢索引</span><span class="sxs-lookup"><span data-stu-id="10d5d-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="10d5d-186">使用搜尋-ms 通訊協定來查詢索引</span><span class="sxs-lookup"><span data-stu-id="10d5d-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="10d5d-187">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="10d5d-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="10d5d-188">以程式設計方式使用 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="10d5d-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

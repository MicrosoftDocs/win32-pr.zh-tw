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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>使用 SQL 和 AQS 方法來查詢索引

使用 Windows Search 來查詢索引的方式有好幾種。 本主題將概述 Advanced Query 語法 (AQS) 和結構化查詢語言 (SQL)  (SQL) 型方法。

本主題的組織方式如下：

- [以 SQL 為基礎的查詢](#sql-based-queries)
  - [使用 OLE DB](#using-ole-db)
  - [使用 ADO 和 ADO.NET](#using-ado-and-adonet)
  - [在本機和遠端查詢中使用 SQL](#using-sql-in-local-and-remote-queries)
- [以 AQS 為基礎的查詢](#aqs-based-queries)
  - [使用 ISearchQueryHelper](#using-isearchqueryhelper)
  - [使用搜尋 ms 通訊協定](#using-the-search-ms-protocol)
- [相關主題](#related-topics)

## <a name="sql-based-queries"></a>以 SQL 為基礎的查詢

SQL 是定義查詢的文字語言。 SQL 在許多不同的資料庫技術中都很常見。 Windows Search 會使用 SQL、執行它的子集，並藉由將專案加入至語言來延伸它。 Windows Search 所使用的 Windows Search SQL 會擴充部分的標準 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強它的實用性。 Windows Search SQL 的所有功能都與 Windows XP 和 Windows Server 2003 及更新版本上的 Windows Search 相容。

如需使用 SQL 語法 Windows Search 的詳細資訊，請參閱[WINDOWS SEARCH Sql 語法](-search-sql-ovwofsearchquery.md)的[Windows Search Sql 語法和總覽查詢索引](-search-sql-windowssearch-entry.md)。

下列查詢索引的方法是以 SQL 為基礎。

### <a name="using-ole-db"></a>使用 OLE DB

物件連結與嵌入資料庫 (OLE DB) 是 COM (API 的元件物件模型，可讓您以一致的方式存取不同類型的資料存放區，包括試算表之類的非關係資料庫。 OLE DB 會透過一組包含 Shell 資料來源、會話、命令和資料列集的抽象概念，將資料存放區與存取它的應用程式分開。 OLE DB 提供者是一種軟體元件，可執行 OLE DB 介面，從特定資料存放區提供資料給應用程式。

您可以使用 C 中的 OleDbConnection 和 OleDbSession 物件，以程式設計方式存取 Windows Search OLE DB 提供者 \# ，以及使用 c + + (中 Active Template Library) ATL (的 OLE DB 支援，) 透過 atlclidb. h。 唯一必須設定的屬性是提供者字串。

您可以使用下列字串：

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

或者，您可以藉由呼叫 [**ISearchQueryHelper：： get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)來取得連接字串。 如需範例，請參閱使用 [ISearchQueryHelper](#using-isearchqueryhelper) 。

> [!Note]  
> Windows Search OLE DB 提供者是唯讀的，而且支援 SELECT 和 GROUP ON 語句。 不支援 INSERT 和 DELETE 子句。

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

如需 OLE DB 的詳細資訊，請參閱 [OLE DB 程式設計總覽](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)。 如需 OLE DB 之 .NET Framework Data Provider 的詳細資訊，請參閱 system.string [命名空間](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) 檔。

### <a name="using-ado-and-adonet"></a>使用 ADO 和 ADO.NET

Microsoft ActiveX Data Objects (ADO) 和 ADO.NET 可讓您撰寫用戶端應用程式，以透過提供者存取及操作資料庫伺服器中的資料。 Windows Search 是唯讀技術：您可以使用桌面搜尋來取出資料，但無法使用 Windows Search 來變更資料。 不過，您可以將搜尋結果傳遞給可以變更資料的技術。

下列程式碼範例示範如何開啟與資料來源的連接、使用 [Windows Search 的 SQL](-search-sql-ovwofsearchquery.md) SELECT 語句來建立和開啟記錄集，以及從索引取得五個最大檔案的 url。

> [!Note]  
> 如需如何取得連接字串的相關資訊，請參閱 [使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)和 [ISearchQueryHelper：： get \_ 連接字串](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)。

#### <a name="ado-and-vbscript"></a>ADO 和 VBScript

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

#### <a name="ado-and-c"></a>ADO 和 c + +

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

#### <a name="ado-and-visualbasic"></a>ADO 和

先在您的專案中加入 ADODB 的參考

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

#### <a name="adonet-and-c"></a>ADO.NET 和 C\#

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

### <a name="using-sql-in-local-and-remote-queries"></a>在本機和遠端查詢中使用 SQL

您可以在本機或遠端執行查詢。 下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的本機查詢。 本機查詢只會查詢本機 SystemIndex 目錄。

```sql
FROM SystemIndex
```

下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的遠端查詢。 加入 ComputerName 會將前一個範例轉換為遠端查詢。

```sql
FROM [<ComputerName>.]SystemIndex
```

根據預設，Windows XP 和 Windows Server 2003 沒有安裝 Windows Search。 只有 Windows Search 4 (WS4) 提供遠端查詢支援。 舊版的 Windows 桌面搜尋 (WDS) ，例如3.01 和更早版本，不支援遠端查詢。 您可以使用 Windows 檔案總管來查詢遠端電腦的本機索引，以尋找 "file：" 通訊協定) 所處理的檔案系統專案 (專案。

若要透過遠端查詢取得專案，專案必須符合下列需求：

- 可透過通用命名慣例 (UNC) 路徑來存取。
- 存在於用戶端可存取的遠端電腦上。
- 將其安全性設定為允許用戶端擁有讀取權限。

Windows 檔案總管具有共用專案的功能，包括網路和共用中心中的「公用」共用 (的「公用」共用 \\ \\ \\ \\ ... ) ，以及「使用者」共用 (\\ \\ 電腦 \\ 使用者 \\ ... ) 透過共用嚮導共用的專案。 在您共用 (s) 的資料夾之後，您可以在 FROM 子句中指定遠端電腦的電腦名稱稱，並在範圍子句中的遠端電腦上指定 UNC 路徑，以查詢本機索引，如下列範例所示：

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>以 AQS 為基礎的查詢

AQS 是 Windows Search 用來查詢索引，以及精簡和縮小搜尋參數的預設查詢語法。 雖然 AQS 主要是使用者面向，但可供開發人員用來以程式設計方式建立查詢。 在 Windows 7 的標準 AQS 中引進，而且必須在 Windows 7 和更新版本中使用，以程式設計方式產生 AQS 查詢。 如需 AQS 的詳細資訊，請參閱以程式設計 [方式使用 Advanced Query 語法](-search-3x-advancedquerysyntax.md)。

下列查詢索引的方法是以 AQS 為基礎。

### <a name="using-isearchqueryhelper"></a>使用 ISearchQueryHelper

您可以使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面開發元件或協助程式類別來查詢索引，此介面可讓您利用系統的一些功能，並簡化 Windows Search 的使用。 此介面可協助您：

- 取得連接到 Windows Search 資料庫 OLE DB 連接字串。
- 將使用者查詢從 AQS 轉換成 Windows Search SQL。

此介面會實作為 helper 類別以進行 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ，並藉由呼叫 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得，如下列 c + + 範例所示。

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

若要執行 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面，請參閱 [使用 ISearchQueryHelper 介面](-search-3x-wds-qryidx-searchqueryhelper.md) 和 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 參考主題。

> [!Note]  
> 舊版 Microsoft Windows 桌面搜尋 (WDS) 2x 相容性：在執行 Windows XP 和 Windows Server 2003 和更新版本的電腦上， [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) 已被取代。 相反地，開發人員應該使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 取得連接字串、將使用者的查詢剖析為 SQL，然後查詢 OLE DB。

### <a name="using-the-search-ms-protocol"></a>使用搜尋 ms 通訊協定

**搜尋 ms** [應用程式協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是啟動應用程式（例如 Windows 檔案總管）以查詢 Windows Search 索引的慣例。 它可讓您使用參數值引數建立查詢，包括屬性引數、先前儲存的搜尋、先進的查詢語法 (AQS) 、自然查詢語法 (NQS) ，以及索引子和查詢本身的語言代碼識別碼 (Lcid) 。

如需搜尋 ms 通訊協定語法的詳細資訊，請參閱 [使用搜尋 Ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以程式設計方式查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[使用搜尋-ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)
</dt> <dt>

[以程式設計方式使用 Advanced 查詢語法](-search-3x-advancedquerysyntax.md)
</dt> </dl>

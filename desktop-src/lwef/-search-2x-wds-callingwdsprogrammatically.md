---
title: 以程式設計方式呼叫 WDS
description: 您可以使用 ISearchDesktop 介面中的 ExecuteQuery 和 ExecuteSQLQuery 方法，以程式設計方式查詢 Microsoft Windows 桌面搜尋 (WDS) 2.x。
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682295"
---
# <a name="calling-wds-programmatically"></a>以程式設計方式呼叫 WDS

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

您可以使用 [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85))介面中的 **ExecuteQuery** 和 **ExecuteSQLQuery** 方法，以程式設計方式查詢 Microsoft Windows 桌面搜尋 (WDS) 2.x。 **ExecuteQuery** 方法會根據以參數形式傳遞的查詢文字、資料行和限制，傳回索引中的記錄集。 **ExecuteSQLQuery** 方法也會傳回結果的記錄集，但需要傳入 (SQL) 命令的確切結構化查詢語言 (SQL) 。 大部分案例都應該使用 **ExecuteQuery** 。

## <a name="regular-queries"></a>一般查詢

一般查詢是由使用者輸入至 WDS 輸入方塊的查詢，包括所有 [先進的查詢語法](-search-2x-wds-aqsreference.md)。 此查詢會傳遞至 **ExecuteQuery** ，以及要傳回的 WDS 2.x [架構](-search-2x-wds-schematable.md) 資料行、資料行和排序結果的順序，以及用來限制結果的任何子句。

方法的格式如下：

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| 方向 | 變數           | 描述                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 位於        | lpcwstrQuery       | 查詢文字。 此查詢與在 Windows 桌面搜尋使用者介面的 [搜尋] 文字方塊中輸入的查詢相同。 <br/> 例如：`"from:Zara dinner plans"`<br/> |
| 位於        | lpcwstrColumn      | 要包含的資料行（以逗號分隔）。 <br/> 例如：`"DocTitle, Url"`<br/>                                                                                            |
| 位於        | lpcwstrSort        | 要排序的覆寫資料行，其後依 ASC 遞增或遞減（遞減）。 <br/> 例如：`"LastAuthor DESC"`<br/>                                                  |
| 位於        | lpcwstrRestriction | 在 Windows 桌面搜尋中，透過 WHERE 子句附加的限制。 <br/> 例如：`"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| 外       | ppiRs              | 產生的記錄集<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>SQL 查詢

**ISearchDesktop.Exe的 cuteSQLQuery** 方法可用來傳送直接 WDS 資料庫查詢。 查詢的語法類似于 SharePoint Server 所使用的語法，以及使用 Monarch 樣式 SQL GROUP BY 子句的能力。 查詢會完全依照傳入的方式執行，而不會在 ExecuteQuery API 執行時進行額外的 Advanced Query 語法處理。

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

方法的格式如下：

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| 方向 | 變數   | 描述                                    |
|-----------|------------|------------------------------------------------|
| 位於        | lpcwstrSQL | 要針對 WDS 索引執行的 SQL 查詢 |
| 外       | ppiRs      | 產生的記錄集                       |



 

資源：

-   ISearchDesktop 介面的支援檔案： https://addins.msn.com/support/WDSSDK.zip
-   ISearchDesktop c # 範例： https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>C + + 程式碼範例

> [!Note]
>
> 此程式碼和資訊是以「原樣」提供，不含任何明示或默示擔保，包括但不限於特定用途的適售性及/或適用性默示擔保。
>
> 著作權 (C) Microsoft。 著作權所有，並保留一切權利。

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[進階查詢語法](-search-2x-wds-aqsreference.md)
</dt> <dt>

[認知類型](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[從 Web Pages 呼叫 WDS](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 


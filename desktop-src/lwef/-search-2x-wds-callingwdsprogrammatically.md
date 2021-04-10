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
# <a name="calling-wds-programmatically"></a><span data-ttu-id="80e87-103">以程式設計方式呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="80e87-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="80e87-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="80e87-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="80e87-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="80e87-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="80e87-106">您可以使用 [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85))介面中的 **ExecuteQuery** 和 **ExecuteSQLQuery** 方法，以程式設計方式查詢 Microsoft Windows 桌面搜尋 (WDS) 2.x。</span><span class="sxs-lookup"><span data-stu-id="80e87-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="80e87-107">**ExecuteQuery** 方法會根據以參數形式傳遞的查詢文字、資料行和限制，傳回索引中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="80e87-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="80e87-108">**ExecuteSQLQuery** 方法也會傳回結果的記錄集，但需要傳入 (SQL) 命令的確切結構化查詢語言 (SQL) 。</span><span class="sxs-lookup"><span data-stu-id="80e87-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="80e87-109">大部分案例都應該使用 **ExecuteQuery** 。</span><span class="sxs-lookup"><span data-stu-id="80e87-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="80e87-110">一般查詢</span><span class="sxs-lookup"><span data-stu-id="80e87-110">Regular Queries</span></span>

<span data-ttu-id="80e87-111">一般查詢是由使用者輸入至 WDS 輸入方塊的查詢，包括所有 [先進的查詢語法](-search-2x-wds-aqsreference.md)。</span><span class="sxs-lookup"><span data-stu-id="80e87-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="80e87-112">此查詢會傳遞至 **ExecuteQuery** ，以及要傳回的 WDS 2.x [架構](-search-2x-wds-schematable.md) 資料行、資料行和排序結果的順序，以及用來限制結果的任何子句。</span><span class="sxs-lookup"><span data-stu-id="80e87-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="80e87-113">方法的格式如下：</span><span class="sxs-lookup"><span data-stu-id="80e87-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="80e87-114">方向</span><span class="sxs-lookup"><span data-stu-id="80e87-114">Direction</span></span> | <span data-ttu-id="80e87-115">變數</span><span class="sxs-lookup"><span data-stu-id="80e87-115">Variable</span></span>           | <span data-ttu-id="80e87-116">描述</span><span class="sxs-lookup"><span data-stu-id="80e87-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e87-117">位於</span><span class="sxs-lookup"><span data-stu-id="80e87-117">In</span></span>        | <span data-ttu-id="80e87-118">lpcwstrQuery</span><span class="sxs-lookup"><span data-stu-id="80e87-118">lpcwstrQuery</span></span>       | <span data-ttu-id="80e87-119">查詢文字。</span><span class="sxs-lookup"><span data-stu-id="80e87-119">The query text.</span></span> <span data-ttu-id="80e87-120">此查詢與在 Windows 桌面搜尋使用者介面的 [搜尋] 文字方塊中輸入的查詢相同。</span><span class="sxs-lookup"><span data-stu-id="80e87-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="80e87-121">例如：`"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="80e87-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="80e87-122">位於</span><span class="sxs-lookup"><span data-stu-id="80e87-122">In</span></span>        | <span data-ttu-id="80e87-123">lpcwstrColumn</span><span class="sxs-lookup"><span data-stu-id="80e87-123">lpcwstrColumn</span></span>      | <span data-ttu-id="80e87-124">要包含的資料行（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="80e87-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="80e87-125">例如：`"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="80e87-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="80e87-126">位於</span><span class="sxs-lookup"><span data-stu-id="80e87-126">In</span></span>        | <span data-ttu-id="80e87-127">lpcwstrSort</span><span class="sxs-lookup"><span data-stu-id="80e87-127">lpcwstrSort</span></span>        | <span data-ttu-id="80e87-128">要排序的覆寫資料行，其後依 ASC 遞增或遞減（遞減）。</span><span class="sxs-lookup"><span data-stu-id="80e87-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="80e87-129">例如：`"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="80e87-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="80e87-130">位於</span><span class="sxs-lookup"><span data-stu-id="80e87-130">In</span></span>        | <span data-ttu-id="80e87-131">lpcwstrRestriction</span><span class="sxs-lookup"><span data-stu-id="80e87-131">lpcwstrRestriction</span></span> | <span data-ttu-id="80e87-132">在 Windows 桌面搜尋中，透過 WHERE 子句附加的限制。</span><span class="sxs-lookup"><span data-stu-id="80e87-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="80e87-133">例如：`"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="80e87-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="80e87-134">外</span><span class="sxs-lookup"><span data-stu-id="80e87-134">Out</span></span>       | <span data-ttu-id="80e87-135">ppiRs</span><span class="sxs-lookup"><span data-stu-id="80e87-135">ppiRs</span></span>              | <span data-ttu-id="80e87-136">產生的記錄集</span><span class="sxs-lookup"><span data-stu-id="80e87-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="80e87-137">SQL 查詢</span><span class="sxs-lookup"><span data-stu-id="80e87-137">SQL Queries</span></span>

<span data-ttu-id="80e87-138">**ISearchDesktop.Exe的 cuteSQLQuery** 方法可用來傳送直接 WDS 資料庫查詢。</span><span class="sxs-lookup"><span data-stu-id="80e87-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="80e87-139">查詢的語法類似于 SharePoint Server 所使用的語法，以及使用 Monarch 樣式 SQL GROUP BY 子句的能力。</span><span class="sxs-lookup"><span data-stu-id="80e87-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="80e87-140">查詢會完全依照傳入的方式執行，而不會在 ExecuteQuery API 執行時進行額外的 Advanced Query 語法處理。</span><span class="sxs-lookup"><span data-stu-id="80e87-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="80e87-141">方法的格式如下：</span><span class="sxs-lookup"><span data-stu-id="80e87-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="80e87-142">方向</span><span class="sxs-lookup"><span data-stu-id="80e87-142">Direction</span></span> | <span data-ttu-id="80e87-143">變數</span><span class="sxs-lookup"><span data-stu-id="80e87-143">Variable</span></span>   | <span data-ttu-id="80e87-144">描述</span><span class="sxs-lookup"><span data-stu-id="80e87-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="80e87-145">位於</span><span class="sxs-lookup"><span data-stu-id="80e87-145">In</span></span>        | <span data-ttu-id="80e87-146">lpcwstrSQL</span><span class="sxs-lookup"><span data-stu-id="80e87-146">lpcwstrSQL</span></span> | <span data-ttu-id="80e87-147">要針對 WDS 索引執行的 SQL 查詢</span><span class="sxs-lookup"><span data-stu-id="80e87-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="80e87-148">外</span><span class="sxs-lookup"><span data-stu-id="80e87-148">Out</span></span>       | <span data-ttu-id="80e87-149">ppiRs</span><span class="sxs-lookup"><span data-stu-id="80e87-149">ppiRs</span></span>      | <span data-ttu-id="80e87-150">產生的記錄集</span><span class="sxs-lookup"><span data-stu-id="80e87-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="80e87-151">資源：</span><span class="sxs-lookup"><span data-stu-id="80e87-151">Resources:</span></span>

-   <span data-ttu-id="80e87-152">ISearchDesktop 介面的支援檔案： https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="80e87-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="80e87-153">ISearchDesktop c # 範例： https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="80e87-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="80e87-154">C + + 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="80e87-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="80e87-155">此程式碼和資訊是以「原樣」提供，不含任何明示或默示擔保，包括但不限於特定用途的適售性及/或適用性默示擔保。</span><span class="sxs-lookup"><span data-stu-id="80e87-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="80e87-156">著作權 (C) Microsoft。</span><span class="sxs-lookup"><span data-stu-id="80e87-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="80e87-157">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="80e87-157">All rights reserved.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="80e87-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="80e87-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="80e87-159">**參考**</span><span class="sxs-lookup"><span data-stu-id="80e87-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80e87-160">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="80e87-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="80e87-161">認知類型</span><span class="sxs-lookup"><span data-stu-id="80e87-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="80e87-162">從 Web Pages 呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="80e87-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 


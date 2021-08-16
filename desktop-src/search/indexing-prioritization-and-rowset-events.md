---
description: 概述 Windows 7 的索引優先順序和資料列集事件的簡介。
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: 在 Windows 7 中編制優先順序和資料列集事件的索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680499"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>在 Windows 7 中編制優先順序和資料列集事件的索引

本主題概述 Windows 7 的索引優先順序和資料列集事件的簡介。

本主題的組織方式如下：

-   [編制優先順序和資料列集事件的索引](#indexing-prioritization-and-rowset-events)
    -   [IRowsetPriorization 範例](#irowsetpriorization-examples)
    -   [IRowsetPrioritization 事件](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>編制優先順序和資料列集事件的索引

在 Windows 7？（含）以後版本中，有一個優先順序堆疊，在此堆疊中，用戶端可以要求在該查詢中使用的範圍優先于一般專案的上方。

此優先順序堆疊具有下列特性：

-   堆疊中的專案可以有前景、高或低優先順序：
    -   **前景**：會略過輪詢邏輯，並以機器允許的速度快速進行索引編制。
    -   **高**：已使用輪詢要求優先順序。
    -   **低**：已要求優先處理，而不是堆疊上其他範圍的費用，但高於未優先的索引。
-   任何高或前景優先順序的要求都會自動將要求的查詢帶到堆疊的頂端。
-   只有堆疊頂端的專案可以有前景優先順序。
-   具有前景優先順序的查詢會在優先順序中向下遇到，會收到事件，通知它已遺失前景優先順序，且已成為輪詢的高優先權。

優先權堆疊會設定在索引子中處理之專案的整體優先順序，如下所示：

-   高優先順序通知沒有輪詢，通常只會針對少數專案傳送。 例如，Windows 檔案總管會針對小型複製引擎作業使用此優先順序。
-   優先權堆疊是堆疊的最上層，具有輪詢，而是最後要求的優先權查詢。
-   堆疊中的第二個查詢。
-   堆疊中的第三個查詢。
-   堆疊中的第四個查詢等等。
-   一般優先順序專案。
-   已刪除的專案。
    > [!Note]  
    > 每個群組內的專案會在內部透過較舊的每個專案語義排列優先順序。

     

### <a name="irowsetpriorization-examples"></a>IRowsetPriorization 範例

優先順序工作的主要 API 可透過下列介面取得，您可以藉由查詢傳回的資料列集來呼叫這些 API：


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



資料列集優先順序的運作方式如下：

1.  在索引子資料列集上使用 [IUnknown：： QueryInterface 方法](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))取得 [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) 。 **DBPROP \_** 在執行查詢之前，必須先使用 OLE DB [ICommandProperties：： SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85))方法將 ENABLEROWSETEVENTS 設為 **TRUE** ，才能使用資料列集優先順序。
2.  [**IRowsetPrioritization：： SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) 會針對屬於查詢的範圍設定優先順序，以及在查詢範圍內有未處理的檔編制索引時，產生範圍統計事件的間隔。 如果優先權層級設定為 [預設值]，就會引發此事件。
3.  [**IRowsetPrioritization：： GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) 可用來取得範圍中的索引項目目數、要在範圍中新增的未處理檔數目，以及在此範圍內需要重新編制索引的檔數目。

### <a name="irowsetprioritization-events"></a>IRowsetPrioritization 事件

[**ROWSETEVENT \_ 類型**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)列舉的 [**IRowsetEvents：： OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent)中有三個數據列集事件：


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



資料列集事件如下所示：

-   **ROWSETEVENT \_ 類型 \_ DATAEXPIRED** 事件表示支援資料列集的資料已過期，且應要求新的資料列集。
-   資料列 **集 \_ 型別 \_ FOREGROUNDLOST** 事件表示在優先順序堆疊中具有前景優先順序的專案已降級，因為其他人優先處理此查詢。
-   **ROWSETEVENT \_ 類型 \_ SCOPESTATISTICS** 事件提供您從 [**IRowsetPrioritization：： GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics)方法呼叫取得的相同資訊，但透過推播技師修理，如下所示：
    -   如果已使用優先順序 API 來要求非預設的優先順序層級，以及非零的統計資料事件頻率，就會發生此事件。
    -   只有當統計資料實際變更，而且 [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) 中所指定的間隔已過 (間隔無法保證事件) 的頻率時，才會發生此事件。
    -   此事件保證會引發「彈跳零」狀態 (剩餘的零個專案，零修改剩餘的) ，但前提是已引發非零的事件。
    -   如果佇列在統計資料事件頻率之前排在佇列中，則索引子可能會處理專案而不傳送此事件。

## <a name="additional-resources"></a>其他資源

請參閱下列與優先順序和資料列集相關的資源：

-   介面：
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   枚舉：
    -   [**設定 \_ 旗標的優先順序**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**優先權 \_ 層級**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**ROWSETEVENT \_ 類型**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 7 搜尋](./-search-3x-wds-overview.md)
</dt> <dt>

[Windows 7 搜尋的新](new-for-windows-7-search.md)
</dt> <dt>

[WindowsWindows 7 中的 Shell 程式庫](-search-win7-development-scenarios.md)
</dt> </dl>

 

 
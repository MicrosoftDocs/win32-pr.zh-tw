---
title: 查詢
description: 在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。 查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241948"
---
# <a name="queries"></a>查詢

在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。 查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。

-   [從 Direct3D 11 至 Direct3D 12 的查詢差異](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [查詢堆積](#query-heaps)
-   [建立查詢堆積](#creating-query-heaps)
-   [從查詢中解壓縮資料](#extracting-data-from-a-query)
-   [相關主題](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>從 Direct3D 11 至 Direct3D 12 的查詢差異

下列查詢類型不再存在於 Direct3D 12 中，其功能會併入其他進程：

-   **事件查詢** -事件功能現在由圍牆處理。
-   無 **交集的時間戳記查詢**-在 Direct3D 12 中，GPU 時鐘可以設定為穩定狀態 (請參閱) 的 [計時](timing.md)區段。 如果 GPU 在 (時間戳記之間的閒置（稱為脫離的查詢) ）之間的，GPU 時鐘比較沒有意義。 具有穩定的電源，從不同的命令清單發出的兩個時間戳記查詢可以可靠地進行比較。 相同命令清單中的兩個時間戳記一律可以可靠地進行比較。
-   **串流輸出統計資料查詢** -在 Direct3D 12 中，沒有單一資料流程輸出 (因此) 溢位查詢用於所有輸出資料流程。 應用程式需要發出多個單一資料流程查詢，然後將結果相互關聯。
-   **資料流程輸出統計資料述詞和遮蔽** 述詞查詢- (寫入記憶體) 和 [Predication](predication.md) 的查詢， (讀取記憶體) 不再結合，因此不需要這些查詢類型。

已將新的二進位遮蔽查詢類型新增至 Direct3D 12。 這可讓您只在意物件是否完全 pixels occluded 或不 (的 predication 策略，而不是 pixels occluded 的圖元數) 來指出此裝置的數量，這可能會更有效率地執行查詢。

## <a name="query-heaps"></a>查詢堆積

查詢可以是數種類型的其中一種 ([**D3D12 \_ 查詢 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) ，並在提交至 GPU 之前分組為查詢堆積。

您可以使用新的查詢類型 D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽，其行為就像 D3D12 \_ 查詢 \_ 類型 \_ 遮蔽，但它會傳回二進位0/1 結果：0表示沒有樣本通過深度和樣板測試，1表示至少有一個樣本通過深度和樣板測試。 這可讓遮蔽查詢不會干擾與深度/樣板測試相關聯的任何 GPU 效能優化。

## <a name="creating-query-heaps"></a>建立查詢堆積

與建立查詢堆積相關的 Api 是列舉 [**D3D12 \_ 查詢 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)、結構 [**D3D12 \_ 查詢 \_ 堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)和方法 [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)。

核心執行時間會驗證查詢堆積類型是否為 [**D3D12 \_ 堆積 \_ 型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 別列舉的有效成員，以及計數是否大於0。

查詢堆積內的每個個別查詢元素都可以個別啟動和停止。

使用查詢堆積的 Api 是列舉 [**D3D12 \_ 查詢 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)，以及 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)方法。

D3D12 \_ query \_ 類型 \_ TIMESTAMP 是唯一僅支援 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 的查詢。 所有其他查詢類型都需要 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 **EndQuery**。

Debug 層會驗證下列各項：

-   開始時間戳查詢是不合法的， &mdash; 您只能將它結束
-   不合法地開始查詢兩次，而不需要結束指定元素) 的 (。 對於需要 begin 和 end 的查詢，在指定專案) 的對應開始 (之前結束查詢是不合法的。
-   傳遞至 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 的查詢類型必須符合傳遞至 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)的查詢類型。

核心執行時間會驗證下列各項：

-   無法在時間戳記查詢上呼叫 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 。
-   針對支援 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 的查詢類型 (除了 timestamp) 以外的所有專案，指定元素的查詢不得跨越命令清單界限。
-   *ElementIndex* 必須在範圍內。
-   查詢類型是 [**D3D12 \_ 查詢 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) 列舉的有效成員。
-   查詢類型必須與查詢堆積相容。 下表顯示每個查詢類型所需的查詢堆積類型：

    

    | 查詢類型                                  | 查詢堆積類型                                |
    |---------------------------------------------|------------------------------------------------|
    | D3D12 \_ 查詢 \_ 類型 \_ 遮蔽               | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 遮蔽            |
    | D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽       | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 遮蔽            |
    | D3D12 \_ 查詢 \_ 類型 \_ 時間戳記               | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 時間戳記            |
    | D3D12 \_ 查詢 \_ 類型 \_ 管線 \_ 統計資料    | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 管線 \_ 統計資料 |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM0 | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料       |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM1 | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料       |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM2 | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料       |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM3 | D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料       |

    

     

-   命令清單類型支援此查詢類型。 下表顯示哪些命令清單類型支援的查詢。

    

    | 查詢類型                                  | 支援的命令清單類型         |
    |---------------------------------------------|--------------------------------------|
    | D3D12 \_ 查詢 \_ 類型 \_ 遮蔽               | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽       | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ 時間戳記               | 直接、計算和選擇性複製 |
    | D3D12 \_ 查詢 \_ 類型 \_ 管線 \_ 統計資料    | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM0 | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM1 | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM2 | 直接                               |
    | D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM3 | 直接                               |

    

     

## <a name="extracting-data-from-a-query"></a>從查詢中解壓縮資料

從查詢中取出資料的方法是使用 [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) 方法。 **ResolveQueryData** 適用于所有記憶體類型 (是否為系統記憶體或裝置本機記憶體) ，但需要目的地資源 [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)。 

## <a name="related-topics"></a>相關主題

* [計數器和查詢](counters-and-queries.md)
* [Predication 查詢逐步解說](predication-queries.md)

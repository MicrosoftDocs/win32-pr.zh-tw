---
description: 建立查詢並在其中加入計數器之後，請呼叫 PdhCollectQueryData 函數，以取得查詢中所有計數器的目前原始資料。
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: 收集效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319184"
---
# <a name="collecting-performance-data"></a>收集效能資料

[建立查詢](creating-a-query.md)並在其中加入計數器之後，請呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)函數，以取得查詢中所有計數器的目前原始資料。

許多計數器（例如速率計數器）都需要兩個數據樣本來計算格式化的資料值。 PDH 會維護目前範例和先前所收集範例的資料。 下列程式說明如何收集需要兩個樣本來計算可顯示值的計數器值。

**若要收集需要兩個樣本的計數器值來計算可顯示的值**

1.  呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) 以收集第一個範例。
2.  呼叫 [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) 函式，以在集合之間等待最少1秒。
3.  再次呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) ，以收集第二個範例。
4.  呼叫 [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) 函數來計算可顯示的值。
5.  重複步驟2到4。

您也可以呼叫 [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) 函式，以建立等待指定時間量的計時執行緒、收集範例，然後觸發應用程式定義的事件，這是您自行執行等候期間的替代方法。

如果您想要從記錄檔查詢效能資料，您也可以定義時間範圍。 時間範圍會將查詢限制在時間範圍內所收集的樣本 (每個範例都包含收集) 的時間戳記。 如需有關如何設定和取出時間範圍的詳細資訊，請參閱 [設定查詢的時間範圍](setting-a-time-range-for-a-query.md)。

如果您想要收集效能資料，並將它寫入記錄檔，您可以呼叫 [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) 函式，而不是呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)。 如需詳細資訊，請參閱 [使用記錄](working-with-log-files.md) 檔和將 [效能資料寫入至記錄](writing-performance-data-to-a-log-file.md)檔。

如需計算可顯示範例值的詳細資訊，請參閱 [顯示效能資料](displaying-performance-data.md)。

## <a name="understanding-multiple-processor-counters"></a>瞭解多個處理器計數器

某些效能計數器是針對單一處理器系統所設計，而且對於多處理器電腦而言可能不正確。 例如，進程受限於單處理器 100%;不過，它的執行緒可以使用數個處理器，並匯總超過100%。

[ \\ Processor (\_ Total) \\ % processor Time] 計數器值是所有處理器的平均使用量。 例如，如果您有兩個處理器，一個在100%，另一個為0% 時，此計數器將會報告50%。 所以範圍是從0到100。

" \\ Process (X) \\ % process Time" 計數器值是進程 X 之所有線程的處理器使用量總和。例如，在有兩個處理器的電腦中，如果處理常式有兩個執行緒，一個佔用75% 的 CPU，而另一個 CPU 的另一個 CPU 有80%，此計數器將會報告155%。 此計數器的範圍是從0到 100 \* ProcessorCount。

* * Windows Server 2003 和 Windows XP： * *

您可以接收 CPU 使用量的預期值範圍以外的值。 為了計算 CPU 使用量的百分比，PDH 需要兩個樣本 (各自有原始值和時間戳記) 。 因為 PDH 只使用實例名稱來比對進程，所以有時可能會使用來自不同進程的兩個範例。 例如，如果取樣三個進程，而第三個樣本之後有一個進程終止，另一個進程將移至該終止進程所清空的位置。 如此一來，格式化的計數器會在您格式化第四個樣本時提供不正確的值，因為它會使用來自終止進程的第三個範例，以及移至終止的進程位置之進程的第四個範例。

下表說明在收集資料時，進程終止時，會發生這種情況。 此表顯示三個進程 X 實例的五個計數器值範例。這些範例會以一秒的間隔收集。 在收集第三個樣本之後，會終止在插槽1中的進程 X。 當插槽1中的進程 X 終止時，插槽2中的進程 X 會移至插槽1。 當您在插槽2中收集進程 X 的第四個範例時，第一個值現在是20而不是1000，而第二個值是1500。 當您格式化計數器值時，會得到1480毫秒，而不是預期的500毫秒。 當您格式化第五個範例值時，應該會取得預期的值。

| 範例   | 進程 X 的插槽0 | 進程 X 的插槽1           | 進程 X 的插槽2                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| 範例 1 | 0                    | 0                              | 0                                        |
| 範例 2 | 20                   | 10                             | 500                                      |
| 範例 3 | 40                   | 20                             | 1,000                                    |
| 範例 4 | 60                   | 先前插槽2中的 1500 ()  | 不適用。 現在已在插槽1中收集。 |
| 範例5 | 80                   | 2,000                          | 不適用。 現在已在插槽1中收集。 |



 

 

 

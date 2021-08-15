---
description: 若要開啟記錄檔進行讀取，請呼叫 PdhOpenQuery 並指定記錄檔的路徑。
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: 使用記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82281694b72a2c28bb0e65ee4db16bd9ba33b8ed9c6e5e74dbf6c6cbf559507a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143741"
---
# <a name="working-with-log-files"></a>使用記錄檔

若要開啟記錄檔進行讀取，請呼叫 [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) 並指定記錄檔的路徑。 若要開啟記錄檔進行寫入，您必須呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。 若要關閉記錄檔，請根據您用來開啟記錄檔的功能，呼叫 [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) 或 [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) 。

## <a name="reading-from-a-log-file"></a>從記錄檔讀取

從記錄檔讀取效能資料與從即時來源讀取資料一樣：您可以開啟查詢、將計數器新增至查詢，以及呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) 從記錄檔收集範例。  \_ \_ \_ 當您到達記錄檔的結尾時，PdhCollectQueryData 會傳回 PDH 沒有任何資料。

記錄檔中的每個範例都包含最初收集和寫入記錄檔時的時間戳記。 若要取得記錄檔中第一個和最後一個範例的時間戳記，請呼叫 [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) 函式。 如果您想要限制從記錄檔讀取到特定時間範圍的範例，請參閱 [設定查詢的時間範圍](setting-a-time-range-for-a-query.md)。

如果您不知道記錄檔中有哪些效能物件和計數器，可以呼叫 [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) 來判斷物件清單。 指定物件時，您可以呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) 或 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) ，以抓取記錄檔中所包含的物件實例和計數器清單。

如果您呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)，請使用實例和計數器清單，為每個可能的實例和計數器組合建立路徑。 當您呼叫 [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 將計數器新增至查詢時，如果記錄檔不包含指定的組合，則函式會失敗。

如果您使用 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)，您可以建立包含實例名稱和計數器萬用字元的路徑，例如， \\ 物件 (\*) \\ \* 。 如果物件不包含實例，此函數會傳回 PDH \_ 無效 \_ 路徑。 在此情況下，請使用僅限計數器的萬用字元（例如物件）來呼叫 **PdhExpandWildCardPath** \\ \\ \* 。

較新的作業系統可以讀取舊版作業系統上產生的記錄檔;不過，在舊版作業系統上，無法讀取在 Windows Vista 和更新版本的作業系統上建立的記錄檔。

如需從記錄檔讀取資料的範例，請參閱 [從記錄檔讀取效能資料](reading-performance-data-from-a-log-file.md)。

## <a name="reading-from-multiple-log-files"></a>從多個記錄檔讀取

如果您需要建立從數個記錄檔讀取的查詢，請呼叫 [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) 將記錄檔系結在一起。 然後，您必須使用以 ' H ' 結尾的 PDH 函式，例如 [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)。

## <a name="writing-to-a-log-file"></a>寫入至記錄檔

寫入至記錄檔之前，請呼叫 [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) 來建立查詢，並指定效能資料的來源，也就是即時資料或記錄檔。 然後，新增您想要查詢的計數器。

若要開啟目的地檔案，請呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。 當您開啟記錄檔時，請指定查詢。 若要收集效能資料，並將其寫入記錄檔中，請呼叫 [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)。

如果將計數器資料寫入至以逗號分隔的 (.csv) 或 tab 分隔的 ( tsv) 記錄檔，而且路徑包含萬用字元實例，則路徑會展開，而且只有在展開路徑時存在的實例才會包含在記錄檔中。 但是，如果是 binary ( .blg) 或 SQL 記錄檔，則不會展開萬用字元，讓記錄檔包含在記錄期間建立的實例。

如需將資料寫入記錄檔的範例，請參閱將 [效能資料寫入至記錄](writing-performance-data-to-a-log-file.md)檔。

## <a name="compressing-a-log-file"></a>壓縮記錄檔

您可以使用 [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) 函數來壓縮記錄檔。 例如，從記錄檔讀取十筆記錄、呼叫 **PdhComputeCounterStatistics** 來計算平均值，然後將 mean 值寫入輸出記錄檔。

下列主題提供使用記錄檔的其他資訊。

-   [取得記錄檔的大小](getting-the-size-of-a-log-file.md)

 

 




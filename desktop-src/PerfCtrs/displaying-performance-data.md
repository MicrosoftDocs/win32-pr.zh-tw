---
description: 大部分的計數器都需要兩個範例值，才能計算可顯示的值。
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: 顯示效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d913474b794585dd557fae2b1fc232336b637d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977915"
---
# <a name="displaying-performance-data"></a>顯示效能資料

大部分的計數器都需要兩個範例值，才能計算可顯示的值。 每個計數器的公式會決定計數器是否需要兩個樣本。 如需計數器及其公式的清單，請參閱 [Windows Server 2003 部署套件](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))的「計數器類型」一節。

[收集效能資料](collecting-performance-data.md) 會顯示如何取出範例資料。 擁有範例之後，您通常會呼叫 [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) 來計算可顯示的值。

如果您需要向上或向下調整計數器值以顯示值，請在呼叫 [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)之前呼叫 [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)函數。 計數器值可以使用從-7 到7的10倍的乘冪來調整。

如果計數器路徑包含實例名稱的萬用字元，請呼叫 [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) ，以抓取每個所收集實例的格式化計數器值陣列。

您也可以使用 [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) 和 [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) 函數來計算可顯示的值。 若要使用這些函式，您必須在每個 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) 呼叫之後取得收集的範例，並自行儲存範例。 若要取得範例，請呼叫 [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) 或 [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) 函數。 針對以時間為基礎的計數器值，請在 **PdhFormatFromRawValue** 之前呼叫 [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) ，以取得計數器的時間基底。

如果您使用原始資料執行計算，請務必先檢查 [**PDH \_ 原始 \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)結構的 **CStatus** 成員，再使用範例。 如果 **CStatus** 的值不是 pdh \_ CStatus \_ 新 \_ 資料或 pdh \_ CStatus \_ 有效 \_ 的資料，此範例就無效。

## <a name="displaying-statistics-for-a-counter"></a>顯示計數器的統計資料

如果您想要計算計數器的最小值、最大值和平均值，請呼叫 [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) 函數。 當您收集範例時，請將 [**PDH \_ 原始 \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) 結構儲存在您傳遞至 **PdhComputeCounterStatistics** 的陣列中。 函數會傳回 [**PDH \_ 統計資料**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) 結構中的統計值。

您也可以使用此函數來壓縮記錄檔。 例如，從記錄檔讀取十筆記錄、呼叫 [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) 來計算平均值，然後將 mean 值寫入輸出記錄檔。

 

 

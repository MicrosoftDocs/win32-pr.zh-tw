---
description: 若要建立從即時來源或記錄檔收集效能資料的新查詢，請呼叫 PdhOpenQuery 函數。 函數會傳回您在後續的 PDH 函式呼叫中使用之查詢的控制碼。
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: 建立查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115565"
---
# <a name="creating-a-query"></a>建立查詢

若要建立從即時來源或記錄檔收集效能資料的新查詢，請呼叫 [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) 函數。 函數會傳回您在後續的 PDH 函式呼叫中使用之查詢的控制碼。

建立查詢之後，請針對您要加入至查詢的每個計數器呼叫 [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 函數。 您可以使用下列其中一種方法來提供完整的計數器路徑。

-   將計數器路徑定義為靜態字串。 如果您一律監視相同的計數器，而且您熟悉計數器路徑的正確語法，請使用這個方法。 如需用來指定計數器之正確語法的詳細資訊，請參閱 [指定計數器路徑](specifying-a-counter-path.md)。
-   使用電腦、物件、計數器和實例的名稱，初始化 [**PDH \_ 計數器 \_ 路徑 \_ 元素**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) 結構。 將此結構傳遞給 [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) ，這會傳回指定專案的計數器路徑。
-   指定包含萬用字元的計數器路徑，並呼叫 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) ，以取得符合路徑中萬用字元的計數器名稱清單。 掃描計數器名稱清單，然後將您要從此清單中的計數器加入至查詢。
-   呼叫 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) 函式來顯示對話方塊，讓使用者流覽及選取效能計數器。 如需詳細資訊，請參閱 [流覽計數器](browsing-counters.md)。

請注意，如果指定的計數器實例不存在， [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 就不會報告錯誤狀況。 相反地，它會傳回錯誤 \_ 成功。 這種行為的原因是，如果指定了不存在的計數器實例或存在但尚未建立的計數器實例，就不知道。

遺漏的計數器實例將會透過 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)、 [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)或 [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)報告。 只有針對某個計數器實例呼叫 **PdhCollectQueryData** ，而且計數器實例仍不存在時，會假設該計數器實例不存在，且此函式會傳回 PDH \_ 無 \_ 資料。 但是，如果查詢一個以上的計數器，  \_ 即使其中一個計數器實例尚未存在，PdhCollectQueryData 仍可能會傳回錯誤成功。 在此情況下，請針對每個感興趣的計數器實例呼叫 **PdhGetRawCounterValue** 或 **PdhGetFormattedCounterValue** 。 當呼叫 **PdhGetRawCounterValue** 時，如果實例不存在，此函式會傳回錯誤 \_ 成功，並將 [**PDH \_ 原始 \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **CStatus** 成員設定為 pdh \_ 狀態 \_ 無 \_ 實例。 當呼叫 **PdhGetFormattedCounterValue** 時，如果實例不存在，此函式會傳回 pdh \_ 無效 \_ 的資料，並將 [**pdh \_ bcp.fmt \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)的 **CStatus** 成員設定為 pdh \_ CStatus \_ NO \_ 實例。

請注意， [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 函式中指定的計數器路徑必須當地語系化。 [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)函式會提供地區設定中立的方式，將效能計數器加入至查詢。 此函數是將地區設定中立的計數器新增至查詢的建議方式。

若要從查詢中移除計數器，請呼叫 [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) 函數。

在您完成查詢的資料收集之後，請呼叫 [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) 函式來關閉查詢並釋放所有配置的系統資源。 **PdhCloseQuery** 會關閉與查詢相關聯的所有計數器控制碼。

 

 




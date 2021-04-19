---
description: 若要顯示對話方塊，以列出電腦上定義的效能物件和計數器，請呼叫 PdhBrowseCounters 函數。
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: 流覽計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969363"
---
# <a name="browsing-counters"></a>流覽計數器

若要顯示對話方塊，以列出電腦上定義的效能物件和計數器，請呼叫 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) 函數。 此對話方塊可讓使用者流覽和選取效能計數器。 您可以使用 [**PDH \_ 流覽 \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) 設定結構來指定對話方塊的設定。 例如，您可以將對話方塊設定為傳回一或多個選取專案。

在輸入時， **szReturnPathBuffer** 成員會包含在對話方塊中選取的預設效能物件和計數器。 在輸出時，緩衝區會包含使用者選取的效能物件和計數器。 您也可以使用 **pCallBack** 成員來指定回呼函式，以處理對話方塊所傳回的計數器名稱。

請注意， \_ \_ 如果 **bSingleCounterPerDialog** 為 **FALSE** ，且使用者按一下 [關閉] 按鈕，則此對話方塊可能會傳回 PDH 對話方塊，所以您的錯誤處理必須考慮這一點。

如需使用 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) 函數的範例，請參閱 [流覽效能計數器](browsing-performance-counters.md)。

若要取得電腦上的效能物件清單，您也可以呼叫 [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) 函數。 若要取得效能物件的計數器和實例清單，請呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) 函數。 您也可以使用這些函數來識別記錄檔中所包含的效能物件和計數器。 對 **PdhEnumObjectItems** 的重複呼叫會傳回相同的計數器和實例清單，直到您先呼叫 **PdhEnumObjects** 重新整理效能物件清單為止。 如需列舉物件和計數器的範例，請參閱 [列舉處理常式物件](enumerating-process-objects.md)。

## <a name="selecting-the-data-source"></a>選取資料來源

您可以搭配使用 [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) 與 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) ，以提示使用者選取資料來源是即時或從記錄檔，而且如果是記錄檔，則為其名稱。 如果您不想要顯示 [資料來源] 對話方塊，您可以呼叫 **PdhSelectDataSource** 來只顯示檔案瀏覽器類別目錄。 若要這樣做，請將 PDH \_ 旗標檔案 \_ \_ 瀏覽器指定 \_ 為 **PdhSelectDataSource** 呼叫的第二個參數。

 

 




---
description: 每個事件記錄檔都包含一個標頭 (，其 \_ \_ 具有固定大小的 ELF LOGFILE 標頭結構) ，後面接著 EVENTLOGRECORD 結構) 所代表 (的事件記錄數目，以及 ELF \_ EOF 記錄結構 (所代表的檔案結尾記錄) \_ 。
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: 事件記錄檔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ed6df35ac1fcd641a9a895b2c32eb34d6a4c1cb472ab03f16417f55900c767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814288"
---
# <a name="event-log-file-format"></a>事件記錄檔格式

每個事件記錄檔都包含一個標頭 (，其具有固定大小的 [**ELF \_ LOGFILE \_ 標頭**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) 結構) ，後面接著 [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) 結構) 所代表 (的事件記錄數目，以及 [**ELF \_ EOF \_ 記錄**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) 結構 (所代表的檔案結尾記錄) 。

建立事件記錄檔時，會在事件記錄檔中寫入 ELF 記錄檔 **\_ \_ 標頭** 結構和 **ELF \_ EOF \_ 記錄** 結構，並在每次事件寫入記錄檔時更新。

當應用程式呼叫 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) 函式以將專案寫入事件記錄檔時，系統會將參數傳遞給事件記錄服務。 事件記錄服務會使用此資訊將 **EVENTLOGRECORD** 結構寫入事件記錄檔。 下圖說明此程序。

![寫入記錄檔](images/evreport.png)

事件記錄會以下列其中一種方式組織：

-   未換行。 在事件記錄檔標頭之後，最舊的記錄會緊接在 **ELF \_ EOF \_ 記錄**) 之前新增 (的最後一筆記錄之後新增記錄。 下列範例顯示非包裝方法：

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    當建立事件記錄檔或清除事件記錄檔時，可能會發生非換行。 事件記錄檔會繼續保持未換行，直到達到事件記錄檔大小限制為止。 事件記錄檔大小受限於 **MaxSize** 設定值或系統資源數量。

    當達到事件記錄檔大小限制時，可能會開始換行。 換行是由 **保留** 設定值所控制。 如需事件記錄檔設定值的詳細資訊，請參閱 [Eventlog 索引鍵](eventlog-key.md)。

-   包裝。 記錄會組織成圓形緩衝區。 新增記錄時，會取代最舊的記錄。 最舊和最新記錄的位置將會有所不同。 下列範例顯示包裝方法。

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    在此範例中，最舊的記錄已不再為1，但為102，因為已覆寫記錄1到101的空間。

    **ELF \_ EOF \_ 記錄** 和最舊的記錄之間有一些空間，因為系統會清除整數筆記錄，以釋放最新記錄的空間。 例如，如果最新記錄的長度為100個位元組，而兩個最舊的記錄是75位元組長，則系統會移除兩個最舊的記錄。 寫入新記錄時，稍後將會使用額外的50個位元組。

    事件記錄檔具有固定的大小，而且當檔案中的記錄自動換行時，檔案結尾的記錄通常會分割成兩筆記錄。 例如，如果下一次寫入的位置是從檔案結尾算起的100個位元組，且記錄的大小為300個位元組，則會在檔案結尾寫入前100個位元組，而下一個200位元組將會寫入檔案開頭的 **ELF \_ LOGFILE \_ 標頭** 之後。 如果位於檔案結尾的可用空間小於 **EVENTLOGRECORD** (0x38 bytes) 的固定部分，則所有新記錄都會寫入至檔案開頭的 **ELF \_ LOGFILE \_ 標頭** 之後。 檔案結尾未使用的位元組將會填入模式0x00000027。

如需詳細資訊和程式碼範例，請參閱 [報告事件](reporting-an-event.md)。

 

 

---
description: OpenEventLog、OpenBackupEventLog、RegisterEventSource、DeregisterEventSource 和 CloseEventLog 函數會開啟和關閉事件記錄控制碼。
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: 事件記錄作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974406"
---
# <a name="event-logging-operations"></a>事件記錄作業

[**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)、 [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)、 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)、 [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)和 [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)函數會開啟和關閉事件記錄控制碼。

下表顯示可在開啟的事件記錄檔上執行的作業，以及每項作業的對應函式。



| 作業 | 函式                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| 備份    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| 清除     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| 監視器   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| 查詢     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)、 [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| 讀取      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| 寫入     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

[**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)和 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)函式會採用選擇性的伺服器名稱做為參數，因此可以在遠端伺服器上執行作業。 使用 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 來讀取或執行管理作業 (備份、清除、監視和查詢記錄檔) ，以及使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 來寫入記錄檔。

事件記錄函式的每個呼叫都是不可部分完成的作業。 當您從事件記錄檔讀取時，只會傳回整個事件記錄。 當您寫入事件記錄檔時，每個事件記錄都會以順序寫入記錄檔中的完整記錄。 下列清單描述事件記錄服務如何處理特殊條件：

-   事件記錄服務會同時接收讀取作業和寫入作業：如果讀取位置是在檔案結尾，讀取作業會失敗並出現「檔案結尾」狀態 (如果寫入作業未完成) ，則會傳回新的記錄 (如果寫入作業已完成) 則會傳回新的記錄。
-   事件記錄服務會在接收讀取作業之前完成清除作業：讀取作業失敗，並出現「檔案結尾」狀態。
-   事件記錄服務會在接收寫入作業之前完成明確的作業：清除作業會截斷記錄，然後寫入作業會在記錄檔的開頭加入新的記錄。

 

 




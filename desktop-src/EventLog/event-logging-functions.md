---
description: 下列函式可用於事件記錄。
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: 事件記錄功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069588"
---
# <a name="event-logging-functions"></a>事件記錄功能

下列函式可用於事件記錄。



| 函式                                                         | 描述                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | 將指定的事件記錄檔儲存至備份檔案。                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | 清除指定的事件記錄檔，並選擇性地將記錄檔的目前副本儲存至備份檔案。  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | 關閉指定之事件記錄檔的讀取控制碼。                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | 關閉指定之事件記錄檔的寫入控制碼。                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | 抓取指定之事件記錄檔的相關資訊。                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | 捕獲指定事件記錄檔中的記錄數目。                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | 抓取指定之事件記錄檔中最舊記錄的絕對記錄號碼。               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | 讓應用程式在事件寫入至指定的事件記錄檔時接收通知。 |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | 開啟備份事件記錄檔的控制碼。                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | 開啟指定之事件記錄檔的控制碼。                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | 從指定的事件記錄檔讀取大量的專案。                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | 抓取指定之事件記錄檔的已註冊控制碼。                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | 在指定事件記錄檔的結尾寫入專案。                                              |



 

 

 




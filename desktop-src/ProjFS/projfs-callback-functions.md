---
title: ProjFS 回呼函式
description: 下列回呼函數是在 projectedfslib 中宣告。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 595fac418ce57e1e6caff718d75b458390efd31c2e8727cd2feb8ee5a5d86eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031158"
---
# <a name="callback-functions"></a>回呼函數

下列回呼函數是在 projectedfslib 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | 通知提供者，先前調用回呼的作業應該取消。 |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | 通知提供者目錄列舉已結束。 |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | 從提供者要求目錄列舉資訊。
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | 要求檔案主要資料流程的內容。
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | 從提供者要求檔案或目錄的資訊。
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | 將檔案系統作業的通知傳送給提供者。
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | 判斷指定的檔案路徑是否存在於提供者的備份存放區中。
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | 通知提供者目錄列舉正在啟動。
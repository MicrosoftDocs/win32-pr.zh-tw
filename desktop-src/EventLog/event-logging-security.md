---
description: 安全性記錄檔是設計來供系統使用。 不過，如果使用者已被授與「SE \_ 安全性 \_ 名稱」許可權 (&\# 0034; 管理審核和安全性記錄&\# 0034; 使用者權限) ，則使用者可以讀取和清除安全性記錄。 如需詳細資訊，請參閱許可權。
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: 事件記錄安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4e2dce7318efeb6f26917bca1d6812eb32a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983585"
---
# <a name="event-logging-security"></a>事件記錄安全性

**安全** 日誌是設計來供系統使用。 不過，如果使用者已被授與 「SE \_ 安全性 \_ 名稱」許可權 (「管理審核和安全性記錄」使用者權限) ，則使用者可以讀取和清除安全性記錄。 如需詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges)。

只有本地安全機構 (Lsass.exe) 有 **安全** 日誌的寫入權限。 沒有其他帳戶可以要求此許可權。 若要將事件寫入 **安全** 日誌，請使用 [**AuthzReportSecurityEvent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) 函數。

**應用程式** 記錄檔、**系統** 記錄和自訂記錄檔的存取會受到限制。 系統會根據授與執行執行緒之帳戶的存取權，來授與存取權。 下表顯示事件記錄功能所需的存取類型。



| 存取權限                 | Description                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| ELF \_ LOGFILE \_ CLEAR (0x0004)  | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)所需。                                                    |
| ELF \_ LOGFILE \_ READ (0x0001)   | [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)和 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)所需。 |
| ELF \_ \_ 記錄檔寫入 (0x0002)  | [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)所需。                                        |



 

使用 **CustomSD** 登錄值來設定 **應用程式** 記錄檔、 **系統** 記錄檔和自訂記錄檔的安全性。 如需詳細資訊，請參閱 [Eventlog 索引鍵](eventlog-key.md)。

**WINDOWS XP/2000：** 下表說明針對每個記錄檔的每個帳戶授與的存取權限。

| 記錄             | 帳戶                 | 讀取 | 寫入 | 清除 |
|-----------------|-------------------------|------|-------|-------|
| **應用程式** | 系統管理員 (系統)  | X    | X     | X     |
|                 | 系統管理員 (網域)  | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | 互動式使用者        | X    | X     |       |
| **系統**      | 系統管理員 (系統)  | X    | X     | X     |
|                 | 系統管理員 (網域)  | X    |       | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | 互動式使用者        | X    |       |       |
| *Custom*        | 系統管理員 (系統)  | X    | X     | X     |
|                 | 系統管理員 (網域)  | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | 互動式使用者        | X    | X     |       |



 

若要授與 Guest 帳戶成員的存取權，請變更下列登錄值：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **EventLog** \\ *記錄* 檔 \\ **RestrictGuestAccess**

 

 

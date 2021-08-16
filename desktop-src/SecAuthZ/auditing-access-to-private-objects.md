---
description: 受保護的伺服器可以使用下列功能，在安全性事件記錄檔中產生審核報告。
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: 審核私用物件的存取權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac3a38a9f0af292a77a539491e0cea5f1faf40b570f34a35371ad43a7abe757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784589"
---
# <a name="auditing-access-to-private-objects"></a>審核私用物件的存取權

受保護的伺服器可以使用下列功能，在安全性事件記錄檔中產生審核報告。



| 函式                                                                                                     | 描述                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | 與 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) 函式相同，不同之處在于它可以產生失敗或成功存取嘗試的審核訊息。                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | 與 [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) 函式相同，不同之處在于它可以產生失敗或成功存取嘗試的審核訊息。                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | 與 [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式相同，不同之處在于它可以產生失敗或成功存取嘗試的審核訊息。                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | 與 [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) 函式相同，不同之處在于它可讓呼叫執行緒在模擬用戶端之前執行存取檢查。 |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | 產生審核訊息，指出用戶端嘗試關閉私用物件。                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | 產生審核訊息，指出用戶端嘗試刪除私用物件。                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | 產生審核訊息，指出用戶端嘗試開啟或建立私用物件。                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | 產生審核訊息，指出用戶端嘗試使用一組指定的許可權，以及嘗試存取私用物件。                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | 產生審核訊息，指出用戶端嘗試使用一組指定的許可權。                                                                                                                        |



 

 

 

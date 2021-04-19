---
description: 說明在存取控制中使用模擬權杖的方式。
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: 模擬權杖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000313"
---
# <a name="impersonation-tokens"></a>模擬權杖

模擬執行緒有兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)：

-   描述伺服器 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly)。 若要取得此權杖的控制碼，請呼叫 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 函數。
-   模擬存取權杖，描述正在模擬之用戶端的安全性內容。 若要取得此權杖的控制碼，請呼叫 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函數。

伺服器可以使用下列功能中的模擬 [*權杖*](/windows/desktop/SecGloss/i-gly) ：

-   在 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)、 [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)和 [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式中，判斷 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 是否允許用戶端有一組存取權限。
-   在 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數中，啟用或停用用戶端的許可權。
-   在 [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) 函式中，判斷是否已在用戶端的權杖中啟用一組許可權。
-   在安全性事件記錄檔中產生專案的函式，例如 [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) 或 [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)。 這些函式會使用模擬權杖來取得記錄專案之用戶端的相關資訊。

 

 

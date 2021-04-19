---
description: 安全性 \_ \_ 模擬層級列舉會定義四個模擬等級，以決定伺服器可在用戶端內容中執行的作業。
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: " (授權) 的模擬層級"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91654f42a86e5c47069197bed084df56f5445dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984680"
---
# <a name="impersonation-levels-authorization"></a> (授權) 的模擬層級

[**安全性模擬 \_ \_ 層級**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level)列舉會定義四個模擬等級，以決定伺服器可在用戶端內容中執行的作業。



| 模擬等級    | Description                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | 伺服器無法模擬或識別用戶端。                                            |
| SecurityIdentification | 伺服器可以取得用戶端的身分識別和許可權，但無法模擬用戶端。 |
| SecurityImpersonation  | 伺服器可以在本機系統上模擬用戶端的安全性內容。                    |
| SecurityDelegation     | 伺服器可以在遠端系統上模擬用戶端的安全性內容。                      |



 

具名管道、RPC 或 DDE 連接的用戶端可以控制模擬層級。 例如，具名管道用戶端可以呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數來開啟具名管道的控制碼，並指定伺服器的模擬等級。

當具名管道、RPC 或 DDE 連接是遠端時，會忽略傳遞至 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 以設定模擬等級的旗標。 在此情況下，用戶端的模擬層級取決於伺服器啟用的模擬等級，這是由目錄服務中伺服器帳戶上的旗標所設定。 例如，如果伺服器已啟用委派，即使傳遞給 **CreateFile** 的旗標指定了識別模擬等級，用戶端的模擬等級也會設定為委派。

DDE 用戶端會使用 [**DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) 函數搭配 [**\_ \_ \_ 服務結構的安全性品質**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) 來指定模擬等級。 SecurityImpersonation 層級是具名管道、RPC 和 DDE 伺服器的預設值。 [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself)、 [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)和 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)函數可讓呼叫者指定模擬層級。 使用 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 函式來取得 [*存取權杖*](/windows/desktop/SecGloss/a-gly)的模擬層級。

在 SecurityImpersonation 層級，大部分執行緒的動作都會發生線上程模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)的安全性內容中，而不是在擁有線程之 [*進程*](/windows/desktop/SecGloss/p-gly)的 [*主要權杖*](/windows/desktop/SecGloss/p-gly)中。 例如，如果模擬執行緒開啟 [安全物件](securable-objects.md)，系統就會使用模擬權杖來檢查執行緒的存取。 同樣地，如果模擬執行緒建立新的物件，例如藉由呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式，新物件的擁有者就是用戶端 [*存取權杖*](/windows/desktop/SecGloss/a-gly)的預設擁有者。

不過，在下列情況下，系統會使用進程的主要權杖，而不是呼叫執行緒的模擬權杖：

-   如果模擬執行緒呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數，則新的進程一律會繼承進程的主要 token。
-   對於需要 SE TCB 名稱許可權的函式（ \_ \_ 例如 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) 函數），系統一律會檢查進程主要權杖中的許可權。
-   對於需要 SE AUDIT NAME 許可權的函式（ \_ \_ 例如 [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) 函式），系統一律會檢查進程主要權杖中的許可權。
-   在 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函式的呼叫中，執行緒可以指定函式是否使用模擬權杖或主要權杖來判斷是否要授與要求的存取權。

 

 

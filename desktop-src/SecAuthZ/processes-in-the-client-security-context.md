---
description: 伺服器應用程式可以呼叫 CreateProcessAsUser 函數，以建立在用戶端安全性內容中執行的新進程。
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: 用戶端安全性內容中的進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974136"
---
# <a name="processes-in-the-client-security-context"></a>用戶端安全性內容中的進程

伺服器應用程式可以呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函數，以建立在用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中執行的新進程。 使用用戶端的 [*存取權杖*](/windows/desktop/SecGloss/a-gly)來呼叫時， **CreateProcessAsUser** 需要 SE \_ ASSIGNPRIMARYTOKEN \_ 名稱和 se \_ 提高 \_ 配額 \_ 名稱許可權，這些許可權是由在 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)中執行的 Windows 服務所持有。

[**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)函式也需要 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly)。 伺服器可以藉由啟動用戶端的 [登入會話](client-logon-sessions.md) ，或模擬 [用戶端](client-impersonation.md) 並複製模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)，取得用戶端的主要存取權杖。

下列程式描述建立用戶端進程的兩種方式。

**登入用戶端以建立用戶端進程**

1.  在對 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera)的呼叫中使用用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly)，將用戶端記錄到本機電腦上。 **LogonUser** 會為用戶端的 [*登入會話*](/windows/desktop/SecGloss/l-gly)產生主要權杖。
2.  如果伺服器需要使用用戶端的安全性內容，請在 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)函式的呼叫中使用主要權杖，以存取用戶端 [*進程*](/windows/desktop/SecGloss/p-gly)的可執行檔。
3.  在 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)的呼叫中使用主要權杖，在用戶端的安全性內容中建立進程。

> [!Note]  
> 使用下列技術建立的進程可能無法存取網路資源，除非它有用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly)。

 

**藉由模擬用戶端建立用戶端進程**

1.  使用模擬函數（例如 [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)）開始模擬。
2.  呼叫 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函數，取得具有用戶端安全性內容的模擬權杖。
3.  呼叫 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) 函式，將模擬權杖轉換為主要權杖。
4.  在 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式的呼叫中使用主要權杖，以在用戶端的安全性內容中建立處理常式。

根據預設， [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 會在非互動式視窗工作站和桌上型電腦上建立用戶端 [*進程*](/windows/desktop/SecGloss/p-gly) 。 若要建立互動式程式，伺服器必須先設定互動式視窗工作站和桌上型電腦 (Dacl) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) ，以確保允許用戶端存取它們。 若要這麼做，最好的方式是將用戶端登入， [取得用戶端登入會話的安全識別碼 (SID) ](/previous-versions//aa446670(v=vs.85))，然後在互動式視窗工作站和桌上型電腦的存取允許 ace 中使用該 SID。 伺服器接著可以呼叫 **CreateProcessAsUser**，指定互動式視窗工作站和桌面 winsta0 \\ 預設值。 如需顯示此程式的範例，請參閱 [在 c + + 中啟動互動式用戶端程式](/previous-versions//aa379608(v=vs.85))。

 

 

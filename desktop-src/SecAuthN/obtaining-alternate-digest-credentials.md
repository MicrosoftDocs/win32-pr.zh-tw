---
description: 若要取得與目前登入會話相關聯的認證，請將 \_ 替代安全性主體的資訊填入 SEC 的 WINNT \_ AUTH 身分 \_ 識別結構中。
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: 取得替代的摘要認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194061"
---
# <a name="obtaining-alternate-digest-credentials"></a>取得替代的摘要認證

若要取得與目前登入 [*會話*](../secgloss/s-gly.md)相關聯的 [*認證*](../secgloss/c-gly.md)，請將替代 [*安全性主體*](../secgloss/s-gly.md)的資訊填入 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)結構中。 使用 *pAuthData* 參數將結構傳遞至 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數。

下表說明 [**SEC \_ 驗證身分 \_ \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構的成員。



| member             | 描述                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **使用者**           | 以 Null 終止的字串，包含其認證將用來建立安全性內容的安全性主體名稱。 |
| **UserLength**     | **使用者** 成員的長度（以字元為單位）。 省略終止的 null。                                                         |
| **網域**         | 以 Null 終止的字串，識別包含安全性主體帳戶的網域。                                  |
| **DomainLength**   | **網域** 成員的長度（以字元為單位）。 省略終止的 null。                                                       |
| **密碼**       | 以 Null 終止的字串，其中包含安全性主體的密碼。                                                            |
| **密碼長度** | **密碼** 成員的長度（以字元為單位）。 省略終止的 null。                                                     |
| **旗標**          | 指出字串成員是否為 ANSI 或 [*Unicode*](../secgloss/u-gly.md) 格式。  |



 

下表列出結構 **旗標** 成員的有效值。



| 常數                            | 描述                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEC 的 \_ WINNT \_ 驗證身分 \_ 識別 \_ ANSI    | 此結構中的字串為 ANSI 格式。                                                                    |
| SEC 的 \_ WINNT \_ 驗證身分 \_ 識別 \_ UNICODE | 此結構中的字串採用 [*Unicode*](../secgloss/u-gly.md) 格式。 |



 

結構和常數是在使用平臺軟體發展工具組 (SDK) 所散發的 Rpcdce .h 標頭檔中宣告的。

下列範例示範用戶端呼叫，以取得特定使用者帳戶的摘要認證。


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



**\_ Tcslen** 函式會傳回字串長度（以字元為單位），不包含終止的 null 字元。

如果您的應用程式可以使用在登入時建立的認證，請參閱 [取得預設摘要認證](obtaining-default-digest-credentials.md)。

 

 

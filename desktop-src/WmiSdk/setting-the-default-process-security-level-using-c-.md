---
description: 當用戶端應用程式第一次登入 Windows Management Instrumentation (WMI) 時，必須使用 CoInitializeSecurity 的呼叫來設定預設的進程安全性層級。
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: 使用 c + + 設定預設進程安全性層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514084"
---
# <a name="setting-the-default-process-security-level-using-c"></a>使用 c + + 設定預設進程安全性層級

當用戶端應用程式第一次登入 Windows Management Instrumentation (WMI) 時，必須使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫來設定預設的進程安全性層級。 COM 會使用呼叫中的資訊，來判斷另一個進程存取用戶端應用程式處理常式時必須擁有多少安全性。

本主題將討論下列各節：

-   [使用 c + + 變更預設驗證認證](#changing-the-default-authentication-credentials-using-c)
-   [使用 c + + 變更預設模擬層級](#changing-the-default-impersonation-levels-using-c)

針對大部分的用戶端應用程式，下列範例中所示的引數會設定 WMI 的預設安全性。


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



將驗證層級設定為 [ **RPC \_ C \_ 驗證 \_ 等級] \_ 預設值** ，可讓 DCOM 協商驗證層級，以符合目的電腦的安全性需求。 如需詳細資訊，請參閱 [使用 c + + 變更預設驗證認證](#changing-the-default-authentication-credentials-using-c) ，以及 [使用 c + + 變更預設的模擬設定](#changing-the-default-impersonation-levels-using-c)。

## <a name="changing-the-default-authentication-credentials-using-c"></a>使用 c + + 變更預設驗證認證

預設驗證認證適用于大部分的情況，但您可能需要在不同的情況下使用不同的驗證認證。 例如，您可能會想要將加密新增至驗證程式。

下表列出並描述不同層級的驗證。



| 驗證層級                 | Description                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| RPC \_ C \_ 驗證 \_ 層級 \_ 預設值        | 預設安全性驗證。                                                      |
| RPC \_ C \_ 驗證 \_ 層級 \_ 無           | 不需要驗證。                                                                    |
| RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT        | 只有當用戶端與伺服器建立關聯性時，才會進行驗證。           |
| RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫           | 每次伺服器接收 RPC 時的驗證。                                  |
| RPC \_ C \_ 驗證 \_ 層級 \_ PKT            | 每次伺服器從用戶端接收資料時進行驗證。                      |
| RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性 | 驗證未修改封包中的資料。                        |
| RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權   | 包含所有先前的驗證層級，並加密每個 RPC 呼叫的值。 |



 

您可以在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的 *pAuthList* 參數中使用 **唯一的 \_ 驗證 \_ 清單** 結構，以指定多個使用者的預設驗證認證。

下列程式碼範例顯示如何變更驗證認證。


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a>使用 c + + 變更預設模擬層級

COM 提供從系統登錄讀取的預設安全性層級。 不過，除非特別修改，否則登錄設定會將模擬等級設定為太低，讓 WMI 無法運作。 一般而言，預設模擬層級是 **rpc \_ c \_ IMP \_ 層級 \_ 識別**，但是 WMI 至少需要 **rpc \_ c \_ IMP \_ 層級 \_** 模擬才能與大部分的提供者搭配運作，而且您可能會遇到需要設定較高層級模擬的情況。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。 下表列出不同的模擬層級。



| 層級                           | 描述                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| RPC \_ C \_ IMP \_ 層級 \_ 預設值     | 作業系統會選擇模擬的層級。                                                      |
| RPC \_ C \_ IMP \_ 層級 \_ 匿名   | 伺服器可以模擬用戶端，但模擬權杖無法用於任何作業。               |
| RPC \_ C \_ IMP \_ 層級 \_ 識別    | 伺服器可以取得用戶端的身分識別，並模擬用戶端以進行 ACL 檢查。                 |
| RPC \_ C \_ IMP \_ 層級模擬 \_ | 伺服器可以跨一個電腦界限來模擬用戶端。                                           |
| RPC \_ C \_ IMP \_ 層級 \_ 委派    | 伺服器可以跨多個界限模擬用戶端，並可代表用戶端進行呼叫。 |



 

 

 

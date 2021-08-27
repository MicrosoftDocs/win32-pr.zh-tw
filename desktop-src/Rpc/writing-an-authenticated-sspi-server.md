---
title: 撰寫經過驗證的 SSPI 伺服器
description: 在用戶端和伺服器程式之間可以進行驗證通訊之前，伺服器必須註冊其驗證資訊。
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- 遠端程序呼叫 RPC、工作、撰寫經過驗證的 SSPI 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462f153905d6b654a0533c7bd05bff0e9627869d6910fb1fea05fe9340b788a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010346"
---
# <a name="writing-an-authenticated-sspi-server"></a>撰寫經過驗證的 SSPI 伺服器

在用戶端和伺服器程式之間可以進行驗證通訊之前，伺服器必須註冊其驗證資訊。 尤其是，伺服器必須註冊其主體名稱，並指定它所使用的驗證服務。 如需主體名稱的詳細資訊，請參閱 [主體名稱](principal-names.md)。 如需驗證服務的詳細資訊，請參閱 [驗證服務](authentication-services.md)。

為了註冊其驗證資訊，伺服器會呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函數。 將主體名稱的指標傳遞為第一個參數的值。 將第二個參數設定為常數，表示應用程式將使用的驗證服務。 如需驗證服務的描述，請參閱 [驗證-服務常數](authentication-service-constants.md)。

伺服器也可以將金鑰取得函式的位址傳遞為第三個參數的值。 請參閱 [金鑰](key-acquisition-functions.md)取得函式。 若要針對選取的驗證服務使用預設的金鑰取得函數，請將第三個參數設定為 **Null**。 如果您提供金鑰取得函式， [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式的最後一個參數是要傳遞至金鑰取得函式的指標資料。 **RpcServerRegisterAuthInfo** 的呼叫會顯示在下列程式碼片段中。


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



此外，伺服器可能會提供具有授權功能的 RPC 執行時間程式庫。 若要設定授權函數，請呼叫 [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) 函數。

分散式應用程式的伺服器部分可以呼叫函數 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 或 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) 來查詢驗證資訊的系結控制碼。

如果您的伺服器向安全性支援提供者註冊，將不會分派具有無效認證的用戶端呼叫。 但是，不會分派沒有認證的呼叫。 有三種方式可以防止這種情況發生：

-   使用 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)（具有安全性回呼函式）註冊介面;這會讓 RPC 執行時間程式庫自動拒絕對該介面的未經驗證呼叫。 註冊回呼函數與其他檢查存取認證的方法相容;回呼函式本身可以呼叫 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient)、 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)或 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數或其他函式。 不過，這些函式無法使用傳遞至函式的引數，因為它們不會在該時間點 unmarshalled。

> [!IMPORTANT]
> 使用具有安全性回呼函式的 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 來註冊介面，是檢查用戶端認證的最大建議方法。

 

-   呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 來判斷用戶端所使用的安全性層級。 如果用戶端未經驗證，則您的存根會傳回錯誤。

 

 





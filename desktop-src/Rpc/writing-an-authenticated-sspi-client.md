---
title: 撰寫經過驗證的 SSPI 用戶端
description: 將已驗證的 SSPI 用戶端和遠端程序呼叫寫入 (RPC) 。
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- 遠端程序呼叫 RPC、工作、撰寫已驗證的 SSPI 用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445d5340b03f07805a9e2ab89deb8c915a76160db67b504259ae8de0bbabee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010356"
---
# <a name="writing-an-authenticated-sspi-client"></a>撰寫經過驗證的 SSPI 用戶端

所有 RPC 用戶端/伺服器會話都需要用戶端與伺服器之間的系結。 若要將安全性新增至用戶端/伺服器應用程式，程式必須使用已驗證的系結。 本節說明在用戶端與伺服器之間建立已驗證系結的程式。

-   [建立用戶端系結控制碼](#creating-client-side-binding-handles)
-   [提供用戶端認證給伺服器](#providing-client-credentials-to-the-server)

如需相關資訊，請參閱平臺軟體發展工具組中 [與大部分安全性套件和通訊協定搭配使用的程式](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) (SDK) 。

## <a name="creating-client-side-binding-handles"></a>建立用戶端系結控制碼

若要使用伺服器程式建立已驗證的會話，用戶端應用程式必須使用其系結控制碼提供驗證資訊。 若要設定已驗證的系結控制碼，用戶端會叫用 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函數。 這兩個函數幾乎完全相同。 兩者之間唯一的差異在於，用戶端可以使用 **RpcBindingSetAuthInfoEx** 函式來指定服務品質。

下列程式碼片段顯示 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 呼叫的方式。


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



在用戶端成功呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函式之後，rpc 執行時間程式庫會自動驗證系結上的所有 RPC 呼叫。 用戶端選取的安全性和驗證層級僅適用于該系結控制碼。 衍生自系結控制碼的內容控制碼將使用相同的安全性資訊，但是對系結控制碼的後續修改不會反映在內容控制碼中。 如需詳細資訊，請參閱 [內容控制碼](context-handles.md)。

在用戶端選擇另一個層級，或直到進程終止之前，驗證等級會保持有效。 大部分的應用程式都不需要變更安全性層級。 用戶端可以藉由叫用 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 並傳遞系結控制碼來查詢任何系結控制碼，以取得其授權資訊。

## <a name="providing-client-credentials-to-the-server"></a>提供用戶端認證給伺服器

伺服器會使用用戶端的系結資訊來強制執行安全性。 用戶端一律會傳遞系結控制碼做為遠端程序呼叫的第一個參數。 不過，伺服器無法使用控制碼，除非它被宣告為 IDL 檔案或伺服器應用程式佈建檔中遠端程式的第一個參數， (ACF) 。 您可以選擇在 IDL 檔案中列出系結控制碼，但這會強制所有用戶端宣告和操作系結控制碼，而不是使用自動或隱含系結。 如需詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。

另一種方法是讓系結控制碼離開 IDL 檔案，並將 **明確的 \_ 控制碼** 屬性放入伺服器的 ACF 中。 如此一來，用戶端就可以使用最適合應用程式的系結類型，而伺服器則使用系結控制碼，就好像是明確宣告一樣。

從系結控制碼解壓縮用戶端認證的程式會如下所示：

-   RPC 用戶端會呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ，並在傳遞至伺服器的系結資訊中包含其驗證資訊。
-   通常，伺服器會呼叫 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) ，以便如同用戶端一樣運作。 如果系結控制碼未經過驗證，則呼叫會失敗，而且 RPC \_ S \_ 沒有 \_ 內容 \_ 可用。 若要取得用戶端的使用者名稱、在模擬時呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ，或在 Windows XP 或更新版本的 Windows 上呼叫 RpcGetAuthorizationCoNtextForClient，請呼叫 [](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)以取得授權內容，然後使用 Authz 函式來取得名稱。
-   伺服器通常會呼叫 [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) 來建立具有 acl 的物件。 完成這項作業之後，稍後的安全性檢查就會變成自動。

 

 
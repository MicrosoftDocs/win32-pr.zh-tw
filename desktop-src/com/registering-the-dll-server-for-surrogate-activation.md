---
title: 註冊 DLL 伺服器以進行代理程式啟用
description: 註冊 DLL 伺服器以進行代理程式啟用
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683149"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>註冊 DLL 伺服器以進行代理程式啟用

在下列情況下，將會在代理程式中載入 DLL 伺服器：

-   登錄中的 CLSID 機碼底下必須指定 AppID 值，以及對應的 [appid](appid-key.md) 金鑰。
-   在啟用呼叫中，會 [**設定 \_ CLSCTX \_ 本機伺服器**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) 位，而且 CLSID 機碼不會指定 [LocalServer32](localserver32.md)、 [LocalServer](localserver.md)或 [LocalService](localservice.md)。 如果設定了其他 **CLSCTX** 位，則會遵循同進程、本機或遠端執行旗標的 [**處理演算法**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)。
-   CLSID 機碼包含 [InprocServer32](inprocserver32.md) 子機碼。
-   **InprocServer32** 索引鍵中指定的 proxy/stub DLL 存在。
-   [DllSurrogate](dllsurrogate.md)值存在於 **AppID** 索引鍵下。

如果有 **LocalServer**、 **LocalServer32** 或 **LocalService**，指出 exe 是否存在，exe 伺服器或服務將一律會依喜好啟動，以將 DLL 伺服器載入至代理程式。

必須指定 **DllSurrogate** 的命名值，才能進行代理程式啟用。 啟用指的是對下列任何啟用函數的呼叫：

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

若要啟動系統提供的代理程式實例，請將 **DllSurrogate** 的值設為空字串或 **Null**。 若要指定啟動自訂代理，請將值設定為代理的路徑。

如果 [RemoteServerName](remoteservername.md) 和 **DllSurrogate** 都指定給相同的 AppID，則會忽略 **RemoteServerName** 值，而且 **DllSurrogate** 值會導致本機電腦啟用。 若為遠端代理啟用，請在用戶端上指定 **RemoteServerName** 但不指定 **DllSurrogate** ，並在伺服器上指定 **DllSurrogate** 。

設計為一律在本身的代理程式中單獨執行的 DLL 伺服器，最好是以 AppID 等於其 CLSID 來設定。 在 **AppID** 下，只要以空字串值指定 **DllSurrogate** 。

最好是設定 DLL 伺服器，其設計目的是要在自己的代理程式中單獨執行，並使用 **AppID** 登錄機碼下指定的 [RunAs](runas.md)值，為網路上的多個用戶端提供服務。 **RunAs** 是否指定「互動式使用者」或特定使用者身分識別，取決於使用者介面、安全性和其他伺服器需求。 如果指定了 **RunAs** 值，不論用戶端的身分識別為何，都只會載入一個伺服器實例來服務所有用戶端。 另一方面，如果目的是要在代理中執行一個 DLL 伺服器實例，以服務每個遠端用戶端身分識別，請勿使用 **RunAs** 設定伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DLL 伺服器需求](dll-server-requirements.md)
</dt> <dt>

[代理共用](surrogate-sharing.md)
</dt> </dl>

 

 
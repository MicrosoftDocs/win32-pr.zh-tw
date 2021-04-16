---
title: 關於 RAS 管理 Dll
description: 每次使用者嘗試連線或中斷連線時，RAS 管理 DLL 都會匯出 RAS 伺服器所呼叫的功能。
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- RAS 系統管理 RRAS、RAS 管理 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104507744"
---
# <a name="about-ras-administration-dlls"></a>關於 RAS 管理 Dll

每次使用者嘗試連線或中斷連線時，RAS 管理 DLL 都會匯出 RAS 伺服器所呼叫的功能。 以下是 RAS 管理 DLL 的一些可能用途：

-   決定是否允許使用者連接到伺服器。 除了標準的 RAS 使用者驗證之外，管理 DLL 還可以提供安全性檢查。
-   記錄每個使用者連接的時間，並中斷與伺服器的連線。 這可能適用于計費或審核用途。
-   將 IP 位址指派給每個使用者。 這對安全性很有説明，因為這項功能是用來將使用者的連接對應至特定電腦。

RAS 系統管理 DLL 的位置是在登錄中指定;請參閱 [RAS 管理 DLL 登錄設定](ras-administration-dll-registry-setup.md)。

RAS 支援多個管理 Dll。 登錄支援多個 DLL 位置。 RAS 會以 Dll 在登錄中列出的順序來呼叫 Dll 中的函式，請參閱 [RAS 管理 DLL 登錄設定](ras-administration-dll-registry-setup.md)。

**Windows 2000 伺服器：** RAS 不支援多個 Dll。

RAS 系統管理 DLL 必須執行並匯出下列所有功能：

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

此外，RAS 管理 DLL 也必須執行和匯出

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) 和

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

或

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) 和

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

如果未執行所有必要的函式，則無法啟動 RAS。

**Windows 2000 伺服器：** 管理 DLL 必須執行 [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) 和 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) 函數。 如果 DLL 實作為這些函式的其中之一，它也必須執行另一個函數。

「路由及遠端存取」服務第一次啟動時，RAS 會呼叫 [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) 函數。 **MprAdminInitializeDll** 函式提供管理 DLL 執行任何必要初始化的機會。 同樣地，當「路由及遠端存取」服務關閉時，RAS 會呼叫 [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) 服務。 此函數可讓系統管理 DLL 在結束之前執行任何必要的清除。

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)和 [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)函式可讓 DLL 審核伺服器的使用者連接。 當使用者嘗試連接時，RAS 伺服器會呼叫 **MprAdminAcceptNewConnection** 函式。 此函式可讓使用者無法連接。 **MprAdminAcceptNewConnection** 函式也可以產生帳單或審核的記錄專案。 當使用者中斷連線時，RAS 伺服器會呼叫 **MprAdminConnectionHangupNotification** 函式，以記錄使用者中斷連線的時間。

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)和 [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)函數類似于 **MprAdminAcceptNewConnection** 和 [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)。 不過，當 RAS 呼叫 **MprAdminAcceptNewConnection2** 和 **MprAdminConnectionHangupNotification2** 函式時，ras 會傳入 [**ras \_ CONNECTION \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2)類型的其他參數。

RAS 支援多個管理 Dll。 只有在每個 Dll 中的 [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) 或 [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) 函數執行都接受連接時，才允許遠端存取使用者進行連線。 換句話說，每個 DLL 都必須接受連接，使用者才能連接。

當單一 RAS 連線連接到 RAS 伺服器時，可能會使用多個連結。 [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)和 [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)函式可讓管理 DLL 管理連接中的個別連結。 每當建立連線的新連結時，RAS 就會呼叫 **MprAdminAcceptNewLink** 。 因為所有連接都至少需要一個連結，所以在 [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)或 [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)傳回之後，RAS 一律會立即呼叫 **MprAdminAcceptNewLink** 一次，前提是 [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)或 [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)已接受連線。 只要關閉連接的連結，RAS 就會呼叫 **MprAdminLinkHangupNotification** 。

由於 RAS 支援多個系統管理 Dll，因此只有在每個 Dll 中的 [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) 函式都接受連接時，才允許遠端存取使用者進行連線。 換句話說，每個 DLL 都必須接受連結，才能建立連結。

在 RAS 伺服器驗證使用者之後，它會呼叫 [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) 函數來取得遠端用戶端的 IP 位址。 此函數提供將 IP 位址對應至撥入使用者的替代配置。 如果未執行 **MprAdminGetIpAddressForUser** ，RAS 伺服器會將遠端使用者與從 ip 位址的靜態集區中選取的 ip 位址建立關聯，或由動態主機設定通訊協定 (DHCP) 伺服器所選取的 ip 位址建立關聯。 **MprAdminGetIpAddressForUser** 函式可讓 DLL 覆寫此預設 ip 位址，並為每個使用者指定特定的 ip 位址。 **MprAdminGetIpAddressForUser** 函式可以設定旗標，讓 RAS 在使用者中斷連線時呼叫 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)功能。 然後，DLL 可以使用 **MprAdminReleaseIpAddress** 來更新其使用者與 IP 位址的對應。

RAS 支援多個系統管理 Dll，但它只會在第一個執行和匯出的 DLL 中呼叫 [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) 和 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) 函式。 RAS 會忽略其他 Dll 中這些函式的實作為。 RAS 會依照這些函式在登錄中列出的順序來檢查這些函式的[dll。](ras-administration-dll-registry-setup.md)

RAS 會將呼叫序列化至管理 DLL。 針對指定的 RAS 用戶端呼叫其中一個 DLL 的函式，並不會針對不同的 RAS 用戶端優先呼叫該函式;RAS 在初始呼叫完成之前，不會呼叫其他用戶端的函式。 此外，序列化會延伸至特定的函數群組。 IP 位址函數會序列化為群組;對 [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) 或 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) 的呼叫會封鎖對兩個函式的呼叫，直到初始呼叫傳回為止。 [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) 和 [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) 也會序列化為群組。

RAS 會在一個進程中執行指派 IP 位址的函式;連接和中斷連接通知的功能是在另一個進程中執行。 因此，DLL 不會相依于這兩組函數之間的共用資料。

請勿從 callout 函式內呼叫任何 [Ras 管理功能](ras-administration-functions.md) 或 [Ras 使用者管理功能](ras-user-administration-functions.md) 。 從標注函式內進行呼叫時，不會傳回這些函數的呼叫。

如果嘗試載入 RAS 管理 DLL 或呼叫其中一個 DLL 的函式時，RAS 伺服器會在系統事件記錄檔中記錄錯誤。 例如，如果 DLL 為匯出的函式指定了錯誤的名稱，或如果未在 DEF 檔案中包含函式名稱，就會發生這種情況。 事件記錄檔中的專案會指出失敗的原因。

**Windows 2000/NT：** 不支援多個系統管理 Dll。

 

 





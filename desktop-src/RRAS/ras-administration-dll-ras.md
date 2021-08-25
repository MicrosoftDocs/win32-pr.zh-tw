---
title: RAS 系統管理 DLL
description: 當使用者嘗試連線或中斷連線時，DLL 會匯出 RAS 伺服器所呼叫的函式。
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6be479d00175750fb4d6ffce73aab4439d2c7df9e6e07f97e9964f267ce82a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909918"
---
# <a name="ras-administration-dll"></a>RAS 系統管理 DLL

當使用者嘗試連線或中斷連線時，DLL 會匯出 RAS 伺服器所呼叫的函式。 您可以使用 DLL 來執行下列系統管理功能：

-   決定是否允許使用者連接到伺服器。 除了標準的 RAS 使用者驗證之外，這也可以提供安全性檢查。
-   記錄每個使用者連接的時間，並中斷與伺服器的連線。 這可能適用于計費或審核用途。
-   將 IP 位址指派給每個使用者。 這對於將使用者的連接對應至特定電腦的安全性目的很有用。

開發 RAS 伺服器管理 DLL 時，請執行下列功能。

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

RAS 系統管理 DLL 必須執行和匯出上述所有功能。 如果未執行任何功能，遠端存取服務將無法啟動。

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)和 [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)函式可讓 DLL 審核伺服器的使用者連接。 當使用者嘗試連接時，Windows NT/2000 Windows 的 RAS 伺服器會呼叫 **RasAdminAcceptNewConnection** 函數。 函數可以防止使用者連接。 您也可以使用函式來產生記錄檔中的專案，以供計費或進行審核。 當使用者中斷連線時，RAS 伺服器會呼叫 **RasAdminConnectionHangupNotification** 函式，以記錄使用者中斷連線的時間。

在 RAS 伺服器驗證呼叫端之後，它會呼叫 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) 函數來取得遠端用戶端的 IP 位址。 DLL 可以使用此函式來提供替代配置，以將 IP 位址對應至撥入使用者。 如果未執行 **RasAdminGetIpAddressForUser** ，RAS 伺服器會將遠端使用者連線到從 ip 位址的靜態集區中選取的 ip 位址，或由動態主機設定通訊協定 (DHCP) server 所選取的 ip 位址。 **RasAdminGetIpAddressForUser** 函式可讓 DLL 覆寫此預設 ip 位址，並為每個使用者指定特定的 ip 位址。 **RasAdminGetIpAddressForUser** 函式可以設定旗標，讓 RAS 在使用者中斷連線時呼叫 [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)功能。 DLL 可以使用 [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) 來更新其使用者與 IP 位址對應。

RAS 會將呼叫序列化至管理 DLL。 針對不同的 RAS 用戶端呼叫該函式時，永遠不會針對指定的 RAS 用戶端呼叫其中一個 DLL 的函式，在 RAS 呼叫其他用戶端的函式之前，一定會完成初始呼叫。 此外，序列化會延伸至特定的函數群組。 IP 位址函數會序列化為群組;對 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) 或 [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) 的呼叫會封鎖呼叫，直到初始呼叫完成為止。 [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) 和 [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) 也會序列化為群組。

RAS 會執行在一個進程中指派 IP 位址的函式，並在另一個進程中執行連接和中斷連接通知的函式。 因此，DLL 不應該相依于兩組函數之間的共用資料。

如果嘗試載入 RAS 管理 DLL 或呼叫其中一個 DLL 的函式時，RAS 伺服器會在系統事件記錄檔中記錄錯誤。 例如，如果 DLL 為匯出的函式指定了錯誤的名稱，或者如果它未在 .def 檔中包含函式名稱，就會發生這種情況。 事件記錄檔中的專案會指出失敗的原因。

**Windows 2000 伺服器和更新版本：** 執行此函式介面的 RAS 管理 Dll 無法再運作。 請改用 Windows 的最新版本所提供的 MprAdmin 函數介面。 如需詳細資訊，請參閱路由和 RAS 檔中的 [RAS 管理參考](remote-access-service-administration-reference.md) 。

 

 





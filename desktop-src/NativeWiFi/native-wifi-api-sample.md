---
description: 示範基本無線網路管理功能的使用。
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: 原生 Wifi API 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993119"
---
# <a name="native-wifi-api-sample"></a>原生 Wifi API 範例

示範如何使用基本無線網路管理功能的原生 Wifi API 範例，隨附于 Microsoft Windows 軟體開發套件 (SDK) 。 您可以從 [下載中心](https://developer.microsoft.com/windows/downloads)取得最新版本的 Windows SDK。

原生 Wifi 範例原始程式碼預設會安裝在下列目錄中：

**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ 範例 \\ NetDs \\ Wlan**

原生 Wifi API 範例位於下列資料夾底下：

**wlan**

原生 Wifi 範例可在 Windows Vista 和更新版本、windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2) 的無線區域網路 API 上進行編譯和執行。 Windows XP （含 SP3）和適用于 Windows XP SP2 的無線區域網路 API 不支援範例的部分功能。 如需 windows XP 含 SP3 以及適用于 Windows XP SP2 的無線區域網路 API 所支援的功能清單，請參閱 [WINDOWS xp 上的原生 WIFI Api 支援](about-wireless-lan-api-for-windows-xp-service-pack-2.md)。

原生 Wifi 範例會示範如何執行下列工作：

-   列舉無線介面。 請參閱 [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)。
-   取得介面的功能。 請參閱 [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability)。

    * * Windows XP 含 SP3 以及適用于 Windows XP SP2 的無線區域網路 API： * * 這項功能不受支援。

-   查詢介面。 請參閱 [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)。
-   設定網路介面的參數。 請參閱 [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)。 此功能可用來開啟和關閉無線無線電 (，因此可啟用或停用無線網路連線) 。
-   掃描可用的無線網路。 請參閱 [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)。
-   取得可用或可見無線網路的清單。 請參閱 [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)。
-   取得、儲存或刪除設定檔。 請參閱 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)、 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)和 [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)。
-   連線到無線網路或中斷其連接。 請參閱 [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) 和 [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用原生 Wifi](using-native-wifi.md)
</dt> <dt>

[Windows Vista 無線 SDK 論壇](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[針對 Windows Vista 802.11 無線連線進行疑難排解](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 

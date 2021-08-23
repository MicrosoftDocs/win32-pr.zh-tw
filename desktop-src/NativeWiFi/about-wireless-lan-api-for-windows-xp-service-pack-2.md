---
description: Windows XP service pack 2 (SP2) 和 Windows XP service pack 3 (SP3) 支援原生 Wifi API 功能的子集。
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Windows XP 上的原生 Wifi API 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc284ed24a6aa6ddb266b410a6233c15e063bf909aa9c82f0afa3dc070c9289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685308"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Windows XP 上的原生 Wifi API 支援

Windows XP service pack 2 (SP2) 和 Windows XP service pack 3 (SP3) 支援原生 Wifi API 功能的子集。 這項功能預設包含在 Windows XP SP3 中。 在 Windows XP （含 SP2）中，您可以套用可透過套用的修正程式（也就是 Windows XP Service Pack 2 (SP2) 的無線區域網路 API）來新增此功能。 如需詳細資訊或下載此修正程式，請參閱 [說明及支援] 知識庫中的「開發人員無法建立可透過 Microsoft Windows XP service Pack 2 中的無線零設定服務管理無線設定檔和連線的無線用戶端程式 (SP2) 」 [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) 。

由於 Windows XP 中的基礎結構差異，原生 Wifi API 有一些限制。 以下是限制清單：

-   最多可以有一個與設定檔相關聯的 SSID。
-   基礎結構網路一律會出現在配置檔案清單中的特定網路之前。
-   設定檔名稱衍生自 SSID，使用者無法將其設定為任一字元串。
-   不支援 PHY 類型。
-   不支援將 (PMK) 快取成對的主要金鑰。
-   獨立硬體廠商 (IHV) 擴充功能不受支援。
-   不支援設定檔許可權。
-   只有 wlan 通知進行中的連線 \_ \_ \_ \_ 完成，而且有 \_ 提供 wlan 通知的 \_ \_ 已中斷連線通知。
-   不支援 Global 802.1 X 和 EAPOL configuration 設定。

Windows XP 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API 支援下列功能：

-   [**WLAN \_ 通知 \_ 回呼**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WlanAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[關於原生 Wifi](about-native-wifi.md)
</dt> </dl>

 

 

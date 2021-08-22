---
description: 原生 Wifi 的新功能
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: 原生 Wifi 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a9430fa2c1645d574f8b4ab851a8cf5ce1407139cfe63a6aabeb3ebfd57abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064858"
---
# <a name="whats-new-in-native-wifi"></a>原生 Wifi 的新功能

## <a name="windows-10-version-2004"></a>Windows 10 (版本 2004)

請參閱透過網站布建 [Wi-Fi 設定檔](prov-wifi-profile-via-website.md)。

## <a name="windows-10"></a>Windows 10

已將對熱點2.0 的支援新增至 [WLAN \_ 設定檔架構](wlan-profileschema-schema.md)。 作用點2.0 可讓您使用現有的認證和服務提供者網路中的成員資格，自動連線至公用 Wi-Fi 服務。 服務提供者會指定如何使用新的架構專案來描述要使用的網路，以及如何對它們進行驗證。 請參閱 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素檔以取得詳細資料。

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 與 Windows Server 2012

下列功能已新增至 Windows 8 和 Windows Server 2012 上的原生 Wifi api。

Wi-Fi 直接功能，以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。 Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。

下列函數支援 Wi-Fi 直接功能。

-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

下列功能已新增至 Windows 7 和 Windows Server 2008 R2 上的原生 Wifi api。

無線裝載網路可讓單一實體的無線介面卡以用戶端的身分連線到 (AP) 的硬體存取點，同時作為軟體 AP，讓其他支援無線裝置的裝置能夠連線。

下列功能支援無線裝載的網路功能。

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

下列可搭配無線託管網路使用的新結構。

-   [**WLAN \_ 託管 \_ 網路 \_ 連線 \_ 設定**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**WLAN \_ HOSTED \_ NETWORK \_ 資料 \_ 對等 \_ 狀態 \_ 變更**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**WLAN \_ 託管 \_ 網路 \_ 對等 \_ 狀態**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**WLAN \_ HOSTED \_ NETWORK \_ 無線電 \_ 狀態**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**WLAN \_ 託管 \_ 網路 \_ 安全性 \_ 設定**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**WLAN \_ 託管 \_ 網路 \_ 狀態 \_ 變更**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**WLAN \_ 託管 \_ 網路 \_ 狀態**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

下列使用無線裝載網路的新列舉。

-   [**WLAN \_ 託管 \_ 網路 \_ 通知 \_ 碼**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**WLAN \_ 託管 \_ 網路 \_ 操作碼**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**WLAN \_ 託管 \_ 網路 \_ 對等 \_ 驗證 \_ 狀態**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**WLAN \_ 託管 \_ 網路 \_ 原因**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**WLAN \_ 託管 \_ 網路 \_ 狀態**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於無線託管網路](about-the-wireless-hosted-network.md)
</dt> <dt>

[使用無線託管網路和網際網路連線共用](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 




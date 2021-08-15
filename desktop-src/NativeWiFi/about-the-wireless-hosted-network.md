---
description: 關於無線託管網路
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: 關於無線託管網路
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f207dceaf0c835acc7886b48d5e6b030179240afb2a7f50b6f3744c574a185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801488"
---
# <a name="about-the-wireless-hosted-network"></a>關於無線託管網路

無線裝載網路是 Windows 7 和安裝了無線局域網路服務 Windows Server 2008 R2 支援的新 WLAN 功能。 這項功能會實現兩個主要功能：

-   將實體無線介面卡虛擬化為一個以上的虛擬無線介面卡，有時又稱為虛擬 Wi-fi。
-   以軟體為基礎的無線存取點 (AP) 有時稱為 SoftAP，使用指定的虛擬無線介面卡。

這兩個函式會一起並存于 Windows 系統中。 啟用或停用無線裝載的網路，可啟用或停用虛擬 Wi-Fi 和 SoftAP。 在 Windows 中，無法分別啟用或停用這兩個函式。

利用這項功能，Windows 電腦可以使用單一實體無線介面卡，以用戶端的身分連線到硬體存取點 (AP) ，同時作為軟體 AP，讓其他支援無線裝置的裝置連線到該裝置。 這項功能需要在本機電腦上安裝具有網路功能的無線介面卡。 無線介面卡的驅動程式必須執行由 Microsoft 定義的無線區域網路設備磁碟機模型，以用於 Windows 7。 若要接收 Windows 7 標誌，無線驅動程式必須執行無線裝載網路功能。

在本機電腦上，任何時候都有一個已啟用的無線網路，而且無線裝載的網路只會使用一個無線介面卡。 如果有多個受網路支援的無線介面卡，Windows 將會選擇一個介面卡，以供無線裝載的網路使用。 使用裝載的網路 Api 時，可將受主機網路的無線介面卡虛擬化到最多3個邏輯配接器：

-   站配接器 (STA) 供用戶端或臨機操作無線應用程式使用。 STA 介面卡會繼承原始實體無線介面卡的所有設定，並表現與實體介面卡相同的行為。 在概念上，您可以在虛擬化之後，將 STA 介面卡視為與實體介面卡相同。 只要對應的無線實體介面卡存在，STA 介面卡一律會在系統中。
-   用來裝載 SoftAP 的無線網路的 AP 介面卡。 只有在第一 (次呼叫 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)、 [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)或 [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)函式時，才會在 Windows 系統中出現 AP 介面卡) 。 一旦建立之後，就會在無線裝載的網路停用之前，將 AP 介面卡保留在系統中。 如果稍後已啟用無線裝載網路，則會再次在系統中顯示 AP 介面卡。
-   虛擬站介面卡 (VSTA) 供硬體廠商用來擴充 Windows 中的無線裝載網路功能。 VSTA 介面卡是選擇性的，且只能由對應的 IHV 服務在系統中建立。 與「AP 介面卡」不同的是，只有在 ihv 服務將介面卡初始化之後，才會在 Windows 系統中存在，直到 ihv 服務釋出介面卡的時間為止。

虛擬 Wi-Fi 會將邏輯配接器對應至 NDIS 埠。 將 STA、AP 和 VSTA 介面卡系結至特定的 NDIS 埠，是由 Windows 決定。 STA 介面卡一律會系結至埠0。 當虛擬化啟動時，會將 AP 介面卡系結至下一個可用的 NDIS 埠，且系結會維持不變，直到虛擬化在無線託管網路停用時才會結束。 VSTA 介面卡會系結至下一個可用的 NDIS 埠（當對應的 IHV 服務初始化時），且系結會維持不變，直到由 IHV 服務釋放為止。

您可以建立 VSTA 介面卡，以供 Ihv 使用，而不需要建立 SoftAP 介面卡。

下列組合適用于具有虛擬化的實體介面卡：

-   STA 介面卡。
-   STA 和 AP 介面卡。
-   STA 和 VSTA 介面卡。
-   STA、AP 和 VSTA 介面卡。

除了 STA 介面卡案例之外，所有其他組合都只有在啟用無線裝載的網路時才有效。 就像單一 STA 介面卡案例一樣，如果無線裝載網路已停用，就會是實體介面卡。 如果已啟用無線裝載網路，則在系統中從未叫用無線裝載的網路時，它是 STA 介面卡。

在 AP 介面卡和系統中的任何其他介面卡之間，禁止第2層橋接。 相同的限制適用于在系統中出現的 VSTA 介面卡。

Windows 中的無線裝載網路功能會實現 SoftAP。 不過，此 SoftAP 並不是用來取代以硬體為基礎的無線 AP 裝置。 尤其是，當電腦進入睡眠狀態 (待命) 、休眠或電腦重新開機之前，如果無線裝載網路正在執行，無線裝載的網路將會停止。 當電腦從睡眠、休眠或重新開機恢復之後，無線裝載的網路將不會自動重新開機。 此外，SoftAP 也不會提供 DNS 解析。 如果無法使用網際網路連線共用來提供外部 DNS 伺服器 (請參閱下面的《 ICS 討論」) 。在與 SoftAP 連線的兩部電腦或裝置之間的完整功能變數名稱 (FQDN) 解析（包括裝載 SoftAP 的電腦），只有在這兩個實體將 SoftAP 網路的網路類型標示為私用 (HOME 或 [網路類別] 快顯視窗中的 [工作] 時，才能運作。)  由於裝載 SoftAP 的機器一律會將 SoftAP 網路類型標示為私人，因此只有連線到 SoftAP 的電腦或裝置必須將 SoftAP 網路類型標示為私人，才能讓 FQDN 解析正常運作。

SoftAP 和臨機操作網路在相同的實體介面卡上互斥。 如果 SoftAP 正在 AP 介面卡上執行，而且使用者或應用程式在 STA 介面卡上啟動臨機操作網路，將會關閉 SoftAP。 在 STA 介面卡上執行 Iif 臨機操作網路，嘗試在 AP 介面卡上啟動 SoftAP 將會失敗。

為了保護裝載 SoftAP 的電腦與連線到 SoftAP 的裝置之間的無線通訊，無線裝載的網路要求所有連線的裝置都必須使用 WPA2-PSK/AES 加密套件。 當第一次呼叫 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)、 [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)或 [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)函式時，如果第一 (次叫用無線裝載的網路時，共用金鑰是由 Windows 所產生的63字元值) 。 使用者或應用程式無法變更此共用金鑰的值，但應用程式可以藉由呼叫 [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) 函式要求作業系統重新產生新的金鑰，或使用者可以要求作業系統使用 **netsh wlan** 命令重新產生新的金鑰。 此共用金鑰稱為無線裝載網路的主要或系統金鑰，而且會在無線裝載網路的啟動和停止時持續存在。 此主要金鑰在 **netsh wlan** 命令中稱為「系統安全性金鑰」。

為了方便使用，無線裝載的網路也支援次要或使用者安全性金鑰的概念，該金鑰更容易使用，但可能較不安全。 此次要金鑰在 **netsh wlan** 命令中稱為「使用者安全性金鑰」。 Windows 不會產生次要金鑰。 使用者必須提供此金鑰的值。 使用者或應用程式可以藉由呼叫 [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) 函式或使用 **netsh wlan** 命令來設定或變更金鑰值。 次要金鑰可以設定為持續或暫存。 針對暫存金鑰，如果無線裝載的網路已在執行中，則在無線裝載的網路停止之前，次要金鑰將會是有效的。 針對暫存金鑰，如果無線裝載的網路未執行，它只會在下一個無線裝載的網路開始和停止之間有效。

在任何電腦上，無線裝載的 Hetwork 只有一個主要金鑰和最多一個次要金鑰。 透過 Wi-Fi 受保護的設定)  (的任何裝置，將會收到主要金鑰。 其他手動設定的裝置可以使用任一個金鑰。 每當金鑰變更時，具有舊金鑰值的任何裝置都將無法連線到無線裝載的網路，而不需要使用新的金鑰重新布建。 不過，具有其他未變更金鑰的裝置應該會繼續能夠連線到無線裝載的網路。

應用程式可以註冊無線裝載的網路通知，如此一來，當無線裝載的網路上的屬性變更時，就會將 WLAN 通知傳送至應用程式回呼。 應用程式會藉由呼叫 [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) ，並將 *dwNotifSource* 參數設定為包含 WLAN \_ 通知 \_ 來源 HNWK 位，來註冊無線裝載的網路通知 \_ 。

Windows 提供兩種方式讓 IT 系統管理員管理無線裝載的網路功能。 對於網域成員的電腦，系統管理員可以使用群組原則來禁止無線裝載的網路。 系統管理員可以使用 **netsh wlan** 命令，啟用或停用本機電腦上的無線網路。

## <a name="supported-scenarios-for-wireless-hosted-network"></a>無線託管網路的支援案例

無線裝載網路可為 Windows 電腦提供兩種主要案例：

•提供無線個人區域網路 (無線 PAN) ，以與其他各種無線裝置搭配使用的能力。

•可供其他電腦和裝置使用的網路連線共用。

無線 PAN 是由無線裝載網路自行啟用的主要案例。 當無線裝載的網路在電腦上啟動後，任何支援 WPA2/AES 的支援無線裝置都可以連線到 softAP，就像是連線到一般硬體 AP 一樣。 連線到無線裝載網路的裝置形成了無線 PAN，讓他們能夠與裝載 SoftAP 的 Windows 電腦以及本身之間交換資訊。

供其他電腦和裝置使用的網路連線共用需要使用網際網路連線共用 (ICS) 。 在此案例中，ICS 的公用介面是共用連線，而私用介面是裝載 SoftAP 的虛擬配接器。 共用連接可以是乙太網路、無線區域網路或無線 WAN 連線。 在無線區域網路連線的情況下，ICS 的公用介面可以是來自另一個無線區域網路介面卡或裝載 SoftAP 的相同實體無線介面卡上的站虛擬網路介面卡。 最常見的網路共用用途是共用網際網路連線，而 ICS 公用介面上的網路可以存取網際網路。

無線裝載的網路會與 Wi-Fi 受保護的安裝程式 (WPS) ，Windows 7 和 Windows Server 2008 R2 中的另一項重要的新功能，並安裝了無線局域網路服務。 無線裝載的網路和 WPS 支援的案例會為支援 wps 的裝置布建支援 WPS 的裝置，以用於不支援 WPS 的硬體 AP。 在此情況下，會在背景中叫用裝載于 Windows 的 SoftAP，以將硬體 AP 設定檔推送至支援 WPS 的裝置。

## <a name="user-and-application-access-to-wireless-hosted-network"></a>無線裝載網路的使用者和應用程式存取

終端使用者會使用協力廠商應用程式或 **netsh** 命令，與 Windows 中的無線託管網路功能互動。 目前沒有任何原生使用者介面可用於設定或管理 Windows 7 上的無線裝載網路，或是安裝了無線局域網路服務 Windows Server 2008 R2。

協力廠商應用程式和 **netsh** 命令是以公用無線託管網路功能為基礎。 這組函式提供一組完整的功能，可在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上管理無線託管網路。

以下是無線託管網路功能的清單，以及來自終端使用者觀點的一般動作，該函式會用於：



| 使用的函數                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)、 [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | 啟動無線託管網路。<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)、 [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | 停止無線託管網路。<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)、 [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)、 [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | 設定無線託管網路設定 (變更 SSID、變更次要金鑰，或要求重新產生主要金鑰) 。<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)、 [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)、 [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | 查詢無線裝載的網路設定和資訊 (狀態、SSID、次要金鑰、主要金鑰，或目前已連線 ) 的裝置清單。<br/> |



 

**Netsh** 命令是供 advanced 使用者或系統管理員使用。

*Netsh.exe* 的無線區域網路有許多子命令。 您可以從命令提示字元中輸入下列命令，以取得 **netsh** 和 wireless LAN 選項的完整清單：

**netsh wlan/？**

Technet 上也有提供無線區域網路所有 Netsh 命令的相關檔。 如需詳細資訊，請參閱 [無線區域網路 (WLAN) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

以下是一些通常用於無線區域網路和無線裝載網路的 **netsh** 命令，雖然支援其他命令組合：



| 命令                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | 描述                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | 啟動無線託管網路。<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | 停止無線託管網路。<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ 模式 = \] 允許不允許 \|**<br/>                                                                                                                                                                                                                                                                      | 啟用或停用無線託管網路。<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid = \] <ssid> \[ key = \] <passphrase> \[ keyUsage = \] 永久性 \| 暫存** <br/> | 設定無線託管網路設定。<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan refresh hostednetwork \[ data = \] key**<br/>                                                                                                                                                                                                                                                                                       | 重新整理無線網路主機金鑰。<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ 設定 = \] 安全性\]**<br/>                                                                                                                                                                                                                                                                     | 顯示無線主控的網路資訊。<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | 顯示無線區域網路的通用設定。<br/>           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用無線託管網路和網際網路連線共用](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[無線託管網路範例](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 

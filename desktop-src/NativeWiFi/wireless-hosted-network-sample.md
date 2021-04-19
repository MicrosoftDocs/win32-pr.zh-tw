---
description: 示範無線託管網路功能的使用。
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: 無線託管網路範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974061"
---
# <a name="wireless-hosted-network-sample"></a>無線託管網路範例

Microsoft Windows 軟體開發套件 (SDK) 隨附的無線裝載網路範例，示範如何使用無線裝載的網路功能。 您可以從 [下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)取得最新版本的 Windows SDK。

根據預設，無線裝載的網路範例原始程式碼會安裝在下列目錄中：

**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ Wlan**

無線 Hosted Network 範例位於下列資料夾底下：

**WirelessHostedNetwork**

您可以在 Windows 7 的 Windows SDK 上編譯無線裝載的網路範例。 無線裝載的網路範例可以在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行。

在 Windows 7 上，以及安裝了無線局域網路服務的 Windows Server 2008 R2 上，如果電腦上有具備網路功能的無線介面卡，作業系統會安裝一個虛擬裝置。 如果電腦具有單一無線網路介面卡，此虛擬裝置通常會在 [網路連線] 資料夾中顯示為「無線網路連線2」，且裝置名稱為「Microsoft 虛擬 WiFi 微型網路介面卡」。 此虛擬裝置專門用來執行軟體存取點 (SoftAP) 連接。 此虛擬裝置的存留期會系結至實體無線介面卡。 如果實體無線介面卡已停用，此虛擬裝置也會一併移除。

無線裝載的網路功能可用來啟動和停止無線裝載的網路、設定或變更設定，或查詢資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於無線託管網路](about-the-wireless-hosted-network.md)
</dt> <dt>

[使用託管網路和網際網路連線共用](using-hosted-network-and-internet-connection-sharing.md)
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

 

 




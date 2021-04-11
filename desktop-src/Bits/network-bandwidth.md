---
title: 網路頻寬
description: 背景傳輸只會使用閒置的網路頻寬，以保持使用者與其他網路應用程式（例如 Internet Explorer）的互動式體驗。
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023711"
---
# <a name="network-bandwidth"></a>網路頻寬

背景傳輸只會使用閒置的網路頻寬，以保持使用者與其他網路應用程式（例如網頁瀏覽器）的互動式體驗。 BITS 會在使用者增加或減少其頻寬的使用時，調整其頻寬的使用方式。 請注意，BITS 在高網路使用期間仍會傳輸少量的資料，以確保 BITS 作業會產生進度。

BITS 會監視網際網路閘道裝置上的網路流量 (IGD) 或用戶端的網路介面卡 (NIC) ，而且只會使用網路頻寬的閒置部分。 BITS 也可讓您在 HTTP 連線上 [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) ，以協助減輕網路擁塞。

如果 BITS 使用網路介面卡來測量流量，且沒有在用戶端上執行任何網路應用程式，BITS 將耗用大部分的可用頻寬。 這並不表示用戶端以外的網路閒置了;網路可能會有完整的容量。

如果用戶端有快速的網路介面卡，但完整的網際網路連線是透過低速連結 (例如 DSL 路由器) ，因為 BITS 將會競爭整個頻寬，而不是只使用低速連結上的可用頻寬，因此這可能是一個問題。BITS 無法看到用戶端以外的網路流量。

支援計數器的閘道裝置可以消除此問題，因為 BITS 會測量低速連結上的流量，並適當地使用頻寬。 如果裝置不支援計數器，您可以使用 **MaxInternetBandwidth** 原則來限制 BITS 在用戶端電腦上使用的頻寬，以降低這種連線類型的影響。 如需詳細資訊，請參閱 [群組原則](group-policies.md)。

如果電腦包含多個網路介面，例如數據機、虛擬私人網路 (VPN) ，以及數個網路介面卡)  (NIC，BITS 會呼叫 IP Helper 函式 [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex)，以判斷具有最適合指定 ip 位址之路由的介面。 然後，BITS 會監視該介面上的頻寬使用量。

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>使用網際網路閘道裝置 (IGD) 來判斷使用量

若要使用閘道裝置，裝置必須支援位元組計數器， (裝置必須回應 GetTotalBytesSent 和 GetTotalBytesReceived 動作) 且必須啟用通用隨插即用 (UPnP) 。

如果有下列情況，BITS 會使用網路介面卡：

-   閘道裝置不支援計數器
-   未啟用 UPnP
-   伺服器位於相同的子網中
-   閘道裝置未傳回小於200滴答的計數器資料

如果使用者使用公用網路設定檔，則設定檔必須允許 UPnP。 根據預設，私用和網域網路設定檔會允許 UPnP。

如果使用 VPN 連線，BITS 會使用 UPnP 傳回的第一個裝置。
---
title: 關於 EAP
description: 可延伸的驗證通訊協定 (EAP) ，這是許多 Microsoft 網路元件所支援的標準。
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- 可延伸的驗證通訊協定，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84866f7f550213850bf95c39a6f0847df31bed3550db66139f2ec30bf921b5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276041"
---
# <a name="about-eap"></a>關於 EAP

本主題說明可延伸的驗證通訊協定 (EAP) ，這是許多 Microsoft 網路元件所支援的標準。

## <a name="eap-components"></a>EAP 元件

EAP 對於保護無線 (802.1 X) Lan、有線區域網路以及撥號和虛擬私人網路 (Vpn) 的安全性非常重要。

下列元件支援 EAP 通訊協定。

-   適用于撥號和 VPN 的 Microsoft 遠端存取用戶端和伺服器 (PPTP 和 L2TP/IPSec) 將 EAP 實作為 PPP 的延伸模組。 如需詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063)。
-   Microsoft IEEE 802.1 X 相容的無線和有線區域網路客戶會依照 IEEE 802.1 X draft 標準的定義來實行 EAP。
-   Microsoft RADIUS 伺服器稱為網際網路驗證服務 (IAS) 依照 [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055)中的定義來實行 EAP。

上述所有元件都支援透過 Microsoft Windows 軟體開發套件 (SDK) 的可延伸架構，讓您可以整合協力廠商驗證模組。 這種可延伸的機制可用來支援權杖卡、Kerberos、公開金鑰和 S/金鑰驗證通訊協定。

## <a name="protected-extensible-authentication-protocol"></a>受保護的可延伸驗證通訊協定

除了 EAP 之外，無線 (802.1 X) 實行和 RADIUS 伺服器也支援稱為受保護 EAP (PEAP) 的新興標準。

PEAP 提供許多重要服務給其他 EAP 驗證通訊協定，如下所示。

-   PEAP 使用傳輸層安全性 (TLS) （ (SSL) 型技術的安全通訊端層），來加密其他 EAP 驗證通訊協定的 EAP 封包。 如需詳細資訊，請參閱 [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050)。
-   PEAP 使用伺服器憑證來驗證服務器端與 RADIUS 伺服器。
-   PEAP 提供快速的重新驗證功能，可支援在無線裝置之間進行有效率的漫遊。
-   PEAP 管理分散和重新組裝 EAP 封包。
-   PEAP 會產生用來加密無線流量的金鑰。

PEAP 讓撰寫 EAP 通訊協定更加容易，因為程式設計師不再需要解決這些問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 EAP 和 EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 





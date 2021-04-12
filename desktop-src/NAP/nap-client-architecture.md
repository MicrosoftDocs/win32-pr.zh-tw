---
title: NAP 用戶端架構
description: NAP 用戶端是執行 Windows XP （含 Service Pack 3） (SP3) 、Windows Vista 或 Windows Server 2008 的電腦，其中包含 NAP 平臺。
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301828"
---
# <a name="nap-client-architecture"></a>NAP 用戶端架構

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 用戶端是執行 Windows XP （含 Service Pack 3） (SP3) 、Windows Vista 或 Windows Server 2008 的電腦，其中包含 NAP 平臺。

下圖顯示 nap 用戶端上 NAP 平臺的架構。

![nap 用戶端上 nap 平臺的架構](images/nap-client-side-arch.png)

NAP 用戶端架構包含下列各項：

-    (EC) 元件的強制用戶端層

    每個 NAP EC 都是針對不同類型的網路存取而定義。 例如，DHCP 設定有 NAP EC，以及遠端存取 VPN 連線的 NAP EC。 NAP EC 可以與特定類型的 NAP 強制端點比對。 例如，DHCP NAP EC 的設計目的是要與以 DHCP 為基礎的 NAP 強制端點搭配使用。 NAP 平臺和協力廠商軟體廠商會提供部分 NAP ECs，或 Microsoft 可提供他人。

-    (SHA) 元件的系統健康情況代理程式層級

    SHA 元件會維護和報告系統健康情況的一或多個元素。 例如，可能會有適用于防毒軟體的 SHA，以及用於作業系統更新的 SHA。 SHA 可以與補救伺服器比對，這是一部電腦，其中包含 NAP 用戶端可以存取的健康狀態更新資源，可補救其不符合規範的狀態。 例如，檢查防毒軟體簽章的 SHA 與包含最新防毒軟體簽章檔案的伺服器相符。 Sha 不需要有對應的補救伺服器。 例如，SHA 可以直接檢查本機系統設定，以確保已啟用主機型防火牆。 Windows Vista 和 Windows XP Service Pack 3 包含 Windows 安全性健康情況代理程式 (的 WSHA) ，可監視 Windows 安全性 Center 的設定。 協力廠商軟體廠商或 Microsoft 可以提供其他 Sha 給 NAP 平臺。

-   NAP 代理程式

    會維護 NAP 用戶端的目前健全狀況狀態資訊，並促進 NAP EC 和 SHA 層之間的通訊。 Nap 代理程式隨附于 NAP 平臺。

-   系統健康狀態代理程式 API

    提供一組功能，可讓 Sha 向 NAP 代理程式註冊、指出系統健康狀態、回應 NAP 代理程式系統健康狀態的查詢，以及讓 NAP 代理程式將系統健康情況補救資訊傳遞給 SHA。 SHA API 可讓廠商建立和安裝其他 Sha。 SHA API 隨附于 NAP 平臺。 請參閱下列 NAP 介面： [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)、 [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)和 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)。

為了指出特定 SHA 的健全狀況狀態，SHA 會建立 ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) 的健全狀況聲明，並將其傳遞至 NAP 代理程式。 SoH 可包含一或多個系統健康狀態元素。 例如，防毒程式的 SHA 可以建立 SoH，其中包含電腦上執行的防毒軟體的狀態、其版本，以及最後收到的防毒軟體簽章更新。 每當 SHA 更新其狀態時，就會建立新的 SoH，並將其傳遞至 NAP 代理程式。 為了指出 NAP 用戶端的整體健全狀況狀態，NAP 代理程式會使用系統健康狀態聲明 (SSoH) ，其中包含 NAP 用戶端的版本資訊，以及所安裝 Sha 的 Soh 集。

下列各節將進一步詳細說明 NAP 用戶端架構的元件。

## <a name="nap-enforcement-client"></a>NAP 強制用戶端

NAP 強制用戶端 (EC) 要求某個網路存取層級，會將電腦的健康狀態傳遞到提供網路存取的 NAP 強制端點。 NAP 強制端點是使用 NAP 或可搭配 NAP 使用的電腦或網路存取裝置，需要評估 NAP 用戶端的健康狀態，並提供受限的網路存取或通訊。 如果電腦的健全狀況不符合規範，則 NAP EC 會指出 nap 用戶端對 NAP 用戶端架構的其他元件有何限制的狀態。

在 Windows XP 含 SP3、Windows Vista 和 Windows Server 2008 中提供之 NAP 平臺的 NAP ECs 如下：

-   Ipsec 受 IPsec 保護的通訊 NAP EC。
-   802.1 X 驗證連接的 EAPHost NAP EC。
-   遠端存取 VPN 連線的 VPN NAP EC。
-   Dhcp NAP EC 用於以 DHCP 為基礎的 IPv4 位址設定。
-   Ts 閘道連接的 TS 閘道 NAP EC。

若是 Windows XP SP3，802.1 X 驗證的有線和無線連線有個別的 NAP ECs。

### <a name="ipsec-nap-ec"></a>IPsec NAP EC

IPsec NAP EC 是從 NAP 代理程式取得 SSoH 的元件，並將其傳送至健康情況登錄授權單位 (HRA) 、執行 Windows Server 2008 的電腦，以及 Internet Information Services (IIS) ，以從憑證授權單位單位取得符合規範之電腦 (CA) 的健康情況憑證。 IPsec NAP EC 在 [NAP 用戶端設定] 嵌入式管理單元中也稱為 IPsec 信賴憑證者 EC。 IPsec NAP EC 也會與下列互動：

-   用來儲存健康情況憑證的憑證存放區。
-   Windows 中的 IPsec 元件，可確保健全狀況憑證用於受 IPsec 保護的通訊。
-   以主機為基礎的防火牆 (例如 Windows 防火牆) ，因此防火牆允許受 IPsec 保護的流量。

### <a name="eaphost-nap-ec"></a>EAPHost NAP EC

EAPHost NAP EC 是從 NAP 代理程式取得 SSoH 的元件，並將其傳送為 802.1 X 驗證連接的 PEAP 型別長度值 (TLV) 訊息。 EAPHost NAP EC 在 [NAP 用戶端設定] 嵌入式管理單元中稱為 EAP 隔離 EC。

### <a name="vpn-nap-ec"></a>VPN NAP EC

VPN NAP EC 是遠端存取連線管理員服務中的功能，可從 NAP 代理程式取得 SSoH，並將其作為遠端存取 VPN 連線的 PEAP-TLS 訊息傳送。 在 [NAP 用戶端設定] 嵌入式管理單元中，VPN NAP EC 稱為「遠端存取隔離 EC」。

### <a name="dhcp-nap-ec"></a>DHCP NAP EC

DHCP NAP EC 是 DHCP 用戶端服務中的功能，使用業界標準 DHCP 訊息來交換系統健康情況訊息和有限的網路存取訊號。 在 [NAP 用戶端設定] 嵌入式管理單元中，IPsec DHCP EC 稱為 DHCP 隔離 EC。 DHCP NAP EC 從 NAP 代理程式取得 SSoH。 DHCP 用戶端服務會在必要時將 SSoH 片段化，並將每個片段放入在 DHCPDiscover、DHCPRequest 或 DHCPInform 訊息中傳送的 Microsoft 廠商特定 DHCP 選項。 DHCPDecline 和 DHCPRelease 訊息不包含 SSoH。

## <a name="system-health-agent"></a>系統健康狀態代理程式

系統健康狀態代理程式 (SHA) 會執行系統健康狀態更新，並以 SoH 的形式將其狀態發佈至 NAP 代理程式。 SoH 包含 NAP 健全狀況原則伺服器可用來確認用戶端電腦是否處於健全狀況的必要狀態的資訊。 SHA 會與系統健康狀態驗證（ (SHV) 在 NAP 平臺架構的伺服器端上）進行比對。 相對應的 SHV 會將 SoH 回應 (SoHR) 傳送給 NAP 用戶端，而 NAP 用戶端是由 NAP EC 和 NAP 代理程式傳遞至 SHA，告知它在 SHA 不是處於健康狀態的必要狀態時該怎麼辦。 例如，防毒軟體 SHV 傳送的 SoHR 可以指示對應的防毒軟體 SHA 查詢防毒軟體簽章伺服器，以取得最新版本的防毒軟體簽章檔案。 SoHR 也可以包含要查詢的防毒軟體簽章伺服器的名稱或 IP 位址。

SHA 可以使用本機安裝的原則用戶端，協助系統健康管理功能與原則伺服器搭配使用。 例如，軟體更新 SHA 可以使用本機安裝的軟體用戶端軟體 (原則用戶端) ，以 (原則伺服器) 的軟體補救伺服器執行版本檢查和安裝和更新功能。

## <a name="nap-agent"></a>NAP 代理程式

NAP 代理程式提供下列服務：

-   收集每個 SHA 的 Soh 並加以快取。 每當 SHA 提供新的或更新的 SoH 時，就會更新 SoH 快取。
-   會儲存 SSoH，並在要求時將其提供給 NAP ECs。
-   當受限制的狀態變更時，將通知傳遞至 Sha。
-   會維護系統限制的狀態，並收集每個 SHA 的狀態資訊。
-   將 Sohr 傳遞給適當的 SHA。

 

 





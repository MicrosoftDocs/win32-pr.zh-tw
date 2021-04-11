---
title: NAP 伺服器端架構
description: NAP 伺服器端架構
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092559"
---
# <a name="nap-server-side-architecture"></a>NAP 伺服器端架構

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 伺服器端平臺架構會使用執行 Windows Server 2008 的電腦。 下圖顯示 NAP 平臺的伺服器端支援架構，包括 Windows 型 NAP 強制端點和 NAP 健康原則伺服器。

![nap 平臺的伺服器端支援架構](images/nap-server-side-arch.png)

以 Windows 為基礎的 NAP 強制端點有一層 NAP 強制伺服器 (ES) 元件。 每個 NAP ES 都是針對不同類型的網路存取或通訊而定義。 例如，遠端存取 VPN 連線的 NAP ES，以及 DHCP 設定的 NAP ES。 NAP ES 通常符合特定類型的支援 NAP 用戶端。 例如，DHCP NAP ES 是設計來搭配使用 DHCP 型 NAP 強制用戶端 (EC) 。 協力廠商軟體廠商或 Microsoft 可以為 NAP 平臺提供額外的 NAP ESs。 NAP ES 從其對應的 NAP EC 取得健全狀況 (SSoH) 的系統聲明，並將其傳送至 NAP 健康原則伺服器，作為遠端驗證撥入使用者服務 (RADIUS) 廠商專屬的屬性 (VSA) 的 Access-Request [訊息](https://www.ietf.org/rfc/rfc2865.txt?number=2865)

如伺服器端架構圖所示，NAP 健全狀況原則伺服器具有下列元件：

-   網路原則伺服器 (NPS) 服務

    接收 RADIUS Access-Request 訊息、解壓縮 SSoH，然後將它傳遞給 NAP 管理伺服器元件。 NPS 服務隨附于 Windows Server 2008。

-   NAP 管理伺服器

    促進 NPS 服務與系統健康狀態驗證 (Shv) 之間的通訊。 Nap 管理伺服器元件隨附于 NAP 平臺。

-   SHV 元件的層級

    每個 SHV 都是針對一或多個系統健康狀態資訊類型所定義，而且可以與 SHA 相符。 例如，可能有一個適用于防毒程式的 SHV。 SHV 可能與一或多個健康需求伺服器相符。 例如，用於檢查防毒軟體簽章的 SHV 會與包含最新簽章檔案的伺服器相符。 Shv 不需要有對應的健康需求伺服器。 SHV 可以指示支援 NAP 的用戶端檢查本機系統設定，以確定已啟用以主機為基礎的防火牆。 Windows Server 2008 包含 Windows 安全性健全狀況驗證程式 (WSHV) 。 其他 Shv 由協力廠商軟體廠商或 Microsoft 做為 NAP 平臺的附加元件提供。

-   SHV API

    提供一組函數呼叫，可讓 Shv 向 NAP 管理伺服器元件註冊、接收健康狀態聲明 (Soh) 自 NAP 管理伺服器元件，以及傳送健全狀況回應的聲明 (Sohr) 至 NAP 管理伺服器元件。 SHV API 隨附于 NAP 平臺。 請參閱下列 NAP 介面： [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) 和 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)。

如先前所述，NAP 伺服器端基礎結構的較常見設定是由 NAP 強制端點所組成，以提供特定類型的網路存取或通訊，以及個別的 NPS 健康原則伺服器，提供系統健康情況驗證和修復。 您可以在個別的 Windows NAP 強制端點上，將 NPS 服務安裝為 NAP 健康原則伺服器。 不過，在此設定中，每個 NAP 強制端點接著必須個別設定網路存取和健康原則。 建議的設定是使用不同的 NAP 健康原則伺服器。

整體 NAP 架構包含下列元件集：

-   三個 NAP 用戶端元件 (SHA 層、NAP 代理程式和 NAP EC 層) 。
-   四個 NAP 伺服器端元件 (SHV 層、NAP 管理伺服器、NPS 服務，以及 Windows 型 NAP 強制端點) 的 NAP ES 層。
-   健康需求伺服器，也就是可提供 NAP 健康原則伺服器目前系統健康情況需求的電腦。
-   補救伺服器，這是包含 NAP 用戶端可以存取以補救其不符合規範狀態的健康狀態更新資源的電腦。

下圖顯示 NAP 平臺元件之間的關聯性。

![nap 平臺元件之間的關聯性](images/nap-components.png)

請注意下列元件集的相符：

-   NAP ECs 和 NAP ESs 通常相符。

    例如，NAP 用戶端上的 DHCP NAP EC 與 DHCP 伺服器上的 DHCP NAP ES 相符。

-   可以比對 SHA 和補救伺服器。

    例如，用戶端上的防毒軟體 SHA 符合防毒軟體的補救伺服器。

-   Shv 和健康需求伺服器可以進行比對。

    例如，NAP 健康原則伺服器上的防毒軟體 SHV 可以與防毒軟體健康需求伺服器進行比對。

協力廠商軟體廠商可透過下列方式擴充 NAP 平臺：

-   建立新方法，以評估 NAP 用戶端的健全狀況。

    協力廠商軟體廠商必須建立適用于 NAP 用戶端的 SHA、NAP 健康原則伺服器的 SHV，以及（如有需要）健康需求和補救伺服器。 如果健康需求或補救伺服器已存在，例如防毒軟體簽章散發伺服器，則只需要建立對應的 SHA 和 SHV 元件。 在某些情況下，不需要健康需求或補救伺服器。

-   建立新的方法，以強制執行網路存取或通訊的健康需求。

    協力廠商軟體廠商必須在 NAP 用戶端上建立 NAP EC。 如果強制方法使用 Windows 服務，則協力廠商軟體廠商必須建立對應的 NAP ES，以使用 RADIUS 通訊協定或在 NAP 強制端點上安裝的 NPS 服務作為 RADIUS proxy 來與 NAP 健康原則伺服器通訊。

下列各節將進一步詳細說明 NAP 伺服器端架構的元件。

## <a name="nap-enforcement-server"></a>NAP 強制伺服器

NAP 強制伺服器 (ES) 允許某些層級的網路存取或通訊，可將 NAP 用戶端的健康狀態傳遞給網路健康原則伺服器進行評估，並根據回應來強制執行有限的網路存取。

Windows Server 2008 隨附的 NAP ESs 如下所示：

-   Ipsec 受 IPsec 保護的通訊 NAP ES。

    針對受 IPsec 保護的通訊， (HRA) 的健康情況登錄授權單位、執行 Windows Server 2008 的電腦，以及從憑證授權單位單位取得健康情況憑證的 Internet Information Services (IIS) ，將 NAP 用戶端的健康狀態資訊傳遞給 NAP 健康原則伺服器。

-   Dhcp NAP ES，用於以 DHCP 為基礎的 IP 位址設定。

    DHCP NAP ES 是 DHCP 伺服器服務中的功能，使用業界標準 DHCP 訊息與 NAP 用戶端上的 DHCP NAP EC 通訊。 有限網路存取的 DHCP 強制是透過 DHCP 選項完成的。

-   終端機服務 (TS 閘道伺服器連接的 TS) 閘道 NAP ES。

針對遠端存取 VPN 和 802.1 X 驗證連線，NPS 服務中的功能會使用 NAP 用戶端與 NAP 健康原則伺服器之間的 PEAP TLV 訊息。 VPN 強制會透過套用至 VPN 連線的 IP 封包篩選器來執行。 802.1 x 強制執行于 802.1 X 網路存取裝置上，方法是將 IP 封包篩選套用至連線，或指派與受限制網路對應的 VLAN 識別碼。

## <a name="nap-administration-server"></a>NAP 管理伺服器

NAP 管理伺服器元件提供下列服務：

-   透過 NPS 服務取得 NAP ES 的 SSoHs。
-   將 SSoHs 中的 Soh 散發給 (SHV) 的適當系統健康情況驗證程式。
-   從 Shv 收集 Sohr，並將其傳遞給 NPS 服務進行評估。

## <a name="nps-service"></a>NPS 服務

RADIUS 是一種廣泛部署的通訊協定，可啟用集中式驗證、授權及帳戶處理 (Rfc) 2865 和2866的要求中所述的網路存取。 RADIUS 最初是針對撥號遠端存取而開發，現在受到無線存取點、驗證乙太網路交換器、VPN 伺服器、數位用戶線路 (DSL) 存取伺服器，以及其他網路存取伺服器的支援。

NPS 是在 Windows Server 2008 中執行 RADIUS 伺服器和 proxy。 NPS 會取代 Windows Server 2003 中 (IAS) 的網際網路驗證服務。 針對 NAP 平臺，NPS 服務包含 NAP 系統管理員伺服器元件、支援 SHV API 和可安裝的 Shv，以及設定健康原則的選項。

NPS 服務會根據來自 Shv 的 Sohr 和設定的健康情況原則，建立系統健康狀態回應的系統聲明 (SSoHR) ，指出 NAP 用戶端是否符合規範，以及是否包含來自 Shv 的 Sohr 集。

## <a name="system-health-validator-shv"></a>系統健康狀態驗證 (SHV)

SHV 會從 NAP 管理伺服器接收 SoH，並將系統健全狀況狀態資訊與所需的系統健全狀況狀態進行比較。 例如，如果 SoH 來自防毒軟體 SHA，並且包含最後一個病毒碼檔案的版本號碼，則對應的防毒軟體 SHV 可以檢查防毒軟體健康需求伺服器是否有最新的版本號碼，以驗證 NAP 用戶端的 SoH。

SHV 會將 SoHR 傳回給 NAP 管理伺服器。 SoHR 可以包含有關 NAP 用戶端上對應 SHA 如何符合目前系統健康需求的資訊。 例如，防毒軟體 SHV 傳送的 SoHR 可指示 NAP 用戶端上的防毒軟體 SHA，根據名稱或 IP 位址，向特定的防毒軟體簽章伺服器要求最新版本的防毒軟體簽章檔案。

 

 





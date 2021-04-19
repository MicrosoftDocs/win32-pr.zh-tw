---
title: 設定 RPC over HTTP 的電腦
description: 若要使用 HTTP 做為 RPC 的傳輸通訊協定，在 Internet Information Server 內執行的 RPC Proxy (IIS) 必須在伺服器程式的網路上設定。
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d1b39276633f3b827f778deef77edd5630c599
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966194"
---
# <a name="configuring-computers-for-rpc-over-http"></a>設定 RPC over HTTP 的電腦

若要使用 HTTP 做為 RPC 的傳輸通訊協定，在 Internet Information Server 內執行的 RPC Proxy (IIS) 必須在伺服器程式的網路上設定。 本節說明設定選項。 如需使用 RPC over HTTP 時最佳程式設計和設定作法的建議，請參閱 [RPC OVER Http 部署建議](rpc-over-http-deployment-recommendations.md)。 主要工作是設定 RPC Proxy，以接受 rpc over HTTP 連線，並將其轉送至 RPC over HTTP 伺服器程式。

IIS 必須先安裝在執行 RPC Proxy 的電腦上。 安裝 IIS 之後，會安裝 RPC Proxy。 您可以同時從主控台中的 [ **新增/移除 Windows 元件** ] 安裝 IIS 和 RPC Proxy。 RPC Proxy 是從 **網路服務** 安裝，在 Windows 安裝程式中則是透過 **HTTP proxy 呼叫 rpc** proxy。 如果同時安裝 IIS 和 RPC Proxy，Windows 會確保以正確的順序安裝它們。

> [!Note]  
> 安裝完成之後，如果 IIS 是在安裝過程中執行，則必須重新開機。

 

在安裝 RPC Proxy 之後，必須執行一些額外的設定工作：

1.  開啟 IIS MMC 嵌入式管理單元，並將 RPC Proxy 虛擬目錄設定為需要安全性，如 [RPC OVER HTTP 安全性](rpc-over-http-security.md)所述。 只有當您打算使用 RPC over HTTP v2 時，才需要執行此步驟。
2.  如果 IIS 未安裝憑證，則必須取得並安裝該電腦的有效憑證，才能在與 RPC Proxy 通訊時使用 SSL。 此步驟僅與 RPC over HTTP v2 相關。 由於 RPC over HTTP v1 不支援 SSL，因此 RPC over HTTP v1 可以省略此步驟。
3.  設定 **ValidPorts** 索引鍵，如 [RPC over HTTP 安全性](rpc-over-http-security.md)所述。

當這些設定工作完成時，RPC over HTTP proxy 就可以將來自 RPC over HTTP 用戶端的要求轉寄至 RPC over HTTP 伺服器。

## <a name="rpc-over-http-registry-keys"></a>RPC over HTTP 登錄機碼

本節說明在 RPC over HTTP 連線中用來設定用戶端、伺服器或 RPC Proxy 的額外登錄機碼。 通常不需要這些金鑰;這些都是為了完整性而提供。

**HKLM \\ Software \\ Microsoft \\ Rpc \\ DefaultChannelLifetime**

DWORD。 覆寫預設通道存留期。 用於用戶端和 RPC Proxy。 通道存留期是以位元組表示。 如果未指定，則會使用1GB。 僅用於 RPC over HTTP v2。 在 RPC Proxy 上變更時，必須重新開機 IIS，變更才會生效。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ClientReceiveWindow**

DWORD。 如果有的話，會指定用戶端用於從 RPC Proxy 接收之資料的接收視窗。 有效的最小值為8K。 最大值為1GB。 如果值不存在，則會使用64K。 僅用於 RPC over HTTP v2。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ InProxyReceiveWindow**

DWORD。 如果存在，則指定 RPC Proxy 用於從用戶端接收之資料的接收視窗。 有效的最小值為8K。 最大值為1GB。 如果值不存在，則會使用64K。 僅用於 RPC over HTTP v2。 變更此值時，必須重新開機 IIS，變更才會生效。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ OutProxyReceiveWindow**

DWORD。 如果有的話，會為從伺服器接收的資料指定 RPC Proxy 所使用的接收視窗。 有效的最小值為8K。 最大值為1GB。 如果值不存在，則會使用64K。 僅用於 RPC over HTTP v2。 變更此值時，必須重新開機 IIS，變更才會生效。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ServerReceiveWindow**

DWORD。 如果存在，則指定伺服器用於從 RPC Proxy 接收之資料的接收視窗。 有效的最小值為8K。 最大值為1GB。 如果值不存在，則會使用64K。 僅用於 RPC over HTTP v2。 變更此值時，必須重新開機 IIS，變更才會生效。

\-

**HKLM \\ 軟體 \\ 原則 \\ Microsoft \\ Windows NT \\ Rpc \\ MinimumConnectionTimeout**

DWORD。 如果存在，則指定用戶端和 RPC Proxy 所使用的最小連接逾時（以秒為單位）。 使用的實際時間是此值的下限，以及 IIS 閒置連接逾時時間。 如果為零，或索引鍵不存在，則會使用 IIS 閒置連接逾時。 僅用於 RPC over HTTP v2。 在 RPC Proxy 上對這個值進行變更時，必須重新開機 IIS，變更才會生效。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ UseProxyForIPAddrIfRDNSFails**

當出現並設定為非零，且以 RPC Proxy 位址提供數值 IP 位址時，RPC over HTTP 用戶端會嘗試反向名稱解析，如果失敗，則會嘗試透過 HTTP proxy 連接到 RPC Proxy。 可以用來模擬需要這類行為之安裝的 Windows NT 行為。 針對 RPC over HTTP v2 略過。 只有在使用 RPC over HTTP v1 時才會使用。 只有在 Windows 2000 Service Pack 3 (SP3) 和更新版本才支援。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RpcProxy \\ AllowAnonymous**

DWORD。 如果不存在或設為零，RPC Proxy 會檢查連線是否已通過驗證，以及是否有安全 (SSL 或其他形式的加密) 。 如果任一個為 false，則會拒絕連接。 如果這個值包含非零的，則會允許匿名和非加密的連接。 這項設定是任何虛擬目錄設定的新增功能。 例如，如果虛擬目錄層級上已停用匿名存取，但 **AllowAnonymous** 不是零，則在 IIS 層級仍會封鎖匿名存取。 僅用於 rpc over HTTP v2 中的 RPC Proxy。 在 RPC Proxy 上對這個值進行變更時，必須重新開機 IIS，變更才會生效。

> [!WARNING]
> 基於安全性考慮，Microsoft 強烈建議您不要在生產系統上設定 **AllowAnonymous** 值。 應設定此金鑰的唯一原因是要在沒有外部存取的封閉網路上進行測試。 任何連線到網際網路的系統，以及將 **AllowAnonymous** 機碼設定為非零值的 RPC Proxy，都很容易受到攻擊。

 

 

 





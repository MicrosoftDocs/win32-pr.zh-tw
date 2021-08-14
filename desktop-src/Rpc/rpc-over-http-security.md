---
title: RPC over HTTP 安全性
description: 除了標準 RPC 安全性之外，RPC over HTTP 還提供三種類型的安全性，這會導致 rpc over HTTP 流量受到 RPC 的保護，然後由 RPC over HTTP 所提供的通道機制雙向保護。
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f1ebd5a7198a2b2ccae7703b92011bbd45b037db2f7ef8eb116e28ef06d8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926128"
---
# <a name="rpc-over-http-security"></a>RPC over HTTP 安全性

除了標準 RPC 安全性之外，RPC over HTTP 還提供三種類型的安全性，這會導致 rpc over HTTP 流量受到 RPC 的保護，然後由 RPC over HTTP 所提供的通道機制雙向保護。 如需標準 RPC 安全性機制的說明，請參閱 [安全性](security.md)。 RPC over HTTP 通道機制以下列方式新增至一般 RPC 安全性：

-   透過 IIS (提供安全性，僅適用于 RPC over HTTP v2) 。
-   提供 SSL 加密和 RPC Proxy 驗證 (相互驗證) 。 也僅適用于 RPC over HTTP v2。
-   提供 RPC Proxy 層級的限制，以決定允許伺服器網路上的哪些電腦接收 RPC over HTTP 呼叫。

下列各節將詳細說明這三項安全性功能。

## <a name="iis-authentication"></a>IIS 驗證

RPC over HTTP 可以利用 IIS 的一般驗證機制。 您可以使用 IIS MMC 嵌入式管理單元中 [預設的網站] 底下的 [Rpc] 節點來設定 RPC Proxy 的虛擬目錄：

![螢幕擷取畫面，顯示 IIS MMC 嵌入式管理單元中預設網站底下的 [Rpc] 節點。](images/rpc-http-1.png)

您可以將 IIS 設定為停用匿名存取，並要求對 RPC Proxy 的虛擬目錄進行驗證。 若要這樣做，請以滑鼠右鍵按一下 Rpc 節點，然後選取 [ **屬性**]。 選取 [**目錄安全性**] 索引標籤，然後按一下 [**驗證和存取控制**] 群組中的 [**編輯**] 按鈕，如下所示：

![顯示 [RPC 屬性] 對話方塊的螢幕擷取畫面。](images/rpc-http-2.png)

雖然您可以使用 RPC over HTTP，即使 RPC Proxy 虛擬目錄允許匿名存取，但基於安全性考慮，Microsoft 強烈建議您停用對該虛擬目錄的匿名存取。 相反地，RPC over HTTP 會啟用基本驗證，Windows 整合式驗證或兩者。 請記住，只有 rpc over HTTP v2 能夠針對需要基本或 Windows 整合式驗證的 rpc Proxy 進行驗證;如果停用不 **允許匿名存取**，則 RPC over HTTP v1 將無法連接。 由於 RPC over HTTP v2 是更安全且穩固的執行，因此使用支援它的 Windows 版本將可提升安裝的安全性。

> [!Note]  
> 根據預設，RPC proxy 虛擬目錄會標示為允許匿名存取。 不過，rpc over HTTP v2 的 RPC proxy 會拒絕預設未驗證的要求。

 

## <a name="traffic-encryption"></a>流量加密

RPC over HTTP 可使用 SSL 加密 RPC over HTTP 用戶端與 RPC proxy 之間的流量。 RPC proxy 與 RPC over HTTP 伺服器之間的流量會使用一般 RPC 安全性機制進行加密，而且不會使用 SSL (即使用戶端和 RPC proxy 之間的 SSL 是) 選擇的。 這是因為流量的部分會在組織的網路內和防火牆後方進行。

RPC over HTTP 用戶端與 RPC proxy 之間的流量（通常透過網際網路傳輸）除了針對 RPC 選擇的加密機制之外，還可以使用 SSL 進行加密。 在此情況下，路由的網際網路部分上的流量會變成雙向加密。 如果 RPC proxy 或周邊網路中的其他電腦遭到入侵，則透過 RPC proxy 加密流量會提供次要防禦。 因為 RPC proxy 無法將次要加密層解密，所以 RPC proxy 無法存取所傳送的資料。 如需詳細資訊，請參閱[RPC over HTTP 部署建議](rpc-over-http-deployment-recommendations.md)。 SSL 加密僅適用于 RPC over HTTP v2。

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>限制對特定電腦的 RPC over HTTP 呼叫

IIS 安全性設定是以允許的電腦和埠範圍為基礎。 使用 RPC over HTTP 的功能是由執行 IIS 和 RPC proxy 之電腦上的兩個登錄專案所控制。 第一個專案是切換 RPC proxy 功能的旗標。 第二個是選擇性的電腦清單，可供 proxy 轉寄 RPC 呼叫。

根據預設，用戶端會透過 HTTP 呼叫將 RPC proxy 連線至通道 RPC over HTTP 呼叫，而不能存取任何 RPC 伺服器進程，除了 rpc over HTTP 伺服器進程（在與 RPC proxy 相同的電腦上執行）。 如果啟用的旗標未定義或設為零值，IIS 就會停用 RPC proxy。 如果已定義啟用的旗標並設定為非零值，則用戶端可以在執行 IIS 的電腦上連接到 RPC over HTTP 伺服器。 若要讓用戶端透過另一部電腦上的 RPC over HTTP 伺服器進程進行通道處理，您必須將登錄專案新增至 IIS 電腦的 RPC over HTTP 伺服器清單。

RPC 伺服器無法接受 RPC over HTTP 呼叫，除非它們特別要求 RPC 在 RPC over HTTP 上接聽。

下列範例示範如何設定登錄，以允許用戶端連接到網際網路上的伺服器：

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

**ValidPorts** 專案是 REG \_ SZ 專案，其中包含可允許 IIS RPC proxy 轉寄 rpc 呼叫的電腦清單，以及其應該用來連線到 rpc 伺服器的埠。 REG \_ SZ 專案採用下列格式： Rosco： 593;Rosco： 2000-8000; 資料 \* ：4000-8000。

在此範例中，IIS 可以在埠593和2000到8000的情況下，將 RPC over HTTP 呼叫轉送至伺服器 "Rosco"。 它也可以將呼叫傳送至名稱開頭為 "Data" 的任何伺服器。 它會連線到埠4000到8000。 此外，在將流量轉送至 RPC over HTTP 伺服器上的指定埠之前，RPC proxy 會使用接聽該埠的 RPC 服務來執行特殊的封包交換，以確認它是否願意透過 HTTP 接受要求。

如需根據這些範例設定的範例，如果 RPC 服務在伺服器 "Data1" 上接聽埠4500，但是未以 _ * ncacn HTTP * * 呼叫其中一個 [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)函式 \_ ，則會拒絕要求。 此行為可針對因設定錯誤而在開啟的埠上接聽的伺服器，提供額外的保護。除非伺服器特別要求在 RPC over HTTP 上接聽，否則它不會接收來自防火牆外部的呼叫。

**ValidPorts** 索引鍵中的專案必須與用戶端要求的 RPC over HTTP 伺服器完全相符， (不區分大小寫) 。 為了簡化處理，RPC proxy 不會執行 RPC over HTTP 用戶端所提供之名稱的標準化。 因此，如果用戶端要求 rosco.microsoft.com，而且在 **ValidPorts** 中只包含 rosco，則 RPC proxy 將不會與名稱相符，即使兩個名稱可能會參考相同的電腦也一樣。 此外，如果 Rosco 的 IP 位址是66.77.88.99，而且用戶端要求66.77.88.99，但 **ValidPorts** 機碼只包含 Rosco，則 RPC proxy 將拒絕該連接。 如果用戶端可能會根據名稱或 IP 位址要求 RPC over HTTP 伺服器，請在 **ValidPorts** 金鑰中插入這兩者。

> [!Note]  
> 雖然 RPC 已啟用 IPv6，但 RPC proxy 不支援 **ValidPorts** 金鑰中的 ipv6 位址。 如果使用 IPv6 來連接 RPC proxy 和 RPC over HTTP 伺服器，就只能使用 DNS 名稱。

 

IIS 會在啟動時讀取 **已啟用** 和 **ValidPorts** 的登錄專案。 此外，RPC over HTTP 會讀取大約每5分鐘的 **ValidPorts** 金鑰內容。 如果 **ValidPorts** 專案已變更，則會在5分鐘內執行變更。

**RPC OVER HTTP v1：** WEB 服務必須使用網際網路 Service Manager 停止並重新啟動，才能執行登錄專案中的新值。

 

 





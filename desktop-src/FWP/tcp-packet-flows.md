---
title: TCP 封包流程
description: 在一般的 TCP 會話期間，Windows 篩選平台 (WFP) 篩選引擎層級的順序。
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932385"
---
# <a name="tcp-packet-flows"></a>TCP 封包流程

本節說明在一般 TCP 會話期間，Windows 篩選平台 (WFP) 篩選引擎的各層的順序。

> [!Note]  
> IPv6 的 TCP 封包流程遵循與 IPv4 相同的模式。

 

> [!Note]  
> 非 TCP 封包流程遵循的模式與 [UDP 封包流程](udp-packet-flows.md)相同。

 

## <a name="tcp-connection-establishment"></a>TCP 連接建立

<dl> 伺服器 (接收者) 執行被動開啟

-   系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4
-   接聽： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V4

  
用戶端 (傳送者) 執行 Active Open

-   系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4
-   connect： FWPM \_ LAYER \_ ALE \_ CONNECT 重新 \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   connect： FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   SYN： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4
-   SYN： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

  
伺服器

-   SYN： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   SYN： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4
-   SYN： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4
-   SYN-ACK： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4
-   SYN-ACK： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

  
用戶端

-   SYN-ACK： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   SYN-ACK： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4
-   ACK： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4
-   ACK： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

  
伺服器

-   ACK： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   ACK： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4
-   接聽完成。 伺服器可以執行接受。

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>收到的 TCP SYN 未接聽埠或通訊協定

伺服器 (接收者) 

-   SYN： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   SYN： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4 \_ 捨棄
-   RST： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4
-   RST： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

> [!Note]  
> 具有特定錯誤狀況的傳輸捨棄時，不會指出 TCP SYN （不含端點）。 在傳輸捨棄時封鎖此封包，使堆疊不會將對應的事件傳送 (RST) 。 如需隱形模式篩選的範例，請參閱 [防止埠掃描](preventing-port-scanning.md)。

 

## <a name="data-transmitted-over-a-tcp-connection"></a>透過 TCP 連接傳輸的資料

<dl> 用戶端 (寄件者) 

-   傳送
-   資料： FWPM \_ 圖層 \_ 串流 \_ V4
-   TCP 區段： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4
-   IP 資料包： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

  
伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   資料： FWPM \_ 圖層 \_ 串流 \_ V4
-   資料可供讀取。

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>成功重新授權 TCP 封包

伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4
-   data： FWPM \_ LAYER \_ STREAM \_ V4 (輸入) 

## <a name="failed-reauthorization-of-a-tcp-packet"></a>TCP 封包的重新授權失敗

伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4
-   TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ ACCEPT \_ V4 \_ 捨棄

## <a name="tcp-connection-termination"></a>TCP 連接終止

任何 WFP 層都不會指出 TCP 連接終止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 





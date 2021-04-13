---
title: UDP 封包流程
description: 在典型的 UDP 會話期間，會在 Windows 篩選平台 (WFP) 篩選引擎層級的順序。
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301532"
---
# <a name="udp-packet-flows"></a>UDP 封包流程

本節說明在一般的 UDP 會話期間，Windows 篩選平台 (WFP) 篩選引擎層級的順序。

> [!Note]  
> IPv6 的 UDP 封包流程遵循與 IPv4 相同的模式。

 

> [!Note]  
> 所有的非 TCP 封包流程都會遵循與 UDP 封包流程相同的模式。

 

## <a name="udp-connection-establishment"></a>建立 UDP 連接

<dl> 伺服器 (接收者) 執行被動開啟

-   系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4

  
用戶端 (傳送者) 執行 Active Open

-   系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4
-   sendto： FWPM \_ LAYER \_ ALE \_ CONNECT 重新 \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) 
-   sendto： FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4
-   data： FWPM \_ LAYER \_ \_ 資料包資料 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4
-   IP 資料包： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4

  
伺服器

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4
-   data： FWPM \_ LAYER \_ \_ 資料包資料 \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>收到的 UDP 訊息沒有接聽埠或通訊協定

伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   IP 資料包： FWPM \_ 層 \_ 輸入 \_ IPPACKET \_ V4 \_ 捨棄
-   無法連線到 ICMP 目的地： FWPM \_ 層 \_ 輸出 \_ ICMP \_ 錯誤 \_ V4
-   無法連線到 ICMP 目的地： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4
-   無法連線到 ICMP 目的地： FWPM \_ 圖層 \_ 輸出 \_ IPPACKET \_ V4

> [!Note]  
> 具有特定錯誤狀況的 IPPACKET 捨棄時，不會指出 UDP 與沒有端點。 在 IPPACKET 捨棄時封鎖此封包，使堆疊不會將對應的事件傳送 (ICMP 錯誤) 。

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>成功重新授權 UDP 封包

伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ \_ 資料包資料 \_ V4 (輸入) 

## <a name="failed-reauthorization-of-a-udp-packet"></a>UDP 封包的重新授權失敗

伺服器 (接收者) 

-   IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4
-   UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4
-   UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4 \_ 捨棄

## <a name="udp-connection-termination"></a>UDP 連接終止

任何 WFP 層都不會指出 UDP 連接終止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 





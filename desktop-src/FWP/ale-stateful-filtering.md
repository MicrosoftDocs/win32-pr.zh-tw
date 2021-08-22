---
title: ALE 具狀態篩選
description: 在應用層強制安裝的篩選 (Windows 篩選平台的 ALE) 層 (WFP) 執行具狀態網路篩選。
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbcb0517bb1e48c337f0ffd9589a1f39a3e4239aa0b3971dc81a71b402891f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388908"
---
# <a name="ale-stateful-filtering"></a>ALE 具狀態篩選

在應用層強制安裝的篩選 (Windows 篩選平台的 ALE) 層 (WFP) 執行具狀態網路篩選。 *Ale 流程* 是用來做為 ale 可設定狀態的篩選基礎。

ALE 流程是根據來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定，將網路流量分組的方式。 ALE 流程可以是泛型，也就是一或多個描述項可能符合 (或萬用字元) 的所有專案 \* 。 例如，一般的 UDP ALE 流程將會描述為來源 IP 位址 = \* 、目的地 Ip 位址 = \* 、來源埠 = \* 、目的地埠 = \* 和通訊協定 = UDP。

授權連線之後 (輸入連線會在 [**FWPM \_ 層 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層以及 **FWPM \_ 層 \_ ale \_ auth auth \_ CONNECT \_ v {4 \| 6}** 層) 的輸出連線，就會建立一個 ale 流程，如此一來，就會自動允許屬於相同 ale 流程的所有封包、輸入和輸出。 由於原則變更可能需要封鎖先前允許的連線，因此在發生原則變更時，必須 [重新授權](ale-re-authorization.md) ALE 流程。

ALE 具狀態篩選只會將屬於 ALE 流程的第一個封包分類，以大幅減少所需分類的數目。 相較之下，非具狀態的篩選需要分類流經網路的每個封包。

ALE 流程具有相關聯的方向，也就是流程第一個封包的方向。 藉由允許輸入起始的連接與輸出起始的連接具有不同的原則，即可提供更有彈性的原則。

## <a name="tcp-ale-flow"></a>TCP ALE Flow

TCP 流量的 ALE 流程是由 TCP/IP (來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定) 的五個元組所識別。

TCP ALE 流程與連線的 TCP 通訊端具有相同的存留期。 連接的 TCP 通訊端可以是使用 [**connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) 建立的通訊端，或是 [**接受 ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) 呼叫所建立的通訊端。

ALE 會維護 TCP ALE 流程與 TCP 控制區塊之間的一對一關聯性， (TCB) 。

## <a name="udp-ale-flow"></a>UDP ALE Flow

> [!Note]  
> 非 TCP 或 ICMP 的通訊協定會視為 UDP。

 

UDP 流量的 ALE 流程是由 TCP/IP (來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定) 的五個元組所識別。

UDP ALE 流程是根據 UDP 通訊端建立，它代表應用程式正在通訊的遠端對等。 遠端對等是由 (目的地 IP 位址和目的地埠) 元組所識別。

UDP 通訊端和與其交談的遠端對等之間，有一對多關聯性。

當本機 UDP 通訊端關閉時，將會刪除與其相關聯的所有 ALE 流程。

在沒有通訊端關閉的情況下，UDP 單播 ALE 流程具有 [可](ale-flow-customization.md) 設定的閒置 timeout，預設為60秒。 如果在此視窗內沒有傳送或接收任何封包，則會刪除 ALE 流程。 當整個系統的 ALE 流程數目達到特定閾值時，此預設的超時時間會逐漸縮短。

## <a name="icmp-ale-flow"></a>ICMP ALE Flow

ICMP 流量的 ALE 流程是由六個元組所識別 (來源 IP 位址、目的地 IP 位址、ICMP 類型、ICMP 代碼、通訊協定和 ICMP 識別碼) 。 ICMP 識別碼只是針對 ICMP echo/回復流量的 ALE 流程的一部分。

在沒有通訊端關閉的情況下，ICMP 單播 ALE 流程具有 [可](ale-flow-customization.md) 設定的閒置 timeout，預設為60秒。 如果在此視窗內沒有傳送或接收任何封包，則會刪除 ALE 流程。 當整個系統的 ALE 流程數目達到特定閾值時，此預設的超時時間會逐漸縮短。

只有 ICMP 非錯誤訊息會指出至 ALE 層。 Icmp 錯誤訊息可以在 ICMP 錯誤層級進行檢查 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用層強制 (ALE) ](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE 層](ale-layers.md)
</dt> <dt>

[ALE 多播/廣播流量](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[ALE Flow 自訂](ale-flow-customization.md)
</dt> <dt>

[TCP 封包流程](tcp-packet-flows.md)
</dt> <dt>

[UDP 封包流程](udp-packet-flows.md)
</dt> <dt>

[Winsock 函數](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 
---
description: TCP/IP 具有特性，可讓通訊協定以其標準化的實作為需求來運作。
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: TCP/IP 特性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f720dac1157149fe34da1b6bcbc08928654f268c7ac3e32b2e22599ae43cb701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733418"
---
# <a name="tcpip-characteristics"></a>TCP/IP 特性

TCP/IP 具有特性，可讓通訊協定以其標準化的實作為需求來運作。 這些特性可以與導致效能不佳的開發選項結合。 這些 TCP/IP 特性對應用程式所造成的影響，取決於應用程式是交易式或串流處理。

交易式應用程式會受到連接建立和終止所需的額外負荷所影響。 例如，每次在乙太網路上建立連接時，都必須傳送大約60個位元組的三個封包，而且交換必須有大約一個 RTT。 當連線終止時，會交換四封封包。 這適用于每個連接;開啟和關閉連接的應用程式通常會在每次發生時產生此額外負荷。

TCP/IP 的另一個層面是 *緩慢啟動*，這會在每次建立連接時進行。 「緩慢啟動」是在收到這些區段的認可之前，可傳送的資料區段數目的人工限制。 「緩慢啟動」的設計目的是要限制網路擁塞。 建立透過乙太網路的連線時，不論接收器的視窗大小為何，4 KB 傳輸最多可能需要 3-4 RTT，因為速度很慢。

稱為 Nagle 演算法的 TCP/IP 優化也可以限制連接上的資料傳送速率。 Nagle 演算法的設計目的是為了降低傳送少量資料的應用程式（例如 Telnet）（一次傳送一個字元）的通訊協定額外負荷。 堆疊會等待應用程式中的更多資料或認可，然後再繼續進行，而不是立即傳送具有大量標頭和少量資料的封包。

延遲的通知（通常稱為 *延遲 ACK*）也會設計為 tcp/ip，以在從接收端應用程式取得傳回資料時，能夠更有效率地附掛通知。 可惜的是，如果這項資料不存在，而且傳送端正在等候通知，則每個傳送大約200毫秒的延遲可能會發生。

當 TCP 連接關閉時，在起始關閉的節點上的連線資源會進入等候狀態，稱為「等待時間」，以防止在網路中的重複封包損毀時防止資料損毀。 這可確保兩端都已完成連接。 當應用程式經常開啟和關閉連接時，這可能會導致資源耗盡，例如 RAM 和埠。

除了受到延遲的 ACK 和其他擁塞規避配置的影響之外，串流應用程式也可能會受到接收端上太小的預設接收視窗大小所影響。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式行為](application-behavior-2.md)
</dt> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle 演算法](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 




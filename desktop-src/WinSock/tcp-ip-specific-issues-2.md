---
description: 某些程式設計技術會遇到與 TCP/IP 執行連結的效能問題。
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: TCP/IP 特定問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e63bf20f545106d6b94ad4628c3fe4fe779136bacd5c8bd1a88ec32da1f233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993257"
---
# <a name="tcpip-specific-issues"></a>TCP/IP 特定問題

某些程式設計技術會遇到與 TCP/IP 執行連結的效能問題。 這類效能問題不會建議 TCP/IP 沒有效率或效能瓶頸;相反地，當無法理解 TCP/IP 作業時，就會看到這些問題。

下列問題指出 TCP/IP 作業與網路應用程式開發選擇的組合會導致效能不佳的常見案例。

-   連線繁重的應用程式。

    某些應用程式會為每個交易具現化新的 TCP 連接。 TCP 連線建立需要一些時間、額外的 RTTs，而且會受到緩慢的啟動。 此外，關閉的連線會受時間等候，這會耗用系統資源。

    連線繁重的應用程式大多很常見，因為它們很容易建立;測試和錯誤處理非常簡單。 在持續連線上偵測錯誤可能需要相當多的程式碼和精力，因此有時不會完成。

    重複使用 TCP 連線來解決這種情況。 這可能會導致透過 TCP 連接進行序列化，除非交易是透過多個連接進行多工處理。 如果採取這種方式，連接數目應限制為兩個，而且需要應用層框架和先進的錯誤處理。

-   零長度的傳送緩衝區和封鎖傳送。

    藉由使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數設定傳送緩衝區來關閉緩衝處理 (如此 \_ SNDBUF) 為零，就類似于關閉磁碟快取。 將傳送緩衝區設定為零併發出封鎖傳送時，應用程式有50% 的機會達到200毫秒的延遲通知。

    除非您已考慮所有網路環境的影響，否則請勿關閉傳送緩衝處理。 其中一個例外狀況：使用重迭 i/o 的串流資料應該將傳送緩衝區設定為零。

-   傳送-傳送-接收程式設計模型。

    將應用程式結構化以執行傳送傳送接收，會增加您遇到 Nagle 演算法的機率，而導致 RTT 的延遲 + 200 毫秒。 如果最後一次傳送小於 TCP 最大區段大小 (MSS、單一資料包中的最大資料) ，可能會遇到 Nagle 演算法。 MSS 可以是較大的值 (64K 在 IPv4 中，甚至更大的 IPv6) ，因此不會計入通常小的 MSS。 更好的選擇是使用 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 或 **memcpy** 函式，將這兩個傳送合併成單一傳送。

-   大量的同時連線。

    除了特殊用途的應用程式之外，並行連接不應超過二。 超過兩個並行連接會導致資源浪費。 理想的規則是有最多四個短暫的連接，或每個目的地有兩個持續連線。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式行為](application-behavior-2.md)
</dt> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle 演算法](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 




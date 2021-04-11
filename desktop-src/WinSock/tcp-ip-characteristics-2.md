---
description: TCP/IP 具有特性，可讓通訊協定以其標準化的實作為需求來運作。
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: TCP/IP 特性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849844"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="6514e-103">TCP/IP 特性</span><span class="sxs-lookup"><span data-stu-id="6514e-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="6514e-104">TCP/IP 具有特性，可讓通訊協定以其標準化的實作為需求來運作。</span><span class="sxs-lookup"><span data-stu-id="6514e-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="6514e-105">這些特性可以與導致效能不佳的開發選項結合。</span><span class="sxs-lookup"><span data-stu-id="6514e-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="6514e-106">這些 TCP/IP 特性對應用程式所造成的影響，取決於應用程式是交易式或串流處理。</span><span class="sxs-lookup"><span data-stu-id="6514e-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="6514e-107">交易式應用程式會受到連接建立和終止所需的額外負荷所影響。</span><span class="sxs-lookup"><span data-stu-id="6514e-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="6514e-108">例如，每次在乙太網路上建立連接時，都必須傳送大約60個位元組的三個封包，而且交換必須有大約一個 RTT。</span><span class="sxs-lookup"><span data-stu-id="6514e-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="6514e-109">當連線終止時，會交換四封封包。</span><span class="sxs-lookup"><span data-stu-id="6514e-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="6514e-110">這適用于每個連接;開啟和關閉連接的應用程式通常會在每次發生時產生此額外負荷。</span><span class="sxs-lookup"><span data-stu-id="6514e-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="6514e-111">TCP/IP 的另一個層面是 *緩慢啟動*，這會在每次建立連接時進行。</span><span class="sxs-lookup"><span data-stu-id="6514e-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="6514e-112">「緩慢啟動」是在收到這些區段的認可之前，可傳送的資料區段數目的人工限制。</span><span class="sxs-lookup"><span data-stu-id="6514e-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="6514e-113">「緩慢啟動」的設計目的是要限制網路擁塞。</span><span class="sxs-lookup"><span data-stu-id="6514e-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="6514e-114">建立透過乙太網路的連線時，不論接收器的視窗大小為何，4 KB 傳輸最多可能需要 3-4 RTT，因為速度很慢。</span><span class="sxs-lookup"><span data-stu-id="6514e-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="6514e-115">稱為 Nagle 演算法的 TCP/IP 優化也可以限制連接上的資料傳送速率。</span><span class="sxs-lookup"><span data-stu-id="6514e-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="6514e-116">Nagle 演算法的設計目的是為了降低傳送少量資料的應用程式（例如 Telnet）（一次傳送一個字元）的通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="6514e-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="6514e-117">堆疊會等待應用程式中的更多資料或認可，然後再繼續進行，而不是立即傳送具有大量標頭和少量資料的封包。</span><span class="sxs-lookup"><span data-stu-id="6514e-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="6514e-118">延遲的通知（通常稱為 *延遲 ACK*）也會設計為 tcp/ip，以在從接收端應用程式取得傳回資料時，能夠更有效率地附掛通知。</span><span class="sxs-lookup"><span data-stu-id="6514e-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="6514e-119">可惜的是，如果這項資料不存在，而且傳送端正在等候通知，則每個傳送大約200毫秒的延遲可能會發生。</span><span class="sxs-lookup"><span data-stu-id="6514e-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="6514e-120">當 TCP 連接關閉時，在起始關閉的節點上的連線資源會進入等候狀態，稱為「等待時間」，以防止在網路中的重複封包損毀時防止資料損毀。</span><span class="sxs-lookup"><span data-stu-id="6514e-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="6514e-121">這可確保兩端都已完成連接。</span><span class="sxs-lookup"><span data-stu-id="6514e-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="6514e-122">當應用程式經常開啟和關閉連接時，這可能會導致資源耗盡，例如 RAM 和埠。</span><span class="sxs-lookup"><span data-stu-id="6514e-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="6514e-123">除了受到延遲的 ACK 和其他擁塞規避配置的影響之外，串流應用程式也可能會受到接收端上太小的預設接收視窗大小所影響。</span><span class="sxs-lookup"><span data-stu-id="6514e-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6514e-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="6514e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6514e-125">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="6514e-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="6514e-126">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="6514e-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="6514e-127">Nagle 演算法</span><span class="sxs-lookup"><span data-stu-id="6514e-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 




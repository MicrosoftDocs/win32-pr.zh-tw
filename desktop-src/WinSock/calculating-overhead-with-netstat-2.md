---
description: 使用 Netstat 計算額外負荷
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: 使用 Netstat 計算額外負荷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998239"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="40624-103">使用 Netstat 計算額外負荷</span><span class="sxs-lookup"><span data-stu-id="40624-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="40624-104">使用 Netstat 計算額外負荷應該在無訊息的網路上執行，以避免其他網路流量扭曲資料，例如廣播或多播流量。</span><span class="sxs-lookup"><span data-stu-id="40624-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="40624-105">**使用 Netstat 計算應用程式的網路額外負荷**</span><span class="sxs-lookup"><span data-stu-id="40624-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="40624-106">使用 Netstat 取出目前的介面統計資料。</span><span class="sxs-lookup"><span data-stu-id="40624-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="40624-107">執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="40624-107">Execute the application.</span></span>
3.  <span data-ttu-id="40624-108">使用 Netstat 再次取得介面統計資料。</span><span class="sxs-lookup"><span data-stu-id="40624-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="40624-109">計算兩個 Netstat 度量之間接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="40624-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="40624-110">範例</span><span class="sxs-lookup"><span data-stu-id="40624-110">Example</span></span>

<span data-ttu-id="40624-111">下列範例示範這些步驟，使用 TTCP 傳送10個位元組的資料，一次一個位元組。</span><span class="sxs-lookup"><span data-stu-id="40624-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="40624-112">首先，會計算應用程式的理論負擔。</span><span class="sxs-lookup"><span data-stu-id="40624-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="40624-113">針對此測試，所有封包都是60位元組 (Ethernet 最小) 。</span><span class="sxs-lookup"><span data-stu-id="40624-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="40624-114">這項傳輸需要三封封包來設定連線、10個數據封包、10個認可封包 (延遲的 ACK 幾乎每次都會觸發) ，而四個封包則可正常地關閉連接。</span><span class="sxs-lookup"><span data-stu-id="40624-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="40624-115">這相當於27個60位元組的封包，或1620個位元組 (3 + 4 + 10 + 10) \* 60 = 1620) 。</span><span class="sxs-lookup"><span data-stu-id="40624-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="40624-116">由於只會傳送10個位元組的資料，因此額外負荷為1610個位元組，超過99% 的通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="40624-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="40624-117">命令</span><span class="sxs-lookup"><span data-stu-id="40624-117">Commands</span></span>

<span data-ttu-id="40624-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="40624-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="40624-119">**ttcp-t-h0-D-l1-n10-p9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="40624-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="40624-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="40624-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="40624-121">計算</span><span class="sxs-lookup"><span data-stu-id="40624-121">Calculations</span></span>

<span data-ttu-id="40624-122">**已傳送：** 816 位元組</span><span class="sxs-lookup"><span data-stu-id="40624-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="40624-123">**收到：** 674 位元組</span><span class="sxs-lookup"><span data-stu-id="40624-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="40624-124">**位元組總計：** 1490</span><span class="sxs-lookup"><span data-stu-id="40624-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="40624-125">**使用者位元組：** 10</span><span class="sxs-lookup"><span data-stu-id="40624-125">**User bytes:** 10</span></span>

<span data-ttu-id="40624-126">**額外負荷：** 1480/1490 = 99.3%</span><span class="sxs-lookup"><span data-stu-id="40624-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="40624-127">\* \* Goodput： \* \* = 5 個位元組/秒 (或40位/秒) </span><span class="sxs-lookup"><span data-stu-id="40624-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="40624-128">因為 Netstat 值中未納入填補位元組，所以傳送的實際位元組數不符合理論值。</span><span class="sxs-lookup"><span data-stu-id="40624-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40624-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="40624-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40624-130">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="40624-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="40624-131">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="40624-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 




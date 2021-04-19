---
description: 在此版本的範例程式中，我們進行了幾項明顯的變更，以改善效能。
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 修訂1：清除明顯的
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983570"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="c9fe3-103">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="c9fe3-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="c9fe3-104">在此版本的範例程式中，我們進行了幾項明顯的變更，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="c9fe3-105">這一版的程式碼遠不受效能調整，但這是一個很好的遞增步驟，可讓您檢查漸進式更佳方法的效果。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="c9fe3-106">此應用程式範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="c9fe3-107">請勿在您的應用程式中使用此程式碼範例;這僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="c9fe3-108">此版本中的變更</span><span class="sxs-lookup"><span data-stu-id="c9fe3-108">Changes in this Version</span></span>

<span data-ttu-id="c9fe3-109">此版本會反映下列變更：</span><span class="sxs-lookup"><span data-stu-id="c9fe3-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="c9fe3-110">已移除 SNDBUF = 0。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="c9fe3-111">因為未緩衝的傳送和延遲的通知已移除，所以200毫秒的延遲。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="c9fe3-112">已移除傳送-傳送-接收行為。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="c9fe3-113">這種變更可消除由於 Nagle 和延遲的 ACK 互動所造成的200毫秒延遲。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="c9fe3-114">移除位元組由小到小的假設。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-114">Removed little-endian assumption.</span></span> <span data-ttu-id="c9fe3-115">位元組現在依序排列。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="c9fe3-116">剩餘問題</span><span class="sxs-lookup"><span data-stu-id="c9fe3-116">Remaining Problems</span></span>

<span data-ttu-id="c9fe3-117">在此版本中，仍會發生下列問題：</span><span class="sxs-lookup"><span data-stu-id="c9fe3-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="c9fe3-118">應用程式仍會以繁重的連接。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-118">The application is still connect heavy.</span></span> <span data-ttu-id="c9fe3-119">由於已移除 600 + 毫秒的延遲，因此應用程式現在會達到每秒12個連接的持續速率。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="c9fe3-120">許多並行連接現在都會發生問題。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="c9fe3-121">應用程式仍然是 fat;未變更的儲存格仍會傳播到伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="c9fe3-122">應用程式仍然表現不佳的串流;3位元組傳送仍是小型傳送。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="c9fe3-123">應用程式現在會傳送2個位元組/RTT，在直接連線的乙太網路上等於 4 KB/s。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="c9fe3-124">這並不太快，但時間等候可能會先造成問題。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="c9fe3-125">額外負荷會降至99.3%，但仍不是很好的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="c9fe3-126">關鍵效能計量</span><span class="sxs-lookup"><span data-stu-id="c9fe3-126">Key Performance Metrics</span></span>

<span data-ttu-id="c9fe3-127">下列關鍵效能計量是以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="c9fe3-128">請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。</span><span class="sxs-lookup"><span data-stu-id="c9fe3-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="c9fe3-129">此版本會反映下列效能計量：</span><span class="sxs-lookup"><span data-stu-id="c9fe3-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="c9fe3-130">儲存格時間-2 × RTT</span><span class="sxs-lookup"><span data-stu-id="c9fe3-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="c9fe3-131">Goodput-2 個位元組/RTT</span><span class="sxs-lookup"><span data-stu-id="c9fe3-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="c9fe3-132">通訊協定額外負荷-99.3%</span><span class="sxs-lookup"><span data-stu-id="c9fe3-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9fe3-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9fe3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9fe3-134">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="c9fe3-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-135">網路術語</span><span class="sxs-lookup"><span data-stu-id="c9fe3-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-136">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="c9fe3-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-137">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="c9fe3-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-138">修訂3：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="c9fe3-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-139">未來的改進</span><span class="sxs-lookup"><span data-stu-id="c9fe3-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 




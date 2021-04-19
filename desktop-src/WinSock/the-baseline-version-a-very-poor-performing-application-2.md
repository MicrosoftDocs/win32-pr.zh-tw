---
description: 在 Windows 通訊端中執行效能不佳的應用程式的基準版本 (Winsock) 。
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 基準版本：執行效能不佳的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971844"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="a5b1b-103">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="a5b1b-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="a5b1b-104">用來計算更新的初始、不良執行程式碼範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="a5b1b-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="a5b1b-105">為了簡單起見，下列範例中沒有錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="a5b1b-106">任何實際執行應用程式一律會檢查傳回值。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="a5b1b-107">應用程式的前幾個範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="a5b1b-108">請勿在您的應用程式中使用這些程式碼範例;它們僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="a5b1b-109">在此狀態下，應用程式會有最差的可能網路效能。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="a5b1b-110">這個範例應用程式版本的問題包括：</span><span class="sxs-lookup"><span data-stu-id="a5b1b-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="a5b1b-111">應用程式很多對話。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-111">The application is chatty.</span></span> <span data-ttu-id="a5b1b-112">每個交易太小，不需要逐一更新資料格。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="a5b1b-113">即使可以同時更新資料格，仍會將交易嚴格序列化。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="a5b1b-114">傳送緩衝區會設定為零，而且應用程式會針對每個傳送產生200毫秒的延遲，每個資料格三次。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="a5b1b-115">應用程式非常大量連接，每個資料格連接一次。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="a5b1b-116">由於每一筆交易的等候時間狀態超過600毫秒，因此應用程式會根據指定目的地的每秒連線數限制。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="a5b1b-117">應用程式為 fat;許多交易對伺服器狀態沒有任何影響，因為許多資料格不會因為更新而變更。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="a5b1b-118">應用程式表現不良的串流;小型傳送會耗用大量的 CPU 和 RAM。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="a5b1b-119">應用程式針對其傳送採用位元組由小到大的標記法。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="a5b1b-120">這對目前的 Windows 平臺是自然的假設，但長期的程式碼可能會有危險。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="a5b1b-121">關鍵效能計量</span><span class="sxs-lookup"><span data-stu-id="a5b1b-121">Key Performance Metrics</span></span>

<span data-ttu-id="a5b1b-122">下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="a5b1b-123">請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="a5b1b-124">儲存格時間、單一資料格更新的網路時間，需要 \* 有4個 RTT + 600 毫秒的 Nagle 和延遲的 ACK 互動。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="a5b1b-125">Goodput 小於6個位元組。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="a5b1b-126">通訊協定額外負荷為99.6%。</span><span class="sxs-lookup"><span data-stu-id="a5b1b-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5b1b-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5b1b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b1b-128">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="a5b1b-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="a5b1b-129">網路術語</span><span class="sxs-lookup"><span data-stu-id="a5b1b-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="a5b1b-130">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="a5b1b-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="a5b1b-131">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="a5b1b-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="a5b1b-132">修訂3：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="a5b1b-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="a5b1b-133">未來的改進</span><span class="sxs-lookup"><span data-stu-id="a5b1b-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 




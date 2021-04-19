---
description: 在這個版本的應用程式中，會使用壓縮的區區塊轉送資料。 這項變更會導致顯著的效能改進。
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 修訂三：壓縮的區區塊轉送
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982359"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="65335-104">修訂三：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="65335-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="65335-105">在這個版本的應用程式中，會使用壓縮的區區塊轉送資料。</span><span class="sxs-lookup"><span data-stu-id="65335-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="65335-106">這項變更會導致顯著的效能改進。</span><span class="sxs-lookup"><span data-stu-id="65335-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="65335-107">此版本中的變更</span><span class="sxs-lookup"><span data-stu-id="65335-107">Changes in this Version</span></span>

<span data-ttu-id="65335-108">此版本會反映下列變更：</span><span class="sxs-lookup"><span data-stu-id="65335-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="65335-109">儲存格更新不再序列化。</span><span class="sxs-lookup"><span data-stu-id="65335-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="65335-110">由於使用封鎖傳送，因此應用程式不再有對話。</span><span class="sxs-lookup"><span data-stu-id="65335-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="65335-111">使用資料壓縮，因而產生較不 fat 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="65335-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="65335-112">這一版的應用程式仍有問題;因為使用了大型傳送而沒有接收，所以會有鎖死的風險。</span><span class="sxs-lookup"><span data-stu-id="65335-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="65335-113">伺服器會針對每3個收到的位元組傳送一個位元組。</span><span class="sxs-lookup"><span data-stu-id="65335-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="65335-114">如果此範例應用程式的接收緩衝區大小小於1000個位元組，這可能會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="65335-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="65335-115">關鍵效能計量</span><span class="sxs-lookup"><span data-stu-id="65335-115">Key Performance Metrics</span></span>

<span data-ttu-id="65335-116">下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="65335-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="65335-117">請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。</span><span class="sxs-lookup"><span data-stu-id="65335-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="65335-118">此版本會反映下列效能計量：</span><span class="sxs-lookup"><span data-stu-id="65335-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="65335-119">資料格時間— 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="65335-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="65335-120">Goodput-2 Kb/RTT</span><span class="sxs-lookup"><span data-stu-id="65335-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="65335-121">通訊協定額外負荷-14%</span><span class="sxs-lookup"><span data-stu-id="65335-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="65335-122">有14% 的額外負荷，6% 是來自乙太網路標頭，而另8% 來自連線啟動和卸載。</span><span class="sxs-lookup"><span data-stu-id="65335-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65335-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="65335-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65335-124">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="65335-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="65335-125">網路術語</span><span class="sxs-lookup"><span data-stu-id="65335-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="65335-126">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="65335-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="65335-127">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="65335-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="65335-128">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="65335-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="65335-129">未來的改進</span><span class="sxs-lookup"><span data-stu-id="65335-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 




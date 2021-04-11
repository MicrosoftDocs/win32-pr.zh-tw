---
description: 在此修訂中，已重新設計範例應用程式，以消除不必要的連接。
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 修訂2：重新設計較少的連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114912"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="b446f-103">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="b446f-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="b446f-104">在此修訂中，已重新設計範例應用程式，以消除不必要的連接。</span><span class="sxs-lookup"><span data-stu-id="b446f-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="b446f-105">此應用程式範例也會提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。</span><span class="sxs-lookup"><span data-stu-id="b446f-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="b446f-106">請勿在您的應用程式中使用此程式碼範例;這僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="b446f-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="b446f-107">剩餘問題</span><span class="sxs-lookup"><span data-stu-id="b446f-107">Remaining Problems</span></span>

<span data-ttu-id="b446f-108">修訂中的變更已重新設計應用程式，每個更新只會進行一個 connect。</span><span class="sxs-lookup"><span data-stu-id="b446f-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="b446f-109">應用程式仍包含下列效能問題：</span><span class="sxs-lookup"><span data-stu-id="b446f-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="b446f-110">應用程式仍在序列化和對話中。</span><span class="sxs-lookup"><span data-stu-id="b446f-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="b446f-111">應用程式仍有 fat 設計;有許多傳送不需要在此設計中進行任何操作。</span><span class="sxs-lookup"><span data-stu-id="b446f-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="b446f-112">傳送只是3個位元組，這是不佳的串流。</span><span class="sxs-lookup"><span data-stu-id="b446f-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="b446f-113">關鍵效能計量</span><span class="sxs-lookup"><span data-stu-id="b446f-113">Key Performance Metrics</span></span>

<span data-ttu-id="b446f-114">下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。</span><span class="sxs-lookup"><span data-stu-id="b446f-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="b446f-115">請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。</span><span class="sxs-lookup"><span data-stu-id="b446f-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="b446f-116">此版本會反映下列效能計量：</span><span class="sxs-lookup"><span data-stu-id="b446f-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="b446f-117">儲存格時間— 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="b446f-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="b446f-118">Goodput-4 個位元組/RTT</span><span class="sxs-lookup"><span data-stu-id="b446f-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="b446f-119">通訊協定額外負荷-96.8%</span><span class="sxs-lookup"><span data-stu-id="b446f-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="b446f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b446f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b446f-121">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="b446f-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="b446f-122">網路術語</span><span class="sxs-lookup"><span data-stu-id="b446f-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="b446f-123">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="b446f-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="b446f-124">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="b446f-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="b446f-125">修訂3：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="b446f-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="b446f-126">未來的改進</span><span class="sxs-lookup"><span data-stu-id="b446f-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 




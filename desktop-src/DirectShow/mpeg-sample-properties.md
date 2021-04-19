---
description: MPEG 範例屬性
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: MPEG 範例屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966616"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="357f5-103">MPEG 範例屬性</span><span class="sxs-lookup"><span data-stu-id="357f5-103">MPEG Sample Properties</span></span>

<span data-ttu-id="357f5-104">MPEG 範例具有下列特性。</span><span class="sxs-lookup"><span data-stu-id="357f5-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="357f5-105">**時間戳記**</span><span class="sxs-lookup"><span data-stu-id="357f5-105">**Time Stamps**</span></span>

<span data-ttu-id="357f5-106">並非所有範例都有開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="357f5-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="357f5-107">封包和承載資料的範例停止時間並不實用;通常會設定為開始時間加1。</span><span class="sxs-lookup"><span data-stu-id="357f5-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="357f5-108">如果產生的系統層封包具有有效的時間點，則 MPEG 封包或承載資料範例將會設定開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="357f5-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="357f5-109">如需時間戳記的詳細資訊，請參閱2.4.1 的 >ISO1-11172：「封包標頭可能包含解碼和/或呈現時間戳記 (DTS 和 PT) 參考封包中的第一個存取單位」。</span><span class="sxs-lookup"><span data-stu-id="357f5-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="357f5-110">針對 MPEG \_ 資料流程主要類型，開始時間是第一個位元組的位元組位置，以每秒1個位元組分級。</span><span class="sxs-lookup"><span data-stu-id="357f5-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="357f5-111">停止時間是最後一個位元組的位元組位置。</span><span class="sxs-lookup"><span data-stu-id="357f5-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="357f5-112">因此，連續的範例應該要有第一個封包的停止時間等於下一個封包的開始時間。</span><span class="sxs-lookup"><span data-stu-id="357f5-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="357f5-113">針對視訊 CD 資料，媒體的原點必須符合 CDFS.SYS 所公開之影片 CD 檔案的格式，且開頭必須有標準 RIFF 組塊。</span><span class="sxs-lookup"><span data-stu-id="357f5-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="357f5-114">針對 MPEG video 封包和裝載類型，時間戳記是第一個影片框架的呈現時間，其圖片開始程式碼會在範例中開始。</span><span class="sxs-lookup"><span data-stu-id="357f5-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="357f5-115">針對 MPEG 音訊封包和裝載類型，時間戳記是在範例中開始其同步程式碼的第一個音訊框架的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="357f5-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="357f5-116">假設處理篩選器可以成功 prerolled 沒有時間戳記的封包和內容資料。</span><span class="sxs-lookup"><span data-stu-id="357f5-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="357f5-117">**間斷**</span><span class="sxs-lookup"><span data-stu-id="357f5-117">**Discontinuities**</span></span>

<span data-ttu-id="357f5-118">如果資料流程中有中斷 (例如，即時資料中的間隙，或是資料中或搜尋) 之後的錯誤，則會在下一個媒體範例上設定 [中斷] 屬性。</span><span class="sxs-lookup"><span data-stu-id="357f5-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="357f5-119">這也允許時間戳記不連續。</span><span class="sxs-lookup"><span data-stu-id="357f5-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="357f5-120">**資料流程結束通知**</span><span class="sxs-lookup"><span data-stu-id="357f5-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="357f5-121">當解碼器收到此通知時，它必須處理任何緩衝的資料。</span><span class="sxs-lookup"><span data-stu-id="357f5-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="357f5-122">任何新的資料都必須以不連續的屬性開頭。</span><span class="sxs-lookup"><span data-stu-id="357f5-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="357f5-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="357f5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="357f5-124">DirectShow 中的 MPEG 2 支援</span><span class="sxs-lookup"><span data-stu-id="357f5-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




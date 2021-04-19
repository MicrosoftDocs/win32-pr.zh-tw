---
description: 使用 MPEG-2 分隔器
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: 使用 MPEG-2 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987666"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="1c7f0-103">使用 MPEG-2 分隔器</span><span class="sxs-lookup"><span data-stu-id="1c7f0-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="1c7f0-104">從 Microsoft® Windows® XP 開始，MPEG 2 分隔器篩選器已被取代。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="1c7f0-105">請改用 [Mpeg-2 信號](mpeg-2-demultiplexer.md) 。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="1c7f0-106">MPEG-2 分隔器篩選器支援包含至少下列其中一種資料流程類型的 MPEG-2 程式資料流程的提取模式播放。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="1c7f0-107">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="1c7f0-107">MPEG-2 video</span></span>
-   <span data-ttu-id="1c7f0-108">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="1c7f0-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="1c7f0-109">針對 DVD-Video 所定義的杜比 AC-3 音訊編碼</span><span class="sxs-lookup"><span data-stu-id="1c7f0-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="1c7f0-110">LPCM (線性脈衝程式碼的調製) 音訊編碼，如 DVD-Video 所定義</span><span class="sxs-lookup"><span data-stu-id="1c7f0-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="1c7f0-111">如需 MPEG-2 分隔器所支援之媒體類型的清單，請參閱 [Mpeg-2 分隔器媒體類型](mpeg-2-splitter-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="1c7f0-112">MPEG-2 分隔器不會剖析傳輸資料流程。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="1c7f0-113">只有) 使用 (推送模式的傳輸資料流程的 MPEG-2 信號篩選篩選。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="1c7f0-114">**時間戳記**</span><span class="sxs-lookup"><span data-stu-id="1c7f0-114">**Time Stamps**</span></span>

<span data-ttu-id="1c7f0-115">播放 MPEG-2 程式串流時，MPEG-2 分隔器篩選器會將它所遇到的第一個系統時鐘參考視為任何資料流程的時間來源。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="1c7f0-116">這與使用呈現時間戳記的 [Mpeg-2 資料流程分隔器](mpeg-1-stream-splitter-filter.md)不同。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="1c7f0-117">[**IAMParse：： GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime)方法會傳回已處理之資料的 (可能估計) 資料流程系統時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="1c7f0-118">如果 MPEG-2 分隔器篩選器遇到具有非持續性屬性集的輸入範例 (可使用 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 或 [**IMediaSample2：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) 來設定 [中斷] 屬性，直到它找到資料中的第一個元件並調整其時間戳記，如此一來，該套件 (scr) 的系統時鐘參考才會被視為與中斷之前的 scr 時間相同。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="1c7f0-119">如果 SCR 時鐘顯示為向前跳或向前跳到一秒以上，則 (與 MPEG-2 程式串流規格) ，這也會被視為時鐘不連續，並從傳遞給下游篩選器的時間戳記減去明顯的時鐘差異。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="1c7f0-120">**資料流程選取範圍**</span><span class="sxs-lookup"><span data-stu-id="1c7f0-120">**Stream Selection**</span></span>

<span data-ttu-id="1c7f0-121">播放 MPEG-2 程式串流時，會選擇第一個影片串流和第一個播放程式串流的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="1c7f0-122">最多支援一個音訊和一個影片輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="1c7f0-123">透過 [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) 介面，相同類型的不同資料流程可以選取為系統標頭中的音訊限制所指定的數位。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="1c7f0-124">針對 MPEG-2 音訊，目前假設資料流程形成連續的範圍，從資料流程0xC0 開始。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="1c7f0-125">**支援的介面**</span><span class="sxs-lookup"><span data-stu-id="1c7f0-125">**Supported Interfaces**</span></span>

<span data-ttu-id="1c7f0-126">MPEG-2 分隔器篩選器支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="1c7f0-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="1c7f0-128">僅限 MPEG-2 程式串流。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="1c7f0-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="1c7f0-130">僅限 MPEG-2 程式串流，僅限音訊串流。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="1c7f0-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="1c7f0-132">包括位元組模式搜尋。</span><span class="sxs-lookup"><span data-stu-id="1c7f0-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c7f0-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c7f0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c7f0-134">DirectShow 中的 MPEG 2 支援</span><span class="sxs-lookup"><span data-stu-id="1c7f0-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




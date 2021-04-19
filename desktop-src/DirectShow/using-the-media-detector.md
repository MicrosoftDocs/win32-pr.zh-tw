---
description: 使用媒體偵測器
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: 使用媒體偵測器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974755"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="e84a6-103">使用媒體偵測器</span><span class="sxs-lookup"><span data-stu-id="e84a6-103">Using the Media Detector</span></span>

<span data-ttu-id="e84a6-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e84a6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e84a6-105">媒體偵測器是一種協助程式物件，可取得檔案的相關資訊，例如資料流程的數目、類型和持續時間。</span><span class="sxs-lookup"><span data-stu-id="e84a6-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="e84a6-106">它也包含從影片串流中取出海報框架的方法。</span><span class="sxs-lookup"><span data-stu-id="e84a6-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="e84a6-107">它會公開 [**IMediaDet**](imediadet.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="e84a6-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="e84a6-108">媒體偵測器會以兩種模式的其中一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="e84a6-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="e84a6-109">當您建立媒體偵測器的實例時，它不會附加至特定的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="e84a6-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="e84a6-110">在此模式中，您可以從多個來源檔案取出串流資訊。</span><span class="sxs-lookup"><span data-stu-id="e84a6-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="e84a6-111">不過，一旦您使用媒體偵測器來取得海報框架，它就會切換為 *點陣圖抓取模式*。</span><span class="sxs-lookup"><span data-stu-id="e84a6-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="e84a6-112">在點陣圖抓取模式中，媒體偵測器會附加至特定的影片資料流程，而資料流程資訊方法將無法再運作。</span><span class="sxs-lookup"><span data-stu-id="e84a6-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="e84a6-113">此外，也沒有辦法將媒體偵測器切換回其啟動模式。</span><span class="sxs-lookup"><span data-stu-id="e84a6-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="e84a6-114">因此，在您取得海報框架之前，請先取得所需的任何串流資訊，或者為每個串流建立新的媒體偵測器實例。</span><span class="sxs-lookup"><span data-stu-id="e84a6-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="e84a6-115">若要取得串流資訊，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e84a6-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="e84a6-116">以原始程式檔的名稱呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md) ]。</span><span class="sxs-lookup"><span data-stu-id="e84a6-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="e84a6-117">呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) 取得來源中的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="e84a6-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="e84a6-118">使用 IMediaDet 指定串流號碼 [**：:p 的 \_ CurrentStream**](imediadet-put-currentstream.md)。</span><span class="sxs-lookup"><span data-stu-id="e84a6-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="e84a6-119">然後呼叫下列一或多個方法：</span><span class="sxs-lookup"><span data-stu-id="e84a6-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="e84a6-120">[**IMediaDet：： get \_StreamType**](imediadet-get-streamtype.md)：抓取資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e84a6-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="e84a6-121">[**IMediaDet：： get \_StreamLength**](imediadet-get-streamlength.md)：抓取資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e84a6-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="e84a6-122">[**IMediaDet：： get \_幀**](imediadet-get-framerate.md)速率：抓取視頻資料流程的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="e84a6-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="e84a6-123">若要取得海報框架，請指定串流號碼，如同上一個步驟所示。</span><span class="sxs-lookup"><span data-stu-id="e84a6-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="e84a6-124">然後呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md)，將海報框架複製到緩衝區，或呼叫 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)，以將海報框架儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="e84a6-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e84a6-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e84a6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e84a6-126">使用來源</span><span class="sxs-lookup"><span data-stu-id="e84a6-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 




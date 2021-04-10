---
description: 設定來源的屬性
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: 設定來源的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845672"
---
# <a name="setting-properties-on-sources"></a><span data-ttu-id="910ca-103">設定來源的屬性</span><span class="sxs-lookup"><span data-stu-id="910ca-103">Setting Properties on Sources</span></span>

<span data-ttu-id="910ca-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="910ca-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="910ca-105">當您建立新的來源物件時，有幾個您需要設定的屬性，以及您可以選擇性地設定的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="910ca-105">When you create a new source object, there are a few properties you are required to set and others you can optionally set.</span></span> <span data-ttu-id="910ca-106">您必須設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="910ca-106">You must set the following properties.</span></span>

-   <span data-ttu-id="910ca-107">相對於時間軸其餘部分的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-107">The start and stop times, relative to the rest of the timeline.</span></span> <span data-ttu-id="910ca-108">呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="910ca-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="910ca-109">請勿在相同的播放軌內的來源物件上設定重迭的時間，否則會造成未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="910ca-109">Do not set overlapping times on source objects within the same track, or it will cause undefined behavior.</span></span>
-   <span data-ttu-id="910ca-110">要做為來源剪輯使用的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="910ca-110">The media file to use as a source clip.</span></span> <span data-ttu-id="910ca-111">呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md)。</span><span class="sxs-lookup"><span data-stu-id="910ca-111">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md).</span></span>
-   <span data-ttu-id="910ca-112">相對於原始來源檔案的媒體開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-112">The media start and stop times, relative to the original source file.</span></span> <span data-ttu-id="910ca-113">呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="910ca-113">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="910ca-114">例外狀況：如果來源是靜止影像，請勿指定媒體時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-114">Exception: If the source is a still image, do not specify the media times.</span></span> <span data-ttu-id="910ca-115">如需媒體時間的詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="910ca-115">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="910ca-116">來源物件會從父群組繼承其媒體類型，因此不需要指定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="910ca-116">A source object inherits its media type from the parent group, so it is not necessary to specify a media type.</span></span>

<span data-ttu-id="910ca-117">選擇性屬性包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="910ca-117">Optional properties include the following:</span></span>

-   <span data-ttu-id="910ca-118">延展模式。</span><span class="sxs-lookup"><span data-stu-id="910ca-118">The stretch mode.</span></span> <span data-ttu-id="910ca-119">延展模式會指定 Microsoft® DirectShow®編輯服務 (DES) 如何轉譯大小不符合輸出維度的來源。</span><span class="sxs-lookup"><span data-stu-id="910ca-119">The stretch mode specifies how Microsoft® DirectShow® Editing Services (DES) renders a source whose size does not match the output dimensions.</span></span> <span data-ttu-id="910ca-120">根據預設，DES 會伸展影像，而不會保留長寬比。</span><span class="sxs-lookup"><span data-stu-id="910ca-120">By default, DES stretches an image without preserving the aspect ratio.</span></span> <span data-ttu-id="910ca-121">或者，DES 可以裁剪映射或建立黑邊。</span><span class="sxs-lookup"><span data-stu-id="910ca-121">Alternatively, DES can crop an image or create a letterbox.</span></span> <span data-ttu-id="910ca-122">呼叫 [**IAMTimelineSrc：： SetStretchMode**](iamtimelinesrc-setstretchmode.md) 方法來指定延展模式。</span><span class="sxs-lookup"><span data-stu-id="910ca-122">Call the [**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md) method to specify the stretch mode.</span></span>
-   <span data-ttu-id="910ca-123">來源檔案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-123">The duration of the source file.</span></span> <span data-ttu-id="910ca-124">如果您在設定媒體時間之前設定了此屬性，DES 會驗證媒體停止時間，並在超過檔案持續時間時截斷停止時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-124">If you set this property before setting the media times, DES validates the media stop time and truncates the stop time if it exceeds the file duration.</span></span> <span data-ttu-id="910ca-125">這有助於避免稍後轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="910ca-125">This can help avoid rendering errors later.</span></span> <span data-ttu-id="910ca-126">您可以使用媒體偵測器來取得檔案的持續時間，如 [使用媒體](using-the-media-detector.md)偵測器中所述。</span><span class="sxs-lookup"><span data-stu-id="910ca-126">You can obtain the duration of the file using the media detector, as described in [Using the Media Detector](using-the-media-detector.md).</span></span> <span data-ttu-id="910ca-127">呼叫 [**IAMTimelineSrc：： SetMediaLength**](iamtimelinesrc-setmedialength.md) 方法來指定檔案持續時間。</span><span class="sxs-lookup"><span data-stu-id="910ca-127">Call the [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md) method to specify the file duration.</span></span>
-   <span data-ttu-id="910ca-128">資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="910ca-128">The stream number.</span></span> <span data-ttu-id="910ca-129">根據預設，來源物件會使用檔案中的第一個資料流程，該資料流程符合父群組的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="910ca-129">By default, a source object uses the first stream in the file that matches the media type of the parent group.</span></span> <span data-ttu-id="910ca-130">如果檔案包含兩個或多個相同媒體類型的資料流程，請呼叫 [**IAMTimelineSrc：： SetStreamNumber**](iamtimelinesrc-setstreamnumber.md)來選取要使用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="910ca-130">If a file contains two or more streams of the same media type, select which stream to use by calling [**IAMTimelineSrc::SetStreamNumber**](iamtimelinesrc-setstreamnumber.md).</span></span> <span data-ttu-id="910ca-131">您可以使用媒體偵測器來尋找資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="910ca-131">You can use the media detector to find the number of streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="910ca-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="910ca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="910ca-133">使用來源</span><span class="sxs-lookup"><span data-stu-id="910ca-133">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 




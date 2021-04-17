---
description: 啟用來源讀取器的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: 'MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511325"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="c44fb-103">MF \_ 來源 \_ 讀取器 \_ 啟用 \_ ADVANCED \_ VIDEO \_ 處理屬性</span><span class="sxs-lookup"><span data-stu-id="c44fb-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="c44fb-104">啟用 [來源讀取器](source-reader.md)的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。</span><span class="sxs-lookup"><span data-stu-id="c44fb-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="c44fb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c44fb-105">Data type</span></span>

<span data-ttu-id="c44fb-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c44fb-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c44fb-107">備註</span><span class="sxs-lookup"><span data-stu-id="c44fb-107">Remarks</span></span>

<span data-ttu-id="c44fb-108">如果此屬性為 **TRUE**，則來源讀取器可以將視頻處理器插入處理管線中，以啟用下列格式轉換類型：</span><span class="sxs-lookup"><span data-stu-id="c44fb-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="c44fb-109">色彩空間轉換 (YUV 到 RGB-32) </span><span class="sxs-lookup"><span data-stu-id="c44fb-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="c44fb-110">去交錯</span><span class="sxs-lookup"><span data-stu-id="c44fb-110">Deinterlacing</span></span>
-   <span data-ttu-id="c44fb-111">影片調整大小</span><span class="sxs-lookup"><span data-stu-id="c44fb-111">Video resizing</span></span>
-   <span data-ttu-id="c44fb-112">畫面播放速率轉換</span><span class="sxs-lookup"><span data-stu-id="c44fb-112">Frame-rate conversion</span></span>

<span data-ttu-id="c44fb-113">如果此屬性為 **TRUE**，則 [ [MF \_ READWRITE 停用 \_ \_ 轉換器](mf-readwrite-disable-converters.md) ] 屬性必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c44fb-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="c44fb-114">來源讀取器會尋找在 [ **MFT \_ 類別] \_ 視頻 \_ 處理器** 類別中註冊的視頻處理器，包括針對本機進程註冊的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="c44fb-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="c44fb-115">如需有關 MFTs 本機註冊的詳細資訊， (參閱 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ) 。如果找不到其他適合的視頻處理器，來源讀取器會使用轉碼視頻處理器 (XVP) 。</span><span class="sxs-lookup"><span data-stu-id="c44fb-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="c44fb-116">應用程式會藉由呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)來指定所需的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="c44fb-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="c44fb-117">當來源讀取器設定視頻處理器時，它會嘗試符合輸出類型的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="c44fb-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="c44fb-118">畫面播放速率 ([MF \_ MT \_ 幀 \_ 速率](mf-mt-frame-rate-attribute.md)) </span><span class="sxs-lookup"><span data-stu-id="c44fb-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="c44fb-119">框架大小 ([MF \_ MT \_ 框架 \_ 大小](mf-mt-frame-size-attribute.md)) </span><span class="sxs-lookup"><span data-stu-id="c44fb-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="c44fb-120">交錯模式 ([MF \_ MT \_ 交錯 \_ 模式](mf-mt-interlace-mode-attribute.md)) </span><span class="sxs-lookup"><span data-stu-id="c44fb-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="c44fb-121">圖元外觀比例 ([MF \_ MT \_ 圖元 \_ 外觀 \_ 比例](mf-mt-pixel-aspect-ratio-attribute.md)) </span><span class="sxs-lookup"><span data-stu-id="c44fb-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="c44fb-122">類型 ([MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)) </span><span class="sxs-lookup"><span data-stu-id="c44fb-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="c44fb-123">此屬性類似于 [MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理](mf-source-reader-enable-video-processing.md) 屬性，但提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="c44fb-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="c44fb-124">支援更廣泛的格式轉換。</span><span class="sxs-lookup"><span data-stu-id="c44fb-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="c44fb-125">應用程式可以註冊自己的轉換器。</span><span class="sxs-lookup"><span data-stu-id="c44fb-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="c44fb-126">某些轉換可在使用 GPU 的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="c44fb-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="c44fb-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c44fb-127">Requirements</span></span>



| <span data-ttu-id="c44fb-128">需求</span><span class="sxs-lookup"><span data-stu-id="c44fb-128">Requirement</span></span> | <span data-ttu-id="c44fb-129">值</span><span class="sxs-lookup"><span data-stu-id="c44fb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c44fb-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c44fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c44fb-131">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c44fb-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c44fb-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c44fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c44fb-133">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c44fb-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c44fb-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c44fb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c44fb-135"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="c44fb-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c44fb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c44fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c44fb-137">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c44fb-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c44fb-138">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="c44fb-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="c44fb-139">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="c44fb-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 





---
description: 指定 h.264 影片串流的最大巨大區塊處理速率。
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: 'MF_MT_H264_MAX_MB_PER_SEC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974181"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="e1b4d-103">MF \_ MT \_ H264 \_ \_ 每秒最大 MB \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="e1b4d-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="e1b4d-104">指定 h.264 影片串流的最大巨大區塊處理速率。</span><span class="sxs-lookup"><span data-stu-id="e1b4d-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1b4d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e1b4d-105">Data type</span></span>

<span data-ttu-id="e1b4d-106">**\[ UINT32 \]** 儲存為 **UINT8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="e1b4d-107">適用於</span><span class="sxs-lookup"><span data-stu-id="e1b4d-107">Applies to</span></span>

[<span data-ttu-id="e1b4d-108">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e1b4d-109">備註</span><span class="sxs-lookup"><span data-stu-id="e1b4d-109">Remarks</span></span>

<span data-ttu-id="e1b4d-110">此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e1b4d-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="e1b4d-111">屬性的值是 UINT32 值的陣列，對應至 UVC 1.5 h.264 影片格式描述項中的下欄欄位。</span><span class="sxs-lookup"><span data-stu-id="e1b4d-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="e1b4d-112">Array 元素</span><span class="sxs-lookup"><span data-stu-id="e1b4d-112">Array Element</span></span> | <span data-ttu-id="e1b4d-113">描述項欄位</span><span class="sxs-lookup"><span data-stu-id="e1b4d-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="e1b4d-114">0</span><span class="sxs-lookup"><span data-stu-id="e1b4d-114">0</span></span>             | <span data-ttu-id="e1b4d-115">**dwMaxMBperSecOneResolutionNoScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="e1b4d-116">1</span><span class="sxs-lookup"><span data-stu-id="e1b4d-116">1</span></span>             | <span data-ttu-id="e1b4d-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="e1b4d-118">2</span><span class="sxs-lookup"><span data-stu-id="e1b4d-118">2</span></span>             | <span data-ttu-id="e1b4d-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="e1b4d-120">3</span><span class="sxs-lookup"><span data-stu-id="e1b4d-120">3</span></span>             | <span data-ttu-id="e1b4d-121">**dwMaxMBperSecFourResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="e1b4d-122">4</span><span class="sxs-lookup"><span data-stu-id="e1b4d-122">4</span></span>             | <span data-ttu-id="e1b4d-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="e1b4d-124">5</span><span class="sxs-lookup"><span data-stu-id="e1b4d-124">5</span></span>             | <span data-ttu-id="e1b4d-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="e1b4d-126">6</span><span class="sxs-lookup"><span data-stu-id="e1b4d-126">6</span></span>             | <span data-ttu-id="e1b4d-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="e1b4d-128">7</span><span class="sxs-lookup"><span data-stu-id="e1b4d-128">7</span></span>             | <span data-ttu-id="e1b4d-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="e1b4d-130">8</span><span class="sxs-lookup"><span data-stu-id="e1b4d-130">8</span></span>             | <span data-ttu-id="e1b4d-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="e1b4d-132">9</span><span class="sxs-lookup"><span data-stu-id="e1b4d-132">9</span></span>             | <span data-ttu-id="e1b4d-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="e1b4d-134">10</span><span class="sxs-lookup"><span data-stu-id="e1b4d-134">10</span></span>            | <span data-ttu-id="e1b4d-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="e1b4d-136">11</span><span class="sxs-lookup"><span data-stu-id="e1b4d-136">11</span></span>            | <span data-ttu-id="e1b4d-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="e1b4d-138">12</span><span class="sxs-lookup"><span data-stu-id="e1b4d-138">12</span></span>            | <span data-ttu-id="e1b4d-139">**dwMaxMBperSecOneResolutionFullScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="e1b4d-140">13</span><span class="sxs-lookup"><span data-stu-id="e1b4d-140">13</span></span>            | <span data-ttu-id="e1b4d-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="e1b4d-142">14</span><span class="sxs-lookup"><span data-stu-id="e1b4d-142">14</span></span>            | <span data-ttu-id="e1b4d-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="e1b4d-144">15</span><span class="sxs-lookup"><span data-stu-id="e1b4d-144">15</span></span>            | <span data-ttu-id="e1b4d-145">**dwMaxMBperSecFourResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="e1b4d-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="e1b4d-146">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="e1b4d-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b4d-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1b4d-147">Requirements</span></span>



| <span data-ttu-id="e1b4d-148">需求</span><span class="sxs-lookup"><span data-stu-id="e1b4d-148">Requirement</span></span> | <span data-ttu-id="e1b4d-149">值</span><span class="sxs-lookup"><span data-stu-id="e1b4d-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b4d-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1b4d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b4d-151">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1b4d-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e1b4d-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1b4d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b4d-153">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1b4d-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e1b4d-154">標頭</span><span class="sxs-lookup"><span data-stu-id="e1b4d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b4d-155"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b4d-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b4d-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1b4d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b4d-157">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e1b4d-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1b4d-158">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="e1b4d-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





---
description: '\_ \_ \_ \_ \_ \_ \_ 當 CapsType 成員設定為 StreamConfigCapsType 聯集的 VideoCap 成員時，TAPI 串流設定 caps 結構會包含 tapi 影片串流設定 caps 結構。'
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: 'TAPI_VIDEO_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999674"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="fa4cb-103">TAPI \_ 影片 \_ 串流 \_ 設定 \_ CAPS 結構</span><span class="sxs-lookup"><span data-stu-id="fa4cb-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="fa4cb-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用此結構。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa4cb-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fa4cb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fa4cb-106">當 **CapsType** 成員設定為 [**StreamConfigCapsType**](streamconfigcapstype.md)聯集的 **VideoCap** 成員時，tapi [**\_ 串流 \_ \_**](tapi-stream-config-caps.md)設定 caps 結構會包含 **tapi \_ 影片 \_ 串流設定 \_ \_ caps** 結構。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa4cb-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="fa4cb-108">成員</span><span class="sxs-lookup"><span data-stu-id="fa4cb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa4cb-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-110">顯示給應用程式使用者之音訊串流設定類型的易記描述。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-111">**VideoStandard**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-112">使用的影片標準。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-113">**InputSize**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-114">輸入框架的大小。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-115">**MinCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-116">最小裁剪大小。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-117">**MaxCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-118">裁剪大小上限。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-119">**CropGranularityX**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-120">沿著 X 軸允許裁剪的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-121">**CropGranularityY**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-122">沿著 y 軸允許裁剪的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-123">**CropAlignX**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-124">X 軸裁剪的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-125">**CropAlignY**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-126">Y 軸裁剪的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-127">**MinOutputSize**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-128">影片視窗的最小結果大小。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-129">**MaxOutputSize**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-130">影片視窗的結果大小上限。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-131">**OutputGranularityX**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-132">沿著 X 軸輸出大小的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-133">**OutputGranularityY**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-134">沿著 y 軸的輸出大小的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-135">**StretchTapsX**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-136">沿著 X 軸伸展。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-137">**StretchTapsY**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-138">沿著 y 軸伸展。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-139">**ShrinkTapsX**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-140">沿著 X 軸壓縮。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-141">**ShrinkTapsY**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-142">沿著 y 軸壓縮。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-143">**MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-144">最小影片畫面間隔。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-145">**MaxFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-146">最大影片畫面間隔。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-147">**MinBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-148">每秒的最小位數。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="fa4cb-149">**MaxBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="fa4cb-150">每秒最大位數。</span><span class="sxs-lookup"><span data-stu-id="fa4cb-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa4cb-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa4cb-151">Requirements</span></span>



| <span data-ttu-id="fa4cb-152">需求</span><span class="sxs-lookup"><span data-stu-id="fa4cb-152">Requirement</span></span> | <span data-ttu-id="fa4cb-153">值</span><span class="sxs-lookup"><span data-stu-id="fa4cb-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4cb-154">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fa4cb-154">TAPI version</span></span><br/> | <span data-ttu-id="fa4cb-155">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="fa4cb-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="fa4cb-156">標頭</span><span class="sxs-lookup"><span data-stu-id="fa4cb-156">Header</span></span><br/>       | <dl> <span data-ttu-id="fa4cb-157"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa4cb-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa4cb-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa4cb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4cb-159">**TAPI \_ 串流 \_ 設定 \_ CAP**</span><span class="sxs-lookup"><span data-stu-id="fa4cb-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 





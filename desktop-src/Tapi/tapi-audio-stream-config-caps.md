---
description: '\_ \_ \_ \_ \_ \_ \_ 當 CapsType 成員設定為 StreamConfigCapsType 聯集的 AudioCap 成員時，tapi 音訊串流設定 caps 結構會包含在 tapi 串流設定的 cap 結構中。'
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: 'TAPI_AUDIO_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982591"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="fe385-103">TAPI \_ 音訊 \_ 串流 \_ 設定 \_ CAPS 結構</span><span class="sxs-lookup"><span data-stu-id="fe385-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="fe385-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用此結構。</span><span class="sxs-lookup"><span data-stu-id="fe385-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe385-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fe385-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fe385-106">當 **CapsType** 成員設定為 [**StreamConfigCapsType**](streamconfigcapstype.md)聯集的 **AudioCap** 成員時，tapi **\_ 音訊 \_ 串流設定 \_ \_ caps** 結構會包含在 [**tapi \_ 串流 \_ \_**](tapi-stream-config-caps.md)設定的 cap 結構中。</span><span class="sxs-lookup"><span data-stu-id="fe385-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe385-107">語法</span><span class="sxs-lookup"><span data-stu-id="fe385-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="fe385-108">成員</span><span class="sxs-lookup"><span data-stu-id="fe385-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe385-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="fe385-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-110">顯示給應用程式使用者之音訊串流設定類型的易記描述。</span><span class="sxs-lookup"><span data-stu-id="fe385-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-111">**MinimumChannels**</span><span class="sxs-lookup"><span data-stu-id="fe385-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-112">與資料流程相關聯的通道數目下限。</span><span class="sxs-lookup"><span data-stu-id="fe385-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-113">**MaximumChannels**</span><span class="sxs-lookup"><span data-stu-id="fe385-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-114">與資料流程相關聯的通道數目上限。</span><span class="sxs-lookup"><span data-stu-id="fe385-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-115">**ChannelsGranularity**</span><span class="sxs-lookup"><span data-stu-id="fe385-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-116">通道計數的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fe385-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-117">**MinimumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="fe385-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-118">每個樣本的最小位數。</span><span class="sxs-lookup"><span data-stu-id="fe385-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-119">**MaximumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="fe385-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-120">每個樣本的位數上限。</span><span class="sxs-lookup"><span data-stu-id="fe385-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-121">**BitsPerSampleGranularity**</span><span class="sxs-lookup"><span data-stu-id="fe385-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-122">每個樣本值的位細微性。</span><span class="sxs-lookup"><span data-stu-id="fe385-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-123">**MinimumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="fe385-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-124">最小取樣頻率。</span><span class="sxs-lookup"><span data-stu-id="fe385-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-125">**MaximumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="fe385-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-126">最大取樣頻率。</span><span class="sxs-lookup"><span data-stu-id="fe385-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-127">**SampleFrequencyGranularity**</span><span class="sxs-lookup"><span data-stu-id="fe385-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-128">取樣頻率值的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fe385-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-129">**MinimumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="fe385-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-130">每秒的最小平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="fe385-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-131">**MaximumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="fe385-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-132">每秒最大的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="fe385-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="fe385-133">**AvgBytesPerSecGranularity**</span><span class="sxs-lookup"><span data-stu-id="fe385-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="fe385-134">每秒位元組數值的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="fe385-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe385-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe385-135">Requirements</span></span>



| <span data-ttu-id="fe385-136">需求</span><span class="sxs-lookup"><span data-stu-id="fe385-136">Requirement</span></span> | <span data-ttu-id="fe385-137">值</span><span class="sxs-lookup"><span data-stu-id="fe385-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe385-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fe385-138">TAPI version</span></span><br/> | <span data-ttu-id="fe385-139">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="fe385-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="fe385-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fe385-140">Header</span></span><br/>       | <dl> <span data-ttu-id="fe385-141"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe385-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe385-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe385-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe385-143">**TAPI \_ 串流 \_ 設定 \_ CAP**</span><span class="sxs-lookup"><span data-stu-id="fe385-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 





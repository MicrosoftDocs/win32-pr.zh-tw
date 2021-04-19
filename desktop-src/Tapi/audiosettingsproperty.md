---
description: ITAudioSettings：： GetRange、ITAudioSettings：： Get 和 ITAudioSettings：： Set 方法會使用 AudioSettingsProperty 列舉來指出要處理的音訊設定屬性。
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: 'AudioSettingsProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982639"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="57775-103">AudioSettingsProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="57775-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="57775-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="57775-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="57775-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="57775-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="57775-106">[**ITAudioSettings：： GetRange**](itaudiosettings-getrange.md)、 [**ITAudioSettings：： Get**](itaudiosettings-get.md)和 [**ITAudioSettings：： Set**](itaudiosettings-set.md)方法會使用 **AudioSettingsProperty** 列舉來指出要處理的音訊設定屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="57775-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="57775-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="57775-108">常數</span><span class="sxs-lookup"><span data-stu-id="57775-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57775-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**</span><span class="sxs-lookup"><span data-stu-id="57775-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="57775-110">信號設定屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**</span><span class="sxs-lookup"><span data-stu-id="57775-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="57775-112">無聲臨界值屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings \_ 磁片區**</span><span class="sxs-lookup"><span data-stu-id="57775-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="57775-114">Volume 屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ 餘額**</span><span class="sxs-lookup"><span data-stu-id="57775-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="57775-116">餘額屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_ 音量**</span><span class="sxs-lookup"><span data-stu-id="57775-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="57775-118">音量屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ 高音**</span><span class="sxs-lookup"><span data-stu-id="57775-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="57775-120">高音屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ 低音**</span><span class="sxs-lookup"><span data-stu-id="57775-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="57775-122">低音屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="57775-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**</span><span class="sxs-lookup"><span data-stu-id="57775-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="57775-124">Monaural 屬性。</span><span class="sxs-lookup"><span data-stu-id="57775-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57775-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="57775-125">Requirements</span></span>



| <span data-ttu-id="57775-126">需求</span><span class="sxs-lookup"><span data-stu-id="57775-126">Requirement</span></span> | <span data-ttu-id="57775-127">值</span><span class="sxs-lookup"><span data-stu-id="57775-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57775-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="57775-128">TAPI version</span></span><br/> | <span data-ttu-id="57775-129">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="57775-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="57775-130">標頭</span><span class="sxs-lookup"><span data-stu-id="57775-130">Header</span></span><br/>       | <dl> <span data-ttu-id="57775-131"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57775-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57775-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57775-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57775-133">**ITAudioSettings：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="57775-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="57775-134">**ITAudioSettings：： Get**</span><span class="sxs-lookup"><span data-stu-id="57775-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="57775-135">**ITAudioSettings：： Set**</span><span class="sxs-lookup"><span data-stu-id="57775-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 





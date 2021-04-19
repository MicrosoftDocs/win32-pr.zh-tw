---
description: 多個方法會使用 TAPIControlFlags 列舉來指出指定的屬性是以自動或手動方式控制。
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: 'TAPIControlFlags 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990778"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="12387-103">TAPIControlFlags 列舉</span><span class="sxs-lookup"><span data-stu-id="12387-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="12387-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="12387-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="12387-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="12387-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="12387-106">多個方法會使用 **TAPIControlFlags** 列舉來指出指定的屬性是以自動或手動方式控制。</span><span class="sxs-lookup"><span data-stu-id="12387-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="12387-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12387-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="12387-108">常數</span><span class="sxs-lookup"><span data-stu-id="12387-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12387-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ 旗標 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="12387-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="12387-110">TAPI 沒有屬性的控制旗標。</span><span class="sxs-lookup"><span data-stu-id="12387-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="12387-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_自動 TAPIControl 旗標 \_**</span><span class="sxs-lookup"><span data-stu-id="12387-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="12387-112">屬性會自動受到控制。</span><span class="sxs-lookup"><span data-stu-id="12387-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="12387-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl \_ 旗標 \_ 手冊**</span><span class="sxs-lookup"><span data-stu-id="12387-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="12387-114">屬性是以手動方式控制。</span><span class="sxs-lookup"><span data-stu-id="12387-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12387-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="12387-115">Requirements</span></span>



| <span data-ttu-id="12387-116">需求</span><span class="sxs-lookup"><span data-stu-id="12387-116">Requirement</span></span> | <span data-ttu-id="12387-117">值</span><span class="sxs-lookup"><span data-stu-id="12387-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12387-118">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="12387-118">TAPI version</span></span><br/> | <span data-ttu-id="12387-119">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="12387-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="12387-120">標頭</span><span class="sxs-lookup"><span data-stu-id="12387-120">Header</span></span><br/>       | <dl> <span data-ttu-id="12387-121"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="12387-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12387-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12387-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12387-123">**ITAudioDeviceControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="12387-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="12387-124">**ITAudioDeviceControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="12387-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="12387-125">**ITAudioDeviceControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="12387-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="12387-126">**ITAudioSettings：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="12387-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="12387-127">**ITAudioSettings：： Get**</span><span class="sxs-lookup"><span data-stu-id="12387-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="12387-128">**ITAudioSettings：： Set**</span><span class="sxs-lookup"><span data-stu-id="12387-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="12387-129">**ITCallQualityControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="12387-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="12387-130">**ITCallQualityControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="12387-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="12387-131">**ITCallQualityControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="12387-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="12387-132">**ITStreamQualityControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="12387-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="12387-133">**ITStreamQualityControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="12387-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="12387-134">**ITStreamQualityControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="12387-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 





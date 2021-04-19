---
description: ITCallQualityControl：： GetRange、ITCallQualityControl：： Get 和 ITCallQualityControl：： Set 方法會使用 CallQualityProperty 列舉來指出要處理的呼叫品質屬性。
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: 'CallQualityProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998855"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="0d652-103">CallQualityProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="0d652-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="0d652-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0d652-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d652-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0d652-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d652-106">[**ITCallQualityControl：： GetRange**](itcallqualitycontrol-getrange.md)、 [**ITCallQualityControl：： Get**](itcallqualitycontrol-get.md)和 [**ITCallQualityControl：： Set**](itcallqualitycontrol-set.md)方法會使用 **CallQualityProperty** 列舉來指出要處理的呼叫品質屬性。</span><span class="sxs-lookup"><span data-stu-id="0d652-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d652-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d652-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="0d652-108">常數</span><span class="sxs-lookup"><span data-stu-id="0d652-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0d652-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**</span><span class="sxs-lookup"><span data-stu-id="0d652-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-110">控制間隔。</span><span class="sxs-lookup"><span data-stu-id="0d652-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**</span><span class="sxs-lookup"><span data-stu-id="0d652-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-112">會議的位元速率。</span><span class="sxs-lookup"><span data-stu-id="0d652-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="0d652-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-114">最大輸入位速率。</span><span class="sxs-lookup"><span data-stu-id="0d652-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="0d652-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-116">目前的輸入位速度。</span><span class="sxs-lookup"><span data-stu-id="0d652-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="0d652-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-118">最大輸出位元速率。</span><span class="sxs-lookup"><span data-stu-id="0d652-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="0d652-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-120">目前的輸出位元速率。</span><span class="sxs-lookup"><span data-stu-id="0d652-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ >maxcpuload**</span><span class="sxs-lookup"><span data-stu-id="0d652-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-122">最大 CPU 負載。</span><span class="sxs-lookup"><span data-stu-id="0d652-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="0d652-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**</span><span class="sxs-lookup"><span data-stu-id="0d652-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="0d652-124">目前的 CPU 負載。</span><span class="sxs-lookup"><span data-stu-id="0d652-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d652-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d652-125">Requirements</span></span>



| <span data-ttu-id="0d652-126">需求</span><span class="sxs-lookup"><span data-stu-id="0d652-126">Requirement</span></span> | <span data-ttu-id="0d652-127">值</span><span class="sxs-lookup"><span data-stu-id="0d652-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d652-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0d652-128">TAPI version</span></span><br/> | <span data-ttu-id="0d652-129">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="0d652-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="0d652-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0d652-130">Header</span></span><br/>       | <dl> <span data-ttu-id="0d652-131"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d652-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d652-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d652-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d652-133">**ITCallQualityControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="0d652-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="0d652-134">**ITCallQualityControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="0d652-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="0d652-135">**ITCallQualityControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="0d652-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 





---
description: ITStreamQualityControl：： GetRange、ITStreamQualityControl：： Get 和 ITStreamQualityControl：： Set 方法所使用的 StreamQualityProperty 列舉，表示要處理的資料流程品質屬性。
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: 'StreamQualityProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980245"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="ff868-103">StreamQualityProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="ff868-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="ff868-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ff868-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ff868-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ff868-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ff868-106">[**ITStreamQualityControl：： GetRange**](itstreamqualitycontrol-getrange.md)、 [**ITStreamQualityControl：： Get**](itstreamqualitycontrol-get.md)和 [**ITStreamQualityControl：： Set**](itstreamqualitycontrol-set.md)方法所使用的 **StreamQualityProperty** 列舉，表示要處理的資料流程品質屬性。</span><span class="sxs-lookup"><span data-stu-id="ff868-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff868-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff868-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="ff868-108">常數</span><span class="sxs-lookup"><span data-stu-id="ff868-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ff868-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**</span><span class="sxs-lookup"><span data-stu-id="ff868-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="ff868-110">最大位元速率。</span><span class="sxs-lookup"><span data-stu-id="ff868-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="ff868-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**</span><span class="sxs-lookup"><span data-stu-id="ff868-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="ff868-112">最小位元速率。</span><span class="sxs-lookup"><span data-stu-id="ff868-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="ff868-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="ff868-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ff868-114">最大幀間隔。</span><span class="sxs-lookup"><span data-stu-id="ff868-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="ff868-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="ff868-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ff868-116">最小框架間隔。</span><span class="sxs-lookup"><span data-stu-id="ff868-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff868-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff868-117">Requirements</span></span>



| <span data-ttu-id="ff868-118">需求</span><span class="sxs-lookup"><span data-stu-id="ff868-118">Requirement</span></span> | <span data-ttu-id="ff868-119">值</span><span class="sxs-lookup"><span data-stu-id="ff868-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff868-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ff868-120">TAPI version</span></span><br/> | <span data-ttu-id="ff868-121">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="ff868-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="ff868-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ff868-122">Header</span></span><br/>       | <dl> <span data-ttu-id="ff868-123"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff868-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff868-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff868-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff868-125">**ITStreamQualityControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="ff868-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="ff868-126">**ITStreamQualityControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="ff868-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="ff868-127">**ITStreamQualityControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="ff868-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 





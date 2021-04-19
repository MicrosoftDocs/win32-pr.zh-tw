---
description: TAPI 串流設定 CAPS 結構會使用 StreamConfigCapsType 列舉 \_ 類型 \_ \_ 作為參數，指出是否牽涉到音訊或影片串流。
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: 'StreamConfigCapsType 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984890"
---
# <a name="streamconfigcapstype-enumeration"></a><span data-ttu-id="7d0ef-103">StreamConfigCapsType 列舉</span><span class="sxs-lookup"><span data-stu-id="7d0ef-103">StreamConfigCapsType enumeration</span></span>

<span data-ttu-id="7d0ef-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="7d0ef-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7d0ef-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="7d0ef-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7d0ef-106">[**TAPI \_ 串流設定 \_ \_ CAPS**](tapi-stream-config-caps.md)結構會使用 **StreamConfigCapsType** 列舉類型作為參數，指出是否牽涉到音訊或影片串流。</span><span class="sxs-lookup"><span data-stu-id="7d0ef-106">The **StreamConfigCapsType** enumeration type is used by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure as a switch to indicate whether audio or video streaming is involved.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d0ef-107">Syntax</span></span>


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a><span data-ttu-id="7d0ef-108">常數</span><span class="sxs-lookup"><span data-stu-id="7d0ef-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d0ef-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="7d0ef-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7d0ef-110">音訊串流設定。</span><span class="sxs-lookup"><span data-stu-id="7d0ef-110">Audio streaming configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7d0ef-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="7d0ef-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7d0ef-112">影片串流設定。</span><span class="sxs-lookup"><span data-stu-id="7d0ef-112">Video streaming configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d0ef-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d0ef-113">Requirements</span></span>



| <span data-ttu-id="7d0ef-114">需求</span><span class="sxs-lookup"><span data-stu-id="7d0ef-114">Requirement</span></span> | <span data-ttu-id="7d0ef-115">值</span><span class="sxs-lookup"><span data-stu-id="7d0ef-115">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0ef-116">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7d0ef-116">TAPI version</span></span><br/> | <span data-ttu-id="7d0ef-117">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="7d0ef-117">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="7d0ef-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7d0ef-118">Header</span></span><br/>       | <dl> <span data-ttu-id="7d0ef-119"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d0ef-119"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d0ef-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d0ef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0ef-121">**TAPI \_ 串流 \_ 設定 \_ CAP**</span><span class="sxs-lookup"><span data-stu-id="7d0ef-121">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 





---
description: PHONEHOOKSWITCHMODE \_ 位旗標常數描述 hookswitch 裝置的麥克風和喇叭元件。
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: 'PHONEHOOKSWITCHMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001235"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="041cb-103">PHONEHOOKSWITCHMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="041cb-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="041cb-104">**PHONEHOOKSWITCHMODE \_** 位旗標常數描述 hookswitch 裝置的麥克風和喇叭元件。</span><span class="sxs-lookup"><span data-stu-id="041cb-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="041cb-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE \_ MIC**</span><span class="sxs-lookup"><span data-stu-id="041cb-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041cb-106">裝置的麥克風處於作用中狀態，喇叭為靜音。</span><span class="sxs-lookup"><span data-stu-id="041cb-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="041cb-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**</span><span class="sxs-lookup"><span data-stu-id="041cb-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041cb-108">裝置的麥克風和說話者皆為作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="041cb-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="041cb-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE \_ ONHOOK**</span><span class="sxs-lookup"><span data-stu-id="041cb-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041cb-110">裝置的麥克風和說話者都是 onhook。</span><span class="sxs-lookup"><span data-stu-id="041cb-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="041cb-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ 喇叭**</span><span class="sxs-lookup"><span data-stu-id="041cb-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041cb-112">裝置的喇叭處於作用中狀態，麥克風為靜音。</span><span class="sxs-lookup"><span data-stu-id="041cb-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="041cb-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="041cb-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041cb-114">裝置的 hookswitch 模式目前未知。</span><span class="sxs-lookup"><span data-stu-id="041cb-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="041cb-115">備註</span><span class="sxs-lookup"><span data-stu-id="041cb-115">Remarks</span></span>

<span data-ttu-id="041cb-116">無延伸。</span><span class="sxs-lookup"><span data-stu-id="041cb-116">No extensibility.</span></span> <span data-ttu-id="041cb-117">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="041cb-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="041cb-118">這些常數可用來為手機裝置的麥克風和說話者元件提供個別的控制層級。</span><span class="sxs-lookup"><span data-stu-id="041cb-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="041cb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="041cb-119">Requirements</span></span>



| <span data-ttu-id="041cb-120">需求</span><span class="sxs-lookup"><span data-stu-id="041cb-120">Requirement</span></span> | <span data-ttu-id="041cb-121">值</span><span class="sxs-lookup"><span data-stu-id="041cb-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="041cb-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="041cb-122">TAPI version</span></span><br/> | <span data-ttu-id="041cb-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="041cb-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="041cb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="041cb-124">Header</span></span><br/>       | <dl> <span data-ttu-id="041cb-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="041cb-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 





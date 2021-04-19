---
description: PHONEHOOKSWITCHDEV \_ 位旗標常數會描述各種音訊 i/o 裝置，每個裝置都有自己的 hookswitch 能從電腦控制。
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: 'PHONEHOOKSWITCHDEV_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996115"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="98d33-103">PHONEHOOKSWITCHDEV \_ 常數</span><span class="sxs-lookup"><span data-stu-id="98d33-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="98d33-104">**PHONEHOOKSWITCHDEV \_** 位旗標常數會描述各種音訊 i/o 裝置，每個裝置都有自己的 hookswitch 能從電腦控制。</span><span class="sxs-lookup"><span data-stu-id="98d33-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="98d33-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV \_ 聽筒**</span><span class="sxs-lookup"><span data-stu-id="98d33-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="98d33-106">這是標準的 ear 和 mouthpiece 電話。</span><span class="sxs-lookup"><span data-stu-id="98d33-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d33-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV \_ 耳機**</span><span class="sxs-lookup"><span data-stu-id="98d33-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="98d33-108">這是連線到電話集合的耳機。</span><span class="sxs-lookup"><span data-stu-id="98d33-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d33-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ 喇叭**</span><span class="sxs-lookup"><span data-stu-id="98d33-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="98d33-110">這是內建的 loudspeaker 和麥克風。</span><span class="sxs-lookup"><span data-stu-id="98d33-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="98d33-111">這也可能是連至電話集合的外部連線附屬喇叭。</span><span class="sxs-lookup"><span data-stu-id="98d33-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98d33-112">備註</span><span class="sxs-lookup"><span data-stu-id="98d33-112">Remarks</span></span>

<span data-ttu-id="98d33-113">無延伸。</span><span class="sxs-lookup"><span data-stu-id="98d33-113">No extensibility.</span></span> <span data-ttu-id="98d33-114">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="98d33-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="98d33-115">這些常數會在 [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 資料結構中用來指出電話裝置的 hookswitch 裝置功能。</span><span class="sxs-lookup"><span data-stu-id="98d33-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="98d33-116">[**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus)結構會報告電話 hookswitch 裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="98d33-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="98d33-117">[**PhoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch)和 [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch)函式會使用它做為參數，以選取手機的 i/o 裝置。</span><span class="sxs-lookup"><span data-stu-id="98d33-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d33-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="98d33-118">Requirements</span></span>



| <span data-ttu-id="98d33-119">需求</span><span class="sxs-lookup"><span data-stu-id="98d33-119">Requirement</span></span> | <span data-ttu-id="98d33-120">值</span><span class="sxs-lookup"><span data-stu-id="98d33-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="98d33-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="98d33-121">TAPI version</span></span><br/> | <span data-ttu-id="98d33-122">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="98d33-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="98d33-123">標頭</span><span class="sxs-lookup"><span data-stu-id="98d33-123">Header</span></span><br/>       | <dl> <span data-ttu-id="98d33-124"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="98d33-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 





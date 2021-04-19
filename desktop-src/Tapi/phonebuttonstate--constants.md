---
description: PHONEBUTTONSTATE 位旗標常數描述按鈕的位置。
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: 'PHONEBUTTONSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001035"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="7e6ef-103">PHONEBUTTONSTATE_ 常數</span><span class="sxs-lookup"><span data-stu-id="7e6ef-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="7e6ef-104">**PHONEBUTTONSTATE_** 位旗標常數描述按鈕的位置。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="7e6ef-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="7e6ef-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e6ef-106">按鈕處於「關閉」狀態 (按下) 。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e6ef-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="7e6ef-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e6ef-108">指出服務提供者不知道按鈕的向上或向下狀態，而且未來將不會知道。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="7e6ef-109"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="7e6ef-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e6ef-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="7e6ef-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e6ef-111">指出目前不知道按鈕的向上或向下狀態，但未來可能會變成已知狀態。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="7e6ef-112"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="7e6ef-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e6ef-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="7e6ef-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e6ef-114">按鈕處於「up」狀態。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e6ef-115">備註</span><span class="sxs-lookup"><span data-stu-id="7e6ef-115">Remarks</span></span>

<span data-ttu-id="7e6ef-116">無延伸。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-116">No extensibility.</span></span> <span data-ttu-id="7e6ef-117">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="7e6ef-118">為了回溯相容性，服務提供者必須負責檢查手機上的已協商 API 版本，並且不使用所協商版本不支援的 PHONEBUTTONSTATE_ 值。</span><span class="sxs-lookup"><span data-stu-id="7e6ef-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6ef-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e6ef-119">Requirements</span></span>



| <span data-ttu-id="7e6ef-120">需求</span><span class="sxs-lookup"><span data-stu-id="7e6ef-120">Requirement</span></span> | <span data-ttu-id="7e6ef-121">值</span><span class="sxs-lookup"><span data-stu-id="7e6ef-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7e6ef-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7e6ef-122">TAPI version</span></span><br/> | <span data-ttu-id="7e6ef-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7e6ef-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7e6ef-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7e6ef-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7e6ef-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="7e6ef-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 





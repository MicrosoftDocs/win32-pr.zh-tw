---
description: 表示任何仍舊 (的 PGC、Cell 或 VOBU) 的開頭。
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: 'EC_DVD_STILL_ON (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977631"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="acbc1-103">EC \_ DVD \_ 仍 \_ 在開啟</span><span class="sxs-lookup"><span data-stu-id="acbc1-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="acbc1-104">表示任何仍舊 (的 PGC、Cell 或 VOBU) 的開頭。</span><span class="sxs-lookup"><span data-stu-id="acbc1-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="acbc1-105">參數</span><span class="sxs-lookup"><span data-stu-id="acbc1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbc1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="acbc1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="acbc1-107">布林值 (**BOOL**) 指出按鈕是否可用的值。</span><span class="sxs-lookup"><span data-stu-id="acbc1-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="acbc1-108">零 (0) 表示按鈕可供使用，因此 [**IDvdControl2：： StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) 方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="acbc1-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="acbc1-109">一個 (1) 表示沒有可用的按鈕，因此 **IDvdControl2：： StillOff** 可運作。</span><span class="sxs-lookup"><span data-stu-id="acbc1-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="acbc1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="acbc1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="acbc1-111">**DWORD** 值，指出仍會持續的秒數。</span><span class="sxs-lookup"><span data-stu-id="acbc1-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="acbc1-112">0xFFFFFFFF 表示仍無限制，這表示要等到使用者按下按鈕，或直到應用程式呼叫 [**IDvdControl2：： StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)為止。</span><span class="sxs-lookup"><span data-stu-id="acbc1-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acbc1-113">備註</span><span class="sxs-lookup"><span data-stu-id="acbc1-113">Remarks</span></span>

<span data-ttu-id="acbc1-114">所有按鈕的組合和仍可 (按鈕在上仍開啟的按鈕、具有仍然關閉的按鈕、按下 [開啟] 按鈕、按下 [開啟]、[仍關閉]) 。</span><span class="sxs-lookup"><span data-stu-id="acbc1-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="acbc1-115">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="acbc1-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbc1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="acbc1-116">Requirements</span></span>



| <span data-ttu-id="acbc1-117">需求</span><span class="sxs-lookup"><span data-stu-id="acbc1-117">Requirement</span></span> | <span data-ttu-id="acbc1-118">值</span><span class="sxs-lookup"><span data-stu-id="acbc1-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbc1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="acbc1-119">Header</span></span><br/> | <dl> <span data-ttu-id="acbc1-120"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="acbc1-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbc1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acbc1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbc1-122">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="acbc1-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="acbc1-123">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="acbc1-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="acbc1-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="acbc1-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





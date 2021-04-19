---
description: 表示已起始 DVD 播放的速率變更。
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: 'EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990583"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="3ddd4-103">EC \_ DVD \_ 播放 \_ 速率 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="3ddd4-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="3ddd4-104">表示已起始 DVD 播放的速率變更。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ddd4-105">參數</span><span class="sxs-lookup"><span data-stu-id="3ddd4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddd4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3ddd4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3ddd4-107">長時程表示新的播放速率。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="3ddd4-108">值是實際的播放率乘以10000，因此播放速率等於 10000.0/ *lParam1*。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="3ddd4-109">小於零的值表示反向播放模式，而大於零的值表示向前播放模式。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="3ddd4-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3ddd4-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3ddd4-111">零個。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ddd4-112">備註</span><span class="sxs-lookup"><span data-stu-id="3ddd4-112">Remarks</span></span>

<span data-ttu-id="3ddd4-113">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="3ddd4-114">播放 *速率* 是播放 *速度* 的反向。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="3ddd4-115">例如，如果播放速度為2x，則速率為0.5。</span><span class="sxs-lookup"><span data-stu-id="3ddd4-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddd4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ddd4-116">Requirements</span></span>



| <span data-ttu-id="3ddd4-117">需求</span><span class="sxs-lookup"><span data-stu-id="3ddd4-117">Requirement</span></span> | <span data-ttu-id="3ddd4-118">值</span><span class="sxs-lookup"><span data-stu-id="3ddd4-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddd4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3ddd4-119">Header</span></span><br/> | <dl> <span data-ttu-id="3ddd4-120"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="3ddd4-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddd4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ddd4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddd4-122">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="3ddd4-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3ddd4-123">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="3ddd4-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3ddd4-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="3ddd4-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





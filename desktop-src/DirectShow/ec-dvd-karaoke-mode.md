---
description: 表示 DVD 導覽器已開始播放或完成播放卡拉卡拉卡拉的資料。
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: 'EC_DVD_KARAOKE_MODE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995256"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="9f5e5-103">EC \_ DVD \_ 卡拉卡拉 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="9f5e5-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="9f5e5-104">表示 DVD 導覽 [器](data-flow-in-the-dvd-navigator.md) 已開始播放或完成播放卡拉卡拉卡拉的資料。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f5e5-105">參數</span><span class="sxs-lookup"><span data-stu-id="9f5e5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5e5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9f5e5-107">布林值。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-107">Boolean value.</span></span> <span data-ttu-id="9f5e5-108">若 **為 TRUE**，表示現正播放卡拉卡拉軌。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="9f5e5-109">否則，就不會播放任何的卡拉 ok 曲目。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="9f5e5-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9f5e5-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f5e5-112">備註</span><span class="sxs-lookup"><span data-stu-id="9f5e5-112">Remarks</span></span>

<span data-ttu-id="9f5e5-113">只要 DVD 播放機變更網域，就會對此事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="9f5e5-114">此事件會在所有 DVD 網域中引發。</span><span class="sxs-lookup"><span data-stu-id="9f5e5-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f5e5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f5e5-115">Requirements</span></span>



| <span data-ttu-id="9f5e5-116">需求</span><span class="sxs-lookup"><span data-stu-id="9f5e5-116">Requirement</span></span> | <span data-ttu-id="9f5e5-117">值</span><span class="sxs-lookup"><span data-stu-id="9f5e5-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5e5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9f5e5-118">Header</span></span><br/> | <dl> <span data-ttu-id="9f5e5-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="9f5e5-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f5e5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f5e5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f5e5-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="9f5e5-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="9f5e5-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="9f5e5-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9f5e5-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="9f5e5-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





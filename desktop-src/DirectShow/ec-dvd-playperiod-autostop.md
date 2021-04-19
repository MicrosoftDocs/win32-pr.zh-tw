---
description: 指出導覽器已完成播放 IDvdControl2：:P layPeriodInTitleAutoStop 呼叫中指定的區段。
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: 'EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993296"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="86287-103">EC \_ DVD \_ PLAYPERIOD \_ AUTOSTOP</span><span class="sxs-lookup"><span data-stu-id="86287-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="86287-104">指出導覽器已完成播放 [**IDvdControl2：:P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)呼叫中指定的區段。</span><span class="sxs-lookup"><span data-stu-id="86287-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="86287-105">參數</span><span class="sxs-lookup"><span data-stu-id="86287-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86287-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="86287-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="86287-107">零個。</span><span class="sxs-lookup"><span data-stu-id="86287-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="86287-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="86287-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="86287-109">零個。</span><span class="sxs-lookup"><span data-stu-id="86287-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86287-110">備註</span><span class="sxs-lookup"><span data-stu-id="86287-110">Remarks</span></span>

<span data-ttu-id="86287-111">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="86287-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="86287-112">在導覽器完成播放指定的區段之前，也會一併傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="86287-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="86287-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="86287-113">Requirements</span></span>



| <span data-ttu-id="86287-114">需求</span><span class="sxs-lookup"><span data-stu-id="86287-114">Requirement</span></span> | <span data-ttu-id="86287-115">值</span><span class="sxs-lookup"><span data-stu-id="86287-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86287-116">標頭</span><span class="sxs-lookup"><span data-stu-id="86287-116">Header</span></span><br/> | <dl> <span data-ttu-id="86287-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="86287-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86287-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86287-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86287-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="86287-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="86287-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="86287-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="86287-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="86287-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="86287-122">**IDvdControl2：:P layPeriodInTitleAutoStop**</span><span class="sxs-lookup"><span data-stu-id="86287-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 





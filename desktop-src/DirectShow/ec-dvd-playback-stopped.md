---
description: 表示 DVD 播放已停止。 當標題或章節完成，而且 DVD 導覽器找不到任何其他分支指示以進行後續播放時，就會傳送此事件。 當應用程式停止播放時，不會傳送此事件。
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: 'EC_DVD_PLAYBACK_STOPPED (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000749"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="05f21-105">EC \_ DVD \_ 播放 \_ 已停止</span><span class="sxs-lookup"><span data-stu-id="05f21-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="05f21-106">表示 DVD 播放已停止。</span><span class="sxs-lookup"><span data-stu-id="05f21-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="05f21-107">當標題或章節完成，而且 [DVD 導覽器](dvd-navigator-filter.md) 找不到任何其他分支指示以進行後續播放時，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="05f21-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="05f21-108">當應用程式停止播放時，不會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="05f21-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="05f21-109">參數</span><span class="sxs-lookup"><span data-stu-id="05f21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f21-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="05f21-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="05f21-111">[**DVD \_ PB \_ 已停止**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped)列舉的成員，表示播放停止的原因。</span><span class="sxs-lookup"><span data-stu-id="05f21-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="05f21-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="05f21-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="05f21-113">零個。</span><span class="sxs-lookup"><span data-stu-id="05f21-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05f21-114">備註</span><span class="sxs-lookup"><span data-stu-id="05f21-114">Remarks</span></span>

<span data-ttu-id="05f21-115">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="05f21-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f21-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f21-116">Requirements</span></span>



| <span data-ttu-id="05f21-117">需求</span><span class="sxs-lookup"><span data-stu-id="05f21-117">Requirement</span></span> | <span data-ttu-id="05f21-118">值</span><span class="sxs-lookup"><span data-stu-id="05f21-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f21-119">標頭</span><span class="sxs-lookup"><span data-stu-id="05f21-119">Header</span></span><br/> | <dl> <span data-ttu-id="05f21-120"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="05f21-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f21-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f21-122">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="05f21-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="05f21-123">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="05f21-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="05f21-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="05f21-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





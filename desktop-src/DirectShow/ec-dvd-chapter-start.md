---
description: 指示 DVD 播放程式在 DVD \_ 網域標題網域中開始播放新程式 \_ 。
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: 'EC_DVD_CHAPTER_START (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990107"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="4cf0c-103">EC \_ DVD \_ 章節 \_ 入門</span><span class="sxs-lookup"><span data-stu-id="4cf0c-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="4cf0c-104">指示 DVD 播放程式在 DVD \_ 網域標題網域中開始播放新程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4cf0c-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cf0c-105">參數</span><span class="sxs-lookup"><span data-stu-id="4cf0c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf0c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4cf0c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4cf0c-107">**DWORD** 值，指出新的章節 (程式) 號碼。</span><span class="sxs-lookup"><span data-stu-id="4cf0c-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="4cf0c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4cf0c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4cf0c-109">零個。</span><span class="sxs-lookup"><span data-stu-id="4cf0c-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cf0c-110">備註</span><span class="sxs-lookup"><span data-stu-id="4cf0c-110">Remarks</span></span>

<span data-ttu-id="4cf0c-111">只有簡單的線性電影會發出此事件的信號。</span><span class="sxs-lookup"><span data-stu-id="4cf0c-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="4cf0c-112">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="4cf0c-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf0c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cf0c-113">Requirements</span></span>



| <span data-ttu-id="4cf0c-114">需求</span><span class="sxs-lookup"><span data-stu-id="4cf0c-114">Requirement</span></span> | <span data-ttu-id="4cf0c-115">值</span><span class="sxs-lookup"><span data-stu-id="4cf0c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf0c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4cf0c-116">Header</span></span><br/> | <dl> <span data-ttu-id="4cf0c-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="4cf0c-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf0c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cf0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf0c-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="4cf0c-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="4cf0c-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="4cf0c-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4cf0c-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="4cf0c-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="4cf0c-122">**DVD \_ 網域列舉**</span><span class="sxs-lookup"><span data-stu-id="4cf0c-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 





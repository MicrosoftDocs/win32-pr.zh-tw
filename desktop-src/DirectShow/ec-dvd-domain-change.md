---
description: 表示 DVD 播放機的新網域。
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: 'EC_DVD_DOMAIN_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995929"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="da013-103">EC \_ DVD \_ 網域 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="da013-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="da013-104">表示 DVD 播放機的新網域。</span><span class="sxs-lookup"><span data-stu-id="da013-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="da013-105">參數</span><span class="sxs-lookup"><span data-stu-id="da013-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da013-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="da013-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="da013-107">表示新網域的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="da013-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="da013-108">[**DVD \_ 網域**](/windows/win32/api/strmif/ne-strmif-dvd_domain)的成員列舉資料類型。</span><span class="sxs-lookup"><span data-stu-id="da013-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="da013-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="da013-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="da013-110">零個。</span><span class="sxs-lookup"><span data-stu-id="da013-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da013-111">備註</span><span class="sxs-lookup"><span data-stu-id="da013-111">Remarks</span></span>

<span data-ttu-id="da013-112">只要 DVD 播放機變更網域，就會對此事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="da013-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="da013-113">此事件會在所有 DVD 網域中引發。</span><span class="sxs-lookup"><span data-stu-id="da013-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="da013-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="da013-114">Requirements</span></span>



| <span data-ttu-id="da013-115">需求</span><span class="sxs-lookup"><span data-stu-id="da013-115">Requirement</span></span> | <span data-ttu-id="da013-116">值</span><span class="sxs-lookup"><span data-stu-id="da013-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da013-117">標頭</span><span class="sxs-lookup"><span data-stu-id="da013-117">Header</span></span><br/> | <dl> <span data-ttu-id="da013-118"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="da013-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da013-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da013-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da013-120">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="da013-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="da013-121">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="da013-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="da013-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="da013-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





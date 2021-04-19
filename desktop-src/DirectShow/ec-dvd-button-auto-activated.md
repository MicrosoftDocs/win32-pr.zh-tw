---
description: 表示 DVD 功能表按鈕已根據光碟上的指示自動啟用。發生這種情況時，當功能表超時且光碟已指定要自動啟用的按鈕時。
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: 'EC_DVD_BUTTON_AUTO_ACTI加值稅ED (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984378"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="826a8-103">\_ \_ \_ 自動啟用 EC DVD \_ 按鈕</span><span class="sxs-lookup"><span data-stu-id="826a8-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="826a8-104">表示 DVD 功能表按鈕已根據光碟上的指示自動啟用。發生這種情況時，當功能表超時且光碟已指定要自動啟用的按鈕時。</span><span class="sxs-lookup"><span data-stu-id="826a8-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="826a8-105">參數</span><span class="sxs-lookup"><span data-stu-id="826a8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826a8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="826a8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="826a8-107">**DWORD** 值，表示已啟用的按鈕。</span><span class="sxs-lookup"><span data-stu-id="826a8-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="826a8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="826a8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="826a8-109">零個。</span><span class="sxs-lookup"><span data-stu-id="826a8-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="826a8-110">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="826a8-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="826a8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="826a8-111">Requirements</span></span>



| <span data-ttu-id="826a8-112">需求</span><span class="sxs-lookup"><span data-stu-id="826a8-112">Requirement</span></span> | <span data-ttu-id="826a8-113">值</span><span class="sxs-lookup"><span data-stu-id="826a8-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826a8-114">標頭</span><span class="sxs-lookup"><span data-stu-id="826a8-114">Header</span></span><br/> | <dl> <span data-ttu-id="826a8-115"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="826a8-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826a8-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="826a8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826a8-117">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="826a8-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="826a8-118">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="826a8-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="826a8-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="826a8-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





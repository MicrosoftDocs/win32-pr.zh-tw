---
description: 當 VMR 7's 配置器展示者在呈現的介面上呼叫 DirectDraw Flip 方法時傳送。 這可讓 VMR 將其 DirectXVA 資料表與 DirectDraw 的翻轉鏈同步處理。
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: 'EC_VMR_SURFACE_FLIPPED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993513"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="e9bb6-104">已 \_ 翻轉 EC VMR \_ 介面 \_</span><span class="sxs-lookup"><span data-stu-id="e9bb6-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="e9bb6-105">當 VMR 7's 配置器展示者在呈現的介面上呼叫 DirectDraw Flip 方法時傳送。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="e9bb6-106">這可讓 VMR 將其 DirectXVA 資料表與 DirectDraw 的翻轉鏈同步處理。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9bb6-107">參數</span><span class="sxs-lookup"><span data-stu-id="e9bb6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9bb6-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e9bb6-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e9bb6-109"> (**HRESULT**) 從 DirectDraw Flip 方法傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="e9bb6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e9bb6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e9bb6-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9bb6-112">備註</span><span class="sxs-lookup"><span data-stu-id="e9bb6-112">Remarks</span></span>

<span data-ttu-id="e9bb6-113">自訂配置器-VMR-7 的展示者應該傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="e9bb6-114">此事件不會轉送至應用程式，而且不會與 VMR-9 的配置器-展示者一起使用。</span><span class="sxs-lookup"><span data-stu-id="e9bb6-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bb6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9bb6-115">Requirements</span></span>



| <span data-ttu-id="e9bb6-116">需求</span><span class="sxs-lookup"><span data-stu-id="e9bb6-116">Requirement</span></span> | <span data-ttu-id="e9bb6-117">值</span><span class="sxs-lookup"><span data-stu-id="e9bb6-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bb6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e9bb6-118">Header</span></span><br/> | <dl> <span data-ttu-id="e9bb6-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb6-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bb6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9bb6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bb6-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="e9bb6-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e9bb6-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="e9bb6-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





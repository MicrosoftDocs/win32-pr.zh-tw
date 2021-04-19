---
description: 表示 IDvdControl2 介面方法的可用集合已變更。
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: 'EC_DVD_VALID_UOPS_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992872"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="23d1d-103">EC \_ DVD \_ 有效 \_ UOPS \_ 變更</span><span class="sxs-lookup"><span data-stu-id="23d1d-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="23d1d-104">表示 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面方法的可用集合已變更。</span><span class="sxs-lookup"><span data-stu-id="23d1d-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="23d1d-105">參數</span><span class="sxs-lookup"><span data-stu-id="23d1d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d1d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="23d1d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="23d1d-107">**DWORD** 值，包含來自 [**有效 \_ UOP \_ 旗**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) 標列舉的零或多個旗標組合。</span><span class="sxs-lookup"><span data-stu-id="23d1d-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="23d1d-108">這些位會指出 DVD 光碟明確停用的 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 命令。</span><span class="sxs-lookup"><span data-stu-id="23d1d-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="23d1d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="23d1d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="23d1d-110">零個。</span><span class="sxs-lookup"><span data-stu-id="23d1d-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23d1d-111">備註</span><span class="sxs-lookup"><span data-stu-id="23d1d-111">Remarks</span></span>

<span data-ttu-id="23d1d-112">此事件表示 DVD 光碟上的內容只會明確停用的作業。它不保證呼叫未停用的方法是有效的。</span><span class="sxs-lookup"><span data-stu-id="23d1d-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="23d1d-113">例如，如果沒有任何按鈕， [**IDvdControl2：： ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) 方法將無法運作，即使方法未明確停用也是一樣。</span><span class="sxs-lookup"><span data-stu-id="23d1d-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="23d1d-114">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="23d1d-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d1d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="23d1d-115">Requirements</span></span>



| <span data-ttu-id="23d1d-116">需求</span><span class="sxs-lookup"><span data-stu-id="23d1d-116">Requirement</span></span> | <span data-ttu-id="23d1d-117">值</span><span class="sxs-lookup"><span data-stu-id="23d1d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d1d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="23d1d-118">Header</span></span><br/> | <dl> <span data-ttu-id="23d1d-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="23d1d-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d1d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23d1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d1d-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="23d1d-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="23d1d-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="23d1d-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="23d1d-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="23d1d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





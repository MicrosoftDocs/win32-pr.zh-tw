---
description: 支援最多三個欄位的每個使用者事件。
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: 'WPCEVENT_CUSTOM (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192613"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="b160e-103">WPCEVENT \_ 自訂事件</span><span class="sxs-lookup"><span data-stu-id="b160e-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="b160e-104">支援最多三個欄位的每個使用者事件。</span><span class="sxs-lookup"><span data-stu-id="b160e-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="b160e-105">事件會顯示在 **活動檢視器** 中， **另** 一個區段具有下列階層：</span><span class="sxs-lookup"><span data-stu-id="b160e-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="b160e-106">Publisher</span><span class="sxs-lookup"><span data-stu-id="b160e-106">Publisher</span></span>

2.  <span data-ttu-id="b160e-107">應用程式</span><span class="sxs-lookup"><span data-stu-id="b160e-107">Application</span></span>

3.  <span data-ttu-id="b160e-108">事件</span><span class="sxs-lookup"><span data-stu-id="b160e-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="b160e-109">參數</span><span class="sxs-lookup"><span data-stu-id="b160e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b160e-110">*發行者*</span><span class="sxs-lookup"><span data-stu-id="b160e-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-111">事件的發行者 (例如) 的公司名稱。</span><span class="sxs-lookup"><span data-stu-id="b160e-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="b160e-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="b160e-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-113">產生事件的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b160e-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="b160e-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-115">產生事件之應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="b160e-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-116">*事件*</span><span class="sxs-lookup"><span data-stu-id="b160e-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-117">事件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b160e-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-118">*Value1*</span><span class="sxs-lookup"><span data-stu-id="b160e-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-119">自訂欄位1。</span><span class="sxs-lookup"><span data-stu-id="b160e-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="b160e-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-121">自訂欄位2。</span><span class="sxs-lookup"><span data-stu-id="b160e-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-122">*Value3*</span><span class="sxs-lookup"><span data-stu-id="b160e-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-123">自訂欄位3。</span><span class="sxs-lookup"><span data-stu-id="b160e-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-124">*封鎖*</span><span class="sxs-lookup"><span data-stu-id="b160e-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-125">[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。</span><span class="sxs-lookup"><span data-stu-id="b160e-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="b160e-126">*原因*</span><span class="sxs-lookup"><span data-stu-id="b160e-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="b160e-127">提供有關封鎖或不封鎖原因之額外資訊的自訂字串。</span><span class="sxs-lookup"><span data-stu-id="b160e-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b160e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b160e-128">Requirements</span></span>



| <span data-ttu-id="b160e-129">需求</span><span class="sxs-lookup"><span data-stu-id="b160e-129">Requirement</span></span> | <span data-ttu-id="b160e-130">值</span><span class="sxs-lookup"><span data-stu-id="b160e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b160e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b160e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b160e-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b160e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b160e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b160e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b160e-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="b160e-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="b160e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b160e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b160e-136"><dt>Wpcevent。h</dt></span><span class="sxs-lookup"><span data-stu-id="b160e-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b160e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b160e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b160e-138">使用適用于家長監護的記錄 Api</span><span class="sxs-lookup"><span data-stu-id="b160e-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="b160e-139">**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="b160e-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





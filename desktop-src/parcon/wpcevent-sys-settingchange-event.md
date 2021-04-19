---
description: 父控制項設定變更時產生的系統層級事件。
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: 'WPCEVENT_SYS_SETTINGCHANGE (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978375"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="f894b-103">WPCEVENT \_ SYS \_ SETTINGCHANGE 事件</span><span class="sxs-lookup"><span data-stu-id="f894b-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="f894b-104">父控制項設定變更時產生的系統層級事件。</span><span class="sxs-lookup"><span data-stu-id="f894b-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="f894b-105">參數</span><span class="sxs-lookup"><span data-stu-id="f894b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f894b-106">*類別*</span><span class="sxs-lookup"><span data-stu-id="f894b-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-107">產生事件的類別。</span><span class="sxs-lookup"><span data-stu-id="f894b-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-108">*設定*</span><span class="sxs-lookup"><span data-stu-id="f894b-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-109">**WPC \_ 設定** 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="f894b-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-110">*擁有者*</span><span class="sxs-lookup"><span data-stu-id="f894b-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-111">正在產生事件之使用者的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="f894b-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-112">*OldVal*</span><span class="sxs-lookup"><span data-stu-id="f894b-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-113">此設定的先前值（如果已刪除或已變更）。</span><span class="sxs-lookup"><span data-stu-id="f894b-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="f894b-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-115">此設定的新值（如果已加入或已變更）。</span><span class="sxs-lookup"><span data-stu-id="f894b-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-116">*原因*</span><span class="sxs-lookup"><span data-stu-id="f894b-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-117">[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。</span><span class="sxs-lookup"><span data-stu-id="f894b-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="f894b-118">*選擇性*</span><span class="sxs-lookup"><span data-stu-id="f894b-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="f894b-119">選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="f894b-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f894b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f894b-120">Requirements</span></span>



| <span data-ttu-id="f894b-121">需求</span><span class="sxs-lookup"><span data-stu-id="f894b-121">Requirement</span></span> | <span data-ttu-id="f894b-122">值</span><span class="sxs-lookup"><span data-stu-id="f894b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f894b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f894b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f894b-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f894b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f894b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f894b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f894b-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="f894b-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f894b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f894b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f894b-128"><dt>Wpcevent。h</dt></span><span class="sxs-lookup"><span data-stu-id="f894b-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f894b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f894b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f894b-130">使用適用于家長監護的記錄 Api</span><span class="sxs-lookup"><span data-stu-id="f894b-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="f894b-131">**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="f894b-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





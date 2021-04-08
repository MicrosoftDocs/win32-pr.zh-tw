---
title: 'UDN_DELTAPOS (Commctrl 的通知碼) '
description: 當控制項的位置即將變更時，作業系統會將其傳送至上下按鈕控制項的父視窗。
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685953"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="97948-104">UDN \_ DELTAPOS 通知碼</span><span class="sxs-lookup"><span data-stu-id="97948-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="97948-105">當控制項的位置即將變更時，作業系統會將其傳送至上下按鈕控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="97948-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="97948-106">當使用者按下控制項的向上或向下箭號時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="97948-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="97948-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="97948-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="97948-108">參數</span><span class="sxs-lookup"><span data-stu-id="97948-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97948-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97948-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97948-110">[**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown)結構的指標，其中包含位置變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97948-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="97948-111">此結構的 **iPos** 成員包含控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="97948-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="97948-112">結構的 **iDelta** 成員是帶正負號的整數，其中包含位置的建議變更。</span><span class="sxs-lookup"><span data-stu-id="97948-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="97948-113">如果使用者按一下 [向上] 按鈕，這就是正值。</span><span class="sxs-lookup"><span data-stu-id="97948-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="97948-114">如果使用者按一下 [向下] 按鈕，則此值為負值。</span><span class="sxs-lookup"><span data-stu-id="97948-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97948-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="97948-115">Return value</span></span>

<span data-ttu-id="97948-116">傳回非零以防止控制項的位置變更，或傳回零以允許變更。</span><span class="sxs-lookup"><span data-stu-id="97948-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="97948-117">備註</span><span class="sxs-lookup"><span data-stu-id="97948-117">Remarks</span></span>

<span data-ttu-id="97948-118">UDN \_ DELTAPOS 通知碼會在 [**wm \_ VSCROLL**](wm-vscroll.md) 或 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息之前傳送，這會實際變更控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="97948-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="97948-119">這可讓您檢查、允許、修改或禁止變更。</span><span class="sxs-lookup"><span data-stu-id="97948-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="97948-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="97948-120">Requirements</span></span>



| <span data-ttu-id="97948-121">需求</span><span class="sxs-lookup"><span data-stu-id="97948-121">Requirement</span></span> | <span data-ttu-id="97948-122">值</span><span class="sxs-lookup"><span data-stu-id="97948-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97948-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97948-123">Minimum supported client</span></span><br/> | <span data-ttu-id="97948-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97948-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97948-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97948-125">Minimum supported server</span></span><br/> | <span data-ttu-id="97948-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97948-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97948-127">標頭</span><span class="sxs-lookup"><span data-stu-id="97948-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="97948-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="97948-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97948-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97948-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97948-130">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="97948-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


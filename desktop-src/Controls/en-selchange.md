---
title: 'EN_SELCHANGE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，指出目前的選取範圍已變更。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686290"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="03a8c-105">EN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="03a8c-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="03a8c-106">通知 rich edit 控制項的父視窗，指出目前的選取範圍已變更。</span><span class="sxs-lookup"><span data-stu-id="03a8c-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="03a8c-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="03a8c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="03a8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="03a8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03a8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03a8c-110">[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)結構，可接收選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="03a8c-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a8c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="03a8c-111">Return value</span></span>

<span data-ttu-id="03a8c-112">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="03a8c-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03a8c-113">備註</span><span class="sxs-lookup"><span data-stu-id="03a8c-113">Remarks</span></span>

<span data-ttu-id="03a8c-114">若要接收 EN \_ SELCHANGE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="03a8c-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="03a8c-115">當插入號位置變更，但未選取任何文字時，就會傳送此通知碼 (選取範圍是空的) 。</span><span class="sxs-lookup"><span data-stu-id="03a8c-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="03a8c-116">當使用者按一下滑鼠、輸入或按下方向鍵時，插入號位置可能會變更。</span><span class="sxs-lookup"><span data-stu-id="03a8c-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a8c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="03a8c-117">Requirements</span></span>



| <span data-ttu-id="03a8c-118">需求</span><span class="sxs-lookup"><span data-stu-id="03a8c-118">Requirement</span></span> | <span data-ttu-id="03a8c-119">值</span><span class="sxs-lookup"><span data-stu-id="03a8c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03a8c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03a8c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03a8c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a8c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03a8c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03a8c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03a8c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a8c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03a8c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="03a8c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a8c-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="03a8c-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a8c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03a8c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="03a8c-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="03a8c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="03a8c-128">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="03a8c-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="03a8c-129">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="03a8c-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 






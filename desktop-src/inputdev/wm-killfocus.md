---
title: 'WM_KILLFOCUS 訊息 (Winuser .h) '
description: 在失去鍵盤焦點之前，立即傳送至視窗。
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024959"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="c873e-104">WM \_ KILLFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="c873e-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="c873e-105">在失去鍵盤焦點之前，立即傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="c873e-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="c873e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c873e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c873e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c873e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c873e-108">接收鍵盤焦點的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c873e-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="c873e-109">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c873e-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c873e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c873e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c873e-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c873e-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c873e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c873e-112">Return value</span></span>

<span data-ttu-id="c873e-113">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="c873e-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c873e-114">備註</span><span class="sxs-lookup"><span data-stu-id="c873e-114">Remarks</span></span>

<span data-ttu-id="c873e-115">如果應用程式顯示插入號，則應該在此時終結插入點。</span><span class="sxs-lookup"><span data-stu-id="c873e-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="c873e-116">處理此訊息時，請勿進行任何會顯示或啟動視窗的函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="c873e-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="c873e-117">這會導致執行緒產生控制權，而且可能會導致應用程式停止回應訊息。</span><span class="sxs-lookup"><span data-stu-id="c873e-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="c873e-118">如需詳細資訊，請參閱 [訊息鎖死](/windows/desktop/winmsg/about-messages-and-message-queues)。</span><span class="sxs-lookup"><span data-stu-id="c873e-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="c873e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c873e-119">Requirements</span></span>



| <span data-ttu-id="c873e-120">需求</span><span class="sxs-lookup"><span data-stu-id="c873e-120">Requirement</span></span> | <span data-ttu-id="c873e-121">值</span><span class="sxs-lookup"><span data-stu-id="c873e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c873e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c873e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c873e-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c873e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c873e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c873e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c873e-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c873e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c873e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c873e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c873e-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c873e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c873e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c873e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c873e-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="c873e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c873e-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="c873e-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="c873e-131">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="c873e-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="c873e-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="c873e-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c873e-133">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="c873e-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 


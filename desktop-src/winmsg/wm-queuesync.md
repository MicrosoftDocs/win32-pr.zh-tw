---
description: 以電腦為基礎的訓練 (CBT) 應用程式傳送，以將使用者輸入訊息與透過 WH JOURNALPLAYBACK 程式傳送的其他訊息分開 \_ 。
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: 'WM_QUEUESYNC 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977330"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="f4d7a-103">WM \_ QUEUESYNC 訊息</span><span class="sxs-lookup"><span data-stu-id="f4d7a-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="f4d7a-104">以電腦為基礎的訓練 (CBT) 應用程式傳送，以將使用者輸入訊息與透過 [**WH \_ JOURNALPLAYBACK**](about-hooks.md) 程式傳送的其他訊息分開。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="f4d7a-105">參數</span><span class="sxs-lookup"><span data-stu-id="f4d7a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4d7a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4d7a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4d7a-107">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4d7a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4d7a-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4d7a-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4d7a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4d7a-110">Return value</span></span>

<span data-ttu-id="f4d7a-111">類型： **void**</span><span class="sxs-lookup"><span data-stu-id="f4d7a-111">Type: **void**</span></span>

<span data-ttu-id="f4d7a-112">如果 CBT 應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d7a-113">備註</span><span class="sxs-lookup"><span data-stu-id="f4d7a-113">Remarks</span></span>

<span data-ttu-id="f4d7a-114">每當 CBT 應用程式使用 [**WH \_ JOURNALPLAYBACK**](about-hooks.md) 程式時，第一個和最後一則訊息為 **WM \_ QUEUESYNC**。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="f4d7a-115">這可讓 CBT 應用程式攔截並檢查使用者起始的訊息，而不需要針對其所傳送的事件執行此動作。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="f4d7a-116">如果應用程式指定 **Null** 視窗控制碼，則會將訊息張貼至使用中視窗的訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="f4d7a-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d7a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4d7a-117">Requirements</span></span>



| <span data-ttu-id="f4d7a-118">需求</span><span class="sxs-lookup"><span data-stu-id="f4d7a-118">Requirement</span></span> | <span data-ttu-id="f4d7a-119">值</span><span class="sxs-lookup"><span data-stu-id="f4d7a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d7a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4d7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4d7a-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4d7a-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f4d7a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4d7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4d7a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4d7a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4d7a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f4d7a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4d7a-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f4d7a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4d7a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4d7a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4d7a-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="f4d7a-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="f4d7a-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4d7a-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f4d7a-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="f4d7a-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="f4d7a-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="f4d7a-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f4d7a-131">鉤</span><span class="sxs-lookup"><span data-stu-id="f4d7a-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 

---
description: 當計時器到期時，張貼至安裝執行緒的訊息佇列。 此訊息是由 GetMessage 或 PeekMessage 函數所張貼。
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: 'WM_TIMER 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194256"
---
# <a name="wm_timer-message"></a><span data-ttu-id="67660-104">WM \_ 計時器訊息</span><span class="sxs-lookup"><span data-stu-id="67660-104">WM\_TIMER message</span></span>

<span data-ttu-id="67660-105">當計時器到期時，張貼至安裝執行緒的訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="67660-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="67660-106">此訊息是由 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數所張貼。</span><span class="sxs-lookup"><span data-stu-id="67660-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="67660-107">參數</span><span class="sxs-lookup"><span data-stu-id="67660-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67660-108">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67660-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67660-109">計時器識別碼。</span><span class="sxs-lookup"><span data-stu-id="67660-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="67660-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67660-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67660-111">應用程式定義回呼函式的指標，該函式會在安裝計時器時傳遞給 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函數。</span><span class="sxs-lookup"><span data-stu-id="67660-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67660-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="67660-112">Return value</span></span>

<span data-ttu-id="67660-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="67660-113">Type: **LRESULT**</span></span>

<span data-ttu-id="67660-114">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="67660-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="67660-115">備註</span><span class="sxs-lookup"><span data-stu-id="67660-115">Remarks</span></span>

<span data-ttu-id="67660-116">您可以在視窗程式中提供 **WM \_ 計時器** 案例來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="67660-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="67660-117">否則， [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)會呼叫用來安裝計時器之 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)函式的呼叫中指定的 [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)回呼函數。</span><span class="sxs-lookup"><span data-stu-id="67660-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="67660-118">**WM \_ 計時器** 訊息是低優先順序的訊息。</span><span class="sxs-lookup"><span data-stu-id="67660-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="67660-119">只有當執行緒的訊息佇列中沒有其他較高優先順序的訊息時， [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 和 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式才會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="67660-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="67660-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="67660-120">Requirements</span></span>



| <span data-ttu-id="67660-121">需求</span><span class="sxs-lookup"><span data-stu-id="67660-121">Requirement</span></span> | <span data-ttu-id="67660-122">值</span><span class="sxs-lookup"><span data-stu-id="67660-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67660-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67660-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67660-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67660-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="67660-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67660-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67660-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67660-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67660-127">標頭</span><span class="sxs-lookup"><span data-stu-id="67660-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67660-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="67660-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67660-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67660-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="67660-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="67660-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67660-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="67660-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="67660-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="67660-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="67660-133">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="67660-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="67660-134">**TimerProc**</span><span class="sxs-lookup"><span data-stu-id="67660-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="67660-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="67660-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67660-136">計時器</span><span class="sxs-lookup"><span data-stu-id="67660-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 

---
description: 當應用程式要求透過呼叫 CreateWindowEx 或 CreateWindow 函數來建立視窗時傳送。
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: 'WM_CREATE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997828"
---
# <a name="wm_create-message"></a><span data-ttu-id="d146b-103">WM \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="d146b-103">WM\_CREATE message</span></span>

<span data-ttu-id="d146b-104">當應用程式要求透過呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 或 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數來建立視窗時傳送。</span><span class="sxs-lookup"><span data-stu-id="d146b-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="d146b-105"> (在函式傳回前傳送訊息。 ) 新視窗的視窗程式會在視窗建立之後，但視窗變成可見之前收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="d146b-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="d146b-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d146b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="d146b-107">參數</span><span class="sxs-lookup"><span data-stu-id="d146b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d146b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d146b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d146b-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d146b-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d146b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d146b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d146b-111">[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的指標，其中包含所要建立之視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d146b-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d146b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d146b-112">Return value</span></span>

<span data-ttu-id="d146b-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d146b-113">Type: **LRESULT**</span></span>

<span data-ttu-id="d146b-114">如果應用程式處理此訊息，則應該傳回零以繼續建立視窗。</span><span class="sxs-lookup"><span data-stu-id="d146b-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="d146b-115">如果應用程式傳回-1，則會終結視窗，且 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 或 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數會傳回 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="d146b-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="d146b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d146b-116">Requirements</span></span>



| <span data-ttu-id="d146b-117">需求</span><span class="sxs-lookup"><span data-stu-id="d146b-117">Requirement</span></span> | <span data-ttu-id="d146b-118">值</span><span class="sxs-lookup"><span data-stu-id="d146b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d146b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d146b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d146b-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d146b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d146b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d146b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d146b-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d146b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d146b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d146b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d146b-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d146b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d146b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d146b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d146b-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="d146b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d146b-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="d146b-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="d146b-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="d146b-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="d146b-129">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="d146b-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="d146b-130">**WM \_ NCCREATE**</span><span class="sxs-lookup"><span data-stu-id="d146b-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="d146b-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="d146b-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d146b-132">Windows</span><span class="sxs-lookup"><span data-stu-id="d146b-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 

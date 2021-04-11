---
description: 在終結視窗時傳送。 它會傳送至視窗從螢幕中移除之後終結的視窗程式。
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: 'WM_DESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193704"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="c1942-104">WM 損 \_ 毀訊息</span><span class="sxs-lookup"><span data-stu-id="c1942-104">WM\_DESTROY message</span></span>

<span data-ttu-id="c1942-105">在終結視窗時傳送。</span><span class="sxs-lookup"><span data-stu-id="c1942-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="c1942-106">它會傳送至視窗從螢幕中移除之後終結的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="c1942-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="c1942-107">這則訊息會先傳送至被終結的視窗，然後再傳送至子視窗 (是否有任何) 終結。</span><span class="sxs-lookup"><span data-stu-id="c1942-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="c1942-108">在訊息處理期間，可以假設所有子視窗仍然存在。</span><span class="sxs-lookup"><span data-stu-id="c1942-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="c1942-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c1942-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="c1942-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1942-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1942-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1942-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1942-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c1942-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1942-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1942-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1942-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c1942-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1942-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1942-115">Return value</span></span>

<span data-ttu-id="c1942-116">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1942-116">Type: **LRESULT**</span></span>

<span data-ttu-id="c1942-117">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c1942-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1942-118">備註</span><span class="sxs-lookup"><span data-stu-id="c1942-118">Remarks</span></span>

<span data-ttu-id="c1942-119">如果終結的視窗是剪貼簿檢視器鏈的一部分 (藉由呼叫 [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) 函式來設定) ，則在從 WM 終結訊息傳回之前，視窗必須先處理 [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) 函 **式 \_** ，以從鏈中移除本身。</span><span class="sxs-lookup"><span data-stu-id="c1942-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1942-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1942-120">Requirements</span></span>



| <span data-ttu-id="c1942-121">需求</span><span class="sxs-lookup"><span data-stu-id="c1942-121">Requirement</span></span> | <span data-ttu-id="c1942-122">值</span><span class="sxs-lookup"><span data-stu-id="c1942-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1942-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1942-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1942-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1942-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1942-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1942-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1942-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1942-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1942-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c1942-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1942-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c1942-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1942-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1942-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1942-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="c1942-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1942-131">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="c1942-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="c1942-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="c1942-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="c1942-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="c1942-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="c1942-134">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="c1942-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="c1942-135">**WM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c1942-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="c1942-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="c1942-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1942-137">Windows</span><span class="sxs-lookup"><span data-stu-id="c1942-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 

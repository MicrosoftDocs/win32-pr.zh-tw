---
description: 使用 WM \_ SYNCPAINT 訊息來同步處理繪製，同時避免連結獨立的 GUI 執行緒。
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: 'WM_SYNCPAINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991498"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="cfa09-103">WM \_ SYNCPAINT 訊息</span><span class="sxs-lookup"><span data-stu-id="cfa09-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="cfa09-104">使用 **WM \_ SYNCPAINT** 訊息來同步處理繪製，同時避免連結獨立的 GUI 執行緒。</span><span class="sxs-lookup"><span data-stu-id="cfa09-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="cfa09-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="cfa09-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="cfa09-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfa09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa09-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfa09-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa09-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="cfa09-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cfa09-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfa09-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa09-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="cfa09-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa09-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfa09-111">Return value</span></span>

<span data-ttu-id="cfa09-112">如果應用程式處理此訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="cfa09-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa09-113">備註</span><span class="sxs-lookup"><span data-stu-id="cfa09-113">Remarks</span></span>

<span data-ttu-id="cfa09-114">當視窗隱藏、顯示、移動或調整大小時，系統可能會判斷必須將 **WM \_ SYNCPAINT** 訊息傳送至其他執行緒的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="cfa09-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="cfa09-115">應用程式必須將 **WM \_ SYNCPAINT** 傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  進行處理。</span><span class="sxs-lookup"><span data-stu-id="cfa09-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="cfa09-116">如果必須繪製視窗框架， **DefWindowProc** 函式會將 [**wm \_ NCPAINT**](wm-ncpaint.md) 訊息傳送至視窗程式，並在視窗背景清除時傳送 [**wm \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="cfa09-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa09-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfa09-117">Requirements</span></span>



| <span data-ttu-id="cfa09-118">需求</span><span class="sxs-lookup"><span data-stu-id="cfa09-118">Requirement</span></span> | <span data-ttu-id="cfa09-119">值</span><span class="sxs-lookup"><span data-stu-id="cfa09-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa09-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfa09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa09-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfa09-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cfa09-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfa09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa09-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfa09-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfa09-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cfa09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa09-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cfa09-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa09-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfa09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa09-127">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="cfa09-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="cfa09-128">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="cfa09-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="cfa09-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cfa09-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cfa09-130">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="cfa09-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="cfa09-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="cfa09-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="cfa09-132">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="cfa09-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 

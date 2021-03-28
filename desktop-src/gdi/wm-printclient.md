---
description: 將 WM \_ PRINTCLIENT 訊息傳送至視窗，要求它在指定的裝置內容中繪製其工作區，最常見的是在印表機裝置內容中。
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: 'WM_PRINTCLIENT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973512"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="f9f3e-103">WM \_ PRINTCLIENT 訊息</span><span class="sxs-lookup"><span data-stu-id="f9f3e-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="f9f3e-104">將 **WM \_ PRINTCLIENT** 訊息傳送至視窗，要求它在指定的裝置內容中繪製其工作區，最常見的是在印表機裝置內容中。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="f9f3e-105">與 [**wm \_ 列印**](wm-print.md)不同的是， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)不會處理 **wm \_ PRINTCLIENT** 。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="f9f3e-106">視窗應該透過應用程式定義的 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))函式來處理 **WM \_ PRINTCLIENT** 訊息，才能正確地使用它。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="f9f3e-107">參數</span><span class="sxs-lookup"><span data-stu-id="f9f3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f3e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9f3e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f3e-109">要在其中繪製的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="f9f3e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9f3e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f3e-111">繪圖選項。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-111">The drawing options.</span></span> <span data-ttu-id="f9f3e-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="f9f3e-113">值</span><span class="sxs-lookup"><span data-stu-id="f9f3e-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="f9f3e-114">意義</span><span class="sxs-lookup"><span data-stu-id="f9f3e-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="f9f3e-115"><dt>**PRF \_ CHECKVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="f9f3e-116">只有當視窗可見時，才會繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="f9f3e-117"><dt>**PRF \_ 子系**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="f9f3e-118">繪製所有可見的子系視窗。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="f9f3e-119"><dt>**PRF \_ 用戶端**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="f9f3e-120">繪製視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="f9f3e-121"><dt>**PRF \_ ERASEBKGND**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="f9f3e-122">在繪製視窗之前清除背景。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="f9f3e-123"><dt>**PRF \_ 非工作區**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="f9f3e-124">繪製視窗的非工作區。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="f9f3e-125"><dt>**\_所擁有的 PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="f9f3e-126">繪製所有擁有的視窗。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9f3e-127">備註</span><span class="sxs-lookup"><span data-stu-id="f9f3e-127">Remarks</span></span>

<span data-ttu-id="f9f3e-128">視窗可以用與 [**WM \_ 油漆**](./wm-paint.md)相同的方式來處理此訊息，但不需要呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) () 提供裝置內容，而且視窗應該繪製其整個工作區，而不只是不正確區域。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="f9f3e-129">可以在系統中任何地方使用的視窗（例如控制項）都應該處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="f9f3e-130">其他視窗也可能需要處理此訊息，因為它相當容易執行。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="f9f3e-131">[AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow)函式要求以動畫顯示的視窗必須執行 **WM \_ PRINTCLIENT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f9f3e-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f3e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9f3e-132">Requirements</span></span>



| <span data-ttu-id="f9f3e-133">需求</span><span class="sxs-lookup"><span data-stu-id="f9f3e-133">Requirement</span></span> | <span data-ttu-id="f9f3e-134">值</span><span class="sxs-lookup"><span data-stu-id="f9f3e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f3e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9f3e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f3e-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f3e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f9f3e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9f3e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f3e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f3e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9f3e-139">標頭</span><span class="sxs-lookup"><span data-stu-id="f9f3e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f3e-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f9f3e-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f3e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9f3e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f3e-142">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="f9f3e-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="f9f3e-143">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="f9f3e-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="f9f3e-144">**AnimateWindow**</span><span class="sxs-lookup"><span data-stu-id="f9f3e-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="f9f3e-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="f9f3e-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="f9f3e-146">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="f9f3e-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="f9f3e-147">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="f9f3e-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 

---
description: 當您 \_ 必須繪製 WM NCPAINT 訊息的框架時，就會將它傳送至視窗。
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: 'WM_NCPAINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848890"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="3f381-103">WM \_ NCPAINT 訊息</span><span class="sxs-lookup"><span data-stu-id="3f381-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="3f381-104">當您必須繪製 **WM \_ NCPAINT** 訊息的框架時，就會將它傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="3f381-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="3f381-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="3f381-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="3f381-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f381-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f381-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f381-108">視窗更新區域的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3f381-108">A handle to the update region of the window.</span></span> <span data-ttu-id="3f381-109">更新區域會裁剪至視窗框架。</span><span class="sxs-lookup"><span data-stu-id="3f381-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="3f381-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f381-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f381-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3f381-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f381-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f381-112">Return value</span></span>

<span data-ttu-id="3f381-113">如果應用程式處理此訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3f381-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f381-114">備註</span><span class="sxs-lookup"><span data-stu-id="3f381-114">Remarks</span></span>

<span data-ttu-id="3f381-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會繪製視窗框架。</span><span class="sxs-lookup"><span data-stu-id="3f381-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="3f381-116">應用程式可以攔截 **WM \_ NCPAINT** 訊息，並繪製自己的自訂視窗框架。</span><span class="sxs-lookup"><span data-stu-id="3f381-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="3f381-117">視窗的裁剪區域一律是矩形，即使框架的形狀改變也一樣。</span><span class="sxs-lookup"><span data-stu-id="3f381-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="3f381-118">*WParam* 值可以傳遞給 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="3f381-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="3f381-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f381-119">Requirements</span></span>



| <span data-ttu-id="3f381-120">需求</span><span class="sxs-lookup"><span data-stu-id="3f381-120">Requirement</span></span> | <span data-ttu-id="3f381-121">值</span><span class="sxs-lookup"><span data-stu-id="3f381-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f381-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f381-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f381-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f381-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3f381-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f381-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f381-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f381-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f381-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3f381-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f381-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3f381-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f381-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f381-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f381-129">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="3f381-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="3f381-130">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="3f381-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="3f381-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3f381-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3f381-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="3f381-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="3f381-133">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="3f381-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="3f381-134">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="3f381-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 

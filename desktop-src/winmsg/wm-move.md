---
description: 移動視窗之後傳送。
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: 'WM_MOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995836"
---
# <a name="wm_move-message"></a><span data-ttu-id="eafa0-103">WM \_ 移動訊息</span><span class="sxs-lookup"><span data-stu-id="eafa0-103">WM\_MOVE message</span></span>

<span data-ttu-id="eafa0-104">移動視窗之後傳送。</span><span class="sxs-lookup"><span data-stu-id="eafa0-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="eafa0-105">視窗會透過其 [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="eafa0-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="eafa0-106">參數</span><span class="sxs-lookup"><span data-stu-id="eafa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafa0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eafa0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eafa0-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="eafa0-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eafa0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eafa0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eafa0-110">視窗工作區左上角的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="eafa0-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="eafa0-111">低序位單字包含 x 座標，而高序位單字包含 y 座標。</span><span class="sxs-lookup"><span data-stu-id="eafa0-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafa0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eafa0-112">Return value</span></span>

<span data-ttu-id="eafa0-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="eafa0-113">Type: **LRESULT**</span></span>

<span data-ttu-id="eafa0-114">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="eafa0-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafa0-115">備註</span><span class="sxs-lookup"><span data-stu-id="eafa0-115">Remarks</span></span>

<span data-ttu-id="eafa0-116">這些參數是以螢幕座標提供，用於重迭和快顯視窗，以及子視窗的父系-工作區座標。</span><span class="sxs-lookup"><span data-stu-id="eafa0-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="eafa0-117">下列範例示範如何從 *lParam* 參數取得位置。</span><span class="sxs-lookup"><span data-stu-id="eafa0-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="eafa0-118">您也可以使用 [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) 宏將 *lParam* 參數轉換成 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="eafa0-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="eafa0-119">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會在處理 [**wm \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)訊息時，傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。</span><span class="sxs-lookup"><span data-stu-id="eafa0-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="eafa0-120">如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。</span><span class="sxs-lookup"><span data-stu-id="eafa0-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafa0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eafa0-121">Requirements</span></span>



| <span data-ttu-id="eafa0-122">需求</span><span class="sxs-lookup"><span data-stu-id="eafa0-122">Requirement</span></span> | <span data-ttu-id="eafa0-123">值</span><span class="sxs-lookup"><span data-stu-id="eafa0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafa0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eafa0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eafa0-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eafa0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eafa0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eafa0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eafa0-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eafa0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eafa0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="eafa0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eafa0-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="eafa0-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafa0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eafa0-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="eafa0-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="eafa0-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="eafa0-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafa0-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="eafa0-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafa0-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eafa0-134">**WM \_ WINDOWPOSCHANGED**</span><span class="sxs-lookup"><span data-stu-id="eafa0-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="eafa0-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="eafa0-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eafa0-136">Windows</span><span class="sxs-lookup"><span data-stu-id="eafa0-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="eafa0-137">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="eafa0-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eafa0-138">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="eafa0-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="eafa0-139">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafa0-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 

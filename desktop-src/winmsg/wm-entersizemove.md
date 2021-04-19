---
description: 在進入移動或調整強制回應迴圈之後，傳送一次至視窗。
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: 'WM_ENTERSIZEMOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996838"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="c1d2d-103">WM \_ ENTERSIZEMOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="c1d2d-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="c1d2d-104">在進入移動或調整強制回應迴圈之後，傳送一次至視窗。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="c1d2d-105">當使用者按一下視窗的標題列或調整框線，或是當視窗將 [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，而訊息的 *WParam* 參數指定 **sc \_ MOVE** 或 **sc \_ SIZE** 值時，此視窗會進入移動或調整大小的強制回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="c1d2d-106">當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 傳回時，作業就會完成。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="c1d2d-107">不論是否已啟用完整視窗的拖曳，系統都會傳送 **WM \_ ENTERSIZEMOVE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="c1d2d-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="c1d2d-109">參數</span><span class="sxs-lookup"><span data-stu-id="c1d2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d2d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1d2d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d2d-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1d2d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1d2d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d2d-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d2d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1d2d-114">Return value</span></span>

<span data-ttu-id="c1d2d-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-115">Type: **LRESULT**</span></span>

<span data-ttu-id="c1d2d-116">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="c1d2d-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d2d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1d2d-117">Requirements</span></span>



| <span data-ttu-id="c1d2d-118">需求</span><span class="sxs-lookup"><span data-stu-id="c1d2d-118">Requirement</span></span> | <span data-ttu-id="c1d2d-119">值</span><span class="sxs-lookup"><span data-stu-id="c1d2d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d2d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1d2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d2d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1d2d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1d2d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1d2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d2d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1d2d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1d2d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c1d2d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d2d-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c1d2d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1d2d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1d2d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1d2d-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1d2d-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c1d2d-129">**WM \_ EXITSIZEMOVE**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="c1d2d-130">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="c1d2d-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="c1d2d-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1d2d-132">Windows</span><span class="sxs-lookup"><span data-stu-id="c1d2d-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 

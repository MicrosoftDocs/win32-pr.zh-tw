---
description: 在離開移動或調整大小強制回應迴圈之後，傳送一次至視窗。
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: 'WM_EXITSIZEMOVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980550"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="55aa9-103">WM \_ EXITSIZEMOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="55aa9-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="55aa9-104">在離開移動或調整大小強制回應迴圈之後，傳送一次至視窗。</span><span class="sxs-lookup"><span data-stu-id="55aa9-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="55aa9-105">當使用者按一下視窗的標題列或調整框線，或是當視窗將 [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，而訊息的 *wParam* 參數指定 **sc \_ MOV** E 或 **sc \_ 大小** 值時，此視窗會進入移動或調整大小的強制回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="55aa9-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="55aa9-106">當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 傳回時，作業就會完成。</span><span class="sxs-lookup"><span data-stu-id="55aa9-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="55aa9-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="55aa9-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="55aa9-108">參數</span><span class="sxs-lookup"><span data-stu-id="55aa9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55aa9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55aa9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55aa9-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="55aa9-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55aa9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55aa9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55aa9-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="55aa9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55aa9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="55aa9-113">Return value</span></span>

<span data-ttu-id="55aa9-114">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="55aa9-114">Type: **LRESULT**</span></span>

<span data-ttu-id="55aa9-115">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="55aa9-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="55aa9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="55aa9-116">Requirements</span></span>



| <span data-ttu-id="55aa9-117">需求</span><span class="sxs-lookup"><span data-stu-id="55aa9-117">Requirement</span></span> | <span data-ttu-id="55aa9-118">值</span><span class="sxs-lookup"><span data-stu-id="55aa9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55aa9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55aa9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55aa9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55aa9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="55aa9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55aa9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55aa9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55aa9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55aa9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="55aa9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55aa9-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="55aa9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55aa9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55aa9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="55aa9-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="55aa9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55aa9-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="55aa9-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="55aa9-128">**WM \_ ENTERSIZEMOVE**</span><span class="sxs-lookup"><span data-stu-id="55aa9-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="55aa9-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="55aa9-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55aa9-130">Windows</span><span class="sxs-lookup"><span data-stu-id="55aa9-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 

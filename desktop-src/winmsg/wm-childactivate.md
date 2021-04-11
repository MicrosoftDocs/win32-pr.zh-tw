---
description: 當使用者按一下視窗的標題列時，或視窗啟用、移動或調整大小時，傳送至子視窗。
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: 'WM_CHILDACTI加值稅E 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693860"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="83e09-103">WM \_ CHILDACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="83e09-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="83e09-104">當使用者按一下視窗的標題列時，或視窗啟用、移動或調整大小時，傳送至子視窗。</span><span class="sxs-lookup"><span data-stu-id="83e09-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="83e09-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="83e09-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="83e09-106">參數</span><span class="sxs-lookup"><span data-stu-id="83e09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e09-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83e09-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83e09-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="83e09-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="83e09-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83e09-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83e09-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="83e09-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e09-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="83e09-111">Return value</span></span>

<span data-ttu-id="83e09-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="83e09-112">Type: **LRESULT**</span></span>

<span data-ttu-id="83e09-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="83e09-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e09-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="83e09-114">Requirements</span></span>



| <span data-ttu-id="83e09-115">需求</span><span class="sxs-lookup"><span data-stu-id="83e09-115">Requirement</span></span> | <span data-ttu-id="83e09-116">值</span><span class="sxs-lookup"><span data-stu-id="83e09-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e09-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83e09-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83e09-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83e09-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="83e09-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83e09-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83e09-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83e09-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83e09-121">標頭</span><span class="sxs-lookup"><span data-stu-id="83e09-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e09-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="83e09-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e09-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83e09-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="83e09-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="83e09-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83e09-125">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="83e09-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="83e09-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="83e09-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="83e09-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="83e09-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="83e09-128">Windows</span><span class="sxs-lookup"><span data-stu-id="83e09-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 

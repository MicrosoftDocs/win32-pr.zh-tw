---
description: 當視窗的大小或位置即將變更時，傳送至視窗。 應用程式可以使用此訊息來覆寫視窗的預設最大大小和位置，或其預設的最小或最大追蹤大小。
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: 'WM_GETMINMAXINFO 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850643"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="79268-104">WM \_ GETMINMAXINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="79268-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="79268-105">當視窗的大小或位置即將變更時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="79268-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="79268-106">應用程式可以使用此訊息來覆寫視窗的預設最大大小和位置，或其預設的最小或最大追蹤大小。</span><span class="sxs-lookup"><span data-stu-id="79268-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="79268-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="79268-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="79268-108">參數</span><span class="sxs-lookup"><span data-stu-id="79268-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79268-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79268-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79268-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="79268-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79268-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79268-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79268-112">[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)結構的指標，其中包含預設最大化的位置和維度，以及預設的最小和最大追蹤大小。</span><span class="sxs-lookup"><span data-stu-id="79268-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="79268-113">應用程式可以藉由設定此結構的成員來覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="79268-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79268-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="79268-114">Return value</span></span>

<span data-ttu-id="79268-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="79268-115">Type: **LRESULT**</span></span>

<span data-ttu-id="79268-116">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="79268-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="79268-117">備註</span><span class="sxs-lookup"><span data-stu-id="79268-117">Remarks</span></span>

<span data-ttu-id="79268-118">追蹤大小上限是可使用框線來調整視窗大小的最大視窗大小。</span><span class="sxs-lookup"><span data-stu-id="79268-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="79268-119">最小的追蹤大小是可使用框線來調整視窗大小的最小視窗大小。</span><span class="sxs-lookup"><span data-stu-id="79268-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="79268-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="79268-120">Requirements</span></span>



| <span data-ttu-id="79268-121">需求</span><span class="sxs-lookup"><span data-stu-id="79268-121">Requirement</span></span> | <span data-ttu-id="79268-122">值</span><span class="sxs-lookup"><span data-stu-id="79268-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79268-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79268-123">Minimum supported client</span></span><br/> | <span data-ttu-id="79268-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79268-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79268-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79268-125">Minimum supported server</span></span><br/> | <span data-ttu-id="79268-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79268-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79268-127">標頭</span><span class="sxs-lookup"><span data-stu-id="79268-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="79268-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="79268-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79268-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79268-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="79268-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="79268-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="79268-131">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="79268-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="79268-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="79268-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="79268-133">**MINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="79268-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="79268-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="79268-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79268-135">Windows</span><span class="sxs-lookup"><span data-stu-id="79268-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 

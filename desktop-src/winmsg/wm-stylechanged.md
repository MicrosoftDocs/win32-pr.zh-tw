---
description: 在 SetWindowLong 函式已變更一個或多個視窗的樣式之後，傳送至視窗。
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: 'WM_STYLECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513884"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="ff026-103">WM \_ STYLECHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="ff026-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="ff026-104">在 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式已變更一個或多個視窗的樣式之後，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="ff026-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="ff026-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="ff026-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="ff026-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff026-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff026-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff026-108">指出視窗的樣式或延伸視窗樣式是否已變更。</span><span class="sxs-lookup"><span data-stu-id="ff026-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="ff026-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="ff026-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="ff026-110">值</span><span class="sxs-lookup"><span data-stu-id="ff026-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="ff026-111">意義</span><span class="sxs-lookup"><span data-stu-id="ff026-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="ff026-112"><dt>**GWL \_EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="ff026-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="ff026-113">擴充的視窗樣式已變更。</span><span class="sxs-lookup"><span data-stu-id="ff026-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="ff026-114"><dt>**GWL \_樣式**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="ff026-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="ff026-115">視窗樣式已變更。</span><span class="sxs-lookup"><span data-stu-id="ff026-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="ff026-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff026-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff026-117">[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)結構的指標，其中包含視窗的新樣式。</span><span class="sxs-lookup"><span data-stu-id="ff026-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="ff026-118">應用程式可以檢查樣式，但無法加以變更。</span><span class="sxs-lookup"><span data-stu-id="ff026-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff026-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff026-119">Return value</span></span>

<span data-ttu-id="ff026-120">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff026-120">Type: **LRESULT**</span></span>

<span data-ttu-id="ff026-121">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="ff026-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff026-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff026-122">Requirements</span></span>



| <span data-ttu-id="ff026-123">需求</span><span class="sxs-lookup"><span data-stu-id="ff026-123">Requirement</span></span> | <span data-ttu-id="ff026-124">值</span><span class="sxs-lookup"><span data-stu-id="ff026-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff026-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff026-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ff026-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff026-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff026-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff026-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ff026-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff026-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff026-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ff026-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff026-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ff026-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff026-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff026-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff026-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="ff026-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff026-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="ff026-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="ff026-134">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="ff026-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="ff026-135">**WM \_ STYLECHANGING**</span><span class="sxs-lookup"><span data-stu-id="ff026-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="ff026-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="ff026-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff026-137">Windows</span><span class="sxs-lookup"><span data-stu-id="ff026-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 

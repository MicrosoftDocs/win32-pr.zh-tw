---
description: 當 SetWindowLong 函式即將變更一個或多個視窗的樣式時，傳送至視窗。
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: 'WM_STYLECHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849349"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="65c71-103">WM \_ STYLECHANGING 訊息</span><span class="sxs-lookup"><span data-stu-id="65c71-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="65c71-104">當 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式即將變更一個或多個視窗的樣式時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="65c71-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="65c71-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="65c71-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="65c71-106">參數</span><span class="sxs-lookup"><span data-stu-id="65c71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c71-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65c71-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65c71-108">指出視窗的樣式或延伸視窗樣式是否正在變更。</span><span class="sxs-lookup"><span data-stu-id="65c71-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="65c71-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="65c71-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="65c71-110">值</span><span class="sxs-lookup"><span data-stu-id="65c71-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="65c71-111">意義</span><span class="sxs-lookup"><span data-stu-id="65c71-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="65c71-112"><dt>**GWL \_EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="65c71-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="65c71-113">擴充的視窗樣式即將變更。</span><span class="sxs-lookup"><span data-stu-id="65c71-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="65c71-114"><dt>**GWL \_樣式**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="65c71-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="65c71-115">視窗樣式即將變更。</span><span class="sxs-lookup"><span data-stu-id="65c71-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="65c71-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65c71-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65c71-117">[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)結構的指標，其中包含為視窗建議的新樣式。</span><span class="sxs-lookup"><span data-stu-id="65c71-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="65c71-118">應用程式可以檢查樣式，並視需要加以變更。</span><span class="sxs-lookup"><span data-stu-id="65c71-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c71-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="65c71-119">Return value</span></span>

<span data-ttu-id="65c71-120">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="65c71-120">Type: **LRESULT**</span></span>

<span data-ttu-id="65c71-121">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="65c71-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c71-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="65c71-122">Requirements</span></span>



| <span data-ttu-id="65c71-123">需求</span><span class="sxs-lookup"><span data-stu-id="65c71-123">Requirement</span></span> | <span data-ttu-id="65c71-124">值</span><span class="sxs-lookup"><span data-stu-id="65c71-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c71-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65c71-125">Minimum supported client</span></span><br/> | <span data-ttu-id="65c71-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65c71-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="65c71-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65c71-127">Minimum supported server</span></span><br/> | <span data-ttu-id="65c71-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65c71-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65c71-129">標頭</span><span class="sxs-lookup"><span data-stu-id="65c71-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="65c71-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="65c71-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c71-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65c71-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="65c71-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="65c71-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="65c71-133">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="65c71-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="65c71-134">**WM \_ STYLECHANGED**</span><span class="sxs-lookup"><span data-stu-id="65c71-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="65c71-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="65c71-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="65c71-136">Windows</span><span class="sxs-lookup"><span data-stu-id="65c71-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 

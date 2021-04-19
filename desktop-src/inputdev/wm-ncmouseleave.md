---
title: 'WM_NCMOUSELEAVE 訊息 (Winuser .h) '
description: 當游標離開先前呼叫 TrackMouseEvent 所指定之視窗的非工作區時，張貼至視窗。
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001104"
---
# <a name="wm_ncmouseleave-message"></a><span data-ttu-id="05c9a-104">WM \_ NCMOUSELEAVE 訊息</span><span class="sxs-lookup"><span data-stu-id="05c9a-104">WM\_NCMOUSELEAVE message</span></span>

<span data-ttu-id="05c9a-105">當游標離開先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定之視窗的非工作區時，張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="05c9a-105">Posted to a window when the cursor leaves the nonclient area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="05c9a-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="05c9a-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a><span data-ttu-id="05c9a-107">參數</span><span class="sxs-lookup"><span data-stu-id="05c9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c9a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05c9a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05c9a-109">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="05c9a-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="05c9a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05c9a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05c9a-111">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="05c9a-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c9a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="05c9a-112">Return value</span></span>

<span data-ttu-id="05c9a-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="05c9a-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c9a-114">備註</span><span class="sxs-lookup"><span data-stu-id="05c9a-114">Remarks</span></span>

<span data-ttu-id="05c9a-115">當產生此訊息時，會取消 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 要求的所有追蹤。</span><span class="sxs-lookup"><span data-stu-id="05c9a-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="05c9a-116">如果滑鼠需要進一步追蹤滑鼠停留行為，應用程式必須在滑鼠重新進入視窗時呼叫 **TrackMouseEvent** 。</span><span class="sxs-lookup"><span data-stu-id="05c9a-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c9a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="05c9a-117">Requirements</span></span>



| <span data-ttu-id="05c9a-118">需求</span><span class="sxs-lookup"><span data-stu-id="05c9a-118">Requirement</span></span> | <span data-ttu-id="05c9a-119">值</span><span class="sxs-lookup"><span data-stu-id="05c9a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c9a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05c9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05c9a-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05c9a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05c9a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05c9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05c9a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05c9a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05c9a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="05c9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c9a-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="05c9a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c9a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05c9a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="05c9a-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="05c9a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05c9a-128">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="05c9a-128">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="05c9a-129">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="05c9a-129">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="05c9a-130">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="05c9a-130">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="05c9a-131">**WM \_ MOUSELEAVE**</span><span class="sxs-lookup"><span data-stu-id="05c9a-131">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
</dt> <dt>

<span data-ttu-id="05c9a-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="05c9a-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05c9a-133">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="05c9a-133">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 


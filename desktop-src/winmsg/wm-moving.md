---
description: 傳送至使用者正在移動的視窗。 藉由處理這個訊息，應用程式可以監視拖曳矩形的位置，並且視需要變更其位置。
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: 'WM_MOVING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979727"
---
# <a name="wm_moving-message"></a><span data-ttu-id="2ad47-104">WM \_ 移動訊息</span><span class="sxs-lookup"><span data-stu-id="2ad47-104">WM\_MOVING message</span></span>

<span data-ttu-id="2ad47-105">傳送至使用者正在移動的視窗。</span><span class="sxs-lookup"><span data-stu-id="2ad47-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="2ad47-106">藉由處理這個訊息，應用程式可以監視拖曳矩形的位置，並且視需要變更其位置。</span><span class="sxs-lookup"><span data-stu-id="2ad47-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="2ad47-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="2ad47-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="2ad47-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ad47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad47-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ad47-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad47-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2ad47-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2ad47-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ad47-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad47-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，該結構具有視窗目前的位置，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="2ad47-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="2ad47-113">若要變更拖曳矩形的位置，應用程式必須變更此結構的成員。</span><span class="sxs-lookup"><span data-stu-id="2ad47-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad47-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ad47-114">Return value</span></span>

<span data-ttu-id="2ad47-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ad47-115">Type: **LRESULT**</span></span>

<span data-ttu-id="2ad47-116">如果應用程式處理此訊息，則應該傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="2ad47-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad47-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ad47-117">Requirements</span></span>



| <span data-ttu-id="2ad47-118">需求</span><span class="sxs-lookup"><span data-stu-id="2ad47-118">Requirement</span></span> | <span data-ttu-id="2ad47-119">值</span><span class="sxs-lookup"><span data-stu-id="2ad47-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad47-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ad47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad47-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ad47-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2ad47-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ad47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad47-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ad47-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ad47-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2ad47-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad47-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2ad47-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad47-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ad47-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ad47-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="2ad47-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ad47-128">**WM \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="2ad47-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="2ad47-129">**WM 重設 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="2ad47-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="2ad47-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="2ad47-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2ad47-131">Windows</span><span class="sxs-lookup"><span data-stu-id="2ad47-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="2ad47-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="2ad47-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2ad47-133">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ad47-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 

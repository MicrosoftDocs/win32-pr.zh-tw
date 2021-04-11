---
title: 'WM_GESTURENOTIFY 訊息 (Winuser .h) '
description: 讓您有機會設定手勢設定。
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104531"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="63846-104">WM \_ GESTURENOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="63846-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="63846-105">讓您有機會設定手勢設定。</span><span class="sxs-lookup"><span data-stu-id="63846-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="63846-106">參數</span><span class="sxs-lookup"><span data-stu-id="63846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63846-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63846-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63846-108">未使用的。</span><span class="sxs-lookup"><span data-stu-id="63846-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="63846-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63846-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63846-110">指向 [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)的指標。</span><span class="sxs-lookup"><span data-stu-id="63846-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63846-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="63846-111">Return value</span></span>

<span data-ttu-id="63846-112">應從 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)傳回值。</span><span class="sxs-lookup"><span data-stu-id="63846-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="63846-113">備註</span><span class="sxs-lookup"><span data-stu-id="63846-113">Remarks</span></span>

<span data-ttu-id="63846-114">當收到 **WM \_ GESTURENOTIFY** 訊息時，應用程式可以使用 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) 來指定要接收的手勢。</span><span class="sxs-lookup"><span data-stu-id="63846-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="63846-115">這則訊息應該一律使用 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數進行反升。</span><span class="sxs-lookup"><span data-stu-id="63846-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="63846-116">處理 **WM \_ GESTURENOTIFY** 訊息將會變更視窗存留期的手勢設定，而不只是下一個手勢。</span><span class="sxs-lookup"><span data-stu-id="63846-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="63846-117">範例</span><span class="sxs-lookup"><span data-stu-id="63846-117">Examples</span></span>

<span data-ttu-id="63846-118">下列範例顯示如何啟用所有手勢。</span><span class="sxs-lookup"><span data-stu-id="63846-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="63846-119">如需更多範例，請參閱 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)。</span><span class="sxs-lookup"><span data-stu-id="63846-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="63846-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="63846-120">Requirements</span></span>



| <span data-ttu-id="63846-121">需求</span><span class="sxs-lookup"><span data-stu-id="63846-121">Requirement</span></span> | <span data-ttu-id="63846-122">值</span><span class="sxs-lookup"><span data-stu-id="63846-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63846-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63846-123">Minimum supported client</span></span><br/> | <span data-ttu-id="63846-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63846-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="63846-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63846-125">Minimum supported server</span></span><br/> | <span data-ttu-id="63846-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63846-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="63846-127">標頭</span><span class="sxs-lookup"><span data-stu-id="63846-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="63846-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="63846-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63846-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63846-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63846-130">通知</span><span class="sxs-lookup"><span data-stu-id="63846-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="63846-131">Windows Touch 手勢程式設計指南</span><span class="sxs-lookup"><span data-stu-id="63846-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="63846-132">**GESTURENOTIFYSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="63846-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="63846-133">**SetGestureConfig**</span><span class="sxs-lookup"><span data-stu-id="63846-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


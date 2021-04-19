---
title: 'WM_DRAWCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿的內容變更時，傳送至剪貼簿檢視器鏈中的第一個視窗。 這可讓剪貼簿檢視器視窗顯示剪貼簿的新內容。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967536"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="b7a88-106">WM \_ DRAWCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="b7a88-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="b7a88-107">當剪貼簿的內容變更時，傳送至剪貼簿檢視器鏈中的第一個視窗。</span><span class="sxs-lookup"><span data-stu-id="b7a88-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="b7a88-108">這可讓剪貼簿檢視器視窗顯示剪貼簿的新內容。</span><span class="sxs-lookup"><span data-stu-id="b7a88-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="b7a88-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="b7a88-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="b7a88-110">參數</span><span class="sxs-lookup"><span data-stu-id="b7a88-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7a88-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7a88-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7a88-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b7a88-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b7a88-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7a88-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7a88-114">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b7a88-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7a88-115">備註</span><span class="sxs-lookup"><span data-stu-id="b7a88-115">Remarks</span></span>

<span data-ttu-id="b7a88-116">只有 [剪貼簿檢視器] 視窗會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="b7a88-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="b7a88-117">這些是使用 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函式新增至剪貼簿檢視器鏈的 windows。</span><span class="sxs-lookup"><span data-stu-id="b7a88-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="b7a88-118">每個接收 **WM \_ DRAWCLIPBOARD** 訊息的視窗都必須呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，以將訊息傳遞至剪貼簿檢視器鏈中的下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="b7a88-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="b7a88-119">[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)會傳回鏈中下一個視窗的控制碼，而且可能會變更以回應 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="b7a88-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7a88-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7a88-120">Requirements</span></span>



| <span data-ttu-id="b7a88-121">需求</span><span class="sxs-lookup"><span data-stu-id="b7a88-121">Requirement</span></span> | <span data-ttu-id="b7a88-122">值</span><span class="sxs-lookup"><span data-stu-id="b7a88-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a88-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7a88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a88-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7a88-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b7a88-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7a88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a88-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7a88-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7a88-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b7a88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a88-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b7a88-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7a88-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7a88-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7a88-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="b7a88-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7a88-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="b7a88-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="b7a88-132">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="b7a88-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="b7a88-133">**WM \_ CHANGECBCHAIN**</span><span class="sxs-lookup"><span data-stu-id="b7a88-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="b7a88-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="b7a88-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b7a88-135">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="b7a88-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


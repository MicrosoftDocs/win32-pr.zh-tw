---
title: 'WM_CHANGECBCHAIN 訊息 (Winuser .h) '
description: 從鏈中移除視窗時，傳送至剪貼簿檢視器鏈中的第一個視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN 訊息資料交換
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104088"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="270c9-105">WM \_ CHANGECBCHAIN 訊息</span><span class="sxs-lookup"><span data-stu-id="270c9-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="270c9-106">從鏈中移除視窗時，傳送至剪貼簿檢視器鏈中的第一個視窗。</span><span class="sxs-lookup"><span data-stu-id="270c9-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="270c9-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="270c9-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="270c9-108">參數</span><span class="sxs-lookup"><span data-stu-id="270c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="270c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="270c9-110">從剪貼簿檢視器鏈中移除的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="270c9-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="270c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="270c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="270c9-112">在要移除的視窗後面的鏈中，下一個視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="270c9-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="270c9-113">如果要移除的視窗是鏈中的最後一個視窗，則此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="270c9-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270c9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="270c9-114">Return value</span></span>

<span data-ttu-id="270c9-115">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="270c9-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="270c9-116">備註</span><span class="sxs-lookup"><span data-stu-id="270c9-116">Remarks</span></span>

<span data-ttu-id="270c9-117">每個剪貼簿檢視器視窗都會將控制碼儲存至剪貼簿檢視器鏈中的下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="270c9-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="270c9-118">一開始，這個控制碼是 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函數的傳回值。</span><span class="sxs-lookup"><span data-stu-id="270c9-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="270c9-119">當剪貼簿檢視器視窗收到 **WM \_ CHANGECBCHAIN** 訊息時，它應該呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，將訊息傳遞至鏈中的下一個視窗，除非下一個視窗是要移除的視窗。</span><span class="sxs-lookup"><span data-stu-id="270c9-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="270c9-120">在此情況下，剪貼簿檢視器應該將 *lParam* 參數所指定的控制碼儲存為鏈中的下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="270c9-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="270c9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="270c9-121">Requirements</span></span>



| <span data-ttu-id="270c9-122">需求</span><span class="sxs-lookup"><span data-stu-id="270c9-122">Requirement</span></span> | <span data-ttu-id="270c9-123">值</span><span class="sxs-lookup"><span data-stu-id="270c9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270c9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="270c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="270c9-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="270c9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="270c9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="270c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="270c9-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="270c9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="270c9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="270c9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="270c9-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="270c9-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="270c9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="270c9-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="270c9-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="270c9-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="270c9-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="270c9-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="270c9-133">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="270c9-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="270c9-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="270c9-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="270c9-135">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="270c9-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


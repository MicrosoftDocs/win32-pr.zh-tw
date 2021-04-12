---
title: 'WM_TOUCH 訊息 (Winuser .h) '
description: 當一或多個觸控點（例如手指或畫筆）觸及觸控式的數位化板介面時，通知視窗。
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384937"
---
# <a name="wm_touch-message"></a><span data-ttu-id="3b750-104">WM \_ 觸控訊息</span><span class="sxs-lookup"><span data-stu-id="3b750-104">WM\_TOUCH message</span></span>

<span data-ttu-id="3b750-105">當一或多個觸控點（例如手指或畫筆）觸及觸控式的數位化板介面時，通知視窗。</span><span class="sxs-lookup"><span data-stu-id="3b750-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b750-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b750-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b750-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b750-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b750-108">低序位文字包含與此訊息相關聯的觸控點數目。</span><span class="sxs-lookup"><span data-stu-id="3b750-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="3b750-109">高序位字組保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3b750-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3b750-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b750-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b750-111">包含觸控輸入控點，可用於 [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) 的呼叫，以取得與此訊息相關聯之觸控點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3b750-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="3b750-112">這個控制碼只在目前的進程內有效，不應該跨進程傳遞，除非 **LPARAM** 在 **SendMessage** 或 **PostMessage** 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="3b750-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="3b750-113">當應用程式不再需要這個控制碼時，應用程式必須呼叫 **CloseTouchInputHandle** 來釋放與此控制碼相關聯的進程記憶體。</span><span class="sxs-lookup"><span data-stu-id="3b750-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="3b750-114">如果無法這麼做，可能會導致應用程式記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="3b750-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="3b750-115">請注意，在訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)之後，這個參數中的觸控輸入控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="3b750-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="3b750-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 將會關閉並使此控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="3b750-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="3b750-117">另請注意，在使用 [**PostMessage**](sendmessage--postmessage--and-related-functions.md)、 **SendMessage** 或其中一個變體轉送訊息之後，此參數中的觸控輸入控點將不再有效。</span><span class="sxs-lookup"><span data-stu-id="3b750-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="3b750-118">這些函式會關閉並使此控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="3b750-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b750-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b750-119">Return value</span></span>

<span data-ttu-id="3b750-120">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3b750-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="3b750-121">如果應用程式未處理訊息，則必須呼叫 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="3b750-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="3b750-122">未這樣做會導致應用程式流失記憶體，因為觸控輸入控制碼未關閉，且相關聯的進程記憶體未釋出。</span><span class="sxs-lookup"><span data-stu-id="3b750-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b750-123">備註</span><span class="sxs-lookup"><span data-stu-id="3b750-123">Remarks</span></span>

<span data-ttu-id="3b750-124">**WM \_觸控** 訊息不遵守 windows 的 **HTTRANSPARENT** 區域。</span><span class="sxs-lookup"><span data-stu-id="3b750-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="3b750-125">如果視窗傳回 **HTTRANSPARENT** 來回應 **WM \_ NCHITTEST** 訊息，則滑鼠訊息會移至父系，而 **WM \_ 觸控** 訊息會直接移至視窗。</span><span class="sxs-lookup"><span data-stu-id="3b750-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="3b750-126">範例</span><span class="sxs-lookup"><span data-stu-id="3b750-126">Examples</span></span>

<span data-ttu-id="3b750-127">下列程式碼範例示範如何取得與此訊息相關聯的詳細觸控輸入資訊。</span><span class="sxs-lookup"><span data-stu-id="3b750-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="3b750-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b750-128">Requirements</span></span>



| <span data-ttu-id="3b750-129">需求</span><span class="sxs-lookup"><span data-stu-id="3b750-129">Requirement</span></span> | <span data-ttu-id="3b750-130">值</span><span class="sxs-lookup"><span data-stu-id="3b750-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b750-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b750-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3b750-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b750-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3b750-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b750-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3b750-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b750-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="3b750-135">標頭</span><span class="sxs-lookup"><span data-stu-id="3b750-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b750-136"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3b750-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b750-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b750-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b750-138">訊息</span><span class="sxs-lookup"><span data-stu-id="3b750-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="3b750-139">操作和慣性程式設計指南</span><span class="sxs-lookup"><span data-stu-id="3b750-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="3b750-140">Windows Touch 輸入程式設計指南</span><span class="sxs-lookup"><span data-stu-id="3b750-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 


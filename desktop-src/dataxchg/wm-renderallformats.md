---
title: 'WM_RENDERALLFORMATS 訊息 (Winuser .h) '
description: 如果剪貼簿擁有者有延遲轉譯一或多個剪貼簿格式，則會在終結之前傳送給剪貼簿擁有者。
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS 訊息資料交換
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509092"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="37cba-104">WM \_ RENDERALLFORMATS 訊息</span><span class="sxs-lookup"><span data-stu-id="37cba-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="37cba-105">如果剪貼簿擁有者有延遲轉譯一或多個剪貼簿格式，則會在終結之前傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="37cba-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="37cba-106">若要讓剪貼簿的內容仍然可供其他應用程式使用，剪貼簿擁有者必須以它能夠產生的所有格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式將資料放在剪貼簿上。</span><span class="sxs-lookup"><span data-stu-id="37cba-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="37cba-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="37cba-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="37cba-108">參數</span><span class="sxs-lookup"><span data-stu-id="37cba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37cba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37cba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37cba-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="37cba-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="37cba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37cba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37cba-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="37cba-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37cba-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="37cba-113">Return value</span></span>

<span data-ttu-id="37cba-114">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="37cba-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="37cba-115">備註</span><span class="sxs-lookup"><span data-stu-id="37cba-115">Remarks</span></span>

<span data-ttu-id="37cba-116">回應 **WM \_ RENDERALLFORMATS** 訊息時，應用程式必須呼叫 [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) 函式，然後藉由呼叫 [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) 函式來檢查它是否仍是剪貼簿擁有者，然後再呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)。</span><span class="sxs-lookup"><span data-stu-id="37cba-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="37cba-117">在開啟剪貼簿之後，應用程式必須檢查它是否仍是剪貼簿擁有者，因為它會在收到 **WM \_ RENDERALLFORMATS** 訊息之後，但在開啟剪貼簿之前，另一個應用程式可能已開啟並取得剪貼簿的擁有權，而且不應該覆寫該應用程式的資料。</span><span class="sxs-lookup"><span data-stu-id="37cba-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="37cba-118">在大部分的情況下，應用程式不應該在呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)之前呼叫 [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard)函式，因為這樣做會清除應用程式已經轉譯的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="37cba-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="37cba-119">當應用程式傳回時，系統會從可用的剪貼簿格式清單中移除任何 unrendered 格式。</span><span class="sxs-lookup"><span data-stu-id="37cba-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="37cba-120">如需延遲呈現的詳細資訊，請參閱 [延遲](clipboard-operations.md#delayed-rendering)轉譯。</span><span class="sxs-lookup"><span data-stu-id="37cba-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="37cba-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="37cba-121">Requirements</span></span>



| <span data-ttu-id="37cba-122">需求</span><span class="sxs-lookup"><span data-stu-id="37cba-122">Requirement</span></span> | <span data-ttu-id="37cba-123">值</span><span class="sxs-lookup"><span data-stu-id="37cba-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cba-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37cba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37cba-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37cba-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37cba-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37cba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37cba-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37cba-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37cba-128">標頭</span><span class="sxs-lookup"><span data-stu-id="37cba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="37cba-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="37cba-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37cba-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37cba-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="37cba-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="37cba-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37cba-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="37cba-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="37cba-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="37cba-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="37cba-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="37cba-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="37cba-135">**WM \_ RENDERFORMAT**</span><span class="sxs-lookup"><span data-stu-id="37cba-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="37cba-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="37cba-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="37cba-137">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="37cba-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


---
description: 傳送至視窗，以取得與視窗相關聯之大型或小型圖示的控制碼。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: 'WM_GETICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990335"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="1a5a7-104">WM \_ GETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="1a5a7-104">WM\_GETICON message</span></span>

<span data-ttu-id="1a5a7-105">傳送至視窗，以取得與視窗相關聯之大型或小型圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="1a5a7-106">系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="1a5a7-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="1a5a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a5a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a5a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a5a7-110">要抓取的圖示類型。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-110">The type of icon being retrieved.</span></span> <span data-ttu-id="1a5a7-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1a5a7-112">值</span><span class="sxs-lookup"><span data-stu-id="1a5a7-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="1a5a7-113">意義</span><span class="sxs-lookup"><span data-stu-id="1a5a7-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="1a5a7-114"><dt>**圖示 \_BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1a5a7-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="1a5a7-115">取出視窗的大型圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="1a5a7-116"><dt>**圖示 \_小**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a5a7-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="1a5a7-117">取出視窗的小圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="1a5a7-118"><dt>**圖示 \_SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1a5a7-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="1a5a7-119">抓取應用程式所提供的小圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="1a5a7-120">如果應用程式不提供，系統就會針對該視窗使用系統產生的圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1a5a7-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a5a7-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a5a7-122">要抓取之圖示的 DPI。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="1a5a7-123">這可以用來根據圖示大小提供不同的圖示。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5a7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a5a7-124">Return value</span></span>

<span data-ttu-id="1a5a7-125">類型： **HICON**</span><span class="sxs-lookup"><span data-stu-id="1a5a7-125">Type: **HICON**</span></span>

<span data-ttu-id="1a5a7-126">傳回值是大型或小型圖示的控制碼，視 *wParam* 的值而定。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="1a5a7-127">當應用程式收到此訊息時，它可以將控制碼傳回至大型或小型圖示，或將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5a7-128">備註</span><span class="sxs-lookup"><span data-stu-id="1a5a7-128">Remarks</span></span>

<span data-ttu-id="1a5a7-129">當應用程式收到此訊息時，它可以將控制碼傳回至大型或小型圖示，或將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="1a5a7-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會傳回與視窗相關聯之大型或小型圖示的控制碼，視 *wParam* 的值而定。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="1a5a7-131">沒有圖示的視窗會明確設定 (使用 **WM \_ SETICON**) 使用已註冊視窗類別的圖示，而在此情況下， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會傳回0作為 **wm \_ GETICON** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="1a5a7-132">如果將 **WM \_ GETICON** 訊息傳送至視窗會傳回0，接下來請嘗試呼叫視窗的 [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) 函式。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="1a5a7-133">如果傳回0，則嘗試 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函數。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a5a7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a5a7-134">Requirements</span></span>



| <span data-ttu-id="1a5a7-135">需求</span><span class="sxs-lookup"><span data-stu-id="1a5a7-135">Requirement</span></span> | <span data-ttu-id="1a5a7-136">值</span><span class="sxs-lookup"><span data-stu-id="1a5a7-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5a7-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a5a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1a5a7-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a5a7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1a5a7-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a5a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1a5a7-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a5a7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a5a7-141">標頭</span><span class="sxs-lookup"><span data-stu-id="1a5a7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a5a7-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1a5a7-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a5a7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a5a7-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a5a7-144">**參考**</span><span class="sxs-lookup"><span data-stu-id="1a5a7-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a5a7-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1a5a7-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1a5a7-146">**WM \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="1a5a7-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="1a5a7-147">**概念**</span><span class="sxs-lookup"><span data-stu-id="1a5a7-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a5a7-148">Windows</span><span class="sxs-lookup"><span data-stu-id="1a5a7-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 

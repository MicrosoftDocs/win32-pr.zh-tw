---
description: 您將 **WM_SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: 'WM_SETREDRAW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593454"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="73720-103">WM_SETREDRAW 訊息</span><span class="sxs-lookup"><span data-stu-id="73720-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="73720-104">您會將 **WM \_ SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。</span><span class="sxs-lookup"><span data-stu-id="73720-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="73720-105">若要傳送此訊息，請使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="73720-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="73720-106">參數</span><span class="sxs-lookup"><span data-stu-id="73720-106">Parameters</span></span>

`wParam`

<span data-ttu-id="73720-107">重繪狀態。</span><span class="sxs-lookup"><span data-stu-id="73720-107">The redraw state.</span></span> <span data-ttu-id="73720-108">如果此參數為 **TRUE**，則會在變更之後重新繪製內容。</span><span class="sxs-lookup"><span data-stu-id="73720-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="73720-109">如果此參數為 **FALSE**，則不能在變更之後重新繪製內容。</span><span class="sxs-lookup"><span data-stu-id="73720-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="73720-110">未使用此參數。</span><span class="sxs-lookup"><span data-stu-id="73720-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="73720-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73720-111">Return value</span></span>

<span data-ttu-id="73720-112">如果您的應用程式處理此訊息，則應該會傳回0。</span><span class="sxs-lookup"><span data-stu-id="73720-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="73720-113">備註</span><span class="sxs-lookup"><span data-stu-id="73720-113">Remarks</span></span>

<span data-ttu-id="73720-114">如果您的應用程式必須在清單方塊中加入數個專案，這則訊息會很有用。</span><span class="sxs-lookup"><span data-stu-id="73720-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="73720-115">您的應用程式可以呼叫此訊息，並將 *wParam* 設定為 **FALSE**、新增專案，然後再呼叫 *wParam* 設定為 **TRUE** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="73720-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="73720-116">最後，您的應用程式可以呼叫 [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) (*hWnd*、 **null**、 **null**、RDW \_ 清除 \| RDW \_ 框架 \| RDW \_ 使 \| RDW ALLCHILDREN) 無效，使 \_ 清單方塊重新繪製。</span><span class="sxs-lookup"><span data-stu-id="73720-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="73720-117">您應該使用 [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) 搭配指定的旗標（而不是 [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect)），因為前者對於本身具有非工作區的某些控制項是必要的，或是具有導致它們被賦予非工作區的視窗樣式 (例如 **WS_THICKFRAME**、 **WS_BORDER** 或 **WS_EX_CLIENTEDGE**) 。</span><span class="sxs-lookup"><span data-stu-id="73720-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="73720-118">如果控制項沒有非工作區，則使用這些旗標的 **RedrawWindow** 將只會執行與 **InvalidateRect** 一樣多的失效。</span><span class="sxs-lookup"><span data-stu-id="73720-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="73720-119">當 *wParam* 設定為 **FALSE** 時，將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc** 函式會將 **WS_VISIBLE** 樣式從視窗中移除。</span><span class="sxs-lookup"><span data-stu-id="73720-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="73720-120">雖然視窗內容在螢幕上仍是可見的，但 [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) 函式會在此狀態的視窗上呼叫時傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="73720-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="73720-121">當 *wParam* 設定為 **TRUE** 時，將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc** 函式會將 **WS_VISIBLE** 樣式加入至視窗（如果未設定的話）。</span><span class="sxs-lookup"><span data-stu-id="73720-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="73720-122">如果您的應用程式將 *wParam* 設為 **TRUE** 的 **WM_SETREDRAW** 訊息傳送至隱藏的視窗，則視窗會變成可見。</span><span class="sxs-lookup"><span data-stu-id="73720-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="73720-123">**Windows 10 和更新版本;Windows Server 2016 和更新版本**。</span><span class="sxs-lookup"><span data-stu-id="73720-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="73720-124">系統會在視窗中，將名為 *SysSetRedraw* 的屬性設定為視窗，其視窗程式會將 **WM_SETREDRAW** 訊息傳遞至 **DefWindowProc**。</span><span class="sxs-lookup"><span data-stu-id="73720-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="73720-125">您可以使用 [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) 函數來取得可用的屬性值。</span><span class="sxs-lookup"><span data-stu-id="73720-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="73720-126">停用重繪時， **GetProp** 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="73720-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="73720-127">當重新啟用重繪或視窗屬性不存在時， **GetProp** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="73720-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="73720-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="73720-128">Requirements</span></span>

| <span data-ttu-id="73720-129">需求</span><span class="sxs-lookup"><span data-stu-id="73720-129">Requirement</span></span> | <span data-ttu-id="73720-130">值</span><span class="sxs-lookup"><span data-stu-id="73720-130">Value</span></span> |
|-|-|
| <span data-ttu-id="73720-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73720-131">Minimum supported client</span></span> | <span data-ttu-id="73720-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73720-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="73720-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73720-133">Minimum supported server</span></span> | <span data-ttu-id="73720-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73720-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="73720-135">標頭</span><span class="sxs-lookup"><span data-stu-id="73720-135">Header</span></span> | <dl><span data-ttu-id="73720-136"><dt>Winuser (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="73720-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="73720-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73720-137">See also</span></span>

* [<span data-ttu-id="73720-138">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="73720-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="73720-139">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="73720-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="73720-140">RedrawWindow</span><span class="sxs-lookup"><span data-stu-id="73720-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)

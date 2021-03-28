---
description: 應用程式會將 WM \_ SETREDRAW 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: 'WM_SETREDRAW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193783"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="2ad5c-103">WM \_ SETREDRAW 訊息</span><span class="sxs-lookup"><span data-stu-id="2ad5c-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="2ad5c-104">應用程式會將 **WM \_ SETREDRAW** 訊息傳送至視窗，以允許重新繪製該視窗中的變更，或防止重繪該視窗中的變更。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="2ad5c-105">若要傳送此訊息，請使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="2ad5c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ad5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ad5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad5c-108">重繪狀態。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-108">The redraw state.</span></span> <span data-ttu-id="2ad5c-109">如果此參數為 **TRUE**，則會在變更之後重新繪製內容。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="2ad5c-110">如果此參數為 **FALSE**，則不能在變更之後重新繪製內容。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="2ad5c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ad5c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad5c-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad5c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ad5c-113">Return value</span></span>

<span data-ttu-id="2ad5c-114">如果應用程式處理此訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad5c-115">備註</span><span class="sxs-lookup"><span data-stu-id="2ad5c-115">Remarks</span></span>

<span data-ttu-id="2ad5c-116">如果應用程式必須在清單方塊中加入數個專案，則此訊息會很有用。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="2ad5c-117">應用程式可以呼叫此訊息，並將 *wParam* 設定為 **FALSE**、新增專案，然後再呼叫 *wParam* 設定為 **TRUE** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="2ad5c-118">最後，應用程式可以呼叫 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) (*hWnd*、 **null**、 **null**、RDW \_ 清除 \| RDW \_ 框架 \| RDW \_ 使 \| RDW \_ ALLCHILDREN) 無效，使清單方塊重新繪製。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="2ad5c-119">使用指定之旗標的 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) ，而不是 [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ，因為前者對於本身具有非工作區的某些控制項而言是必要的，或是具有導致它們被賦予非工作區 (例如 **ws \_ THICKFRAME**、 **ws \_ BORDER** 或 **ws \_ EX \_ CLIENTEDGE**) 的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="2ad5c-120">如果控制項沒有非工作區，則使用這些旗標的 **RedrawWindow** 只會執行與 **InvalidateRect** 一樣多的失效。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="2ad5c-121">如果應用程式將 **WM \_ SETREDRAW** 訊息傳送至隱藏的視窗，該視窗就會變成可見的 (也就是說，作業系統會將 **WS \_ visible** 樣式加入視窗) 。</span><span class="sxs-lookup"><span data-stu-id="2ad5c-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad5c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ad5c-122">Requirements</span></span>



| <span data-ttu-id="2ad5c-123">需求</span><span class="sxs-lookup"><span data-stu-id="2ad5c-123">Requirement</span></span> | <span data-ttu-id="2ad5c-124">值</span><span class="sxs-lookup"><span data-stu-id="2ad5c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad5c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ad5c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad5c-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ad5c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2ad5c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ad5c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad5c-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ad5c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ad5c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2ad5c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad5c-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2ad5c-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad5c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ad5c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad5c-132">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="2ad5c-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="2ad5c-133">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="2ad5c-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="2ad5c-134">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="2ad5c-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 

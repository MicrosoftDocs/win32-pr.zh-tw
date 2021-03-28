---
description: 會將 WM \_ 列印訊息傳送至視窗，要求它在指定的裝置內容中（最常用於印表機裝置內容）繪製自身。
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: 'WM_PRINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026605"
---
# <a name="wm_print-message"></a><span data-ttu-id="1a6f9-103">WM \_ 列印訊息</span><span class="sxs-lookup"><span data-stu-id="1a6f9-103">WM\_PRINT message</span></span>

<span data-ttu-id="1a6f9-104">會將 **WM \_ 列印** 訊息傳送至視窗，要求它在指定的裝置內容中（最常用於印表機裝置內容）繪製自身。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="1a6f9-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="1a6f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a6f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a6f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6f9-108">要在其中繪製的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a6f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6f9-110">繪圖選項。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-110">The drawing options.</span></span> <span data-ttu-id="1a6f9-111">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1a6f9-112">值</span><span class="sxs-lookup"><span data-stu-id="1a6f9-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="1a6f9-113">意義</span><span class="sxs-lookup"><span data-stu-id="1a6f9-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="1a6f9-114"><dt>**PRF \_ CHECKVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="1a6f9-115">只有當視窗可見時，才會繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="1a6f9-116"><dt>**PRF \_ 子系**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="1a6f9-117">繪製所有可見的子系視窗。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="1a6f9-118"><dt>**PRF \_ 用戶端**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="1a6f9-119">繪製視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="1a6f9-120"><dt>**PRF \_ ERASEBKGND**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="1a6f9-121">在繪製視窗之前清除背景。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="1a6f9-122"><dt>**PRF \_ 非工作區**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="1a6f9-123">繪製視窗的非工作區。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="1a6f9-124"><dt>**\_所擁有的 PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="1a6f9-125">繪製所有擁有的視窗。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a6f9-126">備註</span><span class="sxs-lookup"><span data-stu-id="1a6f9-126">Remarks</span></span>

<span data-ttu-id="1a6f9-127">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據指定的繪圖選項來處理此訊息：如果指定了 PRF \_ CHECKVISIBLE，而且不會顯示視窗，則不執行任何動作。如果指定了 prf 非工作區，請 \_ 在指定的裝置內容中繪製非工作區，如果指定了 prf \_ ERASEBKGND，請傳送一個 [**wm \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)訊息給視窗，如果 \_ 指定了 prf 用戶端 [**\_**](wm-printclient.md) ，請傳送一個 wm PRINTCLIENT 訊息給視窗，如果設定了 prf 子系，請將 \_ 每個可見的子 **\_** \_ **\_** 視窗傳送至 wm 列印訊息。</span><span class="sxs-lookup"><span data-stu-id="1a6f9-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6f9-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a6f9-128">Requirements</span></span>



| <span data-ttu-id="1a6f9-129">需求</span><span class="sxs-lookup"><span data-stu-id="1a6f9-129">Requirement</span></span> | <span data-ttu-id="1a6f9-130">值</span><span class="sxs-lookup"><span data-stu-id="1a6f9-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6f9-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a6f9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6f9-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a6f9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1a6f9-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a6f9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6f9-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a6f9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a6f9-135">標頭</span><span class="sxs-lookup"><span data-stu-id="1a6f9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6f9-136"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6f9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a6f9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6f9-138">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="1a6f9-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="1a6f9-139">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="1a6f9-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="1a6f9-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1a6f9-141">**WM \_ ERASEBKGND**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="1a6f9-142">**WM \_ PRINTCLIENT**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 

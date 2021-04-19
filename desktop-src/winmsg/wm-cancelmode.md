---
description: 傳送以取消特定模式，例如滑鼠捕捉。
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: 'WM_CANCELMODE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975789"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="2e4ab-103">WM \_ CANCELMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="2e4ab-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="2e4ab-104">傳送以取消特定模式，例如滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="2e4ab-105">例如，當顯示對話方塊或訊息方塊時，系統會將此訊息傳送至使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="2e4ab-106">某些函式也會將此訊息明確地傳送到指定的視窗，不論它是否為使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="2e4ab-107">例如， [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函式會在停用指定的視窗時傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="2e4ab-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="2e4ab-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e4ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4ab-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e4ab-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4ab-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e4ab-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e4ab-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4ab-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4ab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e4ab-114">Return value</span></span>

<span data-ttu-id="2e4ab-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-115">Type: **LRESULT**</span></span>

<span data-ttu-id="2e4ab-116">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e4ab-117">備註</span><span class="sxs-lookup"><span data-stu-id="2e4ab-117">Remarks</span></span>

<span data-ttu-id="2e4ab-118">傳送 **WM \_ CANCELMODE** 訊息時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會取消標準捲軸輸入的內部處理、取消內部功能表處理，以及放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="2e4ab-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4ab-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e4ab-119">Requirements</span></span>



| <span data-ttu-id="2e4ab-120">需求</span><span class="sxs-lookup"><span data-stu-id="2e4ab-120">Requirement</span></span> | <span data-ttu-id="2e4ab-121">值</span><span class="sxs-lookup"><span data-stu-id="2e4ab-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4ab-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e4ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4ab-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e4ab-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2e4ab-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e4ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4ab-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e4ab-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e4ab-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2e4ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e4ab-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2e4ab-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e4ab-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e4ab-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e4ab-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e4ab-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2e4ab-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="2e4ab-132">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="2e4ab-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="2e4ab-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e4ab-134">Windows</span><span class="sxs-lookup"><span data-stu-id="2e4ab-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 

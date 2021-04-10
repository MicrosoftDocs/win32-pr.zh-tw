---
title: 'WM_CTLCOLORDLG 訊息 (Winuser .h) '
description: 在系統繪製對話方塊之前，傳送至對話方塊。 藉由回應此訊息，對話方塊可以使用指定的顯示裝置內容控制碼來設定其文字和背景色彩。
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685571"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="66e66-105">WM \_ CTLCOLORDLG 訊息</span><span class="sxs-lookup"><span data-stu-id="66e66-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="66e66-106">在系統繪製對話方塊之前，傳送至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="66e66-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="66e66-107">藉由回應此訊息，對話方塊可以使用指定的顯示裝置內容控制碼來設定其文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="66e66-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="66e66-108">參數</span><span class="sxs-lookup"><span data-stu-id="66e66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66e66-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66e66-110">對話方塊的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="66e66-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="66e66-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66e66-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66e66-112">對話方塊的控制代碼。</span><span class="sxs-lookup"><span data-stu-id="66e66-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e66-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e66-113">Return value</span></span>

<span data-ttu-id="66e66-114">如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。</span><span class="sxs-lookup"><span data-stu-id="66e66-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="66e66-115">系統會使用筆刷來繪製對話方塊的背景。</span><span class="sxs-lookup"><span data-stu-id="66e66-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="66e66-116">備註</span><span class="sxs-lookup"><span data-stu-id="66e66-116">Remarks</span></span>

<span data-ttu-id="66e66-117">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取對話方塊的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="66e66-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="66e66-118">系統不會自動損毀傳回的筆刷。</span><span class="sxs-lookup"><span data-stu-id="66e66-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="66e66-119">當不再需要時，應用程式會負責終結筆刷。</span><span class="sxs-lookup"><span data-stu-id="66e66-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="66e66-120">線上程之間永遠不會傳送 **WM \_ CTLCOLORDLG** 訊息。</span><span class="sxs-lookup"><span data-stu-id="66e66-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="66e66-121">它只會在一個執行緒內傳送。</span><span class="sxs-lookup"><span data-stu-id="66e66-121">It is sent only within one thread.</span></span>

<span data-ttu-id="66e66-122">請注意，會將 **WM \_ CTLCOLORDLG** 訊息傳送至對話方塊本身; 所有其他 \**WM \_ CTLCOLOR \** _ 訊息都會傳送給控制項的擁有者。</span><span class="sxs-lookup"><span data-stu-id="66e66-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="66e66-123">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換為 _ *INT \_ PTR*\* 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="66e66-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="66e66-124">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="66e66-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="66e66-125">[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="66e66-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e66-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e66-126">Requirements</span></span>



| <span data-ttu-id="66e66-127">需求</span><span class="sxs-lookup"><span data-stu-id="66e66-127">Requirement</span></span> | <span data-ttu-id="66e66-128">值</span><span class="sxs-lookup"><span data-stu-id="66e66-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e66-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66e66-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66e66-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66e66-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66e66-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66e66-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66e66-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66e66-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66e66-133">標頭</span><span class="sxs-lookup"><span data-stu-id="66e66-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e66-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="66e66-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e66-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e66-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="66e66-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="66e66-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66e66-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="66e66-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="66e66-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="66e66-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="66e66-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="66e66-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66e66-140">對話方塊</span><span class="sxs-lookup"><span data-stu-id="66e66-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="66e66-141">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="66e66-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="66e66-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="66e66-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="66e66-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="66e66-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 


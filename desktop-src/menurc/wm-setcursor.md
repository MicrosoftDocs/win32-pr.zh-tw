---
title: 'WM_SETCURSOR 訊息 (Winuser .h) '
description: 如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025184"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="254f7-104">WM \_ SETCURSOR 訊息</span><span class="sxs-lookup"><span data-stu-id="254f7-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="254f7-105">如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="254f7-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="254f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="254f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="254f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="254f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="254f7-108">包含游標的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="254f7-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="254f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="254f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="254f7-110">*LParam* 的低序位文字會指定資料指標位置的點擊測試結果。</span><span class="sxs-lookup"><span data-stu-id="254f7-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="254f7-111">如需可能的值，請參閱 [WM_NCHITTEST](../inputdev/wm-nchittest.md) 的傳回值。</span><span class="sxs-lookup"><span data-stu-id="254f7-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="254f7-112">*LParam* 的高序位單字會指定觸發此事件的滑鼠視窗訊息，例如 [WM_MOUSEMOVE](../inputdev/wm-mousemove.md)。</span><span class="sxs-lookup"><span data-stu-id="254f7-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="254f7-113">當視窗進入功能表模式時，此值為零。</span><span class="sxs-lookup"><span data-stu-id="254f7-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="254f7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="254f7-114">Return value</span></span>

<span data-ttu-id="254f7-115">如果應用程式處理此訊息，則應該傳回 **TRUE** 以停止進一步的處理，或傳回 **FALSE** 以繼續。</span><span class="sxs-lookup"><span data-stu-id="254f7-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="254f7-116">備註</span><span class="sxs-lookup"><span data-stu-id="254f7-116">Remarks</span></span>

<span data-ttu-id="254f7-117">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)函式會在處理之前，將 **WM \_ SETCURSOR** 訊息傳遞至父視窗。</span><span class="sxs-lookup"><span data-stu-id="254f7-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="254f7-118">如果父視窗傳回 **TRUE**，則會停止進一步處理。</span><span class="sxs-lookup"><span data-stu-id="254f7-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="254f7-119">將訊息傳遞至視窗的父視窗，可讓父視窗控制子視窗中資料指標的設定。</span><span class="sxs-lookup"><span data-stu-id="254f7-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="254f7-120">**DefWindowProc** 函式也會使用這個訊息，將資料指標設定為不在工作區中的箭號，如果是在工作區中，則為已註冊的類別游標。</span><span class="sxs-lookup"><span data-stu-id="254f7-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="254f7-121">如果 *lParam* 參數的低序位字是 **HTERROR** ，而 *lParam* 的高序位字指定按下其中一個滑鼠按鍵， **DefWindowProc** 就會呼叫 [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) 函數。</span><span class="sxs-lookup"><span data-stu-id="254f7-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="254f7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="254f7-122">Requirements</span></span>



| <span data-ttu-id="254f7-123">需求</span><span class="sxs-lookup"><span data-stu-id="254f7-123">Requirement</span></span> | <span data-ttu-id="254f7-124">值</span><span class="sxs-lookup"><span data-stu-id="254f7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="254f7-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="254f7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="254f7-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="254f7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="254f7-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="254f7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="254f7-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="254f7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="254f7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="254f7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="254f7-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="254f7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="254f7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="254f7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="254f7-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="254f7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="254f7-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="254f7-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="254f7-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="254f7-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="254f7-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="254f7-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="254f7-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="254f7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="254f7-137">游標</span><span class="sxs-lookup"><span data-stu-id="254f7-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 


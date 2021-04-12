---
title: 'WM_NEXTDLGCTL 訊息 (Winuser .h) '
description: 傳送至對話方塊程式，將鍵盤焦點設定至對話方塊中的不同控制項。
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508952"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="fed93-104">WM \_ NEXTDLGCTL 訊息</span><span class="sxs-lookup"><span data-stu-id="fed93-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="fed93-105">傳送至對話方塊程式，將鍵盤焦點設定至對話方塊中的不同控制項。</span><span class="sxs-lookup"><span data-stu-id="fed93-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="fed93-106">參數</span><span class="sxs-lookup"><span data-stu-id="fed93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed93-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fed93-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fed93-108">如果 *lParam* 為 **TRUE**，則此參數會識別接收焦點的控制項。</span><span class="sxs-lookup"><span data-stu-id="fed93-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="fed93-109">如果 *lParam* 為 **FALSE**，則此參數會指出具有 **WS \_ TABSTOP** 樣式的下一個或上一個控制項是否會收到焦點。</span><span class="sxs-lookup"><span data-stu-id="fed93-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="fed93-110">如果 *wParam* 為零，則下一個控制項會接收焦點;否則，具有 **WS \_ TABSTOP** 樣式的先前控制項就會收到焦點。</span><span class="sxs-lookup"><span data-stu-id="fed93-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="fed93-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fed93-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fed93-112">低序位單字表示系統使用 *wParam* 的方式。</span><span class="sxs-lookup"><span data-stu-id="fed93-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="fed93-113">如果低序位字是 **TRUE**，則 *wParam* 是與接收焦點的控制項相關聯的控制碼;否則， *wParam* 是一個旗標，指出下一個或前一個具有 **WS \_ TABSTOP** 樣式的控制項是否會收到焦點。</span><span class="sxs-lookup"><span data-stu-id="fed93-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed93-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fed93-114">Return value</span></span>

<span data-ttu-id="fed93-115">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="fed93-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fed93-116">備註</span><span class="sxs-lookup"><span data-stu-id="fed93-116">Remarks</span></span>

<span data-ttu-id="fed93-117">這則訊息會執行其他對話方塊管理作業，而非 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函式 **WM \_ NEXTDLGCTL** 會更新預設的按鍵框線、設定預設的控制項識別碼，並自動選取編輯控制項的文字 (如果目標視窗是編輯控制項) 。</span><span class="sxs-lookup"><span data-stu-id="fed93-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="fed93-118">如果您的應用程式將會同時處理設定焦點的其他訊息，請不要使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式來傳送 **WM \_ NEXTDLGCTL** 訊息。</span><span class="sxs-lookup"><span data-stu-id="fed93-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="fed93-119">請改用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="fed93-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed93-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fed93-120">Requirements</span></span>



| <span data-ttu-id="fed93-121">需求</span><span class="sxs-lookup"><span data-stu-id="fed93-121">Requirement</span></span> | <span data-ttu-id="fed93-122">值</span><span class="sxs-lookup"><span data-stu-id="fed93-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed93-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fed93-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fed93-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fed93-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fed93-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fed93-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fed93-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fed93-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fed93-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fed93-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed93-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fed93-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed93-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fed93-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="fed93-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="fed93-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fed93-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="fed93-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="fed93-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="fed93-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="fed93-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="fed93-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="fed93-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="fed93-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fed93-135">對話方塊</span><span class="sxs-lookup"><span data-stu-id="fed93-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 


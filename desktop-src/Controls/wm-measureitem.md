---
title: 'WM_MEASUREITEM 訊息 (Winuser .h) '
description: 當控制項或功能表建立時，傳送至下拉式方塊、清單方塊、清單視圖或功能表項目的擁有者視窗。
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843876"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="f1bc6-104">WM \_ MEASUREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="f1bc6-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="f1bc6-105">當控制項或功能表建立時，傳送至下拉式方塊、清單方塊、清單視圖或功能表項目的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="f1bc6-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f1bc6-107">參數</span><span class="sxs-lookup"><span data-stu-id="f1bc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bc6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1bc6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1bc6-109">包含 *lParam* 參數所指向之 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的 **CtlID** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="f1bc6-110">此值會識別傳送了 **WM \_ MEASUREITEM** 訊息的控制項。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="f1bc6-111">如果值為零，則會由功能表傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="f1bc6-112">如果此值為非零值，則會由下拉式方塊或清單方塊傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="f1bc6-113">如果此值為非零值，而且 *lParam* 所指向之 **MEASUREITEMSTRUCT** 的 **ITEMID** 成員值是 (UINT) 1，則訊息是由組合編輯欄位所傳送。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1bc6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1bc6-115">[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的指標，其中包含主控描繪控制項或功能表項目的維度。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bc6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1bc6-116">Return value</span></span>

<span data-ttu-id="f1bc6-117">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1bc6-118">備註</span><span class="sxs-lookup"><span data-stu-id="f1bc6-118">Remarks</span></span>

<span data-ttu-id="f1bc6-119">當擁有者視窗收到 **WM \_ MEASUREITEM** 訊息時，擁有者會填入訊息的 *lParam* 參數所指向的 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構並傳回; 這會通知系統有控制項的維度。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="f1bc6-120">如果清單方塊或下拉式方塊是以 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 或 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式來建立，則會將此訊息傳送給控制項中每個專案的擁有者; 否則，此訊息會傳送一次。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="f1bc6-121">系統會將 **wm \_ MEASUREITEM** 訊息傳送至下拉式方塊的擁有者視窗，以及使用 OWNERDRAWFIXED 樣式建立的清單方塊，然後再傳送 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="f1bc6-122">如此一來，當擁有者收到此訊息時，系統尚未判斷控制項中所使用之字型的高度和寬度;需要這些值的函式呼叫和計算應該會出現在應用程式或程式庫的主要功能中。</span><span class="sxs-lookup"><span data-stu-id="f1bc6-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bc6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1bc6-123">Requirements</span></span>



| <span data-ttu-id="f1bc6-124">需求</span><span class="sxs-lookup"><span data-stu-id="f1bc6-124">Requirement</span></span> | <span data-ttu-id="f1bc6-125">值</span><span class="sxs-lookup"><span data-stu-id="f1bc6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bc6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1bc6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bc6-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1bc6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1bc6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1bc6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bc6-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1bc6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1bc6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f1bc6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1bc6-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f1bc6-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1bc6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1bc6-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1bc6-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="f1bc6-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1bc6-134">**MEASUREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1bc6-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="f1bc6-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="f1bc6-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f1bc6-136">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="f1bc6-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 


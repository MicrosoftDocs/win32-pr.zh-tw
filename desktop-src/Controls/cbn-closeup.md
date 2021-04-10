---
title: 'CBN_CLOSEUP (Winuser 的通知碼) '
description: 在下拉式方塊的清單方塊已關閉時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106445"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="849ed-105">CBN \_ 特寫通知碼</span><span class="sxs-lookup"><span data-stu-id="849ed-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="849ed-106">在下拉式方塊的清單方塊已關閉時傳送。</span><span class="sxs-lookup"><span data-stu-id="849ed-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="849ed-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="849ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="849ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="849ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="849ed-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="849ed-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="849ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="849ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="849ed-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="849ed-114">備註</span><span class="sxs-lookup"><span data-stu-id="849ed-114">Remarks</span></span>

<span data-ttu-id="849ed-115">如果使用者變更目前的選取範圍，下拉式方塊也會在下拉式清單關閉時傳送 [CBN \_ SELCHANGE](cbn-selchange.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="849ed-116">一般來說，您無法預測通知碼的傳送順序。</span><span class="sxs-lookup"><span data-stu-id="849ed-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="849ed-117">尤其是在 \_ CBN \_ 特寫通知碼之前或之後，可能會發生 CBN SELCHANGE 通知碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="849ed-118">若要在每次使用者選取清單專案時執行特定進程，您可以處理 [CBN \_ SELCHANGE](cbn-selchange.md) 或 CBN \_ 特寫通知碼。</span><span class="sxs-lookup"><span data-stu-id="849ed-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="849ed-119">一般來說，您會先等候 CBN \_ 特寫通知碼，再處理目前選取範圍內的變更。</span><span class="sxs-lookup"><span data-stu-id="849ed-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="849ed-120">如果需要大量的處理，這可能特別重要。</span><span class="sxs-lookup"><span data-stu-id="849ed-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="849ed-121">此通知碼不會傳送至具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="849ed-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="849ed-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="849ed-122">Requirements</span></span>



| <span data-ttu-id="849ed-123">需求</span><span class="sxs-lookup"><span data-stu-id="849ed-123">Requirement</span></span> | <span data-ttu-id="849ed-124">值</span><span class="sxs-lookup"><span data-stu-id="849ed-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="849ed-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="849ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="849ed-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="849ed-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="849ed-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="849ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="849ed-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="849ed-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="849ed-129">標頭</span><span class="sxs-lookup"><span data-stu-id="849ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="849ed-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="849ed-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="849ed-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="849ed-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="849ed-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="849ed-133">CBN \_ 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="849ed-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="849ed-134">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="849ed-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="849ed-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="849ed-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="849ed-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="849ed-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="849ed-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="849ed-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="849ed-138">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="849ed-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


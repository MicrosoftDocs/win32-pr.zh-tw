---
title: 'LBN_SELCHANGE (Winuser 的通知碼) '
description: 通知應用程式，清單方塊中的選取專案已因使用者輸入而變更。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685925"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="7315d-105">LBN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="7315d-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="7315d-106">通知應用程式，清單方塊中的選取專案已因使用者輸入而變更。</span><span class="sxs-lookup"><span data-stu-id="7315d-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="7315d-107">清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7315d-108">參數</span><span class="sxs-lookup"><span data-stu-id="7315d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7315d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7315d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7315d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="7315d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7315d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7315d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7315d-113">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7315d-114">備註</span><span class="sxs-lookup"><span data-stu-id="7315d-114">Remarks</span></span>

<span data-ttu-id="7315d-115">此通知碼只會由具有 [**磅 \_ 通知**](list-box-styles.md) 樣式的清單方塊來傳送。</span><span class="sxs-lookup"><span data-stu-id="7315d-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="7315d-116">如果 [**LB \_ SETSEL**](lb-setsel.md)、 [**LB \_ SETCURSEL**](lb-setcursel.md)、 [**lb \_ SELECTSTRING**](lb-selectstring.md)、 [**lb \_ SELITEMRANGE**](lb-selitemrange.md) 或 [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) message 變更選取專案，則不會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="7315d-117">若為多重選取清單方塊， \_ 當使用者按下方向鍵時，即使選取範圍未變更，也會傳送 LBN SELCHANGE 通知碼。</span><span class="sxs-lookup"><span data-stu-id="7315d-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="7315d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7315d-118">Requirements</span></span>



| <span data-ttu-id="7315d-119">需求</span><span class="sxs-lookup"><span data-stu-id="7315d-119">Requirement</span></span> | <span data-ttu-id="7315d-120">值</span><span class="sxs-lookup"><span data-stu-id="7315d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7315d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7315d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7315d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7315d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7315d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7315d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7315d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7315d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7315d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7315d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7315d-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7315d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7315d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7315d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7315d-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="7315d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7315d-129">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="7315d-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="7315d-130">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="7315d-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="7315d-131">LBN \_ SELCANCEL</span><span class="sxs-lookup"><span data-stu-id="7315d-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="7315d-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="7315d-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7315d-133">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="7315d-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


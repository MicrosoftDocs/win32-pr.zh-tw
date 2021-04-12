---
title: 'CBN_SELCHANGE (Winuser 的通知碼) '
description: 當使用者變更下拉式方塊清單方塊中目前的選取範圍時傳送。
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935098"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="b2867-104">CBN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="b2867-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="b2867-105">當使用者變更下拉式方塊清單方塊中目前的選取範圍時傳送。</span><span class="sxs-lookup"><span data-stu-id="b2867-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="b2867-106">使用者可以在清單方塊中按一下或使用方向鍵來變更選取專案。</span><span class="sxs-lookup"><span data-stu-id="b2867-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="b2867-107">下拉式方塊的父視窗會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="b2867-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b2867-108">參數</span><span class="sxs-lookup"><span data-stu-id="b2867-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2867-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2867-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2867-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2867-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="b2867-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="b2867-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b2867-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2867-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2867-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2867-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2867-114">備註</span><span class="sxs-lookup"><span data-stu-id="b2867-114">Remarks</span></span>

<span data-ttu-id="b2867-115">若要取得目前選取範圍的索引，請將 [**CB \_ GETCURSEL**](cb-getcursel.md) 訊息傳送至控制項。</span><span class="sxs-lookup"><span data-stu-id="b2867-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="b2867-116">\_使用 [**CB \_ SETCURSEL**](cb-setcursel.md)訊息設定目前的選取範圍時，不會傳送 CBN SELCHANGE 通知碼。</span><span class="sxs-lookup"><span data-stu-id="b2867-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2867-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2867-117">Requirements</span></span>



| <span data-ttu-id="b2867-118">需求</span><span class="sxs-lookup"><span data-stu-id="b2867-118">Requirement</span></span> | <span data-ttu-id="b2867-119">值</span><span class="sxs-lookup"><span data-stu-id="b2867-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2867-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2867-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2867-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2867-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2867-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2867-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2867-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2867-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2867-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b2867-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2867-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b2867-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2867-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2867-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2867-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="b2867-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2867-128">CBN \_ 特寫</span><span class="sxs-lookup"><span data-stu-id="b2867-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="b2867-129">CBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="b2867-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="b2867-130">**CB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="b2867-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="b2867-131">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="b2867-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="b2867-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="b2867-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b2867-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2867-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b2867-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2867-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b2867-135">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="b2867-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


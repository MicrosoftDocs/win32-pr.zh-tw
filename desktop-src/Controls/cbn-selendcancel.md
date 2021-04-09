---
title: 'CBN_SELENDCANCEL (Winuser 的通知碼) '
description: 當使用者選取專案時傳送，然後選取另一個控制項或關閉對話方塊。 這表示要忽略使用者的初始選項。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686294"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="0b81a-106">CBN \_ SELENDCANCEL 通知碼</span><span class="sxs-lookup"><span data-stu-id="0b81a-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="0b81a-107">當使用者選取專案時傳送，然後選取另一個控制項或關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0b81a-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="0b81a-108">這表示要忽略使用者的初始選項。</span><span class="sxs-lookup"><span data-stu-id="0b81a-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="0b81a-109">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="0b81a-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0b81a-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b81a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b81a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b81a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b81a-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b81a-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="0b81a-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="0b81a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0b81a-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b81a-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b81a-115">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0b81a-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b81a-116">備註</span><span class="sxs-lookup"><span data-stu-id="0b81a-116">Remarks</span></span>

<span data-ttu-id="0b81a-117">在具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊中， \_ 不會傳送 CBN SELENDCANCEL 通知碼。</span><span class="sxs-lookup"><span data-stu-id="0b81a-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="0b81a-118">[CBN \_ SELENDOK](cbn-selendok.md)通知碼會在每個[CBN \_ SELCHANGE](cbn-selchange.md)通知碼之前立即傳送。</span><span class="sxs-lookup"><span data-stu-id="0b81a-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b81a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b81a-119">Requirements</span></span>



| <span data-ttu-id="0b81a-120">需求</span><span class="sxs-lookup"><span data-stu-id="0b81a-120">Requirement</span></span> | <span data-ttu-id="0b81a-121">值</span><span class="sxs-lookup"><span data-stu-id="0b81a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b81a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b81a-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b81a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b81a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b81a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b81a-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b81a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b81a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0b81a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b81a-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0b81a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b81a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b81a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b81a-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="0b81a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b81a-130">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="0b81a-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="0b81a-131">CBN \_ SELENDOK</span><span class="sxs-lookup"><span data-stu-id="0b81a-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="0b81a-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="0b81a-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0b81a-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b81a-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0b81a-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b81a-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b81a-135">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="0b81a-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


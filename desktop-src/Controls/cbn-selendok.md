---
title: 'CBN_SELENDOK (Winuser 的通知碼) '
description: 當使用者選取清單專案時傳送，或選取專案然後關閉清單。 這表示會處理使用者的選取專案。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965905"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="e097d-106">CBN \_ SELENDOK 通知碼</span><span class="sxs-lookup"><span data-stu-id="e097d-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="e097d-107">當使用者選取清單專案時傳送，或選取專案然後關閉清單。</span><span class="sxs-lookup"><span data-stu-id="e097d-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="e097d-108">這表示會處理使用者的選取專案。</span><span class="sxs-lookup"><span data-stu-id="e097d-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="e097d-109">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="e097d-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e097d-110">參數</span><span class="sxs-lookup"><span data-stu-id="e097d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e097d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e097d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e097d-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="e097d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="e097d-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="e097d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e097d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e097d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e097d-115">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e097d-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e097d-116">備註</span><span class="sxs-lookup"><span data-stu-id="e097d-116">Remarks</span></span>

<span data-ttu-id="e097d-117">在具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊中，CBN \_ SELENDOK 通知碼會在每個 [CBN \_ SELCHANGE](cbn-selchange.md) 通知程式碼之前立即傳送。</span><span class="sxs-lookup"><span data-stu-id="e097d-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e097d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e097d-118">Requirements</span></span>



| <span data-ttu-id="e097d-119">需求</span><span class="sxs-lookup"><span data-stu-id="e097d-119">Requirement</span></span> | <span data-ttu-id="e097d-120">值</span><span class="sxs-lookup"><span data-stu-id="e097d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e097d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e097d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e097d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e097d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e097d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e097d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e097d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e097d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e097d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e097d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e097d-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e097d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e097d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e097d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e097d-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="e097d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e097d-129">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="e097d-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="e097d-130">CBN \_ SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="e097d-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="e097d-131">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="e097d-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e097d-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e097d-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e097d-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e097d-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e097d-134">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="e097d-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


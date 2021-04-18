---
title: 'CBN_DROPDOWN (Winuser 的通知碼) '
description: 在下拉式方塊的清單方塊即將顯示時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965732"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="da349-105">CBN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="da349-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="da349-106">在下拉式方塊的清單方塊即將顯示時傳送。</span><span class="sxs-lookup"><span data-stu-id="da349-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="da349-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="da349-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="da349-108">參數</span><span class="sxs-lookup"><span data-stu-id="da349-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da349-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da349-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da349-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="da349-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="da349-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="da349-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="da349-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da349-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da349-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da349-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da349-114">備註</span><span class="sxs-lookup"><span data-stu-id="da349-114">Remarks</span></span>

<span data-ttu-id="da349-115">只有當下拉式方塊具有 [**cbs \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式時，才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="da349-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="da349-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="da349-116">Requirements</span></span>



| <span data-ttu-id="da349-117">需求</span><span class="sxs-lookup"><span data-stu-id="da349-117">Requirement</span></span> | <span data-ttu-id="da349-118">值</span><span class="sxs-lookup"><span data-stu-id="da349-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da349-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da349-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da349-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da349-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da349-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da349-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da349-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da349-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da349-123">標頭</span><span class="sxs-lookup"><span data-stu-id="da349-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="da349-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="da349-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da349-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da349-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="da349-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="da349-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da349-127">CBN \_ 特寫</span><span class="sxs-lookup"><span data-stu-id="da349-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="da349-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="da349-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="da349-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da349-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="da349-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da349-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="da349-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="da349-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


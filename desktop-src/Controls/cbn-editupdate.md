---
title: 'CBN_EDITUPDATE (Winuser 的通知碼) '
description: 當下拉式方塊的編輯控制項部分即將顯示變更的文字時傳送。
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106284"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="277c8-104">CBN \_ EDITUPDATE 通知碼</span><span class="sxs-lookup"><span data-stu-id="277c8-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="277c8-105">當下拉式方塊的編輯控制項部分即將顯示變更的文字時傳送。</span><span class="sxs-lookup"><span data-stu-id="277c8-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="277c8-106">此通知碼會在控制項格式化文字之後，但在顯示文字之前傳送。</span><span class="sxs-lookup"><span data-stu-id="277c8-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="277c8-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="277c8-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="277c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="277c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="277c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="277c8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="277c8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="277c8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="277c8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="277c8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="277c8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="277c8-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="277c8-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="277c8-114">備註</span><span class="sxs-lookup"><span data-stu-id="277c8-114">Remarks</span></span>

<span data-ttu-id="277c8-115">如果下拉式方塊具有 [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) 樣式，則不會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="277c8-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="277c8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="277c8-116">Requirements</span></span>



| <span data-ttu-id="277c8-117">需求</span><span class="sxs-lookup"><span data-stu-id="277c8-117">Requirement</span></span> | <span data-ttu-id="277c8-118">值</span><span class="sxs-lookup"><span data-stu-id="277c8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="277c8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="277c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="277c8-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="277c8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="277c8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="277c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="277c8-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="277c8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="277c8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="277c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="277c8-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="277c8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277c8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="277c8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="277c8-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="277c8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="277c8-127">CBN \_ EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="277c8-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="277c8-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="277c8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="277c8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="277c8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="277c8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="277c8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="277c8-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="277c8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


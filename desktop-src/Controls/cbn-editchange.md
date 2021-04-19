---
title: 'CBN_EDITCHANGE (Winuser 的通知碼) '
description: 在使用者採取動作可能改變下拉式方塊的編輯控制項部分中的文字之後傳送。
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965328"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="58a7d-104">CBN \_ EDITCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="58a7d-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="58a7d-105">在使用者採取動作可能改變下拉式方塊的編輯控制項部分中的文字之後傳送。</span><span class="sxs-lookup"><span data-stu-id="58a7d-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="58a7d-106">不同于 [CBN \_ EDITUPDATE](cbn-editupdate.md) 通知碼，系統會在系統更新畫面之後傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="58a7d-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="58a7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="58a7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a7d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58a7d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58a7d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="58a7d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="58a7d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58a7d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58a7d-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58a7d-114">備註</span><span class="sxs-lookup"><span data-stu-id="58a7d-114">Remarks</span></span>

<span data-ttu-id="58a7d-115">如果下拉式方塊具有 [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) 樣式，則不會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="58a7d-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a7d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="58a7d-116">Requirements</span></span>



| <span data-ttu-id="58a7d-117">需求</span><span class="sxs-lookup"><span data-stu-id="58a7d-117">Requirement</span></span> | <span data-ttu-id="58a7d-118">值</span><span class="sxs-lookup"><span data-stu-id="58a7d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a7d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58a7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58a7d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58a7d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58a7d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58a7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58a7d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58a7d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58a7d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="58a7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a7d-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="58a7d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a7d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58a7d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="58a7d-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="58a7d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58a7d-127">CBN \_ EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="58a7d-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="58a7d-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="58a7d-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="58a7d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58a7d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="58a7d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58a7d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="58a7d-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="58a7d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


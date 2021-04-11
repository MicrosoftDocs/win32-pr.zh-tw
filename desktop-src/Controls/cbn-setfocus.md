---
title: 'CBN_SETFOCUS (Winuser 的通知碼) '
description: 在下拉式方塊收到鍵盤焦點時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- CBN_SETFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317528"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="18a31-105">CBN \_ SETFOCUS 通知碼</span><span class="sxs-lookup"><span data-stu-id="18a31-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="18a31-106">在下拉式方塊收到鍵盤焦點時傳送。</span><span class="sxs-lookup"><span data-stu-id="18a31-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="18a31-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="18a31-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="18a31-108">參數</span><span class="sxs-lookup"><span data-stu-id="18a31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18a31-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18a31-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="18a31-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="18a31-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="18a31-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="18a31-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18a31-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18a31-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18a31-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18a31-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="18a31-114">Requirements</span></span>



| <span data-ttu-id="18a31-115">需求</span><span class="sxs-lookup"><span data-stu-id="18a31-115">Requirement</span></span> | <span data-ttu-id="18a31-116">值</span><span class="sxs-lookup"><span data-stu-id="18a31-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a31-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18a31-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18a31-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18a31-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18a31-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18a31-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18a31-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18a31-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18a31-121">標頭</span><span class="sxs-lookup"><span data-stu-id="18a31-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18a31-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="18a31-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a31-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18a31-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="18a31-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="18a31-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18a31-125">CBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="18a31-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="18a31-126">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="18a31-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="18a31-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18a31-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="18a31-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18a31-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="18a31-129">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="18a31-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


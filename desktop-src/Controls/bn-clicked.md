---
title: 'BN_CLICKED (Winuser 的通知碼) '
description: 當使用者按一下按鈕時傳送。 按鈕的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- BN_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094183"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="341d9-105">BN \_ 按一下通知碼</span><span class="sxs-lookup"><span data-stu-id="341d9-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="341d9-106">當使用者按一下按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="341d9-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="341d9-107">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="341d9-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="341d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="341d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="341d9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="341d9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="341d9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="341d9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="341d9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="341d9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="341d9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="341d9-113">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="341d9-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="341d9-114">備註</span><span class="sxs-lookup"><span data-stu-id="341d9-114">Remarks</span></span>

<span data-ttu-id="341d9-115">[已停用] 按鈕不會將 BN \_ 按一下的通知程式碼傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="341d9-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="341d9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="341d9-116">Requirements</span></span>



| <span data-ttu-id="341d9-117">需求</span><span class="sxs-lookup"><span data-stu-id="341d9-117">Requirement</span></span> | <span data-ttu-id="341d9-118">值</span><span class="sxs-lookup"><span data-stu-id="341d9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341d9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="341d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="341d9-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="341d9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="341d9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="341d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="341d9-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="341d9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="341d9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="341d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="341d9-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="341d9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="341d9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="341d9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="341d9-126">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="341d9-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="341d9-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="341d9-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="341d9-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="341d9-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="341d9-129">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="341d9-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


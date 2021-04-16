---
title: 'BN_KILLFOCUS (Winuser 的通知碼) '
description: 當按鈕失去鍵盤焦點時傳送。 此按鈕必須有 BS \_ 通知樣式才能傳送此通知碼。 按鈕的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464665"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="895b3-106">BN \_ KILLFOCUS 通知碼</span><span class="sxs-lookup"><span data-stu-id="895b3-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="895b3-107">當按鈕失去鍵盤焦點時傳送。</span><span class="sxs-lookup"><span data-stu-id="895b3-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="895b3-108">此按鈕必須有 [**BS \_ 通知**](button-styles.md) 樣式才能傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="895b3-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="895b3-109">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="895b3-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="895b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="895b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="895b3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="895b3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="895b3-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="895b3-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="895b3-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="895b3-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="895b3-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="895b3-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="895b3-115">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="895b3-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="895b3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="895b3-116">Requirements</span></span>



| <span data-ttu-id="895b3-117">需求</span><span class="sxs-lookup"><span data-stu-id="895b3-117">Requirement</span></span> | <span data-ttu-id="895b3-118">值</span><span class="sxs-lookup"><span data-stu-id="895b3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895b3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="895b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="895b3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="895b3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="895b3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="895b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="895b3-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="895b3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="895b3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="895b3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="895b3-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="895b3-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="895b3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="895b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="895b3-126">BN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="895b3-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 


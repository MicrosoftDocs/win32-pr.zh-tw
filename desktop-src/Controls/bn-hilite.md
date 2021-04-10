---
title: 'BN_HILITE (Winuser 的通知碼) '
description: 當使用者選取按鈕時傳送。
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934097"
---
# <a name="bn_hilite-notification-code"></a><span data-ttu-id="3fa90-104">BN \_ HILITE 通知碼</span><span class="sxs-lookup"><span data-stu-id="3fa90-104">BN\_HILITE notification code</span></span>

<span data-ttu-id="3fa90-105">當使用者選取按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="3fa90-105">Sent when the user selects a button.</span></span>

> [!Note]  
> <span data-ttu-id="3fa90-106">此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="3fa90-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="3fa90-107">應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="3fa90-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="3fa90-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="3fa90-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="3fa90-109">參數</span><span class="sxs-lookup"><span data-stu-id="3fa90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa90-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fa90-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa90-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="3fa90-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="3fa90-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="3fa90-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="3fa90-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fa90-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa90-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3fa90-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fa90-115">備註</span><span class="sxs-lookup"><span data-stu-id="3fa90-115">Remarks</span></span>

<span data-ttu-id="3fa90-116">BN \_ HILITE 與 [BN \_ 推](bn-pushed.md) 播的通知碼相同。</span><span class="sxs-lookup"><span data-stu-id="3fa90-116">BN\_HILITE is the same as the [BN\_PUSHED](bn-pushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa90-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fa90-117">Requirements</span></span>



| <span data-ttu-id="3fa90-118">需求</span><span class="sxs-lookup"><span data-stu-id="3fa90-118">Requirement</span></span> | <span data-ttu-id="3fa90-119">值</span><span class="sxs-lookup"><span data-stu-id="3fa90-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa90-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fa90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa90-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fa90-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3fa90-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fa90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa90-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fa90-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3fa90-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3fa90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa90-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3fa90-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


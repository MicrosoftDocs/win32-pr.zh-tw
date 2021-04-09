---
title: 'BN_UNPUSHED (Winuser 的通知碼) '
description: 當按鈕的推送狀態設定為未推送時傳送。
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094076"
---
# <a name="bn_unpushed-notification-code"></a><span data-ttu-id="c6a35-104">BN \_ 未推送通知碼</span><span class="sxs-lookup"><span data-stu-id="c6a35-104">BN\_UNPUSHED notification code</span></span>

<span data-ttu-id="c6a35-105">當按鈕的推送狀態設定為未推送時傳送。</span><span class="sxs-lookup"><span data-stu-id="c6a35-105">Sent when the push state of a button is set to unpushed.</span></span>

> [!Note]  
> <span data-ttu-id="c6a35-106">此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="c6a35-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="c6a35-107">應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="c6a35-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="c6a35-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c6a35-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c6a35-109">參數</span><span class="sxs-lookup"><span data-stu-id="c6a35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a35-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6a35-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a35-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a35-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="c6a35-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="c6a35-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c6a35-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6a35-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a35-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6a35-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6a35-115">備註</span><span class="sxs-lookup"><span data-stu-id="c6a35-115">Remarks</span></span>

<span data-ttu-id="c6a35-116">BN \_ 未推送與 [BN \_ UNHILITE](bn-unhilite.md) 通知碼相同。</span><span class="sxs-lookup"><span data-stu-id="c6a35-116">BN\_UNPUSHED is the same as the [BN\_UNHILITE](bn-unhilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a35-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6a35-117">Requirements</span></span>



| <span data-ttu-id="c6a35-118">需求</span><span class="sxs-lookup"><span data-stu-id="c6a35-118">Requirement</span></span> | <span data-ttu-id="c6a35-119">值</span><span class="sxs-lookup"><span data-stu-id="c6a35-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a35-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6a35-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a35-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6a35-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6a35-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6a35-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a35-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6a35-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6a35-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c6a35-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6a35-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c6a35-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a35-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6a35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a35-127">BN \_ 推送</span><span class="sxs-lookup"><span data-stu-id="c6a35-127">BN\_PUSHED</span></span>](bn-pushed.md)
</dt> </dl>

 


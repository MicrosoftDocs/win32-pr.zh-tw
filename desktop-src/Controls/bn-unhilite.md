---
title: 'BN_UNHILITE (Winuser 的通知碼) '
description: 當醒目提示應該從按鈕移除時傳送。
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- BN_UNHILITE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934047"
---
# <a name="bn_unhilite-notification-code"></a><span data-ttu-id="d29c7-104">BN \_ UNHILITE 通知碼</span><span class="sxs-lookup"><span data-stu-id="d29c7-104">BN\_UNHILITE notification code</span></span>

<span data-ttu-id="d29c7-105">當醒目提示應該從按鈕移除時傳送。</span><span class="sxs-lookup"><span data-stu-id="d29c7-105">Sent when the highlight should be removed from a button.</span></span>

> [!Note]  
> <span data-ttu-id="d29c7-106">此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="d29c7-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="d29c7-107">應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="d29c7-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="d29c7-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="d29c7-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d29c7-109">參數</span><span class="sxs-lookup"><span data-stu-id="d29c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29c7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d29c7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c7-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="d29c7-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="d29c7-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="d29c7-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d29c7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d29c7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c7-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d29c7-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d29c7-115">備註</span><span class="sxs-lookup"><span data-stu-id="d29c7-115">Remarks</span></span>

<span data-ttu-id="d29c7-116">BN \_ UNHILITE 與 [BN \_ 未推送](bn-unpushed.md) 通知碼相同。</span><span class="sxs-lookup"><span data-stu-id="d29c7-116">BN\_UNHILITE is the same as the [BN\_UNPUSHED](bn-unpushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29c7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d29c7-117">Requirements</span></span>



| <span data-ttu-id="d29c7-118">需求</span><span class="sxs-lookup"><span data-stu-id="d29c7-118">Requirement</span></span> | <span data-ttu-id="d29c7-119">值</span><span class="sxs-lookup"><span data-stu-id="d29c7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d29c7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d29c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d29c7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d29c7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d29c7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d29c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d29c7-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d29c7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d29c7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d29c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d29c7-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d29c7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


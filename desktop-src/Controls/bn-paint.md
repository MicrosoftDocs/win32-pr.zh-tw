---
title: 'BN_PAINT (Winuser 的通知碼) '
description: 在應繪製按鈕時傳送。
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024602"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="e9a60-104">BN \_ 油漆通知碼</span><span class="sxs-lookup"><span data-stu-id="e9a60-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="e9a60-105">在應繪製按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="e9a60-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="e9a60-106">此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="e9a60-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="e9a60-107">應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="e9a60-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="e9a60-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="e9a60-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e9a60-109">參數</span><span class="sxs-lookup"><span data-stu-id="e9a60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a60-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9a60-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9a60-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9a60-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="e9a60-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="e9a60-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e9a60-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9a60-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9a60-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e9a60-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9a60-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9a60-115">Requirements</span></span>



| <span data-ttu-id="e9a60-116">需求</span><span class="sxs-lookup"><span data-stu-id="e9a60-116">Requirement</span></span> | <span data-ttu-id="e9a60-117">值</span><span class="sxs-lookup"><span data-stu-id="e9a60-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a60-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9a60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a60-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9a60-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9a60-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9a60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a60-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9a60-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9a60-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e9a60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9a60-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e9a60-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


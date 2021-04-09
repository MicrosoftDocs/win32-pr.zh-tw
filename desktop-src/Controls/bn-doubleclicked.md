---
title: 'BN_DOUBLECLICKED (Winuser 的通知碼) '
description: 當使用者按兩下按鈕時傳送。
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843300"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="03a94-104">BN \_ DOUBLECLICKED 通知碼</span><span class="sxs-lookup"><span data-stu-id="03a94-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="03a94-105">當使用者按兩下按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="03a94-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="03a94-106">系統會自動為 [**BS \_ USERBUTTON**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕和 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="03a94-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="03a94-107">其他按鈕類型只有在 \_ 有 [**BS \_ 通知**](button-styles.md) 樣式時，才會傳送 BN DOUBLECLICKED。</span><span class="sxs-lookup"><span data-stu-id="03a94-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="03a94-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="03a94-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="03a94-109">參數</span><span class="sxs-lookup"><span data-stu-id="03a94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a94-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03a94-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03a94-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="03a94-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="03a94-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="03a94-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="03a94-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03a94-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03a94-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03a94-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03a94-115">備註</span><span class="sxs-lookup"><span data-stu-id="03a94-115">Remarks</span></span>

<span data-ttu-id="03a94-116">BN \_ DOUBLECLICKED 與 [BN \_ DBLCLK](bn-dblclk.md) 通知碼相同。</span><span class="sxs-lookup"><span data-stu-id="03a94-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a94-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="03a94-117">Requirements</span></span>



| <span data-ttu-id="03a94-118">需求</span><span class="sxs-lookup"><span data-stu-id="03a94-118">Requirement</span></span> | <span data-ttu-id="03a94-119">值</span><span class="sxs-lookup"><span data-stu-id="03a94-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a94-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03a94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03a94-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a94-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03a94-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03a94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03a94-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03a94-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03a94-124">標頭</span><span class="sxs-lookup"><span data-stu-id="03a94-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a94-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="03a94-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


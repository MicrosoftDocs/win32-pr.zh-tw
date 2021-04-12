---
title: 'BN_DBLCLK (Winuser 的通知碼) '
description: 當使用者按兩下按鈕時傳送。
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024861"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="9b606-104">BN \_ DBLCLK 通知碼</span><span class="sxs-lookup"><span data-stu-id="9b606-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="9b606-105">當使用者按兩下按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="9b606-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="9b606-106">系統會自動為 [**BS \_ USERBUTTON**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕和 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="9b606-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="9b606-107">其他按鈕類型只有在 \_ 有 [**BS \_ 通知**](button-styles.md) 樣式時，才會傳送 BN DBLCLK。</span><span class="sxs-lookup"><span data-stu-id="9b606-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="9b606-108">按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="9b606-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="9b606-109">參數</span><span class="sxs-lookup"><span data-stu-id="9b606-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b606-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b606-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b606-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b606-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="9b606-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="9b606-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9b606-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b606-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b606-114">按鈕的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b606-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b606-115">備註</span><span class="sxs-lookup"><span data-stu-id="9b606-115">Remarks</span></span>

<span data-ttu-id="9b606-116">BN \_ DBLCLK 與 [BN \_ DOUBLECLICKED](bn-doubleclicked.md) 通知碼相同。</span><span class="sxs-lookup"><span data-stu-id="9b606-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b606-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b606-117">Requirements</span></span>



| <span data-ttu-id="9b606-118">需求</span><span class="sxs-lookup"><span data-stu-id="9b606-118">Requirement</span></span> | <span data-ttu-id="9b606-119">值</span><span class="sxs-lookup"><span data-stu-id="9b606-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b606-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b606-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b606-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b606-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9b606-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b606-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b606-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b606-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b606-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9b606-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b606-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9b606-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b606-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b606-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b606-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="9b606-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b606-128">BN \_ 按一下</span><span class="sxs-lookup"><span data-stu-id="9b606-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="9b606-129">BN \_ DOUBLECLICKED</span><span class="sxs-lookup"><span data-stu-id="9b606-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="9b606-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="9b606-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9b606-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="9b606-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


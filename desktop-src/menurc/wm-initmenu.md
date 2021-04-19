---
title: 'WM_INITMENU 訊息 (Winuser .h) '
description: 當功能表即將變成作用中時傳送。
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968992"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="62e6d-104">WM \_ INITMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="62e6d-104">WM\_INITMENU message</span></span>

<span data-ttu-id="62e6d-105">當功能表即將變成作用中時傳送。</span><span class="sxs-lookup"><span data-stu-id="62e6d-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="62e6d-106">當使用者按一下功能表列上的專案，或按下功能表鍵時，就會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="62e6d-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="62e6d-107">這可讓應用程式在功能表顯示前修改功能表。</span><span class="sxs-lookup"><span data-stu-id="62e6d-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="62e6d-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="62e6d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="62e6d-109">參數</span><span class="sxs-lookup"><span data-stu-id="62e6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e6d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62e6d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62e6d-111">要初始化之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62e6d-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="62e6d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62e6d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62e6d-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="62e6d-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e6d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="62e6d-114">Return value</span></span>

<span data-ttu-id="62e6d-115">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="62e6d-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e6d-116">備註</span><span class="sxs-lookup"><span data-stu-id="62e6d-116">Remarks</span></span>

<span data-ttu-id="62e6d-117">只有在第一次存取功能表時，才會傳送 **wm \_ INITMENU** 訊息; 只會為每個存取產生一個 **wm \_ INITMENU** 訊息。</span><span class="sxs-lookup"><span data-stu-id="62e6d-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="62e6d-118">例如，在按住按鈕時將滑鼠移到數個功能表項目上時，不會產生新的訊息。</span><span class="sxs-lookup"><span data-stu-id="62e6d-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="62e6d-119">**WM \_INITMENU** 不會提供功能表項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="62e6d-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e6d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="62e6d-120">Requirements</span></span>



| <span data-ttu-id="62e6d-121">需求</span><span class="sxs-lookup"><span data-stu-id="62e6d-121">Requirement</span></span> | <span data-ttu-id="62e6d-122">值</span><span class="sxs-lookup"><span data-stu-id="62e6d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e6d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62e6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="62e6d-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62e6d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62e6d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62e6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="62e6d-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62e6d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62e6d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="62e6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e6d-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="62e6d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e6d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62e6d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="62e6d-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="62e6d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62e6d-131">**WM \_ INITMENUPOPUP**</span><span class="sxs-lookup"><span data-stu-id="62e6d-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="62e6d-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="62e6d-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62e6d-133">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="62e6d-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 


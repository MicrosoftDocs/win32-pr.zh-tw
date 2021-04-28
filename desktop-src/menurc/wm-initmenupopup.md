---
title: 'WM_INITMENUPOPUP 訊息 (Winuser .h) '
description: WM_INITMENUPOPUP 訊息-在下拉式功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092516"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="d7be5-105">WM \_ INITMENUPOPUP 訊息</span><span class="sxs-lookup"><span data-stu-id="d7be5-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="d7be5-106">當下拉功能表或子功能表即將變成作用中時傳送。</span><span class="sxs-lookup"><span data-stu-id="d7be5-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="d7be5-107">這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。</span><span class="sxs-lookup"><span data-stu-id="d7be5-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="d7be5-108">參數</span><span class="sxs-lookup"><span data-stu-id="d7be5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7be5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7be5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7be5-110">下拉式功能表或子功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7be5-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="d7be5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7be5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7be5-112">低序位字組會指定開啟下拉式功能表或子功能表之功能表項目的以零為起始的相對位置。</span><span class="sxs-lookup"><span data-stu-id="d7be5-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="d7be5-113">高序位單字指出下拉式功能表是否為 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="d7be5-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="d7be5-114">如果功能表是 [視窗] 功能表，此參數為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d7be5-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7be5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7be5-115">Return value</span></span>

<span data-ttu-id="d7be5-116">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d7be5-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7be5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7be5-117">Requirements</span></span>



| <span data-ttu-id="d7be5-118">需求</span><span class="sxs-lookup"><span data-stu-id="d7be5-118">Requirement</span></span> | <span data-ttu-id="d7be5-119">值</span><span class="sxs-lookup"><span data-stu-id="d7be5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7be5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7be5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7be5-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7be5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d7be5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7be5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7be5-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7be5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d7be5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d7be5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7be5-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d7be5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7be5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7be5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7be5-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="d7be5-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="d7be5-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7be5-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d7be5-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7be5-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d7be5-130">**WM \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="d7be5-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="d7be5-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="d7be5-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7be5-132">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="d7be5-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 


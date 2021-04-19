---
description: 應用程式會將 WM \_ MDIACTI加值稅E 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以指示用戶端視窗啟用不同的 MDI 子視窗。
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: 'WM_MDIACTI加值稅E 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988806"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="e84c8-103">WM \_ MDIACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="e84c8-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="e84c8-104">應用程式會將 **WM \_ MDIACTI加值稅E** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以指示用戶端視窗啟用不同的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="e84c8-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="e84c8-105">參數</span><span class="sxs-lookup"><span data-stu-id="e84c8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84c8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e84c8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84c8-107">要啟用之 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e84c8-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="e84c8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e84c8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84c8-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e84c8-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84c8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e84c8-110">Return value</span></span>

<span data-ttu-id="e84c8-111">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e84c8-111">Type: **LRESULT**</span></span>

<span data-ttu-id="e84c8-112">如果應用程式將此訊息傳送至 MDI 用戶端視窗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e84c8-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="e84c8-113">如果 MDI 子視窗處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="e84c8-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84c8-114">備註</span><span class="sxs-lookup"><span data-stu-id="e84c8-114">Remarks</span></span>

<span data-ttu-id="e84c8-115">當用戶端視窗處理此訊息時，它會將 **WM \_ MDIACTI加值稅E** 傳送至已停用的子視窗，以及要啟用的子視窗。</span><span class="sxs-lookup"><span data-stu-id="e84c8-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="e84c8-116">MDI 子視窗所收到的訊息參數如下所示：</span><span class="sxs-lookup"><span data-stu-id="e84c8-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="e84c8-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e84c8-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e84c8-118">要停用之 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e84c8-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="e84c8-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e84c8-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e84c8-120">要啟用之 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e84c8-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="e84c8-121">Mdi 子視窗會獨立于 MDI 框架視窗之外啟用。</span><span class="sxs-lookup"><span data-stu-id="e84c8-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="e84c8-122">當框架視窗變成作用中時，上次使用 **wm \_ MDIACTI加值稅E** 訊息啟動的子視窗會收到 [**WM \_ NCACTI加值稅E**](wm-ncactivate.md) 訊息，以繪製活動視窗框架和標題列，而子視窗則不會接收另一個 **WM \_ MDIACTI加值稅E** 訊息。</span><span class="sxs-lookup"><span data-stu-id="e84c8-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84c8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e84c8-123">Requirements</span></span>



| <span data-ttu-id="e84c8-124">需求</span><span class="sxs-lookup"><span data-stu-id="e84c8-124">Requirement</span></span> | <span data-ttu-id="e84c8-125">值</span><span class="sxs-lookup"><span data-stu-id="e84c8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e84c8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e84c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e84c8-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84c8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e84c8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e84c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e84c8-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84c8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e84c8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e84c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84c8-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e84c8-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84c8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e84c8-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="e84c8-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="e84c8-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e84c8-134">**WM \_ MDIGETACTIVE**</span><span class="sxs-lookup"><span data-stu-id="e84c8-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="e84c8-135">**WM \_ MDINEXT**</span><span class="sxs-lookup"><span data-stu-id="e84c8-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="e84c8-136">**WM \_ NCACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="e84c8-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="e84c8-137">**概念**</span><span class="sxs-lookup"><span data-stu-id="e84c8-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e84c8-138">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="e84c8-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





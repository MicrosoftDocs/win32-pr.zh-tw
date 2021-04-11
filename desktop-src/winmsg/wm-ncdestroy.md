---
description: 通知視窗，其非工作區已被終結。 DestroyWindow 函式會將 WM \_ NCDESTROY 訊息傳送至位於 wm 損毀訊息之後的視窗 \_ 。
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: 'WM_NCDESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944308"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="4c514-104">WM \_ NCDESTROY 訊息</span><span class="sxs-lookup"><span data-stu-id="4c514-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="4c514-105">通知視窗，其非工作區已被終結。</span><span class="sxs-lookup"><span data-stu-id="4c514-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="4c514-106">[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會將 **wm \_ NCDESTROY** 訊息傳送至位於 wm 損 [**\_ 毀**](wm-destroy.md)訊息之後的視窗。[**使用 \_ WM**](wm-destroy.md)終結來釋放與視窗相關聯的配置記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="4c514-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="4c514-107">當子視窗終結之後，會傳送 **WM \_ NCDESTROY** 訊息。</span><span class="sxs-lookup"><span data-stu-id="4c514-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="4c514-108">相反地，在子視窗終結之前，會先傳送 [**WM \_ 摧毀**](wm-destroy.md) 。</span><span class="sxs-lookup"><span data-stu-id="4c514-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="4c514-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="4c514-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="4c514-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c514-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c514-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c514-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c514-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4c514-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4c514-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c514-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c514-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4c514-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c514-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c514-115">Return value</span></span>

<span data-ttu-id="4c514-116">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4c514-116">Type: **LRESULT**</span></span>

<span data-ttu-id="4c514-117">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4c514-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c514-118">備註</span><span class="sxs-lookup"><span data-stu-id="4c514-118">Remarks</span></span>

<span data-ttu-id="4c514-119">此訊息會釋出任何內部配置給視窗的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4c514-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c514-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c514-120">Requirements</span></span>



| <span data-ttu-id="4c514-121">需求</span><span class="sxs-lookup"><span data-stu-id="4c514-121">Requirement</span></span> | <span data-ttu-id="4c514-122">值</span><span class="sxs-lookup"><span data-stu-id="4c514-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c514-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c514-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4c514-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c514-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4c514-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c514-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4c514-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c514-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c514-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4c514-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c514-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4c514-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c514-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c514-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c514-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="4c514-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c514-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="4c514-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="4c514-132">**WM 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="4c514-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="4c514-133">**WM \_ NCCREATE**</span><span class="sxs-lookup"><span data-stu-id="4c514-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="4c514-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="4c514-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4c514-135">Windows</span><span class="sxs-lookup"><span data-stu-id="4c514-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 

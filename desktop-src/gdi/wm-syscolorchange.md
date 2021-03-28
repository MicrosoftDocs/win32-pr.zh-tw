---
description: '\_當系統色彩設定有變更時，會將 WM SYSCOLORCHANGE 訊息傳送至所有最上層視窗。'
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: 'WM_SYSCOLORCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973768"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="e551d-103">WM \_ SYSCOLORCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e551d-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="e551d-104">當系統色彩設定有變更時，會將 **WM \_ SYSCOLORCHANGE** 訊息傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="e551d-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="e551d-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e551d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="e551d-106">參數</span><span class="sxs-lookup"><span data-stu-id="e551d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e551d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e551d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e551d-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e551d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e551d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e551d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e551d-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e551d-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e551d-111">備註</span><span class="sxs-lookup"><span data-stu-id="e551d-111">Remarks</span></span>

<span data-ttu-id="e551d-112">系統會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至受系統色彩變更影響的任何視窗。</span><span class="sxs-lookup"><span data-stu-id="e551d-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="e551d-113">具有使用現有系統色彩之筆刷的應用程式應該刪除這些筆刷，然後使用新的系統色彩重新建立這些筆刷。</span><span class="sxs-lookup"><span data-stu-id="e551d-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="e551d-114">使用通用控制項的最上層視窗必須將 **WM \_ SYSCOLORCHANGE** 訊息轉寄給控制項; 否則，將不會通知控制項色彩變更。</span><span class="sxs-lookup"><span data-stu-id="e551d-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="e551d-115">這可確保您的通用控制項所使用的色彩與其他使用者介面物件所使用的色彩一致。</span><span class="sxs-lookup"><span data-stu-id="e551d-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="e551d-116">例如，工具列控制項會使用「3D 物件」色彩來繪製其按鈕。</span><span class="sxs-lookup"><span data-stu-id="e551d-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="e551d-117">如果使用者變更3D 物件色彩，但卻未將 **WM \_ SYSCOLORCHANGE** 訊息轉寄至工具列，則工具列按鈕會維持其原始色彩，而系統中其他按鈕的色彩也會變更。</span><span class="sxs-lookup"><span data-stu-id="e551d-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e551d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e551d-118">Requirements</span></span>



| <span data-ttu-id="e551d-119">需求</span><span class="sxs-lookup"><span data-stu-id="e551d-119">Requirement</span></span> | <span data-ttu-id="e551d-120">值</span><span class="sxs-lookup"><span data-stu-id="e551d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e551d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e551d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e551d-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e551d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e551d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e551d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e551d-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e551d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e551d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e551d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e551d-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e551d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e551d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e551d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e551d-128">色彩總覽</span><span class="sxs-lookup"><span data-stu-id="e551d-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="e551d-129">色彩訊息</span><span class="sxs-lookup"><span data-stu-id="e551d-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="e551d-130">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="e551d-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 

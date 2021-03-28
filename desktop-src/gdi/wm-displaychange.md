---
description: '\_當顯示解析度變更時，會將 WM DISPLAYCHANGE 訊息傳送到所有視窗。'
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: 'WM_DISPLAYCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192386"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="36a36-103">WM \_ DISPLAYCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="36a36-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="36a36-104">當顯示解析度變更時，會將 **WM \_ DISPLAYCHANGE** 訊息傳送到所有視窗。</span><span class="sxs-lookup"><span data-stu-id="36a36-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="36a36-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="36a36-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="36a36-106">參數</span><span class="sxs-lookup"><span data-stu-id="36a36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a36-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36a36-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36a36-108">顯示的新影像深度（以位/圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="36a36-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="36a36-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36a36-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36a36-110">低序位字組指定螢幕的水準解析度。</span><span class="sxs-lookup"><span data-stu-id="36a36-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="36a36-111">高序位字組指定螢幕的垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="36a36-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36a36-112">備註</span><span class="sxs-lookup"><span data-stu-id="36a36-112">Remarks</span></span>

<span data-ttu-id="36a36-113">此訊息只會傳送至最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="36a36-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="36a36-114">所有其他視窗則會公佈。</span><span class="sxs-lookup"><span data-stu-id="36a36-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="36a36-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="36a36-115">Requirements</span></span>



| <span data-ttu-id="36a36-116">需求</span><span class="sxs-lookup"><span data-stu-id="36a36-116">Requirement</span></span> | <span data-ttu-id="36a36-117">值</span><span class="sxs-lookup"><span data-stu-id="36a36-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a36-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36a36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36a36-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36a36-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="36a36-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36a36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36a36-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36a36-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36a36-122">標頭</span><span class="sxs-lookup"><span data-stu-id="36a36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a36-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36a36-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a36-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36a36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a36-125">繪製和繪製總覽</span><span class="sxs-lookup"><span data-stu-id="36a36-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="36a36-126">繪製和繪製訊息</span><span class="sxs-lookup"><span data-stu-id="36a36-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="36a36-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36a36-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="36a36-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36a36-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 

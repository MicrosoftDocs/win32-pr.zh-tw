---
title: 'WM_HSCROLLCLIPBOARD 訊息 (Winuser .h) '
description: 由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466365"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="46029-104">WM \_ HSCROLLCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="46029-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="46029-105">由剪貼簿檢視器視窗傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="46029-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="46029-106">當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而且在剪貼簿檢視器的水準捲軸中發生事件時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="46029-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="46029-107">擁有者應該滾動剪貼簿影像，並更新捲軸值。</span><span class="sxs-lookup"><span data-stu-id="46029-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="46029-108">參數</span><span class="sxs-lookup"><span data-stu-id="46029-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46029-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46029-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46029-110">剪貼簿檢視器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="46029-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="46029-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46029-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46029-112">*LParam* 的低序位字指定捲軸事件。</span><span class="sxs-lookup"><span data-stu-id="46029-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="46029-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="46029-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="46029-114">如果 *lParam* 的低序位字是 **SB \_ THUMBPOSITION**，則 *lParam* 的高序位字組會指定捲動方塊的目前位置; 否則，就不會使用高序位字。</span><span class="sxs-lookup"><span data-stu-id="46029-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="46029-115">值</span><span class="sxs-lookup"><span data-stu-id="46029-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="46029-116">意義</span><span class="sxs-lookup"><span data-stu-id="46029-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="46029-117"><dt>**SB \_ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="46029-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="46029-118">結束捲軸。</span><span class="sxs-lookup"><span data-stu-id="46029-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="46029-119"><dt>**SB \_左方**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="46029-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="46029-120">滾動至左上方。</span><span class="sxs-lookup"><span data-stu-id="46029-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="46029-121"><dt>**SB \_右**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="46029-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="46029-122">向右下方。</span><span class="sxs-lookup"><span data-stu-id="46029-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="46029-123"><dt>**SB \_LINELEFT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46029-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="46029-124">向左滾動一個單位。</span><span class="sxs-lookup"><span data-stu-id="46029-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="46029-125"><dt>**SB \_LINERIGHT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="46029-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="46029-126">向右滾動一個單位。</span><span class="sxs-lookup"><span data-stu-id="46029-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="46029-127"><dt>**SB \_PAGELEFT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="46029-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="46029-128">以視窗的寬度向左滾動。</span><span class="sxs-lookup"><span data-stu-id="46029-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="46029-129"><dt>**SB \_PAGERIGHT**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="46029-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="46029-130">向右滾動視窗的寬度。</span><span class="sxs-lookup"><span data-stu-id="46029-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="46029-131"><dt>**SB \_THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="46029-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="46029-132">滾動至絕對位置。</span><span class="sxs-lookup"><span data-stu-id="46029-132">Scroll to absolute position.</span></span> <span data-ttu-id="46029-133">目前的位置是由高序位字指定。</span><span class="sxs-lookup"><span data-stu-id="46029-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46029-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="46029-134">Return value</span></span>

<span data-ttu-id="46029-135">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="46029-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="46029-136">備註</span><span class="sxs-lookup"><span data-stu-id="46029-136">Remarks</span></span>

<span data-ttu-id="46029-137">剪貼簿擁有者可以使用 [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) 函式，在 [剪貼簿檢視器] 視窗中滾動影像，並讓適當的區域失效。</span><span class="sxs-lookup"><span data-stu-id="46029-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="46029-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="46029-138">Requirements</span></span>



| <span data-ttu-id="46029-139">需求</span><span class="sxs-lookup"><span data-stu-id="46029-139">Requirement</span></span> | <span data-ttu-id="46029-140">值</span><span class="sxs-lookup"><span data-stu-id="46029-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46029-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46029-141">Minimum supported client</span></span><br/> | <span data-ttu-id="46029-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46029-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46029-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46029-143">Minimum supported server</span></span><br/> | <span data-ttu-id="46029-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46029-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46029-145">標頭</span><span class="sxs-lookup"><span data-stu-id="46029-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="46029-146"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="46029-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46029-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46029-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="46029-148">**參考**</span><span class="sxs-lookup"><span data-stu-id="46029-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="46029-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46029-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="46029-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46029-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="46029-151">**概念**</span><span class="sxs-lookup"><span data-stu-id="46029-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46029-152">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="46029-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="46029-153">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="46029-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="46029-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="46029-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


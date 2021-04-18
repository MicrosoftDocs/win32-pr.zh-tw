---
title: 'WM_VSCROLLCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，並在剪貼簿檢視器的垂直捲動條中發生事件時，將剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465613"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="31b9c-104">WM \_ VSCROLLCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="31b9c-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="31b9c-105">當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，並在剪貼簿檢視器的垂直捲動條中發生事件時，將剪貼簿檢視器視窗傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="31b9c-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="31b9c-106">擁有者應該滾動剪貼簿影像，並更新捲軸值。</span><span class="sxs-lookup"><span data-stu-id="31b9c-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="31b9c-107">參數</span><span class="sxs-lookup"><span data-stu-id="31b9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b9c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31b9c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b9c-109">剪貼簿檢視器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="31b9c-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="31b9c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31b9c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b9c-111">*LParam* 的低序位字指定捲軸事件。</span><span class="sxs-lookup"><span data-stu-id="31b9c-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="31b9c-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="31b9c-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="31b9c-113">值</span><span class="sxs-lookup"><span data-stu-id="31b9c-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="31b9c-114">意義</span><span class="sxs-lookup"><span data-stu-id="31b9c-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="31b9c-115"><dt>**SB \_底部**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="31b9c-116">向右下方。</span><span class="sxs-lookup"><span data-stu-id="31b9c-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="31b9c-117"><dt>**SB \_ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="31b9c-118">結束捲軸。</span><span class="sxs-lookup"><span data-stu-id="31b9c-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="31b9c-119"><dt>**SB \_LINEDOWN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="31b9c-120">向下移動一行。</span><span class="sxs-lookup"><span data-stu-id="31b9c-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="31b9c-121"><dt>**SB \_系列系列**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="31b9c-122">向上移動一行。</span><span class="sxs-lookup"><span data-stu-id="31b9c-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="31b9c-123"><dt>**SB \_PAGEDOWN**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="31b9c-124">向下移動一頁。</span><span class="sxs-lookup"><span data-stu-id="31b9c-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="31b9c-125"><dt>**SB \_PAGEUP**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="31b9c-126">向上滾動一頁。</span><span class="sxs-lookup"><span data-stu-id="31b9c-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="31b9c-127"><dt>**SB \_THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="31b9c-128">滾動至絕對位置。</span><span class="sxs-lookup"><span data-stu-id="31b9c-128">Scroll to absolute position.</span></span> <span data-ttu-id="31b9c-129">目前的位置是由高序位字指定。</span><span class="sxs-lookup"><span data-stu-id="31b9c-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="31b9c-130"><dt>**SB \_前**</dt> <dt>6</dt>名</span><span class="sxs-lookup"><span data-stu-id="31b9c-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="31b9c-131">滾動至左上方。</span><span class="sxs-lookup"><span data-stu-id="31b9c-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="31b9c-132">如果 *lParam* 的低序位字是 **SB \_ THUMBPOSITION**，則 *lParam* 的高序位字組會指定捲動方塊的目前位置; 否則，將不會使用 *lParam* 的高序位字。</span><span class="sxs-lookup"><span data-stu-id="31b9c-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b9c-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="31b9c-133">Return value</span></span>

<span data-ttu-id="31b9c-134">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="31b9c-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b9c-135">備註</span><span class="sxs-lookup"><span data-stu-id="31b9c-135">Remarks</span></span>

<span data-ttu-id="31b9c-136">剪貼簿擁有者可以使用 [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) 函式，在 [剪貼簿檢視器] 視窗中滾動影像，並讓適當的區域失效。</span><span class="sxs-lookup"><span data-stu-id="31b9c-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b9c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="31b9c-137">Requirements</span></span>



| <span data-ttu-id="31b9c-138">需求</span><span class="sxs-lookup"><span data-stu-id="31b9c-138">Requirement</span></span> | <span data-ttu-id="31b9c-139">值</span><span class="sxs-lookup"><span data-stu-id="31b9c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b9c-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31b9c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="31b9c-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31b9c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="31b9c-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31b9c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="31b9c-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31b9c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31b9c-144">標頭</span><span class="sxs-lookup"><span data-stu-id="31b9c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b9c-145"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="31b9c-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b9c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31b9c-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="31b9c-147">**參考**</span><span class="sxs-lookup"><span data-stu-id="31b9c-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="31b9c-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31b9c-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="31b9c-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31b9c-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="31b9c-150">**概念**</span><span class="sxs-lookup"><span data-stu-id="31b9c-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="31b9c-151">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="31b9c-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="31b9c-152">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="31b9c-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="31b9c-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="31b9c-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


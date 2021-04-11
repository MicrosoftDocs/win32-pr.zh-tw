---
description: 傳送至使用者正在調整大小的視窗。 藉由處理此訊息，應用程式可以監視拖曳矩形的大小和位置，並視需要變更其大小或位置。
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: 'WM_SIZING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693063"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="e1a1b-104">WM 重設 \_ 大小訊息</span><span class="sxs-lookup"><span data-stu-id="e1a1b-104">WM\_SIZING message</span></span>

<span data-ttu-id="e1a1b-105">傳送至使用者正在調整大小的視窗。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="e1a1b-106">藉由處理此訊息，應用程式可以監視拖曳矩形的大小和位置，並視需要變更其大小或位置。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="e1a1b-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="e1a1b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1a1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1a1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1a1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a1b-110">要調整大小之視窗的邊緣。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="e1a1b-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e1a1b-112">值</span><span class="sxs-lookup"><span data-stu-id="e1a1b-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e1a1b-113">意義</span><span class="sxs-lookup"><span data-stu-id="e1a1b-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="e1a1b-114"><dt>**WMSZ \_底部**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="e1a1b-115">下邊緣</span><span class="sxs-lookup"><span data-stu-id="e1a1b-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="e1a1b-116"><dt>**WMSZ \_BOTTOMLEFT**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="e1a1b-117">左下角</span><span class="sxs-lookup"><span data-stu-id="e1a1b-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="e1a1b-118"><dt>**WMSZ \_BOTTOMRIGHT**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="e1a1b-119">右下角</span><span class="sxs-lookup"><span data-stu-id="e1a1b-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="e1a1b-120"><dt>**WMSZ \_左方**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="e1a1b-121">左邊緣</span><span class="sxs-lookup"><span data-stu-id="e1a1b-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="e1a1b-122"><dt>**WMSZ \_右**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="e1a1b-123">右邊緣</span><span class="sxs-lookup"><span data-stu-id="e1a1b-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="e1a1b-124"><dt>**WMSZ \_前**</dt> <dt>3</dt>名</span><span class="sxs-lookup"><span data-stu-id="e1a1b-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="e1a1b-125">上邊緣</span><span class="sxs-lookup"><span data-stu-id="e1a1b-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="e1a1b-126"><dt>**WMSZ \_下拉式功能表**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="e1a1b-127">左上角</span><span class="sxs-lookup"><span data-stu-id="e1a1b-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="e1a1b-128"><dt>**WMSZ \_右上**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="e1a1b-129">右上角</span><span class="sxs-lookup"><span data-stu-id="e1a1b-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="e1a1b-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1a1b-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a1b-131">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含拖曳矩形的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="e1a1b-132">若要變更拖曳矩形的大小或位置，應用程式必須變更此結構的成員。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1a1b-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1a1b-133">Return value</span></span>

<span data-ttu-id="e1a1b-134">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-134">Type: **LRESULT**</span></span>

<span data-ttu-id="e1a1b-135">如果應用程式處理此訊息，則應該傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e1a1b-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1a1b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1a1b-136">Requirements</span></span>



| <span data-ttu-id="e1a1b-137">需求</span><span class="sxs-lookup"><span data-stu-id="e1a1b-137">Requirement</span></span> | <span data-ttu-id="e1a1b-138">值</span><span class="sxs-lookup"><span data-stu-id="e1a1b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a1b-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1a1b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e1a1b-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1a1b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e1a1b-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1a1b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e1a1b-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1a1b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1a1b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="e1a1b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1a1b-144"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e1a1b-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1a1b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1a1b-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1a1b-146">**參考**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1a1b-147">**WM \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="e1a1b-148">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="e1a1b-149">**概念**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1a1b-150">Windows</span><span class="sxs-lookup"><span data-stu-id="e1a1b-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="e1a1b-151">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="e1a1b-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e1a1b-152">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e1a1b-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 

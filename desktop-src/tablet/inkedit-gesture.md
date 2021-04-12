---
description: 當應用程式手勢被辨識時發生。
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: 'InkEdit 的軌跡事件 (筆跡) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193338"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="77030-103">InkEdit 手勢事件</span><span class="sxs-lookup"><span data-stu-id="77030-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="77030-104">當應用程式手勢被辨識時發生。</span><span class="sxs-lookup"><span data-stu-id="77030-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="77030-105">語法</span><span class="sxs-lookup"><span data-stu-id="77030-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="77030-106">參數</span><span class="sxs-lookup"><span data-stu-id="77030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77030-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77030-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77030-108">用來建立此手勢的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件。</span><span class="sxs-lookup"><span data-stu-id="77030-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="77030-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77030-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77030-110">[InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，其中包含組成此手勢的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。</span><span class="sxs-lookup"><span data-stu-id="77030-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="77030-111">*手勢* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77030-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77030-112">[**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的陣列，以信賴度為限。</span><span class="sxs-lookup"><span data-stu-id="77030-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="77030-113">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="77030-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="77030-114">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="77030-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77030-115">是否應該取消組成此軌跡的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合，以免清除筆墨並引發 [**筆劃**](inkedit-stroke.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="77030-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77030-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="77030-116">Return value</span></span>

<span data-ttu-id="77030-117">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="77030-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77030-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="77030-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77030-119">備註</span><span class="sxs-lookup"><span data-stu-id="77030-119">Remarks</span></span>

<span data-ttu-id="77030-120">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="77030-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="77030-121">**\_ IInkEditEvents** 介面會以 DISPID IeeGesture 的識別碼來實作為 IDispatch 介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="77030-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="77030-122">只有在最後一次呼叫辨識方法或上次引發 [**辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)超時時，才會引發 **手勢** 事件，因為 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)是第一個 **IInkStrokeDisp** 物件。</span><span class="sxs-lookup"><span data-stu-id="77030-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="77030-123">如果已取消 **手勢** 事件，則會針對引發 **手勢** 事件的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合引發 [**筆劃**](inkedit-stroke.md)事件。</span><span class="sxs-lookup"><span data-stu-id="77030-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="77030-124">若要進行此事件， [InkEdit](inkedit-control-reference.md) 控制項必須訂閱一組應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="77030-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="77030-125">若要在一組手勢中設定 InkEdit 控制項的興趣，請呼叫 [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="77030-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="77030-126">如需應用程式手勢的清單，請參閱 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="77030-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="77030-127">[InkEdit](inkedit-control-reference.md)控制項無法辨識多個筆劃手勢。</span><span class="sxs-lookup"><span data-stu-id="77030-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="77030-128">[InkEdit](inkedit-control-reference.md)控制項會訂閱下列手勢。</span><span class="sxs-lookup"><span data-stu-id="77030-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="77030-129">手勢</span><span class="sxs-lookup"><span data-stu-id="77030-129">Gesture</span></span>                              | <span data-ttu-id="77030-130">動作</span><span class="sxs-lookup"><span data-stu-id="77030-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="77030-131">向左、向下、向左</span><span class="sxs-lookup"><span data-stu-id="77030-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="77030-132">Enter</span><span class="sxs-lookup"><span data-stu-id="77030-132">Enter</span></span><br/>     |
| <span data-ttu-id="77030-133">Right</span><span class="sxs-lookup"><span data-stu-id="77030-133">Right</span></span><br/>                     | <span data-ttu-id="77030-134">Space</span><span class="sxs-lookup"><span data-stu-id="77030-134">Space</span></span><br/>     |
| <span data-ttu-id="77030-135">Left</span><span class="sxs-lookup"><span data-stu-id="77030-135">Left</span></span><br/>                      | <span data-ttu-id="77030-136">退格鍵</span><span class="sxs-lookup"><span data-stu-id="77030-136">Backspace</span></span><br/> |
| <span data-ttu-id="77030-137">右上角、右上角</span><span class="sxs-lookup"><span data-stu-id="77030-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="77030-138">索引標籤</span><span class="sxs-lookup"><span data-stu-id="77030-138">Tab</span></span><br/>       |



 

<span data-ttu-id="77030-139">若要改變手勢的預設動作：</span><span class="sxs-lookup"><span data-stu-id="77030-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="77030-140">加入 **筆勢** 和 [**筆觸**](inkedit-stroke.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="77030-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="77030-141">**在軌跡事件處理** 程式中，取消筆勢的 **手勢** 事件，然後執行筆勢的替代動作。</span><span class="sxs-lookup"><span data-stu-id="77030-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="77030-142">在 [[**筆劃**](inkedit-stroke.md)事件處理常式] 中，取消引發已取消的 **手勢** 事件之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 **筆觸** 事件。</span><span class="sxs-lookup"><span data-stu-id="77030-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="77030-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="77030-143">Requirements</span></span>



| <span data-ttu-id="77030-144">需求</span><span class="sxs-lookup"><span data-stu-id="77030-144">Requirement</span></span> | <span data-ttu-id="77030-145">值</span><span class="sxs-lookup"><span data-stu-id="77030-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77030-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77030-146">Minimum supported client</span></span><br/> | <span data-ttu-id="77030-147">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77030-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="77030-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77030-148">Minimum supported server</span></span><br/> | <span data-ttu-id="77030-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="77030-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="77030-150">標頭</span><span class="sxs-lookup"><span data-stu-id="77030-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="77030-151"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="77030-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="77030-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="77030-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="77030-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77030-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="77030-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77030-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77030-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="77030-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="77030-156">**InkApplicationGesture 列舉**</span><span class="sxs-lookup"><span data-stu-id="77030-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="77030-157">[**SetGestureStatus 方法 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="77030-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="77030-158">**RecoTimeout 屬性**</span><span class="sxs-lookup"><span data-stu-id="77030-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="77030-159">[**筆觸事件 \[ InkEdit 控制項\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="77030-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="77030-160">使用手勢</span><span class="sxs-lookup"><span data-stu-id="77030-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 


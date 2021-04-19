---
description: 在識別應用程式特定的手勢時發生。
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: 'InkCollector 的軌跡事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb68add1a3fbba5781624f1df98c3a637745b95a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972206"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="32548-103">InkCollector 手勢事件</span><span class="sxs-lookup"><span data-stu-id="32548-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="32548-104">在識別應用程式特定的手勢時發生。</span><span class="sxs-lookup"><span data-stu-id="32548-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="32548-105">語法</span><span class="sxs-lookup"><span data-stu-id="32548-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="32548-106">參數</span><span class="sxs-lookup"><span data-stu-id="32548-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32548-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32548-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32548-108">產生 **手勢** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="32548-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="32548-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32548-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32548-110">辨識器傳回做為手勢的 [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="32548-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="32548-111">*手勢* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32548-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32548-112">從辨識器 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) 物件的陣列，以信賴度為限。</span><span class="sxs-lookup"><span data-stu-id="32548-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="32548-113">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="32548-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="32548-114">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="32548-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32548-115">**變異 \_** 如果應該取消此手勢，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="32548-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32548-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="32548-116">Return value</span></span>

<span data-ttu-id="32548-117">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="32548-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32548-118">備註</span><span class="sxs-lookup"><span data-stu-id="32548-118">Remarks</span></span>

<span data-ttu-id="32548-119">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICEGesture 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="32548-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="32548-120">當 [ [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) ] 屬性設定為 [ [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)] 時，當使用者加入手勢以及 **手勢** 事件發生的時間，是您無法以程式設計方式改變的固定值。</span><span class="sxs-lookup"><span data-stu-id="32548-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="32548-121">在 **InkAndGesture** 模式中，手勢辨識的速度較快。</span><span class="sxs-lookup"><span data-stu-id="32548-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="32548-122">若要在 [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) 模式中防止筆墨收集：</span><span class="sxs-lookup"><span data-stu-id="32548-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="32548-123">將 [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) 設定為 [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)。</span><span class="sxs-lookup"><span data-stu-id="32548-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="32548-124">刪除 [**筆劃**](inkcollector-stroke.md) 事件中的筆劃。</span><span class="sxs-lookup"><span data-stu-id="32548-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="32548-125">處理 **手勢** 事件中的手勢。</span><span class="sxs-lookup"><span data-stu-id="32548-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="32548-126">若要在 gesturing 時防止筆墨流程，請將 [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="32548-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="32548-127">除了插入筆墨時，會在選取或清除模式時引發 **手勢** 事件。</span><span class="sxs-lookup"><span data-stu-id="32548-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="32548-128">您必須負責追蹤編輯模式，並且應該在解讀事件之前留意模式。</span><span class="sxs-lookup"><span data-stu-id="32548-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="32548-129">若要辨識筆勢，您必須使用可收集筆跡的物件或控制項。</span><span class="sxs-lookup"><span data-stu-id="32548-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="32548-130">應用程式手勢會定義為您的應用程式中支援的手勢。</span><span class="sxs-lookup"><span data-stu-id="32548-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="32548-131">若要進行此事件，物件或控制項必須對一組應用程式手勢感興趣。</span><span class="sxs-lookup"><span data-stu-id="32548-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="32548-132">若要設定一組手勢中感興趣的物件或控制項，請呼叫物件或控制項的 [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="32548-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="32548-133">如需特定應用程式手勢的清單，請參閱 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="32548-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="32548-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="32548-134">Requirements</span></span>



| <span data-ttu-id="32548-135">需求</span><span class="sxs-lookup"><span data-stu-id="32548-135">Requirement</span></span> | <span data-ttu-id="32548-136">值</span><span class="sxs-lookup"><span data-stu-id="32548-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32548-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32548-137">Minimum supported client</span></span><br/> | <span data-ttu-id="32548-138">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32548-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="32548-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32548-139">Minimum supported server</span></span><br/> | <span data-ttu-id="32548-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="32548-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="32548-141">標頭</span><span class="sxs-lookup"><span data-stu-id="32548-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="32548-142"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="32548-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="32548-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="32548-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="32548-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32548-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="32548-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32548-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32548-146">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="32548-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="32548-147">**InkApplicationGesture 列舉**</span><span class="sxs-lookup"><span data-stu-id="32548-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="32548-148">**SetGestureStatus 方法**</span><span class="sxs-lookup"><span data-stu-id="32548-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="32548-149">使用手勢</span><span class="sxs-lookup"><span data-stu-id="32548-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 


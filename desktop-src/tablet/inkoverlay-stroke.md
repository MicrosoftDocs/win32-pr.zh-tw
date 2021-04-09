---
description: 當使用者在任何平板電腦上繪製新筆劃時發生。
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: 'InkOverlay：筆觸事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694995"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="6ad41-103">InkOverlay。筆觸事件</span><span class="sxs-lookup"><span data-stu-id="6ad41-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="6ad41-104">當使用者在任何平板電腦上繪製新筆劃時發生。</span><span class="sxs-lookup"><span data-stu-id="6ad41-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad41-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ad41-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6ad41-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ad41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad41-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ad41-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad41-108">產生 [**筆劃**](inkcollector-stroke.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="6ad41-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ad41-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad41-110">收集的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="6ad41-111">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6ad41-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad41-112">指定是否應該取消事件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="6ad41-113">若 **為 TRUE**，則表示筆劃的集合已取消。</span><span class="sxs-lookup"><span data-stu-id="6ad41-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad41-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ad41-114">Return value</span></span>

<span data-ttu-id="6ad41-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6ad41-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad41-116">備註</span><span class="sxs-lookup"><span data-stu-id="6ad41-116">Remarks</span></span>

<span data-ttu-id="6ad41-117">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICEStroke 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="6ad41-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="6ad41-118">在 [選取] 或 [清除] 模式中（而不只是在插入筆墨時），就會引發 [**筆劃**](inkcollector-stroke.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="6ad41-119">這需要您監視您負責設定) 的編輯模式 (，並在解讀事件之前感知模式。</span><span class="sxs-lookup"><span data-stu-id="6ad41-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="6ad41-120">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="6ad41-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="6ad41-121">當使用者完成繪製筆劃時，不會在將筆劃加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合時引發 [**筆劃**](inkcollector-stroke.md)事件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="6ad41-122">當使用者第一次開始繪製筆劃時，會立即將其新增至 InkStrokes 集合;不過，在筆劃完成之前，不會引發 **筆劃** 事件。</span><span class="sxs-lookup"><span data-stu-id="6ad41-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="6ad41-123">因此，筆劃可以存在於 **筆劃** 事件處理常式未看到的 InkStrokes 集合中。</span><span class="sxs-lookup"><span data-stu-id="6ad41-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ad41-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ad41-124">Requirements</span></span>



| <span data-ttu-id="6ad41-125">需求</span><span class="sxs-lookup"><span data-stu-id="6ad41-125">Requirement</span></span> | <span data-ttu-id="6ad41-126">值</span><span class="sxs-lookup"><span data-stu-id="6ad41-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad41-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ad41-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad41-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ad41-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6ad41-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ad41-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad41-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="6ad41-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6ad41-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6ad41-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad41-132"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6ad41-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6ad41-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ad41-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ad41-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad41-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6ad41-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ad41-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad41-136">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="6ad41-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="6ad41-137">[**StrokesAdded 事件 \[ InkStrokes 集合\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="6ad41-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="6ad41-138">[**StrokesDeleted 事件 \[ InkOverlay 類別\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="6ad41-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="6ad41-139">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="6ad41-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="6ad41-140">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="6ad41-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


---
description: 當使用者在任何平板電腦上繪製新筆劃時發生。
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: 'InkCollector： Stroke 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e75ee7f3e8129fdab52e62178fe4b8a322807fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998446"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="30dca-103">InkCollector。筆觸事件</span><span class="sxs-lookup"><span data-stu-id="30dca-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="30dca-104">當使用者在任何平板電腦上繪製新筆劃時發生。</span><span class="sxs-lookup"><span data-stu-id="30dca-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="30dca-105">語法</span><span class="sxs-lookup"><span data-stu-id="30dca-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="30dca-106">參數</span><span class="sxs-lookup"><span data-stu-id="30dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30dca-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30dca-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dca-108">產生 **筆劃** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="30dca-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="30dca-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30dca-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dca-110">收集的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。</span><span class="sxs-lookup"><span data-stu-id="30dca-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="30dca-111">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="30dca-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30dca-112">**變異 \_TRUE** 表示取消事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="30dca-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30dca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="30dca-113">Return value</span></span>

<span data-ttu-id="30dca-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="30dca-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30dca-115">備註</span><span class="sxs-lookup"><span data-stu-id="30dca-115">Remarks</span></span>

<span data-ttu-id="30dca-116">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICEStroke 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="30dca-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="30dca-117">在 [選取] 或 [清除] 模式中（而不只是在插入筆墨時），就會引發 **筆劃** 事件。</span><span class="sxs-lookup"><span data-stu-id="30dca-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="30dca-118">這需要您監視您負責設定) 的編輯模式 (，並在解讀事件之前感知模式。</span><span class="sxs-lookup"><span data-stu-id="30dca-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="30dca-119">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="30dca-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="30dca-120">當使用者完成繪製筆劃時，不會在將筆劃加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合時引發 **筆劃** 事件。</span><span class="sxs-lookup"><span data-stu-id="30dca-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="30dca-121">當使用者第一次開始繪製筆劃時，會立即將其新增至 InkStrokes 集合;不過，在筆劃完成之前，不會引發 **筆劃** 事件。</span><span class="sxs-lookup"><span data-stu-id="30dca-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="30dca-122">因此，筆劃可以存在於 **筆劃** 事件處理常式未看到的 InkStrokes 集合中。</span><span class="sxs-lookup"><span data-stu-id="30dca-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30dca-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="30dca-123">Requirements</span></span>



| <span data-ttu-id="30dca-124">需求</span><span class="sxs-lookup"><span data-stu-id="30dca-124">Requirement</span></span> | <span data-ttu-id="30dca-125">值</span><span class="sxs-lookup"><span data-stu-id="30dca-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30dca-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30dca-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30dca-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30dca-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="30dca-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30dca-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30dca-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="30dca-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="30dca-130">標頭</span><span class="sxs-lookup"><span data-stu-id="30dca-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="30dca-131"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="30dca-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30dca-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="30dca-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="30dca-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30dca-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="30dca-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30dca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dca-135">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="30dca-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="30dca-136">[**StrokesAdded 事件 \[ InkStrokes 集合\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="30dca-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="30dca-137">[**StrokesDeleted 事件 \[ InkOverlay 類別\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="30dca-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="30dca-138">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="30dca-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="30dca-139">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="30dca-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


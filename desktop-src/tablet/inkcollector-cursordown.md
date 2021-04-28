---
description: InkCollector. CursorDown 事件-發生于游標提示連線到數位化的平板電腦介面時。
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: 'InkCollector. CursorDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110296"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="de165-103">InkCollector. CursorDown 事件</span><span class="sxs-lookup"><span data-stu-id="de165-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="de165-104">當游標提示接觸到數位化的 tablet 介面時發生。</span><span class="sxs-lookup"><span data-stu-id="de165-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="de165-105">語法</span><span class="sxs-lookup"><span data-stu-id="de165-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="de165-106">參數</span><span class="sxs-lookup"><span data-stu-id="de165-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de165-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de165-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de165-108">產生 **CursorDown** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="de165-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="de165-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de165-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de165-110">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件造成引發 **CursorDown** 事件時所啟動的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。</span><span class="sxs-lookup"><span data-stu-id="de165-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de165-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de165-111">Return value</span></span>

<span data-ttu-id="de165-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="de165-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de165-113">備註</span><span class="sxs-lookup"><span data-stu-id="de165-113">Remarks</span></span>

<span data-ttu-id="de165-114">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 IInkPictureEvents 中定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de165-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="de165-115">\_IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 介面會以 DISPID ICECursorDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de165-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="de165-116">請小心使用此事件，因為在事件處理常式中執行太多程式碼時，可能會對筆墨效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="de165-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="de165-117">若要改善即時筆墨效能，請在 [**MouseDown**](inkcollector-mousedown.md) 和 [**MouseUp**](inkcollector-mouseup.md) 事件處理常式中隱藏或顯示滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="de165-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="de165-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="de165-118">Requirements</span></span>



| <span data-ttu-id="de165-119">需求</span><span class="sxs-lookup"><span data-stu-id="de165-119">Requirement</span></span> | <span data-ttu-id="de165-120">值</span><span class="sxs-lookup"><span data-stu-id="de165-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de165-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de165-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de165-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de165-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="de165-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de165-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de165-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="de165-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="de165-125">標頭</span><span class="sxs-lookup"><span data-stu-id="de165-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="de165-126"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="de165-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="de165-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="de165-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="de165-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de165-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="de165-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de165-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de165-130">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="de165-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="de165-131">**CursorButtonDown 事件**</span><span class="sxs-lookup"><span data-stu-id="de165-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="de165-132">**CursorButtonUp 事件**</span><span class="sxs-lookup"><span data-stu-id="de165-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="de165-133">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="de165-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="de165-134">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="de165-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


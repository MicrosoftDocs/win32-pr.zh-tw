---
description: InkCollector：當滑鼠指標移到 InkCollector 或 InkOverlay 物件上方時，就會發生此事件。
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: 'InkCollector： MouseMove 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110156"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="72732-103">InkCollector MouseMove 事件</span><span class="sxs-lookup"><span data-stu-id="72732-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="72732-104">發生于滑鼠指標移至 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上方時。</span><span class="sxs-lookup"><span data-stu-id="72732-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="72732-105">語法</span><span class="sxs-lookup"><span data-stu-id="72732-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="72732-106">參數</span><span class="sxs-lookup"><span data-stu-id="72732-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72732-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72732-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72732-108">已按下的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="72732-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="72732-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72732-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72732-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="72732-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="72732-111">*pX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72732-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72732-112">滑鼠點擊的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="72732-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="72732-113">*.py* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72732-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72732-114">滑鼠點擊的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="72732-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="72732-115">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="72732-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72732-116">**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="72732-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72732-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="72732-117">Return value</span></span>

<span data-ttu-id="72732-118">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="72732-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72732-119">備註</span><span class="sxs-lookup"><span data-stu-id="72732-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72732-120">[ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="72732-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="72732-121">這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。</span><span class="sxs-lookup"><span data-stu-id="72732-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="72732-122">某些控制項依賴 [**MouseDown**](inkcollector-mousedown.md)、 **MouseMove** 和 [**MouseUp**](inkcollector-mouseup.md) 事件之間的特定關聯性。</span><span class="sxs-lookup"><span data-stu-id="72732-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="72732-123">取消其中某些事件可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="72732-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="72732-124">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseMove 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="72732-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="72732-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="72732-125">Requirements</span></span>



| <span data-ttu-id="72732-126">需求</span><span class="sxs-lookup"><span data-stu-id="72732-126">Requirement</span></span> | <span data-ttu-id="72732-127">值</span><span class="sxs-lookup"><span data-stu-id="72732-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72732-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72732-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72732-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72732-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="72732-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72732-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72732-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="72732-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="72732-132">標頭</span><span class="sxs-lookup"><span data-stu-id="72732-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="72732-133"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="72732-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="72732-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="72732-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="72732-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72732-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="72732-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72732-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72732-137">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="72732-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="72732-138">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="72732-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="72732-139">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="72732-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 





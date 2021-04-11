---
description: 發生于 InkCollector 或 InkOverlay 物件具有焦點時，滑鼠滾輪移動時。
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: '滑鼠滾輪事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852176"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="33112-103">滑鼠滾輪事件</span><span class="sxs-lookup"><span data-stu-id="33112-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="33112-104">發生于 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件具有焦點時，滑鼠滾輪移動時。</span><span class="sxs-lookup"><span data-stu-id="33112-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="33112-105">語法</span><span class="sxs-lookup"><span data-stu-id="33112-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="33112-106">參數</span><span class="sxs-lookup"><span data-stu-id="33112-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33112-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33112-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-108">已按下的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="33112-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="33112-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33112-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="33112-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="33112-111">*差異* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33112-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-112">滑鼠滾輪旋轉的刻度數目的帶正負號計數。</span><span class="sxs-lookup"><span data-stu-id="33112-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="33112-113">一個刻度是一個滑鼠滾輪的刻痕。</span><span class="sxs-lookup"><span data-stu-id="33112-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="33112-114">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="33112-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-115">滑鼠點擊的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="33112-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="33112-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33112-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-117">滑鼠點擊的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="33112-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="33112-118">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="33112-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33112-119">是否應該取消父控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="33112-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="33112-120">預設值為 **FALSE**，指定不應取消事件。</span><span class="sxs-lookup"><span data-stu-id="33112-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33112-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="33112-121">Return value</span></span>

<span data-ttu-id="33112-122">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33112-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33112-123">備註</span><span class="sxs-lookup"><span data-stu-id="33112-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="33112-124">[ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="33112-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="33112-125">這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。</span><span class="sxs-lookup"><span data-stu-id="33112-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="33112-126">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseWheel 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="33112-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="33112-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="33112-127">Requirements</span></span>



| <span data-ttu-id="33112-128">需求</span><span class="sxs-lookup"><span data-stu-id="33112-128">Requirement</span></span> | <span data-ttu-id="33112-129">值</span><span class="sxs-lookup"><span data-stu-id="33112-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33112-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33112-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33112-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33112-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="33112-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33112-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33112-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="33112-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="33112-134">標頭</span><span class="sxs-lookup"><span data-stu-id="33112-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="33112-135"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="33112-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33112-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="33112-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="33112-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33112-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="33112-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33112-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33112-139">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="33112-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="33112-140">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="33112-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="33112-141">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="33112-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 





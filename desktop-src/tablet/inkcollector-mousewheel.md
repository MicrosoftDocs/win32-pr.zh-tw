---
description: 發生于 InkCollector 或 InkOverlay 物件具有焦點時，滑鼠滾輪移動時。
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: 'InkCollector. 滑鼠滾輪事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991716"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="d8dae-103">InkCollector. 滑鼠滾輪事件</span><span class="sxs-lookup"><span data-stu-id="d8dae-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="d8dae-104">發生于 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件具有焦點時，滑鼠滾輪移動時。</span><span class="sxs-lookup"><span data-stu-id="d8dae-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8dae-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8dae-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d8dae-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8dae-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-108">已按下的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="d8dae-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d8dae-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8dae-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d8dae-111">*差異* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-112">滑鼠滾輪旋轉的刻度數目的帶正負號計數。</span><span class="sxs-lookup"><span data-stu-id="d8dae-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="d8dae-113">一個刻度是一個滑鼠滾輪的刻痕。</span><span class="sxs-lookup"><span data-stu-id="d8dae-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="d8dae-114">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-115">滑鼠點擊的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8dae-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d8dae-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-117">滑鼠點擊的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8dae-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d8dae-118">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dae-119">**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d8dae-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="d8dae-120">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d8dae-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8dae-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8dae-121">Return value</span></span>

<span data-ttu-id="d8dae-122">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d8dae-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8dae-123">備註</span><span class="sxs-lookup"><span data-stu-id="d8dae-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8dae-124">[ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="d8dae-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="d8dae-125">這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。</span><span class="sxs-lookup"><span data-stu-id="d8dae-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="d8dae-126">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseWheel 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="d8dae-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8dae-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8dae-127">Requirements</span></span>



| <span data-ttu-id="d8dae-128">需求</span><span class="sxs-lookup"><span data-stu-id="d8dae-128">Requirement</span></span> | <span data-ttu-id="d8dae-129">值</span><span class="sxs-lookup"><span data-stu-id="d8dae-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dae-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8dae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8dae-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8dae-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d8dae-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8dae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8dae-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="d8dae-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d8dae-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d8dae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8dae-135"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d8dae-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d8dae-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8dae-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8dae-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8dae-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d8dae-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8dae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8dae-139">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="d8dae-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d8dae-140">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="d8dae-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="d8dae-141">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="d8dae-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 





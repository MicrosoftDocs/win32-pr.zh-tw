---
description: 發生于滑鼠指標移至 InkCollector 或 InkOverlay 物件上方時。
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: 'InkOverlay. MouseMove 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194794"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="541b6-103">InkOverlay. MouseMove 事件</span><span class="sxs-lookup"><span data-stu-id="541b6-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="541b6-104">發生于滑鼠指標移至 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上方時。</span><span class="sxs-lookup"><span data-stu-id="541b6-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="541b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="541b6-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="541b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="541b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541b6-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541b6-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541b6-108">已按下的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="541b6-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="541b6-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541b6-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541b6-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="541b6-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="541b6-111">*pX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541b6-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541b6-112">滑鼠點擊的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="541b6-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="541b6-113">*.py* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541b6-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541b6-114">滑鼠點擊的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="541b6-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="541b6-115">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="541b6-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="541b6-116">是否應該取消父控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="541b6-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="541b6-117">預設值為 **FALSE**，指定不應取消事件。</span><span class="sxs-lookup"><span data-stu-id="541b6-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541b6-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="541b6-118">Return value</span></span>

<span data-ttu-id="541b6-119">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="541b6-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="541b6-120">備註</span><span class="sxs-lookup"><span data-stu-id="541b6-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="541b6-121">[ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="541b6-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="541b6-122">這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。</span><span class="sxs-lookup"><span data-stu-id="541b6-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="541b6-123">某些控制項依賴 [**MouseDown**](inkcollector-mousedown.md)、 [**MouseMove**](inkcollector-mousemove.md)和 [**MouseUp**](inkcollector-mouseup.md) 事件之間的特定關聯性。</span><span class="sxs-lookup"><span data-stu-id="541b6-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="541b6-124">取消其中某些事件可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="541b6-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="541b6-125">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseMove 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="541b6-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="541b6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="541b6-126">Requirements</span></span>



| <span data-ttu-id="541b6-127">需求</span><span class="sxs-lookup"><span data-stu-id="541b6-127">Requirement</span></span> | <span data-ttu-id="541b6-128">值</span><span class="sxs-lookup"><span data-stu-id="541b6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="541b6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="541b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="541b6-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="541b6-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="541b6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="541b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="541b6-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="541b6-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="541b6-133">標頭</span><span class="sxs-lookup"><span data-stu-id="541b6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="541b6-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="541b6-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="541b6-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="541b6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="541b6-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="541b6-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="541b6-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="541b6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541b6-138">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="541b6-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="541b6-139">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="541b6-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="541b6-140">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="541b6-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 





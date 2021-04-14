---
description: 發生于滑鼠指標位於 InkCollector 或 InkOverlay 物件上方，並放開滑鼠按鍵時。
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: InkCollector (Msinkaut) 的 MouseUp 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f217cf6f5eeff930c1746d1a5ceac180686942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468772"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="1b91a-103">InkCollector，事件</span><span class="sxs-lookup"><span data-stu-id="1b91a-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="1b91a-104">發生于滑鼠指標位於 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上方，並放開滑鼠按鍵時。</span><span class="sxs-lookup"><span data-stu-id="1b91a-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b91a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1b91a-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="1b91a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1b91a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b91a-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b91a-108">已釋放的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="1b91a-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="1b91a-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b91a-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="1b91a-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="1b91a-111">*pX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b91a-112">滑鼠點擊的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1b91a-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="1b91a-113">*.py* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b91a-114">滑鼠點擊的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1b91a-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="1b91a-115">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b91a-116">**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1b91a-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b91a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b91a-117">Return value</span></span>

<span data-ttu-id="1b91a-118">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b91a-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b91a-119">備註</span><span class="sxs-lookup"><span data-stu-id="1b91a-119">Remarks</span></span>

<span data-ttu-id="1b91a-120">若要改善即時筆墨效能，請在 [**MouseDown**](inkcollector-mousedown.md) 和 **MouseUp** 事件處理常式中隱藏或顯示滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="1b91a-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="1b91a-121">[ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="1b91a-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="1b91a-122">這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。</span><span class="sxs-lookup"><span data-stu-id="1b91a-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="1b91a-123">某些控制項依賴 [**MouseDown**](inkcollector-mousedown.md)、 [**MouseMove**](inkcollector-mousemove.md)和 **MouseUp** 事件之間的特定關聯性。</span><span class="sxs-lookup"><span data-stu-id="1b91a-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="1b91a-124">取消其中某些事件可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="1b91a-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="1b91a-125">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseUp 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="1b91a-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b91a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b91a-126">Requirements</span></span>



| <span data-ttu-id="1b91a-127">需求</span><span class="sxs-lookup"><span data-stu-id="1b91a-127">Requirement</span></span> | <span data-ttu-id="1b91a-128">值</span><span class="sxs-lookup"><span data-stu-id="1b91a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b91a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b91a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1b91a-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b91a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1b91a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b91a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1b91a-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="1b91a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1b91a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1b91a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b91a-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1b91a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b91a-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="1b91a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b91a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b91a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1b91a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b91a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b91a-138">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="1b91a-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="1b91a-139">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="1b91a-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="1b91a-140">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="1b91a-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 





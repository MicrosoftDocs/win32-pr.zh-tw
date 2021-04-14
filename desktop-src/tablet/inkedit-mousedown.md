---
description: 發生于滑鼠停留在 InkEdit 控制項上時，使用者按下滑鼠按鍵時。
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: InkEdit)  (筆跡的事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852180"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="1d2ad-103">InkEdit 的 MouseDown 事件</span><span class="sxs-lookup"><span data-stu-id="1d2ad-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="1d2ad-104">發生于滑鼠停留在 [InkEdit](inkedit-control-reference.md) 控制項上時，使用者按下滑鼠按鍵時。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d2ad-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="1d2ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d2ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2ad-107">*按鈕*</span><span class="sxs-lookup"><span data-stu-id="1d2ad-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2ad-108">[**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)列舉的成員，指出所按下的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="1d2ad-109">值</span><span class="sxs-lookup"><span data-stu-id="1d2ad-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="1d2ad-110">意義</span><span class="sxs-lookup"><span data-stu-id="1d2ad-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="1d2ad-111"><dt>**否 \_按鈕**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="1d2ad-112">預設值。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-112">Default.</span></span> <span data-ttu-id="1d2ad-113">不按任何滑鼠鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="1d2ad-114"><dt>**左方 \_按鈕**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="1d2ad-115">按滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="1d2ad-116"><dt>**RIGHT \_按鈕**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="1d2ad-117">按滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="1d2ad-118"><dt>**中間 \_按鈕**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="1d2ad-119">按滑鼠中間鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="1d2ad-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="1d2ad-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2ad-121">[**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)列舉的成員，指出事件時要按下的輔助按鍵。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="1d2ad-122">值</span><span class="sxs-lookup"><span data-stu-id="1d2ad-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="1d2ad-123">意義</span><span class="sxs-lookup"><span data-stu-id="1d2ad-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="1d2ad-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="1d2ad-125">指定 SHIFT 鍵已做為修飾詞使用。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="1d2ad-126"><dt>**IKM \_控制項**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="1d2ad-127">指定使用 CTRL 鍵做為修飾詞。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="1d2ad-128"><dt>**IKM \_Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="1d2ad-129">指定使用 ALT 鍵做為修飾詞。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="1d2ad-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="1d2ad-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2ad-131">滑鼠指標的目前 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="1d2ad-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="1d2ad-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2ad-133">滑鼠指標的目前 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2ad-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d2ad-134">Return value</span></span>

<span data-ttu-id="1d2ad-135">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d2ad-136">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2ad-137">備註</span><span class="sxs-lookup"><span data-stu-id="1d2ad-137">Remarks</span></span>

<span data-ttu-id="1d2ad-138">當指標停留在 [InkEdit](inkedit-control-reference.md) 控制項上時，如果按下滑鼠按鍵，該控制項就會捕捉滑鼠並接收所有的滑鼠事件，直到和包含最後一個 [**MouseUp**](inkedit-mouseup.md) 事件為止。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="1d2ad-139">這表示滑鼠事件所傳回的 (x、y) 滑鼠指標座標不一定會在接收它們的物件內部區域中。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="1d2ad-140">如果連續按下滑鼠按鍵，則在第一次按下時捕捉滑鼠的物件會收到所有的滑鼠事件，直到所有按鈕都放開為止。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="1d2ad-141">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="1d2ad-142">**\_ IInkEditEvents** 介面會以 DISPID IeeMouseDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1d2ad-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2ad-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d2ad-143">Requirements</span></span>



| <span data-ttu-id="1d2ad-144">需求</span><span class="sxs-lookup"><span data-stu-id="1d2ad-144">Requirement</span></span> | <span data-ttu-id="1d2ad-145">值</span><span class="sxs-lookup"><span data-stu-id="1d2ad-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2ad-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d2ad-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2ad-147">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d2ad-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d2ad-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d2ad-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2ad-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="1d2ad-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1d2ad-150">標頭</span><span class="sxs-lookup"><span data-stu-id="1d2ad-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2ad-151"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1d2ad-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d2ad-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d2ad-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2ad-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1d2ad-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d2ad-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2ad-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="1d2ad-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1d2ad-156">**InkMouseButton 列舉**</span><span class="sxs-lookup"><span data-stu-id="1d2ad-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="1d2ad-157">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="1d2ad-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="1d2ad-158">[**MouseMove 事件 \[ InkEdit 控制項\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="1d2ad-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="1d2ad-159">[**MouseUp 事件 \[ InkEdit 控制項\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="1d2ad-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 


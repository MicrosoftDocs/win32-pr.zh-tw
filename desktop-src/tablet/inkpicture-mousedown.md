---
description: 發生于滑鼠指標位於 InkPicture 控制項上方且按下滑鼠按鍵時。
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: InkPicture)  (Msinkaut 的事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193724"
---
# <a name="inkpicturemousedown-event"></a><span data-ttu-id="98414-103">InkPicture 的 MouseDown 事件</span><span class="sxs-lookup"><span data-stu-id="98414-103">InkPicture.MouseDown event</span></span>

<span data-ttu-id="98414-104">發生于滑鼠指標位於 [InkPicture](inkpicture-control-reference.md) 控制項上方且按下滑鼠按鍵時。</span><span class="sxs-lookup"><span data-stu-id="98414-104">Occurs when the mouse pointer is over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="98414-105">語法</span><span class="sxs-lookup"><span data-stu-id="98414-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="98414-106">參數</span><span class="sxs-lookup"><span data-stu-id="98414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98414-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98414-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98414-108">已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="98414-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="98414-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98414-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98414-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="98414-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="98414-111">*pX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98414-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98414-112">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="98414-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="98414-113">*.py* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98414-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98414-114">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="98414-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="98414-115">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="98414-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98414-116">**變異 \_TRUE** 表示取消父控制項的這個事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="98414-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98414-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="98414-117">Return value</span></span>

<span data-ttu-id="98414-118">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="98414-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98414-119">備註</span><span class="sxs-lookup"><span data-stu-id="98414-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="98414-120">參數 pX 與 .Py 是以圖元為單位，而不是與筆墨空間座標系統相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="98414-120">The parameters pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="98414-121">這是因為此事件會取代無法辨識的應用程式的相關滑鼠事件，而且該應用程式類型只會參考圖元。</span><span class="sxs-lookup"><span data-stu-id="98414-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="98414-122">某些控制項依賴 **MouseDown**、 [**MouseMove**](inkpicture-mousemove.md)和 [**MouseUp**](inkpicture-mouseup.md) 事件之間的特定關聯性。</span><span class="sxs-lookup"><span data-stu-id="98414-122">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkpicture-mousemove.md), and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="98414-123">取消其中某些事件可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="98414-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="98414-124">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="98414-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="98414-125">**\_ IInkPictureEvents** 介面會以 DISPID IPEMouseDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="98414-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="98414-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="98414-126">Requirements</span></span>



| <span data-ttu-id="98414-127">需求</span><span class="sxs-lookup"><span data-stu-id="98414-127">Requirement</span></span> | <span data-ttu-id="98414-128">值</span><span class="sxs-lookup"><span data-stu-id="98414-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98414-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98414-129">Minimum supported client</span></span><br/> | <span data-ttu-id="98414-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98414-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="98414-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98414-131">Minimum supported server</span></span><br/> | <span data-ttu-id="98414-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="98414-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="98414-133">標頭</span><span class="sxs-lookup"><span data-stu-id="98414-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="98414-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="98414-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98414-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="98414-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="98414-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98414-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="98414-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98414-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98414-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="98414-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


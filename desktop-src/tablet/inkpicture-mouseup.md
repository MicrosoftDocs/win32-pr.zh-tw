---
description: 發生于滑鼠指標移至 InkPicture 控制項上並放開滑鼠按鍵時。
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: InkPicture (Msinkaut) 的 MouseUp 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987642"
---
# <a name="inkpicturemouseup-event"></a><span data-ttu-id="92df2-103">InkPicture，事件</span><span class="sxs-lookup"><span data-stu-id="92df2-103">InkPicture.MouseUp event</span></span>

<span data-ttu-id="92df2-104">發生于滑鼠指標移至 [InkPicture](inkpicture-control-reference.md) 控制項上並放開滑鼠按鍵時。</span><span class="sxs-lookup"><span data-stu-id="92df2-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="92df2-105">語法</span><span class="sxs-lookup"><span data-stu-id="92df2-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="92df2-106">參數</span><span class="sxs-lookup"><span data-stu-id="92df2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92df2-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92df2-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df2-108">已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="92df2-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="92df2-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92df2-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df2-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="92df2-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="92df2-111">*pX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92df2-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df2-112">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="92df2-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="92df2-113">*.py* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92df2-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df2-114">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="92df2-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="92df2-115">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="92df2-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92df2-116">**變異 \_TRUE** 表示取消父控制項的 MouseUp 事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="92df2-116">**VARIANT\_TRUE** to cancel the MouseUp event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92df2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="92df2-117">Return value</span></span>

<span data-ttu-id="92df2-118">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="92df2-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92df2-119">備註</span><span class="sxs-lookup"><span data-stu-id="92df2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92df2-120">參數 *pX* 與 *.py* 是以圖元為單位，而不是與筆墨空間座標系統相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="92df2-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="92df2-121">這是因為此事件會取代無法辨識的應用程式的相關滑鼠事件，而且該應用程式類型只會參考圖元。</span><span class="sxs-lookup"><span data-stu-id="92df2-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="92df2-122">某些控制項依賴 [**MouseDown**](inkpicture-mousedown.md)、 [**MouseMove**](inkpicture-mousemove.md)和 **MouseUp** 事件之間的特定關聯性。</span><span class="sxs-lookup"><span data-stu-id="92df2-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="92df2-123">取消其中某些事件可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="92df2-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="92df2-124">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="92df2-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="92df2-125">**\_ IInkPictureEvents** 介面會以 DISPID IPEMouseDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92df2-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="92df2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="92df2-126">Requirements</span></span>



| <span data-ttu-id="92df2-127">需求</span><span class="sxs-lookup"><span data-stu-id="92df2-127">Requirement</span></span> | <span data-ttu-id="92df2-128">值</span><span class="sxs-lookup"><span data-stu-id="92df2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92df2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92df2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="92df2-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92df2-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92df2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92df2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="92df2-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="92df2-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="92df2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="92df2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="92df2-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="92df2-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92df2-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="92df2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="92df2-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92df2-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="92df2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92df2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92df2-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="92df2-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


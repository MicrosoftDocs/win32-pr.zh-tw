---
description: 當游標提示接觸到數位化的 tablet 介面時發生。
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: 'InkPicture. CursorDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513925"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="e890e-103">InkPicture. CursorDown 事件</span><span class="sxs-lookup"><span data-stu-id="e890e-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="e890e-104">當游標提示接觸到數位化的 tablet 介面時發生。</span><span class="sxs-lookup"><span data-stu-id="e890e-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e890e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e890e-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="e890e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e890e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e890e-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e890e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e890e-108">產生 **CursorDown** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="e890e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="e890e-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e890e-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e890e-110">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件造成引發 **CursorDown** 事件時所啟動的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。</span><span class="sxs-lookup"><span data-stu-id="e890e-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e890e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e890e-111">Return value</span></span>

<span data-ttu-id="e890e-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e890e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e890e-113">備註</span><span class="sxs-lookup"><span data-stu-id="e890e-113">Remarks</span></span>

<span data-ttu-id="e890e-114">這些事件方法會定義在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 介面中。</span><span class="sxs-lookup"><span data-stu-id="e890e-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="e890e-115">**\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 介面會以 DISPID ICECursorDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e890e-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="e890e-116">請小心使用此事件，因為在事件處理常式中執行太多程式碼時，可能會對筆墨效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="e890e-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="e890e-117">若要改善即時筆墨效能，請在 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件處理常式中隱藏或顯示滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="e890e-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e890e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e890e-118">Requirements</span></span>



| <span data-ttu-id="e890e-119">需求</span><span class="sxs-lookup"><span data-stu-id="e890e-119">Requirement</span></span> | <span data-ttu-id="e890e-120">值</span><span class="sxs-lookup"><span data-stu-id="e890e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e890e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e890e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e890e-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e890e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e890e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e890e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e890e-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="e890e-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e890e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e890e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e890e-126"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e890e-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e890e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e890e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e890e-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e890e-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e890e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e890e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e890e-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e890e-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e890e-131">**CursorButtonUp 事件**</span><span class="sxs-lookup"><span data-stu-id="e890e-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="e890e-132">**CursorButtonDown 事件**</span><span class="sxs-lookup"><span data-stu-id="e890e-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="e890e-133">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="e890e-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="e890e-134">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="e890e-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


---
description: 從 InkDisp 物件中刪除筆劃時發生。
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: 'InkDisp. InkDeleted 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971361"
---
# <a name="inkdispinkdeleted-event"></a><span data-ttu-id="85632-103">InkDisp. InkDeleted 事件</span><span class="sxs-lookup"><span data-stu-id="85632-103">InkDisp.InkDeleted event</span></span>

<span data-ttu-id="85632-104">從 [**InkDisp**](inkdisp-class.md) 物件中刪除筆劃時發生。</span><span class="sxs-lookup"><span data-stu-id="85632-104">Occurs when a stroke is deleted from the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85632-105">語法</span><span class="sxs-lookup"><span data-stu-id="85632-105">Syntax</span></span>


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="85632-106">參數</span><span class="sxs-lookup"><span data-stu-id="85632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85632-107">*StrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85632-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85632-108">指定當此事件發生時，已刪除之所有筆劃的筆觸識別碼資訊的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="85632-108">Specifies the integer array of stroke ID information for all of the strokes that have been deleted when this event occurs.</span></span>

<span data-ttu-id="85632-109">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="85632-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85632-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="85632-110">Return value</span></span>

<span data-ttu-id="85632-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="85632-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85632-112">備註</span><span class="sxs-lookup"><span data-stu-id="85632-112">Remarks</span></span>

<span data-ttu-id="85632-113">如果您使用 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 控制項 (其中 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) 等於 [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) 和 [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) 並透過筆劃傳遞橡皮擦，則會取得下列一連串的事件：</span><span class="sxs-lookup"><span data-stu-id="85632-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   <span data-ttu-id="85632-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="85632-114">**InkDeleted**</span></span>
-   [<span data-ttu-id="85632-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="85632-115">**InkAdded**</span></span>](inkdisp-inkadded.md)
-   <span data-ttu-id="85632-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="85632-116">**InkDeleted**</span></span>

<span data-ttu-id="85632-117">因為基礎程式碼會新增內部、不可見的筆觸來追蹤橡皮擦，所以會發生其他 [**InkAdded**](inkdisp-inkadded.md) 和 **InkDeleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="85632-117">The additional [**InkAdded**](inkdisp-inkadded.md) and **InkDeleted** events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="85632-118">此事件方法是在 \_ IInkEvents 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="85632-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="85632-119">\_IInkEvents 介面會以 DISPID IEInkDeleted 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="85632-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkDeleted.</span></span>

<span data-ttu-id="85632-120">即使在選取或清除模式下，也不只是在插入筆墨時，也會引發 **InkDeleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="85632-120">The **InkDeleted** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="85632-121">這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。</span><span class="sxs-lookup"><span data-stu-id="85632-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="85632-122">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="85632-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="85632-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="85632-123">Requirements</span></span>



| <span data-ttu-id="85632-124">需求</span><span class="sxs-lookup"><span data-stu-id="85632-124">Requirement</span></span> | <span data-ttu-id="85632-125">值</span><span class="sxs-lookup"><span data-stu-id="85632-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85632-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85632-126">Minimum supported client</span></span><br/> | <span data-ttu-id="85632-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85632-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85632-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85632-128">Minimum supported server</span></span><br/> | <span data-ttu-id="85632-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="85632-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85632-130">標頭</span><span class="sxs-lookup"><span data-stu-id="85632-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="85632-131"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="85632-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85632-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="85632-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="85632-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85632-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85632-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85632-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85632-135">**InkDisp 類別**</span><span class="sxs-lookup"><span data-stu-id="85632-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="85632-136">[**System.windows.controls.inkcanvas.editingmode 屬性 \[ InkOverlay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="85632-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="85632-137">[**EraserMode 屬性 \[ InkOverlay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="85632-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="85632-138">**InkAdded 事件**</span><span class="sxs-lookup"><span data-stu-id="85632-138">**InkAdded Event**</span></span>](inkdisp-inkadded.md)
</dt> <dt>

[<span data-ttu-id="85632-139">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="85632-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="85632-140">InkPicture 控制項參考</span><span class="sxs-lookup"><span data-stu-id="85632-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="85632-141">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="85632-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


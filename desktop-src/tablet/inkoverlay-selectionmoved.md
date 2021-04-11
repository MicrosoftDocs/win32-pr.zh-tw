---
description: 發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或選取專案屬性。
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: 'SelectionMoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320443"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="29f49-103">SelectionMoved 事件</span><span class="sxs-lookup"><span data-stu-id="29f49-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="29f49-104">發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="29f49-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f49-105">語法</span><span class="sxs-lookup"><span data-stu-id="29f49-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="29f49-106">參數</span><span class="sxs-lookup"><span data-stu-id="29f49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29f49-107">*OldSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29f49-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f49-108">所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionMoved** 事件之前就已存在。</span><span class="sxs-lookup"><span data-stu-id="29f49-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="29f49-109">這個矩形是以筆墨空間座標指定，可允許復原案例。</span><span class="sxs-lookup"><span data-stu-id="29f49-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29f49-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="29f49-110">Return value</span></span>

<span data-ttu-id="29f49-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29f49-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29f49-112">備註</span><span class="sxs-lookup"><span data-stu-id="29f49-112">Remarks</span></span>

<span data-ttu-id="29f49-113">此事件方法是在 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 僅分派介面中定義， (具有 DISPID IOESelectionMoved 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="29f49-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="29f49-114">若要取得已移動之筆劃集合的新周框，請呼叫 [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) 方法。</span><span class="sxs-lookup"><span data-stu-id="29f49-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="29f49-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="29f49-115">Requirements</span></span>



| <span data-ttu-id="29f49-116">需求</span><span class="sxs-lookup"><span data-stu-id="29f49-116">Requirement</span></span> | <span data-ttu-id="29f49-117">值</span><span class="sxs-lookup"><span data-stu-id="29f49-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29f49-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29f49-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29f49-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29f49-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="29f49-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29f49-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29f49-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="29f49-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="29f49-122">標頭</span><span class="sxs-lookup"><span data-stu-id="29f49-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29f49-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="29f49-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="29f49-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="29f49-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="29f49-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29f49-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="29f49-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29f49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f49-127">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="29f49-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="29f49-128">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="29f49-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="29f49-129">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="29f49-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


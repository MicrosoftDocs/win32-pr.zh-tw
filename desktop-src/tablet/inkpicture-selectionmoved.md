---
description: 發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或選取專案屬性。
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: 'InkPicture. SelectionMoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319727"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="161a7-103">InkPicture. SelectionMoved 事件</span><span class="sxs-lookup"><span data-stu-id="161a7-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="161a7-104">發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="161a7-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="161a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="161a7-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="161a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="161a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="161a7-107">*OldSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="161a7-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161a7-108">所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionMoved** 事件之前就已存在。</span><span class="sxs-lookup"><span data-stu-id="161a7-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="161a7-109">這個矩形是以筆墨空間座標指定，可允許復原案例。</span><span class="sxs-lookup"><span data-stu-id="161a7-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="161a7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="161a7-110">Return value</span></span>

<span data-ttu-id="161a7-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="161a7-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="161a7-112">備註</span><span class="sxs-lookup"><span data-stu-id="161a7-112">Remarks</span></span>

<span data-ttu-id="161a7-113">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionMoved 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="161a7-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="161a7-114">若要取得已移動之筆劃集合的新周框，請呼叫 [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) 方法。</span><span class="sxs-lookup"><span data-stu-id="161a7-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="161a7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="161a7-115">Requirements</span></span>



| <span data-ttu-id="161a7-116">需求</span><span class="sxs-lookup"><span data-stu-id="161a7-116">Requirement</span></span> | <span data-ttu-id="161a7-117">值</span><span class="sxs-lookup"><span data-stu-id="161a7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="161a7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="161a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="161a7-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="161a7-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="161a7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="161a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="161a7-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="161a7-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="161a7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="161a7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="161a7-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="161a7-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="161a7-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="161a7-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="161a7-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="161a7-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="161a7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="161a7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="161a7-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="161a7-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="161a7-128">[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="161a7-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="161a7-129">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="161a7-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


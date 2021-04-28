---
description: SelectionResized 事件-發生于目前選取範圍的大小變更時，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: 'SelectionResized 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116876"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="edbd5-103">SelectionResized 事件</span><span class="sxs-lookup"><span data-stu-id="edbd5-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="edbd5-104">發生于目前選取範圍的大小變更時，例如透過對使用者介面的變異、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="edbd5-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbd5-105">語法</span><span class="sxs-lookup"><span data-stu-id="edbd5-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="edbd5-106">參數</span><span class="sxs-lookup"><span data-stu-id="edbd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbd5-107">*OldSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edbd5-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edbd5-108">所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionResized** 事件之前就已存在。</span><span class="sxs-lookup"><span data-stu-id="edbd5-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="edbd5-109">這個矩形是以筆墨空間座標指定，可允許復原案例。</span><span class="sxs-lookup"><span data-stu-id="edbd5-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edbd5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="edbd5-110">Return value</span></span>

<span data-ttu-id="edbd5-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="edbd5-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbd5-112">備註</span><span class="sxs-lookup"><span data-stu-id="edbd5-112">Remarks</span></span>

<span data-ttu-id="edbd5-113">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionResized 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="edbd5-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbd5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="edbd5-114">Requirements</span></span>



| <span data-ttu-id="edbd5-115">需求</span><span class="sxs-lookup"><span data-stu-id="edbd5-115">Requirement</span></span> | <span data-ttu-id="edbd5-116">值</span><span class="sxs-lookup"><span data-stu-id="edbd5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbd5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edbd5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="edbd5-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edbd5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="edbd5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edbd5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="edbd5-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="edbd5-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="edbd5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="edbd5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbd5-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="edbd5-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="edbd5-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="edbd5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="edbd5-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edbd5-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="edbd5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edbd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbd5-126">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="edbd5-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="edbd5-127">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="edbd5-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="edbd5-128">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="edbd5-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


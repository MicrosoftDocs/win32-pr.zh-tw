---
description: 發生于目前選取範圍的大小變更時，例如透過對使用者介面的變異、剪下和貼上程式，或選取專案屬性。
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: 'SelectionResized 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194791"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="d2f3e-103">SelectionResized 事件</span><span class="sxs-lookup"><span data-stu-id="d2f3e-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="d2f3e-104">發生于目前選取範圍的大小變更時，例如透過對使用者介面的變異、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2f3e-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f3e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2f3e-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="d2f3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2f3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f3e-107">*OldSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2f3e-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f3e-108">所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionResized** 事件之前就已存在。</span><span class="sxs-lookup"><span data-stu-id="d2f3e-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="d2f3e-109">這個矩形是以筆墨空間座標指定，可允許復原案例。</span><span class="sxs-lookup"><span data-stu-id="d2f3e-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f3e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2f3e-110">Return value</span></span>

<span data-ttu-id="d2f3e-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d2f3e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f3e-112">備註</span><span class="sxs-lookup"><span data-stu-id="d2f3e-112">Remarks</span></span>

<span data-ttu-id="d2f3e-113">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionResized 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2f3e-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f3e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2f3e-114">Requirements</span></span>



| <span data-ttu-id="d2f3e-115">需求</span><span class="sxs-lookup"><span data-stu-id="d2f3e-115">Requirement</span></span> | <span data-ttu-id="d2f3e-116">值</span><span class="sxs-lookup"><span data-stu-id="d2f3e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f3e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2f3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f3e-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2f3e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d2f3e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2f3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f3e-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="d2f3e-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d2f3e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d2f3e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2f3e-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d2f3e-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2f3e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2f3e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2f3e-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f3e-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d2f3e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2f3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f3e-126">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="d2f3e-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="d2f3e-127">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="d2f3e-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="d2f3e-128">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="d2f3e-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


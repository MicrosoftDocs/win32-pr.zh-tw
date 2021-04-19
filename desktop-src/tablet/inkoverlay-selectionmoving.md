---
description: 當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: 'SelectionMoving 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975250"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="33558-103">SelectionMoving 事件</span><span class="sxs-lookup"><span data-stu-id="33558-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="33558-104">當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="33558-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="33558-105">語法</span><span class="sxs-lookup"><span data-stu-id="33558-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="33558-106">參數</span><span class="sxs-lookup"><span data-stu-id="33558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33558-107">*CurSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33558-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33558-108">在 **SelectionMoving** 事件之後要將選取範圍移至其中的矩形。</span><span class="sxs-lookup"><span data-stu-id="33558-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="33558-109">這個矩形是在用戶端視窗座標中指定，可讓您在調整大小時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="33558-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33558-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="33558-110">Return value</span></span>

<span data-ttu-id="33558-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33558-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33558-112">備註</span><span class="sxs-lookup"><span data-stu-id="33558-112">Remarks</span></span>

<span data-ttu-id="33558-113">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有非 DISPID IOESELECTIONMOVING 的識別碼) \_ 。</span><span class="sxs-lookup"><span data-stu-id="33558-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="33558-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="33558-114">Requirements</span></span>



| <span data-ttu-id="33558-115">需求</span><span class="sxs-lookup"><span data-stu-id="33558-115">Requirement</span></span> | <span data-ttu-id="33558-116">值</span><span class="sxs-lookup"><span data-stu-id="33558-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33558-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33558-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33558-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33558-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="33558-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33558-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33558-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="33558-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="33558-121">標頭</span><span class="sxs-lookup"><span data-stu-id="33558-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33558-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="33558-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33558-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="33558-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="33558-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33558-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="33558-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33558-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33558-126">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="33558-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="33558-127">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="33558-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="33558-128">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="33558-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="33558-129">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="33558-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





---
description: 發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或選取屬性）。
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: 'SelectionResizing 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7debb9461aae39c0549bce863a0513b86c53ffa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194419"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="f5b96-103">SelectionResizing 事件</span><span class="sxs-lookup"><span data-stu-id="f5b96-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="f5b96-104">發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。</span><span class="sxs-lookup"><span data-stu-id="f5b96-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b96-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5b96-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="f5b96-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5b96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b96-107">*CurSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-108">**SelectionResizing** 事件之後選取範圍的周框。</span><span class="sxs-lookup"><span data-stu-id="f5b96-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="f5b96-109">這個矩形是在用戶端視窗座標中指定，可讓您在調整大小時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f5b96-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b96-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5b96-110">Return value</span></span>

<span data-ttu-id="f5b96-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f5b96-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b96-112">備註</span><span class="sxs-lookup"><span data-stu-id="f5b96-112">Remarks</span></span>

<span data-ttu-id="f5b96-113">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionResizing 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5b96-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b96-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5b96-114">Requirements</span></span>



| <span data-ttu-id="f5b96-115">需求</span><span class="sxs-lookup"><span data-stu-id="f5b96-115">Requirement</span></span> | <span data-ttu-id="f5b96-116">值</span><span class="sxs-lookup"><span data-stu-id="f5b96-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b96-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5b96-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b96-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f5b96-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5b96-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b96-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="f5b96-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f5b96-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f5b96-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b96-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f5b96-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5b96-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5b96-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5b96-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b96-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f5b96-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5b96-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b96-126">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="f5b96-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f5b96-127">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="f5b96-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="f5b96-128">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="f5b96-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





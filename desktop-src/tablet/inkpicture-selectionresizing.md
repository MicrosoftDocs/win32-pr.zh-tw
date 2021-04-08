---
description: 發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或選取屬性）。
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: 'InkPicture. SelectionResizing 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945165"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="d4152-103">InkPicture. SelectionResizing 事件</span><span class="sxs-lookup"><span data-stu-id="d4152-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="d4152-104">發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。</span><span class="sxs-lookup"><span data-stu-id="d4152-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4152-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4152-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="d4152-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4152-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4152-107">*CurSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4152-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4152-108">**SelectionResizing** 事件之後選取範圍的周框。</span><span class="sxs-lookup"><span data-stu-id="d4152-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="d4152-109">這個矩形是在用戶端視窗座標中指定，可讓您在調整大小時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="d4152-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4152-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4152-110">Return value</span></span>

<span data-ttu-id="d4152-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d4152-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4152-112">備註</span><span class="sxs-lookup"><span data-stu-id="d4152-112">Remarks</span></span>

<span data-ttu-id="d4152-113">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionResizing 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="d4152-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4152-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4152-114">Requirements</span></span>



| <span data-ttu-id="d4152-115">需求</span><span class="sxs-lookup"><span data-stu-id="d4152-115">Requirement</span></span> | <span data-ttu-id="d4152-116">值</span><span class="sxs-lookup"><span data-stu-id="d4152-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4152-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4152-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4152-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4152-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d4152-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4152-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4152-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="d4152-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d4152-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d4152-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4152-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d4152-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4152-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4152-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4152-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4152-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d4152-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4152-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4152-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d4152-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="d4152-127">[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="d4152-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="d4152-128">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="d4152-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





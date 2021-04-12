---
description: 當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: 'InkPicture. SelectionMoving 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027413"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="f31df-103">InkPicture. SelectionMoving 事件</span><span class="sxs-lookup"><span data-stu-id="f31df-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="f31df-104">當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f31df-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31df-105">語法</span><span class="sxs-lookup"><span data-stu-id="f31df-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="f31df-106">參數</span><span class="sxs-lookup"><span data-stu-id="f31df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31df-107">*CurSelectionRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f31df-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31df-108">在 **SelectionMoving** 事件之後要將選取範圍移至其中的矩形。</span><span class="sxs-lookup"><span data-stu-id="f31df-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="f31df-109">這個矩形是在用戶端視窗座標中指定，可讓您在調整大小時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f31df-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31df-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f31df-110">Return value</span></span>

<span data-ttu-id="f31df-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f31df-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31df-112">備註</span><span class="sxs-lookup"><span data-stu-id="f31df-112">Remarks</span></span>

<span data-ttu-id="f31df-113">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionMoving 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="f31df-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31df-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f31df-114">Requirements</span></span>



| <span data-ttu-id="f31df-115">需求</span><span class="sxs-lookup"><span data-stu-id="f31df-115">Requirement</span></span> | <span data-ttu-id="f31df-116">值</span><span class="sxs-lookup"><span data-stu-id="f31df-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31df-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f31df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f31df-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f31df-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f31df-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f31df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f31df-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="f31df-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f31df-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f31df-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f31df-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f31df-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f31df-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f31df-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f31df-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31df-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f31df-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f31df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31df-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f31df-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="f31df-127">[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="f31df-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="f31df-128">**InkRectangle 類別**</span><span class="sxs-lookup"><span data-stu-id="f31df-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





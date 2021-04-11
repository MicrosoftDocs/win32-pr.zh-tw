---
description: InkPicture 控制項調整大小時， (寬度和/或高度屬性值變更) 時發生。
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: 'InkPicture： Resize 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027208"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="0b310-103">InkPicture。調整大小事件</span><span class="sxs-lookup"><span data-stu-id="0b310-103">InkPicture.Resize event</span></span>

<span data-ttu-id="0b310-104">[InkPicture](inkpicture-control-reference.md)控制項調整大小時， (寬度和/或高度屬性值變更) 時發生。</span><span class="sxs-lookup"><span data-stu-id="0b310-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b310-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b310-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="0b310-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b310-107">*離開*</span><span class="sxs-lookup"><span data-stu-id="0b310-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="0b310-108">從視窗左邊的圖元數，其中包含控制項左邊的控制項。</span><span class="sxs-lookup"><span data-stu-id="0b310-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0b310-109">*前幾個*</span><span class="sxs-lookup"><span data-stu-id="0b310-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="0b310-110">從視窗頂端的圖元數，包含控制項頂端的控制項。</span><span class="sxs-lookup"><span data-stu-id="0b310-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0b310-111">*對*</span><span class="sxs-lookup"><span data-stu-id="0b310-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="0b310-112">從視窗左邊的圖元數，其中包含控制項右邊的控制項。</span><span class="sxs-lookup"><span data-stu-id="0b310-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0b310-113">*下層*</span><span class="sxs-lookup"><span data-stu-id="0b310-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="0b310-114">從視窗頂端的圖元數，包含控制項底部的控制項。</span><span class="sxs-lookup"><span data-stu-id="0b310-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b310-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b310-115">Return value</span></span>

<span data-ttu-id="0b310-116">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0b310-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b310-117">備註</span><span class="sxs-lookup"><span data-stu-id="0b310-117">Remarks</span></span>

<span data-ttu-id="0b310-118">控制項的新寬度（以圖元為單位）會等於 *右邊* 和 *左方* 參數之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0b310-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="0b310-119">同樣地，新的高度將等於 *底端* 和 *頂端* 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0b310-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="0b310-120">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="0b310-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="0b310-121">**\_ IInkPictureEvents** 介面會以 **DISPID \_ IPEResize** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="0b310-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b310-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b310-122">Requirements</span></span>



| <span data-ttu-id="0b310-123">需求</span><span class="sxs-lookup"><span data-stu-id="0b310-123">Requirement</span></span> | <span data-ttu-id="0b310-124">值</span><span class="sxs-lookup"><span data-stu-id="0b310-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b310-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b310-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b310-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b310-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0b310-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b310-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b310-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="0b310-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0b310-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0b310-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b310-130"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0b310-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0b310-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b310-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b310-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b310-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0b310-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b310-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b310-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0b310-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 





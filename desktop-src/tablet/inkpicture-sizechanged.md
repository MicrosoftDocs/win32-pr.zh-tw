---
description: 發生于調整 InkPicture 控制項的大小時，特別是在寬度或高度屬性值變更之後。
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: 'InkPicture. SizeChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945164"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="a3eee-103">InkPicture. SizeChanged 事件</span><span class="sxs-lookup"><span data-stu-id="a3eee-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="a3eee-104">發生于調整 [InkPicture](inkpicture-control-reference.md) 控制項的大小時，特別是在 [**寬度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) 或 [**高度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) 屬性值變更之後。</span><span class="sxs-lookup"><span data-stu-id="a3eee-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3eee-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3eee-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="a3eee-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3eee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3eee-107">*左方* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3eee-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3eee-108">[InkPicture](inkpicture-control-reference.md)控制項左邊的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="a3eee-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="a3eee-109">*頂端* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3eee-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3eee-110">[InkPicture](inkpicture-control-reference.md)控制項頂端的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a3eee-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="a3eee-111">*Right* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3eee-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3eee-112">[InkPicture](inkpicture-control-reference.md)控制項右邊的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="a3eee-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="a3eee-113">*底部* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3eee-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3eee-114">[InkPicture](inkpicture-control-reference.md)控制項底部的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a3eee-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3eee-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3eee-115">Return value</span></span>

<span data-ttu-id="a3eee-116">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a3eee-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3eee-117">備註</span><span class="sxs-lookup"><span data-stu-id="a3eee-117">Remarks</span></span>

<span data-ttu-id="a3eee-118">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="a3eee-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="a3eee-119">**\_ IInkPictureEvents** 介面會以 DISPID IPESizeChanged 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a3eee-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3eee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3eee-120">Requirements</span></span>



| <span data-ttu-id="a3eee-121">需求</span><span class="sxs-lookup"><span data-stu-id="a3eee-121">Requirement</span></span> | <span data-ttu-id="a3eee-122">值</span><span class="sxs-lookup"><span data-stu-id="a3eee-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3eee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3eee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3eee-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3eee-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a3eee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3eee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3eee-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="a3eee-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a3eee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a3eee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3eee-128"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a3eee-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3eee-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3eee-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3eee-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3eee-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a3eee-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3eee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3eee-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a3eee-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


---
description: 發生于滑鼠滾輪移動時，InkPicture 控制項有焦點時。
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: 'InkPicture. 滑鼠滾輪事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319420"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="41f9e-103">InkPicture. 滑鼠滾輪事件</span><span class="sxs-lookup"><span data-stu-id="41f9e-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="41f9e-104">發生于滑鼠滾輪移動時， [InkPicture](inkpicture-control-reference.md) 控制項有焦點時。</span><span class="sxs-lookup"><span data-stu-id="41f9e-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="41f9e-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="41f9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="41f9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f9e-107">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-108">已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="41f9e-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="41f9e-109">*Shift* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="41f9e-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="41f9e-111">*差異* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-112">滑鼠滾輪的距離。</span><span class="sxs-lookup"><span data-stu-id="41f9e-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="41f9e-113">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-114">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="41f9e-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="41f9e-115">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-116">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="41f9e-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="41f9e-117">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41f9e-118">VARIANT \_ TRUE 表示取消父控制項的 **滑鼠滾輪** 事件，否則為 variant \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="41f9e-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f9e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="41f9e-119">Return value</span></span>

<span data-ttu-id="41f9e-120">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41f9e-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f9e-121">備註</span><span class="sxs-lookup"><span data-stu-id="41f9e-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41f9e-122">參數 *x* 和 *y* 是以圖元為單位，而不是與筆墨空間座標系統相關聯的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="41f9e-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="41f9e-123">這是因為此事件會取代無法辨識的應用程式的相關滑鼠事件，而且該應用程式類型只會參考圖元。</span><span class="sxs-lookup"><span data-stu-id="41f9e-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="41f9e-124">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="41f9e-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="41f9e-125">**\_ IInkPictureEvents** 介面會以 DISPID IPEMouseWheel 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="41f9e-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f9e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="41f9e-126">Requirements</span></span>



| <span data-ttu-id="41f9e-127">需求</span><span class="sxs-lookup"><span data-stu-id="41f9e-127">Requirement</span></span> | <span data-ttu-id="41f9e-128">值</span><span class="sxs-lookup"><span data-stu-id="41f9e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f9e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41f9e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="41f9e-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41f9e-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="41f9e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41f9e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="41f9e-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="41f9e-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="41f9e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="41f9e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f9e-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="41f9e-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="41f9e-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="41f9e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="41f9e-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41f9e-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="41f9e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41f9e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f9e-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="41f9e-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


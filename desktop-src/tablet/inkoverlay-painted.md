---
description: 當 InkOverlay 物件或 InkPicture 控制項已完成重繪本身時發生。
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: 'InkOverlay：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469468"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="7cd29-103">InkOverlay. 繪製事件</span><span class="sxs-lookup"><span data-stu-id="7cd29-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="7cd29-104">當 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 控制項已完成重繪本身時發生。</span><span class="sxs-lookup"><span data-stu-id="7cd29-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd29-105">語法</span><span class="sxs-lookup"><span data-stu-id="7cd29-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="7cd29-106">參數</span><span class="sxs-lookup"><span data-stu-id="7cd29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd29-107">*hDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7cd29-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd29-108">發生事件的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="7cd29-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7cd29-109">*Rect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7cd29-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd29-110">重新繪製的 [**InkRectangle**](inkrectangle-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="7cd29-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd29-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cd29-111">Return value</span></span>

<span data-ttu-id="7cd29-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7cd29-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd29-113">備註</span><span class="sxs-lookup"><span data-stu-id="7cd29-113">Remarks</span></span>

<span data-ttu-id="7cd29-114">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEPainted 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="7cd29-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd29-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cd29-115">Requirements</span></span>



| <span data-ttu-id="7cd29-116">需求</span><span class="sxs-lookup"><span data-stu-id="7cd29-116">Requirement</span></span> | <span data-ttu-id="7cd29-117">值</span><span class="sxs-lookup"><span data-stu-id="7cd29-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd29-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cd29-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd29-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cd29-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7cd29-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cd29-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd29-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="7cd29-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7cd29-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7cd29-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd29-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7cd29-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7cd29-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7cd29-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cd29-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd29-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7cd29-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cd29-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd29-127">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="7cd29-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 





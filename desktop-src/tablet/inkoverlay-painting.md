---
description: 發生于 InkOverlay 物件或 InkPicture 完成重繪本身之前。
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: 'InkOverlay：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513929"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="a1b57-103">InkOverlay. 繪製事件</span><span class="sxs-lookup"><span data-stu-id="a1b57-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="a1b57-104">發生于 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 完成重繪本身之前。</span><span class="sxs-lookup"><span data-stu-id="a1b57-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b57-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1b57-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="a1b57-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1b57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b57-107">*hDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1b57-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b57-108">將在其上進行繪製的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="a1b57-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="a1b57-109">*Rect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1b57-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b57-110">要重新繪製的矩形。</span><span class="sxs-lookup"><span data-stu-id="a1b57-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="a1b57-111">*允許* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a1b57-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b57-112">是否會發生重新繪製。</span><span class="sxs-lookup"><span data-stu-id="a1b57-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b57-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1b57-113">Return value</span></span>

<span data-ttu-id="a1b57-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a1b57-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1b57-115">備註</span><span class="sxs-lookup"><span data-stu-id="a1b57-115">Remarks</span></span>

<span data-ttu-id="a1b57-116">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEPainting 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="a1b57-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b57-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1b57-117">Requirements</span></span>



| <span data-ttu-id="a1b57-118">需求</span><span class="sxs-lookup"><span data-stu-id="a1b57-118">Requirement</span></span> | <span data-ttu-id="a1b57-119">值</span><span class="sxs-lookup"><span data-stu-id="a1b57-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b57-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1b57-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b57-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1b57-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a1b57-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1b57-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b57-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="a1b57-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a1b57-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a1b57-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b57-125"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a1b57-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1b57-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1b57-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1b57-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b57-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a1b57-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1b57-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b57-129">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="a1b57-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 





---
description: 發生于 InkPicture 控制項自行重繪之前。
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: 'InkPicture：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193332"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="3334f-103">InkPicture。繪製事件</span><span class="sxs-lookup"><span data-stu-id="3334f-103">InkPicture.Painting event</span></span>

<span data-ttu-id="3334f-104">發生于 [InkPicture](inkpicture-control-reference.md) 控制項自行重繪之前。</span><span class="sxs-lookup"><span data-stu-id="3334f-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="3334f-105">語法</span><span class="sxs-lookup"><span data-stu-id="3334f-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="3334f-106">參數</span><span class="sxs-lookup"><span data-stu-id="3334f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3334f-107">*hDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3334f-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3334f-108">將在其上進行繪製的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="3334f-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="3334f-109">*Rect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3334f-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3334f-110">要重新繪製的筆墨矩形。</span><span class="sxs-lookup"><span data-stu-id="3334f-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="3334f-111">*允許* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3334f-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3334f-112">是否會發生重新繪製。</span><span class="sxs-lookup"><span data-stu-id="3334f-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3334f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3334f-113">Return value</span></span>

<span data-ttu-id="3334f-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3334f-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3334f-115">備註</span><span class="sxs-lookup"><span data-stu-id="3334f-115">Remarks</span></span>

<span data-ttu-id="3334f-116">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEPainting 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="3334f-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="3334f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3334f-117">Requirements</span></span>



| <span data-ttu-id="3334f-118">需求</span><span class="sxs-lookup"><span data-stu-id="3334f-118">Requirement</span></span> | <span data-ttu-id="3334f-119">值</span><span class="sxs-lookup"><span data-stu-id="3334f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3334f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3334f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3334f-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3334f-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3334f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3334f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3334f-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="3334f-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3334f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3334f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3334f-125"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3334f-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3334f-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3334f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3334f-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3334f-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3334f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3334f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3334f-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3334f-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 





---
description: InkPicture 控制項已完成重繪本身時發生。
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: 'InkPicture 繪製事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987001"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="3b59b-103">InkPicture 繪製事件</span><span class="sxs-lookup"><span data-stu-id="3b59b-103">InkPicture.Painted event</span></span>

<span data-ttu-id="3b59b-104">[InkPicture](inkpicture-control-reference.md)控制項已完成重繪本身時發生。</span><span class="sxs-lookup"><span data-stu-id="3b59b-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b59b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b59b-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="3b59b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b59b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b59b-107">*hDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b59b-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b59b-108">發生事件的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="3b59b-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3b59b-109">*Rect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b59b-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b59b-110">重新繪製的 [**InkRectangle**](inkrectangle-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="3b59b-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b59b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b59b-111">Return value</span></span>

<span data-ttu-id="3b59b-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b59b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b59b-113">備註</span><span class="sxs-lookup"><span data-stu-id="3b59b-113">Remarks</span></span>

<span data-ttu-id="3b59b-114">此事件方法是在識別碼為 DISPID IOEPainted 的 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分配介面中定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3b59b-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b59b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b59b-115">Requirements</span></span>



| <span data-ttu-id="3b59b-116">需求</span><span class="sxs-lookup"><span data-stu-id="3b59b-116">Requirement</span></span> | <span data-ttu-id="3b59b-117">值</span><span class="sxs-lookup"><span data-stu-id="3b59b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b59b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b59b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b59b-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b59b-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3b59b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b59b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b59b-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="3b59b-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3b59b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3b59b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b59b-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3b59b-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3b59b-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b59b-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b59b-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b59b-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3b59b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b59b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b59b-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3b59b-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 





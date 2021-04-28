---
description: DoubleClick 事件-當 InkCollector 或 InkOverlay 物件按兩下時，就會發生此事件。
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: 'DoubleClick 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086826"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="077d3-103">DoubleClick 事件</span><span class="sxs-lookup"><span data-stu-id="077d3-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="077d3-104">當按兩下 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="077d3-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="077d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="077d3-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="077d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="077d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077d3-107">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="077d3-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="077d3-108">是否應該取消父控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="077d3-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077d3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="077d3-109">Return value</span></span>

<span data-ttu-id="077d3-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="077d3-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="077d3-111">備註</span><span class="sxs-lookup"><span data-stu-id="077d3-111">Remarks</span></span>

<span data-ttu-id="077d3-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEDblClick 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="077d3-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="077d3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="077d3-113">Requirements</span></span>



| <span data-ttu-id="077d3-114">需求</span><span class="sxs-lookup"><span data-stu-id="077d3-114">Requirement</span></span> | <span data-ttu-id="077d3-115">值</span><span class="sxs-lookup"><span data-stu-id="077d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="077d3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="077d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="077d3-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="077d3-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="077d3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="077d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="077d3-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="077d3-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="077d3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="077d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="077d3-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="077d3-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="077d3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="077d3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="077d3-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="077d3-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="077d3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="077d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077d3-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="077d3-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 





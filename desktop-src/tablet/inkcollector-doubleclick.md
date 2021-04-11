---
description: 當按兩下 InkCollector 或 InkOverlay 物件時發生。
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: 'InkCollector. DoubleClick 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847779"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="554e1-103">InkCollector. DoubleClick 事件</span><span class="sxs-lookup"><span data-stu-id="554e1-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="554e1-104">當按兩下 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="554e1-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="554e1-105">語法</span><span class="sxs-lookup"><span data-stu-id="554e1-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="554e1-106">參數</span><span class="sxs-lookup"><span data-stu-id="554e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554e1-107">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="554e1-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="554e1-108">**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="554e1-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="554e1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="554e1-109">Return value</span></span>

<span data-ttu-id="554e1-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="554e1-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="554e1-111">備註</span><span class="sxs-lookup"><span data-stu-id="554e1-111">Remarks</span></span>

<span data-ttu-id="554e1-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEDblClick 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="554e1-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="554e1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="554e1-113">Requirements</span></span>



| <span data-ttu-id="554e1-114">需求</span><span class="sxs-lookup"><span data-stu-id="554e1-114">Requirement</span></span> | <span data-ttu-id="554e1-115">值</span><span class="sxs-lookup"><span data-stu-id="554e1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="554e1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="554e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="554e1-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="554e1-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="554e1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="554e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="554e1-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="554e1-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="554e1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="554e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="554e1-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="554e1-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="554e1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="554e1-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="554e1-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="554e1-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="554e1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="554e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554e1-125">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="554e1-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 





---
description: IInkTablet 新增至系統時發生。
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: 'InkCollector. TabletAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943254"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="b9814-103">InkCollector. TabletAdded 事件</span><span class="sxs-lookup"><span data-stu-id="b9814-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="b9814-104">[**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)新增至系統時發生。</span><span class="sxs-lookup"><span data-stu-id="b9814-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9814-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9814-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="b9814-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9814-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9814-107">*平板* \[ 電腦在\]</span><span class="sxs-lookup"><span data-stu-id="b9814-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9814-108">已新增至系統的 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件。</span><span class="sxs-lookup"><span data-stu-id="b9814-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9814-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9814-109">Return value</span></span>

<span data-ttu-id="b9814-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b9814-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9814-111">備註</span><span class="sxs-lookup"><span data-stu-id="b9814-111">Remarks</span></span>

<span data-ttu-id="b9814-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICETabletAdded 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="b9814-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9814-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9814-113">Requirements</span></span>



| <span data-ttu-id="b9814-114">需求</span><span class="sxs-lookup"><span data-stu-id="b9814-114">Requirement</span></span> | <span data-ttu-id="b9814-115">值</span><span class="sxs-lookup"><span data-stu-id="b9814-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9814-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9814-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b9814-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9814-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b9814-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9814-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b9814-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="b9814-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b9814-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b9814-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9814-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b9814-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b9814-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9814-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9814-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9814-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b9814-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9814-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9814-125">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="b9814-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b9814-126">**IInkTablet 介面**</span><span class="sxs-lookup"><span data-stu-id="b9814-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





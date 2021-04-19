---
description: 從系統移除 IInkTablet 時發生。
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: 'InkCollector. TabletRemoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec723a6752f79a1a1d56d318d49ec3d025919d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972205"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="2ce27-103">InkCollector. TabletRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="2ce27-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="2ce27-104">從系統移除 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 時發生。</span><span class="sxs-lookup"><span data-stu-id="2ce27-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce27-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ce27-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="2ce27-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ce27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce27-107">*TabletId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ce27-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce27-108">用來當做已移除 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件之識別碼的完整值。</span><span class="sxs-lookup"><span data-stu-id="2ce27-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce27-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ce27-109">Return value</span></span>

<span data-ttu-id="2ce27-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2ce27-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce27-111">備註</span><span class="sxs-lookup"><span data-stu-id="2ce27-111">Remarks</span></span>

<span data-ttu-id="2ce27-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICETabletRemoved 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="2ce27-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce27-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ce27-113">Requirements</span></span>



| <span data-ttu-id="2ce27-114">需求</span><span class="sxs-lookup"><span data-stu-id="2ce27-114">Requirement</span></span> | <span data-ttu-id="2ce27-115">值</span><span class="sxs-lookup"><span data-stu-id="2ce27-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce27-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ce27-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce27-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ce27-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2ce27-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ce27-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce27-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="2ce27-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2ce27-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2ce27-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ce27-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2ce27-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2ce27-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ce27-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ce27-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce27-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2ce27-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ce27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce27-125">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="2ce27-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="2ce27-126">**IInkTablet 介面**</span><span class="sxs-lookup"><span data-stu-id="2ce27-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





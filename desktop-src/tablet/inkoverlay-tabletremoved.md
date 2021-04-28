---
description: TabletRemoved 事件-當 IInkTablet 從系統移除時，就會發生此事件。
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: 'TabletRemoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5572ec4c8afd664ef96534e93c402ec2141f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086646"
---
# <a name="inkoverlaytabletremoved-event"></a><span data-ttu-id="8cc6c-103">TabletRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="8cc6c-103">InkOverlay.TabletRemoved event</span></span>

<span data-ttu-id="8cc6c-104">從系統移除 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 時發生。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8cc6c-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="8cc6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cc6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc6c-107">*TabletId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cc6c-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc6c-108">用來當做已移除 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件之識別碼的完整值。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc6c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cc6c-109">Return value</span></span>

<span data-ttu-id="8cc6c-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc6c-111">備註</span><span class="sxs-lookup"><span data-stu-id="8cc6c-111">Remarks</span></span>

<span data-ttu-id="8cc6c-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICETabletRemoved 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc6c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cc6c-113">Requirements</span></span>



| <span data-ttu-id="8cc6c-114">需求</span><span class="sxs-lookup"><span data-stu-id="8cc6c-114">Requirement</span></span> | <span data-ttu-id="8cc6c-115">值</span><span class="sxs-lookup"><span data-stu-id="8cc6c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc6c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8cc6c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc6c-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cc6c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8cc6c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8cc6c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc6c-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="8cc6c-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8cc6c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8cc6c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc6c-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8cc6c-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cc6c-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="8cc6c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8cc6c-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cc6c-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8cc6c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cc6c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc6c-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="8cc6c-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8cc6c-126">**IInkTablet 介面**</span><span class="sxs-lookup"><span data-stu-id="8cc6c-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





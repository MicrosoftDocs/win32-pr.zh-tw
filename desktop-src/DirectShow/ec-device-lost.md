---
description: 隨插即用裝置已移除或變成可供使用。
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: 'EC_DEVICE_LOST (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996228"
---
# <a name="ec_device_lost"></a><span data-ttu-id="3fd3d-103">EC \_ 裝置 \_ 遺失</span><span class="sxs-lookup"><span data-stu-id="3fd3d-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="3fd3d-104">隨插即用裝置已移除或變成可供使用。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fd3d-105">參數</span><span class="sxs-lookup"><span data-stu-id="3fd3d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd3d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3fd3d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3fd3d-107"> (**iunknown** \*) 指標指向代表裝置之篩選的 **iunknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="3fd3d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3fd3d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3fd3d-109">如果裝置已移除，則為零; 如果裝置再次可用，則為1。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="3fd3d-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="3fd3d-110">Default Action</span></span>

<span data-ttu-id="3fd3d-111">無。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd3d-112">備註</span><span class="sxs-lookup"><span data-stu-id="3fd3d-112">Remarks</span></span>

<span data-ttu-id="3fd3d-113">當裝置再次變成可用時，裝置篩選器的先前狀態將不再有效。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="3fd3d-114">應用程式必須重建圖形，才能使用裝置。</span><span class="sxs-lookup"><span data-stu-id="3fd3d-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd3d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fd3d-115">Requirements</span></span>



| <span data-ttu-id="3fd3d-116">需求</span><span class="sxs-lookup"><span data-stu-id="3fd3d-116">Requirement</span></span> | <span data-ttu-id="3fd3d-117">值</span><span class="sxs-lookup"><span data-stu-id="3fd3d-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd3d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3fd3d-118">Header</span></span><br/> | <dl> <span data-ttu-id="3fd3d-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd3d-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd3d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fd3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd3d-121">裝置移除通知</span><span class="sxs-lookup"><span data-stu-id="3fd3d-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="3fd3d-122">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="3fd3d-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3fd3d-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="3fd3d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





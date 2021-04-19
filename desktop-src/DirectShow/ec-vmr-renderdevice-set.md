---
description: VMR 已選取其轉譯機制時傳送。
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: 'EC_VMR_RENDERDEVICE_SET (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977573"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="1cbf0-103">EC \_ VMR \_ RENDERDEVICE \_ 集</span><span class="sxs-lookup"><span data-stu-id="1cbf0-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="1cbf0-104">VMR 已選取其轉譯機制時傳送。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cbf0-105">參數</span><span class="sxs-lookup"><span data-stu-id="1cbf0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbf0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1cbf0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1cbf0-107">可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1cbf0-107">May be one of the following values:</span></span>



| <span data-ttu-id="1cbf0-108">值</span><span class="sxs-lookup"><span data-stu-id="1cbf0-108">Value</span></span>                        | <span data-ttu-id="1cbf0-109">意義</span><span class="sxs-lookup"><span data-stu-id="1cbf0-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="1cbf0-110">VMR 轉譯裝置重迭 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cbf0-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="1cbf0-111">VMR 只會轉譯成重迭表面 (VMR-7) 。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="1cbf0-112">VMR \_ 轉譯 \_ 裝置 \_ VIDMEM</span><span class="sxs-lookup"><span data-stu-id="1cbf0-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="1cbf0-113">VMR 會轉譯成視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="1cbf0-114">VMR \_ 轉譯 \_ 裝置 \_ SYSMEM</span><span class="sxs-lookup"><span data-stu-id="1cbf0-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="1cbf0-115">VMR 只會轉譯為系統記憶體 (VMR-7) 。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="1cbf0-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1cbf0-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1cbf0-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cbf0-118">備註</span><span class="sxs-lookup"><span data-stu-id="1cbf0-118">Remarks</span></span>

<span data-ttu-id="1cbf0-119">此事件是由 VMR-7 和 VMR-9 所傳送，而且會轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="1cbf0-120">請注意，VMR-9 僅支援視訊記憶體呈現目標。</span><span class="sxs-lookup"><span data-stu-id="1cbf0-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbf0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cbf0-121">Requirements</span></span>



| <span data-ttu-id="1cbf0-122">需求</span><span class="sxs-lookup"><span data-stu-id="1cbf0-122">Requirement</span></span> | <span data-ttu-id="1cbf0-123">值</span><span class="sxs-lookup"><span data-stu-id="1cbf0-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbf0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1cbf0-124">Header</span></span><br/> | <dl> <span data-ttu-id="1cbf0-125"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf0-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbf0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cbf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbf0-127">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="1cbf0-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1cbf0-128">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="1cbf0-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





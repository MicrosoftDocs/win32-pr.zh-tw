---
description: 表示元件花費在處理每個樣本的時間量。
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: 'EC_PROCESSING_LATENCY (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999074"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="1fe9b-103">EC \_ 處理 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="1fe9b-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="1fe9b-104">表示元件花費在處理每個樣本的時間量。</span><span class="sxs-lookup"><span data-stu-id="1fe9b-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fe9b-105">參數</span><span class="sxs-lookup"><span data-stu-id="1fe9b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe9b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1fe9b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1fe9b-107"> (**CONST 參考 \_ 時間** \*) 處理每個樣本的時間量，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="1fe9b-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1fe9b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1fe9b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1fe9b-109">零個。</span><span class="sxs-lookup"><span data-stu-id="1fe9b-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="1fe9b-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="1fe9b-110">Default Action</span></span>

<span data-ttu-id="1fe9b-111">無。</span><span class="sxs-lookup"><span data-stu-id="1fe9b-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe9b-112">備註</span><span class="sxs-lookup"><span data-stu-id="1fe9b-112">Remarks</span></span>

<span data-ttu-id="1fe9b-113">[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的簡報者 (EVR) 篩選器可以將此訊息傳送至 EVR，以通知 EVR 有關展示者的處理延遲。</span><span class="sxs-lookup"><span data-stu-id="1fe9b-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe9b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fe9b-114">Requirements</span></span>



| <span data-ttu-id="1fe9b-115">需求</span><span class="sxs-lookup"><span data-stu-id="1fe9b-115">Requirement</span></span> | <span data-ttu-id="1fe9b-116">值</span><span class="sxs-lookup"><span data-stu-id="1fe9b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe9b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1fe9b-117">Header</span></span><br/> | <dl> <span data-ttu-id="1fe9b-118"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe9b-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fe9b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fe9b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe9b-120">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="1fe9b-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1fe9b-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="1fe9b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: 資料流程控制停止命令已生效。
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: 'EC_STREAM_CONTROL_STOPPED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000771"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="eaa13-103">EC \_ 資料流程 \_ 控制 \_ 已停止</span><span class="sxs-lookup"><span data-stu-id="eaa13-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="eaa13-104">資料流程控制停止命令已生效。</span><span class="sxs-lookup"><span data-stu-id="eaa13-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaa13-105">參數</span><span class="sxs-lookup"><span data-stu-id="eaa13-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa13-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="eaa13-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="eaa13-107"> (**IUnknown** \*) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標，指向停止資料流程的 pin。</span><span class="sxs-lookup"><span data-stu-id="eaa13-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="eaa13-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="eaa13-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="eaa13-109"> (**DWORD**) 使用者定義值。</span><span class="sxs-lookup"><span data-stu-id="eaa13-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="eaa13-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="eaa13-110">Default Action</span></span>

<span data-ttu-id="eaa13-111">無。</span><span class="sxs-lookup"><span data-stu-id="eaa13-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa13-112">備註</span><span class="sxs-lookup"><span data-stu-id="eaa13-112">Remarks</span></span>

<span data-ttu-id="eaa13-113">篩選準則會傳送此事件以回應 [**IAMStreamControl：： StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 方法。</span><span class="sxs-lookup"><span data-stu-id="eaa13-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="eaa13-114">**StopAt** 方法會指定 pin 的參考時間以停止串流。</span><span class="sxs-lookup"><span data-stu-id="eaa13-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="eaa13-115">當串流處理中斷時，篩選會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="eaa13-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="eaa13-116">*PSender* 參數會指定執行 stop 命令的 pin。</span><span class="sxs-lookup"><span data-stu-id="eaa13-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="eaa13-117">根據執行方式而定，它可能不是收到 [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 呼叫的 pin。</span><span class="sxs-lookup"><span data-stu-id="eaa13-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="eaa13-118">*DwCookie* 參數是由應用程式在 [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)方法中指定。</span><span class="sxs-lookup"><span data-stu-id="eaa13-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="eaa13-119">此參數可讓應用程式追蹤對方法的多個呼叫。</span><span class="sxs-lookup"><span data-stu-id="eaa13-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa13-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaa13-120">Requirements</span></span>



| <span data-ttu-id="eaa13-121">需求</span><span class="sxs-lookup"><span data-stu-id="eaa13-121">Requirement</span></span> | <span data-ttu-id="eaa13-122">值</span><span class="sxs-lookup"><span data-stu-id="eaa13-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa13-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eaa13-123">Header</span></span><br/> | <dl> <span data-ttu-id="eaa13-124"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa13-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaa13-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaa13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa13-126">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="eaa13-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="eaa13-127">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="eaa13-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





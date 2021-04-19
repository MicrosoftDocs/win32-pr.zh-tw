---
description: 資料流程控制項啟動命令已生效。
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: 'EC_STREAM_CONTROL_STARTED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990558"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="8f771-103">\_已開始使用 EC 資料流程 \_ 控制項 \_</span><span class="sxs-lookup"><span data-stu-id="8f771-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="8f771-104">資料流程控制項啟動命令已生效。</span><span class="sxs-lookup"><span data-stu-id="8f771-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f771-105">參數</span><span class="sxs-lookup"><span data-stu-id="8f771-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f771-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="8f771-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="8f771-107"> (**IUnknown** \*) 指標指向啟動資料流程的 pin [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面。</span><span class="sxs-lookup"><span data-stu-id="8f771-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="8f771-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="8f771-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="8f771-109"> (**DWORD**) 使用者定義值。</span><span class="sxs-lookup"><span data-stu-id="8f771-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8f771-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="8f771-110">Default Action</span></span>

<span data-ttu-id="8f771-111">無。</span><span class="sxs-lookup"><span data-stu-id="8f771-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f771-112">備註</span><span class="sxs-lookup"><span data-stu-id="8f771-112">Remarks</span></span>

<span data-ttu-id="8f771-113">篩選準則會傳送此事件以回應 [**IAMStreamControl：： StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 方法。</span><span class="sxs-lookup"><span data-stu-id="8f771-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="8f771-114">這個方法會指定 pin 開始串流的參考時間。</span><span class="sxs-lookup"><span data-stu-id="8f771-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="8f771-115">串流處理開始時，篩選準則會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="8f771-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="8f771-116">*PSender* 參數會指定執行 start 命令的 pin。</span><span class="sxs-lookup"><span data-stu-id="8f771-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="8f771-117">根據執行方式而定，它可能不是收到 [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 呼叫的 pin。</span><span class="sxs-lookup"><span data-stu-id="8f771-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="8f771-118">*DwCookie* 參數是由應用程式在 [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)方法中指定。</span><span class="sxs-lookup"><span data-stu-id="8f771-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="8f771-119">此參數可讓應用程式追蹤對方法的多個呼叫。</span><span class="sxs-lookup"><span data-stu-id="8f771-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f771-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f771-120">Requirements</span></span>



| <span data-ttu-id="8f771-121">需求</span><span class="sxs-lookup"><span data-stu-id="8f771-121">Requirement</span></span> | <span data-ttu-id="8f771-122">值</span><span class="sxs-lookup"><span data-stu-id="8f771-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f771-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8f771-123">Header</span></span><br/> | <dl> <span data-ttu-id="8f771-124"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f771-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f771-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f771-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f771-126">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="8f771-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8f771-127">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="8f771-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: 使用一組受限制的查詢來起始與事件提供者的通訊。
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: 'IWbemEventSink 介面 (Wbemprov .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996886"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="41e14-103">IWbemEventSink 介面</span><span class="sxs-lookup"><span data-stu-id="41e14-103">IWbemEventSink interface</span></span>

<span data-ttu-id="41e14-104">**IWbemEventSink** 介面會使用一組受限制的查詢來起始與事件提供者的通訊。</span><span class="sxs-lookup"><span data-stu-id="41e14-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="41e14-105">這個介面會擴充 [**IWbemObjectSink**](iwbemobjectsink.md)，提供處理安全性和效能的新方法。</span><span class="sxs-lookup"><span data-stu-id="41e14-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="41e14-106">如需使用此介面的詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md) 和 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="41e14-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="41e14-107">成員</span><span class="sxs-lookup"><span data-stu-id="41e14-107">Members</span></span>

<span data-ttu-id="41e14-108">**IWbemEventSink** 介面具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41e14-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="41e14-109">方法</span><span class="sxs-lookup"><span data-stu-id="41e14-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="41e14-110">方法</span><span class="sxs-lookup"><span data-stu-id="41e14-110">Methods</span></span>

<span data-ttu-id="41e14-111">**IWbemEventSink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="41e14-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="41e14-112">方法</span><span class="sxs-lookup"><span data-stu-id="41e14-112">Method</span></span>                                                                | <span data-ttu-id="41e14-113">描述</span><span class="sxs-lookup"><span data-stu-id="41e14-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="41e14-114">**GetRestrictedSink**</span><span class="sxs-lookup"><span data-stu-id="41e14-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="41e14-115">由取用者呼叫以設定受限制的事件查詢。</span><span class="sxs-lookup"><span data-stu-id="41e14-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="41e14-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="41e14-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="41e14-117">檢查事件接收的狀態。</span><span class="sxs-lookup"><span data-stu-id="41e14-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="41e14-118">**SetBatchingParameters**</span><span class="sxs-lookup"><span data-stu-id="41e14-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="41e14-119">由取用者呼叫以設定批次參數。</span><span class="sxs-lookup"><span data-stu-id="41e14-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="41e14-120">**SetSinkSecurity**</span><span class="sxs-lookup"><span data-stu-id="41e14-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="41e14-121">用來更新事件接收上的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="41e14-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="41e14-122">備註</span><span class="sxs-lookup"><span data-stu-id="41e14-122">Remarks</span></span>

<span data-ttu-id="41e14-123">當 ([**IWbemObjectSink**](iwbemobjectsink.md) 或 **IWbemEventSink**) 執行事件訂閱接收時，請勿從接收器物件的方法內呼叫 WMI。</span><span class="sxs-lookup"><span data-stu-id="41e14-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="41e14-124">例如，呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ，以在 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 的實中取消接收，可能會干擾 WMI 狀態。</span><span class="sxs-lookup"><span data-stu-id="41e14-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="41e14-125">若要取消事件訂閱，請設定旗標，並從另一個執行緒或物件呼叫 **IWbemServices：： CancelAsyncCall** 。</span><span class="sxs-lookup"><span data-stu-id="41e14-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="41e14-126">對於與事件接收無關的執行（例如物件、列舉和查詢查詢），您可以回呼 WMI。</span><span class="sxs-lookup"><span data-stu-id="41e14-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="41e14-127">接收程式應在100毫秒內處理事件通知，因為傳遞事件通知的 WMI 執行緒無法執行其他工作，直到接收物件處理完成為止。</span><span class="sxs-lookup"><span data-stu-id="41e14-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="41e14-128">如果通知需要大量處理，接收端可以使用另一個執行緒的內部佇列來處理處理。</span><span class="sxs-lookup"><span data-stu-id="41e14-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e14-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="41e14-129">Requirements</span></span>



| <span data-ttu-id="41e14-130">需求</span><span class="sxs-lookup"><span data-stu-id="41e14-130">Requirement</span></span> | <span data-ttu-id="41e14-131">值</span><span class="sxs-lookup"><span data-stu-id="41e14-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e14-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41e14-132">Minimum supported client</span></span><br/> | <span data-ttu-id="41e14-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41e14-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="41e14-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41e14-134">Minimum supported server</span></span><br/> | <span data-ttu-id="41e14-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41e14-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="41e14-136">標頭</span><span class="sxs-lookup"><span data-stu-id="41e14-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e14-137"><dt>Wbemprov (包含 Wbemidl) </dt></span><span class="sxs-lookup"><span data-stu-id="41e14-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="41e14-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="41e14-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="41e14-139"><dt>Wbemuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41e14-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="41e14-140">DLL</span><span class="sxs-lookup"><span data-stu-id="41e14-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e14-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41e14-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="41e14-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41e14-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e14-143">適用于 WMI 的 COM API</span><span class="sxs-lookup"><span data-stu-id="41e14-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 





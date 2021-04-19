---
description: ITParticipantEvent 介面包含可取得參與者事件描述的方法。
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: 'ITParticipantEvent 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000828"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="2ac5a-103">ITParticipantEvent 介面</span><span class="sxs-lookup"><span data-stu-id="2ac5a-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="2ac5a-104">\[**ITParticipantEvent** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ac5a-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2ac5a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ac5a-106">**ITParticipantEvent** 介面包含可取得參與者事件描述的方法。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="2ac5a-107">當應用程式的 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)方法的實，指出 [**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)等於 **TE \_ 私** 用時，方法的 *pEvent* 參數就是 **ITParticipantEvent** 介面的 **IDispatch** 指標。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="2ac5a-108">這個介面的方法可以用來取得發生之參與者變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="2ac5a-109">您必須呼叫 [**ITTAPI：:p 的 \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，並設定包含 **TE \_ 私** 用事件的事件篩選遮罩，以啟用參與者事件的接收。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="2ac5a-110">如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="2ac5a-111">如需詳細資訊，請參閱 [事件](events.md) 總覽。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="2ac5a-112">成員</span><span class="sxs-lookup"><span data-stu-id="2ac5a-112">Members</span></span>

<span data-ttu-id="2ac5a-113">**ITParticipantEvent** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2ac5a-114">**ITParticipantEvent** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2ac5a-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="2ac5a-115">方法</span><span class="sxs-lookup"><span data-stu-id="2ac5a-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ac5a-116">方法</span><span class="sxs-lookup"><span data-stu-id="2ac5a-116">Methods</span></span>

<span data-ttu-id="2ac5a-117">**ITParticipantEvent** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="2ac5a-118">方法</span><span class="sxs-lookup"><span data-stu-id="2ac5a-118">Method</span></span>                                                         | <span data-ttu-id="2ac5a-119">描述</span><span class="sxs-lookup"><span data-stu-id="2ac5a-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ac5a-120">**取得 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="2ac5a-121">取得事件的 [**參與者 \_ 事件**](participant-event.md) 描述元。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="2ac5a-122">**取得 \_ 參與者**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="2ac5a-123">取得 [**ITParticipant**](itparticipant.md) 介面陣列的指標，代表牽涉到事件的參與者。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="2ac5a-124">**取得子 \_ 流**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="2ac5a-125">取得 [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) 介面陣列的指標，代表涉及事件的子串流。</span><span class="sxs-lookup"><span data-stu-id="2ac5a-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="2ac5a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ac5a-126">Requirements</span></span>



| <span data-ttu-id="2ac5a-127">需求</span><span class="sxs-lookup"><span data-stu-id="2ac5a-127">Requirement</span></span> | <span data-ttu-id="2ac5a-128">值</span><span class="sxs-lookup"><span data-stu-id="2ac5a-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac5a-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2ac5a-129">TAPI version</span></span><br/> | <span data-ttu-id="2ac5a-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2ac5a-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2ac5a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2ac5a-131">Header</span></span><br/>       | <dl> <span data-ttu-id="2ac5a-132"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac5a-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2ac5a-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ac5a-133">Library</span></span><br/>      | <dl> <span data-ttu-id="2ac5a-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="2ac5a-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2ac5a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2ac5a-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ac5a-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ac5a-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2ac5a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ac5a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac5a-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="2ac5a-139">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="2ac5a-140">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="2ac5a-141">**參與者 \_ 活動**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="2ac5a-142">**ITTAPIEventNotification：： Event**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="2ac5a-143">**TAPI \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="2ac5a-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="2ac5a-144">註冊事件程式碼片段</span><span class="sxs-lookup"><span data-stu-id="2ac5a-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 


---
title: 錯誤
description: 錯誤訊息是用來傳達有關遠端端點失敗的錯誤資訊。
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- 適用于 Windows 的 Web 服務錯誤
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966787"
---
# <a name="faults"></a><span data-ttu-id="0cffd-106">錯誤</span><span class="sxs-lookup"><span data-stu-id="0cffd-106">Faults</span></span>

<span data-ttu-id="0cffd-107">錯誤訊息是用來傳達有關遠端端點失敗的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="0cffd-107">A fault message is used to communicate error information about a failure at a remote endpoint.</span></span> <span data-ttu-id="0cffd-108">錯誤訊息就像任何其他訊息，但訊息本文的格式有標準格式。</span><span class="sxs-lookup"><span data-stu-id="0cffd-108">A fault message is like any other message, except the format of the message body has a standard format.</span></span> <span data-ttu-id="0cffd-109">基礎結構通訊協定（例如 WS-ADDRESSING）以及較高層級的應用程式協定都可以使用錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-109">Faults can be used both by infrastructure protocols, such as WS-Addressing, and by higher-level application protocols.</span></span>

-   [<span data-ttu-id="0cffd-110">概觀</span><span class="sxs-lookup"><span data-stu-id="0cffd-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="0cffd-111">在服務中產生錯誤</span><span class="sxs-lookup"><span data-stu-id="0cffd-111">Generating faults in a Service</span></span>](#generating-faults-in-a-service)
-   [<span data-ttu-id="0cffd-112">處理用戶端上的錯誤</span><span class="sxs-lookup"><span data-stu-id="0cffd-112">Handling faults on a client</span></span>](#handling-faults-on-a-client)
-   [<span data-ttu-id="0cffd-113">使用錯誤與訊息</span><span class="sxs-lookup"><span data-stu-id="0cffd-113">Using faults with messages</span></span>](#using-faults-with-messages)

## <a name="overview"></a><span data-ttu-id="0cffd-114">概觀</span><span class="sxs-lookup"><span data-stu-id="0cffd-114">Overview</span></span>

<span data-ttu-id="0cffd-115">錯誤訊息主體的內容會使用 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構在此 API 中表示。</span><span class="sxs-lookup"><span data-stu-id="0cffd-115">The contents of the body of a fault message is represented in this API using the [**WS\_FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) structure.</span></span> <span data-ttu-id="0cffd-116">雖然錯誤有一組固定的欄位，可用來提供有關失敗的資訊 (例如識別錯誤類型的 [**ws \_ \_ 錯誤碼**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) ，以及包含描述錯誤) 之文字的 [**ws \_ 錯誤 \_ 原因**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) ，它也會包含一個詳細資料欄位，可用來指定與錯誤相關的任意 XML 內容。</span><span class="sxs-lookup"><span data-stu-id="0cffd-116">Although a fault has a fixed set of fields used to providing information about the failure (like the [**WS\_FAULT\_CODE**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) that identifies the type of fault, and the [**WS\_FAULT\_REASON**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) that contains text describing the fault), it also contains a detail field that can be used to specify arbitrary XML content relating to the fault.</span></span>

## <a name="generating-faults-in-a-service"></a><span data-ttu-id="0cffd-117">在服務中產生錯誤</span><span class="sxs-lookup"><span data-stu-id="0cffd-117">Generating faults in a Service</span></span>

<span data-ttu-id="0cffd-118">服務通常會因為處理要求時發生一些錯誤而傳送錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-118">A service will typically send a fault due to some error that was encountered while processing the request.</span></span> <span data-ttu-id="0cffd-119">此 API 所使用的模型是服務中遇到處理錯誤的程式碼將會在 [WS \_ error](ws-error.md) 物件中捕捉必要的錯誤資訊，然後在呼叫鏈中較高層級的程式碼將會使用在較低層所捕捉的資訊來傳送錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-119">The model used by this API is that the code in the service that encounters the processing error will capture the necessary fault information in the [WS\_ERROR](ws-error.md) object, and then code at a higher level in the call chain will actually send the fault using the information captured at the lower layer.</span></span> <span data-ttu-id="0cffd-120">此配置可讓傳送錯誤的程式碼與錯誤狀況對應至錯誤的方式隔離，同時仍然允許傳送豐富的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="0cffd-120">This scheme allows the code that sends the fault to be insulated from how errors situations are mapped to faults while still allowing for rich fault information to be sent.</span></span>

<span data-ttu-id="0cffd-121">下列屬性可以與 [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) 搭配使用，以捕獲 [WS \_ ERROR](ws-error.md) 物件的錯誤資訊：</span><span class="sxs-lookup"><span data-stu-id="0cffd-121">The following properties can be used with [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) to capture fault information for a [WS\_ERROR](ws-error.md) object:</span></span>

-   <span data-ttu-id="0cffd-122">[**WS \_錯誤 \_ 的 \_ 屬性 \_ 動作**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。</span><span class="sxs-lookup"><span data-stu-id="0cffd-122">[**WS\_FAULT\_ERROR\_PROPERTY\_ACTION**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id).</span></span> <span data-ttu-id="0cffd-123">這會指定要用於錯誤訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="0cffd-123">This specifies the action to use for the fault message.</span></span> <span data-ttu-id="0cffd-124">如果未指定此值，則會提供預設動作。</span><span class="sxs-lookup"><span data-stu-id="0cffd-124">If this is not specified, then a default action is supplied.</span></span>
-   <span data-ttu-id="0cffd-125">[**WS \_錯誤 \_ \_ 屬性 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-125">[**WS\_FAULT\_ERROR\_PROPERTY\_FAULT**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id).</span></span> <span data-ttu-id="0cffd-126">這包含在錯誤訊息主體中傳送的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構。</span><span class="sxs-lookup"><span data-stu-id="0cffd-126">This contains the [**WS\_FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) structure that is sent in the body of the fault message.</span></span>
-   <span data-ttu-id="0cffd-127">[**WS \_錯誤 \_ 的 \_ 屬性 \_ 標頭**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。</span><span class="sxs-lookup"><span data-stu-id="0cffd-127">[**WS\_FAULT\_ERROR\_PROPERTY\_HEADER**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id).</span></span> <span data-ttu-id="0cffd-128">某些錯誤包含訊息標頭，這些訊息標頭會新增至錯誤訊息，以傳達與要求訊息標頭相關的處理失敗。</span><span class="sxs-lookup"><span data-stu-id="0cffd-128">Some faults include message headers which are added to the fault message to convey processing failures relating to headers of the request message.</span></span> <span data-ttu-id="0cffd-129">這個屬性可以用來指定包含要加入錯誤訊息之標頭的 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md) 。</span><span class="sxs-lookup"><span data-stu-id="0cffd-129">This property can be used to specify a [WS\_XML\_BUFFER](ws-xml-buffer.md) containing a header to be added to the fault message.</span></span>

<span data-ttu-id="0cffd-130">任何新增至 [WS \_ error](ws-error.md) 物件的錯誤字串，都會當做傳送的錯誤中的文字使用。</span><span class="sxs-lookup"><span data-stu-id="0cffd-130">Any error strings that are added to the [WS\_ERROR](ws-error.md) object are used as the text in the fault that is sent.</span></span> <span data-ttu-id="0cffd-131">您可以使用 [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)將錯誤字串新增至 error 物件。</span><span class="sxs-lookup"><span data-stu-id="0cffd-131">Error strings can be added to the error object using [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).</span></span>

<span data-ttu-id="0cffd-132">[**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)函數可以用來設定 [WS \_ ERROR](ws-error.md)物件的這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0cffd-132">The [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) function can be used to set these properties of the [WS\_ERROR](ws-error.md) object.</span></span>

<span data-ttu-id="0cffd-133">若要設定 [WS \_ ERROR](ws-error.md) 物件中儲存之錯誤的詳細資料，請使用 [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) 函數。</span><span class="sxs-lookup"><span data-stu-id="0cffd-133">To set the detail of the fault stored in the [WS\_ERROR](ws-error.md) object, use the [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) function.</span></span> <span data-ttu-id="0cffd-134">您可以使用此函式將任意 XML 內容與錯誤相關聯。</span><span class="sxs-lookup"><span data-stu-id="0cffd-134">This function can be used to associate arbitrary XML content with the fault.</span></span>

<span data-ttu-id="0cffd-135">[服務主機](service-host.md)會使用[WS \_ ERROR](ws-error.md)物件中的上述資訊自動傳送錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-135">The [Service Host](service-host.md) will automatically send faults by using the above information in the [WS\_ERROR](ws-error.md) object.</span></span> <span data-ttu-id="0cffd-136">[**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)屬性可用來控制將如何傳送錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0cffd-136">The [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property can be used to control how detailed of a fault will be sent.</span></span>

<span data-ttu-id="0cffd-137">如果在通道層處理，則可以使用 [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)傳送 [WS \_ ERROR](ws-error.md)物件的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-137">If working at the channel layer, faults can be sent for a [WS\_ERROR](ws-error.md) object using [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).</span></span>

## <a name="handling-faults-on-a-client"></a><span data-ttu-id="0cffd-138">處理用戶端上的錯誤</span><span class="sxs-lookup"><span data-stu-id="0cffd-138">Handling faults on a client</span></span>

<span data-ttu-id="0cffd-139">如果用戶端在使用 [服務 Proxy](service-proxy.md) 或透過 [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) 或 [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)時收到錯誤，則會傳回 **WS \_ E 端點錯誤 \_ \_ \_ 接收** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-139">If a client receives a fault when using a [Service Proxy](service-proxy.md) or via [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) or [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), the **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** error will be returned.</span></span> <span data-ttu-id="0cffd-140"> (需詳細資訊，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。 ) 這些函式也會以收到的錯誤相關資訊，填入提供給呼叫的 [WS \_ ERROR](ws-error.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0cffd-140">(For more information, see [Windows Web Services Return Values](windows-web-services-return-values.md).) These functions will also populate the [WS\_ERROR](ws-error.md) object supplied to the call with information about the received fault.</span></span>

<span data-ttu-id="0cffd-141">您可以使用 [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)來查詢 [WS \_ ERROR](ws-error.md)物件的下列屬性，以取得所收到之錯誤的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="0cffd-141">The following properties of an [WS\_ERROR](ws-error.md) object can be queried using [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) to obtain information about a fault that was received:</span></span>

-   <span data-ttu-id="0cffd-142">[**WS \_錯誤 \_ 的 \_ 屬性 \_ 動作**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。</span><span class="sxs-lookup"><span data-stu-id="0cffd-142">[**WS\_FAULT\_ERROR\_PROPERTY\_ACTION**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id).</span></span> <span data-ttu-id="0cffd-143">這會指定錯誤訊息的動作值。</span><span class="sxs-lookup"><span data-stu-id="0cffd-143">This specifies the action value of the fault message.</span></span>
-   <span data-ttu-id="0cffd-144">[**WS \_錯誤 \_ \_ 屬性 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cffd-144">[**WS\_FAULT\_ERROR\_PROPERTY\_FAULT**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id).</span></span> <span data-ttu-id="0cffd-145">這包含從錯誤訊息主體還原序列化的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構。</span><span class="sxs-lookup"><span data-stu-id="0cffd-145">This contains the [**WS\_FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) structure that was deserialized from the body of the fault message.</span></span>

<span data-ttu-id="0cffd-146">錯誤可能會在錯誤的詳細資料中包含任意的其他 XML 內容。</span><span class="sxs-lookup"><span data-stu-id="0cffd-146">A fault may contain arbitrary additional XML content in the detail of the fault.</span></span> <span data-ttu-id="0cffd-147">您可以使用 [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) 函式來存取此函數。</span><span class="sxs-lookup"><span data-stu-id="0cffd-147">This can be accessed using the use the [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) function.</span></span>

## <a name="using-faults-with-messages"></a><span data-ttu-id="0cffd-148">使用錯誤與訊息</span><span class="sxs-lookup"><span data-stu-id="0cffd-148">Using faults with messages</span></span>

<span data-ttu-id="0cffd-149">下一節適用于直接處理錯誤訊息主體的內容時。</span><span class="sxs-lookup"><span data-stu-id="0cffd-149">The following section applies when dealing directly with the contents of the body of a fault message.</span></span>

<span data-ttu-id="0cffd-150">錯誤訊息主體的內容是由標準的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構所表示，它具有序列化的內建支援。</span><span class="sxs-lookup"><span data-stu-id="0cffd-150">The contents of the body of a fault message is represented by the standard [**WS\_FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) structure, which has built-in support for serialization.</span></span>

<span data-ttu-id="0cffd-151">例如，下列程式碼可以用來將錯誤寫入訊息主體：</span><span class="sxs-lookup"><span data-stu-id="0cffd-151">For example, the following code can be used to write a fault to a message body:</span></span>

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

<span data-ttu-id="0cffd-152">下列程式碼可以用來讀取訊息本文中的錯誤：</span><span class="sxs-lookup"><span data-stu-id="0cffd-152">The following code can be used to read a fault from a message body:</span></span>

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

<span data-ttu-id="0cffd-153">為了知道接收的訊息是否為錯誤，可以參考 [**WS \_ message \_ 屬性 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) 。</span><span class="sxs-lookup"><span data-stu-id="0cffd-153">In order to know whether a received message is a fault or not, the [**WS\_MESSAGE\_PROPERTY\_IS\_FAULT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) can be consulted.</span></span> <span data-ttu-id="0cffd-154">這個屬性是根據主體中的第一個元素是否為 [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) 或 [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)期間的錯誤元素所設定。</span><span class="sxs-lookup"><span data-stu-id="0cffd-154">This property is set based on whether the first element in the body is a fault element during [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) or [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).</span></span>

<span data-ttu-id="0cffd-155">若要在指定 [ws \_ 錯誤時](ws-error.md)建立 [**\_ Ws**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)錯誤，請使用 [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)函數。</span><span class="sxs-lookup"><span data-stu-id="0cffd-155">To create a [**WS\_FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) given a [WS\_ERROR](ws-error.md), use the [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) function.</span></span>

<span data-ttu-id="0cffd-156">下列列舉是錯誤的一部分：</span><span class="sxs-lookup"><span data-stu-id="0cffd-156">The following enumerations are part of faults:</span></span>

-   [<span data-ttu-id="0cffd-157">**WS \_ 錯誤 \_ 洩漏**</span><span class="sxs-lookup"><span data-stu-id="0cffd-157">**WS\_FAULT\_DISCLOSURE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [<span data-ttu-id="0cffd-158">**WS 錯誤的 \_ \_ \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="0cffd-158">**WS\_FAULT\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

<span data-ttu-id="0cffd-159">下列函數是錯誤的一部分：</span><span class="sxs-lookup"><span data-stu-id="0cffd-159">The following functions are part of faults:</span></span>

-   [<span data-ttu-id="0cffd-160">**WsCreateFaultFromError**</span><span class="sxs-lookup"><span data-stu-id="0cffd-160">**WsCreateFaultFromError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [<span data-ttu-id="0cffd-161">**WsGetFaultErrorDetail**</span><span class="sxs-lookup"><span data-stu-id="0cffd-161">**WsGetFaultErrorDetail**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [<span data-ttu-id="0cffd-162">**WsGetFaultErrorProperty**</span><span class="sxs-lookup"><span data-stu-id="0cffd-162">**WsGetFaultErrorProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [<span data-ttu-id="0cffd-163">**WsSetFaultErrorDetail**</span><span class="sxs-lookup"><span data-stu-id="0cffd-163">**WsSetFaultErrorDetail**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [<span data-ttu-id="0cffd-164">**WsSetFaultErrorProperty**</span><span class="sxs-lookup"><span data-stu-id="0cffd-164">**WsSetFaultErrorProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

<span data-ttu-id="0cffd-165">下列結構是錯誤的一部分：</span><span class="sxs-lookup"><span data-stu-id="0cffd-165">The following structures are part of faults:</span></span>

-   [<span data-ttu-id="0cffd-166">**WS \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="0cffd-166">**WS\_FAULT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [<span data-ttu-id="0cffd-167">**WS \_ \_ 錯誤碼**</span><span class="sxs-lookup"><span data-stu-id="0cffd-167">**WS\_FAULT\_CODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [<span data-ttu-id="0cffd-168">**WS \_ 錯誤 \_ 詳細資料 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="0cffd-168">**WS\_FAULT\_DETAIL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [<span data-ttu-id="0cffd-169">**WS \_ 錯誤 \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="0cffd-169">**WS\_FAULT\_REASON**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 





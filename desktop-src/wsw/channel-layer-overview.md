---
title: 通道層總覽
description: 通道層提供傳輸通道的抽象概念，以及通道上送出的訊息。
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- 適用于 Windows 的通道層總覽 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567010"
---
# <a name="channel-layer-overview"></a><span data-ttu-id="db257-106">通道層總覽</span><span class="sxs-lookup"><span data-stu-id="db257-106">Channel Layer Overview</span></span>

<span data-ttu-id="db257-107">通道層提供傳輸通道的抽象概念，以及通道上送出的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="db257-108">它也包含在 SOAP 結構之間序列化 C 資料類型的函式。</span><span class="sxs-lookup"><span data-stu-id="db257-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="db257-109">通道層可透過由傳送或接收的資料，以及包含主體和標頭的 [訊息](message.md) ，以及抽象訊息交換通訊協定的 [通道](channel.md) ，以及提供自訂設定的屬性，來完全控制通訊。</span><span class="sxs-lookup"><span data-stu-id="db257-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="db257-110">訊息</span><span class="sxs-lookup"><span data-stu-id="db257-110">Message</span></span>

<span data-ttu-id="db257-111">[訊息](message.md)是封裝網路資料的物件，特別是在網路上傳輸或接收的資料。</span><span class="sxs-lookup"><span data-stu-id="db257-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="db257-112">訊息結構是由 SOAP 定義，其中包含一組不連續的標頭和訊息主體。</span><span class="sxs-lookup"><span data-stu-id="db257-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="db257-113">標頭會放在記憶體緩衝區中，並使用串流 API 來讀取或寫入訊息主體。</span><span class="sxs-lookup"><span data-stu-id="db257-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![此圖顯示訊息的標頭和本文。](images/messageenvelope.png)

<span data-ttu-id="db257-115">雖然訊息的資料模型一律是 XML 資料模型，但實際的電傳格式很有彈性。</span><span class="sxs-lookup"><span data-stu-id="db257-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="db257-116">傳送訊息之前，會使用特定編碼方式來編碼 (例如文字、二進位或 MTOM) 。</span><span class="sxs-lookup"><span data-stu-id="db257-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="db257-117">如需編碼的詳細資訊，請參閱 [**WS \_ 編碼方式**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) 。</span><span class="sxs-lookup"><span data-stu-id="db257-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![顯示數種訊息編碼格式的圖表。](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="db257-119">通路</span><span class="sxs-lookup"><span data-stu-id="db257-119">Channel</span></span>

<span data-ttu-id="db257-120">[通道](channel.md)是一個物件，用來在兩個或多個端點之間的網路上傳送和接收訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="db257-121">通道有相關聯的資料，描述如何在傳送訊息時 [處理](endpoint-address.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="db257-122">傳送通道上的訊息，就像是將它放在斜槽中一樣，通道也包含訊息應該送到的資訊，以及如何取得訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![顯示訊息通道的圖表。](images/channelsaschute.png)

<span data-ttu-id="db257-124">通道會分類為 [**通道類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)。</span><span class="sxs-lookup"><span data-stu-id="db257-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="db257-125">通道類型會指定訊息可流動的方向。</span><span class="sxs-lookup"><span data-stu-id="db257-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="db257-126">通道類型也會識別通道為會話或無會話。</span><span class="sxs-lookup"><span data-stu-id="db257-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="db257-127">會話定義為在兩個或更多方之間相互關聯訊息的抽象方法。</span><span class="sxs-lookup"><span data-stu-id="db257-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="db257-128">會話通道的範例是 TCP 通道，其使用 TCP 連線作為具體會話的執行。</span><span class="sxs-lookup"><span data-stu-id="db257-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="db257-129">無會話通道的範例是 UDP，它沒有基礎會話機制。</span><span class="sxs-lookup"><span data-stu-id="db257-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="db257-130">雖然 HTTP 具有基礎 TCP 連線，但這項事實不會直接透過此 API 公開，因此 HTTP 也會被視為無會話通道。</span><span class="sxs-lookup"><span data-stu-id="db257-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![顯示會話和無會話通道類型的圖表。](images/channeltypes.png)

<span data-ttu-id="db257-132">雖然通道類型會描述通道的方向和會話資訊，但不會指定通道的實作為方式。</span><span class="sxs-lookup"><span data-stu-id="db257-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="db257-133">通道應使用何種通訊協定？</span><span class="sxs-lookup"><span data-stu-id="db257-133">What protocol should the channel use?</span></span> <span data-ttu-id="db257-134">通道應該如何嘗試傳遞訊息？</span><span class="sxs-lookup"><span data-stu-id="db257-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="db257-135">使用何種安全性？</span><span class="sxs-lookup"><span data-stu-id="db257-135">What kind of security is used?</span></span> <span data-ttu-id="db257-136">它是 singlecast 還是多播？</span><span class="sxs-lookup"><span data-stu-id="db257-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="db257-137">這些設定稱為通道的「系結」。</span><span class="sxs-lookup"><span data-stu-id="db257-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="db257-138">系結包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="db257-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="db257-139">[**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結，識別要使用 (TCP、UDP、HTTP、NAMEDPIPE) 的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="db257-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="db257-140">[**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)，指定如何保護通道的安全。</span><span class="sxs-lookup"><span data-stu-id="db257-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="db257-141">設定的 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)，指定其他選擇性設定。</span><span class="sxs-lookup"><span data-stu-id="db257-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="db257-142">請參閱屬性清單的 [**WS \_ 通道 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) 。</span><span class="sxs-lookup"><span data-stu-id="db257-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![顯示通道屬性清單的圖表。](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="db257-144">接聽程式</span><span class="sxs-lookup"><span data-stu-id="db257-144">Listener</span></span>

<span data-ttu-id="db257-145">若要開始進行通訊，用戶端會建立通道物件。</span><span class="sxs-lookup"><span data-stu-id="db257-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="db257-146">但服務如何取得其通道物件？</span><span class="sxs-lookup"><span data-stu-id="db257-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="db257-147">它會藉由建立接聽程式來執行此[動作。](listener.md)</span><span class="sxs-lookup"><span data-stu-id="db257-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="db257-148">建立接聽程式時，需要相同的系結資訊來建立通道。</span><span class="sxs-lookup"><span data-stu-id="db257-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="db257-149">一旦建立接聽程式之後，應用程式就可以接受來自接聽程式的通道。</span><span class="sxs-lookup"><span data-stu-id="db257-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="db257-150">由於應用程式可能會落在接受通道後方，因此接聽程式通常會保留已準備好接受 (的通道佇列，) 。</span><span class="sxs-lookup"><span data-stu-id="db257-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![顯示接聽程式佇列中通道的圖表。](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="db257-152"> (用戶端) 起始通訊</span><span class="sxs-lookup"><span data-stu-id="db257-152">Initiating Communication (client)</span></span>

<span data-ttu-id="db257-153">若要在用戶端上起始通訊，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-153">To initiate communication on the client, use the following sequence.</span></span>

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a><span data-ttu-id="db257-154">接受通訊 (伺服器) </span><span class="sxs-lookup"><span data-stu-id="db257-154">Accepting Communication (server)</span></span>

<span data-ttu-id="db257-155">若要接受伺服器上的連入通訊，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-155">To accept incoming communications on the server, use the following sequence.</span></span>

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="db257-156"> (用戶端或伺服器) 傳送訊息</span><span class="sxs-lookup"><span data-stu-id="db257-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="db257-157">若要傳送訊息，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="db257-158">[**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)函式不允許串流處理，並假設主體只包含一個元素。</span><span class="sxs-lookup"><span data-stu-id="db257-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="db257-159">若要避免這些條件約束，請使用下列順序，而不是 **WsSendMessage**。</span><span class="sxs-lookup"><span data-stu-id="db257-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

<span data-ttu-id="db257-160">[**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)函式會使用序列化來寫入主體專案。</span><span class="sxs-lookup"><span data-stu-id="db257-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="db257-161">若要將資料直接寫入 XML 寫入器，請使用下列順序，而不是 **WsWriteBody**。</span><span class="sxs-lookup"><span data-stu-id="db257-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="db257-162">[**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader)函式會使用序列化將標頭設定為訊息的標頭緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db257-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="db257-163">若要使用 XML 寫入器來寫入標頭，請使用下列順序，而不是 **WsAddCustomHeader**。</span><span class="sxs-lookup"><span data-stu-id="db257-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="db257-164"> (用戶端或伺服器) 接收訊息</span><span class="sxs-lookup"><span data-stu-id="db257-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="db257-165">若要接收訊息，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-165">To receive messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

<span data-ttu-id="db257-166">[**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)函式不允許串流處理，並假設主體只包含一個專案，而且訊息的型別 (動作和主體) 的架構都是事先知道的。</span><span class="sxs-lookup"><span data-stu-id="db257-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="db257-167">若要避免這些條件約束，請使用下列順序，而不是 **WsReceiveMessage**。</span><span class="sxs-lookup"><span data-stu-id="db257-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

<span data-ttu-id="db257-168">[**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)函式會使用序列化來讀取主體元素。</span><span class="sxs-lookup"><span data-stu-id="db257-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="db257-169">若要直接從 [XML 讀取器](xml-reader.md)讀取資料，請使用下列順序，而不是 **WsReadBody**。</span><span class="sxs-lookup"><span data-stu-id="db257-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="db257-170">[**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)函式會使用序列化來取得訊息的標頭緩衝區中的標頭。</span><span class="sxs-lookup"><span data-stu-id="db257-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="db257-171">若要使用 [XML 讀取器](xml-reader.md) 讀取標頭，請使用下列順序，而不是 **WsGetCustomHeader**。</span><span class="sxs-lookup"><span data-stu-id="db257-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a><span data-ttu-id="db257-172">要求回復 (用戶端) </span><span class="sxs-lookup"><span data-stu-id="db257-172">Request Reply (client)</span></span>

<span data-ttu-id="db257-173">您可以使用下列順序來執行用戶端上的要求-回復。</span><span class="sxs-lookup"><span data-stu-id="db257-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

<span data-ttu-id="db257-174">[**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)函式會假設要求和回復訊息內文的單一專案，而且訊息的型別 (動作和內文的架構) 事先知道。</span><span class="sxs-lookup"><span data-stu-id="db257-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="db257-175">為了避免這些限制，您可以手動傳送要求和回復訊息，如下列順序所示。</span><span class="sxs-lookup"><span data-stu-id="db257-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="db257-176">此序列符合傳送和接收訊息的較早順序，除非有注明。</span><span class="sxs-lookup"><span data-stu-id="db257-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a><span data-ttu-id="db257-177">要求回復 (伺服器) </span><span class="sxs-lookup"><span data-stu-id="db257-177">Request Reply (server)</span></span>

<span data-ttu-id="db257-178">若要在伺服器上接收要求訊息，請使用與上一節中所述的相同順序來接收訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="db257-179">若要傳送回復或錯誤訊息，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="db257-180">[**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)函式會假設主體中有單一元素，但不允許串流處理。</span><span class="sxs-lookup"><span data-stu-id="db257-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="db257-181">若要避免這些限制，請使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="db257-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="db257-182">這與先前用來傳送訊息的順序相同，但在初始化時，會使用 [**ws \_ 回復 \_ 訊息**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) ，而不是 **ws \_ 空白 \_ 訊息** 。</span><span class="sxs-lookup"><span data-stu-id="db257-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a><span data-ttu-id="db257-183">訊息交換模式</span><span class="sxs-lookup"><span data-stu-id="db257-183">Message Exchange Patterns</span></span>

<span data-ttu-id="db257-184">[**WS \_ 通道 \_ 型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)別會針對指定的通道，規定可能的訊息交換模式。</span><span class="sxs-lookup"><span data-stu-id="db257-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="db257-185">支援的類型會根據系結而有所不同，如下所示：</span><span class="sxs-lookup"><span data-stu-id="db257-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="db257-186">[**WS \_HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 要求**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 和伺服器上的 **ws \_ 通道 \_ 類型 \_ 回復** 。</span><span class="sxs-lookup"><span data-stu-id="db257-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="db257-187">[**WS \_TCP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工 \_ 會話**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 雙工 \_** 會話。</span><span class="sxs-lookup"><span data-stu-id="db257-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="db257-188">[**WS \_UDP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 輸入** 。</span><span class="sxs-lookup"><span data-stu-id="db257-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="db257-189">[**WS \_NAMEDPIPE \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 輸入** 。</span><span class="sxs-lookup"><span data-stu-id="db257-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="db257-190">訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="db257-190">Message Loops</span></span>

<span data-ttu-id="db257-191">每個訊息交換模式都有特定的「迴圈」，可用來傳送或接收訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="db257-192">迴圈會描述傳送/接收多個訊息所需的作業的合法順序。</span><span class="sxs-lookup"><span data-stu-id="db257-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="db257-193">這些迴圈會在以下的文法生產中描述。</span><span class="sxs-lookup"><span data-stu-id="db257-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="db257-194">「End」詞彙是傳回 **WS \_ S \_ end** 的接收 (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) ，指出通道上沒有其他可用的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="db257-195">平行生產會指定平行 (x & y) 該作業 x 可以與 y 同時進行。</span><span class="sxs-lookup"><span data-stu-id="db257-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="db257-196">用戶端會使用下列迴圈：</span><span class="sxs-lookup"><span data-stu-id="db257-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="db257-197">下列迴圈會在伺服器上使用：</span><span class="sxs-lookup"><span data-stu-id="db257-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="db257-198">使用伺服器上的 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 系結時，必須先成功接收才能傳送，即使通道 [**類型為 WS \_ 通道類型的 \_ \_ 雙工 \_ 會話**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)，仍允許傳送。</span><span class="sxs-lookup"><span data-stu-id="db257-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="db257-199">在第一次接收之後。</span><span class="sxs-lookup"><span data-stu-id="db257-199">After the first receive.</span></span> <span data-ttu-id="db257-200">套用一般迴圈。</span><span class="sxs-lookup"><span data-stu-id="db257-200">the regular loop applies.</span></span>

<span data-ttu-id="db257-201">請注意， [**ws \_ 通道 \_ 類型 \_ 要求**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 和 **WS \_ 通道 \_ 類型 \_ 回復** 的通道可以用來傳送和接收單向訊息 (以及標準要求-回復模式) 。</span><span class="sxs-lookup"><span data-stu-id="db257-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="db257-202">若要完成此作業，請關閉回復通道而不傳送回復。</span><span class="sxs-lookup"><span data-stu-id="db257-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="db257-203">在此情況下，要求通道上將不會收到任何回復。</span><span class="sxs-lookup"><span data-stu-id="db257-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="db257-204">使用伺服器上的 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ \_ 安全性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系 **結來 \_ \_ 結束** 的傳回值，需要成功接收才能傳送，即使通道類型為 **WS \_ 通道類型的 \_ \_ 雙工會 \_ 話**，仍允許傳送。</span><span class="sxs-lookup"><span data-stu-id="db257-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="db257-205">第一次接收時，會套用一般迴圈。</span><span class="sxs-lookup"><span data-stu-id="db257-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="db257-206">將會傳回，表示沒有可用的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="db257-207">用戶端或伺服器迴圈可能會使用多個通道實例，以平行方式完成。</span><span class="sxs-lookup"><span data-stu-id="db257-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="db257-208">訊息篩選</span><span class="sxs-lookup"><span data-stu-id="db257-208">Message Filtering</span></span>

<span data-ttu-id="db257-209">伺服器通道可能會篩選出不適合應用程式的接收訊息，例如建立 [安全性內容](security-context.md)的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="db257-210">在這種情況下，會從 [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)傳回 **WS \_ S \_ END** ，而該通道上將不會提供任何應用程式訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="db257-211">不過，這並不表示用戶端想要結束與伺服器的通訊。</span><span class="sxs-lookup"><span data-stu-id="db257-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="db257-212">其他通道上可能會有更多的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-212">More messages may be available on another channel.</span></span> <span data-ttu-id="db257-213">請參閱 [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel)。</span><span class="sxs-lookup"><span data-stu-id="db257-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="db257-214">取消</span><span class="sxs-lookup"><span data-stu-id="db257-214">Cancellation</span></span>

<span data-ttu-id="db257-215">[**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)函式是用來取消通道的暫止 IO。</span><span class="sxs-lookup"><span data-stu-id="db257-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="db257-216">此 API 不會等候 IO 作業 (的) 完成。</span><span class="sxs-lookup"><span data-stu-id="db257-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="db257-217">如需詳細資訊，請參閱 **WsAbortChannel** 的 [**WS \_ 通道 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)狀態圖表和檔。</span><span class="sxs-lookup"><span data-stu-id="db257-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="db257-218">[**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API 可用來取消接聽程式的暫止 IO。</span><span class="sxs-lookup"><span data-stu-id="db257-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="db257-219">此 API 不會等候 IO 作業 (的) 完成。</span><span class="sxs-lookup"><span data-stu-id="db257-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="db257-220">中止接聽程式也會導致所有暫止的接受中止。</span><span class="sxs-lookup"><span data-stu-id="db257-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="db257-221">如需詳細資訊，請參閱 WS 接聽程式 [**\_ \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) 狀態圖和 **WsAbortListener** 。</span><span class="sxs-lookup"><span data-stu-id="db257-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="db257-222">TCP</span><span class="sxs-lookup"><span data-stu-id="db257-222">TCP</span></span>

<span data-ttu-id="db257-223">[**WS \_ tcp \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援透過 TCP 的 SOAP。</span><span class="sxs-lookup"><span data-stu-id="db257-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="db257-224">SOAP over TCP 規格是以 .NET 框架機制為基礎。</span><span class="sxs-lookup"><span data-stu-id="db257-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="db257-225">此版本不支援埠共用。</span><span class="sxs-lookup"><span data-stu-id="db257-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="db257-226">開啟的每個接聽程式都必須使用不同的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="db257-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="db257-227">UDP</span><span class="sxs-lookup"><span data-stu-id="db257-227">UDP</span></span>

<span data-ttu-id="db257-228">[**WS \_ udp \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援 SOAP over udp。</span><span class="sxs-lookup"><span data-stu-id="db257-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="db257-229">UDP 系結有一些限制：</span><span class="sxs-lookup"><span data-stu-id="db257-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="db257-230">不支援安全性。</span><span class="sxs-lookup"><span data-stu-id="db257-230">There is no support for security.</span></span>
-   <span data-ttu-id="db257-231">訊息可能會遺失或重複。</span><span class="sxs-lookup"><span data-stu-id="db257-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="db257-232">僅支援一種編碼： [**WS \_ 編碼 \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)。</span><span class="sxs-lookup"><span data-stu-id="db257-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="db257-233">訊息基本上會限制為64k，如果大小超過網路的 MTU，通常會有更大的可能遺失。</span><span class="sxs-lookup"><span data-stu-id="db257-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="db257-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="db257-234">HTTP</span></span>

<span data-ttu-id="db257-235">[**WS \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援 SOAP over HTTP。</span><span class="sxs-lookup"><span data-stu-id="db257-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="db257-236">若要控制用戶端和伺服器上的 HTTP 特定標頭，請參閱 [**WS \_ HTTP \_ MESSAGE \_ MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)。</span><span class="sxs-lookup"><span data-stu-id="db257-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="db257-237">若要在伺服器上傳送和接收非 SOAP 訊息，請針對 [**ws \_ 通道 \_ 屬性 \_ 編碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)使用 [**ws \_ 編碼 \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) 。</span><span class="sxs-lookup"><span data-stu-id="db257-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="db257-238">NAMEDPIPES</span><span class="sxs-lookup"><span data-stu-id="db257-238">NAMEDPIPES</span></span>

<span data-ttu-id="db257-239">[**WS \_ NAMEDPIPE \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援透過具名管道的 SOAP，允許使用 NetNamedPipeBinding 與 Windows Communication Foundation (WCF) 服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="db257-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="db257-240">相互關聯要求/回復訊息</span><span class="sxs-lookup"><span data-stu-id="db257-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="db257-241">要求/回復訊息會以下列兩種方式之一相互關聯：</span><span class="sxs-lookup"><span data-stu-id="db257-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="db257-242">相互關聯是使用通道做為相互關聯機制來完成。</span><span class="sxs-lookup"><span data-stu-id="db257-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="db257-243">例如，使用 [**ws \_ 定址 \_ 版本 \_ 傳輸**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 和 [**WS \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結時，要求訊息的回復會與要求相互關聯，而這就是 HTTP 回應的實體主體。</span><span class="sxs-lookup"><span data-stu-id="db257-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="db257-244">相互關聯是使用 MessageID 和 RelatesTo 標頭來完成。</span><span class="sxs-lookup"><span data-stu-id="db257-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="db257-245">即使使用 [**ws \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結) ，此機制也可搭配 [**Ws-addressing \_ \_ 版本 \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)和 **ws \_ 定址 \_ 版本 \_ 0 \_ 9** (使用。</span><span class="sxs-lookup"><span data-stu-id="db257-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="db257-246">在此情況下，要求訊息會包含 MessageID 標頭。</span><span class="sxs-lookup"><span data-stu-id="db257-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="db257-247">回應訊息包含具有要求 MessageID 標頭值的 RelatesTo 標頭。</span><span class="sxs-lookup"><span data-stu-id="db257-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="db257-248">RelatesTo 標頭可讓用戶端將回應與它所傳送的要求相互關聯。</span><span class="sxs-lookup"><span data-stu-id="db257-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="db257-249">下列通道層 Api 會根據通道的 [**WS \_ 定址 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 自動使用適當的相互關聯機制。</span><span class="sxs-lookup"><span data-stu-id="db257-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="db257-250">**WsRequestReply**</span><span class="sxs-lookup"><span data-stu-id="db257-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="db257-251">**WsSendReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="db257-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="db257-252">**WsSendFaultMessageForError**</span><span class="sxs-lookup"><span data-stu-id="db257-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="db257-253">如果未使用這些 Api，可以使用 [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) 或 [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)以手動方式新增和存取標頭。</span><span class="sxs-lookup"><span data-stu-id="db257-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="db257-254">自訂通道和接聽程式</span><span class="sxs-lookup"><span data-stu-id="db257-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="db257-255">如果預先定義的通道系結組不符合應用程式的需求，則在建立通道或接聽程式時，可以藉由指定 [**WS \_ 自 \_ 定義 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結來定義自訂通道和接聽程式的執行。</span><span class="sxs-lookup"><span data-stu-id="db257-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="db257-256">通道/接聽程式的實際實作為透過 [**WS \_ 通道 \_ 屬性 \_ 自訂 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) 或 ws 接聽程式 [**\_ \_ 屬性 \_ 自訂 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) 接聽程式回呼屬性指定為一組回呼。</span><span class="sxs-lookup"><span data-stu-id="db257-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="db257-257">建立自訂通道或接聽程式之後，結果會是可以與現有 Api 搭配使用的[ws \_ 通道](ws-channel.md)或 ws 接聽程式物件。 [ \_ ](ws-listener.md)</span><span class="sxs-lookup"><span data-stu-id="db257-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="db257-258">自訂通道和接聽程式也可以搭配服務 Proxy 和 [服務主機](service-host.md)使用，方法是在 [**ws \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結列舉中指定 **ws \_ 自訂 \_ 通道 \_** 系結值，並在建立服務 Proxy 或服務主機時，指定 ws [**通道屬性自訂 \_ \_ \_ \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)和 ws 接聽程式 [**\_ \_ 屬性 \_ 自訂 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)接聽程式回呼屬性。</span><span class="sxs-lookup"><span data-stu-id="db257-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="db257-259">安全性</span><span class="sxs-lookup"><span data-stu-id="db257-259">Security</span></span>

<span data-ttu-id="db257-260">通道可讓您透過下列屬性限制作業的各種層面所使用的記憶體數量：</span><span class="sxs-lookup"><span data-stu-id="db257-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="db257-261">[**WS \_通道 \_ 屬性的 \_ 最大 \_ 緩衝 \_ 訊息 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-262">[**WS \_通道 \_ 屬性 \_ 最大 \_ 資料流程處理 \_ 訊息 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-263">[**WS \_通道 \_ 屬性 \_ 最大 \_ 資料流程處理 \_ 開始 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-264">[**WS \_通道 \_ 屬性 \_ 最大 \_ HTTP \_ 要求 \_ 標頭 \_ 緩衝區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-265">[**WS \_通道 \_ 屬性 \_ 最大 \_ 會話 \_ 字典 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)。</span><span class="sxs-lookup"><span data-stu-id="db257-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="db257-266">這些屬性具有預設值，在大部分情況下都是保守且安全的。</span><span class="sxs-lookup"><span data-stu-id="db257-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="db257-267">預設值和對它們所做的任何修改都應謹慎地針對可能會導致遠端使用者拒絕服務的潛在攻擊媒介進行評估。</span><span class="sxs-lookup"><span data-stu-id="db257-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="db257-268">通道可讓您透過下列屬性來設定作業各個層面的超時值：</span><span class="sxs-lookup"><span data-stu-id="db257-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="db257-269">[**WS \_通道 \_ 屬性 \_ 連接 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-270">[**WS \_通道 \_ 屬性 \_ 傳送 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-271">[**WS \_通道 \_ 屬性 \_ 接收 \_ 回應 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-272">[**WS \_通道 \_ 屬性 \_ 接收 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-273">[**WS \_通道 \_ 屬性 \_ 解析 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，</span><span class="sxs-lookup"><span data-stu-id="db257-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="db257-274">[**WS \_通道 \_ 屬性 \_ 關閉 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)。</span><span class="sxs-lookup"><span data-stu-id="db257-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="db257-275">這些屬性具有預設值，在大部分情況下都是保守且安全的。</span><span class="sxs-lookup"><span data-stu-id="db257-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="db257-276">增加超時值會增加遠端方可以存留本機資源的時間量，例如記憶體、通訊端，以及執行同步 i/o 的執行緒。</span><span class="sxs-lookup"><span data-stu-id="db257-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="db257-277">應用程式應該評估預設值，並在增加時間時小心使用，因為它可能會開啟可能會導致遠端電腦拒絕服務的潛在攻擊媒介。</span><span class="sxs-lookup"><span data-stu-id="db257-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="db257-278">使用 WWSAPI 通道 API 時，應謹慎評估的一些其他設定選項和應用程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="db257-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="db257-279">使用通道/接聽程式層時，會由應用程式負責在伺服器端建立和接受通道。</span><span class="sxs-lookup"><span data-stu-id="db257-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="db257-280">同樣地，應用程式會在用戶端上建立並開啟通道。</span><span class="sxs-lookup"><span data-stu-id="db257-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="db257-281">應用程式應該對這些作業加上上限，因為每個通道都會耗用記憶體和其他有限的資源，例如通訊端。</span><span class="sxs-lookup"><span data-stu-id="db257-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="db257-282">當建立通道以回應遠端方所觸發的任何動作時，應用程式應該特別小心。</span><span class="sxs-lookup"><span data-stu-id="db257-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="db257-283">應用程式會由應用程式撰寫邏輯來建立通道並接受這些通道。</span><span class="sxs-lookup"><span data-stu-id="db257-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="db257-284">每個通道都會耗用有限的資源，例如記憶體和通訊端。</span><span class="sxs-lookup"><span data-stu-id="db257-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="db257-285">應用程式的上限應該是其願意接受的通道數目上限，或者遠端方可以進行許多連線，進而導致 OOM，因而導致阻絕服務。</span><span class="sxs-lookup"><span data-stu-id="db257-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="db257-286">它也應該使用較短的時間，主動接收來自這些連接的訊息。</span><span class="sxs-lookup"><span data-stu-id="db257-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="db257-287">如果沒有收到任何訊息，則作業將會超時，且應該釋放連接。</span><span class="sxs-lookup"><span data-stu-id="db257-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="db257-288">應用程式會透過解讀 ReplyTo 或 FaultTo SOAP 標頭來傳送回復或錯誤。</span><span class="sxs-lookup"><span data-stu-id="db257-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="db257-289">安全做法是只接受「匿名」的 ReplyTo 或 FaultTo 標頭，這表示現有的連接 (TCP、HTTP) 或來源 IP (UDP) 應該用來傳送 SOAP 回復。</span><span class="sxs-lookup"><span data-stu-id="db257-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="db257-290">在建立資源 (例如通道) 來回複不同的位址時，應用程式應該要特別小心，除非該訊息是由可以說出回復傳送目的地位址的合作物件所簽署。</span><span class="sxs-lookup"><span data-stu-id="db257-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="db257-291">在通道層中完成的驗證無法取代透過安全性達成的資料完整性。</span><span class="sxs-lookup"><span data-stu-id="db257-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="db257-292">應用程式必須依賴 WWSAPI 的安全性功能，以確保它會與受信任的實體通訊，而且也必須依賴安全性以確保資料完整性。</span><span class="sxs-lookup"><span data-stu-id="db257-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="db257-293">同樣地，使用 WWSAPI 訊息 API 時，應謹慎評估訊息設定選項和應用程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="db257-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="db257-294">用來儲存訊息標頭的堆積大小，可以使用 [**WS \_ message \_ PROPERTY property \_ 堆積 \_ PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) 屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="db257-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="db257-295">提高此值可讓訊息的標頭耗用更多記憶體，這可能會導致 OOM。</span><span class="sxs-lookup"><span data-stu-id="db257-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="db257-296">Message 物件的使用者必須瞭解標頭存取 Api 是 O (n) 與訊息中的標頭數目有關，因為它們會檢查是否有重複的專案。</span><span class="sxs-lookup"><span data-stu-id="db257-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="db257-297">在訊息中需要許多標頭的設計可能會導致過多的 CPU 使用量。</span><span class="sxs-lookup"><span data-stu-id="db257-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="db257-298">您可以使用 [ [**WS \_ 訊息 \_ 屬性 \_ 最大 \_ 處理 \_ 標頭**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) ] 屬性來設定訊息中的標頭數目上限。</span><span class="sxs-lookup"><span data-stu-id="db257-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="db257-299">此外，也有根據訊息堆積大小的隱含限制。</span><span class="sxs-lookup"><span data-stu-id="db257-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="db257-300">增加這兩個值可提供更多的標頭，以在使用標頭存取 Api) 時，將尋找標頭所需的時間 (。</span><span class="sxs-lookup"><span data-stu-id="db257-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 





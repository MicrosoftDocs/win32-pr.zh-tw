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
# <a name="channel-layer-overview"></a>通道層總覽

通道層提供傳輸通道的抽象概念，以及通道上送出的訊息。 它也包含在 SOAP 結構之間序列化 C 資料類型的函式。 通道層可透過由傳送或接收的資料，以及包含主體和標頭的 [訊息](message.md) ，以及抽象訊息交換通訊協定的 [通道](channel.md) ，以及提供自訂設定的屬性，來完全控制通訊。

## <a name="message"></a>訊息

[訊息](message.md)是封裝網路資料的物件，特別是在網路上傳輸或接收的資料。 訊息結構是由 SOAP 定義，其中包含一組不連續的標頭和訊息主體。 標頭會放在記憶體緩衝區中，並使用串流 API 來讀取或寫入訊息主體。

![此圖顯示訊息的標頭和本文。](images/messageenvelope.png)

雖然訊息的資料模型一律是 XML 資料模型，但實際的電傳格式很有彈性。 傳送訊息之前，會使用特定編碼方式來編碼 (例如文字、二進位或 MTOM) 。 如需編碼的詳細資訊，請參閱 [**WS \_ 編碼方式**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) 。

![顯示數種訊息編碼格式的圖表。](images/messageandencodings.png)

## <a name="channel"></a>通路

[通道](channel.md)是一個物件，用來在兩個或多個端點之間的網路上傳送和接收訊息。

通道有相關聯的資料，描述如何在傳送訊息時 [處理](endpoint-address.md) 訊息。 傳送通道上的訊息，就像是將它放在斜槽中一樣，通道也包含訊息應該送到的資訊，以及如何取得訊息。

![顯示訊息通道的圖表。](images/channelsaschute.png)

通道會分類為 [**通道類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)。 通道類型會指定訊息可流動的方向。 通道類型也會識別通道為會話或無會話。 會話定義為在兩個或更多方之間相互關聯訊息的抽象方法。 會話通道的範例是 TCP 通道，其使用 TCP 連線作為具體會話的執行。 無會話通道的範例是 UDP，它沒有基礎會話機制。 雖然 HTTP 具有基礎 TCP 連線，但這項事實不會直接透過此 API 公開，因此 HTTP 也會被視為無會話通道。

![顯示會話和無會話通道類型的圖表。](images/channeltypes.png)

雖然通道類型會描述通道的方向和會話資訊，但不會指定通道的實作為方式。 通道應使用何種通訊協定？ 通道應該如何嘗試傳遞訊息？ 使用何種安全性？ 它是 singlecast 還是多播？ 這些設定稱為通道的「系結」。 系結包含下列各項：

-   [**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結，識別要使用 (TCP、UDP、HTTP、NAMEDPIPE) 的傳輸通訊協定。
-   [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)，指定如何保護通道的安全。
-   設定的 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)，指定其他選擇性設定。 請參閱屬性清單的 [**WS \_ 通道 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) 。

![顯示通道屬性清單的圖表。](images/channelsandbindings.png)

## <a name="listener"></a>接聽程式

若要開始進行通訊，用戶端會建立通道物件。 但服務如何取得其通道物件？ 它會藉由建立接聽程式來執行此[動作。](listener.md) 建立接聽程式時，需要相同的系結資訊來建立通道。 一旦建立接聽程式之後，應用程式就可以接受來自接聽程式的通道。 由於應用程式可能會落在接受通道後方，因此接聽程式通常會保留已準備好接受 (的通道佇列，) 。

![顯示接聽程式佇列中通道的圖表。](images/channelaccept.png)

## <a name="initiating-communication-client"></a> (用戶端) 起始通訊

若要在用戶端上起始通訊，請使用下列順序。

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

## <a name="accepting-communication-server"></a>接受通訊 (伺服器) 

若要接受伺服器上的連入通訊，請使用下列順序。

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

## <a name="sending-messages-client-or-server"></a> (用戶端或伺服器) 傳送訊息

若要傳送訊息，請使用下列順序。

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

[**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)函式不允許串流處理，並假設主體只包含一個元素。 若要避免這些條件約束，請使用下列順序，而不是 **WsSendMessage**。

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

[**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)函式會使用序列化來寫入主體專案。 若要將資料直接寫入 XML 寫入器，請使用下列順序，而不是 **WsWriteBody**。

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

[**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader)函式會使用序列化將標頭設定為訊息的標頭緩衝區。 若要使用 XML 寫入器來寫入標頭，請使用下列順序，而不是 **WsAddCustomHeader**。

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a> (用戶端或伺服器) 接收訊息

若要接收訊息，請使用下列順序。

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

[**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)函式不允許串流處理，並假設主體只包含一個專案，而且訊息的型別 (動作和主體) 的架構都是事先知道的。 若要避免這些條件約束，請使用下列順序，而不是 **WsReceiveMessage**。

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

[**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)函式會使用序列化來讀取主體元素。 若要直接從 [XML 讀取器](xml-reader.md)讀取資料，請使用下列順序，而不是 **WsReadBody**。

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

[**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)函式會使用序列化來取得訊息的標頭緩衝區中的標頭。 若要使用 [XML 讀取器](xml-reader.md) 讀取標頭，請使用下列順序，而不是 **WsGetCustomHeader**。

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

## <a name="request-reply-client"></a>要求回復 (用戶端) 

您可以使用下列順序來執行用戶端上的要求-回復。

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

[**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)函式會假設要求和回復訊息內文的單一專案，而且訊息的型別 (動作和內文的架構) 事先知道。 為了避免這些限制，您可以手動傳送要求和回復訊息，如下列順序所示。 此序列符合傳送和接收訊息的較早順序，除非有注明。

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

## <a name="request-reply-server"></a>要求回復 (伺服器) 

若要在伺服器上接收要求訊息，請使用與上一節中所述的相同順序來接收訊息。

若要傳送回復或錯誤訊息，請使用下列順序。

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

[**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)函式會假設主體中有單一元素，但不允許串流處理。 若要避免這些限制，請使用下列順序。 這與先前用來傳送訊息的順序相同，但在初始化時，會使用 [**ws \_ 回復 \_ 訊息**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) ，而不是 **ws \_ 空白 \_ 訊息** 。

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

## <a name="message-exchange-patterns"></a>訊息交換模式

[**WS \_ 通道 \_ 型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)別會針對指定的通道，規定可能的訊息交換模式。 支援的類型會根據系結而有所不同，如下所示：

-   [**WS \_HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 要求**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 和伺服器上的 **ws \_ 通道 \_ 類型 \_ 回復** 。
-   [**WS \_TCP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工 \_ 會話**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 雙工 \_** 會話。
-   [**WS \_UDP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 輸入** 。
-   [**WS \_NAMEDPIPE \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結支援用戶端上的 [**ws \_ 通道 \_ 類型 \_ 雙工**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ，以及伺服器上的 **ws \_ 通道 \_ 類型 \_ 輸入** 。

## <a name="message-loops"></a>訊息迴圈

每個訊息交換模式都有特定的「迴圈」，可用來傳送或接收訊息。 迴圈會描述傳送/接收多個訊息所需的作業的合法順序。 這些迴圈會在以下的文法生產中描述。 「End」詞彙是傳回 **WS \_ S \_ end** 的接收 (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) ，指出通道上沒有其他可用的訊息。 平行生產會指定平行 (x & y) 該作業 x 可以與 y 同時進行。

用戶端會使用下列迴圈：

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

下列迴圈會在伺服器上使用：

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

使用伺服器上的 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 系結時，必須先成功接收才能傳送，即使通道 [**類型為 WS \_ 通道類型的 \_ \_ 雙工 \_ 會話**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)，仍允許傳送。 在第一次接收之後。 套用一般迴圈。

請注意， [**ws \_ 通道 \_ 類型 \_ 要求**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 和 **WS \_ 通道 \_ 類型 \_ 回復** 的通道可以用來傳送和接收單向訊息 (以及標準要求-回復模式) 。 若要完成此作業，請關閉回復通道而不傳送回復。 在此情況下，要求通道上將不會收到任何回復。 使用伺服器上的 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ \_ 安全性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系 **結來 \_ \_ 結束** 的傳回值，需要成功接收才能傳送，即使通道類型為 **WS \_ 通道類型的 \_ \_ 雙工會 \_ 話**，仍允許傳送。 第一次接收時，會套用一般迴圈。

將會傳回，表示沒有可用的訊息。

用戶端或伺服器迴圈可能會使用多個通道實例，以平行方式完成。

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>訊息篩選

伺服器通道可能會篩選出不適合應用程式的接收訊息，例如建立 [安全性內容](security-context.md)的訊息。 在這種情況下，會從 [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)傳回 **WS \_ S \_ END** ，而該通道上將不會提供任何應用程式訊息。 不過，這並不表示用戶端想要結束與伺服器的通訊。 其他通道上可能會有更多的訊息。 請參閱 [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel)。

## <a name="cancellation"></a>取消

[**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)函式是用來取消通道的暫止 IO。 此 API 不會等候 IO 作業 (的) 完成。 如需詳細資訊，請參閱 **WsAbortChannel** 的 [**WS \_ 通道 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)狀態圖表和檔。

[**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API 可用來取消接聽程式的暫止 IO。 此 API 不會等候 IO 作業 (的) 完成。 中止接聽程式也會導致所有暫止的接受中止。 如需詳細資訊，請參閱 WS 接聽程式 [**\_ \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) 狀態圖和 **WsAbortListener** 。

## <a name="tcp"></a>TCP

[**WS \_ tcp \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援透過 TCP 的 SOAP。 SOAP over TCP 規格是以 .NET 框架機制為基礎。

此版本不支援埠共用。 開啟的每個接聽程式都必須使用不同的埠號碼。

## <a name="udp"></a>UDP

[**WS \_ udp \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援 SOAP over udp。

UDP 系結有一些限制：

-   不支援安全性。
-   訊息可能會遺失或重複。
-   僅支援一種編碼： [**WS \_ 編碼 \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)。
-   訊息基本上會限制為64k，如果大小超過網路的 MTU，通常會有更大的可能遺失。

## <a name="http"></a>HTTP

[**WS \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援 SOAP over HTTP。

若要控制用戶端和伺服器上的 HTTP 特定標頭，請參閱 [**WS \_ HTTP \_ MESSAGE \_ MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)。

若要在伺服器上傳送和接收非 SOAP 訊息，請針對 [**ws \_ 通道 \_ 屬性 \_ 編碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)使用 [**ws \_ 編碼 \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) 。

## <a name="namedpipes"></a>NAMEDPIPES

[**WS \_ NAMEDPIPE \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結支援透過具名管道的 SOAP，允許使用 NetNamedPipeBinding 與 Windows Communication Foundation (WCF) 服務進行通訊。

## <a name="correlating-requestreply-messages"></a>相互關聯要求/回復訊息

要求/回復訊息會以下列兩種方式之一相互關聯：

-   相互關聯是使用通道做為相互關聯機制來完成。 例如，使用 [**ws \_ 定址 \_ 版本 \_ 傳輸**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 和 [**WS \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結時，要求訊息的回復會與要求相互關聯，而這就是 HTTP 回應的實體主體。
-   相互關聯是使用 MessageID 和 RelatesTo 標頭來完成。 即使使用 [**ws \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結) ，此機制也可搭配 [**Ws-addressing \_ \_ 版本 \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)和 **ws \_ 定址 \_ 版本 \_ 0 \_ 9** (使用。 在此情況下，要求訊息會包含 MessageID 標頭。 回應訊息包含具有要求 MessageID 標頭值的 RelatesTo 標頭。 RelatesTo 標頭可讓用戶端將回應與它所傳送的要求相互關聯。

下列通道層 Api 會根據通道的 [**WS \_ 定址 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 自動使用適當的相互關聯機制。

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

如果未使用這些 Api，可以使用 [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) 或 [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)以手動方式新增和存取標頭。

## <a name="custom-channels-and-listeners"></a>自訂通道和接聽程式

如果預先定義的通道系結組不符合應用程式的需求，則在建立通道或接聽程式時，可以藉由指定 [**WS \_ 自 \_ 定義 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結來定義自訂通道和接聽程式的執行。 通道/接聽程式的實際實作為透過 [**WS \_ 通道 \_ 屬性 \_ 自訂 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) 或 ws 接聽程式 [**\_ \_ 屬性 \_ 自訂 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) 接聽程式回呼屬性指定為一組回呼。 建立自訂通道或接聽程式之後，結果會是可以與現有 Api 搭配使用的[ws \_ 通道](ws-channel.md)或 ws 接聽程式物件。 [ \_ ](ws-listener.md)

自訂通道和接聽程式也可以搭配服務 Proxy 和 [服務主機](service-host.md)使用，方法是在 [**ws \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結列舉中指定 **ws \_ 自訂 \_ 通道 \_** 系結值，並在建立服務 Proxy 或服務主機時，指定 ws [**通道屬性自訂 \_ \_ \_ \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)和 ws 接聽程式 [**\_ \_ 屬性 \_ 自訂 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)接聽程式回呼屬性。

## <a name="security"></a>安全性

通道可讓您透過下列屬性限制作業的各種層面所使用的記憶體數量：

-   [**WS \_通道 \_ 屬性的 \_ 最大 \_ 緩衝 \_ 訊息 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 最大 \_ 資料流程處理 \_ 訊息 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 最大 \_ 資料流程處理 \_ 開始 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 最大 \_ HTTP \_ 要求 \_ 標頭 \_ 緩衝區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 最大 \_ 會話 \_ 字典 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)。

這些屬性具有預設值，在大部分情況下都是保守且安全的。 預設值和對它們所做的任何修改都應謹慎地針對可能會導致遠端使用者拒絕服務的潛在攻擊媒介進行評估。

通道可讓您透過下列屬性來設定作業各個層面的超時值：

-   [**WS \_通道 \_ 屬性 \_ 連接 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 傳送 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 接收 \_ 回應 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 接收 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 解析 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)，
-   [**WS \_通道 \_ 屬性 \_ 關閉 \_ 超時**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)。

這些屬性具有預設值，在大部分情況下都是保守且安全的。 增加超時值會增加遠端方可以存留本機資源的時間量，例如記憶體、通訊端，以及執行同步 i/o 的執行緒。 應用程式應該評估預設值，並在增加時間時小心使用，因為它可能會開啟可能會導致遠端電腦拒絕服務的潛在攻擊媒介。

使用 WWSAPI 通道 API 時，應謹慎評估的一些其他設定選項和應用程式設計考慮：

-   使用通道/接聽程式層時，會由應用程式負責在伺服器端建立和接受通道。 同樣地，應用程式會在用戶端上建立並開啟通道。 應用程式應該對這些作業加上上限，因為每個通道都會耗用記憶體和其他有限的資源，例如通訊端。 當建立通道以回應遠端方所觸發的任何動作時，應用程式應該特別小心。
-   應用程式會由應用程式撰寫邏輯來建立通道並接受這些通道。 每個通道都會耗用有限的資源，例如記憶體和通訊端。 應用程式的上限應該是其願意接受的通道數目上限，或者遠端方可以進行許多連線，進而導致 OOM，因而導致阻絕服務。 它也應該使用較短的時間，主動接收來自這些連接的訊息。 如果沒有收到任何訊息，則作業將會超時，且應該釋放連接。
-   應用程式會透過解讀 ReplyTo 或 FaultTo SOAP 標頭來傳送回復或錯誤。 安全做法是只接受「匿名」的 ReplyTo 或 FaultTo 標頭，這表示現有的連接 (TCP、HTTP) 或來源 IP (UDP) 應該用來傳送 SOAP 回復。 在建立資源 (例如通道) 來回複不同的位址時，應用程式應該要特別小心，除非該訊息是由可以說出回復傳送目的地位址的合作物件所簽署。
-   在通道層中完成的驗證無法取代透過安全性達成的資料完整性。 應用程式必須依賴 WWSAPI 的安全性功能，以確保它會與受信任的實體通訊，而且也必須依賴安全性以確保資料完整性。

同樣地，使用 WWSAPI 訊息 API 時，應謹慎評估訊息設定選項和應用程式設計考慮：

-   用來儲存訊息標頭的堆積大小，可以使用 [**WS \_ message \_ PROPERTY property \_ 堆積 \_ PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) 屬性來設定。 提高此值可讓訊息的標頭耗用更多記憶體，這可能會導致 OOM。
-   Message 物件的使用者必須瞭解標頭存取 Api 是 O (n) 與訊息中的標頭數目有關，因為它們會檢查是否有重複的專案。 在訊息中需要許多標頭的設計可能會導致過多的 CPU 使用量。
-   您可以使用 [ [**WS \_ 訊息 \_ 屬性 \_ 最大 \_ 處理 \_ 標頭**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) ] 屬性來設定訊息中的標頭數目上限。 此外，也有根據訊息堆積大小的隱含限制。 增加這兩個值可提供更多的標頭，以在使用標頭存取 Api) 時，將尋找標頭所需的時間 (。

 

 





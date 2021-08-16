---
title: 錯誤
description: 錯誤訊息是用來傳達有關遠端端點失敗的錯誤資訊。
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Windows 的錯誤 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cd9e28e9ec9ce2f3068643d44306f542eebabb9b0b0c8860b15e9e986b49b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841768"
---
# <a name="faults"></a>錯誤

錯誤訊息是用來傳達有關遠端端點失敗的錯誤資訊。 錯誤訊息就像任何其他訊息，但訊息本文的格式有標準格式。 基礎結構通訊協定（例如 WS-ADDRESSING）以及較高層級的應用程式協定都可以使用錯誤。

-   [概觀](#overview)
-   [在服務中產生錯誤](#generating-faults-in-a-service)
-   [處理用戶端上的錯誤](#handling-faults-on-a-client)
-   [使用錯誤與訊息](#using-faults-with-messages)

## <a name="overview"></a>概觀

錯誤訊息主體的內容會使用 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構在此 API 中表示。 雖然錯誤有一組固定的欄位，可用來提供有關失敗的資訊 (例如識別錯誤類型的 [**ws \_ \_ 錯誤碼**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) ，以及包含描述錯誤) 之文字的 [**ws \_ 錯誤 \_ 原因**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) ，它也會包含一個詳細資料欄位，可用來指定與錯誤相關的任意 XML 內容。

## <a name="generating-faults-in-a-service"></a>在服務中產生錯誤

服務通常會因為處理要求時發生一些錯誤而傳送錯誤。 此 API 所使用的模型是服務中遇到處理錯誤的程式碼將會在 [WS \_ error](ws-error.md) 物件中捕捉必要的錯誤資訊，然後在呼叫鏈中較高層級的程式碼將會使用在較低層所捕捉的資訊來傳送錯誤。 此配置可讓傳送錯誤的程式碼與錯誤狀況對應至錯誤的方式隔離，同時仍然允許傳送豐富的錯誤資訊。

下列屬性可以與 [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) 搭配使用，以捕獲 [WS \_ ERROR](ws-error.md) 物件的錯誤資訊：

-   [**WS \_錯誤 \_ 的 \_ 屬性 \_ 動作**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。 這會指定要用於錯誤訊息的動作。 如果未指定此值，則會提供預設動作。
-   [**WS \_錯誤 \_ \_ 屬性 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)錯誤。 這包含在錯誤訊息主體中傳送的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構。
-   [**WS \_錯誤 \_ 的 \_ 屬性 \_ 標頭**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。 某些錯誤包含訊息標頭，這些訊息標頭會新增至錯誤訊息，以傳達與要求訊息標頭相關的處理失敗。 這個屬性可以用來指定包含要加入錯誤訊息之標頭的 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md) 。

任何新增至 [WS \_ error](ws-error.md) 物件的錯誤字串，都會當做傳送的錯誤中的文字使用。 您可以使用 [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)將錯誤字串新增至 error 物件。

[**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)函數可以用來設定 [WS \_ ERROR](ws-error.md)物件的這些屬性。

若要設定 [WS \_ ERROR](ws-error.md) 物件中儲存之錯誤的詳細資料，請使用 [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) 函數。 您可以使用此函式將任意 XML 內容與錯誤相關聯。

[服務主機](service-host.md)會使用[WS \_ ERROR](ws-error.md)物件中的上述資訊自動傳送錯誤。 [**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)屬性可用來控制將如何傳送錯誤的詳細資訊。

如果在通道層處理，則可以使用 [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)傳送 [WS \_ ERROR](ws-error.md)物件的錯誤。

## <a name="handling-faults-on-a-client"></a>處理用戶端上的錯誤

如果用戶端在使用 [服務 Proxy](service-proxy.md) 或透過 [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) 或 [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)時收到錯誤，則會傳回 **WS \_ E 端點錯誤 \_ \_ \_ 接收** 錯誤。  (如需詳細資訊，請參閱[Windows Web 服務傳回值](windows-web-services-return-values.md)。 ) 這些函式也會以收到的錯誤相關資訊，填入提供給呼叫的[WS \_ ERROR](ws-error.md)物件。

您可以使用 [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)來查詢 [WS \_ ERROR](ws-error.md)物件的下列屬性，以取得所收到之錯誤的相關資訊：

-   [**WS \_錯誤 \_ 的 \_ 屬性 \_ 動作**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)。 這會指定錯誤訊息的動作值。
-   [**WS \_錯誤 \_ \_ 屬性 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)錯誤。 這包含從錯誤訊息主體還原序列化的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構。

錯誤可能會在錯誤的詳細資料中包含任意的其他 XML 內容。 您可以使用 [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) 函式來存取此函數。

## <a name="using-faults-with-messages"></a>使用錯誤與訊息

下一節適用于直接處理錯誤訊息主體的內容時。

錯誤訊息主體的內容是由標準的 [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) 結構所表示，它具有序列化的內建支援。

例如，下列程式碼可以用來將錯誤寫入訊息主體：

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

下列程式碼可以用來讀取訊息本文中的錯誤：

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

為了知道接收的訊息是否為錯誤，可以參考 [**WS \_ message \_ 屬性 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) 。 這個屬性是根據主體中的第一個元素是否為 [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) 或 [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)期間的錯誤元素所設定。

若要在指定 [ws \_ 錯誤時](ws-error.md)建立 [**\_ Ws**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)錯誤，請使用 [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)函數。

下列列舉是錯誤的一部分：

-   [**WS \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**WS 錯誤的 \_ \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

下列函數是錯誤的一部分：

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

下列結構是錯誤的一部分：

-   [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**WS \_ \_ 錯誤碼**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**WS \_ 錯誤 \_ 詳細資料 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**WS \_ 錯誤 \_ 原因**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 





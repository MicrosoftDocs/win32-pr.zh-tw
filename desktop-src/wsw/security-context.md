---
title: 安全性內容
description: 安全性內容可讓您根據 SecureConversation 來建立訊息安全性內容。
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- 安全性內容原生-Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316789"
---
# <a name="security-context"></a>安全性內容

安全性內容可讓您根據 SecureConversation 來建立訊息安全性內容。 接著，該內容可以用來保護訊息的安全，作為單次安全性的替代方案，其中會針對每個要求傳輸認證。 在交換多個訊息時，所建立的安全性內容是更有效率的訊息安全方法。


安全性內容需要有啟動程式安全性認證，用來保護內容中傳送的訊息。 [**Ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結、 [**ws \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)系結，以及 ws 使用者 [**\_ 名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)系結結構可用於此用途。

安全性內容是一種訊息安全性功能，而且是透過訊息安全性系結來設定。

## <a name="client"></a>用戶端

在用戶端上，安全性內容會系結至特定通道。 它是使用 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結來設定。 內容的行為和存留期是由通道所決定。 在通道上傳送第一個訊息時，就會建立安全性內容。 之後，內容會以可設定的間隔主動更新。 如果伺服器傳回的錯誤指出內容需要更新，則會在傳送下一個訊息時更新內容。 如果通道處於開啟狀態，則關閉通道時，會取消訊息的內容。

## <a name="server"></a>伺服器

在伺服器上，安全性內容的設定方式與用戶端上的設定方式相同。 但是，它並不會系結至任何特定通道。 相反地，針對具有 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 系結集的接聽程式所建立的所有通道，都能夠接收訊息，其中包含在該接聽程式的通道上建立的任何安全性內容。

當訊息抵達支援安全性內容的通道時，該訊息所使用的內容可以藉由呼叫 [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) 函數與 [**WS \_ message \_ 屬性 \_ 安全性 \_ 內容**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)來取得。 抓取的值可以搭配 [**WsRevokeSecurityCoNtext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) 和 [**WsGetSecurityCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)使用。

## <a name="metadata"></a>中繼資料

[**WS \_ 安全性 \_ 內容訊息安全性系結 \_ \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)結構是用來從中繼資料中解壓縮安全性內容原則。 如需詳細資訊，請參閱 [中繼資料匯入](metadata-import.md)。

下列 API 專案會搭配安全性內容使用。

| 列舉型別                                                                    | 描述                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**WS \_ 安全性 \_ 上下文 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | 識別安全性內容物件的屬性。 |



 



| 函式                                                             | 描述                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | 取得指定之安全性內容的屬性。 |
| [**WsRevokeSecurityCoNtext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | 撤銷安全性內容。                        |



 



| Handle                                           | Description                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [WS \_ 安全性 \_ 內容](ws-security-context.md) | 用來參考安全性內容物件的不透明類型。 |



 



| 結構                                                               | Description                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**WS \_ 安全性 \_ 上下文 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | 定義 [WS \_ 安全性 \_ 內容](ws-security-context.md)的屬性。 |



 

 

 





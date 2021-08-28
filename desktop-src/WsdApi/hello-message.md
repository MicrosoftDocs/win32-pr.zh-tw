---
description: 用來在網路上宣告裝置或服務是否存在的 WS-Discovery 訊息。
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Hello 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3fe850c4df51fba75c33e202a0bd742226cfb38
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882567"
---
# <a name="hello-message"></a>Hello 訊息

Hello 訊息是用來在網路上宣告裝置或服務是否存在的 WS-Discovery 訊息。 您也可以在其他案例中傳送 Hello 訊息。 如需 Hello 訊息的詳細資訊，請參閱 [WS 探索規格](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的4.1 節。

UDP 多播會將 Hello 訊息傳送到埠3702。 此訊息為未經授權。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列 SOAP 訊息會顯示範例 Hello 訊息。

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:0f5d604c-81ac-4abc-8010-51dbffad55f2
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="14">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Hello>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
        <wsd:Types>wsdp:Device</wsd:Types>
        <wsd:MetadataVersion>2</wsd:MetadataVersion>
    </wsd:Hello>
</soap:Body>
```

Hello 訊息具有下列焦點點。



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>對焦點</th>
<th>XML</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>您好</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
&lt;/wsa:Action&gt;</code></pre></td>
<td>Hello SOAP 動作會將訊息識別為 Hello 訊息。</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>包含應用程式順序資訊，這有助於維護訊息的順序，即使是依序接收訊息也是如此。 AppSequence 會依照 <a href="appsequence-validation-rules.md">AppSequence 驗證規則</a>中的說明進行驗證。</td>
</tr>
<tr class="odd">
<td>位址</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>包含端點位址。 <a href="resolve-message.md">解析</a>訊息中可能會參考此位址。</td>
</tr>
<tr class="even">
<td>類型</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>包含主機所公告的 WS-Discovery 類型。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料 Exchange 訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[再見訊息](bye-message.md)
</dt> </dl>

 

 




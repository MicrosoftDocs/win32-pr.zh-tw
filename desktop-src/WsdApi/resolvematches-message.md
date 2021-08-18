---
description: 為了回應用戶端所傳送的 WS-Discovery 訊息會由相符的服務解析訊息。
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: ResolveMatches 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1daffe985f3956e57ad69fd7c4fc4d199f0b24bd5fdab5677b7ef83765e5fcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756798"
---
# <a name="resolvematches-message"></a>ResolveMatches 訊息

ResolveMatches 訊息是為了回應用戶端的 [解析](resolve-message.md) 訊息而傳送的 WS-Discovery 訊息（由相符的服務）。 如需 ResolveMatches 訊息的詳細資訊，請參閱 [WS 探索規格](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的6.2 節。

ResolveMatches 訊息會由 UDP 單播傳送到埠 3702 (傳送用戶端 [解析](resolve-message.md) 訊息的埠) 。 ResolveMatches 必須在解析訊息的4秒內傳送;否則，Windows 防火牆可能會捨棄封包。

任何傳送 [解析](resolve-message.md) 訊息的 DPWS 應用程式都會收到 ResolveMatches 訊息。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列 SOAP 訊息會顯示範例 ResolveMatches 訊息。

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

ResolveMatches 訊息具有下列焦點點。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>對焦點</th>
<th>XML</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
</wsa:Action></code></pre></td>
<td>ResolveMatches SOAP 動作會將訊息識別為 ResolveMatches 訊息。</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:RelatesTo></code></pre></td>
<td>服務回應之訊息的識別碼。 此標頭符合 <a href="resolve-message.md">解析</a> 訊息中的 MessageId。</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
</wsd:AppSequence></code></pre></td>
<td>包含應用程式順序資訊，這有助於維護訊息的順序，即使是依序接收訊息也是如此。 AppSequence 會依照 <a href="appsequence-validation-rules.md">AppSequence 驗證規則</a>中的說明進行驗證。</td>
</tr>
<tr class="even">
<td>位址</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>包含正在解析之端點的位址。</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs 是可用來在用戶端與服務之間進行通訊的傳輸位址。 Addrs 會依照 <a href="xaddr-validation-rules.md">XAddr 驗證規則</a>中的說明進行驗證。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料 Exchange 訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[解析訊息](resolve-message.md)
</dt> </dl>

 

 




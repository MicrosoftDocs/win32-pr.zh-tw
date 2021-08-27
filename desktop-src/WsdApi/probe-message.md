---
description: 用戶端用來依服務類型搜尋網路服務的 WS-Discovery 訊息。
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: 探查訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f186de4f68faceca096ddaa231b57d1112bc1e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879851"
---
# <a name="probe-message"></a>探查訊息

探查訊息是用戶端用來在網路上依服務類型搜尋服務的 WS-Discovery 訊息。 如需探查訊息的詳細資訊，請參閱 [WS 探索規格](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的5.2 節。

UDP 多播會將探查訊息傳送到埠3702。 不支援單播探查訊息。

DPWS 用戶端會傳送探查訊息。 下列清單會顯示 WSDAPI 傳送探查訊息的案例。

-   函數探索用戶端傳送探查訊息。
-   呼叫 [**IWSDiscoveryProvider：： SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) 的 WSDAPI 用戶端會傳送探查訊息。
-   呼叫 [**IWSDiscoveryProvider：： SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) 的 WSDAPI 用戶端會傳送探查訊息。
-   使用導向探索的應用程式會透過 HTTP 或 HTTPS 傳送探查訊息。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列 SOAP 訊息會顯示範例探查訊息。

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

探查訊息具有下列焦點點。



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
<td>探查</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
&lt;/wsa:Action&gt;</code></pre></td>
<td>探查 SOAP 動作會將訊息識別為探查訊息。</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:MessageID&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:MessageID&gt;</code></pre></td>
<td>包含 <a href="probematches-message.md">ProbeMatches</a> 訊息中的 RelatesTo 元素所參考的訊息識別碼。</td>
</tr>
<tr class="odd">
<td>類型</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>包含用戶端搜尋的 WS-Discovery 類型。 這個元素不能是空的。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料 Exchange 訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[ProbeMatches 訊息](probematches-message.md)
</dt> </dl>

 

 




---
description: 用來要求中繼資料的 WS-Transfer 訊息。
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: 取得 (中繼資料交換) HTTP 要求和訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ad240a51fdbabf4184b8769f4e3cca6daa4244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986859"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>取得 (中繼資料交換) HTTP 要求和訊息

Get 訊息是用來要求中繼資料的 WS-Transfer 訊息。 如需取得訊息的詳細資訊，請參閱 [WS-傳輸規格](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf)的3.1 節。 因為中繼資料交換是透過 HTTP 進行，所以 Get 訊息是 HTTP 要求的承載。

DPWS 用戶端傳送 Get 訊息。 函數探索用戶端、呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)的 wsdapi 用戶端，以及呼叫 [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) 的 wsdapi 用戶端會傳送此訊息。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列範例顯示範例 Get HTTP 要求。

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Get HTTP 要求具有下列焦點點。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>對焦點</th>
<th>標題列</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL 路徑</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>已張貼 Get HTTP 要求的 URL 路徑。</td>
</tr>
<tr class="even">
<td>主機和埠</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>導向 Get HTTP 要求的主機和埠。</td>
</tr>
</tbody>
</table>



 

下列 SOAP 訊息顯示範例取得訊息。

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Get 訊息具有下列焦點點。



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
<td>收件者</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:To>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:To></code></pre></td>
<td>要求中繼資料之裝置的識別碼。</td>
</tr>
<tr class="even">
<td>Get</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>Get SOAP 動作會將訊息識別為取得訊息。</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>包含 <a href="getresponse--metadata-exchange--message.md">GetResponse</a> 訊息中所參考的訊息識別碼。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料交換訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[GetResponse 訊息](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 




---
description: 用戶端用來依名稱搜尋網路服務的 WS-Discovery 訊息。
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: 解析訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed3ab1778fada267a72207309eb8cb515727d5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627764"
---
# <a name="resolve-message"></a>解析訊息

解析訊息是用戶端用來依名稱搜尋網路服務的 WS-Discovery 訊息。 用戶端只會在 HTTP 訊息 (（例如 [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange 要求或) 傳送的服務訊息）時傳送解析訊息。 如需有關解決訊息的詳細資訊，請參閱 [WS 探索規格](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)的6.1 節。

UDP 多播會將解析訊息傳送到埠3702。 不支援單播解析訊息。

DPWS 用戶端會傳送解析訊息。 下列清單會顯示 WSDAPI 傳送解析訊息的案例。

-   如果 [ProbeMatches](probematches-message.md) 訊息中未包含任何 XAddrs，則函式探索用戶端會傳送解析訊息。
-   呼叫 [**IWSDiscoveryProvider：： SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) 方法的用戶端會傳送解析訊息。
-   如果將邏輯裝置位址傳遞給 *pszDeviceId*，則呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)的用戶端可能會傳送解析訊息。
-   如果函式是以設定為 **Null** 的 pDeviceAddress 參數呼叫，則呼叫 [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced)的用戶端會傳送解析訊息。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列 SOAP 訊息顯示範例解析訊息。

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

解析訊息具有下列焦點點。



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
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>解決</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>解析 SOAP 動作會將訊息識別為解析訊息。</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>包含 <a href="resolvematches-message.md">ResolveMatches</a> 訊息中所參考的訊息識別碼。</td>
</tr>
<tr class="odd">
<td>位址</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>包含正在解析之端點的位址。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料 Exchange 訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[ResolveMatches 訊息](resolvematches-message.md)
</dt> </dl>

 

 




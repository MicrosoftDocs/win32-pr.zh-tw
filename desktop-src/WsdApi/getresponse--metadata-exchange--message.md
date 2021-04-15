---
description: 用來回應中繼資料要求的 WS-Transfer 訊息。
ms.assetid: aff05317-35db-4ea6-9692-1e09e4682fe7
title: GetResponse (中繼資料交換) 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b91546076698f17a25b8a87444ae3eca71d65a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192911"
---
# <a name="getresponse-metadata-exchange-message"></a>GetResponse (中繼資料交換) 訊息

GetResponse 訊息是用來回應中繼資料要求的 WS-Transfer 訊息。 如需有關 GetResponse 訊息的詳細資訊，請參閱 [WS-傳輸規格](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf)的3.1 節。

任何傳送 [Get](get--metadata-exchange--http-request-and-message.md) 訊息的 DPWS 應用程式都會收到 GetResponse 訊息。

> [!Note]  
> 本主題說明 WSDAPI 用戶端和主機所產生的 DPWS 訊息範例。 WSDAPI 會剖析並接受其他不符合此範例的 DPWS 相容訊息。 請勿使用此範例來確認 DPWS 互通性;請改用 [ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

 

下列 SOAP 訊息會顯示範例 GetResponse 訊息。

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof"
    xmlns:sim="https://schemas.example.org/SimpleService"
    xmlns:att="https://schemas.example.org/AttachmentService"
    xmlns:eve="https://schemas.example.org/EventingService">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:119dcdf5-fc0d-4d40-bf1f-de52dc292744
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:RelatesTo>
</soap:Header>
<soap:Body>
    <wsx:Metadata>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice">
            <wsdp:ThisDevice>
                <wsdp:FriendlyName>
                    WSDAPI Basic Interop Server
                </wsdp:FriendlyName>
                <wsdp:FirmwareVersion>alpha</wsdp:FirmwareVersion>
                <wsdp:SerialNumber>1</wsdp:SerialNumber>
            </wsdp:ThisDevice>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel">
            <wsdp:ThisModel>
                <wsdp:Manufacturer>
                    Microsoft
                </wsdp:Manufacturer>
                <wsdp:ManufacturerUrl>
                    https://www.microsoft.com/
                </wsdp:ManufacturerUrl>
                <wsdp:ModelName>
                    WSDAPI Interop device
                </wsdp:ModelName>
                <wsdp:ModelNumber>0.1</wsdp:ModelNumber>
                <wsdp:ModelUrl>
                    https://www.microsoft.com/
                </wsdp:ModelUrl>
                <wsdp:PresentationUrl>
                    https://www.microsoft.com/
                </wsdp:PresentationUrl>
            </wsdp:ThisModel>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship">
            <wsdp:Relationship Type="https://schemas.xmlsoap.org/ws/2006/02/devprof/host">
                <wsdp:Host>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleDeviceType</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleDevice
                    </wsdp:ServiceId>
                </wsdp:Host>
                <wsdp:Hosted>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleService</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleService1
                    </wsdp:ServiceId>
                </wsdp:Hosted>
            </wsdp:Relationship>
        </wsx:MetadataSection>
    </wsx:Metadata>
</soap:Body>
</soap:Envelope>
```

GetResponse 訊息具有下列焦點點。



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GetResponse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
</wsa:Action></code></pre></td>
<td>GetResponse SOAP 動作會將訊息識別為 GetResponse 訊息。</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:RelatesTo></code></pre></td>
<td>裝置回應之訊息的識別碼。 此標頭符合 <a href="get--metadata-exchange--http-request-and-message.md">Get</a> 訊息中的 MessageID。</td>
</tr>
<tr class="odd">
<td>位址</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>包含此裝置上所裝載之服務的端點位址。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料交換訊息](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[取得訊息](get--metadata-exchange--http-request-and-message.md)
</dt> </dl>

 

 




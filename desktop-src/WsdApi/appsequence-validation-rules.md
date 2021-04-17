---
description: WS-Discovery 宣告和回應訊息中包含的資訊 (Hello、ProbeMatches 和 ResolveMatches) 。
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: AppSequence 驗證規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513056"
---
# <a name="appsequence-validation-rules"></a>AppSequence 驗證規則

WS-Discovery 宣告和回應訊息中包含的資訊 ([Hello](hello-message.md)、 [ProbeMatches](probematches-message.md)和 [ResolveMatches](resolvematches-message.md)) 。 這項資訊會在這些訊息傳遞給堆疊上方的元件之前，由 WSDAPI 處理和驗證 (例如網路總管或呼叫 WSDAPI) 的應用程式。

下列 XML 會顯示範例 AppSequence 元素。 Wsd 前置詞是指命名空間 `https://schemas.xmlsoap.org/ws/2005/04/discovery` 。

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI 會忽略過時的訊息。 針對每個裝置 () SOAP 主體中的端點位址唯一識別，則 WSDAPI 會忽略 AppSequence >messagenumber 低於最後一則訊息的任何訊息。

WSDAPI 忽略過時的 XAddr 宣告。 如果 AppSequence InstanceId 低於最後一個 InstanceId，則 WSDAPI 會忽略 SOAP 主體中通告的 XAddrs。 此外，如果 InstanceId 與 previous 相同，但 MetadataVersion 低於最後一個 MetadataVersion，則 WSDAPI 會忽略 XAddrs。

WSDAPI 會忽略重複的 WS-Discovery 訊息。 如果有兩個相同的 WS-Discovery 訊息傳送至 WSDAPI，則只會處理第一個收到的訊息。 這通常只與直接呼叫 [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) 或 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 介面的應用程式有關。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 




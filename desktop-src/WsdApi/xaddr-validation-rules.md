---
description: ProbeMatches 和 ResolveMatches 訊息中包含的傳輸位址 (XAddrs) ，會在 WSDAPI 傳送 HTTP 訊息（例如中繼資料要求）之前，受到基本驗證的要求。
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: XAddr 驗證規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3b167101b6012bcf20779381993cfff4ea7ea22d35eef5397ac1349baa2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049506"
---
# <a name="xaddr-validation-rules"></a>XAddr 驗證規則

[ProbeMatches](probematches-message.md)和[ResolveMatches](resolvematches-message.md)訊息中包含的傳輸位址 (XAddrs) ，會在 WSDAPI 傳送 HTTP 訊息（例如中繼資料要求）之前，受到基本驗證的要求。

這是為了確保 XAddrs 與用戶端位於相同的子網上。

下列 XML 會顯示範例 XAddrs 元素。 Wsd 前置詞是指命名空間 `https://schemas.xmlsoap.org/ws/2005/04/discovery` 。

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

必須符合下列所有條件，HTTP 訊息才能透過網路傳送。

-   XAddrs 必須是 HTTP 或 HTTPS 位址。 系統會忽略其他架構的 XAddrs。
-   如果有任何 HTTPS XAddrs，則所有 XAddrs 都必須是 HTTPS。 包含 HTTP 和 HTTPS 位址的 XAddr 區段都是完全忽略的。 此外，裝置的端點位址必須完全符合 HTTPS XAddrs。
-   XAddrs 必須是可透過 DNS 解析的 IP 位址或主機名稱。 通常會使用 IP 位址。
-   XAddrs (中至少有一個 IP 位址，或從 XAddrs) 中所包含之主機名稱解析的 IP 位址，必須與接收 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息的介面卡位於相同的子網中。
-   第一個 XAddr 中指定的位址和埠必須是可存取的。 在建立 HTTP 連線時，WSDAPI 會嘗試連接到此位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[探索和中繼資料 Exchange 訊息模式](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 




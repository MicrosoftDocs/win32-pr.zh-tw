---
description: Web 服務的裝置設定檔 (DPWS) 主機和用戶端會透過 UDP 和 HTTP 使用一連串的 SOAP 訊息，透過網路進行通訊。
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: 探索和中繼資料 Exchange 訊息模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856790"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>探索和中繼資料 Exchange 訊息模式

Web 服務的裝置設定檔 (DPWS) 主機和用戶端會透過 UDP 和 HTTP 使用一連串的 SOAP 訊息，透過網路進行通訊。

下圖顯示 DPWS 主機與用戶端之間預期的 UDP 和 HTTP 流量的總覽。

![此圖顯示 DPWS 主機與用戶端之間的 UDP 和 HTTP 流量。](images/ws-discovery-and-metadata-exchange-message-patterns.png)

在沒有網路請求的情況下，會產生[Hello](hello-message.md)、[再見](bye-message.md)、[探查](probe-message.md)、[解析](resolve-message.md)和[取得](get--metadata-exchange--http-request-and-message.md)訊息;這些訊息是用來宣佈裝置狀態或發出搜尋要求。 系統會產生[ProbeMatches](probematches-message.md)、 [ResolveMatches](resolvematches-message.md)和[GetResponse](getresponse--metadata-exchange--message.md)訊息，以回應探查、解決和取得訊息。

[Hello](hello-message.md)、 [再見](bye-message.md)、 [Resolve](resolve-message.md)和 [ResolveMatches](resolvematches-message.md) 訊息一律會透過 UDP 進行。 同樣地， [Get](get--metadata-exchange--http-request-and-message.md) 和 [GetResponse](getresponse--metadata-exchange--message.md) 中繼資料訊息一律會透過 HTTP 或 HTTPS 進行。 [探查](probe-message.md) 和 [ProbeMatches](probematches-message.md) 訊息通常會透過 UDP 傳輸，但會透過 HTTP 或 HTTPS 連接在導向的探索案例中進行。 如需有關導向探索訊息模式的詳細資訊，請參閱 [使用導向探索來疑難排解應用程式](troubleshooting-applications-using-directed-discovery.md)。

下列清單顯示網路上一般的訊息順序。 並非所有的訊息都是強制性的。

1.  [您好](hello-message.md)
2.  [探查](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [解決](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [取得](get--metadata-exchange--http-request-and-message.md) (中繼資料交換要求) 
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [再見](bye-message.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於裝置上的 Web 服務](about-web-services-for-devices.md)
</dt> </dl>

 

 




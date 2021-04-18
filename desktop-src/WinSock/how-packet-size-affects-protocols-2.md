---
description: 有關媒體封包大小的主題中所討論的媒體封包大小問題，會影響不同的 PF \_ IPX 通訊協定。
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: 封包大小如何影響通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318379"
---
# <a name="how-packet-size-affects-protocols"></a>封包大小如何影響通訊協定

[有關媒體封包大小](about-media-packet-size-2.md)的主題中所討論的媒體封包大小問題，會影響不同的 PF \_ IPX 通訊協定。 處理各種路由器和媒體大小限制的常見策略，是在遠端工作站的網路編號符合本機工作站時使用完整媒體大小，否則會改回最小的封包大小。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

提供資料包服務;每個資料包都必須位於封包大小上限內。 Winsock 將最大的資料包封包大小設定為本機媒體封包大小，減去 IPX 標頭。 不過請記住，如果封包是路由傳送的，則可能會達到路由器限制（路由）。 請確定您的應用程式可以切換回546位元組的資料包。

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

提供資料流程和序列封包服務。 Winsock IPX/SPX 可讓資料流程和訊息跨越多個封包，因此封包大小不會限制 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)所處理的資料量。 不過，基礎媒體大小必須正確設定，否則第一個大型封包將會無法傳遞，且連接將會重設。 如果目標站在區域網路上，Winsock 會將其封包大小設定為媒體封包大小。 否則，它會預設為512個位元組。 您可以在 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 或 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept) [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)之後立即變更此大小。

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII 具有大型的網際網路封包協商功能，可維持最適合的封包大小，而不需要程式設計人員介入。 但是，如果遠端工作站不支援 SPXII 並協商至標準的 SPX，NSPROTO 的 \_ spx 規則就會生效。



| 通訊協定     | 媒體      | 類型        | 資料封包大小 |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | 乙太網路   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | 單元        |                  |
|              | Token Ring | 4 mb   |                  |
|              |            | 16 mb  |                  |
| NSPROTO \_ SPX | 乙太網路   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | 單元        |                  |
|              | Token Ring | 4 mb   |                  |
|              |            | 16 mb  |                  |



 

</dd> </dl>

 

 




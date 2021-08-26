---
description: Microsoft 網路監視器 3 (Netmon) 是用來檢查網路流量的封包分析器。
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: 下載 Netmon 和範例 DPWS 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030218"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>下載 Netmon 和範例 DPWS 篩選器

Microsoft 網路監視器 3 (Netmon) 是用來檢查網路流量的封包分析器。 必須先下載 Netmon，才能[檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)和[檢查 HTTP 中繼資料的網路追蹤 Exchange](inspecting-network-traces-for-http-metadata-exchange.md)可以遵循的疑難排解步驟。 下載 Netmon 之後，您可以使用 DPWS 篩選器來協助找出感興趣的流量。

## <a name="downloading-netmon"></a>下載 Netmon

若要下載 Netmon，請移至 [Microsoft 網路監視器](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) 並依照指示進行。 如需有關 Netmon 的詳細資訊，請參閱 [說明及支援] 知識庫中的「網路監視器3.0 的相關資訊」 [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) 。

## <a name="sample-dpws-filters"></a>範例 DPWS 篩選

有時候，WS-Discovery 和中繼資料交換疑難排解必須在忙碌的網路上進行。 範例篩選可以用來協助將 Netmon 輸出限制為感興趣的流量。 如需有關使用 Netmon 篩選器的詳細資訊，請參閱 [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) 。

下列範例顯示的篩選準則會將輸出限制為所有廣播 WS-Discovery 流量。

> [!Note]  
> 此篩選不會從堆疊中找出未回應源自埠3702之多播 WS-Discovery 訊息的流量。 如果使用這類堆疊，則必須先修改此範例篩選器再使用。

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

下列範例顯示的篩選準則會將輸出限制為預設埠上傳送至 WSDAPI 堆疊的 HTTP 訊息。

> [!Note]  
> 服務可能會從5357以外的埠傳送相關的 HTTP 訊息。 如果有興趣來自其他埠的流量，則必須先修改此範例篩選器再使用。

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

下列範例顯示的篩選準則會將輸出限制為 IPv4 多播流量。

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

下列範例顯示的篩選準則會將輸出限制為 IPv6 多播流量。

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

某些篩選準則可以合併以進一步限制結果。 下列範例顯示的篩選準則會將輸出限制為 IPv4 多播 WS-Discovery 流量。

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

使用這些篩選器時，可能會從 Netmon 結果中排除相關的流量。 當服務位於預設埠以外的埠（ (5357/5358) ，以及當 DPWS 堆疊未使用預設通訊埠回應訊息時，就會發生排除情形。 在這些情況下，必須在使用之前修改篩選。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




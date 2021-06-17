---
description: 瞭解如何檢查 HTTP 中繼資料交換的網路追蹤。 使用可顯示原始封包的網路封包分析器。
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: 檢查 HTTP 中繼資料交換的網路追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e653b0852f84382873973cd63fbd3223a245dd4
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262680"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>檢查 HTTP 中繼資料交換的網路追蹤

任何可顯示原始封包的網路封包分析器，都可以用來檢查 HTTP 中繼資料交換要求。 建議使用 Microsoft 網路監視器 3 (Netmon) 。 如需 Netmon 的詳細資訊，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。

針對使用安全通道進行通訊的用戶端和主機，此診斷程式可能不會很有用，因為訊息內容已加密。

**檢查 HTTP 中繼資料交換的網路追蹤**

1.  將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。
2.  在用戶端或主機上安裝封包分析器 (Netmon) 。
3.  設定封包分析器，以在連接主機和用戶端的網路介面卡上捕獲流量。
4.  啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。
5.  篩選結果，以隔離 WS-Discovery 和中繼資料交換流量。 若要查看範例 Netmon 篩選器，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。
    > [!Note]  
    > 此為選用步驟。

     

6.  確認用戶端與主機之間傳送的訊息符合基本流量需求。

## <a name="verifying-that-messages-meet-traffic-requirements"></a>確認訊息符合流量需求

WSDAPI 用戶端和主機必須傳送符合下列準則的訊息。 如需訊息模式的一般資訊，請參閱 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)。

-   訊息必須符合 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)主題中提供的流量需求，除非絕對確定 WS-Discovery 不會用於中繼資料交換。
-   必須在用戶端與 [ProbeMatches](probematches-message.md)或 [ResolveMatches](resolvematches-message.md)訊息的 **XAddrs** 元素中提供的第一個傳輸位址之間建立 TCP 連接。 下列清單顯示用來建立 TCP 連接的一般封包交換。
    -   用戶端會將 TCP SYN 封包傳送至指定埠上的主機。
    -   主機會將 TCP SYN/ACK 封包傳送給用戶端。
    -   用戶端會將 TCP ACK 封包傳送至指定埠上的主機。

    一旦用戶端傳送 TCP ACK 封包，就會建立 TCP 連接。 請注意，如果先前已建立 TCP 連接，則不會發生此訊息交換。
-   用戶端必須傳送有效的 [Get](get--metadata-exchange--http-request-and-message.md) HTTP 要求和訊息。
-   主機必須接聽 [Get](get--metadata-exchange--http-request-and-message.md) HTTP 要求中所指定的 URL 路徑。
-   [取得](get--metadata-exchange--http-request-and-message.md)中繼資料訊息的 **To** 專案必須存在，而且不是空的。 **To** 元素的值必須符合其中一個主機端點位址。 主機的端點位址通常會在 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息中公告。
-   主機必須傳送有效的 HTTP 回應標頭。 如果初始要求成功，回應標頭應包含 HTTP/1.1 200 狀態碼。
-   主機必須傳送有效的 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。
-   [GetResponse](getresponse--metadata-exchange--message.md)訊息的 **RelatesTo** 元素必須存在，且不得為空白。 其值必須符合對應的 [Get](get--metadata-exchange--http-request-and-message.md)訊息中 **MessageId** 元素的值。

如果由程式傳送的 HTTP 要求或中繼資料交換訊息不符合這些流量需求，則會成功識別出問題的原因，而不需要進行進一步的疑難排解步驟。 重寫程式，使其產生符合標準的訊息和要求，並重新測試程式。

如果仍然無法識別問題的來源，請洽詢 Microsoft 支援服務尋求協助。 在聯繫支援之前，請收集適當的記錄檔，以協助找出問題的根本原因。 如需詳細資訊，請參閱 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[下載 Netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




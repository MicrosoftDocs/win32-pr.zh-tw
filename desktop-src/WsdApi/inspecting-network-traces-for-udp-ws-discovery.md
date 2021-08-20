---
description: 任何可顯示原始封包的網路封包分析器都可以用來檢查 UDP WS-Discovery 封包。 建議使用 Microsoft 網路監視器 3 (Netmon) 。 如需 Netmon 的詳細資訊，請參閱下載 Netmon 和範例 DPWS 篩選器。
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: 檢查 UDP WS-Discovery 的網路追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce21e2943a37640eb091aa03c02eba0886164166b2959e31e897ee788424cd41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920752"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>檢查 UDP WS-Discovery 的網路追蹤

任何可顯示原始封包的網路封包分析器都可以用來檢查 UDP WS-Discovery 封包。 建議使用 Microsoft 網路監視器 3 (Netmon) 。 如需 Netmon 的詳細資訊，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。

**檢查 UDP WS-探索的網路追蹤**

1.  將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。
2.  在用戶端或主機上安裝封包分析器 (Netmon) 。
3.  設定封包分析器，以在連接主機和用戶端的網路介面卡上捕獲流量。
4.  啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。
5.  篩選結果以隔離 WS-Discovery 流量。 若要查看範例 Netmon 篩選器，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。
    > [!Note]  
    > 此為選用步驟。

     

6.  確認用戶端與主機之間傳送的訊息符合基本流量需求。

## <a name="verifying-that-messages-meet-traffic-requirements"></a>確認訊息符合流量需求

WSDAPI 用戶端和主機必須傳送符合下列準則的訊息。 如需訊息模式的一般資訊，請參閱[探索和中繼資料 Exchange 訊息模式](discovery-and-metadata-exchange-message-patterns.md)。

-   [探查](probe-message.md) 訊息必須由 UDP 多播傳送到埠3702。
-   [探查](probe-message.md)訊息的 **Types** 元素必須存在，而且不可以是空的。 它必須包含主機將回應的類型。
-   [ProbeMatches](probematches-message.md)訊息必須傳送給傳送[探查](probe-message.md)的 UDP 通訊埠。
-   [ProbeMatches](probematches-message.md)訊息的 **RelatesTo** 元素必須存在，且不得為空白。 其值必須符合對應 [探查](probe-message.md)訊息中 **MessageId** 元素的值。
-   如果 [ProbeMatches](probematches-message.md)訊息中包含了 **XAddrs** 元素，則必須驗證提供的傳輸位址。 如需詳細資訊，請參閱 [XAddr 驗證規則](xaddr-validation-rules.md)。
-   [ProbeMatches](probematches-message.md)訊息必須在對應[探查](probe-message.md)訊息的4秒內傳送。 Windows 防火牆可能會捨棄在探查訊息之後傳送超過4秒的 ProbeMatches 訊息。
-   如果 [ProbeMatches](probematches-message.md)訊息中未包含任何 **XAddrs** 元素，且用戶端或主機會傳送 HTTP 訊息 (例如 [取得](get--metadata-exchange--http-request-and-message.md)中繼資料交換要求或) 的服務訊息，則用戶端或主機必須透過 UDP 多播將 [解析](resolve-message.md)訊息傳送到埠3702。
-   如果傳送了 [解析](resolve-message.md) 訊息，則必須將 [ResolveMatches](resolvematches-message.md) 訊息傳送至傳送解析訊息的 UDP 通訊埠。
-   [ResolveMatches](resolvematches-message.md)訊息必須在對應的[解析](resolve-message.md)訊息的4秒內傳送。 Windows 防火牆可能會捨棄在解析訊息之後超過4秒傳送的 ResolveMatchesmessage。

如果程式所傳送的訊息不符合這些訊息需求，則會成功識別出問題的原因，而不需要進行進一步的疑難排解步驟。 重寫程式，使其產生符合標準的訊息，並重新測試程式。

如果仍然無法識別問題的來源，請洽詢 Microsoft 支援服務尋求協助。 在聯繫支援之前，請收集適當的記錄檔，以協助找出問題的根本原因。 如需詳細資訊，請參閱 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[下載 Netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




---
description: 如果泛型主機和用戶端可以在網路上看到彼此，但是實際的主機和用戶端無法，則可能是問題是在網路上端點之間傳送的訊息中。
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: 使用 WSD Debug 用戶端來驗證多播流量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831fa0583a4525c5df3a42d0ce4679d217f63e57e2c645ef429157fdf8cafbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552325"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>使用 WSD Debug 用戶端來驗證多播流量

如果泛型主機和用戶端可以在網路上看到彼此，但是實際的主機和用戶端無法，則可能是問題是在網路上端點之間傳送的訊息中。 如需泛型主機和用戶端的詳細資訊，請參閱 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。 因為完整的網路追蹤可能很難收集、篩選和讀取，所以可以使用 WSD Debug 用戶端工具來列印 WS-Discovery 訊息的多播邊。

多播模式中的 WSD Debug 用戶端只能檢查一半的訊息，因為用戶端無法列印單播訊息。 如果您有興趣的單播流量，請直接跳到 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。

此程式會顯示一個方法，顯示網路上的所有多播流量。 若只要顯示進出裝置的多播流量，請參閱下面的「 [篩選 WSD Debug 用戶端結果](#filtering-wsd-debug-client-results) 」一節。

**使用 WSD Debug 用戶端來驗證多播流量**

1.  將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。
2.  開啟命令提示字元，然後執行下列命令： **WSDDebug \_client.exe/mode 多播**
3.  啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。
4.  確認訊息正在進行多播。

如果所需的訊息顯示在 WSD Debug 用戶端輸出中，則應用程式失敗可能會位於多播訊息內容中，或是對應單播回應訊息的存在或內容中。 遵循 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)中的指示，繼續進行疑難排解。

如果在 WSD Debug 用戶端輸出中顯示必要的訊息，則可能已識別出應用程式問題的來源。 網路上可能不會傳輸多播流量。 當應用程式未正確列舉多播介面卡時，就會發生此錯誤。 應用程式必須在所有網路介面上明確地傳送多播流量;否則，可能不會針對回送介面或其他介面產生封包。 若要確認封包未出現在網路上，請遵循 [檢查網路追蹤中的 UDP ws-management](inspecting-network-traces-for-udp-ws-discovery.md) 的指示，並尋找遺失的多播訊息的辨識項。

## <a name="verifying-that-messages-are-being-multicast"></a>確認訊息正在多播

一律確認 [探查](probe-message.md) 訊息是多播。 （選擇性）確認 [Hello](hello-message.md) 和 [Resolve](resolve-message.md) 訊息是多播。 請注意，並非所有應用程式都使用解析訊息。 如需有關用戶端和主機所使用之訊息模式的詳細資訊，請參閱[使用 WSDAPI 疑難排解的](getting-started-with-wsdapi-troubleshooting.md)[探索和中繼資料 Exchange 訊息模式](discovery-and-metadata-exchange-message-patterns.md)和開始使用。

必須觸發訊息，才能依照上述步驟3所述的方式傳送訊息。 WSD Debug 用戶端會將原始的 SOAP 訊息顯示為輸出。 因為所有在多播模式中由 WSD Debug 用戶端列印的訊息都會透過多播通訊端接收，所以不會顯示訊息目的地位址。

下列範例 WSD Debug 用戶端輸出會顯示探查訊息。 元素會將 \<wsa:Action> 訊息識別為探查訊息。 檢查 \<wsa:Action> 欄位，確認接收的訊息是探查訊息。

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

下列範例 WSD Debug 用戶端輸出會顯示 Hello 訊息。 元素會將 \<wsa:Action> 訊息識別為 Hello 訊息。

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a>篩選 WSD Debug 用戶端結果

篩選 WSD Debug 用戶端結果有助於識別牽涉到裝置的事件流量。 只有在雜訊的網路上才需要篩選。

有兩種方式可以篩選結果。 啟動 WSD Debug 用戶端時，可以明確識別要篩選的 IP 位址。 或者，您可以在用戶端啟動之後指定 IP 位址。 本節將說明這兩種方法。

**若要在啟動 WSD Debug 用戶端時指定要篩選的 IP 位址**

1.  將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。
2.  收集裝置 (es) 的 IP 位址。 如果裝置有多個位址 (例如，它同時具有 IPv4 和 IPv6 位址) 必須收集所有位址。
3.  開啟命令提示字元，然後執行下列命令： **WSDDebug \_client.exe/mode 多播/ip add***<device IP>*

*<device IP>* 是 IP 位址。 下列清單顯示此 IP 位址的一些範例格式。

-   192.168.0.1
-   ：：1
-   mydevice.contoso.com

WSD Debug 用戶端會自動解析在命令提示字元中提供的主機名稱。

**若要在啟動 WSD Debug 用戶端之後篩選結果**

1.  將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。
2.  收集裝置 (es) 的 IP 位址。 如果裝置有多個位址 (例如，它同時具有 IPv4 和 IPv6 位址) 必須收集所有位址。
3.  開啟命令提示字元，然後執行下列命令： **WSDDebug \_client.exe/mode 多播**
4.  在 WSD Debug 用戶端命令提示字元中，執行下列命令： **ip add***<device IP>*
5.  重複步驟4，直到新增所有裝置 IP 位址為止。

下列程式假設已啟動 WSD Debug 用戶端，並依 IP 位址進行篩選。

**確認正在篩選正確的 IP 位址**

-   在 WSD Debug 用戶端命令提示字元中，執行下列命令： **ip 列印**

    要篩選的 IP 位址清單隨即出現。

下列程式假設已啟動 WSD Debug 用戶端，並依 IP 位址進行篩選。

**若要停用篩選**

-   在 WSD Debug 用戶端命令提示字元中，執行下列命令： **ip clear**

    所有多播流量現在都會顯示在調試輸出中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




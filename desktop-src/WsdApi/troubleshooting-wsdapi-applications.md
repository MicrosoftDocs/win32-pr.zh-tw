---
description: 列出針對 WSDAPI 應用程式進行疑難排解時要使用的診斷程式。
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: 針對其他 WSDAPI 應用程式進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996625"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>針對其他 WSDAPI 應用程式進行疑難排解

應用程式可以直接呼叫 WSDAPI 介面和函式來執行裝置探索和中繼資料交換。 這些應用程式所使用的訊息模式會有所不同。

此疑難排解指南的目標是協助 WSDAPI 應用程式開發人員成功地執行裝置 proxy。 本指南的目的並非協助您疑難排解 WSDAPI 的所有層面。 如果已成功建立裝置 proxy，且用戶端和主機可以在網路上看到彼此，則本指南無法解決應用程式的問題。 若要針對這些應用程式問題進行疑難排解，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 的指示，並聯絡 Microsoft 支援服務尋求進一步的協助。

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>針對呼叫 WSDCreateDeviceProxy 的用戶端進行疑難排解

應用程式會呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) 來建立和初始化 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) 介面的實例。 此裝置 proxy 物件可用來通告裝置上的服務，也可以用來交換中繼資料。

呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) 的應用程式一律會使用下列訊息。

-   [Get](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) 的應用程式有時會使用下列訊息。

-   [解決](resolve-message.md)
-   [ResolveMatches](resolvematches-message.md)

當邏輯裝置位址 (時，會產生 [解析](resolve-message.md)和 [ResolveMatches](resolvematches-message.md)訊息，格式 urn： uuid： {guid} ) 的裝置位址會傳遞至 *pszDeviceId*。 當實體裝置位址傳遞至 *pszDeviceId* 時，不會產生這些訊息。 當使用 Resolve 和 ResolveMatches 訊息時，會在 [Get](get--metadata-exchange--http-request-and-message.md) 和 [GetResponse](getresponse--metadata-exchange--message.md) 訊息之前傳送這些訊息。

您應使用下列診斷程式 (順序) ，以協助找出使用實體裝置位址呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) 的應用程式發生問題。

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
3.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
4.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

您應使用下列診斷程式 (順序) ，以協助找出使用邏輯裝置位址呼叫 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) 的應用程式發生問題。

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
3.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
4.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。
5.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
6.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
7.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

確認已產生 [解析](resolve-message.md) 和 [ResolveMatches](resolvematches-message.md) 訊息，並符合流量需求。 不需要在 WSD Debug 用戶端輸出或網路追蹤中尋找 [探查](probe-message.md) 或 [ProbeMatches](probematches-message.md) 訊息。

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>針對呼叫 WSDCreateDeviceProxyAdvanced 的用戶端進行疑難排解

應用程式會呼叫 [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) 來建立和初始化 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) 介面的實例。 不同于 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)， **WSDCreateDeviceProxyAdvanced** 具有用來定義裝置傳輸位址的 *pDeviceAddress* 參數。 如果指定此傳輸位址，則不需要邏輯位址解析，且不會產生 [解析](resolve-message.md) 和 [ResolveMatches](resolvematches-message.md) 訊息。

如果 *pDeviceAddress* 設定為 **Null** ，而 *pszDeviceId* 是邏輯位址，則需要解決位址，而且會產生 [解析](resolve-message.md) 和 [ResolveMatches](resolvematches-message.md) 訊息。

下列診斷程式應依序 (使用) ，以協助找出使用非 **Null**_PDeviceAddress_ 參數呼叫 [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced)的應用程式問題。 當 *pDeviceAddress* 為 **Null** 且 *pszDeviceId* 是實體位址時，也可以使用這些程式。

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
3.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
4.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

您應使用下列診斷程式 (順序) ，以協助找出應用程式的問題，並將 *pDeviceAddress* 設定為 **Null** ，並將 *pszDeviceId* 設定為邏輯位址，以找出呼叫 [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced)的應用程式問題。

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
3.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
4.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。
5.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
6.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
7.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

確認已產生 [解析](resolve-message.md) 和 [ResolveMatches](resolvematches-message.md) 訊息，並符合流量需求。 不需要在 WSD Debug 用戶端輸出或網路追蹤中尋找 [探查](probe-message.md) 或 [ProbeMatches](probematches-message.md) 訊息。

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>使用 IWSDiscoveryProvider 介面疑難排解用戶端

呼叫 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 介面的應用程式不會執行中繼資料交換。 這個介面僅供探索之用。 **IWSDiscoveryProvider** 介面上呼叫的每個方法都有不同的訊息模式和疑難排解程式。

當應用程式呼叫 [**IWSDiscoveryProvider：： SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype)時，會產生 [探查](probe-message.md) 訊息。 探查訊息會由 UDP 多播傳送到埠3702。 會產生 [ProbeMatches](probematches-message.md) 訊息以回應。 ProbeMatches 訊息是由 UDP 單播傳送，且來自埠3702。

當應用程式呼叫 [**IWSDiscoveryProvider：： SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid)時，會產生 [解析](resolve-message.md) 訊息。 UDP 多播會將解析訊息傳送到埠3702。 會產生 [ResolveMatches](resolvematches-message.md) 訊息以回應。 ResolveMatches 是由 UDP 單播傳送，且來自埠3702。

下列診斷程式應依序 (使用) ，以協助識別呼叫 [**IWSDiscoveryProvider：： SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) 或 [**IWSDiscoveryProvider：： SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid)的應用程式發生問題。 確認所呼叫 API 所產生的訊息符合流量需求。

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
3.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
4.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。

如果應用程式呼叫 [**IWSDiscoveryProvider：： SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress)，則它是導向的探索應用程式。 如需疑難排解的詳細資訊，請參閱 [使用導向探索來疑難排解應用程式](troubleshooting-applications-using-directed-discovery.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




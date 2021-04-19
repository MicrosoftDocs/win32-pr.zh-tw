---
description: 裝置上的 Web 服務 API (WSDAPI) 用來開發用戶端應用程式，以尋找和存取裝置，以及開發在 Windows Vista 和 Windows Server 2008 上執行的裝置主機和相關聯的服務。
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: WSDAPI 介面的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975028"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>WSDAPI 介面的總覽

裝置上的 Web 服務 API (WSDAPI) 用來開發用戶端應用程式，以尋找和存取裝置，以及開發在 Windows Vista 和 Windows Server 2008 上執行的裝置主機和相關聯的服務。 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal)API 和[WsdCodeGen](web-services-for-devices-code-generator.md)工具是可用於用戶端、裝置主機和服務開發的補充工具。 WSDAPI 介面可以直接用來公開 advanced 功能。

## <a name="major-wsdapi-interfaces"></a>主要 WSDAPI 介面

四個主要的 WSDAPI 介面為 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider)、 [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher)、 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)和 [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)。 如需所有 WSDAPI 介面的清單，請參閱 [ [裝置上的 Web 服務] 介面](web-services-for-devices-interfaces.md)。

## <a name="iwsdiscoveryprovider"></a>IWSDiscoveryProvider

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 用來在用戶端上執行 WS-Discovery 的功能。

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) WS-Discovery [探查](probe-message.md) 和 [解決](resolve-message.md) 訊息，以及接收 [Hello](hello-message.md)、 [再見](bye-message.md)、 [ProbeMatches](probematches-message.md)和 [ResolveMatches](resolvematches-message.md) 訊息的問題。 建立用來描述及控制特定 DPWS 裝置的 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)介面時，請使用透過 **IWSDiscoveryProvider** 介面抓取的資訊。

在建立裝置 proxy 之前，只要先解析特定的 DPWS 裝置位址，就不需要 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 介面。 必要時， [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)會自動解析裝置位址。

[函數探索](/previous-versions/windows/desktop/fundisc/fd-portal)API 可用於一般裝置和服務探索，因為 API 可以探索 DPWS 裝置以及使用其他通訊協定的裝置。 撰寫一般探索應用程式時，請考慮使用函數探索。

## <a name="iwsdiscoverypublisher"></a>IWSDiscoveryPublisher

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) 可用來在目標服務（例如裝置）上執行 WS-Discovery 功能。

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) 可讓應用程式使用 WS-Discovery 的 Hello 和再見訊息發佈其存在。 此介面可讓應用程式接收探查和解析要求，以及建立和傳送 ProbeMatches 和 ResolveMatches 回應。

只要發行 [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)物件存在，就不需要 [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher)介面。 **IWSDDeviceHost** 會管理自己的 WS-Discovery 存在。

## <a name="iwsddeviceproxy"></a>IWSDDeviceProxy

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) 可用來執行用戶端的 ws 探索、透過 ws-metadataexchange 和控制功能。 這種功能包括選擇性的安全通道、WS-事件和附件功能。

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)介面具有下列三種用途。

-   視需要解析邏輯裝置位址。
-   起始對裝置的中繼資料要求，以列舉服務的類型和位址。
-   提供 [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) 物件的來源，可用來將控制訊息發出至裝置上的特定服務。

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)物件通常是在 [WsdCodeGen](web-services-for-devices-code-generator.md)所產生的程式碼內建立和使用。

## <a name="iwsddevicehost"></a>IWSDDeviceHost

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) 可用來執行裝置端的 ws 探索、Ws-透過 ws-metadataexchange 和服務裝載功能。 託管服務可能會回應控制訊息，並且可能支援安全通道、WS-事件和附件功能。

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)介面具有下列用途。

-   裝載服務物件。
-   使用 WS 探索宣佈網路上有裝置主機存在。
-   回應 WS-MetadataExchange 要求，並描述託管服務的類型和位置。
-   將網路要求分派至服務物件。

WS-MANAGEMENT、透過 ws-metadataexchange 和 WS-Eventing 訂用帳戶管理功能完全是在裝置主機物件內處理。 必須符合下列需求，才能在裝置主機內託管服務。

-   主機必須藉由呼叫 [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost)來建立。
-   與服務相關聯的中繼資料必須註冊。
-   服務本身必須註冊。
-   裝置主機必須啟動。

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)物件通常是在 [WsdCodeGen](web-services-for-devices-code-generator.md)所產生的程式碼內建立和使用。

 

 

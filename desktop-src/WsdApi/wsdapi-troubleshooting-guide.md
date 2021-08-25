---
description: 本指南的目的是要協助使用者疑難排解在使用 WSDAPI 探索 Api、建立 WSDAPI 主機或裝置 proxy 時所發生的失敗，或使用作業系統函式 (例如功能探索或依賴 WSDAPI 的網路總管) 。
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: WSDAPI 疑難排解指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a904b2bf4072721e6c0e9c01191aa1b3d5f55224b096434062b7aa8535fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860029"
---
# <a name="wsdapi-troubleshooting-guide"></a>WSDAPI 疑難排解指南

本指南的目的是要協助使用者疑難排解在使用 WSDAPI 探索 Api、建立 WSDAPI 主機或裝置 proxy 時所發生的失敗，或使用作業系統函式 (例如 [功能探索](/previous-versions/windows/desktop/fundisc/fd-portal) 或依賴 WSDAPI 的網路總管) 。 主要目標是在用戶端和主機無法在網路上看到彼此時，協助進行疑難排解。

針對 WSDAPI 使用者，本指南包含的資訊可協助您成功地疑難排解裝置 proxy (使用 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)) 、使用 [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider))  (的探索提供者，或使用 [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher) (的探索發行者) 。

本指南假設用戶端和主機可以在受控制的環境中正確地與 WSDAPI 進行交互操作。 因此，本指南的目的並不是為了協助針對可能產生不當 WS 訊息的 DPWS 堆疊進行疑難排解。 如需有關使用 wsdapi 測試互通性的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 中的[wsdapi 基本互通性工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

在開始針對應用程式進行疑難排解之前，您應該先熟悉[Exchange 訊息模式的探索和中繼資料](discovery-and-metadata-exchange-message-patterns.md)。

本指南涵蓋下列各節。

-   [使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
-   [WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)

---
description: 本指南的目的是要協助使用者疑難排解在使用 WSDAPI 探索 Api、建立 WSDAPI 主機或裝置 proxy 時所發生的失敗，或使用作業系統函式 (例如功能探索或依賴 WSDAPI 的網路總管) 。
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: WSDAPI 疑難排解指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987452"
---
# <a name="wsdapi-troubleshooting-guide"></a>WSDAPI 疑難排解指南

本指南的目的是要協助使用者疑難排解在使用 WSDAPI 探索 Api、建立 WSDAPI 主機或裝置 proxy 時所發生的失敗，或使用作業系統函式 (例如 [功能探索](/previous-versions/windows/desktop/fundisc/fd-portal) 或依賴 WSDAPI 的網路總管) 。 主要目標是在用戶端和主機無法在網路上看到彼此時，協助進行疑難排解。

針對 WSDAPI 使用者，本指南包含的資訊可協助您成功地疑難排解裝置 proxy (使用 [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)) 、使用 [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider))  (的探索提供者，或使用 [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher) (的探索發行者) 。

本指南假設用戶端和主機可以在受控制的環境中正確地與 WSDAPI 進行交互操作。 因此，本指南的目的並不是為了協助針對可能產生不當 WS 訊息的 DPWS 堆疊進行疑難排解。 如需有關使用 WSDAPI 測試互通性的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 中的 [Wsdapi 基本互通性工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 。

開始針對您的應用程式進行疑難排解之前，您應該先熟悉 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)。

本指南涵蓋下列各節。

-   [使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
-   [WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)

---
description: TAPI 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制。
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: '關於電話語音服務提供者 (TSP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690072"
---
# <a name="about-the-telephony-service-provider-tsp"></a>關於電話語音服務提供者 (TSP) 

\[ H323 和 IPConf Tsp 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

TAPI 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制。 TAPI 應用程式使用標準化命令、TAPI 傳遞給電話語音服務提供者，而 TSP 則處理必須與裝置交換的特定命令。

下列各節簡要說明 Microsoft Windows 所提供的 Tsp：

-   [H323 TSP](h323-tsp.md)
-   [IPConf TSP](ipconf-tsp.md)
-   [核心模式設備磁碟機 TSP](kernel-mode-device-driver-tsp.md)
-   [NDIS Proxy TSP](ndis-proxy-tsp.md)
-   [遠端 TSP](remote-tsp.md)
-   [協力廠商 TSP](third-party-tsp.md)
-   [Unimodem TSP](unimodem-tsp.md)

如需詳細資訊，請參閱目標作業系統的資源套件。 專用通訊裝置的協力廠商 Tsp 通常會由製造商提供，並會與裝置一起安裝。

下列主題說明如何建立可在 Microsoft 電話語音環境內正常運作的 TSP，以及如何建立 TSP/MSP 組：

-   [電話語音服務提供者介面 (TSPI) ](telephony-service-provider-interface-tspi-.md)
-   [TSPI 參考](tspi-reference.md)
-   [媒體服務提供者](./media-service-providers-start-page.md)

> [!Note]  
> TSP 是使用者建立的 DLL。 如果您要建立64位 Windows 平臺的 TSP，您必須將它編譯為64位 DLL 或 Dll。

 

 

 

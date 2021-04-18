---
description: TAPI 3.1 版是以 COM 為基礎的 API，可合併傳統和 IP 電話語音。 可能的應用程式範圍從使用公用交換器電話網絡的簡單語音通話 (PSTN) 到具有服務品質 (QOS) 的多播多媒體 IP 會議。
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: TAPI 3.1 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983487"
---
# <a name="tapi-31-overview"></a>TAPI 3.1 總覽

TAPI 3.1 版是以 COM 為基礎的 API，可合併傳統和 IP 電話語音。 可能的應用程式範圍從使用公用交換器電話網絡的簡單語音通話 (PSTN) 到具有服務品質 (QOS) 的多播多媒體 IP 會議。

如需有關 TAPI 3.1 IP 電話語音功能的詳細資訊，請參閱 Microsoft 網站上的「使用 TAPI 3 的 IP 電話語音」白皮書。

TAPI 3.1 有四個主要元件：

-   COM API
-   TAPI 伺服器
-   電話語音服務提供者 (Tsp) 
-   媒體串流提供者 (Msp) 

下圖說明 TAPI 3.1 架構：

![tapi 3 架構](images/callarc-gif-1.png)

API 會實作為元件物件模型的套件， (COM) 物件。 將 TAPI 移至物件導向 COM 模型，可讓開發人員以許多語言撰寫啟用 TAPI 的應用程式，例如 JAVA、Visual Basic 或 C/c + +。 使用 COM 可讓元件升級 TAPI 功能。

TAPI 伺服器程式 (TAPISRV) 將 TAPI 服務提供者介面從 TAPI 3.x 和 TAPI 2.x (TSPI) ，讓 TAPI 2.x 的電話語音服務提供者可以與 TAPI 3.x 搭配使用，以維護 TAPI 的內部狀態。 TAPISRV 會實作為 SVCHOST 內的服務進程。

[服務提供者](./tapi-service-providers.md) 會抽象化提供者特定的媒體傳輸機制。 它們通常會成對存在–電話語音服務提供者 (TSP) 用於通話控制和媒體服務提供者 (適用于媒體控制的 MSP) 。

[電話語音服務提供者](./telephony-service-providers-start-page.md) (tsp) 負責將 TAPI 的通訊協定獨立呼叫模型解析為通訊協定特定的呼叫控制機制。 TAPI 3.1 提供與 TAPI 2.1 Tsp 的回溯相容性。  (的兩個 IP 電話語音服務提供者和其相關聯的 Msp) 預設隨附于 TAPI 3.1：-323 TSP 和 IP 多播會議 TSP。

[媒體服務提供者](media-service-providers-start-page.md) (msp) 提供統一的方式來存取通話中的媒體串流，支援 DirectShow<sup>TM</sup> API 作為主要媒體串流處理常式。 TAPI Msp 會針對特定的 TSP 實行 DirectShow 介面，且所有使用 DirectShow 串流的電話語音服務都需要這些介面。 一般資料流程是由應用程式處理。

 

 

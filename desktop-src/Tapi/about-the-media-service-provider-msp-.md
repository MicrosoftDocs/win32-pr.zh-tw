---
description: " (MSP 的 TAPI 3 媒體服務提供者) 可讓應用程式對特定傳輸機制的媒體具有相當大的控制權。"
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: '關於媒體服務提供者 (MSP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f6113fa6c5fcceddaf379894d5680cbdccccec5be228041967dabb11fcc2caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872920"
---
# <a name="about-the-media-service-provider-msp"></a>關於媒體服務提供者 (MSP) 

 (MSP 的 TAPI 3 媒體服務提供者) 可讓應用程式對特定傳輸機制的媒體具有相當大的控制權。 MSP 永遠存在，與電話語音服務提供者 (TSP) 配對。 如同 TSP 是用於呼叫控制的抽象層，MSP 可控制媒體，而不需要裝置特定的程式碼撰寫。 如需 MSP/TSP 通訊的範例，請參閱 [TAPI 服務提供者總覽](./tapi-service-provider-overview.md)。

MSP 利用 TAPI 所定義的特殊終端機、串流和子資料流程介面，讓媒體控制。 [關於通話和媒體控制項](about-call-and-media-controls.md)的圖表說明這些介面如何顯示在 TAPI 3 應用程式中。

此外，MSP 可能會執行私用 [提供者特定的介面](provider-specific-interfaces.md)，而 TAPI 會匯總到公開給應用程式的標準物件。 例如，microsoft IPConf MSP （與 microsoft Windows 2000 一起安裝）會執行 [**ITParticipant**](itparticipant.md)介面，此介面會提供會議個別成員的控制項。

下列主題簡要說明可能與 Microsoft 作業系統一起安裝的 Msp。 如需設定和使用方式的詳細資訊，請參閱目標平臺的資源套件。

其他協力廠商媒體服務提供者可以針對特定的通訊協定或實體裝置來撰寫。 [媒體服務提供者介面 (MSPI) ](media-service-provider-interface-mspi-.md)說明必須執行的介面，才能讓 MSP 與 Microsoft 電話語音的元件互動。

 

 

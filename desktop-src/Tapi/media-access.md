---
description: 媒體功能與 tapi 2.2 (TAPI/C) （而不是 TAPI 3 (COM) ）不同，主要是因為 COM API 可存取媒體服務提供者 (Msp) 。
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: 媒體存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575608"
---
# <a name="media-access"></a>媒體存取

媒體功能與 tapi 2.2 (TAPI/C) （而不是 TAPI 3 (COM) ）不同，主要是因為 COM API 可存取媒體服務提供者 (Msp) 。 如需有關 Msp 的詳細資訊，請參閱 [關於 (MSP) 的媒體服務提供者 ](./about-the-media-service-provider-msp-.md)。 如需媒體串流作業的詳細資訊，請參閱 [媒體控制項](./device-control.md)。

應用程式的兩個最重要的概念是媒體類型 (或模式) 和串流。 此類型是傳輸資料的形式。 如需詳細資訊和 TAPI 定義類型的清單，請參閱 [LINEMEDIAMODE \_ 常數](linemediamode--constants.md)。 媒體資料流程是實際的資料串流。 MSP 可以提供直接的資料流程存取。 TAPI 2.2 應用程式有一些存取權，但主要是參考其他 Api 來執行這類控制項。

這些 Api 包括波形 API、通訊 API 和 Media Control 介面 (MCI) 。 波形 API 用於多媒體程式設計，而通訊 API 是平臺軟體發展工具組 (SDK) 所提供的一組通訊功能，而 MCI 則提供用來控制媒體裝置的高階一般化介面。

例如，針對線路裝置，應用程式可以使用 TAPI 2.2 來建立與另一個工作站的連線。 一旦建立連線之後，應用程式就可以在相關聯的裝置上使用波形 API (或 MCI Waveaudio API) 來播放 (傳送) 和記錄 (透過連接接收) 音訊資料。 同樣地，如果連線媒體資料流程來自數據機，則應用程式會使用通訊 API 的數據機設定延伸來控制媒體串流。

若要使用媒體串流存取線路裝置上的電話或電話來提供 TAPI 2.2，服務提供者必須同時執行電話語音 SPI 和適當的媒體串流 SPI 或裝置驅動程式介面， (的 DDI) 。 服務提供者可同時支援線路和電話。

因為這些裝置類別和媒體串流作業彼此獨立運作，所以其使用方式必須在應用層級進行協調。 共用呼叫和媒體串流的多個應用程式，可能需要在應用層級協調其活動，以防止 TAPI 和媒體串流 API 的使用狀況發生衝突。

TAPI 會報告媒體資料流程類型的變更， (語音、傳真、資料數據機等) 至參與的應用程式。 此程式有時稱為「 [*呼叫分類*](c-tapgloss.md)」。 用來決定媒體資料流程類型的機制是服務提供者的特定機制。 例如，服務提供者可以篩選媒體媒體類型的能源或色調的媒體串流，也可以使用特殊的鈴聲、透過網路在訊息中交換的資料，或是關於呼叫端或呼叫識別碼的知識，以做出這項決定。

-   [呼叫監視](call-monitoring.md)
-   [媒體控制項](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [數位收集](digit-gathering.md)
-   [產生 Inband 數位和音調](generating-inband-digits-and-tones.md)

 

 

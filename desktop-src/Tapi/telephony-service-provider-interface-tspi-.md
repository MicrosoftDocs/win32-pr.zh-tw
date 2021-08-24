---
description: 電話語音服務提供者 (TSPI) 處理通訊程式設計的裝置特定控制項。
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: '電話語音服務提供者介面 (TSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681798"
---
# <a name="telephony-service-provider-interface-tspi"></a>電話語音服務提供者介面 (TSPI) 

電話語音服務提供者 (TSPI) 處理通訊程式設計的裝置特定控制項。 TSP 必須符合電話語音服務提供者 (TSPI) ，才能在 Microsoft 電話語音環境內作為服務提供者。 TSPI 會定義由通訊設備提供的電話語音服務提供者所公開的外部函數。

TSP 作者必須熟悉 [Microsoft 電話語音總覽](./microsoft-telephony-overview.md)中的材質，其中涵蓋了一般的電話語音架構，並概述數個電話語音 api 的通用材質。 例如，本節包含會話控制作業（例如公園）的清單，其中包含每項作業的說明，並跳至相關的 TAPI 2.2、TAPI 3 和 TSPI 程式設計專案。

下列總覽涵蓋 TSP 作者需求專屬的相關內容。 請注意，撰寫 TSP 最困難的部分是裝置和作業系統特定的詳細資料，這不在本檔的討論範圍內。

TSPI 總覽分為下列幾節：

-   [一般程式設計考慮](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) 包括 DLL 需求、適當的版本處理、TAPI 執行的錯誤檢查、TSPI 函式對應至 tapi 2.2 (Tapi/C) 功能的摘要，以及 TSPI 中表示的服務層級的討論。
-   [電話語音服務提供者的生命週期](life-cycle-of-a-telephony-service-provider.md)包含 TSP 操作階段的高階摘要。
-   [裝置存取](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) 涵蓋了 TSP 如何將裝置資訊和控制項公開到 TAPI 的基本概念。
-   [會話存取](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) 涵蓋了 TAPI 在通訊會話期間預期的 TSP。
-   [媒體存取](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) 可針對媒體串流提供一組有限的控制項。 使用媒體服務提供者可以更精細地控制，而服務提供者的作者應該在可行時使用此 API。 TSPI 會提供 TSP/MSP 配對之間的通訊。
-   [電話的裝置](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85))涵蓋的補充資訊和作業，會在 TSP 處理手機組控制項時公開。 這些作業是選擇性的。
-   [電話語音服務提供程式 UI DLL 介面](the-telephony-service-provider-ui-dll-interface.md) 涵蓋的特殊函式，可讓使用者直接設定 TSP 功能的許多層面。

如需 TSPI 程式設計項目的詳細資訊，請參閱 [TSPI 參考](tspi-reference.md) 。

 

 

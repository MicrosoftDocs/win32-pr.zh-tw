---
description: TAPI 3 呼叫和媒體控制項是一組一般的 COM 物件、介面和方法，可在兩部或多部電腦之間進行呼叫。
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: 關於呼叫和媒體控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853448"
---
# <a name="about-call-and-media-controls"></a>關於呼叫和媒體控制項

TAPI 3 呼叫和媒體控制項是一組一般的 COM 物件、介面和方法，可在兩部或多部電腦之間進行呼叫。 在 TAPI 3 的內容中， *電話* 指的並非只是透過交換交換電話網絡的語音傳輸 (PSTN) ，而是指服務提供者所在的任何中度和傳輸機制：例如，在公司內部網路上執行的多媒體多播會議。

TAPI 3 呼叫和媒體控制架構中的五個主要物件是 [tapi](tapi-object.md)、 [位址](address-object.md)、 [終端](terminal-object.md)機、 [電話](call-object.md)和 [CallHub](callhub-object.md)。 此外，也已針對 [提供者特定介面](provider-specific-interfaces.md)進行布建。

下圖說明這些物件的互動方式。

![tapi 3.0 呼叫和媒體控制物件之間的互動](images/sdkobj2.png)

## <a name="features"></a>功能

-   將呼叫和媒體功能抽象化，以允許不同和看似不相容的通訊協定，將通用介面公開給應用程式。
-   根據元件物件模型 (COM) 因此，應用程式幾乎可以用任何語言來撰寫。 如果您需要有關 COM 的其他資訊，請參閱平臺軟體發展工具組 (SDK) 。
-   電話語音服務提供者所提供的呼叫控制 (Tsp) ，其可執行傳輸特定的機制。
-   媒體服務提供者所提供的媒體控制項 (Msp) 。 目前的 Msp 使用 DirectShow。 DirectShow 是一種模組化系統，稱為篩選器，以稱為篩選圖形的設定排列。 篩選圖形管理員會監看這些篩選的連接，並控制資料流程的資料流程。 如果您需要 DirectShow 的其他資訊，請參閱 Platform SDK。

 

 




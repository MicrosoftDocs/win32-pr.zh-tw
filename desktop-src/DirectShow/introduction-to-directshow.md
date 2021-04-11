---
description: DirectShow 簡介
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: DirectShow 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109069"
---
# <a name="introduction-to-directshow"></a>DirectShow 簡介

Microsoft® DirectShow®是在 Microsoft Windows®平臺上串流處理媒體的架構。 DirectShow 為多媒體串流提供高品質的捕獲和播放功能。 它支援各種不同的格式，包括先進的系統格式 (ASF) 、運動圖片專家群組 (MPEG) 、Audio-Video 交錯 (AVI) 、MPEG 音訊第3層 (MP3) 和 WAV 音效檔。 它支援根據適用于 Windows 的 Windows Driver Model (WDM) 或影片，從數位和類比裝置進行捕捉。 它會自動偵測並使用影片和音訊加速硬體（如有提供），但也支援不含加速硬體的系統。

DirectShow 是以元件物件模型 (COM) 為基礎。 若要撰寫 DirectShow 應用程式或元件，您必須瞭解 COM 用戶端程式設計。 針對大部分的應用程式，您不需要執行自己的 COM 物件。 DirectShow 提供您所需的元件。 但是，如果您想要藉由撰寫自己的元件來擴充 DirectShow，則必須將它們實作為 COM 物件。

DirectShow 是針對 c + + 所設計。 Microsoft 不提供適用于 DirectShow 的受控 API。

DirectShow 簡化了媒體播放、格式轉換和捕獲工作。 同時，針對需要自訂解決方案的應用程式，它會提供基礎資料流程控制架構的存取權。 您也可以建立自己的 DirectShow 元件，以支援新的格式或自訂效果。

您可以使用 DirectShow 撰寫之應用程式類型的範例包括檔案播放程式、電視和 DVD 播放機、影片編輯應用程式、檔案格式轉換器、音訊-影片捕獲應用程式、編碼器和解碼器、數位訊號處理器等等。

本節包含下列主題：

-   [DirectShow 的新功能](whats-new-in-directshow.md)
-   [DirectShow 中支援的格式](supported-formats-in-directshow.md)
-   [DirectShow 常見問題](directshow-faq.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 




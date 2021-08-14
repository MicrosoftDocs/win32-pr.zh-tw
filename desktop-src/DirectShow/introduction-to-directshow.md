---
description: DirectShow 簡介
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: DirectShow 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cd4dc2a75233c519c4ca3d5db213451b097c0528ab782109da611b6e35aca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952577"
---
# <a name="introduction-to-directshow"></a>DirectShow 簡介

microsoft® DirectShow®是 microsoft Windows®平臺上串流媒體的架構。 DirectShow 為多媒體串流提供高品質的捕獲和播放功能。 它支援各種不同的格式，包括先進的系統格式 (ASF) 、運動圖片專家群組 (MPEG) 、Audio-Video 交錯 (AVI) 、MPEG 音訊第3層 (MP3) 和 WAV 音效檔。 它支援根據 Windows Driver Model (WDM) 或影片 Windows，從數位和類比裝置進行捕捉。 它會自動偵測並使用影片和音訊加速硬體（如有提供），但也支援不含加速硬體的系統。

DirectShow 是以 (COM) 的元件物件模型為基礎。 若要撰寫 DirectShow 的應用程式或元件，您必須瞭解 COM 用戶端程式設計。 針對大部分的應用程式，您不需要執行自己的 COM 物件。 DirectShow 提供您所需的元件。 但是，如果您想要藉由撰寫自己的元件來延伸 DirectShow，您必須將它們實作為 COM 物件。

DirectShow 是針對 c + + 所設計。 Microsoft 不會提供 DirectShow 的受控 API。

DirectShow 可簡化媒體播放、格式化轉換和捕獲工作。 同時，針對需要自訂解決方案的應用程式，它會提供基礎資料流程控制架構的存取權。 您也可以建立自己的 DirectShow 元件，以支援新的格式或自訂效果。

您可以撰寫 DirectShow 的應用程式類型範例包括檔案播放程式、電視和 DVD 播放機、影片編輯應用程式、檔案格式轉換器、音訊-影片捕獲應用程式、編碼器和解碼器、數位訊號處理器等等。

本節包含下列主題：

-   [DirectShow 的新功能](whats-new-in-directshow.md)
-   [DirectShow 中支援的格式](supported-formats-in-directshow.md)
-   [DirectShow常見問題](directshow-faq.yml)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 




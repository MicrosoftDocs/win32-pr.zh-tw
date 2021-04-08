---
title: 關於 Windows Touch
description: 本主題提供 Windows Touch 的簡短總覽。
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch，軟體發展工具組
- Windows Touch，SDK
- Windows Touch，關於
- Windows Touch，新功能
- Windows Touch，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931934"
---
# <a name="about-windows-touch"></a>關於 Windows Touch

本主題提供 Windows Touch 的簡短總覽。

Windows 7 作業系統中的新硬體和 API 元素，可讓應用程式接收來自多個連絡人的輸入。 如此一來，這類應用程式就能夠偵測並回應應用程式可見表面上的多個同時觸控點。 這項功能在 Windows 7 中的功能是透過報告和追蹤接觸的新訊息來提供。 [**WM \_ 觸控**](wm-touchdown.md)的新訊息會回報動作 (向上、向下、移動) 、位置和觸控點的識別碼。 Windows Touch 的訊息是由 Windows 產生，並且會傳遞至註冊 Windows Touch 輸入的 windows。

除了新的觸控輸入訊息之外，還會將手勢訊息新增至現有的視窗訊息清單中。 筆勢的訊息支援是由單一新的視窗訊息所啟用 ([**WM \_ 手勢**](wm-gesture.md)) 當使用者輸入被辨識為手勢時，傳送或張貼至適當的應用程式視窗。 專用的 API 函式會封裝此訊息的建立和取用詳細資料。 這是因為與訊息相關聯的資訊可能會在未來變更，而不會中斷已使用此訊息的應用程式。

除了軌跡訊息之外，還將特製化介面新增至 Windows SDK。 這些介面會啟用觸控輸入的先進支援，讓應用程式開發人員可以輕鬆地建立自然的使用者介面。 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面會將 [**WM \_ 觸控**](wm-touchdown.md)訊息解釋為引發事件，其中包含觸控點集合的平移、旋轉和縮放資訊。 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面可搭配 **IManipulationProcessor** 介面使用，以啟用動畫，並確保物件在移動時保持在使用者的畫面上。

Windows Touch 的 API 元素與 Microsoft PixelSense SDK (有一些相似之處，之前稱為 Microsoft Surface SDK) ，但以 Microsoft PixelSense 為目標的應用程式不會在 Windows Touch 電腦上執行。 此外，以 Windows Touch 為目標的應用程式不會在 Microsoft PixelSense 上執行。

Windows Touch 的部分功能內建于 Windows 7 的核心中。 這項功能可供使用者使用，而不需要開發人員明確啟用支援。 但是，若要充分利用 Windows Touch，開發人員必須使用 Windows Touch API。 若要開始學習 Windows Touch 的運作方式，請參閱程式 [設計指南](programming-guide.md) ，或從 [選擇正確的方法](choosing-the-right-approach-to-windows-touch.md)開始著手 Windows Touch。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[架構總覽](architectural-overview.md)
</dt> <dt>

[選擇正確的方法來 Windows Touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Touch](windows-touch-portal.md)
</dt> </dl>

 

 





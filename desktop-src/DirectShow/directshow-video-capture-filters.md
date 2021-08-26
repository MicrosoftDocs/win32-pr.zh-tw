---
description: DirectShow影片捕獲篩選
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow影片捕獲篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cafe2815376ddb2a099c309228ba1bf24ae9315f305edb7312b88dd1196f82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966328"
---
# <a name="directshow-video-capture-filters"></a>DirectShow影片捕獲篩選

DirectShow 中的捕獲篩選器有一些功能與其他種類的篩選器有所區別。 雖然[Capture Graph Builder](capture-graph-builder.md)會隱藏許多詳細資料，但最好先閱讀本節，以瞭解 DirectShow Capture 圖形。

**釘選類別**

Capture 濾波器通常有兩個以上的輸出圖釘可提供相同類型的資料，例如預覽 pin 和捕捉 pin。 因此，媒體類型並不適合用來區別 pin。 相反地，pin 會透過其功能來區別，其使用稱為 *pin 類別* 的 GUID 來識別。

如需如何針對其類別查詢 pin 的討論，請參閱 [使用釘選類別](working-with-pin-categories.md)。 不過，大部分的應用程式都不需要直接查詢 pin。 相反地，不同的 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 方法會取得參數，以指定要在其上操作的釘選類別。 Capture Graph Builder 會自動尋找正確的 pin。

**預覽釘選和捕捉釘**

某些影片捕獲裝置有個別的輸出 pin 可供預覽和捕捉。 預覽 pin 是用來在螢幕上呈現影片，而捕捉釘用來將影片寫入檔案。

預覽 pin 和捕捉 pin 有下列差異：

-   預覽 pin 會視需要卸載框架，以維護捕捉釘選上的輸送量。
-   從捕捉釘選的每個畫面格都會加上時間戳記，並在框架被捕獲時提供串流時間。 預覽 pin 不會時間戳記所提供的範例。

預覽框架沒有時間戳記的原因是，篩選圖形在串流中引進了少量的延遲。 如果將捕獲時間當做展示時間使用，則影片轉譯器會將每個樣本視為稍微延遲。 這可能會導致影片轉譯器在嘗試趕上時，卸載畫面格。 移除時間戳記可確保轉譯器會在到達時顯示每個範例，而不會卸載框架。

預覽 pin 的釘選類別為釘選 \_ 類別 \_ 預覽版。 捕捉釘選的類別是釘選 \_ 類別 \_ 捕獲。

**影片埠釘選**

影片埠是影片裝置 (（例如類比電視調諧器) 和視訊卡）之間的硬體連接。 影片埠可讓裝置將影片資料直接傳送至圖形配接器。 影片會使用硬體重迭顯示在畫面上。 影片埠可能是在不同卡片上連接兩個裝置的實際纜線;或者，它可能是相同卡片上的硬式連接。

影片埠的優點是影片會直接進入視訊記憶體，而不會有 CPU 的任何工作。 不過，影片埠有一些缺點：

-   無論您是否想要預覽影片，影片埠一律會在捕捉期間使用重迭表面。
-   系統會自動在畫面格之間進行切換，因此很難將翻轉與其他影片作業進行同步處理。

如果捕捉裝置使用影片埠，則捕獲篩選器會有影片埠 pin，而不是預覽 pin。 影片埠 pin 的釘選類別是釘選 \_ 類別 \_ VIDEOPORT。

每個 capture 濾波器都至少有一個 capture pin。 此外，它可能會有預覽 pin 或影片埠 pin，但不能同時有兩者。 篩選器可以有多個捕捉釘和預覽 pin，每個都提供不同的媒體類型。 因此，單一篩選器可能會有影片捕獲釘選、影片預覽釘選、音訊捕獲 pin 和音訊預覽 pin。 不過， (沒有適用于音訊的影片埠。 ) 

**上游 WDM 篩選**

Windows (WDM) 裝置的驅動程式模型可能需要來自 capture 篩選器的一些額外篩選準則。 這些篩選器包括下列各項：

-   [電視調諧器篩選器](tv-tuner-filter.md)。 控制類比 TV 調諧器的微調。
-   [電視音訊篩選器](tv-audio-filter.md)。 控制類比 TV 調諧器的音訊設定。
-   [類比視頻縱橫條濾波器](analog-video-crossbar-filter.md)。 透過硬體裝置路由傳送影片和音訊信號。 例如，裝置可能會有多個輸入，例如 S-video 和複合影片。 縱橫比對篩選器可讓應用程式選取輸入。

雖然這些是 DirectShow 中的個別篩選，但它們通常代表相同的硬體裝置。 每個篩選器會控制裝置的不同功能。 篩選是透過釘選，但不會在 pin 連線之間移動媒體資料。 因此，這些篩選器上的釘選不會藉由建立媒體類型來連接。 相反地，它們會使用稱為 *媒體* 的 GUID 值。 系統會針對指定的裝置迷你驅動程式，唯一定義中等 Guid。 例如，相同的電視視訊卡的電視調諧器篩選器和影片捕獲篩選器都支援相同的媒體，讓應用程式能夠正確地建立圖形。

在實務上，只要您使用 **ICaptureGraphBuilder2** 來建立您的捕獲圖形，這些篩選器就會自動新增至圖形。 如需更詳細的討論，請參閱 [WDM 類別驅動程式篩選器](wdm-class-driver-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow 中的影片捕獲](about-video-capture-in-directshow.md)
</dt> </dl>

 

 




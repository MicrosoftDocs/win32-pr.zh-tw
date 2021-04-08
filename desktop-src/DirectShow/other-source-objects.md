---
description: 其他來源物件
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: 其他來源物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688203"
---
# <a name="other-source-objects"></a>其他來源物件

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

除了影片和音訊來源之外， (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 也支援下列來源物件。

**靜止影像**

DES 針對靜止映射支援下列檔案格式：

-   Bitmap (.bmp)
-   GIF (圖形交換格式) 
-   JPEG (聯合攝影專家群組) 
-   Targa 或 Truevision 圖形介面卡 (. tga) ： Mode 2 (16 位、24、bit 或32位格式的未壓縮 RGB) 。

這些檔案可以用來當做靜止影像或建立動畫。 若是點陣圖、JPEG 和 Targa 檔案，如果您使用檔案作為靜止影像，請呼叫 [**IAMTimelineSrc：： SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) 方法將畫面播放速率設定為零。

**DIB 順序**

由於有一系列的點陣圖、JPEG 或 Targa 檔案，轉譯引擎可以建立一個 DIB 順序。 若要建立 DIB 順序，請以數位順序提供檔案，例如 Image001.bmp、Image002.bmp、Image003.bmp 等等。 使用序列中的第一個檔案作為來源。 藉由呼叫 [**IAMTimelineSrc：： SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)來設定序列的畫面播放速率。 轉譯引擎會依指定的畫面播放速率迴圈處理序列中的影像。

如果序列太短而無法填滿持續時間，則在給定畫面播放速率的情況下，其餘的持續時間會是實心。 轉譯期間未發生任何錯誤。

**GIF 來源**

DES 支援使用 GIF89a 規格的 GIF 來源，包括動畫和透明 Gif。 使用動畫 GIF 時，與其他檔案類型不同的是，您不需要設定畫面播放速率。 GIF 檔案指定動畫中每個影像之間的延遲。

為了支援透明 Gif，DES 會將影像中的透明區域轉換為 RGB 三重 RGB (0，0，0) 。 然後，您可以在 RGB (0、0、0) 上使用 [金鑰轉換](key-transition.md) 為索引鍵。

DES 也會將落在 RGB (0 –7、0–7、0– 7) 範圍內的任何黑色區域轉換為 RGB (8、8、8) 值（除了透明度索引，如果它落在該範圍內）。 這項轉換無法偵測到眼睛。

**影片色彩來源**

[影片色彩來源](video-color-source.md)物件會建立純色的連續影片影像。 此物件的一個用途是讓它成為轉換中的一層。 例如，在影片淡入或淡出的影片中使用它。

**自訂來源篩選**

如果篩選準則符合下列條件，DES 可將 DirectShow 來源篩選器作為時間軸來源：

-   它支援搜尋
-   它會產生 DES 所支援的格式。 只要使用者的系統具有能夠解碼的 DirectShow 篩選器，就可以壓縮格式。

若要使用自訂來源，請指定篩選的 CLSID 作為來源物件的子物件 GUID。 如需詳細資訊， [請參閱子](subobjects.md)內容。 若要支援自訂屬性，請將它們實作為 **IDispatch** "put" 屬性。 來源物件僅支援靜態屬性;不支援動態屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用來源](working-with-sources.md)
</dt> </dl>

 

 




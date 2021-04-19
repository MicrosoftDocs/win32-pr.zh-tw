---
description: Windows Media 音訊和影片編解碼器是物件的集合，可用來壓縮和解壓縮數位媒體資料。
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Windows Media 轉碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998949"
---
# <a name="windows-media-codecs"></a>Windows Media 轉碼器

Windows Media 音訊和影片編解碼器是物件的集合，可用來壓縮和解壓縮數位媒體資料。 每個編解碼器都是由兩個物件所組成：編碼器和一個解碼器。 檔的這個部分會說明如何使用 Windows Media 音訊和影片編解碼器的功能來產生和取用壓縮的資料流程。

> [!Note]  
> 本檔主要適用于想要在以 c + + 為基礎的媒體應用程式中使用 Windows Media 編解碼器的開發人員。 如需 Windows Media 編解碼器功能的技術總覽，請參閱 [關於 Windows Media 編解碼器](about-the-windows-media-codecs.md)。

 

「 *編解碼器* 」一詞是「壓縮程式」和「解壓縮程式」一詞的獨有。 編解碼器通常會實作為一對 COM 物件：一個用於編碼內容，另一個用於解碼內容。 在某些情況下，COM 物件會佔用相同的動態連結程式庫 (DLL) 。

每個編解碼器物件都會執行兩個不同但類似的介面：



| 介面                              | 描述                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | 與 Microsoft 媒體基礎相容。 |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | 與 DirectShow 相容。                 |



 

音訊和影片不僅有不同的編解碼器，也有不同的編解碼器可用於不同類型的內容，您可能想要將它放入音訊或影片檔案中。 用來壓縮和解壓縮單字資料的演算法，與用來壓縮和解壓縮音樂資料的演算法不同。

## <a name="codec-descriptions"></a>編解碼器描述

下表說明 Windows Media 編解碼器的用途。



| 轉碼器                                                                     | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media 音訊](windowsmediaaudioencoder.md)                       | 支援三種編碼內容類別別的音訊編解碼器： Standard、Professional 和無損。                                                                                                                                                                                      |
| [Windows Media 音訊語音](windowsmediaaudiovoiceencoder.md)            | 針對以高壓縮率編碼人類聲音而優化的音訊編解碼器。 這是最常用於串流的串流編解碼器。 針對混合音樂和語音的內容，此編解碼器可以動態變更所使用的編碼演算法，以獲得最佳品質。 |
| [Windows Media 視訊9](windowsmediavideo9encoder.md)                    | 支援四種編碼內容類別別的影片編解碼器：簡單設定檔、主要設定檔、Advanced Profile 和 Image。                                                                                                                                                                  |
| [Windows Media 視訊9螢幕](usingthewindowsmediavideo9screencodec.md) | 針對從電腦監視器編碼順序螢幕擷取畫面優化的影片編解碼器。 此編解碼器通常用於軟體訓練或支援，方法是在使用電腦應用程式時錄製監視器映射。                                                                         |



 

最新版本的編解碼器物件也可以存取某些舊版編解碼器，包括 Windows Media 視訊7和8、Windows Media Screen 7、較舊的 Microsoft MPEG-2 編解碼器，以及 Microsoft ISO MPEG-2 編解碼器。

> [!Note]  
> 本檔未涵蓋這些舊版編解碼器;它僅涵蓋目前版本的編解碼器。

 

針對較舊的編解碼器，請使用與使用目前編解碼器時相同的程式;不過，請記住，並非所有編解碼器都支援所有的功能。

## <a name="in-this-section"></a>本節內容

-   [關於 Windows Media 編解碼器](about-the-windows-media-codecs.md)
-   [使用編解碼器和 DSP 物件](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [編碼方法](encodingmethods.md)
-   [編解碼器實行](codecimplementation.md)
-   [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)
-   [使用編解碼器 DMOs](workingwithcodecdmos.md)
-   [使用編解碼器 MFTs](workingwithcodecmfts.md)
-   [使用音訊](workingwithaudio.md)
-   [使用影片](workingwithvideo.md)
-   [將壓縮的媒體儲存在 AVI 檔案中](storingcompressedmediainavifiles.md)
-   [使用 VBR 編碼](usingvbrencoding.md)
-   [使用 Two-Pass 編碼](usingtwoencodingpasses.md)
-   [取得編碼統計資料](gettingencodingstatistics.md)
-   [使用資料單位延伸模組](usingdataunitextensions.md)
-   [編解碼器和 DSP IPropertyBag 常數](codecanddspproperties.md)
-   [目錄剖析器](toc-parser.md)
-   [Windows Media 編解碼器常見問題](frequentlyaskedquestions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> <dt>

[適用于 Windows 的媒體技術](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 

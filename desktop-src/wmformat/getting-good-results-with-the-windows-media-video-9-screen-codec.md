---
title: 使用 Windows Media 視訊9螢幕編解碼器取得良好的結果
description: 使用 Windows Media 視訊9螢幕編解碼器取得良好的結果
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media 格式 SDK，Windows Media 視訊9螢幕編解碼器
- Advanced Systems Format (ASF) ，Windows Media 視訊9螢幕編解碼器
- ASF (Advanced Systems Format) ，Windows Media 視訊9螢幕編解碼器
- 編解碼器，Windows Media 視訊9螢幕
- Windows Media 視訊9螢幕編解碼器，結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932948"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>使用 Windows Media 視訊9螢幕編解碼器取得良好的結果

Windows Media 視訊9畫面編解碼器的設計目的是要為螢幕擷取畫面產生高度壓縮的影片。 由於螢幕擷取畫面的大部分需求都牽涉到相當簡單和靜態的映射，因此，最高層級的壓縮通常表示影像品質很大的犧牲。 不過，每個螢幕擷取畫面都是不同的，而產生的影像品質可能會因情況而有很大的差異。

判斷螢幕編解碼器會話設定檔設定的最佳方式，就是使用以品質為基礎的變數位元速率資料流程來編碼測試檔案。 將品質設定為您想要的值，並將螢幕擷取畫面編碼為您錄製最終檔案的方式。 寫入檔案時，請使用非同步讀取器物件來播放，並定期呼叫 [**IWMReaderAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)。 藉由監視每次呼叫之 [**WM \_ 讀取器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)結構的 **dwBandwidth** 成員值，您可以判斷達到您想要的品質所需的大約位元速率。 然後，您可以將該位元速率用於常數位元速率編碼。

如果您發現您想要的品質需要比您用於傳遞案例更高的位元速率，您可以嘗試下列技術，以從編解碼器獲得更高的效率。

-   針對螢幕擷取畫面使用較小的解析度。 若要取得比您所需更大的螢幕解析度，也可以藉由呈現比所需更多的資訊，來為檢視器建立混淆。
-   在螢幕擷取畫面中使用較少的圖形。 Windows Media 視訊9畫面編解碼器經過優化，可將 Windows 基本專案和高品質的文字編碼。 通常是因為點陣圖圖形所造成的問題，這些圖形通常包含數以千計的個人色彩。 當您捕捉時，螢幕上的點陣圖越少，結果就越好。 如果您無法從螢幕擷取畫面中排除圖形，有幾種方式可以將點陣圖對影像品質的影響降至最低：
    -   縮小圖形的大小。
    -   減少同時出現在螢幕上的個別圖形數目。
    -   減少圖形的移動量。 例如，如果圖形是在視窗中，請盡可能讓視窗保持固定。
    -   避免將滑鼠指標移到圖形上，或將視窗或其他元素拖曳到圖形上。
-   使用較慢的 [*畫面播放速率*](wmformat-glossary.md)。 螢幕捕捉通常會以極低的畫面播放速率來有效 (有時每秒4或5個畫面格) 。
-   減少伴隨音訊的位元速率。

此外，編解碼器不支援調整影片矩形的大小。 換句話說，如果您嘗試使用編解碼器將 800 x 600 螢幕編碼成 640 x 480 的影片矩形，則產生的影片將會有重要的成品，可讓螢幕上的大部分文字無法辨認。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定畫面抓取資料流程**](configuring-screen-capture-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> </dl>

 

 





---
description: 使用 Windows Media 視訊9螢幕編解碼器
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: '使用 Windows Media 視訊9螢幕編解碼器 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992633"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>使用 Windows Media 視訊9螢幕編解碼器 (Microsoft 媒體基礎) 

Windows Media 視訊9畫面編解碼器已針對壓縮 *應用程式影片* 進行優化，其中包含電腦顯示的連續螢幕擷取畫面。 編解碼器會利用一般的影像簡單性 (相對較少的色彩、大量的直線等等) 和相對缺乏的動作，以達到非常高的壓縮比率。 這項優化的缺點是不符合應用程式影片預期特性的影片，可能很難以可接受的品質層級進行壓縮。

Windows Media 視訊9螢幕編碼程式是由類別識別碼 CLSID CMSSEncMediaObject2 來識別 \_ ，而此解碼器會識別出類別識別碼 clsid \_ CMSSDecMediaObject。 使用此編解碼器之媒體類型的 FOURCC 值為 "MSS2"。

## <a name="configuring-the-encoder"></a>設定編碼器

Windows Media 視訊9畫面編解碼器的編碼器的設定方式與標準視頻編碼器相同。

> [!Note]  
> 螢幕編碼器只支援一次傳遞編碼。 您可以將 [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) 屬性設定為2，並處理輸入兩次，而不會發生錯誤，但是這樣做並沒有任何好處。 這是已知的問題，可能會在未來的版本中修正。

 

## <a name="getting-the-best-results"></a>取得最佳結果

如果您在螢幕擷取畫面內容中發現您想要的品質，需要比您用於傳遞案例更高的位元速率，您可以嘗試下列技巧以從編解碼器獲得更高的效率：

-   針對螢幕擷取畫面使用較小的解析度。 若要取得比所需更大的螢幕解析度，可以藉由呈現不必要的資訊來混淆檢視器。
-   使用較慢的畫面播放速率。 螢幕捕捉通常會以極低的畫面播放速率來有效 (有時每秒4或5個畫面格) 。
-   在螢幕擷取畫面中使用較少的圖形。 Windows Media 視訊9畫面編解碼器經過優化，可將 Windows 基本專案和高品質的文字編碼。 通常是因為點陣圖圖形所造成的問題，這些圖形通常包含數以千計的個人色彩。 當您捕捉時，螢幕上的點陣圖越少，結果就越好。 如果您無法從螢幕擷取畫面中排除圖形，有數種方式可以將點陣圖對影像品質的影響降至最低：
    -   縮小圖形的大小。
    -   減少同時出現在螢幕上的個別圖形數目。
    -   減少圖形的移動量。 例如，如果圖形是在視窗中，請盡可能讓視窗保持固定。
    -   避免將滑鼠指標移到圖形上，或將視窗或其他元素拖曳到圖形上。

## <a name="decoding"></a>解碼

解碼螢幕擷取畫面影片沒有特殊需求。 不過，如同所有 Windows Media 視訊9編解碼器，螢幕擷取畫面解碼器無法在沒有編解碼器私用資料的情況下正確解壓縮編碼的內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定影片編碼](configuringvideoencoding.md)
</dt> <dt>

[使用影片編解碼器私用資料](usingvideocodecprivatedata.md)
</dt> <dt>

[Windows Media 視訊9螢幕編碼器](windowsmediavideo9screenencoder.md)
</dt> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 




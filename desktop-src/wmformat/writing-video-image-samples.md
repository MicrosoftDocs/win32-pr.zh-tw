---
title: 撰寫影片影像範例
description: 撰寫影片影像範例
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Advanced Systems Format (ASF) 、撰寫影片影像範例
- ASF (Advanced Systems 格式) 、撰寫影片影像範例
- 影片影像，撰寫範例
- 串流，撰寫影片影像範例
- 編解碼器，撰寫影片影像範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fbac644d7938477ba3d2e8b21ebb6e631a47708
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314250"
---
# <a name="writing-video-image-samples"></a>撰寫影片影像範例

影片影像串流是包含一系列靜止影像的影片。 影像可以在框架內移動，且每個影像都可以 blend 至下一個影像。 影片影像資料流程會使用 Windows Media 視訊9映射 v2 編解碼器進行編碼。 輸出影片類似于 Windows Media 視訊9編解碼器所建立的影片。

若要建立包含影片影像資料流程的設定檔，請依照 [從編解碼器取得串流設定資訊](getting-stream-configuration-information-from-codecs.md)中所述的方式列舉影片編解碼器開始。 搜尋支援 WMMEDIASUBTYPE \_ WVP2 子類型的編解碼器。

在寫入器物件上設定設定檔之後，請呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) 來取得影片影像輸入資料流程的媒體屬性。 藉由呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)，從 media properties 物件取得媒體類型，並將子類型變更為 WMMEDIASUBTYPE \_ VIDEOIMAGE。 您應該將影片的寬度和高度設定為包含您將新增至資料流程之影像所需的最大維度。 然後以修改過的輸入類型呼叫 [**IWMMediaProps：： SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) 。 現在您已準備好開始將範例傳送至寫入器物件。

每個範例的開頭都必須是 **WMT \_ VIDEOIMAGE \_ sample2.xml** 結構。 此外，範例可能包含點陣圖影像。 影像只會附加至它所顯示的第一個框架的範例。 使用該映射的所有其他畫面都只需要結構中的資訊。 輸入點陣圖必須格式化為 RGB，每圖元24位。

點陣圖檔案會儲存影像資料，讓影像中每個資料列的資料都採用數個可整除的位元組。  (這稱為點陣圖的 stride。 ) 這會將每個資料列的開頭強制為 **DWORD** 界限，讓複製更有效率。 如果影像資料列未平均整除四個，則會將資料列填補為四個位元組的下一個最高倍數。 當您附加影像資料時，您必須移除存在於每個資料列之資料結尾的任何填補。

Windows Media 視訊9映射 v2 編解碼器會在記憶體中一次維護最多兩個映射。 這些影像稱為先前的映射和目前的映射。 每個影像都有一組 **WMT \_ VIDEOIMAGE \_ sample2.xml** 結構中的成員，它會指示影像在框架中的呈現方式。 您可以藉由將 **WMT \_ VIDEOIMAGE \_ sample2.xml** 的 DWCONTROLFLAGS 成員設定為 WMT \_ VIDEOIMAGE \_ 範例 \_ 輸入框架來加入影像 \_ 。 當您將輸入框架傳遞給編解碼器時，該映射會成為目前的映射。 在先前的範例中，目前影像的影像通常會成為先前的影像，而先前範例中先前影像的影像則會被捨棄。 您可以將 **bKeepPrevImage** 成員設為 **TRUE**，以設定編解碼器保留舊的先前映射。 在此情況下，會捨棄先前範例中目前映射的影像。

影片影像框架的基本組合取決於每個影像的兩個因素：感興趣的區域和 blend 係數。 影像的相關區域是由原始點、寬度和高度所定義。 相關區域所描述的影像部分會填滿輸出框架。 如果感興趣區域的大小與輸出框架不同，則編解碼器會調整其大小。 影像的 blend 係數決定兩個影像的混合。 目前和先前影像的 blend 係數必須總計為1.0。 例如，如果 **fCurrBlendCoef** 設定為0.5，而 **fPrevBlendCoef** 設定為0.5，則輸出框架是由兩個影像中所需區域的相等 blend 所組成。

藉由操作影像的感興趣區域，您可以建立平移和縮放效果。 Blend 係數可讓您跨淡化 (在影像之間) 溶解。 除了這些效果之外，您還可以使用其中一個預先定義的轉換來建立更複雜的框架。 本檔的「 [影片影像轉換](video-image-transitions.md) 」一節會說明可用的轉換。 使用轉換時，您必須設定每個畫面格。 最簡單的方法是建立一個函式，以累加方式變更 **WMT \_ VIDEOIMAGE \_ sample2.xml** 結構的成員，以取得完整效果。

如需針對 deformations 設定之值的詳細資訊，請參閱 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)。

**注意** 如果您想要將音訊包含在具有影片影像資料流程的檔案中，您必須使用未壓縮的音訊輸入。 若要將影片影像串流與現有的壓縮音訊串流合併，您必須將音訊解壓縮，並以未壓縮的形式傳遞範例。 如果您在撰寫影片影像串流時，將壓縮的範例傳遞給寫入器，將會發生錯誤，導致樣本從影片中卸載。

此外，沒有音訊串流的壓縮影片影像檔案可以在單一 ASF 封包中包含數個非常小、高度壓縮的影片畫面格，這可能會導致舊版 Windows Media Player 的播放體驗不佳。 若要避免這個問題，最好的解決方法是將無訊息音訊串流插入檔案中，但這也會增加檔案大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**視訊影像**](video-image.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





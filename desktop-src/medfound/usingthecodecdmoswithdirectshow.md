---
description: 在 DirectShow 中使用視窗媒體編解碼器
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: 在 DirectShow 中使用視窗媒體編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495a2675335474351da80b9845fba67f9e967d637d7c9d9c749ffc2f12ce3ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012178"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>在 DirectShow 中使用視窗媒體編解碼器

Windows Media 音訊和影片編碼器和解碼物件原本是設計和優化，以使用 ASF 檔案容器格式和 Windows 媒體格式 SDK。 編解碼器物件適用于特定案例的 DirectShow，也就是一次傳遞 CBR 和以品質為基礎的視頻串流編碼。 但是，如果您考慮直接在 DirectShow 使用 ASF 以外的檔案容器來使用編解碼器物件，則有一些您應該事先瞭解的行為和問題。

> [!Note]  
> 如果您要搭配 DirectShow 使用獨立編解碼器，您可能只想要將它們當作 DMOs 使用。 換句話說，您將使用 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，而不是 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)。

 

## <a name="wm-audio-in-avi-files"></a>AVI 檔案中的 WM 音訊

您可以使用 DirectShow 將 WMA 串流編碼為您有多工器篩選器的任何檔案容器格式。 不過，Windows Media 音訊和影片編解碼器介面不支援 AVI 檔案中的 WMA，因為無法使用預設的 DirectShow avi 播放篩選器，以使用 wma 串流來維持 avi 檔案中的音訊影片同步。 如需詳細資訊，請參閱將 [壓縮的媒體儲存在 AVI 檔案中](storingcompressedmediainavifiles.md)。

音訊編碼器 DMO 會輸出不同持續時間的範例，即使是在「固定位元速率」模式中也一樣。 因此最適合使用時間戳的檔案容器格式。 AVI 檔案不會提供每個音訊樣本或樣本群組的時間戳記。 在 DirectShow 中，avi 分隔器篩選器會根據 AVI 資料流程標頭中 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構內的 **nAvgBytesPerSec** 值，為每個音訊) 畫面格的每個 (樣本群組製造時間戳記。

以此計算為基礎的假設是資料流程中的所有音訊樣本都是相等的持續時間;不過，DMO 輸出的範例不是相等的持續時間，所以 AVI 分隔器所套用的時間戳記並不精確。 因此，不可能在不修改 AVI 分隔器或音訊解碼器 DMO 的情況下，使用任何以 DirectShow 為基礎的應用程式來播放具有音訊和影片串流的 AVI 檔案。在某些情況下，Windows Media 音訊9語音編解碼器將可運作，但即使這會在任何搜尋作業之後遺失同步，因此其實不能被視為可行的解決方案。

如果您有 MP3 編碼器，則可以使用 WMV 和 MP3 為音訊串流建立 AVI 檔案。 這類檔案將會在 Windows Media Player 和其他 DirectShow 架構的應用程式中正確地播放和搜尋，因為 AVI 分隔器包含 MP3 資料流程的特殊處理常式代碼。 另一個選項是使用未壓縮的 PCM 音訊，雖然所產生的檔案大小明顯比壓縮的音訊串流更大。 由於 DirectShow 範例應用程式會建立 AVI 檔案，因此不會示範如何使用音訊編碼器 DMO。

## <a name="one-pass-encoding"></a>一次傳遞編碼

影片編碼器 DMO 可在兩種編碼模式的 DirectShow 中輕鬆運作： CBR 和以品質為基礎的 VBR。 只要您在建立篩選圖形時遵循正確的作業順序（如範例應用程式中所示），使用 AVI 多工器和檔案寫入器將 WMV 內容放入 AVI 檔案中相當簡單。

## <a name="two-pass-encoding"></a>雙通路編碼

雙通編碼模式需要更複雜的圖形建立和串流處理方法，以防止 DMO 在開始第二次行程之前，從第一次行程排清其內容。 在兩次傳遞編碼中，必須執行圖形一次，因此 DMO 可以執行其檔案資料的前置處理分析，然後再將圖形倒轉並再次執行，讓 DMO 可以執行實際的編碼。

當圖形進入第二次行程的執行狀態時，DMO 包裝函式會在第一個範例上設定不中斷旗標，因為時間戳記不是以第一次行程的最後時間戳記為順序。 當 DMO （其設計目的不是以這種方式在 DirectShow 中運作時），會接收不連續旗標，它會執行排清並遺失從第一次行程儲存的資料。 若要解決此問題，最好的解決方法是撰寫自訂 DMO 包裝函式篩選器，在第一次行程之後 seeked 圖形時，不會設定不連續旗標。 此 SDK 中 Windows (VfW) 範例的影片示範如何執行兩次傳遞編碼。

## <a name="interlaced-content"></a>交錯式內容

WMV 編碼器 DMO 可以編碼交錯的內容，同時保留交錯式，這對於從電視捕捉的內容也很實用，而且也可以在電視上播放。 不過，您無法使用預設的 DMO 包裝函式來保留交錯，因為該篩選不支援其輸入範例上的 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) 。

DMO 使用該介面來取得它所接收之每個範例的交錯式設定。 如果找不到介面，就像是 DMO 包裝函式的情況一樣，DMO 只會將輸入範例視為 noninterlaced。 若要在 DirectShow 中執行交錯編碼，有幾個替代方案。 最簡單的方法可能是直接使用 Windows 媒體格式9系列 SDK，或使用 WM asf 寫入器 DirectShow 篩選器來建立交錯式 asf 檔案。 然後，您可以將該檔案轉碼成其他格式。 如果您轉碼到 avi，您將會有一個交錯式檔案，但標準 DirectShow AVI 播放篩選器將無法辨識它，因為它們不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)。 另一種方法是撰寫您自己的 DMO 包裝函式篩選器，以支援 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 

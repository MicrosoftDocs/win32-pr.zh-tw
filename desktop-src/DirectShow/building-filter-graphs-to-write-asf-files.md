---
description: 建立篩選圖形來寫入 ASF 檔案
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: 建立篩選圖形來寫入 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467829"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>建立篩選圖形來寫入 ASF 檔案

建立以 Windows Media 為基礎的內容時，應用程式通常會使用下列其中一種情況：

-   將內容從其他格式轉換或轉碼成 Windows Media 格式。
-   將非 Windows Media 架構 (原生串流格式的內容，) 到 ASF 檔案中。
-   捕獲即時資料，並立即將其編碼為 Windows Media 格式。

轉碼 ASF 檔案

您可以透過各種方式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來建立檔案轉碼篩選圖形。 最簡單的方式是將 WM ASF 寫入器新增至篩選圖形，然後使用 IGraphBuilder：： RenderFile 方法自動建立圖形。

另一種方式是將每個篩選手動新增至圖形並連接釘選。 新增 WM ASF 寫入器之後，如果預設設定檔不適用，請使用 IConfigAsfWriter 方法進行設定，並將 WM ASF 寫入器輸入接點連接到上游篩選器上對應的輸出圖釘。

下圖顯示典型的 WM ASF 寫入器轉碼篩選圖形設定。

![轉碼篩選圖形](images/asf-transcode.png)

將原生資料流程格式插入至 ASF 檔案

根據預設，WM ASF 寫入器篩選器預期會在其輸入圖釘上使用未壓縮的音訊和影片串流，並使用 Windows Media 音訊和 Windows Media 視訊編解碼器來壓縮資料流程。 不過，ASF 檔案容器可以用於任何類型的資料。 藉由將數位媒體資料放入 ASF 檔案容器中，您可以新增 ASF 提供的功能，例如中繼資料和數位版權管理 (DRM) ，而不需要轉碼您的內容。

若要建立包含非以 Windows Media 為基礎之內容的 ASF 檔案，應用程式必須在 WM ASF 寫入器的篩選圖形上游中壓縮資料流程，然後藉由呼叫 [**IConfigAsfWriter2：： SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) 來略過 Wm Asf 寫入器的壓縮機制，如下所示：


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



然後使用所需的設定檔來設定篩選。 輸入資料流程的媒體類型必須完全符合設定檔中的格式。 在某些情況下，您可能需要檢查輸入資料流程的格式，並建立自訂設定檔以符合此格式。

當您將 WM ASF 寫入器連線到上游篩選器時，請使用 IGraphBuilder：： ConnectDirect 方法。 請勿使用任何 "智慧型 connect" 方法（例如 IGraphBuilder：： Connect 或 IGraphBuilder：： RenderFile）來連接篩選，因為這樣會停用篩選準則的「略過壓縮」模式。

直接從裝置到 ASF 檔案的捕獲

當直接將音訊或影片捕獲到 ASF 檔案時，篩選圖形看起來會如下所示，視所使用的捕獲裝置類型而定。

![windows media 影片捕獲圖形](images/asf-webcam.png)

如需建立影片和音訊捕獲圖形的詳細資訊，請參閱下列主題：

-   [音訊捕獲](audio-capture.md)
-   [影片捕獲](video-capture.md)

除非所有的 pin 都已連線，否則不會執行 WM ASF 寫入器。 如果您使用預設系統設定檔來設定 WM ASF 寫入器 (不建議使用) ，或任何包含音訊和影片串流的設定檔，則會為每個串流建立輸入 pin，而且必須連線到每個輸出。 例如，如果您不想要捕獲音訊，請務必使用僅限影片的設定檔來設定篩選，如此就不會建立音訊 pin。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 




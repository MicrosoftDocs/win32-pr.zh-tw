---
description: 影片功能
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: 影片功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4841f5f33b39adc6bd12775e07085e14886d250cd59c988884ae7ca8a6a21b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290837"
---
# <a name="video-capabilities"></a>影片功能

[**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps)方法會以 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)和 [**影片 \_ 串流設定 \_ \_ 帽**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps)結構的配對陣列來呈現影片功能。 您可以使用此方法來公開 pin 所支援的所有格式和解析度，如下所述。

如需 **GetStreamCaps** 的音訊相關範例，請參閱 [音訊功能](audio-capabilities.md)。

假設您的捕獲卡支援 JPEG 格式，其解析度介於 160 x 120 圖元與 320 x 240 圖元（含）之間。 在此情況下，支援的解析度之間的差異在於，這是因為您在每個支援的解析度中新增或減少一個圖元以取得下一個支援的解析度。 在支援的解決方案中，這項差異稱為資料細微性。

假設您的卡片也支援 640 x 480 的大小。 以下說明此單一解析度，以及上述的解析度範圍 (在 160 x 120 圖元與 320 x 240 圖元) 之間的大小。

![從 160 x 120 到 320 x 240 圖元的解析度，加上 640 x 480](images/strmcap1.png)

此外，假設它支援 160 x 120 與 320 x 240 之間的24位色彩 RGB 格式，但資料細微性為8。 下圖顯示此案例中的一些有效大小。

![從 160 x 120 到320至240的解析度，資料細微性 = 8](images/strmcap3.png)

若要以另一種方式，並列出更多的解決方式，請在有效的解決方式清單中輸入下列各項。

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ...其他解決方案 .。。
-   312 x 232
-   320 x 240

使用 **GetStreamCaps** 來公開這些色彩格式和維度功能，方法是提供媒體類型 320 x 240 JPEG (如果這是您的預設或慣用大小) 結合 160 x 120 的最小功能、320 x 240 的最大功能，以及1的資料細微性。 您使用 **GetStreamCaps** 所公開的下一組是 640 x 480 JPEG 的媒體類型，結合最少 640 x 480 和最大 640 x 480 以及0的資料細微性。 第三組包含 320 x 240、24位 RGB 的媒體類型，具有 160 x 120 的最小功能、320 x 240 的最大功能，以及8的資料細微性。 如此一來，您幾乎可以發佈卡片可能支援的所有格式和功能。 必須知道您所提供之壓縮格式的應用程式，可以取得所有配對，並建立媒體類型的所有唯一子類型清單。

篩選器會分別從 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的 **rcSource** 和 **rcTarget** 成員取得其媒體類型來源和目標矩形。 篩選準則不需要支援來源和目標矩形。

整個 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 檔中所描述的裁剪矩形，與輸出圖釘的 **VIDEOINFOHEADER** 結構 **rcSource** 矩形相同。

整個 **IAMStreamConfig** 檔中所描述的輸出矩形，與輸出釘選 **BITMAPINFOHEADER** 結構的 **biWidth** 和 **BiHeight** 成員相同 (查看 [AVI 檔案格式的 DV 資料](dv-data-in-the-avi-file-format.md)。 ) 。

如果篩選的輸出圖釘連接到具有非空白來源和目標矩形的媒體類型，則需要您的篩選，將輸入格式的來源 subrectangle 延伸至輸出格式的目標 subrectangle。 來源 subrectangle 會儲存在 [**影片串流設定 \_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) 結構的 **InputSize** 成員中。

例如，請考慮下列影片壓縮程式案例：輸入影像為 RGB 格式，且大小為 160 x 120 圖元。 來源矩形的左上角位於座標 (20、20) ，而其右下角為 (30，30) 。 輸出影像採用 MPEG 格式，大小為 320 x 240。 目標矩形的左上角位於 (0、0) ，其右下角為 (100100) 。 在此情況下，篩選器應該採用 160 x 120 RGB 來源點陣圖的 10 x 10 段，使其填滿 320 x 240 點陣圖的前 100 x 100 區域，讓其餘的 320 x 240 點陣圖保持不變。 下圖顯示此案例。

![subrectangle 延展](images/strmcap4.png)

篩選可能不支援這種情況，而且可能無法使用 **rcSource** 和 **rcTarget** 不是空的媒體類型進行連接。

**VIDEOINFOHEADER** 結構會公開篩選資料速率功能的相關資訊。 例如，假設您已將輸出圖釘連接至具有特定媒體類型的下一個篩選器 (直接或使用 [**CMediaType：： SetFormat**](cmediatype-setformat.md) 函式所傳遞的媒體類型) 。 查看該媒體類型之 **VIDEOINFOHEADER** 格式結構的 **dwBitRate** 成員，以查看您應該壓縮影片的資料速率。 如果您將 **VIDEOINFOHEADER** 結構的 **AvgTimePerFrame** 成員中每個畫面格的時間單位乘以 **dwBitRate** 成員中的資料速率，並除以 10000000 (每秒的單位數) ，您就可以找出每個畫面格的位元組數目。 您可以產生較小的大小框架，但永遠不會有一個較大的框架。 若要判斷影片壓縮程式或取得篩選器的畫面播放速率，請使用輸出釘選媒體類型的 **AvgTimePerFrame** 。

 

 




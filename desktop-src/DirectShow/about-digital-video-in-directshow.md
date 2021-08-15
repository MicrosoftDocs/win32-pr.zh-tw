---
description: 關於 DirectShow 的數位視訊
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: 關於 DirectShow 的數位視訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664806"
---
# <a name="about-digital-video-in-directshow"></a>關於 DirectShow 的數位視訊

數位視訊 (DV) 可以從 DV 攝影機中捕捉、儲存在使用者電腦上的檔案中，或使用影片磁帶錄製器儲存在磁帶上 (VTR) 。 因此，應用程式可能會在 DV 串流上執行的作業包括：

-   從 DV 攝影機捕獲實況影片。
-   從 VTR 磁帶傳輸 DV 資料至電腦。
-   將 DV 資料從電腦傳輸到 VTR。
-   從檔案讀取 DV 資料。
-   將 DV 資料寫入檔案。
-   轉譯 DV 串流中的音訊和影片。

DirectShow 提供下列 DV 篩選器：

-   [MSDV 驅動程式](msdv-driver.md)。 MSDV 驅動程式控制 DV 裝置，例如攝像機。 裝置可能具有相機子單位和 VTR 子單位;MSDV 會控制兩個次單元連接。 MSDV 驅動程式會以 DirectShow 濾波器的形式出現在應用程式中。
-   [DV 分隔](dv-splitter-filter.md) 器篩選器。 DV 框架在相同的框架中包含音訊和影片。 DV 分隔器篩選器會將音訊資料解壓縮，並將其輸出為一或兩個音訊串流。 它會將原始資料輸出為個別的 DV 影片串流。
-   [DV 影片解碼](dv-video-decoder-filter.md) 篩選器。 將 DV 影片解碼成未壓縮的影片。
-   [DV 影片編碼器](dv-video-encoder-filter.md) 篩選器。 將未壓縮的影片編碼為 DV 編碼的影片。
-   [DV Muxer](dv-muxer-filter.md)。 結合 DV 影片串流與一或兩個音訊串流，以建立單一交錯 DV 串流。

DV 分隔器和 DV 影片解碼可一起運作。 分割器會採用交錯的資料流程，並輸出個別的音訊和 DV 影片串流。 此解碼器會將 DV 影片轉換成未壓縮的影片。 下圖說明此程式。

![dv 分隔器和 dv 解碼器](images/dv-filters1.png)

DV 影片編碼器和 DV Muxer 會反轉進程：編碼器會將未壓縮的影片轉換成 DV 影片，而 mux 則結合了音訊和 DV 影片來建立單一交錯式串流，如下圖所示。

![dv 編碼器和 dv muxer](images/dv-filters2.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




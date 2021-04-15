---
title: 使用非同步讀取器讀取檔案
description: 使用非同步讀取器讀取檔案
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK，讀取檔案
- Windows Media Format SDK，非同步讀取器
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- 非同步讀取器，IWMReaderCallback 介面
- IWMReaderCallback，非同步讀取器
- 非同步讀取器，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374403"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>使用非同步讀取器讀取檔案

非同步讀取器會使用多個執行緒和非同步呼叫來讀取 ASF 檔案中的內容。 非同步讀取器所支援的功能，適用于將內容呈現給使用者的應用程式。

讀取器物件的最基本功能可細分為下列步驟。 在這些步驟中，「應用程式」指的是您使用 Windows Media Format SDK 撰寫的程式。

1.  應用程式會執行 [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) 介面，以處理來自讀取器的訊息。 這包括兩個回呼方法： **OnStatus**，它會接收與讀取器和 **OnSample** 的各個層面狀態相關的訊息，這會從讀取器接收未壓縮的範例。
2.  應用程式會將要讀取的檔案名傳遞給讀取器。 當讀取器開啟檔案時，它會將輸出編號指派給每個資料流程。 如果檔案使用相互排除，讀取器會為所有互斥資料流程指派單一輸出。
3.  應用程式會從讀取器取得各種輸出的設定相關資訊。 收集的資訊將可讓應用程式正確地轉譯媒體範例。
4.  應用程式會指示讀取器開始從檔案讀取資料。 讀取器會開始將未壓縮的範例傳遞給 **OnSample** 回呼，並在緩衝區物件中包裝的緩衝區中一次傳遞一個。 讀取器所提供的範例處於展示階段順序。 讀取器將繼續傳遞範例，直到應用程式停止為止，或直到到達檔案結尾為止。
5.  應用程式會在讀取器傳遞之後，負責呈現資料。 Windows Media Format SDK 不提供任何轉譯常式。 一般而言，應用程式會使用其他 Sdk 來呈現資料，例如 Microsoft DirectX® SDK，或 Microsoft Windows Platform SDK 的多媒體功能。
6.  當讀取完成時，應用程式會指示讀取器關閉檔案。

這些步驟說明于 >audioplayer 範例應用程式中，還有其他步驟。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

讀取器也支援更先進的功能。 讀取器可讓您執行下列作業：

-   暫停檔案的播放。
-   取得讀取器效能統計資料。
-   適用于互斥資料流程的控制資料流程選取範圍。
-   手動設定緩衝區以進行輸出。
-   提供您自己的時鐘。
-   取得檔案作業的狀態 (緩衝、下載或儲存) 。
-   使用標準 COM 介面、 **IStream** 來開啟檔案。
-   搜尋 ASF 檔案中的特定點。
-   從檔案標頭讀取設定檔資料。

下列各節將詳細說明如何使用 reader 物件。

-   [在 OnStatus 回呼中執行讀取器訊息](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [若要執行 OnSample 回呼](to-implement-the-onsample-callback.md)
-   [建立讀取器並開啟檔案](to-create-a-reader-and-open-a-file.md)
-   [使用非同步讀取器取出媒體範例](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [使用非同步讀取器依時間進行搜尋](to-seek-by-time-using-the-asynchronous-reader.md)
-   [使用非同步讀取器依框架編號搜尋](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [使用非同步讀取器依 SMPTE 時間程式碼進行搜尋](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [搜尋標記](to-seek-to-markers.md)
-   [暫停或停止播放](to-pause-or-stop-playback.md)
-   [取得讀取器效能統計資料](to-get-reader-performance-statistics.md)
-   [使用手動資料流程選取](to-use-manual-stream-selection.md)
-   [使用非同步讀取器傳遞壓縮的範例](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**讀取器物件**](reader-object.md)
</dt> </dl>

 

 





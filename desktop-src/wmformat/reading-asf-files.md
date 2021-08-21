---
title: 讀取 ASF 檔案
description: 讀取 ASF 檔案
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows媒體格式 SDK，讀取 ASF 檔案
- 'Windows媒體格式 SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01f417cafad4e125c6c176ac35e95ff3ab8f08c4f600b811865a9fb6ae51362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197515"
---
# <a name="reading-asf-files"></a>讀取 ASF 檔案

Windows 媒體格式 SDK 可以用來從 ASF 檔案傳遞媒體範例。 使用兩個物件來抓取範例、讀取器物件和同步讀取器物件。

讀取器物件是 Windows 媒體格式 SDK 中的原始讀取物件。 讀取器物件使用非同步架構將範例推送至應用程式。 使用 reader 物件建立的應用程式必須執行回呼函式，以回應這個多執行緒模型所產生的各種訊息和事件。 為了清楚起見，本章節將會以非同步讀取器的形式來參考 reader 物件。

此 Windows 媒體格式 SDK 的這個版本有新的同步讀取器物件。 同步讀取器不會使用多個執行緒來處理來自 ASF 檔案的範例。 使用同步讀取器所建立的應用程式會視需要抓取範例，而不是等候讀取器傳送。

建立應用程式以讀取 ASF 檔案時，您必須選擇要使用的讀取器物件。 一般情況下，設計用來傳遞 Windows 媒體內容的應用程式應該使用非同步讀取器來建立，而設計用來編輯 ASF 檔案的應用程式應該使用同步讀取器來建立。

下表列出兩個讀取器物件的主要功能。 您可以使用此表格來協助判斷要用於應用程式的物件。



| 功能                                                                    | 非同步讀取器 | 同步讀者 |
|----------------------------------------------------------------------------|--------------|-------------|
| 依輸出編號讀取未壓縮的範例                                 | 是          | 是         |
| 依串流號碼讀取壓縮的範例                                   | 是          | 是         |
| 依串流號碼讀取未壓縮的範例                                 | 否           | 是         |
| 從網際網路網站讀取                                                    | 是          | 否          |
| 讀取中繼資料                                                              | 是          | 是         |
| 搜尋展示時間                                                  | 是          | 是         |
| 搜尋至框架                                                              | 是          | 是         |
| 搜尋至標記                                                             | 是          | 否          |
| 在播放期間于壓縮和未壓縮的範例傳遞之間切換 | 否           | 是         |
| 使用 **IStream** 介面開啟檔案                                     | 是          | 是         |



 

下列各節提供有關使用兩個讀取器物件的詳細資訊。



| 區段                                                                                      | 描述                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [使用輸出](working-with-outputs.md)                                             | 說明如何使用和操作輸出。 適用于這兩個讀取器物件。                                                            |
| [設定檔案讀取的緩衝區](allocating-buffers-for-file-reading.md)               | 說明如何使用您自己的緩衝區集區來保存讀取器或同步讀取器所提供的範例。                            |
| [在播放時讀取中繼資料](reading-metadata-at-playback.md)                             | 描述如何在播放時利用中繼資料支援。 適用于這兩個讀取器物件。                                        |
| [在播放時取得設定檔資訊](getting-profile-information-at-playback.md)       | 說明如何存取已開啟檔案的設定檔資訊。 適用于這兩個讀取器物件。                                           |
| [讀取多頻道音訊](reading-multichannel-audio.md)                                 | 描述如何設定寫入器以正確地將多頻道音訊解碼。                                                            |
| [轉譯內容](rendering-content.md)                                                   | 討論轉譯未壓縮範例的相關問題。 適用于這兩個讀取器物件。                                         |
| [取得最佳的影片搜尋效能](getting-the-best-video-seeking-performance.md) | 描述改善影片搜尋效能的方法。                                                                                    |
| [使用非同步讀取器讀取檔案](reading-files-with-the-asynchronous-reader.md) | 說明如何使用非同步讀取器物件讀取 ASF 檔案。                                                                   |
| [使用同步讀取器讀取檔案](reading-files-with-the-synchronous-reader.md)   | 說明如何使用同步讀取器物件讀取 ASF 檔案。                                                                    |
| [啟用 DirectX Video 加速](enabling-directx-video-acceleration.md)               | 說明如何執行 DirectX Video 加速，以使用部分視訊卡的硬體加速功能來解碼影片。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> <dt>

[**讀取器物件**](reader-object.md)
</dt> <dt>

[**同步讀取器物件**](synchronous-reader-object.md)
</dt> </dl>

 

 





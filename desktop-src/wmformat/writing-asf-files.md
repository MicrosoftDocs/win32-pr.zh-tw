---
title: 寫入 ASF 檔案
description: 寫入 ASF 檔案
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows媒體格式 SDK，寫入 ASF 檔案
- Windows媒體格式 SDK，建立 ASF 檔案
- 'Windows媒體格式 SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，寫入檔案
- ASF (Advanced Systems Format) ，寫入檔案
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4bec466a9f38dfedaa7e860fdc5e3eda56e0ca5fa1f1240bc18c54dfd51513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590618"
---
# <a name="writing-asf-files"></a>寫入 ASF 檔案

您可以使用 Windows 媒體格式 SDK 的寫入器物件，從數位媒體資料建立 ASF 檔案。 若要建立寫入器物件的實例，請呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數。 寫入器物件會協調許多元件的功能，包括 Windows 媒體格式 SDK 外部的編解碼器。

寫入器物件的基本功能可細分為下列步驟。 在這些步驟中，「應用程式」是指您使用 Windows 媒體格式 SDK 撰寫的程式。

1.  應用程式會為寫入器提供用來建立 ASF 檔案的設定檔。 當寫入器載入設定檔資料時，它會將輸入編號指派給設定檔的每個連接。
2.  應用程式會為寫入器提供要寫入之檔案的輸出檔名稱。 寫入器會建立寫入器檔案接收物件，以管理檔案建立和輸入。 如需詳細資訊，請參閱 [寫入器檔案接收物件](writer-file-sink-object.md)。
3.  寫入器會根據設定檔中的資訊，建立新檔案的標頭。
4.  應用程式會將未壓縮的範例傳遞給寫入器。 在緩衝區物件中包裝的緩衝區中，一次傳遞一個範例。 應用程式應該同時傳遞每個資料流程的範例，讓寫入器以展示時間順序接收所有範例。
5.  寫入器會將範例傳遞給適當的編解碼器以進行壓縮。 當寫入器收到壓縮的範例時，它會使用來自其他資料流程的範例來交錯它們，如此一來，範例就會以展示時間順序進入檔案，而不受串流。 然後，範例資料會變成封包，並寫入檔案的資料區段。
6.  當處理所有樣本時，寫入器可以將索引新增至檔案，以增強搜尋效能。

這些步驟說明于 WMStats 範例應用程式中，還有其他步驟。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

寫入器也支援更先進的功能，可讓您執行下列作業：

-   編輯檔案標頭中的中繼資料。
-   撰寫 precompressed 範例。
-   寫入網路接收器以串流處理即時資料。
-   寫入至檔案接收以取得 advanced file control 選項。
-   寫入推播接收器，以散發給將傳遞內容給終端使用者的伺服器。
-   傳遞 postview 範例以驗證輸出。
-   傳遞寫入器-效能統計資料。

下列各節將詳細說明如何使用寫入器物件。



| 區段                                                                    | 描述                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [將設定檔與寫入器搭配使用](to-use-profiles-with-the-writer.md)     | 描述如何指定要搭配寫入器使用的設定檔。                                             |
| [使用輸入](working-with-inputs.md)                             | 描述如何識別和設定寫入器中的輸入設定。                              |
| [使用寫入器編輯中繼資料](to-edit-metadata-with-the-writer.md)   | 描述如何使用寫入器來編輯新檔案的中繼資料。                                       |
| [撰寫範例](to-write-samples.md)                                   | 描述如何將範例傳遞給寫入器。                                                           |
| [設定資料單位延伸模組](setting-data-unit-extensions.md)           | 說明如何將擴充資料新增至範例。                                                         |
| [撰寫壓縮的範例](writing-compressed-samples.md)               | 說明如何將預先壓縮的範例傳遞給寫入器。                                            |
| [寫入影像資料流程](writing-image-streams.md)                         | 說明如何設定影像資料流程的輸入。                                               |
| [撰寫影片影像範例](writing-video-image-samples.md)             | 說明如何設定影片影像範例。                                                        |
| [寫入變數位元速率資料流程](writing-variable-bit-rate-streams.md) | 說明如何將變數的位元速率寫入 (VBR) 資料流程。                                                |
| [使用 Two-Pass 編碼](using-two-pass-encoding.md)                     | 描述如何在寫入檔案之前，讓編解碼器先執行初步傳遞。                    |
| [強制插入 Key-Frame](to-force-key-frame-insertion.md)           | 說明如何手動強制編解碼器將範例編碼為主要畫面格。                           |
| [管理寫入器延遲](to-manage-writer-latency.md)                   | 描述如何將撰寫範例所需的時間降到最低，以將範例處理到輸出檔或接收。 |
| [使用寫入器接收器](working-with-writer-sinks.md)                 | 說明如何使用寫入器接收將內容傳遞至檔案或網路位置。               |
| [取得寫入器統計資料](to-get-writer-statistics.md)                   | 描述如何取得寫入器的統計資料。                                                        |
| [使用寫入器 Postview](to-use-writer-postview.md)                       | 描述當您撰寫要驗證的檔案時，如何取得未壓縮的範例。                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> <dt>

[**寫入器檔案接收物件**](writer-file-sink-object.md)
</dt> <dt>

[**寫入器網路接收物件**](writer-network-sink-object.md)
</dt> <dt>

[**寫入器物件**](writer-object.md)
</dt> </dl>

 

 





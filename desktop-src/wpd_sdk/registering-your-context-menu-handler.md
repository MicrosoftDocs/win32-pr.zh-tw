---
description: 註冊您的內容功能表處理常式
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: 註冊您的內容功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027e01d4b3bc58727579b77345d3f1b8eed668e5b858e49eb4859a40db9ad2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083542"
---
# <a name="registering-your-context-menu-handler"></a>註冊您的內容功能表處理常式

為了讓 WPD 命名空間能夠辨識您的內容功能表處理常式，您必須在 Windows 登錄中正確註冊。 WPD 內容功能表處理常式的註冊專案類似于 shell 的註冊專案，但會將它們註冊為特殊檔案類型。 WPD 操作功能表處理常式會根據它們所代表的內容類型進行註冊。 以下是 WPD 內容功能表處理常式的範例註冊樹：


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



上述範例會向 WPD 命名空間註冊 shell 影像檢視器。 當使用者在裝置上按一下滑鼠右鍵或按兩下 Windows 裝置上的內容時，它會叫用此操作功能表處理常式。 WPD 命名空間會使用 WPD \_ 內容 \_ 類型來決定要載入哪些內容功能表處理常式。 如果 WPD \_ 內容 \_ 類型等於 WPD \_ 內容類型 [ \_ \_ 未指定]、 \_ [WPD 內容類型]、 \_ [一般檔案] \_ \_ 或 \_ [WPD 內容類型] \_ \_ 程式，則 WPD 命名空間會根據所選檔案的副檔名，嘗試尋找最佳的相符專案。 如果副檔名或內容類型都沒有提供實用的分類，WPD 命名空間會在 **WPDCoNtextMenu. 泛型** 登錄機碼下載入內容功能表處理常式。 下表列出可供內容功能表處理常式使用的所有檔案類別，以及它們所代表的內容類型和副檔名：



| 登錄金鑰                           | WPD 內容類型                                                                                               | 副檔名                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDCoNtextMenu 裝置**              | 在此機碼下註冊可在裝置層級啟用您的內容功能表處理常式。  (在裝置上按一下滑鼠右鍵。 )    | (N/A)                                                                                                    |
| **WPDCoNtextMenu.儲存體**             | 在此機碼下註冊可在儲存層級啟用您的內容功能表處理常式。  (以滑鼠右鍵按一下儲存體。 )  | (N/A)                                                                                                    |
| **WPDCoNtextMenu 資料夾**              | WPD \_ 內容 \_ 類型 \_ 資料夾                                                                                     | (N/A)                                                                                                    |
| **WPDCoNtextMenu 影像**               | WPD \_ 內容 \_ 類型 \_ 影像                                                                                      | .bmp <br/> .gif <br/> .png <br/> .jpg <br/> .jpe <br/> .jpeg <br/>   |
| **WPDCoNtextMenu 音訊**               | WPD \_ 內容 \_ 類型 \_ 音訊                                                                                      | .aiff <br/> .mp3 <br/> .wav <br/> .wma <br/>                                     |
| **WPDCoNtextMenu 影片**               | WPD \_ 內容 \_ 類型 \_ 影片                                                                                      | .asf<br/> .avi <br/> .dvr-ms <br/> .mpeg <br/> .mpg <br/> .wmv <br/> |
| **WPDCoNtextMenu 播放清單**<br/> | WPD \_ 內容 \_ 類型 \_ 播放清單                                                                                   | . .wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> . 另外 <br/>                     |
| **WPDContextMenu.Doc>ument**            | WPD \_ 內容 \_ 類型 \_ 檔                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDCoNtextMenu。連絡人**<br/>  | WPD \_ 內容 \_ 類型 \_ 連絡人                                                                                    | 無                                                                                                     |
| **WPDCoNtextMenu.Email**               | WPD \_ 內容 \_ 類型 \_ 電子郵件                                                                                      | 無                                                                                                     |
| **WPDCoNtextMenu 約會**         | WPD \_ 內容 \_ 類型 \_ 約會                                                                                | 無                                                                                                     |
| **WPDCoNtextMenu。工作**                | WPD \_ 內容 \_ 類型 \_ 工作                                                                                       | 無                                                                                                     |
| **WPDCoNtextMenu**                | WPD \_ 內容 \_ 類型 \_ 備忘錄                                                                                       | 無                                                                                                     |
| **WPDCoNtextMenu.ImageAlbum**          | WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯                                                                               | 無                                                                                                     |
| **WPDCoNtextMenu.AudioAlbum**          | WPD \_ 內容 \_ 類型 \_ 音訊 \_ 專輯                                                                               | 無                                                                                                     |
| **WPDCoNtextMenu.VideoAlbum**          | WPD \_ 內容 \_ 類型 \_ 影片 \_ 專輯                                                                               | 無                                                                                                     |
| **WPDCoNtextMenu.MixedAlbum**          | WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯                                                                      | 無                                                                                                     |
| **WPDCoNtextMenu 泛型**             | \_ \_ 未指定 WPD 內容類型 \_                                                                                | 所有其他副檔名                                                                                |



 

 

 





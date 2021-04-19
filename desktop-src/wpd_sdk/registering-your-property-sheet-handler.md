---
description: 註冊您的屬性工作表處理常式
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: 註冊您的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979907"
---
# <a name="registering-your-property-sheet-handler"></a>註冊您的屬性工作表處理常式

為了讓 WPD 命名空間能夠辨識您的屬性工作表處理常式，您必須在 Windows 登錄中正確註冊。 WPD 屬性工作表處理常式的註冊專案類似于 shell 的註冊專案，但會將它們註冊為特殊檔案類型。 WPD 屬性工作表處理常式是根據它們所代表的內容類型來註冊。 以下是 WPD 內容功能表處理常式的範例註冊樹：


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



上述範例會使用 WPD 命名空間來註冊自訂處理常式。 當使用者透過 Windows Shell 以滑鼠右鍵按一下裝置上的影像檔案，並選取 [ **屬性**] 時，它會叫用這個屬性工作表處理常式。 WPD 命名空間會使用 WPD \_ 內容 \_ 類型來決定要載入的屬性工作表處理常式。 如果內容類型並未提供有用的分類，則命名空間會將屬性工作表處理常式載入 **WPDPropSheet 一般** 登錄機碼底下。 下表列出可供內容功能表處理常式使用的所有檔案類別，以及它們所代表的內容類型和副檔名。



| 登錄金鑰                   | WPD 內容類型                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDCoNtextMenu 裝置**      | 在此機碼下註冊可在裝置層級啟用您的內容功能表處理常式。  (在裝置上按一下滑鼠右鍵。 )                    |
| **WPDCoNtextMenu**     | 在此機碼下註冊可在儲存層級啟用您的內容功能表處理常式。  (以滑鼠右鍵按一下儲存體。 )                  |
| **WPDCoNtextMenu 資料夾**      | WPD \_ 內容 \_ 類型 \_ 資料夾                                                                                                     |
| **WPDCoNtextMenu 影像**       | WPD \_ 內容 \_ 類型 \_ 影像                                                                                                      |
| **WPDCoNtextMenu 音訊**       | WPD \_ 內容 \_ 類型 \_ 音訊                                                                                                      |
| **WPDCoNtextMenu 影片**       | WPD \_ 內容 \_ 類型 \_ 影片                                                                                                      |
| **WPDCoNtextMenu 播放清單**    | WPD \_ 內容 \_ 類型 \_ 播放清單                                                                                                   |
| **WPDContextMenu.Doc>ument**    | WPD \_ 內容 \_ 類型 \_ 檔                                                                                                   |
| **WPDCoNtextMenu。連絡人**     | WPD \_ 內容 \_ 類型 \_ 連絡人                                                                                                    |
| **WPDCoNtextMenu.Email**       | WPD \_ 內容 \_ 類型 \_ 電子郵件                                                                                                      |
| **WPDCoNtextMenu 約會** | WPD \_ 內容 \_ 類型 \_ 約會                                                                                                |
| **WPDCoNtextMenu。工作**        | WPD \_ 內容 \_ 類型 \_ 工作                                                                                                       |
| **WPDCoNtextMenu**        | WPD \_ 內容 \_ 類型 \_ 備忘錄                                                                                                       |
| **WPDCoNtextMenu.ImageAlbum**  | WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯                                                                                               |
| **WPDCoNtextMenu.AudioAlbum**  | WPD \_ 內容 \_ 類型 \_ 音訊 \_ 專輯                                                                                               |
| **WPDCoNtextMenu.VideoAlbum**  | WPD \_ 內容 \_ 類型 \_ 影片 \_ 專輯                                                                                               |
| **WPDCoNtextMenu.MixedAlbum**  | WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯                                                                                      |
| **WPDCoNtextMenu 泛型**     | \_ \_ 未指定 WPD 內容類型 \_<br/> WPD \_ 內容 \_ 類型 \_ 一般 \_ 檔案<br/> WPD \_ 內容 \_ 類型 \_ 方案<br/> |



 

 

 





---
description: WPD \_ 內容 \_ 類型 \_ 音訊
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981026"
---
# <a name="wpd_content_type_audio"></a>WPD \_ 內容 \_ 類型 \_ 音訊

將其類型描述為 WPD \_ 內容 \_ 類型音訊的物件 \_ ，代表音訊檔案，例如 Windows Media 音訊 (WMA) 或 MP3 檔案。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。     |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                          |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                          |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。     |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                          |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                          |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                  |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。              |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                  |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                          |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。              |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                            |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                          |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                          |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                             |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                          |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                       |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                          |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                         |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                          |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                          |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果可以刪除物件，則為必要。                                             |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 總 \_ 位元速率](media-properties.md)                                            | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 位元速率 \_ 類型](media-properties.md)                                              | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 著作權](media-properties.md)                                                     | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 訂用帳戶 \_ 內容 \_ 識別碼](media-properties.md)                       | 如果此物件代表線上訂閱服務的內容，則建議使用此選項。 |
| [WPD \_ 媒體 \_ 使用 \_ 計數](media-properties.md)                                                    | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 略過 \_ 計數](media-properties.md)                                                  | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 上次 \_ 訪問 \_ 時間](media-properties.md)                                 | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 家長 \_ 評等](media-properties.md)                                        | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 中繼 \_ 類型](media-properties.md)                                                  | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 編輯器](media-properties.md)                                                       | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 有效 \_ 評等](media-properties.md)                                      | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 子 \_ 標題](media-properties.md)                                                    | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)                                              | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 取樣 \_ 率](media-properties.md)                                                | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 星級 \_ 分級](media-properties.md)                                                | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 使用者 \_ 有效 \_ 評等](media-properties.md)                           | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 標題](media-properties.md)                                                             | 必要。                                                                          |
| [WPD \_ 媒體 \_ 持續時間](media-properties.md)                                                       | 必要。                                                                          |
| [WPD \_ 媒體 \_ \_ 立即購買](media-properties.md)                                                        | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 編碼 \_ 設定檔](media-properties.md)                                      | 選擇性。                                                                          |
| [WPD \_ MEDIA \_ 演出者](media-properties.md)                                                                            | 建議使用。                                                                       |
| [WPD \_ MEDIA \_ 專輯 \_ 演出者](media-properties.md)                                                                     | 建議使用。                                                                       |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                                                                       | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)                                                                  | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                                                                       | 選擇性。                                                                          |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                                                             | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 時間 \_ 書簽](media-properties.md)                                                                    | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 位元組 \_ 書簽](media-properties.md)                                                                    | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ GUID](media-properties.md)                                                                              | 選擇性。                                                                          |
| [WPD \_ 媒體 \_ 子 \_ 描述](media-properties.md)                                                                  | 選擇性。                                                                          |
| [WPD \_ 音樂 \_ 專輯](music-properties.md)                                                             | 建議使用。                                                                       |
| [WPD \_ 音樂 \_ 軌](music-properties.md)                                                             | 建議使用。                                                                       |
| [WPD \_ 音樂 \_ 歌詞](music-properties.md)                                                           | 選擇性。                                                                          |
| [WPD \_ 音樂的 \_ 情緒](music-properties.md)                                                               | 選擇性。                                                                          |
| [WPD \_ 音訊 \_ 位元速率](audio-properties.md)                                                         | 建議使用。                                                                       |
| [WPD \_ 音訊 \_ 頻道 \_ 計數](audio-properties.md)                                            | 選擇性。                                                                          |
| [WPD \_ 音訊 \_ 格式 \_ 代碼](audio-properties.md)                                                | 選擇性。                                                                          |
| [WPD \_ 音訊 \_ 位 \_ 深度](audio-properties.md)                                                    | 選擇性。                                                                          |
| [WPD \_ 音訊 \_ 區塊 \_ 對齊](audio-properties.md)                                        | 選擇性。                                                                          |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                               | 必要或選擇性       | Description                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)      | 選擇性。                  | 包含完整的音訊檔案。                  |
| [**WPD \_ 資源 \_ 專輯 \_ 封面**](wpd-resource-album-art.md) | 建議使用（如果有的話）。 | 包含專輯的圖片。                |
| [**WPD \_ 資源 \_ AUDIOCLIP**](wpd-resource-audio-clip.md) | 選擇性。                  | 包含完整音訊檔案的範例剪輯。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




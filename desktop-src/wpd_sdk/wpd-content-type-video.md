---
description: WPD \_ 內容 \_ 類型 \_ 影片
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424119"
---
# <a name="wpd_content_type_video"></a>WPD \_ 內容 \_ 類型 \_ 影片

將其類型描述為 WPD \_ 內容 \_ 類型 video 的物件 \_ 代表影片檔案。

這種類型的物件支援下列屬性。



|  屬性名稱                             | 必要或選擇性              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                               |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                                                                    |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                                                                    |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                               |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                                                                    |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                                                                    |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                                                            |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                                                        |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                                                            |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                                                                    |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                                                        |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                                                                      |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                                                                    |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                                                                    |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                                                       |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                                                                    |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                                                                 |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                                                                    |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                                                                   |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                                                                    |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                                                                    |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果無法刪除物件，則為必要。                                                                                    |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 總 \_ 位元速率](media-properties.md)                                            | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 位元速率 \_ 類型](media-properties.md)                                              | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 著作權](media-properties.md)                                                     | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 訂用帳戶 \_ 內容 \_ 識別碼](media-properties.md)                       | 如果此物件代表線上訂閱服務的內容，則建議使用此選項。                                          |
| [WPD \_ 媒體 \_ 使用 \_ 計數](media-properties.md)                                                    | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 略過 \_ 計數](media-properties.md)                                                  | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 上次 \_ 訪問 \_ 時間](media-properties.md)                                 | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 家長 \_ 評等](media-properties.md)                                        | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 中繼 \_ 類型](media-properties.md)                                                  | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 編輯器](media-properties.md)                                                       | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 有效 \_ 評等](media-properties.md)                                      | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 子 \_ 標題](media-properties.md)                                                    | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)                                              | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 取樣 \_ 率](media-properties.md)                                                | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 星級 \_ 分級](media-properties.md)                                                | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 使用者 \_ 有效 \_ 評等](media-properties.md)                           | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 標題](media-properties.md)                                                             | 必要。                                                                                                                    |
| [WPD \_ 媒體 \_ 持續時間](media-properties.md)                                                       | 必要。                                                                                                                    |
| [WPD \_ 媒體 \_ \_ 立即購買](media-properties.md)                                                        | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 編碼 \_ 設定檔](media-properties.md)                                      | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 寬度](media-properties.md)                                                             | 必要。                                                                                                                    |
| [WPD \_ 媒體 \_ 高度](media-properties.md)                                                           | 必要。                                                                                                                    |
| [WPD \_ MEDIA \_ 演出者](media-properties.md)                                                           | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                                                  | 建議使用。                                                                                                                 |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)                                        | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                                                 | 選擇性。                                                                                                                    |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                                             | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 時間 \_ 書簽](media-properties.md)                                            | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 位元組 \_ 書簽](media-properties.md)                                            | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ GUID](media-properties.md)                                                               | 選擇性。                                                                                                                    |
| [WPD \_ 媒體 \_ 子 \_ 描述](media-properties.md)                                        | 選擇性。                                                                                                                    |
| [WPD \_ 影片 \_ 作者](video-properties.md)                                                           | 選擇性。                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ 站 \_ 名稱](video-properties.md)                       | 選擇性。                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER](video-properties.md)                   | 選擇性。                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT](video-properties.md)                                    | 選擇性。                                                                                                                    |
| [WPD \_ 影片 \_ 緩衝區 \_ 大小](video-properties.md)                                                | 選擇性。                                                                                                                    |
| [WPD \_ 影片 \_ 點數](video-properties.md)                                                         | 選擇性。                                                                                                                    |
| [WPD \_ 影片 \_ 主要 \_ 畫面 \_ 距離](video-properties.md)                                 | 選擇性。                                                                                                                    |
| [WPD \_ 視頻 \_ 品質 \_ 設定](video-properties.md)                                        | 選擇性。                                                                                                                    |
| [WPD \_ 影片 \_ 掃描 \_ 類型](video-properties.md)                                                    | 必要。                                                                                                                    |
| [WPD \_ 影片 \_ 位元速率](video-properties.md)                                                         | 必要。                                                                                                                    |
| [WPD \_ VIDEO \_ FOURCC 程式 \_ 代碼](video-properties.md)                                                | 如果編解碼器是 Microsoft Video for Windows (VFW) 、Microsoft DirectShow 和 Windows Media 格式所支援的，則為必要項。 |
| [WPD \_ 影片的 \_ 畫面播放速率](video-properties.md)                                                     | 選擇性。                                                                                                                    |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                              | 必要或選擇性       | 描述                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)     | 必要。                  | 包含 (檔案) 資料的影片。                                      |
| [**WPD \_ 資源 \_ 縮圖**](wpd-resource-thumbnail.md) | 建議使用（如果有的話）。 | 包含影片的主要畫面格或其他非空白範例框架。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




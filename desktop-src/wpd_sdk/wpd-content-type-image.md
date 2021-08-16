---
description: WPD \_ 內容 \_ 類型 \_ 影像
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846347ac83345ed685a10739126028ca1728bb16a52fe7083fcc7dd823447c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193492"
---
# <a name="wpd_content_type_image"></a>WPD \_ 內容 \_ 類型 \_ 影像

將其型別描述為 WPD \_ 內容 \_ 類型影像的物件 \_ 代表靜止影像。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                   |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                                        |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                                        |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                   |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                                        |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                                        |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                                |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                            |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                                |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                                        |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                            |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                                          |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                                        |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                                        |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                           |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                                        |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                                     |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                                        |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                                       |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                                        |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ BITDEPTH](image-properties.md)                                                       | 建議使用。                                                                                     |
| [WPD \_ 影像 \_ 裁剪 \_ 狀態](image-properties.md)                                          | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ 色彩已 \_ 更正 \_ 狀態](image-properties.md)                         | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ FNUMBER](image-properties.md)                                                                           | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ 曝光 \_ 時間](image-properties.md)                                                                    | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ 曝光 \_ 索引](image-properties.md)                                                                   | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ 水準 \_ 解析度](image-properties.md)                                                            | 選擇性。                                                                                        |
| [WPD \_ 影像 \_ 垂直 \_ 解析度](image-properties.md)                                                              | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 著作權](media-properties.md)                                                     | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 寬度](media-properties.md)                                                             | 必要。                                                                                        |
| [WPD \_ 媒體 \_ 高度](media-properties.md)                                                           | 必要。                                                                                        |
| [WPD \_ MEDIA \_ 演出者](media-properties.md)                                                                            | 建議使用。                                                                                     |
| [WPD \_ MEDIA \_ 專輯 \_ 演出者](media-properties.md)                                                                     | 建議使用。 這個屬性會識別原先建立此物件的人員或人員。 |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                                                                       | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)                                                                  | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                                                                       | 選擇性。                                                                                        |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                                                             | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 位元組 \_ 書簽](media-properties.md)                                                                    | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ GUID](media-properties.md)                                                                              | 選擇性。                                                                                        |
| [WPD \_ 媒體 \_ 子 \_ 描述](media-properties.md)                                                                  | 選擇性。                                                                                        |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                                 | 必要或選擇性 | Description                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)        | 必要。            | 包含影像資料。                                                                 |
| [**WPD \_ 資源 \_ 縮圖**](wpd-resource-thumbnail.md)    | 建議使用。         | 包含影像的縮圖。                                                    |
| [**WPD \_ 資源 \_ 音訊 \_ 剪輯**](wpd-resource-audio-clip.md) | 選擇性。            | 如果此影像有相關聯的音訊注釋，此資源就會包含音訊資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




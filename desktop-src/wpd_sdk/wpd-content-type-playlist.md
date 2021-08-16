---
description: WPD \_ 內容 \_ 類型 \_ 播放清單
ms.assetid: 4223970d-8c37-4326-a2df-bec558f8ac5e
title: WPD_CONTENT_TYPE_PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032f4cb1aeca4614efe5ad3b6b9634262a257a4391c299d90839cbc6ad9eacac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842298"
---
# <a name="wpd_content_type_playlist"></a>WPD \_ 內容 \_ 類型 \_ 播放清單

將其類型描述為 WPD \_ 內容 \_ 類型 \_ 播放清單的物件代表播放清單。 播放清單可以由實體檔案表示，也可以包含儲存為中繼資料的參考。

這種類型的物件支援下列屬性。



| 屬性名稱           | 必要或選擇性                 |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                  |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                                                                                      |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                                                                                      |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                 |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                                                                                      |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                                                                                      |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                                                                              |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                                                                          |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                                                                              |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                                                                                      |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                                                                          |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。亦即，如果參考儲存為中繼資料，而不是檔案中的實體資料。 |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                                                                                      |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                                                                                      |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                                                                         |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                                                                                      |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                                                                                   |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                                                                                      |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                                                                                     |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                                                                                      |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                                                                                      |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果無法刪除物件，則為必要。                                                                                                      |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                                                                                      |
| [WPD \_ 媒體 \_ 物件 \_ 書簽](object-properties.md)                                                                 | 建議使用。                                                                                                                                   |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                          | 必要或選擇性 | 描述                                                                                                                  |
|--------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md) | 選擇性。            | 如果播放清單是實體檔案（例如，列出要播放之媒體檔案的 XML 檔案），則這是實際的檔案位元組。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




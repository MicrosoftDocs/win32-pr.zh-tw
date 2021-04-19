---
description: WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯
ms.assetid: e2ae9f89-5a71-4443-b0c1-81e4c650e1bb
title: WPD_CONTENT_TYPE_IMAGE_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67a20f6a6628008e31b23a0ceb05fee4931793a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975230"
---
# <a name="wpd_content_type_image_album"></a>WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯

將其型別描述為 WPD \_ 內容 \_ 類型影像專輯的物件 \_ \_ 代表一組靜止影像。 影像專輯在功能上相當於影像檔案的播放清單，但是用來代表使用者的實體相片專輯。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                              |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。    |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                         |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                         |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。     |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                         |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                         |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                 |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (亦即，它代表) 的系統檔案。 |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                 |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                         |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。             |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                           |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                         |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                         |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                            |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                         |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                      |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                         |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                        |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                         |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性                                                                          |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果無法刪除物件，則為必要。                                         |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                         |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




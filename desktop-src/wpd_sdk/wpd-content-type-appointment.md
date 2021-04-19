---
description: WPD \_ 內容 \_ 類型 \_ 約會
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1ec4a316690241372bc7d0fa13789731dde925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987725"
---
# <a name="wpd_content_type_appointment"></a>WPD \_ 內容 \_ 類型 \_ 約會

將其類型描述為 WPD \_ 內容類型約會的物件， \_ 代表行事 \_ 曆中的約會。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                      |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                                      |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                      |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                      |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                              |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。          |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                              |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                      |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。          |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                        |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                         |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                      |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                   |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                     |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                      |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                      |
| [WPD \_ 約會 \_ 位置](appointment-properties.md)                                     | 必要。                                                                      |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果可以刪除物件，則為必要。                                         |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                      |
| [WPD \_ 一般 \_ 資訊 \_ 主體](object-properties.md)                                                            | 必要。                                                                      |
| [WPD \_ 一般 \_ 資訊 \_ 主體 \_ 文字](object-properties.md)                                                         | 建議使用。                                                                   |
| [WPD \_ 一般 \_ 資訊 \_ 優先順序](object-properties.md)                                                           | 建議使用。                                                                   |
| [WPD \_ 一般 \_ 資訊 \_ 開始 \_ 日期時間](object-properties.md)                                                    | 建議使用。                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME](object-properties.md)                                                      | 建議使用。                                                                   |
| [WPD \_ 一般 \_ 資訊 \_ 注意事項](object-properties.md)                                                              | 選擇性。                                                                      |
| [WPD \_ 約會 \_ 位置](object-properties.md)                                                                   | 必要。                                                                      |
| [WPD \_ 約會 \_ 類型](appointment-properties.md)                                             | 選擇性。                                                                      |
| [WPD \_ 預約 \_ 必填 \_ 出席者](appointment-properties.md)                | 選擇性。                                                                      |
| [WPD \_ 預約 \_ 選用 \_ 出席者](appointment-properties.md)                | 選擇性。                                                                      |
| [WPD \_ 約會已 \_ 接受 \_ 出席者](appointment-properties.md)                | 選擇性。                                                                      |
| [WPD \_ 約會 \_ 資源](appointment-properties.md)                                   | 選擇性。                                                                      |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




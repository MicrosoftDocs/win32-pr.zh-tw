---
description: WPD \_ 內容 \_ 類型 \_ 區段
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423778"
---
# <a name="wpd_content_type_section"></a>WPD \_ 內容 \_ 類型 \_ 區段

將其類型描述為 WPD \_ 內容類型區段的物件， \_ \_ 代表包含在另一個物件中的資料區段。 例如，大型音訊檔案可以描述為多個章節的集合，而且每個章節都可能是 WPD \_ 內容 \_ 類型 \_ 區段物件。

WPD \_ 物件 \_ 參考屬性可識別指定區段的父物件。

這種類型的物件支援下列屬性。



| 屬性名稱       | 必要或選擇性             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                           | 必要。                                                             |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                            | 必要。                                                             |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                                       | 如果物件代表檔案，則為必要。                             |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                                     | 必要。                                                             |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                                   | 必要。                                                             |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                                      | 必要。                                                             |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                               | 如果物件是隱藏的，則為必要項。                                     |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                               | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。 |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                                       | 如果物件至少有一個資源，則為必要項。                     |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                                         | 如果物件代表檔案，則為必要。                             |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                                  | 如果物件不打算供裝置取用，則建議使用。 |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                           | 如果物件具有其他物件的參考，則為必要。               |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                               | 選擇性。                                                             |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                                | 選擇性。                                                             |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                             | 如果物件受到 DRM 技術的保護，則為必要項。                |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                                      | 選擇性。                                                             |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                                    | 建議使用。                                                          |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                                    | 選擇性。                                                             |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則建議使用。            |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)                | 選擇性。                                                             |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md)            | 選擇性。                                                             |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                          | 如果無法刪除物件，則為必要。                             |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                           | 選擇性。                                                             |
| [WPD \_ 區段 \_ 資料 \_ 位移](section-attribute-properties.md)                                           | 必要。                                                             |
| [WPD \_ 區段 \_ 資料 \_ 長度](section-attribute-properties.md)                                           | 必要。                                                             |
| [WPD \_ 區段 \_ 資料 \_ 單位](section-attribute-properties.md)                                             | 建議使用。                                                          |
| [WPD \_ 區段 \_ 資料 \_ 參考的 \_ 物件 \_ 資源](section-attribute-properties.md) | 建議使用。                                                          |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




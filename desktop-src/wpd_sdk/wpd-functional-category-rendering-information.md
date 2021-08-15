---
description: WPD \_ 功能 \_ 類別 \_ 轉譯 \_ 資訊
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0665d9918726495d72b318b60a39a4713c01c9ad3a80ab0dbe15be5fc87576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083242"
---
# <a name="wpd_functional_category_rendering_information"></a>WPD \_ 功能 \_ 類別 \_ 轉譯 \_ 資訊

WPD \_ 功能 \_ 類別轉譯 \_ \_ 資訊功能物件描述裝置可轉譯的媒體檔案類型。



| 屬性名稱                                                                                                         | 必要或選擇性                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                         |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                         |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                                                                                      |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                                                                                  |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                                                                                      |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                                                                                              |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                                                                                  |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                                                                                                |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                                                                                 |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                                                                                              |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                                                                                           |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                                                                                             |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果無法刪除物件，則為必要。                                                                                                              |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                                                                                              |
| [WPD \_ 功能 \_ 物件 \_ 類別](miscellaneous-properties.md)                      | 必要。 如需 Windows 可攜式裝置所定義的分類，請參閱 [**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)。 |
| [WPD \_ 轉譯 \_ 資訊 \_ 設定檔](miscellaneous-properties.md)              | 必要。                                                                                                                                              |
| [WPD \_ 轉譯 \_ 資訊 \_ 設定檔 \_ 專案 \_ 類型](miscellaneous-properties.md)                                     | 選擇性。                                                                                                                                              |
| [WPD \_ 轉譯 \_ 資訊 \_ 設定檔 \_ 專案的 \_ \_ 資源](miscellaneous-properties.md)                      | 選擇性。                                                                                                                                              |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 




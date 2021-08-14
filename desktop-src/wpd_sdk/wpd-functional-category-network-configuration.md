---
description: WPD \_ 功能 \_ 類別 \_ 網路 \_ 設定
ms.assetid: c5c93ebf-0072-49c2-a109-a2edb7e1bd8d
title: WPD_FUNCTIONAL_CATEGORY_NETWORK_CONFIGURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c87647e206ed8dfd95a2eb4ee6f8833724a1a8a645beefc67be9254030570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193056"
---
# <a name="wpd_functional_category_network_configuration"></a>WPD \_ 功能 \_ 類別 \_ 網路 \_ 設定

WPD \_ 功能 \_ 類別網路 \_ 設定 \_ 功能物件會封裝裝置的網路設定功能，例如 WiFi 設定檔或合作關係。



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
| [\_允許 WPD 資料夾 \_ 內容 \_ 類型 \_](miscellaneous-properties.md)                 | 建議使用。                                                                                                                                           |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 




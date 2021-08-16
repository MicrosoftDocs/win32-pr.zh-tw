---
description: WPD \_ 功能 \_ 類別 \_ 裝置
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842214"
---
# <a name="wpd_functional_category_device"></a>WPD \_ 功能 \_ 類別 \_ 裝置

WPD \_ 功能 \_ 類別 \_ 裝置功能物件會將裝置封裝 (也就是裝置最上層的物件) 。 如果裝置會執行此功能類別目錄，除了針對 [裝置物件](device-object.md)所列出的屬性之外，它也應該支援這些屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                      |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                                                           |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 必要。                                                                                                           |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                      |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                                                           |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                                                           |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                                                   |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                                               |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                                                   |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                                                           |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                                               |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                                                             |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                                                           |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                                                           |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                                              |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                                                           |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                                                        |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                                                           |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                                                          |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                                                           |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                                                           |
| [WPD \_ 功能 \_ 物件 \_ 類別](miscellaneous-properties.md)                      | 必要。                                                                                                           |
| [WPD \_ 裝置 \_ 同步 \_ 夥伴](device-properties.md)                                           | 選擇性。                                                                                                           |
| [WPD \_ 裝置 \_ 固件 \_ 版本](device-properties.md)                                   | 必要。                                                                                                           |
| [WPD \_ 裝置 \_ 電源 \_ 等級](device-properties.md)                                             | 如果裝置有電池則建議使用。                                                                                |
| [WPD \_ 裝置 \_ 電源 \_ 來源](device-properties.md)                                           | 建議使用。                                                                                                        |
| [WPD \_ 裝置 \_ 通訊協定](device-properties.md)                                                    | 建議使用。                                                                                                        |
| [WPD \_ 裝置 \_ 製造商](device-properties.md)                                            | 必要。                                                                                                           |
| [WPD \_ 裝置 \_ 型號](device-properties.md)                                                          | 必要。                                                                                                           |
| [WPD \_ 裝置 \_ 序號 \_](device-properties.md)                                         | 必要。                                                                                                           |
| [WPD \_ 裝置 \_ 支援 \_ 非 \_ 取用](device-properties.md)                    | 如果裝置支援不可取用的物件，則為必要。亦即，如果裝置可用於簡單的資料儲存。 |
| [WPD \_ 裝置 \_ DATETIME](device-properties.md)                                                    | 選擇性。                                                                                                           |
| [WPD \_ 裝置 \_ 易記 \_ 名稱](device-properties.md)                                         | 建議使用。                                                                                                        |
| [WPD \_ 裝置 \_ 支援的 \_ DRM \_ 配置](device-properties.md)                        | 如果裝置支援 DRM 技術，則建議使用此選項。                                                                  |
| [\_ \_ 已排序 WPD 裝置支援 \_ \_ 的格式 \_](device-properties.md)       | 如果裝置支援慣用的格式順序，則建議使用。                                                       |
| [WPD \_ 裝置 \_ 類型](device-properties.md)                                                            | 建議使用。                                                                                                        |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 




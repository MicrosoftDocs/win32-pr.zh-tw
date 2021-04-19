---
description: WPD \_ 功能 \_ 類別 \_ 儲存體
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987748"
---
# <a name="wpd_functional_category_storage"></a>WPD \_ 功能 \_ 類別 \_ 儲存體

WPD \_ 功能 \_ 類別 \_ 儲存體功能物件會將實體檔案儲存體封裝在裝置上。



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
| [WPD \_ 功能 \_ 物件 \_ 類別](miscellaneous-properties.md)                      | 必要。 請參閱 Windows 可攜式裝置所定義分類的 [**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md) 。 |
| [WPD \_ 儲存體 \_ 類型](storage-properties.md)                                                         | 必要。                                                                                                                                              |
| [WPD \_ 儲存體 \_ 檔 \_ 系統 \_ 類型](storage-properties.md)                               | 選擇性。                                                                                                                                              |
| [WPD \_ 儲存體 \_ 容量](storage-properties.md)                                                 | 必要。                                                                                                                                              |
| [WPD \_ 儲存體 \_ 可用 \_ 空間 \_ \_ （以位元組為單位）](storage-properties.md)                        | 選擇性。                                                                                                                                              |
| [WPD \_ \_ \_ \_ 物件中的儲存體可用空間 \_](storage-properties.md)                    | 選擇性。                                                                                                                                              |
| [WPD \_ 儲存體 \_ 描述](storage-properties.md)                                           | 選擇性。                                                                                                                                              |
| [WPD \_ 儲存體 \_ 序號 \_](storage-properties.md)                                      | 選擇性。                                                                                                                                              |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                    | 必要或選擇性 | Description                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**WPD \_ 資源 \_ 圖示**](wpd-resource-icon.md) | 選擇性。            | 包含此儲存體的圖示表示。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 




---
description: WPD \_ 內容 \_ 類型行事 \_ 曆
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819955c0554269deb26c6b6f7f7f3c74ee8715e2dca804b5d3d554b9657be524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927868"
---
# <a name="wpd_content_type_calendar"></a>WPD \_ 內容 \_ 類型行事 \_ 曆

將其型別描述為 WPD \_ 內容 \_ 類型行事 \_ 曆的物件代表行事曆。 物件可以是包含行事曆資訊或資料夾的檔案，其中包含與其他行事曆相關的物件，例如工作、約會等等。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                         | 必要或選擇性                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要。                                                             |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                             |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 如果物件代表檔案，則為必要。                             |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要。                                                             |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                             |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                             |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                     |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。 |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                     |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                             |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。 |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。               |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                             |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                             |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                             |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                          |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                             |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                     | 如果物件是由另一個物件參考，則建議使用。            |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                             |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                             |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                               | 如果可以刪除物件，則為必要。                                |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                             |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                          | 必要或選擇性                             | 描述        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md) | 如果物件是由二進位資料所支援，則為必要項。 | 包含資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




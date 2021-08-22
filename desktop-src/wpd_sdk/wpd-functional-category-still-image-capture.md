---
description: WPD \_ 功能 \_ 類別 \_ 仍為 \_ 影像 \_ 捕捉
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fb0f6f19930780784083eaeddc1156bf55c99943aae8ad5850374c04211dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444808"
---
# <a name="wpd_functional_category_still_image_capture"></a>WPD \_ 功能 \_ 類別 \_ 仍為 \_ 影像 \_ 捕捉

WPD \_ 功能 \_ 類別仍為「 \_ \_ 影像捕捉」 \_ 功能物件，會在裝置上封裝仍為影像捕捉功能，例如相機或相機附件。



| 屬性名稱                                                                                                            | 必要或選擇性                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                   | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                         |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                    | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                               | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                             | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。                                                                         |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                           | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                              | 必要。                                                                                                                                              |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                       | 如果物件是隱藏的，則為必要項。                                                                                                                      |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                       | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                                                                                  |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                               | 如果物件至少有一個資源，則為必要項。                                                                                                      |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                                 | 如果物件代表檔案，則為必要。                                                                                                              |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                          | 如果物件不打算供裝置取用，則建議使用。                                                                                  |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                   | 如果物件具有其他物件的參考，則為必要。                                                                                                |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                       | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                        | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                     | 如果物件受到 DRM 技術的保護，則為必要項。                                                                                                 |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                              | 選擇性。                                                                                                                                              |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                            | 建議使用。                                                                                                                                           |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                            | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                   | 如果物件是由另一個物件參考，則建議使用。                                                                                             |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)        | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md)    | 選擇性。                                                                                                                                              |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                        | 如果無法刪除物件，則為必要。                                                                                                              |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                   | 選擇性。                                                                                                                                              |
| [WPD \_ 功能 \_ 物件 \_ 類別](miscellaneous-properties.md)                         | 必要。 如需 Windows 可攜式裝置所定義的分類，請參閱 [**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)。 |
| [WPD \_ 仍然是 \_ 映射 \_ 捕獲 \_ 解析](still-image-properties.md)                  | 必要。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 格式](still-image-properties.md)                          | 必要。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 壓縮 \_ 設定](still-image-properties.md)                | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像的 \_ 白色 \_ 餘額](still-image-properties.md)                            | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像 \_ RGB \_ 增益](still-image-properties.md)                                      | 選擇性。                                                                                                                                              |
| [WPD \_ 仍為 \_ 影像 \_ FNUMBER](still-image-properties.md)                                         | 選擇性。                                                                                                                                              |
| [WPD \_ 仍為 \_ 影像 \_ 焦點 \_ 長度](still-image-properties.md)                              | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像 \_ 焦點 \_ 距離](still-image-properties.md)                          | 選擇性。                                                                                                                                              |
| [WPD \_ 仍為 \_ 影像 \_ 焦點 \_ 模式](still-image-properties.md)                                  | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 計量 \_ 模式](still-image-properties.md)         | 選擇性。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 閃爍 \_ 模式](still-image-properties.md)                                  | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 時間](still-image-properties.md)                            | 選擇性。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 曝光 \_ 程式 \_ 模式](still-image-properties.md)           | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 索引](still-image-properties.md)                          | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像 \_ 曝光 \_ 偏差 \_ 補償](still-image-properties.md) | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 映射 \_ 捕捉 \_ 延遲](still-image-properties.md)                            | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 模式](still-image-properties.md)                              | 選擇性。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 對比](still-image-properties.md)                                       | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像 \_ 清晰度](still-image-properties.md)                                     | 選擇性。                                                                                                                                              |
| [WPD \_ 仍 \_ 影像 \_ 數位 \_ 縮放](still-image-properties.md)                              | 選擇性。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 效果 \_ 模式](still-image-properties.md)                                | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是影像高載 \_ \_ \_ 數目](still-image-properties.md)                              | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是影像高載 \_ \_ \_ 間隔](still-image-properties.md)                          | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ TIMELAPSE \_ 數位](still-image-properties.md)                      | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ TIMELAPSE \_ 間隔](still-image-properties.md)                  | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 焦點 \_ 計量 \_ 模式](still-image-properties.md)               | 選擇性。                                                                                                                                              |
| [WPD \_ 仍然是 \_ 影像 \_ 上傳 \_ URL](still-image-properties.md)                                  | 選擇性。                                                                                                                                              |
| [WPD \_ 靜止 \_ 影像 \_ 演出者](still-image-properties.md)                                           | 選擇性。                                                                                                                                              |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

其中許多屬性都有互連的效果。 例如，如果 **WPD 仍為「 \_ \_ 影像曝光」 \_ \_ 計量 \_ 模式** 設定為「自動」，則會連結 f-停止、曝光時間及曝光計量，而不同的計量會導致其他人改變。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 




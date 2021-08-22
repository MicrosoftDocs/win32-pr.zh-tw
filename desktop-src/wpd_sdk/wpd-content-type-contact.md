---
description: WPD \_ 內容 \_ 類型 \_ 連絡人
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8354aa444f476e7c0b64d2e3d14d474c6eea02f90e8313c20073db2d0368fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083332"
---
# <a name="wpd_content_type_contact"></a>WPD \_ 內容 \_ 類型 \_ 連絡人

將其型別描述為 WPD \_ 內容 \_ 類型 CONTACT 的物件 \_ 代表個人連絡人資料。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                                                   | 必要或選擇性                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                           | 必要。                                                                      |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                                      | 如果物件代表檔案，則為必要。                                      |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                                    | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                                  | 必要。                                                                      |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                                     | 必要。                                                                      |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                              | 如果物件是隱藏的，則為必要項。                                              |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                              | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。          |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                                      | 如果物件至少有一個資源，則為必要項。                              |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                                        | 如果物件代表檔案，則為必要。                                      |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                                 | 如果物件不打算供裝置取用，則建議使用。          |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                          | 如果物件具有其他物件的參考，則為必要。                        |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                              | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                               | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                            | 如果物件受到 DRM 技術的保護，則為必要項。                         |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                                     | 選擇性。                                                                      |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                                   | 建議使用。                                                                   |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                                   | 選擇性。                                                                      |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                          | 如果物件是由另一個物件參考，則建議使用。                     |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)               | 選擇性。                                                                      |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md)           | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 顯示 \_ 名稱](contact-properties.md)                                                  | 必要。                                                                      |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                               | 如果無法刪除物件，則為必要。                                      |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                          | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 顯示 \_ 名稱](contact-properties.md)                                                                           | 必要。                                                                      |
| [WPD \_ 連絡人的 \_ 名字 \_](contact-properties.md)                                                      | 建議使用。                                                                   |
| [WPD \_ 連絡人 \_ 中間 \_ 名](contact-properties.md)                                                  | 建議使用。                                                                   |
| [WPD \_ 連絡人 \_ 姓氏 \_](contact-properties.md)                                                        | 建議使用。                                                                   |
| [WPD \_ 連絡人 \_ 首碼](contact-properties.md)                                                               | 建議使用。                                                                   |
| [WPD \_ 連絡人 \_ 尾碼](contact-properties.md)                                                               | 建議使用。                                                                   |
| [WPD \_ CONTACT \_ 拼音 \_ 名字 \_](contact-properties.md)                                   | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 注音的 \_ 姓氏 \_](contact-properties.md)                                     | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FULL \_ 郵政 \_ 位址](contact-properties.md)                | 建議使用。                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ 郵政 \_ 位址 \_ LINE1](contact-properties.md)              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ 郵政 \_ 位址 \_ LINE2](contact-properties.md)              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ 郵政 \_ 位址 \_ 城市](contact-properties.md)                | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ 郵政 \_ 位址 \_ 區域](contact-properties.md)            | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ 郵政 \_ 位址 \_ 郵遞區號 \_](contact-properties.md) | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 個人 \_ 郵寄 \_ 位址 \_ 國家/地區](contact-properties.md)          | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ 完整 \_ 郵寄 \_ 位址](contact-properties.md)                | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ 郵政 \_ 位址 \_ LINE1](contact-properties.md)              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ 郵寄 \_ 位址 \_ LINE2](contact-properties.md)              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 公司 \_ 郵寄 \_ 位址 \_ 城市](contact-properties.md)                | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 商務 \_ 郵寄 \_ 位址 \_ 區域](contact-properties.md)            | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 商務 \_ 郵寄 \_ 位址 \_ 郵遞區號 \_](contact-properties.md) | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 公司 \_ 郵寄 \_ 位址 \_ 國家/地區](contact-properties.md)          | 選擇性。                                                                      |
| [WPD \_ 聯繫 \_ 其他 \_ 完整的 \_ 郵寄 \_ 位址](contact-properties.md)                      | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 其他 \_ 郵政 \_ 位址 \_ LINE1](contact-properties.md)                    | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 其他 \_ 郵寄 \_ 位址 \_ LINE2](contact-properties.md)                    | 選擇性。                                                                      |
| [WPD \_ 聯繫 \_ 其他 \_ 郵寄 \_ 位址 \_ 城市](contact-properties.md)                      | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 其他 \_ 郵寄 \_ 位址 \_ 區域](contact-properties.md)                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 其他 \_ 郵寄 \_ 位址 \_ 郵遞區號 \_](contact-properties.md)       | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 其他 \_ 郵寄 \_ 位址 \_ 郵寄 \_ 國家/地區](contact-properties.md) | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 主要 \_ 電子郵件 \_ 位址](contact-properties.md)                               | 建議使用。                                                                   |
| [WPD \_ 連絡人 \_ 個人 \_ 電子郵件](contact-properties.md)                                              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ EMAIL2](contact-properties.md)                                            | 選擇性。                                                                      |
| [WPD \_ 聯絡 \_ 公司 \_ 電子郵件](contact-properties.md)                                              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL2](contact-properties.md)                                            | 選擇性。                                                                      |
| [WPD \_ 聯繫 \_ 其他 \_ 電子郵件](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 主要 \_ 電話](contact-properties.md)                                                | 建議使用。                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE](contact-properties.md)                                              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ 電話2](contact-properties.md)                                            | 選擇性。                                                                      |
| [WPD \_ 聯絡 \_ 公司 \_ 電話](contact-properties.md)                                              | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ 電話2](contact-properties.md)                                            | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 移動 \_ 電話](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ 電話2](contact-properties.md)                                                | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FAX](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FAX](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 呼機](contact-properties.md)                                                                 | 選擇性。                                                                      |
| [WPD \_ 聯繫 \_ 其他 \_ 電話](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 主要 \_ 網址 \_](contact-properties.md)                                   | 建議使用。                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ WEB \_ ADDRESS](contact-properties.md)                                 | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ 網址 \_](contact-properties.md)                                 | 選擇性。                                                                      |
| [WPD \_ 聯絡 \_ 立即 \_ MESSENGER](contact-properties.md)                                        | 建議                                                                    |
| [WPD \_ CONTACT \_ 立即 \_ MESSENGER2](contact-properties.md)                                      | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 立即 \_ MESSENGER3](contact-properties.md)                                      | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 公司 \_ 名稱](contact-properties.md)                                                  | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 拼音 \_ 公司 \_ 名稱](contact-properties.md)                               | 選擇性                                                                       |
| [WPD \_ 連絡人 \_ 角色](contact-properties.md)                                                                   | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 出生日期](contact-properties.md)                                                         | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 主要 \_ 傳真](contact-properties.md)                                                                            | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 配偶](contact-properties.md)                                                                                  | 選擇性。                                                                      |
| [WPD \_ 連絡人 \_ 子女](contact-properties.md)                                                                                | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ ASSISTANT](contact-properties.md)                                                                               | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 周年 \_ 日](contact-properties.md)                                                                       | 選擇性。                                                                      |
| [WPD \_ CONTACT \_ 鈴聲](contact-properties.md)                                                                                | 選擇性。                                                                      |
| [WPD \_ 一般 \_ 資訊 \_ 注意事項](object-properties.md)                                                                        | 選擇性。                                                                      |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                                       | 必要或選擇性       | 描述                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)              | 選擇性。                  | 包含連絡人資料。         |
| [**WPD \_ 資源 \_ 連絡人 \_ 相片**](wpd-resource-contact-photo.md) | 建議使用（如果有的話）。 | 包含連絡人的圖片。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




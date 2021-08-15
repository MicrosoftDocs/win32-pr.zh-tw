---
description: WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58121d351219c246117106d578ed3672ebf25eecf9e159f957494b5c5eae9280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193522"
---
# <a name="wpd_content_type_functional_object"></a>WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件

將其型別描述為 WPD \_ 內容 \_ 功能物件的物件 \_ ，代表可封裝裝置功能的功能物件。

無論何種類型，所有功能物件都支援下列屬性。  (如果您定義自訂功能物件，它也必須支援這些屬性。 ) 



| 屬性名稱                                                                                                         | 必要或選擇性                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                                                | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。        |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                                 | 必要。                                                                             |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                            | 必要。                                                                             |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)                          | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。        |
| [WPD \_ 物件 \_ 格式](object-properties.md)                                                        | 必要。                                                                             |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                                           | 必要。                                                                             |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                                    | 如果物件是隱藏的，則為必要項。                                                     |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                                    | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。                 |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                                            | 如果物件至少有一個資源，則為必要項。                                     |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)                              | 如果物件代表檔案，則為必要。                                             |
| [不可取用的 WPD \_ 物件 \_ \_](object-properties.md)                                       | 如果物件不打算供裝置取用，則建議使用。                 |
| [WPD \_ 物件 \_ 參考](object-properties.md)                                                | 如果物件具有其他物件的參考，則為必要。                               |
| [WPD \_ 物件 \_ 關鍵字](object-properties.md)                                                    | 選擇性。                                                                             |
| [WPD \_ 物件 \_ 同步 \_ 識別碼](object-properties.md)                                                     | 選擇性。                                                                             |
| [WPD \_ 物件 \_ 受到 \_ DRM \_ 保護](object-properties.md)                                  | 如果物件受到 DRM 技術的保護，則為必要項。                                |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                                           | 選擇性。                                                                             |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 建議使用。                                                                          |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                                         | 選擇性。                                                                             |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)                                                                | 如果物件是由另一個物件參考，則建議使用。                            |
| [WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼](object-properties.md)     | 選擇性。                                                                             |
| [WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_](object-properties.md) | 選擇性。                                                                             |
| [WPD \_ 物件 \_ 可以 \_ 刪除](object-properties.md)                                                                     | 如果無法刪除物件，則為必要。                                             |
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 選擇性。                                                                             |
| [WPD \_ 功能 \_ 物件 \_ 類別](miscellaneous-properties.md)                      | 必要。 請參閱下表，以瞭解 Windows 可攜式裝置所定義的分類。 |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="functional-object-categories"></a>功能物件類別

您可以根據函式的功能，將功能物件分組為類別。 類別是由 WPD \_ 功能 \_ 物件 \_ 類別屬性描述， (GUID 值) 。 類別會決定支援哪些其他屬性。

下表說明 Windows 可攜式裝置所定義的分類。 請參閱類別的描述，以瞭解物件所支援的其他屬性和資源。



| 功能類別                                                                                        | Description                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ 功能 \_ 類別 \_ 全部**](wpd-functional-category-all.md)                                      | 這個功能類別目錄只會用來做為特定查詢函式的參數 (指出所有功能物件類型都可接受) ，而且不是驅動程式所報告的功能類別。 |
| [**WPD \_ 功能 \_ 類別 \_ 音訊 \_ 捕獲**](wpd-functional-category-audio-capture.md)                 | 物件會在裝置上封裝音訊捕捉功能，例如，答錄機或其他音訊錄製元件。                                                                      |
| [**WPD \_ 功能 \_ 類別 \_ 裝置**](wpd-functional-category-device.md)                                | 物件會封裝裝置 (也就是裝置最上層的物件) 。                                                                                                                          |
| [**WPD \_ 功能 \_ 類別 \_ 網路 \_ 設定**](wpd-functional-category-network-configuration.md) | 物件會封裝裝置的網路設定功能，例如 WiFi 設定檔或合作關係。                                                                                   |
| [**WPD \_ 功能 \_ 類別 \_ 轉譯 \_ 資訊**](wpd-functional-category-rendering-information.md) | 物件描述裝置能夠播放的媒體檔案類型。                                                                                                                            |
| [**WPD \_ 功能 \_ 類別 \_ SMS**](wpd-functional-category-sms.md)                                      | 物件會封裝短訊息服務功能， (在裝置上通常稱為「文字訊息」 ) 。                                                                                             |
| [**WPD \_ 功能 \_ 類別 \_ 仍為 \_ 影像 \_ 捕捉**](wpd-functional-category-still-image-capture.md)    | 物件會在裝置上封裝靜止的影像捕捉功能，例如相機或相機附件。                                                                                              |
| [**WPD \_ 功能 \_ 類別 \_ 儲存體**](wpd-functional-category-storage.md)                              | 物件會將實體檔案儲存體封裝在裝置上。                                                                                                                                              |
| [**WPD \_ 功能 \_ 類別 \_ 影片 \_ 捕獲**](wpd-functional-category-video-capture.md)                 | 物件會在裝置上封裝影片捕捉功能，例如，影片錄製器元件。 應用程式會使用這個物件來進行以程式設計的方式控制。                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 




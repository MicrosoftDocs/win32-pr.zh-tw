---
description: 註冊檔案類型是建立檔案關聯的第一個步驟，這會使該檔案類型 &\# 0034; 已知&\# 0034; 到 Shell。 但是，如果沒有檔案類型處理常式，Shell 就無法從和檔案公開資訊給使用者。
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: 檔案類型處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847915"
---
# <a name="file-type-handlers"></a>檔案類型處理常式

[註冊檔案類型](fa-how-work.md) 是建立檔案關聯的第一個步驟，這會使該檔案類型「知道」至 Shell。 但是，如果沒有檔案類型處理常式，Shell 就無法從和檔案公開資訊給使用者。

本主題的組織方式如下：

-   [使檔案類型知道 Shell](#make-a-file-type-known-to-shell)
-   [檔案類型處理常式描述](#file-type-handler-descriptions)
-   [相關主題](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>使檔案類型知道 Shell

在下列 Windows 檔案總管的螢幕擷取畫面中，影像檔案 Desert 會出現在 [Shell **圖片** ] 媒體櫃中，而且只會與油漆應用程式相關聯。

![顯示 explorer 開啟沒有檔案類型之影像的螢幕擷取畫面](images/file-assoc/fileassoc-filetypehandler.png)

上一個螢幕擷取畫面中的 Desert 已知檔案缺少下列由檔案類型處理常式啟用的功能：

-   縮圖或預覽
-   快速鍵功能表中的影像特定動詞，例如：
    -   輪替預覽
    -   設定為桌面背景
    -   列印
-   **詳細資料** 窗格中的影像特定屬性，例如：
    -   拍攝日期
    -   標籤
    -   分級
-   為檔案文字編制索引

在下列螢幕擷取畫面中，相同的檔案 (Desert。已知的) 具有 .jpg 副檔名，也就是具有相關檔案類型處理常式的已註冊檔案類型，因此會顯示縮圖影像和其他屬性。

![具有已註冊檔案類型和相關檔案類型處理常式的影像](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>檔案類型處理常式描述

下表列出每個檔案類型處理常式所提供的功能：



| 處理常式                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [快速鍵功能表](context-menu-handlers.md)                   | 快捷方式功能表處理常式（有時稱為內容功能表處理常式）是一種檔案類型處理常式，可將命令新增至現有的內容功能表。 這些處理常式會與特定檔案類型相關聯，並且在每次對檔案類型的成員顯示內容功能表時呼叫。                                                                                                                                                                                                                                                                           |
| [縮圖](thumbnail-providers.md)                         | 提供影像以表示 Shell 專案的處理常式。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [屬性](../properties/building-property-handlers-properties.md) | 屬性處理常式，可存取 Windows Search、Windows 檔案總管和其他需要存取屬性之應用程式的專案屬性。                                                                                                                                                                                                                                                                                                                                                                                                              |
| [預覽](preview-handlers.md)                              | 一個處理常式，可快速產生要在 Windows 檔案總管預覽窗格中顯示之專案的唯讀、簡單視圖。                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [篩選條件](../search/-search-3x-wds-extidx-filters.md)              | 此為 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行篩選，可掃描檔中的文字和屬性 (也稱為屬性) 。 它會從這些檔中解壓縮文字區塊，篩選出內嵌的格式，並保留文字位置的相關資訊。 它也會解壓縮值的區塊，這些值是整份檔的屬性，或是檔的定義完善部分。 **IFilter** 提供建立高階應用程式的基礎，例如檔索引子和與應用程式無關的檢視器。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 

---
description: 物件的需求
ms.assetid: 4c3da994-fe12-4cb8-8f11-c4930cae96af
title: 物件的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51265b4334e43ab6aec4cdef313ae0002cc66bf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193934"
---
# <a name="requirements-for-objects"></a>物件的需求

WPD 會依內容類型分類所有物件。 特定類型的物件必須支援屬性和資源的最小清單 (以及裝置物件的一組命令) 。 物件的類型是由其 [WPD \_ 物件 \_ 內容 \_ 類型](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) 屬性描述，每個物件都必須支援此屬性。

WPD 會將下列內容類型定義 (為 GUID 值) 。 廠商可透過提供自己的 GUID，自由建立自己的自訂內容類型。

請注意，一般用途的應用程式通常只會處理其中一個預先定義的類型。 當然，廠商的應用程式可以充分利用他們所知道的自訂類型。

若要瞭解每個都必須支援的屬性和資源，請參閱下列各物件類型的 [描述] 頁面。



| 內容類型 GUID                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ 內容 \_ 類型 \_ 全部**](wpd-content-type-all.md)                                   | 此內容類型只適用于特定的查詢方法，以指出您對所有裝置類型有興趣，您無法建立此類型的物件。如果您要設計自訂物件，則至少必須支援這些屬性。<br/>                                                                                                                                 |
| [**WPD \_ 內容 \_ 類型 \_ 約會**](wpd-content-type-appointment.md)                   | 物件是行事曆中的約會。                                                                                                                                                                                                                                                                                                                                                          |
| [**WPD \_ 內容 \_ 類型 \_ 音訊**](wpd-content-type-audio.md)                               | 物件是音訊檔案，例如 WMA 或 MP3 檔案。                                                                                                                                                                                                                                                                                                                                              |
| [**WPD \_ 內容 \_ 類型 \_ 音訊 \_ 專輯**](wpd-content-type-audio-album.md)                  | 物件是音訊專輯。                                                                                                                                                                                                                                                                                                                                                                        |
| [**WPD \_ 內容 \_ 類型行事 \_ 曆**](wpd-content-type-calendar.md)                         | 物件是行事曆。                                                                                                                                                                                                                                                                                                                                                                            |
| [**WPD \_ 內容 \_ 類型 \_ 憑證**](wpd-content-type-certificate.md)                   | 物件是用來進行驗證的憑證。                                                                                                                                                                                                                                                                                                                                                 |
| [**WPD \_ 內容 \_ 類型 \_ 連絡人**](wpd-content-type-contact.md)                           | 物件是個人連絡人資料，例如 vCard 檔。                                                                                                                                                                                                                                                                                                                                           |
| [**WPD \_ 內容 \_ 類型 \_ 連絡人 \_ 群組**](wpd-content-type-contact-group.md)              | 物件代表一組連絡人。 這個物件的 WPD \_ 物件 \_ 參考屬性包含各種 WPD \_ 內容 \_ 類型連絡人物件的物件識別碼清單 \_ 。                                                                                                                                                                                                                     |
| [**WPD \_ 內容 \_ 類型 \_ 檔**](wpd-content-type-document.md)                         | 物件是文字的容器（不論是否有格式）。 範例包括 Microsoft Word 檔案和純文字檔。                                                                                                                                                                                                                                                                          |
| [**WPD \_ 內容 \_ 類型 \_ 電子郵件**](wpd-content-type-email.md)                               | 物件是電子郵件。                                                                                                                                                                                                                                                                                                                                                                             |
| [**WPD \_ 內容 \_ 類型 \_ 資料夾**](wpd-content-type-folder.md)                             | 物件是資料夾。                                                                                                                                                                                                                                                                                                                                                                              |
| [**WPD \_ 內容 \_ 類型 \_ 功能 \_ 物件**](wpd-content-type-functional-object.md)      | 物件是功能物件，代表裝置功能。                                                                                                                                                                                                                                                                                                                                |
| [**WPD \_ 內容 \_ 類型 \_ 一般 \_ 檔案**](wpd-content-type-generic-file.md)                | 物件是一般的實體檔案，其不屬於任何其他預先定義的檔案內容類型。                                                                                                                                                                                                                                                                                  |
| [**WPD \_ 內容 \_ 類型 \_ 影像**](wpd-content-type-image.md)                               | 物件是靜止影像，例如 JPEG 檔案。                                                                                                                                                                                                                                                                                                                                                    |
| [**WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯**](wpd-content-type-image-album.md)                  | 物件是影像專輯。                                                                                                                                                                                                                                                                                                                                                                        |
| [**WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換**](wpd-content-type-memo.md)                          | 物件是媒體轉換物件。 媒體轉換物件可以代表將相關內容群組在線上發佈的容器物件。 例如，RSS 通道可以表示為媒體轉型物件，而這個物件的 WPD \_ 物件 \_ REFERENCES 屬性包含代表通道中每一個專案的物件識別碼清單。                                                       |
| [**WPD \_ 內容 \_ 類型 \_ 備忘錄**](wpd-content-type-memo.md)                                 | 物件代表備忘錄資料，例如文字筆記。                                                                                                                                                                                                                                                                                                                                           |
| [**WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯**](wpd-content-type-mixed-content-album.md) | 物件是混合媒體物件的專輯，例如音訊、影像和影片檔案。                                                                                                                                                                                                                                                                                                            |
| [**WPD \_ 內容 \_ 類型 \_ 播放清單**](wpd-content-type-playlist.md)                         | 物件是播放清單。                                                                                                                                                                                                                                                                                                                                                                            |
| [**WPD \_ 內容 \_ 類型 \_ 方案**](wpd-content-type-program.md)                           | 物件代表可以執行的檔案，例如腳本或可執行檔。                                                                                                                                                                                                                                                                                                                |
| [**WPD \_ 內容 \_ 類型 \_ 區段**](wpd-content-type-section.md)                           | 物件描述包含在另一個物件中的資料區段。 例如，一系列的章節最可能會說明大型音訊檔案。 每一章都可以是 WPD \_ 內容 \_ 類型 \_ 區段物件，其具有自己的章節藝術、中繼資料等，而其資料是大型音訊檔案的子集 (例如，第一章是前10分鐘，第二章是接下來的20分鐘，依此類推) 。 |
| [**WPD \_ 內容 \_ 類型 \_ 工作**](wpd-content-type-task.md)                                 | 物件是一項工作，例如待辦事項清單中的專案。                                                                                                                                                                                                                                                                                                                                               |
| [**WPD \_ 內容 \_ 類型 \_ 電視**](wpd-content-type-television.md)                     | 物件是電視節目。                                                                                                                                                                                                                                                                                                                                                                |
| [**\_ \_ 未指定 WPD 內容類型 \_**](wpd-content-type-unspecified.md)                   | 物件是不屬於預先定義之 WPD 內容類型的泛型物件。                                                                                                                                                                                                                                                                                                             |
| [**WPD \_ 內容 \_ 類型 \_ 影片**](wpd-content-type-video.md)                               | 物件是一種影片，例如 WMV 或 AVI 檔。                                                                                                                                                                                                                                                                                                                                                    |
| [**WPD \_ 內容 \_ 類型 \_ 影片 \_ 專輯**](wpd-content-type-video-album.md)                  | 物件是影片專輯。                                                                                                                                                                                                                                                                                                                                                                         |
| [**WPD \_ 內容 \_ 類型 \_ 無線 \_ 設定檔**](wpd-content-type-wireless-profile.md)        | 物件包含無線網路存取訊號。                                                                                                                                                                                                                                                                                                                                             |
| [裝置物件](device-object.md)                                                        | 不是 PROPERTYKEY，但所有物件都必須支援本節中所列的屬性。                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> </dl>

 


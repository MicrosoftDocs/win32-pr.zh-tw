---
title: " (舊版 Windows 環境功能的架構) "
description: 架構會記載索引用來儲存資料以進行索引編制或排序的值和屬性。
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a122959b007ba4d4434e65b53fc2e330857cafe
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "104023147"
---
# <a name="schema"></a>結構描述

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

架構會記載索引用來儲存資料以進行索引編制或排序的值和屬性。 架構資料表會列出資料行及其屬性 (類型與 propid) 包含在適用于 Microsoft Windows 桌面搜尋 (WDS) 2.6.5 的架構中。

## <a name="schema"></a>結構描述



| 資料行名稱                  | Description                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | 註解                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| 建立                       | 建立檔案的日期和時間                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | 專案的使用者易記資料夾                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | 檔作者                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | 類別                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | 關鍵字                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Subject (Re：、Fw：等等 ) 的前置詞                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | 標題                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | 登錄中的檔案類型使用者易記描述 (例如： psq--> Product Studio 查詢檔)                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | 上層資料夾的名稱                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/資料夾                   |
| IsAttachment                 | 表示專案是附件                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | 指出專案已標示為要刪除 (回收站、已刪除的專案等 )                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | 使用者上次查看專案的日期                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| 人員                       | 參與此專案的人員                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/人員                       |
| PerceivedType                | 物件附注的 PerceivedType：這只適用于抓取。                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | PerceivedType 的顯示名稱。永不顯示或查詢                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | 最有趣的日期 (檔案的上次寫入時間、電子郵件收到的日期)                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| 大小                         | 檔案的大小。                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | 檔案的主體。 注意：目前，電子郵件主旨會對應至 PrimaryTitle，而不會因為其長度而重複出現 | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | 以查詢為基礎的 URL                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| 寫入                        | 上次寫入檔案的日期和時間                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | 專案的到期日                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | 表示專案未完全可用                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | 指出專案已標示為已完成                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | 指出專案已加上旗標                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | 顯示給旗標的文字，例如，評論、後續操作等等。                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| 身分識別                     | OE 使用者的身分識別                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/身分識別                     |
| IsRead                       | 表示已讀取專案                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| 重要性                   | MAPI 重要性或優先順序                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/重要性                   |
| ContainerHash                | 識別要依據一般容器 URL 刪除之附件的雜湊碼                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | 檔案格式或 MIMETYPE (例如，適用于 .EML 檔案的 ' message/rfc822 ')                                               | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | 索引子上次將檔編目至目錄更新的時間                                                           | 0b63e350-9ccc-11d0-bcdb-00805fccce04/4                            |
| 市集                        | 存放區或通訊協定處理常式 (FILE、MAIL、OUTLOOKEXPRESS)                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| FileExt                      | 副檔名                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | 檔案的名稱                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | 簡短 (8.3) 檔案的檔案名                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | 訊息中的附件名稱                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | [密件副本：] 欄位中的位址                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | [密件副本：] 欄位中的人員名稱                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Cc：欄位中的位址                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Cc：欄位中的人員名稱                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | 電子郵件執行緒中交談的唯一識別碼                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | [來源：] 欄位中的位址                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | [寄件者：] 欄位中的人員名稱                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | 指出郵件已回復或轉寄 (cdoPR \_ ACTION = 261 262)                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | 指出 mail 的附件 (T 或 F)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| 接收                 | 傳遞時間                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/接收                 |
| ToAddress                    | 位址在 [到] 中：欄位                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | [收件者：] 欄位中的人員名稱                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | 工作的狀態                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | 會議/事件的結束時間 (通常)                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/結束日期                      |
| IsRecurring                  | 指出專案是週期性的 (例如會議)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | 會議/事件的開始時間 (通常)                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/開始日期                    |
| 持續時間                     | 會議的長度（以分鐘為單位）                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/持續時間                     |
| Location                     | 發生專案 (例如會議) 的位置                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/位置                     |
| 周年                  | 週年日                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/周年                  |
| AssistantName                | 助理名稱                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | 助理電話                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | 連絡人的生日                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/生日                     |
| BusinessAddressCity          | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressStreet        | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressStreet        |
| BusinessAddressCountry       | 公司位址資訊                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | 回撥電話資訊                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | 連絡人的子女名稱                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/子系                     |
| CompanyMainTelephone         | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | 連絡人電子郵件名稱                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | 電子郵件地址的顯示名稱                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| 名字                    | 連絡人的名字                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | 連絡人的完整名稱                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| 性別                       | 男性/女性/其他                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/性別                       |
| 愛好                        | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/愛好                        |
| HomeAddressCity              | 首頁位址資訊                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | 首頁位址資訊                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | 首頁位址資訊                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | 首頁位址資訊                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | 首頁位址資訊                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressStreet            |
| HomeFaxNumber                | 傳真資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | 傳真資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| IMAddress                    | 立即訊息資訊                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | 連絡人的職稱                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/昵稱                     |
| Office                       | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/辦公室                       |
| OfficeTelephone              | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| 姓氏                     | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                |  (Dr. 的職業職稱，Mrs，Ms. )                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | 電話資訊                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/專業                   |
| 配偶                       | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/配偶                       |
| 後置詞                       | 連絡資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/尾碼                       |
| TelexNumber                  | 電傳資訊                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | TTY/TDD 資訊                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | 連絡人網頁                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/網頁                      |
| DocCompany                   | 公司                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | 檔 wa 上次儲存的使用者                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | 前次列印時間                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | 投影片                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | 音訊檔案的平均資料速率（Kbps）                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | 音訊檔案的長度（以毫秒為單位）                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | 專輯名稱                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | 演出者的名稱                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | 專輯的類型                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | 專輯中的曲目數                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | 記錄專輯的年份                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | 攝影機的製造商                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | 攝影機模型                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | 所採用的資料 FILETIME                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientation                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | 影像的維度                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | 影像的 X 解析度                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | 影像的 Y 解析度                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | 影片串流的框架高度                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | 影片串流每毫秒的畫面播放速率（以毫秒為單位）                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | 影片資料流程的框架寬度                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| 類別                        | 類別名稱                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/類別                        |
| 函式                     | 函式名稱                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/func                         |
| 結構                       | 結構名稱                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/結構                       |
| 介面                    | 介面名稱                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/介面                    |
| 代理人                     | 委派名稱                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/委派                     |
| 屬性                     | 屬性名稱                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/屬性                     |
| 列舉                         | 列舉名稱                                                                                                               | 8dee0300-16c2-101b-b121-08002b2ecda9/enum                         |
| 常數                        | Const 名稱                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/const                        |
| 事件                        | 事件名稱                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/事件                        |
| 欄位                        | 欄位名稱                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/欄位                        |
| 定義                       | 定義名稱                                                                                                             | 8dee0300-16c2-101b-b121-08002b2ecda9/def                          |
| 元件                    | 元件名稱                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/元件                    |
| Project                      | 專案名稱                                                                                                            | 8dee0300-16c2-101b-b121-08002b2ecda9/專案                      |
| 解決方法                     | 方案名稱                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/解決方案                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[開發通訊協定處理常式](-search-2x-wds-phaddins.md)
</dt> <dt>

[進階查詢語法](-search-2x-wds-aqsreference.md)
</dt> <dt>

[認知類型](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 





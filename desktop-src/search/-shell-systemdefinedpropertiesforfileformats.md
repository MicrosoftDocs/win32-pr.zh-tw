---
description: Microsoft Windows 提供一些可供您的檔案格式使用的系統屬性。
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: 自訂檔案格式的 System-Defined 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112401"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>自訂檔案格式的 System-Defined 屬性

Microsoft Windows 提供一些可供您的檔案格式使用的系統屬性。 如果您要建立自訂檔案格式，您應該盡可能支援最多的系統定義屬性。 建立自訂屬性處理常式之前，您應該先檢查系統提供的處理常式，看看您是否可以使用它，而不是撰寫自己的處理常式。

下表將檔案格式分類，然後列出檔案格式應支援的最重要系統屬性。 為了提供絕佳的使用者體驗，您應該針對檔案格式的類別目錄支援所有優先順序1和2屬性。

-   [通訊](#communications)
-   [連絡人](#contacts)
-   [文件](#documents)
-   [泛型](#generic)
-   [音樂](#music)
-   [圖片](#pictures)
-   [影片](#videos)
-   [相關主題](#related-topics)

## <a name="communications"></a>通訊



| Name            | 屬性                               | 優先順序 |
|-----------------|----------------------------------------|----------|
| 收到日期   | DateReceived            | 1        |
| 從名稱      | FromName                | 1        |
| 具有附件 | HasAttachments          | 1        |
| Mailbox         | Storeddisplayname | 1        |
| Name            | System.string                        | 1        |
| 主體         | System. Subject                         | 1        |
| 名稱        | ToName                  | 1        |
| 類別        | System. Category                        | 2        |
| 類型            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>連絡人



| Name             | 屬性                           | 優先順序 |
|------------------|------------------------------------|----------|
| 帳戶名稱     | System.servicemodel   | 1        |
| 公司電話   | BusinessTelephone   | 1        |
| 公司          | Company                     | 1        |
| 電子郵件地址    | PrimaryEmailAddress | 1        |
| 重要性       | System. ImportanceText              | 1        |
| 行動電話     | MobileTelephone     | 1        |
| 商務位址 | BusinessAddress     | 2        |
| 企業傳真     | BusinessFaxNumber   | 2        |
| 類別         | System. Category                    | 2        |
| 首頁位址     | HomeAddress         | 2        |
| 住家電話       | HomeTelephone       | 2        |
| 標題            | System.Title                       | 2        |



 

## <a name="documents"></a>文件



| Name      | 屬性             | 優先順序 |
|-----------|----------------------|----------|
| Authors   | System.Author        | 1        |
| 全文檢索 | System. 全文檢索      | 1        |
| 標籤      | System.Keywords      | 1        |
| 類型      | System.PerceivedType | 1        |
| 類別  | System. Category      | 2        |
| 標題     | System.Title         | 2        |



 

## <a name="generic"></a>泛型



| Name     | 屬性             | 優先順序 |
|----------|----------------------|----------|
| Authors  | System.Author        | 1        |
| 標題    | System.Title         | 1        |
| 類型     | System.PerceivedType | 1        |
| 類別 | System. Category      | 2        |
| 標籤     | System.Keywords      | 2        |



 

## <a name="music"></a>音樂



| Name         | 屬性                     | 優先順序 |
|--------------|------------------------------|----------|
| \#           | TrackNumber     | 1        |
| 專輯        | AlbumTitle      | 1        |
| 演出者      | 系統音樂          | 1        |
| Genre        | System.object           | 1        |
| 分級       | 系統評分                | 1        |
| 標題        | System.Title                 | 1        |
| 專輯演出者 | AlbumArtist     | 2        |
| 位元速度     | EncodingBitrate | 2        |
| 導體   | System.servicemodel       | 2        |
| 長度       | System.object。持續時間        | 2        |
| Protected    | IsProtected       | 2        |
| Year         | Year            | 2        |



 

## <a name="pictures"></a>圖片



| Name          | 屬性                        | 優先順序 |
|---------------|---------------------------------|----------|
| 匯入日期 | System. DateImported             | 1        |
| 拍攝日期    | DateTaken          | 1        |
| 分級        | 系統評分                   | 1        |
| 標籤          | System.Keywords                 | 1        |
| 類型          | System.PerceivedType            | 1        |
| Authors       | System.Author                   | 2        |
| 攝影機 maker  | CameraManufacturer | 2        |
| 攝影機模型  | CameraModel        | 2        |
| 註解      | System. Comment                  | 2        |
| 維度    | 系統維度         | 2        |



 

## <a name="videos"></a>影片



| Name         | 屬性                 | 優先順序 |
|--------------|--------------------------|----------|
| 長度       | System.object。持續時間    | 1        |
| 分級       | 系統評分            | 1        |
| 標籤         | System.Keywords          | 1        |
| 類型         | System.PerceivedType     | 1        |
| 框架高度 | FrameHeight | 2        |
| 框架寬度  | FrameWidth  | 2        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[屬性系統](../properties/building-property-handlers.md)
</dt> <dt>

[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 

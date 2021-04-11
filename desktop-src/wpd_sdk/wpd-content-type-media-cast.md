---
description: WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116085"
---
# <a name="wpd_content_type_media_cast"></a>WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換

描述其類型作為 WPD \_ 內容 \_ 類型媒體轉換的物件， \_ \_ 代表相關內容的集合。

Mediacast 物件可以視為將相關內容分組的容器物件，就像播放清單群組音樂一樣。 通常，Mediacast 物件是用來將線上發佈的媒體內容分組。 例如，RSS 通道可以表示為 Mediacast 物件，其物件參考指向代表通道中每個專案的內容物件。

這種類型的物件支援下列屬性。



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **屬性名稱**                                                                                                     | **必要或選擇性**                                              |
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
| [WPD \_ 物件 \_ 語言 \_ 地區設定](object-properties.md)                                                                | 如果無法刪除物件，則為必要。                             |
| [WPD \_ 媒體 \_ 著作權](media-properties.md)                                                     | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 家長 \_ 評等](media-properties.md)                                        | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 中繼 \_ 類型](media-properties.md)                                                  | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 子 \_ 標題](media-properties.md)                                                    | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)                                              | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 標題](media-properties.md)                                                             | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 擁有者](media-properties.md)                                                             | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 管理 \_ 編輯器](media-properties.md)                                        | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 管理員](media-properties.md)                                                     | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                                                  | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)                                        | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                                                 | 選擇性。                                                             |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                                             | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 物件 \_ 書簽](media-properties.md)                                        | 建議                                                           |
| [WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期](media-properties.md)                                       | 建議使用。                                                          |
| [WPD \_ 媒體 \_ 生存 \_ 時間 \_](media-properties.md)                                             | 選擇性。                                                             |
| [WPD \_ 媒體 \_ 子 \_ 描述](object-properties.md)                                                                 | 選擇性。                                                             |



 

## <a name="typical-resources"></a>一般資源

這些物件通常包含下列資源。



| 資源名稱                                               | 必要或選擇性 | Description                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)      | 選擇性。            | 包含 mediacast 檔案資料。 例如，如果此 mediacast 代表 RSS 通道，這可能是 RSS 檔。 |
| [**WPD \_ 資源 \_ 縮圖**](wpd-resource-thumbnail.md)  | 選擇性。            | 包含表示此 mediacast 的縮圖。                                                                         |
| [**WPD \_ 資源 \_ 專輯 \_ 封面**](wpd-resource-album-art.md) | 選擇性。            | 包含此 mediacast 的作品。                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>RSS 元素與 Mediacast 屬性的對應

RSS 通道可以表示為 Mediacast 物件，其參考指向代表特定通道中每個專案的內容物件。

RSS 饋送中的元素具有下列階層和屬性。


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



下表列出 RSS 摘要中的通道元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| **Channel 元素** | **RSS 饋送需求** | **對應的 Mediacast 屬性**                                            |
| category            | 選擇性。                | [WPD \_ 媒體內容類型 \_](media-properties.md)                       |
| cloud               | 不適用。          | 不適用。                                                                 |
| 著作權           | 選擇性。                | [WPD \_ 媒體 \_ 著作權](media-properties.md)               |
| description         | 必要。                | [WPD \_ 媒體 \_ 描述](media-properties.md)           |
| docs                | 不適用。          | 不適用。                                                                 |
| 產生器           | 不適用。          | 不適用。                                                                 |
| 語言            | 不適用。          | 不適用。                                                                 |
| lastBuildDate       | 選擇性。                | [WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期](media-properties.md) |
| link                | 必要。                | [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)  |
| managingEditor      | 選擇性。                | [WPD \_ 媒體 \_ 管理 \_ 編輯器](media-properties.md)  |
| pubDate             | 選擇性。                | [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)        |
| rating              | 不適用。          | 不適用。                                                                 |
| skipDays            | 不適用。          | 不適用。                                                                 |
| skipHours           | 不適用。          | 不適用。                                                                 |
| >textinput           | 不適用。          | 不適用。                                                                 |
| title               | 必要。                | [WPD \_ 物件 \_ 名稱](object-properties.md)                      |
| ttl                 | 選擇性。                | [WPD \_ 媒體 \_ 生存 \_ 時間 \_](media-properties.md)       |
| 站長           | 選擇性。                | [WPD \_ 媒體 \_ 管理員](media-properties.md)               |



 

下表列出 RSS 摘要中的影像元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| **Image 元素** | **RSS 饋送需求** | **Mediacast 屬性**                                                         |
| description       | 選擇性。                | [WPD \_ 媒體 \_ 描述](media-properties.md)          |
| 身高            | 選擇性。                | [WPD \_ 媒體 \_ 高度](media-properties.md)                    |
| link              | 選擇性。                | [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md) |
| title             | 選擇性。                | [WPD \_ 物件 \_ 名稱](object-properties.md)                     |
| url               | 選擇性。                | [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)           |
| width             | 選擇性。                | [WPD \_ 媒體 \_ 寬度](media-properties.md)                      |



 

下表列出 RSS 摘要中的專案元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| **Item 元素** | **Attribute** | **RSS 饋送需求** | **Mediacast 屬性**                                                         |
| 編寫           |               | 選擇性。                | [WPD \_ MEDIA \_ 演出者](media-properties.md)                    |
| category         |               | 選擇性。                | [WPD \_ 媒體內容類型 \_](media-properties.md)                      |
|                  | 網域        | 不適用。          | 不適用。                                                                |
| description      |               | 選擇性。                | [WPD \_ 媒體 \_ 描述](media-properties.md)          |
| 外殼        |               | 選擇性。                |                                                                                |
|                  | url           | 必要。                | [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)           |
|                  | 長度        | 必要。                | [WPD \_ 物件 \_ 大小](object-properties.md)                     |
|                  | 類型          | 必要。                |  (MIME 類型應對應至屬性內容類型。 )                  |
| guid             |               | 選擇性。                | [WPD \_ 媒體 \_ GUID](media-properties.md)                        |
|                  | isPermaLink   | 不適用。          | 不適用。                                                                |
| link             |               | 選擇性。                | [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md) |
| pubDate          |               | 選擇性。                | [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)       |
| source           |               | 不適用。          | 不適用。                                                                |
| title            |               | 選擇性。                | [WPD \_ 物件 \_ 名稱](object-properties.md)                     |



 

下列範例顯示發行公司的 CEO 所提供之虛構播客的完整 RSS 摘要。


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>將 RSS 通道元素對應至 WPD 屬性值

下表說明上一個範例中 RSS 通道元素的值如何對應至特定的 WPD 屬性。



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **WPD 屬性**                                                                             | **值**                                                                                     |
| [WPD \_ 媒體 \_ 著作權](media-properties.md)                            | 2006 Lucerne 發行 LP，LLLP。 著作權所有，並保留一切權利。                                        |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                        | Lucerne 發佈 CEO Peter Bankov 會查看線上發行物的最新趨勢。 |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                    | 新聞                                                                                          |
| [WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期](media-properties.md)              | 2006年6月9日，14:00:28 EDT                                                                 |
| [WPD \_ 媒體 \_ 管理 \_ 編輯器](media-properties.md)               | someone@example.com                                                                           |
| [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)                     | 2006年6月9日，14:00:28 EDT                                                                 |
| [WPD \_ 媒體 \_ 生存 \_ 時間 \_](media-properties.md)                    | 240                                                                                           |
| [WPD \_ 媒體 \_ 標題](media-properties.md)                                    | 數位發行                                                                       |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WPD \_ 媒體 \_ 管理員](media-properties.md)                            | someone@example.com                                                                           |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                  | WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換                                                               |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                | 2006年6月9日，14:00:28 EDT                                                                 |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                  | 2006年6月9日，14:00:28 EDT                                                                 |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                | 2006年6月9日，14:00:28 EDT                                                                 |
| [WPD \_ 物件 \_ 格式](object-properties.md)                               | WPD \_ 物件 \_ 格式 \_ 抽象 \_ 媒體 \_ 轉換                                                    |
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                       | 會話相依值。                                                                      |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                   | 數位發行                                                                       |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)     | 數位發行                                                                       |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                        | MyPodcasts (裝置上的虛構播客資料夾) 。 針對此範例，請採用 "0A0"。        |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md) | 會話獨立值。  (在此範例中採用 "0A1"。 )                                    |
| [WPD \_ 物件 \_ 參考](object-properties.md)                       | N 個專案的0A2<br/>                                                                   |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                   | 13790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>將 RSS 影像元素對應至 WPD 屬性值

下表說明上一個範例中 RSS 影像元素的值如何對應至特定的 WPD 屬性。



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **WPD 屬性**                                                                                                        | **值**                                           |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                                                   | Lucerne 標誌                                        |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [WPD \_ 媒體 \_ 高度](media-properties.md)                                                             | 300                                                 |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [WPD \_ 媒體 \_ 寬度](media-properties.md)                                                               | 300                                                 |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                                              | Lucerne 發行                                  |
| [WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除](attributes.md)                               | VARIANT \_ TRUE                                       |
| [WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [WPD \_ 資源 \_ 屬性 \_ 格式](resource-attribute-properties.md)                     | WPD \_ 物件 \_ 格式 \_ GIF                            |
| [WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小](attributes.md) | 1024                                                |
| [WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>將 RSS 專案元素對應至 WPD 屬性值

下表說明上一個範例中 RSS 專案專案的值如何對應至特定的 WPD 屬性。



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **WPD 屬性**<br/>                                                                  | **值**                                                                                                                        |
| [WPD \_ 媒體 \_ 標題](media-properties.md)                                    | 數位發行                                                                                                          |
| [WPD \_ 媒體 \_ 持續時間](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ MEDIA \_ 演出者](media-properties.md)                                  | 苜蓿                                                                                                                          |
| [WPD \_ 媒體 \_ 描述](media-properties.md)                        | 線上發行集很快就會改變。 發行公司的 CEO 會檢查過去5年的趨勢及其含意。 |
| [WPD \_ 媒體 \_ 目的地 \_ URL](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD \_ 媒體內容類型 \_](media-properties.md)                                    | 新聞                                                                                                                             |
| [WPD \_ 媒體 \_ GUID](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD \_ 媒體 \_ 發行 \_ 日期](media-properties.md)                     | 週四，2006年6月1日 14:00:28 EDT                                                                                                   |
| [WPD \_ 媒體 \_ 來源 \_ URL](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD \_ 物件 \_ 反向 \_ 參考](object-properties.md)            | 0A1                                                                                                                              |
| [WPD \_ 物件 \_ 內容 \_ 類型](object-properties.md)                  | WPD \_ 內容 \_ 類型 \_ 媒體 \_ 影像                                                                                                 |
| [撰寫的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                | 週四，2006年6月1日 14:00:28 EDT                                                                                                   |
| [已 \_ 建立 WPD 物件 \_ 日期 \_](object-properties.md)                  | 週四，2006年6月1日 14:00:28 EDT                                                                                                   |
| [修改的 WPD \_ 物件 \_ 日期 \_](object-properties.md)                | 週四，2006年6月1日 14:00:28 EDT                                                                                                   |
| [WPD \_ 物件 \_ 格式](object-properties.md)                               | WPD \_ 物件 \_ 格式 \_ MP3                                                                                                         |
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                       | 會話相依。  (在此範例中採用 "0A2"。 )                                                                               |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                   | 數位發行                                                                                                          |
| [WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                        | 0A0                                                                                                                              |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md) | 與會話無關。                                                                                                             |
| [WPD \_ 物件 \_ 大小](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 





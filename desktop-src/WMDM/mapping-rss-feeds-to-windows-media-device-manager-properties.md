---
title: 將 RSS 摘要對應至 Windows Media 裝置管理員屬性
description: 將 RSS 摘要對應至 Windows Media 裝置管理員屬性
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media 裝置管理員，RSS 摘要
- 裝置管理員，RSS 摘要
- 程式設計指南，RSS 摘要
- 桌面應用程式，RSS 摘要
- 建立 Windows Media 裝置管理員應用程式、RSS 摘要
- RSS 摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839456"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>將 RSS 摘要對應至 Windows Media 裝置管理員屬性

Windows Media Player 11 提供 RSS 匯總程式功能，可讓使用者在他們的電腦上儲存從播客取得的內容。 本主題說明在 RSS 摘要中找到的 XML 元素。 此外，它還會將這些 RSS 元素對應至 Windows Media 裝置管理員屬性。

RSS 饋送中的元素具有下列階層和屬性：


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



下表列出 RSS 摘要中的通道元素，以及對應的 Windows Media 裝置管理員屬性。



| Channel 元素 | 狀態         | 對應的 Windows Media 裝置管理員屬性   |
|-----------------|----------------|-------------------------------------------------------|
| category        | 選擇性       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| cloud           | 不適用 | 不適用                                        |
| 著作權       | 選擇性       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| description     | 必要       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| docs            | 不適用 | 不適用                                        |
| 產生器       | 不適用 | 不適用                                        |
| 語言        | 不適用 | 不適用                                        |
| lastBuildDate   | 選擇性       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | 必要       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | 選擇性       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | 選擇性       | [g \_ wszWMDMYear](metadata-constants.md)              |
| rating          | 不適用 | 不適用                                        |
| skipDays        | 不適用 | 不適用                                        |
| skipHours       | 不適用 | 不適用                                        |
| >textinput       | 不適用 | 不適用                                        |
| title           | 必要       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | 選擇性       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| 站長       | 選擇性       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

下表列出 RSS 摘要中的影像元素和對應的 WMDM 屬性。



| Image 項目 | 狀態   | 對應的 Windows Media 裝置管理員屬性 |
|---------------|----------|-----------------------------------------------------|
| description   | 選擇性 | [g \_ wszWMDMDescription](metadata-constants.md)     |
| 身高        | 選擇性 | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | 選擇性 | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | 選擇性 | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | 選擇性 | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | 選擇性 | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

下表列出 RSS 摘要中的專案元素，以及對應的 Windows Media 裝置管理員屬性。



| Item 項目 | 屬性   | 狀態         | 對應的 Windows Media 裝置管理員屬性            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| 編寫       |             | 選擇性       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | 選擇性       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | 網域      | 不適用 | 不適用                                                 |
| description  |             | 選擇性       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| 外殼    |             | 選擇性       | 不適用                                                 |
|              | 長度      | 必要       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | 必要       |  (MIME 類型應對應至屬性內容類型。 )  |
|              | url         | 必要       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | 選擇性       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | 不適用 | 不適用                                                 |
| link         |             | 選擇性       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | 選擇性       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | 不適用 | 不適用                                                 |
| title        |             | 選擇性       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

範例

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
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
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



RSS 通道元素與 Windows Media 裝置管理員屬性值的對應

下表說明上一個範例中 RSS 通道元素的值如何對應至特定的 Windows Media 裝置管理員屬性。



| Windows Media 裝置管理員屬性                    | 值                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | 2006年6月9日，14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | Lucerne 發佈 CEO Peter Bankov 會查看線上發行物的最新趨勢。 |
| [g \_ wszWMDMDESTINATION \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | 2006年6月9日，14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | 數位發行                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | WMDM \_ FORMATCODE \_ 媒體 \_ 轉換                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | 新聞                                                                                          |
| [g \_ wszWMDMLAST \_ 修改 \_ 日期](metadata-constants.md) | 2006年6月9日，14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | 2006年6月9日，14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne 發行 LP，LLLP。 著作權所有，並保留一切權利。                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | 數位發行                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | 2006年6月9日，14:00:28 EDT                                                                 |



 

將 RSS 影像元素對應至 Windows Media 裝置管理員屬性值

下表說明上一個範例中 RSS 影像元素的值如何對應至特定的 Windows Media 裝置管理員屬性。



| Windows Media 裝置管理員屬性                | 值                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | WPD \_ 物件 \_ 格式 \_ GIF                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Lucerne 標誌                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Lucerne 發行                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

將 RSS 專案元素對應至 Windows Media 裝置管理員屬性值

下表說明上一個範例中 RSS 專案專案的值如何對應至特定的 Windows Media 裝置管理員屬性。



| Windows Media 裝置管理員屬性                | 值                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | 苜蓿                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | 週四，2006年6月1日 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | 線上發行集很快就會改變。 發行公司的 CEO 會檢查過去五年的趨勢及其含意。 |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | 週四，2006年6月1日 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | WMDM \_ FORMATCODE \_ MP3                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | 新聞                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | 週四，2006年6月1日 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | 數位發行                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | 週四，2006年6月1日 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼資料常數**](metadata-constants.md)
</dt> </dl>

 

 





---
description: 說明如何讓 OpenSearch web 服務存取您的資料存放區，以及如何避免可能的阻礙。
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: 在 Windows 同盟搜尋中啟用資料存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456751"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>在 Windows 同盟搜尋中啟用資料存放區

說明如何讓[OpenSearch](https://github.com/dewitt/opensearch) web 服務存取您的資料存放區，以及如何避免可能的阻礙。

本主題的組織方式如下：

-   [接受搜尋要求的條件](#conditions-for-search-request-acceptance)
    -   [支援的查詢語法](#supported-query-syntax)
    -   [支援的驗證通訊協定](#supported-authentication-protocols)
-   [在 RSS 或 Atom 中傳送查詢並傳回搜尋結果](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [RSS 摘要輸出的範例](#example-of-an-rss-feed-output)
-   [自動對應至 Windows Shell 屬性](#automatic-mapping-to-windows-shell-properties)
-   [瞭解如何對檔案類型 Windows 地圖專案](#understanding-how-windows-maps-items-to-file-types)
-   [避免啟用資料存放區的潛在阻礙](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>接受搜尋要求的條件

您在 web 伺服器上建立的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務 **必須** 滿足下列兩項需求：

-   能夠接受 `GET URL` 來自用戶端的查詢。
-   允許在 URL 中內嵌搜尋字詞。

    下列範例顯示如何將搜尋字詞內嵌在 URL 中。

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> 聯合搜尋不支援 `POST` 將要求傳送至 web 服務。

 

如需有關如何建立 URL 的詳細資訊，請參閱[Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「URL 範本參數」。

### <a name="supported-query-syntax"></a>支援的查詢語法

Windows 7 中不需要特定的查詢語法。 OpenSearch 提供者接受使用者在 Windows 檔案總管的輸入方塊中輸入的任何詞彙，然後將其編碼成 URL。 它會根據在[Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「url 範本參數」中所述的 url 範本來執行此動作。

使用者預期會將不同的詞彙視為隱含以 and 連結在一起。 例如，「Microsoft Windows」的查詢應該只傳回包含「Windows」和「microsoft」的結果。

### <a name="supported-authentication-protocols"></a>支援的驗證通訊協定

Windows同盟搜尋支援以 Windows 為基礎的驗證，並可透過下列通訊協定提供認證給 web 服務：

-   NTLM。
-   Kerberos。
-   基本 (僅透過 HTTPs) 。
-   其他安全性支援提供者 (ssp) 安裝在提供額外查詢容量的 Windows 上。 請參閱 [SSP 介面](../secauthn/sspi.md) SDK 檔，以隨時掌握其他 ssp 的可能加法。

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>在 RSS 或 Atom 中傳送查詢並傳回搜尋結果

[OpenSearch](https://github.com/dewitt/opensearch)提供者負責將 XML 專案值對應至可供 Windows 應用程式使用 Windows Shell 系統屬性。 但是，您不限於標準 RSS 或 Atom 專案的預設對應，而且可以在每個屬性的 Windows 命名空間中包含自訂 XML 元素。 例如，您可以在 item 元素內加入自己的自訂 XML **專案**，以提供 Windows 的額外中繼資料。 您也可以從其他 XML 命名空間（例如 iTunes）對應元素。

### <a name="example-of-an-rss-feed-output"></a>RSS 摘要輸出的範例

下列 RSS 摘要輸出範例會傳回一個專案。


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



如需有關屬性對應的詳細資訊，請參閱在[Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「WIndows 同盟搜尋中的擴充元素」和「自訂屬性對應」章節。

## <a name="automatic-mapping-to-windows-shell-properties"></a>自動對應至 Windows Shell 屬性

在 rss 摘要的專案內，您可以選擇包含自動對應至 Windows Shell 系統屬性的其他 XML 元素。 若要這樣做，請在 Windows Shell 屬性後面加上名為的元素，並在前面加上 Windows Shell 系統命名空間。 下列範例說明命名空間宣告 `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` ，以及包含屬性對應的元素 `win:System.Contact.PrimaryEmailAddress` ：


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



此處使用的命名空間前置詞 (`"win"`) 是建議的作法; 您可以使用任何前置詞。 不過，您必須使用確切的 Windows Shell 屬性名稱，且必須包含 (URI) 的確切統一資源識別項，如下列範例所示：


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**關於 Windows Shell 系統屬性**

Windows 定義[系統屬性](../properties/props.md)的完整清單，以及每個屬性所需的實數值型別格式。 例如，[ [FileExtension](../properties/props-system-fileextension.md) ] 視窗 Shell 屬性的檔指定值必須包含前置的點 ( ".docx"，而不是 ".docx" ) 。

**日期和時間值**

慣用的日期和時間格式為 ISO-8601，如下列範例所示：


```
2008-01-16T 19:20:30:.45+01:00
```



.NET 開發人員應該使用 DateTime 類別搭配 `ToString("R") ` 來輸出正確的格式。

如需屬性對應的詳細資訊，請參閱在[Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案中的「Windows 同盟搜尋中的擴充元素」。

## <a name="understanding-how-windows-maps-items-to-file-types"></a>瞭解如何對檔案類型 Windows 地圖專案

在 Windows 檔案總管 UI 內搜尋，可讓使用者在 RSS 專案指向遠端儲存的檔案時，將結果視為檔案。 使用者可以拖放專案至桌面，Windows 檔案總管 UI 會顯示正確的圖示，並提供適當的快捷方式功能表。 如果 RSS 專案未指向遠端儲存的檔案，則會將該檔案視為連結，而使用者可以在其上執行動作，例如建立快捷方式或在瀏覽器中開啟它。

下列流程圖顯示 Windows 如何判斷專案的檔案類型。

![流程圖：顯示從專案到決策的路徑，以將其視為 web 連結類型專案或檔案類型](images/determineanitemfiletype.png)

[OpenSearch](https://github.com/dewitt/opensearch)提供者會執行下列步驟，將專案對應至檔案類型：

-   識別是否應將專案視為檔案或網頁連結。
-   識別要使用的正確副檔名。

例如，如果專案有使用檔案系統路徑的連結 URL (例如 `file:///\\server\share\etc\item.ext`) ，則[OpenSearch](https://github.com/dewitt/opensearch)提供者會將連結視為檔案，並依此範例) 中的路徑 ( 中使用的副檔名來決定類型。

如果專案使用標準 RSS 主機殼或 **MediaRSS media： content** 元素， [OpenSearch](https://github.com/dewitt/opensearch)提供者會假設該專案為檔案，並識別副檔名，如下所示：

-   如果已為專案對應[FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性，則提供者會使用該副檔名。
-   如果 [FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性尚未對應，則提供者會使用主機殼或 content 元素中指定的 **類型** 屬性。 這個元素應該包含 `MIMEType` 字串，例如 `"image/jpeg"` 。 如果與在 `MIMEType` 用戶端電腦上註冊的副檔名相關聯，該專案就會被視為該類型的檔案。 如果未 `MIMEType` 與用戶端電腦上註冊的副檔名建立關聯，則會將該專案視為 web 連結類型。 [OpenSearch](https://github.com/dewitt/opensearch)提供者不會嘗試剖析 **Url** 屬性來尋找副檔名。
-   如果與在 `MIMEType` 用戶端電腦上註冊的副檔名相關聯，則提供者會判斷副檔名是否為已知的 web 檔案類型 (.htm、.html、.asp、.aspx、php、swf、.stm) 。 如果是，則會將檔案類型視為 web 連結類型;否則，它會被視為一種檔案類型。 例如，如果 `MIMEType "text/html"` 與 .htm 的副檔名相關聯，該專案就會被視為 web 連結，而不是 .htm 檔案類型。

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>避免啟用資料存放區的潛在阻礙

某些資料存放區不會提供[OpenSearch](https://github.com/dewitt/opensearch)相容的 web 服務，但仍可連線至 Windows 同盟搜尋。 這類資料存放區包括：

-   Windows 7 同盟搜尋中不支援的驗證方法的遠端索引。

    範例包括表單架構驗證和其他自訂驗證方法。

-   如果高價值的公用存放區具有公用 web api，則任何人都可以撰寫[OpenSearch](https://github.com/dewitt/opensearch)相容的另一個 web 服務，並在幕後呼叫這些 api。

    範例包括國會和醫療研究資料庫的程式庫。

-   專屬的企業資料存放區或索引，以及舊版內容管理存放區，可能無法執行前端。

不過，有一些替代方法可避免阻礙啟用資料存放區。 以下是其中一些替代方案：

**當您無法修改現有資料來源的 web 服務，或 web 服務提供自訂 API 時，撰寫中間人 web 服務：**

1.  撰寫可接受 Windows 7 查詢的中間人 web 服務。
2.  連線至您的資料來源，並取出查詢結果。
3.  以 RSS 或 Atom 格式重新格式化結果。
4.  將結果傳回到 Windows 7 用戶端。
5.  請注意，對於 enterprise data services 和許多網際網路資料服務，您可能需要代表 web 服務傳遞使用者認證，以根據使用者的許可權來執行結果修剪。

**當您無法啟用公用資料存放區時，若要使用現有的搜尋引擎：**

1.  使用已支援 RSS [OpenSearch](https://github.com/dewitt/opensearch)的公用搜尋引擎。 若要這麼做，您可以為使用者提供 .osdx 檔案，該檔案的 URL 範本會將結果限制為只有特定網域的結果。
2.  請參閱下列[OpenSearch](https://github.com/dewitt/opensearch)描述的範例，以使用針對 live.com 的查詢來搜尋 Windows 的說明內容。

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

**當您無法啟用專屬的企業資料存放區或索引時，若要使用支援 OpenSearch 的現有索引伺服器：**

1.  選取現有的索引伺服器，以支援[OpenSearch](https://github.com/dewitt/opensearch)來為您的內容編制索引，例如 SharePoint 搜尋伺服器。
2.  使用 URL 範本內的關鍵字語法，建立 .osdx 檔案，將 SharePoint 索引的結果限制為只有來自您伺服器的結果。

**如果伺服器端專用解決方案無法運作，則撰寫用戶端資料存放區：**

1.  撰寫位於 Windows [OpenSearch](https://github.com/dewitt/opensearch)提供者和外部資料源之間的用戶端[OpenSearch](https://github.com/dewitt/opensearch)資料來源。
2.  使用 Windows SDK 中的[IOpenSearchSource 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource)API 來建立適當設定的 searchconnector-ms 檔案，讓 Windows 檔案總管可以使用查詢參數來呼叫您的實作為。 然後，您的實作為會傳回以 RSS 或 Atom 格式格式化的結果。 這麼做可讓您的執行程式提供自訂驗證 UI，並使用其專屬的 API 連接到資料來源。

> [!Note]  
> 開啟 .osdx 檔案會在% userprofile%/searches 目錄中建立 searchconnector-ms 檔案 (搜尋) 連接器，並在% userprofile%/links 目錄中放置該檔案的連結。

 

## <a name="additional-resources"></a>其他資源

如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱[Windows 中同盟搜尋](/previous-versions//dd742958(v=vs.85))的「其他資源」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[在 Windows 中使用同盟搜尋開始使用](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)
</dt> <dt>

[在 Windows 同盟搜尋中建立 OpenSearch 的描述檔案](-search-federated-search-osdx-file.md)
</dt> <dt>

[遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)
</dt> <dt>

[在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)
</dt> </dl>

 

 

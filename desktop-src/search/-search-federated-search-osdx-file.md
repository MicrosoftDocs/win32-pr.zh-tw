---
description: 說明如何建立 OpenSearch 描述 (. .osdx) 檔，以透過 OpenSearch 通訊協定將外部資料存放區連接到 Windows 用戶端。
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: 在 Windows 同盟搜尋中建立 OpenSearch 的描述檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f58b29a860c7d53583b7fd17ddd942bb21b08d649ea7e54d5b2278be2f8d4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456859"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>在 Windows 同盟搜尋中建立 OpenSearch 的描述檔案

說明如何建立 OpenSearch 描述 (. .osdx) 檔，以透過[OpenSearch](https://github.com/dewitt/opensearch)通訊協定將外部資料存放區連接到 Windows 用戶端。 同盟搜尋可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。

本主題包含下列幾節：

-   [OpenSearch描述檔](#opensearch-description-file)
    -   [必要的必要子項目](#mininum-required-child-elements)
-   [Windows 同盟搜尋中的標準元素](#standard-elements-in-windows-federated-search)
    -   [Shortname](#shortname)
    -   [說明](#description)
    -   [RSS/Atom 結果的 URL 範本](#url-template-for-rssatom-results)
    -   [Web 結果的 URL 範本](#url-template-for-web-results)
    -   [URL 範本參數](#url-template-parameters)
    -   [分頁的結果](#paged-results)
    -   [使用專案索引進行分頁](#paging-using-the-item-index)
    -   [使用頁面索引進行分頁](#paging-using-the-page-index)
    -   [頁面大小](#page-size)
-   [Windows 同盟搜尋中的擴充元素](#extended-elements-in-windows-federated-search)
    -   [最大結果計數](#maximum-result-count)
    -   [屬性對應](#property-mapping)
-   [預覽](#previews)
-   [開啟檔案位置功能表項目](#open-file-location-menu-item)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch描述檔

Windows 同盟搜尋的 OpenSearch 描述 (. .osdx) 檔必須遵守下列規則：

-   這是有效的 OpenSearch 描述檔（如[OpenSearch](https://github.com/dewitt/opensearch) 1.1 規格所定義）。
-   請提供具有 RSS 或 Atom 格式類型的 URL 範本。
-   從 web 下載時，請使用 .osdx 副檔名，或與 .osdx 副檔名相關聯。 例如，伺服器不需要使用 .osdx。 伺服器可以傳回具有任何副檔名的檔案，例如 .xml，並將其視為 .osdx 檔（如果它使用正確的 MIME 類型來 OpenSearch 描述檔 (. .osdx 檔案) 。
-    (建議的) 提供 **ShortName** 元素值。

### <a name="mininum-required-child-elements"></a>必要的必要子項目

下列 .osdx 檔案是由 **ShortName** 和專案所組成 `Url` ，這些都是必要的最小子項目。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Windows 同盟搜尋中的標準元素

除了最小的子項目之外，同盟搜尋也支援下列標準元素。

### <a name="shortname"></a>Shortname

Windows 使用 **ShortName** 元素值來命名 searchconnector-ms (搜尋連接器) 在使用者開啟 .osdx 檔案時所建立的檔案。 Windows 可確保產生的檔案名只使用 Windows 檔案名中允許的字元。 如果未提供任何 **ShortName** 值，searchconnector-ms 檔案會嘗試改用 .osdx 檔案的檔案名。

下列程式碼說明如何在 .osdx 檔案中使用 **ShortName** 元素。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>描述

當使用者選取 searchconnector-ms 檔案時，Windows 使用 **Description** 元素值來填入 Windows 檔案總管詳細資料窗格中所顯示的檔案描述。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>RSS/Atom 結果的 URL 範本

.Osdx 檔案必須包含一個 **url 格式** 專案和樣板屬性 (url **範本，)** 以 RSS 或 Atom 格式傳回結果。 格式屬性必須 `application/rss+xml` 針對 RSS 格式化的結果設定為，或 `application/atom+xml` 針對 Atom 格式的結果設定為，如下列程式碼所示。

> [!Note]  
> **Url 格式** 元素和 **範本** 屬性通常稱為 url 範本。

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Web 結果的 URL 範本

如果有可在網頁瀏覽器中查看的搜尋結果版本，您應該提供 **Url format =** `text/html` element 和 **template** 屬性，如下列程式碼所示。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



如果您提供 **Url 格式 = "text/html"** 元素和 **範本** 屬性，則按鈕會出現在 Windows 檔案總管命令列中，如下列螢幕擷取畫面所示，可讓使用者在執行查詢時，開啟網頁瀏覽器來查看搜尋結果。

![顯示 [web 搜尋匯總] 按鈕的螢幕擷取畫面。](images/websearchroll-overcommandbarbutton.png)

在某些案例中，查詢回復至資料存放區的 web UI 是很重要的。 例如，使用者可能會想要查看超過100的結果 (OpenSearch 提供者要求) 的預設專案數。 若是如此，使用者可能也會想要使用僅適用于資料存放區網站的搜尋功能，例如使用不同的排序次序重新查詢，或使用相關的中繼資料來切換和篩選查詢。

### <a name="url-template-parameters"></a>URL 範本參數

OpenSearch 提供者一律會執行下列動作：

1.  使用 URL 範本將要求傳送至 web 服務。
2.  將要求傳送至 web 服務之前，嘗試取代 URL 範本中找到的權杖，如下所示：
    -   取代下表所列的標準 OpenSearch 權杖。
    -   移除下表中未列出的任何權杖。



| 支援的權杖  | OpenSearch 提供者的使用方式                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| SearchTerms    | 取代為使用者在 Windows 檔案總管搜尋輸入方塊中輸入的搜尋字詞。<br/>                                         |
| StartIndex     | 在「頁面」中取得結果時使用。<br/> 取代為要傳回的第一個結果專案的索引。<br/>                        |
| StartPage      | 在「頁面」中取得結果時使用。<br/> 取代為要傳回之搜尋結果集的頁碼。<br/>               |
| 字數          | 在「頁面」中取得結果時使用。<br/> 以每頁 Windows 檔案總管要求的搜尋結果數目取代。<br/> |
| 語言       | 取代為字串，表示要傳送之查詢的語言。<br/>                                                          |
| {inputEncoding}  | 以字串取代 (這類「UTF-16」 ) ，表示要傳送之查詢的字元編碼。<br/>                                |
| OutputEncoding | 取代為字串 (例如 "UTF-16" ) ，表示所需的 web 服務回應字元編碼。<br/>       |



 

### <a name="paged-results"></a>分頁的結果

您可能會想要限制每個要求傳回的結果數目。 您可以選擇一次傳回結果的「頁面」，或讓 OpenSearch 提供者依專案編號或頁碼取得額外的結果頁面。 例如，如果您每個頁面傳送二十個結果，則您傳送的第一個頁面會在專案索引1和頁面1開始：您傳送的第二個頁面會從專案索引21開始，在第2頁開始。 您可以使用 `{startItem}` URL 範本中的或標記，定義您希望 OpenSearch 提供者如何要求專案 `{startPage}` 。

### <a name="paging-using-the-item-index"></a>使用專案索引進行分頁

專案索引會識別結果頁面中的第一個結果專案。 如果您想要讓用戶端使用專案索引來傳送要求，您可以使用 `{startIndex}` **Url** 專案 **範本** 屬性中的權杖，如下列程式碼所示。


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



然後[OpenSearch](https://github.com/dewitt/opensearch)提供者會以起始索引值取代 URL 中的權杖。 第一個要求會從第一個專案開始，如下列範例所示：


```
https://example.com/rss.php?query=frogs&start=1
```



OpenSearch 提供者可以藉由變更 `{startIndex}` 參數值併發出新的要求，來取得其他專案。 提供者會重複此程式，直到取得足夠的結果來滿足其限制，或達到結果的結尾。 OpenSearch 提供者會在結果的第一頁中查看 web 服務所傳回的專案數，並將預期的頁面大小設定為該數位。 它會使用該數位來遞增 `{startIndex}` 後續要求的值。 例如，如果 web 服務在第一個要求中傳回20個結果，則提供者會將預期的頁面大小設定為20。 在下一個要求中，提供者會以 `{startIndex}` 值21取代，以取得接下來的20個專案。

> [!Note]  
> 如果 web 服務所傳回的結果頁面所含的專案數少於預期的頁面大小，則 OpenSearch 提供者會假設它已收到最後一頁的結果，並停止發出要求。

 

### <a name="paging-using-the-page-index"></a>使用頁面索引進行分頁

頁面索引會識別指定的結果頁面。 如果您想要讓用戶端使用頁碼傳送要求，您可以使用 `{startPage}` **Url 格式** 專案 **範本** 屬性中的權杖來指出，如下列範例所示：


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



然後 OpenSearch 提供者會使用頁碼參數來取代 URL 中的權杖。 第一個要求會從第一頁開始，如下列範例所示：


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> 如果 web 服務所傳回的結果頁面所含的專案數少於預期的頁面大小，則 OpenSearch 提供者會假設它已收到最後一頁的結果，並停止發出要求。

 

### <a name="page-size"></a>頁面大小

您可能會想要設定 web 服務，以允許要求指定頁面的大小，方法是在 URL 中使用某些參數。 您必須使用權杖，在 .osdx 檔案中指定要求，如下所示 `{count}` ：


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



然後[OpenSearch](https://github.com/dewitt/opensearch)提供者可以設定所需的頁面大小（以每頁的結果數目為單位），如下列範例所示：


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



根據預設，OpenSearch 提供者會使用50的頁面大小來提出要求。 如果您想要不同的頁面大小，則請勿提供 `{count}` 權杖，而是將所需的數位直接放在 **Url 範本** 專案中。

OpenSearch 提供者會根據第一個要求傳回的結果數目來決定頁面大小。 如果所收到結果的第一頁的專案數少於所要求的計數，則提供者會重設任何後續頁面要求的頁面大小。 如果後續頁面要求傳回的專案數少於所要求的數目，OpenSearch 提供者會假設它已達到結果的結尾。

## <a name="extended-elements-in-windows-federated-search"></a>Windows 同盟搜尋中的擴充元素

除了標準元素之外，同盟搜尋也支援下列擴充元素： **MaximumResultCount** 和 **ResultsProcessing**。

由於[OpenSearch](https://github.com/dewitt/opensearch) v1.1 規格中不支援這些擴充的子項目，因此必須使用下列命名空間來新增這些專案：


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>最大結果計數

依預設，搜尋連接器的限制為每個使用者查詢100個結果。 這項限制可以透過將 **MaximumResultCount** 元素包含在 OSD 檔案中進行自訂，如下列範例所示：


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



上述範例會宣告最上層 OpenSearchDescription 專案中的命名空間前置詞 `ms-ose` ，然後在專案名稱中使用該前置詞做為前置詞。 這是必要的宣告，因為 [OpenSearch](https://github.com/dewitt/opensearch) v1.1 規格中不支援 **MaximumResultCount** 。

### <a name="property-mapping"></a>屬性對應

當 web 服務以 RSS 或 Atom 摘要傳回結果時，OpenSearch 提供者必須將摘要中的專案中繼資料對應至 Windows Shell 可以使用的屬性。 下列螢幕擷取畫面說明 OpenSearch 提供者如何對應部分預設 RSS 元素。

![顯示內建 rss 與 windows shell 屬性對應的螢幕擷取畫面](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>預設對應

下表列出 RSS XML 元素 Windows Shell 系統屬性的預設對應。 XML 路徑相對於 item 元素。 `"media:"`前置詞是由[Yahoo Search namespace](https://www.rssboard.org/media-rss)命名空間所定義。



| RSS XML 路徑                  | WindowsShell 屬性 (標準名稱)  |
|-------------------------------|-----------------------------------------|
| 連結                          | System. ItemUrl                          |
| 標題                         | System.servicemodel                         |
| 作者                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| 描述                   | System. AutoSummary                      |
| 類別                      | System.Keywords                         |
| enclosure/@type               | System. MIMEType                         |
| enclosure/@length             | System. Size                             |
| enclosure/@url                | System. >contenturl                       |
| 媒體：類別                | System.Keywords                         |
| media:content/@fileSize       | System. Size                             |
| media:content/@type           | System. MIMEType                         |
| media:content/@url            | System. >contenturl                       |
| media:group/content/@fileSize | System. Size                             |
| media:group/content/@type     | System. MIMEType                         |
| media:group/content/@url      | System. >contenturl                       |
| media:thumbnail/@url          | System. ItemThumbnailUrl                 |



 

> [!Note]  
> 除了標準 RSS 或 Atom 專案的預設對應之外，您還可以在每個屬性的 Windows 命名空間中包含額外的 XML 元素，藉以對應其他 Windows Shell 系統屬性。 您也可以在 .osdx 檔案中新增自訂屬性對應，以從其他現有的 XML 命名空間（例如 MediaRSS、iTunes 等等）對應元素。

 

### <a name="custom-property-mappings"></a>自訂屬性對應

您可以藉由指定 .osdx 檔中的對應，自訂將 RSS 輸出中的專案對應至 Windows Shell 系統屬性。

RSS 輸出會指定：

-   XML 命名空間和
-   若為專案的任何子項目，則為要對應的元素名稱。

.osdx 檔案會識別命名空間中每個元素名稱的 Windows Shell 屬性。 您在 .osdx 檔案中定義的屬性對應會覆寫這些指定屬性的預設對應（如果存在的話）。

下圖說明 RSS 擴充功能如何對應至 Windows 的屬性 (正式名稱) 。

![圖表顯示 xml 命名空間和 xml 路徑的組合會產生正式名稱](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>RSS 結果和 OSD 屬性對應範例

下列範例 RSS 輸出會將 " `https://example.com/schema/2009` example" 前置詞識別為 XML 命名空間。 這個前置詞必須在 **電子郵件** 元素之前再次出現。


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



在下列 .osdx 檔中，XML **電子郵件** 專案對應至 Windows Shell 屬性 [系統. EmailAddress](../properties/props-system-contact-emailaddress.md)。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



有些屬性是無法對應的，因為它們的值可能會在稍後覆寫或無法編輯。 例如，無法對應 [ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) 或 [ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) ，因為它們是從連結或主機殼元素中提供的 URL 值計算而來。

### <a name="thumbnails"></a>縮圖

您可以使用 **media：縮圖 url = ""** 元素，為任何專案提供縮圖影像 url。 理想的解決方式是 150 x 150 圖元。 支援的最大縮圖為 256 x 256 圖元。 提供較大的影像會佔用更多頻寬，讓使用者不會有額外的好處。

### <a name="open-file-location-context-menu"></a>開啟檔案位置內容功能表

Windows 提供名為 [結果專案的 **開啟檔案位置**] 的快捷方式功能表。 如果使用者從該功能表選取專案，則會開啟所選取專案的「父系」 URL。 如果 URL 是 web URL （例如 `https://...` ），則會開啟網頁瀏覽器並流覽至該 url。 您的摘要應該提供每個專案的自訂 url，以確保 Windows 開啟有效的 url。 這可以藉由在專案 XML 內的元素內包含 URL 來完成，如下列範例所示：


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



如果未在專案的 XML 中明確設定此屬性，則 OpenSearch 提供者會將它設定為專案 URL 的父資料夾。 在上述範例中，OpenSearch 提供者會使用連結值，並將[ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell 屬性值設定為 `"https://example.com/"` 。

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>使用屬性描述清單自訂 Windows 檔案總管的視圖

某些 Windows 檔案總管 view 版面配置是由屬性描述清單或 proplists 所定義。 proplist 是以分號分隔的屬性清單（例如 `"prop:System.ItemName; System.Author"` ），可用來控制 Windows 檔案總管中顯示結果的方式。

下列螢幕擷取畫面說明可使用 proplists 自訂之 Windows 檔案總管的 UI 區域：

![顯示 windows explorer ui 區域的螢幕擷取畫面，可使用 proplists 來自訂](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Windows 檔案總管的每個區域都有相關聯的 proplists 集合，其本身會指定為屬性。 您可以針對結果集內的個別專案或一組結果中的所有專案，指定自訂 proplists。



| 要自訂的 UI 區域               | Windows執行自訂的 Shell 屬性 |
|------------------------------------|----------------------------------------------------------|
| 搜尋) 時 (內容視圖模式 | PropList. ContentViewModeForSearch                 |
| 流覽) 時 (內容視圖模式  | PropList. ContentViewModeForBrowse                 |
| 磚視圖模式                     | PropList. TileInfo                                 |
| [詳細資料] 窗格                       | PropList. PreviewDetails                           |
| 提示 (專案的停留工具提示)      | PropList                                  |



 

 

**若要為個別專案指定唯一的 proplist：**

1.  在您的 RSS 輸出中，新增自訂元素，代表您要自訂的 proplist。 例如，下列範例會設定 [詳細資料] 窗格的清單：
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  若要將屬性套用至搜尋結果中的每個專案，而不修改 RSS 輸出，請在 .osdx 檔案中的 **PropertyDefaultValues** 元素內指定 proplist，如下列範例所示：

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>屬性的內容視圖模式版面配置

**PropList. ContentViewModeForSearch** 和 **PropList. ContentViewModeForBrowse** proplists 中指定的屬性清單會決定內容視圖模式中顯示的內容。 如需屬性清單的詳細資訊，請參閱 [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)。

這些屬性會根據下列版面配置模式中顯示的數位來配置：

![顯示內容視圖中預設版面配置模式的螢幕擷取畫面](images/propertiesnumberslayoutpattern.png)

如果我們使用下列屬性清單，


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



接著，我們會看到下列畫面：

![顯示範例屬性版面配置的螢幕擷取畫面。](images/samplepropertylayout.png)

> [!Note]  
> 為了獲得最佳可讀性，應標記最右側資料行中顯示的屬性。

 

### <a name="property-list-flags"></a>屬性清單旗標

只有在 proplists 檔中定義的其中一個旗標適用于內容查看模式配置中的專案顯示： ` "~"` 。 在先前的範例中，Windows 檔案總管 view 會標記一些屬性，例如 `Tags: animals; zoo; lion` 。 當您在清單中指定屬性時，這是預設行為。 例如，proplist `"System.Author"` 會顯示為 `"Authors: value"` 。 當您想要隱藏屬性標籤時，請將放 `"~"` 在屬性名稱的前方。 例如，如果 proplist 具有 `"~System.Size"` ，屬性只會顯示為一個值，而不會顯示標籤。

## <a name="previews"></a>預覽

當使用者在 Windows 檔案總管中選取結果專案，而且預覽窗格已開啟時，就會預覽專案的內容。

預覽版中所要顯示的內容是由 URL 指定，如下所示：

1.  如果已針對專案設定 **WebPreviewUrl** Windows Shell 屬性，則請使用該 URL。
    > [!Note]  
    > 使用 Windows Shell 命名空間，或在 .osdx 檔案中明確對應，就必須在 RSS 中提供屬性。

     

2.  如果沒有，則改為使用連結 URL。

下列流程圖顯示此邏輯。

![流程圖顯示 windows explorer 如何選取要用於預覽的 url](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

預覽可能會使用不同于專案本身的 URL。 這表示，如果您為連結 url 和主機殼提供不同的 url，或 `media:content URL` Windows 檔案總管使用連結 url 來預覽專案，但是會使用其他 URL 進行檔案類型偵測、開啟、下載等等。

Windows 檔案總管如何判斷要使用的 URL：

1.  如果您提供 ItemFolderPathDisplay 的對應，則 Windows 檔案總管會使用該 URL [。](../properties/props-system-itemfolderpathdisplay.md)
2.  如果您未提供對應，則 Windows 檔案總管會識別連結和主機殼 url 是否不同。 如果是的話，Windows 檔案總管使用連結 URL。
3.  如果 url 相同或只有連結 URL，則 Windows 檔案總管會從完整的 url 中移除檔案名，以剖析連結以尋找父容器。
    > [!Note]  
    > 如果您認為 URL 剖析會導致服務的無作用連結，您應該提供屬性的明確對應。

     

## <a name="open-file-location-menu-item"></a>開啟檔案位置功能表項目

當您以滑鼠右鍵按一下專案時，就會出現 [ **開啟檔案位置** ] 功能表命令。 此命令會將使用者帶到容器或該專案的位置。 例如，在 SharePoint 搜尋中，針對文件庫中的檔案選取此選項，就會在網頁瀏覽器中開啟文件庫根。

當使用者按一下 [**開啟檔案位置**] 時，Windows 檔案總管會使用下列流程圖所示的邏輯，嘗試尋找父容器：

![顯示 windows explorer 如何識別父容器的流程圖](images/howwindowsexploreridentifiesaparentcontainer.png)

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

[在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)
</dt> <dt>

[遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)
</dt> <dt>

[在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)
</dt> </dl>

 

 

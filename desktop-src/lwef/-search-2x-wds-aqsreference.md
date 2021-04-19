---
title: 進階查詢語法
description: " (AQS) 的 Advanced Query 語法，可供 Microsoft Windows 桌面搜尋 (WDS) 協助使用者和程式設計師更妥善地定義和縮小搜尋的範圍。"
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "106965417"
---
# <a name="advanced-query-syntax"></a>進階查詢語法

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

 (AQS) 的 Advanced Query 語法，可供 Microsoft Windows 桌面搜尋 (WDS) 協助使用者和程式設計師更妥善地定義和縮小搜尋的範圍。 使用 AQS 可讓您輕鬆地縮小搜尋範圍，並提供更好的結果集。 下列參數可縮小搜尋範圍：

-   檔種類：資料夾、檔、簡報、圖片等等。
-   檔案存放區：特定的資料庫和位置。
-   檔案屬性：大小、日期、標題等等。
-   檔案內容：關鍵字，例如「專案交付專案」、「AQS」、「藍色 suede 鞋」等等。

此外，搜尋參數可以使用搜尋運算子來合併。 本節的其餘部分將說明查詢語法、參數和運算子，以及如何結合以提供目標搜尋結果。 這些表格描述與 WDS 搭配使用的語法，以及可針對 **Windows 桌面搜尋** 結果視窗中顯示的每個檔案種類查詢的屬性。

## <a name="desktop-search-syntax"></a>桌面搜尋語法

搜尋查詢可以包含一或多個關鍵字，以及布林運算子和選擇性準則。 這些選擇性準則可以根據下列內容縮小搜尋範圍：

-   檔案所在的範圍或資料存放區
-   檔案的種類
-   檔案的受控屬性

以下是更詳細說明的選擇性準則，請使用下列語法：

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

假設使用者想要搜尋的檔中包含「上一季」、John 或 Joanne 所建立的片語，以及使用者儲存到 >mydocuments 資料夾。 查詢可能如下所示：

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>範圍：位置和資料存放區

使用者可以將搜尋範圍限制在特定資料夾位置或資料存放區。 例如，如果您使用數個電子郵件帳戶，而您想要將查詢限制為 Microsoft Outlook 或 Microsoft Outlook Express，則可以使用 `store:outlook` 或分別使用或 `store:oe` 。



| 依資料存放區限制搜尋 | 用法              | 範例                                  |
|-------------------------------|------------------|------------------------------------------|
| 桌面                       | 桌面          | 存放區： desktop                            |
| 檔案                         | files            | store： files                              |
| Outlook                       | Outlook          | store： outlook                            |
| Outlook Express               | Oe               | store： oe                                 |
| 特定資料夾               | 資料夾資料夾或 | 資料夾資料夾： >mydocuments 或 in： >mydocuments |



 

如果您有可用來編目自訂存放區的通訊協定處理常式（例如 Lotus Notes），您可以使用存放區的存放區或通訊協定處理常式名稱。 例如，如果您實作為「附注」的「Lotus Notes」資料存放區來執行通訊協定處理常式，則查詢語法會是 `store:notes` 。

### <a name="common-file-kinds"></a>一般檔案類型

使用者也可以將搜尋限制為特定類型的檔案，稱為「檔種類」。 下表列出檔案種類，並提供用來搜尋這類檔案的語法範例。



| 依檔案類型限制：       | 用法              | 範例                        |
|---------------------------------|------------------|--------------------------------|
| 所有檔案類型                  | 一切       | 種類：所有專案                |
| 通訊                  | 通訊   | 種類：通訊            |
| 連絡人                        | 連絡人         | 種類：連絡人                  |
| 電子郵件                          | 電子郵件            | 種類： email                     |
| 立即 Messenger 對話 | 我               | 種類： im                        |
| 會議                        | 會議         | 種類：會議                  |
| 工作                           | 工作            | 種類： tasks                     |
| 備註                           | 版本            | kind： notes                     |
| 文件                       | docs             | 種類：檔                      |
| 文字檔                  | text             | kind： text                      |
| 試算表                    | 電子 表格     | 種類：試算表              |
| 簡報                   | 簡報    | 種類：簡報             |
| 音樂                           | music            | 種類：音樂                     |
| 圖片                        | 圖片             | 種類：圖片                      |
| 影片                          | videos           | 種類：影片                    |
| 資料夾                         | 資料夾          | 種類：資料夾                   |
| 資料夾名稱                     | 資料夾資料夾或 | 資料夾資料夾： mydocs 或 in： mydocs |
| 我的最愛                       | 我的最愛        | 種類：我的最愛                 |
| 程式                        | 程式集         | 種類：程式                  |



 

### <a name="boolean-operators"></a>布林運算子

搜尋關鍵字和檔案屬性可以合併，以使用運算子擴大或縮小搜尋的範圍。 下表說明搜尋查詢中使用的常見運算子。



| 關鍵字/符號  | 範例                                              | 函式                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | 社交非安全性<br/>                        | 尋找包含 *社交*（但不是 *安全性*）的專案。<br/>                                              |
|                 | 社會保障<br/>                           | 尋找包含 *社交* 和 *安全性* 的專案。<br/>                                              |
| OR              | 社交或安全性<br/>                         | 尋找包含 *社交* 或 *安全性* 的專案。<br/>                                                    |
| 引號 | 「社會安全」<br/>                          | 尋找包含確切片語 *社會安全* 的專案。<br/>                                        |
| 括號     |  (社會安全) <br/>                          | 依任何順序尋找包含 *社交* 和 *安全性* 的專案。<br/>                                      |
| >            | 日期： >11/05/04<br/> 大小： >500<br/>  | 尋找日期為11/05/04 之後的專案。 <br/> 尋找大小超過500個位元組的專案。<br/> |
| <            | 日期： <11/05/04 <br/> 大小： <500<br/> | 尋找日期早于11/05/04 的專案。 <br/> 尋找大小小於500個位元組的專案。<br/>   |
| ..              | 日期： 11/05/04. 11/10/04<br/>                    | 尋找日期開頭為11/05/04 且結束于11/10/04 的專案。<br/>                               |



 

> [!Note]
>
> 運算子 **不** 是 and **或** 必須是大寫，而且無法在一個查詢中結合 (例如 `social OR security NOT retirement`) 。

 

### <a name="boolean-properties"></a>布林值屬性

某些檔案類型可讓使用者使用布林值屬性來搜尋檔案，如下表所述。



| 屬性       | 範例                   | 函式                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| 是：附件  | 報表為：附件      | 尋找包含 *報表* 之附件的專案。 與 `isattachment:true` 相同。                           |
| isonline:      | 報表 isonline： true      | 尋找線上且包含 *報表* 的專案。                                                         |
| isrecurring   | 報表 isrecurring： true   | 尋找週期性且包含 *報表* 的專案。                                                       |
| isflagged:     | 報表 isflagged： true     | 尋找已標示 (評論的專案、後續操作，例如) 和包含 *報表* 的專案。                       |
| isdeleted     | 報表 isdeleted： true     | 尋找標示為已刪除 (資源回收筒或刪除專案的專案，例如) 和包含 *報表* 的專案。 |
| iscompleted   | 報表 iscompleted： false  | 尋找未標示為完成且包含 *報表* 的專案。                                        |
| hasattachment: | 報表 hasattachment： true | 尋找包含 *報表* 和附件的專案                                                          |
| hasflag:       | 報表 hasflag： true       | 尋找包含 *報表* 並具有旗標的專案。                                                                |



 

### <a name="dates"></a>日期

除了使用稍早所述的運算子來搜尋特定日期和日期範圍之外，AQS 還可讓您 (如 `today` 、或 `tomorrow` `next week`) 和 day (例如 `Tuesday` 或 `Monday..Wednesday`) 和 month (`February` 值) 。



| 相對於：    | 語法範例                                                                                                                         | 結果                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 天             | 日期：今天<br/> 日期：明天<br/> 日期：昨天<br/>                                                               | 尋找今天日期的專案。<br/> 尋找具有明天日期的專案。<br/> 尋找昨天日期的專案。 <br/>                                                                                                                                                                                                                     |
| 周/月/年 | 日期：本周<br/> 日期：上周<br/> 日期：下個月<br/> 日期：上月<br/> 日期：明年 <br/> | 尋找日期落在目前周內的專案。<br/> 尋找過去一周內有日期的專案。<br/> 尋找日期落在下一周的專案。<br/> 尋找日期在上個月內發生的專案。<br/> 尋找日期落在下一年的專案。 <br/> |



 

## <a name="properties-by-file-kind"></a>依檔案類型的屬性

使用者可以搜尋不同檔案類型的特定屬性。 某些屬性 (例如檔案大小) 通用於所有檔案，而其他屬性則僅限於特定種類。 例如，投影片計數是針對簡報所特有。 下表依檔案種類列出這些屬性。

### <a name="file-kind-everything"></a>檔種類：所有專案

這些都是所有檔案類型通用的屬性。 若要在查詢中包含所有類型的檔案，語法如下：

`kind:everything <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性       | 用法                      | 範例                        |
|----------------|--------------------------|--------------------------------|
| 標題          | 標題、主旨或相關  | 標題：「每季財務」    |
| 狀態         | status                   | 狀態：完成                |
| 日期           | date                     | 日期：上周                 |
| 修改日期  | datemodified 或修改 | 修改日期：上周             |
| 重要性     | 重要性或優先順序   | 重要性：高                |
| 大小           | {1}size{2}                     | 大小： > 50                   |
| 已刪除        | 已刪除或 isdeleted     | isdeleted： true                 |
| 為附件  | isattachment             | isattachment： true              |
| 收件者             | 至或 toname             | 至： bob                         |
| 副本             | cc 或 ccname             | cc： john                        |
| 公司        | company                  | 公司： Microsoft              |
| Location       | location                 | 位置：「會議室102」 |
| 類別       | category                 | 類別：商務              |
| 關鍵字       | 關鍵字                 | 關鍵字：「銷售預測」   |
| 專輯          | 專輯                    | 專輯：「每晚飛出」           |
| 檔案名稱      | filename 或 file         | 檔案名： MyResume              |
| Genre          | genre                    | genre:rock                     |
| 作者         | 作者或             | 作者： "Stephen 王"          |
| 人員         | 人或           | 使用： (sonja 或 david)           |
| 資料夾         | 資料夾、或路徑    | 資料夾：下載               |
| 副檔名 | ext 或 fileext           | ext:.txt                       |



 

### <a name="attachment"></a>附件

這些是附件的通用屬性。 若要將搜尋限制為僅限附件，語法為：

`kind:attachment <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性 | 用法            | 範例                  |
|----------|----------------|--------------------------|
| 人員   | 人或 | 人員： john 或 with： john |



 

### <a name="contacts"></a>連絡人

這些是連絡人的通用屬性。 若要將搜尋限制為僅限連絡人，語法為：

`kind:contacts <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性              | 用法                 | 範例                            |
|-----------------------|---------------------|------------------------------------|
| 職稱             | jobtitle            | jobtitle： CFO                       |
| IM 位址            | imaddress           | imaddress： john\_doe@msn.com        |
| 助理的電話     | assistantsphone     | assistantsphone： 555-3323           |
| 助理名稱        | assistantname       | assistantname： Paul                 |
| Profession            | 職業          | 專業： plumber                 |
| 暱稱              | 暱稱            | 昵稱： Tex                       |
| 配偶                | 配偶              | 配偶： Debbie                      |
| 商業城市         | businesscity        | businesscity：西雅圖               |
| 商務郵遞區號  | businesspostalcode  | businesspostalcode：98006           |
| 商務首頁    | businesshomepage    | businesshomepage:www |
| 回呼電話號碼 | callbackphonenumber | callbackphonenumber： 555-555-2121   |
| 車輛電話             | carphone            | carphone： 555-555-2121              |
| Children              | 兒童            | 子系： Timmy                     |
| 名字            | firstname           | firstname： John                     |
| 姓氏             | lastname            | lastname： Doe                       |
| 首頁傳真              | homefax             | homefax： 555-555-2121               |
| 管理員的名稱        | managersname        | managersname： John                  |
| 呼叫器                 | pager               | 呼機： 555-555-2121                 |
| 商務電話        | >businessphone       | >businessphone： 555-555-2121         |
| 住家電話            | homePhone           | homephone： 555-555-2121             |
| 行動電話          | 手機         | mobilephone： 555-555-2121           |
| Office                | Office              | office：範例                      |
| 周年           | 周年         | 周年紀念日： 1/1/06                 |
| Birthday              | 生日            | 生日： 1/1/06                    |
| 網頁              | 網頁             | 網頁:www          |



 

> [!Note]
>
> 電話號碼會依照輸入進行編制索引。 例如，如果使用者在輸入電話號碼時未包含國家或區功能變數代碼，則如果在電話號碼中使用國家或區功能變數代碼進行搜尋，則使用者將無法找到連絡人。

 

### <a name="communications"></a>通訊

這些是通訊的通用屬性。 若要將搜尋限制為僅限通訊，語法為：

`kind:communications <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性       | 用法                           | 範例                         |
|----------------|-------------------------------|---------------------------------|
| 寄件者           | from 或召集人             | 從： john                       |
| 已收到       | 已接收或已傳送              | 已傳送：昨天                  |
| 主體        | 主旨或標題              | 主旨：「每季財務」   |
| 具有附件 | hasattachments, hasattachment | hasattachment： true              |
| 附件    | 附件或附件     | attachment:presentation.ppt     |
| 密件副本            | 密件副本、bccname 或 bccaddress    | 密件副本： dave                        |
| Cc 位址     | ccaddress 或 cc               | ccaddress： john\_doe@outlook.com |
| 後續追蹤旗標 | followupflag                  | followupflag：2                  |
| 到期日       | duedate 或逾期                | 逾期：上周                   |
| 讀取           | read 或 isread                | 是： read                         |
| 已完成   | iscompleted                   | 是：已完成                    |
| 不完整     | 未完成或 isincomplete    | 為：不完整                   |
| 有旗標       | hasflag 或 isflagged          | 具有：旗標                        |
| 持續時間       | duration                      | 持續時間： > 50                |



 

### <a name="calendar"></a>Calendar

這些是行事曆的通用屬性。 若要將搜尋限制為僅限行事曆，語法為：

`kind:calendar <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性  | 用法                      | 範例          |
|-----------|--------------------------|------------------|
| 重複執行 | 週期性或 isrecurring | 是：週期性     |
| 組織者 | 召集人、依據或    | 召集人： debbie |



 

### <a name="documents"></a>文件

這些是檔的通用屬性。 若要將搜尋限制為僅限檔，語法為：

`kind:documents <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性          | 用法             | 範例                       |
|-------------------|-----------------|-------------------------------|
| 註解          | comments        | 批註：「需要最終評論」 |
| 上次儲存者     | lastsavedby     | lastsavedby： john              |
| 檔管理員  | documentmanager | documentmanager： john          |
| 修訂編號   | revisionnumber  | revisionnumber：1.0。3          |
| 檔案格式   | documentformat  | documentformat： MIMETYPE       |
| 上次列印日期 | datelastprinted | datelastprinted：上周     |



 

### <a name="presentation"></a>簡報

這些是簡報的通用屬性。 若要將搜尋限制為只搜尋簡報，語法為：

`kind:presentation <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性    | 用法        | 範例           |
|-------------|------------|-------------------|
| 投影片計數 | slidecount | slidecount： >20 |



 

### <a name="music"></a>音樂

這些是音樂檔案的通用屬性。 若要將搜尋限制為僅限音樂，語法為：

`kind:music <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性 | 用法                | 範例                  |
|----------|--------------------|--------------------------|
| 位元速率 | 位元速率，費率      | 位元速率：192              |
| 演出者   | 演出者、寄件者 | 演出者： John Singer       |
| 持續時間 | duration           | 持續時間：3               |
| 專輯    | 專輯              | 專輯：「最大點擊次數」    |
| Genre    | genre              | genre:rock               |
| Track    | 追蹤              | 追蹤：12                 |
| Year     | year               | year： > 1980 < 1990 |



 

### <a name="picture"></a>Picture

這些是圖片的通用屬性。 若要限制僅搜尋圖片，語法為：

`kind:picture <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性     | 用法         | 範例               |
|--------------|-------------|-----------------------|
| 攝影機製作  | cameramake  | cameramake：範例     |
| 攝影機模型 | cameramodel | cameramodel：範例    |
| 維度   | dimensions  | 維度：8X10       |
| Orientation  | orientation | 方向：橫向 |
| 拍攝日期   | datetaken   | datetaken：昨天   |
| 寬度        | width       | 寬度：1600            |
| 高度       | 身高      | 高度：1200           |



 

### <a name="video"></a>影片

這些是影片的通用屬性。 若要限制僅搜尋影片，語法為：

`kind:video <property>:<value>`

其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。



| 屬性 | 用法           | 範例                                |
|----------|---------------|----------------------------------------|
| Name     | name、subject | name： "家人度假給海灘 05" |
| 分機      | ext、fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[認知類型](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[從命令列呼叫 WDS](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[從 Web Pages 呼叫 WDS](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 






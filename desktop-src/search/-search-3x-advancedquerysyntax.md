---
description: Advanced Query 語法 (AQS) 是 Windows Search 用來查詢索引以及精簡和縮小搜尋參數的預設查詢語法。
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: 以程式設計方式使用 Advanced 查詢語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970384"
---
# <a name="using-advanced-query-syntax-programmatically"></a>以程式設計方式使用 Advanced 查詢語法

Advanced Query 語法 (AQS) 是 Windows Search 用來查詢索引以及精簡和縮小搜尋參數的預設查詢語法。 開發人員會採用 AQS 來以程式設計方式建立查詢， (以及使用者將其搜尋參數縮小) 。 標準 AQS 是在 Windows 7 中引進的，而且必須在 Windows 7 和更新版本中用來以程式設計方式產生 AQS 查詢。

本主題的組織方式如下：

-   [關於 Advanced Query 語法](#about-advanced-query-syntax)
    -   [範例](#examples)
    -   [屬性](#properties)
-   [以當地語言使用關鍵字](#keyword-use-in-local-languages)
-   [Windows 7 中的標準 Advanced 查詢語法](#canonical-advanced-query-syntax-in-windows-7)
    -   [範例](#examples)
    -   [查詢運算子](#query-operators)
    -   [查詢值](#query-values)
-   [範圍限制](#scope-restrictions)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-advanced-query-syntax"></a>關於 Advanced Query 語法

查詢是由與 AND、OR 和 NOT 連接的基本查詢所組成，如下列範例語法所示：

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> AQS 不區分大小寫，但 AND、OR 和 NOT 除外，其必須全部為大寫。

 

如果查詢有兩個以上的使用和或或，則不論是 AND 或 OR，它們都會從左至右系結。 也就是說，查詢 "apple AND 梨 OR 梅紅" 將會被解釋為 " (apple AND 梨) 或梅紅"，而查詢 "apple OR 梨 AND 梅紅" 將會被視為撰寫為「 (apple 或梨) 和梅紅」。 因此，如果檔包含梅紅這個字，但不是 apple，也不是使用梨，則第一個查詢會傳回它，但第二個查詢則不會傳回。 因此，我們建議您針對任何混合和和或的查詢使用明確括弧，以避免發生錯誤或誤解。

基本查詢會搜尋符合屬性之限制的專案。 基本查詢的唯一必要部分是限制或搜尋值。 如果您未指定屬性，Windows Search 會搜尋所有屬性。 <restr> 表示搜尋限制。

以下是適用于基本查詢的表單：

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

屬性是由關鍵字（例如作者或大小）或標準屬性名稱（例如 [DateModified](../properties/props-system-datemodified.md)）所指定。 屬性的有效表單如下所示：

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

運算子表示作業，例如 < 或 =。 如需有效運算子的清單，請參閱本主題稍後的「查詢運算子」一節。

基本限制是可在不使用括弧撰寫的屬性上進行簡單的限制：

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

限制是搜尋值，例如數值或字串值（選擇性地使用運算子）。 有效的限制表單如下所示：

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

如果您未指定運算子，Windows Search 會為您的查詢選擇最適當的運算子：

-   若為字串屬性，則 \_ 會假設為 COP 單字 \_ STARTSWITH $< 運算子。
-   若為其他所有屬性，則 \_ 會假設 COP 等於 = 運算子。

若要以程式設計方式使用 AQS，建議您一律具有明確的運算子。 搜尋簡單值或值範圍的有效表單如下所示：

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

簡單的值可以包含下列任何一種類型：

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>範例

此查詢會搜尋包含「上一季」、Theresa 或授權作者所撰寫的檔，並將其儲存到資料夾 MyDocs 的查詢，其中結合了三個基本查詢，如下所示：

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

三個基本查詢如下：

-   「上一季」
-   作者： (theresa 或授權) 
-   資料夾： MyDocs

使用標準語法的基本查詢為：

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>屬性

屬性是由關鍵字所參考，可以是 Windows 7 和更新版本中的標準屬性名稱。 Windows UI 中的 AQS 可以使用標籤，而不是 [標準的屬性](../properties/props-system-author.md)名稱，例如作者，而不是 author。 在 Windows Vista 及更早版本中，不論 UI 語言為何，都可以使用英文標籤。 在 Windows 7 和更新版本中，Windows Search 只能辨識目前預設 UI 語言中的關鍵字。

### <a name="support-for-custom-properties"></a>自訂屬性的支援

在 Windows Vista 及更早版本中，AQS 中無法使用自訂屬性。 在 Windows 7 和更新版本中，AQS 會使用向屬性系統註冊的自訂屬性。 如需有關建立自訂屬性的詳細資訊，請參閱 [屬性系統](../properties/building-property-handlers.md)。

### <a name="datetime-properties-in-windows-8"></a>Windows 8 中的日期時間屬性

從 Windows 8 開始，DateTime 屬性 (如 [DateModified](../properties/props-system-datemodified.md)) 支援 [ISO-8601](https://www.w3.org/TR/NOTE-datetime)指定的標準日期和時間格式，選擇性地包括 UTC 時區。

-   **Windows 8 及更早版本，不含 UTC 時區的日期時間：** *YYYY* - *MM* - *DDThh*：*MM*：*ss*

    無論使用者或系統的地區設定為何，此格式都會指定本地時間。

-   **Windows 8，日期時間（UTC 時區）：** *YYYY* - *MM* - *DDThh*：*MM*：*ssTZD*

    此格式會指定指定之 UTC 時區的時間。

## <a name="keyword-use-in-local-languages"></a>以當地語言使用關鍵字

在 Windows 7 （含）以後版本中，助憶鍵關鍵字僅適用于系統語言，例如德文關鍵字（僅限德文版作業系統）和英文關鍵字（僅限英文版作業系統）。 [System. author](../properties/props-system-author.md) 是標準關鍵字，而 system.string 屬性的助憶鍵值為 author，例如。 引進標準關鍵字可彌補在所有作業系統上（不論語言為何）都不能完全辨識英文助憶鍵關鍵字的事實，就像是 Windows Vista 和更早版本中的情況一樣。

> [!Note]  
> 在 Windows 7 和更新版本中，Windows Search 只會辨識目前預設語言的關鍵字，而不是以英文為目前的預設值。 我們建議開發人員一律使用標準語法，讓其應用程式不會有關鍵詞的語言問題。

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Windows 7 中的標準 Advanced 查詢語法

Windows 7 中的關鍵字已引進標準語法。 具有標準屬性的查詢範例為 `System.Message.FromAddress:=me@microsoft.com` 。 在 Windows 7 和更新版本上執行的應用程式中撰寫查詢程式碼時，您必須使用標準語法以程式設計方式產生 AQS 查詢。 如果您未使用標準語法，而您的應用程式是以與應用程式程式碼語言不同的地區設定或 UI 語言進行部署，您的查詢將不會正確地解讀。

標準關鍵字語法的慣例如下：

-   屬性的標準語法是其標準名稱，例如 `System.Photo.LightSource` 。 標準名稱不區分大小寫。
-   布林運算子的標準語法是由關鍵字 AND、OR 和 NOT 組成，全部都是大寫。
-   運算子 <、>、= 等等都不會當地語系化，因此也是標準語法的一部分。
-   如果屬性 `P` 有列舉值或名為 N ₁至 nk.bin 的範圍，則 *I* 值或範圍的標準語法是 P 的正式名稱，後面接著字元 \# ，後面接著 N <sub>I</sub>，如下列範例所示：
    -   `System.Photo.LightSource#Daylight`等等 `System.Photo.LightSource#StandardA` 。
-   若為具有值或範圍名稱為 N ₁至 Nk.bin 的已定義語義型別 T， *I* 值或範圍的標準語法為 t 的正式名稱，後面接著字元 \# ，後面接著 N <sub>I</sub>，如下列範例所示：
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   針對文字值（例如單字或片語），標準語法與一般語法相同。 標準語法中具有常值的查詢範例如下：
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> 在 Windows 7 和更新版本中，沒有適用于數位的標準語法。 因為浮點數格式會因地區設定而異，所以不支援使用包含浮點常數的標準查詢。 相反地，整數常數只能使用數位來撰寫 (千位) 的分隔符號，並可在 Windows 7 和更新版本的標準查詢中安全地使用。

 

### <a name="examples"></a>範例

下表顯示標準屬性的一些範例，以及使用它們的語法。



| 標準屬性的類型 | 範例                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 字串值               | [System.Author](../properties/props-system-author.md)<br/>    | 在 author 屬性中搜尋字串值： <br/>`System.Author:Jacobs`                                                                                                                                                              |
| 列舉範圍          | [System. Priority](../properties/props-system-priority.md)             | Priority 屬性的值範圍可以是數值：<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System. IsDeleted](../properties/props-system-isdeleted.md)<br/> | 布林值可以搭配任何布林值屬性使用：<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`和 `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| 數值                  | [System. Size](../properties/props-system-size.md)<br/>      | 您無法安全地撰寫牽涉到浮點常數的標準查詢，因為浮點數格式會因地區設定而異。 您必須撰寫整數，但不能為千位分隔符號。 例如：<br/>`System.Size:<12345` |



 

如需標準屬性和屬性系統的一般詳細資訊，請參閱 [系統屬性](../properties/props.md)。 或者，請參閱公用標頭檔。

### <a name="query-operators"></a>查詢運算子

如果屬性 p 具有某個專案的多個值，則 p：的 AQS 查詢會傳回 <restr> 專案，如果 <restr> 至少有一個值為 **true** 。  (<restr> 代表限制。 ) 

下表所列的語法包含運算子、運算子符號、範例和範例描述。 運算子和符號可以用在任何語言中，並包含在任何查詢中。 請勿使用 COP \_ 隱含或 COP \_ 應用程式 \_ 特定的運算子。 某些運算子具有可互換的符號。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>運算子</th>
<th>符號</th>
<th>範例</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System. FileExtension： = &quot; .txt&quot;<br/></td>
<td>此值為字串 &quot; <em>.txt</em> &quot; 。<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System.string：≠ picture<br/> DateTaken：-[] ¹<br/> 系統種類： &lt; &gt; 圖片<br/> System.object：不是圖片<br/> System.object：--圖片<br/></td>
<td><a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。<br/> <a href="/windows/desktop/properties/props-system-photo-datetaken">DateTaken</a>屬性具有值。<br/> <a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。 <br/> <a href="/windows/desktop/properties/props-system-kind">System.object</a>屬性不是圖片。 <br/> 未套用至相同屬性的雙重運算子不會取消。因此，system.string：--picture 相當於 System.object：-picture 和 system.string： NOT picture。<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. Size： &lt; 1kb<br/></td>
<td>此值小於 <em>1kb</em>。<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>ItemDate： &gt; StructuredQueryType. DateTime # Today<br/></td>
<td>此值大於 <em>今天</em>。<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. Size： &lt; = 1kb<br/></td>
<td>這個值小於或等於 <em>1kb</em>。<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. Size： &gt; = 1kb<br/></td>
<td>此值等於或大於 <em>1kb</em>。<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System.string： ~ &lt; &quot; c + + 入門&quot;<br/></td>
<td>尋找檔案名以 &quot; <em>c + + 入門</em>字元開頭的專案 &quot; 。<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>CameraModel： ~ &gt; 非<br/></td>
<td>尋找屬性值結尾為 <em>非</em>字元的專案。<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System.object. ~ = round <br/> Autosummary： ~ ~ round<br/></td>
<td>在主旨中尋找具有這個字串的訊息，並將符合 &quot; g<em>四捨五入</em> 規則 &quot; 。<br/> 尋找包含 Autosummary 的所有專案，其中包含 <em>四捨五入</em>的字元。<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author： ~！ &quot;桑傑&quot;<br/></td>
<td>尋找未 &quot; 在其中<em>sanjay</em>字元順序的作者 &quot; 。<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System.string： ~ &quot; Mic？ Osoft W * d&quot;<br/></td>
<td>尋找檔案名以 <em>Mic</em>開頭的檔案，後面接著一些字元，後面接著 <em>osoft w</em>，後面接著以 <em>d</em>結尾的任何字元。 <br/> ？ 和 * 字元不會以逐字的方式解讀，而且可以像 DOS 樣式的萬用字元一樣運作：<br/>
<ul>
<li>? 符合一個任一字元。</li>
<li>* 符合零或多個任一字元。</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>StructuredQuery： $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>適用于 Windows 7 和更新版本。 在 [屬性] 中尋找 [ &quot; <em>Sanjay Jacobs</em> ] &quot; 。 <em>Sanjay</em>字後面必須接著<em>Jacobs</em>這個字。<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author： $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>適用于 Windows 7 和更新版本。 尋找作者包含開頭為字元 San 之單字的任何專案 &quot; <em></em> &quot; 。<br/> 尋找檔案名中包含以 <em>微型</em>開頭之單字的任何檔案，後面接著以 <em>exe</em>開頭的單字。<br/></td>
</tr>
</tbody>
</table>



 

¹空的方括弧 (\[ \]) 表示「沒有值」。

若為字串屬性，預設作業會是 COP \_ word \_ 開頭 \_ ，或 COP \_ 單字 \_ 等於。

### <a name="query-values"></a>查詢值

下表列出如何限制查詢值的實用範例。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值/符號</th>
<th>範例</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>自動<br/></td>
<td>可以搜尋的任何字元序列。 字串不能包含屬於語法一部分的空白字元或字元組合。 此範例會搜尋以 <em>auto</em>開頭的單字。<br/></td>
</tr>
<tr class="even">
<td>加上引號的字串 &quot;&quot;</td>
<td>&quot;結論：有效 &quot; &quot; 的 &quot; &quot; blue &quot; &quot; team&quot;<br/></td>
<td>任何字元序列。 字串不會被解釋為語法的一部分。<br/> 如果查詢成對，引號可以包含在查詢中。 此範例會搜尋 <em> &quot; blue &quot; team</em>。<br/></td>
</tr>
<tr class="odd">
<td>整數</td>
<td>5678<br/></td>
<td>只使用整數的數位。 請勿使用任何分隔符號作為千位。<br/></td>
</tr>
<tr class="even">
<td>浮點數</td>
<td>5678.1234<br/></td>
<td>因為浮點數格式會因地區設定而異，所以標準查詢無法使用浮點數常數。 使用具有浮點數的標準語法不是當地語系化安全的。 <br/></td>
</tr>
<tr class="odd">
<td>布林<strong>值 true</strong> / <strong>false</strong></td>
<td>IsRead： = StructuredQueryType。布林值 # True<br/> IsEncrypted：-System.object. StructuredQueryType。布林值 # False<br/></td>
<td><strong>TRUE</strong>布林值。<br/> <strong>FALSE</strong>布林值。<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System.string： = []<br/></td>
<td>空白方括弧表示沒有任何值。 這個範例會尋找尚未標記的所有專案。 <br/></td>
</tr>
<tr class="odd">
<td>絕對日期</td>
<td>System. ItemDate： 1/26/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>尋找日期為2010年1月26日的專案。<br/> 尋找于2002年10月15日至19:00:00 與19:00:59 之間修改的專案。 <br/>
<blockquote>
[!Note]<br />
由於日期格式 (類似浮點數格式) 不同的地區設定，因此不支援使用具有絕對日期的標準語法，而且不是當地語系化的安全。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>相對日期</td>
<td>ItemDate： StructuredQueryType. DateTime # Today<br/> DateAcquired： System. StructuredQueryType. DateTime # NextMonth<br/> DateReceived： StructuredQueryType. DateTime # LastYear<br/></td>
<td>尋找今天日期的專案。<br/> 在下個月尋找具有日期的專案。<br/> 尋找過去一年中日期的專案。<br/>
<blockquote>
[!Note]<br />
除了搜尋特定日期和日期範圍之外，AQS 還可辨識相對日期值 (例如 <em>today</em>、 <em>明天</em>、 <em>nextweek</em>、 <em>nextmonth</em>) 和 day (例如 <em>星期二</em> 或 <em>星期一。星期三</em>) 和 month (<em>二月</em>) 。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>ItemDate： 11/05/04. 11/10/04 系統。大小：5kb。10kb<br/></td>
<td>雙句點表示值範圍。 尋找日期介於11/05/04 和11/10/04 （含）之間的專案。<br/> 尋找大小介於5和10kb 之間的專案。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>範圍限制

使用者可以將搜尋範圍限制在特定資料夾位置或資料存放區。 例如，如果您使用數個電子郵件帳戶，而您想要將查詢限制為 Microsoft Outlook 或 Microsoft Outlook Express，則可以使用 `System.Search.Store:mapi` 或分別使用或 `System.Search.Store:oe` 。 下表說明如何依資料存放區限制搜尋的一些範例。



| 依資料存放區限制搜尋  | 關鍵字 | 範例                                     |
|--------------------------------|---------|---------------------------------------------|
| 檔案                          | file    | System. Store： file                    |
| Outlook                        | Mapi    | System. Store： mapi                    |
| Outlook Express                | Oe      | System. Store： oe                      |
| 離線檔案                  | Csc     | System. Store： csc                     |
| 本機磁片磁碟機上的特定資料夾 | folder  | ItemFolderNameDisplay： C： " \\ MyFolder" |



 

## <a name="additional-resources"></a>其他資源

-   在 Windows 7 （含）以後版本中，您可以根據是否符合 AQS 條件來使用快捷方式功能表選項。 如需詳細資訊，請參閱 [建立快捷方式功能表處理常式](../shell/context-menu-handlers.md)中的「使用 Advanced Query 語法取得靜態動詞的動態行為」。
-   AQS 查詢可以限制為特定類型的檔案，也就是所謂的檔案類型。 如需詳細資訊，請參閱 [檔案類型和關聯](../shell/fa-intro.md)。 如需屬性參考 [檔，請參閱 system.string](../properties/props-system-kind.md)和 [system. KindText](../properties/props-system-kindtext.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以程式設計方式查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[使用 SQL 和 AQS 方法來查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[使用搜尋-ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

---
description: Windows 使用者可以將搜尋儲存為搜尋資料夾，這個檔案是由 XML 檔案所產生，該檔案是以可供 Windows 搜尋子系統使用的形式儲存查詢。
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: 儲存的搜尋檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19cf936f78b045814bf7cba31a123c40d61927a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511094"
---
# <a name="saved-search-file-format"></a>儲存的搜尋檔案格式

在 Windows Vista 和更新版本中，使用者可以將搜尋儲存為搜尋資料夾，這個檔案是由 XML 檔案所產生，該檔案是以可供 Windows 搜尋子系統使用的形式來儲存查詢。 本主題說明 (的檔案格式 \* 。搜尋-ms) ，其中包含下列各節：

- [已儲存搜尋的總覽](#overview-of-saved-searches)
- [\<viewInfo> 元素](/windows)
  - [\<viewInfo> 屬性](/windows)
  - [\<viewInfo> 子項目](/windows)
- [\<query> 元素](/windows)
  - [\<query> 子項目](/windows)
- [\<properties> 元素](/windows)
- [搜尋-ms 檔案格式的完整規格](#full-specification-of-the-search-ms-file-format)
- [已儲存搜尋的範例](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>已儲存搜尋的總覽

使用者可以將搜尋查詢儲存為搜尋資料夾，Windows 檔案總管顯示在 [搜尋] 資料夾底下的虛擬資料夾。 開啟搜尋資料夾會執行已儲存的搜尋，並顯示最新的結果。 儲存的搜尋檔案會以 Windows Search 可採取行動的格式來儲存查詢、指定要搜尋的內容、搜尋位置，以及如何呈現結果。

已儲存的搜尋是從 XML 檔案產生， (\* 。搜尋-ms) 在% userprofile% \\ 搜尋資料夾中。 資料會分成 XML 檔案中的三個主要元素：

- \<viewInfo> 指定簡報資訊
- \<query> 指定 (搜尋查詢資訊
- \<properties> 指定的屬性 \* 。搜尋-ms 檔案本身

下列範例顯示已儲存之搜尋檔案的高階結構。

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>\<viewInfo> 項目

\<viewInfo>元素會指定如何向使用者呈現結果。 下列範例顯示元素的結構。

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> 屬性

下表說明 \<viewInfo> 元素的屬性。

| 屬性     | 描述                                                                     | 值                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| viewMode      | 指定資料夾的視圖。                                                      | 詳細資料 \| 圖示 \| 磚  |
| iconSize      | 控制非堆疊時，專案的圖示和縮圖的預設大小。 | 介於16到256之間的整數 |
| stackIconSize | 僅供內部使用。 請勿使用。                                              | n/a                        |
| displayName   | 僅供內部使用。 請勿使用。                                              | n/a                        |
| autoListFlags | 僅供內部使用。 請勿使用。                                              | n/a                        |
| folderFlags   | 僅供內部使用。 請勿使用。                                              | n/a                        |
| taskFlags     | 僅供內部使用。 請勿使用。                                              | n/a                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> 子項目

專案的子專案 \<viewInfo> 會指定 Windows 檔案總管搜尋結果中顯示的資料行，以及如何分組和排序結果。 每個子項目都包含一組已排序的資料行，這些資料行是由系統屬性的標準名稱所識別 (例如，system.servicemodel) 。 如果未在儲存的搜尋檔案中定義，搜尋結果會顯示一組預設的資料行，適用于所顯示的檔案類型。

| 元素               | 描述                                                                                        | 值                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | 指定要出現在結果檢視中的已排序資料行清單。 使用者可以變更此清單。 | 任何系統屬性。                                         |
| frequentlyUsedColumns | 僅供內部使用。 請勿使用。                                                                 | n/a                                                          |
| columnChooserColumns  | 僅供內部使用。 請勿使用。                                                                 | n/a                                                          |
| groupBy               | 指定用來將結果分組的單一系統屬性。 使用者可以變更此值。  | 任何系統屬性。                                         |
| sortList              | 指定排序結果所依據之資料行的排序清單。                                       | 最多四個系統屬性。 使用者可以變更此清單。 |
| stackList             | 僅供內部使用。 請勿使用。                                                                 | n/a                                                          |

## <a name="query-element"></a>\<query> 項目

\<query>元素會指定屬性，以定義查詢結果的方式。 下列範例顯示元素的結構。

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> 子項目

下表說明 \<scope> 元素的子項目。

| 元素    | 描述                                                                                                               | 值                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 提供者  | 僅供內部使用。 請勿使用。                                                                                        | n/a                                                                                                                                                                                                                                                            |
| 對子 | 僅供內部使用。 請勿使用。                                                                                        | n/a                                                                                                                                                                                                                                                            |
| 影響範圍      | 識別要在搜尋中包含或排除的位置。                                                                 | 要包含或排除之位置的路徑或 [已知資料夾識別碼](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) 。 此元素也可以指定搜尋是否應包含/排除 (淺層或深層搜尋) 的子路徑。 |
| kindList   | 識別要搜尋)  (的檔案類型。                                                                             | 任何 system.string 值。                                                                                                                                                                                                                                         |
| 條件 | 指定篩選結果的規則。 例如，可能會將結果限制為傳送給特定人員或的電子郵件。 | Microsoft.visualstudio.testtools.uitest.extension.andcondition.match、orCondition、notCondition、leafCondition。                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope> 項目

\<scope>元素會識別要在搜尋中包含或排除的位置。 \<scope>元素必須包含至少一個 \<include> 子項目，以及零或多個 \<exclude> 元素。 您可以將位置指定為支援的路徑 (環境變數) 或作為 [已知的資料夾識別碼](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid)。 此外，您可以將非遞迴設定為 "true" 或 "false" (預設為遞迴) ，藉此指定每個位置來搜尋 deep 或淺層。 您可以藉由指定 exclude 元素來排除部分內含的位置清單。

以下顯示的專案 \<scope> 會搜尋檔特殊資料夾，但不會搜尋其子系、"e：" 磁片區和其子系，而不是 "e： \\ windows" 目錄或其任何子系：

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>\<kindList> 項目

這些元素會定義應該出現在程式庫中之專案的「種類」聯集。 有效值為：

- 行事曆
- communication
- 連絡人
- 文件
- 電子郵件
- 饋送
- folder
- 遊戲
- instantmessage
- 雜誌
- link
- 電影
- music
- 注意
- picture
- 程式
- recordedtv
- searchfolder
- 工作 (task)
- 影片
- webhistory
- item
- 其他

### <a name="conditions-element"></a>\<conditions> 項目

條件是用於比較搜尋結果的篩選準則。 例如，您可以篩選符合特定準則的結果，例如作者名稱或檔案大小。 條件集內建在具有邏輯 AND、OR 和 NOT 分支的單一條件樹狀結構中。

下列範例顯示元素的結構 \<condition> 。

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

條件類型可以是下列其中一項：

| 類型          | Description                                 | 可用的屬性                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| Microsoft.visualstudio.testtools.uitest.extension.andcondition.match  | 結合兩個或多個子條件 | n/a                                                |
| orCondition   | 分離兩個以上的子條件 | n/a                                                |
| notCondition  | 子條件的否定               | n/a                                                |
| leafCondition | 比較屬性與值                | property、propertyType、operator、value、valuetype |

專案 \<leafCondition> 的屬性會識別要篩選結果的屬性和值。

### <a name="example-conditions-element"></a>範例： \<conditions> 元素

下列範例會針對 John 撰寫的所有未讀取專案篩選結果。 也就是說，IsRead 屬性是 false，而字串 "john" 則出現在 Author 或 ItemAuthors 屬性中。

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>\<properties> 項目

\<properties>元素會描述已儲存之搜尋本身的屬性。 儲存的搜尋檔案支援四個屬性： \<author> 、 \<kind> 、 \<description> 和 \<tags> 。 這些僅供內部使用。

## <a name="full-specification-of-the-search-ms-file-format"></a>搜尋-ms 檔案格式的完整規格

以下是已儲存搜尋檔案的完整 XML 範例。

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>已儲存搜尋的範例

以下是搜尋 ms 檔案的範例 \* 。

### <a name="recent-documentssearch-ms"></a>最近使用的檔。搜尋-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>最近的音樂。搜尋-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>最近由我共用。搜尋-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```

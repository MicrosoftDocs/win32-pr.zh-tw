---
description: 瞭解如何在 Windows Search 中使用連結引數，作為控制搜尋範圍的方法。
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: '連結引數 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a1ae426881473a631a11b40ec8e567f600daa4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886822"
---
# <a name="crumb-argument-windows-search"></a>連結引數 (Windows Search) 

`crumb`引數支援 (AQS) 語句的完整先進查詢語法，特別適用于控制搜尋範圍的方法。 除了 AQS ements 之外， `crumb` 引數也可以 `location` 在 Windows Vista 和 XP 上的參數上採用特殊參數 `kind` `store` ，如本主題稍後所述。

本主題的組織方式如下：

-   [連結語法](#crumb-syntax)
    -   [一般範例](#general-examples)
-   [使用連結搭配 Vista (位置) ](#using-crumb-with-vista-location)
    -   [Vista 範例](#vista-examples)
    -   [一般資料夾的常數](#constants-for-common-folders)
-   [使用連結搭配 Windows XP (種類和 store) ](#using-crumb-with-windows-xp-kind-and-store)
    -   [XP 範例](#xp-examples)
-   [相關主題](#related-topics)

 

## <a name="crumb-syntax"></a>連結語法

連結語法如下所示：


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



資料 &lt; 行 &gt; 部分是屬性系統中的任何屬性，而且 &lt; 值 &gt; 部分是該屬性的有效值。 <label>部分是顯示為使用者介面提示之屬性的選擇性別名。

### <a name="general-examples"></a>一般範例


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>使用連結搭配 Vista (位置) 

在連結參數中，Windows vista 支援完整 AQS 和 `location` 屬性，此屬性只有 Windows Vista 才有提供特殊的執行功能。 您可以在 `location` 單一連結參數中使用 AQS 字串或屬性，但不能同時使用兩者。 如果連結參數包含 AQS，則會忽略該連結參數中的其他專案。

`location`屬性可讓您指定要搜尋的路徑。 Windows如果位置是在索引子的編目範圍之外，Vista 可以略過索引子並直接進行目錄。 因此，這些搜尋可能會比使用索引子的搜尋更慢。

當您指定 `location` 屬性時，支援兩個額外的參數和選擇性參數：



| 參數 | 值                  | 說明                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 包含 | 包含、排除        | 指定查詢是否應包含或排除該路徑的專案。 "Include" 是預設值。 WindowsVista 不支援排除專案（不含）。  (請參閱範例)  |
| 遞迴 | 遞迴、非遞迴 | 指定搜尋是否應從 location： value 中定義的值開始遞迴所有子資料夾 &lt; &gt; 。 「遞迴」是預設值。                             |



 

若要使用 search-ms： protocol 設定搜尋範圍，您有不同的選項，視範圍的目標而定。

本機電腦上的資料夾：

-   使用 AQS (連結 = folder： <URL 編碼路徑>) 
-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

遠端電腦/網路上的資料夾：

-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

經由已知 UNC 通訊協定處理常式存取的資料夾：

-   使用 AQS (連結 = store： <UNC protocol handler name>) 
-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

### <a name="vista-examples"></a>Vista 範例


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



第一個範例會從 shell://Personal 位置開始搜尋「休假」 (使用者的我的檔資料夾) 的特殊快捷方式，包括該資料夾和所有子資料夾。 請參閱下表。

第二個範例會在 C： pictures 內執行搜尋 \\ ，但無法在 c： \\ pictures \\ 重複。

第三個範例會在 C：檔內執行搜尋 \\ ，其限制為 [kind] 屬性設定為 [圖片] 的檔案。

### <a name="constants-for-common-folders"></a>一般資料夾的常數

WindowsVista 可讓您使用[KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85))值，以提供獨特的系統獨立方式來識別應用程式經常使用的特殊資料夾，但在任何指定的系統上可能不會有相同的名稱或位置。 例如，系統資料夾可能是一個系統上的 "c： \\ Windows"，另一個則是 "c： \\ Winnt"。 在 Windows Vista 之前，使用[CSIDLs](/windows/desktop/shell/csidl) 。

使用下列語法來使用這些位置：


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>使用連結搭配 Windows XP (種類和 store) 

針對 Windows XP (WDS 3.x) 上的 Windows Search，AQS 條款 "kind" 和 "store" 具有特殊的實作為。 「種類」值與 [WDS 2.x 中使用的值](../lwef/-search-2x-wds-perceivedtype.md)相同。 "Store" 值包括下列各項：

-   Mapi
-   file
-   outlookexpress
-   任意

### <a name="xp-examples"></a>XP 範例


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



第一個範例會從 John 傳回 Microsoft Outlook Express 電子郵件，其中包含自訂標籤「OE 郵件」。 第二個範例會執行搜尋來自 John 的任何通訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[具有 Parameter-Value 引數的開始使用](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[地區設定識別碼引數](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[語法引數](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY 引數](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[子查詢引數](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 

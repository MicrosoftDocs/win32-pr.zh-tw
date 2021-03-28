---
description: 程式庫說明檔是定義程式庫的 XML 檔。
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: 程式庫描述架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104973904"
---
# <a name="library-description-schema"></a>程式庫描述架構

程式庫說明檔是定義程式庫的 XML 檔。 程式庫會將本機和遠端儲存位置的專案匯總成 Windows 檔案總管中的單一視圖。 程式庫描述檔案會遵循程式庫描述架構，並儲存為連結 \* 庫-ms 檔案。

本主題包含下列幾節：

-   [程式庫描述架構的總覽](#overview-of-the-library-description-schema)
-   [命名空間版本控制](#namespace-versioning)
-   [程式庫描述檔案的範例](#example-of-a-library-description-file)
-   [相關主題](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>程式庫描述架構的總覽

程式庫包含儲存在一或多個儲存位置中的檔案。 程式庫不會實際儲存這些檔案;相反地，他們會監視包含檔案的資料夾，並讓使用者以不同的方式存取和排列檔案。 例如，使用者可以將音樂檔案放在本機硬碟上的多個資料夾中，也可以在外部硬碟上。 使用 **音樂媒體** 櫃時，使用者可以同時存取所有的檔案，並以演出者名稱或專輯標題將其全部以單一群組進行排序。

程式庫描述架構包含三個主要部分，如下表所述：



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一般程式庫資訊 | 程式庫顯示給使用者時，Windows 檔案總管可以使用的程式庫相關資訊，例如名稱、擁有者、版本、圖示。                   |
| 程式庫屬性          | 描述程式庫的一或多個屬性。 這些自訂屬性是程式庫特有的。                                                     |
| 程式庫位置           | 一或多個搜尋連接器，用來識別要包含在程式庫中的存放位置。 每個位置也可以有一組唯一的屬性。 |



 

Windows 7 中的程式庫檔案會儲存在已知的資料夾 FOLDERID 連結 \_ 庫中。 依預設，[FOLDERID 連結 \_ 庫] 資料夾位於% USERPROFILE% \\ AppData \\ 漫遊 \\ Microsoft \\ Windows 連結 \\ 庫。

## <a name="namespace-versioning"></a>命名空間版本控制

程式庫描述檔案格式 (程式庫 \* -ms) 的版本是藉由變更命名空間來追蹤。 若為 Windows 7，檔案格式具有下列預設命名空間： https://schemas.microsoft.com/windows/2009/library 。

不過，您可以使用特定程式庫描述檔案中的專案來追蹤文件庫內容的版本 [<version>](schema-library-version.md) 。

## <a name="example-of-a-library-description-file"></a>程式庫描述檔案的範例

以下是程式庫描述檔案的範例，此檔案會定義檔檔案的程式庫。


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[folderType 元素 (程式庫架構) ](schema-library-foldertype.md)
</dt> <dt>

[iconReference 元素 (程式庫架構) ](schema-library-iconreference.md)
</dt> <dt>

[isLibraryPinned 元素 (程式庫架構) ](schema-library-islibrarypinned.md)
</dt> <dt>

[libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md)
</dt> <dt>

[ (程式庫架構的 name 元素) ](schema-library-name.md)
</dt> <dt>

[ownerSID 元素 (程式庫架構) ](schema-library-ownersid.md)
</dt> <dt>

[property 元素 (程式庫架構) ](schema-library-property.md)
</dt> <dt>

[propertyStore 元素 (程式庫架構) ](schema-library-propertystore.md)
</dt> <dt>

[searchConnectorDescription 元素 (程式庫架構) ](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchConnectorDescriptionList 元素 (程式庫架構) ](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateInfo 元素 (程式庫架構) ](schema-library-templateinfo.md)
</dt> <dt>

[version 元素 (程式庫架構) ](schema-library-version.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

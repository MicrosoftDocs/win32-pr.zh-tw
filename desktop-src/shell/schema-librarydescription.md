---
description: <libraryDescription>元素是程式庫定義的最上層容器。 這個元素是必要的。
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: 'libraryDescription 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a454321649746dc9408110e2fb96a616934977022ac80a4c0325494d354bfb46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942058"
---
# <a name="librarydescription-element-library-schema"></a>libraryDescription 元素 (程式庫架構) 

<libraryDescription>元素是程式庫定義的最上層容器。 這個元素是必要的。

## <a name="syntax"></a>Syntax


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>項目資訊



| 父元素 | 子元素                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [ (程式庫架構) 的名稱元素 ](schema-library-name.md)。 必要。                                                     |
|                | [OwnerSID 元素 (程式庫架構) ](schema-library-ownersid.md)。 選擇性。                                             |
|                | [Version 元素 (程式庫架構) ](schema-library-version.md)。 選擇性。                                               |
|                | [IsLibraryPinned 元素 (程式庫架構) ](schema-library-islibrarypinned.md)。 選擇性。                               |
|                | [IconReference 元素 (程式庫架構) ](schema-library-iconreference.md)。 選擇性。                                   |
|                | [PropertyStore 元素 (程式庫架構) ](schema-library-propertystore.md)。 選擇性。                                   |
|                | [TemplateInfo 元素 (程式庫架構) ](schema-library-templateinfo.md)。 選擇性。                                     |
|                | [SearchConnectorDescriptionList 元素 (程式庫架構) ](schema-library-searchconnectordescriptionlist.md)。 必要。 |



 

## <a name="remarks"></a>備註

每個程式庫都可以包含一個或多個位置，而使用者可以使用 Windows 檔案總管流覽或搜尋這些位置。 使用 [<searchConnectorDescription>](schema-library-searchconnectordescription.md) 容器元素中的元素，搜尋連接器會定義這些位置 [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) 。

程式庫可以有一組唯一的屬性，而且程式庫中的位置也可以有一組唯一的屬性。 這些屬性是在 [<property>](schema-library-property.md) 容器元素內的元素中定義 [<propertyStore>](schema-library-propertystore.md) 。

## <a name="example"></a>範例


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

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

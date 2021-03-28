---
description: <libraryDescription>元素是程式庫定義的最上層容器。 這個元素是必要的。
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: 'libraryDescription 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972293"
---
# <a name="librarydescription-element-library-schema"></a><span data-ttu-id="760df-104">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="760df-104">libraryDescription Element (Library Schema)</span></span>

<span data-ttu-id="760df-105"><libraryDescription>元素是程式庫定義的最上層容器。</span><span class="sxs-lookup"><span data-stu-id="760df-105">The <libraryDescription> element is the top-level container for the library definition.</span></span> <span data-ttu-id="760df-106">這個元素是必要的。</span><span class="sxs-lookup"><span data-stu-id="760df-106">This element is required.</span></span>

## <a name="syntax"></a><span data-ttu-id="760df-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="760df-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="760df-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="760df-108">Element Information</span></span>



| <span data-ttu-id="760df-109">父元素</span><span class="sxs-lookup"><span data-stu-id="760df-109">Parent element</span></span> | <span data-ttu-id="760df-110">子元素</span><span class="sxs-lookup"><span data-stu-id="760df-110">Child elements</span></span>                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | <span data-ttu-id="760df-111">[ (程式庫架構) 的名稱元素 ](schema-library-name.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-111">[name Element (Library Schema)](schema-library-name.md).</span></span> <span data-ttu-id="760df-112">必要。</span><span class="sxs-lookup"><span data-stu-id="760df-112">Required.</span></span>                                                     |
|                | <span data-ttu-id="760df-113">[OwnerSID 元素 (程式庫架構) ](schema-library-ownersid.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-113">[ownerSID Element (Library Schema)](schema-library-ownersid.md).</span></span> <span data-ttu-id="760df-114">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-114">Optional.</span></span>                                             |
|                | <span data-ttu-id="760df-115">[Version 元素 (程式庫架構) ](schema-library-version.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-115">[version Element (Library Schema)](schema-library-version.md).</span></span> <span data-ttu-id="760df-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-116">Optional.</span></span>                                               |
|                | <span data-ttu-id="760df-117">[IsLibraryPinned 元素 (程式庫架構) ](schema-library-islibrarypinned.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-117">[isLibraryPinned Element (Library Schema)](schema-library-islibrarypinned.md).</span></span> <span data-ttu-id="760df-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-118">Optional.</span></span>                               |
|                | <span data-ttu-id="760df-119">[IconReference 元素 (程式庫架構) ](schema-library-iconreference.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-119">[iconReference Element (Library Schema)](schema-library-iconreference.md).</span></span> <span data-ttu-id="760df-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-120">Optional.</span></span>                                   |
|                | <span data-ttu-id="760df-121">[PropertyStore 元素 (程式庫架構) ](schema-library-propertystore.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-121">[propertyStore Element (Library Schema)](schema-library-propertystore.md).</span></span> <span data-ttu-id="760df-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-122">Optional.</span></span>                                   |
|                | <span data-ttu-id="760df-123">[TemplateInfo 元素 (程式庫架構) ](schema-library-templateinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-123">[templateInfo Element (Library Schema)](schema-library-templateinfo.md).</span></span> <span data-ttu-id="760df-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="760df-124">Optional.</span></span>                                     |
|                | <span data-ttu-id="760df-125">[SearchConnectorDescriptionList 元素 (程式庫架構) ](schema-library-searchconnectordescriptionlist.md)。</span><span class="sxs-lookup"><span data-stu-id="760df-125">[searchConnectorDescriptionList Element (Library Schema)](schema-library-searchconnectordescriptionlist.md).</span></span> <span data-ttu-id="760df-126">必要。</span><span class="sxs-lookup"><span data-stu-id="760df-126">Required.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="760df-127">備註</span><span class="sxs-lookup"><span data-stu-id="760df-127">Remarks</span></span>

<span data-ttu-id="760df-128">每個程式庫都可以包含一個或多個位置，而使用者可以使用 Windows 檔案總管流覽或搜尋這些位置。</span><span class="sxs-lookup"><span data-stu-id="760df-128">Each library can contain one or more locations that can be browsed or searched by a user using Windows Explorer.</span></span> <span data-ttu-id="760df-129">使用 [<searchConnectorDescription>](schema-library-searchconnectordescription.md) 容器元素中的元素，搜尋連接器會定義這些位置 [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) 。</span><span class="sxs-lookup"><span data-stu-id="760df-129">The locations are defined by search connectors using [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elements in a [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) container element.</span></span>

<span data-ttu-id="760df-130">程式庫可以有一組唯一的屬性，而且程式庫中的位置也可以有一組唯一的屬性。</span><span class="sxs-lookup"><span data-stu-id="760df-130">A library can have a unique set of properties, and locations in the library can also have unique sets of properties.</span></span> <span data-ttu-id="760df-131">這些屬性是在 [<property>](schema-library-property.md) 容器元素內的元素中定義 [<propertyStore>](schema-library-propertystore.md) 。</span><span class="sxs-lookup"><span data-stu-id="760df-131">These properties are defined in [<property>](schema-library-property.md) elements within a [<propertyStore>](schema-library-propertystore.md) container element.</span></span>

## <a name="example"></a><span data-ttu-id="760df-132">範例</span><span class="sxs-lookup"><span data-stu-id="760df-132">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="760df-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="760df-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="760df-134">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="760df-134">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="760df-135">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="760df-135">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

---
description: 選擇性 <propertyStore> 元素會指定以 XML 為基礎之 IPropertyStore 的位置，以儲存此搜尋連接器的開啟中繼資料。 這個元素沒有任何屬性，而且只有一個子項目。
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: 'propertyStore 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689843"
---
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="3af5c-104">propertyStore 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="3af5c-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="3af5c-105">選擇性 <propertyStore> 元素會指定以 XML 為基礎之 IPropertyStore 的位置，以儲存此搜尋連接器的開啟中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3af5c-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="3af5c-106">這個元素沒有任何屬性，而且只有一個子項目。</span><span class="sxs-lookup"><span data-stu-id="3af5c-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="3af5c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3af5c-107">Syntax</span></span>


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="3af5c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3af5c-108">Element Information</span></span>



| <span data-ttu-id="3af5c-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="3af5c-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="3af5c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3af5c-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3af5c-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="3af5c-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="3af5c-112">propertyStore (搜尋連接器架構) 的 property 元素 </span><span class="sxs-lookup"><span data-stu-id="3af5c-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="3af5c-113">範例</span><span class="sxs-lookup"><span data-stu-id="3af5c-113">Example</span></span>

<span data-ttu-id="3af5c-114">下列範例顯示 <propertyStore> 具有兩個元素的元素 <property> 。</span><span class="sxs-lookup"><span data-stu-id="3af5c-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 




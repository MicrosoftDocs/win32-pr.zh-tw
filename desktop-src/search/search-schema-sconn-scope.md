---
description: 選擇性 <scope> 元素會指定專案的集合 <scopeItem> ，這些專案會定義此特定搜尋連接器的範圍包含與排除專案。
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: '範圍元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971178"
---
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="eda0d-103">範圍元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="eda0d-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="eda0d-104">選擇性 <scope> 元素會指定專案的集合 <scopeItem> ，這些專案會定義此特定搜尋連接器的範圍包含與排除專案。</span><span class="sxs-lookup"><span data-stu-id="eda0d-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="eda0d-105">如果 <scope> 存在，則必須包含至少一個 <scopeItem> 元素。</span><span class="sxs-lookup"><span data-stu-id="eda0d-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="eda0d-106">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="eda0d-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda0d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eda0d-107">Syntax</span></span>


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="eda0d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="eda0d-108">Element Information</span></span>



| <span data-ttu-id="eda0d-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="eda0d-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="eda0d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eda0d-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="eda0d-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="eda0d-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="eda0d-112">[ScopeItem 元素 (搜尋連接器架構) ](search-schema-sconn-scopeitem.md)。</span><span class="sxs-lookup"><span data-stu-id="eda0d-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eda0d-113">備註</span><span class="sxs-lookup"><span data-stu-id="eda0d-113">Remarks</span></span>

<span data-ttu-id="eda0d-114">您 <scope> 可以使用和專案 <scopeItem> 來識別應該搜尋的位置，以及要從搜尋中排除哪些位置。</span><span class="sxs-lookup"><span data-stu-id="eda0d-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="eda0d-115">範例</span><span class="sxs-lookup"><span data-stu-id="eda0d-115">Example</span></span>

<span data-ttu-id="eda0d-116">下列範例顯示的搜尋範圍包含 C： \\ ExampleFolder 及其所有的子資料夾（c： \\ ExampleFolder ExcludeMe 除外） \\ 。</span><span class="sxs-lookup"><span data-stu-id="eda0d-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




---
description: <scopeItem>元素代表排除/包含範圍資料表中的單一專案。
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: 'scopeItem 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112376"
---
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="1621b-103">scopeItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="1621b-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="1621b-104"><scopeItem>元素代表排除/包含範圍資料表中的單一專案。</span><span class="sxs-lookup"><span data-stu-id="1621b-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="1621b-105"><scopeItem> 藉由新增可控制資料夾包含和排除的三個新元素、控制結果的深度，以及指定範圍的位置，來擴充標準 shellLinkType 類型。</span><span class="sxs-lookup"><span data-stu-id="1621b-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="1621b-106">如果 <scope> 元素存在，則需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="1621b-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="1621b-107">它有三個子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1621b-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1621b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1621b-108">Syntax</span></span>


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
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



## <a name="element-information"></a><span data-ttu-id="1621b-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1621b-109">Element Information</span></span>



| <span data-ttu-id="1621b-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="1621b-110">Parent Element</span></span>                                                           | <span data-ttu-id="1621b-111">子元素</span><span class="sxs-lookup"><span data-stu-id="1621b-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="1621b-112">範圍元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="1621b-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="1621b-113">[範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="1621b-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="1621b-114">[範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-depth.md)。</span><span class="sxs-lookup"><span data-stu-id="1621b-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="1621b-115">[scopeItem Url 元素 (搜尋連接器架構) ](search-schema-sconn-scope-url.md)。</span><span class="sxs-lookup"><span data-stu-id="1621b-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1621b-116">備註</span><span class="sxs-lookup"><span data-stu-id="1621b-116">Remarks</span></span>

<span data-ttu-id="1621b-117">您 <scope> 可以使用和專案 <scopeItem> 來識別應該搜尋的位置，以及要從搜尋中排除哪些位置。</span><span class="sxs-lookup"><span data-stu-id="1621b-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="1621b-118">範例</span><span class="sxs-lookup"><span data-stu-id="1621b-118">Example</span></span>

<span data-ttu-id="1621b-119">下列範例顯示的搜尋範圍包含 C： \\ ExampleFolder 及其所有的子資料夾（c： \\ ExampleFolder ExcludeMe 除外） \\ 。</span><span class="sxs-lookup"><span data-stu-id="1621b-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 




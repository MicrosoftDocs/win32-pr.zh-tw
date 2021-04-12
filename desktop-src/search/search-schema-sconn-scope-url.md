---
description: <url>元素指定代表搜尋連接器範圍的 URL。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: 'scopeItem url 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847803"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="d86f2-104">scopeItem url 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="d86f2-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="d86f2-105"><url>元素指定代表搜尋連接器範圍的 URL。</span><span class="sxs-lookup"><span data-stu-id="d86f2-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="d86f2-106">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="d86f2-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d86f2-107">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="d86f2-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d86f2-108">Element Information</span></span>



| <span data-ttu-id="d86f2-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="d86f2-109">Parent Element</span></span>                                                                   | <span data-ttu-id="d86f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d86f2-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="d86f2-111">scopeItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="d86f2-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="d86f2-112">備註</span><span class="sxs-lookup"><span data-stu-id="d86f2-112">Remarks</span></span>

<span data-ttu-id="d86f2-113">值可以是本機檔案系統路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="d86f2-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="d86f2-114">範例</span><span class="sxs-lookup"><span data-stu-id="d86f2-114">Example</span></span>

<span data-ttu-id="d86f2-115">下列範例顯示的搜尋範圍包含 C： \\ ExampleFolder 及其所有的子資料夾（c： \\ ExampleFolder ExcludeMe 除外） \\ 。</span><span class="sxs-lookup"><span data-stu-id="d86f2-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 




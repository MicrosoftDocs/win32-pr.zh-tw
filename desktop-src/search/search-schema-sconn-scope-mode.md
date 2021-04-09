---
description: <mode>元素指定是否應該在搜尋連接器的範圍中包含或排除 URL。 允許的值包括和排除。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: " (搜尋連接器架構) 的模式元素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689840"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="58339-105"> (搜尋連接器架構) 的模式元素</span><span class="sxs-lookup"><span data-stu-id="58339-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="58339-106"><mode>元素指定是否應該在搜尋連接器的範圍中包含或排除 URL。</span><span class="sxs-lookup"><span data-stu-id="58339-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="58339-107">允許的值有 `Include` 與 `Exclude`。</span><span class="sxs-lookup"><span data-stu-id="58339-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="58339-108">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="58339-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="58339-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58339-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
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



## <a name="element-information"></a><span data-ttu-id="58339-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="58339-110">Element Information</span></span>



| <span data-ttu-id="58339-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="58339-111">Parent Element</span></span>                                                                   | <span data-ttu-id="58339-112">子元素</span><span class="sxs-lookup"><span data-stu-id="58339-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="58339-113">scopeItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="58339-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="58339-114">備註</span><span class="sxs-lookup"><span data-stu-id="58339-114">Remarks</span></span>

<span data-ttu-id="58339-115">無法搜尋或流覽排除的範圍。</span><span class="sxs-lookup"><span data-stu-id="58339-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="58339-116">您可以嵌套 scopeItem Url。</span><span class="sxs-lookup"><span data-stu-id="58339-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="58339-117">例如，您可以包含父範圍及其所有子系（除了一個之外），方法是新增包含的父 URL、深度的深度值，以及排除子 URL。</span><span class="sxs-lookup"><span data-stu-id="58339-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="58339-118">範例</span><span class="sxs-lookup"><span data-stu-id="58339-118">Example</span></span>

<span data-ttu-id="58339-119">下列範例顯示的搜尋範圍包含 C： \\ ExampleFolder 及其所有的子資料夾（c： \\ ExampleFolder ExcludeMe 除外） \\ 。</span><span class="sxs-lookup"><span data-stu-id="58339-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




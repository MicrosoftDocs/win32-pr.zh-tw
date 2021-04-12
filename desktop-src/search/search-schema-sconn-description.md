---
description: 選擇性 <description> 元素指定此搜尋連接器的描述。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: " (搜尋連接器架構) 的 description 元素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318144"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="e1a5c-105"> (搜尋連接器架構) 的 description 元素</span><span class="sxs-lookup"><span data-stu-id="e1a5c-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="e1a5c-106">選擇性</span><span class="sxs-lookup"><span data-stu-id="e1a5c-106">The optional</span></span> <description> <span data-ttu-id="e1a5c-107">元素指定此搜尋連接器的描述。</span><span class="sxs-lookup"><span data-stu-id="e1a5c-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="e1a5c-108">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e1a5c-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1a5c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1a5c-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e1a5c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e1a5c-110">Element Information</span></span>



| <span data-ttu-id="e1a5c-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="e1a5c-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e1a5c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e1a5c-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e1a5c-113">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="e1a5c-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="e1a5c-114">備註</span><span class="sxs-lookup"><span data-stu-id="e1a5c-114">Remarks</span></span>

<span data-ttu-id="e1a5c-115">描述應該很容易使用，因為它可以在工具提示中使用。</span><span class="sxs-lookup"><span data-stu-id="e1a5c-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="e1a5c-116">範例</span><span class="sxs-lookup"><span data-stu-id="e1a5c-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 




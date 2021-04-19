---
description: 選擇性 <author> 元素會指定這個文件庫的作者。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: 'author 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970380"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="aeb88-104">author 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="aeb88-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="aeb88-105">選擇性 <author> 元素會指定這個文件庫的作者。</span><span class="sxs-lookup"><span data-stu-id="aeb88-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="aeb88-106">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="aeb88-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb88-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeb88-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="aeb88-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="aeb88-108">Element Information</span></span>



| <span data-ttu-id="aeb88-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="aeb88-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="aeb88-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aeb88-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="aeb88-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="aeb88-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="aeb88-112">範例</span><span class="sxs-lookup"><span data-stu-id="aeb88-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 




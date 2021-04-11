---
description: 選擇性的布林值 <isIndexed> 元素會指定是否要使用 Windows Search 4 或更高的) ，在本機或遠端 (搜尋連接器所描述的位置進行索引。
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: 'isIndexed 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112380"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="af259-103">isIndexed 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="af259-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="af259-104">選擇性的布林值 <isIndexed> 元素會指定是否要使用 Windows Search 4 或更高的) ，在本機或遠端 (搜尋連接器所描述的位置進行索引。</span><span class="sxs-lookup"><span data-stu-id="af259-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="af259-105">本機資料夾的預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="af259-105">The default value is true for local folders.</span></span> <span data-ttu-id="af259-106">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="af259-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="af259-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af259-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="af259-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="af259-108">Element Information</span></span>



| <span data-ttu-id="af259-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="af259-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="af259-110">子元素</span><span class="sxs-lookup"><span data-stu-id="af259-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="af259-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="af259-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="af259-112">範例</span><span class="sxs-lookup"><span data-stu-id="af259-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 




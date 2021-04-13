---
description: 布林值 <isSearchOnlyItem> 元素會指定搜尋提供者是否除了搜尋模式之外，還支援瀏覽模式。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: 'isSearchOnlyItem 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511080"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="22245-104">isSearchOnlyItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="22245-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="22245-105">布林值 <isSearchOnlyItem> 元素會指定搜尋提供者是否除了搜尋模式之外，還支援瀏覽模式。</span><span class="sxs-lookup"><span data-stu-id="22245-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="22245-106">這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="22245-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="22245-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22245-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="22245-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="22245-108">Element Information</span></span>



| <span data-ttu-id="22245-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="22245-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="22245-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22245-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="22245-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="22245-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="22245-112">備註</span><span class="sxs-lookup"><span data-stu-id="22245-112">Remarks</span></span>

<span data-ttu-id="22245-113">此值 `true` 表示使用者無法流覽搜尋連接器位置。</span><span class="sxs-lookup"><span data-stu-id="22245-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="22245-114">此值 `false` 表示使用者可以流覽搜尋連接器位置。</span><span class="sxs-lookup"><span data-stu-id="22245-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="22245-115">範例</span><span class="sxs-lookup"><span data-stu-id="22245-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 




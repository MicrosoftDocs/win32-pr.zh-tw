---
description: 布林值 <supportsAdvancedQuerySyntax> 元素會指定搜尋提供者是否支援 Advanced 查詢語法。 預設為 false。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: 'supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973427"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="1d15d-105">supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="1d15d-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="1d15d-106">布林值 <supportsAdvancedQuerySyntax> 元素會指定搜尋提供者是否支援 [Advanced 查詢語法](-search-3x-advancedquerysyntax.md)。</span><span class="sxs-lookup"><span data-stu-id="1d15d-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="1d15d-107">預設為 false。</span><span class="sxs-lookup"><span data-stu-id="1d15d-107">The default is false.</span></span> <span data-ttu-id="1d15d-108">這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1d15d-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d15d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d15d-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="1d15d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1d15d-110">Element Information</span></span>



| <span data-ttu-id="1d15d-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="1d15d-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="1d15d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1d15d-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="1d15d-113">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="1d15d-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="1d15d-114">備註</span><span class="sxs-lookup"><span data-stu-id="1d15d-114">Remarks</span></span>

<span data-ttu-id="1d15d-115">此值 `true` 表示搜尋提供者支援在搜尋查詢中傳送的 Advanced Query 語法。</span><span class="sxs-lookup"><span data-stu-id="1d15d-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="1d15d-116">範例</span><span class="sxs-lookup"><span data-stu-id="1d15d-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 




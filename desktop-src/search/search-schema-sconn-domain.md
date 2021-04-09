---
description: 選擇性 <domain> 元素會指定此搜尋連接器所使用之搜尋服務的 URL。 它會顯示在詳細資料窗格中。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: '網域元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847805"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="0fd0e-105">網域元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="0fd0e-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="0fd0e-106">選擇性 <domain> 元素會指定此搜尋連接器所使用之搜尋服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="0fd0e-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="0fd0e-107">它會顯示在詳細資料窗格中。</span><span class="sxs-lookup"><span data-stu-id="0fd0e-107">It is displayed in the details pane.</span></span> <span data-ttu-id="0fd0e-108">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="0fd0e-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd0e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd0e-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="0fd0e-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0fd0e-110">Element Information</span></span>



| <span data-ttu-id="0fd0e-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="0fd0e-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="0fd0e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0fd0e-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="0fd0e-113">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="0fd0e-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="0fd0e-114">備註</span><span class="sxs-lookup"><span data-stu-id="0fd0e-114">Remarks</span></span>

<span data-ttu-id="0fd0e-115">URL 應該是搜尋提供者的最上層網域。</span><span class="sxs-lookup"><span data-stu-id="0fd0e-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="0fd0e-116">例如： https://www.example.com 。</span><span class="sxs-lookup"><span data-stu-id="0fd0e-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="0fd0e-117">範例</span><span class="sxs-lookup"><span data-stu-id="0fd0e-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 




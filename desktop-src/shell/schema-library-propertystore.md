---
description: <propertyStore>元素會指定這個程式庫所使用的一或多個屬性集合。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: 'propertyStore 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973532"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="920c5-104">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="920c5-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="920c5-105"><propertyStore>元素會指定這個程式庫所使用的一或多個屬性集合。</span><span class="sxs-lookup"><span data-stu-id="920c5-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="920c5-106">這個元素是選擇性的，且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="920c5-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="920c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="920c5-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="920c5-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="920c5-108">Element Information</span></span>



| <span data-ttu-id="920c5-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="920c5-109">Parent Element</span></span>                                                               | <span data-ttu-id="920c5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="920c5-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="920c5-111">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="920c5-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="920c5-112">property 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="920c5-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="920c5-113">備註</span><span class="sxs-lookup"><span data-stu-id="920c5-113">Remarks</span></span>

<span data-ttu-id="920c5-114"><propertyStore>元素可以有一或多 <property> 個子項目。</span><span class="sxs-lookup"><span data-stu-id="920c5-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="920c5-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="920c5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920c5-116">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="920c5-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="920c5-117">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="920c5-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

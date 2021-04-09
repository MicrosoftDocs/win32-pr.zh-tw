---
description: 選擇性 <dateCreated> 元素會使用 ISO 8601 標準來識別建立此搜尋連接器的日期和時間。 它沒有任何子項目，而且沒有任何屬性。
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: 'dateCreated 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689848"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="74049-104">dateCreated 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="74049-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="74049-105">選擇性 <dateCreated> 元素會使用 ISO 8601 標準來識別建立此搜尋連接器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="74049-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="74049-106">它沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="74049-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="74049-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74049-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="74049-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="74049-108">Element Information</span></span>



| <span data-ttu-id="74049-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="74049-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="74049-110">子元素</span><span class="sxs-lookup"><span data-stu-id="74049-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="74049-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="74049-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="74049-112">備註</span><span class="sxs-lookup"><span data-stu-id="74049-112">Remarks</span></span>

<span data-ttu-id="74049-113">此元素的值格式會遵循 ISO 8601 標準。</span><span class="sxs-lookup"><span data-stu-id="74049-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="74049-114">常見的用法是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="74049-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="74049-115">\[YYYY \] - \[ MM \] - \[ DD \] T \[ hh \] ： \[ mm \] ： \[ ss \] ± \[ hh \] ： \[ MM \] ( "1981-04-05T14：30： 30-05： 00" ) </span><span class="sxs-lookup"><span data-stu-id="74049-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="74049-116">\[YYYY \] \[ mm \] \[ DD \] T \[ HH \] \[ MM \] \[ ss \] Z ( "19810405T193030Z" ) </span><span class="sxs-lookup"><span data-stu-id="74049-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="74049-117">範例</span><span class="sxs-lookup"><span data-stu-id="74049-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 




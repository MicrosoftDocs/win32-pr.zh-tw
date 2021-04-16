---
description: 選擇性 <iconReference> 元素會指定這個位置的自訂圖示。 此元素沒有屬性和子項目。
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: 'iconReference 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511083"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="6e598-104">iconReference 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="6e598-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="6e598-105">選擇性 <iconReference> 元素會指定這個位置的自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="6e598-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="6e598-106">此元素沒有屬性和子項目。</span><span class="sxs-lookup"><span data-stu-id="6e598-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e598-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e598-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="6e598-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6e598-108">Element Information</span></span>



| <span data-ttu-id="6e598-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="6e598-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="6e598-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6e598-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6e598-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="6e598-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6e598-112">備註</span><span class="sxs-lookup"><span data-stu-id="6e598-112">Remarks</span></span>

<span data-ttu-id="6e598-113">參考的格式必須以適合 [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) 函式的形式指定： (例如， <dll file name> <icon index>) 。</span><span class="sxs-lookup"><span data-stu-id="6e598-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="6e598-114">範例</span><span class="sxs-lookup"><span data-stu-id="6e598-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 

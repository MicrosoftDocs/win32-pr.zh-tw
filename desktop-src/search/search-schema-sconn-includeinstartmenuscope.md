---
description: 選擇性的布林值 <includeInStartMenuScope> 元素會指定是否應將此搜尋連接器包含在 [開始] 功能表搜尋範圍內。
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: 'includeInStartMenuScope 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986308"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="a82d4-103">includeInStartMenuScope 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="a82d4-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="a82d4-104">選擇性的布林值 <includeInStartMenuScope> 元素會指定是否應將此搜尋連接器包含在 [開始] 功能表搜尋範圍內。</span><span class="sxs-lookup"><span data-stu-id="a82d4-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="a82d4-105">使用檔案系統作為資料來源之搜尋連接器的預設值是 true，而針對屬性處理常式所使用的搜尋連接器，則預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="a82d4-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="a82d4-106">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a82d4-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a82d4-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a82d4-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a82d4-108">Element Information</span></span>



| <span data-ttu-id="a82d4-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="a82d4-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a82d4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a82d4-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a82d4-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="a82d4-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a82d4-112">備註</span><span class="sxs-lookup"><span data-stu-id="a82d4-112">Remarks</span></span>

<span data-ttu-id="a82d4-113">如果您在 [開始] 功能表範圍中包含搜尋連接器，使用者可以從 [開始] 功能表的 [搜尋] 方塊中搜尋您的位置。</span><span class="sxs-lookup"><span data-stu-id="a82d4-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="a82d4-114">範例</span><span class="sxs-lookup"><span data-stu-id="a82d4-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 




---
description: 選擇性的布林值 <isDefaultNonOwnerSaveLocation> 元素會指定當來自家庭電腦上另一部電腦的使用者選擇儲存專案時，是否應使用搜尋連接器中所述的位置做為預設的儲存位置。
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: 'isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966681"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="352b5-103">isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="352b5-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="352b5-104">選擇性的布林值 <isDefaultNonOwnerSaveLocation> 元素會指定當來自家庭電腦上另一部電腦的使用者選擇儲存專案時，是否應使用搜尋連接器中所述的位置做為預設的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="352b5-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="352b5-105">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="352b5-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="352b5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="352b5-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="352b5-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="352b5-107">Element Information</span></span>



| <span data-ttu-id="352b5-108">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="352b5-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="352b5-109">子元素</span><span class="sxs-lookup"><span data-stu-id="352b5-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="352b5-110">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="352b5-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="352b5-111">備註</span><span class="sxs-lookup"><span data-stu-id="352b5-111">Remarks</span></span>

<span data-ttu-id="352b5-112">若為 true，當使用者從家用電腦中的另一部電腦選擇儲存專案時，Windows 檔案總管會將專案儲存至專案中指定的位置 <simpleLocation> 。</span><span class="sxs-lookup"><span data-stu-id="352b5-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="352b5-113">範例</span><span class="sxs-lookup"><span data-stu-id="352b5-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 




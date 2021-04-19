---
description: 這個選擇性 <templateInfo> 元素會指定資料夾類型，以顯示透過此搜尋連接器的查詢結果。 這個元素沒有任何屬性，而且只有一個強制子系。
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: 'templateInfo 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970962"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="e97f2-104">templateInfo 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="e97f2-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="e97f2-105">這個選擇性 <templateInfo> 元素會指定資料夾類型，以顯示透過此搜尋連接器的查詢結果。</span><span class="sxs-lookup"><span data-stu-id="e97f2-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="e97f2-106">這個元素沒有任何屬性，而且只有一個強制子系。</span><span class="sxs-lookup"><span data-stu-id="e97f2-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="e97f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e97f2-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e97f2-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e97f2-108">Element Information</span></span>



| <span data-ttu-id="e97f2-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="e97f2-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e97f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e97f2-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e97f2-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="e97f2-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="e97f2-112">folderType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="e97f2-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="e97f2-113">備註</span><span class="sxs-lookup"><span data-stu-id="e97f2-113">Remarks</span></span>

<span data-ttu-id="e97f2-114">如果您未在元素中指定特定的資料夾類型 <templateInfo> ，Windows 會使用一般搜尋連接器資料夾類型 {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}。</span><span class="sxs-lookup"><span data-stu-id="e97f2-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="e97f2-115">TemplateInfo 元素範例</span><span class="sxs-lookup"><span data-stu-id="e97f2-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 




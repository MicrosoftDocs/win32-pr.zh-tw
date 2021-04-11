---
description: <depth>元素會指定搜尋連接器的範圍是否應包含子 url。 允許的值為 Deep 和淺層。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: '搜尋連接器架構 (的深度元素) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943276"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="f3946-105">搜尋連接器架構 (的深度元素) </span><span class="sxs-lookup"><span data-stu-id="f3946-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="f3946-106"><depth>元素會指定搜尋連接器的範圍是否應包含子 url。</span><span class="sxs-lookup"><span data-stu-id="f3946-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="f3946-107">允許的值有 `Deep` 與 `Shallow`。</span><span class="sxs-lookup"><span data-stu-id="f3946-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="f3946-108">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f3946-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3946-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3946-109">Syntax</span></span>


```
<!-- depth -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f3946-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3946-110">Element Information</span></span>



| <span data-ttu-id="f3946-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="f3946-111">Parent Element</span></span>                                                                   | <span data-ttu-id="f3946-112">子元素</span><span class="sxs-lookup"><span data-stu-id="f3946-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f3946-113">scopeItem 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="f3946-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="f3946-114">備註</span><span class="sxs-lookup"><span data-stu-id="f3946-114">Remarks</span></span>

<span data-ttu-id="f3946-115">如果深度較深，使用者可以流覽或搜尋 scopeItem 的 URL 層級或任何子 Url 內的專案。</span><span class="sxs-lookup"><span data-stu-id="f3946-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="f3946-116">範例</span><span class="sxs-lookup"><span data-stu-id="f3946-116">Example</span></span>

<span data-ttu-id="f3946-117">下列範例顯示的搜尋範圍包含 C： \\ FolderA 及其所有的子資料夾和 C： FolderB， \\ 但不包含任何子資料夾。</span><span class="sxs-lookup"><span data-stu-id="f3946-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




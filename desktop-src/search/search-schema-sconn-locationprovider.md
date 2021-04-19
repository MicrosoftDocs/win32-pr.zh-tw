---
description: 選擇性 <locationProvider> 元素會指定 web 服務提供者搜尋連接器要使用的搜尋提供者。 這個元素包含一個強制屬性和一個選擇性的子項目。
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: 'locationProvider 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972004"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="7d262-104">locationProvider 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="7d262-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="7d262-105">選擇性 <locationProvider> 元素會指定 web 服務提供者搜尋連接器要使用的搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="7d262-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="7d262-106">這個元素包含一個強制屬性和一個選擇性的子項目。</span><span class="sxs-lookup"><span data-stu-id="7d262-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d262-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d262-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="7d262-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7d262-108">Element Information</span></span>



| <span data-ttu-id="7d262-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="7d262-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="7d262-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7d262-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d262-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="7d262-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="7d262-112">propertyBag 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="7d262-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="7d262-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7d262-113">Attributes</span></span>



| <span data-ttu-id="7d262-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7d262-114">Attribute</span></span> | <span data-ttu-id="7d262-115">描述</span><span class="sxs-lookup"><span data-stu-id="7d262-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="7d262-116">必要。</span><span class="sxs-lookup"><span data-stu-id="7d262-116">Required.</span></span> <span data-ttu-id="7d262-117">搜尋提供者 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d262-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="7d262-118">codebase</span><span class="sxs-lookup"><span data-stu-id="7d262-118">codebase</span></span>  | <span data-ttu-id="7d262-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7d262-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="7d262-120">備註</span><span class="sxs-lookup"><span data-stu-id="7d262-120">Remarks</span></span>

<span data-ttu-id="7d262-121">@clsidOpenSearch 提供者的屬性值為 {48E277F6-4E74-4cd6-BA6F-FA4F42898223}。</span><span class="sxs-lookup"><span data-stu-id="7d262-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="7d262-122">以檔案系統和通訊協定處理常式為基礎的搜尋連接器可以 [<simpleLocation>](search-schema-sconn-simplelocation.md) 改用元素。</span><span class="sxs-lookup"><span data-stu-id="7d262-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="7d262-123">如果 <locationProvider> 存在， <simpleLocation> 則搜尋連接器描述中不能有元素。</span><span class="sxs-lookup"><span data-stu-id="7d262-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="7d262-124">LocationProvider 元素範例</span><span class="sxs-lookup"><span data-stu-id="7d262-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 




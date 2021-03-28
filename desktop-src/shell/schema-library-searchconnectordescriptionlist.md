---
description: 這個 <searchConnectorDescriptionList> 元素包含的搜尋連接器清單，會對應到此程式庫中包含的位置。 每個搜尋連接器都是由 <searchConnectorDescription> 元素所定義。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: 'searchConnectorDescriptionList 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973604"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="39375-105">searchConnectorDescriptionList 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="39375-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="39375-106">這個 <searchConnectorDescriptionList> 元素包含的搜尋連接器清單，會對應到此程式庫中包含的位置。</span><span class="sxs-lookup"><span data-stu-id="39375-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="39375-107">每個搜尋連接器都是由 <searchConnectorDescription> 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="39375-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="39375-108">這個元素是選擇性的，且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="39375-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="39375-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="39375-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="39375-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="39375-110">Element Information</span></span>



| <span data-ttu-id="39375-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="39375-111">Parent Element</span></span>                                                               | <span data-ttu-id="39375-112">子元素</span><span class="sxs-lookup"><span data-stu-id="39375-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39375-113">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="39375-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="39375-114">searchConnectorDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="39375-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="39375-115">備註</span><span class="sxs-lookup"><span data-stu-id="39375-115">Remarks</span></span>

<span data-ttu-id="39375-116">Windows 同盟搜尋和通訊協定處理常式範圍的搜尋連接器不能包含在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="39375-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39375-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="39375-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39375-118">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="39375-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="39375-119">[搜尋連接器描述架構](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39375-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 

---
description: <version>元素指定此程式庫的內容版本。 此元素沒有屬性和子項目。
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: 'version 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972296"
---
# <a name="version-element-library-schema"></a><span data-ttu-id="bb943-104">version 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="bb943-104">version Element (Library Schema)</span></span>

<span data-ttu-id="bb943-105"><version>元素指定此程式庫的內容版本。</span><span class="sxs-lookup"><span data-stu-id="bb943-105">The <version> element specifies the content version of this library.</span></span> <span data-ttu-id="bb943-106">此元素沒有屬性和子項目。</span><span class="sxs-lookup"><span data-stu-id="bb943-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb943-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb943-107">Syntax</span></span>

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a><span data-ttu-id="bb943-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bb943-108">Element Information</span></span>



| <span data-ttu-id="bb943-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="bb943-109">Parent Element</span></span>                                                               | <span data-ttu-id="bb943-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bb943-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="bb943-111">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="bb943-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | <span data-ttu-id="bb943-112">無</span><span class="sxs-lookup"><span data-stu-id="bb943-112">None</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="bb943-113">備註</span><span class="sxs-lookup"><span data-stu-id="bb943-113">Remarks</span></span>

<span data-ttu-id="bb943-114">程式庫的內容版本與程式庫的檔案格式不同 (library \* -ms) 版本。</span><span class="sxs-lookup"><span data-stu-id="bb943-114">The content version of the library is different from the library's file format (\*.library-ms) version.</span></span> <span data-ttu-id="bb943-115">程式庫的檔案格式版本是在 [命名空間](library-schema-entry.md)中指定。</span><span class="sxs-lookup"><span data-stu-id="bb943-115">The library's file format version is specified in the [namespace](library-schema-entry.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb943-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb943-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb943-117">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="bb943-117">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="bb943-118">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="bb943-118">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

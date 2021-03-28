---
description: <iconReference>元素指定此程式庫的自訂圖示。 這個元素是選擇性的，且沒有任何屬性或子項目。
title: 'iconReference 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991298"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="a9902-104">iconReference 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="a9902-105"><iconReference>元素指定此程式庫的自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="a9902-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="a9902-106">這個元素是選擇性的，且沒有任何屬性或子項目。</span><span class="sxs-lookup"><span data-stu-id="a9902-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9902-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9902-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="a9902-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a9902-108">Element Information</span></span>



| <span data-ttu-id="a9902-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="a9902-109">Parent Element</span></span>                                                               | <span data-ttu-id="a9902-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a9902-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a9902-111">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a9902-112">備註</span><span class="sxs-lookup"><span data-stu-id="a9902-112">Remarks</span></span>

<span data-ttu-id="a9902-113">您必須在適合 [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) 函數的表單中指定圖示參考。</span><span class="sxs-lookup"><span data-stu-id="a9902-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="a9902-114">例如：`ModuleFileName,IconResourceIndex`。</span><span class="sxs-lookup"><span data-stu-id="a9902-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9902-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9902-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9902-116">folderType 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="a9902-117">isLibraryPinned 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="a9902-118">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="a9902-119"> (程式庫架構的 name 元素) </span><span class="sxs-lookup"><span data-stu-id="a9902-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="a9902-120">ownerSID 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="a9902-121">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="a9902-122">searchConnectorDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="a9902-123">searchConnectorDescriptionList 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="a9902-124">templateInfo 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="a9902-125">version 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="a9902-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 




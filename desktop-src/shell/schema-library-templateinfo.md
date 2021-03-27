---
description: 專案 <templateInfo> 是 folderType 專案的容器，可指定資料夾類型，以顯示透過此程式庫查詢的結果。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: 'templateInfo 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512197"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="53038-104">templateInfo 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="53038-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="53038-105">專案 <templateInfo> 是 [folderType](schema-library-foldertype.md) 專案的容器，可指定資料夾類型，以顯示透過此程式庫查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="53038-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="53038-106">這個元素是選擇性的，且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="53038-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="53038-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53038-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="53038-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="53038-108">Element Information</span></span>



| <span data-ttu-id="53038-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="53038-109">Parent Element</span></span>                                                               | <span data-ttu-id="53038-110">子元素</span><span class="sxs-lookup"><span data-stu-id="53038-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="53038-111">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="53038-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="53038-112">folderType 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="53038-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="53038-113">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="53038-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="53038-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="53038-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53038-115">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="53038-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="53038-116">[搜尋連接器描述架構](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53038-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 

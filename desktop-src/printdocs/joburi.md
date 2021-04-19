---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981948"
---
# <a name="joburi"></a><span data-ttu-id="b5729-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="b5729-104">JobURI</span></span>

<span data-ttu-id="b5729-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="b5729-105">This topic is not current.</span></span> <span data-ttu-id="b5729-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="b5729-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b5729-107">為檔指定 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="b5729-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="b5729-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b5729-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b5729-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b5729-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b5729-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b5729-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b5729-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b5729-111">Element Information</span></span>



| <span data-ttu-id="b5729-112">Name</span><span class="sxs-lookup"><span data-stu-id="b5729-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="b5729-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="b5729-113">Element Type</span></span> <br/>   | <span data-ttu-id="b5729-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b5729-114">Property</span></span><br/> |
| <span data-ttu-id="b5729-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="b5729-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b5729-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="b5729-116">Job</span></span><br/>      |
| <span data-ttu-id="b5729-117">注意</span><span class="sxs-lookup"><span data-stu-id="b5729-117">Notes</span></span> <br/>          | <span data-ttu-id="b5729-118">None</span><span class="sxs-lookup"><span data-stu-id="b5729-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b5729-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b5729-119">Structural Content</span></span>

<span data-ttu-id="b5729-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="b5729-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b5729-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="b5729-121">Structure Variables</span></span>

<span data-ttu-id="b5729-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="b5729-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b5729-123">Name</span><span class="sxs-lookup"><span data-stu-id="b5729-123">Name</span></span>                       | <span data-ttu-id="b5729-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="b5729-124">Data type</span></span>         | <span data-ttu-id="b5729-125">單位</span><span class="sxs-lookup"><span data-stu-id="b5729-125">Unit</span></span> | <span data-ttu-id="b5729-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="b5729-126">Supported values</span></span> | <span data-ttu-id="b5729-127">總結</span><span class="sxs-lookup"><span data-stu-id="b5729-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b5729-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="b5729-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="b5729-129">字串</span><span class="sxs-lookup"><span data-stu-id="b5729-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b5729-130">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b5729-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b5729-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5729-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5729-132">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="b5729-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





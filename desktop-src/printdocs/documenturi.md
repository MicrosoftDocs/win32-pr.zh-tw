---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d339b1b469f276492f7989b0ed7951ca1edad8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997065"
---
# <a name="documenturi"></a><span data-ttu-id="1b0c5-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="1b0c5-104">DocumentURI</span></span>

<span data-ttu-id="1b0c5-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-105">This topic is not current.</span></span> <span data-ttu-id="1b0c5-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1b0c5-107">為檔指定 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="1b0c5-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1b0c5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1b0c5-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1b0c5-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1b0c5-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1b0c5-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1b0c5-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1b0c5-111">Element Information</span></span>



| <span data-ttu-id="1b0c5-112">Name</span><span class="sxs-lookup"><span data-stu-id="1b0c5-112">Name</span></span> | <span data-ttu-id="1b0c5-113">值</span><span class="sxs-lookup"><span data-stu-id="1b0c5-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="1b0c5-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="1b0c5-114">Element Type</span></span> <br/>   | <span data-ttu-id="1b0c5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1b0c5-115">Property</span></span><br/> |
| <span data-ttu-id="1b0c5-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1b0c5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1b0c5-117">文件</span><span class="sxs-lookup"><span data-stu-id="1b0c5-117">Document</span></span><br/> |
| <span data-ttu-id="1b0c5-118">注意</span><span class="sxs-lookup"><span data-stu-id="1b0c5-118">Notes</span></span> <br/>          | <span data-ttu-id="1b0c5-119">None</span><span class="sxs-lookup"><span data-stu-id="1b0c5-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="1b0c5-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1b0c5-120">Structural Content</span></span>

<span data-ttu-id="1b0c5-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="1b0c5-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="1b0c5-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="1b0c5-122">Structure Variables</span></span>

<span data-ttu-id="1b0c5-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1b0c5-124">Name</span><span class="sxs-lookup"><span data-stu-id="1b0c5-124">Name</span></span>                            | <span data-ttu-id="1b0c5-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="1b0c5-125">Data type</span></span>         | <span data-ttu-id="1b0c5-126">單位</span><span class="sxs-lookup"><span data-stu-id="1b0c5-126">Unit</span></span> | <span data-ttu-id="1b0c5-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="1b0c5-127">Supported values</span></span> | <span data-ttu-id="1b0c5-128">總結</span><span class="sxs-lookup"><span data-stu-id="1b0c5-128">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="1b0c5-129">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="1b0c5-129">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="1b0c5-130">字串</span><span class="sxs-lookup"><span data-stu-id="1b0c5-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1b0c5-131">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1b0c5-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="1b0c5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b0c5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b0c5-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1b0c5-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





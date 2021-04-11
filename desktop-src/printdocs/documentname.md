---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: System.drawing.printing.printdocument.documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5f087744f40111f176e6797dab356c5d290d8f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103696310"
---
# <a name="documentname"></a><span data-ttu-id="b1dc5-104">System.drawing.printing.printdocument.documentname</span><span class="sxs-lookup"><span data-stu-id="b1dc5-104">DocumentName</span></span>

<span data-ttu-id="b1dc5-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="b1dc5-105">This topic is not current.</span></span> <span data-ttu-id="b1dc5-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="b1dc5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b1dc5-107">指定檔的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="b1dc5-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="b1dc5-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b1dc5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b1dc5-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b1dc5-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b1dc5-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b1dc5-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b1dc5-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b1dc5-111">Element Information</span></span>



| <span data-ttu-id="b1dc5-112">Name</span><span class="sxs-lookup"><span data-stu-id="b1dc5-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="b1dc5-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="b1dc5-113">Element Type</span></span> <br/>   | <span data-ttu-id="b1dc5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b1dc5-114">Property</span></span><br/> |
| <span data-ttu-id="b1dc5-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="b1dc5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b1dc5-116">文件</span><span class="sxs-lookup"><span data-stu-id="b1dc5-116">Document</span></span><br/> |
| <span data-ttu-id="b1dc5-117">注意</span><span class="sxs-lookup"><span data-stu-id="b1dc5-117">Notes</span></span> <br/>          | <span data-ttu-id="b1dc5-118">None</span><span class="sxs-lookup"><span data-stu-id="b1dc5-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b1dc5-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b1dc5-119">Structural Content</span></span>

<span data-ttu-id="b1dc5-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="b1dc5-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="b1dc5-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="b1dc5-121">Structure Variables</span></span>

<span data-ttu-id="b1dc5-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="b1dc5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b1dc5-123">Name</span><span class="sxs-lookup"><span data-stu-id="b1dc5-123">Name</span></span>                             | <span data-ttu-id="b1dc5-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="b1dc5-124">Data type</span></span>         | <span data-ttu-id="b1dc5-125">單位</span><span class="sxs-lookup"><span data-stu-id="b1dc5-125">Unit</span></span> | <span data-ttu-id="b1dc5-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="b1dc5-126">Supported values</span></span> | <span data-ttu-id="b1dc5-127">總結</span><span class="sxs-lookup"><span data-stu-id="b1dc5-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b1dc5-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="b1dc5-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="b1dc5-129">字串</span><span class="sxs-lookup"><span data-stu-id="b1dc5-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b1dc5-130">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b1dc5-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b1dc5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1dc5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1dc5-132">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="b1dc5-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





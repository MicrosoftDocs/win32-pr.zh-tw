---
description: 瞭解 System.drawing.printing.printdocument.documentname 屬性，它會指定檔的描述性名稱。
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: System.drawing.printing.printdocument.documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409271"
---
# <a name="documentname"></a><span data-ttu-id="185d0-103">System.drawing.printing.printdocument.documentname</span><span class="sxs-lookup"><span data-stu-id="185d0-103">DocumentName</span></span>

<span data-ttu-id="185d0-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="185d0-104">This topic is not current.</span></span> <span data-ttu-id="185d0-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="185d0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="185d0-106">指定檔的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="185d0-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="185d0-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="185d0-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="185d0-108">結構化內容</span><span class="sxs-lookup"><span data-stu-id="185d0-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="185d0-109">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="185d0-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="185d0-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="185d0-110">Element Information</span></span>



| <span data-ttu-id="185d0-111">Name</span><span class="sxs-lookup"><span data-stu-id="185d0-111">Name</span></span> | <span data-ttu-id="185d0-112">值</span><span class="sxs-lookup"><span data-stu-id="185d0-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="185d0-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="185d0-113">Element Type</span></span> <br/>   | <span data-ttu-id="185d0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="185d0-114">Property</span></span><br/> |
| <span data-ttu-id="185d0-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="185d0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="185d0-116">文件</span><span class="sxs-lookup"><span data-stu-id="185d0-116">Document</span></span><br/> |
| <span data-ttu-id="185d0-117">注意</span><span class="sxs-lookup"><span data-stu-id="185d0-117">Notes</span></span> <br/>          | <span data-ttu-id="185d0-118">None</span><span class="sxs-lookup"><span data-stu-id="185d0-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="185d0-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="185d0-119">Structural Content</span></span>

<span data-ttu-id="185d0-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="185d0-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="185d0-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="185d0-121">Structure Variables</span></span>

<span data-ttu-id="185d0-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="185d0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="185d0-123">Name</span><span class="sxs-lookup"><span data-stu-id="185d0-123">Name</span></span>                             | <span data-ttu-id="185d0-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="185d0-124">Data type</span></span>         | <span data-ttu-id="185d0-125">單位</span><span class="sxs-lookup"><span data-stu-id="185d0-125">Unit</span></span> | <span data-ttu-id="185d0-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="185d0-126">Supported values</span></span> | <span data-ttu-id="185d0-127">總結</span><span class="sxs-lookup"><span data-stu-id="185d0-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="185d0-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="185d0-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="185d0-129">string</span><span class="sxs-lookup"><span data-stu-id="185d0-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="185d0-130">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="185d0-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="185d0-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="185d0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="185d0-132">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="185d0-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





---
description: 取得 DocumentURI 屬性的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548806"
---
# <a name="documenturi"></a><span data-ttu-id="2c159-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="2c159-105">DocumentURI</span></span>

<span data-ttu-id="2c159-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2c159-106">This topic is not current.</span></span> <span data-ttu-id="2c159-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2c159-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c159-108">為檔指定 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="2c159-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="2c159-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2c159-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2c159-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2c159-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2c159-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2c159-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2c159-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2c159-112">Element Information</span></span>



| <span data-ttu-id="2c159-113">Name</span><span class="sxs-lookup"><span data-stu-id="2c159-113">Name</span></span> | <span data-ttu-id="2c159-114">值</span><span class="sxs-lookup"><span data-stu-id="2c159-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2c159-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="2c159-115">Element Type</span></span> <br/>   | <span data-ttu-id="2c159-116">屬性</span><span class="sxs-lookup"><span data-stu-id="2c159-116">Property</span></span><br/> |
| <span data-ttu-id="2c159-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2c159-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2c159-118">文件</span><span class="sxs-lookup"><span data-stu-id="2c159-118">Document</span></span><br/> |
| <span data-ttu-id="2c159-119">注意</span><span class="sxs-lookup"><span data-stu-id="2c159-119">Notes</span></span> <br/>          | <span data-ttu-id="2c159-120">None</span><span class="sxs-lookup"><span data-stu-id="2c159-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2c159-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2c159-121">Structural Content</span></span>

<span data-ttu-id="2c159-122">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="2c159-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2c159-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="2c159-123">Structure Variables</span></span>

<span data-ttu-id="2c159-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2c159-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2c159-125">Name</span><span class="sxs-lookup"><span data-stu-id="2c159-125">Name</span></span>                            | <span data-ttu-id="2c159-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="2c159-126">Data type</span></span>         | <span data-ttu-id="2c159-127">單位</span><span class="sxs-lookup"><span data-stu-id="2c159-127">Unit</span></span> | <span data-ttu-id="2c159-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="2c159-128">Supported values</span></span> | <span data-ttu-id="2c159-129">摘要</span><span class="sxs-lookup"><span data-stu-id="2c159-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="2c159-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="2c159-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="2c159-131">string</span><span class="sxs-lookup"><span data-stu-id="2c159-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2c159-132">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2c159-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2c159-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c159-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c159-134">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2c159-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





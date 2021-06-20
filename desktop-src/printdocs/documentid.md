---
description: 瞭解 DocumentID 元素，它會指定檔的唯一識別碼。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b267fead0322351cde396bf2eb6d0efa8c523f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409281"
---
# <a name="documentid"></a><span data-ttu-id="3e0c2-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="3e0c2-104">DocumentID</span></span>

<span data-ttu-id="3e0c2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3e0c2-105">This topic is not current.</span></span> <span data-ttu-id="3e0c2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3e0c2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3e0c2-107">指定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e0c2-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="3e0c2-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3e0c2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3e0c2-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3e0c2-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3e0c2-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3e0c2-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3e0c2-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3e0c2-111">Element Information</span></span>



| <span data-ttu-id="3e0c2-112">Name</span><span class="sxs-lookup"><span data-stu-id="3e0c2-112">Name</span></span> | <span data-ttu-id="3e0c2-113">值</span><span class="sxs-lookup"><span data-stu-id="3e0c2-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3e0c2-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="3e0c2-114">Element Type</span></span> <br/>   | <span data-ttu-id="3e0c2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3e0c2-115">Property</span></span><br/> |
| <span data-ttu-id="3e0c2-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3e0c2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3e0c2-117">文件</span><span class="sxs-lookup"><span data-stu-id="3e0c2-117">Document</span></span><br/> |
| <span data-ttu-id="3e0c2-118">注意</span><span class="sxs-lookup"><span data-stu-id="3e0c2-118">Notes</span></span> <br/>          | <span data-ttu-id="3e0c2-119">None</span><span class="sxs-lookup"><span data-stu-id="3e0c2-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3e0c2-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3e0c2-120">Structural Content</span></span>

<span data-ttu-id="3e0c2-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="3e0c2-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="3e0c2-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="3e0c2-122">Structure Variables</span></span>

<span data-ttu-id="3e0c2-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3e0c2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3e0c2-124">Name</span><span class="sxs-lookup"><span data-stu-id="3e0c2-124">Name</span></span>                           | <span data-ttu-id="3e0c2-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="3e0c2-125">Data type</span></span>         | <span data-ttu-id="3e0c2-126">單位</span><span class="sxs-lookup"><span data-stu-id="3e0c2-126">Unit</span></span> | <span data-ttu-id="3e0c2-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="3e0c2-127">Supported values</span></span> | <span data-ttu-id="3e0c2-128">總結</span><span class="sxs-lookup"><span data-stu-id="3e0c2-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="3e0c2-129">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="3e0c2-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="3e0c2-130">string</span><span class="sxs-lookup"><span data-stu-id="3e0c2-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3e0c2-131">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3e0c2-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3e0c2-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e0c2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e0c2-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3e0c2-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





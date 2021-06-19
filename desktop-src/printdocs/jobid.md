---
description: 深入瞭解 JobID 元素，此專案會指定作業的唯一識別碼。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408881"
---
# <a name="jobid"></a><span data-ttu-id="bc137-104">JobID</span><span class="sxs-lookup"><span data-stu-id="bc137-104">JobID</span></span>

<span data-ttu-id="bc137-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bc137-105">This topic is not current.</span></span> <span data-ttu-id="bc137-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bc137-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc137-107">指定作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc137-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="bc137-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bc137-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bc137-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="bc137-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bc137-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="bc137-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bc137-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bc137-111">Element Information</span></span>



| <span data-ttu-id="bc137-112">Name</span><span class="sxs-lookup"><span data-stu-id="bc137-112">Name</span></span> | <span data-ttu-id="bc137-113">值</span><span class="sxs-lookup"><span data-stu-id="bc137-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="bc137-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="bc137-114">Element Type</span></span> <br/>   | <span data-ttu-id="bc137-115">屬性</span><span class="sxs-lookup"><span data-stu-id="bc137-115">Property</span></span><br/> |
| <span data-ttu-id="bc137-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="bc137-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc137-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="bc137-117">Job</span></span><br/>      |
| <span data-ttu-id="bc137-118">注意</span><span class="sxs-lookup"><span data-stu-id="bc137-118">Notes</span></span> <br/>          | <span data-ttu-id="bc137-119">None</span><span class="sxs-lookup"><span data-stu-id="bc137-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bc137-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="bc137-120">Structural Content</span></span>

<span data-ttu-id="bc137-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="bc137-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="bc137-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="bc137-122">Structure Variables</span></span>

<span data-ttu-id="bc137-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="bc137-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc137-124">Name</span><span class="sxs-lookup"><span data-stu-id="bc137-124">Name</span></span>                      | <span data-ttu-id="bc137-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="bc137-125">Data type</span></span>         | <span data-ttu-id="bc137-126">單位</span><span class="sxs-lookup"><span data-stu-id="bc137-126">Unit</span></span> | <span data-ttu-id="bc137-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="bc137-127">Supported values</span></span> | <span data-ttu-id="bc137-128">總結</span><span class="sxs-lookup"><span data-stu-id="bc137-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="bc137-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="bc137-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="bc137-130">string</span><span class="sxs-lookup"><span data-stu-id="bc137-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bc137-131">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="bc137-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="bc137-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc137-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc137-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bc137-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





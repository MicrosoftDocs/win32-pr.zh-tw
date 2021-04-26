---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb6259d8623a4611364023bf0f74784fe308b58
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998105"
---
# <a name="jobname"></a><span data-ttu-id="ebb59-104">JobName</span><span class="sxs-lookup"><span data-stu-id="ebb59-104">JobName</span></span>

<span data-ttu-id="ebb59-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ebb59-105">This topic is not current.</span></span> <span data-ttu-id="ebb59-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ebb59-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ebb59-107">指定作業的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="ebb59-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="ebb59-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ebb59-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ebb59-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ebb59-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ebb59-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ebb59-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ebb59-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ebb59-111">Element Information</span></span>



| <span data-ttu-id="ebb59-112">Name</span><span class="sxs-lookup"><span data-stu-id="ebb59-112">Name</span></span> | <span data-ttu-id="ebb59-113">值</span><span class="sxs-lookup"><span data-stu-id="ebb59-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="ebb59-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="ebb59-114">Element Type</span></span> <br/>   | <span data-ttu-id="ebb59-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ebb59-115">Property</span></span><br/> |
| <span data-ttu-id="ebb59-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ebb59-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ebb59-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="ebb59-117">Job</span></span><br/>      |
| <span data-ttu-id="ebb59-118">注意</span><span class="sxs-lookup"><span data-stu-id="ebb59-118">Notes</span></span> <br/>          | <span data-ttu-id="ebb59-119">None</span><span class="sxs-lookup"><span data-stu-id="ebb59-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ebb59-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ebb59-120">Structural Content</span></span>

<span data-ttu-id="ebb59-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="ebb59-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="ebb59-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="ebb59-122">Structure Variables</span></span>

<span data-ttu-id="ebb59-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ebb59-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ebb59-124">Name</span><span class="sxs-lookup"><span data-stu-id="ebb59-124">Name</span></span>                        | <span data-ttu-id="ebb59-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="ebb59-125">Data type</span></span>         | <span data-ttu-id="ebb59-126">單位</span><span class="sxs-lookup"><span data-stu-id="ebb59-126">Unit</span></span> | <span data-ttu-id="ebb59-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="ebb59-127">Supported values</span></span> | <span data-ttu-id="ebb59-128">總結</span><span class="sxs-lookup"><span data-stu-id="ebb59-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="ebb59-129">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="ebb59-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="ebb59-130">字串</span><span class="sxs-lookup"><span data-stu-id="ebb59-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ebb59-131">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ebb59-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="ebb59-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebb59-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb59-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ebb59-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





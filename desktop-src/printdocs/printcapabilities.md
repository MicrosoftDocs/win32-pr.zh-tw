---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975614"
---
# <a name="printcapabilities"></a><span data-ttu-id="47012-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="47012-104">PrintCapabilities</span></span>

<span data-ttu-id="47012-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="47012-105">This topic is not current.</span></span> <span data-ttu-id="47012-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="47012-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47012-107">PrintCapabilities 元素代表 PrintCapabilities 檔的根目錄。</span><span class="sxs-lookup"><span data-stu-id="47012-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="47012-108">PrintCapabilities 檔包含在指定特定裝置設定的情況下，描述支援的裝置屬性所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="47012-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="47012-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="47012-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="47012-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="47012-110">XML Attributes</span></span>

<span data-ttu-id="47012-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="47012-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="47012-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="47012-112">XML Attribute</span></span>      | <span data-ttu-id="47012-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="47012-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47012-114">version</span><span class="sxs-lookup"><span data-stu-id="47012-114">version</span></span><br/> | <span data-ttu-id="47012-115">指定定義元素類型及其結構的架構版本。</span><span class="sxs-lookup"><span data-stu-id="47012-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="47012-116">Version 屬性的類型為 integer。</span><span class="sxs-lookup"><span data-stu-id="47012-116">The version attribute is of type integer.</span></span> <span data-ttu-id="47012-117">目前的架構版本指定為 "1"。</span><span class="sxs-lookup"><span data-stu-id="47012-117">The current schema version is designated "1".</span></span> <span data-ttu-id="47012-118">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="47012-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="47012-119">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="47012-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="47012-120">項目資訊</span><span class="sxs-lookup"><span data-stu-id="47012-120">Element Information</span></span>

<span data-ttu-id="47012-121">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="47012-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="47012-122">類別</span><span class="sxs-lookup"><span data-stu-id="47012-122">Category</span></span>                   | <span data-ttu-id="47012-123">詳細資料</span><span class="sxs-lookup"><span data-stu-id="47012-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47012-124">父元素</span><span class="sxs-lookup"><span data-stu-id="47012-124">Parent elements</span></span><br/> | <span data-ttu-id="47012-125">僅限檔根目錄。</span><span class="sxs-lookup"><span data-stu-id="47012-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="47012-126">子元素</span><span class="sxs-lookup"><span data-stu-id="47012-126">Child elements</span></span><br/>  | <span data-ttu-id="47012-127">*功能* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="47012-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="47012-128">*ParameterDef* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="47012-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="47012-129">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="47012-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="47012-130">這個元素</span><span class="sxs-lookup"><span data-stu-id="47012-130">This element</span></span><br/>    | <span data-ttu-id="47012-131">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="47012-131">No character data is permitted.</span></span><br/> <span data-ttu-id="47012-132">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="47012-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="47012-133">設定相依性</span><span class="sxs-lookup"><span data-stu-id="47012-133">Configuration Dependencies</span></span>

<span data-ttu-id="47012-134">根項目可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="47012-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="47012-135">範例</span><span class="sxs-lookup"><span data-stu-id="47012-135">Example</span></span>

<span data-ttu-id="47012-136">請參閱 [PrintCapabilities 檔範例](printcapabilities-document-example.md)。</span><span class="sxs-lookup"><span data-stu-id="47012-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47012-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="47012-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47012-138">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="47012-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





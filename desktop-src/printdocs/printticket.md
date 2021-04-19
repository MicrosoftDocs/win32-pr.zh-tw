---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986458"
---
# <a name="printticket"></a><span data-ttu-id="69ac0-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="69ac0-104">PrintTicket</span></span>

<span data-ttu-id="69ac0-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="69ac0-105">This topic is not current.</span></span> <span data-ttu-id="69ac0-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="69ac0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="69ac0-107">PrintTicket 元素是 PrintTicket 檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="69ac0-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="69ac0-108">PrintTicket 元素包含輸出工作所需的所有工作格式資訊。</span><span class="sxs-lookup"><span data-stu-id="69ac0-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="69ac0-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="69ac0-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="69ac0-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="69ac0-110">XML Attributes</span></span>

<span data-ttu-id="69ac0-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="69ac0-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="69ac0-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="69ac0-112">XML Attribute</span></span>      | <span data-ttu-id="69ac0-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="69ac0-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ac0-114">version</span><span class="sxs-lookup"><span data-stu-id="69ac0-114">version</span></span><br/> | <span data-ttu-id="69ac0-115">指定定義專案類型和其結構的架構版本（整數類型的常值）。</span><span class="sxs-lookup"><span data-stu-id="69ac0-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="69ac0-116">目前的架構版本為 "1"。</span><span class="sxs-lookup"><span data-stu-id="69ac0-116">The current schema version is "1".</span></span> <span data-ttu-id="69ac0-117">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="69ac0-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="69ac0-118">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="69ac0-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="69ac0-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="69ac0-119">Element Information</span></span>

<span data-ttu-id="69ac0-120">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="69ac0-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="69ac0-121">類別</span><span class="sxs-lookup"><span data-stu-id="69ac0-121">Category</span></span>                   | <span data-ttu-id="69ac0-122">詳細資料</span><span class="sxs-lookup"><span data-stu-id="69ac0-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ac0-123">父元素</span><span class="sxs-lookup"><span data-stu-id="69ac0-123">Parent elements</span></span><br/> | <span data-ttu-id="69ac0-124">僅限檔根目錄。</span><span class="sxs-lookup"><span data-stu-id="69ac0-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="69ac0-125">子元素</span><span class="sxs-lookup"><span data-stu-id="69ac0-125">Child elements</span></span><br/>  | <span data-ttu-id="69ac0-126">*功能* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="69ac0-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="69ac0-127">*ParameterInit* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="69ac0-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="69ac0-128">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="69ac0-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="69ac0-129">這個元素</span><span class="sxs-lookup"><span data-stu-id="69ac0-129">This element</span></span><br/>    | <span data-ttu-id="69ac0-130">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="69ac0-130">No character data is permitted.</span></span><br/> <span data-ttu-id="69ac0-131">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="69ac0-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="69ac0-132">設定相依性</span><span class="sxs-lookup"><span data-stu-id="69ac0-132">Configuration Dependencies</span></span>

<span data-ttu-id="69ac0-133">設定相依性只適用于 PrintCapabilities 檔中的元素。</span><span class="sxs-lookup"><span data-stu-id="69ac0-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="69ac0-134">範例</span><span class="sxs-lookup"><span data-stu-id="69ac0-134">Example</span></span>

<span data-ttu-id="69ac0-135">請參閱 [PrintTicket 範例](printticket-example.md)。</span><span class="sxs-lookup"><span data-stu-id="69ac0-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69ac0-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="69ac0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69ac0-137">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="69ac0-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





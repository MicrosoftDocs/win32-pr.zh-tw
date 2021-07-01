---
description: 尋找有關 PrintTicket 元素的資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120073"
---
# <a name="printticket"></a><span data-ttu-id="46dbe-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="46dbe-105">PrintTicket</span></span>

<span data-ttu-id="46dbe-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="46dbe-106">This topic is not current.</span></span> <span data-ttu-id="46dbe-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="46dbe-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46dbe-108">PrintTicket 元素是 PrintTicket 檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="46dbe-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="46dbe-109">PrintTicket 元素包含輸出工作所需的所有工作格式資訊。</span><span class="sxs-lookup"><span data-stu-id="46dbe-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="46dbe-110">元素標記</span><span class="sxs-lookup"><span data-stu-id="46dbe-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="46dbe-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="46dbe-111">XML Attributes</span></span>

<span data-ttu-id="46dbe-112">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="46dbe-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="46dbe-113">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="46dbe-113">XML Attribute</span></span>      | <span data-ttu-id="46dbe-114">詳細資料</span><span class="sxs-lookup"><span data-stu-id="46dbe-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dbe-115">version</span><span class="sxs-lookup"><span data-stu-id="46dbe-115">version</span></span><br/> | <span data-ttu-id="46dbe-116">指定定義專案類型和其結構的架構版本（整數類型的常值）。</span><span class="sxs-lookup"><span data-stu-id="46dbe-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="46dbe-117">目前的架構版本為 "1"。</span><span class="sxs-lookup"><span data-stu-id="46dbe-117">The current schema version is "1".</span></span> <span data-ttu-id="46dbe-118">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="46dbe-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="46dbe-119">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="46dbe-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="46dbe-120">項目資訊</span><span class="sxs-lookup"><span data-stu-id="46dbe-120">Element Information</span></span>

<span data-ttu-id="46dbe-121">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="46dbe-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="46dbe-122">類別</span><span class="sxs-lookup"><span data-stu-id="46dbe-122">Category</span></span>                   | <span data-ttu-id="46dbe-123">詳細資料</span><span class="sxs-lookup"><span data-stu-id="46dbe-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dbe-124">父元素</span><span class="sxs-lookup"><span data-stu-id="46dbe-124">Parent elements</span></span><br/> | <span data-ttu-id="46dbe-125">僅限檔根目錄。</span><span class="sxs-lookup"><span data-stu-id="46dbe-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="46dbe-126">子元素</span><span class="sxs-lookup"><span data-stu-id="46dbe-126">Child elements</span></span><br/>  | <span data-ttu-id="46dbe-127">*功能* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="46dbe-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="46dbe-128">*ParameterInit* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="46dbe-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="46dbe-129">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="46dbe-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="46dbe-130">這個元素</span><span class="sxs-lookup"><span data-stu-id="46dbe-130">This element</span></span><br/>    | <span data-ttu-id="46dbe-131">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="46dbe-131">No character data is permitted.</span></span><br/> <span data-ttu-id="46dbe-132">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="46dbe-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="46dbe-133">設定相依性</span><span class="sxs-lookup"><span data-stu-id="46dbe-133">Configuration Dependencies</span></span>

<span data-ttu-id="46dbe-134">設定相依性只適用于 PrintCapabilities 檔中的元素。</span><span class="sxs-lookup"><span data-stu-id="46dbe-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="46dbe-135">範例</span><span class="sxs-lookup"><span data-stu-id="46dbe-135">Example</span></span>

<span data-ttu-id="46dbe-136">請參閱 [PrintTicket 範例](printticket-example.md)。</span><span class="sxs-lookup"><span data-stu-id="46dbe-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46dbe-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="46dbe-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46dbe-138">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="46dbe-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





---
description: 深入瞭解 PrintCapabilities 元素，其代表 PrintCapabilities 檔的根目錄。
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407021"
---
# <a name="printcapabilities"></a><span data-ttu-id="16cf3-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="16cf3-103">PrintCapabilities</span></span>

<span data-ttu-id="16cf3-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="16cf3-104">This topic is not current.</span></span> <span data-ttu-id="16cf3-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="16cf3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16cf3-106">PrintCapabilities 元素代表 PrintCapabilities 檔的根目錄。</span><span class="sxs-lookup"><span data-stu-id="16cf3-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="16cf3-107">PrintCapabilities 檔包含在指定特定裝置設定的情況下，描述支援的裝置屬性所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="16cf3-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="16cf3-108">元素標記</span><span class="sxs-lookup"><span data-stu-id="16cf3-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="16cf3-109">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="16cf3-109">XML Attributes</span></span>

<span data-ttu-id="16cf3-110">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="16cf3-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="16cf3-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="16cf3-111">XML Attribute</span></span>      | <span data-ttu-id="16cf3-112">詳細資料</span><span class="sxs-lookup"><span data-stu-id="16cf3-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cf3-113">version</span><span class="sxs-lookup"><span data-stu-id="16cf3-113">version</span></span><br/> | <span data-ttu-id="16cf3-114">指定定義元素類型及其結構的架構版本。</span><span class="sxs-lookup"><span data-stu-id="16cf3-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="16cf3-115">Version 屬性的類型為 integer。</span><span class="sxs-lookup"><span data-stu-id="16cf3-115">The version attribute is of type integer.</span></span> <span data-ttu-id="16cf3-116">目前的架構版本指定為 "1"。</span><span class="sxs-lookup"><span data-stu-id="16cf3-116">The current schema version is designated "1".</span></span> <span data-ttu-id="16cf3-117">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="16cf3-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="16cf3-118">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="16cf3-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="16cf3-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="16cf3-119">Element Information</span></span>

<span data-ttu-id="16cf3-120">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="16cf3-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="16cf3-121">類別</span><span class="sxs-lookup"><span data-stu-id="16cf3-121">Category</span></span>                   | <span data-ttu-id="16cf3-122">詳細資料</span><span class="sxs-lookup"><span data-stu-id="16cf3-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cf3-123">父元素</span><span class="sxs-lookup"><span data-stu-id="16cf3-123">Parent elements</span></span><br/> | <span data-ttu-id="16cf3-124">僅限檔根目錄。</span><span class="sxs-lookup"><span data-stu-id="16cf3-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="16cf3-125">子元素</span><span class="sxs-lookup"><span data-stu-id="16cf3-125">Child elements</span></span><br/>  | <span data-ttu-id="16cf3-126">*功能* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="16cf3-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="16cf3-127">*ParameterDef* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="16cf3-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="16cf3-128">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="16cf3-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="16cf3-129">這個元素</span><span class="sxs-lookup"><span data-stu-id="16cf3-129">This element</span></span><br/>    | <span data-ttu-id="16cf3-130">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="16cf3-130">No character data is permitted.</span></span><br/> <span data-ttu-id="16cf3-131">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="16cf3-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="16cf3-132">設定相依性</span><span class="sxs-lookup"><span data-stu-id="16cf3-132">Configuration Dependencies</span></span>

<span data-ttu-id="16cf3-133">根項目可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="16cf3-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="16cf3-134">範例</span><span class="sxs-lookup"><span data-stu-id="16cf3-134">Example</span></span>

<span data-ttu-id="16cf3-135">請參閱 [PrintCapabilities 檔範例](printcapabilities-document-example.md)。</span><span class="sxs-lookup"><span data-stu-id="16cf3-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16cf3-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="16cf3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16cf3-137">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="16cf3-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





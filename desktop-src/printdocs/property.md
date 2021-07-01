---
description: 瞭解檔和列印中的屬性元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: '屬性 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120293"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="2e02c-105">屬性 (檔和列印) </span><span class="sxs-lookup"><span data-stu-id="2e02c-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="2e02c-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2e02c-106">This topic is not current.</span></span> <span data-ttu-id="2e02c-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2e02c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e02c-108">屬性專案會宣告裝置、作業格式或其他相關屬性，其名稱是由其名稱屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="2e02c-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="2e02c-109">值元素用來將值指派給屬性。</span><span class="sxs-lookup"><span data-stu-id="2e02c-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="2e02c-110">屬性可能很複雜，可能包含多個子屬性。</span><span class="sxs-lookup"><span data-stu-id="2e02c-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="2e02c-111">子屬性也會以屬性元素表示。</span><span class="sxs-lookup"><span data-stu-id="2e02c-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="2e02c-112">元素標記</span><span class="sxs-lookup"><span data-stu-id="2e02c-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="2e02c-113">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="2e02c-113">XML Attributes</span></span>

<span data-ttu-id="2e02c-114">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e02c-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="2e02c-115">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="2e02c-115">XML Attribute</span></span>   | <span data-ttu-id="2e02c-116">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2e02c-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e02c-117">NAME</span><span class="sxs-lookup"><span data-stu-id="2e02c-117">name</span></span><br/> | <span data-ttu-id="2e02c-118">保存屬性（attribute）的 name 屬性（property），該屬性（property）是標準屬性（property）或私用屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="2e02c-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="2e02c-119">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="2e02c-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="2e02c-120">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2e02c-120">Element Information</span></span>

<span data-ttu-id="2e02c-121">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="2e02c-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="2e02c-122">類別</span><span class="sxs-lookup"><span data-stu-id="2e02c-122">Category</span></span>                   | <span data-ttu-id="2e02c-123">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2e02c-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e02c-124">父元素</span><span class="sxs-lookup"><span data-stu-id="2e02c-124">Parent elements</span></span><br/> | <span data-ttu-id="2e02c-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="2e02c-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="2e02c-126">功能</span><span class="sxs-lookup"><span data-stu-id="2e02c-126">Feature</span></span><br/> <span data-ttu-id="2e02c-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="2e02c-127">PrintTicket</span></span><br/> <span data-ttu-id="2e02c-128">選項</span><span class="sxs-lookup"><span data-stu-id="2e02c-128">Option</span></span><br/> <span data-ttu-id="2e02c-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2e02c-129">ParameterDef</span></span><br/> <span data-ttu-id="2e02c-130">屬性</span><span class="sxs-lookup"><span data-stu-id="2e02c-130">Property</span></span><br/> <span data-ttu-id="2e02c-131">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="2e02c-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="2e02c-132">子元素</span><span class="sxs-lookup"><span data-stu-id="2e02c-132">Child elements</span></span><br/>  | <span data-ttu-id="2e02c-133">系統不會將任何意義指派給元素的順序。</span><span class="sxs-lookup"><span data-stu-id="2e02c-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="2e02c-134">如果用戶端選擇歸屬元素順序中的一些重要性，則可以隨意進行。</span><span class="sxs-lookup"><span data-stu-id="2e02c-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="2e02c-135">*屬性* (一或多個) *值* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="2e02c-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="2e02c-136">或</span><span class="sxs-lookup"><span data-stu-id="2e02c-136">or</span></span> <br/> <span data-ttu-id="2e02c-137">*屬性* (零或多個) *值* (一或多個) </span><span class="sxs-lookup"><span data-stu-id="2e02c-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="2e02c-138">這個元素</span><span class="sxs-lookup"><span data-stu-id="2e02c-138">This element</span></span><br/>    | <span data-ttu-id="2e02c-139">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="2e02c-139">No character data is permitted.</span></span><br/> <span data-ttu-id="2e02c-140">允許同級的重複子值元素。</span><span class="sxs-lookup"><span data-stu-id="2e02c-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="2e02c-141">設定相依性</span><span class="sxs-lookup"><span data-stu-id="2e02c-141">Configuration Dependencies</span></span>

<span data-ttu-id="2e02c-142">屬性可能具有設定相依性，除非它出現在 ParameterDef 元素中。</span><span class="sxs-lookup"><span data-stu-id="2e02c-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="2e02c-143">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="2e02c-143">Element Usage</span></span>

<span data-ttu-id="2e02c-144">除了出現在功能和選項專案中之外，屬性專案也可以出現在個別基礎技術的根層級上。</span><span class="sxs-lookup"><span data-stu-id="2e02c-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="2e02c-145">列印架構會定義一組屬性元素，可用來以可移植的方式描述裝置。</span><span class="sxs-lookup"><span data-stu-id="2e02c-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="2e02c-146">但是，如果這些屬性不符合您的需求做為 PrintCapabilities 提供者 (通常是因為支援的裝置具有列印架構) 不預期的新穎層面，您可能會引進自己的私用屬性元素。</span><span class="sxs-lookup"><span data-stu-id="2e02c-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="2e02c-147">您可以藉由將一或多個私用子屬性新增為公用屬性的元素內容，來增強或詳細地增強或詳細說明公用屬性所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e02c-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="2e02c-148">您可以使用 XML 專案標記來定義屬性元素 <Property> 。</span><span class="sxs-lookup"><span data-stu-id="2e02c-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="2e02c-149">每個屬性都會透過其 name 屬性來指派名稱。</span><span class="sxs-lookup"><span data-stu-id="2e02c-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="2e02c-150">名稱必須是 XML QName，而且必須符合命名空間慣例。</span><span class="sxs-lookup"><span data-stu-id="2e02c-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="2e02c-151">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="2e02c-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="2e02c-152">屬性名稱屬性及其在父屬性專案階層中的位置 (如果它是子屬性) 可唯一識別 PrintCapabilities 檔內的屬性或 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="2e02c-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="2e02c-153">屬性可包含一或多個值元素，或是一或多個子屬性元素 (稱為子屬性) ，或兩者的組合。</span><span class="sxs-lookup"><span data-stu-id="2e02c-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="2e02c-154">當屬性本身由多個元件組成時，子屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="2e02c-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="2e02c-155">例如，"ConsumableColor" 屬性可能具有 "C"、"M" 和 "Y" 元件。</span><span class="sxs-lookup"><span data-stu-id="2e02c-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="2e02c-156">範例</span><span class="sxs-lookup"><span data-stu-id="2e02c-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2e02c-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e02c-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e02c-158">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2e02c-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





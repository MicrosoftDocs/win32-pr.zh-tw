---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: '屬性 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321723"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="8d8b3-104">屬性 (檔和列印) </span><span class="sxs-lookup"><span data-stu-id="8d8b3-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="8d8b3-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-105">This topic is not current.</span></span> <span data-ttu-id="8d8b3-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d8b3-107">屬性專案會宣告裝置、作業格式或其他相關屬性，其名稱是由其名稱屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="8d8b3-108">值元素用來將值指派給屬性。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="8d8b3-109">屬性可能很複雜，可能包含多個子屬性。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="8d8b3-110">子屬性也會以屬性元素表示。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="8d8b3-111">元素標記</span><span class="sxs-lookup"><span data-stu-id="8d8b3-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="8d8b3-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="8d8b3-112">XML Attributes</span></span>

<span data-ttu-id="8d8b3-113">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="8d8b3-114">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="8d8b3-114">XML Attribute</span></span>   | <span data-ttu-id="8d8b3-115">詳細資料</span><span class="sxs-lookup"><span data-stu-id="8d8b3-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8b3-116">NAME</span><span class="sxs-lookup"><span data-stu-id="8d8b3-116">name</span></span><br/> | <span data-ttu-id="8d8b3-117">保存屬性（attribute）的 name 屬性（property），該屬性（property）是標準屬性（property）或私用屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="8d8b3-118">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="8d8b3-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8d8b3-119">Element Information</span></span>

<span data-ttu-id="8d8b3-120">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="8d8b3-121">類別</span><span class="sxs-lookup"><span data-stu-id="8d8b3-121">Category</span></span>                   | <span data-ttu-id="8d8b3-122">詳細資料</span><span class="sxs-lookup"><span data-stu-id="8d8b3-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8b3-123">父元素</span><span class="sxs-lookup"><span data-stu-id="8d8b3-123">Parent elements</span></span><br/> | <span data-ttu-id="8d8b3-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="8d8b3-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="8d8b3-125">功能</span><span class="sxs-lookup"><span data-stu-id="8d8b3-125">Feature</span></span><br/> <span data-ttu-id="8d8b3-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="8d8b3-126">PrintTicket</span></span><br/> <span data-ttu-id="8d8b3-127">選項</span><span class="sxs-lookup"><span data-stu-id="8d8b3-127">Option</span></span><br/> <span data-ttu-id="8d8b3-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8d8b3-128">ParameterDef</span></span><br/> <span data-ttu-id="8d8b3-129">屬性</span><span class="sxs-lookup"><span data-stu-id="8d8b3-129">Property</span></span><br/> <span data-ttu-id="8d8b3-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="8d8b3-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="8d8b3-131">子元素</span><span class="sxs-lookup"><span data-stu-id="8d8b3-131">Child elements</span></span><br/>  | <span data-ttu-id="8d8b3-132">系統不會將任何意義指派給元素的順序。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="8d8b3-133">如果用戶端選擇歸屬元素順序中的一些重要性，則可以隨意進行。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="8d8b3-134">*屬性* (一或多個) *值* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="8d8b3-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="8d8b3-135">或</span><span class="sxs-lookup"><span data-stu-id="8d8b3-135">or</span></span> <br/> <span data-ttu-id="8d8b3-136">*屬性* (零或多個) *值* (一或多個) </span><span class="sxs-lookup"><span data-stu-id="8d8b3-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="8d8b3-137">這個元素</span><span class="sxs-lookup"><span data-stu-id="8d8b3-137">This element</span></span><br/>    | <span data-ttu-id="8d8b3-138">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-138">No character data is permitted.</span></span><br/> <span data-ttu-id="8d8b3-139">允許同級的重複子值元素。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="8d8b3-140">設定相依性</span><span class="sxs-lookup"><span data-stu-id="8d8b3-140">Configuration Dependencies</span></span>

<span data-ttu-id="8d8b3-141">屬性可能具有設定相依性，除非它出現在 ParameterDef 元素中。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="8d8b3-142">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="8d8b3-142">Element Usage</span></span>

<span data-ttu-id="8d8b3-143">除了出現在功能和選項專案中之外，屬性專案也可以出現在個別基礎技術的根層級上。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="8d8b3-144">列印架構會定義一組屬性元素，可用來以可移植的方式描述裝置。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="8d8b3-145">但是，如果這些屬性不符合您的需求做為 PrintCapabilities 提供者 (通常是因為支援的裝置具有列印架構) 不預期的新穎層面，您可能會引進自己的私用屬性元素。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="8d8b3-146">您可以藉由將一或多個私用子屬性新增為公用屬性的元素內容，來增強或詳細地增強或詳細說明公用屬性所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="8d8b3-147">您可以使用 XML 專案標記來定義屬性元素 <Property> 。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="8d8b3-148">每個屬性都會透過其 name 屬性來指派名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="8d8b3-149">名稱必須是 XML QName，而且必須符合命名空間慣例。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="8d8b3-150">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="8d8b3-151">屬性名稱屬性及其在父屬性專案階層中的位置 (如果它是子屬性) 可唯一識別 PrintCapabilities 檔內的屬性或 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="8d8b3-152">屬性可包含一或多個值元素，或是一或多個子屬性元素 (稱為子屬性) ，或兩者的組合。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="8d8b3-153">當屬性本身由多個元件組成時，子屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="8d8b3-154">例如，"ConsumableColor" 屬性可能具有 "C"、"M" 和 "Y" 元件。</span><span class="sxs-lookup"><span data-stu-id="8d8b3-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="8d8b3-155">範例</span><span class="sxs-lookup"><span data-stu-id="8d8b3-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="8d8b3-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d8b3-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d8b3-157">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="8d8b3-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: ParameterDef 和 ParameterInit 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985829"
---
# <a name="parameterdef-and-parameterinit-elements"></a><span data-ttu-id="2c91d-104">ParameterDef 和 ParameterInit 元素</span><span class="sxs-lookup"><span data-stu-id="2c91d-104">ParameterDef and ParameterInit Elements</span></span>

<span data-ttu-id="2c91d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2c91d-105">This topic is not current.</span></span> <span data-ttu-id="2c91d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2c91d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c91d-107">ParameterDef 元素與 ParameterInit 元素不同之處在于，它會描述 ParameterInit 元素可包含的值，而 ParameterInit 專案則會將值指派給參數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-107">A ParameterDef element differs from a ParameterInit element in that it describes the value that a ParameterInit element can contain, while a ParameterInit element assigns a value to the parameter.</span></span> <span data-ttu-id="2c91d-108">ParameterDef 元素是由一組特定的屬性元素所組成，也就是 ParameterDef 元素的子系，可指定資料的類型、最大值、最小值和預設值，以及其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2c91d-108">A ParameterDef element consists of a specific set of Property elements, which are children of the ParameterDef element, that specify the type of data, maximum, minimum, and default values for the data, and other information.</span></span> <span data-ttu-id="2c91d-109">本主題稍後會討論這些屬性元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-109">These Property elements are discussed later in this topic.</span></span>

<span data-ttu-id="2c91d-110">ParameterDef 元素只能出現在其允許的內容中。</span><span class="sxs-lookup"><span data-stu-id="2c91d-110">ParameterDef elements can appear only in their allowed context.</span></span> <span data-ttu-id="2c91d-111">針對列印架構的初始版本，它們可能位於 PrintCapabilities 檔的根層級。</span><span class="sxs-lookup"><span data-stu-id="2c91d-111">For the initial version of the Print Schema they may be located at the root level of the PrintCapabilities document.</span></span> <span data-ttu-id="2c91d-112">ParameterDef 元素的 name 屬性會定義參數名稱。</span><span class="sxs-lookup"><span data-stu-id="2c91d-112">The name attribute of the ParameterDef element defines the parameter name.</span></span> <span data-ttu-id="2c91d-113">PrintCapabilities 檔中的每個 ParameterDef 元素都必須被指派一個唯一的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="2c91d-113">Each ParameterDef element in the PrintCapabilities document must be assigned a unique name attribute.</span></span>

> [!Note]
> <span data-ttu-id="2c91d-114">若要列印功能檔提供者：</span><span class="sxs-lookup"><span data-stu-id="2c91d-114">to Print Capabilities Document Providers:</span></span>
> 
> <span data-ttu-id="2c91d-115">參數名稱的意義是通用的;也就是說，如果某個 PrintCapabilities 檔中的 ParameterDef 專案具有相同的名稱屬性 (命名空間所形成的字串，以及 ParameterDef 專案的描述性名稱) 為另一個 PrintCapabilities 檔中的 ParameterDef 專案，則會假設這兩個元素都代表相同的概念，而且應該以相同的方式加以解讀。</span><span class="sxs-lookup"><span data-stu-id="2c91d-115">The meaning of a parameter name is universal; that is, if a ParameterDef element in one PrintCapabilities document has the same name attribute (the string formed from the namespace and the descriptive name of the ParameterDef element) as a ParameterDef element in another PrintCapabilities document, it is assumed that both of these elements represent the same concept and should be interpreted in the same manner.</span></span> <span data-ttu-id="2c91d-116">因此，在一個 PrintCapabilities 檔的 PrintTicket 中定義的 ParameterDef 元素可以用來初始化不同 PrintCapabilities 檔中所定義之相同名稱的 ParameterInit 專案。</span><span class="sxs-lookup"><span data-stu-id="2c91d-116">Thus a ParameterDef element defined in a PrintTicket for one PrintCapabilities document can be used to initialize the ParameterInit element of the same name defined in a different PrintCapabilities document.</span></span>

 

## <a name="relationship-to-xml-attributes"></a><span data-ttu-id="2c91d-117">與 XML 屬性的關聯性</span><span class="sxs-lookup"><span data-stu-id="2c91d-117">Relationship to XML Attributes</span></span>

<span data-ttu-id="2c91d-118">如同所有 name 屬性的 true，參數名稱的格式為 XML QName。</span><span class="sxs-lookup"><span data-stu-id="2c91d-118">As is true of all name attributes, the parameter name is in the form of an XML QName.</span></span> <span data-ttu-id="2c91d-119">架構定義的參數結構具有由公用命名空間限定的名稱，形成 name 屬性，而私用定義的參數結構名稱屬性則是由 creator 的唯一私用命名空間限定。</span><span class="sxs-lookup"><span data-stu-id="2c91d-119">A Schema-defined parameter construct has a name that is qualified by the public namespace, forming the name attribute, while the name attribute of a privately-defined parameter construct is qualified by a private namespace that is unique to the creator.</span></span>

## <a name="relationship-between-parameterdef-and-property-element-types"></a><span data-ttu-id="2c91d-120">ParameterDef 和 Property 元素類型之間的關聯性</span><span class="sxs-lookup"><span data-stu-id="2c91d-120">Relationship between ParameterDef and Property Element Types</span></span>

<span data-ttu-id="2c91d-121">ParameterDef 在列印架構關鍵字中定義的元素必須在 PrintCapabilities 檔中完整定義。</span><span class="sxs-lookup"><span data-stu-id="2c91d-121">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span> <span data-ttu-id="2c91d-122">Print Schema 關鍵字檔提供 ParameterDef 專案的某些屬性專案的名義值 (例如 DefaultValue 和其他) ，但 PrintCapabilities 檔的作者必須負責定義其餘的屬性元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-122">The Print Schema Keywords document provides nominal values for some Property elements of a ParameterDef element (such as DefaultValue and others), but the author of a PrintCapabilities document is responsible for defining the remaining Property elements.</span></span> <span data-ttu-id="2c91d-123">在任何情況下，所有屬性專案都必須在 ParameterDef 專案中明確定義，包括在 Print Schema 關鍵字中定義的元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-123">In any case, all Property elements must be explicitly defined in a ParameterDef element, including those that are defined in the Print Schema Keywords.</span></span>

<span data-ttu-id="2c91d-124">顯示在列印架構關鍵字中的每個 ParameterDef 專案的特定屬性元素會指定為 *不可變*。</span><span class="sxs-lookup"><span data-stu-id="2c91d-124">Certain Property elements of each ParameterDef element appearing in the Print Schema Keywords are designated as *immutable*.</span></span> <span data-ttu-id="2c91d-125">這表示，列印架構關鍵字定義 ParameterDef 專案的所有 PrintCapabilities 檔定義都必須保留這些屬性元素，而不需要修改。</span><span class="sxs-lookup"><span data-stu-id="2c91d-125">This means that all PrintCapabilities document definitions of Print Schema Keywords-defined ParameterDef elements must preserve these Property elements without modification.</span></span> <span data-ttu-id="2c91d-126">這些不可變的屬性元素可讓參數結構在所有 PrintCapabilities 檔中都是可移植且不明確的。</span><span class="sxs-lookup"><span data-stu-id="2c91d-126">These immutable Property elements allow the parameter constructs to be portable and unambiguous across all PrintCapabilities documents.</span></span> <span data-ttu-id="2c91d-127">ParameterDef 元素中使用的單位是主要範例。</span><span class="sxs-lookup"><span data-stu-id="2c91d-127">A prime example is the units used in a ParameterDef element.</span></span> <span data-ttu-id="2c91d-128">這些單位應該是不可變的，以促進對其意義的一致理解。</span><span class="sxs-lookup"><span data-stu-id="2c91d-128">These units should be immutable, to promote a consistent understanding of their meaning.</span></span> <span data-ttu-id="2c91d-129">在 PrintCapabilities 檔中，可重新定義指定為不可變之 ParameterDef 的屬性元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-129">Property elements of a ParameterDef that are designated as not immutable may be redefined within a PrintCapabilities document.</span></span>

<span data-ttu-id="2c91d-130">ParameterDef 元素是由下列屬性元素所組成。</span><span class="sxs-lookup"><span data-stu-id="2c91d-130">A ParameterDef element is composed of the following Property elements.</span></span> <span data-ttu-id="2c91d-131">除非另有說明，否則全部都必須存在。</span><span class="sxs-lookup"><span data-stu-id="2c91d-131">All must be present unless otherwise noted.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c91d-132">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="2c91d-132">Property Name</span></span></th>
<th><span data-ttu-id="2c91d-133">值</span><span class="sxs-lookup"><span data-stu-id="2c91d-133">Values</span></span></th>
<th><span data-ttu-id="2c91d-134">描述</span><span class="sxs-lookup"><span data-stu-id="2c91d-134">Description</span></span></th>
<th><span data-ttu-id="2c91d-135">變？</span><span class="sxs-lookup"><span data-stu-id="2c91d-135">Immutable?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c91d-136">DataType</span><span class="sxs-lookup"><span data-stu-id="2c91d-136">DataType</span></span> <br/></td>
<td><span data-ttu-id="2c91d-137">整數</span><span class="sxs-lookup"><span data-stu-id="2c91d-137">integer</span></span> <br/> <span data-ttu-id="2c91d-138">decimal</span><span class="sxs-lookup"><span data-stu-id="2c91d-138">decimal</span></span><br/> <span data-ttu-id="2c91d-139">字串</span><span class="sxs-lookup"><span data-stu-id="2c91d-139">string</span></span><br/> <span data-ttu-id="2c91d-140">無預設值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-140">No default value.</span></span><br/></td>
<td><span data-ttu-id="2c91d-141">指定參數值是整數、浮點數或文字字串。</span><span class="sxs-lookup"><span data-stu-id="2c91d-141">Specifies whether the parameter value is an integer, or floating point number, or a text string.</span></span> <span data-ttu-id="2c91d-142">參數的值會使用與對應的 XSD 基本資料類型相同的格式來表示;也就是整數、十進位或字串。</span><span class="sxs-lookup"><span data-stu-id="2c91d-142">The value of a parameter is expressed in the same format as the corresponding XSD basic data type; that is, as an integer, decimal, or string.</span></span> <br/></td>
<td><span data-ttu-id="2c91d-143">Yes</span><span class="sxs-lookup"><span data-stu-id="2c91d-143">Yes</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c91d-144">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2c91d-144">DefaultValue</span></span> <br/></td>
<td><span data-ttu-id="2c91d-145">DataType 屬性指定的型別。</span><span class="sxs-lookup"><span data-stu-id="2c91d-145">The type specified by the DataType Property.</span></span><br/> <span data-ttu-id="2c91d-146">無預設值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-146">No default value.</span></span><br/></td>
<td><span data-ttu-id="2c91d-147">指定用來初始化使用者介面 (UI) 控制項的值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-147">Specifies the value with which to initialize a user interface (UI) control.</span></span><br/>
<ul>
<li><span data-ttu-id="2c91d-148">或</span><span class="sxs-lookup"><span data-stu-id="2c91d-148">or</span></span> <br/></li>
</ul>
<span data-ttu-id="2c91d-149">指定當 PrintTicket 中缺少相關的參數專案時，所要使用的值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-149">Specifies the value to use if the relevant parameter element is missing from the PrintTicket.</span></span><br/></td>
<td><span data-ttu-id="2c91d-150">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-150">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c91d-151">強制性</span><span class="sxs-lookup"><span data-stu-id="2c91d-151">Mandatory</span></span> <br/></td>
<td><span data-ttu-id="2c91d-152">無條件：必須一律提供 ParameterInit 元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-152">Unconditional: the ParameterInit element must always be supplied.</span></span> <br/> <span data-ttu-id="2c91d-153">條件式：只有在 PrintTicket 的 Option 元素內參考參數時，才需要 ParameterInit 元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-153">Conditional: the ParameterInit element is required only if the parameter is referenced within an Option element in a PrintTicket.</span></span><br/> <span data-ttu-id="2c91d-154">DefaultValue：條件式。</span><span class="sxs-lookup"><span data-stu-id="2c91d-154">DefaultValue: Conditional.</span></span><br/></td>
<td><span data-ttu-id="2c91d-155">指出 ParameterInit 元素必須明確出現的時間。</span><span class="sxs-lookup"><span data-stu-id="2c91d-155">Indicates when a ParameterInit element must appear explicitly.</span></span> <span data-ttu-id="2c91d-156">如果是條件式，則如果 PrintTicket 包含參考參數的選項，則 ParameterInit 必須初始化。</span><span class="sxs-lookup"><span data-stu-id="2c91d-156">If Conditional, the ParameterInit must be initialized if the PrintTicket contains an Option that references the parameter.</span></span><br/> <span data-ttu-id="2c91d-157">由 UI 用戶端和 PrintCapabilities 或 PrintTicket 提供者使用。</span><span class="sxs-lookup"><span data-stu-id="2c91d-157">Used by UI Clients and PrintCapabilities or PrintTicket providers.</span></span> <span data-ttu-id="2c91d-158">請注意，在任何條件約束中，ParameterDef 元素的強制屬性必須設定為無條件。</span><span class="sxs-lookup"><span data-stu-id="2c91d-158">Note that in any constraint, the Mandatory Property of the ParameterDef element must be set to Unconditional.</span></span> <span data-ttu-id="2c91d-159">ParameterDef 必須有定義的值，否則無法評估相依的值或條件約束。</span><span class="sxs-lookup"><span data-stu-id="2c91d-159">The ParameterDef must have a defined Value, otherwise the dependent Value or constraint could not be evaluated.</span></span><br/></td>
<td><span data-ttu-id="2c91d-160">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-160">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c91d-161">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2c91d-161">MaxLength</span></span> <br/></td>
<td><span data-ttu-id="2c91d-162">如果 DataType 屬性指定 string，則為整數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-162">integer if DataType Property specifies string.</span></span><br/> <span data-ttu-id="2c91d-163">DefaultValue：不會強制執行最大值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-163">DefaultValue: No maximum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="2c91d-164">若為字串值參數，則指定允許的最長字串。</span><span class="sxs-lookup"><span data-stu-id="2c91d-164">For string-valued parameters, specifies the longest allowed string.</span></span> <span data-ttu-id="2c91d-165">UI 和 PrintCapabilities 或 PrintTicket 提供者會使用這個屬性來驗證 ParameterDef 元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-165">UI and PrintCapabilities or PrintTicket providers use this Property to validate the ParameterDef element.</span></span><br/></td>
<td><span data-ttu-id="2c91d-166">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-166">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c91d-167">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2c91d-167">MaxValue</span></span> <br/></td>
<td><span data-ttu-id="2c91d-168">如果 DataType 屬性指定整數，則為整數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-168">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="2c91d-169">如果 DataType 屬性指定 decimal，則為 decimal。</span><span class="sxs-lookup"><span data-stu-id="2c91d-169">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="2c91d-170">DefaultValue：不會強制執行最大值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-170">DefaultValue: No maximum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="2c91d-171">若為整數或十進位值 ParameterDef 元素，則會定義最大的允許值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-171">For integer-or decimal-valued ParameterDef elements, defines the largest allowed value.</span></span><br/></td>
<td><span data-ttu-id="2c91d-172">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-172">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c91d-173">MinLength</span><span class="sxs-lookup"><span data-stu-id="2c91d-173">MinLength</span></span> <br/></td>
<td><span data-ttu-id="2c91d-174">如果 DataType 屬性指定 string，則為整數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-174">integer if DataType Property specifies string.</span></span> <br/> <span data-ttu-id="2c91d-175">DefaultValue：不會強制執行最小值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-175">DefaultValue: No minimum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="2c91d-176">針對字串值，定義允許的最短字串。</span><span class="sxs-lookup"><span data-stu-id="2c91d-176">For string values, defines the shortest allowed string.</span></span> <span data-ttu-id="2c91d-177">UI 和 PrintCapabilities 或 PrintTicket 提供者會使用這個屬性來驗證 ParameterDef 元素。</span><span class="sxs-lookup"><span data-stu-id="2c91d-177">UI and PrintCapabilities or PrintTicket providers use this Property to validate the ParameterDef element.</span></span><br/></td>
<td><span data-ttu-id="2c91d-178">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-178">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c91d-179">MinValue</span><span class="sxs-lookup"><span data-stu-id="2c91d-179">MinValue</span></span> <br/></td>
<td><span data-ttu-id="2c91d-180">如果 DataType 屬性指定整數，則為整數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-180">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="2c91d-181">如果 DataType 屬性指定 decimal，則為 decimal。</span><span class="sxs-lookup"><span data-stu-id="2c91d-181">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="2c91d-182">DefaultValue：不會強制執行最小值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-182">DefaultValue: No minimum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="2c91d-183">針對整數或十進位值參數，定義最小的允許值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-183">For integer- or decimal-valued parameters, defines the smallest allowed value.</span></span> <br/></td>
<td><span data-ttu-id="2c91d-184">否</span><span class="sxs-lookup"><span data-stu-id="2c91d-184">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c91d-185">多個</span><span class="sxs-lookup"><span data-stu-id="2c91d-185">Multiple</span></span> <br/></td>
<td><span data-ttu-id="2c91d-186">如果 DataType 屬性指定整數，則為整數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-186">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="2c91d-187">如果 DataType 屬性指定 decimal，則為 decimal。</span><span class="sxs-lookup"><span data-stu-id="2c91d-187">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="2c91d-188">DefaultValue：1</span><span class="sxs-lookup"><span data-stu-id="2c91d-188">DefaultValue: 1</span></span><br/></td>
<td><span data-ttu-id="2c91d-189">若為整數或十進位值參數，參數的值應該是這個數位的倍數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-189">For integer- or decimal-valued parameters, the value of the parameter should be a multiple of this number.</span></span> <span data-ttu-id="2c91d-190">如需詳細資訊，請參閱下表的 <a href="#notes-on-multiple">多個注意事項</a> 。</span><span class="sxs-lookup"><span data-stu-id="2c91d-190">For more information, see <a href="#notes-on-multiple">Notes on Multiple</a> following this table.</span></span><br/></td>
<td><span data-ttu-id="2c91d-191">No</span><span class="sxs-lookup"><span data-stu-id="2c91d-191">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c91d-192">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="2c91d-192">UnitType</span></span> <br/></td>
<td><span data-ttu-id="2c91d-193">字串值，表示用於參數的單位。</span><span class="sxs-lookup"><span data-stu-id="2c91d-193">string value indicating the units used for the parameter.</span></span><br/> <span data-ttu-id="2c91d-194">無預設值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-194">No default value.</span></span><br/></td>
<td><span data-ttu-id="2c91d-195">表示用來表示參數的單位。</span><span class="sxs-lookup"><span data-stu-id="2c91d-195">Indicates the units in which the parameter is expressed.</span></span> <span data-ttu-id="2c91d-196">例如，以十分之一度為單位的角度、microns 中的長度等等。</span><span class="sxs-lookup"><span data-stu-id="2c91d-196">For example, angles in tenths of degrees, lengths in microns, and so on.</span></span><br/></td>
<td><span data-ttu-id="2c91d-197">Yes</span><span class="sxs-lookup"><span data-stu-id="2c91d-197">Yes</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a><span data-ttu-id="2c91d-198">多個筆記</span><span class="sxs-lookup"><span data-stu-id="2c91d-198">Notes on Multiple</span></span>

<span data-ttu-id="2c91d-199">對於具有整數或十進位值的 ParameterInit 元素，ParameterInit 的值應該是此數位的倍數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-199">For ParameterInit elements with integer or decimal values, the value of the ParameterInit should be a multiple of this number.</span></span> <span data-ttu-id="2c91d-200">例如，您可以將此屬性設定為0.1，將十進位值 ParameterInit 元素限制為十分之一。</span><span class="sxs-lookup"><span data-stu-id="2c91d-200">For example, decimal-valued ParameterInit elements can be limited to tenths by setting this property to 0.1.</span></span> <span data-ttu-id="2c91d-201">UI 元素在建立對話方塊和 UI 控制項時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2c91d-201">UI elements use this Property when they construct dialogs and UI controls.</span></span> <span data-ttu-id="2c91d-202">此外，PrintTicket 驗證程式代碼可以使用這個屬性，將 ParameterInit 的值四捨五入為多個指定的最接近值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-202">In addition, PrintTicket validation code can use this Property to round the value of a ParameterInit to the nearest value indicated by Multiple.</span></span> <span data-ttu-id="2c91d-203">注意：設備磁碟機與 PrintCapabilities 提供者不應假設 ParameterInit 值是此屬性值的倍數。</span><span class="sxs-lookup"><span data-stu-id="2c91d-203">Note: Device drivers and PrintCapabilities providers should not assume that ParameterInit values are multiples of this Property value.</span></span> <span data-ttu-id="2c91d-204">每個提供者都必須能夠將任意值舍入為最接近的可用值，因為可能是不同的提供者可能會為此屬性指定不同和衝突的值。</span><span class="sxs-lookup"><span data-stu-id="2c91d-204">Each provider must be able to round arbitrary values to the nearest useable value due to the possibility that different providers might specify different and conflicting values for this property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c91d-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c91d-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c91d-206">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2c91d-206">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





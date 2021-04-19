---
description: 所有符合 CIM 規範的執行都必須處理一組標準的限定詞。
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: 標準限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997509"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="a9f72-103">標準限定詞</span><span class="sxs-lookup"><span data-stu-id="a9f72-103">Standard Qualifiers</span></span>

<span data-ttu-id="a9f72-104">所有符合 CIM 規範的執行都必須處理一組標準的限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="a9f72-105">任何特定的物件都未列出所有的限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="a9f72-106">通常，擴充類別會提供額外的限定詞，以促進類別實例的布建和其他作業。</span><span class="sxs-lookup"><span data-stu-id="a9f72-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="a9f72-107">提供者必須負責強制執行限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="a9f72-108">WMI 不會強制執行限定詞，但只會使用它們來通知使用者屬性的使用方式。</span><span class="sxs-lookup"><span data-stu-id="a9f72-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="a9f72-109">WMI 符合 CIM 2.5 規格的規範。</span><span class="sxs-lookup"><span data-stu-id="a9f72-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="a9f72-110">限定詞有下列限制：</span><span class="sxs-lookup"><span data-stu-id="a9f72-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="a9f72-111">並非所有標準限定詞都可以一起使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="a9f72-112">並非所有的限定詞都可以套用至所有的結構，例如關聯或參考。</span><span class="sxs-lookup"><span data-stu-id="a9f72-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="a9f72-113">這些限制是在 [適用于] 清單中所識別。</span><span class="sxs-lookup"><span data-stu-id="a9f72-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="a9f72-114">針對特定的結構（例如關聯或參考），使用合法限定詞可能會進一步限制，因為某些限定詞是互斥的，使用一個限定詞可能表示對另一個限定詞的值有一些限制，依此類推。</span><span class="sxs-lookup"><span data-stu-id="a9f72-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="a9f72-115">這些使用規則已記載。</span><span class="sxs-lookup"><span data-stu-id="a9f72-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="a9f72-116">合法限定詞只會由屬性、方法、實例或子類別的實體（而不是透過關聯或參考）所繼承。</span><span class="sxs-lookup"><span data-stu-id="a9f72-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="a9f72-117">例如，參考不會繼承套用至屬性的 **MaxLen** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="a9f72-118">以下列出 WMI 標準限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="a9f72-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**抽象**</span><span class="sxs-lookup"><span data-stu-id="a9f72-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-120">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-121">適用于：類別、關聯、指示</span><span class="sxs-lookup"><span data-stu-id="a9f72-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="a9f72-122">指出類別是否為抽象，而且只作為新類別的基底。</span><span class="sxs-lookup"><span data-stu-id="a9f72-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="a9f72-123">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-123">The default is **FALSE**.</span></span> <span data-ttu-id="a9f72-124">您無法建立抽象類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="a9f72-125">缺少這個辨識符號表示類別不是抽象的，因此，所有抽象類別都需要此限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**骨料**</span><span class="sxs-lookup"><span data-stu-id="a9f72-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-127">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-128">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-128">Applies to: references</span></span>

<span data-ttu-id="a9f72-129">指出參考是否為匯總關聯的父元件。</span><span class="sxs-lookup"><span data-stu-id="a9f72-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="a9f72-130">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-130">The default is **FALSE**.</span></span>

<span data-ttu-id="a9f72-131">使用方式： **匯總** 和 **匯總** 限定詞會一起使用   **，匯總會符合關聯** ，而 **Aggregate** 則會指定父系參考。</span><span class="sxs-lookup"><span data-stu-id="a9f72-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**聚集**</span><span class="sxs-lookup"><span data-stu-id="a9f72-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-133">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-134">適用于：關聯</span><span class="sxs-lookup"><span data-stu-id="a9f72-134">Applies to: associations</span></span>

<span data-ttu-id="a9f72-135">指出關聯是否為匯總。</span><span class="sxs-lookup"><span data-stu-id="a9f72-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="a9f72-136">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-136">The default is **FALSE**.</span></span> <span data-ttu-id="a9f72-137">搭配 **Aggregate** 使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-137">Used with **Aggregate**.</span></span> <span data-ttu-id="a9f72-138">所有匯總關聯都需要此限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**別名**</span><span class="sxs-lookup"><span data-stu-id="a9f72-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-140">Data type: **string**</span></span>

<span data-ttu-id="a9f72-141">適用物件：屬性、參考、方法</span><span class="sxs-lookup"><span data-stu-id="a9f72-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="a9f72-142">架構中屬性或方法的替代名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="a9f72-143">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="a9f72-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-145">Data type: **string**</span></span>

<span data-ttu-id="a9f72-146">適用物件：屬性、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="a9f72-147">限定陣列的型別。</span><span class="sxs-lookup"><span data-stu-id="a9f72-147">Type of the qualified array.</span></span>

<span data-ttu-id="a9f72-148">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a9f72-148">Valid values are:</span></span>

-   <span data-ttu-id="a9f72-149">包 (預設) </span><span class="sxs-lookup"><span data-stu-id="a9f72-149">bag (default)</span></span>
-   <span data-ttu-id="a9f72-150">索引</span><span class="sxs-lookup"><span data-stu-id="a9f72-150">indexed</span></span>
-   <span data-ttu-id="a9f72-151">排序</span><span class="sxs-lookup"><span data-stu-id="a9f72-151">ordered</span></span>

<span data-ttu-id="a9f72-152">使用方式：僅將這種類型的限定詞套用至屬性和參數，這些屬性和參數是使用括弧語法) 所定義 (陣列。</span><span class="sxs-lookup"><span data-stu-id="a9f72-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="a9f72-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-154">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-154">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-155">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-156">每個重要位置都可以是「開啟」或「關閉」的重要位位置對應。</span><span class="sxs-lookup"><span data-stu-id="a9f72-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="a9f72-157">每個 "on" 位會對應至 **BitValues** 陣列中的對應值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="a9f72-158">藉由將多個位「開啟」，則會指出 **BitValues** 陣列中的多個並行值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="a9f72-159">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-159">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-160">如需詳細資訊，請參閱 [點陣圖和 BitValues](bitmap-and-bitvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f72-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span><span class="sxs-lookup"><span data-stu-id="a9f72-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-162">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-162">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-163">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-164">將位位置值轉譯為相關聯的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="a9f72-165">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-165">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-166">如需詳細資訊，請參閱 [點陣圖和 BitValues](bitmap-and-bitvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f72-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**構造 函數**</span><span class="sxs-lookup"><span data-stu-id="a9f72-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-168">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-169">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="a9f72-169">Applies to: methods</span></span>

<span data-ttu-id="a9f72-170">指出方法是否建立實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="a9f72-171">這些方法不會限制為單一實例或單一類別的作用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="a9f72-172">例如，函式可以建立關聯實例，以及定義此函式之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="a9f72-173">「函式 **辨識符號」** 僅供資訊之用，不應該是由物件管理員處理。</span><span class="sxs-lookup"><span data-stu-id="a9f72-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="a9f72-174">物件管理員不需要在建立物件時呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="a9f72-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="a9f72-175">此外，呼叫函式時，物件管理員不需要叫用針對原始類別之任何父類別所定義的任何方法。</span><span class="sxs-lookup"><span data-stu-id="a9f72-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="a9f72-176">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span><span class="sxs-lookup"><span data-stu-id="a9f72-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-178">Data type: **string**</span></span>

<span data-ttu-id="a9f72-179">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-179">Applies to: classes</span></span>

<span data-ttu-id="a9f72-180">用來建立此類別之實例的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="a9f72-181">值可以是 "PutInstance" 或另一個建立實例的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="a9f72-182">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-182">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-183">使用方式：只有在 **SupportsCreate** 限定詞存在時，才能使用這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span><span class="sxs-lookup"><span data-stu-id="a9f72-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-185">Data type: **string**</span></span>

<span data-ttu-id="a9f72-186">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-186">Applies to: classes</span></span>

<span data-ttu-id="a9f72-187">用來刪除這個類別之實例的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="a9f72-188">值為 "DeleteInstance" 或另一個刪除實例之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="a9f72-189">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-189">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-190">使用方式：只有在 **SupportsDelete** 限定詞存在時，才能使用這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a9f72-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-192">Data type: **string**</span></span>

<span data-ttu-id="a9f72-193">適用于： any</span><span class="sxs-lookup"><span data-stu-id="a9f72-193">Applies to: any</span></span>

<span data-ttu-id="a9f72-194">命名元素的描述。</span><span class="sxs-lookup"><span data-stu-id="a9f72-194">Description of a named element.</span></span> <span data-ttu-id="a9f72-195">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**析 構 函數**</span><span class="sxs-lookup"><span data-stu-id="a9f72-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-197">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-197">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-198">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="a9f72-198">Applies to: methods</span></span>

<span data-ttu-id="a9f72-199">指出方法是否刪除實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="a9f72-200">使用「 **函** 式」限定詞辨識符號的方法會刪除套用了「函式」 () 的實例，而不會限制在單一實例或類別上的作用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="a9f72-201">例如，函式可能會刪除關聯實例，以及定義此函式之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="a9f72-202">「 **函** 式辨識符號」僅供資訊之用，不應該是由物件管理員處理。</span><span class="sxs-lookup"><span data-stu-id="a9f72-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="a9f72-203">當刪除實例時，物件管理員不會呼叫具有「 **函** 式」限定詞的方法。</span><span class="sxs-lookup"><span data-stu-id="a9f72-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="a9f72-204">此外，呼叫函式時，物件管理員不需要叫用針對原始類別之任何父類別所定義的任何析構函數方法。</span><span class="sxs-lookup"><span data-stu-id="a9f72-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="a9f72-205">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a9f72-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-207">Data type: **string**</span></span>

<span data-ttu-id="a9f72-208">適用于： any</span><span class="sxs-lookup"><span data-stu-id="a9f72-208">Applies to: any</span></span>

<span data-ttu-id="a9f72-209">在 UI 中顯示的名稱，而非元素的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="a9f72-210">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span><span class="sxs-lookup"><span data-stu-id="a9f72-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-212">Data type: **string**</span></span>

<span data-ttu-id="a9f72-213">適用于： any</span><span class="sxs-lookup"><span data-stu-id="a9f72-213">Applies to: any</span></span>

<span data-ttu-id="a9f72-214">限定的字串類型元素包含內嵌的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="a9f72-215">限定詞值會在與擁有限定專案之類別相同的命名空間中，指定 CIM 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="a9f72-216">內嵌實例是指定類別的實例，包括其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="a9f72-217">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**表**</span><span class="sxs-lookup"><span data-stu-id="a9f72-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-219">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-220">適用于： any</span><span class="sxs-lookup"><span data-stu-id="a9f72-220">Applies to: any</span></span>

<span data-ttu-id="a9f72-221">指出屬性是否代表非負整數，這可能會增加或減少，但絕不會超過最大值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="a9f72-222">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-222">The default is **FALSE**.</span></span>

<span data-ttu-id="a9f72-223">屬性的最大值不能大於 2 ^*n* -1。</span><span class="sxs-lookup"><span data-stu-id="a9f72-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="a9f72-224">*N* 可以是8、16、32或64，這取決於套用此限定詞之屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a9f72-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="a9f72-225">當模型化的資訊大於或等於最大值時，量測計的值會有其最大值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="a9f72-226">如果隨後將模型化的資訊減少到最大值，量測計也會減少。</span><span class="sxs-lookup"><span data-stu-id="a9f72-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="a9f72-227">此限定詞只適用于具有不帶正負號的整數資料類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9f72-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**在**</span><span class="sxs-lookup"><span data-stu-id="a9f72-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-229">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-229">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-230">適用于：參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-230">Applies to: parameters</span></span>

<span data-ttu-id="a9f72-231">指出參數是否用來將值傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="a9f72-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="a9f72-232">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In、Out**</span><span class="sxs-lookup"><span data-stu-id="a9f72-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-234">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-234">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-235">適用于：參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-235">Applies to: parameters</span></span>

<span data-ttu-id="a9f72-236">指出參數是否為輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="a9f72-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**關鍵**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="a9f72-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-238">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-238">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-239">適用物件：屬性、參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-239">Applies to: properties, references</span></span>

<span data-ttu-id="a9f72-240">指出屬性是否為命名空間控制碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="a9f72-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="a9f72-241">如果有一個以上的屬性具有索引 [**鍵**](key-qualifier.md) 限定詞，則所有這類屬性統稱 (複合索引鍵) 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="a9f72-242">在一起時，索引鍵屬性必須提供每個類別實例的唯一參考。</span><span class="sxs-lookup"><span data-stu-id="a9f72-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="a9f72-243">如果將這個限定詞放置在屬性上，則只允許值 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**懶惰**</span><span class="sxs-lookup"><span data-stu-id="a9f72-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-245">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-245">Applies to: properties</span></span>

<span data-ttu-id="a9f72-246">指出屬性需要大量資源才能傳回，而且需要大量的處理器時間和記憶體。</span><span class="sxs-lookup"><span data-stu-id="a9f72-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="a9f72-247">WMI 藉由不嘗試傳回以 **延遲** 辨識符號標記的屬性，來改善查詢的效能。</span><span class="sxs-lookup"><span data-stu-id="a9f72-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span><span class="sxs-lookup"><span data-stu-id="a9f72-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-249">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-249">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-250">適用物件：類別、屬性、關聯、指示、參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="a9f72-251">值的集合，表示位置的路徑，您可以在這裡找到有關屬性、類別、關聯、指示或參考之來源的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a9f72-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="a9f72-252">對應字串可以是目錄路徑、URL、登錄機碼、包含檔、CIM 類別的參考，或是其他格式。</span><span class="sxs-lookup"><span data-stu-id="a9f72-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="a9f72-253">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**麥克斯**</span><span class="sxs-lookup"><span data-stu-id="a9f72-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-255">資料類型： **int**</span><span class="sxs-lookup"><span data-stu-id="a9f72-255">Data type: **int**</span></span>

<span data-ttu-id="a9f72-256">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-256">Applies to: references</span></span>

<span data-ttu-id="a9f72-257">在關聯中，指定參考可以有每一組其他參考值的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="a9f72-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="a9f72-258">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-258">The default is **NULL**.</span></span> <span data-ttu-id="a9f72-259">例如，如果關聯將實例與 B 實例相關聯，而且每個 B 實例最多隻能有一個實例，則的參考最多應該有一個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="a9f72-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-261">資料類型： **int**</span><span class="sxs-lookup"><span data-stu-id="a9f72-261">Data type: **int**</span></span>

<span data-ttu-id="a9f72-262">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-263">**字串** 資料項目的字元) 長度上限 (，並指出固定長度陣列的支援。</span><span class="sxs-lookup"><span data-stu-id="a9f72-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="a9f72-264">如果遇到固定長度的陣列， **MaxLen** 限定詞會包含剖析期間所找到的固定長度。</span><span class="sxs-lookup"><span data-stu-id="a9f72-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="a9f72-265">如果遇到可變長度的陣列，則不會使用這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="a9f72-266">**MaxLen** 可用來建議應儲存在陣列中的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="a9f72-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="a9f72-267">覆寫預設值時，可以指定任何不帶正負號的整數值 (**uint32**) 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="a9f72-268">**Null** 值 (預設值) 表示不限長度。</span><span class="sxs-lookup"><span data-stu-id="a9f72-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**Timespan.maxvalue**</span><span class="sxs-lookup"><span data-stu-id="a9f72-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-270">資料類型： **int**</span><span class="sxs-lookup"><span data-stu-id="a9f72-270">Data type: **int**</span></span>

<span data-ttu-id="a9f72-271">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-272">物件的最大值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-272">Maximum value of the object.</span></span> <span data-ttu-id="a9f72-273">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**化**</span><span class="sxs-lookup"><span data-stu-id="a9f72-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-275">資料類型： **int**</span><span class="sxs-lookup"><span data-stu-id="a9f72-275">Data type: **int**</span></span>

<span data-ttu-id="a9f72-276">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-276">Applies to: references</span></span>

<span data-ttu-id="a9f72-277">參考的最小基數 (指定的參考可對關聯) 中的每個其他參考值設定的最小值數目。</span><span class="sxs-lookup"><span data-stu-id="a9f72-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="a9f72-278">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="a9f72-278">The default is 0.</span></span>

<span data-ttu-id="a9f72-279">例如，如果關聯將實例與 B 實例相關聯，而且每個 B 實例至少必須有一個實例，則的參考應該至少有一個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="a9f72-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-281">資料類型： **int**</span><span class="sxs-lookup"><span data-stu-id="a9f72-281">Data type: **int**</span></span>

<span data-ttu-id="a9f72-282">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-283">指出物件的最小值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="a9f72-284">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span><span class="sxs-lookup"><span data-stu-id="a9f72-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-286">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-286">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-287">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-287">Applies to: properties</span></span>

<span data-ttu-id="a9f72-288">值的集合，指出物件的屬性和 CIM 架構中的其他屬性之間的對應。</span><span class="sxs-lookup"><span data-stu-id="a9f72-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="a9f72-289">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-289">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-290">物件屬性會使用下列語法來識別。</span><span class="sxs-lookup"><span data-stu-id="a9f72-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="a9f72-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="a9f72-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="a9f72-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**外地**</span><span class="sxs-lookup"><span data-stu-id="a9f72-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-293">Data type: **string**</span></span>

<span data-ttu-id="a9f72-294">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-294">Applies to: references</span></span>

<span data-ttu-id="a9f72-295">實例的位置，其值為 <*namespacetype*>：//<*namespacehandle*> 預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-296">使用方式：此限定詞不能與 **NonlocalType** 限定詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span><span class="sxs-lookup"><span data-stu-id="a9f72-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-298">Data type: **string**</span></span>

<span data-ttu-id="a9f72-299">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-299">Applies to: references</span></span>

<span data-ttu-id="a9f72-300">實例的位置類型。</span><span class="sxs-lookup"><span data-stu-id="a9f72-300">Type of location of an instance.</span></span> <span data-ttu-id="a9f72-301">其值為 <namespacetype> 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="a9f72-302">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-302">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-303">使用方式：此辨識符號不能與 **非本機** 辨識符號一起使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="a9f72-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-305">Data type: **string**</span></span>

<span data-ttu-id="a9f72-306">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-306">Applies to: properties</span></span>

<span data-ttu-id="a9f72-307">值，表示相關聯的屬性為 **Null** (屬性沒有有效或有意義的值) 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="a9f72-308">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-308">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-309">用來定義 **Null** 值的慣例和限制與適用于 **ValueMap** 辨識符號的慣例和限制相同。</span><span class="sxs-lookup"><span data-stu-id="a9f72-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="a9f72-310">注意：無法覆寫此限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="a9f72-311">允許子類別傳回不同于父類別的 **Null** 值是不合理的。</span><span class="sxs-lookup"><span data-stu-id="a9f72-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**擴展**</span><span class="sxs-lookup"><span data-stu-id="a9f72-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-313">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-313">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-314">適用于：參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-314">Applies to: parameters</span></span>

<span data-ttu-id="a9f72-315">指出參數是否會從方法傳回值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="a9f72-316">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**覆蓋**</span><span class="sxs-lookup"><span data-stu-id="a9f72-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-318">Data type: **string**</span></span>

<span data-ttu-id="a9f72-319">適用物件：屬性、方法、參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="a9f72-320">父類別或次級結構 (屬性、方法或參考) 由衍生類別中相同名稱的屬性、方法或參考所覆寫。</span><span class="sxs-lookup"><span data-stu-id="a9f72-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="a9f72-321">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-321">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-322">其格式為：</span><span class="sxs-lookup"><span data-stu-id="a9f72-322">The format is:</span></span>

<span data-ttu-id="a9f72-323">\[<*類別*>。 \] <*從屬結構*></span><span class="sxs-lookup"><span data-stu-id="a9f72-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="a9f72-324">如果省略類別名稱，則會將覆寫套用至類別階層中父類別的從屬結構。</span><span class="sxs-lookup"><span data-stu-id="a9f72-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="a9f72-325">使用方式：覆 **寫** 辨識符號只能根據相同的中繼模型來參考結構。</span><span class="sxs-lookup"><span data-stu-id="a9f72-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="a9f72-326">在覆寫操作期間，不允許變更結構名稱或簽章。</span><span class="sxs-lookup"><span data-stu-id="a9f72-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span><span class="sxs-lookup"><span data-stu-id="a9f72-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-328">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-328">Applies to: classes</span></span>

<span data-ttu-id="a9f72-329">指出子類別上的屬性值是否會覆寫父類別中的值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="a9f72-330">這項功能的含意是，如果您針對父類別執行查詢，而 **WHERE** 子句包含這個屬性，則父系必須傳回具有覆寫值的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="a9f72-331">因此，Windows 管理會調整傳送至父類別的查詢 **WHERE** 子句，以排除這個屬性的參考。</span><span class="sxs-lookup"><span data-stu-id="a9f72-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**傳播**</span><span class="sxs-lookup"><span data-stu-id="a9f72-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-333">Data type: **string**</span></span>

<span data-ttu-id="a9f72-334">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-334">Applies to: properties</span></span>

<span data-ttu-id="a9f72-335">要傳播之金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-335">Name of the key being propagated.</span></span> <span data-ttu-id="a9f72-336">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-336">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-337">使用這個辨識符號時，會假設具有包含類別做為其目標的參考上只存在一個弱式限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="a9f72-338">相關聯的屬性必須與弱式關聯另一端之類別中的限定詞所命名的屬性具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="a9f72-339">其格式為：</span><span class="sxs-lookup"><span data-stu-id="a9f72-339">The format is:</span></span>

<span data-ttu-id="a9f72-340">\[<*類別*>。 \] <*從屬結構*></span><span class="sxs-lookup"><span data-stu-id="a9f72-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="a9f72-341">使用方式：使用 **傳播** 的辨識符號時，必須使用值 **TRUE** 指定 [**金鑰**](key-qualifier.md)限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**讀**</span><span class="sxs-lookup"><span data-stu-id="a9f72-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-343">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-344">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-344">Applies to: properties</span></span>

<span data-ttu-id="a9f72-345">指出屬性是否可讀取。</span><span class="sxs-lookup"><span data-stu-id="a9f72-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="a9f72-346">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**必填**</span><span class="sxs-lookup"><span data-stu-id="a9f72-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-348">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-348">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-349">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-349">Applies to: properties</span></span>

<span data-ttu-id="a9f72-350">指出屬性是否需要非 null 值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="a9f72-351">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**修訂**</span><span class="sxs-lookup"><span data-stu-id="a9f72-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-353">Data type: **string**</span></span>

<span data-ttu-id="a9f72-354">適用于：類別、關聯、指示、架構</span><span class="sxs-lookup"><span data-stu-id="a9f72-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="a9f72-355">架構物件的次要修訂編號。</span><span class="sxs-lookup"><span data-stu-id="a9f72-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="a9f72-356">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-356">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-357">使用方式：使用 **修訂** 限定詞時，必須要有 **版本** 限定詞才能提供主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="a9f72-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**模式**</span><span class="sxs-lookup"><span data-stu-id="a9f72-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-359">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-359">Data type: **string**</span></span>

<span data-ttu-id="a9f72-360">適用物件：屬性、方法</span><span class="sxs-lookup"><span data-stu-id="a9f72-360">Applies to: properties, methods</span></span>

<span data-ttu-id="a9f72-361">定義功能的架構名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f72-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="a9f72-362">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**源**</span><span class="sxs-lookup"><span data-stu-id="a9f72-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-364">Data type: **string**</span></span>

<span data-ttu-id="a9f72-365">適用物件：類別、關聯、指示、參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="a9f72-366">實例的位置。</span><span class="sxs-lookup"><span data-stu-id="a9f72-366">Location of an instance.</span></span> <span data-ttu-id="a9f72-367">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-367">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-368">限定詞的值是 <*namespacetype*>：//<*namespacehandle*>。</span><span class="sxs-lookup"><span data-stu-id="a9f72-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="a9f72-369">使用方式： **來源** 辨識符號不能與 **SourceType** 限定詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="a9f72-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-371">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-371">Data type: **string**</span></span>

<span data-ttu-id="a9f72-372">適用物件：類別、關聯、指示、參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="a9f72-373">實例的位置類型。</span><span class="sxs-lookup"><span data-stu-id="a9f72-373">Type of location of an instance.</span></span> <span data-ttu-id="a9f72-374">此辨識符號的值是 <*namespacetype*>。</span><span class="sxs-lookup"><span data-stu-id="a9f72-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="a9f72-375">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-375">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-376">使用方式： **SourceType** 限定詞不能與 **來源** 辨識符號一起使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="a9f72-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-378">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-378">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-379">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-379">Applies to: classes</span></span>

<span data-ttu-id="a9f72-380">指出類別是否支援建立實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="a9f72-381">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="a9f72-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-383">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-383">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-384">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-384">Applies to: classes</span></span>

<span data-ttu-id="a9f72-385">指出類別是否支援刪除實例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="a9f72-386">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span><span class="sxs-lookup"><span data-stu-id="a9f72-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-388">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-388">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-389">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-389">Applies to: classes</span></span>

<span data-ttu-id="a9f72-390">指出類別是否支援修改 (更新實例) 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="a9f72-391">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**終端**</span><span class="sxs-lookup"><span data-stu-id="a9f72-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-393">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-393">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-394">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="a9f72-394">Applies to: classes</span></span>

<span data-ttu-id="a9f72-395">指出類別是否可以有子類別。</span><span class="sxs-lookup"><span data-stu-id="a9f72-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="a9f72-396">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-396">The default is **FALSE**.</span></span>

<span data-ttu-id="a9f72-397">如果已宣告子類別，則編譯器會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9f72-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="a9f72-398">使用方式：此限定詞不能與 **抽象** 辨識符號並存。</span><span class="sxs-lookup"><span data-stu-id="a9f72-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="a9f72-399">如果同時指定了 **終端** 機和 **抽象** 限定詞，則編譯器會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9f72-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**單位**</span><span class="sxs-lookup"><span data-stu-id="a9f72-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-401">Data type: **string**</span></span>

<span data-ttu-id="a9f72-402">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-403">用來表示相關聯資料項目的單位類型。</span><span class="sxs-lookup"><span data-stu-id="a9f72-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="a9f72-404">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-404">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-405">例如，大小資料項目的 **單位** 值可能為 "bytes"。</span><span class="sxs-lookup"><span data-stu-id="a9f72-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="a9f72-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-407">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-407">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-408">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-409">屬性、方法傳回型別或方法參數允許的值集。</span><span class="sxs-lookup"><span data-stu-id="a9f72-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="a9f72-410">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-410">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-411">使用方式：此限定詞可以單獨使用，也可以與 **值** 限定詞組合使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="a9f72-412">搭配 **values** 辨識符號使用時，在 **ValueMap** 陣列中的值位置會提供 **值** 陣列中對應專案的位置。</span><span class="sxs-lookup"><span data-stu-id="a9f72-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="a9f72-413">請僅使用具有字串和整數值的 **ValueMap** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="a9f72-414">在值地圖陣列中表示整數值的語法是 \[ + \| = \] 數位 \[ \* 數位 \] 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="a9f72-415">內容、最大位數和表示值會受限於相關聯屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="a9f72-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="a9f72-416">例如，uint8 可能未簽署、必須小於四位數，且必須代表小於256的值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-418">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="a9f72-418">Data type: **string array**</span></span>

<span data-ttu-id="a9f72-419">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="a9f72-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a9f72-420">將整數值轉譯為相關聯字串的一組值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="a9f72-421">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-421">The default is **NULL**.</span></span>

<span data-ttu-id="a9f72-422">這個屬性也會指定要對應至列舉屬性的字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="a9f72-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="a9f72-423">這個限定詞可以套用至整數屬性或字串屬性，而且對應可以是隱含或明確。</span><span class="sxs-lookup"><span data-stu-id="a9f72-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="a9f72-424">如果對應是隱含的，則整數或字串屬性值代表 **值** 陣列中的序數位置。</span><span class="sxs-lookup"><span data-stu-id="a9f72-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="a9f72-425">如果對應是明確的，則屬性必須是整數，而且有效的屬性值會列在由 **ValueMap** 辨識符號定義的陣列中。</span><span class="sxs-lookup"><span data-stu-id="a9f72-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="a9f72-426">如需詳細資訊，請參閱 [值對應](value-map.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f72-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="a9f72-427">如果不存在 **ValueMap** 辨識符號，則會使用相關聯的屬性、方法傳回型別或方法參數中的值，將 **值** 陣列索引 (零相對的) 。</span><span class="sxs-lookup"><span data-stu-id="a9f72-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="a9f72-428">如果有 **ValueMap** 辨識符號，則值索引是由值對應中的屬性值位置所定義。</span><span class="sxs-lookup"><span data-stu-id="a9f72-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本**</span><span class="sxs-lookup"><span data-stu-id="a9f72-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9f72-430">Data type: **string**</span></span>

<span data-ttu-id="a9f72-431">適用物件：類別、架構、關聯、指示</span><span class="sxs-lookup"><span data-stu-id="a9f72-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="a9f72-432">架構物件的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="a9f72-432">Major version number of the schema object.</span></span> <span data-ttu-id="a9f72-433">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-433">The default is **NULL**.</span></span> <span data-ttu-id="a9f72-434">變更介面的架構進行變更時，版本號碼會遞增。</span><span class="sxs-lookup"><span data-stu-id="a9f72-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**弱**</span><span class="sxs-lookup"><span data-stu-id="a9f72-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-436">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-436">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-437">適用于：參考</span><span class="sxs-lookup"><span data-stu-id="a9f72-437">Applies to: references</span></span>

<span data-ttu-id="a9f72-438">指出參考類別的索引鍵是否包含關聯中其他參與者的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a9f72-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="a9f72-439">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-439">The default is **FALSE**.</span></span>

<span data-ttu-id="a9f72-440">當參考類別的識別相依于關聯中其他參與者的身分識別時，會使用這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="a9f72-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="a9f72-441">任何一個指定類別的參考都不能是弱式。</span><span class="sxs-lookup"><span data-stu-id="a9f72-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="a9f72-442">關聯中的其他類別必須定義索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a9f72-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="a9f72-443">關聯中其他類別的索引鍵會在參考的類別中重複，並以 **傳播** 的辨識符號標記。</span><span class="sxs-lookup"><span data-stu-id="a9f72-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**寫**</span><span class="sxs-lookup"><span data-stu-id="a9f72-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-445">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-445">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-446">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-446">Applies to: properties</span></span>

<span data-ttu-id="a9f72-447">表示應用程式或腳本可以變更屬性值。</span><span class="sxs-lookup"><span data-stu-id="a9f72-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="a9f72-448">執行應用程式的帳戶必須能夠存取包含類別實例的命名空間。</span><span class="sxs-lookup"><span data-stu-id="a9f72-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="a9f72-449">提供者的執行也可能會限制對提供者資料的存取。</span><span class="sxs-lookup"><span data-stu-id="a9f72-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="a9f72-450">**TRUE** 值表示屬性可由 WMI 和提供者允許存取的取用者讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="a9f72-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="a9f72-451">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-451">The default is **FALSE**.</span></span>

<span data-ttu-id="a9f72-452">缺少 **寫入** 限定詞的屬性仍可寫入。</span><span class="sxs-lookup"><span data-stu-id="a9f72-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="a9f72-453">提供者的執行可能會讓提供者類別中的任何屬性變更，不論 **寫入** 限定詞是否存在。</span><span class="sxs-lookup"><span data-stu-id="a9f72-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span><span class="sxs-lookup"><span data-stu-id="a9f72-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-455">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-455">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-456">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-456">Applies to: properties</span></span>

<span data-ttu-id="a9f72-457">表示在建立實例時，是否可寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="a9f72-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="a9f72-458">此限定詞可與 **WriteAtCreate** 限定詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="a9f72-459">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9f72-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span><span class="sxs-lookup"><span data-stu-id="a9f72-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="a9f72-461">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9f72-461">Data type: **boolean**</span></span>

<span data-ttu-id="a9f72-462">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="a9f72-462">Applies to: properties</span></span>

<span data-ttu-id="a9f72-463">指出屬性在實例更新時是否可寫入。</span><span class="sxs-lookup"><span data-stu-id="a9f72-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="a9f72-464">此限定詞可與 **WriteAtCreate** 限定詞搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a9f72-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="a9f72-465">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a9f72-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a9f72-466">範例</span><span class="sxs-lookup"><span data-stu-id="a9f72-466">Examples</span></span>

<span data-ttu-id="a9f72-467">如需有關如何抓取限定詞的詳細資訊，請參閱 TechNet 資源庫上的 [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="a9f72-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f72-468">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f72-468">Requirements</span></span>



| <span data-ttu-id="a9f72-469">需求</span><span class="sxs-lookup"><span data-stu-id="a9f72-469">Requirement</span></span> | <span data-ttu-id="a9f72-470">值</span><span class="sxs-lookup"><span data-stu-id="a9f72-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a9f72-471">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9f72-471">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f72-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9f72-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a9f72-473">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9f72-473">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f72-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9f72-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9f72-475">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9f72-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f72-476">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="a9f72-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a9f72-477">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="a9f72-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 





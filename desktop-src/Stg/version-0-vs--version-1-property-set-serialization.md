---
title: 屬性集序列化
description: 屬性集序列化格式有兩個版本。
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c635728e169cdddb20437323a49a18496b3459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186022"
---
# <a name="property-set-serialization"></a><span data-ttu-id="b59a4-103">屬性集序列化</span><span class="sxs-lookup"><span data-stu-id="b59a4-103">Property Set Serialization</span></span>

<span data-ttu-id="b59a4-104">屬性集序列化格式有兩個版本。</span><span class="sxs-lookup"><span data-stu-id="b59a4-104">There are two versions of the property set serialization format.</span></span> <span data-ttu-id="b59a4-105">原始規格描述版本0的格式。</span><span class="sxs-lookup"><span data-stu-id="b59a4-105">The original specification describes version 0 of the format.</span></span> <span data-ttu-id="b59a4-106">如需詳細資訊，請參閱 [格式版本](format-version.md) 。</span><span class="sxs-lookup"><span data-stu-id="b59a4-106">See [Format Version](format-version.md) for more information.</span></span> <span data-ttu-id="b59a4-107">第1版延伸原始版本。</span><span class="sxs-lookup"><span data-stu-id="b59a4-107">Version 1 extends the original version.</span></span> <span data-ttu-id="b59a4-108">所有版本0屬性集都是有效的第1版屬性集。</span><span class="sxs-lookup"><span data-stu-id="b59a4-108">All version 0 property sets are valid as version 1 property sets.</span></span> <span data-ttu-id="b59a4-109">序列化屬性集標頭中的 [ **格式版本** ] 欄位表示版本。</span><span class="sxs-lookup"><span data-stu-id="b59a4-109">The **Format Version** field in the header of a serialized property set indicates the version.</span></span>

<span data-ttu-id="b59a4-110">下列專案會識別 version 0 和第1版屬性集序列化格式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="b59a4-110">The following items identify the differences between version 0 and version 1 property set serialization formats.</span></span>

-   <span data-ttu-id="b59a4-111">支援新的 **VARTYPE** 值。</span><span class="sxs-lookup"><span data-stu-id="b59a4-111">Support for new **VARTYPE** values.</span></span> <span data-ttu-id="b59a4-112">如需 **VARTYPE** 值和其使用方式的詳細資訊，請參閱 [IDispatch 資料類型和結構]( /previous-versions/ms221600(v=vs.100)) 和 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構主題。</span><span class="sxs-lookup"><span data-stu-id="b59a4-112">For more information about **VARTYPE** values and how to use them, see the topic [IDispatch Data Types and Structures]( /previous-versions/ms221600(v=vs.100)) and the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

    <span data-ttu-id="b59a4-113">版本0屬性集不支援下列 **VARTYPE** 值，但在第1版中支援：</span><span class="sxs-lookup"><span data-stu-id="b59a4-113">The following **VARTYPE** values are not supported in version 0 property sets, but are supported in version 1:</span></span>

    <span data-ttu-id="b59a4-114">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="b59a4-114">VT\_I1</span></span>

    <span data-ttu-id="b59a4-115">VT \_ 向量 \| vt \_ I1</span><span class="sxs-lookup"><span data-stu-id="b59a4-115">VT\_VECTOR \| VT\_I1</span></span>

    <span data-ttu-id="b59a4-116">VT \_ INT</span><span class="sxs-lookup"><span data-stu-id="b59a4-116">VT\_INT</span></span>

    <span data-ttu-id="b59a4-117">VT \_ UINT</span><span class="sxs-lookup"><span data-stu-id="b59a4-117">VT\_UINT</span></span>

    <span data-ttu-id="b59a4-118">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b59a4-118">VT\_DECIMAL</span></span>

    <span data-ttu-id="b59a4-119">此外，Safearray 也可以在屬性集內進行序列化。</span><span class="sxs-lookup"><span data-stu-id="b59a4-119">Additionally, SafeArrays can be serialized in a property set.</span></span> <span data-ttu-id="b59a4-120">SafeArray 的出現是由 \_ 使用 **OR** 運算的 vt 陣列位所表示，並搭配 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的陣列元素。</span><span class="sxs-lookup"><span data-stu-id="b59a4-120">The presence of a SafeArray is indicated by the VT\_ARRAY bit combined, using an **OR** operation, with the array elements in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span> <span data-ttu-id="b59a4-121">例如，4位元組帶正負號整數的 SafeArray 有一種 VT \_ 陣列 \| vt \_ I4。</span><span class="sxs-lookup"><span data-stu-id="b59a4-121">For example, a SafeArray of 4-byte signed integers has a type of VT\_ARRAY \| VT\_I4.</span></span>

    <span data-ttu-id="b59a4-122">下列元素類型對序列化屬性集中的 SafeArray 有效：</span><span class="sxs-lookup"><span data-stu-id="b59a4-122">The following element types are valid for a SafeArray in a serialized property set:</span></span>



|             |          |             |           |
|-------------|----------|-------------|-----------|
| <span data-ttu-id="b59a4-123">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="b59a4-123">VT\_I1</span></span>      | <span data-ttu-id="b59a4-124">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="b59a4-124">VT\_UI1</span></span>  | <span data-ttu-id="b59a4-125">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="b59a4-125">VT\_I2</span></span>      | <span data-ttu-id="b59a4-126">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="b59a4-126">VT\_UI2</span></span>   |
| <span data-ttu-id="b59a4-127">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b59a4-127">VT\_I4</span></span>      | <span data-ttu-id="b59a4-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b59a4-128">VT\_UI4</span></span>  | <span data-ttu-id="b59a4-129">VT \_ INT</span><span class="sxs-lookup"><span data-stu-id="b59a4-129">VT\_INT</span></span>     | <span data-ttu-id="b59a4-130">VT \_ UINT</span><span class="sxs-lookup"><span data-stu-id="b59a4-130">VT\_UINT</span></span>  |
| <span data-ttu-id="b59a4-131">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="b59a4-131">VT\_R4</span></span>      | <span data-ttu-id="b59a4-132">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b59a4-132">VT\_R8</span></span>   | <span data-ttu-id="b59a4-133">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="b59a4-133">VT\_CY</span></span>      | <span data-ttu-id="b59a4-134">VT \_ 日期</span><span class="sxs-lookup"><span data-stu-id="b59a4-134">VT\_DATE</span></span>  |
| <span data-ttu-id="b59a4-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="b59a4-135">VT\_BSTR</span></span>    | <span data-ttu-id="b59a4-136">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="b59a4-136">VT\_BOOL</span></span> | <span data-ttu-id="b59a4-137">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b59a4-137">VT\_DECIMAL</span></span> | <span data-ttu-id="b59a4-138">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="b59a4-138">VT\_ERROR</span></span> |
| <span data-ttu-id="b59a4-139">VT \_ 變異</span><span class="sxs-lookup"><span data-stu-id="b59a4-139">VT\_VARIANT</span></span> |          |             |           |



 

<span data-ttu-id="b59a4-140">\_指定 VT VARIANT 資料類型時，它會指出 SafeArray 本身會保存 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構。</span><span class="sxs-lookup"><span data-stu-id="b59a4-140">When the VT\_VARIANT data type is specified, it indicates that the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="b59a4-141">這些元素的類型必須來自于上述清單，但它們不能包含嵌套的 VT \_ 變異類型。</span><span class="sxs-lookup"><span data-stu-id="b59a4-141">The types for these elements must be from the preceding list, except they cannot contain nested VT\_VARIANT types.</span></span>

<span data-ttu-id="b59a4-142">請注意， [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行必須能夠在遇到新類型時傳回錯誤，以順利復原。例如，VARENUM 類型。</span><span class="sxs-lookup"><span data-stu-id="b59a4-142">Note that implementations of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) must be able to recover gracefully by returning an error when a new type is encountered; for example, VARENUM types.</span></span>

-   <span data-ttu-id="b59a4-143">區分大小寫的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="b59a4-143">Case sensitive property names.</span></span> <span data-ttu-id="b59a4-144">屬性名稱（例如，在 [**IPropertyStorage：： WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) 方法中指定的名稱）在版本0屬性集中不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b59a4-144">Property names, for example those specified in the [**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) method, are not case sensitive in version 0 property sets.</span></span> <span data-ttu-id="b59a4-145">在第1版的屬性集中，屬性名稱可能會區分大小寫，端視新的行為屬性的值而定。</span><span class="sxs-lookup"><span data-stu-id="b59a4-145">In version 1 property sets, property names can be case-sensitive depending on the value of the new Behavior property.</span></span>

    <span data-ttu-id="b59a4-146">行為屬性是具有 VT UI4 類型的 [屬性識別碼 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) \_ 。</span><span class="sxs-lookup"><span data-stu-id="b59a4-146">The Behavior property is [Property ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) with a type of VT\_UI4.</span></span> <span data-ttu-id="b59a4-147">如果設定此值的最小位，屬性集名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b59a4-147">If the lowest bit of this value is set, the property set names are case sensitive.</span></span> <span data-ttu-id="b59a4-148">\_ \_ 在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)方法的 *grfFlags* 參數中，設定區分大小寫的 PROPSETFLAG 旗標，以指定區分大小寫的屬性集。</span><span class="sxs-lookup"><span data-stu-id="b59a4-148">Set the PROPSETFLAG\_CASE\_SENSITIVE flag in the *grfFlags* parameter of the [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) method to specify a case-sensitive property set.</span></span>

-   <span data-ttu-id="b59a4-149">長屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="b59a4-149">Long property names.</span></span> <span data-ttu-id="b59a4-150">版本0屬性集的屬性名稱必須小於或等於256個字元，包括字串結束字元（適用于 Unicode 字碼頁中的屬性集）。</span><span class="sxs-lookup"><span data-stu-id="b59a4-150">Property names for version 0 property sets must be less than or equal to 256 characters, including the string terminator, for property sets in the Unicode code page.</span></span> <span data-ttu-id="b59a4-151">如果不在 Unicode 字碼頁中，則必須小於256個位元組。</span><span class="sxs-lookup"><span data-stu-id="b59a4-151">If not in the Unicode code page, they must be less than 256 bytes.</span></span> <span data-ttu-id="b59a4-152">另一方面，第1版屬性集會擁有無限制長度的屬性名稱，不過它們仍受限於 256 kb 的整體屬性集大小限制 (KB) 。</span><span class="sxs-lookup"><span data-stu-id="b59a4-152">Version 1 property sets, on the other hand, can have property names of unlimited length, although they are still limited by the overall property set size limit of 256 kilobytes (KB).</span></span>

<span data-ttu-id="b59a4-153">建議 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行預設會建立和維護第0版的屬性集。</span><span class="sxs-lookup"><span data-stu-id="b59a4-153">It is recommended that implementations of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) create and maintain version 0 property sets by default.</span></span> <span data-ttu-id="b59a4-154">如果呼叫端隨後要求第1版格式的特定功能，則只應該更新屬性集的版本。</span><span class="sxs-lookup"><span data-stu-id="b59a4-154">If a caller subsequently requests a feature specific to the version 1 format, only then should the version of the property set be updated.</span></span> <span data-ttu-id="b59a4-155">例如，如果撰寫型別 VT 陣列的屬性 \_ ，或寫入 long 屬性名稱，則實作為應將屬性集格式更新為第1版。</span><span class="sxs-lookup"><span data-stu-id="b59a4-155">For example, if a property of type VT\_ARRAY is written or if a long property name is written, then the implementation should update the property set format to version 1.</span></span> <span data-ttu-id="b59a4-156">如果在 \_ \_ [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的呼叫中指定 PROPSETFLAG 區分大小寫的列舉值，就會發生這個指導方針的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b59a4-156">One exception to this guideline occurs if the PROPSETFLAG\_CASE\_SENSITIVE enumeration value is specified in the call to [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span></span> <span data-ttu-id="b59a4-157">在此情況下，必須將屬性集建立為第1版屬性集。</span><span class="sxs-lookup"><span data-stu-id="b59a4-157">In this case, the property set must be created as a version 1 property set.</span></span>

 

 
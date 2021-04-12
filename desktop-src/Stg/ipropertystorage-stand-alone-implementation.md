---
title: IPropertyStorage-獨立執行
description: 系統提供的 IPropertySetStorage 獨立實作為 IPropertyStorage 的執行，此介面會在屬性集儲存體中讀取和寫入屬性。
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-獨立執行
- IPropertyStorage Strctd Stg.，獨立部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375653"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="4ed6c-105">IPropertyStorage-獨立執行</span><span class="sxs-lookup"><span data-stu-id="4ed6c-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="4ed6c-106">系統提供的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 獨立實作為 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的執行，此介面會在屬性集儲存體中讀取和寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="4ed6c-107">**IPropertySetStorage** 介面會在儲存體中建立並開啟屬性集。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="4ed6c-108">[**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)和 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面也會在獨立的執行中提供。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="4ed6c-109">若要取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)之獨立執行的指標，請呼叫 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)函式來建立新的屬性集或 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) ，以取得現有屬性集的介面指標 (或呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)獨立執行) 的 [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)或 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="4ed6c-110">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行會在任何儲存或資料流程物件上建立屬性集，而不只是在複合檔案儲存和資料流程上。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="4ed6c-111">獨立的執行不相依于複合檔案，並且可搭配任何結構化儲存體的執行使用。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="4ed6c-112">如需此介面之複合檔案執行的詳細資訊，請參閱 [IPropertyStorage 複合檔案執行](ipropertystorage-compound-file-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4ed6c-113">使用時機</span><span class="sxs-lookup"><span data-stu-id="4ed6c-113">When to Use</span></span>

<span data-ttu-id="4ed6c-114">使用 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 來管理單一屬性集內的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="4ed6c-115">其方法支援讀取、寫入和刪除屬性，以及可與屬性識別碼相關聯的選擇性字串名稱。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="4ed6c-116">其他方法支援標準認可和還原儲存體作業。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="4ed6c-117">另外還有一種方法可設定與屬性儲存體相關聯的時間，另一種方法則允許指派 CLSID 來將其他程式碼（例如使用者介面程式碼）與屬性集建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="4ed6c-118">[**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)方法會提供 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)之獨立執行的指標，它會列舉集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="4ed6c-119">版本0和第1版屬性集格式</span><span class="sxs-lookup"><span data-stu-id="4ed6c-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="4ed6c-120">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行同時支援 version 0 和 version 1 property set 序列化格式。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="4ed6c-121">如需詳細資訊，請參閱 [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="4ed6c-122">除非要求新功能，否則會以 version 0 格式建立屬性集，並保留該格式。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="4ed6c-123">屆時，格式會更新為第1版。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="4ed6c-124">例如，如果使用 PROPSETFLAG 預設旗標建立屬性集 \_ ，其格式為0版。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="4ed6c-125">只要符合版本0格式的屬性類型會寫入至該屬性集並從該屬性集讀取，屬性集會維持為版本0格式。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="4ed6c-126">如果第1版屬性類型寫入屬性集，屬性集會自動更新為第1版。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="4ed6c-127">之後，只有瞭解0版的執行，就無法再讀取該屬性集。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="4ed6c-128">IPropertyStorage 和 Variant 類型</span><span class="sxs-lookup"><span data-stu-id="4ed6c-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="4ed6c-129">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行不支援在 \_ \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **vt** 成員中，以 vt 未知或 vt 的 variant 類型。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="4ed6c-130">SafeArray 內支援下列 variant 類型：也就是說，這些值可以與 \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的 vt 陣列合併。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="4ed6c-131">IPropertyStorage 的複合檔案執行在 SafeArray 內支援的 Variant 類型[ ](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="4ed6c-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="4ed6c-132">VT\_I1</span></span>

<span data-ttu-id="4ed6c-133">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="4ed6c-133">VT\_UI1</span></span>

<span data-ttu-id="4ed6c-134">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="4ed6c-134">VT\_I2</span></span>

<span data-ttu-id="4ed6c-135">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="4ed6c-135">VT\_UI2</span></span>

<span data-ttu-id="4ed6c-136">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4ed6c-136">VT\_I4</span></span>

<span data-ttu-id="4ed6c-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4ed6c-137">VT\_UI4</span></span>

<span data-ttu-id="4ed6c-138">VT \_ INT</span><span class="sxs-lookup"><span data-stu-id="4ed6c-138">VT\_INT</span></span>

<span data-ttu-id="4ed6c-139">VT \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4ed6c-139">VT\_UINT</span></span>

<span data-ttu-id="4ed6c-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="4ed6c-140">VT\_R4</span></span>

<span data-ttu-id="4ed6c-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4ed6c-141">VT\_R8</span></span>

<span data-ttu-id="4ed6c-142">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="4ed6c-142">VT\_CY</span></span>

<span data-ttu-id="4ed6c-143">VT \_ 日期</span><span class="sxs-lookup"><span data-stu-id="4ed6c-143">VT\_DATE</span></span>

<span data-ttu-id="4ed6c-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="4ed6c-144">VT\_BSTR</span></span>

<span data-ttu-id="4ed6c-145">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="4ed6c-145">VT\_BOOL</span></span>

<span data-ttu-id="4ed6c-146">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="4ed6c-146">VT\_DECIMAL</span></span>

<span data-ttu-id="4ed6c-147">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="4ed6c-147">VT\_ERROR</span></span>

<span data-ttu-id="4ed6c-148">VT \_ 變異</span><span class="sxs-lookup"><span data-stu-id="4ed6c-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="4ed6c-149">當 VT \_ VARIANT 與 vt 陣列合併時 \_ ，SafeArray 本身會保存 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="4ed6c-150">不過，這些元素的類型必須取自上述清單，不能是 VT \_ 變異，也不能包含 vt \_ 向量、vt \_ 陣列或 vt \_ BYREF 指標。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="4ed6c-151">IPropertyStorage 方法</span><span class="sxs-lookup"><span data-stu-id="4ed6c-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="4ed6c-152">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的獨立執行支援下列方法：</span><span class="sxs-lookup"><span data-stu-id="4ed6c-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="4ed6c-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-154">讀取 *rgpspec* 陣列中所指定的屬性，並在 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)元素的 *rgvar* 陣列中提供所有有效屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="4ed6c-155">在系統提供的獨立執行中，參考資料流或儲存類型的重複屬性識別碼會導致多個對 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 或 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 的呼叫，而 [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 的成功或失敗取決於基礎儲存體實作為共用開啟儲存體的能力。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="4ed6c-156">此外，若要確保安全線程作業，如果相同的資料流程或儲存值屬性透過相同的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 指標多次要求，則會根據屬性是否已開啟，以及基礎檔案系統是否處理多個資料流程或儲存區的開啟而定，開啟會成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="4ed6c-157">因此，在資料流程或儲存值屬性上的 [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 作業一律會導致呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)或 [**IStorage：： OPENSTORAGE**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)，傳遞存取 (STGM \_ READWRITE，例如) 和共用值 (STGM \_ 共用 \_ 獨佔，例如在最初開啟或建立屬性集時所指定) 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="4ed6c-158">如果方法失敗，寫入 *rgvar* 的值 \[ \] 就不會定義。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="4ed6c-159">如果已成功開啟部分資料流程或儲存值屬性，但執行完成之前發生錯誤，則應該在方法傳回之前釋放這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-161">寫入 *rgpspec* 陣列中指定的屬性 \[ \] ，並將 *rgvar* 中指定的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)標記和值指派給它們 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="4ed6c-162">已存在的屬性會指派指定的 **PROPVARIANT** 值，而且不會建立目前存在的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage：:D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-164">刪除在 *rgpspec* 中指定的屬性 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-166">讀取與 *rgpropid* 陣列中所指定屬性識別碼相關聯的現有字串名稱 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-168">將 *rglpwstrName* 陣列中指定的字串名稱指派給 *rgpropid* 陣列中所指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage：:D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-170">藉由將 **Null** 寫入屬性名稱，來刪除 *rgpropid* 陣列中所指定之屬性識別碼的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-172">設定屬性集資料流程的 **CLSID** 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="4ed6c-173">在獨立的執行中，在簡單屬性集上設定 CLSID (其中一個可以包含儲存或資料流程值屬性（如 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) 中所述）也會在基礎 substorage 上設定 clsid，以便透過呼叫 [**IStorage：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)來取得它。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-175">針對簡單和簡單的屬性集，將記憶體映射排清到磁片子系統。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="4ed6c-176">此外，針對簡單交易模式屬性集，這個方法會在屬性集上呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage：： Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-178">僅針對簡單屬性集，會呼叫基礎儲存體的 [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) 方法，並重新開啟「內容」資料流程。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="4ed6c-179">針對簡單的屬性集，只會傳回 E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-181">建立會執行 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的列舉值物件，您可以呼叫這些方法來列舉 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，以提供集合中每個屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="4ed6c-182">這項執行會建立一個陣列，以讀取整個屬性集，並在呼叫 [**IEnumSTATPROPSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 時共用。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage：： Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-184">填入 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的成員，其中包含整個屬性集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="4ed6c-185">傳回時，提供結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="4ed6c-186">針對簡單儲存集，此實作為呼叫 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (或 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) ，以從基礎儲存體或資料流程取得資訊。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="4ed6c-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="4ed6c-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="4ed6c-188">僅針對簡單屬性集，設定基礎儲存體所支援的時間。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="4ed6c-189">這項 [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) 的執行會呼叫基礎儲存體的 [**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) 方法，以修改時間。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="4ed6c-190">它支援基礎方法支援的時間，可能是修改時間、存取時間或建立時間。</span><span class="sxs-lookup"><span data-stu-id="4ed6c-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4ed6c-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ed6c-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed6c-192">IPropertySetStorage-獨立執行</span><span class="sxs-lookup"><span data-stu-id="4ed6c-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="4ed6c-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="4ed6c-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="4ed6c-194">**IStorage：： SetElementTimes**</span><span class="sxs-lookup"><span data-stu-id="4ed6c-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="4ed6c-195">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="4ed6c-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="4ed6c-196">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="4ed6c-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="4ed6c-197">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="4ed6c-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 
---
title: IPropertySetStorage-NTFS 檔案系統執行
description: 當檔案本身不是複合檔案時，NTFS 5.0 版可針對 NTFS 磁片區上的檔案提供 IPropertySetStorage 的執行。
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd Stg.、、NTFS 檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999589"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a><span data-ttu-id="57b0e-104">IPropertySetStorage-NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="57b0e-104">IPropertySetStorage-NTFS File System Implementation</span></span>

<span data-ttu-id="57b0e-105">當檔案本身不是複合檔案時，NTFS 5.0 版可針對 NTFS 磁片區上的檔案提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的執行。</span><span class="sxs-lookup"><span data-stu-id="57b0e-105">NTFS version 5.0 provides an implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for files on an NTFS volume when the files themselves are not compound files.</span></span> <span data-ttu-id="57b0e-106">NTFS 執行相當於 [複合檔案執行](ipropertysetstorage-compound-file-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="57b0e-106">The NTFS implementation is equivalent to the [compound file implementation](ipropertysetstorage-compound-file-implementation.md).</span></span> <span data-ttu-id="57b0e-107">如需例外狀況的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="57b0e-107">For more information about exceptions, see Remarks.</span></span>

<span data-ttu-id="57b0e-108">**若要取得 IPropertySetStorage NTFS 執行的指標**</span><span class="sxs-lookup"><span data-stu-id="57b0e-108">**To get a pointer to the NTFS implementation of IPropertySetStorage**</span></span>

1.  <span data-ttu-id="57b0e-109">呼叫 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)並在 *grfFlags* 參數中指定 STGFMT 檔案，以建立新的檔案。 **\_**</span><span class="sxs-lookup"><span data-stu-id="57b0e-109">Call [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) and specify **STGFMT\_FILE** in the *grfFlags* parameter to create a new file.</span></span>
2.  <span data-ttu-id="57b0e-110">呼叫 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)並指定 STGFMT 檔案 **， \_** 或 STGFMT *grfFlags* 參數中的 **\_ 任何** 列舉值，以開啟現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="57b0e-110">Call [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) and specify either the **STGFMT\_FILE** or **STGFMT\_ANY** enumeration value in the *grfFlags* parameter to open an existing file.</span></span>

<span data-ttu-id="57b0e-111">不過，您無法為複合檔案取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的 NTFS 實作為。</span><span class="sxs-lookup"><span data-stu-id="57b0e-111">However, you cannot obtain the NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for a compound file.</span></span> <span data-ttu-id="57b0e-112">使用 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)開啟複合檔案時，指定 STGFMT 檔 **\_** 列舉值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="57b0e-112">When opening a compound file with [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), specifying the **STGFMT\_FILE** enumeration value results in an error.</span></span>

<span data-ttu-id="57b0e-113">此外，也無法交易簡單的屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-113">Also, simple property sets cannot be transacted.</span></span> <span data-ttu-id="57b0e-114">也就是說，您無法在 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)和 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法的 *grfmode* 參數中指定 **STGM \_ 交易**，除非您同時在 *grfFlags* 參數中指定 **PROPSETFLAG \_ 簡單**。</span><span class="sxs-lookup"><span data-stu-id="57b0e-114">That is, you cannot specify **STGM\_TRANSACTED** in the *grfmode* parameter of the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods unless you also specify **PROPSETFLAG\_NONSIMPLE** in the *grfFlags* parameter.</span></span> <span data-ttu-id="57b0e-115">屬性集的儲存物件本身不支援交易處理。</span><span class="sxs-lookup"><span data-stu-id="57b0e-115">The property set storage object itself does not support transaction processing.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="57b0e-116">使用時機</span><span class="sxs-lookup"><span data-stu-id="57b0e-116">When to Use</span></span>

<span data-ttu-id="57b0e-117">呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 方法，以建立、開啟或刪除目前 NTFS 屬性集儲存區中的屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-117">Call the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) methods to create, open, or delete property sets in the current NTFS property set storage.</span></span> <span data-ttu-id="57b0e-118">另外還有一個方法 [**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)，它會提供列舉值的指標，可用來列舉儲存區中的屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-118">There is also a method, [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), that supplies a pointer to an enumerator that can be used to enumerate the property sets in the storage.</span></span>

## <a name="compatibility"></a><span data-ttu-id="57b0e-119">相容性</span><span class="sxs-lookup"><span data-stu-id="57b0e-119">Compatibility</span></span>

<span data-ttu-id="57b0e-120">從 Windows 2000 開始，可以使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的 NTFS 實作為。</span><span class="sxs-lookup"><span data-stu-id="57b0e-120">The NTFS implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) are available starting with Windows 2000.</span></span> <span data-ttu-id="57b0e-121">舊版無法存取這些屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-121">Earlier versions cannot access these property sets.</span></span>

<span data-ttu-id="57b0e-122">NTFS 執行會將屬性集儲存在 NTFS 檔案的替代資料流程中。</span><span class="sxs-lookup"><span data-stu-id="57b0e-122">The NTFS implementation stores property sets in alternate streams of an NTFS file.</span></span> <span data-ttu-id="57b0e-123">複製主要檔案時，必須複製替代資料流程。</span><span class="sxs-lookup"><span data-stu-id="57b0e-123">The alternate streams must be copied when the main file is copied.</span></span>

> [!Caution]  
> <span data-ttu-id="57b0e-124">並非所有檔案系統都支援這類串流。</span><span class="sxs-lookup"><span data-stu-id="57b0e-124">Not all file systems support such streams.</span></span> <span data-ttu-id="57b0e-125">如果將含有屬性集的 NTFS 檔案複製到 FAT 磁片區，則只會複製檔案中的資料;屬性集遺失。</span><span class="sxs-lookup"><span data-stu-id="57b0e-125">If an NTFS file with property sets is copied to a FAT volume, only the data in the file is copied; the property set is lost.</span></span> <span data-ttu-id="57b0e-126">在此情況下， [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) 函數不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="57b0e-126">The [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) function does not return an error in this case.</span></span>

 

> [!Caution]  
> <span data-ttu-id="57b0e-127">如果執行檔案複製的電腦不是在 Windows 2000 或更新版本上執行的電腦，屬性集可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="57b0e-127">If the computer performing the file copy is not a computer running on Windows 2000 or later, the property sets may be lost.</span></span> <span data-ttu-id="57b0e-128">例如，如果在 Windows 95 作業系統上執行的電腦複製了 NTFS 檔案，即使目的地檔案也在 NTFS 磁片區上，也會遺失屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-128">For example, if a computer running on Windows 95 operating system copies an NTFS file, the property set is lost even if the destination file is also on an NTFS volume.</span></span>

 

## <a name="methods"></a><span data-ttu-id="57b0e-129">方法</span><span class="sxs-lookup"><span data-stu-id="57b0e-129">Methods</span></span>

<span data-ttu-id="57b0e-130">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 檔案系統執行支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="57b0e-130">The NTFS file system implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="57b0e-131"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="57b0e-131"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="57b0e-132">在目前的 NTFS 檔案儲存體中建立新的屬性集，並在傳回時提供介面指標給 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS 檔案執行。</span><span class="sxs-lookup"><span data-stu-id="57b0e-132">Creates a new property set in the current NTFS file storage and, on return, supplies an interface pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS file implementation.</span></span> <span data-ttu-id="57b0e-133">*Grfmode* 參數中指定的共用模式必須是 **STGM \_ 共用 \_ 專屬** 的。</span><span class="sxs-lookup"><span data-stu-id="57b0e-133">The sharing mode specified in the *grfmode* parameter must be **STGM\_SHARE\_EXCLUSIVE**.</span></span>

</dd> <dt>

<span data-ttu-id="57b0e-134"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="57b0e-134"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="57b0e-135">開啟目前屬性儲存區中的現有屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-135">Opens an existing property set in the current property storage.</span></span> <span data-ttu-id="57b0e-136">傳回時，它會提供介面指標給 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的 NTFS 檔案執行。</span><span class="sxs-lookup"><span data-stu-id="57b0e-136">On return, it supplies an interface pointer to the NTFS file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage).</span></span> <span data-ttu-id="57b0e-137">*Grfmode* 參數中指定的共用模式必須是 **STGM \_ 共用 \_ 專屬** 的。</span><span class="sxs-lookup"><span data-stu-id="57b0e-137">The sharing mode specified in the *grfmode* parameter must be **STGM\_SHARE\_EXCLUSIVE**.</span></span>

</dd> <dt>

<span data-ttu-id="57b0e-138"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage：:D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="57b0e-138"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="57b0e-139">刪除目前屬性儲存區中的屬性集。</span><span class="sxs-lookup"><span data-stu-id="57b0e-139">Deletes a property set in the current property storage.</span></span>

</dd> <dt>

<span data-ttu-id="57b0e-140"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="57b0e-140"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="57b0e-141">建立用來列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的物件。</span><span class="sxs-lookup"><span data-stu-id="57b0e-141">Creates an object used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="57b0e-142">每個 **STATPROPSETSTG** 結構都會提供單一屬性集的相關資料。</span><span class="sxs-lookup"><span data-stu-id="57b0e-142">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57b0e-143">備註</span><span class="sxs-lookup"><span data-stu-id="57b0e-143">Remarks</span></span>

<span data-ttu-id="57b0e-144">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的 NTFS 實作為檔案中的存放區屬性集，而不會影響該檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="57b0e-144">The NTFS implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) store property sets in a file without affecting the contents of that file.</span></span> <span data-ttu-id="57b0e-145">例如，如果您在名為 Default.htm 的 HTML 檔案中建立屬性集，該檔案仍然會在網頁瀏覽器中正確顯示。</span><span class="sxs-lookup"><span data-stu-id="57b0e-145">For example, if you create a property set in an HTML file named Default.htm, that file still displays properly in a Web browser.</span></span> <span data-ttu-id="57b0e-146">也就是說，使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數存取檔案時，會無法偵測使用這兩個介面的檔案變更。</span><span class="sxs-lookup"><span data-stu-id="57b0e-146">That is, changes to a file using these two interfaces are undetectable when accessing a file with the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="57b0e-147">當使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 將屬性集寫入 ntfs 版本5.0 磁片區上的檔案時，ntfs 會提供安全的執行。</span><span class="sxs-lookup"><span data-stu-id="57b0e-147">The NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) provides a safe implementation when used to write property sets to a file on an NTFS version 5.0 volume.</span></span> <span data-ttu-id="57b0e-148">即使發生系統失敗，這些屬性集也無法由實作為損毀。</span><span class="sxs-lookup"><span data-stu-id="57b0e-148">Such property sets cannot be corrupted by the implementation even in the event of a system failure.</span></span> <span data-ttu-id="57b0e-149">例如，如果在將屬性集排清至磁片的情況下呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 時發生系統的電源失敗，屬性集永遠不會保持在中繼狀態。</span><span class="sxs-lookup"><span data-stu-id="57b0e-149">For example, if the power to a system fails during a call to [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) while the property set is flushed to the disk, the property set is never left in an intermediate state.</span></span> <span data-ttu-id="57b0e-150">先前的屬性集版本會保留或儲存所有更新。</span><span class="sxs-lookup"><span data-stu-id="57b0e-150">Either the previous version of the property set remains or all of the updates are saved.</span></span>

<span data-ttu-id="57b0e-151">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 實與複合檔案執行的方式不同，如下所示：</span><span class="sxs-lookup"><span data-stu-id="57b0e-151">The NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) differs from the compound file implementation in the following ways:</span></span>

-   <span data-ttu-id="57b0e-152">從 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面取得的 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)結構包含 **clsid** 成員，其值一律為零 (**clsid \_ Null**) 。</span><span class="sxs-lookup"><span data-stu-id="57b0e-152">A [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure obtained from the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interface contains a **clsid** member whose value is always zero (**CLSID\_NULL**).</span></span> <span data-ttu-id="57b0e-153">使用複合檔案執行時，會針對非簡單 (傳回正確的 **clsid** 成員，請參閱屬性集) 屬性集的 [儲存和資料流程物件](storage-vs--stream-for-a-property-set.md) 。</span><span class="sxs-lookup"><span data-stu-id="57b0e-153">With the compound file implementation, the correct **clsid** member is returned for non-simple (see [Storage and Stream Objects for a Property Set](storage-vs--stream-for-a-property-set.md)) property sets.</span></span>
-   <span data-ttu-id="57b0e-154">使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函數取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面指標的 NTFS 實作為時， *grfmode* 參數必須遵循與複合檔案執行相同的規則。</span><span class="sxs-lookup"><span data-stu-id="57b0e-154">When obtaining an NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface pointer using the [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function, the *grfmode* parameter must follow the same rules as for the compound file implementation.</span></span>

    <span data-ttu-id="57b0e-155">此外，可能不會使用下列旗標：</span><span class="sxs-lookup"><span data-stu-id="57b0e-155">In addition, the following flags may not be used:</span></span>

    <span data-ttu-id="57b0e-156">**STGM \_SIMPLE**、 **STGM \_ 交易**、 **STGM \_ CONVERT**、 **STGM \_ PRIORITY** 和 **STGM \_ DELETEONRELEASE**。</span><span class="sxs-lookup"><span data-stu-id="57b0e-156">**STGM\_SIMPLE**, **STGM\_TRANSACTED**, **STGM\_CONVERT**, **STGM\_PRIORITY**, and **STGM\_DELETEONRELEASE**.</span></span>

-   <span data-ttu-id="57b0e-157">當 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**STGOPENSTORAGEEX**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函數取得 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面時，共用模式主要會套用至該介面的其他實例，而不會套用至開啟檔案本身的實例。</span><span class="sxs-lookup"><span data-stu-id="57b0e-157">When an NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface is obtained by the [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions, the sharing modes primarily apply to other instances of that interface, and not to instances of opening the file itself.</span></span> <span data-ttu-id="57b0e-158">例如，如果透過呼叫 **StgOpenStorageEx** 函式來開啟 NTFS **IPropertySetStorage** 介面，並將 *grfmode* 參數設定為 **STGM \_ READWRITE \| STGM \_ 共用 \_ 獨佔**，則可以使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函數來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="57b0e-158">For example, if an NTFS **IPropertySetStorage** interface is opened by calling the **StgOpenStorageEx** function, with the *grfmode* parameter set to **STGM\_READWRITE\|STGM\_SHARE\_EXCLUSIVE**, it is possible to open the file with the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

    <span data-ttu-id="57b0e-159">開啟此介面的這類並行實例受限於下列條件約束： [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式中的 *dwShareMode* 參數必須指定檔案 **\_ 共用 \_ 讀取** 旗標，且 *dwAccess* 參數不得指定 **刪除** 旗標。</span><span class="sxs-lookup"><span data-stu-id="57b0e-159">Such simultaneous instances of opening this interface are subject to the following constraints: the *dwShareMode* parameter in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function must specify the **FILE\_SHARE\_READ** flag, and the *dwAccess* parameter must not specify the **DELETE** flag.</span></span> <span data-ttu-id="57b0e-160">此外，您不能在這些屬性集介面開啟的檔案上呼叫 [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) 和 [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) 函式，因為這些函式需要 **刪除** 檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="57b0e-160">Also, the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) and [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) functions must not be called on a file for which these property set interfaces are open, as these functions require **DELETE** access to the file.</span></span>

-   <span data-ttu-id="57b0e-161">如果 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 方法是以唯讀方式開啟，而且檔案目前沒有任何屬性集，則傳回的物件將不會實際保存開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="57b0e-161">If an NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) method is opened as read-only, and the file currently has no property sets, the object returned will not actually hold open the file.</span></span> <span data-ttu-id="57b0e-162">因此，即使原始開啟作業的共用模式會拒絕它，該檔案的其他開頭也會成功。</span><span class="sxs-lookup"><span data-stu-id="57b0e-162">Consequently, other openings of that file will succeed, even if the sharing mode of the original open operation would otherwise reject it.</span></span>

    <span data-ttu-id="57b0e-163">範例如果 NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 是以 **STGM \_ READ \| STGM \_ SHARE \_ 專有** 的模式開啟，而且檔案沒有屬性集，就可以同時開啟檔案 **STGM \_ READWRITE \| STGM \_ 共用 \_ 獨佔**。</span><span class="sxs-lookup"><span data-stu-id="57b0e-163">Example; if an NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is opened in the mode **STGM\_READ\|STGM\_SHARE\_EXCLUSIVE**, and the file has no property sets, it will be possible to simultaneously open the file **STGM\_READWRITE\|STGM\_SHARE\_EXCLUSIVE**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57b0e-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="57b0e-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b0e-165">IPropertyStorage-NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="57b0e-165">IPropertyStorage-NTFS File System Implementation</span></span>](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[<span data-ttu-id="57b0e-166">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="57b0e-166">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="57b0e-167">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="57b0e-167">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="57b0e-168">**IStorage：： EnumElements**</span><span class="sxs-lookup"><span data-stu-id="57b0e-168">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="57b0e-169">**PROPSETFLAG 常數**</span><span class="sxs-lookup"><span data-stu-id="57b0e-169">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="57b0e-170">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="57b0e-170">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 
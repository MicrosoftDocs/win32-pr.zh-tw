---
title: IStorage-Compound 檔案的執行
description: IStorage 的複合檔案執行可讓您建立和管理位於複合檔案物件中之儲存物件內的 substorages 和資料流程。
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965652"
---
# <a name="istorage-compound-file-implementation"></a><span data-ttu-id="9338f-104">IStorage-Compound 檔案的執行</span><span class="sxs-lookup"><span data-stu-id="9338f-104">IStorage-Compound File Implementation</span></span>

<span data-ttu-id="9338f-105">[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的複合檔案執行可讓您建立和管理位於複合檔案物件中之儲存物件內的 substorages 和資料流程。</span><span class="sxs-lookup"><span data-stu-id="9338f-105">The compound file implementation of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) allows you to create and manage substorages and streams within a storage object residing in a compound file object.</span></span> <span data-ttu-id="9338f-106">若要建立複合檔案物件並取得 **IStorage** 指標，請呼叫 API 函數 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)。</span><span class="sxs-lookup"><span data-stu-id="9338f-106">To create a compound file object and get an **IStorage** pointer, call the API function [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="9338f-107">若要開啟現有的複合檔案物件並取得其根 **IStorage** 指標，請呼叫 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)。</span><span class="sxs-lookup"><span data-stu-id="9338f-107">To open an existing compound file object and get its root **IStorage** pointer, call [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span>

<span data-ttu-id="9338f-108">使用複合儲存的應用程式應該在 HKEY \_ 類別 \_ 根 SystemFileAssociations 中註冊 \\ ，而且應該提供自己的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="9338f-108">Applications that use compound storage should be registered in HKEY\_CLASSES\_ROOT\\SystemFileAssociations and should provide their own property handlers.</span></span> <span data-ttu-id="9338f-109">如需詳細資訊，請參閱 [應用程式註冊](/windows/desktop/shell/app-registration)的「註冊動詞和其他檔案關聯資訊」一節。</span><span class="sxs-lookup"><span data-stu-id="9338f-109">For more information, see the "Registering Verbs and Other File Association Information" section of [Application Registration](/windows/desktop/shell/app-registration).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="9338f-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="9338f-110">When to Use</span></span>

<span data-ttu-id="9338f-111">大部分的應用程式都會使用此實作為來建立和管理儲存體和串流。</span><span class="sxs-lookup"><span data-stu-id="9338f-111">Most applications use this implementation to create and manage storages and streams.</span></span>

## <a name="methods"></a><span data-ttu-id="9338f-112">方法</span><span class="sxs-lookup"><span data-stu-id="9338f-112">Methods</span></span>

<dl> <dt>

<span data-ttu-id="9338f-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span><span class="sxs-lookup"><span data-stu-id="9338f-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-114">使用這個儲存物件中包含的指定名稱，建立並開啟資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-114">Creates and opens a stream object with the specified name contained in this storage object.</span></span> <span data-ttu-id="9338f-115">名稱長度不得超過31個字元 (不包括字串結束字元) 。</span><span class="sxs-lookup"><span data-stu-id="9338f-115">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="9338f-116">000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-116">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="9338f-117">這是複合檔案限制，而非結構化儲存體限制。</span><span class="sxs-lookup"><span data-stu-id="9338f-117">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="9338f-118">[**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法的 COM 提供的複合檔案執行不支援下列行為：</span><span class="sxs-lookup"><span data-stu-id="9338f-118">The COM-provided compound file implementation of the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method does not support the following behaviors:</span></span>

-   <span data-ttu-id="9338f-119">\_不支援 STGM DELETEONRELEASE 旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-119">The STGM\_DELETEONRELEASE flag is not supported.</span></span>
-   <span data-ttu-id="9338f-120">\_資料流程物件不支援交易模式 (STGM 交易) 。</span><span class="sxs-lookup"><span data-stu-id="9338f-120">Transacted mode (STGM\_TRANSACTED) is not supported for stream objects.</span></span>
-   <span data-ttu-id="9338f-121">不支援從相同的儲存體多次開啟相同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9338f-121">Opening the same stream more than once from the same storage is not supported.</span></span> <span data-ttu-id="9338f-122">\_ \_ *GrfMode* 參數中必須指定 STGM 共用獨佔共用模式旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-122">The STGM\_SHARE\_EXCLUSIVE sharing-mode flag must be specified in the *grfMode* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span><span class="sxs-lookup"><span data-stu-id="9338f-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-124">使用 *grfMode* 參數中指定的存取模式，在此儲存物件內開啟現有的資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-124">Opens an existing stream object within this storage object using the access modes specified in the *grfMode* parameter.</span></span> <span data-ttu-id="9338f-125">000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-125">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="9338f-126">這是複合檔案限制，而非結構化儲存體限制。</span><span class="sxs-lookup"><span data-stu-id="9338f-126">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="9338f-127">[**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)方法的 COM 提供的複合檔案執行不支援下列行為：</span><span class="sxs-lookup"><span data-stu-id="9338f-127">The COM-provided compound file implementation of the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method does not support the following behavior:</span></span>

-   <span data-ttu-id="9338f-128">STGM \_ DELETEONRELEASE 旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-128">The STGM\_DELETEONRELEASE flag.</span></span>
-   <span data-ttu-id="9338f-129">交易模式 (\_ 資料流程物件的交易式) STGM。</span><span class="sxs-lookup"><span data-stu-id="9338f-129">Transacted mode (STGM\_TRANSACTED) for stream objects.</span></span>
-   <span data-ttu-id="9338f-130">從相同的儲存體多次開啟相同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9338f-130">Opening the same stream more than once from the same storage.</span></span> <span data-ttu-id="9338f-131">\_ \_ 必須指定 STGM 共用專屬旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-131">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span><span class="sxs-lookup"><span data-stu-id="9338f-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-133">使用指定的存取模式，以指定的名稱建立並開啟新的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-133">Creates and opens a new storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="9338f-134">名稱長度不得超過31個字元 (不包括字串結束字元) 。</span><span class="sxs-lookup"><span data-stu-id="9338f-134">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="9338f-135">000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-135">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="9338f-136">這是複合檔案限制，而非結構化儲存體限制。</span><span class="sxs-lookup"><span data-stu-id="9338f-136">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="9338f-137">[**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)方法的 COM 提供的複合檔案執行不支援下列行為：</span><span class="sxs-lookup"><span data-stu-id="9338f-137">The COM-provided compound file implementation of the [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="9338f-138">\_非根儲存體的 STGM 優先權旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-138">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="9338f-139">從相同的父儲存體多次開啟相同的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-139">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="9338f-140">\_ \_ 必須指定 STGM 共用專屬旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-140">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="9338f-141">STGM \_ DELETEONRELEASE 旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-141">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="9338f-142">如果指定此旗標，函數會傳回 STG. \_ E \_ INVALIDFLAG。</span><span class="sxs-lookup"><span data-stu-id="9338f-142">If this flag is specified, the function returns STG\_E\_INVALIDFLAG.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span><span class="sxs-lookup"><span data-stu-id="9338f-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-144">在指定的存取模式中，以指定的名稱開啟現有的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-144">Opens an existing storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="9338f-145">000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-145">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="9338f-146">這是複合檔案限制，而非結構化儲存體限制。</span><span class="sxs-lookup"><span data-stu-id="9338f-146">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="9338f-147">[**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)方法的 COM 提供的複合檔案執行不支援下列行為：</span><span class="sxs-lookup"><span data-stu-id="9338f-147">The COM-provided compound file implementation of the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="9338f-148">\_非根儲存體的 STGM 優先權旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-148">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="9338f-149">從相同的父儲存體多次開啟相同的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-149">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="9338f-150">\_ \_ 必須指定 STGM 共用專屬旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-150">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="9338f-151">STGM \_ DELETEONRELEASE 旗標。</span><span class="sxs-lookup"><span data-stu-id="9338f-151">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="9338f-152">如果指定此旗標，函數會傳回 STG. \_ E \_ INVALIDFUNCTION。</span><span class="sxs-lookup"><span data-stu-id="9338f-152">If this flag is specified, the function returns STG\_E\_INVALIDFUNCTION.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span><span class="sxs-lookup"><span data-stu-id="9338f-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-154">只將這個開啟的儲存物件的 substorages 和資料流程複製到另一個儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-154">Copies only the substorages and streams of this open storage object into another storage object.</span></span> <span data-ttu-id="9338f-155">*RgiidExclude* 參數可以設定為 iid \_ IStream 以只複製 substorages，或設定為僅複製 \_ 資料流程的 iid IStorage。</span><span class="sxs-lookup"><span data-stu-id="9338f-155">The *rgiidExclude* parameter can be set to IID\_IStream to copy only substorages, or to IID\_IStorage to copy only streams.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage：： MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span><span class="sxs-lookup"><span data-stu-id="9338f-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-157">將 substorage 或串流從此儲存物件複製或移動到另一個儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-157">Copies or moves a substorage or stream from this storage object to another storage object.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span><span class="sxs-lookup"><span data-stu-id="9338f-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-159">確保對儲存物件所做的任何變更會在交易模式中開啟，並反映在父儲存體中;針對根儲存體，反映實際裝置中的變更;例如，磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="9338f-159">Ensures that any changes made to a storage object open in transacted mode are reflected in the parent storage; for a root storage, reflects the changes in the actual device; for example, a file on disk.</span></span> <span data-ttu-id="9338f-160">若是以直接模式開啟的根儲存物件，除了將所有記憶體緩衝區排清到磁片之外，此方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9338f-160">For a root storage object opened in direct mode, this method has no effect except to flush all memory buffers to the disk.</span></span> <span data-ttu-id="9338f-161">若是直接模式中的非根儲存物件，這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9338f-161">For nonroot storage objects in direct mode, this method has no effect.</span></span>

<span data-ttu-id="9338f-162">除非 \_ *grfCommitFlags* 參數中指定了 STGC 覆寫，否則 COM 提供的複合檔案執行會使用兩個階段的認可進程。</span><span class="sxs-lookup"><span data-stu-id="9338f-162">The COM-provided compound files implementation uses a two-phase commit process unless STGC\_OVERWRITE is specified in the *grfCommitFlags* parameter.</span></span> <span data-ttu-id="9338f-163">這兩個階段的程式可確保資料的穩定性，以防認可作業失敗。</span><span class="sxs-lookup"><span data-stu-id="9338f-163">This two-phase process ensures the robustness of data, in case the commit operation fails.</span></span> <span data-ttu-id="9338f-164">首先，所有新資料都會寫入基礎檔案中未使用的空間。</span><span class="sxs-lookup"><span data-stu-id="9338f-164">First, all new data is written to unused space in the underlying file.</span></span> <span data-ttu-id="9338f-165">必要時，會設定檔案的新空間。</span><span class="sxs-lookup"><span data-stu-id="9338f-165">If necessary, new space is allocated to the file.</span></span> <span data-ttu-id="9338f-166">完成此步驟之後，檔案中的資料表會使用單一磁區寫入作業進行更新，以指出要使用新資料來取代舊的資料。</span><span class="sxs-lookup"><span data-stu-id="9338f-166">After this step has been completed, a table in the file is updated using a single-sector write operation to indicate that the new data is to be used in place of the old.</span></span> <span data-ttu-id="9338f-167">舊資料會變成可用空間，以便在下一次認可作業時使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-167">The old data becomes free space to be used at the next commit operation.</span></span> <span data-ttu-id="9338f-168">因此，如果在認可變更時發生錯誤，就可以使用舊的資料，而且可以還原。</span><span class="sxs-lookup"><span data-stu-id="9338f-168">Thus, the old data is available and can be restored if an error occurs when committing changes.</span></span> <span data-ttu-id="9338f-169">如果 \_ 指定了 STGC 覆寫，則會使用單一階段認可作業。</span><span class="sxs-lookup"><span data-stu-id="9338f-169">If STGC\_OVERWRITE is specified, a single phase commit operation is used.</span></span> <span data-ttu-id="9338f-170">如需交易模式旗標的詳細資訊，請參閱 [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) 列舉。</span><span class="sxs-lookup"><span data-stu-id="9338f-170">For more information about transacted mode flags, see [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span><span class="sxs-lookup"><span data-stu-id="9338f-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-172">捨棄自從上次認可作業之後對儲存物件所做的所有變更。</span><span class="sxs-lookup"><span data-stu-id="9338f-172">Discards all changes that have been made to the storage object since the last commit operation.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage：： EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span><span class="sxs-lookup"><span data-stu-id="9338f-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-174">建立並抓取列舉值物件的指標，該物件可用來列舉此儲存物件內所包含的儲存和資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-174">Creates and retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.</span></span> <span data-ttu-id="9338f-175">COM 提供的複合檔案執行會取得該資訊的快照。</span><span class="sxs-lookup"><span data-stu-id="9338f-175">The COM-provided compound file implementation takes a snapshot of that information.</span></span> <span data-ttu-id="9338f-176">因此，在取得新的列舉值之前，對資料流程和儲存體的變更都不會反映在枚舉器中。</span><span class="sxs-lookup"><span data-stu-id="9338f-176">Therefore, changes to the streams and storages are not reflected in the enumerator until a new enumerator is obtained.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage：:D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span><span class="sxs-lookup"><span data-stu-id="9338f-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::DestroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-178">從這個儲存物件 (substorage 或 stream) 移除指定的元素。</span><span class="sxs-lookup"><span data-stu-id="9338f-178">Removes the specified element (substorage or stream) from this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage：： RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span><span class="sxs-lookup"><span data-stu-id="9338f-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-180">重新命名這個儲存物件中指定的 substorage 或資料流程。</span><span class="sxs-lookup"><span data-stu-id="9338f-180">Renames the specified substorage or stream in this storage object.</span></span> <span data-ttu-id="9338f-181">000到01f 字元（作為資料流程/儲存體名稱的第一個字元）是保留供 OLE 使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-181">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="9338f-182">這是複合檔案限制，而非結構化儲存體限制。</span><span class="sxs-lookup"><span data-stu-id="9338f-182">This is a compound file restriction, not a structured storage restriction.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage：： SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span><span class="sxs-lookup"><span data-stu-id="9338f-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-184">設定指定之儲存元素的修改、存取和建立時間。</span><span class="sxs-lookup"><span data-stu-id="9338f-184">Sets the modification, access, and creation times of the specified storage element.</span></span> <span data-ttu-id="9338f-185">COM 提供的複合檔案執行會維護內部儲存物件的修改和變更時間。</span><span class="sxs-lookup"><span data-stu-id="9338f-185">The COM-provided compound-file implementation maintains modification and change times for internal storage objects.</span></span> <span data-ttu-id="9338f-186">根儲存物件支援基礎檔案系統 (或 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)) 所支援的任何內容。</span><span class="sxs-lookup"><span data-stu-id="9338f-186">Root storage objects support whatever is supported by the underlying file system (or by [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)).</span></span> <span data-ttu-id="9338f-187">複合檔案執行不會維護任何內部資料流程的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="9338f-187">The compound file implementation does not maintain any time stamps for internal streams.</span></span> <span data-ttu-id="9338f-188">不支援的時間戳記會回報為零，讓呼叫端能夠測試支援。</span><span class="sxs-lookup"><span data-stu-id="9338f-188">Unsupported time stamps are reported as zero, which allows the caller to test for support.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage：： SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="9338f-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-190">將指定的 CLSID 指派給這個儲存物件。</span><span class="sxs-lookup"><span data-stu-id="9338f-190">Assigns the specified CLSID to this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage：： SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span><span class="sxs-lookup"><span data-stu-id="9338f-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-192">在此儲存物件中儲存最多32位的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9338f-192">Stores up to 32 bits of state information in this storage object.</span></span> <span data-ttu-id="9338f-193">這個方法所設定的狀態僅供外部使用。</span><span class="sxs-lookup"><span data-stu-id="9338f-193">The state set by this method is for external use only.</span></span> <span data-ttu-id="9338f-194">COM 提供的複合檔案執行不會根據狀態執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="9338f-194">The COM-provided compound file implementation does not perform any action based on the state.</span></span>

</dd> <dt>

<span data-ttu-id="9338f-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span><span class="sxs-lookup"><span data-stu-id="9338f-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="9338f-196">抓取這個開啟的儲存物件的 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) 結構。</span><span class="sxs-lookup"><span data-stu-id="9338f-196">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this open storage object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9338f-197">備註</span><span class="sxs-lookup"><span data-stu-id="9338f-197">Remarks</span></span>

<span data-ttu-id="9338f-198">如果以簡單模式開啟儲存物件，則會限制上述方法的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9338f-198">If the storage object is opened in simple mode, use of the above methods is restricted.</span></span> <span data-ttu-id="9338f-199">如果以 \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)或 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)函式的 *grfMode* 參數中指定的 STGM simple 元素開啟，則儲存體會處於簡單模式。</span><span class="sxs-lookup"><span data-stu-id="9338f-199">A storage is in simple mode if it is opened with the STGM\_SIMPLE element specified in the *grfMode* parameter of the [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function.</span></span> <span data-ttu-id="9338f-200">如需簡單模式儲存體的詳細資訊，請參閱 [**STGM 常數**](stgm-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9338f-200">For more information about simple-mode storages, see [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="9338f-201">如果已從 **StgCreateStorageEx** 函式取得簡單模式的儲存物件，則可以呼叫 [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 方法，但 [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 方法無法進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="9338f-201">If the simple-mode storage object was obtained from the **StgCreateStorageEx** function, then the [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method can be called but the [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method cannot.</span></span> <span data-ttu-id="9338f-202">如果已從 **StgOpenStorageEx** 函式取得簡單模式儲存物件，則可以呼叫 **OpenStream** 方法，但 **CreateStream** 方法無法進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="9338f-202">If the simple mode storage object was obtained from the **StgOpenStorageEx** function, then the **OpenStream** method can be called but the **CreateStream** method cannot.</span></span>

<span data-ttu-id="9338f-203">當使用簡單模式儲存物件來建立資料流程時，該資料流程的大小下限通常為4096個位元組。</span><span class="sxs-lookup"><span data-stu-id="9338f-203">When a simple-mode storage object is used to create a stream, the minimum size of that stream typically is 4096 bytes.</span></span> <span data-ttu-id="9338f-204">如果將較少的資料寫入資料流程，則大小會四捨五入為4096個位元組。</span><span class="sxs-lookup"><span data-stu-id="9338f-204">If less data is written to the stream, the size is rounded up to 4096 bytes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9338f-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="9338f-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9338f-206">複合檔案執行限制</span><span class="sxs-lookup"><span data-stu-id="9338f-206">Compound File Implementation Limits</span></span>](structured-storage-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9338f-207">**IFillLockBytes**</span><span class="sxs-lookup"><span data-stu-id="9338f-207">**IFillLockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[<span data-ttu-id="9338f-208">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="9338f-208">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="9338f-209">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="9338f-209">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="9338f-210">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="9338f-210">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="9338f-211">**IStream**</span><span class="sxs-lookup"><span data-stu-id="9338f-211">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="9338f-212">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="9338f-212">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="9338f-213">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="9338f-213">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="9338f-214">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="9338f-214">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="9338f-215">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="9338f-215">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 
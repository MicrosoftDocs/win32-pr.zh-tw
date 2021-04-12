---
title: 'STGM 常數 (ObjBase) '
description: 旗標，表示用來建立和刪除物件之物件和存取模式的條件。
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464484"
---
# <a name="stgm-constants"></a><span data-ttu-id="1e34b-103">STGM 常數</span><span class="sxs-lookup"><span data-stu-id="1e34b-103">STGM Constants</span></span>

<span data-ttu-id="1e34b-104">STGM 常數是旗標，表示用來建立和刪除物件之物件和存取模式的條件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="1e34b-105">STGM 常數包含在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面，以及 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)、 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)、 [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)、 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)和 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函數中。</span><span class="sxs-lookup"><span data-stu-id="1e34b-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="1e34b-106">這些元素通常會使用 **OR** 運算子來合併。</span><span class="sxs-lookup"><span data-stu-id="1e34b-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="1e34b-107">它們會在下表所列的群組中加以解讀。</span><span class="sxs-lookup"><span data-stu-id="1e34b-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="1e34b-108">從單一群組使用一個以上的元素是不正確。</span><span class="sxs-lookup"><span data-stu-id="1e34b-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="1e34b-109">建立物件時，請使用建立群組中的旗標，例如使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) 或 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)。</span><span class="sxs-lookup"><span data-stu-id="1e34b-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="1e34b-110">如需 transactioning 的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="1e34b-111">Group</span><span class="sxs-lookup"><span data-stu-id="1e34b-111">Group</span></span>                      | <span data-ttu-id="1e34b-112">旗標</span><span class="sxs-lookup"><span data-stu-id="1e34b-112">Flag</span></span>                         | <span data-ttu-id="1e34b-113">值</span><span class="sxs-lookup"><span data-stu-id="1e34b-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="1e34b-114">Access</span><span class="sxs-lookup"><span data-stu-id="1e34b-114">Access</span></span>                     | <span data-ttu-id="1e34b-115">**STGM \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="1e34b-115">**STGM\_READ**</span></span>               | <span data-ttu-id="1e34b-116">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="1e34b-117">**STGM \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1e34b-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="1e34b-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="1e34b-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="1e34b-119">**STGM \_ READWRITE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="1e34b-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="1e34b-120">0x00000002L</span></span> |
| <span data-ttu-id="1e34b-121">共用</span><span class="sxs-lookup"><span data-stu-id="1e34b-121">Sharing</span></span>                    | <span data-ttu-id="1e34b-122">**STGM \_ 共用 \_ 拒絕 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="1e34b-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="1e34b-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="1e34b-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="1e34b-124">**STGM \_ 共用 \_ 拒絕 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="1e34b-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="1e34b-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="1e34b-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="1e34b-126">**STGM \_ 共用 \_ 拒絕 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1e34b-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="1e34b-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="1e34b-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="1e34b-128">**STGM \_ 共用 \_ 專屬**</span><span class="sxs-lookup"><span data-stu-id="1e34b-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="1e34b-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="1e34b-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="1e34b-130">**STGM \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="1e34b-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="1e34b-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-131">0x00040000L</span></span> |
| <span data-ttu-id="1e34b-132">建立</span><span class="sxs-lookup"><span data-stu-id="1e34b-132">Creation</span></span>                   | <span data-ttu-id="1e34b-133">**STGM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="1e34b-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="1e34b-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="1e34b-135">**STGM \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="1e34b-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="1e34b-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="1e34b-137">**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="1e34b-138">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-138">0x00000000L</span></span> |
| <span data-ttu-id="1e34b-139">Transactioning</span><span class="sxs-lookup"><span data-stu-id="1e34b-139">Transactioning</span></span>             | <span data-ttu-id="1e34b-140">**STGM \_ DIRECT**</span><span class="sxs-lookup"><span data-stu-id="1e34b-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="1e34b-141">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="1e34b-142">**STGM \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="1e34b-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="1e34b-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-143">0x00010000L</span></span> |
| <span data-ttu-id="1e34b-144">Transactioning 效能</span><span class="sxs-lookup"><span data-stu-id="1e34b-144">Transactioning Performance</span></span> | <span data-ttu-id="1e34b-145">**STGM \_ NOSCRATCH**</span><span class="sxs-lookup"><span data-stu-id="1e34b-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="1e34b-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="1e34b-147">**STGM \_ NOSNAPSHOT**</span><span class="sxs-lookup"><span data-stu-id="1e34b-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="1e34b-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-148">0x00200000L</span></span> |
| <span data-ttu-id="1e34b-149">直接 SWMR 和簡單</span><span class="sxs-lookup"><span data-stu-id="1e34b-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="1e34b-150">**STGM \_ 簡單**</span><span class="sxs-lookup"><span data-stu-id="1e34b-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="1e34b-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="1e34b-152">**STGM \_ DIRECT \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="1e34b-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="1e34b-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-153">0x00400000L</span></span> |
| <span data-ttu-id="1e34b-154">發行時刪除</span><span class="sxs-lookup"><span data-stu-id="1e34b-154">Delete On Release</span></span>          | <span data-ttu-id="1e34b-155">**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="1e34b-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="1e34b-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="1e34b-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-158">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-159">指出物件是唯讀的，這表示無法進行修改。</span><span class="sxs-lookup"><span data-stu-id="1e34b-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="1e34b-160">例如，如果資料流程物件是以 **STGM \_ READ** 開啟，則可能會呼叫 [**ISequentialStream：： READ**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) 方法，但是 [**ISequentialStream：： Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) 方法可能不會。</span><span class="sxs-lookup"><span data-stu-id="1e34b-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="1e34b-161">同樣地，如果以 **STGM \_ READ** 開啟的儲存物件，則可能會呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 和 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 方法，但是 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 和 [**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) 方法可能不會。</span><span class="sxs-lookup"><span data-stu-id="1e34b-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1e34b-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="1e34b-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-164">可讓您儲存對物件所做的變更，但不允許存取其資料。</span><span class="sxs-lookup"><span data-stu-id="1e34b-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="1e34b-165">提供的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面實作為不支援這個僅限寫入模式。</span><span class="sxs-lookup"><span data-stu-id="1e34b-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ READWRITE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="1e34b-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-168">啟用物件資料的存取和修改。</span><span class="sxs-lookup"><span data-stu-id="1e34b-168">Enables access and modification of object data.</span></span> <span data-ttu-id="1e34b-169">例如，如果資料流程物件是在此模式中建立或開啟，則可以呼叫 [**IStream：： Read**](/windows/desktop/api/Objidl/nn-objidl-istream) 和 **Istream：： Write**。</span><span class="sxs-lookup"><span data-stu-id="1e34b-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="1e34b-170">請注意，這個常數不是 **STGM \_ WRITE** 和 **STGM \_ READ** 專案的簡單二進位 **或** 運算。</span><span class="sxs-lookup"><span data-stu-id="1e34b-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ 共用 \_ 拒絕 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="1e34b-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="1e34b-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-173">指定不拒絕讀取或寫入存取的後續物件的開頭。</span><span class="sxs-lookup"><span data-stu-id="1e34b-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="1e34b-174">如果未指定共用群組中的旗標，則會假設為此旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ 共用 \_ 拒絕 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="1e34b-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="1e34b-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-177">防止其他人在 **STGM \_ 讀取** 模式下開啟物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="1e34b-178">它通常用於根儲存物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ 共用 \_ 拒絕 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1e34b-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="1e34b-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-181">防止其他人針對 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 存取開啟物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="1e34b-182">在交易模式中，共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_** ，可能會大幅提升效能，因為它們不需要快照集。</span><span class="sxs-lookup"><span data-stu-id="1e34b-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="1e34b-183">如需 transactioning 的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ 共用 \_ 專屬**</span><span class="sxs-lookup"><span data-stu-id="1e34b-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="1e34b-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-186">防止其他人後續以任何模式開啟物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="1e34b-187">請注意，此值不是 **STGM \_ 共用 \_ 拒絕 \_ 讀取** 和 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 值的簡單位 **or** 運算。</span><span class="sxs-lookup"><span data-stu-id="1e34b-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="1e34b-188">在交易模式中，共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_** ，可能會大幅提升效能，因為它們不需要快照集。</span><span class="sxs-lookup"><span data-stu-id="1e34b-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="1e34b-189">如需 transactioning 的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="1e34b-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-192">開啟具有最新認可版本之獨佔存取權的儲存體物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="1e34b-193">因此，當您在 [優先權] 模式中開啟物件時，其他使用者無法認可對該物件所做的變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="1e34b-194">您可以取得複製作業的效能優勢，但會防止其他人認可變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="1e34b-195">限制物件在優先順序模式中開啟的時間。</span><span class="sxs-lookup"><span data-stu-id="1e34b-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="1e34b-196">您必須指定 **STGM \_ DIRECT** 和 **STGM \_ READ** with priority 模式，而且您無法指定 **STGM \_ DELETEONRELEASE**。</span><span class="sxs-lookup"><span data-stu-id="1e34b-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="1e34b-197">**STGM \_DELETEONRELEASE** 只有在建立根物件（例如使用 [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)）時才有效。</span><span class="sxs-lookup"><span data-stu-id="1e34b-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="1e34b-198">開啟現有的根物件（例如 with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)）時無效。</span><span class="sxs-lookup"><span data-stu-id="1e34b-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="1e34b-199">建立或開啟子項目（例如使用 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)）時，它也是不正確。</span><span class="sxs-lookup"><span data-stu-id="1e34b-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="1e34b-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-202">表示應該移除現有的儲存物件或資料流程，新的物件才會取代它。</span><span class="sxs-lookup"><span data-stu-id="1e34b-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="1e34b-203">只有在已成功移除現有的物件時，才會建立新的物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="1e34b-204">嘗試建立時，會使用此旗標：</span><span class="sxs-lookup"><span data-stu-id="1e34b-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="1e34b-205">磁片上的儲存物件，但該名稱的檔案已經存在。</span><span class="sxs-lookup"><span data-stu-id="1e34b-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="1e34b-206">儲存物件內的物件，但是具有指定名稱的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="1e34b-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="1e34b-207">位元組陣列物件，但有一個具有指定名稱的物件存在。</span><span class="sxs-lookup"><span data-stu-id="1e34b-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="1e34b-208">此旗標無法搭配開啟作業使用，例如 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 或 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)。</span><span class="sxs-lookup"><span data-stu-id="1e34b-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="1e34b-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-211">建立新的物件，同時將現有的資料保留在名為 "內容" 的資料流程中。</span><span class="sxs-lookup"><span data-stu-id="1e34b-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="1e34b-212">在儲存物件或位元組陣列的案例中，不論現有的檔案或位元組陣列目前是否包含分層式儲存物件，舊資料都會格式化為資料流程。</span><span class="sxs-lookup"><span data-stu-id="1e34b-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="1e34b-213">只有在建立根儲存物件時，才能使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="1e34b-214">它不能用在儲存物件內;例如，在 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)中。</span><span class="sxs-lookup"><span data-stu-id="1e34b-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="1e34b-215">這也不是同時使用此旗標和 **STGM \_ DELETEONRELEASE** 旗標的有效方式。</span><span class="sxs-lookup"><span data-stu-id="1e34b-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-217">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-218">如果具有指定名稱的現有物件存在，就會導致建立作業失敗。</span><span class="sxs-lookup"><span data-stu-id="1e34b-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="1e34b-219">在此情況下，會傳回 **Stg. \_ E \_ FILEALREADYEXISTS** 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="1e34b-220">這是預設建立模式;也就是說，如果未指定其他 create 旗標，則會隱含 **STGM \_ FAILIFTHERE** 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**</span><span class="sxs-lookup"><span data-stu-id="1e34b-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-222">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-223">表示在直接模式下，儲存體或資料流程專案的每個變更都會在發生時寫入。</span><span class="sxs-lookup"><span data-stu-id="1e34b-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="1e34b-224">如果未指定 **STGM \_ DIRECT** 或 **STGM \_ 交易** ，這就是預設值。</span><span class="sxs-lookup"><span data-stu-id="1e34b-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="1e34b-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-227">表示在交易模式下，只有在呼叫明確認可作業時，才會緩衝處理和寫入變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="1e34b-228">若要忽略變更，請呼叫 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)、 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)或 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面中的 [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)方法。</span><span class="sxs-lookup"><span data-stu-id="1e34b-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="1e34b-229">**IStorage** 的 COM 複合檔案執行不支援交易資料流程，這表示資料流程只能在直接模式中開啟，而且您無法還原這些資料流程的變更，但支援交易儲存體。</span><span class="sxs-lookup"><span data-stu-id="1e34b-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="1e34b-230">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案、獨立和 NTFS 檔案系統執行，同樣不支援交易式的簡單屬性集，因為這些屬性集會儲存在資料流程中。</span><span class="sxs-lookup"><span data-stu-id="1e34b-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="1e34b-231">不過，您可以在 [**grfFlags：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *IPropertySetStorage* 參數中指定 **PROPSETFLAG \_ 簡單** 旗標，以建立簡單屬性集的 transactioning。</span><span class="sxs-lookup"><span data-stu-id="1e34b-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOSCRATCH**</span><span class="sxs-lookup"><span data-stu-id="1e34b-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-234">表示在交易模式下，通常會使用暫時的暫存檔案來儲存修改，直到呼叫 **Commit** 方法為止。</span><span class="sxs-lookup"><span data-stu-id="1e34b-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="1e34b-235">指定 **STGM \_ NOSCRATCH** 可允許使用原始檔案的未使用部分做為工作空間，而不是針對該目的建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e34b-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="1e34b-236">這不會影響原始檔案中的資料，而且在某些情況下可能會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="1e34b-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="1e34b-237">若未同時指定 **STGM \_ 交易**，也不能指定此旗標，而且此旗標只能用於根目錄開啟。</span><span class="sxs-lookup"><span data-stu-id="1e34b-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="1e34b-238">如需 NoScratch 模式的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**</span><span class="sxs-lookup"><span data-stu-id="1e34b-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-241">此旗標會在開啟具有 **STGM \_ 交易** 且沒有 **STGM \_ 共用 \_ 專屬** 或 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 的儲存物件時使用。</span><span class="sxs-lookup"><span data-stu-id="1e34b-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="1e34b-242">在此情況下，指定 **STGM \_ NOSNAPSHOT** 可防止系統提供的執行建立檔案的快照集複本。</span><span class="sxs-lookup"><span data-stu-id="1e34b-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="1e34b-243">相反地，檔案的變更會寫入檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="1e34b-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="1e34b-244">除非在認可期間執行匯總，而且檔案上只有一個目前的寫入器，否則無法回收未使用的空間。</span><span class="sxs-lookup"><span data-stu-id="1e34b-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="1e34b-245">當檔案以無快照模式開啟時，若未指定 **STGM \_ NOSNAPSHOT**，則無法執行另一個開啟的操作。</span><span class="sxs-lookup"><span data-stu-id="1e34b-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="1e34b-246">此旗標只能用於根開啟作業。</span><span class="sxs-lookup"><span data-stu-id="1e34b-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="1e34b-247">如需 NoSnapshot 模式的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ 簡單**</span><span class="sxs-lookup"><span data-stu-id="1e34b-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-250">在有限但經常使用的情況下，提供更快速的複合檔案執行。</span><span class="sxs-lookup"><span data-stu-id="1e34b-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="1e34b-251">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="1e34b-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-254">支援單一寫入器 multireader 檔案作業的直接模式。</span><span class="sxs-lookup"><span data-stu-id="1e34b-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="1e34b-255">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="1e34b-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e34b-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e34b-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="1e34b-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e34b-258">指出當根儲存物件釋放時，會自動終結基礎檔案。</span><span class="sxs-lookup"><span data-stu-id="1e34b-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="1e34b-259">這項功能最適合用來建立暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="1e34b-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="1e34b-260">只有在建立根物件（例如 with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)）時，才能使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="1e34b-261">開啟根物件（例如 with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)）或建立或開啟子項目（例如 with [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)）時，這是不正確。</span><span class="sxs-lookup"><span data-stu-id="1e34b-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="1e34b-262">同時使用此旗標和 STGM CONVERT 旗標也是不正確 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e34b-263">備註</span><span class="sxs-lookup"><span data-stu-id="1e34b-263">Remarks</span></span>

<span data-ttu-id="1e34b-264">您可以結合這些旗標，但只能從每個相關旗標群組中選擇一個旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="1e34b-265">您必須針對所有使用這些常數的函式和方法，指定每個存取和共用群組的一個旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="1e34b-266">其他群組的旗標是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1e34b-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="1e34b-267">交易模式</span><span class="sxs-lookup"><span data-stu-id="1e34b-267">Transacted Mode</span></span>

<span data-ttu-id="1e34b-268">指定 **STGM \_ DIRECT** 旗標時，只能從存取和共用群組指定下列其中一個旗標組合。</span><span class="sxs-lookup"><span data-stu-id="1e34b-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="1e34b-269">請注意，直接模式是因為缺少 **STGM \_ 交易** 而隱含的。</span><span class="sxs-lookup"><span data-stu-id="1e34b-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="1e34b-270">亦即，如果未指定 **STGM \_ Direct** 或 **STGM \_ 交易** ，則會假設為 **STGM \_ direct** 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="1e34b-271">當指定 **STGM \_ 交易** 旗標時，會在交易模式中建立或開啟物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="1e34b-272">在此模式中，物件的變更將不會保存，直到認可為止。</span><span class="sxs-lookup"><span data-stu-id="1e34b-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="1e34b-273">例如，在呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 方法之前，不會保存交易儲存物件的變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="1e34b-274">如果在呼叫 **Commit** 方法之前 (最終發行) 發行儲存物件，或呼叫 [**IStorage：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) 方法，則這種儲存物件的變更將會遺失。</span><span class="sxs-lookup"><span data-stu-id="1e34b-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="1e34b-275">在交易模式中建立或開啟物件時，實作為必須將原始資料和更新保留給這項資料，如此一來，就可以在必要時還原更新。</span><span class="sxs-lookup"><span data-stu-id="1e34b-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="1e34b-276">這通常是藉由將變更寫入臨時區域，直到認可為止，或建立一個稱為快照集的最新認可資料所執行。</span><span class="sxs-lookup"><span data-stu-id="1e34b-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="1e34b-277">在交易模式中開啟根儲存物件時，可以控制臨時資料和快照集複本的位置和行為，以使用 **STGM \_ NOSCRATCH** 和 **STGM \_ NOSNAPSHOT** 旗標將效能優化。</span><span class="sxs-lookup"><span data-stu-id="1e34b-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="1e34b-278">例如， (從 [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) 函式取得根儲存物件;從 [**IStorage：： OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 方法取得的儲存物件是 substorage 物件。 ) 通常會將暫存資料和快照集儲存在與儲存體不同的暫存檔案中。</span><span class="sxs-lookup"><span data-stu-id="1e34b-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="1e34b-279">這些旗標的影響取決於讀取器和/或存取根儲存體的寫入器數目。</span><span class="sxs-lookup"><span data-stu-id="1e34b-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="1e34b-280">在「單一寫入器」案例中，會開啟交易模式儲存物件以供寫入存取，而不會有檔案的其他存取權。</span><span class="sxs-lookup"><span data-stu-id="1e34b-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="1e34b-281">也就是說，檔案會以 **STGM \_ 交易**、 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 的存取權來開啟，以及共用 **STGM \_ 共用 \_ 獨佔**。</span><span class="sxs-lookup"><span data-stu-id="1e34b-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="1e34b-282">在此情況下，會將儲存物件的變更寫入臨時區域。</span><span class="sxs-lookup"><span data-stu-id="1e34b-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="1e34b-283">當這些變更認可時，它們會複製到原始儲存體。</span><span class="sxs-lookup"><span data-stu-id="1e34b-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="1e34b-284">因此，如果沒有實際對儲存物件進行任何變更，就不會有不必要的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="1e34b-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="1e34b-285">在「多個寫入器」案例中，會開啟交易儲存物件以供寫入存取，但是在這類 asway 中會共用以允許其他寫入器。</span><span class="sxs-lookup"><span data-stu-id="1e34b-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="1e34b-286">也就是說，儲存物件是使用 **STGM \_ 交易**、 **STGM \_ 寫入** 或 **STGM \_ READWRITE** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 讀取** 來開啟。</span><span class="sxs-lookup"><span data-stu-id="1e34b-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="1e34b-287">如果改為指定 **STGM \_ 共用 \_ 拒絕 \_** 的共用，則案例為「多重寫入器、多個讀取器」。</span><span class="sxs-lookup"><span data-stu-id="1e34b-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="1e34b-288">在這些情況下，將會在開啟作業期間進行原始資料的快照集。</span><span class="sxs-lookup"><span data-stu-id="1e34b-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="1e34b-289">因此，即使沒有實際對儲存體進行任何變更，而且也不會同時由另一個寫入器同時開啟，在開啟期間仍需要進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="1e34b-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="1e34b-290">如此一來，您可以在 **STGM \_ 共用 \_ 拒絕 \_ 寫入** 或 **STGM \_ 共用 \_ 獨佔** 模式中開啟儲存物件，以取得最佳的開啟時間效能。</span><span class="sxs-lookup"><span data-stu-id="1e34b-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="1e34b-291">如需有關如何在有多個寫入器時認可變更的詳細資訊，請參閱 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)。</span><span class="sxs-lookup"><span data-stu-id="1e34b-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="1e34b-292">在「單一寫入器、多重讀取器」案例中，會開啟交易儲存物件以供寫入存取，但會與讀取器共用。</span><span class="sxs-lookup"><span data-stu-id="1e34b-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="1e34b-293">也就是說， **STGM \_ 交易** 的寫入器會開啟儲存物件、 **STGM \_ READWRITE** 或 **STGM \_ 寫入** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 寫入**。</span><span class="sxs-lookup"><span data-stu-id="1e34b-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="1e34b-294">儲存體是由具有 **STGM \_ 交易** 的讀取器開啟、 **STGM \_ 讀取** 的存取權，以及共用 **STGM \_ 共用 \_ 拒絕 \_ 無**。</span><span class="sxs-lookup"><span data-stu-id="1e34b-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="1e34b-295">在此情況下，寫入器會使用臨時區域來儲存未認可的變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="1e34b-296">如同上述案例，讀取器會在建立資料的快照集複本時，產生開放時間的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="1e34b-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="1e34b-297">臨時區域通常是暫存檔案，與原始資料分開。</span><span class="sxs-lookup"><span data-stu-id="1e34b-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="1e34b-298">將變更認可至原始檔案時，必須從暫存檔案傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="1e34b-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="1e34b-299">若要避免這種資料傳輸，可能會指定 **STGM \_ NOSCRATCH** 旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="1e34b-300">當指定這個旗標時，會將部分的儲存目的檔用於臨時區域，而不是個別的暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="1e34b-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="1e34b-301">如此一來，就可以快速地執行認可變更，因為需要進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="1e34b-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="1e34b-302">缺點是儲存體檔案可能會變得大於原本的大小，因為它必須成長到足以容納原始資料和臨時區域。</span><span class="sxs-lookup"><span data-stu-id="1e34b-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="1e34b-303">若要合併資料並移除此不必要的區域，請在交易模式中重新開啟根儲存體，但不設定 **STGM \_ NOSCRATCH** 旗標。</span><span class="sxs-lookup"><span data-stu-id="1e34b-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="1e34b-304">然後，使用 **STGC \_ 合併** 旗標集合來呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="1e34b-305">快照集區域（像是臨時區域）也是暫存檔案，而這也會受到 STGM 旗標的影響。</span><span class="sxs-lookup"><span data-stu-id="1e34b-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="1e34b-306">藉由指定 **STGM \_ NOSNAPSHOT** 旗標，並不會建立個別的暫存快照集檔案。</span><span class="sxs-lookup"><span data-stu-id="1e34b-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="1e34b-307">相反地，即使每個物件有一或多個寫入器，仍不會修改原始資料。</span><span class="sxs-lookup"><span data-stu-id="1e34b-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="1e34b-308">認可變更時，這些變更會新增至檔案，但原始資料會維持不變。</span><span class="sxs-lookup"><span data-stu-id="1e34b-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="1e34b-309">這種模式會提高效率，因為它可避免在開啟作業期間建立快照集的需求，而縮短執行時間。</span><span class="sxs-lookup"><span data-stu-id="1e34b-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="1e34b-310">不過，使用此模式可能會產生非常大的儲存體檔案，因為無法覆寫檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="1e34b-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="1e34b-311">這對以 NoSnapshot 模式開啟的檔案大小沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="1e34b-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="1e34b-312">直接單一寫入器，Multiple-Reader 模式</span><span class="sxs-lookup"><span data-stu-id="1e34b-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="1e34b-313">如所述，如果該物件是在交易模式中開啟，則可以有一個儲存物件的單一寫入器和多個讀取器。</span><span class="sxs-lookup"><span data-stu-id="1e34b-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="1e34b-314">您也可以藉由指定 **STGM \_ direct \_ SWMR** 旗標，以直接模式達成單一寫入器的 multireader 案例。</span><span class="sxs-lookup"><span data-stu-id="1e34b-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="1e34b-315">在 **STGM \_ DIRECT \_ SWMR** 模式中，一個呼叫端可以開啟物件以進行讀取/寫入存取，而其他呼叫端同時開啟檔案以供唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="1e34b-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="1e34b-316">搭配 **STGM \_ 交易** 旗標使用此旗標是不正確。</span><span class="sxs-lookup"><span data-stu-id="1e34b-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="1e34b-317">在此模式中，寫入器會開啟具有下列旗標的物件：</span><span class="sxs-lookup"><span data-stu-id="1e34b-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="1e34b-318">**STGM \_DIRECT \_ SWMR** \| **STGM \_ READWRITE** \| **STGM \_ 共用 \_ DENYWRITE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="1e34b-319">而且每個讀取器都會使用下列旗標來開啟物件：</span><span class="sxs-lookup"><span data-stu-id="1e34b-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="1e34b-320">**STGM \_DIRECT \_ SWMR** \| **STGM \_ READ** \| **STGM \_ SHARE \_ DENY \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="1e34b-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="1e34b-321">在此模式中，若要修改儲存物件，寫入器必須取得物件的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="1e34b-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="1e34b-322">當所有讀取器都已關閉時，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="1e34b-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="1e34b-323">寫入器會使用 [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) 介面來取得此獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="1e34b-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="1e34b-324">簡單模式</span><span class="sxs-lookup"><span data-stu-id="1e34b-324">Simple Mode</span></span>

<span data-ttu-id="1e34b-325">簡單模式 (**STGM \_ 簡單** 的) 適用于執行完整儲存作業的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1e34b-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="1e34b-326">它很有效率，但具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="1e34b-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="1e34b-327">Substorages 不存在任何支援。</span><span class="sxs-lookup"><span data-stu-id="1e34b-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="1e34b-328">無法封送處理儲存物件和從中取得的資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="1e34b-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="1e34b-329">每個資料流程都有最小的大小。</span><span class="sxs-lookup"><span data-stu-id="1e34b-329">Each stream has a minimum size.</span></span> <span data-ttu-id="1e34b-330">當資料流程釋出時，如果將最小的位元組寫入資料流程，資料流程就會延伸至最小的大小。</span><span class="sxs-lookup"><span data-stu-id="1e34b-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="1e34b-331">例如，特定 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實值的最小大小為 4 KB。</span><span class="sxs-lookup"><span data-stu-id="1e34b-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="1e34b-332">資料流程會建立，並寫入 1 KB。</span><span class="sxs-lookup"><span data-stu-id="1e34b-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="1e34b-333">在該 **IStream** 的最終版本中，資料流程大小會自動延伸至 4 KB。</span><span class="sxs-lookup"><span data-stu-id="1e34b-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="1e34b-334">接著，開啟資料流程並呼叫 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法會顯示 4 KB 的大小。</span><span class="sxs-lookup"><span data-stu-id="1e34b-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="1e34b-335">並非所有 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 的方法都將受到實作為支援。</span><span class="sxs-lookup"><span data-stu-id="1e34b-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="1e34b-336">如需詳細資訊，請參閱 [IStorage 複合檔案執行](istorage-compound-file-implementation.md)和 [IStream 複合檔案執行](istream-compound-file-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="1e34b-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="1e34b-337">[封送處理](/windows/desktop/Midl/marshaling-ole-data-types) 是封裝、解除封裝和傳送介面方法參數的程式，會在遠端程序呼叫內的執行緒或進程界限內， (RPC) 。</span><span class="sxs-lookup"><span data-stu-id="1e34b-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="1e34b-338">如需詳細資訊，請參閱 [封送處理詳細資料](../com/marshaling-details.md) 和 [介面封送處理](../com/interface-marshaling.md)。</span><span class="sxs-lookup"><span data-stu-id="1e34b-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="1e34b-339">使用簡單模式的建立作業取得儲存體物件時：</span><span class="sxs-lookup"><span data-stu-id="1e34b-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="1e34b-340">可以建立資料流程元素，但無法開啟。</span><span class="sxs-lookup"><span data-stu-id="1e34b-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="1e34b-341">藉由呼叫 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)來建立 stream 元素時，在釋放資料流程物件之前，無法建立另一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="1e34b-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="1e34b-342">寫入所有資料流程之後，請呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 以排清變更。</span><span class="sxs-lookup"><span data-stu-id="1e34b-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="1e34b-343">以簡單模式的開啟作業取得儲存體物件時：</span><span class="sxs-lookup"><span data-stu-id="1e34b-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="1e34b-344">一次只能開啟一個資料流程元素。</span><span class="sxs-lookup"><span data-stu-id="1e34b-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="1e34b-345">您無法藉由呼叫 [**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) 方法，或在資料流程結尾以外搜尋或寫入，來變更資料流程的大小。</span><span class="sxs-lookup"><span data-stu-id="1e34b-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="1e34b-346">不過，因為所有資料流程的大小都是最小值，所以即使原始資料的寫入量較少，也可以將資料流程使用到該大小。</span><span class="sxs-lookup"><span data-stu-id="1e34b-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="1e34b-347">若要判斷資料流程的大小，請使用 [**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法。</span><span class="sxs-lookup"><span data-stu-id="1e34b-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="1e34b-348">請注意，如果儲存物件是由非簡單模式的儲存物件所修改，則無法再以簡單模式開啟該儲存元素。</span><span class="sxs-lookup"><span data-stu-id="1e34b-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e34b-349">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e34b-349">Requirements</span></span>



| <span data-ttu-id="1e34b-350">需求</span><span class="sxs-lookup"><span data-stu-id="1e34b-350">Requirement</span></span> | <span data-ttu-id="1e34b-351">值</span><span class="sxs-lookup"><span data-stu-id="1e34b-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e34b-352">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e34b-352">Minimum supported client</span></span><br/> | <span data-ttu-id="1e34b-353">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1e34b-354">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e34b-354">Minimum supported server</span></span><br/> | <span data-ttu-id="1e34b-355">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1e34b-356">標頭</span><span class="sxs-lookup"><span data-stu-id="1e34b-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e34b-357"><dt>ObjBase。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e34b-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e34b-358">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e34b-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e34b-359">**ISequentialStream：： Read**</span><span class="sxs-lookup"><span data-stu-id="1e34b-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="1e34b-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="1e34b-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="1e34b-361">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="1e34b-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="1e34b-362">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="1e34b-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="1e34b-363">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="1e34b-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="1e34b-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="1e34b-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="1e34b-365">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="1e34b-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="1e34b-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="1e34b-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 


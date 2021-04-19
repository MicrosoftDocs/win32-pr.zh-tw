---
title: IPropertyStorage-NTFS 檔案系統執行
description: 當檔案不是複合檔案時，NTFS 5.0 版會針對 NTFS 磁片區上的檔案提供 IPropertyStorage 介面的執行。
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd Stg.、、NTFS 檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966866"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a><span data-ttu-id="4d7f9-104">IPropertyStorage-NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="4d7f9-104">IPropertyStorage-NTFS File System Implementation</span></span>

<span data-ttu-id="4d7f9-105">當檔案不是複合檔案時，NTFS 5.0 版會針對 NTFS 磁片區上的檔案提供 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面的執行。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-105">The NTFS version 5.0 provides an implementation of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface for files on an NTFS volume when the files are not compound files.</span></span>

<span data-ttu-id="4d7f9-106">**若要取得 IPropertySetStorage NTFS 檔案系統執行的指標**</span><span class="sxs-lookup"><span data-stu-id="4d7f9-106">**To get a pointer to the NTFS file system implementation of IPropertySetStorage**</span></span>

1.  <span data-ttu-id="4d7f9-107">使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 執行來呼叫 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-107">Call [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) using the NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>
2.  <span data-ttu-id="4d7f9-108">使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 執行來呼叫 [**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-108">Call [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) using the NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4d7f9-109">使用時機</span><span class="sxs-lookup"><span data-stu-id="4d7f9-109">When to Use</span></span>

<span data-ttu-id="4d7f9-110">使用 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 來管理單一屬性集內的屬性。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-110">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="4d7f9-111">其方法支援讀取、寫入和刪除屬性，以及可與屬性識別碼相關聯的選擇性字串名稱。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-111">Its methods support reading, writing, and deleting properties and the optional string names that can be associated with property identifiers.</span></span> <span data-ttu-id="4d7f9-112">另一個方法可讓您設定與屬性儲存體相關聯的時間，另一個方法則允許指派 CLSID，用來將其他程式碼（例如使用者介面 (UI) 程式碼）與屬性集建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-112">Another method enables you to set times associated with the property storage, and another permits the assignment of a CLSID, used to associate other code, such as user interface (UI) code, with the property set.</span></span> <span data-ttu-id="4d7f9-113">呼叫 [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 方法會提供指向 NTFS 實 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的指標，可讓您列舉集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-113">Calling the [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the NTFS implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enables you to enumerate the properties in the set.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7f9-114">備註</span><span class="sxs-lookup"><span data-stu-id="4d7f9-114">Remarks</span></span>

<span data-ttu-id="4d7f9-115">NTFS 執行基本上提供與複合檔案執行相同的功能。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-115">The NTFS implementation provides essentially the same features as the compound file implementation.</span></span> <span data-ttu-id="4d7f9-116">如需詳細資訊，請參閱 [IPropertyStorage 複合檔案執行](ipropertystorage-compound-file-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-116">For more information, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

<span data-ttu-id="4d7f9-117">因為 NTFS 是健全的檔案系統，所以 NTFS 屬性集永遠不會處於不正確的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-117">Because NTFS is a robust file system, an NTFS property set will never be left in an incorrect state.</span></span> <span data-ttu-id="4d7f9-118">當 NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的內容排清到基礎 NTFS 檔案時，即使在作業期間發生失敗（例如例外處理常式終止），全部或全部都不會將狀態寫入檔案作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-118">When the content of an NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is flushed to the underlying NTFS file, either all or none of the state is written to the file as an atomic operation, even if there is a failure during the operation such as an abnormal process termination.</span></span> <span data-ttu-id="4d7f9-119">若要以複合檔案執行達到類似的行為，必須在交易模式中開啟父 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-119">To achieve similar behavior with the compound file implementation, the parent [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface must be opened in transacted mode.</span></span>

<span data-ttu-id="4d7f9-120">只有在存取 NTFS 5.0 磁片區上設定的 NTFS 屬性時，才可以使用此等級的穩定性。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-120">This level of robustness is only possible when accessing an NTFS property set on an NTFS 5.0 volume.</span></span> <span data-ttu-id="4d7f9-121">您可以在舊版 NTFS 上存取 NTFS 屬性集 (例如，在 Windows NT 或 Windows 2000 上執行的電腦存取 Windows NT 4.0) 上執行的檔案伺服器電腦上的屬性集，但在發生非預期的失敗時，不保證處於正確的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-121">It is possible to access NTFS property sets on earlier versions of NTFS (for example, a computer running on Windows NT or Windows 2000 that accesses the property sets on a file server computer running on Windows NT 4.0), but they are not guaranteed to be in a correct state in the event of an unexpected failure.</span></span>

<span data-ttu-id="4d7f9-122">雖然 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的 ntfs 執行不支援 transactioning，但 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的 ntfs 實作為支援。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-122">Although the NTFS implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) does not support transactioning, the NTFS implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports it.</span></span> <span data-ttu-id="4d7f9-123">也就是說， **STGM \_ 交易** 可以在 *grfMode* 參數中指定給 **IPropertySetStorage** 的 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)和 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-123">That is, **STGM\_TRANSACTED** may be specified in the *grfMode* parameter to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of **IPropertySetStorage**.</span></span> <span data-ttu-id="4d7f9-124">如同在複合檔案執行中，交易模式只適用于簡單屬性儲存體 (在 *grfFlags* 參數) 中指定 **PROPSETFLAG \_ 簡單**。</span><span class="sxs-lookup"><span data-stu-id="4d7f9-124">As in the compound file implementation, transacted mode is possible only for nonsimple property storages (specifying **PROPSETFLAG\_NONSIMPLE** in the *grfFlags* parameter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d7f9-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d7f9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d7f9-126">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="4d7f9-126">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="4d7f9-127">IPropertySetStorage-NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="4d7f9-127">IPropertySetStorage-NTFS File System Implementation</span></span>](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 
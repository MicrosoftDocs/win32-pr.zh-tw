---
description: VDS 物件模型
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: VDS 物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195646"
---
# <a name="vds-object-model"></a><span data-ttu-id="1d047-103">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="1d047-103">VDS Object Model</span></span>

<span data-ttu-id="1d047-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="1d047-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1d047-105">VDS 可間接存取以主機為基礎的存放裝置，例如磁片和 CD-ROM 裝置，以及由硬體 RAID 控制器管理的磁碟陣列。</span><span class="sxs-lookup"><span data-stu-id="1d047-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="1d047-106">某些儲存體實體會建立實體裝置模型、其他模型虛擬結構：磁片區、磁碟分割等等。</span><span class="sxs-lookup"><span data-stu-id="1d047-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="1d047-107">本主題所描述的物件代表 VDS 的實體和虛擬實體。</span><span class="sxs-lookup"><span data-stu-id="1d047-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="1d047-108">應用程式會呼叫這些物件所公開的方法，而 VDS 會呼叫適當的提供者來執行要求的儲存體作業。</span><span class="sxs-lookup"><span data-stu-id="1d047-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="1d047-109">應用程式永遠不會直接呼叫提供者程式。</span><span class="sxs-lookup"><span data-stu-id="1d047-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="1d047-110">物件分類</span><span class="sxs-lookup"><span data-stu-id="1d047-110">Classification of Objects</span></span>

<span data-ttu-id="1d047-111">如下圖所示，軟體提供者程式會執行以主機為基礎之實體模型的物件;硬體提供者程式會執行模型內部和外部硬體 RAID 裝置的物件;其餘的一般物件是提供者獨立的，或是由 VDS 所執行。</span><span class="sxs-lookup"><span data-stu-id="1d047-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="1d047-112">主軸（不是 VDS 物件）是由磁片或磁片區延伸組成的一般儲存體媒體的一詞。</span><span class="sxs-lookup"><span data-stu-id="1d047-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![顯示物件分類的圖表，定義為「通用物件」、「軟體提供者物件」和「硬體提供者物件」。](images/vdsobjectmodel.png)

<span data-ttu-id="1d047-114">若要深入瞭解每個物件的行為，請從下列主題中選取：</span><span class="sxs-lookup"><span data-stu-id="1d047-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="1d047-115">服務載入器和服務物件，請參閱 [啟動和服務物件](startup-and-service-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1d047-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="1d047-116">列舉和非同步物件，請參閱 [Helper 物件](helper-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1d047-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="1d047-117">提供者物件，請參閱 [提供者物件](provider-object.md)。</span><span class="sxs-lookup"><span data-stu-id="1d047-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="1d047-118">套件、磁片、磁片區和磁片區 plex 物件，請參閱 [軟體提供者物件](software-provider-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1d047-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="1d047-119">子系統、控制器、磁片磁碟機、LUN 和 LUN plex 物件，請參閱 [硬體提供者物件](hardware-provider-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1d047-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="1d047-120">建立物件</span><span class="sxs-lookup"><span data-stu-id="1d047-120">Object Creation</span></span>

<span data-ttu-id="1d047-121">與物件建立相關聯的設定和查詢作業可能需要相當長的時間才能完成;因此，VDS 會以非同步方式叫用所有方法。</span><span class="sxs-lookup"><span data-stu-id="1d047-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="1d047-122">探索提供者會傳回所有完成、錯誤或狀態變更事件。</span><span class="sxs-lookup"><span data-stu-id="1d047-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="1d047-123">軟體提供者也會記錄所有錯誤和重大狀態變更。</span><span class="sxs-lookup"><span data-stu-id="1d047-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="1d047-124">刪除物件</span><span class="sxs-lookup"><span data-stu-id="1d047-124">Object Deletion</span></span>

<span data-ttu-id="1d047-125">有幾個 VDS 方法會刪除或轉換 VDS 物件。</span><span class="sxs-lookup"><span data-stu-id="1d047-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="1d047-126">呼叫端可以在方法傳回之後，透過介面指標來保存參考至已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="1d047-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="1d047-127">當呼叫端釋放介面時，VDS 會刪除物件。</span><span class="sxs-lookup"><span data-stu-id="1d047-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="1d047-128">關於刪除物件，呼叫端應該避免叫用這些介面上的 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法以外的任何內容。</span><span class="sxs-lookup"><span data-stu-id="1d047-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="1d047-129">提供者必須夠健全，才能處理不當呼叫端;如果呼叫端在已刪除的物件上叫用方法，則提供者應該傳回 **\_ \_ \_ 已刪除的 VDS E 物件**。</span><span class="sxs-lookup"><span data-stu-id="1d047-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="1d047-130">服務初始化</span><span class="sxs-lookup"><span data-stu-id="1d047-130">Service Initialization</span></span>

<span data-ttu-id="1d047-131">VDS 會為服務載入器和服務物件提供 (Clsid) 的類別識別碼，但只有服務載入器 Clsid 是公用的。</span><span class="sxs-lookup"><span data-stu-id="1d047-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="1d047-132">當提供者、呼叫的應用程式和服務執行下列工作時，就會進行服務初始化：</span><span class="sxs-lookup"><span data-stu-id="1d047-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="1d047-133">每個新的提供者會在安裝期間叫用 [**IVdsAdmin：： RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) 方法，以向 VDS 註冊。</span><span class="sxs-lookup"><span data-stu-id="1d047-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="1d047-134">呼叫會在系統 hive 下建立登錄機碼，此登錄機碼是由提供者的物件 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="1d047-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="1d047-135">包含在此機碼底下的是提供者物件的 Clsid、名稱、版本，以及提供者的版本 GUID。</span><span class="sxs-lookup"><span data-stu-id="1d047-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="1d047-136">提供者物件 Guid 是永久性的;軟體和硬體物件 Guid 不是。</span><span class="sxs-lookup"><span data-stu-id="1d047-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="1d047-137">應用程式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，並將服務載入器 Clsid 傳遞為引數。</span><span class="sxs-lookup"><span data-stu-id="1d047-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="1d047-138">使用服務載入器物件的指標時，應用程式可以將所需的電腦名稱稱做為參數傳遞至 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法，以從本機或遠端啟動 VDS。</span><span class="sxs-lookup"><span data-stu-id="1d047-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="1d047-139">當初始應用程式附加至服務時，VDS 會先在登錄機碼下找到的每個 Clsid 上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，然後在每個提供者上呼叫 [**IVdsProviderPrivate：： OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) 方法來初始化程式。</span><span class="sxs-lookup"><span data-stu-id="1d047-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d047-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d047-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d047-141">關於 VDS</span><span class="sxs-lookup"><span data-stu-id="1d047-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="1d047-142">**IVdsAdmin：： RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="1d047-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="1d047-143">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="1d047-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="1d047-144">**IVdsProviderPrivate：： OnLoad**</span><span class="sxs-lookup"><span data-stu-id="1d047-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 

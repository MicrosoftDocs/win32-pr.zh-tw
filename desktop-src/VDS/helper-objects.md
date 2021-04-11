---
description: VDS 會提供兩個 helper 物件：列舉物件和 async 物件。 本主題將說明每個物件，並提供呼叫端如何與每個物件搭配使用的範例連結。
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Helper 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195245"
---
# <a name="helper-objects"></a><span data-ttu-id="3dc70-104">Helper 物件</span><span class="sxs-lookup"><span data-stu-id="3dc70-104">Helper Objects</span></span>

<span data-ttu-id="3dc70-105">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="3dc70-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="3dc70-106">VDS 會提供兩個 helper 物件：列舉物件和 async 物件。</span><span class="sxs-lookup"><span data-stu-id="3dc70-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="3dc70-107">本主題將說明每個物件，並提供呼叫端如何與每個物件搭配使用的範例連結。</span><span class="sxs-lookup"><span data-stu-id="3dc70-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="3dc70-108">列舉物件</span><span class="sxs-lookup"><span data-stu-id="3dc70-108">Enumeration Object</span></span>

<span data-ttu-id="3dc70-109">列舉物件會透過指定類型的一組 VDS 物件來列舉。</span><span class="sxs-lookup"><span data-stu-id="3dc70-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="3dc70-110">物件可以是提供者、子系統、控制器、Lun、LUN 的 plex、磁片磁碟機、磁片套件、磁片、磁片區或磁片區的 plex。</span><span class="sxs-lookup"><span data-stu-id="3dc70-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="3dc70-111">呼叫端可以從適當方法所傳回的列舉中選取所需的物件，以取得特定物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3dc70-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="3dc70-112">如需程式碼範例，請參閱 [使用列舉物件](working-with-enumeration-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="3dc70-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="3dc70-113">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="3dc70-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="3dc70-114">類型</span><span class="sxs-lookup"><span data-stu-id="3dc70-114">Type</span></span>                                              | <span data-ttu-id="3dc70-115">元素</span><span class="sxs-lookup"><span data-stu-id="3dc70-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="3dc70-116">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="3dc70-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="3dc70-117">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="3dc70-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="3dc70-118">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="3dc70-118">Associated enumerations</span></span>                           | <span data-ttu-id="3dc70-119">無。</span><span class="sxs-lookup"><span data-stu-id="3dc70-119">None.</span></span>                                    |
| <span data-ttu-id="3dc70-120">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="3dc70-120">Associated structures</span></span>                             | <span data-ttu-id="3dc70-121">無。</span><span class="sxs-lookup"><span data-stu-id="3dc70-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="3dc70-122">Async 物件</span><span class="sxs-lookup"><span data-stu-id="3dc70-122">Async Object</span></span>

<span data-ttu-id="3dc70-123">非同步物件會管理非同步作業。</span><span class="sxs-lookup"><span data-stu-id="3dc70-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="3dc70-124">起始非同步作業的方法會傳回指向 [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) 介面的指標，讓呼叫端可以取消、等候和查詢非同步作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3dc70-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="3dc70-125">長時間執行的 VDS 作業通常會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="3dc70-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="3dc70-126">基本和動態軟體提供者程式會以一致的方式執行磁片區、磁碟分割和磁片作業的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="3dc70-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="3dc70-127">硬體提供者可選擇以非同步方式執行非同步相關的方法。</span><span class="sxs-lookup"><span data-stu-id="3dc70-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="3dc70-128">不論提供者如何執行方法，作業都必須將 [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) 介面的指標傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="3dc70-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="3dc70-129">如需程式碼範例，請參閱 [管理非同步作業](managing-asynchronous-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="3dc70-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="3dc70-130">非同步作業包括：</span><span class="sxs-lookup"><span data-stu-id="3dc70-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="3dc70-131">建立 LUN、磁片區或磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="3dc70-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="3dc70-132">格式化磁片區或磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="3dc70-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="3dc70-133">新增或移除 LUN 或磁片區 plex。</span><span class="sxs-lookup"><span data-stu-id="3dc70-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="3dc70-134">中斷磁片區 plex。</span><span class="sxs-lookup"><span data-stu-id="3dc70-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="3dc70-135">擴充或壓縮 LUN 或磁片區。</span><span class="sxs-lookup"><span data-stu-id="3dc70-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="3dc70-136">復原 LUN 或磁片區。</span><span class="sxs-lookup"><span data-stu-id="3dc70-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="3dc70-137">清理磁片。</span><span class="sxs-lookup"><span data-stu-id="3dc70-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="3dc70-138">更換磁片。</span><span class="sxs-lookup"><span data-stu-id="3dc70-138">Replacing a disk.</span></span>

<span data-ttu-id="3dc70-139">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="3dc70-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="3dc70-140">類型</span><span class="sxs-lookup"><span data-stu-id="3dc70-140">Type</span></span>                                              | <span data-ttu-id="3dc70-141">元素</span><span class="sxs-lookup"><span data-stu-id="3dc70-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="3dc70-142">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="3dc70-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="3dc70-143">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="3dc70-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="3dc70-144">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="3dc70-144">Associated enumerations</span></span>                           | <span data-ttu-id="3dc70-145">無。</span><span class="sxs-lookup"><span data-stu-id="3dc70-145">None.</span></span>                          |
| <span data-ttu-id="3dc70-146">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="3dc70-146">Associated structures</span></span>                             | <span data-ttu-id="3dc70-147">無。</span><span class="sxs-lookup"><span data-stu-id="3dc70-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="3dc70-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="3dc70-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc70-149">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="3dc70-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="3dc70-150">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="3dc70-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="3dc70-151">使用列舉物件</span><span class="sxs-lookup"><span data-stu-id="3dc70-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="3dc70-152">管理非同步作業</span><span class="sxs-lookup"><span data-stu-id="3dc70-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 

---
description: 雖然應用程式可以儲存在登錄中的資料類型和大小有幾種技術限制，但是有一些實用的方針可以提升系統效率。
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: 登錄儲存空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993186"
---
# <a name="registry-storage-space"></a><span data-ttu-id="0a43a-103">登錄儲存空間</span><span class="sxs-lookup"><span data-stu-id="0a43a-103">Registry Storage Space</span></span>

<span data-ttu-id="0a43a-104">雖然應用程式可以儲存在登錄中的資料類型和大小有幾種技術限制，但是有一些實用的方針可以提升系統效率。</span><span class="sxs-lookup"><span data-stu-id="0a43a-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="0a43a-105">應用程式應該將設定和初始化資料儲存在登錄中，並將其他類型的資料儲存在其他位置。</span><span class="sxs-lookup"><span data-stu-id="0a43a-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="0a43a-106">一般來說，包含一或兩個 kb (K) 的資料應儲存為檔案，並使用登錄中的機碼來參考，而不是儲存為值。</span><span class="sxs-lookup"><span data-stu-id="0a43a-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="0a43a-107">應用程式應該將資料儲存為檔案，並參考該檔案，而不是複製登錄中的大型資料片段。</span><span class="sxs-lookup"><span data-stu-id="0a43a-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="0a43a-108">可執行檔二進位程式碼絕不能儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="0a43a-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="0a43a-109">值專案所使用的登錄空間遠少於索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0a43a-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="0a43a-110">為了節省空間，應用程式應該將類似的資料以結構的形式群組在一起，並將結構儲存為值，而不是將每個結構成員儲存為個別的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0a43a-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="0a43a-111"> (將資料儲存為二進位格式，可讓應用程式將資料儲存成一個值，而這些值會由數個不相容的類型組成。 ) </span><span class="sxs-lookup"><span data-stu-id="0a43a-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="0a43a-112">登錄檔的視圖會在分頁集區記憶體中對應。</span><span class="sxs-lookup"><span data-stu-id="0a43a-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="0a43a-113">適用于32位的 **Windows Server 2008、Windows vista （含 SP1），適用于32位、Windows vista、Windows Server 2003、WINDOWS XP：** 登錄檔的視圖會對應到電腦快取位址空間中。</span><span class="sxs-lookup"><span data-stu-id="0a43a-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="0a43a-114">因此，無論登錄資料的大小為何，都不會向 (MB) 收取超過 4 mb 的費用。</span><span class="sxs-lookup"><span data-stu-id="0a43a-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="0a43a-115">登錄 hive 的大小上限為 2 GB，但系統 hive 除外。</span><span class="sxs-lookup"><span data-stu-id="0a43a-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="0a43a-116">**Windows server 2003 （含 SP1）、Windows server 2003 和 WINDOWS XP：** 分頁集區記憶體和磁碟空間中的 hive 可能會耗用的總空間量沒有明確的限制，不過系統配額可能會影響實際的大小上限。</span><span class="sxs-lookup"><span data-stu-id="0a43a-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="0a43a-117">從 Windows Server 2003 （含 Service Pack 2） (SP2) 開始，登錄區的大小上限限制為 2 GB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="0a43a-118">系統 hive 的大小上限會受到實體記憶體的限制，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="0a43a-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="0a43a-119">系統</span><span class="sxs-lookup"><span data-stu-id="0a43a-119">System</span></span>                      | <span data-ttu-id="0a43a-120">系統 hive 的大小上限</span><span class="sxs-lookup"><span data-stu-id="0a43a-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a43a-121">x86 系統</span><span class="sxs-lookup"><span data-stu-id="0a43a-121">x86-based systems</span></span>           | <span data-ttu-id="0a43a-122">50% 的實體記憶體，最高 400 MB。**Windows server 2003 SP2、Windows server 2003 SP1、Windows server 2003 和 WINDOWS XP：** 25% 的實體記憶體，最多可達 200 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="0a43a-123">x64 型系統</span><span class="sxs-lookup"><span data-stu-id="0a43a-123">x64-based systems</span></span>           | <span data-ttu-id="0a43a-124">50% 的實體記憶體，最高 1.5 GB。**Windows Server 2003 SP2：** 系統記憶體的25%，最多 200 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="0a43a-125">**Windows server 2003 （含 SP1）、Windows server 2003 和 WINDOWS XP 64-Bit Edition：** 32 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="0a43a-126">Intel Itanium 型系統</span><span class="sxs-lookup"><span data-stu-id="0a43a-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="0a43a-127">50% 的實體記憶體，最多 1 GB。**Windows server 2008、Windows Vista、Windows server 2003 SP2、Windows server 2003 SP1、Windows server 2003 和 WINDOWS XP 64-Bit Edition：** 32 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="0a43a-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0a43a-128">Windows 2000</span></span>

<span data-ttu-id="0a43a-129">登錄資料儲存在分頁集區中，這是用於系統資料的區域，可在不使用時寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="0a43a-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="0a43a-130">**RegistrySizeLimit** 值會建立所有應用程式的登錄資料可取用的分頁集區數量上限。</span><span class="sxs-lookup"><span data-stu-id="0a43a-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="0a43a-131">此值位於下列登錄機碼中：</span><span class="sxs-lookup"><span data-stu-id="0a43a-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="0a43a-132">根據預設，登錄大小限制為分頁集區的25%。</span><span class="sxs-lookup"><span data-stu-id="0a43a-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="0a43a-133"> (分頁集區的預設大小為 32 MB，因此這是 8 MB。 ) 系統可確保 **RegistrySizeLimit** 的最小值是 4 MB，而最大值大約是 **PagedPoolSize** 值的80%。</span><span class="sxs-lookup"><span data-stu-id="0a43a-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="0a43a-134">如果這個專案的值大於分頁集區大小的80%，系統會將登錄的大小上限設定為分頁集區大小的80%。</span><span class="sxs-lookup"><span data-stu-id="0a43a-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="0a43a-135">這可防止登錄使用進程所需的空間。</span><span class="sxs-lookup"><span data-stu-id="0a43a-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="0a43a-136">請注意，設定這個值並不會在分頁集區中配置空間，也無法確保在需要時可以使用該空間。</span><span class="sxs-lookup"><span data-stu-id="0a43a-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="0a43a-137">分頁集區大小是由下列登錄機碼中的 **PagedPoolSize** 值所決定：</span><span class="sxs-lookup"><span data-stu-id="0a43a-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="0a43a-138">如需如何判斷登錄的目前和最大大小的範例，請參閱 [判斷登錄大小](determining-the-registry-size.md)。</span><span class="sxs-lookup"><span data-stu-id="0a43a-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="0a43a-139">分頁集區的最大值約為 300470 MB，因此登錄大小限制為 240-376 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="0a43a-140">但是，如果使用了/3GB 參數，則分頁集區大小上限為 192 MB，因此登錄最多可達 153.6 MB。</span><span class="sxs-lookup"><span data-stu-id="0a43a-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 





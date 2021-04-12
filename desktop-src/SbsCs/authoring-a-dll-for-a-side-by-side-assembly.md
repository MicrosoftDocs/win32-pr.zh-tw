---
description: 建立您自己的並存元件時，請遵循建立並存元件的指導方針。
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: 撰寫適用于並存元件的 Dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193291"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a><span data-ttu-id="33df1-103">撰寫適用于並存元件的 Dll</span><span class="sxs-lookup"><span data-stu-id="33df1-103">Authoring DLLs for Side-by-side Assemblies</span></span>

<span data-ttu-id="33df1-104">建立您自己的並存元件時，請遵循 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md) ，並根據下列指導方針撰寫元件中所使用的任何 dll：</span><span class="sxs-lookup"><span data-stu-id="33df1-104">When creating your own side-by-side assemblies, follow the [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md) and author any DLLs used in the assembly according to the following guidelines:</span></span>

-   <span data-ttu-id="33df1-105">您的 Dll 應設計成可同時在相同的進程中執行多個版本，而不會干擾彼此。</span><span class="sxs-lookup"><span data-stu-id="33df1-105">Your DLLs should be designed so that multiple versions can run at the same time and in the same process without interfering with each other.</span></span> <span data-ttu-id="33df1-106">例如，許多應用程式會裝載多個外掛程式，且每個外掛程式都需要一個元件的不同版本。</span><span class="sxs-lookup"><span data-stu-id="33df1-106">For example, many applications host multiple plug-ins that each require a different version of one component.</span></span> <span data-ttu-id="33df1-107">並行元件的開發人員必須進行設計和測試，以確保在相同的進程中同時執行多個版本的元件時，可以正常運作。</span><span class="sxs-lookup"><span data-stu-id="33df1-107">The developer the side-by-side assembly needs to design and test to ensure that multiple versions of the component work correctly when run at the same time in the same process.</span></span>

-   <span data-ttu-id="33df1-108">如果您打算在 Windows XP 之前的系統上提供元件作為共用元件，則必須繼續在這些系統上安裝元件，作為單一實例共用元件。</span><span class="sxs-lookup"><span data-stu-id="33df1-108">If you plan to provide your component as a shared component on systems earlier than Windows XP, you need to continue to install the component on these systems as a single-instance shared component.</span></span> <span data-ttu-id="33df1-109">在此情況下，您必須確保您的元件具有回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="33df1-109">In this case, you need to ensure your component is backward compatible.</span></span>

-   <span data-ttu-id="33df1-110">當系統上執行一個以上的元件版本時，請評估物件的使用。</span><span class="sxs-lookup"><span data-stu-id="33df1-110">Evaluate the use of objects when more than one version of your assembly is run on the system.</span></span> <span data-ttu-id="33df1-111">判斷元件的不同版本是否需要個別的資料結構，例如記憶體對應檔、具名管道、已註冊的 Windows 訊息和類別、共用記憶體、信號、mutex 和硬體驅動程式。</span><span class="sxs-lookup"><span data-stu-id="33df1-111">Determine whether different versions of the assembly require separate data structures, such as memory-mapped files, named pipes, registered Windows messages and classes, shared memory, semaphores, mutexes, and hardware drivers.</span></span> <span data-ttu-id="33df1-112">跨元件版本使用的任何資料結構都必須向後相容。</span><span class="sxs-lookup"><span data-stu-id="33df1-112">Any data structures used across assembly versions must be backward-compatible.</span></span> <span data-ttu-id="33df1-113">決定哪些資料結構可以跨版本使用，以及哪些資料結構必須是私用的版本。</span><span class="sxs-lookup"><span data-stu-id="33df1-113">Decide which data structures can be used across versions, and which data structures must be private to a version.</span></span> <span data-ttu-id="33df1-114">判斷共用資料結構是否需要個別的同步處理物件，例如信號和 mutex。</span><span class="sxs-lookup"><span data-stu-id="33df1-114">Determine whether shared data structures require separate synchronization objects, such as semaphores and mutexes.</span></span>

-   <span data-ttu-id="33df1-115">某些物件（例如視窗類別和原子）是每個進程的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="33df1-115">Some objects, such as window classes and Atoms, are uniquely named for each process.</span></span> <span data-ttu-id="33df1-116">應該使用資訊清單為每個元件建立物件（例如視窗類別）的版本。</span><span class="sxs-lookup"><span data-stu-id="33df1-116">Objects such as window classes should be versioned for each assembly using the manifest.</span></span> <span data-ttu-id="33df1-117">對於原子之類的物件，除非您打算在不同版本之間共用，否則請使用版本特定識別碼。</span><span class="sxs-lookup"><span data-stu-id="33df1-117">For objects such as Atoms, use version-specific identifiers unless you plan to share across versions.</span></span> <span data-ttu-id="33df1-118">如果您使用特定版本的識別碼，請使用四部分版本控制編號。</span><span class="sxs-lookup"><span data-stu-id="33df1-118">If you use version-specific identifiers, use the four-part versioning number.</span></span>

-   <span data-ttu-id="33df1-119">請勿在任何 DLL 中包含自我註冊程式碼。</span><span class="sxs-lookup"><span data-stu-id="33df1-119">Include no self-registering code in any DLL.</span></span> <span data-ttu-id="33df1-120">並存元件中的 DLL 無法自我註冊。</span><span class="sxs-lookup"><span data-stu-id="33df1-120">A DLL in a side-by-side assembly cannot be self-registering.</span></span>

-   <span data-ttu-id="33df1-121">使用 define 語句定義 DLL 中所有版本特定的名稱 \# 。</span><span class="sxs-lookup"><span data-stu-id="33df1-121">Define all version-specific names in your DLL with \#define statements.</span></span> <span data-ttu-id="33df1-122">這可讓所有登錄機碼都從一個位置進行變更。</span><span class="sxs-lookup"><span data-stu-id="33df1-122">This enables all registry keys to be changed from one location.</span></span> <span data-ttu-id="33df1-123">當您發行新版本的元件時，您只需要變更這個 \# define 語句。</span><span class="sxs-lookup"><span data-stu-id="33df1-123">When you release a new version of your assembly, you only need to change this \#define statement.</span></span> <span data-ttu-id="33df1-124">例如：</span><span class="sxs-lookup"><span data-stu-id="33df1-124">For example:</span></span>

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   <span data-ttu-id="33df1-125">將任何非持續性資料儲存在 Temp 目錄中。</span><span class="sxs-lookup"><span data-stu-id="33df1-125">Store any nonpersistent data in the Temp directory.</span></span>

-   <span data-ttu-id="33df1-126">請勿將使用者資料放入全域位置。</span><span class="sxs-lookup"><span data-stu-id="33df1-126">Do not put user data into global locations.</span></span> <span data-ttu-id="33df1-127">讓應用程式資料與使用者資料分開。</span><span class="sxs-lookup"><span data-stu-id="33df1-127">Keep application data separate from user data.</span></span>

-   <span data-ttu-id="33df1-128">將相依于應用程式名稱的檔案版本指派給所有共用檔案。</span><span class="sxs-lookup"><span data-stu-id="33df1-128">Assign all shared files a file version that depends upon the application's name.</span></span>

-   <span data-ttu-id="33df1-129">指派跨進程使用的所有訊息和資料結構，以防止意外的跨進程共用。</span><span class="sxs-lookup"><span data-stu-id="33df1-129">Assign all messages and data structures used across processes a version to prevent unintentional cross-process sharing.</span></span>

-   <span data-ttu-id="33df1-130">您的 DLL 不應該相依于不存在的版本之間的共用，例如不會跨不同版本的元件共用的共用記憶體區段。</span><span class="sxs-lookup"><span data-stu-id="33df1-130">Your DLL should not depend upon sharing across versions that may not exist, such as shared memory sections that are not shared across different versions of your assembly.</span></span>

-   <span data-ttu-id="33df1-131">如果您加入的新功能不符合原始 DLL 的二進位介面相容性合約，就必須指派新的 CLSID、ProgId 和檔案名。</span><span class="sxs-lookup"><span data-stu-id="33df1-131">If you add new functionality that does not follow the binary interface compatibility contract of the original DLL, you must assign a new CLSID, ProgId, and file name.</span></span> <span data-ttu-id="33df1-132">然後需要並存元件的未來版本，才能使用此 CLSID、ProgId 和檔案名。</span><span class="sxs-lookup"><span data-stu-id="33df1-132">Future versions of your side-by-side assembly is then required to use this CLSID, ProgId, and file name.</span></span> <span data-ttu-id="33df1-133">這可避免在並存版本上登錄不是並存的 DLL 版本時，發生衝突。</span><span class="sxs-lookup"><span data-stu-id="33df1-133">This prevents a conflict when a version of the DLL that is not side-by-side is registered over a side-by-side version.</span></span>

-   <span data-ttu-id="33df1-134">如果您重複使用相同的 CLSID 或 ProgId，請進行測試以確保元件具有回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="33df1-134">If you reuse the same CLSID or ProgId, test to ensure that the assembly is backward compatible.</span></span>

-   <span data-ttu-id="33df1-135">初始化和設定元件程式碼中元件的預設設定。</span><span class="sxs-lookup"><span data-stu-id="33df1-135">Initialize and set the default settings for the assembly in the assembly code.</span></span> <span data-ttu-id="33df1-136">請勿將預設設定儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="33df1-136">Do not save the defaults settings in the registry.</span></span>

-   <span data-ttu-id="33df1-137">將版本指派給所有資料結構。</span><span class="sxs-lookup"><span data-stu-id="33df1-137">Assign versions to all data structures.</span></span>

-   <span data-ttu-id="33df1-138">您的 DLL 應儲存並存元件的狀態，如 [針對並存元件撰寫狀態儲存體](authoring-state-storage-for-side-by-side-assemblies.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="33df1-138">Your DLL should store the state of the side-by-side assembly as described in [Authoring State Storage for Side-by-Side Assemblies](authoring-state-storage-for-side-by-side-assemblies.md).</span></span>

 

 




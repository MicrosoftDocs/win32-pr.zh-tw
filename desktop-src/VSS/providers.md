---
description: 提供者會管理執行中的磁片區，並視需要建立這些磁片區的陰影複製。
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb336dbb51fcbd715ea236ecdc0c62d81daf29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977861"
---
# <a name="providers"></a><span data-ttu-id="5d15b-103">提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-103">Providers</span></span>

<span data-ttu-id="5d15b-104">[*提供者*](vssgloss-p.md) 會管理執行中的磁片區，並視需要建立這些磁片區的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5d15b-104">[*Providers*](vssgloss-p.md) manage running volumes and create the shadow copies of them on demand.</span></span>

<span data-ttu-id="5d15b-105">為了回應要求者提出的要求，提供者會產生 COM 事件以表示應用程式的陰影複製，然後建立並維護該複本，直到不再需要該複本為止。</span><span class="sxs-lookup"><span data-stu-id="5d15b-105">In response to a request from a requester, a provider generates COM events to signal applications of a coming shadow copy, then creates and maintains that copy until it is no longer needed.</span></span>

<span data-ttu-id="5d15b-106">當陰影複製存在時，提供者會建立一個環境，在此環境中，已有陰影複製的任何磁片區實際上有兩個獨立的複本：一個是正在使用的磁片磁碟機，而另一個則是磁片固定且穩定的備份。</span><span class="sxs-lookup"><span data-stu-id="5d15b-106">While a shadow copy is in existence, the provider creates an environment where there are effectively two independent copies of any volume that has been shadow copied: one the running disk being used and updated as normal, the other a copy that is disk fixed and stable for backup.</span></span>

<span data-ttu-id="5d15b-107">雖然提供了預設提供者作為 Windows 的一部分，但其他廠商也可免費提供自己的實作為其本身的儲存體硬體和軟體供應專案的實施。</span><span class="sxs-lookup"><span data-stu-id="5d15b-107">While a default provider is supplied as part of Windows, other vendors are free to supply their own implementations that are optimized for their own storage hardware and software offerings.</span></span>

<span data-ttu-id="5d15b-108">從使用者或備份/還原應用程式開發人員的觀點來看，所有提供者都有相同的介面 (請參閱) [選取提供者](selecting-providers.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d15b-108">From the point of view of an end-user or backup/restore application developer, all providers will have the same interface (see [Selecting Providers](selecting-providers.md)).</span></span>

<span data-ttu-id="5d15b-109">所有提供者都必須能夠執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="5d15b-109">All providers must be able to do the following:</span></span>

-   <span data-ttu-id="5d15b-110">攔截檔案系統與基礎大型儲存系統之間的 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="5d15b-110">Intercept I/O requests between the file system and the underlying mass storage system.</span></span>
-   <span data-ttu-id="5d15b-111">在陰影複製時，捕捉並取出磁片區的狀態，維護磁片上檔案的「時間點」查看，而不會在其狀態中反映部分 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="5d15b-111">Capture and retrieve the status of a volume at the time of shadow copy, maintaining a "point in time" view of the files on the disk with no partial I/O operations reflected in its state.</span></span>
-   <span data-ttu-id="5d15b-112">您可以使用此「時間點」視圖，在包含陰影複製資料的虛擬磁片區) 的情況下，對啟用 VSS 的應用程式公開 (。</span><span class="sxs-lookup"><span data-stu-id="5d15b-112">Use this "point in time" view to expose (minimally to VSS-enabled applications) a virtual volume containing the shadow copied data.</span></span>

<span data-ttu-id="5d15b-113">視完成的方式而定，提供者可以是下列三種類型之一：</span><span class="sxs-lookup"><span data-stu-id="5d15b-113">Depending on how this is done, a provider can be one of three types:</span></span>

-   [<span data-ttu-id="5d15b-114">系統提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-114">System Provider</span></span>](#system-provider)
-   [<span data-ttu-id="5d15b-115">軟體提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-115">Software Providers</span></span>](#software-providers)
-   [<span data-ttu-id="5d15b-116">硬體提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-116">Hardware Providers</span></span>](#hardware-providers)

## <a name="system-provider"></a><span data-ttu-id="5d15b-117">系統提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-117">System Provider</span></span>

<span data-ttu-id="5d15b-118">系統提供一個陰影複製提供者（ [*系統提供者*](vssgloss-s.md)），是 Windows 作業系統安裝的預設部分。</span><span class="sxs-lookup"><span data-stu-id="5d15b-118">One shadow copy provider, the [*system provider*](vssgloss-s.md), is supplied as a default part of a Windows operating system installation.</span></span> <span data-ttu-id="5d15b-119">目前，系統提供者是軟體提供者的特定實例。</span><span class="sxs-lookup"><span data-stu-id="5d15b-119">Currently, the system provider is a particular instance of a software provider.</span></span> <span data-ttu-id="5d15b-120">不過，未來可能會變更。</span><span class="sxs-lookup"><span data-stu-id="5d15b-120">However, this may change in the future.</span></span>

<span data-ttu-id="5d15b-121">為了維護陰影複製所包含之磁片區的「時間點」視圖，系統提供者會使用寫入時複製技術。</span><span class="sxs-lookup"><span data-stu-id="5d15b-121">To maintain a "point in time" view of a volume contained in the shadow copy, the system provider uses a copy-on-write technique.</span></span> <span data-ttu-id="5d15b-122">磁片上已修改的磁區複本 (稱為「差異」 ) ，因為陰影複製建立的開頭是儲存在陰影複製存放區域中。</span><span class="sxs-lookup"><span data-stu-id="5d15b-122">Copies of the sectors on disk that have been modified (called "diffs") since the beginning of the shadow copy creation are stored in a shadow copy storage area.</span></span>

<span data-ttu-id="5d15b-123">因此，系統提供者可以公開即時磁片區，該磁片區可以正常寫入和讀取，並將「差異」套用至即時磁片區的資料，以有效地公開陰影複製的凍結資料。</span><span class="sxs-lookup"><span data-stu-id="5d15b-123">Therefore, the system provider can expose the live volume, which can be written to and read from normally, and apply the "diffs" to the live volume's data to effectively expose the frozen data of the shadow copy.</span></span>

<span data-ttu-id="5d15b-124">系統提供者的陰影複製存放區域必須位於 NTFS 磁碟區上。</span><span class="sxs-lookup"><span data-stu-id="5d15b-124">For the system provider, the shadow copy storage area must be on an NTFS volume.</span></span> <span data-ttu-id="5d15b-125">要進行陰影複製的磁碟區不需要是 NTFS 磁碟區，但是系統上掛接的磁碟區必須至少有一個是 NTFS 磁碟區。</span><span class="sxs-lookup"><span data-stu-id="5d15b-125">The volume to be shadow copied does not need to be an NTFS volume, but at least one volume mounted on the system must be an NTFS volume.</span></span>

## <a name="software-providers"></a><span data-ttu-id="5d15b-126">軟體提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-126">Software Providers</span></span>

<span data-ttu-id="5d15b-127">軟體陰影複製提供者會在檔案系統與磁片區管理員軟體之間的軟體層中攔截及處理 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="5d15b-127">Software shadow copy providers intercept and process I/O requests in a software layer between the file system and the volume manager software.</span></span> <span data-ttu-id="5d15b-128">這些提供者會實作為使用者模式 DLL 元件，以及至少一個核心模式設備磁碟機，通常 (但不一定) 存放裝置篩選器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5d15b-128">These providers are implemented as a user-mode DLL component and at least one kernel-mode device driver, typically (but not necessarily) a storage filter driver.</span></span> <span data-ttu-id="5d15b-129">建立這些陰影複製的工作是在軟體中完成。</span><span class="sxs-lookup"><span data-stu-id="5d15b-129">The work of creating these shadow copies is done in software.</span></span>

<span data-ttu-id="5d15b-130">軟體陰影複製提供者必須藉由存取一組檔案來維護磁片區的「時間點」視圖，才能在陰影複製之前，用來精確地重新建立磁片區狀態。</span><span class="sxs-lookup"><span data-stu-id="5d15b-130">A software shadow copy provider must maintain a "point-in-time" view of a volume by having access to a set of files that can be used to accurately re-create volume status prior to the shadow copy.</span></span> <span data-ttu-id="5d15b-131">其中一個範例是系統提供者的寫入時複製技術。</span><span class="sxs-lookup"><span data-stu-id="5d15b-131">An example of this is the copy-on-write technique of the system provider.</span></span>

<span data-ttu-id="5d15b-132">不過，VSS 對軟體提供者用來建立和維護陰影複製的技術沒有任何限制，而協力廠商廠商可以自由地依照自己的需要來執行軟體提供者。</span><span class="sxs-lookup"><span data-stu-id="5d15b-132">However, VSS places no restrictions on what technique that software providers use to create and maintain shadow copies, and third-party vendors are free to implement their software providers as they see fit.</span></span>

<span data-ttu-id="5d15b-133">此外，VSS 也提供軟體陰影複製提供者大部分功能的支援，例如定義時間點、資料同步處理和清除、提供備份應用程式的通用介面，以及陰影複製的管理。</span><span class="sxs-lookup"><span data-stu-id="5d15b-133">In addition, VSS provides support for much of the functionality of software shadow copy providers, such as defining the point-in-time, data synchronization and flushing, providing a common interface for backup applications, and management of the shadow copy.</span></span>

<span data-ttu-id="5d15b-134">軟體提供者將依定義適用于比硬體提供者更廣泛的儲存平臺，而且應該能夠同樣地使用基本磁碟或邏輯磁片區。</span><span class="sxs-lookup"><span data-stu-id="5d15b-134">A software provider will, by definition, be applicable to a wider range of storage platforms than a hardware provider, and should be able to work with basic disks or logical volumes equally well.</span></span> <span data-ttu-id="5d15b-135">此一般性犧牲可透過在硬體中執行陰影複製來取得效能，而不會使用任何廠商特定的磁片區捕獲或檔案鏡像功能。</span><span class="sxs-lookup"><span data-stu-id="5d15b-135">This generality sacrifices the performance that may be available by implementing shadow copies in hardware and does not make use of any vendor-specific volume capture or file mirroring features.</span></span>

## <a name="hardware-providers"></a><span data-ttu-id="5d15b-136">硬體提供者</span><span class="sxs-lookup"><span data-stu-id="5d15b-136">Hardware Providers</span></span>

<span data-ttu-id="5d15b-137">硬體陰影複製提供者會在硬體層級與硬體存放裝置介面卡或控制器一起運作，以攔截來自檔案系統的 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="5d15b-137">Hardware shadow copy providers intercept I/O requests from the file system at the hardware level by working in conjunction with a hardware storage adapter or controller.</span></span> <span data-ttu-id="5d15b-138">建立陰影複製的工作是由作業系統以外的主機介面卡、存放裝置或 RAID 控制器所執行。</span><span class="sxs-lookup"><span data-stu-id="5d15b-138">The work of creating the shadow copy is performed by a host adapter, storage appliance, or RAID controller outside of the operating system.</span></span>

<span data-ttu-id="5d15b-139">這些提供者會實作為使用者模式 DLL 元件，並與將公開陰影複製資料的硬體通訊：因此，硬體陰影複製提供者可能需要呼叫或建立其他核心模式元件。</span><span class="sxs-lookup"><span data-stu-id="5d15b-139">These providers are implemented as a user-mode DLL component communicating with the hardware that will expose the shadow copy data: therefore, hardware shadow copy providers may need to call or create other kernel-mode components.</span></span>

<span data-ttu-id="5d15b-140">硬體提供者會公開給整個磁片的 VSS 陰影複製，或 (Lun) 的邏輯單元。</span><span class="sxs-lookup"><span data-stu-id="5d15b-140">Hardware providers expose to VSS shadow copies of entire disks or logical units (LUNs).</span></span> <span data-ttu-id="5d15b-141">要求者仍會處理磁片區的陰影複製;所有磁片區對磁片的對應都是由 VSS 在內部處理。</span><span class="sxs-lookup"><span data-stu-id="5d15b-141">Requesters still deal with shadow copies of volumes; all the volume-to-disk mapping is handled internally by VSS.</span></span> <span data-ttu-id="5d15b-142">由位於動態磁碟上的磁片區之硬體提供者所建立的陰影複製具有特定需求：它們無法匯入到相同的系統上。</span><span class="sxs-lookup"><span data-stu-id="5d15b-142">Shadow copies created by hardware providers of volumes that reside on dynamic disks have a specific requirement:  They cannot be imported onto the same system.</span></span> <span data-ttu-id="5d15b-143">您必須在第二個系統上建立可轉移和匯入的使用者。</span><span class="sxs-lookup"><span data-stu-id="5d15b-143">They must be created transportable and imported on a second system.</span></span>

<span data-ttu-id="5d15b-144">雖然硬體陰影複製提供者會使用可定義時間點的 VSS 功能、允許資料同步處理、管理陰影複製，以及提供備份應用程式的通用介面，但 VSS 不會指定硬體提供者產生和維護陰影複製的基礎機制。</span><span class="sxs-lookup"><span data-stu-id="5d15b-144">While a hardware shadow copy provider makes use of VSS functionality that defines the point in time, allows data synchronization, manages the shadow copy, and provides a common interface with backup applications, VSS does not specify the underlying mechanism by which the hardware provider produces and maintains shadow copies.</span></span>

 

 




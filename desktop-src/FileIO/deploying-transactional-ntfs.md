---
description: 在交易式 NTFS 中快取控制項。
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: 部署交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943851"
---
# <a name="deploying-transactional-ntfs"></a><span data-ttu-id="bb91f-103">部署交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="bb91f-103">Deploying Transactional NTFS</span></span>

<span data-ttu-id="bb91f-104">交易式 NTFS (TxF) ，就像大多數的交易機制一樣，視資料寫入的正確順序而定。</span><span class="sxs-lookup"><span data-stu-id="bb91f-104">Transactional NTFS (TxF), like most transaction mechanisms, depends upon correct ordering of data writes.</span></span> <span data-ttu-id="bb91f-105">確保適當的寫入順序需要明確控制資料快取。</span><span class="sxs-lookup"><span data-stu-id="bb91f-105">Ensuring proper write ordering requires explicit control of data caching.</span></span> <span data-ttu-id="bb91f-106">為了滿足這項需求，TxF 要求磁片磁碟機必須執行屬於標準化磁片磁碟機介面（例如 SCSI、SATA 和 ATA）一部分的快取控制機制。</span><span class="sxs-lookup"><span data-stu-id="bb91f-106">To meet this requirement, TxF requires that disk drives implement the caching control mechanisms that are part of standardized drive interfaces such as SCSI, SATA, and ATA.</span></span>

<span data-ttu-id="bb91f-107">TxF 使用的快取控制機制是稱為「強制單位存取」 (FUA) 函數的旗標。</span><span class="sxs-lookup"><span data-stu-id="bb91f-107">The caching control mechanism used by TxF is a flag known as the Force Unit Access (FUA) function.</span></span> <span data-ttu-id="bb91f-108">此旗標指定磁片磁碟機應該先將資料寫入至穩定的媒體儲存體，才能完成信號。</span><span class="sxs-lookup"><span data-stu-id="bb91f-108">This flag specifies that the drive should write the data to stable media storage before signaling complete.</span></span> <span data-ttu-id="bb91f-109">在交易內的某些關鍵點上，TxF 需要發出 FUA，以確保在發生電源中斷時，不會遺失成功回復交易所需的部分控制資料。</span><span class="sxs-lookup"><span data-stu-id="bb91f-109">At certain critical points within a transaction, TxF needs to issue an FUA to ensure that some control data necessary to successfully rollback a transaction is not lost if a power failure occurs.</span></span>

<span data-ttu-id="bb91f-110">伺服器類別磁片磁碟機 (SCSI 和光纖通道) 一般支援 FUA 旗標。</span><span class="sxs-lookup"><span data-stu-id="bb91f-110">Server-class disk drives (SCSI and Fiber Channel) generally support the FUA flag.</span></span> <span data-ttu-id="bb91f-111">從 Vista 開始，Windows 僅支援 SCSI 和光纖通道磁片的 FUA 旗標。</span><span class="sxs-lookup"><span data-stu-id="bb91f-111">Starting in Vista, Windows supports the FUA flag only for SCSI and Fiber Channel disks.</span></span>

<span data-ttu-id="bb91f-112">在商用磁片磁碟機上 (ATA/SATA/USB) ，TxF 的弱點有一段期間，在這段期間內，磁片磁碟機電源失敗會導致 TxF 無法正確回復交易，因此除非已停用磁片磁碟機的寫入快取，否則資料會保持不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="bb91f-112">On commodity drives (ATA/SATA/USB), TxF has periods of vulnerability during which a drive power failure can result in TxF being unable to correctly rollback the transaction, thus leaving data in an inconsistent state unless the drive's write cache is disabled.</span></span>

<span data-ttu-id="bb91f-113">某些主機匯流排介面卡 (Hba) 和儲存控制器 (例如，RAID 系統) 有內建的電池支援快取。</span><span class="sxs-lookup"><span data-stu-id="bb91f-113">Some Host Bus Adapters (HBAs) and storage controllers (for example, RAID systems) have built-in battery-backed caches.</span></span> <span data-ttu-id="bb91f-114">因為這些裝置會在發生電源錯誤時保留快取的資料，所以任何連接到它們的磁片都不需要接受 FUA 旗標。</span><span class="sxs-lookup"><span data-stu-id="bb91f-114">Because these devices preserve cached data if a power fault occurs, any disks connected to them are not required to honor the FUA flag.</span></span> <span data-ttu-id="bb91f-115">此外，電源供應器受到不斷電供應系統供應 (UPS) 保護的磁片不需要接受 FUA 旗標。</span><span class="sxs-lookup"><span data-stu-id="bb91f-115">Further, a disk whose power supply is protected by an uninterruptable power supply (UPS) does not need to honor the FUA flag.</span></span> <span data-ttu-id="bb91f-116">這是因為 UPS 會維持足夠的電源，足以讓磁片將快取排清至媒體。</span><span class="sxs-lookup"><span data-stu-id="bb91f-116">This is because the UPS will maintain power long enough for the disk to flush its cache to the media.</span></span>

<span data-ttu-id="bb91f-117">停用磁片磁碟機的寫入快取，可避免磁片磁碟機接受 FUA 旗標的需求。</span><span class="sxs-lookup"><span data-stu-id="bb91f-117">Disabling a drive's write cache eliminates the requirement for the drive to honor the FUA flag.</span></span> <span data-ttu-id="bb91f-118">您可以藉由向磁片發出 [**IOCTL 磁片集快取 \_ \_ \_ \_ 資訊**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) 控制項程式碼，來停用磁片的寫入快取。</span><span class="sxs-lookup"><span data-stu-id="bb91f-118">You can disable a disk's write caching by issuing the [**IOCTL\_DISK\_SET\_CACHE\_INFORMATION**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) control code to the disk.</span></span> <span data-ttu-id="bb91f-119">寫入快取 (開啟/關閉) 將會在系統重新開機時保留。</span><span class="sxs-lookup"><span data-stu-id="bb91f-119">The state of the write cache (on/off) will be preserved across system reboots.</span></span> <span data-ttu-id="bb91f-120">發出此控制項程式碼對於發出至該磁片的所有 i/o 都會有相當大的效能影響，這很可能會造成顯著的效能降低。</span><span class="sxs-lookup"><span data-stu-id="bb91f-120">Issuing this control code will have very significant performance consequences for all I/O issued to that disk, which will most likely be a noticeable performance degradation.</span></span> <span data-ttu-id="bb91f-121">在部署之前，應該謹慎考慮使用此控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="bb91f-121">Use of this control code should be carefully considered prior to deployment.</span></span>

> [!Note]  
> <span data-ttu-id="bb91f-122">為了讓 TxF 能以一致的方式保護資料的完整性，系統必須符合下列其中一個準則：</span><span class="sxs-lookup"><span data-stu-id="bb91f-122">For TxF to be capable of consistently protecting your data's integrity through power faults, the system must satisfy at least one of the following criteria:</span></span>
>
> -   <span data-ttu-id="bb91f-123">使用伺服器類別磁片 (SCSI、光纖通道) 。</span><span class="sxs-lookup"><span data-stu-id="bb91f-123">Use server-class disks (SCSI, Fiber Channel).</span></span>
> -   <span data-ttu-id="bb91f-124">確定磁片已連接到電池支援的快取 HBA。</span><span class="sxs-lookup"><span data-stu-id="bb91f-124">Make sure the disks are connected to a battery-backed caching HBA.</span></span>
> -   <span data-ttu-id="bb91f-125">使用儲存體控制器 (例如，RAID 系統) 作為存放裝置。</span><span class="sxs-lookup"><span data-stu-id="bb91f-125">Use a storage controller (for example, RAID system) as the storage device.</span></span>
> -   <span data-ttu-id="bb91f-126">確定磁片的電源受到 UPS 的保護。</span><span class="sxs-lookup"><span data-stu-id="bb91f-126">Ensure power to the disk is protected by a UPS.</span></span>
> -   <span data-ttu-id="bb91f-127">確定磁片的寫入快取功能已停用。</span><span class="sxs-lookup"><span data-stu-id="bb91f-127">Ensure that the disk's write caching feature is disabled.</span></span>

 

 

 




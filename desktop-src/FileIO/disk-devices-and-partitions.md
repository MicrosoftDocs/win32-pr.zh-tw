---
description: 描述硬碟、磁碟分割和主開機記錄。
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: 磁片裝置和磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571670"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="7a90e-103">磁片裝置和磁碟分割</span><span class="sxs-lookup"><span data-stu-id="7a90e-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="7a90e-104">硬碟是由一組堆疊片片所組成，每個都有 electromagnetically 儲存在同心圓或 *追蹤* 中的資料。</span><span class="sxs-lookup"><span data-stu-id="7a90e-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="7a90e-105">每個磁碟片都有兩個標頭，每一端都有一個，在磁片旋轉時讀取或寫入資料。</span><span class="sxs-lookup"><span data-stu-id="7a90e-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="7a90e-106">*硬碟* 控制硬碟的位置、讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="7a90e-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="7a90e-107">請注意，所有光碟的標頭都是以一個單位來放置。</span><span class="sxs-lookup"><span data-stu-id="7a90e-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="7a90e-108">曲目的最小可定址單位是一個 *磁區*。</span><span class="sxs-lookup"><span data-stu-id="7a90e-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="7a90e-109">*圓柱* 會定義為出現在每個片上相同位置中的一組曲目。</span><span class="sxs-lookup"><span data-stu-id="7a90e-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="7a90e-110">例如，下圖顯示具有四個磁碟片的硬碟。</span><span class="sxs-lookup"><span data-stu-id="7a90e-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="7a90e-111">柱面 X 是由每個每一端的 (軌 X) 的曲目組成。</span><span class="sxs-lookup"><span data-stu-id="7a90e-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![硬碟，包括曲目、磁區和磁碟片](images/diskdevice.png)

<span data-ttu-id="7a90e-113">硬碟可以包含一或多個稱為 *磁碟分割* 的邏輯區域。</span><span class="sxs-lookup"><span data-stu-id="7a90e-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="7a90e-114">當使用者將硬碟格式化為 *基本磁碟* 時，會建立磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="7a90e-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="7a90e-115">Windows 也支援 *動態磁碟*，本主題不會討論這些動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="7a90e-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="7a90e-116">如需基本磁碟和動態磁碟的詳細資訊，請參閱 [基本和動態磁碟](basic-and-dynamic-disks.md)。</span><span class="sxs-lookup"><span data-stu-id="7a90e-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="7a90e-117">在磁片上建立多個磁碟分割，可讓您使用不同的硬碟。</span><span class="sxs-lookup"><span data-stu-id="7a90e-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="7a90e-118">例如，具有一個磁碟分割之硬碟的系統會包含單一磁片區，而系統會將該磁片磁碟機指定為磁片磁碟機 C。具有具有兩個磁碟分割之硬碟的系統，通常會包含磁片磁碟機 C 和 D。在硬碟上擁有多個磁碟分割可讓您更輕鬆地管理系統，例如組織檔案或支援多個使用者。</span><span class="sxs-lookup"><span data-stu-id="7a90e-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="7a90e-119">基本磁碟上的第一個實體磁區包含一種資料結構，稱為主開機記錄 (MBR) 。</span><span class="sxs-lookup"><span data-stu-id="7a90e-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="7a90e-120">MBR 包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="7a90e-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="7a90e-121">開機程式 (大小上限為442個位元組) </span><span class="sxs-lookup"><span data-stu-id="7a90e-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="7a90e-122">磁片簽章 (唯一的4位元組數位) </span><span class="sxs-lookup"><span data-stu-id="7a90e-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="7a90e-123">分割資料表最多 (四個專案) </span><span class="sxs-lookup"><span data-stu-id="7a90e-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="7a90e-124"> (永遠 0x55AA) 的 MBR 標記結尾</span><span class="sxs-lookup"><span data-stu-id="7a90e-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a90e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a90e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a90e-126">關於磁片區管理</span><span class="sxs-lookup"><span data-stu-id="7a90e-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="7a90e-127">基本和動態磁碟</span><span class="sxs-lookup"><span data-stu-id="7a90e-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 




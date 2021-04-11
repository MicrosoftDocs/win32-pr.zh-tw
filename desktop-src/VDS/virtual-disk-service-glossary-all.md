---
description: 本節提供虛擬磁碟服務中所使用之技術術語的詞彙， (VDS) 檔。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: 虛擬磁碟服務詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944341"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="fe770-103">虛擬磁碟服務詞彙</span><span class="sxs-lookup"><span data-stu-id="fe770-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="fe770-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="fe770-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fe770-105">本節提供虛擬磁碟服務中所使用之技術術語的詞彙， (VDS) 檔。</span><span class="sxs-lookup"><span data-stu-id="fe770-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="fe770-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic 設定**</span><span class="sxs-lookup"><span data-stu-id="fe770-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-107">硬體 RAID 提供者會提供一組規則，以根據簡單的屬性選擇 LUN 邏輯區塊重新對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="fe770-108">Automagic 提供者也可以動態變更效能或錯誤管理的對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic 提示**</span><span class="sxs-lookup"><span data-stu-id="fe770-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-110">提供給 automagic 提供者的資訊，以引導 LUN 邏輯區塊設定。</span><span class="sxs-lookup"><span data-stu-id="fe770-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="fe770-111">提示包括所需容錯、實體不可部分完成性和預期的 i/o 存取模式的資訊。</span><span class="sxs-lookup"><span data-stu-id="fe770-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**基本磁碟**</span><span class="sxs-lookup"><span data-stu-id="fe770-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-113">由最簡單的可能軟體提供者所管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="fe770-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="fe770-114">基本磁碟提供者僅支援直接對應到分割區設定資料結構的磁片區。</span><span class="sxs-lookup"><span data-stu-id="fe770-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**綁定**</span><span class="sxs-lookup"><span data-stu-id="fe770-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-116">選取一組實體資源的對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**轉換**</span><span class="sxs-lookup"><span data-stu-id="fe770-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-118">將基本磁碟轉換為動態磁碟的程式。</span><span class="sxs-lookup"><span data-stu-id="fe770-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**配置**</span><span class="sxs-lookup"><span data-stu-id="fe770-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-120">作業參數的集合，這些參數會將磁片區或 LUN 的對應提供給實體資源。</span><span class="sxs-lookup"><span data-stu-id="fe770-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**控制器**</span><span class="sxs-lookup"><span data-stu-id="fe770-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-122">包含硬體提供者之運行時間智慧的軟體程式。</span><span class="sxs-lookup"><span data-stu-id="fe770-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**磁片**</span><span class="sxs-lookup"><span data-stu-id="fe770-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-124">實體磁片或硬體 RAID LUN。</span><span class="sxs-lookup"><span data-stu-id="fe770-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="fe770-125">磁片是執行時間儲存體 i/o 負載的目標;隨插即用 (PNP) 不會區分 JBOD 和 Lun。</span><span class="sxs-lookup"><span data-stu-id="fe770-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**磁碟片**</span><span class="sxs-lookup"><span data-stu-id="fe770-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-127">用來從套件匯出或匯入磁片區的元件子集。</span><span class="sxs-lookup"><span data-stu-id="fe770-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**磁片套件**</span><span class="sxs-lookup"><span data-stu-id="fe770-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-129">請參閱 *套件*。</span><span class="sxs-lookup"><span data-stu-id="fe770-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**驅動**</span><span class="sxs-lookup"><span data-stu-id="fe770-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-131">硬體 RAID 子系統內的實體磁片主軸。</span><span class="sxs-lookup"><span data-stu-id="fe770-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="fe770-132">磁片磁碟機會由子系統系結至 Lun。</span><span class="sxs-lookup"><span data-stu-id="fe770-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**動態磁碟**</span><span class="sxs-lookup"><span data-stu-id="fe770-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-134">由軟體 RAID 提供者管理的磁片，支援彈性磁片區重新設定。</span><span class="sxs-lookup"><span data-stu-id="fe770-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="fe770-135">動態磁碟會使用磁碟分割作為磁片區的容器;沒有保證的對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**明確設定**</span><span class="sxs-lookup"><span data-stu-id="fe770-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-137">具有參數的設定，包括磁片區類型和確切的版面配置，適用于目標磁片區的集合。</span><span class="sxs-lookup"><span data-stu-id="fe770-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**出口**</span><span class="sxs-lookup"><span data-stu-id="fe770-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-139">將磁片區和該光碟片上的所有磁片區移出套件的動作。</span><span class="sxs-lookup"><span data-stu-id="fe770-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**程度**</span><span class="sxs-lookup"><span data-stu-id="fe770-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-141">影響單一磁片區或磁片的邏輯磁區連續範圍。</span><span class="sxs-lookup"><span data-stu-id="fe770-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="fe770-142">範圍也可以是未配置磁區的範圍。</span><span class="sxs-lookup"><span data-stu-id="fe770-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="fe770-143">通常，檔案系統會向終端使用者顯示範圍詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fe770-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID 磁碟分割表格 (GPT)**</span><span class="sxs-lookup"><span data-stu-id="fe770-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-145">EFI 固件所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="fe770-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="fe770-146">GPT 是平臺固件用來尋找可開機作業系統或其他可執行映射的兩個最低層級軟體設定資料格式的其中一種。</span><span class="sxs-lookup"><span data-stu-id="fe770-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**硬體提供者**</span><span class="sxs-lookup"><span data-stu-id="fe770-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-148">在主機上執行的軟體集合、匯流排介面卡，以及可能會一起運作以呈現和管理 RAID Lun 的外部存放裝置子系統。</span><span class="sxs-lookup"><span data-stu-id="fe770-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="fe770-149">大部分外部儲存子系統的硬體提供者只包含使用者模式的主機型軟體。</span><span class="sxs-lookup"><span data-stu-id="fe770-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**健康**</span><span class="sxs-lookup"><span data-stu-id="fe770-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-151">磁片區或 LUN 目前的錯誤管理狀態。</span><span class="sxs-lookup"><span data-stu-id="fe770-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**熱備份**</span><span class="sxs-lookup"><span data-stu-id="fe770-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-153">暫時將磁片區 plex 新增至磁片區。</span><span class="sxs-lookup"><span data-stu-id="fe770-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**進口**</span><span class="sxs-lookup"><span data-stu-id="fe770-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-155">將磁片區和其所有磁片區移至現有套件的動作。</span><span class="sxs-lookup"><span data-stu-id="fe770-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**只有一組磁片 (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="fe770-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-157">沒有硬體 RAID 裝置所提供之協調控制項的實體主軸集合。</span><span class="sxs-lookup"><span data-stu-id="fe770-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**邏輯區塊數目 (LBN)**</span><span class="sxs-lookup"><span data-stu-id="fe770-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-159">儲存體資料的最小可定址單位。</span><span class="sxs-lookup"><span data-stu-id="fe770-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="fe770-160">LBN 可與 i/o 命令通訊協定搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fe770-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**邏輯區塊對應**</span><span class="sxs-lookup"><span data-stu-id="fe770-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-162">將呈現給提供者的邏輯區塊轉換成提供者所公開的介面。</span><span class="sxs-lookup"><span data-stu-id="fe770-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**邏輯單元編號 (LUN)**</span><span class="sxs-lookup"><span data-stu-id="fe770-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-164">由硬體 RAID 子系統所呈現的實體可定址儲存體單位。</span><span class="sxs-lookup"><span data-stu-id="fe770-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="fe770-165">此字詞也可以參考儲存體單位的 SCSI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe770-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN 編號**</span><span class="sxs-lookup"><span data-stu-id="fe770-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-167">VDS 硬體提供者指派給陣列中 LUN 的數位。</span><span class="sxs-lookup"><span data-stu-id="fe770-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="fe770-168">這與磁片的 SCSI 位址中的「邏輯單元編號」不同。</span><span class="sxs-lookup"><span data-stu-id="fe770-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**管理服務**</span><span class="sxs-lookup"><span data-stu-id="fe770-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-170">執行磁片區設定、監視或錯誤處理時所需執行的軟體程式。</span><span class="sxs-lookup"><span data-stu-id="fe770-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**映射**</span><span class="sxs-lookup"><span data-stu-id="fe770-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-172">對作業系統公開的磁片區，且具有相關聯的磁片區名稱 (磁碟機號) 。</span><span class="sxs-lookup"><span data-stu-id="fe770-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="fe770-173">磁片區可由檔案系統存取。</span><span class="sxs-lookup"><span data-stu-id="fe770-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**掩蔽**</span><span class="sxs-lookup"><span data-stu-id="fe770-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-175">作業系統無法辨識的磁片。</span><span class="sxs-lookup"><span data-stu-id="fe770-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="fe770-176">磁片可以由硬體 RAID 子系統、交換器、其他電腦主機的 SCSI 保留或磁片堆疊中的軟體遮罩。</span><span class="sxs-lookup"><span data-stu-id="fe770-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**主開機記錄磁碟分割 (MBR)**</span><span class="sxs-lookup"><span data-stu-id="fe770-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-178">MBR 是兩種最低層級軟體設定資料格式的其中一種，可供 BIOS 固件用來找出可開機的作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="fe770-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**成員**</span><span class="sxs-lookup"><span data-stu-id="fe770-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-180">包含在一個以上磁片上的串連磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="fe770-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="fe770-181">磁片只能提供給磁片區的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="fe770-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**鏡子**</span><span class="sxs-lookup"><span data-stu-id="fe770-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-183">維護兩個以上相同資料複本的磁片區或磁片對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="fe770-184">對應的類型也稱為 RAID 層級1。</span><span class="sxs-lookup"><span data-stu-id="fe770-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**包**</span><span class="sxs-lookup"><span data-stu-id="fe770-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-186">邏輯磁片區和基礎磁片的集合。</span><span class="sxs-lookup"><span data-stu-id="fe770-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="fe770-187">套件是磁片區的可轉移關閉單位。</span><span class="sxs-lookup"><span data-stu-id="fe770-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="fe770-188">動態磁碟套件和磁片群組是相同專案的條款。</span><span class="sxs-lookup"><span data-stu-id="fe770-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**同位 stripe**</span><span class="sxs-lookup"><span data-stu-id="fe770-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-190">磁片區或磁片對應，可維護同位檢查資訊和資料。</span><span class="sxs-lookup"><span data-stu-id="fe770-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="fe770-191">每個廠商都會提供確切的對應和保護設定。</span><span class="sxs-lookup"><span data-stu-id="fe770-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="fe770-192">包括 RAID 3、4、5和6。</span><span class="sxs-lookup"><span data-stu-id="fe770-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**部分導向的設定**</span><span class="sxs-lookup"><span data-stu-id="fe770-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-194">未完全明確的磁片區或磁片設定。</span><span class="sxs-lookup"><span data-stu-id="fe770-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="fe770-195">系統會指定系結類型和目標資源的集合;實際的版面配置不是。</span><span class="sxs-lookup"><span data-stu-id="fe770-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="fe770-196">部分導向的設定是最常見的磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="fe770-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**分區**</span><span class="sxs-lookup"><span data-stu-id="fe770-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-198">MBR 或 GPT 結構中單一專案所描述的連續邏輯磁區範圍。</span><span class="sxs-lookup"><span data-stu-id="fe770-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="fe770-199">在基本磁碟上，磁碟分割直接對應至簡單磁片區。</span><span class="sxs-lookup"><span data-stu-id="fe770-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="fe770-200">磁碟分割結構會在 BIOS 或 EFI 平臺固件以及作業系統或其他可開機映射之間共用。</span><span class="sxs-lookup"><span data-stu-id="fe770-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-201"><span id="base.path"></span><span id="BASE.PATH"></span>**路徑**</span><span class="sxs-lookup"><span data-stu-id="fe770-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-202">從電腦到磁片或外部硬體 LUN 的存取路徑。</span><span class="sxs-lookup"><span data-stu-id="fe770-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**叢**</span><span class="sxs-lookup"><span data-stu-id="fe770-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-204">鏡像磁片區或 LUN 的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="fe770-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-205"><span id="base.port"></span><span id="BASE.PORT"></span>**港口**</span><span class="sxs-lookup"><span data-stu-id="fe770-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-206">磁片路徑的端點。</span><span class="sxs-lookup"><span data-stu-id="fe770-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**獨立磁片的多餘陣列 (RAID)**</span><span class="sxs-lookup"><span data-stu-id="fe770-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-208">用來管理多個磁片的技術集合。</span><span class="sxs-lookup"><span data-stu-id="fe770-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**執行時間服務**</span><span class="sxs-lookup"><span data-stu-id="fe770-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-210">以 i/o 要求為基礎執行的軟體程式。</span><span class="sxs-lookup"><span data-stu-id="fe770-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**簡單磁片**</span><span class="sxs-lookup"><span data-stu-id="fe770-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-212">未連線至硬體 RAID 控制器的主軸。</span><span class="sxs-lookup"><span data-stu-id="fe770-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="fe770-213">另請參閱 (JBOD) 的一堆磁片。</span><span class="sxs-lookup"><span data-stu-id="fe770-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="fe770-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**軟體提供者**</span><span class="sxs-lookup"><span data-stu-id="fe770-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-215">以主機為基礎的軟體，可公開邏輯磁片區並在磁片上運作。</span><span class="sxs-lookup"><span data-stu-id="fe770-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="fe770-216">軟體提供者包括核心模式執行時間服務、設定資料和使用者模式管理服務。</span><span class="sxs-lookup"><span data-stu-id="fe770-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**跨度**</span><span class="sxs-lookup"><span data-stu-id="fe770-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-218">多個非連續磁片或磁片區範圍的磁片區或磁片線性對應。</span><span class="sxs-lookup"><span data-stu-id="fe770-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="fe770-219">範圍可以在一或多個磁片區或 Lun 上。</span><span class="sxs-lookup"><span data-stu-id="fe770-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**主軸**</span><span class="sxs-lookup"><span data-stu-id="fe770-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-221">磁片儲存體的實體單位。</span><span class="sxs-lookup"><span data-stu-id="fe770-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**疊加**</span><span class="sxs-lookup"><span data-stu-id="fe770-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-223">藉由執行一個以上的邏輯區塊對應作業，來建立磁片區或 LUN 的動作。</span><span class="sxs-lookup"><span data-stu-id="fe770-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="fe770-224">例如，鏡像等量磁片區。</span><span class="sxs-lookup"><span data-stu-id="fe770-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="fe770-225">在硬體 RAID 所建立的 Lun 之間使用軟體 RAID 時，會發生最常見的堆疊。</span><span class="sxs-lookup"><span data-stu-id="fe770-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**條紋**</span><span class="sxs-lookup"><span data-stu-id="fe770-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-227">磁片區或磁片對應，可在多個磁片區、磁片或磁片磁碟機之間交錯連續的範圍。</span><span class="sxs-lookup"><span data-stu-id="fe770-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="fe770-228">此對應也稱為 RAID 0。</span><span class="sxs-lookup"><span data-stu-id="fe770-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**地位**</span><span class="sxs-lookup"><span data-stu-id="fe770-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-230">磁片區、磁片或磁片磁碟機目前的可用性。</span><span class="sxs-lookup"><span data-stu-id="fe770-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**子系統**</span><span class="sxs-lookup"><span data-stu-id="fe770-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-232">硬體提供者軟體的具現化。</span><span class="sxs-lookup"><span data-stu-id="fe770-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="fe770-233">子系統至少包含一個控制器和一個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fe770-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="fe770-234">如果子系統位於電腦外部，一或多個網路路徑會將子系統連接到電腦。</span><span class="sxs-lookup"><span data-stu-id="fe770-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**轉換狀態**</span><span class="sxs-lookup"><span data-stu-id="fe770-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-236">正在進行變更的邏輯與實體對應的狀態。</span><span class="sxs-lookup"><span data-stu-id="fe770-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**未初始化的磁片**</span><span class="sxs-lookup"><span data-stu-id="fe770-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-238">非套件成員的磁片。</span><span class="sxs-lookup"><span data-stu-id="fe770-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**未遮罩的磁片**</span><span class="sxs-lookup"><span data-stu-id="fe770-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-240">作業系統可以看見的磁片。</span><span class="sxs-lookup"><span data-stu-id="fe770-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="fe770-241">軟體卷管理員、檔案系統等等都可以看見未遮罩磁片的內容。</span><span class="sxs-lookup"><span data-stu-id="fe770-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="fe770-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**體積**</span><span class="sxs-lookup"><span data-stu-id="fe770-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="fe770-243">系結至幾乎連續邏輯區塊範圍的磁片區數。</span><span class="sxs-lookup"><span data-stu-id="fe770-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="fe770-244">您可以透過磁碟機號、掛接的資料夾或磁片區 GUID 路徑來存取磁片區。</span><span class="sxs-lookup"><span data-stu-id="fe770-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 

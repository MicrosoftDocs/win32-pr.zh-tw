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
# <a name="virtual-disk-service-glossary"></a>虛擬磁碟服務詞彙

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

本節提供虛擬磁碟服務中所使用之技術術語的詞彙， (VDS) 檔。

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic 設定**
</dt> <dd>

硬體 RAID 提供者會提供一組規則，以根據簡單的屬性選擇 LUN 邏輯區塊重新對應。 Automagic 提供者也可以動態變更效能或錯誤管理的對應。

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic 提示**
</dt> <dd>

提供給 automagic 提供者的資訊，以引導 LUN 邏輯區塊設定。 提示包括所需容錯、實體不可部分完成性和預期的 i/o 存取模式的資訊。

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**基本磁碟**
</dt> <dd>

由最簡單的可能軟體提供者所管理的磁片。 基本磁碟提供者僅支援直接對應到分割區設定資料結構的磁片區。

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**綁定**
</dt> <dd>

選取一組實體資源的對應。

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**轉換**
</dt> <dd>

將基本磁碟轉換為動態磁碟的程式。

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**配置**
</dt> <dd>

作業參數的集合，這些參數會將磁片區或 LUN 的對應提供給實體資源。

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**控制器**
</dt> <dd>

包含硬體提供者之運行時間智慧的軟體程式。

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**磁片**
</dt> <dd>

實體磁片或硬體 RAID LUN。 磁片是執行時間儲存體 i/o 負載的目標;隨插即用 (PNP) 不會區分 JBOD 和 Lun。

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**磁碟片**
</dt> <dd>

用來從套件匯出或匯入磁片區的元件子集。

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**磁片套件**
</dt> <dd>

請參閱 *套件*。

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**驅動**
</dt> <dd>

硬體 RAID 子系統內的實體磁片主軸。 磁片磁碟機會由子系統系結至 Lun。

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**動態磁碟**
</dt> <dd>

由軟體 RAID 提供者管理的磁片，支援彈性磁片區重新設定。 動態磁碟會使用磁碟分割作為磁片區的容器;沒有保證的對應。

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**明確設定**
</dt> <dd>

具有參數的設定，包括磁片區類型和確切的版面配置，適用于目標磁片區的集合。

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**出口**
</dt> <dd>

將磁片區和該光碟片上的所有磁片區移出套件的動作。

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**程度**
</dt> <dd>

影響單一磁片區或磁片的邏輯磁區連續範圍。 範圍也可以是未配置磁區的範圍。 通常，檔案系統會向終端使用者顯示範圍詳細資料。

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID 磁碟分割表格 (GPT)**
</dt> <dd>

EFI 固件所使用的結構。 GPT 是平臺固件用來尋找可開機作業系統或其他可執行映射的兩個最低層級軟體設定資料格式的其中一種。

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**硬體提供者**
</dt> <dd>

在主機上執行的軟體集合、匯流排介面卡，以及可能會一起運作以呈現和管理 RAID Lun 的外部存放裝置子系統。 大部分外部儲存子系統的硬體提供者只包含使用者模式的主機型軟體。

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**健康**
</dt> <dd>

磁片區或 LUN 目前的錯誤管理狀態。

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**熱備份**
</dt> <dd>

暫時將磁片區 plex 新增至磁片區。

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**進口**
</dt> <dd>

將磁片區和其所有磁片區移至現有套件的動作。

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**只有一組磁片 (JBOD)**
</dt> <dd>

沒有硬體 RAID 裝置所提供之協調控制項的實體主軸集合。

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**邏輯區塊數目 (LBN)**
</dt> <dd>

儲存體資料的最小可定址單位。 LBN 可與 i/o 命令通訊協定搭配使用。

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**邏輯區塊對應**
</dt> <dd>

將呈現給提供者的邏輯區塊轉換成提供者所公開的介面。

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**邏輯單元編號 (LUN)**
</dt> <dd>

由硬體 RAID 子系統所呈現的實體可定址儲存體單位。 此字詞也可以參考儲存體單位的 SCSI 識別碼。

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN 編號**
</dt> <dd>

VDS 硬體提供者指派給陣列中 LUN 的數位。 這與磁片的 SCSI 位址中的「邏輯單元編號」不同。

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**管理服務**
</dt> <dd>

執行磁片區設定、監視或錯誤處理時所需執行的軟體程式。

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**映射**
</dt> <dd>

對作業系統公開的磁片區，且具有相關聯的磁片區名稱 (磁碟機號) 。 磁片區可由檔案系統存取。

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**掩蔽**
</dt> <dd>

作業系統無法辨識的磁片。 磁片可以由硬體 RAID 子系統、交換器、其他電腦主機的 SCSI 保留或磁片堆疊中的軟體遮罩。

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**主開機記錄磁碟分割 (MBR)**
</dt> <dd>

MBR 是兩種最低層級軟體設定資料格式的其中一種，可供 BIOS 固件用來找出可開機的作業系統映射。

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**成員**
</dt> <dd>

包含在一個以上磁片上的串連磁片區集合。 磁片只能提供給磁片區的其中一個成員。

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**鏡子**
</dt> <dd>

維護兩個以上相同資料複本的磁片區或磁片對應。 對應的類型也稱為 RAID 層級1。

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**包**
</dt> <dd>

邏輯磁片區和基礎磁片的集合。 套件是磁片區的可轉移關閉單位。 動態磁碟套件和磁片群組是相同專案的條款。

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**同位 stripe**
</dt> <dd>

磁片區或磁片對應，可維護同位檢查資訊和資料。 每個廠商都會提供確切的對應和保護設定。 包括 RAID 3、4、5和6。

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**部分導向的設定**
</dt> <dd>

未完全明確的磁片區或磁片設定。 系統會指定系結類型和目標資源的集合;實際的版面配置不是。 部分導向的設定是最常見的磁片區設定。

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**分區**
</dt> <dd>

MBR 或 GPT 結構中單一專案所描述的連續邏輯磁區範圍。 在基本磁碟上，磁碟分割直接對應至簡單磁片區。 磁碟分割結構會在 BIOS 或 EFI 平臺固件以及作業系統或其他可開機映射之間共用。

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**路徑**
</dt> <dd>

從電腦到磁片或外部硬體 LUN 的存取路徑。

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**叢**
</dt> <dd>

鏡像磁片區或 LUN 的其中一個成員。

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**港口**
</dt> <dd>

磁片路徑的端點。

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**獨立磁片的多餘陣列 (RAID)**
</dt> <dd>

用來管理多個磁片的技術集合。

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**執行時間服務**
</dt> <dd>

以 i/o 要求為基礎執行的軟體程式。

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**簡單磁片**
</dt> <dd>

未連線至硬體 RAID 控制器的主軸。 另請參閱 (JBOD) 的一堆磁片。

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**軟體提供者**
</dt> <dd>

以主機為基礎的軟體，可公開邏輯磁片區並在磁片上運作。 軟體提供者包括核心模式執行時間服務、設定資料和使用者模式管理服務。

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**跨度**
</dt> <dd>

多個非連續磁片或磁片區範圍的磁片區或磁片線性對應。 範圍可以在一或多個磁片區或 Lun 上。

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**主軸**
</dt> <dd>

磁片儲存體的實體單位。

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**疊加**
</dt> <dd>

藉由執行一個以上的邏輯區塊對應作業，來建立磁片區或 LUN 的動作。 例如，鏡像等量磁片區。 在硬體 RAID 所建立的 Lun 之間使用軟體 RAID 時，會發生最常見的堆疊。

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**條紋**
</dt> <dd>

磁片區或磁片對應，可在多個磁片區、磁片或磁片磁碟機之間交錯連續的範圍。 此對應也稱為 RAID 0。

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**地位**
</dt> <dd>

磁片區、磁片或磁片磁碟機目前的可用性。

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**子系統**
</dt> <dd>

硬體提供者軟體的具現化。 子系統至少包含一個控制器和一個磁片磁碟機。 如果子系統位於電腦外部，一或多個網路路徑會將子系統連接到電腦。

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**轉換狀態**
</dt> <dd>

正在進行變更的邏輯與實體對應的狀態。

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**未初始化的磁片**
</dt> <dd>

非套件成員的磁片。

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**未遮罩的磁片**
</dt> <dd>

作業系統可以看見的磁片。 軟體卷管理員、檔案系統等等都可以看見未遮罩磁片的內容。

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**體積**
</dt> <dd>

系結至幾乎連續邏輯區塊範圍的磁片區數。 您可以透過磁碟機號、掛接的資料夾或磁片區 GUID 路徑來存取磁片區。

</dd> </dl>

 

 

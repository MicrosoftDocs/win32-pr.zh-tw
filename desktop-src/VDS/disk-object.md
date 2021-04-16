---
description: 磁片物件
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: 磁片物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553759"
---
# <a name="disk-object"></a>磁片物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

磁片物件會建立以主機為基礎的實體磁片模型。 在本機主機上執行的軟體提供者可以在 LUN 物件不被遮罩至本機主機時，以磁片形式存取 LUN。 如需 LUN 遮罩的詳細資訊，請參閱 [Lun 物件](lun-object.md)。

每個磁片物件都只占一個套件物件;不過，磁片可將範圍貢獻到套件內的任意數量的磁片區。 您可以將磁片指定為熱備用。

## <a name="partition-to-volume-mapping"></a>磁碟分割與磁片區的對應

作業系統包含基本和動態磁碟的支援。 VDS 提供基本提供者和動態提供者來管理這些磁片類型。 基本磁碟永遠不會容錯。 如果作業系統允許這類磁片區系結，動態磁碟可能會有容錯能力。 基本和動態磁碟可包含根據下列其中一個磁碟分割樣式來結構化的磁碟分割：主開機記錄 (MBR) 或 GUID 磁碟分割表格 (GPT) 。 MBR 分割最多可有四個主要磁碟分割，或三個主要磁碟分割加上一個具有無限邏輯磁片磁碟機的延伸磁碟分割。 GPT 分割最多可提供128個主要磁碟分割。

以下是一般的描述。 它會顯示分割區和磁片區之間的一般關聯性，其中有幾個例外狀況。 如需資料分割與磁片區對應的詳細說明，請參閱 [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) 介面。 磁碟分割與磁片區的對應會根據磁片類型（基本或動態）而有所不同。

-   基本磁碟

    基本磁碟上的磁碟分割會直接對應到磁片區，在大部分情況下，您可以將它的樣式設為 MBR 或 GPT 磁碟分割。 下圖顯示兩個版本的 MBR 磁碟分區的對應。 在第一種情況下，資料分割 (P1 到 P4) 會直接對應到 (V1 到 V4) 的磁片區。 擴充的磁碟分割 (Ext) 以第二個 MBR 樣式取代 P4。 擴充磁碟分割內對應到磁片區的邏輯磁碟機數目是無限制的。

    ![顯示 M B R 分割區的兩個對應選項。](images/vdsbasicmapping.png)

    如果有所有可用的資料分割正在使用中，則在下一個圖中，透過 P128 的 GPT 磁碟分割 (P1) 會直接對應到磁片區 (V1 至 V128) 。 GPT 磁片不會利用延伸磁碟分割來提高可用性。

    ![顯示 GPT 磁碟分割。](images/vdsbasicmappinggpt.png)

-   動態磁碟

    動態磁碟上的特殊磁碟分割類型會對應至大量磁片區。 針對動態提供者所加諸的估計限制，請參閱 [套件物件](pack-object.md)。 如下圖所示，P1 內可以有任意數目的範圍對應到磁片區。

    ![顯示動態磁碟上的特殊磁碟分割類型。](images/vdsdynamicmapping.png)

無論磁片類型為何，磁片都可以包含一或多個磁片區。 磁片區是磁片所公開之連續邏輯區塊的範圍。 例如，磁片區可代表整個磁片區、跨距磁片區的其中一個部分、等量磁片區的其中一個成員，或是鏡像磁片區的一個 plex。

### <a name="working-with-disks"></a>使用磁片

使用 [**IVdsPack：： AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) 方法將磁片新增至現有的套件。 呼叫端可以從 [**IVdsPack：： QueryDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) 方法所傳回的列舉中選取所需的磁片物件，以取得特定磁片的指標。 同樣地，您也可以叫用 [**IVdsDisk：： GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) 方法，以判斷哪一個套件包含指定的磁片。

您可以藉由呼叫 [**IVdsPack：： MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) 方法，將磁片從某個套件移至另一個套件。  (VDS 不支援在基本提供者所控制的套件之間遷移基本磁碟 ) 。您也可以將套件中的所有磁片實際移至新主機，以將套件移至另一部主機。 套件會隨著磁片移動，並顯示為新主機上的外部套件。 如需相關指示，請參閱 [將外部磁片新增至套件](adding-foreign-disks-to-a-pack.md)。

除了物件識別碼、名稱、位址、裝置類型和媒體類型，磁片物件屬性還包括磁片狀態、健全狀況和旗標;以位元組為單位的大小、每個磁區的位元組數、每一曲目的磁區，以及每個圓柱的以及匯流排和磁碟分割類型。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)、 [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline)、 [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk)、 [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2)、 [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)、 [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)和 [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex)。**Windows Server 2008：** 不支援 [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) 介面。<br/> **Windows Vista：** 在 Windows Vista Service Pack 1 (SP1) 之前，不支援 [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) 介面。請改用 [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) 。 不支援 [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) 介面。<br/> **Windows Server 2003：** 不支援 [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2)、 [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2)、 [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline)、 [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)和 [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) 介面。<br/> |
| 此物件可能公開的介面     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable)。  (請參閱 [Lun 物件](lun-object.md) ，以取得磁片為 lun 時所公開的其他介面。 ) <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 相關聯的列舉                           | [**VDS \_磁片 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag)標 [**、 \_ vds 磁片 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_disk_status)、 [**vds 磁片 \_ 分區 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag)標、 [**vds 磁片 \_ 分區 \_ 樣式**](/windows/win32/api/vds/ne-vds-__vds_partition_style)，以及 [**vds \_ 磁片 \_ 區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 相關聯的結構                             | [**VDS \_磁片 \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop)、 [**vds \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)、 [**vds \_ 輸入 \_ 磁片**](/windows/desktop/api/Vds/ns-vds-vds_input_disk)、vds 磁碟分割的 [**\_ \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop)、 [**vds 分割區 \_ \_ 資訊 \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt)、 [**vds 分割區 \_ \_ 資訊 \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)和 [**vds \_ 磁片 \_ 區**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[軟體提供者物件](software-provider-objects.md)
</dt> <dt>

[Pack 物件](pack-object.md)
</dt> <dt>

[LUN 物件](lun-object.md)
</dt> <dt>

[將外部磁片新增至套件](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 


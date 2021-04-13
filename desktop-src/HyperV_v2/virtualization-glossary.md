---
description: Windows 虛擬化 SDK 檔中使用的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Hyper-v 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194554"
---
# <a name="hyper-v-glossary"></a>Hyper-v 詞彙

本主題提供 Windows 虛擬化 SDK 檔中使用的詞彙術語。

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**綁定**
</dt> <dd>

軟體服務和層級連結在一起的進程。 安裝網路服務時，會建立服務的系結關聯性和相依性。

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**檢查站**
</dt> <dd>

虛擬機器的快照，可讓系統管理員將虛擬機器復原到建立檢查點時的狀態。

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**緊湊**
</dt> <dd>

藉由從 .vhd 檔案中移除未使用的空間，減少動態擴充的虛擬硬碟大小。

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**差異虛擬硬碟**
</dt> <dd>

將變更儲存至相關聯之父虛擬硬碟的虛擬硬碟，目的是要讓父系保持不變。 差異磁片是與父磁片之 .vhd 檔案相關聯的個別 .vhd 檔案。 變更會繼續累積到差異磁片，直到它合併到父磁片為止。

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**動態擴充虛擬硬碟**
</dt> <dd>

每次修改時都會成長大小的虛擬硬碟。 這種類型的虛擬硬碟會以 3 KB .vhd 檔案的形式啟動，而且可成長為檔案建立時所指定的大小上限。 減少檔案大小的唯一方法是將已刪除的資料移至零，然後壓縮虛擬硬碟。

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**固定大小的虛擬硬碟**
</dt> <dd>

具有固定大小的虛擬硬碟，並在建立磁片時配置所有空間。 新增或刪除資料時，磁片的大小不會變更。

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**第1代虛擬機器**
</dt> <dd>

虛擬機器 (VM) ，其中包含 Windows 8.1 和 Windows Server 2012 R2 之前的 Hyper-v 版本中存在相同的虛擬硬體

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**第2代虛擬機器**
</dt> <dd>

虛擬機器 (VM) ，其中包含簡化的虛擬硬體模型，並使用 UEFI 固件而非 BIOS。 在此 VM 中，大部分的模擬裝置都會被移除，進而降低管理複雜度和安全性攻擊面。

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**客體作業系統**
</dt> <dd>

在虛擬機器上執行的作業系統。

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**
</dt> <dd>

服務與軟體驅動程式的集合，可將效能最大化，並在虛擬機器中提供更好的使用者體驗。 Integration services 僅適用于支援的客體作業系統。

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**索引鍵/值組**
</dt> <dd>

包含唯一識別碼的資料項目目集，稱為索引鍵，而值則是索引鍵的實際資料。

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**實體電腦**
</dt> <dd>

以硬體為基礎的電腦，而不是以軟體為基礎的虛擬機器。

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**儲存狀態**
</dt> <dd>

一種儲存虛擬機器的方式，讓它可以快速恢復，類似于休眠的膝上型電腦。 當您將執行中的虛擬機器置於儲存狀態時，Virtual Server 和 Hyper-v 會停止該虛擬機器，並將存在於記憶體中的資料寫入暫存檔案，並停止耗用系統資源。 從儲存的狀態還原虛擬機器，會傳回其狀態儲存時的相同條件。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**虛擬磁片**
</dt> <dd>

實體磁碟的檔案形式版本。 虛擬磁片會儲存為副檔名為 .vfd 的檔案。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**虛擬硬碟**
</dt> <dd>

虛擬機器的儲存媒體。 它可以位於主機作業系統可存取的任何存放裝置拓撲上，包括外部裝置、儲存區域網路，以及網路連接的存放裝置。 副檔名為 .vhd。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**虛擬機器**
</dt> <dd>

電腦內的電腦，會在軟體中執行。 虛擬機器會模擬獨立、隔離的環境中完整的硬體系統 (從處理器到網路卡)，讓原本不相容的作業系統能夠同步運作。 每個子作業系統都是在它自己的隔離軟體虛擬機器中執行。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**虛擬機器設定**
</dt> <dd>

指派給虛擬機器的資源設定。 範例包括磁片和網路介面卡等裝置，以及記憶體和處理器。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**虛擬機器管理服務**
</dt> <dd>

提供虛擬機器管理存取權的 Hyper-v 服務。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**虛擬機器快照集**
</dt> <dd>

在特定時間點，以檔案為基礎的狀態、磁片資料和虛擬機器設定快照集。

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**虛擬網路**
</dt> <dd>

實體網路交換器的虛擬版本。 您可以將虛擬網路設定成可以存取一或多部虛擬機器的本機或外部網路資源。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**虛擬網路管理員**
</dt> <dd>

用來建立和管理虛擬網路的 Hyper-v 服務。

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**虛擬交換器**
</dt> <dd>

請參閱虛擬網路。

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX 調整大小**
</dt> <dd>

壓縮或展開虛擬硬碟的操作。

</dd> </dl>

 

 




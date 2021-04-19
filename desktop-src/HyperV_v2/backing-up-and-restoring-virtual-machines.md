---
description: Hyper-v 使用磁碟區陰影複製服務 (VSS) 來備份和還原虛擬機器。
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: 備份和還原虛擬機器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985454"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>備份和還原虛擬機器

Hyper-v 使用磁碟區陰影複製服務 (VSS) 來備份和還原虛擬機器。 如果在客體作業系統中安裝備份 (磁片區快照集) 整合服務，則會安裝 VSS 要求者，讓客體作業系統中的 VSS 寫入器參與虛擬機器的備份。 如需詳細資訊，請參閱下列各節：

-   [備份虛擬機器](#backing-up-the-virtual-machines)
-   [還原虛擬機器](#restoring-the-virtual-machines)
-   [容錯移轉叢集與 Hyper-v VSS](#failover-clustering-and-hyper-v-vss)
-   [Hyper-v VSS 寫入器的詳細資料](#details-on-the-hyper-v-vss-writer)
-   [相關主題](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>備份虛擬機器

Hyper-v 使用兩種機制的其中一種來備份每部虛擬機器。 預設的備份機制稱為「儲存狀態」方法，在此方法中，虛擬機器在處理 PrepareForSnapshot 事件期間會處於儲存狀態，快照集會採用適當的磁片區，而虛擬機器則會在處理 PostSnapshot 事件期間回到先前的狀態。

另一項備份機制稱為「子 VM 快照」方法，它會使用子虛擬機器內的 VSS 來參與備份。 若要支援「子 VM 快照集」方法，必須符合下列所有條件：

-   備份 (磁片區快照集) 整合服務已安裝且正在子虛擬機器中執行。 服務名稱是「Hyper-v 磁片區陰影複製要求者」。
-   子虛擬機器必須處於執行中狀態。
-   虛擬機器的快照集檔案位置會設定為主機作業系統中的相同磁片區，作為虛擬機器的 VHD 檔案。
-   子虛擬機器上的所有磁片區都是基本磁碟，而且沒有動態磁碟。
-   子虛擬機器上的所有磁片都必須使用支援快照集的檔案系統 (例如，NTFS) 。

一般而言，備份虛擬機器的程式與在 [VSS 下處理備份的總覽](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)中所述的步驟相同。 當 Hyper-v VSS 寫入器 (「Hyper-v 虛擬機器管理」服務的一部分) 處理 PrepareForSnapshot 事件時，就會發生獨特的行為。 如果備份是使用「子 VM 快照集」方法完成的，則會進行額外的處理，但是子虛擬機器看不到它。

下列程式說明如何備份虛擬機器。

**備份虛擬機器**

1.  針對寫入器中繼資料中的每個虛擬機器，如果使用「儲存狀態」方法，虛擬機器會進入儲存狀態。 針對使用「子 VM 快照」方法的虛擬機器，子虛擬機器中的 Hyper-v 磁片區陰影複製要求者服務會依照在 [VSS 下處理備份](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)的詳細說明，來處理備份。 子虛擬機器上的所有 VSS 事件都是在 PrepareForSnapshot 事件的主機作業系統處理期間發生。
2.  當所有虛擬機器都處於已儲存狀態或建立快照集之後，Hyper-v VSS 寫入器會從 PrepareForSnapshot 事件中返回。 在凍結和解除凍結事件期間，Hyper-v VSS 寫入器不會進行任何處理。
3.  當 Hyper-v VSS 寫入器處理 PostSnapshot 事件時，使用「儲存狀態」方法備份並由 Hyper-v VSS 寫入器進入儲存狀態的虛擬機器，將會回到備份開始之前的狀態。 針對使用「子 VM 快照集」方法進行備份的虛擬機器，會將拍攝快照集的 VHD 檔案的主機映射回復至處理 PrepareForSnapshot 事件期間所建立的快照集。 這項處理會獨立于子虛擬機器上的 VSS 寫入器完成，因此所建立的快照集必須是可自動復原的。  (**VSS \_ VOLSNAP \_ ATTR \_ \_** 未在內容中設定自動復原。 ) 

不支援部份備份。 如果有任何虛擬機器無法建立快照集，將不會備份任何虛擬機器。

> [!Note]  
> 主機作業系統看不到傳遞和 iSCSI 磁片，因此 Hyper-v VSS 寫入器不會加以備份。 您必須在虛擬機器上完全完成這些磁片區的備份。

 

## <a name="restoring-the-virtual-machines"></a>還原虛擬機器

還原虛擬機器是由主機作業系統完全完成;子虛擬機器上的 VSS 寫入器不包含在其中。

下列程式說明如何還原虛擬機器。

**還原虛擬機器**

1.  在處理 PreRestore 事件期間，Hyper-v VSS 寫入器會關閉，並刪除即將還原的任何虛擬機器。
2.  在所有 VSS 寫入器都處理 PreRestore 事件之後，就會還原檔案。
3.  在處理 PostRestore 事件期間，Hyper-v VSS 寫入器會呼叫 [**>ivsscomponent：： GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) 方法。 如果傳回不是 **VSS \_ RS \_ ALL**，則 hyper-v VSS 寫入器會呼叫 [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure)方法，並從 [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore)方法傳回 **False** 。
4.  針對每個已還原的虛擬機器，Hyper-v VSS 寫入器會向 Hyper-v 管理服務註冊虛擬機器。 如果虛擬機器還原至非預設位置，則會在連結至該位置的預設位置中建立符號連結。
5.  針對每個已還原的 VHD，此位置會與針對該虛擬機器指定的位置進行比較。 如果位置不同，則會使用適當的位置來更新設定。
6.  網路設定已更新。 如果虛擬機器在備份時連接的虛擬交換器仍結束，則會建立新的埠並連接至虛擬機器。

## <a name="failover-clustering-and-hyper-v-vss"></a>容錯移轉叢集與 Hyper-v VSS

Hyper-v VSS 寫入器不會針對屬於容錯移轉叢集一部分的虛擬機器提供任何考慮。 在「儲存狀態」方法備份和所有還原期間，虛擬機器會進入儲存狀態或完全刪除。 叢集服務會看到此錯誤，並導致這些節點上的應用程式容錯移轉至其他節點。 若要在「儲存狀態」備份期間避免此情況，必須使用叢集服務來儲存虛擬機器狀態。 為了避免在還原期間發生此情況，虛擬機器上的資源必須離線。

## <a name="details-on-the-hyper-v-vss-writer"></a>Hyper-v VSS 寫入器的詳細資料

寫入器名稱： Microsoft Hyper-V VSS 寫入器

寫入器識別碼：66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 VSS 下處理備份的總覽](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[在 VSS 下處理還原的總覽](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 

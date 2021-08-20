---
description: 一般情況下，陰影複製的建立方式取決於要建立的陰影複製類型、其內容，以及在陰影複製作業中根據至寫入器的角色。
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: 陰影複製建立詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998128"
---
# <a name="shadow-copy-creation-details"></a>陰影複製建立詳細資料

一般情況下，陰影複製的建立方式取決於要建立的陰影複製類型、其內容，以及在陰影複製作業中根據至寫入器的角色。  (如需詳細資訊，請參閱 [陰影複製內容](shadow-copy-context-configurations.md) 設定。 ) 

陰影複製內容是藉由呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) 方法來設定。 在呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法來建立陰影複製之前，要求者必須依照下列各節所指定的順序來呼叫 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 方法。

## <a name="prerequisites-for-all-shadow-copies"></a>所有陰影複製的必要條件

無論寫入器參與的程度為何，建立任何陰影複製時，一律需要使用 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) 和 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)的呼叫來初始化要求者。

如果未進行此呼叫， [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法會傳回錯誤。

## <a name="shadow-copies-with-writer-participation"></a>具有寫入器參與的陰影複製

如果陰影複製內容指定寫入器參與 (亦即， [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) 是使用 **vss \_ CTX \_ 備份** 來呼叫，或 **vss \_ CTX \_ 應用程式 \_ 復原**) ：

-   當陰影複製內容支援寫入器參與時，要求者一律必須呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 。 如果陰影複製內容支援寫入器參與，而且 **>ivssbackupcomponents：： GatherWriterMetadata** 在 [**:D >ivssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)之前未被呼叫，則會傳回錯誤。
-   如果要求者想要選取特定的寫入器元件，則必須先呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ，然後再呼叫 [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 來建立陰影複製集。
-   您必須呼叫 [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)來建立陰影複製集。
-   要求者可以藉由呼叫 [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)，將一或多個磁片區新增至陰影複製集。 某些寫入器元件可能不會指定任何受影響的磁片區。 在此情況下，快照集可以是空的， (也就是不包含任何) 的磁片區。
-   為了保證寫入器中繼資料的一致性，要求者一律會呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ，即使沒有選取任何元件也一樣。 這會導致 VSS 產生 **PrepareForBackup** 事件，其中 vss 會針對每個參與的寫入器呼叫 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) 方法。
-   VSS 會在建立陰影複製以回應 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)之前，先產生 [*PrepareForSnapshot*](vssgloss-p.md)和 [*凍結*](vssgloss-f.md)事件。 寫入器會處理具有 [**CVssWriter：： OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) 和 [**CVssWriter：： OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)的事件。
-   VSS 會在建立陰影複製以回應 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)時，產生 [*解凍*](vssgloss-t.md)事件和 [*PostSnapshot*](vssgloss-p.md)事件。 寫入器會處理具有 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) 和 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)的事件。

## <a name="shadow-copies-without-writer-participation"></a>不含寫入器參與的陰影複製

不建議在標準備份應用程式中建立不含寫入器參與的陰影複製， (查看 [不含寫入器參與](backups-without-writer-participation.md)) 的備份。

有一些用途（例如磁片的快速備份）可提供安全的網路來防止意外的檔案損毀，而不需要明確的寫入器參與即可進行。 這類陰影複製會有 **vss \_ CTX 檔案 \_ \_ 共用 \_ 備份** 或 **vss \_ CTX \_ NAS \_ 復原** 的內容。

針對此類型的陰影複製，請注意下列事項：

-   要求者仍必須 [針對所有陰影複製](#prerequisites-for-all-shadow-copies)，呼叫必要條件中所列的必要方法。
-   要求者可以呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)，但這並非必要。
-   如果要求者呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)、 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)或 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)，將會傳回錯誤。
-   提供者不會針對這種類型的陰影複製產生 [*PrepareForSnapshot*](vssgloss-p.md)、 [*凍結*](vssgloss-f.md)、 [*解除凍結*](vssgloss-t.md)或 [*PostSnapshot*](vssgloss-p.md) 事件。

 

 




---
description: 可轉移的陰影複製可用於加速快速復原。
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: 使用可轉移陰影複製的磁片區快速復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984741"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>使用可轉移陰影複製的磁片區快速復原

可 [*轉移的陰影複製*](vssgloss-t.md)可用於加速 *快速* 復原。

快速復原可以用來快速還原為較早的陰影複製。 涉及的步驟如下：

1.  建立適當 Lun 的可轉移陰影複製。 陰影複製可以是持續性或非 [*持續*](vssgloss-p.md) 性的。
2.  移除原始 Lun
    1.  如果電腦位於叢集中，請將受影響的磁片資源標示為離線，或啟用這些磁片資源的 [維護模式](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) 。
    2.  從這部電腦遮罩受影響的 Lun (以及如果電腦位於叢集中的所有其他節點) 。
3.  使用 [**>ivssbackupcomponents：： ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) 方法匯入陰影複製。
4.  使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 方法來中斷陰影複製。
5.  將新的陰影複製磁片區標示為讀取/寫入。
6.  如果電腦位於叢集中，則會將新的陰影複製 Lun 公開為原始 Lun。
    1.  將陰影複製 Lun 取消遮罩至叢集中的其他節點。
    2.  將先前標示為離線的資源標記為線上，或停用這些磁片資源的維護模式。

> [!Note]  
> 在 Windows Server 2003 Service Pack 1 (SP1) 之前，不支援叢集中的可轉移陰影複製。 只有符合規範的 Lun 才支援這項功能，其中至少有一個 SCSI 重要產品資料 (VPD) 0x83 \_ 類型1、2或8的儲存體識別碼，以及關聯0，而且 lun 必須維持具有 MBR 磁碟分區的基本磁碟。

 

 

 

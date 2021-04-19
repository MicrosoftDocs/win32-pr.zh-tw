---
description: 要求者可以使用 >ivssbackupcomponents：： BreakSnapshotSet 或 IVssBackupComponentsEx2：： BreakSnapshotSetEx 方法來中斷陰影複製集。
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: 中斷陰影複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985127"
---
# <a name="breaking-shadow-copies"></a>中斷陰影複製

要求者可以使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**IVssBackupComponentsEx2：： BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) 方法來中斷陰影複製集。

中斷陰影複製是包含不會再由 VSS 管理之陰影複製的磁片區。 只有陰影複製的 [*提供者*](vssgloss-p.md) 是 [*硬體提供者*](vssgloss-h.md)時，中斷陰影複製才有意義。 這是因為只有硬體提供者可以使用獨立于 VSS 的生命週期，將陰影複製實作為實際的磁片區。 如果 VSS 無法管理這類磁片區，仍可使用。

軟體提供者只有在與 VSS 作業相關時，才會維護陰影複製。 基於這個理由，中斷陰影複製對軟體提供者沒有任何意義。

如果陰影複製是由硬體提供者所管理，要求者必須先匯入陰影複製，然後再呼叫 [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)。 如果是硬體提供者所建立的無法轉移 () 陰影複製，則會隱含地匯入 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 呼叫的一部分。

要求者呼叫 [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)之後，仍然可以透過其裝置物件或其他存取路徑存取陰影複製集，但不再是陰影複製集。 您可以使用虛擬磁碟服務 (VDS) COM 介面，以一或多個 Lun 的形式來管理。 使用 VDS，要求者可以將 Lun 轉換成讀取/寫入、使用磁碟機號掛接，或遮罩/取消遮罩至其他電腦。 如需詳細資訊，請參閱 [VDS API 檔](../vds/virtual-disk-service-portal.md) 。

 

 

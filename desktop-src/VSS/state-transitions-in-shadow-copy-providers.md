---
description: 陰影複製提供者中的狀態轉換模型，會藉由呼叫 >ivssbackupcomponents：： StartSnapshotSet 時所建立的陰影複製提供者來簡化，直到 >ivssbackupcomponents：:D oSnapshotSet 傳回為止。
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: 陰影複製提供者中的狀態轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d628d11419158f947225b2e4cabd7f93975f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983623"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>陰影複製提供者中的狀態轉換

陰影複製提供者中的狀態轉換模型，會藉由呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 時所建立的陰影複製提供者來簡化，直到 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 傳回為止。 如果有其他要求者嘗試在這段時間內建立陰影複製，呼叫 **StartSnapshotSet** 將會失敗， **並 \_ 設定 VSS E \_ 快照 \_ 集 \_ \_ 進行中**，表示第二個要求者應該等待，然後再試一次。

VSS 只會在要求者呼叫 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)之後呼叫 [**IVssProviderCreateSnapshotSet：： AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) ，即使陰影複製失敗或在這個點之前中止也是如此。 這表示在呼叫 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)之前，提供者不會收到 **AbortSnapshots** 的呼叫。 如果陰影複製在此時間點之前中止或失敗，則在新的陰影複製啟動之前，不會提供任何指示給提供者。 因此，提供者必須做好準備，以便在任何時間點處理對 [**IVssHardwareSnapshotProvider：： BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) 的順序呼叫。 這種跨順序的呼叫代表新陰影複製順序的開頭，且將會有新的陰影複製集識別碼。

 

 




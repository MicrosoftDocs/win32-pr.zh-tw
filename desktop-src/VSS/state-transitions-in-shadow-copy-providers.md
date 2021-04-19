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
# <a name="state-transitions-in-shadow-copy-providers"></a><span data-ttu-id="640ac-103">陰影複製提供者中的狀態轉換</span><span class="sxs-lookup"><span data-stu-id="640ac-103">State Transitions in Shadow Copy Providers</span></span>

<span data-ttu-id="640ac-104">陰影複製提供者中的狀態轉換模型，會藉由呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 時所建立的陰影複製提供者來簡化，直到 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 傳回為止。</span><span class="sxs-lookup"><span data-stu-id="640ac-104">The state transition model in a shadow copy provider is simplified by the serialization of shadow copy creation from the time that [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) is called until the call to [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) returns.</span></span> <span data-ttu-id="640ac-105">如果有其他要求者嘗試在這段時間內建立陰影複製，呼叫 **StartSnapshotSet** 將會失敗， **並 \_ 設定 VSS E \_ 快照 \_ 集 \_ \_ 進行中**，表示第二個要求者應該等待，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="640ac-105">If another requester tries to create a shadow copy during this time, the call to **StartSnapshotSet** will fail with error **VSS\_E\_SNAPSHOT\_SET\_IN\_PROGRESS**, indicating that the second requester should wait and try again.</span></span>

<span data-ttu-id="640ac-106">VSS 只會在要求者呼叫 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)之後呼叫 [**IVssProviderCreateSnapshotSet：： AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) ，即使陰影複製失敗或在這個點之前中止也是如此。</span><span class="sxs-lookup"><span data-stu-id="640ac-106">VSS will only call [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) after the requester has called [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), even if the shadow copy fails or is aborted before this point.</span></span> <span data-ttu-id="640ac-107">這表示在呼叫 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)之前，提供者不會收到 **AbortSnapshots** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="640ac-107">This means that a provider will not receive a call to **AbortSnapshots** until after [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) has been called.</span></span> <span data-ttu-id="640ac-108">如果陰影複製在此時間點之前中止或失敗，則在新的陰影複製啟動之前，不會提供任何指示給提供者。</span><span class="sxs-lookup"><span data-stu-id="640ac-108">If a shadow copy is aborted or fails before this point, the provider is not given any indication until a new shadow copy is started.</span></span> <span data-ttu-id="640ac-109">因此，提供者必須做好準備，以便在任何時間點處理對 [**IVssHardwareSnapshotProvider：： BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) 的順序呼叫。</span><span class="sxs-lookup"><span data-stu-id="640ac-109">For this reason, the provider must be prepared to handle an out-of-sequence call to [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) at any point.</span></span> <span data-ttu-id="640ac-110">這種跨順序的呼叫代表新陰影複製順序的開頭，且將會有新的陰影複製集識別碼。</span><span class="sxs-lookup"><span data-stu-id="640ac-110">This out-of-sequence call represents the start of a new shadow copy sequence and will have a new shadow copy set ID.</span></span>

 

 




---
description: 陰影複製提供者必須符合指導方針，以確保要求者相容性。
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: 陰影複製提供者的必要行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97153d3780701fce6edcde4a4a7740ae1d296b58b2bb44ea38c51f3ab1204499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056386"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>陰影複製提供者的必要行為

陰影複製提供者必須符合指導方針，以確保要求者相容性。 在執行時間，使用陰影複製的備份應用程式或任何其他要求者必須能夠正常運作，而不需要瞭解特定提供者的執行詳細資料。

## <a name="automagic-resource-management"></a>Automagic 資源管理

要求者必須直接將磁片區新增至陰影複製集。 要求者可以指定陰影複製屬性，例如 **vss \_ volsnap \_ attr 可 \_ 轉移**、 **vss \_ volsnap \_ attr \_ 差異**，以及/或 vss volsnap 屬性中的 vss **\_ volsnap \_ \_** [**屬性。 \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) 提供者必須接受這些屬性。 如果無法接受這些屬性，則應該將 \* [**IVssHardwareSnapshotProvider：： AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported)中的 *pbIsSupported* 設定為 **FALSE**，表示不支援陰影複製集。

提供者絕對不能同意支援無法建立的陰影複製。 如果要求者未指定 plex 或差異屬性，則提供者必須包含用來配置陰影複製子系統空間的 automagic 邏輯，並使用最適當的方法來建立陰影複製。 硬體提供者不得包含提供者專屬的 API，以管理所需的陰影複製屬性。

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>建立的陰影複製磁片區會 Read-Only 和隱藏

VSS 會在每個受影響的 LUN 上設定旗標，如此一來，當執行 Windows Server 2003 的電腦偵測到產生的陰影複製磁片區時，就會隱藏和唯讀磁片區。 磁碟機號和掛接的資料夾不會自動指派。 VSS 會在陰影複製的整個生命週期中維護這些旗標。

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>硬體陰影複製 Lun 必須是讀取/寫入

VSS 僅支援將基礎 LUN 對應為讀取/寫入的硬體陰影複製。 這必須在建立陰影複製之前完成;它無法在事實之後完成。 硬體提供者不應修改這些旗標。 如需 VSS 如何使用這些旗標的詳細資訊，請參閱 [陰影複製建立](the-shadow-copy-creation-process.md)程式。

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>Windows Cluster Service 不支援自動匯入硬體陰影複製

Windows叢集服務無法容納具有重複簽章和資料分割配置的 Lun。 陰影複製 Lun 必須傳輸到叢集外部的主機。 如需詳細資訊，請參閱 [使用可轉移陰影複製磁片](fast-recovery-using-transportable-shadow-copied-volumes.md)區的快速復原。

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>包含動態磁碟的陰影複製必須傳輸至不同的主機

**在 Windows Server 2008 之前：** 動態磁碟的原生支援無法容納具有重複簽章和設定資料庫內容的 Lun。 陰影複製 Lun 必須傳輸至不同的主機。 VSS 強制執行這項程式，不允許自動匯入動態磁碟的陰影複製。 要求者不應將可轉移的陰影複製傳回相同的主機。

**從 Windows Server 2008 開始：** 這項限制已移除。

## <a name="providers-are-out-of-process"></a>提供者是跨進程

所有提供者都必須實作為跨進程的 COM 元件。

## <a name="time-critical-operations"></a>Time-Critical 作業

長作業（例如同步處理的 plex）應該在 [**IVssHardwareSnapshotProvider：： BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot)中起始。 此函式應該會啟動非同步準備工作，並快速傳回。 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) 做為「會合」函式，提供者可以在此方法中以同步方式等候，以完成 **BeginPrepareSnapshot** 所啟動的準備工作。

提供者不能在 IVssProviderCreateSnapshotSet 中新增延遲 [**：:P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots)、 [**IVssProviderCreateSnapshotSet：： CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)或 [**IVssProviderCreateSnapshotSet：:P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) ，因為應用程式會在這些呼叫期間凍結。 **CommitSnapshots** 應該會在幾秒鐘內傳回，因為這是在排清和保留期間呼叫的，而且如果在10秒內未收到發行，則 Vss 核心支援會取消排清並保留，而這會導致 VSS 無法進行陰影複製建立程式。 如果提供者需要超過幾秒鐘的時間才能完成此呼叫，則建立陰影複製會失敗的機率很高。

## <a name="careful-io-during-commitsnapshots"></a>CommitSnapshots 期間的小心 i/o

在 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)期間，硬體提供者不需要對陰影複製所牽涉到的磁片區執行任何 i/o。 如果需要任何 i/o，則在處理 **CommitSnapshots** 方法時，提供者不能對原始磁片區起始任何 i/o。

在 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)期間，VSS 核心支援驅動程式會封鎖要陰影複製的原始磁片區的 i/o。 如果提供者將同步 i/o 用於陰影複製集中的磁片區，則該 i/o 將會遭到封鎖，且陰影複製認可程式將會鎖死。 在 **CommitSnapshots** 期間，提供者不應呼叫任何 Win32 api，因為它們會有很高的機率導致 i/o 和鎖死。 VSS 核心支援超時會在10秒後中斷此鎖死，但這會導致陰影複製建立失敗。

如果必須嘗試 i/o，則必須以非同步方式執行。 在所有提供者都從其 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 方法傳回之後，i/o 才會完成。 一般情況下，最好是在 [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) 呼叫中執行這類作業。

## <a name="readwrite-shadow-copy-luns"></a>讀取/寫入陰影複製 Lun

在此版本中，即使將磁片區公開為唯讀，VSS 也只支援讀取/寫入陰影複製 Lun。 原因是系統需要變更磁片上的資料結構，例如：

-   陰影複製程式期間變更的磁片簽章
-   資料分割相關的資料結構，包括指出分割區為唯讀、隱藏、陰影複製，而且不應該指派磁碟機號的資料結構。

## <a name="unique-page-83-information"></a>唯一頁面83資訊

原始 LUN 和新建立的陰影複製 LUN 都必須在頁面83資料中至少有一個唯一的儲存識別碼。 至少有一個 \_ 類型為1、2、3或8的儲存體識別碼，而0的關聯在原始 LUN 和新建立的陰影複製 LUN 上必須是唯一的。

 

 




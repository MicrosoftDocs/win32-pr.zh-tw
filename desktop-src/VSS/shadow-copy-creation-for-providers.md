---
description: 為提供者建立陰影複製
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: 為提供者建立陰影複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026576"
---
# <a name="shadow-copy-creation-for-providers"></a>為提供者建立陰影複製

## <a name="the-shadow-copy-creation-process"></a>陰影複製建立程式

要求者是起始建立陰影複製要求的應用程式。 要求者通常是備份應用程式。 必要時，VSS 會呼叫相關的提供者。 大部分的提供者都有興趣提出要求者的三個特定要求。

1.  要求者會使用 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)的呼叫來開始陰影複製建立活動。 這會產生可唯一識別此特定陰影複製集（SnapshotSetId）的型別 **VSS \_ 識別碼** **GUID** 。 此步驟不涉及此提供者，但 SnapshotSetId 在所有後續步驟中都會廣泛使用。
2.  對於要包含在這個陰影複製集中的每個磁片區，要求者會呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)。 VSS 會決定要使用哪一個提供者來陰影複製磁片區。
    -   多個提供者可能會參與陰影複製集。 例如，如果系統磁碟區和資料磁片區是相同陰影複製集的一部分，系統提供者可能會做為系統磁碟區的陰影複製提供者，而硬體提供者可作為資料磁片區的陰影複製提供者。 這兩個提供者都是相同陰影複製集的一部分，而且使用者預期兩個磁片區都有相同的時間點一致性。
    -   若要選取硬體提供者，硬體提供者必須能夠支援參與指定磁片區的所有 Lun。
    -   所有註冊的提供者都有機會指出陰影複製建立期間的指定磁片區支援。 如果有一個以上的提供者指出支援，則 VSS 會先預設為硬體提供者，然後是軟體提供者，最後是系統提供者 (如果沒有其他提供者指出該磁片區的支援) 。
    -   要求者可以藉由明確指出建立陰影複製所需的提供者，來覆寫此預設順序。
    -   如果有多個硬體提供者支援指定的磁片區，則不保證會呼叫硬體提供者的順序。
3.  在一或多個 [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)呼叫之後，要求者可以使用 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法要求建立陰影複製。 VSS 接著會與系統搭配使用，以建立陰影複製。 **DoSnapshotSet** 方法會以非同步方式執行這項工作，而要求者可以輪詢或等候陰影複製建立程式完成。

下圖顯示要求者、VSS 服務、VSS 核心支援、相關的任何 VSS 寫入器，以及任何 VSS 硬體提供者之間的互動。 如需這些互動的詳細說明，請參閱 [陰影複製建立](the-shadow-copy-creation-process.md) 程式。

![要求者、備份元件、寫入器與提供者之間的互動](images/vssimpl.png)

當陰影複製建立程式完成時，要求者可以判斷是否已成功建立陰影複製，如果不是，則判斷失敗的來源。

寫入器應用程式凍結和解除凍結之間的時間間隔必須最小化。 提供者必須以非同步方式啟動與陰影複製相關的所有準備工作 (例如，在 [**IVssHardwareSnapshotProvider：： BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) 方法中使用具有 plex 的硬體提供者啟動同步處理) ，然後在 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) 方法中等待完成。

有多個提供者必須遵循的時間限制視窗。 如此一來，正常運作的提供者將會在 IVssProviderCreateSnapshotSet 之前執行所有不必要的處理 [**：:P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) 和 [**IVssProviderCreateSnapshotSet 之後：:P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots)。

當呼叫 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 時，會修正陰影複製集。 因為其他磁片區不會共用相同的時間點，所以稍後無法新增其他磁片區。

陰影複製集中有64個磁片區的限制。 特定磁片區可對應至整個 LUN、LUN 的一部分，或多個 Lun 的部分。 大部分的設定會有每個 LUN 一個磁片區，雖然可能有任意的對應。

陰影複製組的數目或原始磁片區的陰影複製集數目沒有任何限制。 提供者可以定義特定的限制，或根據可用的硬體資源來動態地限制。

### <a name="point-in-time-for-writerless-applications"></a>Writerless 應用程式的時間點

VSS 包含特殊支援，可定義陰影複製集中所有磁片區的一般時間點。 硬體提供者不需要直接與這些核心技術互動，因為它們是在一般陰影複製認可處理過程中叫用的。 不過，瞭解所使用的機制會很有用，因為它會說明 writerless 應用程式的「時間點」定義 (未公開 VSS 寫入器介面的應用程式，因此不會參與磁片區陰影複製建立程式。 ) 

此 VSS 核心支援常見的時間點會在 VolSnap.sys 驅動程式、檔案系統和 VSS 之間散發。

1.  在叫用 VSS 核心支援之前，VSS 已：
    1.  判斷要在陰影複製中包含哪些磁片區。
    2.  判斷要在每個磁片區上使用的提供者。
    3.  接受凍結/解除凍結訊息的凍結應用程式。
    4.  藉由呼叫 [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) 方法來備妥陰影複製的提供者。 所有提供者現在都在等候實際建立陰影複製。
2.  然後就會建立時間點。 VSS 會同時清除所有要陰影複製的磁片區上的檔案系統。
    1.  VSS \_ \_ \_ \_ 會在清除檔案系統的每個磁片區上發出 IOCTL VOLSNAP FLUSH 和 HOLD \_ 寫入控制命令。 該 IOCTL 會沿著儲存體堆疊向下傳遞至 VolSnap.sys。 然後，VolSnap.sys 會保留所有寫入的 Irp，直到下方的步驟4為止。 任何檔案系統 (例如未經處理的) 而不支援這個新的 IOCTL 會將未知的 IOCTL 向下傳遞，VolSnap.sys 也會將其保留下來。 在 NTFS 磁片區上，清除也會認可 NTFS 記錄檔。
    2.  這會暫停所有的 NTFS/FAT 中繼資料活動;檔案系統中繼資料已完全認可。
    3.  陰影複製立即： VolSnap.sys 會使所有後續的寫入 Irp 排入所有要陰影複製的磁片區上。
    4.  VolSnap.sys 等候陰影複製的磁片區上的所有暫止寫入完成。 磁片區現在在寫入方面是靜止的，而且在每個磁片區上都有完全靜止的時間。 不保證寫入使用者對應區段或寫入 () 和 (b) 在未執行排清 IOCTL 的檔案系統（例如原始 (）之間。
3.  VSS 會藉由呼叫 [**IVssProviderCreateSnapshotSet：： CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 方法，來指示每個提供者都採用陰影複製。 提供者應完成所有準備工作，如此一來就能快速執行這項操作。

    請注意，i/o 系統只有在執行這些 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 方法時才會靜止。 如果提供者對來源和陰影複製 Lun 執行任何同步處理，則必須先完成這項同步處理，然後才會傳回提供者的 **CommitSnapshots** 方法。 它無法以非同步方式執行。

4.  在最後一個提供者的 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 方法傳回之後，VSS 會釋出所有暫止的寫入 irp (包括在認可路徑結束時封鎖檔案系統的 irp，) 由叫用另一個已傳遞至 VolSnap.sys 的 irp 來封鎖檔案系統。
5.  如果陰影複製程式成功，則 VSS 現在：
    1.  呼叫相關提供者的 [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) 。
    2.  針對涉及的寫入器呼叫 [**CVssWriter：： OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) 。
    3.  通知要求者陰影複製進程已完成。

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots)、 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)、 [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) 都是時間緊迫的。 具有寫入器的應用程式的所有 i/o 都凍結于 **PreCommitSnapshots** 至 **PostCommitSnapshots**;任何延遲都會影響應用程式的可用性。 所有檔案 i/o （包括 writerless 應用程式 i/o）在 **CommitSnapshots** 期間都會暫停。

提供者應該在從 [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)傳回之前，先完成所有時間緊迫的工作。

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 應該在幾秒鐘內傳回。 **CommitSnapshots** 階段位於 [排清] 和 [按住] 視窗內。 如果未在10秒內收到後續版本，vss 核心支援將會取消保留 i/o 的排清和保留，而 VSS 將無法進行陰影複製建立程式。 系統上將會發生其他活動，因此提供者不應依賴10秒的時間。 提供者不應在認可期間呼叫 Win32 Api，因為許多會導致非預期的寫入和封鎖。 如果提供者需要幾秒鐘的時間才能完成通話，則會有很高的機率會失敗。
-   從 [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) 到 [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) 傳回的完整順序會對應到接收凍結和解除凍結事件的寫入器之間的視窗。 此視窗的寫入器預設值為60秒，但寫入器可能會以較小的超時時間覆寫此值。 例如，Microsoft Exchange Server writer 將 timeout 變更為20秒。 提供者不應在此方法中花費超過一或兩個。

在 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) 期間，提供者必須避免任何非分頁檔 i/o;這類 i/o 有很高的死結機率。 尤其是，提供者不應同步寫入任何偵錯工具或追蹤記錄。

 

 




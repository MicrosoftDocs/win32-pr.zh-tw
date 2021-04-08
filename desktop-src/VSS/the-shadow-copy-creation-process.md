---
description: 陰影複製建立程式
ms.assetid: ca484eec-31c6-4790-9232-3ed67263f6fb
title: 陰影複製建立程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4239e2b671edcaeb35b404d9b9411b43316c0212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690476"
---
# <a name="the-shadow-copy-creation-process"></a>陰影複製建立程式

以下是建立陰影複製集時，硬體提供者角色的詳細描述。 如需此程式的圖表，請參閱 [提供者的陰影複製建立](shadow-copy-creation-for-providers.md)。

1.  當要求者將每個磁片區新增至陰影複製集時，VSS 會決定相關聯的 Lun。 例如，跨距磁片區可能由多個 Lun 組成。 VSS 會使用每個 LUN 的實體裝置資訊來建立初始 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information) 。
2.  VSS 會呼叫 [**AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) ，以判斷提供者是否支援該 LUN 的陰影複製。 硬體提供者會使用 [**VDS \_ lun \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information) 來判斷是否支援 lun。 這項決定必須全部或 nothing，相同的硬體提供者必須支援對特定磁片區造成的所有 Lun。 在跨距磁片區範例中，提供者無法表示它只支援組成磁片區的其中一個 Lun。
3.  針對陰影複製集中的每個磁片區，VSS 會使用相同的 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)結構陣列來呼叫 [**IVssHardwareSnapshotProvider：： BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) 。 在單一呼叫中，陣列中的所有 Lun 都是唯一的，但是當相同的 LUN 對多個磁片區有所貢獻時，相同的 LUN 可能會出現在後續的呼叫中。 提供者必須正確處理該案例。
4.  在 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)之後，VSS 會在所有受影響的 lun 上設定唯讀、隱藏、無磁碟機號和陰影複製旗標。 旗標會使用 MBR 磁碟上的隱藏磁區或 GPT 磁片上的磁碟分割標頭專案中的作業系統特定位來執行。 旗標會使受影響磁片上的所有磁片區以唯讀和隱藏的形式呈現在接收電腦上。 請注意，在此階段尚未認可陰影複製的 Lun，因此在系統損毀的情況下，將會清除旗標，且不會影響原始 LUN。 也就是說，原始 LUN 上的所有磁片區都會被視為正常，並保留其原始磁碟機號指派、掛接的資料夾和讀取/寫入狀態。
    > [!Note]  
    > 提供者不應嘗試修改任何 LUN 旗標。

     

5.  在 [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)時，會認可陰影複製 lun。 **CommitSnapshots** 應該在幾秒鐘內傳回，否則整個陰影複製建立程式可能會失敗。
6.  [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)之後，VSS 會清除所有涉及陰影複製的原始 lun 上的旗標。 由於陰影複製 Lun 此時已認可，陰影複製 Lun 會保留這些旗標。
7.  [**IVssProviderCreateSnapshotSet 之後:P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots)之後，VSS 會清除在 [**IVssProviderCreateSnapshotSet：： EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)) 之後設定的 LUN 旗 (標，並通知寫入器解除凍結。 VSS 接著會呼叫提供者的 [**IVssProviderCreateSnapshotSet：:P refinalcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots) 和 [**IVssProviderCreateSnapshotSet：:P ostfinalcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots) 方法。
8.  VSS 會藉由呼叫 [**IVssHardwareSnapshotProvider：： GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns)，來抓取 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)結構的陣列，每個新建立的陰影複製 LUN 都有一個陣列。 提供者必須提供足夠的資訊，讓 VSS 和提供者可以在稍後以及任何連線至子系統的系統上，識別陰影複製。 目前，此電腦應該無法存取陰影複製 Lun，提供者必須使用以外的機制，而不是從 LUN 讀取資訊。
9.  針對可轉移的陰影複製，VSS 會將下列內容附加至描述陰影複製集的備份元件檔：
    1.  原始的 LUN [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information) 陣列。
    2.  新的陰影複製 LUN [**VDS \_ lun \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information) 陣列。
    3.  陰影複製集中每個磁片區的磁片區。
10. 若為自動匯入陰影複製，則會開始匯入程式。 在 [**IVssHardwareSnapshotProvider：： LocateLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-locateluns)中，提供者會在建立時獲得 [**GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns)中產生的 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)。 在 **LocateLuns** 期間，提供者應該讓系統看到這些陰影複製 lun。 提供者不應造成匯流排重新掃描。 VSS 會導致重新掃描和列舉，以允許 PNP 探索 Lun，並讓磁片區上線。
11. VSS 會針對系統中新抵達的磁片呼叫 [**IVssHardwareSnapshotProvider：： FillInLunInfo**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-fillinluninfo) 。 VSS 會使用 **FillInLunInfo** 中的陰影複製 lun [**VDS \_ lun \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)陣列，並將其與在 [**GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns)建立期間產生的 **VDS \_ lun \_ 資訊** 進行比較，以及陰影複製集中每個磁片區的磁片區，以識別新抵達的陰影複製 lun。
12. 此時，陰影複製 Lun 上包含的所有磁片區都是隱藏和唯讀的，而 VSS 具有從原始磁片區到陰影複製磁片區的對應。

因為單一 LUN 可包含多個磁片區的一部分，所以陰影複製 Lun 的集合可能包含「額外」的磁片區。 這些磁片區不是陰影複製集的一部分，因此不應使用，因為它們不保證一致。

匯入之後，可以透過 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) 方法存取陰影複製。 您也可以使用 [**>ivssbackupcomponents：： ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot)，將陰影複製公開為磁碟機號、裝載的資料夾或共用。 您也可以使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 方法，將陰影複製集轉換為一般 LUN。 從該處，管理應用程式可以使用適當的磁片管理 Api 來進一步管理 LUN (例如) 變更讀取/寫入屬性。

### <a name="transportable-shadow-copies-on-a-san"></a>SAN 上的可轉移陰影複製

從 Windows Server 2003、Datacenter Edition 和 Windows Server 2003 （Enterprise Edition）開始，VSS 在 SAN 上可提供可轉移的陰影複製集。 從提供者的觀點來看，可在主機之間傳輸 Lun 的觀點來看，不可傳輸和可轉移的陰影複製集之間幾乎沒有任何差異。

**Windows server 2003、Standard Edition、Windows server 2003、Web Edition 和 WINDOWS XP：** 不支援可轉移的陰影複製集。 所有版本的 Windows Server 2003 Service Pack 1 (SP1) 支援可轉移的陰影複製集。

您必須建立可轉移的陰影複製集，並將 **vss \_ VOLSNAP \_ ATTR 可 \_ 轉移** 屬性新增至 [**\_ vss \_ 磁片區快照集 \_ \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉所描述的陰影複製內容中。 集合中的所有磁片區都必須是可轉移的。 藉由從 [**IVssHardwareSnapshotProvider：： AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported)傳回成功，提供者會指出不僅支援 lun，也可傳輸 lun。 當 VSS 在備份元件檔中記錄 LUN 資訊時，會建立可轉移的陰影複製集。 只有在初始建立之後，才能匯入陰影複製集。

在接收電腦上，要求者會匯入陰影複製集。 [**>ivssbackupcomponents：： ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots)方法會使用描述陰影複製集做為輸入的備份元件檔。 匯入的方式如下：

1.  VSS 會從備份元件檔中，建立陰影複製 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information) 結構的陣列。
2.  當 VSS 呼叫 [**IVssHardwareSnapshotProvider：： LocateLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-locateluns)時，在 [**IVssHardwareSnapshotProvider：： GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns)中產生的 [**VDS \_ LUN \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)結構陣列將會傳遞給提供者。 處理此方法時，提供者應該讓系統能夠看見這些陰影複製 Lun。 提供者不應造成匯流排重新掃描。 VSS 將會觸發重新掃描和列舉，以允許 PNP 探索 Lun，並讓磁片區上線。
3.  VSS 會針對系統中新抵達的磁片呼叫 [**IVssHardwareSnapshotProvider：： FillInLunInfo**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-fillinluninfo) 。 VSS 會使用 **FillInLunInfo** 中的 [**vds \_ lun \_ 資訊**](/windows/win32/api/vdslun/ns-vdslun-vds_lun_information)結構的陰影複製 LUN 陣列，並將其與在 [**GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns)中建立陰影複製集時所產生的 **vds \_ lun \_ 資訊** 進行比較，以及陰影複製集中每個磁片區的磁片區，以識別新抵達的陰影複製 lun。
4.  此時，已傳輸 Lun 上包含的所有磁片區都會被掛接為隱藏和唯讀，而 VSS 具有從原始磁片區到陰影複製磁片區的對應。

針對單一機器和可轉移的情況，從呼叫 [**GetTargetLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns) 的點開始，順序會很類似。 針對自動匯入，步驟會在建立後直接進行。

 

 

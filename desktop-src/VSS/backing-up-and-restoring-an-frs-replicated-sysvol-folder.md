---
description: 本主題說明如何判斷 DFSR 或 FSR 是否複寫 SYSVOL 資料夾，並說明如何備份和還原 FRS 複寫的 SYSVOL 資料夾。
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: 備份和還原 FRS-Replicated SYSVOL 資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d841f64bab62114824847f91876ba8bbffbb0166db942c0f3cb9d010b72f106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124598"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>備份和還原 FRS-Replicated SYSVOL 資料夾

系統磁碟區 (SYSVOL) 資料夾提供儲存 [群組原則](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) 物件和腳本重要元素的標準位置。 網域中的每個網域控制站上都有 SYSVOL 資料夾的複本。 SYSVOL 資料夾是由 [分散式檔案系統複寫 (DFSR) ](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 或檔案複寫 [服務 (FRS) ](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10))複寫。 本主題說明如何判斷 DFSR 或 FSR 是否複寫 SYSVOL 資料夾，並說明如何備份和還原 FRS 複寫的 SYSVOL 資料夾。

FRS 可將 SYSVOL 內容複寫到網域內的其他網域控制站。 FRS 會監視 SYSVOL 資料夾，如果儲存在 SYSVOL 資料夾上的任何檔案發生變更，FRS 就會自動將變更的檔案複寫到網域中其他網域控制站上的 SYSVOL 資料夾。

> [!Note]  
> 藉由複寫 SYSVOL 資料夾的內容，只會複寫群組原則範本。 群組原則的容器會透過 Active Directory 複寫進行複寫。 若要讓群組原則能夠順利運作，您必須在網域控制站上使用群組原則範本和群組原則容器。

 

本主題涵蓋下列主題：

-   [判斷網域控制站的 SYSVOL 資料夾是否由 DFSR 或 FRS 複寫](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [備份 DFSR-Replicated SYSVOL 資料夾](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [備份 Windows Server 2008 或 Windows Server 2003 網域上的 FRS-Replicated SYSVOL 資料夾](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [範例 FRS 寫入器元資料檔案](#sample-frs-writer-metadata-document)
-   [設定用於還原 FRS-Replicated SYSVOL 資料夾的登錄機碼](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [執行 FRS-Replicated SYSVOL 資料夾的授權還原](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>判斷網域控制站的 SYSVOL 資料夾是否由 DFSR 或 FRS 複寫

下表摘要說明如何判斷 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 或 FRS 是否正在複寫網域控制站的 SYSVOL 資料夾。

| 如果網域控制站正在執行                                                                                                                  | SYSVOL 的複寫方式 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows伺服器 2008 + Windows server 2008 + [SYSVOL 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)的網域功能等級已完成 | DFSR                    |
| Windows伺服器 2008 + 網域功能等級低於 Windows server 2008                                                                              | FRS                     |
| Windows Server 2003                                                                                                                                  | FRS                     |



 

如果網域的[功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))Windows 伺服器2008，而網域已進行[sysvol 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)，則會使用[DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)來複寫 sysvol 資料夾。 如果網域中的第一個網域控制站直接升級為 Windows Server 2008[功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))，則會自動使用 DFSR 進行 SYSVOL 複寫。 在這種情況下，不需要將 SYSVOL 複寫從 FRS 遷移至 DFSR。 如果網域已升級為 Windows Server 2008[功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))，則會使用 frs 進行 SYSVOL 複寫，直到從 FRS 到 DFSR 的[遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)程式完成為止。

若要判斷是否正在執行 Windows Server 2008 的網域控制站上使用 DFSR 或 FRS，請檢查 **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **Parameters** \\ **SysVols** \\ **遷移 SysVols** \\ **LocalState** 登錄子機碼的值。 如果此登錄子機碼存在，且其值設為 3 (會消除) ，則會使用 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 。 如果子機碼不存在，或其具有不同的值，則會使用 FRS。

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>備份 DFSR-Replicated SYSVOL 資料夾

如果 [dfsr](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)複寫 SYSVOL 資料夾，則可以使用 dfsr VSS 寫入器進行備份。 如需有關 DFSR VSS 寫入器的詳細資訊，請參閱 [dfsr 複寫資料夾](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)。

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>備份 Windows Server 2008 或 Windows Server 2003 網域上的 FRS-Replicated SYSVOL 資料夾

在執行 Windows Server 2008 或 Windows server 2003 的網域控制站上，會有 VSS 基礎結構，因此 frs vss 寫入器可以用來備份 SYSVOL 資料夾和 frs 元件。

FRS VSS 寫入器的寫入器元資料檔案提供 SYSVOL 資料夾的位置和寫入器排除清單的相關資訊。 根據此資訊， (要求者) 的 VSS 備份應用程式可以使用定期以 VSS 為基礎的備份技術來備份 SYSVOL 資料夾。

寫入器元資料檔案包含寫入器的相關資訊、寫入器擁有的資料，以及如何還原該資料。 這是唯讀檔案，可以在進行備份之前，由備份應用程式取出。 [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11))工具可以用來查看 FRS VSS 寫入器的寫入器元資料檔案。 [DiskShadow 清單寫入](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11))器命令會提供有關系統上的寫入器的資訊。 這份清單包含有關網域控制站上使用 FRS 進行 SYSVOL 複寫的網域控制站上的 FRS 寫入器的資訊，或是使用 FRS 複寫 [DFS 連結目標](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))的檔案伺服器的相關資訊。

下列範例 frs 寫入器元資料檔案章節會針對在 D： Windows sysvol 上有 sysvol 資料夾的網域控制站，顯示範例 frs 寫入器元資料檔案 \\ \\ 。 [排除的檔案] 區段中顯示的路徑將與查詢 Netlogon 服務的 **SysVol** 登錄機碼時所取得的路徑相同：

**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NetLogon** \\ **參數** \\ **SysVol**

當網域控制站處於 [SYSVOL 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)的重新導向狀態時，就會發生此規則的唯一例外狀況。 在此狀態中，對應至 FRS 和 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 服務的寫入器會報告其各自的 SYSVOL 資料夾複本。 不過， [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 服務的 SYSVOL 資料夾複本 (通常是一個名為 sysvol DFSR 的資料夾， \_) 是網域控制站所共用的資料夾。此路徑是 **sysvol** 登錄機碼所參考的路徑。

FRS VSS 寫入器需要自訂的還原方法。 這表示在還原由 FRS 複寫的檔案時，必須執行特定的自訂步驟。 如需詳細資訊，請參閱執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原。

> [!Note]  
> Windows 網域控制站的系統狀態備份不包含 frs 資料庫，此資料庫會維護與 SYSVOL 資料夾內的檔案相關之 frs 服務的狀態資訊，以及其他內容集。 系統狀態備份會排除 FRS 資料庫、調試記錄、暫存區域檔案，以及 [預先存在之資料檔案夾](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) 中的檔案。 下列範例 FRS 寫入器規格包含 [排除的檔案] 區段中的排除清單。

 

## <a name="sample-frs-writer-metadata-document"></a>範例 FRS 寫入器元資料檔案

以下是網域控制站的範例 FRS 寫入器元資料檔案，其 SYSVOL 資料夾路徑為 D： \\ Windows \\ SYSVOL。

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>設定用於還原 FRS-Replicated SYSVOL 資料夾的登錄機碼

**BurFlags** 登錄機碼可用來在 DFS 或 SYSVOL 複本集的 FRS 成員上執行權威或非系統授權還原。 Global (整個電腦的) **BurFlags** 登錄機碼包含 REG \_ DWORD 值，而且位於登錄中的下列位置：

**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **備份/還原** \\ **在啟動時的進程**

最常見的 **BurFlags** 登錄機碼值為：

-   D2，也稱為非系統授權模式還原。
-   D4，也稱為授權模式還原。

有全域和複本集特定的 **BurFlags** 登錄機碼。 設定 global **BurFlags** 登錄機碼會重新初始化成員持有的所有複本集。 當伺服器只保留一個複本集時，或它所保存的複本集相對較少且大小較小時，應設定此全域金鑰。 例如，如果伺服器是網域控制站，而該控制器未裝載使用 SYSVOL 資料夾以外的 FRS 複寫的任何內容集，則可以設定全域 **BurFlags** 登錄機碼。

全域 **BurFlags** 登錄機碼可在登錄中的下列位置找到：

**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **備份/還原** \\ **在啟動時的進程**

相較于全域 **BurFlags** 索引鍵，複本集特定的 **BurFlags** 索引鍵允許重新初始化離散的個別複本集，讓狀況良好的複寫集保持不變。

您可以藉由決定該特定複本集的 GUID，找出複本集特定的 **BurFlags** 登錄機碼。

下列程式說明如何判斷哪個 GUID 對應至特定的複本集，並描述如何設定還原。

**判斷哪個 GUID 對應至特定的複本集和設定還原**

1.  停止 FRS 服務。
2.  若要判斷表示特定複本集的 GUID：
    1.  在登錄中找出下列機碼。

        **HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **複本集**

    2.  在 [ **複本集** ] 子機碼底下，有一個或多個子機碼由 GUID 識別。
    3.  每個 GUID 的 **複本集根目錄** 值都是檔案系統路徑，指出由此 GUID 表示的複本集。
    4.  反復查看此 Guid 清單，直到找到所需的複本集為止。 請注意對應的 GUID。

3.  在登錄中找出下列子機碼：

    **HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **累計複本集**

4.  在此子機碼底下，找出在步驟2中記下的相同 GUID。 在 GUID 子機碼底下，建立 **BurFlags** 索引鍵的專案。
5.  重新開機 FRS 服務。

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原

非系統授權還原是在個別網域控制站上重新初始化 SYSVOL 複寫最常見的方式。 Nonauthoritatively 還原的網域控制站必須具有來自其他工作網域控制站的輸入連線，而這些網域控制站會參與 Active Directory 和 FRS 複寫。 在包含許多網域控制站的大型部署環境中，您可以在下列情況下使用非系統授權模式還原來復原其餘的網域控制站：

-   至少必須有一個已知的良好複本成員 (具有健康情況良好的 SYSVOL 資料夾) 的網域控制站。
-   其他網域控制站必須以直接複寫夥伴順序重新初始化。

下列程式說明如何執行非系統授權還原。

**執行非系統授權還原**

1.  停止 FRS 服務。
2.  將備份的資料還原到 SYSVOL 資料夾。
3.  將下列登錄機碼的值設定為 DWORD 值 D2，以設定 **BurFlags** 登錄機碼。

    **HKEY \_\_** \\  \\  \\  \\  \\  \\  \\ **Startup** \\ **BurFlags** 的本機電腦 System CurrentControlSet Services NtFrs 參數備份/還原程式

4.  重新開機 FRS 服務。

當 FRS 服務重新開機時，會發生下列動作：

-   **BurFlags** 登錄機碼的值會重設為零。
-   重新初始化的 FRS 資料夾中的檔案會移至預先存在的資料夾。
-   事件13565會記錄在 FRS 事件記錄檔中，以指出已啟動非系統授權還原。
    > [!Note]  
    > FRS 事件碼記載于的 [說明及支援] 知識庫中的 [FRS 事件記錄檔錯誤碼] <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   FRS 資料庫會重建。
-   如果已針對 SYSVOL 複本集指定父系，則成員會從上游夥伴或從 **複本集父** 登錄機碼中指定的電腦，執行複本集的初始聯結。
-   重新初始化的電腦會在相關的複寫排程開始時，執行受影響複本集的完整複寫。
-   當程式完成時，系統會記錄事件13516，以指出 FRS 可正常運作。 如果未記錄此事件，則 FRS 設定有問題。

> [!Note]  
> 在重新初始化的成員上，將檔案放置在 [預先存在](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) 的資料夾中，是 FRS 中的一項防護措施，其設計目的是為了避免意外的資料遺失。 任何目的地為複本的檔案，只存在於本機預先存在的資料夾中，並在初始複寫之後複寫到適當的資料夾。 發生輸出複寫時，可以刪除預先存在的資料夾中的檔案，以釋放額外的磁片磁碟機空間。

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>執行 FRS-Replicated SYSVOL 資料夾的授權還原

在重大情況下，會使用授權還原作為最後的手段，例如目錄衝突所造成的內容集上的資料分歧。 例如，您可能需要進行授權還原，才能還原複寫已完全停止，且需要從頭重建的 FRS 複本集。

如果您必須執行 SYSVOL 資料夾的授權還原，請注意這是非常複雜的程式。 完整的指導方針會詳細說明在 [說明及支援] 知識庫中的「如何在網域中重建 SYSVOL 樹狀結構和其內容」中，需要針對該 SYSVOL 資料夾內容進行授權還原所需執行的作業 <https://go.microsoft.com/fwlink/p/?linkid=117780> 。

執行授權的 FRS 還原之前，必須符合下列需求：

1.  您必須在所有下游複寫協力電腦上停用 FRS 服務， (已重新初始化的 SYSVOL 資料夾的直接與可轉移) ，才能讓授權還原進行設定。
2.  事件13553和13516已記錄在 FRS 事件記錄檔中。 這些事件表示已在為授權還原設定的網域控制站上建立 SYSVOL 複本集的成員資格。
    > [!Note]  
    > FRS 事件碼記載于的 [說明及支援] 知識庫中的 [FRS 事件記錄檔錯誤碼] <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  針對授權還原設定的網域控制站，會設定為要複寫至其餘網域控制站的所有 SYSVOL 資料的授權。
4.  複本集中的所有其他夥伴都必須使用非系統授權還原來重新初始化。

 

 

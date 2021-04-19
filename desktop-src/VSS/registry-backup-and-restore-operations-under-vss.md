---
description: Windows 登錄服務支援 VSS 寫入器，稱為登錄寫入器，它可讓要求者使用儲存在陰影複製磁片區上的資料來備份系統登錄。
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: VSS 下的登錄備份和還原作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980802"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>VSS 下的登錄備份和還原作業

Windows 登錄服務支援 VSS 寫入器，稱為登錄寫入器，它可讓要求者使用儲存在陰影複製磁片區上的資料來備份系統登錄。 如需登錄寫入器的詳細資訊，請參閱 [內建的 VSS 寫入](in-box-vss-writers.md)器。

登錄寫入器會執行登錄的就地備份和還原。 此外，登錄寫入器只會報告系統 hive;它不會報告使用者 hive。

**Windows Server 2003：** 登錄寫入器使用中繼存放庫檔案 (也稱為算檔) 來儲存登錄資料。 此外，登錄寫入器會報告系統 hive 和使用者 hive。

登錄寫入器的寫入器識別碼是 AFBAB4A2-367D-4D15-A586-71DBB18F8485。

**WINDOWS XP：** 沒有任何登錄寫入器。 登錄資料是由可開機狀態寫入器所報告，其寫入器識別碼是 F2436E37-09F5-41AF-9B2A-4CA2435DBFD5。

> [!Note]  
> Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。 如需有關使用 Microsoft 提供的 Api 和程式來執行線上系統狀態還原的詳細資訊，請參閱 [MSDN 論壇中心](https://msdn.microsoft.com/community/default.aspx)提供的「社區資源」。

 

> [!Note]  
> 下列資訊僅適用于 Windows Server 2003 和 Windows XP。

 

## <a name="registry-backup-using-vss"></a>使用 VSS 的登錄備份

登錄寫入器會將 active registry 檔案匯出並儲存在 key **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist** 所定義的位置。

此登錄專案下的值名稱會識別要儲存的登錄區，而值的資料會提供檔案，其中包含 (hive 檔案) 的檔案。 Hive 檔案的指定格式如下： \\ 裝置 \\ *HarddiskVolumeX* \\ *路徑* \\ *檔案名*。

例如，在 [ **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**] 底下，您可能會看到登錄 **\\ \\ 電腦 \\ 軟體**  =  \\ 裝置 \\ HarddiskVolume1 \\ Windows \\ System32 \\ config \\ SOFTWARE。

登錄寫入器可確保在磁片陰影複製之前，將 hive 檔案儲存至磁片。

備份登錄 hive 時，要求者會 \\ \\ 以磁片區陰影複製的 [*裝置物件*](vssgloss-d.md)字串來取代裝置 *HarddiskVolumeX* 。

> [!Note]  
> 您可以 \\ 使用 QueryDosDevice 函數，將裝置 \\ *HarddiskVolumeX* 路徑轉換成相等的 Win32 [](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew)路徑。 如需詳細資訊，請參閱 [從檔案控制代碼取得檔案名](../memory/obtaining-a-file-name-from-a-file-handle.md) 或 [顯示磁片區路徑名稱](../fileio/displaying-volume-paths.md)。

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>使用非 VSS Win32 Api 的登錄還原

若為線上 (安全模式或完整作業系統) 還原，必須保留 **HKEY \_ 本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **會話管理員** \\ **PendingFileRenameOperations** 登錄機碼中的子機碼。

[**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa)和 [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda)函式會使用此登錄機碼，儲存在 \_ \_ \_ *DWFLAGS* 參數中重新開機值之前使用 MOVEFILE 延遲重新命名之檔案的相關資訊。

為了保留 **PendingFileRenameOperations** 登錄機碼的內容，您的備份應用程式應該呼叫 [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式，以連接要還原到 active registry 的登錄檔。 然後，您的備份應用程式可以使用各種登錄功能，將所需的金鑰和值複製到載入的 hive。 複製完成之後，應該呼叫 [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) 和 [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) 函數。

若為離線 (Windows 修復環境或 Windows PE) 還原，則不需要接受 **PendingFileRenameOperations** 登錄機碼。

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>在 Windows Server 2003 中使用非 VSS Win32 Api 的登錄還原

> [!Note]  
> 下列資訊僅適用于與嚴重損壞修復相關的還原作業 (也稱為在 Windows Server 2003 中執行的裸機修復) 。

 

還原登錄時，備份應用程式必須將目前登錄的一些子機碼移至要還原的登錄中。

若要這樣做，備份應用程式可以呼叫 **RegLoadKey** 來連接要還原到目前作用中登錄的登錄檔。 然後，它可以使用各種登錄函式，將所需的金鑰和值複製到載入的 hive。 複製完成之後，會呼叫 **RegFlushKey** 和 **RegUnloadKey** 。

有一個登錄機碼，指出還原應用程式 (要求者) **HKEY \_ 本機 \_ 電腦 \\ 系統** 下的登錄機碼，在還原時不應覆寫這些登錄機碼：

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

系統狀態還原程式的一部分牽涉到還原先前備份的登錄。

還原 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive 時，備份應用程式必須特別小心，因為安裝 Windows 作業系統暫存版本的程式將會在新安裝的系統 hive 中建立索引鍵，其值必須存留在還原作業的時間。

例如，當更換系統有不同于原始系統的網路介面卡時，還原上一張卡片的原始金鑰將會導致無法預期的結果。 這是因為隨插即用服務已偵測到並將適當的服務和驅動程式登錄專案放入登錄中。 您必須保留這些值，才能在系統還原之後正確開機。

本節說明在執行 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive 的還原時，備份應用程式如何探索要保留的金鑰和檔案。 在某些情況下，這會牽涉到以程式設計的方式，將新安裝的安裝 hive 中的金鑰複製到要還原的 hive。 在其他情況下，確保不會取代產品的登錄機碼，就像在產品的 INF 設定檔中指定這類金鑰一樣簡單。

金鑰 (和要保留的金鑰資料) 會在 **HKEY 的 \_ 本機 \_ 電腦 \\ 系統** hive 中列舉

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

這份檔中的索引鍵是一組 REG \_ 多重 \_ SZ 字串 (稱為索引 *鍵字串*) 。

備份應用程式 (要求者) 必須檢查 active registry 和新還原登錄中這些機碼的值，因為任何應用程式或服務都可以隨時新增值。

備份應用程式如何解讀金鑰字串是由其終端字元所決定：

1.  以反斜線 ( ' ' 結尾的索引鍵字串，) 會被視為子機碼 \\ 。 當遇到這類子字串時，備份應用程式必須保留所有資料和所有附屬索引鍵。

    例如，下列程式指定要在整個還原作業中保留所有從屬金鑰和資料：

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ dmio \\ boot info\\**

    至此，您必須從現有的登錄複製這個金鑰和所有附屬金鑰和資料 (也就是安裝 Windows) 所建立的登錄到新還原的登錄中。 這稱為「 *金鑰取代* 」作業。 這項操作會取代還原登錄中的對應機碼。

2.  終止字元是星號 ( ' ' 的索引鍵字串， \* ) 指定應合併所有子機碼。 例如，索引鍵字串：

    **HKEY \_LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ \\ Services \** _

    指定現有登錄中的服務機碼 (例如，安裝 Windows) 所建立的服務金鑰必須合併到還原的登錄中。 這稱為 _key merge * 作業，而且如果子機碼同時存在於現有的 hive 和還原的 hive 中，則會保留還原目錄中的金鑰，但有下列例外狀況：

    -   如果現有 hive 中的子機碼包含名為 "start" 的值，而且還原中的子機碼不是。
    -   如果現有和已還原之 hive 中的子機碼包含名為 "start" 的值，且其在現有 hive 中的數值較小。

    登錄中的 "start" 值會指定何時啟動服務或驅動程式，且可具有來自0-4 的數值。 值越低，啟動程式中的服務就會越快開始。

    如果現有和已還原的目錄中都有此金鑰，您必須檢查每個 hive 中的 start 鍵值。 如果現有 hive 中的值低於還原的目錄中的值，則必須保留較低的值。

    同樣地，此金鑰是用來判斷服務或驅動程式是在開機時、系統時間、手動、自動或停用時啟動。 較低的值代表較早的開始時間。 您必須將先前的開始時間套用至新的登錄，以確保服務或驅動程式會在下一次開機時正常啟動。

3.  其終止字元不是反斜線也不是星號的索引鍵字串，會被視為要保留的登錄值。

    例如，索引鍵字串：

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Session Manager \\ PendingFileRenameOperations**

    可以用程式設計的方式來保留金鑰的機制包含 Win32 登錄 API。 例如，以下列舉一個演算法：

    1.  將備份的系統 hive 檔案還原至檔案。 在此範例中，讓名稱為 system.string。
    2.  使用 **RegLoadKey** ，以暫存名稱將 System.string 載入 **HKEY \_ 本機 \_ 電腦** 。 例如，其中一個名稱可能是

        **HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**

    3.  從兩個登錄複本列舉 **KeysNotToRestore** 子機碼中的值，並建立清單的超集合。 從現有的中複製每個這類金鑰

        **HKEY \_ 本機 \_ 電腦 \\ 系統**

        的索引鍵

        **HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**

        根據上述語義的索引鍵。

    4.  完成時，請使用 **RegFlushKey**  &  **RegUnloadKey** 進入點來儲存

        **HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**

        金鑰傳回給 System.object。

    5.  最後，使用 **RegReplaceKey** 來指定要取代

        **HKEY \_ 本機 \_ 電腦 \\ 系統**

        hive 檔案、SYSTEM。

 

 

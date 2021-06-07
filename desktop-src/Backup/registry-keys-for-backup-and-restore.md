---
title: 用於備份和還原的登錄機碼和值
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 深入瞭解：備份和還原的登錄機碼和值
keywords:
- 備份備份，登錄機碼
- 登錄機碼備份
- CustomPerformanceSettings 備份
- DisableMonitoring 備份
- FilesNotToBackup 備份
- FilesNotToSnapshot 備份
- KeysNotToRestore 備份
- LastInstance 備份
- LastRestoreId 備份
- MaxShadowCopies 備份
- MinDiffAreaFileSize 備份
- OverallPerformanceSetting 備份
- SYSVOL 備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7058378561072bdc0f51abb455c098a22a9ad5e
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386787"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>用於備份和還原的登錄機碼和值

要求或執行備份和還原作業的應用程式，應該使用下列登錄機碼和值彼此通訊，或透過 [磁碟區陰影複製服務 (VSS) ](/windows/desktop/VSS/volume-shadow-copy-service-portal) 和 Windows 備份等功能進行通訊：

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting 和 CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

請參閱 [OverallPerformanceSetting 和 CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)。

## <a name="disablemonitoring"></a>DisableMonitoring

從 Windows 7 開始，在 Windows 用戶端平臺上，如果使用者尚未這麼做，系統會自動提示使用者設定 Windows 備份功能。 這些通知會在電腦啟動時顯示，在安裝作業系統之後的七天開始。 它們也會在使用者插入硬碟時出現;在此情況下，通知會立即顯示。

協力廠商備份應用程式的 Oem 和開發人員可以使用 **DisableMonitoring** 登錄值來關閉這些自動通知。

根據預設，這個值並不存在，因此必須在下列登錄機碼底下建立：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

**DisableMonitoring** 登錄值的資料類型為 REG \_ DWORD，如下所示：

-   如果值的資料設定為1，而且使用者尚未設定 Windows 備份功能，則會關閉自動通知。 如果 [行動中心] 已有自動通知，設定此登錄值會導致在下列早上的10:00 移除通知。
-   如果值不存在，如果未設定其資料，或其資料設定為零，則不會關閉自動通知。

**Windows Vista 和 WINDOWS XP：** 不支援這個登錄值。

## <a name="filesnottobackup"></a>FilesNotToBackup

**FilesNotToBackup** 登錄機碼會指定備份應用程式不應備份或還原的檔案和目錄名稱。 此機碼中的每個專案都是 \_ 使用 \_ 下列格式的 REG 多重 SZ 字串：

\[*磁片磁碟機* \] \[ \] 路徑 \\*檔案名* \[/s\]

-   *磁片* 磁碟機指定磁片磁碟機，而且是選擇性的。 例如，c： 若要指定所有磁片磁碟機，請使用反斜線 (\\) ; 不需要任何磁碟機號。
-   *路徑* 指定路徑，而且是選擇性的。 它不能包含萬用字元。
-   *FileName* 會指定檔案或目錄，而且是必要的。 它可以包含萬用字元。
-   /s 指定要包含指定路徑的所有子目錄。
-   像是% Systemroot% 的環境變數可以替代整個字串的所有或部分。

下表顯示一些一般專案。

| 專案名稱                             | 預設值                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | 暫存檔案                                                                           |
| 記憶體分頁檔案                       | \\Pagefile.sys                                                                            |
| MS 分散式交易協調器 | C： \\ Windows \\ system32 \\ msdtc msdtc \\ 。記錄檔 C： \\ Windows \\ system32 \\ MSDtc \\ 追蹤 \\ dtctrace .log |
| 離線檔案快取                    | % Systemroot% \\ CSC \\ \* /s                                                                  |
| 電源管理                       | \\hiberfil.sys                                                                            |
| 儲存單一版本                | \\SIS 一般存放區 \\ \* 。 \* /s                                                              |
| 暫存檔案                        | % TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> 執行磁片區層級備份的應用程式通常會在區塊層級複製整個磁片區，因此在備份時無法接受 **FilesNotToBackup** 登錄機碼。 相反地，他們會等待還原時間，以刪除不會備份的檔案。 在大部分的情況下，這是合理的策略。 不過，在單一實例儲存體檔案的情況下，不能在還原時刪除 SIS 一般存放區檔案。

 

針對區塊層級磁片區備份，Windows Server Backup 和 Windows Wbadmin 公用程式會在還原時刪除適當的檔案，以接受 **FilesNotToBackup** 登錄機碼。 系統還原和系統狀態備份不接受 **FilesNotToBackup** 登錄機碼。

**WINDOWS XP：** 系統還原接受 **FilesNotToBackup** 登錄機碼。

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS 支援 **FilesNotToSnapshot** 登錄機碼。 應用程式和服務可以使用此金鑰來指定要從新建立的陰影複製中刪除的檔案。 如需詳細資訊，請參閱 [從陰影複製中排除](/windows/desktop/VSS/excluding-files-from-shadow-copies)檔案。

**Windows Server 2003 和 WINDOWS XP：** 不支援此登錄機碼。

針對區塊層級磁片區備份，Windows Server Backup 會在還原時刪除適當的檔案，以接受 **FilesNotToSnapshot** 登錄機碼。

## <a name="idletimeout"></a>IdleTimeout

**IdleTimeout** 登錄值會指定 VSS 服務閒置時的等候時間（以秒為單位）。 如果達到此超時值且沒有可執行檔工作，則 VSS 服務將會關閉。

您可以在下列登錄機碼下找到這個登錄值：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **VSS** \\ **設定**

如果此登錄值不存在：

-   使用的實際超時值為180秒 (3 分鐘) 預設為3分鐘。
-   您可以建立具有名稱 **IdleTimeout** 和類型 DWORD 的值，並將它設定為所需的值。

如果此登錄值設定為0秒：

-   使用的實際超時值為180秒 (3 分鐘) 。

如果您設定此登錄值：

-   VSS 會使用您設定的超時值。
-   您可以指定介於1到 FFFFFFFF 秒之間的任何值。 不過，建議您選擇介於1到180秒之間的值。

**Windows Server 2003 和 WINDOWS XP：** 不支援此登錄機碼。

## <a name="keysnottorestore"></a>KeysNotToRestore

**KeysNotToRestore** 登錄機碼會指定備份應用程式不應還原的登錄子機碼和值的名稱。 如需詳細資訊，請參閱 [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10))。 不需要接受 **KeysNotToRestore** 登錄機碼。

**Windows Server 2003 和 WINDOWS XP：** 您必須接受 **KeysNotToRestore** 登錄機碼。

針對區塊層級磁片區備份，Windows Server Backup 會在還原時刪除適當的檔案，以接受 **KeysNotToRestore** 登錄機碼。

系統狀態備份會接受 **KeysNotToRestore** 登錄機碼。

## <a name="lastinstance"></a>LastInstance

**LastInstance** 登錄值表示已執行裸機還原作業，而磁片區已被覆寫但未格式化。 如需詳細資訊，請參閱 [使用 VSS 自動化系統復原進行](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery)嚴重損壞修復。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個登錄值。

## <a name="lastrestoreid"></a>LastRestoreId

當備份應用程式執行系統狀態還原時，它必須藉由設定 **LastRestoreId** 登錄值來指出它已完成。 在此情況下，「系統狀態還原」指的是選擇性還原作業系統二進位檔和驅動程式的任何還原。

如果整個開機和系統磁碟區是在磁片區層級還原，則不能設定這個值。

如果 **LastRestoreId** 登錄值不存在，則備份應用程式應該在下列登錄機碼底下建立它：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **BackupRestore** \\ **SystemStateRestore**

建立名稱為 **LastRestoreId** 且類型為 REG SZ 的值 \_ 。 此值應該是唯一的不透明值，例如 GUID。

每當執行新的系統狀態還原時，備份應用程式應變更 **LastRestoreId** 值的資料。

其他需要監視系統狀態還原的應用程式應該儲存此登錄值的資料。 這項資料可以與 **LastRestoreId** 登錄值的目前資料進行比較，以判斷是否已執行新的系統狀態還原。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 之前，不支援這個登錄值。

## <a name="maxshadowcopies"></a>MaxShadowCopies

**MaxShadowCopies** 登錄值會指定可儲存在電腦每個磁片區上的 [*用戶端可存取陰影複製*](/windows/desktop/VSS/vssgloss-c)的最大數目。 用戶端可存取的陰影複製是一種陰影複製，使用 [**\_ vss \_ 快照集 \_ 內容**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context)列舉的 **vss \_ CTX \_ 用戶端 \_ 可存取** 值建立。 共用資料夾陰影複製會使用用戶端可存取的陰影複製。 如需陰影複製的詳細資訊，請參閱 [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) 檔集。

如果 **MaxShadowCopies** 登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **VSS** \\ **設定**

建立名稱為 **MaxShadowCopies** 和類型為 DWORD 的值。 此值的預設資料為64。 最小值為1。 最大值為512。

> [!Note]  
> 若是其他類型的陰影複製，則沒有對應至 **MaxShadowCopies** 的登錄值。 每個磁片區的陰影複製數目上限為512。

 

**注意**  Windows Server 2003 或更新版本支援 **MaxShadowCopies** 設定。

**Windows Server 2003：** 在叢集伺服器上， **MaxShadowCopies** 登錄值的資料可能需要設定為較低的數位。 For more information, see "When you use the Volume Shadow Copy Service on Windows Server 2003-based computers that run many I/O operations, disk volumes take longer to go online" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058).

**WINDOWS XP：** 不支援這個登錄值。

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) 會配置陰影複製存放區域 (或「差異區域」 ) 來儲存陰影複製的資料。 陰影複製存放區域的大小下限是可使用 **MinDiffAreaFileSize** 登錄值指定的每部電腦設定。

如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的大小下限為 32 mb，適用于小於 500 mb 的磁片區，以及大於 500 mb 的磁片區的 320 mb。

**Windows server 2008、Windows server 2003 SP1 和 Windows Vista：** 如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的最小大小為 300 MB。 如果已設定 **MinDiffAreaFileSize** 登錄值，其資料必須介於 300 mb 到 3000 mb (3 GB) ，而且必須是 300 MB 的倍數。

**Windows Server 2003：** 如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的大小下限為 100 MB。

**WINDOWS XP：** 不支援這個登錄值。

如果 **MinDiffAreaFileSize** 登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它：

**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**

建立名稱為 **MinDiffAreaFileSize** 的值，並輸入 REG \_ DWORD。 此索引鍵的資料會以 mb 為單位來指定。 320等於 320 MB，而3200等於 3.2 GB。 您應該指定一個數位，其為32的倍數。 如果您指定的值不是32的倍數，則會使用32的下一個倍數。

如果 **MinDiffAreaFileSize** 登錄值指定的大小下限大於陰影複製存放區的大小上限，則陰影複製可能無法正確運作。 若要指定陰影複製存放區的大小上限，請使用 [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add Shadowstorage 或 vssadmin resize shadowstorage 命令。 若要查看目前的大小上限，請使用 [Vssadmin list shadowstorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 命令。 如果您未設定大小上限，則可以使用的空間量沒有限制。

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting 和 CustomPerformanceSettings

**OverallPerformanceSetting** 和 **CustomPerformanceSettings** 登錄值是用來指定 Windows Server Backup 的效能設定。 只有在 Windows server 作業系統上才支援這些登錄值。

**Windows Server 2003：** 不支援這些登錄值。

如果這些登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它們：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **windows** \\ **CurrentVersion** \\ **windows 區塊層級備份**

若要指定所有磁片區的效能設定，請建立名稱為 **OverallPerformanceSetting** 的值，並輸入 REG \_ DWORD。 值的資料應該設定為下列其中一個值。

| 值 | 意義                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 一般備份效能 (使用完整備份) 。 這項設定會對應到 [ [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))] 中所述的一般備份效能設定。            |
| 2     | 使用增量備份) 來加快備份效能 (。 這項設定會對應到 [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))中所述的更快備份效能設定。     |
| 3     | 藉由指定每個磁片區) 的效能設定，可 (自訂備份效能。 這項設定會對應到 [ [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))] 中所述的自訂設定。 |



 

如果您將 **OverallPerformanceSetting** 設定為3，您也必須個別指定每個磁片區的效能設定。 若要這樣做，請建立名稱為 **CustomPerformanceSettings** 且類型為 REG \_ 多重 \_ SZ 的值。 此值的資料應設定如下：

-   REG 多重 SZ 字串中的每個字串都 \_ \_ 包含磁片區的設定。
-   每個字串都包含一個磁片區 GUID，後面接著一個逗號，後面接著一個 DWORD 值。
-   每個 DWORD 值都可以是 1 (完整備份) 或 2 (增量備份) 。

例如，假設電腦有兩個磁片區，如下所示：

-   這兩個磁片區為 C： \\ 和 D： \\ 。
-   磁片區 C：的 GUID \\ 是 07c473ca4-2df8-11de-9d80-806e6f6e6963，而磁片區 D：的 guid \\ 是 0ac22ea6c-712f-11de-adb0-00215a67606e。
-   您想要指定磁片區 C 的一般備份 perfornance： \\ 磁片區 D：的備份效能更快 \\ 。

若要這樣做，您可以將 **OverallPerformanceSetting** 設定為3，並將 **CustomPerformanceSettings** 設定為 "07c473ca4-2df8-11de-9d80-806e6f6e6963，1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e，2"。

如果您將 **OverallPerformanceSetting** 設定為1或2，則會忽略 **CustomPerformanceSettings** 值中的資料。

## <a name="sysvol"></a>SYSVOL

**SYSVOL** 登錄值是一種方式，可通知分散式檔案系統複寫 (DFSR) 服務，表示已起始系統狀態還原作業。 任何執行 SYSVOL 系統狀態還原的備份應用程式，都應該使用此值來指出還原作業是否為授權或非授權。 DFSR 服務會讀取這個值。 如果未設定此值，則預設會執行 nonauthoritatively 的 SYSVOL 還原。

如果 **SYSVOL** 登錄值不存在，則備份應用程式應該在下列登錄機碼底下建立它：

**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **還原**

建立名稱為 **SYSVOL** 的值，並輸入 REG \_ SZ。 根據系統管理員的要求，值的資料應該設定為「授權」或「非授權」。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 不支援這個登錄值。

 

 

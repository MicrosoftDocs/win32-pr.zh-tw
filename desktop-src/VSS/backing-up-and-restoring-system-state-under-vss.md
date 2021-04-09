---
description: 請注意，本主題僅適用于 Windows Server 2003 R2 和 Windows Server 2003 Service Pack 1 (SP1) 。
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: 在 Windows Server 2003 R2 和 Windows Server 2003 SP1 中備份和還原系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945233"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>在 Windows Server 2003 R2 和 Windows Server 2003 SP1 中備份和還原系統狀態

> [!Note]  
> 本主題僅適用于 Windows Server 2003 R2 和 Windows Server 2003 Service Pack 1 (SP1) 。 如需其他作業系統版本的詳細資訊，請參閱 [備份和還原系統狀態](locating-additional-system-files.md)。

 

> [!Note]  
> Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。 如需有關使用 Microsoft 提供的 Api 和程式來執行線上系統狀態還原的詳細資訊，請參閱 [MSDN 論壇中心](https://msdn.microsoft.com/community/default.aspx)提供的「社區資源」。

 

執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。 這些元素應一律由備份和還原作業視為一個單位來處理。

在 Windows Server 2003 R2 和 Windows Server 2003 （含 SP1）中，沒有任何 Windows API 設計來將這些物件視為一，因此建議要求者擁有自己的系統狀態物件，以便能夠以一致的方式處理這些元件。

由於 VSS 是在 Windows 版本上執行，而 [*系統檔案保護*](vssgloss-s.md) (WFP) 保護系統狀態檔案免于損毀，因此需要特殊步驟來備份和還原系統狀態。

系統狀態包含下列各項：

-   所有受 WFP 保護的檔案、開機檔案，包括 ntldr、ntdetect 和效能計數器設定
-   在網域控制站的系統上，Active Directory (ADSI)  () 
-   系統磁碟區資料夾 (SYSVOL) ，檔案複寫服務會在網域控制站的系統上 (FRS)  () 
-   提供憑證授權單位單位之系統上的憑證伺服器 () 
-   叢集資料庫 (在屬於 Windows 叢集節點的系統上) 
-   註冊服務
-   COM + 類別註冊資料庫

系統狀態可以依任何順序進行備份。

不過，還原系統狀態應該會先取代開機檔案，然後將登錄的系統區段 (hive) 作為程式中的最後一個步驟，而且可能會依下列順序發生：

1.  還原開機檔案。
2.  COM + 類別註冊資料庫
3.  如有需要，請 (還原 SYSVOL、憑證伺服器和叢集資料庫) 。
4.  視需要) 還原 Active Directory (。
5.  還原登錄。

某些系統服務（例如憑證授權單位單位）有傳統的 VSS 寫入器，並遵循 VSS 備份和還原演算法。 其他專案（例如登錄）則需要自訂備份或還原作業;如需詳細資訊，請參閱 [自訂備份和還原](custom-backups-and-restores.md)。

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>開機和系統檔案的 VSS 備份和還原

開機和系統檔案只能以單一實體的形式來備份和還原。

要求者可以安全地使用這些檔案的陰影複製版本，並確定系統磁碟區和開機裝置是 [*陰影複製*](vssgloss-s.md)的。

系統和開機檔案包括：

-   核心開機檔案： <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (（如果有的話）)   
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   所有受 [*系統檔案保護*](vssgloss-s.md) 保護並由 [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) 列舉的檔案 (查看 -   效能計數器設定檔) 的 WFP 受保護檔案的 VSS 還原作業： <dl> % SystemRoot% \\ System32 效能 \\ ？00？。Dat  
    % SystemRoot% \\ System32 效能 \\ ？00？。Bak </dl>
-   如果存在，則會在備份和還原作業中包含網際網路資訊伺服器 (IIS) 的中繼檔，因為它包含 Microsoft Exchange 和其他網路應用程式所使用的狀態。 這個檔案位於下列位置： <dl> % SystemRoot% \\ System32 \\ InetSrv \\ 元資料庫. bin </dl>
-   如果已備份 IIS 中繼檔，則可讓應用程式讀取特定加密專案的金鑰，應還原為系統狀態的一部分。 您可以在下列檔中找到這些檔案： <dl> % SystemRoot% \\ System32 \\ Microsoft \\ 保護\\\*  
    % AllUsersProfile% \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys\\\* </dl>
-備份開機和系統檔案時，您可能必須執行下列動作，以判斷 DOS 開機裝置： 1. 在 [ **HKEY \_ 本機 \_ 電腦** \\ **系統** \\ **安裝** \\ **SystemPartition**] 下尋找系統磁碟分割。
    2.  將系統根目錄環境變數 (% SystemRoot% ) 傳遞給掛接管理員，以取得 NT 裝置名稱。

## <a name="vss-restore-operations-of-wfp-protected-files"></a>WFP 受保護檔案的 VSS 還原作業

WFP 服務是設計來防止系統檔案意外或分次取代。 因此，必須採取特殊步驟來還原 WFP 資料。

這表示當您定義寫入器元資料檔案時，WFP 寫入器應該 **\_ \_ \_ 在 \_ 重新開機** 還原方法時指定 VSS RME 還原。 如果要求者判斷 WFP 寫入器無法指定此還原方法，它會指出寫入器錯誤。

要求者應該在重新開機時，使用 Win32 函數 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa)搭配 **MOVEFILE \_ 延遲 \_ 直到 \_ 重新開機** 參數取代系統檔案，以 **\_ \_ \_ 在 \_ 重新開機時執行 VSS RME 還原** 的還原方法。 還原的檔案不會複製到實際的系統檔案目錄中，直到系統重新開機為止。 只有當下列 **REG \_ WORD** 登錄專案的值設定為1時，才會覆寫受保護的系統檔案：

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **AllowProtectedRenames** = 1

必須先設定此值，才能透過 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) 取代受保護的檔案，並在重新開機之後刪除。

您也應該使用開機磁碟區備份和還原來備份或還原系統 dllcache 目錄，並藉由檢查 **REG \_ EXPAND \_ SZ** 登錄專案來找到它：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ EXPAND \_ SZ</dd> </dl>

系統 dllcache 目錄的內容會從命令提示字元使用系統檔案檢查程式 (SFC) 來重建：

-   **/SCANONCE** 選項會在下一次系統開機時掃描所有受保護的檔案。
-   **/SCANNOW** 選項會立即掃描所有受保護的檔案。

系統將掃描所有受保護的檔案，並在目錄和 dllcache 位置中取代任何不正確版本。

有四個檔案是無法使用 WFP 檔案還原之 WFP 的一部分：

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

這些檔案有助於還原 WFP 檔案，因此有迴圈的相依性。 目前沒有任何方法可以還原這些檔案，除非重新安裝 Windows。

 

 

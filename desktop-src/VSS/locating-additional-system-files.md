---
description: 執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。 備份和還原作業應該一律將這些元素視為一個單位。
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: 備份與還原系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692448"
---
# <a name="backing-up-and-restoring-system-state"></a>備份與還原系統狀態

> [!Note]  
> 本主題適用于 Windows Vista、Windows Server 2008 及更新版本。 如需 Windows Server 2003 的相關資訊，請參閱 [在 Windows server 2003 R2 和 Windows server 2003 SP1 中備份和還原系統狀態](backing-up-and-restoring-system-state-under-vss.md)

 

執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。 備份和還原作業應該一律將這些元素視為一個單位。

> [!Note]  
> Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。

 

備份和復原系統狀態時，建議的策略是除了系統狀態寫入器所列舉的檔案之外，還會備份和復原系統和開機磁碟區。 系統狀態寫入器是將 [ [**vss \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) ] 屬性設為 [vss \_ BOOTABLESYSTEMSTATE] 或 [ \_ vss SYSTEMSERVICE] 的寫入器 \_ \_ 。

> [!IMPORTANT]
> 如果 VSS 寫入器以其 [**vss \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) 識別為系統狀態寫入器，則必須將它包含在系統狀態備份中，即使它是可選取的。

 

除了列舉的作業系統和系統狀態寫入器所列舉的驅動程式二進位檔案之外，還必須在系統狀態下備份某些其他檔案。

VSS 系統狀態寫入器所報告的所有元件都是系統狀態的一部分，除了未設定 VSS \_ CF \_ 非 \_ 系統 \_ 狀態旗標的元件之外。

備份程式也應該設定 **LastRestoreId** 登錄機碼。 如需詳細資訊，請參閱 [備份和還原的登錄機碼和值](../backup/registry-keys-for-backup-and-restore.md)。

> [!Note]  
> 在 Windows Vista、Windows Server 2008 和更新版本中，某些系統檔案的名稱和位置已變更，如下所示。

 

## <a name="system-state"></a>系統狀態

針對 Windows Server 2012 和更新版本，除了各種 VSS 系統狀態寫入器所報告的檔案以外，只需要明確包含下列授權檔案，且必須明確排除下列 DRM 檔案。

## <a name="windows-media-digital-rights-management-files"></a>Windows Media 數位 Rights Management 檔案

在 Windows Server 2008 和更新版本中，下列檔案（包括下列路徑下的所有子目錄）會從系統狀態中排除，而且不得備份：

-   % ProgramData% \\ Microsoft \\ Windows \\ DRM\\

這會取代 [使用檔案系統和安全性功能](working-with-file-system-and-security-features.md)的 Windows Media 數位 Rights Management 一節中的資訊。

## <a name="performance-counter-configuration-files"></a>效能計數器設定檔案

效能計數器設定檔位於% SystemRoot% \\ System32 \\ 目錄中，並具有下列名稱：

<dl> 效能？00？。Dat  
Perfc0??。Dat  
Perfd0??。Dat  
Perfh0??。Dat  
Perfi0??。Dat  
Prfc0???。Dat  
Prfd0???。Dat  
Prfh0???。Dat  
Prfi0???。Dat  
</dl>

這些檔案只會在應用程式安裝期間進行修改，而且應該在系統狀態備份和還原期間進行備份和還原。

## <a name="iis-configuration-files"></a>IIS 設定檔案

> [!Note]  
> 在 Windows Vista Service Pack 1 (SP1) 和更新版本中，您不應該備份這些檔案。 相反地，請使用內建的 IIS 設定寫入器。 如需此寫入器的詳細資訊，請參閱 [內建的 VSS 寫入](in-box-vss-writers.md)器。

 

相關的 IIS 設定檔和其位置如下所示：

-   .NET FX machine.config 檔案位於 framework 版本目錄。
-   ASP.NET 根目錄 web.config 檔案位於 framework 版本目錄。
    > [!Note]  
    > .NET FX 和 ASP.NET 的設定檔都位於 framework 版本目錄中。 如果電腦上安裝了多個版本的架構，此目錄將會包含每個已安裝版本的一個設定檔案。

     

-   IIS applicationHost.config 中央設定檔案位於% windir% \\ system32 \\ inetsrv \\ config 目錄中。 為了讓伺服器瞭解這個設定檔，有架構檔案可決定其文法和結構。 這些檔案位於% windir% \\ system32 \\ inetsrv \\ config \\ schema 目錄中。

Framework 版本目錄路徑會儲存在下列登錄機碼中：

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 。.Netframework \\ InstallRoot**

此外，您必須備份下列密碼編譯金鑰：<dl> % ProgramData% \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys\\\*  
% SystemRoot% \\ System32 \\ Microsoft \\ 保護\\\*  
</dl>

## <a name="framework-files"></a>架構檔案

您必須備份所有的 .NET framework 版本。 這些檔案位於下列其中一個或兩個目錄：

<dl> % windir% \\ Microsoft.Net \\ Framework  
% windir% \\ Microsoft.Net \\ \microsoft.net\framework64\v4.0.30319\  
</dl>

此外，也必須備份元件檔。 這些檔案位於下列目錄：<dl> % windir% \\ 元件  
</dl>

## <a name="task-scheduler-task-files"></a>工作排程器任務檔

必須備份工作排程器的工作檔案。 這些檔案位於下列其中一個或兩個位置：

<dl> % windir% \\ system32 工作 \\ 和任何子目錄 (遞迴)   
% windir% 工作 \\ (沒有任何子目錄)   
</dl>

 

 

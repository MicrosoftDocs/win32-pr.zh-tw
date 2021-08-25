---
description: 下列清單描述 Windows Server 2012 和 Windows Server 2012 R2 的新功能和更新功能區域。 如需新 Windows 8 和 Windows 8.1 技術的詳細資訊，請參閱 Windows 8 和 Windows 8.1 技術。
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 新功能： Windows Server 2012 R2 & Windows Server 2012
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df654e7c448ef4e4f6f4f1599204883cad11bf5e56ccd13c47c76d204f7587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867499"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>新功能： Windows Server 2012 R2 & Windows Server 2012

下列清單描述 Windows Server 2012 和 Windows Server 2012 R2 的新功能和更新功能區域。 如需新 Windows 8 和 Windows 8.1 技術的詳細資訊，請參閱[Windows 8 和 Windows 8.1 技術](/previous-versions/windows/desktop/whatsnew/windows-8-technologies)。

## <a name="whats-new-for-windows-server-2012-r2"></a>Windows Server 2012 R2 的新功能

-   [重複資料刪除](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    重復資料刪除會在磁片區上的資料中尋找並移除重複的資料，同時確保資料保持正確且完整。 如此即可節省磁碟區上的檔案資料儲存空間。 若為 Windows Server 2012 R2，則會啟用許多參數和錯誤碼，並新增 [**MSFT \_ DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata)類別。

-   [軟體清查記錄](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **新功能！** 軟體清查記錄會收集 Windows 伺服器上所安裝之軟體的授權資料，並提供資料的遠端存取，讓資料中心可以輕鬆地匯總資料。

-   [iSCSI 目標伺服器](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    iSCSI 目標伺服器 API 提供 Windows Management Instrumentation (的 WMI) 提供者來管理 Microsoft iSCSI 目標伺服器，例如建立虛擬磁片，以及將它們呈現給用戶端。 針對 Windows Server 2012 R2 新增了許多新功能。

-   [Mobile 裝置管理註冊](../mdmreg/mobile-device-management-registration-portal.md)

    **新功能！** 產業趨勢的開發是讓員工將其個人行動運算裝置連接到公司網路和資源 (內部部署或透過雲端) 來執行工作場所工作。 此趨勢需要支援輕鬆設定網路和資源，讓員工可以在公司註冊個人裝置，以進行工作相關的用途。 支援輕鬆設定的應用程式和技術也必須讓 IT 專業人員管理與將未受管理的裝置連線到公司網路相關聯的風險。 行動裝置管理 (MDM) 註冊會將裝置註冊到管理服務中。

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell 是以工作為基礎的命令列 shell 和指令碼語言，專為系統管理所設計。 Windows Server 2012 R2 的新功能 Windows PowerShell v4 支援 Desired State Configuration，這是 Windows PowerShell 中的新管理平臺，可讓您部署和管理軟體服務的設定資料，以及管理這些服務執行所在的環境。

## <a name="whats-new-for-windows-server-2012"></a>Windows Server 2012 的新功能

-   [Windows聚 類](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows群集可讓您同時管理網路負載平衡叢集和容錯移轉叢集。 此版本加入了許多新功能，包括新的群組管理功能、通用屬性，以及與 WMI 的整合。

-   [使用者存取記錄](/previous-versions/windows/desktop/ual/user-access-logging)

    **新功能！** 使用者存取記錄 (UAL) 是 Windows 伺服器角色用來報告其各自耗用量計量的通用架構。 這個 UAL 架構是較大的授權管理解決方案的基礎和重要元件。

-   [Windows 遠端管理](../winrm/portal.md)

    Windows 遠端管理 (WinRM) 是 Microsoft 在 WS-Management 通訊協定方面的實作，它是以簡易物件存取通訊協定 (SOAP) 為基礎、防火牆適用的通訊協定，允許不同廠商的硬體和作業系統互相操作。 Windows Server 2012 包含許多連接 API，其著重在與執行中的實例和 shell 互動。

-   [Windows管理基礎結構](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **新功能！** Windows 管理基礎結構 (MI) 功能代表最新版本的 Windows Management Instrumentation (WMI) 技術，這些技術是以來自 DMTF (分散式管理工作小組) 的 CIM 標準為基礎。 MI 與舊版 WMI 完全相容，並提供一系列的功能和優點，讓設計和開發提供者和用戶端比以往更容易。

-   [重複資料刪除](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **新功能！** 重復資料刪除會在磁片區上的資料中尋找並移除重複的資料，同時確保資料保持正確且完整。 如此即可節省磁碟區上的檔案資料儲存空間。

-   [iSCSI 目標伺服器](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **新功能！** iSCSI 目標伺服器 API 提供 Windows Management Instrumentation (的 WMI) 提供者來管理 Microsoft iSCSI 目標伺服器，例如建立虛擬磁片，以及將它們呈現給用戶端。

-   [適用于 WMI 的 NFS 提供者](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **新功能！** NFS WMI 提供者提供管理 NFS 伺服器和用戶端設定、檔案共用、群組和用戶端群組的方法。

-   [離線檔案](../devnotes/offline-files.md)

    離線檔案 API 可讓應用程式以程式設計方式控制和監視離線檔案的行為。 Windows Server 2012 新增 [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex)、 [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart)和 [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem)函數。

-   [SMB 管理](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **新功能！** SMB 管理 API 提供 WMI 類別和方法來管理共用和共用存取。

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows伺服器會針對在 Windows server 2008 作業系統或更新版本上執行的電腦，提供最基本的伺服器安裝選項。 Windows Server 2012 提供 Server Core 作為設定和安裝選項。

-   [Windows Server Backup](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    Windows Server Backup 功能會自動備份及還原應用程式資料。 Windows Server 2012 包含雲端備份提供者 API。

-   [Windows桌面共用](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows桌面共用是一種多方的螢幕共用技術。 Windows Server 2012 使用 Windows 的重複 API 來實行這項技術。

-   [遠端桌面服務](../termserv/terminal-services-portal.md)

    Windows桌面共用可讓使用者從遠端存取作業系統的實例。 Windows Server 2012 包含許多新功能，包括子會話、RemoteFX 媒體重新導向，以及遠端桌面訊息代理程式用戶端。

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell 是以工作為基礎的命令列 shell 和指令碼語言，專為系統管理所設計。 Windows Server 2012 的新功能 Windows PowerShell v3 支援 Windows PowerShell 工作流程，它會利用 Windows Workflow Foundation 的優點，讓長時間執行的工作自動化。

-   [管理 OData](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **新功能！** 也稱為 Windows PowerShell Web 服務、管理 OData、Windows PowerShell v3 的新功能，可讓您建立 ASP.NET Web 服務端點，以公開管理資料（透過 Windows PowerShell 命令 acessed）作為 OData Web 服務實體。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Server 2012TechNet 上的 R2](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012TechNet Library 上的 R2 和 Windows Server 2012](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012Microsoft.Com 上的 R2](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 

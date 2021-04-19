---
description: 用來安裝應用程式或更新或在 Windows 上執行之服務的安裝程式引擎。 設定及修復已安裝的應用程式。 撰寫自訂的 msi 套件，以建立應用程式的 exe 安裝程式或更新或升級。
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997154"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> 本檔適用于想要使用 Windows Installer 為應用程式建立安裝程式套件的軟體發展人員。 如果您要尋找 Windows Installer 4.5 及更早版本的可轉散發套件，請參閱 [這篇文章](windows-installer-redistributables.md)。 請注意，Windows Installer 5.0 沒有可轉散發套件。 此版本隨附于 Windows 7、Windows Server 2008 R2 和更新版本的用戶端和伺服器版本中的作業系統， (包括 Windows 10) 。

Microsoft Windows Installer 是 Windows 所提供的安裝和設定服務。 安裝程式服務可讓客戶提供更佳的公司部署，並提供元件管理的標準格式。 安裝程式也會根據作業系統來啟用應用程式和功能的公告。 如需詳細資訊，請參閱 [廣告的平臺支援](platform-support-of-advertisement.md)。

本檔說明 Windows Installer 5.0 及更早版本。 在較舊的版本中，並非所有 Windows Installer 版本提供的功能都可供使用。 本檔不會描述 Windows Installer 2.0 之前的版本。 使用 Windows Installer 3.0 和更新版本，仍然可以安裝為 Windows Installer 2.0 建立的安裝套件和修補程式。

Windows Installer 3.0 和更新版本，可以使用單一交易來安裝多個修補程式，以整合安裝進度、復原和重新開機。 安裝程式可以依照指定的順序套用修補程式，而不考慮將修補程式提供給系統的順序。 使用 Windows Installer 3.0 進行修補時，只會更新受修補程式影響的檔案，而且比舊版安裝程式更快。 您可以依任何順序卸載隨 Windows Installer 3.0 或更新版本安裝的修補程式，讓產品的狀態保持不變，就像從未安裝過修補程式一樣。 具有系統管理員許可權的帳戶可以使用 Windows Installer 3.0 和更新版本的 API 來查詢和清查產品、功能、元件和修補程式資訊。 安裝程式可以用來讀取、編輯和取代網路、URL 和媒體來源的來源清單。 系統管理員可以在使用者和安裝內容之間進行列舉，以及管理來自外部進程的來源清單。

Windows Installer 4.5 和更新版本可以使用 [*交易處理*](t-gly.md)來安裝多個安裝套件。 如果無法順利安裝交易中的所有封裝，或如果使用者取消安裝，Windows Installer 可以復原變更，並將電腦還原為其原始狀態。 安裝程式可確保已安裝屬於多封裝交易的所有套件，或未安裝任何套件。

從 Windows Installer 5.0 開始，可以撰寫套件來保護新的帳戶、Windows [服務](../services/services.md)、檔案、資料夾和登錄機碼。 封裝可以指定拒絕許可權的安全描述項、指定父資源的許可權繼承，或指定新帳戶的許可權。 如需詳細資訊，請參閱 [保護資源](securing-resources-.md)。 Windows Installer 5.0 服務可以列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。 如需詳細資訊，請參閱 [列舉元件](enumerating-components-.md)。 藉由 [使用服務](using-services-configuration.md)設定，Windows Installer 5.0 套件可以自訂電腦上的服務。 安裝程式開發人員可以使用 Windows Installer 5.0 和 [單一套件撰寫](single-package-authoring.md) ，以開發可在每部電腦或每個使用者 [安裝內容](installation-context.md)中安裝應用程式的單一安裝套件。

## <a name="where-applicable"></a>適用時

Windows Installer 可有效地安裝和設定 Windows 上執行的產品和應用程式。 安裝程式會提供新功能，以在不安裝的情況下通告功能、隨選安裝產品，以及新增使用者自訂。

在 Windows Server 2012 或 Windows 8 上執行的 Windows Installer 5.0 支援在 Windows RT 上安裝已核准的應用程式。 未由 Microsoft 簽署的 Windows Installer 套件、修補程式或轉換，無法安裝在 Windows RT 上。 [ [**範本摘要**](template-summary.md) ] 屬性會指出與安裝資料庫相容的平臺，而在此情況下，應該包含 Windows RT 的值。

Windows Installer 適用于桌面樣式應用程式的開發。

## <a name="developer-audience"></a>開發人員對象

本檔適用于想要讓應用程式使用 Windows Installer 的軟體發展人員。 它提供有關安裝套件和安裝程式服務的一般背景資訊。 它包含應用程式開發介面的完整描述，以及安裝程式資料庫的元素。 本檔也包含想要使用資料表編輯器或封裝建立工具來建立或維護安裝之開發人員的補充資訊。

## <a name="run-time-requirements"></a>執行階段需求求

、Windows 7、Windows Server 2008 R2 及更新版本中包含 Windows Installer 5.0。 Windows Installer 5.0 沒有可轉散發套件。

早于 Windows Installer 5.0 的版本，已與 Windows Server 2008、Windows Vista、Windows Server 2003、Windows XP 及 Windows 2000 一起發行。 [Windows Installer](windows-installer-redistributables.md) 可轉散發套件適用于 Windows Installer 4.5 和某些較舊版本。

* Windows Installer 4.5 需要 Windows Server 2008、Windows Vista、Windows XP （含 Service Pack 2） (SP2) 和更新版本，以及 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本。

* Windows Installer 4.0 需要 Windows Vista 或 Windows Server 2008。 在其他作業系統上安裝 Windows Installer 4.0 沒有可轉散發套件。 Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 提供 Windows Installer 4.0 的更新版本，不會新增任何新功能。

* Windows Installer 3.1 需要 Windows Server 2003、Windows XP 或 Windows 2000 Service Pack 3 (SP3) 。

* Windows Installer 3.0 需要 Windows Server 2003、Windows XP 或 Windows 2000 SP3。 Windows Installer 3.0 隨附于 Windows XP Service Pack 2 (SP2) 。 它是以 Windows 2000 Server Service Pack 3 (SP3) 和 Windows 2000 Server Service Pack 4 (SP4) 、Windows XP RTM 和 Windows XP （含 Service Pack 1） (SP1) 和 Windows Server 2003 RTM 的可轉散發套件。

* Windows Installer 2.0 包含在 Windows Server 2003 和 Windows XP 中。

* Windows Installer 2.0 是以封裝的形式提供，可用於安裝或升級至 Windows 2000 上的 Windows Installer 2.0。 此套件不應用來在 Windows Server 2003 和 Windows XP 上安裝或升級 Windows Installer 2.0。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [藍圖](roadmap-to-windows-installer-documentation.md)<br/>                        | Windows Installer 檔的指南。<br/>       |
| [概觀](about-windows-installer.md)<br/>                                          | 有關安裝程式的一般資訊。<br/>          |
| [Windows Installer 的新功能](what-s-new-in-windows-installer.md)<br/>           | 列出 Windows Installer 的新增和變更。<br/> |
| [參考](installer-function-reference.md)<br/>                                    | Windows Installer 功能的檔。<br/>     |
| [Windows Installer 腳本範例](windows-installer-scripting-examples.md)<br/> | 使用腳本 Windows Installer 範例。<br/>          |



 

 

 

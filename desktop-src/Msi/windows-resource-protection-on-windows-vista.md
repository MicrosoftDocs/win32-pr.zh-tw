---
description: Windows Installer 在 Windows Server 2008 和更新版本以及 Windows Vista 及更新版本中安裝基本的系統檔案、資料夾和登錄資訊時，會遵守 Windows 資源保護 (WRP) 。
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: 使用 Windows Installer 和 Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944474"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>使用 Windows Installer 和 Windows 資源保護

Windows Installer 在 Windows Server 2008 和更新版本以及 Windows Vista 及更新版本中安裝基本的系統檔案、資料夾和登錄資訊時，會遵守 Windows 資源保護 (WRP) 。

Windows Server 2008 和 windows Vista 中的 WRP 取代了 windows Server 2003、Windows XP 及 Windows 2000 中的 Windows 檔案保護 (WFP) 。 Windows Installer 開發人員應該注意下列變更：安裝程式如何在 Windows Server 2008 和更新版本以及 Windows Vista 和更新版本中處理受保護的資源：

-   在 Windows Server 2008 （含）以後版本或 Windows Vista 和更新版本上執行時，Windows Installer 會略過 WRP 所保護之任何檔案的安裝，安裝程式會在記錄檔中輸入警告，並繼續安裝的其餘部分，而不會發生錯誤。 在 Windows Server 2003、Windows XP 及 Windows 2000 中，當 Windows Installer 遇到受 WFP 保護的檔案時，安裝程式會要求 WFP 安裝檔案。
-   WRP 在 Windows Server 2008 和更新版本或 Windows Vista 和更新版本上，除了檔案之外，還可以保護登錄機碼。 如果 Windows Installer 遇到受 WRP 保護的登錄機碼，安裝程式會略過該登錄機碼的安裝，安裝程式會在記錄檔中輸入警告，並繼續進行安裝的其餘部分，而不會發生錯誤。
-   請注意，如果 Windows Installer 元件包含受 WRP 保護的檔案或登錄機碼，則必須使用此資源做為元件的 KeyPath。 在此情況下，Windows Installer 不會安裝、更新或移除元件。 您不應該在安裝套件中包含任何受保護的資源。 相反地，您應該針對[Windows 資源保護](../wfp/windows-resource-protection-portal.md)使用[支援的資源取代機制](../wfp/supported-file-replacement-mechanisms.md)。

如需 WRP 的詳細資訊，請參閱[Microsoft Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))上提供的[Windows 資源保護](../wfp/windows-resource-protection-portal.md)和資訊。

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>適用于 Windows Server 2003 和 Windows XP/2000 的 WFP

Windows Installer 在 Windows Server 2003、Windows XP 和 Windows 2000 上安裝基本的系統檔案時，會遵守 Windows 檔案保護 (WFP) 。 如果應用程式的自動安裝修改了受保護的系統檔案，則 WFP 會將檔案還原至已驗證的檔案版本。

Windows Installer 永遠不會嘗試安裝或取代受保護的檔案。 當 [InstallFiles](installfiles-action.md) 動作或 InstallFiles 之前排程的任何其他動作嘗試安裝在 windows Server 2003、windows XP 或 windows 2000 上受到保護的檔案時，安裝程式會使用安裝或取代受保護檔案的要求來呼叫 WFP。 執行 InstallFiles 動作之後，安裝程式會立即從 WFP 要求檔案安裝。 WFP 會以受保護檔案的快取版本，安裝或取代使用者系統上的檔案。 請注意，這並不保證從快取安裝的檔版本是應用程式所需的版本。 在 WFP 安裝檔案之後，安裝程式會判斷此版本是否符合套件中的版本。 如果封裝中的檔案版本大於安裝的版本，安裝程式會通知使用者其無法更新系統，且應用程式可能需要作業系統的更新。

如果在 [InstallFiles](installfiles-action.md) 之後排序的任何動作嘗試安裝或取代系統上尚未安裝的受保護檔案，安裝程式就無法呼叫 WFP 來安裝檔案。 在此情況下，安裝程式會通知使用者無法更新系統，且應用程式可能需要作業系統的更新。

移除檔案時，安裝程式也會檢查 WFP，而且永遠不會嘗試移除受保護的系統檔案。

## <a name="component-key-files-protected-by-wfp"></a>由 WFP 保護的元件金鑰檔案

請注意，如果 Windows Installer 元件包含 WFP 檔案，則必須將此檔案指定為元件的金鑰路徑。

當安裝程式嘗試在 Windows Server 2003、Windows XP 或 Windows 2000 上安裝元件的金鑰檔時，它會先呼叫 WFP 來判斷金鑰檔是否受到保護。 當元件的金鑰檔受到 WFP 的保護，且已安裝該金鑰檔時，只有當封裝中的金鑰檔版本大於安裝的版本時，安裝程式才會更新該元件。 如果安裝套件指定元件已安裝，且目前未安裝元件的金鑰檔，則不論金鑰檔是否受到保護，安裝程式都會安裝元件。 一旦安裝了任何具有 WFP 保護之金鑰檔的元件之後，就會永久安裝它，而安裝程式永遠不會移除或取代元件。

## <a name="installation-of-assemblies-by-wfp"></a>以 WFP 安裝元件

適用于元件的 WFP 與系統檔案的 WFP 不同。

WFP 會偵測取代受保護系統檔案的嘗試，以保護 Windows Server 2003、Windows XP 和 Windows 2000 系統檔案。 當 WFP 收到受保護目錄中檔案的目錄變更通知之後，就會觸發這項保護。 當 WFP 收到此通知時，它會判斷已變更的檔案。 如果檔案受到保護，則 WFP 會查閱靜態類別目錄檔案中的檔案簽章，以判斷新的檔案是否為正確的版本。 如果檔案版本不正確，系統會從快取或散發媒體將檔案取代為正確的版本。

相反地，元件的 WFP 是動態的。 當檔案新增至共用並存元件快取時，會將 WFP 擴充至檔案。 如果元件損毀，則 WFP 會要求安裝程式取代檔案。 根據來源套件是否可存取，Windows Installer 可能或可能無法取代檔案。 如果無法存取來源封裝，WFP 將會出現一個對話方塊，指出它無法還原檔案。

請注意，安裝在% windir% winsxs 中的非受控共用並存元件 \\ 會受到 WFP 保護。 未受管理的私用元件（安裝在應用程式目錄中）不受 WFP 保護。 在應用程式目錄中安裝的 Managed 通用群組件或% windir% \\ 元件 \\ gac 未受 WFP 保護。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 資源保護](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 

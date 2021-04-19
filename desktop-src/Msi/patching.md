---
description: 這些章節說明修補 Windows Installer 安裝。
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: 修補
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3117723bda1699eeae341fc75db201421f6ae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988472"
---
# <a name="patching"></a>修補

使用 Microsoft Windows Installer 安裝的應用程式可以透過將更新的安裝套件重新安裝 () .msi 檔案來進行升級，或將 Windows Installer 修補程式 (.msp 檔) 套用至應用程式。

Windows Installer 修補程式 ( .msp 檔) 是包含應用程式更新的獨立套件，並描述應用程式可接收修補程式的版本。 修補程式至少包含兩個資料庫轉換，而且可以包含儲存在修補程式套件的封包檔串流中的修補檔案。 如需 Windows Installer 修補程式套件元件的詳細資訊，請參閱 [修補套件](patch-packages.md)。

藉由提供 Windows Installer 修補程式來服務應用程式，而不是更新產品的完整安裝套件，可能有其優點。 修補程式可包含整個檔案，或只包含更新部分檔案所需的檔案位。 這可讓使用者下載的升級修補程式，比整個產品的安裝套件小得多。 使用修補程式的更新可以透過升級來保留應用程式的使用者自訂。

* * Windows Installer 4.5 和更新版本： * *

從 Windows Installer 4.5 開始，開發人員可以使用 [元件資料表](component-table.md)中的 **msidbComponentAttributesUninstallOnSupersedence** 值來標記修補程式中的元件。 如果已安裝後續修補程式，並在其 [MsiPatchSequence 資料表](msipatchsequence-table.md)中標示 **msidbPatchSequenceSupersedeEarlier** 值來取代第一個修補程式，Windows Installer 4.5 和更新版本可以取消註冊並卸載標示為 **msidbComponentAttributesUninstallOnSupersedence** 的元件，以避免在電腦上留下未使用的元件。 如果元件未以這個位標示，則取代修補程式的安裝可能會在電腦上留下未使用的元件。 設定 **MSIUNINSTALLSUPERSEDEDCOMPONENTS** 屬性的效果與設定所有元件的這個位相同。

* * Windows Installer 3.0 和更新版本： * *

使用 Windows Installer 3.0 的開發人員，以及撰寫具有 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的 patch 封裝，可以建立可執行下列作業的 patch 封裝：

-   使用安裝程式快取的產品基準，更輕鬆地以較小的 delta 修補程式來服務應用程式。 如需使用產品基準的詳細資訊，請參閱 [減少修補程式大小](reducing-patch-size.md)。
-   略過修補程式未修改的特定資料表相關聯的動作。 這可大幅縮短安裝修補程式所需的時間。 如需可略過哪些資料表的詳細資訊，請參閱 [修補程式優化](patch-optimization.md)。
-   建立並安裝可單獨卸載的修補程式，而不需要卸載並重新安裝整個應用程式和其他修補程式。 如需卸載修補程式的詳細資訊，請參閱 [移除修補程式](removing-patches.md)。
-   以固定順序套用修補程式，而不考慮將修補程式提供給系統的順序。 如需 Windows Installer 如何決定用來套用修補程式之順序的詳細資訊，請參閱將 [修補程式排序](sequencing-patches.md)。
-   將修補程式套用到已安裝在個別使用者管理內容中的應用程式。 如需詳細資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。

* * Windows Installer 2.0： * *

不支援 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。 從 Windows Installer 3.0 開始，修補套件可以包含描述修補程式順序的資訊，相對於其他更新和其他描述性資訊。

建立修補程式套件的建議方法是使用修補程式建立工具，例如 [Msimsp.exe](msimsp-exe.md) 和 [Patchwiz.dll](patchwiz-dll.md)。 開發人員可以產生 patch 建立檔案，如「 [建立修補程式套件](creating-a-patch-package.md)」一節所述。 小型更新修補 [範例](a-small-update-patching-example.md)一節會說明如何建立小型更新修補程式。

Microsoft Windows Installer 接受統一資源定位器 (URL) 作為修補程式的有效來源。 如需如何安裝位於 Web 服務器上之修補程式的詳細資訊，請參閱 [從網際網路下載並安裝修補程式](downloading-and-installing-a-patch-from-the-internet.md)。

當您第一次安裝應用程式時，可以將單一 Windows Installer 修補程式 ( .msp 檔) 套用至安裝套件。 如需詳細資訊，請參閱 [修補初始安裝](patching-initial-installations.md)。

當修補程式的應用程式可能需要存取原始安裝來源時，不可能消除所有的情況。 不過，若要將修補程式需要存取原始來源的可能性降至最低，請遵循下一節所列的點： [防止 Patch 要求存取原始安裝來源](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)。

為了將修補程式未因後續自訂轉換而中斷的可能性降至最低，通常會先安裝修補程式，然後再進行自訂。 先安裝自訂轉換，然後再安裝修補程式，可能會中斷自訂作業。 如需修補自訂應用程式的詳細資訊，請參閱 [修補自訂應用程式](patching-customized-applications.md)。

 

 




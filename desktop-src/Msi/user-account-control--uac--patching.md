---
description: " (UAC) 修補的使用者帳戶控制可讓 Windows Installer 安裝的作者找出可由非系統管理員使用者未來套用的數位簽章修補程式。"
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: " (UAC) 修補的使用者帳戶控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852716"
---
# <a name="user-account-control-uac-patching"></a> (UAC) 修補的使用者帳戶控制

 (UAC) 修補的 [*使用者帳戶控制*](u-gly.md)可讓 Windows Installer 安裝的作者找出可由非系統管理員使用者未來套用的數位簽章修補程式。

如果數位簽章與憑證不符，Windows Vista 會在安裝修補程式之前，先顯示一個要求系統管理員授權的 UAC 對話方塊。 在 Windows Vista 之前的系統上，安裝程式將不會套用與憑證不符的已簽署修補程式。

如果非系統管理員嘗試將修補程式套用至應用程式，但未符合下列條件，則 Windows Vista 會在安裝修補程式之前，通知使用者需要系統管理員授權。 如果符合下列條件，則非系統管理員可以繼續安裝修補程式，而不需要取得額外的系統管理員授權。

-   應用程式是使用 Windows Installer 3.0 或更新版本安裝在 Windows Vista 或 Windows XP 上。

    **Windows Server 2008：** 不支援。

-   如果應用程式是安裝在 Windows XP 上，則也必須從卸載式媒體（例如 CD-ROM 或 DVD 磁片）安裝應用程式。 如果應用程式是安裝在 Windows Vista 上，則不適用此限制。
-   未從 [系統管理安裝](administrative-installation.md) 來源映射安裝應用程式。
-   應用程式原本是依電腦安裝。 如需有關如何讓非系統管理員在修補程式被系統管理員信任之後，將修補程式套用至個別使用者管理的應用程式的相關資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。
-   [MsiPatchCertificate 資料表](msipatchcertificate-table.md)會出現在 ( .msi 檔案) 的 windows Installer 封裝中，並包含啟用 UAC 所需的資訊。 資料表和資訊可能已包含在原始安裝封裝中，或由 Windows Installer patch 檔案新增至封裝， ( .msp 檔案) 。
-   這些修補程式會以 [MsiPatchCertificate 資料表](msipatchcertificate-table.md)中所列的憑證進行數位簽署。 如需數位簽章憑證的詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。
-   修補程式套件上的數位簽章可以針對 [MsiPatchCertificate 資料表](msipatchcertificate-table.md)中的憑證進行驗證。 如需有關使用數位簽章、數位憑證和 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)的詳細資訊，請參閱 Microsoft WINDOWS 軟體開發套件 (SDK) 的 [安全性](https://msdn.microsoft.com/library/cc527452.aspx) 一節。
-   用來驗證修補程式套件上數位簽章的簽署者憑證是有效的，而且尚未撤銷。
    > [!Note]  
    > 雖然您無法使用過期的憑證來簽署修補程式，但如果憑證已過期，則在修補程式上評估數位簽章不會失敗。 評估使用目前的 [MsiPatchCertificate 資料表](msipatchcertificate-table.md)，其中包含原始封裝中的 MsiPatchCertificate 資料表，以及在目前的封裝之前排序的修補程式對資料表所做的任何變更。 修補程式可以將新的憑證新增至 MsiPatchCertificate 資料表，以評估在目前修補之後排序的修補程式。 已撤銷的憑證一律會被拒絕。

     

-   未藉由設定 [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) 屬性或 [DisableLUAPatching](disableluapatching.md) 原則來停用最低許可權修補。

非系統管理員也可以移除使用 UAC 修補套用的修補程式。

系統管理員可以將修補程式套用至每部電腦安裝的產品，不論應用程式的 UAC 設定為何。

您可以使用 [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) 函式來查詢 INSTALLPROPERTY \_ 授權的 \_ LUA \_ 應用程式屬性，或使用 [**ProductInfo**](installer-productinfo.md) 方法來查詢 "AuthorizedLUAApp" 屬性，以判斷應用程式是否已啟用最低許可權修補。 如果任一個屬性的值為1，則會為應用程式啟用最低許可權的使用者帳戶修補。

系統管理員可以將 [DisableLUAPatching](disableluapatching.md) 原則設定為1，以停用電腦上的最低許可權修補。 您可以在應用程式的初始安裝期間將 [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) 屬性設定為1，以防止該應用程式的最低許可權修補。

從 Windows Installer 版本3.0 開始，可以使用這項功能。  (UAC) 修補的使用者帳戶控制，在 Windows XP 中被稱為最低許可權的使用者帳戶 (LUA) 修補。 在 Windows 2000 和 Windows Server 2003 上無法使用 LUA 修補。

如需有關應用程式相容性的詳細資訊，以及如何開發與使用者帳戶控制相容 (UAC) 的應用程式，請參閱 [Microsoft Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))上提供的 uac 資訊。

 

 

---
description: 使用終端機伺服器時，下列可能會影響 Windows Installer 安裝。 當使用者同時使用終端機伺服器時，安裝程式開發人員應該一律測試其 Windows Installer 套件是否如預期般安裝。
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: 使用 Windows Installer 與終端機伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468916"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>使用 Windows Installer 與終端機伺服器

使用終端機伺服器時，下列可能會影響 Windows Installer 安裝。 當使用者同時使用終端機伺服器時，安裝程式開發人員應該一律測試其 Windows Installer 套件是否如預期般安裝。

-   在 Windows Server 2008 和 Windows Vista 之前的作業系統上，必須設定 [EnableAdminTSRemote](enableadmintsremote.md) 系統原則，讓系統管理員能夠在用戶端會話中執行安裝。 從 Windows Server 2008 和 Windows Vista 開始，EnableAdminTSRemote 原則不再具有任何作用。 無論其設定為何，系統管理員和非系統管理員都可以在用戶端會話或主控台會話中執行安裝。 系統管理員和非系統管理員隨時都可以在主控台會話中執行 Windows Installer 安裝。
-   如果[DisableUserInstalls](disableuserinstalls.md)[系統原則](system-policy.md)設定為1，Windows Installer 會防止在個別使用者[安裝內容](installation-context.md)中進行安裝。 在此情況下，安裝程式會忽略所有註冊為每位使用者的應用程式，而且只會搜尋以每一電腦註冊的應用程式。
-   當系統管理員在 Windows 2000 中裝載的終端機伺服器的用戶端會話中執行安裝時，安裝必須使用 UNC 路徑，而不是對應的磁碟機號。

開發人員在開發可與終端機伺服器搭配使用的 Windows Installer 元件時，應遵循下列指導方針。

-   在登錄的 **HKCU** Software 部分中，寫入所有 **hkcu** 登錄資訊 \\  。
-   不建議將設定資訊儲存在 INI 檔案中。
-   第一次執行應用程式時，而不是在安裝時，將每個使用者的資訊寫入登錄中。 如果您必須在安裝時將每位使用者的資訊寫入登錄，請將每位使用者和每一電腦的資訊分成不同的 Windows Installer 元件。 撰寫套件，讓安裝程式在安裝應用程式時，不會嘗試驗證及修復包含每個使用者資訊的元件。
-   僅適用于每部電腦安裝的套件，應該 \* 在 [環境資料表](environment-table.md)的 [名稱] 資料行中包含，將環境變數寫入電腦的環境中。 如果封裝可用於每個使用者安裝或每部電腦安裝，請使用兩個元件。 在 [元件資料表](condition-table.md) 中包含每個使用者的元件，並在 [環境] 資料表中輸入使用者設定。 在元件資料表中包含每一電腦的元件，並在 [環境] 資料表中輸入電腦設定。 根據元件資料表的條件欄位中的 [**ALLUSERS**](allusers.md) 屬性，使用條件陳述式來控制要安裝的元件。
-   從終端機伺服器執行每部電腦安裝時，安裝程式會將每個使用者的環境變數寫入 **HKCU** \\ **。預設** \\ **環境**。 因為終端機伺服器不會複寫登錄的這個區段，所以安裝不會設定每個使用者的環境變數。
-   因為伺服器可能設定為防止使用者修復應用程式，所以您的應用程式應該正常地處理遺失登錄機碼的情況。

當使用 DLL、EXE 或腳本 [自訂動作](custom-actions.md) 的 Windows Installer 封裝安裝在終端機伺服器上的每部電腦安裝內容中時，將會發生下列情況。 在此情況下，安裝程式會設定 [**TerminalServer**](terminalserver.md) 屬性。

-   延遲的自訂動作會在本機系統的內容中執行，除非該動作具有 **msidbCustomActionTypeTSAware** 屬性。 即使自訂動作在非終端機伺服器的系統上模擬使用者，也是如此。 請注意，如果自訂動作的 **msidbCustomActionTypeTSAware** 屬性變更了使用者的登錄，安裝程式就不會自動確保電腦上每位使用者的登錄中也會進行這些變更。
-   在延遲的自訂動作中，從 **HKCU** 登錄 hive 讀取的任何登錄作業都會看到系統的預設登錄區，而不是目前使用者的登錄 hive。
-   在延遲的自訂動作中，寫入 **HKCU** 軟體的任何登錄作業 \\ 都是由安裝程式偵測到，並且會在使用者下次登入時複製到電腦的每個使用者。
-   安裝程式不會偵測到在延遲自訂動作中寫入 **HKCU** 但不在 **HKCU** \\ **Software** 登錄機碼下的任何登錄作業。

如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 [終端機服務](../termserv/terminal-services-portal.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**TerminalServer 屬性**](terminalserver.md)
</dt> <dt>

[**RemoteAdminTS 屬性**](remoteadmints.md)
</dt> <dt>

[終端機服務](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 

---
title: 安裝為服務應用程式
description: 安裝為服務應用程式
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024140"
---
# <a name="installing-as-a-service-application"></a>安裝為服務應用程式

除了以本機伺服器可執行檔的形式執行 (EXE) ，COM 物件也可以自行封裝，以便在本機或遠端用戶端啟動時，以服務應用程式的形式執行。 服務支援許多有用和使用者 interfaceâ的「整合式系統管理功能，包括本機和遠端啟動、停止、暫停和重新開機，以及建立伺服器以在特定 [使用者帳戶](/windows/desktop/Services/service-user-accounts) 和 [視窗工作站](/windows/desktop/winstation/window-stations)上執行的能力。

以服務方式撰寫的物件會透過在其[AppID](appid-key.md)金鑰底下建立[LocalService](localservice.md)值並執行標準服務安裝，來安裝供 COM 使用。

當遠端用戶端啟動時，類別也可以設定為在特定使用者帳戶下執行，而不需要撰寫為服務應用程式。 若要這樣做，類別會安裝當 SCM 啟動其本機伺服器進程時要使用的使用者名稱和密碼。

以這種方式設定類別時，除非 COM 會代表實際的啟用要求啟動進程，否則使用此 CLSID 呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 將會失敗。 換句話說，設定為以特定使用者身分執行的類別，可能無法在任何其他身分識別下註冊。

使用者名稱是取自類別的 APPID 金鑰底下的 [RunAs](runas.md) 命名值。 如果使用者名稱為「互動式使用者」，則類別程式碼會在目前登入之使用者的安全性內容中執行，並連接到互動式視窗工作站。

否則，系統會從登錄的隱藏部分取得密碼，而只提供給電腦的系統管理員和系統的系統管理員。 接著會使用使用者名稱和密碼來建立執行類別程式碼的登入會話。 以這種方式啟動時，類別程式碼會以自己的桌面和視窗來執行，且不會與互動式使用者或其他使用者帳戶中執行的其他類別共用視窗控制碼、剪貼簿或其他使用者介面元素。

使用 **LocalService** 或 **RunAs** 註冊的伺服器，可以在執行中的物件資料表中註冊物件，以允許任何用戶端連接到該物件。 若要這樣做，伺服器對 [**IRunningObjectTable：： Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) 的呼叫必須設定 ROTFLAGS \_ ALLOWANYCLIENT 旗標。 在參考可執行檔之 AppID 的登錄的 AppID 區段中，伺服器設定此位必須有其可執行檔名稱。 "Activate as activator" 伺服器 (未註冊為 **LocalService** 或 **RunAs**) 可能不會使用此旗標注冊物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在安裝時註冊類別](registering-a-class-at-installation.md)
</dt> <dt>

[註冊正在執行的 EXE 伺服器](registering-a-running-exe-server.md)
</dt> <dt>

[在 ROT 中註冊物件](registering-objects-in-the-rot.md)
</dt> <dt>

[自我註冊](self-registration.md)
</dt> </dl>

 

 
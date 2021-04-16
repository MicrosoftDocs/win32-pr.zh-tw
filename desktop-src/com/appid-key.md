---
title: AppID 金鑰
description: 將一或多個 DCOM 物件的設定選項，群組到登錄中的一個集中位置。 相同可執行檔所裝載的 DCOM 物件會分組為一個 AppID，以簡化一般安全性和設定設定的管理。
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- AppID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383002"
---
# <a name="appid-key"></a>AppID 金鑰

將一或多個 DCOM 物件的設定選項，群組到登錄中的一個集中位置。 相同可執行檔所裝載的 DCOM 物件會分組為一個 AppID，以簡化一般安全性和設定設定的管理。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ AppID** \\ *{* AppID \_ GUID *}*



| 登錄值                                           | Description                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | 描述可存取此類別實例之主體 (ACL) 的存取控制清單。 只有未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式才會使用此 ACL。 |
| [**ActivateAtStorage**](activateatstorage.md)           | 將用戶端設定為將相同電腦上的物件具現化，其為它們正在使用或從中初始化的持續性狀態。                                                                    |
| [**AppID**](appid.md)                                   | 識別對應至已命名可執行檔的 AppID GUID。                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | 設定在非預設桌面中，用戶端將如何啟動或系結設定為以「互動式使用者」執行的 COM 伺服器。                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | 針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的應用程式，或針對呼叫 **CoInitializeSecurity** 並指定 AppID 的應用程式，設定驗證等級。               |
| [**DllSurrogate**](dllsurrogate.md)                     | 讓 DLL 伺服器在代理進程中執行。 如果指定了空字串，則會使用系統提供的代理;否則，此值會指定要使用的代理路徑。                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | 讓 DLL 伺服器能夠在自訂的代理程式中執行，並與 [**DllSurrogate**](dllsurrogate.md) 登錄值搭配使用。                                                                          |
| [**端點**](endpoints.md)                           | 設定 COM 應用程式使用指定的 TCP 通訊埠編號進行 DCOM 通訊。                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | 描述可為此類別啟動新伺服器之主體 (ACL) 的存取控制清單。                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | 判斷 COM 是否會載入執行的 COM 伺服器的使用者設定檔，做為啟動使用者應用程式識別。                                                                                           |
| [**LocalService**](localservice.md)                     | 將物件安裝為服務應用程式。                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | 設定此 COM 伺服器的慣用架構（32位或64位）。                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | 將用戶端設定為在呼叫未指定 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構的啟用函式時，要求在特定電腦上執行物件。              |
| [**ROTFlags**](rotflags.md)                             | 控制在執行中的物件資料表中，COM 伺服器的註冊 (ROT) 。                                                                                                                                    |
| [**Runas.exe**](runas.md)                                   | 當遠端用戶端未撰寫為服務應用程式時，將類別設定為在特定使用者帳戶下執行。                                                                       |
| [**ServiceParameters**](serviceparameters.md)           | 指定要傳遞至物件的命令列參數，這些參數會透過 [**LocalService**](localservice.md) 登錄值傳遞給已安裝供 COM 使用的物件。                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | 將軟體限制原則設定 (SRP) 信任層級的應用程式。                                                                                                                                        |



 

## <a name="remarks"></a>備註

Appid 會使用兩種不同的機制對應到可執行檔和類別：

-   使用128位的全域唯一識別碼 (GUID) 來識別 **AppID** 金鑰。 類別會在名為 "AppID" 的 [**CLSID**](clsid-key-hklm.md) 機碼下，指出其對應的 AppID。 此對應會在啟用期間使用。
-   使用表示可執行檔名稱的指名值 (例如 "MYOLDAPP.EXE" ) 。 此命名值的型別為 **REG \_ SZ** ，並且包含與可執行檔相關聯之 AppID 的字串表示。 此對應是用來取得預設存取權限和驗證層級。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

若是 COM 伺服器，在註冊程式期間或執行 dcomcnfg.exe 時，通常會產生對應並寫入登錄中。 不過，想要使用 **AppID** 金鑰設定安全性的 COM 用戶端必須建立適當的登錄機碼，並藉由呼叫登錄函 [式或使用](/windows/desktop/SysInfo/registry-functions) Regedit.exe 來指定所需的對應。 然後，您可以為用戶端設定 [**AccessPermission**](accesspermission.md) 或 [**AuthenticationLevel**](authenticationlevel.md) 之類的值。 例如，假設您的用戶端進程的可執行檔名稱是 "YourClient.exe"，而您想要將驗證層級設定為「無」。 您可以使用 Guidgen.exe 或 Uuidgen.exe 來建立可執行檔之 AppID 的 GUID。 然後您會在登錄中設定值，如下列範例所示，其中00000001代表「無」的驗證層級：

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 
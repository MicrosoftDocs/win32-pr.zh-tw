---
title: 透過登錄設定 Process-Wide 安全性
description: 如果您想要設定整個進程的安全性，有一個解決方案是在登錄中設定您想要的安全性層級。
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8ad3a549a78a10b15e965ba2e2a47b9e5e84f1e8790ccfbf90af622051714e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730908"
---
# <a name="setting-process-wide-security-through-the-registry"></a>透過登錄設定 Process-Wide 安全性

如果您想要設定整個進程的安全性，有一個解決方案是在登錄中設定您想要的安全性層級。 如果您的應用程式無法呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，或如果您不想使用程式設計安全性，這可能是個不錯的選項。 如果您決定使用登錄設定整個進程的安全性，請注意，如果您在程式中呼叫 **CoInitializeSecurity** ，就會使用 **CoInitializeSecurity** 中的值並忽略登錄值。

有兩種方式可以為您的應用程式設定登錄中的安全性：

-   您可以使用 Dcomcnfg.exe，這會提供簡單的使用者介面來修改安全性值。 您可以使用 Dcomcnfg.exe 設定所有的 COM 伺服器。 如需詳細資訊，請參閱 [使用 DCOMCNFG 設定 Process-Wide 安全性](setting-processwide-security-using-dcomcnfg.md)。 不過，用戶端應用程式通常不會出現在 Dcomcnfg.exe 中，除非用戶端建立 GUID 並將它輸入到登錄中。
-   您可以在應用程式的 [AppID](appid-key.md) 金鑰下設定安全性值。 本主題的其餘部分將說明如何使用 **AppID** 金鑰在登錄中設定安全性。

AppID 是 GUID，代表一或多個類別的伺服器進程。 每個類別都只會與一個 AppID 相關聯，而 Appid 只能指派給 Exe。 除非 Dll 是在代理程式中執行，否則 Dll 不會取得 Appid，而是具有 AppID 的代理程式。 如果將多個 Dll 載入至代理，每個代理程式只會有一個 AppID。

針對某些 COM 伺服器，註冊程式碼會產生 AppID，並將專案放在登錄中，以將 AppID 對應到可執行檔的名稱。 但某些 COM 伺服器並不提供此功能。 但是，如果在執行 dcomcnfg.exe 時，伺服器的註冊程式碼新增 HKCR \\ CLSID {ServerCLSID} \\ [LocalServer32](localserver32.md)的專案，則會自動新增 CLSID 的 AppID。

若為非伺服器的 COM 用戶端，則不會建立此對應，因為用戶端從未註冊。 因此，若要使用 **AppID** 金鑰設定安全性，用戶端必須使用登錄 [功能](/windows/desktop/SysInfo/registry-functions) 或使用 regedit 以程式設計的方式建立必要的登錄專案。

如果您決定以 **appid** 金鑰在登錄中設定整個進程的安全性，請注意，您可以在不具有系統管理員許可權的情況下設定的 **appid** 金鑰底下有兩個名為的值：

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

**AuthenticationLevel** 和 **AccessPermission** 值是獨立設定的，而且具有個別的預設值。 如果 **AuthenticationLevel** 值不存在，就會使用 [LegacyAuthenticationLevel](legacyauthenticationlevel.md) 值作為預設值。 同樣地，如果 **AccessPermission** 值不存在，就會使用 [DefaultAccessPermission](defaultaccesspermission.md) 值作為預設值。 不過， **AuthenticationLevel** 和 **AccessPermission** 值會以下列方式相互關聯：

-   如果 **AuthenticationLevel** 為 none，則會忽略該應用程式的 **AccessPermission** 和 **DefaultAccessPermission** 值。
-   如果 **AuthenticationLevel** 不存在，而且 **LegacyAuthenticationLevel** 為 none，則該應用程式的 **AccessPermission** 和 **DefaultAccessPermission** 值會被忽略。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Process-Wide 安全性](setting-processwide-security.md)
</dt> </dl>

 

 
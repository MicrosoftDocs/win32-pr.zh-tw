---
description: 若要使用 WMI 連接到遠端電腦，請確定已針對連線啟用正確的 DCOM 設定和 WMI 命名空間安全性設定。
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: 保護遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2a044e49fed5eaa27fbc246dca3306a6c29650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512992"
---
# <a name="securing-a-remote-wmi-connection"></a>保護遠端 WMI 連接

若要使用 WMI 連接到遠端電腦，請確定已針對連線啟用正確的 DCOM 設定和 WMI 命名空間安全性設定。

WMI 具有預設的模擬、驗證和驗證服務 (遠端連線中的目的電腦所需的 NTLM 或 Kerberos) 設定。 您的本機電腦可以使用目標系統不接受的不同預設值。 您可以在連接呼叫中變更這些設定。

本主題將討論下列各節：

-   [適用于 WMI 的 DCOM 模擬和驗證設定](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [設定 DCOM 安全性以允許使用者從遠端存取電腦](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [允許使用者存取特定的 WMI 命名空間](#allowing-users-access-to-a-specific-wmi-namespace)
-   [將命名空間安全性設定為需要遠端連線的資料加密](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [相關主題](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>適用于 WMI 的 DCOM 模擬和驗證設定

WMI 具有預設 DCOM 模擬、驗證和驗證服務 (遠端系統所需的 NTLM 或 Kerberos) 設定。 您的本機系統可能會使用目標遠端系統不接受的不同預設值。 您可以在連接呼叫中變更這些設定。 如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。 不過，針對驗證服務，建議您指定 **RPC \_ C \_ 驗證 \_ 預設值** ，並允許 DCOM 為目的電腦選擇適當的服務。

您可以在 c + + 中對 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 的呼叫提供參數中的設定。 在腳本中，您可以在呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)、 [**SWbemSecurity**](swbemsecurity.md) 物件或腳本的 [標記](constructing-a-moniker-string.md) 字串中建立安全性設定。

如需所有 c + + 模擬常數的清單，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。 如需使用「標記」連接的 Visual Basic 常數和腳本字串，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

下表列出遠端連線 (電腦 B) 的目的電腦所需的預設 DCOM 模擬、驗證和驗證服務設定。 如需詳細資訊，請參閱保護遠端 WMI 連接。



| 電腦 B 作業系統 | 模擬層級腳本字串 | 驗證層級腳本字串 | 驗證服務 |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista 或更新版本      | Impersonate                          | Pkt                                   | Kerberos               |



 

WMI 遠端連線受 (UAC) 和[Windows 防火牆](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)的[使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))影響。 如需詳細資訊，請參閱 [從 Vista 遠端連線至 WMI](connecting-to-wmi-remotely-starting-with-vista.md) ，並 [透過 Windows 防火牆進行連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。

請注意，連接到本機電腦上的 WMI 具有預設的驗證層級 **PktPrivacy**。

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>設定 DCOM 安全性以允許使用者從遠端存取電腦

WMI 中的安全性與連接至 WMI 命名空間有關。 WMI 使用 DCOM 來處理遠端呼叫。 連線到遠端電腦失敗的原因之一，是因為 DCOM 失敗 (錯誤「DCOM 拒絕存取」的十進位-2147024891 或 hex 0x80070005) 。 如需適用于 c + + 應用程式之 WMI 中 DCOM 安全性的詳細資訊，請參閱 [設定用戶端應用程式安全性](setting-client-application-process-security.md)。

您可以使用 [DCOM 設定公用程式] (**DCOMCnfg.exe**) 在 **主控台** 的 [系統 **管理工具**] 中找到，來設定 WMI 的 dcom 設定。 此公用程式會公開設定，讓某些使用者透過 DCOM 從遠端連線到電腦。 系統管理員群組的成員預設允許遠端連線到電腦。 您可以使用此公用程式來設定安全性，以啟動、存取及設定 WMI 服務。

下列程式描述如何授與特定使用者和群組的 DCOM 遠端啟動和啟用許可權。 如果電腦 A 從遠端連線到電腦 B，您可以在電腦 B 上設定這些許可權，以允許不屬於電腦 B 上 Administrators 群組的使用者或群組，在電腦 B 上執行 DCOM 啟動和啟用呼叫。

**授與使用者或群組的 DCOM 遠端啟動和啟用許可權**

1.  按一下 [ **開始**]，按一下 [ **執行**]，輸入 **DCOMCNFG**，然後按一下 **[確定]**。
2.  在 [**元件服務**] 對話方塊中，依序展開 [**元件服務**]、[**電腦**]，然後以滑鼠右鍵按一下 **我的電腦** 然後按一下 [內容 **]。**
3.  在 [ **我的電腦屬性** ] 對話方塊中，按一下 [ **COM 安全性** ] 索引標籤。
4.  在 [ **啟動和啟用許可權**] 下，按一下 [ **編輯限制**]。
5.  如果您的名稱或群組沒有出現在 [**群組或使用者名稱] 清單** 中，請在 [**啟動許可權**] 對話方塊中，依照下列步驟執行：

    1.  在 [ **啟動許可權** ] 對話方塊中，按一下 [ **新增**]。
    2.  在 [ **選取使用者、電腦或群組** ] 對話方塊的 [ **輸入物件名稱來選取** ] 方塊中，新增您的名稱和群組，然後按一下 **[確定]**。

6.  在 [ **啟動許可權** ] 對話方塊中，選取 [ **群組或使用者名稱** ] 方塊中的使用者和群組。 在 [ **允許** 使用者的 **許可權**] 欄位中，選取 [ **遠端啟動** ] 並選取 [ **遠端啟用**]，然後按一下 **[確定]**。

下列程式描述如何授與特定使用者和群組的 DCOM 遠端存取許可權。 如果電腦 A 從遠端連線到電腦 B，您可以在電腦 B 上設定這些許可權，以允許不屬於電腦 b 上 Administrators 群組的使用者或群組連接到電腦 B。

**授與 DCOM 遠端存取許可權**

1.  按一下 [ **開始**]，按一下 [ **執行**]，輸入 **DCOMCNFG**，然後按一下 **[確定]**。
2.  在 [**元件服務**] 對話方塊中，依序展開 [**元件服務**]、[**電腦**]，然後以滑鼠右鍵按一下 **我的電腦** 然後按一下 [內容 **]。**
3.  在 [ **我的電腦屬性** ] 對話方塊中，按一下 [ **COM 安全性** ] 索引標籤。
4.  在 [ **存取權限**] 下，按一下 [ **編輯限制**]。
5.  在 [**存取權限**] 對話方塊中，選取 [**群組或使用者名稱**] 方塊中的 [**匿名登** 入名稱]。 在 [ **允許** 使用者的 **許可權**] 底下的 [允許] 欄中，選取 [ **遠端存取**]，然後按一下 **[確定]**。

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>允許使用者存取特定的 WMI 命名空間

您可以設定命名空間之 WMI 控制項中的「遠端啟用」許可權，以允許或禁止使用者存取特定的 WMI 命名空間。 如果使用者嘗試連接到不允許其存取的命名空間，則會收到錯誤0x80041003。 根據預設，系統只會針對系統管理員啟用此許可權。 系統管理員可以遠端存取非系統管理員使用者的特定 WMI 命名空間。

下列程式會設定非系統管理員使用者的遠端啟用許可權。

**設定遠端啟用許可權**

1.  使用 WMI 控制連接到遠端電腦。

    如需 WMI 控制項的詳細資訊，請參閱 [使用 Wmi 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。

2.  在 [ **安全性** ] 索引標籤中，選取命名空間，然後按一下 [ **安全性**]。
3.  找出適當的帳戶，並勾選 [**許可權**] 清單中的 [**遠端啟用**]。

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>將命名空間安全性設定為需要遠端連線的資料加密

系統管理員或 MOF 檔案可以設定 WMI 命名空間，如此一來就不會傳回任何資料，除非您使用封包隱私權 (**RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** 或 **PktPrivacy** 做為腳本) 在該命名空間的連接中的標記。 這可確保資料會在網路上進行加密。 如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。 如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

下列 VBScript 程式碼範例示範如何使用 "pktPrivacy" 連接至加密的命名空間。


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI 委派](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[使用 WMI 從遠端建立進程](creating-processes-remotely.md)
</dt> <dt>

[保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)
</dt> <dt>

[保護腳本用戶端](securing-scripting-clients.md)
</dt> </dl>

 

 

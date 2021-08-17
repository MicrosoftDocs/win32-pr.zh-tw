---
description: wmi 使用標準 Windows 安全描述項來控制 WMI 命名空間的存取權。
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: 存取 WMI 命名空間
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b750c8dee2b95597636620dc54ad193cb762cd259b2bf7149c52996e85e09b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926024"
---
# <a name="access-to-wmi-namespaces"></a>存取 WMI 命名空間

wmi 使用標準 Windows *安全描述項* 來控制 WMI 命名空間的存取權。 當您透過 WMI "winmgmts" 的名字標記或 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 或 [**wbemscripting.swbemlocator**](swbemlocator-connectserver.md)的呼叫來連線至 wmi 時，您會連接到特定的命名空間。

本主題將討論下列資訊：

-   [WMI 命名空間安全性](#wmi-namespace-security)
-   [WMI 命名空間的審核](#wmi-namespace-auditing)
-   [命名空間事件的類型](#types-of-namespace-events)
-   [命名空間存取設定](#namespace-access-settings)
-   [WMI 命名空間的預設許可權](#default-permissions-on-wmi-namespaces)
-   [相關主題](#related-topics)

## <a name="wmi-namespace-security"></a>WMI 命名空間安全性

WMI 會將連接到命名空間之使用者的 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 與命名空間的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 進行比較，以維護命名空間安全性。 如需 Windows 安全性的詳細資訊，請參閱[存取 WMI 安全物件](access-to-wmi-securable-objects.md)。

請注意，從 Windows Vista 開始， [ (UAC) 的使用者帳戶控制](https://www.microsoft.com/technet/windowsvista/security/uac.mspx)會影響對 wmi 資料的存取權，以及可使用 [*wmi 控制項*](gloss-w.md)設定的內容。 如需詳細資訊，請參閱 [WMI 命名空間的預設許可權](#default-permissions-on-wmi-namespaces) 以及 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

從遠端電腦連線時，也會影響對 WMI 命名空間的存取。 如需詳細資訊，請參閱[連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)、[保護遠端 WMI](securing-a-remote-wmi-connection.md)連線，以及[透過 Windows 防火牆](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)進行連線。

提供者必須依賴連接的模擬設定，以判斷用戶端腳本或應用程式是否應該接收資料。 如需腳本和用戶端應用程式的詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。 如需 [*提供者*](gloss-p.md) 模擬的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。

## <a name="wmi-namespace-auditing"></a>WMI 命名空間的審核

WMI 會使用命名空間 [*系統存取控制清單 (SACL)*](/windows/desktop/SecGloss/s-gly) 來審核命名空間活動。 若要啟用 WMI 命名空間的審核，請使用 [*Wmi 控制項*](gloss-w.md)上的 [**安全性**] 索引標籤，變更命名空間的 [審核設定]。

安裝作業系統時，不會啟用審核。 若要啟用 [審核]，請按一下標準 **安全性** 視窗中的 [**審核**] 索引標籤。 然後您可以新增一個審核專案。

本機電腦的群組原則必須設定為 [允許審核]。 您可以執行 gpedit.msc MMC 嵌入式管理單元來啟用審核，並在 [**電腦** 設定] 下設定 **Audit 物件存取**  >  **Windows 設定**  >  **安全性設定**  >  **本機原則**  >  **稽核原則**。

審核專案會編輯命名空間的 SACL。 當您新增審核專案時，它可以是使用者、群組、電腦或內建的安全性主體。 加入專案之後，您可以設定產生安全性記錄事件的存取作業。 例如，您可以在 [群組驗證的使用者] 中按一下 [執行方法]。 每當 [已驗證的使用者] 群組的成員在該命名空間中執行方法時，此設定就會產生安全性記錄檔事件。 WMI 事件的事件識別碼為4662。

您的帳戶必須位於系統管理員群組中，並以較高的許可權執行，才能變更 [審核設定]。 內建的系統管理員帳戶也可以變更命名空間的安全性或審核。 如需在提高許可權模式下執行的詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

WMI 審核會產生嘗試存取 WMI 命名空間的成功或失敗事件。 服務不會審核提供者作業成功或失敗。 例如，當腳本連線至 WMI 和命名空間時，可能會失敗，因為執行腳本的帳戶無法存取該命名空間，或可能嘗試操作（例如編輯 DACL），但未授與。

如果您是以 Administrators 群組中的帳戶執行，則可以在 **事件檢視器** 使用者介面中查看命名空間審核事件。

## <a name="types-of-namespace-events"></a>命名空間事件的類型

WMI 會追蹤安全性事件記錄檔中的下列事件種類：

-   稽核成功

    作業必須成功完成兩個步驟，才能成功進行審核。 首先，WMI 會根據用戶端 SID 和命名空間 DACL，授與用戶端應用程式或腳本的存取權。 其次，要求的作業符合該使用者或群組的命名空間 SACL 中的存取權限。

-   Audit 失敗

    WMI 拒絕存取命名空間，但要求的作業符合該使用者或群組的命名空間 SACL 中的存取權限。

## <a name="namespace-access-settings"></a>命名空間存取設定

您可以在 WMI 控制項上，查看各種帳戶的命名空間存取權限。 這些常數會在 [**命名空間存取權限常數**](namespace-access-rights-constants.md)中描述。 您可以使用 WMI 控制或以程式設計方式變更 WMI 命名空間的存取權。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

除了遠端啟用許可權之外，WMI 會針對下列清單所列的所有存取權限進行變更。 這些變更會記錄為與編輯安全性許可權相對應的 audit success 或失敗。

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute 方法
</dt> <dd>

允許使用者執行 WMI 類別上定義的方法。 對應至 **WBEM \_ 方法 \_ 執行** 存取權限常數。

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>完整寫入
</dt> <dd>

允許靜態和動態的 WMI 類別和類別實例的完整讀取、寫入和刪除許可權。 對應至 **WBEM \_ FULL \_ WRITE \_ REP** 存取權限常數。

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>部分寫入
</dt> <dd>

允許靜態 WMI 類別實例的寫入存取權。 對應至 **WBEM \_ 部分 \_ 寫入 \_ 代表** 存取權限常數。

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>提供者寫入
</dt> <dd>

允許動態 WMI 類別實例的寫入存取權。 對應至 **WBEM \_ 寫入 \_ 提供者** 存取權限常數。

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>啟用帳戶
</dt> <dd>

允許 WMI 類別實例的讀取權限。 對應至 **WBEM \_ 啟用** 存取權限常數。

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>遠端啟用
</dt> <dd>

允許遠端電腦存取命名空間。 對應至 **WBEM \_ 遠端 \_ 訪問** 存取權限常數。

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>讀取安全性
</dt> <dd>

允許對 DACL 設定的唯讀存取。 對應至 **讀取 \_ 控制** 存取權限常數。

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>編輯安全性
</dt> <dd>

允許 DACL 設定的寫入權限。 對應至 **寫入 \_ DAC** 存取權限常數。

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>WMI 命名空間的預設許可權

預設安全性群組為：

-   驗證的使用者
-   LOCAL SERVICE
-   NETWORK SERVICE
-   本機電腦上的系統管理員 () 

已驗證的使用者、本機服務和網路服務的預設存取權限為：

-   執行方法
-   全部寫入
-   啟用帳戶

Administrators 群組中的帳戶擁有擁有權限，包括編輯安全描述項。 不過，由於使用者帳戶控制 (UAC) ，因此 WMI 控制項或腳本必須以更高的安全性執行。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

有時腳本或應用程式必須啟用系統管理員許可權（例如 **SeSecurityPrivilege**），才能執行作業。 例如，腳本可以執行 [**Win32 \_ printer**](/windows/desktop/CIMWin32Prov/win32-printer)類別的 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer)方法，而不需要 **SeSecurityPrivilege** ，並且在印表機物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly) [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly)中取得安全性資訊。 不過，除非 **SeSecurityPrivilege** 許可權可供帳戶使用且已啟用，否則 SACL 資訊不會傳回給腳本。 如果帳戶沒有可用的許可權，則無法啟用。 如需詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> </dl>

 

 

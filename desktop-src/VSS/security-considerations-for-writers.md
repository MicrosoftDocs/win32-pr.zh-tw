---
description: VSS 基礎結構需要寫入器進程才能同時作為 COM 用戶端和伺服器。
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: 寫入器的安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980973"
---
# <a name="security-considerations-for-writers"></a>寫入器的安全性考慮

VSS 基礎結構需要寫入器進程才能同時作為 COM 用戶端和伺服器。

以伺服器的身分執行時，VSS 寫入器會公開 COM 介面 (例如， [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 這類 vss 事件處理常式會) 並接收來自 vss 進程的傳入 com 呼叫 (例如要求者和 vss 服務) 或來自 vss 外部進程的 RPC 呼叫，通常是在這些進程產生 vss 事件時 (例如，當要求者呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)) 時。 因此，VSS 寫入器需要安全地管理哪些 COM 用戶端能夠讓傳入的 COM 呼叫進入其進程。

同樣地，VSS 寫入器也可以做為 COM 用戶端，對 VSS 基礎結構所提供的回呼發出傳出的 COM 呼叫，或對 VSS 外部的進程發出 RPC 呼叫。 這些回呼是由備份應用程式或 VSS 服務所提供，可讓寫入器執行工作，例如透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面更新備份元件檔。 因此，VSS 安全性設定必須允許寫入器對其他 VSS 進程發出傳出的 COM 呼叫。

管理寫入器安全性問題最簡單的機制，就是適當選取執行它的使用者帳戶。 寫入器通常需要以 Administrators 群組或 Backup Operators 群組成員的使用者身分執行，或者必須以本機系統帳戶的身分執行。

根據預設，當寫入器作為 COM 用戶端時，如果它不是在這些帳戶下執行，則它所做的任何 COM 呼叫都會自動被 **E \_ ACCESSDENIED** 拒絕，而不會取得 COM 方法的執行。

## <a name="disabling-com-exception-handling"></a>停用 COM 例外狀況處理

開發寫入器時，請將 [COM COMGLB \_ 例外狀況 \_ 沒有 \_ 處理全域選項] 旗標設定為停用 com 例外狀況處理。 請務必這麼做，因為 COM 例外狀況處理可以遮罩 VSS 應用程式中的嚴重錯誤。 遮罩的錯誤可能會讓進程處於不穩定且無法預測的狀態，而導致損毀和停止回應。 如需此旗標的詳細資訊，請參閱 [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions)。

## <a name="setting-writer-default-com-access-check-permission"></a>設定寫入器預設 COM 存取檢查許可權

撰寫者必須注意，當其進程作為伺服器時 (例如，為了處理) 的 VSS 事件，它們必須允許來自其他 VSS 參與者的連入呼叫，例如要求者或 VSS 服務。

不過，根據預設，處理常式只會允許在相同登入會話下執行的 COM 用戶端，) 或在本機系統帳戶下執行。 這是潛在的問題，因為這些預設值不足以支援 VSS 基礎結構。 例如，要求者可能會以「備份操作員」使用者帳戶執行，該帳戶不在與寫入器程式相同的登入會話中，也不是本機系統帳戶。

為了處理這種類型的問題，每個 COM 伺服器進程都可以進一步控制 RPC 或 COM 用戶端是否能夠在此情況) 下，使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的預設 com 存取檢查許可權，以進一步控制是否允許 RPC 或 com 用戶端執行 COM (方法。

寫入器可以明確地執行下列動作：

-   允許所有進程存取寫入器進程。

    此選項可能適用于許多寫入器，而其他 COM 伺服器會使用此選項，例如，所有以 SVCHOST 為基礎的 Windows 服務都已使用此選項，預設為所有 COM + 服務。

    允許所有進程執行傳入的 COM 呼叫不一定是安全性弱點。 作為 COM 伺服器的寫入器，就像所有其他 COM 伺服器一樣，一律會保留在其處理常式中所執行的每個 COM 方法上授權其用戶端的選項。

    若要允許所有進程對寫入器進行 COM 存取，您可以傳遞 **Null** 安全描述項作為 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的第一個參數。  (請注意， **CoInitializeSecurity** 必須針對整個進程呼叫最多一次。 如需 **CoInitializeSecurity** 的詳細資訊，請參閱 COM 檔。 ) 

    下列程式碼範例包含對 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫：

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定寫入器的 COM 層級安全性時，您應該執行下列作業：

    -   將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ CONNECT**。

        為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。

    -   除非寫入器進程需要針對與 VSS 不相關的特定 RPC 或 COM 呼叫，才能進行模擬，否則請將模擬層級設定為 **RPC \_ C \_ IMP \_ 等級 \_ 識別** 。

-   只允許指定的進程存取寫入器進程。

    COM 伺服器 (例如，使用非 **Null** 安全描述項呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的寫入器) 可以使用描述項，將本身設定為僅接受屬於特定帳戶集的使用者的來電。

    寫入器必須確保在有效使用者下執行的 COM 用戶端獲得授權可呼叫其進程。 在第一個參數中指定安全描述項的寫入器必須允許下列使用者對要求者進程執行撥入電話：

    -   [本機系統]
    -   本機 Administrators 群組的成員
    -   本機備份操作員群組的成員
    -   寫入器執行時所用的帳戶

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>明確控制寫入器的使用者帳戶存取權

在某些情況下，將寫入器的存取許可權制為以本機系統或本機系統管理員或本機備份操作員本機群組執行的程式，可能會太嚴格。

例如，可能不需要在系統管理員或備份操作員帳戶下執行寫入程式 (可能是協力廠商的非系統寫入器) 。 基於安全性理由，最好不要以人為方式升級進程的許可權以支援 VSS。

在這些情況下，必須修改 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** 登錄機碼，以指示 VSS 指定的使用者可以安全地執行 vss 寫入器。

在此機碼下，您必須建立與要授與或拒絕存取的帳戶名稱相同的子機碼。 此子機碼必須設定為下表中的其中一個值。

| 值 | 意義                                             |
|-------|-----------------------------------------------------|
| 0     | 拒絕使用者存取您的寫入器和要求者。  |
| 1     | 授與使用者存取您的寫入器。               |
| 2     | 授與使用者對您要求者的存取權。            |
| 3     | 將您的寫入器和要求者的存取權授與使用者。 |



 

下列範例會授與 "MyDomain \\ >myuser" 帳戶的存取權：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

這種機制也可以用來明確地限制允許的使用者執行 VSS 寫入器。 下列範例會限制來自 "ThatDomain \\ Administrator" 帳戶的存取：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

使用者 ThatDomain \\ 系統管理員無法執行 VSS 寫入器。

 

 

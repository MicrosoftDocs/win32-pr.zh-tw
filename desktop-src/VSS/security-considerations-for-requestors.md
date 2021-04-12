---
description: VSS 基礎結構需要 VSS 要求者（例如，備份應用程式）能夠以 COM 用戶端和伺服器的形式來運作。
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: 要求者的安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318980"
---
# <a name="security-considerations-for-requesters"></a>要求者的安全性考慮

VSS 基礎結構需要 VSS 要求者（例如，備份應用程式）能夠以 COM 用戶端和伺服器的形式來運作。

當作為伺服器時，要求者會公開一組 COM 回呼介面，可從外部 (進程（例如，寫入器或 VSS 服務) ）叫用這些介面。 因此，要求者需要安全地管理哪些 COM 用戶端能夠讓傳入的 COM 呼叫進入其進程。

同樣地，要求者可以作為 VSS 寫入器或 VSS 服務所提供之 COM Api 的 COM 用戶端。 要求者特定的安全性設定必須允許來自要求者的傳出 COM 呼叫至這些其他進程。

管理要求者的安全性問題最簡單的機制，就是適當地選取執行它的使用者帳戶。

要求者通常需要以 Administrators 群組或 Backup Operators 群組成員的使用者身分執行，或是以本機系統帳戶的身分執行。

根據預設，當要求者作為 COM 用戶端時，如果它不是在這些帳戶下執行，則任何 COM 呼叫都會自動被 **E \_ ACCESSDENIED** 拒絕，甚至不會進入 COM 方法的執行。

## <a name="disabling-com-exception-handling"></a>停用 COM 例外狀況處理

開發要求者時，請將 [COM COMGLB \_ 例外狀況 \_ 沒有 \_ 處理全域選項] 旗標設定為停用 com 例外狀況處理。 請務必這麼做，因為 COM 例外狀況處理可以遮罩 VSS 應用程式中的嚴重錯誤。 遮罩的錯誤可能會讓進程處於不穩定且無法預測的狀態，而導致損毀和停止回應。 如需此旗標的詳細資訊，請參閱 [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions)。

## <a name="setting-requester-default-com-access-check-permission"></a>設定要求者預設 COM 存取檢查許可權

要求者必須注意，當其程式做為伺服器 (例如，允許寫入器修改備份元件檔) 時，必須允許來自其他 VSS 參與者（例如，寫入器或 VSS 服務）的撥入電話。

不過，根據預設，Windows 進程只會允許在相同登入會話下執行的 COM 用戶端 (自我 SID) 或在本機系統帳戶下執行。 這是潛在問題，因為這些預設值對 VSS 基礎結構而言並不足夠。 例如，寫入器可能會以「備份操作員」使用者帳戶的形式執行，該帳戶不在與要求者進程相同的登入會話中，也不是本機系統帳戶。

為了處理這種類型的問題，每個 COM 伺服器進程都可以進一步控制 RPC 或 COM 用戶端是否允許執行伺服器所執行的 COM 方法 (在此案例中，) 使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的「預設 COM 存取檢查」許可權。

要求者可以明確地執行下列動作：

-   允許所有進程存取要求者進程的呼叫。

    此選項可能適用于大部分的要求者，且由其他 COM 伺服器使用，例如，所有 SVCHOST 型 Windows 服務都已使用此選項，預設為所有 COM + 服務。

    允許所有進程執行傳入的 COM 呼叫不一定是安全性弱點。 作為 COM 伺服器的要求者（如同所有其他 COM 伺服器），一律會保留此選項，以在其處理常式中執行的每個 COM 方法上授權其用戶端。

    請注意，根據預設，VSS 所執行的內部 COM 回呼會受到保護。

    若要允許所有進程對要求者進行 COM 存取，您可以傳遞 **Null** 安全描述項作為 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的第一個參數。  (請注意， **CoInitializeSecurity** 必須針對整個進程呼叫最多一次。 如需 **CoInitializeSecurity** 呼叫的詳細資訊，請參閱 COM 檔或 MSDN。 ) 

    下列程式碼範例顯示要求者如何在 Windows 8 和 Windows Server 2012 和更新版本中呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以便與適用于遠端檔案共用的 VSS 相容 (RVSS) ：

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定要求者的 COM 層級安全性時，您應該執行下列作業：

    -   將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 完整性**。 為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。
    -   將模擬層級設定為 **RPC \_ C \_ IMP \_ 層級 \_** 模擬。
    -   設定 **EOAC \_ 靜態** 的掩蓋安全性功能。 如需有關掩蔽安全性的詳細資訊，請參閱「 [掩蔽](../com/cloaking.md)」。

    下列程式碼範例顯示要求者如何在 Windows 7 和 Windows Server 2008 R2 和更早版本的 (或 Windows 8 和 Windows Server 2012 和更新版本中呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，) 不需要 RVSS 相容性：

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定要求者的 COM 層級安全性時，您應該執行下列作業：

    -   將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ CONNECT**。 為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。
    -   將模擬層級設定為 **RPC \_ C \_ IMP \_ level \_ 識別** ，除非要求者進程需要針對與 VSS 無關的特定 RPC 或 COM 呼叫，允許模擬。

-   僅允許指定的進程存取要求者進程。

    COM 伺服器 (例如要求者) ，其會使用非 **Null** 的安全描述項來呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，因為第一個參數可以使用描述項，將本身設定為僅接受屬於特定帳戶集的使用者的撥入電話。

    要求者必須確定在有效使用者下執行的 COM 用戶端已獲授權可呼叫其進程。 在第一個參數中指定安全描述項的要求者，必須允許下列使用者對要求者進程執行撥入電話：

    -   [本機系統]
    -   本機服務

        **WINDOWS XP：** 在 Windows Server 2003 之前，不支援這個值。

    -   網路服務

        **WINDOWS XP：** 在 Windows Server 2003 之前，不支援這個值。

    -   本機 Administrators 群組的成員
    -   本機備份操作員群組的成員
    -   在下列登錄位置中指定的特殊使用者，以 "1" 作為其 REG \_ DWORD 值

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>明確控制要求者的使用者帳戶存取權

在某些情況下，會將要求者的存取許可權制為以本機系統或本機系統管理員或本機備份操作員群組執行的進程，可能太過嚴格。

例如，指定的要求者進程通常不需要在系統管理員或備份操作員帳戶下執行。 基於安全性理由，最好不要以人為方式升級處理常式許可權以支援 VSS。

在這些情況下，必須修改 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** 登錄機碼，以指示 vss 指定的使用者可以安全地執行 vss 要求者。

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

這種機制也可以用來明確地限制其他允許的使用者執行 VSS 要求者。 下列範例會限制來自 "ThatDomain \\ Administrator" 帳戶的存取：

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

使用者 ThatDomain \\ 系統管理員無法執行 VSS 要求者。

## <a name="performing-a-file-backup-of-the-system-state"></a>執行系統狀態的檔案備份

如果要求者藉由備份個別檔案來執行系統狀態備份，而不是使用磁片區映射進行備份，則必須呼叫 [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) 函式來列舉位於下列目錄之檔案的永久連結：

-   Windows \\ system32 \\ WDI \\ perftrack\\
-   Windows \\ WINSXS\\

這些目錄只能由 Administrators 群組的成員存取。 基於這個理由，這類要求者必須在系統帳戶下執行，或是以 Administrators 群組成員的使用者帳戶執行。

**WINDOWS XP 和 Windows Server 2003：** 在 Windows Vista 和 Windows Server 2008 之前，不支援 [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) 函數。

 

 

---
description: LogonUserExExW 函式會嘗試將使用者登入本機電腦。
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: 'LogonUserExExW 函式 (Winbasep) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 8e6b7c5b377ffa7b517ccd19d1dfbffa08d26191af3822f9d9b17cc02c33d055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922333"
---
# <a name="logonuserexexw-function"></a>LogonUserExExW 函式

**LogonUserExExW** 函式會嘗試將使用者登入本機電腦。 本機電腦是用來呼叫 **LogonUserExExW** 的電腦。 您無法使用 **LogonUserExExW** 來登入遠端電腦。 使用使用者名稱和網域來指定使用者，並使用純文字密碼來 [*驗證*](../secgloss/a-gly.md) 使用者。 如果函式成功，則會接收代表已登入使用者之權杖的控制碼。 然後，您可以使用這個權杖控制碼來模擬指定的使用者，或在大部分情況下，建立在指定使用者的內容中執行的 [*處理*](../secgloss/p-gly.md) 程式。

此函式類似于 [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) 函式，不同之處在于它會採用額外的參數 *pTokenGroups*，也就是在登入成功時，新增至傳回給呼叫者的權杖中的一或多個 [*安全性識別碼*](../secgloss/s-gly.md) (sid) 。

此函式未在公用標頭中宣告，且沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Advapi32.dll。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszUsername* \[在\]
</dt> <dd>

指定使用者名稱之以 null 結束的字串指標。 這是要登入的使用者帳戶名稱。 如果您使用 (UPN) 格式的 [*使用者主體名稱*](../secgloss/u-gly.md) ，則 *lpszDomain* 參數必須為 **Null**。

</dd> <dt>

*lpszDomain* \[在中，選擇性\]
</dt> <dd>

以 null 結束的字串指標，指定其帳戶資料庫包含 *lpszUsername* 帳戶之網域或伺服器的名稱。 如果此參數為 **Null**，則必須以 UPN 格式指定使用者名稱。 如果此參數為 "."，則此函式只會使用本機帳戶資料庫來驗證帳戶。

</dd> <dt>

*lpszPassword* \[在中，選擇性\]
</dt> <dd>

以 null 結束的字串指標，指定 *lpszUsername* 所指定之使用者帳戶的純文字密碼。 當您使用完密碼之後，請呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式來清除記憶體中的密碼。 如需保護密碼的詳細資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*>dwlogontype* \[在\]
</dt> <dd>

要執行的登入作業類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                        | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_登入 \_ 互動式**</dt> <dt>2</dt> </dl>                    | 這種登入類型適用于將以互動方式使用電腦的使用者，例如 [*終端*](../secgloss/t-gly.md) 機伺服器登入的使用者、遠端 shell 或類似的進程。 這種登入類型有額外的費用，可快取已中斷連線作業的登入資訊;因此，它不適合某些用戶端/伺服器應用程式，例如郵件伺服器。<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_登入 \_ 網路**</dt> <dt>3</dt> </dl>                                | 此登入類型適用于高效能伺服器來驗證純文字密碼。 **LogonUserExExW** 函數不會快取此登入類型的認證。<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_登入 \_ 批次**</dt> <dt>4</dt> </dl>                                      | 這種登入類型適用于批次伺服器，在此情況下，進程可能會代表使用者執行，而不需要直接介入。 此類型也適用于較高的效能伺服器，這些伺服器會一次處理許多純文字驗證嘗試，例如郵件或網頁伺服器。 **LogonUserExExW** 函數不會快取此登入類型的認證。<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_登入 \_ 服務**</dt> <dt>5</dt> </dl>                                | 表示服務類型登入。 提供的帳戶必須啟用服務許可權。<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_登入 \_ 解除鎖定**</dt> <dt>7</dt> </dl>                                   | 這種登入類型適用于登入將會以互動方式使用電腦之使用者的 [*GINA*](../secgloss/g-gly.md) dll。 此登入類型可以產生唯一的審核記錄，以顯示何時解除鎖定工作站。<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_登入 \_ 網路 \_ 純**</dt>文本 <dt>8</dt> </dl> | 此登入類型會保留 [*驗證套件*](../secgloss/a-gly.md)中的名稱和密碼，可讓伺服器在模擬用戶端時，與其他網路伺服器進行連線。 伺服器可以接受來自用戶端的純文字認證、呼叫 **LogonUserExExW**、驗證使用者是否可透過網路存取系統，並仍與其他伺服器通訊。 <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_登入 \_ 新 \_ 認證**</dt> <dt>9</dt> </dl>       | 這種登入類型可讓呼叫者複製其目前的權杖，並為輸出連線指定新的認證。 新的登入會話具有相同的本機識別碼，但是針對其他網路連線使用不同的認證。<br/> 只有 **LOGON32 \_ 提供者 \_ WINNT50** 登入提供者才支援此登入類型。<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[在\]
</dt> <dd>

登入提供者。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                           | 意義                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**LOGON32 \_ 提供者 \_ 預設值**</dt> </dl> | 使用系統的標準登入提供者。 預設的 [*安全性提供者*](../secgloss/s-gly.md) 是 NTLM。<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**LOGON32 \_ 提供者 \_ WINNT50**</dt> </dl> | 使用 negotiate 登入提供者。 <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**LOGON32 \_ 提供者 \_ WINNT40**</dt> </dl> | 使用 NTLM 登入提供者。<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[在中，選擇性\]
</dt> <dd>

[**權杖 \_ 群組**](/windows/win32/api/winnt/ns-winnt-token_groups)結構的指標，指定新增至權杖的群組 sid 清單，此函式會在登入成功時收到此清單。 新增至權杖的任何 Sid 也會影響群組擴充。 例如，如果新增的 Sid 是本機群組的成員，這些群組也會新增至接收的存取權杖。

如果此參數不是 **Null**，則此函式的呼叫者必須授與並啟用 **SE \_ TCB \_ 許可權** 許可權。

</dd> <dt>

*phToken* \[out、optional\]
</dt> <dd>

控制碼變數的指標，此變數會接收代表指定使用者之 token 的控制碼。

您可以在 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函數的呼叫中使用傳回的控制碼。

在大部分的情況下，傳回的控制碼是您可以在呼叫 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)函式時使用的 [*主要權杖*](../secgloss/p-gly.md)。 但是，如果您指定 LOGON32 \_ LOGON \_ NETWORK 旗標，除非您呼叫 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)將模擬權杖轉換為主要權杖，否則 **LogonUserExExW** 會傳回您無法在 **CreateProcessAsUser** 中使用的模擬 [*權杖*](../secgloss/i-gly.md)。

當您不再需要這個控制碼時，請呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式來關閉它。

</dd> <dt>

*ppLogonSid* \[out、optional\]
</dt> <dd>

SID 指標的指標，此 SID 會接收使用者登入的 SID。

當您使用完 SID 之後，請呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 函式來釋放它。

</dd> <dt>

*ppProfileBuffer* \[out、optional\]
</dt> <dd>

指標的指標，該指標會接收包含已登入使用者之設定檔的緩衝區位址。

</dd> <dt>

*pdwProfileLength* \[out、optional\]
</dt> <dd>

接收配置檔案緩衝區長度之 **DWORD** 的指標。

</dd> <dt>

*pQuotaLimits* \[out、optional\]
</dt> <dd>

[**配額 \_ 限制**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)結構的指標，此結構會接收已登入使用者之配額的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回非零值。

如果函式失敗，則會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**LOGON32 \_ logon \_ NETWORK** 登入類型是最快的，但有下列限制：

-   函數會傳回模擬 [*權杖*](../secgloss/i-gly.md)，而不是主要權杖。 您無法直接在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式中使用此 token。 不過，您可以呼叫 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) 函式，將權杖轉換為主要權杖，然後在 **CreateProcessAsUser** 中使用它。
-   如果您將權杖轉換為主要權杖，並在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 中使用它來啟動處理常式，則新的進程無法透過重新導向器存取其他網路資源，例如遠端伺服器或印表機。 例外狀況是，如果網路資源不受存取控制，則新的進程將可以存取它。

*LpszUsername* 所指定的帳號必須具有必要的帳戶許可權。 例如，若要使用 **LOGON32 \_ 登入 \_ 互動式** 旗標登入使用者，使用者 (或使用者所屬的群組) 必須具有 **SE \_ 互動式 \_ 登錄 \_ 名稱** 帳戶許可權。 如需影響各種登入作業的帳戶許可權清單，請參閱 [帳戶物件存取權限](../secmgmt/account-object-access-rights.md)。

如果至少有一個權杖存在，則會將使用者視為已登入。 如果您呼叫 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ，然後關閉權杖，使用者仍會登入，直到處理程式 (和所有子進程) 結束為止。

如果提供了選擇性的 *pTokenGroups* 參數，LSA 將不會自動新增本機 SID 或登入 SID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                  |
| 版本<br/>                  | LogonUserExExW 也提供于 windows Server 2003 或 Windows XPwith 一般發行版本。<br/> |
| 標頭<br/>                   | <dl> <dt>Winbasep。h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端/伺服器存取控制](../secauthz/client-server-access-control.md)
</dt> <dt>

[用戶端/伺服器存取控制功能](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**配額 \_ 限制**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 

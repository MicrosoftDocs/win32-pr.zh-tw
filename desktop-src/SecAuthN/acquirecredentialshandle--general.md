---
description: 取得安全性主體預先存在的認證控制碼。
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: 'AcquireCredentialsHandle (一般) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975223"
---
# <a name="acquirecredentialshandle-general-function"></a>AcquireCredentialsHandle (一般) 函數

**AcquireCredentialsHandle (General)** 函式會取得 [*安全性主體*](../secgloss/s-gly.md)預先存在的認證控制碼。 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md)和 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md)函式需要此控制碼。 這些可以是預先存在的認證，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。

> [!Note]  
> 這不是「登入網路」，也不代表認證的收集。

 

如需有關使用此函式搭配特定 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 的詳細資訊，請參閱下列主題。



| 主題                                                                                           | 描述                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)<br/>     | 取得安全性主體的預先存在認證的控制碼，該安全性主體使用 (CredSSP) 的認證安全性支援提供者。<br/> |
| [**AcquireCredentialsHandle (摘要)**](acquirecredentialshandle--digest.md)<br/>       | 取得使用摘要之安全性主體預先存在認證的控制碼。<br/>                                         |
| [**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)<br/>   | 取得使用 Kerberos 之安全性主體預先存在認證的控制碼。<br/>                                       |
| [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md)<br/> | 取得使用 Negotiate 之安全性主體預先存在認證的控制碼。<br/>                                      |
| [**AcquireCredentialsHandle (NTLM)**](acquirecredentialshandle--ntlm.md)<br/>           | 取得使用 NTLM 之安全性主體預先存在認證的控制碼。<br/>                                           |
| [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md)<br/>   | 取得使用 Schannel 之安全性主體的預先存在認證控制碼。<br/>                                       |



 

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszPrincipal* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。

使用摘要 SSP 時，此參數是選擇性的。

使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。

> [!Note]  
> 如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。 Null 字串表示進程需要在其執行 [*安全性內容*](../secgloss/s-gly.md) 之使用者的認證控制碼。

 

</dd> <dt>

*pszPackage* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定將使用這些認證之 [*安全性封裝*](../secgloss/s-gly.md) 的名稱。 這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的 [*安全性封裝*](../secgloss/s-gly.md)名稱。 建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (一般)**](querycontextattributes--general.md) ，並將 *ULATTRIBUTE* 設定為 SECPKG \_ ATTR \_ 封裝 \_ 資訊，以傳回使用中 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊。

使用摘要 SSP 時，請將此參數設定為 WDIGEST \_ SP \_ 名稱。

使用 Schannel SSP 時，請將此參數設定為 UNISP \_ 名稱。

</dd> <dt>

*fCredentialUse* \[在\]
</dt> <dd>

指出將如何使用這些認證的旗標。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_認證 \_ 自動 \_**</dt>登入限制的 <dt>0x00000010</dt> </dl> | 安全性不會使用預設的登入認證或 [認證管理員](credential-manager.md)的認證。<br/> 只有 Negotiate [*限制委派*](../secgloss/s-gly.md)才支援此值。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ 認證 \_ 兩者**</dt> </dl>                                                                                                                  | 驗證傳入的認證或使用本機認證來準備傳出權杖。 此旗標可啟用兩個其他旗標。 此旗標對 Digest 和 Schannel Ssp 而言無效。<br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ 認證 \_ 輸入**</dt> </dl>                                                                                                         | 驗證傳入的伺服器認證。 當呼叫 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md) 或 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) 時，可能會使用驗證授權單位來驗證輸入認證。 如果無法使用這類授權單位，此函式將會失敗，並傳回 SEC \_ E \_ NO \_ 驗證 \_ 授權單位。 驗證是套件特定的。<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ 認證 \_ 輸出**</dt> </dl>                                                                                                      | 允許本機用戶端認證準備傳出權杖。<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_\_ \_ \_ 僅限認證進程原則**</dt> <dt>0x00000020</dt> </dl>   | 此函式會處理伺服器原則，並傳回 **SEC \_ E \_ NO \_ 認證**，表示應用程式應該提示輸入認證。<br/> 只有 Negotiate [*限制委派*](../secgloss/s-gly.md)才支援此值。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/>                                                                                                          |



 

</dd> <dt>

*pvLogonID* \[在\]
</dt> <dd>

識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) 的指標。 此參數是針對檔案系統進程（例如網路重新導向程式）所提供。 此參數可以是 **Null**。

使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。

</dd> <dt>

*pAuthData* \[在\]
</dt> <dd>

封裝特定資料的指標。 這個參數可以是 **Null**，這表示必須使用該 [*安全性封裝*](../secgloss/s-gly.md) 的預設認證。 若要使用提供的認證，請在此參數中傳遞包含這些認證的 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構。 RPC 執行時間會傳遞 [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)中提供的任何內容。

使用摘要 SSP 時，此參數是指向 [**每秒的 \_ WINNT AUTH 身分 \_ \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構的指標，其中包含用來尋找認證的驗證資訊。

使用安全通道 SSP 時，請指定安全通道 [**認證結構， \_**](/windows/win32/api/schannel/ns-schannel-schannel_cred) 指出要使用的通訊協定，以及各種可自訂通道功能的設定。

使用 NTLM 或 Negotiate 套件時，使用者名稱、密碼和網域的最大字元長度分別為256、256和15。

</dd> <dt>

*pGetKeyFn* \[在\]
</dt> <dd>

不使用此參數，應該設定為 **Null**。

</dd> <dt>

*pvGetKeyArgument* \[在\]
</dt> <dd>

不使用此參數，應該設定為 **Null**。

</dd> <dt>

*phCredential* \[擴展\]
</dt> <dd>

[CredHandle](sspi-handles.md)結構的指標，用來接收認證控制碼。

</dd> <dt>

*ptsExpiry* \[擴展\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。 這個 **時間戳記** 結構中所傳回的值取決於 [*限制委派*](../secgloss/s-gly.md)。 [*安全性封裝*](../secgloss/s-gly.md)必須以本地時間傳回此值。

此參數會設定為常數的最長時間。 摘要式 [*安全性內容*](../secgloss/s-gly.md)或認證或使用摘要 SSP 時，沒有到期時間。

使用 Schannel SSP 時，此參數是選擇性的。 當用於驗證的認證是憑證時，此參數會收到該憑證的到期時間。 如果未提供任何憑證，則會傳回最大時間值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則函式會傳回 SEC \_ E \_ OK。

如果函式失敗，則會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                 | Description                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt> </dl> | 沒有足夠的記憶體可完成要求的動作。<br/>                                                                  |
| <dl> <dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt> </dl>      | 發生未對應到 SSPI 錯誤碼的錯誤。<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ 無 \_ 認證**</dt> </dl>      | [*限制委派*](../secgloss/s-gly.md)中不提供任何認證。<br/> |
| <dl> <dt>**秒 \_ E \_ 非 \_ 擁有者**</dt> </dl>           | 函數的呼叫端沒有必要的認證。<br/>                                                                     |
| <dl> <dt>**\_ \_ \_ \_ 找不到 SEC E SECPKG**</dt> </dl>   | 要求的 [*安全性封裝*](../secgloss/s-gly.md) 不存在。<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ 未知的 \_ 認證**</dt> </dl> | 無法辨識提供給封裝的認證。<br/>                                                                            |



 

## <a name="remarks"></a>備註

**AcquireCredentialsHandle (一般)** 函數會傳回主體的控制碼，例如使用者或用戶端，以供特定的 [*限制委派*](../secgloss/s-gly.md)使用。 這可能是預先存在的認證的控制碼，或函式可以建立新的認證集，並將其傳回。 這個控制碼可以在 AcceptSecurityCoNtext 的後續呼叫中使用 [**(一般)**](acceptsecuritycontext--general.md) 和 [**InitializeSecurityCoNtext (的一般)**](initializesecuritycontext--general.md) 函數。

一般而言， **AcquireCredentialsHandle (一般)** 不允許處理常式取得其他登入相同電腦的使用者認證的控制碼。 不過，具有 SE TCB 名稱許可權的呼叫端可以 \_ \_ 選擇指定任何現有登入會話權杖的 [*登入識別碼*](../secgloss/l-gly.md) (LUID) ，以取得該會話認證的控制碼 [](../secgloss/s-gly.md) 。 一般來說，這是由必須代表已登入使用者的核心模式模組所使用。

封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。 如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。

針對核心模式呼叫端，必須注意下列差異：

-   這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md) 字串。
-   您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。

當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode 與 ANSI 名稱<br/>   | **AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI) <br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 

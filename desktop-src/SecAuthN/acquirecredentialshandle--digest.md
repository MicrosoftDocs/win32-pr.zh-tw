---
description: 取得使用摘要之安全性主體預先存在認證的控制碼。
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: 'AcquireCredentialsHandle (Digest) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194207"
---
# <a name="acquirecredentialshandle-digest-function"></a>AcquireCredentialsHandle (Digest) 函數

**AcquireCredentialsHandle (Digest)** 函數會取得 [*安全性主體*](../secgloss/s-gly.md)預先存在的認證控制碼。 [**AcceptSecurityCoNtext (digest)**](acceptsecuritycontext--digest.md)和 [**InitializeSecurityCoNtext (digest)**](initializesecuritycontext--digest.md)函式需要這個控制碼。 這些可以是預先存在的 *認證*，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。

> [!Note]  
> 這不是「登入網路」，也不代表認證的收集。

 

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

> [!Note]  
> 如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。 Null 字串表示進程需要在其執行 [*安全性內容*](../secgloss/s-gly.md) 之使用者的認證控制碼。

 

</dd> <dt>

*pszPackage* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定將使用這些認證之 [*安全性封裝*](../secgloss/s-gly.md) 的名稱。 這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的 [*安全性封裝*](../secgloss/s-gly.md)名稱。 建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (Digest)**](querycontextattributes--digest.md) ，並將 *ULATTRIBUTE* 設定為 SECPKG \_ ATTR \_ 封裝 \_ 資訊，以傳回使用中 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊。

使用摘要 SSP 時，請將此參數設定為 WDIGEST \_ SP \_ 名稱。

</dd> <dt>

*fCredentialUse* \[在\]
</dt> <dd>

指出將如何使用這些認證的旗標。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ 認證 \_ 輸入**</dt> </dl>    | 驗證傳入的伺服器認證。 當呼叫 [**InitializeSecurityCoNtext (digest)**](initializesecuritycontext--digest.md) 或 [**AcceptSecurityCoNtext (摘要)**](acceptsecuritycontext--digest.md) 時，可能會使用驗證授權單位來驗證輸入認證。 如果無法使用這類授權單位，此函式將會失敗，並傳回 SEC \_ E \_ NO \_ 驗證 \_ 授權單位。 驗證是套件特定的。<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ 認證 \_ 輸出**</dt> </dl> | 允許本機用戶端認證準備傳出權杖。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pvLogonID* \[在\]
</dt> <dd>

識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) 的指標。 此參數是針對檔案系統進程（例如網路重新導向程式）所提供。 此參數可以是 **Null**。

</dd> <dt>

*pAuthData* \[在\]
</dt> <dd>

封裝特定資料的指標。 這個參數可以是 **Null**，這表示必須使用該 [*安全性封裝*](../secgloss/s-gly.md) 的預設認證。 若要使用提供的認證，請在此參數中傳遞包含這些認證的 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構。 RPC 執行時間會傳遞 [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)中提供的任何內容。

使用摘要 SSP 時，此參數是指向 [**每秒的 \_ WINNT AUTH 身分 \_ \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構的指標，其中包含用來尋找認證的驗證資訊。

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

**AcquireCredentialsHandle (Digest)** 函式會傳回主體（例如使用者或用戶端）之認證的控制碼，以供特定的 [*限制委派*](../secgloss/s-gly.md)使用。 這可能是預先存在的認證的控制碼，或函式可以建立新的認證集，並將其傳回。 這個控制碼可用於對 [**AcceptSecurityCoNtext (digest)**](acceptsecuritycontext--digest.md) 的後續呼叫，以及 [**InitializeSecurityCoNtext (digest)**](initializesecuritycontext--digest.md) 函數。

一般而言， **AcquireCredentialsHandle (Digest)** 不允許處理常式取得其他登入相同電腦之使用者的認證控制碼。 不過，具有 SE TCB 名稱許可權的呼叫端可以 \_ \_ 選擇指定任何現有登入會話權杖的 [*登入識別碼*](../secgloss/l-gly.md) (LUID) ，以取得該會話認證的控制碼 [](../secgloss/s-gly.md) 。 一般來說，這是由必須代表已登入使用者的核心模式模組所使用。

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

[**AcceptSecurityCoNtext (摘要)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**InitializeSecurityCoNtext (摘要)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 

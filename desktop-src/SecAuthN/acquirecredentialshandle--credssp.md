---
description: AcquireCredentialsHandle (CredSSP) 函數會取得安全性主體預先存在的認證控制碼。
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: AcquireCredentialsHandle (CredSSP) 函式
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969398"
---
# <a name="acquirecredentialshandle-credssp-function"></a>AcquireCredentialsHandle (CredSSP) 函式

**AcquireCredentialsHandle (CredSSP)** 函數會取得安全性主體預先存在的認證控制碼。 [**InitializeSecurityCoNtext (credssp)**](initializesecuritycontext--credssp.md)和 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md)函式需要這個控制碼。 這些可以是預先存在的 *認證*，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。

> [!Note]  
> 這不是「登入網路」，也不代表認證的收集。

## <a name="syntax"></a>語法

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>參數

*pszPrincipal* \[在中，選擇性\]

以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。

> [!Note]  
> 如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。 Null 字串表示進程需要在其執行安全性內容之使用者的認證控制碼。

*pszPackage* \[在\]

以 null 結束的字串指標，指定將使用這些認證之安全性封裝的名稱。 這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的安全性封裝名稱。 建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (CredSSP)**](querycontextattributes--credssp.md) ，並將 *UlAttribute* 設定為 **SECPKG \_ ATTR \_ 封裝 \_ 資訊** ，以傳回使用中安全性封裝的相關資訊。

*fCredentialUse* \[在\]

指出將如何使用這些認證的旗標。 此參數可以是下列其中一個值。

| 值                                                                                                                                                                                                                                        | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ 認證 \_ 輸入**<br/>0x1  | 驗證傳入的伺服器認證。 當呼叫 [**InitializeSecurityCoNtext (credssp)**](initializesecuritycontext--credssp.md) 或 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md) 時，可能會使用驗證授權單位來驗證輸入認證。 如果無法使用這類授權單位，此函式將會失敗，並傳回 **SEC \_ E \_ NO \_ 驗證 \_ 授權** 單位。 驗證是套件特定的 |
| **SECPKG \_ 認證 \_ 輸出**<br/>0x0 | 允許本機用戶端認證準備傳出權杖。 |

*pvLogonId* \[在中，選擇性\]

識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) 的指標。 此參數是針對檔案系統進程（例如網路重新導向程式）所提供。 此參數可以是 **Null**。

*pAuthData* \[在中，選擇性\]

[**CREDSSP \_**](/windows/win32/api/credssp/ns-credssp-credssp_cred)認證結構的指標，此結構會指定 Schannel 和 Negotiate 封裝的驗證資料。

*pGetKeyFn* \[在中，選擇性\]

保留的。 不使用此參數，應該設定為 **Null**。

*pvGetKeyArgument* \[在中，選擇性\]

保留的。 此參數必須設定為 **Null**。

*phCredential* \[擴展\]

[CredHandle](sspi-handles.md)結構的指標，此結構會接收認證控制碼。

*ptsExpiry* \[out、optional\]

[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。 收到的結構值取決於安全性封裝，必須以本地時間指定值。

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 **SEC \_ E \_ OK**。

如果函式失敗，則會傳回下列其中一個錯誤碼。

| 傳回碼                      | Description                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **每 \_ 秒 \_ 沒有足夠的 \_ 記憶體** | 可用的記憶體不足，無法完成要求的動作。 |
| **SEC \_ E \_ 內部 \_ 錯誤**      | 發生未對應到 SSPI 錯誤碼的錯誤。                |
| **SEC \_ E \_ 無 \_ 認證**      | 安全性套件中沒有任何可用的認證。                    |
| **秒 \_ E \_ 非 \_ 擁有者**           | 函數的呼叫端沒有必要的認證。      |
| **\_ \_ \_ \_ 找不到 SEC E SECPKG**   | 要求的安全性封裝不存在。                           |
| **SEC \_ E \_ 未知的 \_ 認證** | 無法辨識提供給封裝的認證。             |

## <a name="remarks"></a>備註

**AcquireCredentialsHandle (CredSSP)** 函數會傳回主體的控制碼，例如使用者或用戶端，以供特定的安全性套件使用。 函數可將控制碼傳回預先存在的認證或新建立的認證，並將其傳回。 這個控制碼可用於對 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md) 的後續呼叫，以及 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md) 函數。

一般而言， **AcquireCredentialsHandle (CredSSP)** 不會提供其他登入同一部電腦的使用者認證。 不過，具有 SE \_ TCB 名稱許可權的呼叫端 \_ 可以藉由指定該會話 (LUID) 的登入 [*識別碼*](../secgloss/l-gly.md#_security_logon_identifier_gly)，來取得現有登入會話的認證。 [](../secgloss/p-gly.md#_security_privilege_gly) 一般來說，這是由必須代表已登入使用者的核心模式模組所使用。

封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。 如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。

針對核心模式呼叫端，必須注意下列差異：

- 這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) 字串。
- 您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。

當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端 | \[僅限 Windows Vista 桌面應用程式\]                                              |
| 最低支援的伺服器 | 僅限 Windows Server 2008 \[ desktop 應用程式\]                                        |
| 標頭                   | Sspi (包含 Security .h)                                                       |
| 程式庫                  | Secur32 .lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Unicode 與 ANSI 名稱   | **AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI)  |

## <a name="see-also"></a>另請參閱

- [SSPI 函數](authentication-functions.md#sspi-functions)
- [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

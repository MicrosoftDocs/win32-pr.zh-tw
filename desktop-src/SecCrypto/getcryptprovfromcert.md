---
description: 取得密碼編譯服務提供者 (CSP) 的控制碼，以及憑證內容的金鑰規格。
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c885c439014a26bafba3be8614981c67d200e9f87cd4e3c4f03e8cbcc1b77e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006656"
---
# <a name="getcryptprovfromcert-function"></a>GetCryptProvFromCert 函式

> [!IMPORTANT]
> 此 API 即將淘汰。 Microsoft 可能會在未來的版本中移除此 API。

 

**GetCryptProvFromCert** 函式會取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼，以及 [*憑證*](../secgloss/c-gly.md)內容的金鑰規格。 您可以使用此函式來取得憑證簽發者 [*私密金鑰*](../secgloss/p-gly.md) 的存取權。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

要做為顯示之任何對話方塊擁有者使用的視窗控制碼。 目前未使用這個成員，所以會忽略。 您可以安全地針對此參數傳遞 **Null** 。

</dd> <dt>

*pCert* \[在\]
</dt> <dd>

憑證的憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構指標。

</dd> <dt>

*phCryptProv* \[擴展\]
</dt> <dd>

[**HCRYPTPROV**](hcryptprov.md)結構的指標，該結構為 CSP 的控制碼。

</dd> <dt>

*pdwKeySpec* \[擴展\]
</dt> <dd>

要取出之私密金鑰的規格。 可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。

</dd> <dt>

*pfDidCryptAcquire* \[在\]
</dt> <dd>

值，這個值會指定函數是否根據憑證取得提供者控制碼。

</dd> <dt>

*ppwszTmpContainer* \[out、optional\]
</dt> <dd>

暫存金鑰容器名稱之以 null 結束的字串指標的位址。 **GetCryptProvFromCert** 函式會提供並初始化暫存容器。 呼叫 **GetCryptProvFromCert** 時，位址應該指向 **Null** 值。

</dd> <dt>

*ppwszProviderName* \[out、optional\]
</dt> <dd>

提供者名稱之以 null 結束的字串指標的位址。 **GetCryptProvFromCert** 函數會傳回提供者名稱。 呼叫 **GetCryptProvFromCert** 時，位址應該指向 **Null** 值。

</dd> <dt>

*pdwProviderType* \[擴展\]
</dt> <dd>

指定 CSP 類型。 這可以是零或其中一個 [密碼編譯提供者類型](cryptographic-provider-types.md)。 如果這個成員是零，金鑰容器就是其中一個 CNG 金鑰儲存提供者。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，此函數會傳回 **TRUE**。 如果失敗， **GetCryptProvFromCert** 函數會傳回 **FALSE** 。

## <a name="remarks"></a>備註

當您使用 **-是** 命令列選項叫用時， [MakeCert](makecert.md)工具會呼叫 **GetCryptProvFromCert** 。

如果 *pfDidCryptAcquire* 參數設定為 **TRUE**，則函式會將 *phCryptProv*、 *pdwKeySpec* 和 *pdwProviderType* 參數設定為提供者的值。

當您使用完 CSP 之後，請呼叫 [**FreeCryptProvFromCert**](freecryptprovfromcert.md) 函式將它釋放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 

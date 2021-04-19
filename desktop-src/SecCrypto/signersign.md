---
description: 簽署指定的檔案。
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994388"
---
# <a name="signersign-function"></a>SignerSign 函式

**SignerSign** 函數會簽署指定的檔案。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSubjectInfo* \[在\]
</dt> <dd>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的指標，此結構會指定要簽署的主旨。

</dd> <dt>

*pSignerCert* \[在\]
</dt> <dd>

[**簽署者 \_**](signer-cert.md)憑證結構的指標，此結構會指定要用來建立數位簽章的憑證。

</dd> <dt>

*pSignatureInfo* \[在\]
</dt> <dd>

簽署者簽章 [**\_ \_ 資訊**](signer-signature-info.md) 結構的指標，其中包含數位簽章的相關資訊。

</dd> <dt>

*pProviderInfo* \[在中，選擇性\]
</dt> <dd>

簽署者提供者 [**\_ \_ 資訊**](signer-provider-info.md) 結構的指標，指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的 [*私密金鑰*](../secgloss/p-gly.md) 資訊。

如果此參數的值為 **Null**，則 *pSignerCert* 參數的值必須指定與 CSP 相關聯的憑證。

</dd> <dt>

*pwszHttpTimeStamp* \[在中，選擇性\]
</dt> <dd>

時間戳記伺服器的 URL。

</dd> <dt>

*psRequest* \[在中，選擇性\]
</dt> <dd>

加入至簽署要求之 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) 結構陣列的指標。 如果 *pwszHttpTimeStamp* 參數不包含非 **Null** 的有效值，就會忽略這個參數。

</dd> <dt>

*pSipData* \[在中，選擇性\]
</dt> <dd>

以其他資料形式傳遞至 SIP 函數的32位值。 此的格式和內容是由 SIP 提供者定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 

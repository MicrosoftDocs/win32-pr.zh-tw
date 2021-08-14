---
description: 時間戳記指定的主體。 此函數支援 Authenticode 時間戳記。 若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 SignerTimeStampEx2 函數。
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: cb33852cb2860a29d43a41b2331a910a098384b872e972a74cf94f627bebf75a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898294"
---
# <a name="signertimestamp-function"></a>SignerTimeStamp 函式

**SignerTimeStamp** 函數時間會將指定的主旨戳記。 此函數支援 Authenticode 時間戳記。 若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 [**SignerTimeStampEx2**](signertimestampex2.md) 函數。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSubjectInfo* \[在\]
</dt> <dd>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。

</dd> <dt>

*pwszHttpTimeStamp* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。

</dd> <dt>

*psRequest* \[在中，選擇性\]
</dt> <dd>

[**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> <dt>

*pSipData* \[在中，選擇性\]
</dt> <dd>

以其他資料形式傳遞至 SIP 函數的32位值。 此的格式和內容是由 SIP 提供者定義。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 

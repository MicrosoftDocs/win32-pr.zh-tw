---
description: 時間戳記指定的主體，並選擇性地傳回 \_ 包含 BLOB 指標之簽署者內容結構的指標。 您可以使用此函式來執行 x.509 公開金鑰基礎結構、RFC 3161&\# 8211; 符合規範的時間戳記。
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975855"
---
# <a name="signertimestampex2-function"></a>SignerTimeStampEx2 函式

**SignerTimeStampEx2** 函式時間會為指定的主旨加上戳記，並選擇性地將指標傳回至包含 [*BLOB*](../secgloss/b-gly.md)指標的 [**簽署者 \_ 內容**](signer-context.md)結構。 您可以使用此函式來執行 x.509 公開金鑰基礎結構、RFC 3161 相容的時間戳記。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，指定要產生的時間戳記類型。 此參數可以是下列其中一個值。 這些值都是互斥的。



| 值                                                                                                                                                                                                          | 意義                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**簽署者 \_ 時間戳記 \_ AUTHENTICODE**</dt> </dl> | 指定 Authenticode 時間戳記。<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**簽署人 \_ 時間戳記 \_ RFC3161**</dt> </dl>                | 指定符合 RFC 3161 規範的時間戳記。<br/> |



 

</dd> <dt>

*pSubjectInfo* \[在\]
</dt> <dd>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。

</dd> <dt>

*pwszHttpTimeStamp* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。

</dd> <dt>

*dwAlgId* \[在\]
</dt> <dd>

指定要用於執行符合 RFC 3161 規範之時間戳記的雜湊演算法。 Authenticode 時間戳記會忽略此參數。

</dd> <dt>

*psRequest* \[在\]
</dt> <dd>

選擇性。 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> <dt>

*pSipData* \[在\]
</dt> <dd>

選擇性。 以其他資料的形式傳遞至 [*主體介面封裝*](../secgloss/s-gly.md) 的32位值 (SIP) 函式。 此參數的格式和內容是由 SIP 提供者定義。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> <dt>

*ppSignerCoNtext* \[擴展\]
</dt> <dd>

選擇性。 包含已簽署 BLOB 之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標位址。 當您完成使用 **簽署者 \_ 內容** 結構時，請呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) 函式來釋放它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 

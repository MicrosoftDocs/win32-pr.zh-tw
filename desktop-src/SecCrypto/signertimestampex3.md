---
description: 時間戳記指定的主體，並支援在多個簽章上設定時間戳記。
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111973"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3 函式

**SignerTimeStampEx3** 函數時間會將指定的主旨戳記，並支援在多個簽章上設定時間戳記。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定要產生之時間戳記類型的旗標。 此參數可以是下列其中一個值。 這些值都是互斥的。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </dl></td>
<td>指定 Authenticode 時間戳記。<br/>
<blockquote>
[!Note]<br />
Authenticode 不再是慣用的時間戳記類型。 未來可能會移除 Authenticode 時間戳記的支援。 建議您改用 RFC 3161。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </dl></td>
<td>指定符合 RFC 3161 規範的時間戳記。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*dwIndex* \[在\]
</dt> <dd>

指定將加入時間戳記的簽章序號。 如果這個值為零 (0) ，外部簽章將會加上時間戳記。

</dd> <dt>

*pSubjectInfo* \[在\]
</dt> <dd>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。

</dd> <dt>

*pwszHttpTimeStamp* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。

</dd> <dt>

*pszAlgorithmOid* \[在\]
</dt> <dd>

雜湊演算法，用於執行符合 RFC 3161 規範的時間戳記。 Authenticode 時間戳記會忽略此參數。

</dd> <dt>

*psRequest* \[在中，選擇性\]
</dt> <dd>

選擇性。 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> <dt>

*pSipData* \[在中，選擇性\]
</dt> <dd>

選擇性。 以其他資料的形式傳遞至 [*主體介面封裝*](../secgloss/s-gly.md) 的32位值 (SIP) 函式。 此參數的格式和內容是由 SIP 提供者定義。

這個參數是選擇性的，如果未包含，則可以是 **Null** 。

</dd> <dt>

*ppSignerCoNtext* \[擴展\]
</dt> <dd>

選擇性。 包含已簽署 BLOB 之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標位址。 當您完成使用 **簽署者 \_ 內容** 結構時，請呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) 函式來釋放它。

</dd> <dt>

*pCryptoPolicy* \[在中，選擇性\]
</dt> <dd>

如果存在，則為憑證 [**強式 \_ \_ 簽署 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) 結構的指標，其中包含用來檢查強式簽章的參數。 時間戳記必須通過此密碼編譯原則。

</dd> <dt>

*保存* 
</dt> <dd>

保留的。 這個值必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 此函式所傳回的可能錯誤碼包括（但不限於）下列程式碼。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>下列情況可能會傳回此錯誤：<br/>
<ul>
<li>您必須設定<em>dwFlags</em>參數的<strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong>或<strong>SIGNER_TIMESTAMP_RFC3161</strong> 。</li>
<li><em>保留</em>的參數必須是<strong>Null</strong>。</li>
<li>如果您在<em>dwFlags</em>參數中設定<strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong>旗標，則必須將<em>dwIndex</em>參數設定為零。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 

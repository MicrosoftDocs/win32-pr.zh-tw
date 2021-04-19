---
description: 使用摘要來加密訊息，以提供隱私權。
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: 'EncryptMessage (Digest) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966672"
---
# <a name="encryptmessage-digest-function"></a>EncryptMessage (Digest) 函數

**EncryptMessage (Digest)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。 **EncryptMessage (Digest)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。 **EncryptMessage (Digest)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。 某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。

此函式僅以 SASL 機制的形式提供。

> [!Note]  
> 您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 **EncryptMessage (Digest)** 和 [**DECRYPTMESSAGE (digest)**](decryptmessage--digest.md) (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

 

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCoNtext* \[在\]
</dt> <dd>

用來加密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。

</dd> <dt>

*fQOP* \[在\]
</dt> <dd>

指出保護品質的封裝特定旗標。 [*安全性套件*](../secgloss/s-gly.md)可以使用此參數來啟用 [*密碼編譯演算法*](../secgloss/c-gly.md)的選取。

使用摘要 SSP 時，此參數必須設定為零。

</dd> <dt>

*pMessage* \[in、out\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。 該緩衝區包含要加密的訊息。 訊息會就地加密，覆寫結構的原始內容。

此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。

包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，它是從 [**QUERYCONTEXTATTRIBUTES (Digest)**](querycontextattributes--digest.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。

使用摘要 SSP 時，必須有類型為之 SECBUFFER \_ 填補或 SEC 緩衝區資料的第二個緩衝區， \_ \_ 才能保存簽章資訊。 [](../secgloss/d-gly.md#_security_digital_signature_gly) 若要取得輸出緩衝區的大小，請呼叫 [**QueryCoNtextAttributes (Digest)**](querycontextattributes--digest.md) 函數，並指定 SECPKG \_ ATTR \_ 大小。 函數會傳回 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) 結構。 輸出緩衝區的大小是 **cbMaxSignature** 和 **cbBlockSize** 成員中值的總和。

不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。

</dd> <dt>

*MessageSeqNo* \[在\]
</dt> <dd>

傳輸應用程式指派給訊息的序號。 如果傳輸應用程式不會維護序號，此參數必須為零。

使用摘要 SSP 時，此參數必須設定為零。 摘要 SSP 會在內部管理順序編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則函式會傳回 SEC \_ E \_ OK。

如果函式失敗，則會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                    | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</dt> </dl>      | 輸出緩衝區太小。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ 內容已 \_ 過期**</dt> </dl>        | 應用程式參考的內容已關閉。 正確撰寫的應用程式應該不會收到此錯誤。<br/>                                                                                               |
| <dl> <dt>**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</dt> </dl> | 不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。<br/>                                                                                                         |
| <dl> <dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt> </dl>    | 沒有足夠的記憶體可完成要求的動作。<br/>                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt> </dl>         | 在 *phCoNtext* 參數中指定了不正確內容控制碼。<br/>                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt> </dl>          | 找不 \_ 到之 secbuffer 資料類型緩衝區。<br/>                                                                                                                                                                                          |
| <dl> <dt>**\_ \_ \_ 不支援 SEC E \_ QOP**</dt> </dl>     | [*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。<br/> |



 

## <a name="remarks"></a>備註

**EncryptMessage (Digest)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。

如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。 包含這項資訊可防止重新執行、插入和隱藏訊息。 [*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。

當您使用摘要 SSP 時，請呼叫 [**QueryCoNtextAttributes (Digest)**](querycontextattributes--digest.md) 函數並指定 SECPKG ATTR 大小，以取得輸出緩衝區的 \_ 大小 \_ 。 函數會傳回 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) 結構。 輸出緩衝區的大小是 **cbMaxSignature** 和 **cbBlockSize** 成員中值的總和。

> [!Note]  
> 您必須依照顯示的順序提供這些緩衝區。

 



| 緩衝區類型                           | Description                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| 之 SECBUFFER \_ 資料流程 \_ 標頭<br/>  | 內部使用。 不需要初始化。<br/>                                                                        |
| 之 SECBUFFER \_ 資料<br/>            | 包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。<br/> |
| 之 SECBUFFER \_ 資料流程 \_ 結尾<br/> | 內部使用。 不需要初始化。<br/>                                                                        |
| 之 SECBUFFER \_ 空白<br/>           | 內部使用。 不需要初始化。 大小可以是零。<br/>                                                      |



 

為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。

**WINDOWS XP：** 此函數也稱為 **SealMessage**。 應用程式現在應該只使用 **EncryptMessage (Digest)** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityCoNtext (摘要)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (摘要)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityCoNtext (摘要)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryCoNtextAttributes (摘要)**](querycontextattributes--digest.md)
</dt> <dt>

[**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

---
description: 使用 Kerberos 加密訊息以提供隱私權。
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: EncryptMessage (Kerberos) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 52ca8fd4d0806db717ae29bdd959e472d72f74ca812e93bcaf3929a488dd4fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008336"
---
# <a name="encryptmessage-kerberos-function"></a>EncryptMessage (Kerberos) 函數

**EncryptMessage (Kerberos)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。 **EncryptMessage (Kerberos)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。 **EncryptMessage (Kerberos)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。 某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。

> [!Note]  
> 當某個執行緒正在進行加密，而另一個執行緒正在解密時，可同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒呼叫 **EncryptMessage (Kerberos)** 和 [**DECRYPTMESSAGE (kerberos)**](decryptmessage--kerberos.md) (SSPI) 內容。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

## <a name="syntax"></a>語法

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
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

此參數可以是下列旗標。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>值</th><th>意義</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>產生標頭或結尾，但不加密訊息。<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</blockquote><br/></td></tr></tbody></table>

</dd> <dt>

*pMessage* \[in、out\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。 該緩衝區包含要加密的訊息。 訊息會就地加密，覆寫結構的原始內容。

此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。

包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，這是從 [**QUERYCONTEXTATTRIBUTES (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。

不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。

</dd> <dt>

*MessageSeqNo* \[在\]
</dt> <dd>

傳輸應用程式指派給訊息的序號。 如果傳輸應用程式不會維護序號，此參數必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則函式會傳回 SEC \_ E \_ OK。

如果函式失敗，則會傳回下列其中一個錯誤碼。

| 傳回碼                                                                                                    | 描述                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</dt> </dl>      | 輸出緩衝區太小。 如需詳細資訊，請參閱＜備註＞。                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ 內容已 \_ 過期**</dt> </dl>        | 應用程式參考的內容已關閉。 正確撰寫的應用程式應該不會收到此錯誤。                                                                                               |
| <dl> <dt>**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</dt> </dl> | 不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。                                                                                                         |
| <dl> <dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt> </dl>    | 沒有足夠的記憶體可完成要求的動作。                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt> </dl>         | 在 *phCoNtext* 參數中指定了不正確內容控制碼。                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt> </dl>          | 找不 \_ 到之 secbuffer 資料類型緩衝區。                                                                                                                                                                                          |
| <dl> <dt>**\_ \_ \_ 不支援 SEC E \_ QOP**</dt> </dl>     | [*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。 |

## <a name="remarks"></a>備註

**EncryptMessage (Kerberos)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。

如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。 包含這項資訊可防止重新執行、插入和隱藏訊息。 [*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。

> [!Note]  
> 您必須依照顯示的順序提供這些緩衝區。

| 緩衝區類型                           | 描述                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| 之 SECBUFFER \_ 資料流程 \_ 標頭<  | 內部使用。 不需要初始化。                                                                       |
| 之 SECBUFFER \_ 資料            | 包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。 |
| 之 SECBUFFER \_ 資料流程 \_ 結尾 | 內部使用。 不需要初始化。                                                                        |
| 之 SECBUFFER \_ 空白           | 內部使用。 不需要初始化。 大小可以是零。                                                      |

為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。

**Windows XP：** 此函數也稱為 **SealMessage**。 應用程式現在應該只使用 **EncryptMessage (Kerberos)** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------|
| 最低支援的用戶端 | Windows\[僅限 XP desktop 應用程式\]          |
| 最低支援的伺服器 | Windows\[僅限 Server 2003 desktop 應用程式\] |
| 標頭                   | Sspi (包含 Security .h)                |
| 程式庫                  | Secur32 .lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityCoNtext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryCoNtextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

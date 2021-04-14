---
description: 使用 Negotiate 加密訊息以提供隱私權。
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: EncryptMessage (Negotiate) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 037866088f58fa1d70939b84062161a6e4f610b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320216"
---
# <a name="encryptmessage-negotiate-function"></a>EncryptMessage (Negotiate) 函數

**EncryptMessage (Negotiate)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。 **EncryptMessage (Negotiate)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。 **EncryptMessage (Negotiate)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。 某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。

> [!Note]  
> 您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 **EncryptMessage (Negotiate)** 和 [**DECRYPTMESSAGE (negotiate)**](decryptmessage--negotiate.md) (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

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

*phCoNtext* \[用於 \] 加密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。

*fQOP* \[在 \] 指出保護品質的封裝特定旗標中。 [*安全性套件*](../secgloss/s-gly.md)可以使用此參數來啟用 [*密碼編譯演算法*](../secgloss/c-gly.md)的選取。

此參數可以是下列旗標。

| 值                  | 意義                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | 產生標頭或結尾，但不加密訊息。 |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。

*pMessage* \[在中，輸出 \] [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標。 在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。 該緩衝區包含要加密的訊息。 訊息會就地加密，覆寫結構的原始內容。

此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。

包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，這是從 [**QUERYCONTEXTATTRIBUTES (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。

不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。

*MessageSeqNo* \[\]傳輸應用程式指派給訊息的序號。 如果傳輸應用程式不會維護序號，此參數必須為零。

## <a name="return-value"></a>傳回值

如果函式成功，則函式會傳回 SEC \_ E \_ OK。

如果函式失敗，則會傳回下列其中一個錯誤碼。

| 傳回碼                         | Description                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ 緩衝區 \_ 太 \_ 小**      | 輸出緩衝區太小。 如需詳細資訊，請參閱＜備註＞。                                                                   |
| **SEC \_ E \_ 內容已 \_ 過期**        | 應用程式參考的內容已關閉。 正確撰寫的應用程式應該不會收到此錯誤。 |
| **SEC \_ E \_ 加密 \_ 系統 \_ 無效** | 不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。                                |
| **每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**    | 沒有足夠的記憶體可完成要求的動作。                                                               |
| **SEC \_ E \_ 不正確 \_ 控制碼**         | 在 *phCoNtext* 參數中指定了不正確內容控制碼。                                                       |
| **SEC \_ E \_ 不正確 \_ 權杖**          | 找不 \_ 到之 secbuffer 資料類型緩衝區。                                                                                            |
| **\_ \_ \_ 不支援 SEC E \_ QOP**     | [*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。             |

## <a name="remarks"></a>備註

**EncryptMessage (Negotiate)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。

如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。 包含這項資訊可防止重新執行、插入和隱藏訊息。 [*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。

> [!Note]  
> 您必須依照顯示的順序提供這些緩衝區。

| 緩衝區類型                | Description                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| 之 SECBUFFER \_ 資料流程 \_ 標頭  | 內部使用。 不需要初始化。                                                |
| 之 SECBUFFER \_ 資料            | 包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。 |
| 之 SECBUFFER \_ 資料流程 \_ 結尾 | 內部使用。 不需要初始化。                                                |
| 之 SECBUFFER \_ 空白           | 內部使用。 不需要初始化。 大小可以是零。                              |

為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。

**WINDOWS XP：** 此函數也稱為 **SealMessage**。 應用程式現在應該只使用 **EncryptMessage (Negotiate)** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------------|
| 最低支援的用戶端 | \[僅限 WINDOWS XP desktop 應用程式\]                |
| 最低支援的伺服器 | 僅限 Windows Server 2003 \[ desktop 應用程式\]       |
| 標頭                   | Sspi (包含 Security .h)                      |
| 程式庫                  | Secur32 .lib                                     |
| DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>另請參閱

- [SSPI 函數](authentication-functions.md#sspi-functions)
- [**AcceptSecurityCoNtext (Negotiate)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md)
- [**InitializeSecurityCoNtext (Negotiate)**](initializesecuritycontext--negotiate.md)
- [**QueryCoNtextAttributes (Negotiate)**](querycontextattributes--negotiate.md)
- [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

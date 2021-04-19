---
description: 使用 Negotiate 解密訊息。
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (Negotiate) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986382"
---
# <a name="decryptmessage-negotiate-function"></a>DecryptMessage (Negotiate) 函數

**DecryptMessage (Negotiate)** 函數會解密訊息。 某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。

> [!Note]  
> 您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)和 **DECRYPTMESSAGE (negotiate)** (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

## <a name="syntax"></a>語法

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a>參數

*phCoNtext* \[在\]

用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。

*pMessage* \[in、out\]

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 其中至少一個必須是之 SECBUFFER \_ 資料類型。 該緩衝區包含加密的訊息。 加密的訊息會就地解密，並覆寫其緩衝區的原始內容。

*MessageSeqNo* \[在\]

傳輸應用程式所預期的序號（如果有的話）。 如果傳輸應用程式不會維護序號，此參數必須設定為零。

*pfQOP* \[擴展\]

**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。

此參數可以是下列旗標。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>值</th><th>意義</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>訊息未加密，但產生的是標頭或結尾。<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>傳回值

如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。

如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。

| 傳回碼                     | Description                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ 未完成 \_ 訊息** | 輸入緩衝區中的資料不完整。 應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (協商)**](decryptmessage--negotiate.md) 。 |
| **SEC \_ E \_ \_ \_ 順序**   | 未以正確的順序接收訊息。                                                                                                                              |

## <a name="remarks"></a>備註

有時候，應用程式會從遠端方讀取資料、嘗試使用 **DecryptMessage (Negotiate)** 將其解密，併發現 **DecryptMessage (Negotiate)** 成功，但輸出緩衝區是空的。 這是正常行為，而且應用程式必須能夠處理它。

**WINDOWS XP：** 此函數也稱為 **UnsealMessage**。 應用程式現在應該只使用 **DecryptMessage (Negotiate)** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端 | \[僅限 WINDOWS XP desktop 應用程式\]          |
| 最低支援的伺服器 | 僅限 Windows Server 2003 \[ desktop 應用程式\] |
| 標頭                   | Sspi (包含 Security .h)                |
| 程式庫                  | Secur32 .lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>另請參閱

- [SSPI 函數](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

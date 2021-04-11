---
description: 使用 Kerberos 解密訊息。
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage (Kerberos) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113809"
---
# <a name="decryptmessage-kerberos-function"></a>DecryptMessage (Kerberos) 函數

**DecryptMessage (Kerberos)** 函數會解密訊息。 某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。

> [!Note]  
> 當某個執行緒正在進行加密，而另一個執行緒正在解密時，可同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒呼叫 [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)和 **DECRYPTMESSAGE (kerberos)** (SSPI) 內容。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

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

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。 緩衝區包含加密的訊息。 加密的訊息會就地解密，並覆寫其緩衝區的原始內容。

*MessageSeqNo* \[在\]

傳輸應用程式所預期的序號（如果有的話）。 如果傳輸應用程式不會維護序號，此參數必須設定為零。

*pfQOP* \[擴展\]

**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。

此參數可以是下列旗標。

| 值                  | 意義                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | 他的訊息未加密，但產生的是標頭或結尾。 |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。

## <a name="return-value"></a>傳回值

如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。

如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。

| 傳回碼                     | Description                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ 未完成 \_ 訊息** | 輸入緩衝區中的資料不完整。 應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) 。 |
| **SEC \_ E \_ \_ \_ 順序**   | 未以正確的順序接收訊息。                                                                                                                            |

## <a name="remarks"></a>備註

有時候，應用程式會從遠端方讀取資料、使用 **DecryptMessage (kerberos)** 嘗試將它解密，併發現 **DecryptMessage (Kerberos)** 成功，但輸出緩衝區是空的。 這是正常行為，而且應用程式必須能夠處理它。

如需與 GSSAPI 交互操作的詳細資訊，請參閱 [SSPI/Kerberos 與 GSSAPI 的互通性](sspi-kerberos-interoperability-with-gssapi.md)。

**WINDOWS XP：** 此函數也稱為 **UnsealMessage**。 應用程式現在應該只使用 **DecryptMessage (Kerberos)** 。

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
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

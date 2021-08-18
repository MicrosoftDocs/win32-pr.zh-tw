---
description: 使用 Schannel 來解密訊息。
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage (Schannel) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: feec97f9e989270d812458cd61ff34132d118d192108c3f2372b192f2e383464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008476"
---
# <a name="decryptmessage-schannel-function"></a>DecryptMessage (Schannel) 函數

**DecryptMessage (Schannel)** 函數會解密訊息。 某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。


此函式也會與安全通道 [*安全性支援提供者*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) 搭配使用 (SSP) ，向訊息寄件者發出重新協商的要求 (重做連接屬性) 或連接關閉。

> [!Note]  
> 如果有一個執行緒正在進行加密，而另一個執行緒正在解密，則可以同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY)的兩個不同執行緒呼叫 [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)和 **DECRYPTMESSAGE (schannel)** (SSPI) 內容。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。


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


用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) 控制碼。

*pMessage* \[in、out\]

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 其中一個類型可能屬於之 SECBUFFER 資料類型 \_ 。 該緩衝區包含加密的訊息。 加密的訊息會就地解密，並覆寫其緩衝區的原始內容。

使用安全通道 SSP 搭配非連接導向的內容時，在輸入上，結構必須包含四個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 只有一個緩衝區必須是之 SECBUFFER 資料類型 \_ ，而且包含已加密的訊息（已就地解密）。 其餘的緩衝區會用於輸出，而且必須是之 SECBUFFER 空的型別 \_ 。 若為連線導向的內容，則 \_ 必須提供之 secbuffer 資料類型緩衝區（如 nonconnection 導向內容所述）。 此外， \_ 也必須提供包含安全性權杖的第二個之 secbuffer TOKEN 類型緩衝區。

*MessageSeqNo* \[在\]

傳輸應用程式所預期的序號（如果有的話）。 如果傳輸應用程式不會維護序號，此參數必須設定為零。

使用 Schannel SSP 時，此參數必須設定為零。 Schannel SSP 不會使用序號。

*pfQOP* \[擴展\]

**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。

使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。

此參數可以是下列旗標。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>值</th><th>意義</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>訊息未加密，但產生的是標頭或結尾。<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>傳回值

如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。

如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。

| 傳回碼                     | 描述                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ 不正確 \_ 控制碼**     | 在 *phCoNtext* 參數中指定了不正確內容控制碼。 搭配 Schannel SSP 使用。     |
| **SEC \_ E \_ 不正確 \_ 權杖**      | 緩衝區的類型錯誤，或找不到之 SECBUFFER 資料類型的緩衝區 \_ 。 搭配 Schannel SSP 使用。  |
| **秒 \_ E \_ 修改的訊息 \_**    | 已更改訊息。 搭配 Schannel SSP 使用。                                                      |
| **SEC \_ E \_ \_ \_ 順序**   | 未以正確的順序接收訊息。                                                          |
| **秒 \_ - \_ 內容已 \_ 過期**    | 訊息寄件者已使用連接完成，並已起始關機。 如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。 搭配 Schannel SSP 使用。 |
| **秒 \_ 我重新 \_ 協商**         | 遠端物件需要新的交握序列，或應用程式剛起始關機。 返回協調迴圈，並呼叫 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md) 或 [**InitializeSecurityCoNtext (**](initializesecuritycontext--schannel.md)安全通道) ，傳遞從 DecryptMessage SECBUFFER_EXTRA 傳回的 () 。 Schannel 核心模式不支援重新協商。 呼叫端應該忽略此傳回值或關閉連接。 如果忽略此值，可能是因為用戶端或伺服器會關閉連接。 |


## <a name="remarks"></a>備註

有時候，應用程式會從遠端方讀取資料、嘗試使用 **DecryptMessage (schannel)** 將資料解密，併發現 **DecryptMessage (Schannel)** 成功，但輸出緩衝區是空的。 這是正常行為，而且應用程式必須能夠處理它。

當您使用安全通道 SSP 時， [**DecryptMessage (一般)**](decryptmessage--general.md) 函數會傳回 \_ \_ \_ 當訊息寄件者關閉連線時，我內容已過期的秒數。 如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。

如果您使用 TLS 1.0，您可能需要多次呼叫此函式，並在每次呼叫時調整輸入緩衝區來解密整個訊息。


**DecryptMessage (Schannel)** 函式會 \_ \_ 在訊息寄件者想要重新協商 ([*安全性內容*](../secgloss/s-gly.md)) 的連線時，傳回每秒重新協商。 應用程式會藉由呼叫 [**AcceptSecurityCoNtext (Schannel)**](acceptsecuritycontext--schannel.md) (server 端) 或 [**InitializeSecurityCoNtext (schannel)**](initializesecuritycontext--schannel.md) (用戶端) 並傳遞從 DecryptMessage SECBUFFER_EXTRA 傳回的 () ，來處理要求的重新協商。 在這個初始呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。 如需詳細資訊，請參閱 [建立 Schannel 安全性內容](creating-an-schannel-security-context.md)。


## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------|
| 最低支援的用戶端 | Windows\[僅限 XP desktop 應用程式\]          |
| 最低支援的伺服器 | Windows\[僅限 Server 2003 desktop 應用程式\] |
| 標頭                   | Sspi (包含 Security .h)                |
| 程式庫                  | Secur32 .lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>另請參閱

- [SSPI 函數](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

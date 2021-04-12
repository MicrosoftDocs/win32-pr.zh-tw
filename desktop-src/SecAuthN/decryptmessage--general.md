---
description: 解密訊息。
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: 'DecryptMessage (一般) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191566"
---
# <a name="decryptmessage-general-function"></a>DecryptMessage (一般) 函數

**DecryptMessage (一般)** 函數會解密訊息。 某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。

摘要式 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 為用戶端與伺服器之間交換的訊息提供加密和解密機密性（僅限 SASL 機制）。

此函式也會搭配安全通道 SSP 使用，以向訊息寄件者發出連接屬性的重新協商 (重做) 或連接關閉的要求。

> [!Note]  
> 您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 [**EncryptMessage (一般)**](encryptmessage--general.md)和 **DECRYPTMESSAGE (一般)** (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。 如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。

 

如需有關使用此函式搭配特定 SSP 的詳細資訊，請參閱下列主題。



| 主題                                                            | 描述                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (摘要)**](decryptmessage--digest.md)       | 使用 Digest 來解密訊息。    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | 使用 Kerberos 解密訊息。  |
| [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) | 使用 Negotiate 解密訊息。 |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | 使用 NTLM 解密訊息。      |
| [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)   | 使用 Schannel 來解密訊息。  |



 

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

<dl> <dt>

*phCoNtext* \[在\]
</dt> <dd>

用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。

</dd> <dt>

*pMessage* \[in、out\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 其中一個類型可能屬於之 SECBUFFER 資料類型 \_ 。 該緩衝區包含加密的訊息。 加密的訊息會就地解密，並覆寫其緩衝區的原始內容。

使用摘要 SSP 時，在輸入上，結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 其中一個型別必須是之 SECBUFFER \_ DATA 或之 secbuffer \_ STREAM，而且必須包含加密的訊息。

使用安全通道 SSP 搭配非連接導向的內容時，在輸入上，結構必須包含四個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。 只有一個緩衝區必須是之 SECBUFFER 資料類型 \_ ，而且包含已加密的訊息（已就地解密）。 其餘的緩衝區會用於輸出，而且必須是之 SECBUFFER 空的型別 \_ 。 若為連線導向的內容，則 \_ 必須提供之 secbuffer 資料類型緩衝區（如 nonconnection 導向內容所述）。 此外， \_ 也必須提供包含安全性權杖的第二個之 secbuffer TOKEN 類型緩衝區。

</dd> <dt>

*MessageSeqNo* \[在\]
</dt> <dd>

傳輸應用程式所預期的序號（如果有的話）。 如果傳輸應用程式不會維護序號，此參數必須設定為零。

使用摘要 SSP 時，此參數必須設定為零。 摘要 SSP 會在內部管理順序編號。

使用 Schannel SSP 時，此參數必須設定為零。 Schannel SSP 不會使用序號。

</dd> <dt>

*pfQOP* \[擴展\]
</dt> <dd>

**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。

使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。

此參數可以是下列其中一個旗標。



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>值</th><th>意義</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>訊息未加密，但產生的是標頭或結尾。<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>使用摘要 SSP 時，當 [*安全性內容*](../secgloss/s-gly.md) 設定 [*為僅驗證*](../secgloss/s-gly.md) 簽章時，請使用此旗標。 如需詳細資訊，請參閱 [保護品質](quality-of-protection.md)。<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。

如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</dt> </dl>      | 訊息緩衝區太小。 搭配摘要 SSP 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</dt> </dl> | 不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。 搭配摘要 SSP 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ 未完成 \_ 訊息**</dt> </dl>     | 輸入緩衝區中的資料不完整。 應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (一般)**](decryptmessage--general.md) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt> </dl>         | 在 *phCoNtext* 參數中指定了不正確內容控制碼。 搭配 Digest 和 Schannel Ssp 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt> </dl>          | 緩衝區的類型錯誤，或找不到之 SECBUFFER 資料類型的緩衝區 \_ 。 搭配 Schannel SSP 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**秒 \_ E \_ 修改的訊息 \_**</dt> </dl>        | 已更改訊息。 搭配 Digest 和 Schannel Ssp 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ \_ \_ 順序**</dt> </dl>       | 未以正確的順序接收訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**\_ \_ \_ 不支援 SEC E \_ QOP**</dt> </dl>     | [*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。 搭配摘要 SSP 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**秒 \_ - \_ 內容已 \_ 過期**</dt> </dl>        | 訊息寄件者已使用連接完成，並已起始關機。 如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。 搭配 Schannel SSP 使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**秒 \_ 我重新 \_ 協商**</dt> </dl>             | 遠端物件需要新的交握序列，或應用程式剛起始關機。 回到協商迴圈，然後呼叫 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) 或 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md)，傳遞空的輸入緩衝區。 <br/> 如果函式傳回類型為 **SEC \_ 緩衝區 \_** 的緩衝區，則應該將這項傳遞至 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) 函式作為輸入緩衝區。<br/> 搭配 Schannel SSP 使用。<br/> Schannel 核心模式不支援重新協商。 呼叫端應該忽略此傳回值或關閉連接。 如果忽略此值，可能是因為用戶端或伺服器會關閉連接。<br/> |



 

## <a name="remarks"></a>備註

當您使用安全通道 SSP 時， **DecryptMessage (一般)** 函數會傳回 \_ \_ \_ 當訊息寄件者關閉連線時，我內容已過期的秒數。 如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。

當您使用安全通道 SSP 時， **DecryptMessage (一般)** 會 \_ 在 \_ 訊息寄件者想要重新協商 ([*安全性內容*](../secgloss/s-gly.md)) 的連接時，傳回秒的重新保護。 應用程式會藉由呼叫 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) (伺服器端) 或 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md) (用戶端) 並傳入空白的輸入緩衝區，來處理要求的重新協商。 在這個初始呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。 如需詳細資訊，請參閱 [建立 Schannel [*安全性內容*](../secgloss/s-gly.md)](creating-an-schannel-security-context.md)。

如需與 GSSAPI 交互操作的詳細資訊，請參閱 [SSPI/Kerberos 與 GSSAPI 的互通性](sspi-kerberos-interoperability-with-gssapi.md)。

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

[**EncryptMessage (一般)**](encryptmessage--general.md)
</dt> <dt>

[**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

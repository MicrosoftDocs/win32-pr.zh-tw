---
description: 如果需要與 GSSAPI 的互通性，則在使用 Kerberos 安全性支援提供者 (SSP) 時必須特別小心。
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: SSPI/Kerberos 與 GSSAPI 的互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689476"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>SSPI/Kerberos 與 GSSAPI 的互通性

如果需要與 GSSAPI 的互通性，則在使用 [*Kerberos*](../secgloss/k-gly.md) [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 時必須特別小心。 下列程式碼慣例允許與 GSSAPI 型應用程式的互通性：

-   [Windows 相容名稱](#windows-compatible-names)
-   [驗證](#authentication)
-   [訊息完整性和隱私權](#message-integrity-and-privacy)

您可以在範例 \\ 安全性 SSPI GSS (SDK) 的平臺軟體發展工具組中找到範例程式碼 \\ \\ 。 此外，對等的 UNIX 範例會散佈在 MIT 和 Heimdal Kerberos 散發套件中，也就是 GSS 用戶端和伺服器。

## <a name="windows-compatible-names"></a>Windows-Compatible 名稱

GSSAPI 函式會使用稱為 gss \_ nt \_ 服務名稱的名稱格式， \_ 如 RFC 中所指定。 例如， sample@host.dom.com 是可在以 GSSAPI 為基礎的應用程式中使用的名稱。 Windows 作業系統無法辨識 gss \_ nt \_ 服務 \_ 名稱格式，而且必須使用完整的 [*服務主體名稱*](../secgloss/s-gly.md)（例如 sample/host.dom.com@REALM ）。

## <a name="authentication"></a>驗證

驗證通常會在用戶端與伺服器之間第一次設定連接時處理。 在此範例中，用戶端會使用 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) ，而伺服器則使用 GSSAPI。

**若要在 SSPI 用戶端中設定驗證**

1.  使用 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)取得輸出 [*認證*](../secgloss/c-gly.md)。
2.  使用 **gss 匯 \_ 入 \_ 名稱** 建立服務名稱 () ，並使用 gss 取得認證來取得輸入認證 **\_ \_**。
3.  使用 [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)取得要傳送至伺服器的驗證權杖。
4.  將權杖傳送到伺服器。

**在 GSSAPI 伺服器中設定驗證**

1.  從用戶端剖析訊息以解壓縮安全性權杖。 使用 **gss \_ accept \_ sec \_ 內容** 函式，將權杖傳遞為引數。
2.  從伺服器剖析訊息以解壓縮安全性權杖。 將此安全性權杖傳遞給 [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)。
3.  將回應權杖傳送給用戶端。

    **Gss \_ accept \_ sec \_ coNtext** 函數可以傳回您可以傳回給用戶端的權杖。

4.  如果需要繼續，請將回應權杖傳送給伺服器;否則，驗證的設定已完成。
5.  如果需要繼續，請等候來自用戶端的下一個權杖;否則，驗證的設定已完成。

## <a name="message-integrity-and-privacy"></a>訊息完整性和隱私權

大部分以 GSSAPI 為基礎的應用程式在傳送訊息之前，會先使用 **GSS \_ Wrap** 函數來簽署訊息。 相反地， **GSS \_** 解除包裝函數會驗證簽章。 **GSS \_「換行** 」適用于2.0 版的 API，現在已廣泛使用並以網際網路標準指定，以說明如何使用 GSSAPI 來為通訊協定新增安全性。 稍早，GSS **SignMessage** 和 **SealMessage** 函式是用於訊息 [*完整性*](../secgloss/i-gly.md) 和 [*隱私權*](../secgloss/p-gly.md)。 **GSS \_** 使用「會議旗標」引數的值所控制的隱私權，可將 Wrap 和 **GSS \_** 解除包裝用於完整性和隱私權 \_ 。

如果指定以 GSSAPI 為基礎的通訊協定使用 **gss \_ get \_ mic** 和 **gss \_ 驗證 \_ mic** 函式，正確的 SSPI 函式會是 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)。 請注意，當會議旗標設為零或使用 Gss wrap 時，MakeSignature 和 VerifySignature 將無法與 **gss \_ wrap** 互通 \_ **\_**。 這同樣適用于混合 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 僅針對簽章設定，而 **gss \_ 驗證 \_ mic**。

> [!Note]  
> 當針對呼叫 **gss \_ Wrap** 和 gss 解除包裝時，請勿 **使用 \_** [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)或 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)函數。

 

SSPI 等同于 **GSS \_ Wrap** 的 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) ，以提供完整性和隱私權。

下列範例顯示如何使用 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 來簽署將由 GSS 解除包裝所 **驗證 \_** 的資料。

在 SSPI 用戶端中：


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



在 GSSAPI 伺服器中：


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



相當於 GSS 解除包裝的 SSPI 是 [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)。 **\_** 以下範例顯示如何使用 **DecryptMessage (Kerberos)** 來解密以 **GSS \_ Wrap** 加密的資料。

在 GSSAPI 伺服器中：


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



在 SSPI 用戶端中：


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 

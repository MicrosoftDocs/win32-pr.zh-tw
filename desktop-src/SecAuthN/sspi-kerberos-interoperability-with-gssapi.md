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
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="a8bbd-103">SSPI/Kerberos 與 GSSAPI 的互通性</span><span class="sxs-lookup"><span data-stu-id="a8bbd-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="a8bbd-104">如果需要與 GSSAPI 的互通性，則在使用 [*Kerberos*](../secgloss/k-gly.md) [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 時必須特別小心。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="a8bbd-105">下列程式碼慣例允許與 GSSAPI 型應用程式的互通性：</span><span class="sxs-lookup"><span data-stu-id="a8bbd-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="a8bbd-106">Windows 相容名稱</span><span class="sxs-lookup"><span data-stu-id="a8bbd-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="a8bbd-107">驗證</span><span class="sxs-lookup"><span data-stu-id="a8bbd-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="a8bbd-108">訊息完整性和隱私權</span><span class="sxs-lookup"><span data-stu-id="a8bbd-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="a8bbd-109">您可以在範例 \\ 安全性 SSPI GSS (SDK) 的平臺軟體發展工具組中找到範例程式碼 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="a8bbd-110">此外，對等的 UNIX 範例會散佈在 MIT 和 Heimdal Kerberos 散發套件中，也就是 GSS 用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="a8bbd-111">Windows-Compatible 名稱</span><span class="sxs-lookup"><span data-stu-id="a8bbd-111">Windows-Compatible Names</span></span>

<span data-ttu-id="a8bbd-112">GSSAPI 函式會使用稱為 gss \_ nt \_ 服務名稱的名稱格式， \_ 如 RFC 中所指定。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="a8bbd-113">例如， sample@host.dom.com 是可在以 GSSAPI 為基礎的應用程式中使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="a8bbd-114">Windows 作業系統無法辨識 gss \_ nt \_ 服務 \_ 名稱格式，而且必須使用完整的 [*服務主體名稱*](../secgloss/s-gly.md)（例如 sample/host.dom.com@REALM ）。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="a8bbd-115">驗證</span><span class="sxs-lookup"><span data-stu-id="a8bbd-115">Authentication</span></span>

<span data-ttu-id="a8bbd-116">驗證通常會在用戶端與伺服器之間第一次設定連接時處理。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="a8bbd-117">在此範例中，用戶端會使用 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) ，而伺服器則使用 GSSAPI。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="a8bbd-118">**若要在 SSPI 用戶端中設定驗證**</span><span class="sxs-lookup"><span data-stu-id="a8bbd-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="a8bbd-119">使用 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)取得輸出 [*認證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="a8bbd-120">使用 **gss 匯 \_ 入 \_ 名稱** 建立服務名稱 () ，並使用 gss 取得認證來取得輸入認證 **\_ \_**。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="a8bbd-121">使用 [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)取得要傳送至伺服器的驗證權杖。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="a8bbd-122">將權杖傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-122">Send the token to the server.</span></span>

<span data-ttu-id="a8bbd-123">**在 GSSAPI 伺服器中設定驗證**</span><span class="sxs-lookup"><span data-stu-id="a8bbd-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="a8bbd-124">從用戶端剖析訊息以解壓縮安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="a8bbd-125">使用 **gss \_ accept \_ sec \_ 內容** 函式，將權杖傳遞為引數。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="a8bbd-126">從伺服器剖析訊息以解壓縮安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="a8bbd-127">將此安全性權杖傳遞給 [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="a8bbd-128">將回應權杖傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-128">Send a response token to the client.</span></span>

    <span data-ttu-id="a8bbd-129">**Gss \_ accept \_ sec \_ coNtext** 函數可以傳回您可以傳回給用戶端的權杖。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="a8bbd-130">如果需要繼續，請將回應權杖傳送給伺服器;否則，驗證的設定已完成。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="a8bbd-131">如果需要繼續，請等候來自用戶端的下一個權杖;否則，驗證的設定已完成。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="a8bbd-132">訊息完整性和隱私權</span><span class="sxs-lookup"><span data-stu-id="a8bbd-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="a8bbd-133">大部分以 GSSAPI 為基礎的應用程式在傳送訊息之前，會先使用 **GSS \_ Wrap** 函數來簽署訊息。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="a8bbd-134">相反地， **GSS \_** 解除包裝函數會驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="a8bbd-135">**GSS \_「換行** 」適用于2.0 版的 API，現在已廣泛使用並以網際網路標準指定，以說明如何使用 GSSAPI 來為通訊協定新增安全性。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="a8bbd-136">稍早，GSS **SignMessage** 和 **SealMessage** 函式是用於訊息 [*完整性*](../secgloss/i-gly.md) 和 [*隱私權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="a8bbd-137">**GSS \_** 使用「會議旗標」引數的值所控制的隱私權，可將 Wrap 和 **GSS \_** 解除包裝用於完整性和隱私權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="a8bbd-138">如果指定以 GSSAPI 為基礎的通訊協定使用 **gss \_ get \_ mic** 和 **gss \_ 驗證 \_ mic** 函式，正確的 SSPI 函式會是 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="a8bbd-139">請注意，當會議旗標設為零或使用 Gss wrap 時，MakeSignature 和 VerifySignature 將無法與 **gss \_ wrap** 互通 \_ **\_**。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="a8bbd-140">這同樣適用于混合 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 僅針對簽章設定，而 **gss \_ 驗證 \_ mic**。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="a8bbd-141">當針對呼叫 **gss \_ Wrap** 和 gss 解除包裝時，請勿 **使用 \_** [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)或 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)函數。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="a8bbd-142">SSPI 等同于 **GSS \_ Wrap** 的 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) ，以提供完整性和隱私權。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="a8bbd-143">下列範例顯示如何使用 [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 來簽署將由 GSS 解除包裝所 **驗證 \_** 的資料。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="a8bbd-144">在 SSPI 用戶端中：</span><span class="sxs-lookup"><span data-stu-id="a8bbd-144">In the SSPI client:</span></span>


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



<span data-ttu-id="a8bbd-145">在 GSSAPI 伺服器中：</span><span class="sxs-lookup"><span data-stu-id="a8bbd-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="a8bbd-146">相當於 GSS 解除包裝的 SSPI 是 [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)。 **\_**</span><span class="sxs-lookup"><span data-stu-id="a8bbd-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="a8bbd-147">以下範例顯示如何使用 **DecryptMessage (Kerberos)** 來解密以 **GSS \_ Wrap** 加密的資料。</span><span class="sxs-lookup"><span data-stu-id="a8bbd-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="a8bbd-148">在 GSSAPI 伺服器中：</span><span class="sxs-lookup"><span data-stu-id="a8bbd-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="a8bbd-149">在 SSPI 用戶端中：</span><span class="sxs-lookup"><span data-stu-id="a8bbd-149">In the SSPI client:</span></span>


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



 

 

---
description: 使用 Schannel 來解密訊息。
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage (Schannel) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689699"
---
# <a name="decryptmessage-schannel-function"></a><span data-ttu-id="c45f2-103">DecryptMessage (Schannel) 函數</span><span class="sxs-lookup"><span data-stu-id="c45f2-103">DecryptMessage (Schannel) function</span></span>

<span data-ttu-id="c45f2-104">**DecryptMessage (Schannel)** 函數會解密訊息。</span><span class="sxs-lookup"><span data-stu-id="c45f2-104">The **DecryptMessage (Schannel)** function decrypts a message.</span></span> <span data-ttu-id="c45f2-105">某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c45f2-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>


<span data-ttu-id="c45f2-106">此函式也會與安全通道 [*安全性支援提供者*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) 搭配使用 (SSP) ，向訊息寄件者發出重新協商的要求 (重做連接屬性) 或連接關閉。</span><span class="sxs-lookup"><span data-stu-id="c45f2-106">This function is also used with the Schannel [*security support provider*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) (SSP) to signal a request from a message sender for a renegotiation (redo) of the connection attributes or for a shutdown of the connection.</span></span>

> [!Note]  
> <span data-ttu-id="c45f2-107">如果有一個執行緒正在進行加密，而另一個執行緒正在解密，則可以同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY)的兩個不同執行緒呼叫 [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)和 **DECRYPTMESSAGE (schannel)** (SSPI) 內容。</span><span class="sxs-lookup"><span data-stu-id="c45f2-107">[**EncryptMessage (Schannel)**](encryptmessage--schannel.md) and **DecryptMessage (Schannel)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="c45f2-108">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="c45f2-108">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>


## <a name="syntax"></a><span data-ttu-id="c45f2-109">語法</span><span class="sxs-lookup"><span data-stu-id="c45f2-109">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="c45f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="c45f2-110">Parameters</span></span>

<span data-ttu-id="c45f2-111">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-111">*phContext* \[in\]</span></span>


<span data-ttu-id="c45f2-112">用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="c45f2-112">A handle to the [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) to be used to decrypt the message.</span></span>

<span data-ttu-id="c45f2-113">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-113">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="c45f2-114">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c45f2-114">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="c45f2-115">在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="c45f2-115">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="c45f2-116">其中一個類型可能屬於之 SECBUFFER 資料類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c45f2-116">One of these may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="c45f2-117">該緩衝區包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="c45f2-117">That buffer contains the encrypted message.</span></span> <span data-ttu-id="c45f2-118">加密的訊息會就地解密，並覆寫其緩衝區的原始內容。</span><span class="sxs-lookup"><span data-stu-id="c45f2-118">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="c45f2-119">使用安全通道 SSP 搭配非連接導向的內容時，在輸入上，結構必須包含四個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="c45f2-119">When using the Schannel SSP with contexts that are not connection oriented, on input, the structure must contain four [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="c45f2-120">只有一個緩衝區必須是之 SECBUFFER 資料類型 \_ ，而且包含已加密的訊息（已就地解密）。</span><span class="sxs-lookup"><span data-stu-id="c45f2-120">Exactly one buffer must be of type SECBUFFER\_DATA and contain an encrypted message, which is decrypted in place.</span></span> <span data-ttu-id="c45f2-121">其餘的緩衝區會用於輸出，而且必須是之 SECBUFFER 空的型別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c45f2-121">The remaining buffers are used for output and must be of type SECBUFFER\_EMPTY.</span></span> <span data-ttu-id="c45f2-122">若為連線導向的內容，則 \_ 必須提供之 secbuffer 資料類型緩衝區（如 nonconnection 導向內容所述）。</span><span class="sxs-lookup"><span data-stu-id="c45f2-122">For connection-oriented contexts, a SECBUFFER\_DATA type buffer must be supplied, as noted for nonconnection-oriented contexts.</span></span> <span data-ttu-id="c45f2-123">此外， \_ 也必須提供包含安全性權杖的第二個之 secbuffer TOKEN 類型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c45f2-123">Additionally, a second SECBUFFER\_TOKEN type buffer that contains a security token must also be supplied.</span></span>

<span data-ttu-id="c45f2-124">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-124">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="c45f2-125">傳輸應用程式所預期的序號（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c45f2-125">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="c45f2-126">如果傳輸應用程式不會維護序號，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="c45f2-126">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="c45f2-127">使用 Schannel SSP 時，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="c45f2-127">When using the Schannel SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="c45f2-128">Schannel SSP 不會使用序號。</span><span class="sxs-lookup"><span data-stu-id="c45f2-128">The Schannel SSP does not use sequence numbers.</span></span>

<span data-ttu-id="c45f2-129">*pfQOP* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-129">*pfQOP* \[out\]</span></span>

<span data-ttu-id="c45f2-130">**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。</span><span class="sxs-lookup"><span data-stu-id="c45f2-130">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="c45f2-131">使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c45f2-131">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

<span data-ttu-id="c45f2-132">此參數可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="c45f2-132">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="c45f2-133">值</span><span class="sxs-lookup"><span data-stu-id="c45f2-133">Value</span></span></th><th><span data-ttu-id="c45f2-134">意義</span><span class="sxs-lookup"><span data-stu-id="c45f2-134">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="c45f2-135"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c45f2-135"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="c45f2-136">訊息未加密，但產生的是標頭或結尾。</span><span class="sxs-lookup"><span data-stu-id="c45f2-136">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="c45f2-137">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="c45f2-137">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="c45f2-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="c45f2-138">Return value</span></span>

<span data-ttu-id="c45f2-139">如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c45f2-139">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="c45f2-140">如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c45f2-140">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="c45f2-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c45f2-141">Return code</span></span>                     | <span data-ttu-id="c45f2-142">Description</span><span class="sxs-lookup"><span data-stu-id="c45f2-142">Description</span></span>                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45f2-143">**SEC \_ E \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="c45f2-143">**SEC\_E\_INVALID\_HANDLE**</span></span>     | <span data-ttu-id="c45f2-144">在 *phCoNtext* 參數中指定了不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="c45f2-144">A context handle that is not valid was specified in the *phContext* parameter.</span></span> <span data-ttu-id="c45f2-145">搭配 Schannel SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="c45f2-145">Used with the Schannel SSP.</span></span>     |
| <span data-ttu-id="c45f2-146">**SEC \_ E \_ 不正確 \_ 權杖**</span><span class="sxs-lookup"><span data-stu-id="c45f2-146">**SEC\_E\_INVALID\_TOKEN**</span></span>      | <span data-ttu-id="c45f2-147">緩衝區的類型錯誤，或找不到之 SECBUFFER 資料類型的緩衝區 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c45f2-147">The buffers are of the wrong type or no buffer of type SECBUFFER\_DATA was found.</span></span> <span data-ttu-id="c45f2-148">搭配 Schannel SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="c45f2-148">Used with the Schannel SSP.</span></span>  |
| <span data-ttu-id="c45f2-149">**秒 \_ E \_ 修改的訊息 \_**</span><span class="sxs-lookup"><span data-stu-id="c45f2-149">**SEC\_E\_MESSAGE\_ALTERED**</span></span>    | <span data-ttu-id="c45f2-150">已更改訊息。</span><span class="sxs-lookup"><span data-stu-id="c45f2-150">The message has been altered.</span></span> <span data-ttu-id="c45f2-151">搭配 Schannel SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="c45f2-151">Used with the Schannel SSP.</span></span>                                                      |
| <span data-ttu-id="c45f2-152">**SEC \_ E \_ \_ \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="c45f2-152">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="c45f2-153">未以正確的順序接收訊息。</span><span class="sxs-lookup"><span data-stu-id="c45f2-153">The message was not received in the correct sequence.</span></span>                                                          |
| <span data-ttu-id="c45f2-154">**秒 \_ - \_ 內容已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="c45f2-154">**SEC\_I\_CONTEXT\_EXPIRED**</span></span>    | <span data-ttu-id="c45f2-155">訊息寄件者已使用連接完成，並已起始關機。</span><span class="sxs-lookup"><span data-stu-id="c45f2-155">The message sender has finished using the connection and has initiated a shutdown.</span></span> <span data-ttu-id="c45f2-156">如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。</span><span class="sxs-lookup"><span data-stu-id="c45f2-156">For information about initiating or recognizing a shutdown, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span> <span data-ttu-id="c45f2-157">搭配 Schannel SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="c45f2-157">Used with the Schannel SSP.</span></span> |
| <span data-ttu-id="c45f2-158">**秒 \_ 我重新 \_ 協商**</span><span class="sxs-lookup"><span data-stu-id="c45f2-158">**SEC\_I\_RENEGOTIATE**</span></span>         | <span data-ttu-id="c45f2-159">遠端物件需要新的交握序列，或應用程式剛起始關機。</span><span class="sxs-lookup"><span data-stu-id="c45f2-159">The remote party requires a new handshake sequence or the application has just initiated a shutdown.</span></span> <span data-ttu-id="c45f2-160">返回協調迴圈，並呼叫 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md) 或 [**InitializeSecurityCoNtext (**](initializesecuritycontext--schannel.md)安全通道) ，傳遞從 DecryptMessage SECBUFFER_EXTRA 傳回的 () 。</span><span class="sxs-lookup"><span data-stu-id="c45f2-160">Return to the negotiation loop and call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) or [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md), pass SECBUFFER_EXTRA returned from DecryptMessage().</span></span> <span data-ttu-id="c45f2-161">Schannel 核心模式不支援重新協商。</span><span class="sxs-lookup"><span data-stu-id="c45f2-161">Renegotiation is not supported for Schannel kernel mode.</span></span> <span data-ttu-id="c45f2-162">呼叫端應該忽略此傳回值或關閉連接。</span><span class="sxs-lookup"><span data-stu-id="c45f2-162">The caller should either ignore this return value or shut down the connection.</span></span> <span data-ttu-id="c45f2-163">如果忽略此值，可能是因為用戶端或伺服器會關閉連接。</span><span class="sxs-lookup"><span data-stu-id="c45f2-163">If the value is ignored, either the client or the server might shut down the connection as a result.</span></span> |


## <a name="remarks"></a><span data-ttu-id="c45f2-164">備註</span><span class="sxs-lookup"><span data-stu-id="c45f2-164">Remarks</span></span>

<span data-ttu-id="c45f2-165">有時候，應用程式會從遠端方讀取資料、嘗試使用 **DecryptMessage (schannel)** 將資料解密，併發現 **DecryptMessage (Schannel)** 成功，但輸出緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="c45f2-165">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Schannel)**, and discover that **DecryptMessage (Schannel)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="c45f2-166">這是正常行為，而且應用程式必須能夠處理它。</span><span class="sxs-lookup"><span data-stu-id="c45f2-166">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="c45f2-167">當您使用安全通道 SSP 時， [**DecryptMessage (一般)**](decryptmessage--general.md) 函數會傳回 \_ \_ \_ 當訊息寄件者關閉連線時，我內容已過期的秒數。</span><span class="sxs-lookup"><span data-stu-id="c45f2-167">When you use the Schannel SSP, the [**DecryptMessage (General)**](decryptmessage--general.md) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="c45f2-168">如需初始化或辨識關機的相關資訊，請參閱 [關閉 Schannel](shutting-down-an-schannel-connection.md)連線。</span><span class="sxs-lookup"><span data-stu-id="c45f2-168">For information about initiating or recognizing a shutdown, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="c45f2-169">如果您使用 TLS 1.0，您可能需要多次呼叫此函式，並在每次呼叫時調整輸入緩衝區來解密整個訊息。</span><span class="sxs-lookup"><span data-stu-id="c45f2-169">If you are using TLS 1.0, you may need to call this function multiple times, adjusting the input buffer on each call, to decrypt a whole message.</span></span>


<span data-ttu-id="c45f2-170">**DecryptMessage (Schannel)** 函式會 \_ \_ 在訊息寄件者想要重新協商 ([*安全性內容*](../secgloss/s-gly.md)) 的連線時，傳回每秒重新協商。</span><span class="sxs-lookup"><span data-stu-id="c45f2-170">The **DecryptMessage (Schannel)** function returns SEC\_I\_RENEGOTIATE when the message sender wants to renegotiate the connection ([*security context*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="c45f2-171">應用程式會藉由呼叫 [**AcceptSecurityCoNtext (Schannel)**](acceptsecuritycontext--schannel.md) (server 端) 或 [**InitializeSecurityCoNtext (schannel)**](initializesecuritycontext--schannel.md) (用戶端) 並傳遞從 DecryptMessage SECBUFFER_EXTRA 傳回的 () ，來處理要求的重新協商。</span><span class="sxs-lookup"><span data-stu-id="c45f2-171">An application handles a requested renegotiation by calling [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (server side) or [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) (client side) and pass SECBUFFER_EXTRA returned from DecryptMessage().</span></span> <span data-ttu-id="c45f2-172">在這個初始呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。</span><span class="sxs-lookup"><span data-stu-id="c45f2-172">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span> <span data-ttu-id="c45f2-173">如需詳細資訊，請參閱 [建立 Schannel 安全性內容](creating-an-schannel-security-context.md)。</span><span class="sxs-lookup"><span data-stu-id="c45f2-173">For more information, see [Creating an Schannel Security Context](creating-an-schannel-security-context.md).</span></span>


## <a name="requirements"></a><span data-ttu-id="c45f2-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="c45f2-174">Requirements</span></span>

| <span data-ttu-id="c45f2-175">需求</span><span class="sxs-lookup"><span data-stu-id="c45f2-175">Requirement</span></span> | <span data-ttu-id="c45f2-176">值</span><span class="sxs-lookup"><span data-stu-id="c45f2-176">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="c45f2-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c45f2-177">Minimum supported client</span></span> | <span data-ttu-id="c45f2-178">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-178">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="c45f2-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c45f2-179">Minimum supported server</span></span> | <span data-ttu-id="c45f2-180">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c45f2-180">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="c45f2-181">標頭</span><span class="sxs-lookup"><span data-stu-id="c45f2-181">Header</span></span>                   | <span data-ttu-id="c45f2-182">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="c45f2-182">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="c45f2-183">程式庫</span><span class="sxs-lookup"><span data-stu-id="c45f2-183">Library</span></span>                  | <span data-ttu-id="c45f2-184">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="c45f2-184">Secur32.lib</span></span>                               |
| <span data-ttu-id="c45f2-185">DLL</span><span class="sxs-lookup"><span data-stu-id="c45f2-185">DLL</span></span>                      | <span data-ttu-id="c45f2-186">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="c45f2-186">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="c45f2-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c45f2-187">See also</span></span>

- [<span data-ttu-id="c45f2-188">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="c45f2-188">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="c45f2-189">**EncryptMessage (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="c45f2-189">**EncryptMessage (Schannel)**</span></span>](encryptmessage--schannel.md)
- [<span data-ttu-id="c45f2-190">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="c45f2-190">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="c45f2-191">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="c45f2-191">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

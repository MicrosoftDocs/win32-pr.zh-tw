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
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="7fc50-103">EncryptMessage (Digest) 函數</span><span class="sxs-lookup"><span data-stu-id="7fc50-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="7fc50-104">**EncryptMessage (Digest)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7fc50-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="7fc50-105">**EncryptMessage (Digest)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="7fc50-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="7fc50-106">**EncryptMessage (Digest)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7fc50-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="7fc50-107">某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="7fc50-108">此函式僅以 SASL 機制的形式提供。</span><span class="sxs-lookup"><span data-stu-id="7fc50-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="7fc50-109">您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 **EncryptMessage (Digest)** 和 [**DECRYPTMESSAGE (digest)**](decryptmessage--digest.md) (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。</span><span class="sxs-lookup"><span data-stu-id="7fc50-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="7fc50-110">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="7fc50-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7fc50-111">語法</span><span class="sxs-lookup"><span data-stu-id="7fc50-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="7fc50-112">參數</span><span class="sxs-lookup"><span data-stu-id="7fc50-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc50-113">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc50-114">用來加密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="7fc50-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="7fc50-115">*fQOP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc50-116">指出保護品質的封裝特定旗標。</span><span class="sxs-lookup"><span data-stu-id="7fc50-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="7fc50-117">[*安全性套件*](../secgloss/s-gly.md)可以使用此參數來啟用 [*密碼編譯演算法*](../secgloss/c-gly.md)的選取。</span><span class="sxs-lookup"><span data-stu-id="7fc50-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="7fc50-118">使用摘要 SSP 時，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="7fc50-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7fc50-119">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc50-120">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7fc50-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="7fc50-121">在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="7fc50-122">該緩衝區包含要加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="7fc50-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="7fc50-123">訊息會就地加密，覆寫結構的原始內容。</span><span class="sxs-lookup"><span data-stu-id="7fc50-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="7fc50-124">此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7fc50-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="7fc50-125">包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，它是從 [**QUERYCONTEXTATTRIBUTES (Digest)**](querycontextattributes--digest.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="7fc50-126">使用摘要 SSP 時，必須有類型為之 SECBUFFER \_ 填補或 SEC 緩衝區資料的第二個緩衝區， \_ \_ 才能保存簽章資訊。 [](../secgloss/d-gly.md#_security_digital_signature_gly)</span><span class="sxs-lookup"><span data-stu-id="7fc50-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="7fc50-127">若要取得輸出緩衝區的大小，請呼叫 [**QueryCoNtextAttributes (Digest)**](querycontextattributes--digest.md) 函數，並指定 SECPKG \_ ATTR \_ 大小。</span><span class="sxs-lookup"><span data-stu-id="7fc50-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="7fc50-128">函數會傳回 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) 結構。</span><span class="sxs-lookup"><span data-stu-id="7fc50-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="7fc50-129">輸出緩衝區的大小是 **cbMaxSignature** 和 **cbBlockSize** 成員中值的總和。</span><span class="sxs-lookup"><span data-stu-id="7fc50-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="7fc50-130">不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="7fc50-131">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc50-132">傳輸應用程式指派給訊息的序號。</span><span class="sxs-lookup"><span data-stu-id="7fc50-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="7fc50-133">如果傳輸應用程式不會維護序號，此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="7fc50-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="7fc50-134">使用摘要 SSP 時，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="7fc50-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="7fc50-135">摘要 SSP 會在內部管理順序編號。</span><span class="sxs-lookup"><span data-stu-id="7fc50-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc50-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fc50-136">Return value</span></span>

<span data-ttu-id="7fc50-137">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7fc50-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="7fc50-138">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7fc50-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="7fc50-139">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7fc50-139">Return code</span></span>                                                                                                    | <span data-ttu-id="7fc50-140">Description</span><span class="sxs-lookup"><span data-stu-id="7fc50-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fc50-141"><dt>**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="7fc50-142">輸出緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="7fc50-142">The output buffer is too small.</span></span> <span data-ttu-id="7fc50-143">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7fc50-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="7fc50-144"><dt>**SEC \_ E \_ 內容已 \_ 過期**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="7fc50-145">應用程式參考的內容已關閉。</span><span class="sxs-lookup"><span data-stu-id="7fc50-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="7fc50-146">正確撰寫的應用程式應該不會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7fc50-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="7fc50-147"><dt>**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="7fc50-148">不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7fc50-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="7fc50-149"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="7fc50-150">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="7fc50-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="7fc50-151"><dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="7fc50-152">在 *phCoNtext* 參數中指定了不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="7fc50-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="7fc50-153"><dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="7fc50-154">找不 \_ 到之 secbuffer 資料類型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7fc50-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7fc50-155"><dt>**\_ \_ \_ 不支援 SEC E \_ QOP**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="7fc50-156">[*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7fc50-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fc50-157">備註</span><span class="sxs-lookup"><span data-stu-id="7fc50-157">Remarks</span></span>

<span data-ttu-id="7fc50-158">**EncryptMessage (Digest)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="7fc50-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="7fc50-159">如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。</span><span class="sxs-lookup"><span data-stu-id="7fc50-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="7fc50-160">包含這項資訊可防止重新執行、插入和隱藏訊息。</span><span class="sxs-lookup"><span data-stu-id="7fc50-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="7fc50-161">[*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。</span><span class="sxs-lookup"><span data-stu-id="7fc50-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="7fc50-162">當您使用摘要 SSP 時，請呼叫 [**QueryCoNtextAttributes (Digest)**](querycontextattributes--digest.md) 函數並指定 SECPKG ATTR 大小，以取得輸出緩衝區的 \_ 大小 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="7fc50-163">函數會傳回 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) 結構。</span><span class="sxs-lookup"><span data-stu-id="7fc50-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="7fc50-164">輸出緩衝區的大小是 **cbMaxSignature** 和 **cbBlockSize** 成員中值的總和。</span><span class="sxs-lookup"><span data-stu-id="7fc50-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="7fc50-165">您必須依照顯示的順序提供這些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7fc50-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="7fc50-166">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="7fc50-166">Buffer type</span></span>                           | <span data-ttu-id="7fc50-167">Description</span><span class="sxs-lookup"><span data-stu-id="7fc50-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc50-168">之 SECBUFFER \_ 資料流程 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="7fc50-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="7fc50-169">內部使用。</span><span class="sxs-lookup"><span data-stu-id="7fc50-169">Used internally.</span></span> <span data-ttu-id="7fc50-170">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="7fc50-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="7fc50-171">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="7fc50-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="7fc50-172">包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7fc50-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="7fc50-173">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="7fc50-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="7fc50-174">內部使用。</span><span class="sxs-lookup"><span data-stu-id="7fc50-174">Used internally.</span></span> <span data-ttu-id="7fc50-175">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="7fc50-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="7fc50-176">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="7fc50-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="7fc50-177">內部使用。</span><span class="sxs-lookup"><span data-stu-id="7fc50-177">Used internally.</span></span> <span data-ttu-id="7fc50-178">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="7fc50-178">No initialization required.</span></span> <span data-ttu-id="7fc50-179">大小可以是零。</span><span class="sxs-lookup"><span data-stu-id="7fc50-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="7fc50-180">為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。</span><span class="sxs-lookup"><span data-stu-id="7fc50-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="7fc50-181">**WINDOWS XP：** 此函數也稱為 **SealMessage**。</span><span class="sxs-lookup"><span data-stu-id="7fc50-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="7fc50-182">應用程式現在應該只使用 **EncryptMessage (Digest)** 。</span><span class="sxs-lookup"><span data-stu-id="7fc50-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc50-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fc50-183">Requirements</span></span>



| <span data-ttu-id="7fc50-184">需求</span><span class="sxs-lookup"><span data-stu-id="7fc50-184">Requirement</span></span> | <span data-ttu-id="7fc50-185">值</span><span class="sxs-lookup"><span data-stu-id="7fc50-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc50-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fc50-186">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc50-187">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7fc50-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fc50-188">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc50-189">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fc50-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7fc50-190">標頭</span><span class="sxs-lookup"><span data-stu-id="7fc50-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc50-191"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="7fc50-192">程式庫</span><span class="sxs-lookup"><span data-stu-id="7fc50-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="7fc50-193"><dt>Secur32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="7fc50-194">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc50-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fc50-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fc50-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="7fc50-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc50-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc50-197">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="7fc50-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="7fc50-198">**AcceptSecurityCoNtext (摘要)**</span><span class="sxs-lookup"><span data-stu-id="7fc50-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="7fc50-199">**DecryptMessage (摘要)**</span><span class="sxs-lookup"><span data-stu-id="7fc50-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="7fc50-200">**InitializeSecurityCoNtext (摘要)**</span><span class="sxs-lookup"><span data-stu-id="7fc50-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="7fc50-201">**QueryCoNtextAttributes (摘要)**</span><span class="sxs-lookup"><span data-stu-id="7fc50-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="7fc50-202">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="7fc50-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="7fc50-203">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="7fc50-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

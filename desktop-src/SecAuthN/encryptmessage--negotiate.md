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
# <a name="encryptmessage-negotiate-function"></a><span data-ttu-id="b6ce1-103">EncryptMessage (Negotiate) 函數</span><span class="sxs-lookup"><span data-stu-id="b6ce1-103">EncryptMessage (Negotiate) function</span></span>

<span data-ttu-id="b6ce1-104">**EncryptMessage (Negotiate)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-104">The **EncryptMessage (Negotiate)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="b6ce1-105">**EncryptMessage (Negotiate)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-105">**EncryptMessage (Negotiate)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="b6ce1-106">**EncryptMessage (Negotiate)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-106">The **EncryptMessage (Negotiate)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="b6ce1-107">某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="b6ce1-108">您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 **EncryptMessage (Negotiate)** 和 [**DECRYPTMESSAGE (negotiate)**](decryptmessage--negotiate.md) (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-108">**EncryptMessage (Negotiate)** and [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="b6ce1-109">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ce1-110">語法</span><span class="sxs-lookup"><span data-stu-id="b6ce1-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="b6ce1-111">參數</span><span class="sxs-lookup"><span data-stu-id="b6ce1-111">Parameters</span></span>

<span data-ttu-id="b6ce1-112">*phCoNtext* \[用於 \] 加密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-112">*phContext* \[in\] A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

<span data-ttu-id="b6ce1-113">*fQOP* \[在 \] 指出保護品質的封裝特定旗標中。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-113">*fQOP* \[in\] Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="b6ce1-114">[*安全性套件*](../secgloss/s-gly.md)可以使用此參數來啟用 [*密碼編譯演算法*](../secgloss/c-gly.md)的選取。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-114">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b6ce1-115">此參數可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-115">This parameter can be the following flag.</span></span>

| <span data-ttu-id="b6ce1-116">值</span><span class="sxs-lookup"><span data-stu-id="b6ce1-116">Value</span></span>                  | <span data-ttu-id="b6ce1-117">意義</span><span class="sxs-lookup"><span data-stu-id="b6ce1-117">Meaning</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b6ce1-118">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="b6ce1-118">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="b6ce1-119">產生標頭或結尾，但不加密訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-119">Produce a header or trailer but do not encrypt the message.</span></span> |

> [!NOTE]
> <span data-ttu-id="b6ce1-120">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-120">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

<span data-ttu-id="b6ce1-121">*pMessage* \[在中，輸出 \] [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-121">*pMessage* \[in, out\] A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b6ce1-122">在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-122">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="b6ce1-123">該緩衝區包含要加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-123">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="b6ce1-124">訊息會就地加密，覆寫結構的原始內容。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-124">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="b6ce1-125">此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-125">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="b6ce1-126">包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，這是從 [**QUERYCONTEXTATTRIBUTES (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-126">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="b6ce1-127">不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-127">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

<span data-ttu-id="b6ce1-128">*MessageSeqNo* \[\]傳輸應用程式指派給訊息的序號。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-128">*MessageSeqNo* \[in\] The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="b6ce1-129">如果傳輸應用程式不會維護序號，此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-129">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6ce1-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6ce1-130">Return value</span></span>

<span data-ttu-id="b6ce1-131">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-131">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b6ce1-132">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-132">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="b6ce1-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6ce1-133">Return code</span></span>                         | <span data-ttu-id="b6ce1-134">Description</span><span class="sxs-lookup"><span data-stu-id="b6ce1-134">Description</span></span>                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ce1-135">**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-135">**SEC\_E\_BUFFER\_TOO\_SMALL**</span></span>      | <span data-ttu-id="b6ce1-136">輸出緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-136">The output buffer is too small.</span></span> <span data-ttu-id="b6ce1-137">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-137">For more information, see Remarks.</span></span>                                                                   |
| <span data-ttu-id="b6ce1-138">**SEC \_ E \_ 內容已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-138">**SEC\_E\_CONTEXT\_EXPIRED**</span></span>        | <span data-ttu-id="b6ce1-139">應用程式參考的內容已關閉。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-139">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="b6ce1-140">正確撰寫的應用程式應該不會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-140">A properly written application should not receive this error.</span></span> |
| <span data-ttu-id="b6ce1-141">**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-141">**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</span></span> | <span data-ttu-id="b6ce1-142">不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-142">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                |
| <span data-ttu-id="b6ce1-143">**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-143">**SEC\_E\_INSUFFICIENT\_MEMORY**</span></span>    | <span data-ttu-id="b6ce1-144">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-144">There is not enough memory available to complete the requested action.</span></span>                                                               |
| <span data-ttu-id="b6ce1-145">**SEC \_ E \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-145">**SEC\_E\_INVALID\_HANDLE**</span></span>         | <span data-ttu-id="b6ce1-146">在 *phCoNtext* 參數中指定了不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-146">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                       |
| <span data-ttu-id="b6ce1-147">**SEC \_ E \_ 不正確 \_ 權杖**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-147">**SEC\_E\_INVALID\_TOKEN**</span></span>          | <span data-ttu-id="b6ce1-148">找不 \_ 到之 secbuffer 資料類型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-148">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                            |
| <span data-ttu-id="b6ce1-149">**\_ \_ \_ 不支援 SEC E \_ QOP**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-149">**SEC\_E\_QOP\_NOT\_SUPPORTED**</span></span>     | <span data-ttu-id="b6ce1-150">[*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-150">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span>             |

## <a name="remarks"></a><span data-ttu-id="b6ce1-151">備註</span><span class="sxs-lookup"><span data-stu-id="b6ce1-151">Remarks</span></span>

<span data-ttu-id="b6ce1-152">**EncryptMessage (Negotiate)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-152">The **EncryptMessage (Negotiate)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="b6ce1-153">如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-153">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="b6ce1-154">包含這項資訊可防止重新執行、插入和隱藏訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-154">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="b6ce1-155">[*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-155">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="b6ce1-156">您必須依照顯示的順序提供這些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-156">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="b6ce1-157">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="b6ce1-157">Buffer type</span></span>                | <span data-ttu-id="b6ce1-158">Description</span><span class="sxs-lookup"><span data-stu-id="b6ce1-158">Description</span></span>                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ce1-159">之 SECBUFFER \_ 資料流程 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="b6ce1-159">SECBUFFER\_STREAM\_HEADER</span></span>  | <span data-ttu-id="b6ce1-160">內部使用。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-160">Used internally.</span></span> <span data-ttu-id="b6ce1-161">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-161">No initialization required.</span></span>                                                |
| <span data-ttu-id="b6ce1-162">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="b6ce1-162">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="b6ce1-163">包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-163">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="b6ce1-164">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="b6ce1-164">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="b6ce1-165">內部使用。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-165">Used internally.</span></span> <span data-ttu-id="b6ce1-166">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-166">No initialization required.</span></span>                                                |
| <span data-ttu-id="b6ce1-167">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="b6ce1-167">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="b6ce1-168">內部使用。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-168">Used internally.</span></span> <span data-ttu-id="b6ce1-169">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-169">No initialization required.</span></span> <span data-ttu-id="b6ce1-170">大小可以是零。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-170">Size can be zero.</span></span>                              |

<span data-ttu-id="b6ce1-171">為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-171">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="b6ce1-172">**WINDOWS XP：** 此函數也稱為 **SealMessage**。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-172">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="b6ce1-173">應用程式現在應該只使用 **EncryptMessage (Negotiate)** 。</span><span class="sxs-lookup"><span data-stu-id="b6ce1-173">Applications should now use **EncryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ce1-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6ce1-174">Requirements</span></span>

| <span data-ttu-id="b6ce1-175">需求</span><span class="sxs-lookup"><span data-stu-id="b6ce1-175">Requirement</span></span> | <span data-ttu-id="b6ce1-176">值</span><span class="sxs-lookup"><span data-stu-id="b6ce1-176">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="b6ce1-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6ce1-177">Minimum supported client</span></span> | <span data-ttu-id="b6ce1-178">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ce1-178">Windows XP \[desktop apps only\]</span></span>                |
| <span data-ttu-id="b6ce1-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6ce1-179">Minimum supported server</span></span> | <span data-ttu-id="b6ce1-180">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ce1-180">Windows Server 2003 \[desktop apps only\]</span></span>       |
| <span data-ttu-id="b6ce1-181">標頭</span><span class="sxs-lookup"><span data-stu-id="b6ce1-181">Header</span></span>                   | <span data-ttu-id="b6ce1-182">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="b6ce1-182">Sspi.h (include Security.h)</span></span>                     |
| <span data-ttu-id="b6ce1-183">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6ce1-183">Library</span></span>                  | <span data-ttu-id="b6ce1-184">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="b6ce1-184">Secur32.lib</span></span>                                     |
| <span data-ttu-id="b6ce1-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b6ce1-185">DLL</span></span>                      | <span data-ttu-id="b6ce1-186">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="b6ce1-186">Secur32.dll</span></span>                                     |

## <a name="see-also"></a><span data-ttu-id="b6ce1-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ce1-187">See also</span></span>

- [<span data-ttu-id="b6ce1-188">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="b6ce1-188">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="b6ce1-189">**AcceptSecurityCoNtext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-189">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
- [<span data-ttu-id="b6ce1-190">**DecryptMessage (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-190">**DecryptMessage (Negotiate)**</span></span>](decryptmessage--negotiate.md)
- [<span data-ttu-id="b6ce1-191">**InitializeSecurityCoNtext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-191">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
- [<span data-ttu-id="b6ce1-192">**QueryCoNtextAttributes (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-192">**QueryContextAttributes (Negotiate)**</span></span>](querycontextattributes--negotiate.md)
- [<span data-ttu-id="b6ce1-193">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-193">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="b6ce1-194">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="b6ce1-194">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

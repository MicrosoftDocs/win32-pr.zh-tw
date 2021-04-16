---
description: 使用 Kerberos 加密訊息以提供隱私權。
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: EncryptMessage (Kerberos) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194528"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="950b6-103">EncryptMessage (Kerberos) 函數</span><span class="sxs-lookup"><span data-stu-id="950b6-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="950b6-104">**EncryptMessage (Kerberos)** 函數會加密訊息以提供 [*隱私權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="950b6-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="950b6-105">**EncryptMessage (Kerberos)** 可讓應用程式在所選機制支援的 [*密碼編譯演算法*](../secgloss/c-gly.md) 之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="950b6-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="950b6-106">**EncryptMessage (Kerberos)** 函數會使用內容控制碼所參考的 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="950b6-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="950b6-107">某些封裝沒有要加密或解密的訊息，而是提供可檢查的完整性 [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="950b6-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="950b6-108">當某個執行緒正在進行加密，而另一個執行緒正在解密時，可同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒呼叫 **EncryptMessage (Kerberos)** 和 [**DECRYPTMESSAGE (kerberos)**](decryptmessage--kerberos.md) (SSPI) 內容。</span><span class="sxs-lookup"><span data-stu-id="950b6-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="950b6-109">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="950b6-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="950b6-110">語法</span><span class="sxs-lookup"><span data-stu-id="950b6-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="950b6-111">參數</span><span class="sxs-lookup"><span data-stu-id="950b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950b6-112">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="950b6-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950b6-113">用來加密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="950b6-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="950b6-114">*fQOP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="950b6-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950b6-115">指出保護品質的封裝特定旗標。</span><span class="sxs-lookup"><span data-stu-id="950b6-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="950b6-116">[*安全性套件*](../secgloss/s-gly.md)可以使用此參數來啟用 [*密碼編譯演算法*](../secgloss/c-gly.md)的選取。</span><span class="sxs-lookup"><span data-stu-id="950b6-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="950b6-117">此參數可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="950b6-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="950b6-118">值</span><span class="sxs-lookup"><span data-stu-id="950b6-118">Value</span></span></th><th><span data-ttu-id="950b6-119">意義</span><span class="sxs-lookup"><span data-stu-id="950b6-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="950b6-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="950b6-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="950b6-121">產生標頭或結尾，但不加密訊息。</span><span class="sxs-lookup"><span data-stu-id="950b6-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="950b6-122">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="950b6-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="950b6-123">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="950b6-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="950b6-124">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="950b6-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="950b6-125">在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="950b6-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="950b6-126">該緩衝區包含要加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="950b6-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="950b6-127">訊息會就地加密，覆寫結構的原始內容。</span><span class="sxs-lookup"><span data-stu-id="950b6-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="950b6-128">此函數不會處理具有之 SECBUFFER \_ READONLY 屬性的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="950b6-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="950b6-129">包含訊息的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構長度不能大於 **cbMaximumMessage**，這是從 [**QUERYCONTEXTATTRIBUTES (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ 資料流程大小) 函式取得 \_ 。</span><span class="sxs-lookup"><span data-stu-id="950b6-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="950b6-130">不使用 SSL 的應用程式必須提供類型[](/windows/win32/api/sspi/ns-sspi-secbuffer)之 secbuffer 填補的之 secbuffer \_ 。</span><span class="sxs-lookup"><span data-stu-id="950b6-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="950b6-131">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="950b6-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950b6-132">傳輸應用程式指派給訊息的序號。</span><span class="sxs-lookup"><span data-stu-id="950b6-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="950b6-133">如果傳輸應用程式不會維護序號，此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="950b6-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950b6-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="950b6-134">Return value</span></span>

<span data-ttu-id="950b6-135">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="950b6-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="950b6-136">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="950b6-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="950b6-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="950b6-137">Return code</span></span>                                                                                                    | <span data-ttu-id="950b6-138">Description</span><span class="sxs-lookup"><span data-stu-id="950b6-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="950b6-139"><dt>**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="950b6-140">輸出緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="950b6-140">The output buffer is too small.</span></span> <span data-ttu-id="950b6-141">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="950b6-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="950b6-142"><dt>**SEC \_ E \_ 內容已 \_ 過期**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="950b6-143">應用程式參考的內容已關閉。</span><span class="sxs-lookup"><span data-stu-id="950b6-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="950b6-144">正確撰寫的應用程式應該不會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="950b6-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="950b6-145"><dt>**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="950b6-146">不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="950b6-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="950b6-147"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="950b6-148">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="950b6-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="950b6-149"><dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="950b6-150">在 *phCoNtext* 參數中指定了不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="950b6-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="950b6-151"><dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="950b6-152">找不 \_ 到之 secbuffer 資料類型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="950b6-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="950b6-153"><dt>**\_ \_ \_ 不支援 SEC E \_ QOP**</dt></span><span class="sxs-lookup"><span data-stu-id="950b6-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="950b6-154">[*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="950b6-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="950b6-155">備註</span><span class="sxs-lookup"><span data-stu-id="950b6-155">Remarks</span></span>

<span data-ttu-id="950b6-156">**EncryptMessage (Kerberos)** 函數會根據訊息和 [*安全性內容*](../secgloss/s-gly.md)中的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="950b6-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="950b6-157">如果傳輸應用程式建立支援序列偵測的 [*安全性內容*](../secgloss/s-gly.md) ，而呼叫端提供序號，則函式會將此資訊包含在加密的訊息中。</span><span class="sxs-lookup"><span data-stu-id="950b6-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="950b6-158">包含這項資訊可防止重新執行、插入和隱藏訊息。</span><span class="sxs-lookup"><span data-stu-id="950b6-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="950b6-159">[*安全性封裝*](../secgloss/s-gly.md)會合並從傳輸應用程式中傳遞的序號。</span><span class="sxs-lookup"><span data-stu-id="950b6-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="950b6-160">您必須依照顯示的順序提供這些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="950b6-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="950b6-161">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="950b6-161">Buffer type</span></span>                           | <span data-ttu-id="950b6-162">Description</span><span class="sxs-lookup"><span data-stu-id="950b6-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="950b6-163">之 SECBUFFER \_ 資料流程 \_ 標頭<</span><span class="sxs-lookup"><span data-stu-id="950b6-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="950b6-164">內部使用。</span><span class="sxs-lookup"><span data-stu-id="950b6-164">Used internally.</span></span> <span data-ttu-id="950b6-165">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="950b6-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="950b6-166">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="950b6-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="950b6-167">包含要加密的 [*純文字*](../secgloss/s-gly.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="950b6-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="950b6-168">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="950b6-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="950b6-169">內部使用。</span><span class="sxs-lookup"><span data-stu-id="950b6-169">Used internally.</span></span> <span data-ttu-id="950b6-170">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="950b6-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="950b6-171">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="950b6-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="950b6-172">內部使用。</span><span class="sxs-lookup"><span data-stu-id="950b6-172">Used internally.</span></span> <span data-ttu-id="950b6-173">不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="950b6-173">No initialization required.</span></span> <span data-ttu-id="950b6-174">大小可以是零。</span><span class="sxs-lookup"><span data-stu-id="950b6-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="950b6-175">為了達到最佳效能，應該從連續的記憶體配置 *pMessage* 結構。</span><span class="sxs-lookup"><span data-stu-id="950b6-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="950b6-176">**WINDOWS XP：** 此函數也稱為 **SealMessage**。</span><span class="sxs-lookup"><span data-stu-id="950b6-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="950b6-177">應用程式現在應該只使用 **EncryptMessage (Kerberos)** 。</span><span class="sxs-lookup"><span data-stu-id="950b6-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="950b6-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="950b6-178">Requirements</span></span>

| <span data-ttu-id="950b6-179">需求</span><span class="sxs-lookup"><span data-stu-id="950b6-179">Requirement</span></span> | <span data-ttu-id="950b6-180">值</span><span class="sxs-lookup"><span data-stu-id="950b6-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="950b6-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="950b6-181">Minimum supported client</span></span> | <span data-ttu-id="950b6-182">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="950b6-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="950b6-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="950b6-183">Minimum supported server</span></span> | <span data-ttu-id="950b6-184">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="950b6-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="950b6-185">標頭</span><span class="sxs-lookup"><span data-stu-id="950b6-185">Header</span></span>                   | <span data-ttu-id="950b6-186">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="950b6-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="950b6-187">程式庫</span><span class="sxs-lookup"><span data-stu-id="950b6-187">Library</span></span>                  | <span data-ttu-id="950b6-188">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="950b6-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="950b6-189">DLL</span><span class="sxs-lookup"><span data-stu-id="950b6-189">DLL</span></span>                      | <span data-ttu-id="950b6-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="950b6-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="950b6-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="950b6-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950b6-192">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="950b6-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="950b6-193">**AcceptSecurityCoNtext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="950b6-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="950b6-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="950b6-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="950b6-195">**InitializeSecurityCoNtext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="950b6-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="950b6-196">**QueryCoNtextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="950b6-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="950b6-197">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="950b6-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="950b6-198">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="950b6-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

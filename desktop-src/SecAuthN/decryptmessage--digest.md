---
description: 使用 Digest 來解密訊息。
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage (Digest) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5363a5efc79d78c9c88e4a817c1c341e0e0f9c02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469213"
---
# <a name="decryptmessage-digest-function"></a><span data-ttu-id="0af6d-103">DecryptMessage (Digest) 函數</span><span class="sxs-lookup"><span data-stu-id="0af6d-103">DecryptMessage (Digest) function</span></span>

<span data-ttu-id="0af6d-104">**DecryptMessage (Digest)** 函數會解密訊息。</span><span class="sxs-lookup"><span data-stu-id="0af6d-104">The **DecryptMessage (Digest)** function decrypts a message.</span></span> <span data-ttu-id="0af6d-105">某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="0af6d-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

<span data-ttu-id="0af6d-106">摘要式 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 為用戶端與伺服器之間交換的訊息提供加密和解密機密性（僅限 SASL 機制）。</span><span class="sxs-lookup"><span data-stu-id="0af6d-106">The Digest [*security support provider*](../secgloss/s-gly.md) (SSP) provides encryption and decryption confidentiality for messages exchanged between client and server as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="0af6d-107">您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 [**EncryptMessage (Digest)**](encryptmessage--digest.md)和 **DECRYPTMESSAGE (digest)** (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。</span><span class="sxs-lookup"><span data-stu-id="0af6d-107">[**EncryptMessage (Digest)**](encryptmessage--digest.md) and **DecryptMessage (Digest)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="0af6d-108">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="0af6d-108">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af6d-109">語法</span><span class="sxs-lookup"><span data-stu-id="0af6d-109">Syntax</span></span>

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="0af6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0af6d-110">Parameters</span></span>

<span data-ttu-id="0af6d-111">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-111">*phContext* \[in\]</span></span>

<span data-ttu-id="0af6d-112">用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="0af6d-112">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="0af6d-113">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-113">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="0af6d-114">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0af6d-114">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="0af6d-115">在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="0af6d-115">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="0af6d-116">其中至少一個必須是之 SECBUFFER \_ 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0af6d-116">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="0af6d-117">該緩衝區包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="0af6d-117">That buffer contains the encrypted message.</span></span> <span data-ttu-id="0af6d-118">加密的訊息會就地解密，並覆寫其緩衝區的原始內容。</span><span class="sxs-lookup"><span data-stu-id="0af6d-118">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="0af6d-119">使用摘要 SSP 時，在輸入上，結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="0af6d-119">When using the Digest SSP, on input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="0af6d-120">其中一個型別必須是之 SECBUFFER \_ DATA 或之 secbuffer \_ STREAM，而且必須包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="0af6d-120">One of these must be of type SECBUFFER\_DATA or SECBUFFER\_STREAM, and it must contain the encrypted message.</span></span>

<span data-ttu-id="0af6d-121">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-121">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="0af6d-122">傳輸應用程式所預期的序號（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0af6d-122">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="0af6d-123">如果傳輸應用程式不會維護序號，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="0af6d-123">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="0af6d-124">使用摘要 SSP 時，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="0af6d-124">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="0af6d-125">摘要 SSP 會在內部管理順序編號。</span><span class="sxs-lookup"><span data-stu-id="0af6d-125">The Digest SSP manages sequence numbering internally.</span></span>

<span data-ttu-id="0af6d-126">*pfQOP* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-126">*pfQOP* \[out\]</span></span>

<span data-ttu-id="0af6d-127">**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。</span><span class="sxs-lookup"><span data-stu-id="0af6d-127">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="0af6d-128">此參數可以是下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="0af6d-128">This parameter can be one of the following flags.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="0af6d-129">值</span><span class="sxs-lookup"><span data-stu-id="0af6d-129">Value</span></span></th><th><span data-ttu-id="0af6d-130">意義</span><span class="sxs-lookup"><span data-stu-id="0af6d-130">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="0af6d-131"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0af6d-131"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="0af6d-132">訊息未加密，但產生的是標頭或結尾。</span><span class="sxs-lookup"><span data-stu-id="0af6d-132">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="0af6d-133">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="0af6d-133">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <span data-ttu-id="0af6d-134"><dt><strong>SIGN_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0af6d-134"><dt><strong>SIGN_ONLY</strong> </dt> </span></span></dl></td><td><span data-ttu-id="0af6d-135">使用摘要 SSP 時，當 [*安全性內容*](../secgloss/s-gly.md) 設定 [*為僅驗證*](../secgloss/s-gly.md) 簽章時，請使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="0af6d-135">When using the Digest SSP, use this flag when the [*security context*](../secgloss/s-gly.md) is set to verify the [*signature*](../secgloss/s-gly.md) only.</span></span> <span data-ttu-id="0af6d-136">如需詳細資訊，請參閱 [保護品質](quality-of-protection.md)。</span><span class="sxs-lookup"><span data-stu-id="0af6d-136">For more information, see [Quality of Protection](quality-of-protection.md).</span></span><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="0af6d-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="0af6d-137">Return value</span></span>

<span data-ttu-id="0af6d-138">如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0af6d-138">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="0af6d-139">如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0af6d-139">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="0af6d-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0af6d-140">Return code</span></span>                         | <span data-ttu-id="0af6d-141">Description</span><span class="sxs-lookup"><span data-stu-id="0af6d-141">Description</span></span>                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af6d-142">**SEC \_ E \_ 緩衝區 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="0af6d-142">**SEC\_E\_BUFFER\_TOO\_SMALL**</span></span>      | <span data-ttu-id="0af6d-143">訊息緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="0af6d-143">The message buffer is too small.</span></span> <span data-ttu-id="0af6d-144">搭配摘要 SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="0af6d-144">Used with the Digest SSP.</span></span>                                                                                                                   |
| <span data-ttu-id="0af6d-145">**SEC \_ E \_ 加密 \_ 系統 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="0af6d-145">**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</span></span> | <span data-ttu-id="0af6d-146">不支援為 [*安全性內容*](../secgloss/s-gly.md)選擇的 [*加密*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="0af6d-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span> <span data-ttu-id="0af6d-147">搭配摘要 SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="0af6d-147">Used with the Digest SSP.</span></span>                                                                                       |
| <span data-ttu-id="0af6d-148">**SEC \_ E \_ 未完成 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="0af6d-148">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span>     | <span data-ttu-id="0af6d-149">輸入緩衝區中的資料不完整。</span><span class="sxs-lookup"><span data-stu-id="0af6d-149">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="0af6d-150">應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (Digest)**](decryptmessage--digest.md) 。</span><span class="sxs-lookup"><span data-stu-id="0af6d-150">The application needs to read more data from the server and call [**DecryptMessage (Digest)**](decryptmessage--digest.md) again.</span></span> |
| <span data-ttu-id="0af6d-151">**SEC \_ E \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0af6d-151">**SEC\_E\_INVALID\_HANDLE**</span></span>         | <span data-ttu-id="0af6d-152">在 *phCoNtext* 參數中指定了不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="0af6d-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span> <span data-ttu-id="0af6d-153">搭配摘要 SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="0af6d-153">Used with the Digest SSP.</span></span>                                                                     |
| <span data-ttu-id="0af6d-154">**秒 \_ E \_ 修改的訊息 \_**</span><span class="sxs-lookup"><span data-stu-id="0af6d-154">**SEC\_E\_MESSAGE\_ALTERED**</span></span>        | <span data-ttu-id="0af6d-155">已更改訊息。</span><span class="sxs-lookup"><span data-stu-id="0af6d-155">The message has been altered.</span></span> <span data-ttu-id="0af6d-156">搭配摘要 SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="0af6d-156">Used with the Digest SSP.</span></span>                                                                                                                      |
| <span data-ttu-id="0af6d-157">**SEC \_ E \_ \_ \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="0af6d-157">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>       | <span data-ttu-id="0af6d-158">未以正確的順序接收訊息。</span><span class="sxs-lookup"><span data-stu-id="0af6d-158">The message was not received in the correct sequence.</span></span>                                                                                                                        |
| <span data-ttu-id="0af6d-159">**\_ \_ \_ 不支援 SEC E \_ QOP**</span><span class="sxs-lookup"><span data-stu-id="0af6d-159">**SEC\_E\_QOP\_NOT\_SUPPORTED**</span></span>     | <span data-ttu-id="0af6d-160">[*安全性內容*](../secgloss/s-gly.md)不支援機密性和 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="0af6d-160">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0af6d-161">搭配摘要 SSP 使用。</span><span class="sxs-lookup"><span data-stu-id="0af6d-161">Used with the Digest SSP.</span></span>                           |

## <a name="remarks"></a><span data-ttu-id="0af6d-162">備註</span><span class="sxs-lookup"><span data-stu-id="0af6d-162">Remarks</span></span>

<span data-ttu-id="0af6d-163">有時候，應用程式會從遠端方讀取資料、嘗試使用 **DecryptMessage (digest)** 將資料解密，併發現 **DecryptMessage (Digest)** 成功，但輸出緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="0af6d-163">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Digest)**, and discover that **DecryptMessage (Digest)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="0af6d-164">這是正常行為，而且應用程式必須能夠處理它。</span><span class="sxs-lookup"><span data-stu-id="0af6d-164">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="0af6d-165">**WINDOWS XP：** 此函數也稱為 **UnsealMessage**。</span><span class="sxs-lookup"><span data-stu-id="0af6d-165">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="0af6d-166">應用程式現在應該只使用 **DecryptMessage (Digest)** 。</span><span class="sxs-lookup"><span data-stu-id="0af6d-166">Applications should now use **DecryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af6d-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="0af6d-167">Requirements</span></span>

| <span data-ttu-id="0af6d-168">需求</span><span class="sxs-lookup"><span data-stu-id="0af6d-168">Requirement</span></span> | <span data-ttu-id="0af6d-169">值</span><span class="sxs-lookup"><span data-stu-id="0af6d-169">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="0af6d-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0af6d-170">Minimum supported client</span></span> | <span data-ttu-id="0af6d-171">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-171">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="0af6d-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0af6d-172">Minimum supported server</span></span> | <span data-ttu-id="0af6d-173">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af6d-173">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="0af6d-174">標頭</span><span class="sxs-lookup"><span data-stu-id="0af6d-174">Header</span></span>                   | <span data-ttu-id="0af6d-175">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="0af6d-175">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="0af6d-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="0af6d-176">Library</span></span>                  | <span data-ttu-id="0af6d-177">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="0af6d-177">Secur32.lib</span></span>                               |
| <span data-ttu-id="0af6d-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0af6d-178">DLL</span></span>                      | <span data-ttu-id="0af6d-179">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="0af6d-179">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="0af6d-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0af6d-180">See also</span></span>

- [<span data-ttu-id="0af6d-181">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="0af6d-181">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="0af6d-182">**EncryptMessage (摘要)**</span><span class="sxs-lookup"><span data-stu-id="0af6d-182">**EncryptMessage (Digest)**</span></span>](encryptmessage--digest.md)
- [<span data-ttu-id="0af6d-183">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="0af6d-183">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="0af6d-184">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="0af6d-184">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

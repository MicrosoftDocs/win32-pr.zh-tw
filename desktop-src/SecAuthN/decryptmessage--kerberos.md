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
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="54794-103">DecryptMessage (Kerberos) 函數</span><span class="sxs-lookup"><span data-stu-id="54794-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="54794-104">**DecryptMessage (Kerberos)** 函數會解密訊息。</span><span class="sxs-lookup"><span data-stu-id="54794-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="54794-105">某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="54794-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="54794-106">當某個執行緒正在進行加密，而另一個執行緒正在解密時，可同時從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒呼叫 [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)和 **DECRYPTMESSAGE (kerberos)** (SSPI) 內容。</span><span class="sxs-lookup"><span data-stu-id="54794-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="54794-107">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="54794-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="54794-108">語法</span><span class="sxs-lookup"><span data-stu-id="54794-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="54794-109">參數</span><span class="sxs-lookup"><span data-stu-id="54794-109">Parameters</span></span>

<span data-ttu-id="54794-110">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54794-110">*phContext* \[in\]</span></span>

<span data-ttu-id="54794-111">用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="54794-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="54794-112">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="54794-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="54794-113">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="54794-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="54794-114">在輸入時，此結構會參考一或多個類型為之 SECBUFFER 資料的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="54794-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="54794-115">緩衝區包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="54794-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="54794-116">加密的訊息會就地解密，並覆寫其緩衝區的原始內容。</span><span class="sxs-lookup"><span data-stu-id="54794-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="54794-117">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54794-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="54794-118">傳輸應用程式所預期的序號（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="54794-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="54794-119">如果傳輸應用程式不會維護序號，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="54794-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="54794-120">*pfQOP* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54794-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="54794-121">**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。</span><span class="sxs-lookup"><span data-stu-id="54794-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="54794-122">此參數可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="54794-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="54794-123">值</span><span class="sxs-lookup"><span data-stu-id="54794-123">Value</span></span>                  | <span data-ttu-id="54794-124">意義</span><span class="sxs-lookup"><span data-stu-id="54794-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54794-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="54794-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="54794-126">他的訊息未加密，但產生的是標頭或結尾。</span><span class="sxs-lookup"><span data-stu-id="54794-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="54794-127">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="54794-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="54794-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="54794-128">Return value</span></span>

<span data-ttu-id="54794-129">如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="54794-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="54794-130">如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="54794-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="54794-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="54794-131">Return code</span></span>                     | <span data-ttu-id="54794-132">Description</span><span class="sxs-lookup"><span data-stu-id="54794-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54794-133">**SEC \_ E \_ 未完成 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="54794-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="54794-134">輸入緩衝區中的資料不完整。</span><span class="sxs-lookup"><span data-stu-id="54794-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="54794-135">應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) 。</span><span class="sxs-lookup"><span data-stu-id="54794-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="54794-136">**SEC \_ E \_ \_ \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="54794-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="54794-137">未以正確的順序接收訊息。</span><span class="sxs-lookup"><span data-stu-id="54794-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="54794-138">備註</span><span class="sxs-lookup"><span data-stu-id="54794-138">Remarks</span></span>

<span data-ttu-id="54794-139">有時候，應用程式會從遠端方讀取資料、使用 **DecryptMessage (kerberos)** 嘗試將它解密，併發現 **DecryptMessage (Kerberos)** 成功，但輸出緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="54794-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="54794-140">這是正常行為，而且應用程式必須能夠處理它。</span><span class="sxs-lookup"><span data-stu-id="54794-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="54794-141">如需與 GSSAPI 交互操作的詳細資訊，請參閱 [SSPI/Kerberos 與 GSSAPI 的互通性](sspi-kerberos-interoperability-with-gssapi.md)。</span><span class="sxs-lookup"><span data-stu-id="54794-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="54794-142">**WINDOWS XP：** 此函數也稱為 **UnsealMessage**。</span><span class="sxs-lookup"><span data-stu-id="54794-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="54794-143">應用程式現在應該只使用 **DecryptMessage (Kerberos)** 。</span><span class="sxs-lookup"><span data-stu-id="54794-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="54794-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="54794-144">Requirements</span></span>

| <span data-ttu-id="54794-145">需求</span><span class="sxs-lookup"><span data-stu-id="54794-145">Requirement</span></span> | <span data-ttu-id="54794-146">值</span><span class="sxs-lookup"><span data-stu-id="54794-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="54794-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54794-147">Minimum supported client</span></span> | <span data-ttu-id="54794-148">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54794-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="54794-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54794-149">Minimum supported server</span></span> | <span data-ttu-id="54794-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54794-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="54794-151">標頭</span><span class="sxs-lookup"><span data-stu-id="54794-151">Header</span></span>                   | <span data-ttu-id="54794-152">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="54794-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="54794-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="54794-153">Library</span></span>                  | <span data-ttu-id="54794-154">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="54794-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="54794-155">DLL</span><span class="sxs-lookup"><span data-stu-id="54794-155">DLL</span></span>                      | <span data-ttu-id="54794-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="54794-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="54794-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54794-157">See also</span></span>

- [<span data-ttu-id="54794-158">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="54794-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="54794-159">**EncryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="54794-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="54794-160">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="54794-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="54794-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="54794-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

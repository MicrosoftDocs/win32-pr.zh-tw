---
description: 使用 NTLM 解密訊息。
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: DecryptMessage (NTLM) 函數
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977975"
---
# <a name="decryptmessage-ntlm-function"></a><span data-ttu-id="ee51d-103">DecryptMessage (NTLM) 函數</span><span class="sxs-lookup"><span data-stu-id="ee51d-103">DecryptMessage (NTLM) function</span></span>

<span data-ttu-id="ee51d-104">**DecryptMessage (NTLM)** 函數會解密訊息。</span><span class="sxs-lookup"><span data-stu-id="ee51d-104">The **DecryptMessage (NTLM)** function decrypts a message.</span></span> <span data-ttu-id="ee51d-105">某些封裝不會將訊息加密和解密，而是會執行並檢查完整性 [*雜湊*](../secgloss/h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="ee51d-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="ee51d-106">您可以從單一 [*安全性支援提供者介面*](../secgloss/s-gly.md)的兩個不同執行緒同時呼叫 [**EncryptMessage (Ntlm)**](encryptmessage--ntlm.md)和 **DECRYPTMESSAGE (ntlm)** (SSPI) 內容（如果一個執行緒正在加密，另一個執行緒正在解密）。</span><span class="sxs-lookup"><span data-stu-id="ee51d-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) and **DecryptMessage (NTLM)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="ee51d-107">如果有一個以上的執行緒加密，或有多個執行緒正在解密，則每個執行緒都應該取得唯一的內容。</span><span class="sxs-lookup"><span data-stu-id="ee51d-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee51d-108">語法</span><span class="sxs-lookup"><span data-stu-id="ee51d-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="ee51d-109">參數</span><span class="sxs-lookup"><span data-stu-id="ee51d-109">Parameters</span></span>

<span data-ttu-id="ee51d-110">*phCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-110">*phContext* \[in\]</span></span>

<span data-ttu-id="ee51d-111">用來解密訊息的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee51d-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="ee51d-112">*pMessage* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="ee51d-113">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ee51d-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="ee51d-114">在輸入時，此結構會參考一或多個 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="ee51d-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="ee51d-115">其中至少一個必須是之 SECBUFFER \_ 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ee51d-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="ee51d-116">該緩衝區包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="ee51d-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="ee51d-117">加密的訊息會就地解密，並覆寫其緩衝區的原始內容。</span><span class="sxs-lookup"><span data-stu-id="ee51d-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="ee51d-118">*MessageSeqNo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="ee51d-119">傳輸應用程式所預期的序號（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="ee51d-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="ee51d-120">如果傳輸應用程式不會維護序號，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="ee51d-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="ee51d-121">*pfQOP* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="ee51d-122">**ULONG** 類型變數的指標，此變數會接收指定保護品質的特定封裝旗標。</span><span class="sxs-lookup"><span data-stu-id="ee51d-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="ee51d-123">此參數可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="ee51d-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="ee51d-124">值</span><span class="sxs-lookup"><span data-stu-id="ee51d-124">Value</span></span></th><th><span data-ttu-id="ee51d-125">意義</span><span class="sxs-lookup"><span data-stu-id="ee51d-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="ee51d-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee51d-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="ee51d-127">訊息未加密，但產生的是標頭或結尾。</span><span class="sxs-lookup"><span data-stu-id="ee51d-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="ee51d-128">KERB_WRAP_NO_ENCRYPT 具有相同的值和相同的意義。</span><span class="sxs-lookup"><span data-stu-id="ee51d-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="ee51d-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee51d-129">Return value</span></span>

<span data-ttu-id="ee51d-130">如果函式驗證以正確的順序接收訊息，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ee51d-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="ee51d-131">如果函數無法解密訊息，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee51d-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="ee51d-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee51d-132">Return code</span></span>                     | <span data-ttu-id="ee51d-133">Description</span><span class="sxs-lookup"><span data-stu-id="ee51d-133">Description</span></span>                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee51d-134">**SEC \_ E \_ 未完成 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="ee51d-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="ee51d-135">輸入緩衝區中的資料不完整。</span><span class="sxs-lookup"><span data-stu-id="ee51d-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="ee51d-136">應用程式需要從伺服器讀取更多資料，並再次呼叫 [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee51d-136">The application needs to read more data from the server and call [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) again.</span></span> |
| <span data-ttu-id="ee51d-137">**SEC \_ E \_ \_ \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="ee51d-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="ee51d-138">未以正確的順序接收訊息。</span><span class="sxs-lookup"><span data-stu-id="ee51d-138">The message was not received in the correct sequence.</span></span>                                                                                                                    |

## <a name="remarks"></a><span data-ttu-id="ee51d-139">備註</span><span class="sxs-lookup"><span data-stu-id="ee51d-139">Remarks</span></span>

<span data-ttu-id="ee51d-140">有時候，應用程式會從遠端方讀取資料、使用 **DecryptMessage (NTLM)** 嘗試將它解密，併發現 **DecryptMessage (NTLM)** 成功，但輸出緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="ee51d-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (NTLM)**, and discover that **DecryptMessage (NTLM)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="ee51d-141">這是正常行為，而且應用程式必須能夠處理它。</span><span class="sxs-lookup"><span data-stu-id="ee51d-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="ee51d-142">**WINDOWS XP：** 此函數也稱為 **UnsealMessage**。</span><span class="sxs-lookup"><span data-stu-id="ee51d-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="ee51d-143">應用程式現在應該只使用 **DecryptMessage (NTLM)** 。</span><span class="sxs-lookup"><span data-stu-id="ee51d-143">Applications should now use **DecryptMessage (NTLM)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee51d-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee51d-144">Requirements</span></span>

| <span data-ttu-id="ee51d-145">需求</span><span class="sxs-lookup"><span data-stu-id="ee51d-145">Requirement</span></span> | <span data-ttu-id="ee51d-146">值</span><span class="sxs-lookup"><span data-stu-id="ee51d-146">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="ee51d-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee51d-147">Minimum supported client</span></span> | <span data-ttu-id="ee51d-148">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="ee51d-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee51d-149">Minimum supported server</span></span> | <span data-ttu-id="ee51d-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee51d-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="ee51d-151">標頭</span><span class="sxs-lookup"><span data-stu-id="ee51d-151">Header</span></span>                   | <span data-ttu-id="ee51d-152">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="ee51d-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="ee51d-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee51d-153">Library</span></span>                  | <span data-ttu-id="ee51d-154">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="ee51d-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="ee51d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ee51d-155">DLL</span></span>                      | <span data-ttu-id="ee51d-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="ee51d-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="ee51d-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee51d-157">See also</span></span>

- [<span data-ttu-id="ee51d-158">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="ee51d-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="ee51d-159">**EncryptMessage (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="ee51d-159">**EncryptMessage (NTLM)**</span></span>](encryptmessage--ntlm.md)
- [<span data-ttu-id="ee51d-160">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="ee51d-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="ee51d-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="ee51d-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

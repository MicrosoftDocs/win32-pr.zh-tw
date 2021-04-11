---
description: 時間戳記指定的主體，並支援在多個簽章上設定時間戳記。
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111973"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="a5028-103">SignerTimeStampEx3 函式</span><span class="sxs-lookup"><span data-stu-id="a5028-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="a5028-104">**SignerTimeStampEx3** 函數時間會將指定的主旨戳記，並支援在多個簽章上設定時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a5028-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="a5028-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a5028-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="a5028-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="a5028-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a5028-107">語法</span><span class="sxs-lookup"><span data-stu-id="a5028-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="a5028-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5028-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5028-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5028-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-110">指定要產生之時間戳記類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="a5028-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="a5028-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a5028-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="a5028-112">這些值都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="a5028-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5028-113">值</span><span class="sxs-lookup"><span data-stu-id="a5028-113">Value</span></span></th>
<th><span data-ttu-id="a5028-114">意義</span><span class="sxs-lookup"><span data-stu-id="a5028-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="a5028-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a5028-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a5028-116">指定 Authenticode 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a5028-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a5028-117">Authenticode 不再是慣用的時間戳記類型。</span><span class="sxs-lookup"><span data-stu-id="a5028-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="a5028-118">未來可能會移除 Authenticode 時間戳記的支援。</span><span class="sxs-lookup"><span data-stu-id="a5028-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="a5028-119">建議您改用 RFC 3161。</span><span class="sxs-lookup"><span data-stu-id="a5028-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="a5028-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a5028-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a5028-121">指定符合 RFC 3161 規範的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a5028-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="a5028-122">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5028-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-123">指定將加入時間戳記的簽章序號。</span><span class="sxs-lookup"><span data-stu-id="a5028-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="a5028-124">如果這個值為零 (0) ，外部簽章將會加上時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a5028-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-125">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5028-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-126">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。</span><span class="sxs-lookup"><span data-stu-id="a5028-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-127">*pwszHttpTimeStamp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5028-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-128">以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="a5028-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-129">*pszAlgorithmOid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5028-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-130">雜湊演算法，用於執行符合 RFC 3161 規範的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a5028-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="a5028-131">Authenticode 時間戳記會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="a5028-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-132">*psRequest* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a5028-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a5028-133">Optional.</span></span> <span data-ttu-id="a5028-134">[**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="a5028-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="a5028-135">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a5028-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-136">*pSipData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a5028-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-137">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a5028-137">Optional.</span></span> <span data-ttu-id="a5028-138">以其他資料的形式傳遞至 [*主體介面封裝*](../secgloss/s-gly.md) 的32位值 (SIP) 函式。</span><span class="sxs-lookup"><span data-stu-id="a5028-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="a5028-139">此參數的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="a5028-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="a5028-140">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a5028-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-141">*ppSignerCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a5028-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a5028-142">Optional.</span></span> <span data-ttu-id="a5028-143">包含已簽署 BLOB 之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標位址。</span><span class="sxs-lookup"><span data-stu-id="a5028-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="a5028-144">當您完成使用 **簽署者 \_ 內容** 結構時，請呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="a5028-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-145">*pCryptoPolicy* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a5028-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5028-146">如果存在，則為憑證 [**強式 \_ \_ 簽署 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) 結構的指標，其中包含用來檢查強式簽章的參數。</span><span class="sxs-lookup"><span data-stu-id="a5028-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="a5028-147">時間戳記必須通過此密碼編譯原則。</span><span class="sxs-lookup"><span data-stu-id="a5028-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="a5028-148">*保存*</span><span class="sxs-lookup"><span data-stu-id="a5028-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="a5028-149">保留的。</span><span class="sxs-lookup"><span data-stu-id="a5028-149">Reserved.</span></span> <span data-ttu-id="a5028-150">這個值必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a5028-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5028-151">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5028-151">Return value</span></span>

<span data-ttu-id="a5028-152">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a5028-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="a5028-153">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a5028-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="a5028-154">此函式所傳回的可能錯誤碼包括（但不限於）下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5028-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="a5028-155">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="a5028-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5028-156">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5028-156">Return code</span></span></th>
<th><span data-ttu-id="a5028-157">Description</span><span class="sxs-lookup"><span data-stu-id="a5028-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="a5028-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a5028-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a5028-159">下列情況可能會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="a5028-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="a5028-160">您必須設定<em>dwFlags</em>參數的<strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong>或<strong>SIGNER_TIMESTAMP_RFC3161</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a5028-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="a5028-161"><em>保留</em>的參數必須是<strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="a5028-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="a5028-162">如果您在<em>dwFlags</em>參數中設定<strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong>旗標，則必須將<em>dwIndex</em>參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="a5028-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a5028-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5028-163">Requirements</span></span>



| <span data-ttu-id="a5028-164">需求</span><span class="sxs-lookup"><span data-stu-id="a5028-164">Requirement</span></span> | <span data-ttu-id="a5028-165">值</span><span class="sxs-lookup"><span data-stu-id="a5028-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5028-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5028-166">Minimum supported client</span></span><br/> | <span data-ttu-id="a5028-167">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5028-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a5028-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5028-168">Minimum supported server</span></span><br/> | <span data-ttu-id="a5028-169">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5028-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5028-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a5028-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5028-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5028-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5028-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5028-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5028-173">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="a5028-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="a5028-174">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="a5028-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="a5028-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="a5028-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 

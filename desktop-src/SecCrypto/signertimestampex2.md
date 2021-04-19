---
description: 時間戳記指定的主體，並選擇性地傳回 \_ 包含 BLOB 指標之簽署者內容結構的指標。 您可以使用此函式來執行 x.509 公開金鑰基礎結構、RFC 3161&\# 8211; 符合規範的時間戳記。
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975855"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="1c31d-104">SignerTimeStampEx2 函式</span><span class="sxs-lookup"><span data-stu-id="1c31d-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="1c31d-105">**SignerTimeStampEx2** 函式時間會為指定的主旨加上戳記，並選擇性地將指標傳回至包含 [*BLOB*](../secgloss/b-gly.md)指標的 [**簽署者 \_ 內容**](signer-context.md)結構。</span><span class="sxs-lookup"><span data-stu-id="1c31d-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="1c31d-106">您可以使用此函式來執行 x.509 公開金鑰基礎結構、RFC 3161 相容的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1c31d-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="1c31d-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c31d-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="1c31d-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="1c31d-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1c31d-109">語法</span><span class="sxs-lookup"><span data-stu-id="1c31d-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="1c31d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c31d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c31d-111">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-112">值，指定要產生的時間戳記類型。</span><span class="sxs-lookup"><span data-stu-id="1c31d-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="1c31d-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1c31d-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="1c31d-114">這些值都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="1c31d-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="1c31d-115">值</span><span class="sxs-lookup"><span data-stu-id="1c31d-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="1c31d-116">意義</span><span class="sxs-lookup"><span data-stu-id="1c31d-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="1c31d-117"><dt>**簽署者 \_ 時間戳記 \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="1c31d-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="1c31d-118">指定 Authenticode 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1c31d-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="1c31d-119"><dt>**簽署人 \_ 時間戳記 \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="1c31d-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="1c31d-120">指定符合 RFC 3161 規範的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1c31d-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1c31d-121">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-122">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。</span><span class="sxs-lookup"><span data-stu-id="1c31d-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="1c31d-123">*pwszHttpTimeStamp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-124">以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="1c31d-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="1c31d-125">*dwAlgId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-126">指定要用於執行符合 RFC 3161 規範之時間戳記的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="1c31d-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="1c31d-127">Authenticode 時間戳記會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="1c31d-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="1c31d-128">*psRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1c31d-129">Optional.</span></span> <span data-ttu-id="1c31d-130">[**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="1c31d-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="1c31d-131">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1c31d-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="1c31d-132">*pSipData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1c31d-133">Optional.</span></span> <span data-ttu-id="1c31d-134">以其他資料的形式傳遞至 [*主體介面封裝*](../secgloss/s-gly.md) 的32位值 (SIP) 函式。</span><span class="sxs-lookup"><span data-stu-id="1c31d-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="1c31d-135">此參數的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="1c31d-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="1c31d-136">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1c31d-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="1c31d-137">*ppSignerCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c31d-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1c31d-138">Optional.</span></span> <span data-ttu-id="1c31d-139">包含已簽署 BLOB 之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標位址。</span><span class="sxs-lookup"><span data-stu-id="1c31d-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="1c31d-140">當您完成使用 **簽署者 \_ 內容** 結構時，請呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="1c31d-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c31d-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c31d-141">Return value</span></span>

<span data-ttu-id="1c31d-142">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1c31d-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="1c31d-143">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1c31d-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="1c31d-144">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1c31d-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c31d-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c31d-145">Requirements</span></span>



| <span data-ttu-id="1c31d-146">需求</span><span class="sxs-lookup"><span data-stu-id="1c31d-146">Requirement</span></span> | <span data-ttu-id="1c31d-147">值</span><span class="sxs-lookup"><span data-stu-id="1c31d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c31d-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c31d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1c31d-149">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1c31d-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c31d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1c31d-151">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c31d-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1c31d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1c31d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c31d-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c31d-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c31d-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c31d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c31d-155">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="1c31d-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="1c31d-156">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="1c31d-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 

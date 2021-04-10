---
description: 簽署指定的檔案，並傳回已簽署資料的指標。
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692459"
---
# <a name="signersignex-function"></a><span data-ttu-id="85525-103">SignerSignEx 函式</span><span class="sxs-lookup"><span data-stu-id="85525-103">SignerSignEx function</span></span>

<span data-ttu-id="85525-104">**SignerSignEx** 函式會簽署指定的檔案，並傳回已簽署資料的指標。</span><span class="sxs-lookup"><span data-stu-id="85525-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="85525-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="85525-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="85525-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="85525-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85525-107">語法</span><span class="sxs-lookup"><span data-stu-id="85525-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="85525-108">參數</span><span class="sxs-lookup"><span data-stu-id="85525-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85525-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85525-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-110">修改此函式的行為。</span><span class="sxs-lookup"><span data-stu-id="85525-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="85525-111">如果要簽署的檔案是可移植的可執行檔 (PE) 檔，這可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="85525-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="85525-112">這些識別碼是在 Mssip 中定義。</span><span class="sxs-lookup"><span data-stu-id="85525-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="85525-113">值</span><span class="sxs-lookup"><span data-stu-id="85525-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="85525-114">意義</span><span class="sxs-lookup"><span data-stu-id="85525-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="85525-115"><dt>**SPC \_專有 \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="85525-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="85525-116">建立 PE 檔案的 SIP 間接資料時，請排除頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="85525-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="85525-117">此旗標優先于 **SPC \_ Inc. \_ PE \_ 頁面 \_ 雜湊 \_ 旗** 標旗標。</span><span class="sxs-lookup"><span data-stu-id="85525-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="85525-118">如果未指定 **spc \_ 專有 \_ PE \_ page \_ 雜湊 \_ 旗** 標或 **spc \_ inc. \_ pe \_ Page \_ 雜湊 \_** 旗標旗標，則會使用 [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) 函數所設定的值來進行此設定。</span><span class="sxs-lookup"><span data-stu-id="85525-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="85525-119">這項設定的預設值是在建立 PE 檔案的 SIP 間接資料時排除頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="85525-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="85525-120">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85525-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="85525-121"><dt>**SPC \_INC. \_ PE 匯 \_ 入 \_ 位址 \_ 表 \_ 旗**</dt>標 <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="85525-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="85525-122">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85525-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="85525-123"><dt>**SPC \_INC \_ PE \_ DEBUG \_ INFO \_ 旗**</dt>標 <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="85525-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="85525-124">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85525-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="85525-125"><dt>**SPC \_INC. \_ PE \_ 資源 \_ 旗**</dt>標 <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="85525-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="85525-126">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85525-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="85525-127"><dt>**SPC \_INC \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="85525-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="85525-128">建立 PE 檔案的 SIP 間接資料時包含頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="85525-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="85525-129">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85525-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="85525-130">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85525-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-131">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的指標，此結構會指定要簽署的主旨。</span><span class="sxs-lookup"><span data-stu-id="85525-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="85525-132">*pSignerCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85525-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-133">[**簽署者 \_**](signer-cert.md)憑證結構的指標，此結構會指定要用來建立數位簽章的憑證。</span><span class="sxs-lookup"><span data-stu-id="85525-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="85525-134">*pSignatureInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85525-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-135">簽署者簽章 [**\_ \_ 資訊**](signer-signature-info.md) 結構的指標，其中包含數位簽章的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="85525-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="85525-136">*pProviderInfo* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="85525-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-137">簽署者提供者 [**\_ \_ 資訊**](signer-provider-info.md) 結構的指標，指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的私密金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="85525-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="85525-138">如果此參數的值為 **Null**，則 *pSignerCert* 參數的值必須指定與 CSP 相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="85525-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="85525-139">*pwszHttpTimeStamp* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="85525-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-140">時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="85525-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="85525-141">*psRequest* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="85525-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-142">加入至簽署要求之 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="85525-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="85525-143">如果 *pwszHttpTimeStamp* 參數不包含非 **Null** 的有效值，就會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="85525-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85525-144">*pSipData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="85525-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-145">以其他資料形式傳遞至 SIP 函數的32位值。</span><span class="sxs-lookup"><span data-stu-id="85525-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="85525-146">此的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="85525-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="85525-147">*ppSignerCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="85525-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85525-148">包含已簽署 [*BLOB*](../secgloss/b-gly.md)之 [**簽署者 \_ 內容**](signer-context.md)結構的指標位址。</span><span class="sxs-lookup"><span data-stu-id="85525-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="85525-149">當您完成使用 **簽署者 \_ 內容** 結構時，請藉由呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md)函數來釋出 **簽署者 \_ 內容** 結構。</span><span class="sxs-lookup"><span data-stu-id="85525-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85525-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="85525-150">Return value</span></span>

<span data-ttu-id="85525-151">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="85525-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="85525-152">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="85525-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="85525-153">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="85525-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85525-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="85525-154">Requirements</span></span>



| <span data-ttu-id="85525-155">需求</span><span class="sxs-lookup"><span data-stu-id="85525-155">Requirement</span></span> | <span data-ttu-id="85525-156">值</span><span class="sxs-lookup"><span data-stu-id="85525-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85525-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85525-157">Minimum supported client</span></span><br/> | <span data-ttu-id="85525-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85525-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="85525-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85525-159">Minimum supported server</span></span><br/> | <span data-ttu-id="85525-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85525-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85525-161">DLL</span><span class="sxs-lookup"><span data-stu-id="85525-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85525-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85525-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85525-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85525-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85525-164">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="85525-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="85525-165">**SignerFreeSignerCoNtext**</span><span class="sxs-lookup"><span data-stu-id="85525-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 

---
description: 簽署和時間戳記指定的檔案，允許多個嵌套的簽章。
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194362"
---
# <a name="signersignex2-function"></a><span data-ttu-id="1e910-103">SignerSignEx2 函式</span><span class="sxs-lookup"><span data-stu-id="1e910-103">SignerSignEx2 function</span></span>

<span data-ttu-id="1e910-104">**SignerSignEx2** 函式會簽署指定的檔案，並為其加上時間戳記，以允許多個嵌套簽章。</span><span class="sxs-lookup"><span data-stu-id="1e910-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="1e910-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1e910-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="1e910-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="1e910-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1e910-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e910-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="1e910-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e910-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e910-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-110">修改此函式的行為。</span><span class="sxs-lookup"><span data-stu-id="1e910-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="1e910-111">如果要簽署的檔案是可移植的可執行檔 (PE) 檔，這可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="1e910-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="1e910-112">值</span><span class="sxs-lookup"><span data-stu-id="1e910-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="1e910-113">意義</span><span class="sxs-lookup"><span data-stu-id="1e910-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="1e910-114"><dt>**SPC \_專有 \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="1e910-115">建立 PE 檔案的 SIP 間接資料時，請排除頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="1e910-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="1e910-116">此旗標優先于 **SPC \_ Inc. \_ PE \_ 頁面 \_ 雜湊 \_ 旗** 標旗標。</span><span class="sxs-lookup"><span data-stu-id="1e910-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="1e910-117">如果未指定 **spc \_ 專有 \_ PE \_ page \_ 雜湊 \_ 旗** 標或 **spc \_ inc. \_ pe \_ Page \_ 雜湊 \_** 旗標旗標，則會使用 [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) 函數所設定的值來進行此設定。</span><span class="sxs-lookup"><span data-stu-id="1e910-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="1e910-118">這項設定的預設值是在建立 PE 檔案的 SIP 間接資料時排除頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="1e910-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="1e910-119">此值定義于 Mssip .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="1e910-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="1e910-120">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="1e910-121"><dt>**SPC \_INC. \_ PE 匯 \_ 入 \_ 位址 \_ 表 \_ 旗**</dt>標 <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="1e910-122">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="1e910-123"><dt>**SPC \_INC \_ PE \_ DEBUG \_ INFO \_ 旗**</dt>標 <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="1e910-124">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="1e910-125"><dt>**SPC \_INC. \_ PE \_ 資源 \_ 旗**</dt>標 <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="1e910-126">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="1e910-127"><dt>**SPC \_INC \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="1e910-128">建立 PE 檔案的 SIP 間接資料時包含頁面雜湊。</span><span class="sxs-lookup"><span data-stu-id="1e910-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="1e910-129">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="1e910-130">此值定義于 Mssip .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="1e910-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="1e910-131"><dt>**SIG \_附加**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="1e910-132">簽章將會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="1e910-132">The signature will be nested.</span></span> <span data-ttu-id="1e910-133">如果您在新增任何簽章之前設定此旗標，則會將產生的簽章新增為外部簽章。</span><span class="sxs-lookup"><span data-stu-id="1e910-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="1e910-134">如果您未設定此旗標，則產生的簽章會取代外部簽章，並刪除所有的內部簽章。</span><span class="sxs-lookup"><span data-stu-id="1e910-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="1e910-135">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e910-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-136">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的指標，此結構會指定要簽署的主旨。</span><span class="sxs-lookup"><span data-stu-id="1e910-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-137">*pSignerCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e910-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-138">[**簽署者 \_**](signer-cert.md)憑證結構的指標，此結構會指定要用來建立數位簽章的憑證。</span><span class="sxs-lookup"><span data-stu-id="1e910-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-139">*pSignatureInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e910-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-140">簽署者簽章 [**\_ \_ 資訊**](signer-signature-info.md) 結構的指標，其中包含數位簽章的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1e910-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-141">*pProviderInfo* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-142">[**簽署者提供者 \_ \_ 資訊**](signer-provider-info.md)結構的指標，此結構會指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的私密金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="1e910-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="1e910-143">如果此參數的值為 **Null**，則 *pSignerCert* 參數必須指定與 CSP 相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="1e910-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-144">*dwTimestampFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-145">如果 *pwszHttpTimeStamp* 參數不是 **Null**，則會傳遞至 [**SignerTimeStampEx3**](signertimestampex3.md)的旗標。</span><span class="sxs-lookup"><span data-stu-id="1e910-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="1e910-146">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1e910-146">This can be one of the following values.</span></span>



| <span data-ttu-id="1e910-147">值</span><span class="sxs-lookup"><span data-stu-id="1e910-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="1e910-148">意義</span><span class="sxs-lookup"><span data-stu-id="1e910-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="1e910-149"><dt>**簽署者 \_ 時間戳記 \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="1e910-150">預設值。</span><span class="sxs-lookup"><span data-stu-id="1e910-150">Default value.</span></span> <span data-ttu-id="1e910-151">指定 Authenticode 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1e910-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="1e910-152"><dt>**簽署人 \_ 時間戳記 \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="1e910-153">指定 RFC 3161 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1e910-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="1e910-154">如果 *pwszHttpTimeStamp* 參數為 **Null**，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="1e910-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-155">*pszTimestampAlgorithmOid* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-156">要用於建立 RFC 3161 時間戳記之演算法的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e910-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="1e910-157">Authenticode 時間戳記會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="1e910-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-158">*pwszHttpTimeStamp* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-159">時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="1e910-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-160">*psRequest* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-161">加入至簽署要求之 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1e910-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="1e910-162">如果 *pwszHttpTimeStamp* 參數不包含有效的值或為 **Null**，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="1e910-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-163">*pSipData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-164">以其他資料形式傳遞至 SIP 函數的32位值。</span><span class="sxs-lookup"><span data-stu-id="1e910-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="1e910-165">此的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="1e910-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-166">*ppSignerCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1e910-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-167">包含已簽署 [*BLOB*](../secgloss/b-gly.md)之 [**簽署者 \_ 內容**](signer-context.md)結構的指標位址。</span><span class="sxs-lookup"><span data-stu-id="1e910-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="1e910-168">當您完成使用 **簽署者 \_ 內容** 結構時，請藉由呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md)函數來釋出 **簽署者 \_ 內容** 結構。</span><span class="sxs-lookup"><span data-stu-id="1e910-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-169">*pCryptoPolicy* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e910-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e910-170">如果存在，則為憑證 [**強式 \_ \_ 簽署 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) 結構的指標，其中包含用來檢查強式簽章的參數。</span><span class="sxs-lookup"><span data-stu-id="1e910-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="1e910-171">如果憑證或其鏈未通過，則不會以任何方式更改檔案。</span><span class="sxs-lookup"><span data-stu-id="1e910-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="1e910-172">如果傳入 URL 以指定時間戳記授權單位 (TSA) ，此原則也會套用至時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1e910-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="1e910-173">*保存*</span><span class="sxs-lookup"><span data-stu-id="1e910-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="1e910-174">保留的。</span><span class="sxs-lookup"><span data-stu-id="1e910-174">Reserved.</span></span> <span data-ttu-id="1e910-175">這個值必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1e910-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e910-176">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e910-176">Return value</span></span>

<span data-ttu-id="1e910-177">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1e910-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="1e910-178">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1e910-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="1e910-179">此函式所傳回的可能錯誤碼包括（但不限於）下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="1e910-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="1e910-180">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1e910-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="1e910-181">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1e910-181">Return code</span></span>                                                                                  | <span data-ttu-id="1e910-182">Description</span><span class="sxs-lookup"><span data-stu-id="1e910-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e910-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1e910-184">如果您將 *dwTimestampFlags* 參數設定為「 **簽署 \_ 時間戳記 \_ AUTHENTICODE**」，則無法將 *dwFlags* 參數設定為「 **SIG \_ 附加**」。</span><span class="sxs-lookup"><span data-stu-id="1e910-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1e910-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e910-185">Requirements</span></span>



| <span data-ttu-id="1e910-186">需求</span><span class="sxs-lookup"><span data-stu-id="1e910-186">Requirement</span></span> | <span data-ttu-id="1e910-187">值</span><span class="sxs-lookup"><span data-stu-id="1e910-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e910-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e910-188">Minimum supported client</span></span><br/> | <span data-ttu-id="1e910-189">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e910-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1e910-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e910-190">Minimum supported server</span></span><br/> | <span data-ttu-id="1e910-191">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e910-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e910-192">DLL</span><span class="sxs-lookup"><span data-stu-id="1e910-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e910-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e910-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e910-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e910-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e910-195">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="1e910-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="1e910-196">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="1e910-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="1e910-197">**SignerFreeSignerCoNtext**</span><span class="sxs-lookup"><span data-stu-id="1e910-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 

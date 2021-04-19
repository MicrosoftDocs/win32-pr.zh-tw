---
description: 簽署指定的檔案。
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994388"
---
# <a name="signersign-function"></a><span data-ttu-id="adbdc-103">SignerSign 函式</span><span class="sxs-lookup"><span data-stu-id="adbdc-103">SignerSign function</span></span>

<span data-ttu-id="adbdc-104">**SignerSign** 函數會簽署指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="adbdc-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="adbdc-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="adbdc-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="adbdc-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="adbdc-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="adbdc-107">語法</span><span class="sxs-lookup"><span data-stu-id="adbdc-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="adbdc-108">參數</span><span class="sxs-lookup"><span data-stu-id="adbdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adbdc-109">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-110">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的指標，此結構會指定要簽署的主旨。</span><span class="sxs-lookup"><span data-stu-id="adbdc-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-111">*pSignerCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-112">[**簽署者 \_**](signer-cert.md)憑證結構的指標，此結構會指定要用來建立數位簽章的憑證。</span><span class="sxs-lookup"><span data-stu-id="adbdc-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-113">*pSignatureInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-114">簽署者簽章 [**\_ \_ 資訊**](signer-signature-info.md) 結構的指標，其中包含數位簽章的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="adbdc-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-115">*pProviderInfo* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-116">簽署者提供者 [**\_ \_ 資訊**](signer-provider-info.md) 結構的指標，指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的 [*私密金鑰*](../secgloss/p-gly.md) 資訊。</span><span class="sxs-lookup"><span data-stu-id="adbdc-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="adbdc-117">如果此參數的值為 **Null**，則 *pSignerCert* 參數的值必須指定與 CSP 相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="adbdc-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-118">*pwszHttpTimeStamp* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-119">時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="adbdc-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-120">*psRequest* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-121">加入至簽署要求之 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="adbdc-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="adbdc-122">如果 *pwszHttpTimeStamp* 參數不包含非 **Null** 的有效值，就會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="adbdc-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="adbdc-123">*pSipData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adbdc-124">以其他資料形式傳遞至 SIP 函數的32位值。</span><span class="sxs-lookup"><span data-stu-id="adbdc-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="adbdc-125">此的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="adbdc-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adbdc-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="adbdc-126">Return value</span></span>

<span data-ttu-id="adbdc-127">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="adbdc-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="adbdc-128">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="adbdc-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="adbdc-129">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="adbdc-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adbdc-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="adbdc-130">Requirements</span></span>



| <span data-ttu-id="adbdc-131">需求</span><span class="sxs-lookup"><span data-stu-id="adbdc-131">Requirement</span></span> | <span data-ttu-id="adbdc-132">值</span><span class="sxs-lookup"><span data-stu-id="adbdc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adbdc-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adbdc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="adbdc-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="adbdc-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adbdc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="adbdc-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adbdc-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adbdc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="adbdc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbdc-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adbdc-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adbdc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adbdc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbdc-140">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="adbdc-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 

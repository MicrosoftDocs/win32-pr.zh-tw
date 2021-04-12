---
description: 從指定的憑證存放區尋找符合指定主體憑證的簽發者憑證。
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192941"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="6512d-103">WTHelperCertFindIssuerCertificate 函式</span><span class="sxs-lookup"><span data-stu-id="6512d-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="6512d-104">\[**WTHelperCertFindIssuerCertificate** 函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6512d-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6512d-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6512d-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6512d-106">**WTHelperCertFindIssuerCertificate** 函式會從指定的憑證存放區尋找符合指定主體憑證的簽發者憑證。</span><span class="sxs-lookup"><span data-stu-id="6512d-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="6512d-107">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="6512d-107">This function has no associated import library.</span></span> <span data-ttu-id="6512d-108">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Wintrust.dll。</span><span class="sxs-lookup"><span data-stu-id="6512d-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6512d-109">語法</span><span class="sxs-lookup"><span data-stu-id="6512d-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="6512d-110">參數</span><span class="sxs-lookup"><span data-stu-id="6512d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6512d-111">*pChildCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6512d-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-112">要尋找相符簽發者憑證的主體憑證。</span><span class="sxs-lookup"><span data-stu-id="6512d-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6512d-113">*chStores* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6512d-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-114">*PahStores* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6512d-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="6512d-115">*pahStores* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6512d-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-116">要在其中搜尋的憑證存放區陣列。</span><span class="sxs-lookup"><span data-stu-id="6512d-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="6512d-117">*psftVerifyAsOf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6512d-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-118">驗證的時間。</span><span class="sxs-lookup"><span data-stu-id="6512d-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="6512d-119">*dwEncoding* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6512d-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-120">**DWORD** 值，指定要檢查之憑證的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="6512d-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="6512d-121">如需可能編碼類型的詳細資訊，請參閱 [憑證和訊息編碼類型](certificate-and-message-encoding-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6512d-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6512d-122">*pdwConfidence* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="6512d-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-123">這個參數可以是零或多個下列信賴值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="6512d-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="6512d-124">值</span><span class="sxs-lookup"><span data-stu-id="6512d-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="6512d-125">意義</span><span class="sxs-lookup"><span data-stu-id="6512d-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="6512d-126"><dt>**CERT \_信心 \_ SIG**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="6512d-127">憑證的簽章有效。</span><span class="sxs-lookup"><span data-stu-id="6512d-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="6512d-128"><dt>**CERT \_信賴 \_ 時間**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="6512d-129">憑證簽發者的時間有效。</span><span class="sxs-lookup"><span data-stu-id="6512d-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="6512d-130"><dt> **CERT \_ 信賴 \_ TIMENEST**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="6512d-131">憑證的有效時間。</span><span class="sxs-lookup"><span data-stu-id="6512d-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="6512d-132"><dt> **CERT \_ 信賴 \_ AUTHIDEXT**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="6512d-133">授權單位識別碼延伸有效。</span><span class="sxs-lookup"><span data-stu-id="6512d-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="6512d-134"><dt> **CERT \_ 信賴 \_ 度**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="6512d-135">憑證與授權單位識別碼延伸的簽章至少為有效。</span><span class="sxs-lookup"><span data-stu-id="6512d-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="6512d-136"><dt> **CERT \_ 信賴度 \_ 最高**</dt> <dt>0x11111000</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="6512d-137">所有其他信賴值的組合。</span><span class="sxs-lookup"><span data-stu-id="6512d-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="6512d-138">*dwError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6512d-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6512d-139">**DWORD** 變數的指標，其中包含此憑證的錯誤值（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="6512d-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6512d-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="6512d-140">Return value</span></span>

<span data-ttu-id="6512d-141">符合 *pChildCoNtext* 參數所指定之主體憑證的簽發者憑證。</span><span class="sxs-lookup"><span data-stu-id="6512d-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="6512d-142">備註</span><span class="sxs-lookup"><span data-stu-id="6512d-142">Remarks</span></span>

<span data-ttu-id="6512d-143">若要成功找到相符的簽發者憑證，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="6512d-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="6512d-144">*PChildCoNtext* 參數所指定的主體憑證簽章必須是有效的。</span><span class="sxs-lookup"><span data-stu-id="6512d-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="6512d-145">*PChildCoNtext* 參數之 **PCertInfo** 成員的 **rgExtension** 成員必須包含 [**CERT \_ 授權單位 \_ 金鑰 \_ 識別碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)結構。</span><span class="sxs-lookup"><span data-stu-id="6512d-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="6512d-146">此結構的 **CertIssuer** 和 **CertSerialMember** 成員非常符合簽發者憑證的對應成員。</span><span class="sxs-lookup"><span data-stu-id="6512d-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="6512d-147">*PsftVerifyAsOf* 參數的值必須在主體憑證的有效期間內。</span><span class="sxs-lookup"><span data-stu-id="6512d-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="6512d-148">主體憑證的有效期間必須在簽發者憑證的有效期間內。</span><span class="sxs-lookup"><span data-stu-id="6512d-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6512d-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="6512d-149">Requirements</span></span>



| <span data-ttu-id="6512d-150">需求</span><span class="sxs-lookup"><span data-stu-id="6512d-150">Requirement</span></span> | <span data-ttu-id="6512d-151">值</span><span class="sxs-lookup"><span data-stu-id="6512d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6512d-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6512d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6512d-153">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6512d-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6512d-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6512d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6512d-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6512d-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6512d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6512d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6512d-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6512d-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 

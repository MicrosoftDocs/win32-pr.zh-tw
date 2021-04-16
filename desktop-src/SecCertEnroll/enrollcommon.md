---
description: EnrollCommon 資料夾包含下列 helper 函式，以及憑證註冊 SDK 提供的範例所使用的宏。
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511993"
---
# <a name="enrollcommon"></a><span data-ttu-id="dc8f6-103">enrollCommon</span><span class="sxs-lookup"><span data-stu-id="dc8f6-103">enrollCommon</span></span>

<span data-ttu-id="dc8f6-104">EnrollCommon 資料夾包含下列 helper 函式，以及憑證註冊 SDK 提供的範例所使用的宏。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="dc8f6-105">預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCommon 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc8f6-106">函式</span><span class="sxs-lookup"><span data-stu-id="dc8f6-106">Function</span></span></th>
<th><span data-ttu-id="dc8f6-107">描述</span><span class="sxs-lookup"><span data-stu-id="dc8f6-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc8f6-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="dc8f6-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="dc8f6-109">接受 <strong>HRESULT</strong> 值、標籤和錯誤字串的宏會列印字串，並將程式控制項傳送至標籤後面的第一個語句。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="dc8f6-110">_JumpError</span></span></td>
<td><span data-ttu-id="dc8f6-111">與 _JumpIfError 宏相同。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="dc8f6-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="dc8f6-113">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="dc8f6-114">_PrintError</span></span></td>
<td><span data-ttu-id="dc8f6-115">列印錯誤訊息和 <strong>HRESULT</strong> 值的宏。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-116">convertWszToSz</span><span class="sxs-lookup"><span data-stu-id="dc8f6-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="dc8f6-117">使用 <strong>WideCharToMultiByte</strong> 函數和系統目前的 ANSI 字碼頁識別碼，將寬字元字串轉換成 ASCII 字元字串。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="dc8f6-118">EnrollCommon 中定義的 decConvertFromUnicode 和 findOIDFromTemplateName 函數會使用這個函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-119">convertSzToWsz</span><span class="sxs-lookup"><span data-stu-id="dc8f6-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="dc8f6-120">使用 <strong>MultiByteToWideChar</strong> 函數和系統目前的 ANSI 字碼頁識別碼，將 ASCII 字串轉換成寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="dc8f6-121">EnrollCommon 中定義的 findCertByTemplate 函數會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-122">convertSzToBstr</span><span class="sxs-lookup"><span data-stu-id="dc8f6-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="dc8f6-123">使用<strong>MultiByteToWideChar</strong>函式，將 ASCII 字串轉換成<strong>BSTR</strong> 。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="dc8f6-124">目前未使用此函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-125">convertWszToBstr</span><span class="sxs-lookup"><span data-stu-id="dc8f6-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="dc8f6-126">將寬字元字串轉換成 <strong>BSTR</strong>。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="dc8f6-127">InstallResponseFromPFX 範例會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-128">checkEnrollStatus</span><span class="sxs-lookup"><span data-stu-id="dc8f6-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="dc8f6-129">使用 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> 和 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> 介面檢查憑證註冊程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="dc8f6-130">EnrollEOBOCMC、enrollPKCS7、enrollRenewalPKCS7、enrollSimpleMachineCert 和 enrollSimpleUserCert 範例都會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-131">findCertByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="dc8f6-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="dc8f6-132">列舉目前使用者的個人憑證存儲，以尋找要使用的公開金鑰符合指定值的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="dc8f6-133">指定的值可以是下列旗標的位元組合：</span><span class="sxs-lookup"><span data-stu-id="dc8f6-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="dc8f6-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="dc8f6-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="dc8f6-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="dc8f6-141">EnrollFromPublicKey 範例會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-142">findCertByEKU</span><span class="sxs-lookup"><span data-stu-id="dc8f6-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="dc8f6-143">列舉目前使用者的個人憑證存儲，以找出增強金鑰使用方法 (EKU) 延伸模組符合輸入上指定的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="dc8f6-144">如需 EKU 延伸模組的詳細資訊，請參閱 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="dc8f6-145">EnrollEOBOCMC 範例會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-146">findCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="dc8f6-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="dc8f6-147">列舉目前使用者的個人憑證存儲，以在輸入時尋找範本符合指定的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="dc8f6-148">EnrollPKCS7 和 enrollRenewalPKCS7 範例會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-149">enrollCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="dc8f6-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="dc8f6-150">使用範本初始化 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> 物件、嘗試註冊隱含建立的憑證要求，並監視註冊程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="dc8f6-151">EnrollEOBOCMC、enrollFromPublicKey、enrollPKCS7 和 enrollRenewalPKCS7 範例都會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-152">verifyCertCoNtext</span><span class="sxs-lookup"><span data-stu-id="dc8f6-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="dc8f6-153">根據指定的 (基礎) 原則，以及選擇性地針對指定的增強金鑰使用方法 (EKU) 延伸模組，驗證憑證鏈的合規性。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="dc8f6-154">如需詳細資訊，請參閱 <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> 函式和 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> 和 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="dc8f6-155">EnrollEOBOCMC、enrollFromPublicKey、enrollPKCS7 和 enrollRenewalPKCS7 範例都會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-156">decConvertFromUnicode</span><span class="sxs-lookup"><span data-stu-id="dc8f6-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="dc8f6-157">將雙位元組 Unicode 字元的字串轉換成單一位元組 ANSI 字元的字串。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="dc8f6-158">EnrollCommon 中定義的 DecodeFileW 函數會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-159">DecodeFileW</span><span class="sxs-lookup"><span data-stu-id="dc8f6-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="dc8f6-160">將編碼的憑證或憑證要求檔案解碼為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="dc8f6-161">InstallResponseFromPFX 範例會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc8f6-162">EncodeToFileW</span><span class="sxs-lookup"><span data-stu-id="dc8f6-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="dc8f6-163">編碼憑證或憑證要求，並將其儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="dc8f6-164">CreateCNGCustomCMC、enrollEOBOCMC 和 enrollFromPublicKey 範例會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc8f6-165">findOIDFromTemplateName</span><span class="sxs-lookup"><span data-stu-id="dc8f6-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="dc8f6-166">抓取名稱所指定之範本的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="dc8f6-167">EnrollCommon 中定義的 findCertByTemplate 函數會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="dc8f6-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="dc8f6-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc8f6-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc8f6-169">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="dc8f6-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 


---
description: EnrollCommon 資料夾包含下列 helper 函式，以及憑證註冊 SDK 提供的範例所使用的宏。
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476014"
---
# <a name="enrollcommon"></a>enrollCommon

EnrollCommon 資料夾包含下列 helper 函式，以及憑證註冊 SDK 提供的範例所使用的宏。 預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCommon 資料夾中。




| 函式 | 描述 | 
|----------|-------------|
| _JumpIfError | 接受 <strong>HRESULT</strong> 值、標籤和錯誤字串的宏會列印字串，並將程式控制項傳送至標籤後面的第一個語句。 | 
| _JumpError | 與 _JumpIfError 宏相同。 | 
| _PrintIfError | 目前無法使用。 | 
| _PrintError | 列印錯誤訊息和 <strong>HRESULT</strong> 值的宏。 | 
| convertWszToSz | 使用 <strong>WideCharToMultiByte</strong> 函數和系統目前的 ANSI 字碼頁識別碼，將寬字元字串轉換成 ASCII 字元字串。 EnrollCommon 中定義的 decConvertFromUnicode 和 findOIDFromTemplateName 函數會使用這個函數。 | 
| convertSzToWsz | 使用 <strong>MultiByteToWideChar</strong> 函數和系統目前的 ANSI 字碼頁識別碼，將 ASCII 字串轉換成寬字元字串。 EnrollCommon 中定義的 findCertByTemplate 函數會使用此函式。 | 
| convertSzToBstr | 使用<strong>MultiByteToWideChar</strong>函式，將 ASCII 字串轉換成<strong>BSTR</strong> 。 目前未使用此函數。 | 
| convertWszToBstr | 將寬字元字串轉換成 <strong>BSTR</strong>。 InstallResponseFromPFX 範例會使用此函式。 | 
| checkEnrollStatus | 使用 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> 和 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> 介面檢查憑證註冊程式的狀態。 EnrollEOBOCMC、enrollPKCS7、enrollRenewalPKCS7、enrollSimpleMachineCert 和 enrollSimpleUserCert 範例都會使用此函數。 | 
| findCertByKeyUsage | 列舉目前使用者的個人憑證存儲，以尋找要使用的公開金鑰符合指定值的第一個憑證。 指定的值可以是下列旗標的位元組合：<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>EnrollFromPublicKey 範例會使用此函式。<br /> | 
| findCertByEKU | 列舉目前使用者的個人憑證存儲，以找出增強金鑰使用方法 (EKU) 延伸模組符合輸入上指定的第一個憑證。 如需 EKU 延伸模組的詳細資訊，請參閱 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> 介面。 EnrollEOBOCMC 範例會使用此函式。 | 
| findCertByTemplate | 列舉目前使用者的個人憑證存儲，以在輸入時尋找範本符合指定的第一個憑證。 EnrollPKCS7 和 enrollRenewalPKCS7 範例會使用此函數。 | 
| enrollCertByTemplate | 使用範本初始化 <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> 物件、嘗試註冊隱含建立的憑證要求，並監視註冊程式的狀態。 EnrollEOBOCMC、enrollFromPublicKey、enrollPKCS7 和 enrollRenewalPKCS7 範例都會使用此函數。 | 
| verifyCertCoNtext | 根據指定的 (基礎) 原則，以及選擇性地針對指定的增強金鑰使用方法 (EKU) 延伸模組，驗證憑證鏈的合規性。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> 函式和 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> 和 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> 結構。 EnrollEOBOCMC、enrollFromPublicKey、enrollPKCS7 和 enrollRenewalPKCS7 範例都會使用此函數。 | 
| decConvertFromUnicode | 將雙位元組 Unicode 字元的字串轉換成單一位元組 ANSI 字元的字串。 EnrollCommon 中定義的 DecodeFileW 函數會使用此函式。 | 
| DecodeFileW | 將編碼的憑證或憑證要求檔案解碼為位元組陣列。 InstallResponseFromPFX 範例會使用此函式。 | 
| EncodeToFileW | 編碼憑證或憑證要求，並將其儲存至檔案。 CreateCNGCustomCMC、enrollEOBOCMC 和 enrollFromPublicKey 範例會使用此函式。 | 
| findOIDFromTemplateName | 抓取名稱所指定之範本的物件識別碼。 EnrollCommon 中定義的 findCertByTemplate 函數會使用此函式。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 


---
description: 從內部的嵌套 PKCS 10 要求建立 CMC 要求物件 \# 。
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318068"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

CreateCNGCustomCMC 範例會從內部的嵌套 PKCS 10 要求建立 CMC request 物件 \# 。 內部要求是使用非對稱 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)所建立。 私密金鑰是使用「密碼編譯 API：新一代」 (CNG) 密碼編譯提供者，以及在命令列上指定的演算法來建立。 您也可以在私密金鑰上設定自訂選項（例如，匯出原則和金鑰保護層級）。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ createCNGCustomCMC 資料夾中。

## <a name="discussion"></a>討論

CreateCNGCustomCMC 範例：

1.  處理下列命令列引數：
    -   CNG [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) (CSP) 的名稱。
    -   用來產生非對稱私密金鑰的演算法名稱。
    -   用來 [*雜湊*](/windows/desktop/SecGloss/h-gly)[*憑證要求*](/windows/desktop/SecGloss/c-gly)的演算法名稱。
    -   要在其中儲存憑證要求的輸出檔。
    -   選擇性的字串 (AlternateSignature) 如果存在，則會指定使用離散而不是合併的簽章演算法。 如需詳細資訊，請參閱 [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) 屬性。
2.  建立 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件，並設定下列屬性：
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**演算法**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**KeyProtection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  建立非對稱私密金鑰。
4.  建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並使用私密金鑰將它初始化。
5.  建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 \# 在步驟4中建立的 PKCS 10 要求物件來初始化它。
6.  根據命令列上是否指定替代簽章字串，將替代簽章演算法旗標設定為 **variant \_ TRUE** 或 **variant \_ FALSE** 。 如需詳細資訊，請參閱 [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)。
7.  從命令列上指定的演算法名稱，建立 (OID) 的 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly)[*物件識別碼*](/windows/desktop/SecGloss/o-gly)，並在 CMC 要求物件上設定 oid。
8.  簽署憑證要求，並使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 進行編碼。
9.  抓取包含已編碼之 CMC 憑證要求的字串，並將其儲存至檔案。 EncodeToFileW 函式定義于 EnrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 

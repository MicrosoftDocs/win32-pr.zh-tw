---
description: 建立自訂的 PKCS \# 10 要求、將它提交給獨立的憑證授權單位單位（ (CA) ），並在憑證存放區中安裝已發行的憑證。
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972261"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

EnrollCustomPKCS10 範例會建立自訂 PKCS \# 10 要求、將它提交給 (CA) 的獨立憑證授權單位單位，並在憑證存放區中安裝已發行的憑證。 獨立 CA 不需要 Active Directory，也不會使用範本。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomPKCS10 資料夾中。

## <a name="discussion"></a>討論

EnrollCustomPKCS10 範例：

1.  處理命令列引數。 命令列應該包含 X. 500 憑證主體名稱、電子郵件 (RFC822) 名稱和增強金鑰使用方法 (EKU) 物件識別碼 (OID) 。 例如，您可以指定下列引數以進行註冊 *user1@example.com* ：
    -   主體名稱： "*CN = user1，dc = example，dc = com*"
    -   RFC822 名稱： *user1@example.com*
    -   用戶端驗證 EKU OID：1.3.6.1.5.5.7.3。2
2.  建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件，並指定 [**X509CertificateEnrollmentCoNtext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext)列舉的 **CoNtextUser** 值，為終端使用者初始化它。
3.  建立 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件，使用物件將主體名稱編碼為位元組陣列，並將陣列加入至 PKCS \# 10 要求物件。
4.  建立 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) 物件，使用命令列上指定的 EKU 物件識別碼 (OID) 來初始化它、建立 [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) 集合、將新的 **IObjectId** (EKU) 物件加入至集合、使用集合來初始化 [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) 物件，並將此物件加入至要求。
5.  建立 [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) 物件，使用命令列上指定的 RFC822 名稱將它初始化、建立 [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) 集合、將新 **IAlternativeName** (RFC822 名稱 ) 物件加入至集合、建立 [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) 物件，並將此物件加入至要求。
6.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件將它初始化，並抓取包含 base64 編碼要求的字串。
7.  建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。
8.  建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。
9.  檢查提交狀態，如果註冊成功，則將憑證安裝至憑證存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 

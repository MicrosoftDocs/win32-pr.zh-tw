---
description: 屬性是用來將值與憑證產生關聯。
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: 外部屬性函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40196f4f42823ad44debeccc0fa85dc4615d58d1a0ccf521b2dd796e72574db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779628"
---
# <a name="external-property-functions"></a>外部屬性函式

屬性是用來將值與憑證產生關聯。 屬性絕不會由 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 傳送或處理，而且不會儲存在憑證內。 一般而言，在從 CA 接收憑證之後，以及將憑證儲存在存放區之前，它們都會與憑證相關聯。 這些屬性會連同憑證儲存在存放區中。 CertEnroll.dll 會實 [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) 介面，以及下列衍生自 **ICertProperty** 的介面：

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

下列各節會識別 Xenroll.dll 所匯出的函式，以管理外部憑證屬性。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [ThumbPrintWStr](#thumbprintwstr)
-   [相關主題](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

Xenroll.dll 中的 [**addBlobPropertyToCertificateWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) 函數會將屬性加入至憑證。

在 CertEnroll.dll 中，所有衍生自 [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) 的物件都會執行 [**SetValueOnCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) 方法，您可以使用此方法將屬性與憑證產生關聯。 此外， [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件也會直接執行 [**enrollment.certificatefriendlyname**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) 和 [**CertificateDescription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription) 屬性。

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

Xenroll.dll 中的 [**GetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) 函式會抓取用來保存 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)的 exchange 憑證。

您可以使用 CertEnroll.dll 中的 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件來建立 CA 的要求，以封存您的私密金鑰。 您必須從 CA 取出 exchange 憑證，並使用該憑證中包含的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 來加密您要提交以封存的私密金鑰。 若要指定或取出 CA exchange 憑證，請呼叫該物件上的 [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) 屬性。

## <a name="resetblobproperties"></a>resetBlobProperties

Xenroll.dll 中的 [**resetBlobProperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) 函式會從憑證中移除屬性集合。

在 CertEnroll.dll 中，所有衍生自 [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) 的屬性物件都會執行 [**RemoveFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) 屬性，讓您可以用來將屬性與憑證解除關聯。

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

Xenroll.dll 中的 [**SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) 函數會指定用來封存私密金鑰的 exchange 憑證。

您可以使用 CertEnroll.dll 中的 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件來建立 CA 的要求，以封存您的私密金鑰。 您必須從 CA 取出 exchange 憑證，並使用該憑證中包含的公開金鑰來加密您要提交以封存的私密金鑰。 若要指定或取出 CA exchange 憑證，請呼叫該物件上的 [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) 屬性。

## <a name="setsignercertificate"></a>SetSignerCertificate

Xenroll.dll 中的 [**SetSignerCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) 函數會指定簽署者憑證。

CertEnroll.dll 中的 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件可用於簽署 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly)、CMC 或自我簽署的 [*憑證要求*](/windows/desktop/SecGloss/c-gly)。 您可以藉由呼叫下列其中一個屬性，使用現有的簽署憑證來初始化物件，並將它與要求產生關聯：

-   IX509CertificateRequestCmc 上的 [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) [](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   IX509CertificateRequestPkcs7 上的 [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) [](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   IX509CertificateRequestCertificate 上的 [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) [](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

此外，如果您從內部要求和範本初始化 CMC 要求，或從現有的要求初始化 PKCS \# 7 要求，則可能會設定簽署憑證。

## <a name="thumbprintwstr"></a>ThumbPrintWStr

Xenroll.dll 中的 [**ThumbPrintWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) 函數會指定或抓取憑證雜湊的值。

在 CertEnroll.dll 中，您可以使用 [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)物件來取得 [*雜湊*](/windows/desktop/SecGloss/h-gly)值， () 由呼叫 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate)方法建立的 [*指紋*](/windows/desktop/SecGloss/t-gly)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 

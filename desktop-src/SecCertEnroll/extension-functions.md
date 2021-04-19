---
description: X.509 第3版憑證格式可識別多個可新增至憑證的延伸模組，以提供有關金鑰使用方式、憑證原則和條件約束、替代名稱表單等的增強資訊。
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc490c8763a00fae9e7fb1e8a702ff87e2c18fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001736"
---
# <a name="extension-functions"></a>擴充功能

[*X.509*](/windows/desktop/SecGloss/x-gly)第3版憑證格式可識別多個可新增至憑證的延伸模組，以提供有關金鑰使用方式、憑證原則和條件約束、替代名稱表單等的增強資訊。

CertEnroll.dll 會執行下列介面來管理憑證延伸：

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

下列各節將討論 Xenroll.dll 管理憑證延伸所匯出的函式。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [相關主題](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

Xenroll.dll 中的 [**AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) 函數會依名稱將憑證範本新增至要求。

使用 CertEnroll.dll，將範本併入憑證要求的慣用方法，是在 PKCS [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) \# 10 或 [* pkcs ) 要求物件或 CMC 要求上的 [**InitializeFromInnerRequestTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename)方法上使用 InitializeFromTemplateName 方法。

如果用戶端上無法使用特定範本，但是 (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位預期會瞭解該範本，您可以使用 [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) 介面來新增第1版的範本，或者您可以使用 [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) 介面將第2版範本新增至憑證要求。 例如，若要新增第1版的範本，請執行下列動作：

1.  建立 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 物件。
2.  建立 [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) 物件，並呼叫 [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) 方法，並指定範本名稱。
3.  藉由呼叫 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)方法，將建立的延伸模組加入至 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。
4.  建立 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件，並呼叫 [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) 方法，並在輸入時指定 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。
5.  藉由呼叫現有 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)要求物件上的 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes)屬性，來取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合物件。

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

Xenroll.dll 中的 [**AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) 函式會依名稱、物件識別碼和版本將憑證範本新增至要求。

如需如何使用 CertEnroll.dll 在要求中併入範本資訊的相關資訊，請參閱 AddCertTypeToRequestWStr。

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

Xenroll.dll 中的 [**AddExtensionsToRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) 函式會將擴充功能的集合加入至要求。

在 CertEnroll.dll 中，會將擴充功能新增至 CMC 或 PKCS 10 要求的屬性集合 \# 。 若要加入延伸模組，請執行下列動作：

1.  建立 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 物件。
2.  建立 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 物件，並呼叫 [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) 方法，從物件識別碼和延伸模組值建立延伸，或使用先前所列的任何介面來定義其中一個較常見的延伸模組。
3.  藉由呼叫 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)方法，將在上一個步驟中建立的每個新擴充功能新增至 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

Xenroll.dll 中的 [**addExtensionToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) 函式會在要求中新增特定的擴充功能。

在 CertEnroll.dll 中，必須先定義特定的擴充功能，並將其新增至延伸模組集合，再將擴充集合新增至 CMC 或 PKCS 10 要求的屬性集合 \# 。 如需詳細資訊，請參閱上述 AddExtensionsToRequest 討論。

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

Xenroll.dll 中的 [**EnableSMIMECapabilities**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) 函式會指定或抓取布林值，指出是否要將 **SMIMECapabilities** 延伸模組加入至要求。

您可以呼叫 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件上的 [**SmimeCapabilities**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities)屬性，在編碼之前自動將 [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)物件新增至要求。

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

Xenroll.dll 中的 [**IncludeSubjectKeyID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) 函式會指定或抓取布林值，指出是否要將 **SubjectKeyIdentifier** 延伸模組加入至要求。

根據預設，初始化 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)要求物件時，會建立 **SubjectKeyIdentifier** 延伸模組。 您可以藉由呼叫 [**SuppressOids**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) 屬性來覆寫此行為。

如果您有 [*公開/私密金鑰*](/windows/desktop/SecGloss/p-gly)組，您也可以在 CertEnroll.dll 中使用 [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) 介面，藉由執行下列動作，將 **SubjectKeyIdentifier** 擴充功能新增至憑證要求：

1.  建立 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 物件。
2.  建立 [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) 物件，並呼叫 [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) 方法，並指定包含識別碼的字串。 一般來說，這是 CA 簽署憑證中包含之 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 的20位元組 sha-1 雜湊。
3.  藉由呼叫 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)方法，將建立的延伸模組加入至 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。
4.  建立 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件，並呼叫 [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) 方法，並在輸入時指定 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。
5.  藉由呼叫現有 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)要求物件上的 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes)屬性，來取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合物件。

## <a name="resetextensions"></a>resetExtensions

Xenroll.dll 中的 [**resetExtensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) 函式會從要求中移除擴充功能集合。

若要使用 CertEnroll.dll 從索引編號移除要求中的延伸模組，請在 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合上呼叫 [**remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove)方法。 若要從要求中移除所有屬性，請呼叫 [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 

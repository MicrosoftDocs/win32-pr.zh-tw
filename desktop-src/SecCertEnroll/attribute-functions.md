---
description: 您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: 屬性函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192617"
---
# <a name="attribute-functions"></a>屬性函式

您可以將屬性新增至憑證要求，以提供證書 [*頒發機構*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。

CertEnroll.dll 會執行下列介面來定義屬性和屬性集合：

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

下列各節會識別 Xenroll.dll 所匯出的函式，以將密碼編譯屬性與憑證要求產生關聯，並討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [ClientId](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [相關主題](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

Xenroll.dll 中的 [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) 函數會將屬性新增至憑證要求。

一般而言，若要使用在 CertEnroll.dll 中執行的物件，將屬性新增至要求，您可以執行下列動作：

1.  建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合物件。
2.  建立 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 物件，並呼叫 [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) 方法，從物件識別碼和屬性值建立屬性，或使用先前所列的任何介面來定義一個更常見的屬性。
3.  使用 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add)方法，將在上一個步驟中建立的每個新屬性加入至 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)集合。
4.  建立 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件，並呼叫 [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) 方法將它初始化，並在輸入上指定 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合。
5.  藉由呼叫現有 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)要求物件上的 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes)屬性，來取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合物件。
6.  將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件加入至 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) 集合。

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

驗證的屬性是名稱/值組，已簽署並加入至簽章。 Xenroll.dll 中的 [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) 函數會將經過驗證的屬性陣列新增至 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 要求。

如上所述， [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) 函式所述，您可以使用 CertEnroll.dll 輕鬆地定義屬性集合，並將其新增至憑證要求。 但是，您無法選擇是否要驗證屬性。 註冊程式會自動進行此決策。

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

Xenroll.dll 中的 [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) 函數會將未經驗證的名稱/值組加入至要求。

您可以使用 CertEnroll.dll 中的 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 介面來定義名稱/值組，也可以執行下列動作，將名稱/值組的集合新增至 CMC 要求物件：

1.  建立並初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。 初始化進程會建立空的 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) 集合。
2.  呼叫現有 CMC 要求物件上的 [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) 屬性，以取出集合。
3.  建立並初始化 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件。
4.  藉由呼叫 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add)方法，將每個新的名稱/值組新增至 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)集合。

註冊程式會將名稱-值組的集合放在 CMC 要求的 **TaggedAttribute** 結構中。

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

Xenroll.dll 中的 [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) 函數會將經過驗證的名稱/值組加入至要求。 這通常用來指定以註冊 (EOBO) 要求中的要求者名稱。

在 CertEnroll.dll 中，使用 [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) 屬性來指定 EOBO 要求中的名稱。

## <a name="clientid"></a>ClientId

Xenroll.dll 中的 [**clientid**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) 函數會指定或抓取 **clientid** 屬性。

使用 CertEnroll.dll 中的 [**ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) 屬性，將此屬性新增至 CMC 或 PKCS \# 10 要求。

## <a name="renewalcertificate"></a>RenewalCertificate

Xenroll.dll 中的 [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) 函數會指定或抓取 **RenewalCertificate** 屬性。

在 CertEnroll.dll 中，當您在 PKCS 7 或 PKCS ) 物件上呼叫 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) 時，會 \# 自動建立。

## <a name="resetattributes"></a>resetAttributes

Xenroll.dll 中的 [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) 函數會從要求中移除屬性集合。

若要使用 CertEnroll.dll 從索引中移除要求的屬性，請在 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)集合上呼叫 [**remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove)方法。 若要從要求中移除所有屬性，請呼叫 [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 

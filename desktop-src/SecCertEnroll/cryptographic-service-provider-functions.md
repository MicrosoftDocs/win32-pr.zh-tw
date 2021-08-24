---
description: Xenroll.dll 所匯出的函式，可用於管理密碼編譯提供者。
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: 密碼編譯服務提供者函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947d9c4f2529071b28052ae5ca34f811d4657c3fd4cede23285999cbaa13a72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883078"
---
# <a name="cryptographic-service-provider-functions"></a>密碼編譯服務提供者函數

下列各節會識別 Xenroll.dll 所匯出的函式，該函式可用於管理密碼編譯提供者。 每個主題也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [相關主題](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

Xenroll.dll 中的 [**EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) 函數會抓取密碼編譯演算法集合。

使用 CertEnroll.dll 時，您可以執行下列動作，以抓取 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 所支援之演算法的相關資訊 (CSP) ：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations)屬性。
6.  在步驟5中抓取的 [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)集合中，呼叫特定 [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)物件上的 [**CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms)屬性。

## <a name="enumcontainerswstr"></a>enumContainersWStr

Xenroll.dll 中的 [**enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) 函式會依據索引，從集合中抓取金鑰容器。

CertEnroll.dll 程式庫不會直接執行此功能。

## <a name="enumproviderswstr"></a>enumProvidersWStr

Xenroll.dll 中的 [**enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) 函式會依據索引，從集合中取出 CSP。

使用 CertEnroll.dll 時，您可以執行下列動作來取出密碼編譯容器的集合：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations)屬性。

## <a name="getalgnamewstr"></a>GetAlgNameWStr

Xenroll.dll 中的 [**GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) 函數會抓取 [*密碼編譯演算法*](/windows/desktop/SecGloss/c-gly)的名稱。

使用 CertEnroll.dll 時，您可以執行下列動作來取出演算法名稱：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**演算法**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)屬性，以取出演算法物件識別碼。
6.  呼叫 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)介面上的 [ [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) ] 屬性，以取得演算法顯示名稱。

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

Xenroll.dll 中的 [**getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) 函數會抓取密碼編譯提供者類型。

使用 CertEnroll.dll 時，您可以執行下列動作來取出提供者類型：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype)屬性。

## <a name="hashalgid"></a>HashAlgID

Xenroll.dll 中的 [**HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) 函式會抓取整數值，其中包含用來簽署要求的演算法識別碼。

使用 CertEnroll.dll 時，您可以執行下列動作來取得雜湊演算法：

-   藉由呼叫 pkcs 10 或 CMC 要求上的 [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation)屬性， [](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) \# 或 [*pkcs \# 7*](/windows/desktop/SecGloss/p-gly)要求上的 [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate)屬性，來取出 IX509SignatureInformation 介面。
-   呼叫簽章資訊物件上的 [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) 屬性，以取出雜湊演算法物件識別碼。

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

Xenroll.dll 中的 [**HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) 函數會指定或抓取字串值，以識別用來簽署要求的雜湊演算法。

使用 CertEnroll.dll 時，您可以執行下列動作來取得雜湊演算法：

-   藉由呼叫 pkcs 10 或 CMC 要求上的 [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation)屬性， [](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) \# 或 Pkcs 7 要求上的 [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate)屬性，來取出 IX509SignatureInformation 介面 \# 。
-   呼叫簽章資訊物件上的 [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) 屬性，以取出雜湊演算法物件識別碼。
-   在步驟2中傳回的 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)介面上呼叫 [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname)屬性，以抓取演算法顯示名稱。

## <a name="providerflags"></a>ProviderFlags

Xenroll.dll 中的 [**ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) 函數會指定或抓取取得 CSP 控制碼時使用的旗標。

CertEnroll.dll 程式庫不會完全對應此函式，但是您可以從註冊物件和 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)取得豐富的屬性資訊。 如需詳細資訊，請檢查 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 和 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 介面所公開的屬性。

## <a name="providernamewstr"></a>ProviderNameWStr

Xenroll.dll 中的 [**ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) 函數會指定或抓取 CSP 的名稱。

使用 CertEnroll.dll 時，您可以執行下列動作來取出提供者名稱：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  在從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上，呼叫 [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)屬性。

## <a name="providertype"></a>ProviderType

Xenroll.dll 中的 [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) 函式會指定或抓取識別 CSP 型別的整數值。

使用 CertEnroll.dll 時，您可以執行下列動作來取出提供者類型：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype)屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 

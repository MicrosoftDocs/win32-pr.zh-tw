---
description: CertEnroll.dll 程式庫會實施五個介面，可用來建立和管理憑證要求。
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: 憑證要求功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04191f49949f662a9b9d780726f7ac7a40b370ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026317"
---
# <a name="certificate-request-functions"></a>憑證要求功能

CertEnroll.dll 程式庫會實施五個介面，可用來建立和管理憑證要求。 在這些情況下， [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 介面代表一個抽象基底物件，此物件定義了下列四個介面所繼承的方法簽章。

| 介面                                                                        | 描述                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | 可讓您直接建立憑證，而不需 (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位。<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | 代表透過 [*cms 的憑證管理*](/windows/desktop/SecGloss/c-gly) (CMC)  (憑證管理訊息（透過 cms）) 憑證要求（可包含嵌套的 PKCS \# 10 要求或其他 CMC 要求物件）。<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | 表示 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 憑證訊息語法 (CMS) 要求物件必須包含嵌套的 PKCS \# 10 要求。<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | 表示 PKCS \# 10 憑證要求。 PKCS \# 10 要求可以直接傳送至 CA，或可由 pkcs \# 7 或 CMC 要求包裝。<br/>                                                                                                                                                            |



 

您可以使用憑證要求物件來初始化 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，以在憑證階層中註冊用戶端，並安裝 CA 所傳回的憑證回應。

下列各節會識別 Xenroll.dll 所匯出的函式，以建立、列舉或刪除憑證要求。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [重設](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [相關主題](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

Xenroll.dll 中的 [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) 函數會建立 base64 編碼的 PKCS \# 10 憑證要求，並將它儲存在檔案中。

CertEnroll.dll 程式庫不會直接執行將要求寫入檔案的功能。 不過，您可以藉由呼叫 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上的 [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata)屬性，並建立自訂函式來將值複製到檔案中，來取得憑證要求。

## <a name="createfilerequestwstr"></a>createFileRequestWStr

Xenroll.dll 中的 [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) 函數會建立 pkcs \# 7、PKCS \# 10 或 CMC 憑證要求，並將它儲存在檔案中。

CertEnroll.dll 程式庫不會直接執行將要求寫入檔案的功能。 不過，您可以藉由呼叫 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上的 [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata)屬性，並建立自訂函式來將值複製到檔案中，來取得憑證要求。

## <a name="createpkcs10wstr"></a>createPKCS10WStr

Xenroll.dll 中的 [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) 函數會建立 PKCS \# 10 憑證要求，並將它複製到位元組陣列。

您可以使用 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件 \# ，從現有的要求、現有的憑證、 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)、 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)或範本來初始化 PKCS 10 要求。

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

Xenroll.dll 中的 [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) 函數會建立 PKCS \# 7 憑證要求，並將它複製到位元組陣列。

您可以使用 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件 \# ，從現有的要求、現有的憑證、內部要求物件或範本初始化 PKCS 7 要求。

## <a name="createrequestwstr"></a>createRequestWStr

Xenroll.dll 中的 [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) 函數會建立 pkcs \# 7、PKCS \# 10 或 CMC 憑證要求，並將它複製到位元組陣列。

若要使用 CertEnroll.dll 程式庫來建立 PKCS \# 7、pkcs \# 10 或 CMC 要求，您可以建立及初始化 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)、 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件的實例。

## <a name="deleterequestcert"></a>DeleteRequestCert

Xenroll.dll 中的 [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) 函式會指定或抓取布林值，指出是否在安裝憑證回應之後移除虛擬憑證。

CertEnroll.dll 中的 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件會自動在要求存放區中建立虛擬憑證，以暫時儲存在註冊程式期間初始化的各種憑證屬性。 CA 發行憑證之後，會將屬性複製到新的憑證，並刪除虛擬憑證。 CertEnroll.dll 程式庫不允許您在安裝憑證回應之後，強制虛擬憑證維持不變。

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

Xenroll.dll 中的 [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) 函式會抓取暫止要求的指定屬性值。

CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

Xenroll.dll 中的 [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) 函式會從要求存放區中移除暫止的要求。

CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。

## <a name="reset"></a>重設

Xenroll.dll 中的 [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) 函數會將憑證註冊控制項傳回到初始狀態。

您可以使用 Certenroll.dll 建立所需類型的新要求物件，以達到相同的結果。

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

Xenroll.dll 中的 [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) 函數會指定暫止要求的屬性。

CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。 您可以呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring)屬性，以抓取設定字串，但僅適用于使用中的註冊物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 


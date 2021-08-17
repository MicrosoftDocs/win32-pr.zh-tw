---
description: 實行 IX509Enrollment 介面。
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: 憑證回應功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902398"
---
# <a name="certificate-response-functions"></a>憑證回應功能

CertEnroll.dll 會 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 介面來提交用戶端憑證要求，並安裝 (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位回應。

註冊程式可以容納下列三種案例：

<dl> 頻外註冊

1.  呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件所執行的任何初始化方法。
2.  呼叫 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) 方法來取得要求。
3.  以手動方式或使用其他程式) ，從頻外 (提交要求。
4.  接收來自 CA 的回應。
5.  呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 方法。

  
自動註冊

1.  呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件所執行的任何初始化方法。
2.  呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 方法。

  
延遲的註冊

1.  呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件所執行的任何初始化方法。
2.  呼叫 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) 方法來取得要求。
3.  儲存要求，直到您準備好提交要求為止。
4.  當您準備好要註冊時，請呼叫 [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) 方法來重新初始化註冊物件。
5.  當 CA 傳回憑證時，呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 方法。

  
</dl>

在註冊過程中，您可以呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status)屬性來取得 [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus)列舉值，以識別註冊成功、暫止、已略過、產生錯誤或遭到拒絕。

下列各節會識別 Xenroll.dll 所匯出的函式，以從 CA 安裝憑證回應。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertCoNtextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertCoNtextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertCoNtextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDS](#writecerttouserds)
-   [相關主題](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

Xenroll.dll 中的 [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) 函數會從檔案安裝 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 回應。

CertEnroll.dll 程式庫不會直接執行從檔案安裝 PKCS \# 7 憑證回應的功能。 不過，您可以建立自訂函式，將檔案資料讀入位元組陣列，然後呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝回應。

如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下，安裝憑證。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

Xenroll.dll 中的 [**acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) 函數會從檔案安裝 PKCS \# 7 或 CMC 憑證回應。

CertEnroll.dll 程式庫不會直接執行從檔案安裝憑證回應的功能。 不過，您可以建立自訂函式，將檔案資料讀入位元組陣列，然後呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 或 CMC 回應。

如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下，安裝憑證。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

Xenroll.dll 中的 [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) 函式會安裝 \# 包含在位元組陣列中的 PKCS 7 回應。

您可以呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 訊息。 如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，因此可讓您在 \# 未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下安裝 PKCS 7 回應。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="acceptresponseblob"></a>acceptResponseBlob

Xenroll.dll 中的 [**acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) 函數會安裝 \# 包含在位元組陣列中的 PKCS 7 或 CMC 憑證回應。

您可以呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 或 CMC 回應。 如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下安裝回應。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="getcertcontextfromfileresponsewstr"></a>getCertCoNtextFromFileResponseWStr

Xenroll.dll 中的 [**getCertCoNtextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) 函數會從檔案抓取用戶端憑證。

CertEnroll.dll 程式庫不會直接執行從儲存在檔案中的 CA 回應取得憑證的功能。 不過，您可以建立自訂函式，將檔案資料讀入位元組陣列中，並呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 或 CMC 回應，然後呼叫 [**憑證**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) 屬性來取得憑證。

如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下，安裝憑證。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="getcertcontextfrompkcs7"></a>getCertCoNtextFromPKCS7

Xenroll.dll 中的 [**getCertCoNtextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) 函數會從 PKCS 7 回應中抓取用戶端憑證 \# 。

呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)方法之後，您可以呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate)屬性來取得憑證。

## <a name="getcertcontextfromresponseblob"></a>getCertCoNtextFromResponseBlob

Xenroll.dll 中的 [**getCertCoNtextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) 函式會從 PKCS \# 7 或 CMC 回應中抓取用戶端憑證。

呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)方法之後，您可以呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate)屬性來取得憑證。

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

Xenroll.dll 中的 [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) 函數會安裝 PKCS \# 7 回應。

您可以呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 或 CMC 回應。 如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下安裝回應。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

Xenroll.dll 中的 [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) 函數會安裝 PKCS \# 7 回應，並傳回已安裝的憑證數目。

您可以呼叫 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) 來安裝 PKCS \# 7 或 CMC 回應。 如果您為 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)的第一個參數指定 [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags)列舉的 **AllowNoOutstandingRequest** 值，則虛擬憑證不需要存在，如此可讓您在未先呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)或 [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)的情況下安裝回應。 但是，如果您要使用 web 腳本來安裝憑證，要求存放區中必須有虛擬憑證存在。 因此，您必須為第一個參數指定 **AllowNone** 。

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

Xenroll.dll 中的 [**SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) 函數會指定或抓取要儲存憑證回應的檔案名。 CertEnroll.dll 程式庫不會執行可讓您將憑證複製到特定檔案的功能。 註冊程式會自動將憑證鏈安裝到適當存放區中的檔案。

## <a name="writecerttocsp"></a>WriteCertToCSP

Xenroll.dll 中的 [**WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) 函式會指定或抓取布林值，指出是否應將憑證寫入 (CSP) 的 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 。 一般而言，如果呼叫此函式，則提供者是 [*智慧卡*](/windows/desktop/SecGloss/s-gly)。

在 CertEnroll.dll 中，當用戶端呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 方法來提交智慧卡憑證的要求併發出憑證時， [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 會自動將憑證安裝在智慧卡上，並假設該卡片是安裝在讀取器中。 [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)方法也會自動將憑證寫入智慧卡。

## <a name="writecerttouserds"></a>WriteCertToUserDS

Xenroll.dll 中的 [**WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) 函數會指定或抓取布林值，指出是否應將憑證儲存在 Active Directory 存放區中。 CertEnroll.dll 程式庫不會執行功能，可讓您指定要將憑證複製到其中的存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 

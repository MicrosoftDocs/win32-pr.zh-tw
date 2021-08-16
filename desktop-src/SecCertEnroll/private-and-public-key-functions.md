---
description: 實行 IX509PrivateKey 和 IX509PublicKey 介面。
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: 私用和公開金鑰函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6f210393ffaeb676e0190d391692225f25e0cfb4bc3acbcd2c3c188bf40a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774421"
---
# <a name="private-and-public-key-functions"></a>私用和公開金鑰函數

CertEnroll.dll 會實行 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 和 [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) 介面。 例如，您可以使用 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 介面在 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)上執行下列動作：

-   建立、開啟、關閉、匯入、匯出和刪除金鑰。
-   指定或取出 [*公開金鑰演算法*](/windows/desktop/SecGloss/p-gly)。
-   指定或取得支援公開金鑰演算法 (CSP) 的可用 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 的相關資訊。
-   指定或取出與 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)相關聯的 [*憑證*](/windows/desktop/SecGloss/c-gly)。
-   指定或取出 [*金鑰容器*](/windows/desktop/SecGloss/k-gly)的名稱。
-   指定或抓取索引鍵的說明和顯示名稱。
-   指定或抓取私密金鑰上的匯出條件約束位置。
-   指定或取得布林值，指出金鑰是否存在。
-   指定或取出值，指出如何在使用之前保護金鑰。
-   指定或取出值，指出金鑰是否可用於簽署、加密或兩者。
-   指定或取出值，以識別可使用金鑰的特定用途。
-   指定或取出金鑰的長度。
-   指定或取出值，指出是否在電腦或使用者的內容中使用或儲存金鑰。
-   取得布林值，這個值會指定是否已開啟索引鍵。
-   指定個人識別碼，以存取 [*智慧卡*](/windows/desktop/SecGloss/s-gly)上的私密金鑰。
-   指定或取出與金鑰相關聯的 CSP 名稱。
-   指定或取得金鑰的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 。

下列各節會識別 Xenroll.dll 所匯出的函式，該函式可用於管理 [*密碼編譯金鑰*](/windows/desktop/SecGloss/c-gly)。 每個主題也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [假如 useexistingkeyset](#useexistingkeyset)
-   [相關主題](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

Xenroll.dll 中的 [**ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) 函數會指定或抓取 [*金鑰容器*](/windows/desktop/SecGloss/k-gly)的名稱。

使用 CertEnroll.dll 時，您可以執行下列動作來取出金鑰容器的名稱：

1.  呼叫現有 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request)屬性。
2.  在步驟1傳回的要求上呼叫 [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) 方法，以取得最內層的要求。
3.  在步驟2所傳回的 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上呼叫 **QueryInterface** ，以轉換為 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件。
4.  呼叫 PKCS 10 要求上的 [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) 屬性 \# 。
5.  呼叫從步驟4取出的 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上的 [**容器**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername)屬性。

## <a name="genkeyflags"></a>GenKeyFlags

Xenroll.dll 中定義的 [**GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) 函數會指定或抓取用來產生私密金鑰或 [*公開/私密金鑰*](/windows/desktop/SecGloss/p-gly)組的旗標。

使用 CertEnroll.dll 時，您可以指定一些不同的屬性，這些屬性會決定如何建立私密金鑰。 如需詳細資訊，請參閱 [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create)。

## <a name="getkeylen"></a>GetKeyLen

Xenroll.dll 中定義的 [**GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) 函數會抓取加密金鑰的最大或最小金鑰大小。

使用 CertEnroll.dll 時，您可以呼叫 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)或 [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)物件的 [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length)屬性來取得金鑰大小（以位為單位）。

## <a name="getkeylenex"></a>GetKeyLenEx

Xenroll.dll 中定義的 [**GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) 函數會抓取加密金鑰的最大或最小金鑰大小或增量長度。

使用 CertEnroll.dll 時，您可以呼叫 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)或 [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)物件的 [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length)屬性來取得金鑰大小（以位為單位）。 如果演算法支援增量索引鍵長度，您可以呼叫 [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)物件上的 [**IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength)屬性，以取得遞增值。 您也可以呼叫 [**MinLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) 和 [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) 屬性來取得最小和最大金鑰大小。

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

Xenroll.dll 中定義的 [**GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) 函式會抓取值，指出 CSP 是否支援 exchange 金鑰、簽署金鑰或兩者。

使用 CertEnroll.dll 時，您可以呼叫 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)或 [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)物件上的 [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec)屬性，以取出金鑰所支援的作業。

## <a name="keyspec"></a>KeySpec

Xenroll.dll 中定義的 [**KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) 函數會指定或抓取索引鍵類型。

使用 CertEnroll.dll 時，您可以在 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上呼叫 [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec)屬性，以取得金鑰所支援的作業。

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

Xenroll.dll 中定義的 [**LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) 函式會指定或抓取布林值，指出加密金鑰是否只能用於資料或金鑰加密。

CertEnroll.dll 不包含此函數的直接對等專案。 不過，您可以指定 [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) 物件，並將它新增至憑證要求，以達到幾乎相等的結果。

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

Xenroll.dll 中定義的 [**PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) 函式會指定或抓取包含所匯出金鑰的檔案名。

使用 CertEnroll.dll 時，您可以在 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)物件上呼叫 [**export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export)方法，以將金鑰匯出至 **BSTR**。 您可以呼叫 [**ExportPublicKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) 方法來匯出非對稱金鑰組的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 部分。

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

Xenroll.dll 中定義的 [**ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) 函式會指定或抓取布林值，指出在產生新的索引鍵時，如果發生錯誤，是否重複使用現有的金鑰。

使用 CertEnroll.dll 時，您可以在 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件上呼叫 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate)方法，並指定 [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions)列舉型別的值，以重複使用現有的私密金鑰。

## <a name="useexistingkeyset"></a>假如 useexistingkeyset

Xenroll.dll 中定義的 [**假如 useexistingkeyset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) 函數會指定或抓取布林值，指出是否要使用現有的索引鍵。

使用 CertEnroll.dll 時，您可以在 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件上呼叫 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate)方法，並指定 [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions)列舉型別的值，以重複使用現有的私用和公開金鑰。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 

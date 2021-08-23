---
description: 本主題說明如何確認憑證支援特定的簽章方法。
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: 確認憑證支援簽章方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098710"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>確認憑證支援簽章方法

本主題說明如何確認憑證支援特定的簽章方法。

Microsoft 加密 API 中的 **CryptXmlEnumAlgorithmInfo** 會列舉憑證的屬性，並在此程式碼範例中用來列舉憑證支援的簽章方法。 若要使用 **CryptXmlEnumAlgorithmInfo** 來列舉憑證支援的簽章方法，呼叫端必須在 **CryptXmlEnumAlgorithmInfo** 的呼叫中提供回呼方法和資料結構，讓它能夠將資料傳遞給回呼方法。

下一個程式碼範例中使用的資料結構具有下欄欄位：

| 欄位                               | 描述                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | **LPWSTR** 欄位，指向包含要檢查之簽章演算法 URI 的字串。                             |
| **certificateAlgorithmInfo**        | **CRYPT \_ OID \_ 資訊** 結構的指標，其中包含憑證所支援之簽章演算法的相關資訊。 |
| **userSignatureAlgorithmSupported** | **布林** 值，指出憑證是否支援簽章演算法。                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



檢查憑證的密碼編譯 API 方法會使用回呼方法，將資料傳回給呼叫端。 **CryptXmlEnumAlgorithmInfo** 會列舉憑證支援的簽章方法，並呼叫每個簽章方法的回呼方法，直到回呼方法傳回 **FALSE** 或在憑證中的所有簽章方法都已列舉為止。

下一個程式碼範例中的回呼方法會搜尋 **CryptXmlEnumAlgorithmInfo** 傳入的簽章方法，以符合呼叫方法所提供的簽章方法。 找到相符的時，回呼方法會檢查系統是否也支援簽章方法。 如果簽章方法符合且受系統支援，則簽章方法會標示為系統支援，而且回呼方法會傳回 **FALSE**。


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



下列程式碼範例會將驗證功能包裝成單一方法。 這個方法會傳回 **布林** 值，指出憑證是否支援簽章方法，以及系統是否支援簽章方法。


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[從檔案載入憑證](load-a-certificate-from-a-file.md)
</dt> <dt>

[確認系統支援摘要式方法](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**在此範例中使用**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**CRYPT \_ OID \_ 資訊**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**詳細資訊**
</dt> <dt>

[密碼編譯 API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[密碼編譯函式](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

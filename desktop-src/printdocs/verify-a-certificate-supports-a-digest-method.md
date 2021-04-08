---
description: 本主題說明如何確認系統支援摘要式方法。
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: 確認系統支援摘要式方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851899"
---
# <a name="verify-the-system-supports-a-digest-method"></a>確認系統支援摘要式方法

本主題說明如何確認系統支援摘要式方法。

XPS 數位簽章會使用密碼編譯 API，其提供驗證系統是否支援特定摘要方法的方法。 若要使用加密 API 的 **CryptXmlEnumAlgorithmInfo** 函式來列舉系統所支援的摘要方法，呼叫端必須提供回呼方法和資料結構。 **CryptXmlEnumAlgorithmInfo** 函式會透過回呼方法，將列舉資料傳回到呼叫端。

此範例中使用的資料結構會顯示在下列程式碼範例中，並包含下欄欄位：

| 欄位                            | 描述                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | **LPWSTR** 欄位，指向包含要檢查之摘要演算法 URI 的字串。 |
| **userDigestAlgorithmSupported** | **布林** 值，指出憑證是否支援摘要演算法。           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



列舉摘要方法的密碼編譯 API 方法會使用回呼方法，將資料傳回給呼叫端。 **CryptXmlEnumAlgorithmInfo** 會列舉系統所支援的摘要方法，並針對它所列舉的每個摘要方法呼叫回呼方法，直到回呼方法傳回 **FALSE** ，或直到系統所支援的所有摘要方法都已列舉為止。 此範例中的回呼方法會比較 **CryptXmlEnumAlgorithmInfo** 所傳入的摘要方法與呼叫方法所提供的摘要方法。


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



下列程式碼範例會將驗證功能包裝成單一方法，這個方法會傳回 **布林** 值，指出系統是否支援 digest 方法。


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[從檔案載入憑證](load-a-certificate-from-a-file.md)
</dt> <dt>

[確認憑證支援簽章方法](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**在此範例中使用**
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

 

 

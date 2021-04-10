---
description: 本主題說明如何確認憑證支援特定的簽章方法。
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: 確認憑證支援簽章方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851896"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="1f641-103">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="1f641-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="1f641-104">本主題說明如何確認憑證支援特定的簽章方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="1f641-105">Microsoft 加密 API 中的 **CryptXmlEnumAlgorithmInfo** 會列舉憑證的屬性，並在此程式碼範例中用來列舉憑證支援的簽章方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="1f641-106">若要使用 **CryptXmlEnumAlgorithmInfo** 來列舉憑證支援的簽章方法，呼叫端必須在 **CryptXmlEnumAlgorithmInfo** 的呼叫中提供回呼方法和資料結構，讓它能夠將資料傳遞給回呼方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="1f641-107">下一個程式碼範例中使用的資料結構具有下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="1f641-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="1f641-108">欄位</span><span class="sxs-lookup"><span data-stu-id="1f641-108">Field</span></span>                               | <span data-ttu-id="1f641-109">描述</span><span class="sxs-lookup"><span data-stu-id="1f641-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f641-110">**userSignatureAlgorithmToCheck**</span><span class="sxs-lookup"><span data-stu-id="1f641-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="1f641-111">**LPWSTR** 欄位，指向包含要檢查之簽章演算法 URI 的字串。</span><span class="sxs-lookup"><span data-stu-id="1f641-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="1f641-112">**certificateAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="1f641-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="1f641-113">**CRYPT \_ OID \_ 資訊** 結構的指標，其中包含憑證所支援之簽章演算法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f641-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="1f641-114">**userSignatureAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="1f641-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="1f641-115">**布林** 值，指出憑證是否支援簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="1f641-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="1f641-116">檢查憑證的密碼編譯 API 方法會使用回呼方法，將資料傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="1f641-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="1f641-117">**CryptXmlEnumAlgorithmInfo** 會列舉憑證支援的簽章方法，並呼叫每個簽章方法的回呼方法，直到回呼方法傳回 **FALSE** 或在憑證中的所有簽章方法都已列舉為止。</span><span class="sxs-lookup"><span data-stu-id="1f641-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="1f641-118">下一個程式碼範例中的回呼方法會搜尋 **CryptXmlEnumAlgorithmInfo** 傳入的簽章方法，以符合呼叫方法所提供的簽章方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="1f641-119">找到相符的時，回呼方法會檢查系統是否也支援簽章方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="1f641-120">如果簽章方法符合且受系統支援，則簽章方法會標示為系統支援，而且回呼方法會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1f641-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


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



<span data-ttu-id="1f641-121">下列程式碼範例會將驗證功能包裝成單一方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="1f641-122">這個方法會傳回 **布林** 值，指出憑證是否支援簽章方法，以及系統是否支援簽章方法。</span><span class="sxs-lookup"><span data-stu-id="1f641-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1f641-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f641-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1f641-124">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="1f641-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="1f641-125">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="1f641-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="1f641-126">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="1f641-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="1f641-127">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="1f641-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="1f641-128">**在此範例中使用**</span><span class="sxs-lookup"><span data-stu-id="1f641-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="1f641-129">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="1f641-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="1f641-130">**CRYPT \_ OID \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1f641-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="1f641-131">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="1f641-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="1f641-132">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="1f641-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="1f641-133">密碼編譯 API</span><span class="sxs-lookup"><span data-stu-id="1f641-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="1f641-134">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="1f641-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="1f641-135">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="1f641-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="1f641-136">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="1f641-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="1f641-137">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="1f641-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

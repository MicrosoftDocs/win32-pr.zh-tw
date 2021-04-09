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
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="d4ba1-103">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="d4ba1-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="d4ba1-104">本主題說明如何確認系統支援摘要式方法。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="d4ba1-105">XPS 數位簽章會使用密碼編譯 API，其提供驗證系統是否支援特定摘要方法的方法。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="d4ba1-106">若要使用加密 API 的 **CryptXmlEnumAlgorithmInfo** 函式來列舉系統所支援的摘要方法，呼叫端必須提供回呼方法和資料結構。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="d4ba1-107">**CryptXmlEnumAlgorithmInfo** 函式會透過回呼方法，將列舉資料傳回到呼叫端。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="d4ba1-108">此範例中使用的資料結構會顯示在下列程式碼範例中，並包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="d4ba1-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="d4ba1-109">欄位</span><span class="sxs-lookup"><span data-stu-id="d4ba1-109">Field</span></span>                            | <span data-ttu-id="d4ba1-110">描述</span><span class="sxs-lookup"><span data-stu-id="d4ba1-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ba1-111">**userDigestAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="d4ba1-112">**LPWSTR** 欄位，指向包含要檢查之摘要演算法 URI 的字串。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="d4ba1-113">**userDigestAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="d4ba1-114">**布林** 值，指出憑證是否支援摘要演算法。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="d4ba1-115">列舉摘要方法的密碼編譯 API 方法會使用回呼方法，將資料傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="d4ba1-116">**CryptXmlEnumAlgorithmInfo** 會列舉系統所支援的摘要方法，並針對它所列舉的每個摘要方法呼叫回呼方法，直到回呼方法傳回 **FALSE** ，或直到系統所支援的所有摘要方法都已列舉為止。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="d4ba1-117">此範例中的回呼方法會比較 **CryptXmlEnumAlgorithmInfo** 所傳入的摘要方法與呼叫方法所提供的摘要方法。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


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



<span data-ttu-id="d4ba1-118">下列程式碼範例會將驗證功能包裝成單一方法，這個方法會傳回 **布林** 值，指出系統是否支援 digest 方法。</span><span class="sxs-lookup"><span data-stu-id="d4ba1-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d4ba1-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4ba1-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d4ba1-120">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="d4ba1-121">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="d4ba1-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="d4ba1-122">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="d4ba1-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="d4ba1-123">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="d4ba1-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="d4ba1-124">**在此範例中使用**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="d4ba1-125">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="d4ba1-126">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="d4ba1-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="d4ba1-127">密碼編譯 API</span><span class="sxs-lookup"><span data-stu-id="d4ba1-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="d4ba1-128">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="d4ba1-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="d4ba1-129">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="d4ba1-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="d4ba1-130">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="d4ba1-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="d4ba1-131">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="d4ba1-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

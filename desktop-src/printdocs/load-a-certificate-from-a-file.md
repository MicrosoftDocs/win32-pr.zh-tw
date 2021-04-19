---
description: 本主題說明如何從憑證檔案載入憑證。
ms.assetid: 60cced55-9fcc-4fce-a462-7abf3f4466f0
title: 從檔案載入憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c708fb042ccdf4acd43986de1404f9ccb266148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971610"
---
# <a name="load-a-certificate-from-a-file"></a><span data-ttu-id="88a22-103">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="88a22-103">Load a Certificate from a File</span></span>

<span data-ttu-id="88a22-104">本主題說明如何從憑證檔案載入憑證。</span><span class="sxs-lookup"><span data-stu-id="88a22-104">This topic describes how to load a certificate from a certificate file.</span></span>

<span data-ttu-id="88a22-105">從憑證檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="88a22-105">To load a certificate from a certificate file</span></span>

1.  <span data-ttu-id="88a22-106">開啟憑證檔案以進行讀取存取。</span><span class="sxs-lookup"><span data-stu-id="88a22-106">Open the certificate file for read access.</span></span>
2.  <span data-ttu-id="88a22-107">將憑證檔案的內容讀入憑證緩衝區。</span><span class="sxs-lookup"><span data-stu-id="88a22-107">Read the contents of the certificate file into the certificate buffer.</span></span>
3.  <span data-ttu-id="88a22-108">使用緩衝區的內容建立憑證。</span><span class="sxs-lookup"><span data-stu-id="88a22-108">Create a certificate using the contents of the buffer.</span></span>


```C++
// In the interest of simplicity, this example
//  uses a fixed-length buffer to hold the certificate. 
// A more robust solution would be to query the size
//  of the certificate file and dynamically
//  allocate a buffer of that size or greater.
#define CERTIFICATE_BUFFER_SIZE 1024

HRESULT  hr                  = S_OK;
BYTE     certEncoded[CERTIFICATE_BUFFER_SIZE] = {0};
DWORD    certEncodedSize     = 0L;
HANDLE   certFileHandle      = NULL;
BOOL     result              = FALSE;

// open the certificate file
certFileHandle = CreateFile(certFile, 
    GENERIC_READ, 
    0, 
    NULL, 
    OPEN_EXISTING, 
    FILE_ATTRIBUTE_NORMAL, 
    NULL);
if (INVALID_HANDLE_VALUE == certFileHandle) {
    hr = HRESULT_FROM_WIN32(GetLastError());
}

if (SUCCEEDED(hr)) {
    // if the buffer is large enough
    //  read the certificate file into the buffer
    if (GetFileSize (certFileHandle, NULL) <= CERTIFICATE_BUFFER_SIZE) {
        result = ReadFile(certFileHandle, 
            certEncoded, 
            CERTIFICATE_BUFFER_SIZE, 
            &certEncodedSize, 
            NULL);
        if (!result) {
            // the read failed, return the error as an HRESULT
            hr = HRESULT_FROM_WIN32(GetLastError());
        } else {
            hr = S_OK;
        }
    } else {
        // The certificate file is larger than the allocated buffer.
        //  To handle this error, you could dynamically allocate
        //  the certificate buffer based on the file size returned or 
        //  use a larger static buffer.
        hr = HRESULT_FROM_WIN32(ERROR_MORE_DATA);
    }    
}
if (SUCCEEDED(hr))
{
    // create a certificate from the contents of the buffer
    *cert = CertCreateCertificateContext(X509_ASN_ENCODING, 
        certEncoded, 
        certEncodedSize);
    if (!(*cert)) {
        hr = HRESULT_FROM_WIN32(GetLastError());
        CloseHandle(certFileHandle);
        hr = E_FAIL;
    } else {
        hr = S_OK;
    }
}
// close the certificate file
if (NULL != certFileHandle) CloseHandle(certFileHandle);
```



## <a name="related-topics"></a><span data-ttu-id="88a22-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="88a22-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="88a22-110">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="88a22-110">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="88a22-111">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="88a22-111">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="88a22-112">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="88a22-112">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="88a22-113">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="88a22-113">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="88a22-114">**在此範例中使用**</span><span class="sxs-lookup"><span data-stu-id="88a22-114">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="88a22-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="88a22-115">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="88a22-116">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="88a22-116">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="88a22-117">**CertCreateCertificateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="88a22-117">**CertCreateCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
</dt> <dt>

<span data-ttu-id="88a22-118">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="88a22-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="88a22-119">密碼編譯 API</span><span class="sxs-lookup"><span data-stu-id="88a22-119">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="88a22-120">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="88a22-120">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="88a22-121">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="88a22-121">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="88a22-122">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="88a22-122">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="88a22-123">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="88a22-123">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

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
# <a name="load-a-certificate-from-a-file"></a>從檔案載入憑證

本主題說明如何從憑證檔案載入憑證。

從憑證檔案載入憑證

1.  開啟憑證檔案以進行讀取存取。
2.  將憑證檔案的內容讀入憑證緩衝區。
3.  使用緩衝區的內容建立憑證。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[確認系統支援摘要式方法](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[確認憑證支援簽章方法](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**在此範例中使用**
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[**CertCreateCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
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

 

 

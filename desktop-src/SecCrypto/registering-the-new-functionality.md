---
description: 新的 DLL 中必須提供在系統登錄中註冊新功能的支援，以及新的函式。
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: 註冊新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5d56153199542c11f00a3ec23d90d35a682c5fe93f91d2978dcd4f72628219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900593"
---
# <a name="registering-the-new-functionality"></a>註冊新功能

新的 DLL 中必須提供在系統登錄中註冊新功能的支援，以及新的函式。 [OID 支援函數](cryptography-functions.md) 可提供此註冊的協助。 Regsvr32.exe 會註冊新的函式。 此工具隨附于 Windows。

新的 DLL 必須提供 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 進入點，以供 Regsvr32.exe 使用。 [*CryptoAPI*](../secgloss/c-gly.md) 函式（例如 [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) 或 [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)）可以在這些進入點內使用，如下列範例所示。


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



此範例必須編譯並連結至新的 DLL。 您必須匯出這兩個進入點以及函式進入點。

若要在電腦上安裝新功能，請從命令提示字元執行 Regsvr32.exe，並指定新 DLL 的名稱和路徑。 Regsvr32.exe 透過 [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85))函式進入點存取 [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)函式，並註冊新的函式和 DLL。

 

 

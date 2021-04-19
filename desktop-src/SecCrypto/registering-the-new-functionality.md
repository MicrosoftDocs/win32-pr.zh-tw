---
description: 新的 DLL 中必須提供在系統登錄中註冊新功能的支援，以及新的函式。
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: 註冊新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985090"
---
# <a name="registering-the-new-functionality"></a><span data-ttu-id="556c3-103">註冊新功能</span><span class="sxs-lookup"><span data-stu-id="556c3-103">Registering the New Functionality</span></span>

<span data-ttu-id="556c3-104">新的 DLL 中必須提供在系統登錄中註冊新功能的支援，以及新的函式。</span><span class="sxs-lookup"><span data-stu-id="556c3-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="556c3-105">[OID 支援函數](cryptography-functions.md) 可提供此註冊的協助。</span><span class="sxs-lookup"><span data-stu-id="556c3-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="556c3-106">Regsvr32.exe 會註冊新的函式。</span><span class="sxs-lookup"><span data-stu-id="556c3-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="556c3-107">此工具隨附于 Windows。</span><span class="sxs-lookup"><span data-stu-id="556c3-107">This tool is included with Windows.</span></span>

<span data-ttu-id="556c3-108">新的 DLL 必須提供 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 進入點，以供 Regsvr32.exe 使用。</span><span class="sxs-lookup"><span data-stu-id="556c3-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="556c3-109">[*CryptoAPI*](../secgloss/c-gly.md) 函式（例如 [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) 或 [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)）可以在這些進入點內使用，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="556c3-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


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



<span data-ttu-id="556c3-110">此範例必須編譯並連結至新的 DLL。</span><span class="sxs-lookup"><span data-stu-id="556c3-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="556c3-111">您必須匯出這兩個進入點以及函式進入點。</span><span class="sxs-lookup"><span data-stu-id="556c3-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="556c3-112">若要在電腦上安裝新功能，請從命令提示字元執行 Regsvr32.exe，並指定新 DLL 的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="556c3-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="556c3-113">Regsvr32.exe 透過 [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85))函式進入點存取 [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)函式，並註冊新的函式和 DLL。</span><span class="sxs-lookup"><span data-stu-id="556c3-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 

---
description: 匯入驅動程式公開金鑰
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: 匯入驅動程式公開金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846499"
---
# <a name="importing-the-drivers-public-key"></a><span data-ttu-id="18fe7-103">匯入驅動程式公開金鑰</span><span class="sxs-lookup"><span data-stu-id="18fe7-103">Importing the Drivers Public Key</span></span>

<span data-ttu-id="18fe7-104">驅動程式的 RSA 公開金鑰包含在憑證之分葉節點的模數和指數標記中。</span><span class="sxs-lookup"><span data-stu-id="18fe7-104">The driver's RSA public key is contained in the Modulus and Exponent tags of the certificate's leaf node.</span></span> <span data-ttu-id="18fe7-105">這兩個值都是以 base64 編碼，而且必須進行解碼。</span><span class="sxs-lookup"><span data-stu-id="18fe7-105">Both values are base64-encoded and must be decoded.</span></span> <span data-ttu-id="18fe7-106">如果您使用的是 Microsoft CryptoAPI，必須將金鑰匯入密碼編譯服務提供者 (CSP) ，也就是執行密碼編譯演算法的模組。</span><span class="sxs-lookup"><span data-stu-id="18fe7-106">If you are using Microsoft's CryptoAPI, you must import the key into a cryptographic service provider (CSP), which is the module that implements the cryptographic algorithms.</span></span>

<span data-ttu-id="18fe7-107">若要將來自 base64 編碼的模數和指數轉換成二進位陣列，請使用 **CryptStringToBinary** 函式，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="18fe7-107">To convert the modulus and exponents from base64 encoding to binary arrays, use the **CryptStringToBinary** function, as shown in the following code.</span></span> <span data-ttu-id="18fe7-108">呼叫函數一次，以取得位元組陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="18fe7-108">Call the function once to get the size of the byte array.</span></span> <span data-ttu-id="18fe7-109">然後配置緩衝區，並再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="18fe7-109">Then allocate the buffer and call the function again.</span></span>


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



<span data-ttu-id="18fe7-110">Base64 編碼的陣列是以大到小的順序，而 CryptoAPI 預期的數位是以位元組由小到大的順序，所以您需要交換從 **CryptStringToBinary** 傳回的陣列位元組順序。</span><span class="sxs-lookup"><span data-stu-id="18fe7-110">The base64-encoded array is in big-endian order, whereas the CryptoAPI expects the number in little-endian order, so you need to swap the byte order of the array that is returned from **CryptStringToBinary**.</span></span> <span data-ttu-id="18fe7-111">模數為256個位元組，但已解碼的位元組陣列可能小於256個位元組。</span><span class="sxs-lookup"><span data-stu-id="18fe7-111">The modulus is 256 bytes, but the decoded byte array might be less than 256 bytes.</span></span> <span data-ttu-id="18fe7-112">若是如此，您將需要配置256個位元組的新陣列、將資料複製到新的陣列，並以零填補陣列的前方。</span><span class="sxs-lookup"><span data-stu-id="18fe7-112">If so, you will need to allocate a new array that is 256 bytes, copy the data into the new array, and pad the front of the array with zeros.</span></span> <span data-ttu-id="18fe7-113">指數是 DWORD (4 位元組的) 值。</span><span class="sxs-lookup"><span data-stu-id="18fe7-113">The exponent is a DWORD (4-byte) value.</span></span>

<span data-ttu-id="18fe7-114">取得模數和指數值之後，您可以將金鑰匯入預設密碼編譯服務提供者 (CSP) ，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="18fe7-114">After you have the modulus and exponent values, you can import the key into the default cryptographic service provider (CSP), as shown in the following code:</span></span>


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



<span data-ttu-id="18fe7-115">現在您可以使用 CryptoAPI，利用驅動程式的公開金鑰來加密命令和狀態要求。</span><span class="sxs-lookup"><span data-stu-id="18fe7-115">Now you can use the CryptoAPI to encrypt commands and status requests with the driver's public key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18fe7-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="18fe7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18fe7-117">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="18fe7-117">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




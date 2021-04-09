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
# <a name="importing-the-drivers-public-key"></a>匯入驅動程式公開金鑰

驅動程式的 RSA 公開金鑰包含在憑證之分葉節點的模數和指數標記中。 這兩個值都是以 base64 編碼，而且必須進行解碼。 如果您使用的是 Microsoft CryptoAPI，必須將金鑰匯入密碼編譯服務提供者 (CSP) ，也就是執行密碼編譯演算法的模組。

若要將來自 base64 編碼的模數和指數轉換成二進位陣列，請使用 **CryptStringToBinary** 函式，如下列程式碼所示。 呼叫函數一次，以取得位元組陣列的大小。 然後配置緩衝區，並再次呼叫函式。


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



Base64 編碼的陣列是以大到小的順序，而 CryptoAPI 預期的數位是以位元組由小到大的順序，所以您需要交換從 **CryptStringToBinary** 傳回的陣列位元組順序。 模數為256個位元組，但已解碼的位元組陣列可能小於256個位元組。 若是如此，您將需要配置256個位元組的新陣列、將資料複製到新的陣列，並以零填補陣列的前方。 指數是 DWORD (4 位元組的) 值。

取得模數和指數值之後，您可以將金鑰匯入預設密碼編譯服務提供者 (CSP) ，如下列程式碼所示：


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



現在您可以使用 CryptoAPI，利用驅動程式的公開金鑰來加密命令和狀態要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




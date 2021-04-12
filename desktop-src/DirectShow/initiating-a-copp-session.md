---
description: 起始 COPP 會話
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: 起始 COPP 會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109557"
---
# <a name="initiating-a-copp-session"></a>起始 COPP 會話

若要 (COPP) 會話起始經認證的輸出保護通訊協定，您必須準備簽 *章，這* 是包含下列數位串連的陣列：

-   驅動程式傳回的128位亂數字。  (此值會顯示為 [取得驅動程式憑證鏈](obtaining-the-drivers-certificate-chain.md)的 *guidRandom* 。 ) 
-   128位對稱 AES 金鑰。
-   狀態要求的32位起始序號。
-   COPP 命令的32位起始序號。

產生對稱 AES 金鑰，如下所示：


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



**CryptGenKey** 函式會建立對稱金鑰，但金鑰仍會保留在 CSP 中。 若要將金鑰匯出至位元組陣列，請使用 **CryptExportKey** 函數。 這是在 \_ 呼叫 **CryptGenKey** 時使用 CRYPT 可匯出旗標的原因。 下列程式碼會匯出金鑰，並將它複製到


```
pData
```



陣列。


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



傳回的資料


```
pData
```



具有下列版面配置：


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



不過，在 CryptoAPI 標頭中不會定義符合此版面配置的結構。 您可以定義一個或進行一些指標算術。 例如，若要驗證金鑰的大小：


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



若要取得金鑰本身的指標：


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



接下來，產生32位的亂數字作為 COPP 狀態要求的起始順序。 建立亂數字的建議方式是呼叫 **CryptGenRandom** 函數。 請勿在 C 執行時間程式庫中使用 **rand** 函式，因為它並不是真正的隨機函數。 產生第二個32位亂數字，作為 COPP 命令的起始順序使用。


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



現在您可以準備 COPP 簽章。 這是256位元組陣列，定義為 [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) 結構。 將陣列的內容初始化為零。 然後，將四個數字複製到陣列中，也就是驅動程式的亂數、AES 金鑰、狀態序號，以及命令序號（依該順序）。 最後，交換整個陣列的位元組順序。

根據 **CryptEncrypt** 的檔：

<dl> 「使用 RSA 金鑰呼叫 **CryptEncrypt** 時，可以加密的純文字資料長度是索引鍵模數減去11個位元組的長度。 第11個位元組是針對 PKCS 1 填補所選擇的最小值 \# 。」  
</dl>

在此情況下，模數為256個位元組，因此最大訊息長度是245位元組 (256 – 11) 。 **AMCOPPSignature** 結構是256個位元組，但簽章中有意義的資料只是40個位元組。 下列程式碼會加密簽章，並在中提供結果。


```
CoppSig
```



.


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



現在將加密的陣列傳遞給 [**IAMCertifiedOutputProtection：： SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart)：


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



如果此方法成功，您就可以將 COPP 命令和狀態要求傳送至驅動程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




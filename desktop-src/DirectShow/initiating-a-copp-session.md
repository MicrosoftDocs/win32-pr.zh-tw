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
# <a name="initiating-a-copp-session"></a><span data-ttu-id="3a083-103">起始 COPP 會話</span><span class="sxs-lookup"><span data-stu-id="3a083-103">Initiating a COPP Session</span></span>

<span data-ttu-id="3a083-104">若要 (COPP) 會話起始經認證的輸出保護通訊協定，您必須準備簽 *章，這* 是包含下列數位串連的陣列：</span><span class="sxs-lookup"><span data-stu-id="3a083-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="3a083-105">驅動程式傳回的128位亂數字。</span><span class="sxs-lookup"><span data-stu-id="3a083-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="3a083-106"> (此值會顯示為 [取得驅動程式憑證鏈](obtaining-the-drivers-certificate-chain.md)的 *guidRandom* 。 ) </span><span class="sxs-lookup"><span data-stu-id="3a083-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="3a083-107">128位對稱 AES 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3a083-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="3a083-108">狀態要求的32位起始序號。</span><span class="sxs-lookup"><span data-stu-id="3a083-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="3a083-109">COPP 命令的32位起始序號。</span><span class="sxs-lookup"><span data-stu-id="3a083-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="3a083-110">產生對稱 AES 金鑰，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3a083-110">Generate a symmetric AES key as follows:</span></span>


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



<span data-ttu-id="3a083-111">**CryptGenKey** 函式會建立對稱金鑰，但金鑰仍會保留在 CSP 中。</span><span class="sxs-lookup"><span data-stu-id="3a083-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="3a083-112">若要將金鑰匯出至位元組陣列，請使用 **CryptExportKey** 函數。</span><span class="sxs-lookup"><span data-stu-id="3a083-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="3a083-113">這是在 \_ 呼叫 **CryptGenKey** 時使用 CRYPT 可匯出旗標的原因。</span><span class="sxs-lookup"><span data-stu-id="3a083-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="3a083-114">下列程式碼會匯出金鑰，並將它複製到</span><span class="sxs-lookup"><span data-stu-id="3a083-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="3a083-115">陣列。</span><span class="sxs-lookup"><span data-stu-id="3a083-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="3a083-116">傳回的資料</span><span class="sxs-lookup"><span data-stu-id="3a083-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="3a083-117">具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="3a083-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="3a083-118">不過，在 CryptoAPI 標頭中不會定義符合此版面配置的結構。</span><span class="sxs-lookup"><span data-stu-id="3a083-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="3a083-119">您可以定義一個或進行一些指標算術。</span><span class="sxs-lookup"><span data-stu-id="3a083-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="3a083-120">例如，若要驗證金鑰的大小：</span><span class="sxs-lookup"><span data-stu-id="3a083-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="3a083-121">若要取得金鑰本身的指標：</span><span class="sxs-lookup"><span data-stu-id="3a083-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="3a083-122">接下來，產生32位的亂數字作為 COPP 狀態要求的起始順序。</span><span class="sxs-lookup"><span data-stu-id="3a083-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="3a083-123">建立亂數字的建議方式是呼叫 **CryptGenRandom** 函數。</span><span class="sxs-lookup"><span data-stu-id="3a083-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="3a083-124">請勿在 C 執行時間程式庫中使用 **rand** 函式，因為它並不是真正的隨機函數。</span><span class="sxs-lookup"><span data-stu-id="3a083-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="3a083-125">產生第二個32位亂數字，作為 COPP 命令的起始順序使用。</span><span class="sxs-lookup"><span data-stu-id="3a083-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="3a083-126">現在您可以準備 COPP 簽章。</span><span class="sxs-lookup"><span data-stu-id="3a083-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="3a083-127">這是256位元組陣列，定義為 [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) 結構。</span><span class="sxs-lookup"><span data-stu-id="3a083-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="3a083-128">將陣列的內容初始化為零。</span><span class="sxs-lookup"><span data-stu-id="3a083-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="3a083-129">然後，將四個數字複製到陣列中，也就是驅動程式的亂數、AES 金鑰、狀態序號，以及命令序號（依該順序）。</span><span class="sxs-lookup"><span data-stu-id="3a083-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="3a083-130">最後，交換整個陣列的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="3a083-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="3a083-131">根據 **CryptEncrypt** 的檔：</span><span class="sxs-lookup"><span data-stu-id="3a083-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="3a083-132">「使用 RSA 金鑰呼叫 **CryptEncrypt** 時，可以加密的純文字資料長度是索引鍵模數減去11個位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="3a083-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="3a083-133">第11個位元組是針對 PKCS 1 填補所選擇的最小值 \# 。」</span><span class="sxs-lookup"><span data-stu-id="3a083-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="3a083-134">在此情況下，模數為256個位元組，因此最大訊息長度是245位元組 (256 – 11) 。</span><span class="sxs-lookup"><span data-stu-id="3a083-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="3a083-135">**AMCOPPSignature** 結構是256個位元組，但簽章中有意義的資料只是40個位元組。</span><span class="sxs-lookup"><span data-stu-id="3a083-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="3a083-136">下列程式碼會加密簽章，並在中提供結果。</span><span class="sxs-lookup"><span data-stu-id="3a083-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="3a083-137">.</span><span class="sxs-lookup"><span data-stu-id="3a083-137">.</span></span>


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



<span data-ttu-id="3a083-138">現在將加密的陣列傳遞給 [**IAMCertifiedOutputProtection：： SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart)：</span><span class="sxs-lookup"><span data-stu-id="3a083-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="3a083-139">如果此方法成功，您就可以將 COPP 命令和狀態要求傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3a083-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a083-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a083-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a083-141">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="3a083-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




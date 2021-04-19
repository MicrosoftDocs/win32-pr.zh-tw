---
description: 完成的訊息會在變更加密規格訊息之後立即傳送，以確認金鑰交換和驗證程式是否成功。
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: 在 TLS 1.0 通訊協定中完成訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990376"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="38007-103">在 TLS 1.0 通訊協定中完成訊息</span><span class="sxs-lookup"><span data-stu-id="38007-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="38007-104">完成的訊息會在變更加密規格訊息之後立即傳送，以確認金鑰交換和驗證程式是否成功。</span><span class="sxs-lookup"><span data-stu-id="38007-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="38007-105">TLS 1.0 通訊協定中的完成訊息會使用 [*虛擬隨機函式*](../secgloss/p-gly.md) 來計算， (PRF) ，其中包含 [*主要金鑰*](../secgloss/m-gly.md)、標籤和種子做為輸入。</span><span class="sxs-lookup"><span data-stu-id="38007-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="38007-106">PRF 會產生任意長度的輸出。</span><span class="sxs-lookup"><span data-stu-id="38007-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="38007-107">下列方法可用來產生 TLS 1.0 完成訊息中使用的 PRF 輸出。</span><span class="sxs-lookup"><span data-stu-id="38007-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="38007-108">使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)來產生 PRF [*雜湊*](../secgloss/h-gly.md)控制碼，並將 **ALG \_ 識別碼** 值設定為 CALG \_ TLS1PRF，並將控制碼傳遞至 *hKey* 參數中傳遞的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="38007-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="38007-109">在使用 CryptSetHashParam 函式的 DwParam 參數中，每個在雜湊控制碼上分別使用值 HP \_ TLS1PRF \_ LABEL 和 HP \_ TLS1PRF \_ seed  [](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)來設定標籤和種子值。</span><span class="sxs-lookup"><span data-stu-id="38007-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="38007-110">最後，通訊協定引擎會使用 DwParam 參數中的值 HP HASHVAL 來呼叫函數 [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) \_ ，以抓取要包含在完成訊息中的 PRF 資料。</span><span class="sxs-lookup"><span data-stu-id="38007-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="38007-111">對 **CryptGetHashParam** 進行呼叫時，通訊協定引擎必須指定要產生的資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="38007-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="38007-112">這是在 *pdwDataLen* 參數中完成，而產生的資料會放在 *>pbdata* 參數所指向的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="38007-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="38007-113">以下是此通訊協定引擎的一般原始程式碼：</span><span class="sxs-lookup"><span data-stu-id="38007-113">The following is typical source code for this protocol engine:</span></span>


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 

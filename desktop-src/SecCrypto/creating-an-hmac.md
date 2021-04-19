---
description: 說明如何建立 HMAC。
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: 建立 HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974512"
---
# <a name="creating-an-hmac"></a><span data-ttu-id="7f88e-103">建立 HMAC</span><span class="sxs-lookup"><span data-stu-id="7f88e-103">Creating an HMAC</span></span>

<span data-ttu-id="7f88e-104">**計算 HMAC**</span><span class="sxs-lookup"><span data-stu-id="7f88e-104">**To compute an HMAC**</span></span>

1.  <span data-ttu-id="7f88e-105">藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)，取得 Microsoft [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的指標。</span><span class="sxs-lookup"><span data-stu-id="7f88e-105">Get a pointer to the Microsoft [*Cryptographic Service Provider*](../secgloss/c-gly.md) (CSP) by calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
2.  <span data-ttu-id="7f88e-106">藉由呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)來建立 [*HMAC*](../secgloss/h-gly.md)[*雜湊物件*](../secgloss/h-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7f88e-106">Create a handle to an [*HMAC*](../secgloss/h-gly.md)[*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="7f88e-107">\_在 *Algid* 參數中傳遞 CALG HMAC。</span><span class="sxs-lookup"><span data-stu-id="7f88e-107">Pass CALG\_HMAC in the *Algid* parameter.</span></span> <span data-ttu-id="7f88e-108">在 *hKey* 參數中傳遞 [*對稱金鑰*](../secgloss/s-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7f88e-108">Pass the handle of a [*symmetric key*](../secgloss/s-gly.md) in the *hKey* parameter.</span></span> <span data-ttu-id="7f88e-109">此對稱金鑰是用來計算 HMAC 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f88e-109">This symmetric key is the key used to compute the HMAC.</span></span>
3.  <span data-ttu-id="7f88e-110">藉由呼叫 [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) ，並將 *dwParam* 參數設定為 [HP HMAC 資訊] 值，以指定要使用的雜湊類型 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7f88e-110">Specify the type of hash to be used by calling [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) with the *dwParam* parameter set to the value HP\_HMAC\_INFO.</span></span> <span data-ttu-id="7f88e-111">*>pbdata* 參數必須指向已初始化的 [**HMAC \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info)結構。</span><span class="sxs-lookup"><span data-stu-id="7f88e-111">The *pbData* parameter must point to an initialized [**HMAC\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) structure.</span></span>
4.  <span data-ttu-id="7f88e-112">呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) 以開始計算資料的 HMAC。</span><span class="sxs-lookup"><span data-stu-id="7f88e-112">Call [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) to begin computing the HMAC of the data.</span></span> <span data-ttu-id="7f88e-113">第一次呼叫 **CryptHashData** 時，會使用 XOR 運算子搭配內部字串和資料來結合索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="7f88e-113">The first call to **CryptHashData** causes the key value to be combined using the XOR operator with the inner string and the data.</span></span> <span data-ttu-id="7f88e-114">XOR 運算的結果會經過雜湊處理，然後在對) **CryptHashData** 的呼叫中傳遞的 *>pbdata* 參數所指向的 HMAC (的目標資料會雜湊處理。</span><span class="sxs-lookup"><span data-stu-id="7f88e-114">The result of the XOR operation is hashed, and then the target data for the HMAC (pointed to by the *pbData* parameter passed in the call to **CryptHashData**) is hashed.</span></span> <span data-ttu-id="7f88e-115">如有必要，您可以接著對 **CryptHashData** 進行後續的呼叫，以完成目標資料的雜湊。</span><span class="sxs-lookup"><span data-stu-id="7f88e-115">If necessary, subsequent calls to **CryptHashData** may then be made to finish the hashing of the target data.</span></span>
5.  <span data-ttu-id="7f88e-116">使用設定為 HP HASHVAL 的 *dwParam* 參數呼叫 [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) \_ 。</span><span class="sxs-lookup"><span data-stu-id="7f88e-116">Call [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the *dwParam* parameter set to HP\_HASHVAL.</span></span> <span data-ttu-id="7f88e-117">此呼叫會導致內部雜湊完成，並使用 XOR 搭配索引鍵來結合外部字串。</span><span class="sxs-lookup"><span data-stu-id="7f88e-117">This call causes the inner hash to be finished and the outer string to be combined using XOR with the key.</span></span> <span data-ttu-id="7f88e-118">XOR 運算的結果會經過雜湊處理，然後在上一個步驟中完成的內部雜湊 (結果) 雜湊。</span><span class="sxs-lookup"><span data-stu-id="7f88e-118">The result of the XOR operation is hashed, and then the result of the inner hash (completed in the previous step) is hashed.</span></span> <span data-ttu-id="7f88e-119">外部雜湊接著會完成，並在 *>pbdata* 參數和 *dwDataLen* 參數中的長度傳回。</span><span class="sxs-lookup"><span data-stu-id="7f88e-119">The outer hash is then finished and returned in the *pbData* parameter and the length in the *dwDataLen* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="7f88e-120">請勿將相同的 [*對稱*](../secgloss/s-gly.md) ([*會話*](../secgloss/s-gly.md)) 金鑰用於訊息加密和 [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 產生。</span><span class="sxs-lookup"><span data-stu-id="7f88e-120">Do not use the same [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key for both message encryption and [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) generation.</span></span> <span data-ttu-id="7f88e-121">使用相同的金鑰會大幅增加攻擊者解碼訊息的風險。</span><span class="sxs-lookup"><span data-stu-id="7f88e-121">Using the same key for both greatly increases the risk of messages being decoded by attackers.</span></span>

 

 

 

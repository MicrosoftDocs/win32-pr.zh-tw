---
description: 說明如何建立 CALG \_ SSL3 \_ SHAMD5 hash。
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: 建立 CALG_SSL3_SHAMD5 雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996811"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="50776-103">建立 CALG \_ SSL3 \_ SHAMD5 雜湊</span><span class="sxs-lookup"><span data-stu-id="50776-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="50776-104">**若要建立 CALG \_ SSL3 \_ SHAMD5 雜湊**</span><span class="sxs-lookup"><span data-stu-id="50776-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="50776-105">使用標準 CryptoAPI 方法，同時建立 MD5 和目標資料的 [*SHA*](../secgloss/s-gly.md) [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="50776-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="50776-106">串連兩個雜湊，最左邊的 MD5 值和 SHA 值。</span><span class="sxs-lookup"><span data-stu-id="50776-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="50776-107">這會產生36個位元組值 (16 個位元組 + 20 個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="50776-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="50776-108">藉由呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG SSL3 SHAMD5 傳入 Algid 參數，取得 [*雜湊物件*](../secgloss/h-gly.md)的控制碼 \_ \_ 。 </span><span class="sxs-lookup"><span data-stu-id="50776-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="50776-109">使用 [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)的呼叫來設定雜湊值。</span><span class="sxs-lookup"><span data-stu-id="50776-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="50776-110">串連的雜湊值會在 >pbdata 參數中當作 **位元組** 傳遞 \* ，且 \_ 必須在 *dwParam* 參數中傳遞 HP HASHVAL 值。</span><span class="sxs-lookup"><span data-stu-id="50776-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="50776-111">在步驟3中使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)所傳回的控制碼呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)將會失敗。</span><span class="sxs-lookup"><span data-stu-id="50776-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="50776-112">呼叫 [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) 以產生簽章。</span><span class="sxs-lookup"><span data-stu-id="50776-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="50776-113">呼叫 [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) 終結雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="50776-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 

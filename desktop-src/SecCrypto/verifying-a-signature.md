---
description: 若要驗證簽章，請使用 CryptCreateHash 建立雜湊物件。 此雜湊物件會累積要驗證的資料。 然後使用 CryptHashData 函式，將資料新增至雜湊物件。
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: 驗證簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114109"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="9ca09-105">驗證簽章</span><span class="sxs-lookup"><span data-stu-id="9ca09-105">Verifying a Signature</span></span>

<span data-ttu-id="9ca09-106">若要驗證簽章，請使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)建立 [*雜湊物件*](../secgloss/h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="9ca09-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="9ca09-107">此雜湊物件會累積要驗證的資料。</span><span class="sxs-lookup"><span data-stu-id="9ca09-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="9ca09-108">然後使用 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) 函式，將資料新增至雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="9ca09-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="9ca09-109">將最後一個資料區塊新增至雜湊之後，請使用 [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) 來驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="9ca09-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="9ca09-110">簽章資料的位址、雜湊物件的控制碼，以及公開金鑰的控制碼都會傳遞至 **CryptVerifySignature**。</span><span class="sxs-lookup"><span data-stu-id="9ca09-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="9ca09-111">當簽章經過驗證 (或驗證) 失敗之後，請使用 [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) 函式終結雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="9ca09-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 

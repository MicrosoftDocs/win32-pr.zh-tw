---
description: Blob 可與 Diffie-Hellman 提供者一起使用，以在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977905"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="584b2-103">Diffie-Hellman 金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="584b2-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="584b2-104">[*Blob*](../secgloss/b-gly.md) 可搭配 [*diffie-hellman*](../secgloss/d-gly.md) 提供者使用，以從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="584b2-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="584b2-105">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="584b2-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="584b2-106">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="584b2-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="584b2-107">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="584b2-107">Public Key BLOBs</span></span>

<span data-ttu-id="584b2-108">Diffie-Hellman 的 [*公開金鑰 blob*](../secgloss/p-gly.md)（輸入 **PUBLICKEYBLOB**）是用來交換 Diffie-Hellman 金鑰交換中的 (G ^ X) mod P 值。</span><span class="sxs-lookup"><span data-stu-id="584b2-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="584b2-109">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="584b2-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="584b2-110">下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。</span><span class="sxs-lookup"><span data-stu-id="584b2-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="584b2-111">欄位</span><span class="sxs-lookup"><span data-stu-id="584b2-111">Field</span></span>          | <span data-ttu-id="584b2-112">描述</span><span class="sxs-lookup"><span data-stu-id="584b2-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584b2-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="584b2-113">dhpubkey</span></span>       | <span data-ttu-id="584b2-114">[**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="584b2-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="584b2-115">**魔術** 成員應設定為0x31484400。</span><span class="sxs-lookup"><span data-stu-id="584b2-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="584b2-116">此十六進位值是 "DH1" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="584b2-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="584b2-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="584b2-117">publickeystruc</span></span> | <span data-ttu-id="584b2-118">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="584b2-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="584b2-119">y</span><span class="sxs-lookup"><span data-stu-id="584b2-119">y</span></span>              | <span data-ttu-id="584b2-120">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="584b2-120">A **BYTE** sequence.</span></span> <span data-ttu-id="584b2-121">Y 值（ (G ^ X) mod P）位於 [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) 結構的正後方，而且應該一律是 **DHPUBKEY bitlen** 欄位的長度（以位元組為單位）， (位長度 P) 除以八。</span><span class="sxs-lookup"><span data-stu-id="584b2-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="584b2-122">如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以八的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="584b2-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="584b2-123">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="584b2-123">Private Key BLOBs</span></span>

<span data-ttu-id="584b2-124">Diffie-Hellman 的 [*私密金鑰 blob*](../secgloss/p-gly.md)（輸入 **PRI加值稅EKEYBLOB**）是用來儲存 Diffie-Hellman 金鑰的公開/私用資訊。</span><span class="sxs-lookup"><span data-stu-id="584b2-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="584b2-125">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="584b2-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="584b2-126">下表說明金鑰 BLOB 的每個元件。</span><span class="sxs-lookup"><span data-stu-id="584b2-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="584b2-127">欄位</span><span class="sxs-lookup"><span data-stu-id="584b2-127">Field</span></span>          | <span data-ttu-id="584b2-128">描述</span><span class="sxs-lookup"><span data-stu-id="584b2-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584b2-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="584b2-129">dhpubkey</span></span>       | <span data-ttu-id="584b2-130">[**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="584b2-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="584b2-131">**魔術** 成員必須設為0x32484400。</span><span class="sxs-lookup"><span data-stu-id="584b2-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="584b2-132">此十六進位值是 "DH2" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="584b2-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="584b2-133">產生器</span><span class="sxs-lookup"><span data-stu-id="584b2-133">generator</span></span>      | <span data-ttu-id="584b2-134">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="584b2-134">A **BYTE** sequence.</span></span> <span data-ttu-id="584b2-135">發電機，G。</span><span class="sxs-lookup"><span data-stu-id="584b2-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="584b2-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="584b2-136">publickeystruc</span></span> | <span data-ttu-id="584b2-137">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="584b2-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="584b2-138">主要</span><span class="sxs-lookup"><span data-stu-id="584b2-138">prime</span></span>          | <span data-ttu-id="584b2-139">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="584b2-139">A **BYTE** sequence.</span></span> <span data-ttu-id="584b2-140">質數模數 P。這項資料必須一律將最重要的位元組數設定為一。</span><span class="sxs-lookup"><span data-stu-id="584b2-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="584b2-141">secret</span><span class="sxs-lookup"><span data-stu-id="584b2-141">secret</span></span>         | <span data-ttu-id="584b2-142">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="584b2-142">A **BYTE** sequence.</span></span> <span data-ttu-id="584b2-143">秘密指數 X。</span><span class="sxs-lookup"><span data-stu-id="584b2-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="584b2-144">產生器和密碼必須一律具有相同的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="584b2-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="584b2-145">如果其中一個位元組比另一個位元組更短，則必須以零值位元組的數位填補，使其相同。</span><span class="sxs-lookup"><span data-stu-id="584b2-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="584b2-146">產生器和密碼都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。</span><span class="sxs-lookup"><span data-stu-id="584b2-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 

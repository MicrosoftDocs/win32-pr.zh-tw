---
description: Blob 可搭配 Diffie-hellman/安全通道提供者使用，以在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Diffie-hellman/Schannel 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692999"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="9f76e-103">Diffie-hellman/Schannel 金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="9f76e-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="9f76e-104">[*Blob*](../secgloss/b-gly.md)可搭配 [*diffie-hellman*](../secgloss/d-gly.md)安全通道提供者使用，以將金鑰 / [](../secgloss/s-gly.md)從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入。</span><span class="sxs-lookup"><span data-stu-id="9f76e-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="9f76e-105">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="9f76e-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="9f76e-106">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="9f76e-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="9f76e-107">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="9f76e-107">Public Key BLOBs</span></span>

<span data-ttu-id="9f76e-108">Diffie-Hellman 的 [*公開金鑰 blob*](../secgloss/p-gly.md)（輸入 **PUBLICKEYBLOB**）是用來交換 Diffie-Hellman 金鑰交換中的 (G ^ X) mod P 值。</span><span class="sxs-lookup"><span data-stu-id="9f76e-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="9f76e-109">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="9f76e-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="9f76e-110">下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。</span><span class="sxs-lookup"><span data-stu-id="9f76e-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="9f76e-111">欄位</span><span class="sxs-lookup"><span data-stu-id="9f76e-111">Field</span></span>          | <span data-ttu-id="9f76e-112">描述</span><span class="sxs-lookup"><span data-stu-id="9f76e-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f76e-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="9f76e-113">dhpubkey</span></span>       | <span data-ttu-id="9f76e-114">[**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="9f76e-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9f76e-115">**魔術** 成員必須設為0x31484400。</span><span class="sxs-lookup"><span data-stu-id="9f76e-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="9f76e-116">此十六進位值是 DH1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="9f76e-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9f76e-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9f76e-117">publickeystruc</span></span> | <span data-ttu-id="9f76e-118">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="9f76e-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9f76e-119">y</span><span class="sxs-lookup"><span data-stu-id="9f76e-119">y</span></span>              | <span data-ttu-id="9f76e-120">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="9f76e-120">A **BYTE** sequence.</span></span> <span data-ttu-id="9f76e-121">Y 值（ (G ^ X) mod P）位於 [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) 結構的正上方。</span><span class="sxs-lookup"><span data-stu-id="9f76e-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9f76e-122">順序的長度（以位元組為單位）是 **DHPUBKEY** 除以八的 **bitlen** 成員。</span><span class="sxs-lookup"><span data-stu-id="9f76e-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="9f76e-123">如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以八的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="9f76e-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="9f76e-124">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="9f76e-124">Private Key BLOBs</span></span>

<span data-ttu-id="9f76e-125">D-H [*私用金鑰 blob*](../secgloss/p-gly.md)（輸入 **PRI加值稅EKEYBLOB**）是用來匯出和匯入 d-h 金鑰的私用資訊。</span><span class="sxs-lookup"><span data-stu-id="9f76e-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="9f76e-126">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="9f76e-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="9f76e-127">下表說明金鑰 BLOB 的每個元件。</span><span class="sxs-lookup"><span data-stu-id="9f76e-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="9f76e-128">欄位</span><span class="sxs-lookup"><span data-stu-id="9f76e-128">Field</span></span>          | <span data-ttu-id="9f76e-129">描述</span><span class="sxs-lookup"><span data-stu-id="9f76e-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f76e-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="9f76e-130">dhpubkey</span></span>       | <span data-ttu-id="9f76e-131">[**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="9f76e-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9f76e-132">**魔術** 成員必須設為0x32484400。</span><span class="sxs-lookup"><span data-stu-id="9f76e-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="9f76e-133">此十六進位值是 DH2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="9f76e-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="9f76e-134">產生器</span><span class="sxs-lookup"><span data-stu-id="9f76e-134">generator</span></span>      | <span data-ttu-id="9f76e-135">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="9f76e-135">A **BYTE** sequence.</span></span> <span data-ttu-id="9f76e-136">產生器 G。</span><span class="sxs-lookup"><span data-stu-id="9f76e-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9f76e-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9f76e-137">publickeystruc</span></span> | <span data-ttu-id="9f76e-138">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="9f76e-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9f76e-139">主要</span><span class="sxs-lookup"><span data-stu-id="9f76e-139">prime</span></span>          | <span data-ttu-id="9f76e-140">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="9f76e-140">A **BYTE** sequence.</span></span> <span data-ttu-id="9f76e-141">質數模數 P。這項資料必須一律將最重要的位元組數設定為一。</span><span class="sxs-lookup"><span data-stu-id="9f76e-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="9f76e-142">secret</span><span class="sxs-lookup"><span data-stu-id="9f76e-142">secret</span></span>         | <span data-ttu-id="9f76e-143">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="9f76e-143">A **BYTE** sequence.</span></span> <span data-ttu-id="9f76e-144">秘密指數 X。</span><span class="sxs-lookup"><span data-stu-id="9f76e-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="9f76e-145">質數、產生器和秘密值的長度必須一律相同（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f76e-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="9f76e-146">如果任何值是一個或更短的值，則必須以所需的零位元組數目填補，使其相同。</span><span class="sxs-lookup"><span data-stu-id="9f76e-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="9f76e-147">質數、產生器和秘密的格式為 [*位元組*](../secgloss/l-gly.md) 由小到大。</span><span class="sxs-lookup"><span data-stu-id="9f76e-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 

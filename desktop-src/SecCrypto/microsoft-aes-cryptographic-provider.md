---
description: Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援與 Microsoft 基底密碼編譯提供者相同的功能，稱為「基底提供者」。
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Microsoft AES 密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581866"
---
# <a name="microsoft-aes-cryptographic-provider"></a><span data-ttu-id="b232c-103">Microsoft AES 密碼編譯提供者</span><span class="sxs-lookup"><span data-stu-id="b232c-103">Microsoft AES Cryptographic Provider</span></span>

<span data-ttu-id="b232c-104">Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援與 Microsoft 基底密碼編譯提供者相同的功能，稱為「基底提供者」。</span><span class="sxs-lookup"><span data-stu-id="b232c-104">The Microsoft Enhanced RSA and AES Cryptographic Provider supports the same capabilities as the Microsoft Base Cryptographic Provider, called the Base Provider.</span></span> <span data-ttu-id="b232c-105">AES 提供者透過更長的金鑰和其他演算法，支援更強的安全性。</span><span class="sxs-lookup"><span data-stu-id="b232c-105">The AES Provider supports stronger security through longer keys and additional algorithms.</span></span> <span data-ttu-id="b232c-106">它可以與所有 CryptoAPI 版本搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b232c-106">It can be used with all versions of CryptoAPI.</span></span>

<span data-ttu-id="b232c-107">**Windows XP：** Microsoft AES 密碼編譯提供者的名稱為 Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 。</span><span class="sxs-lookup"><span data-stu-id="b232c-107">**Windows XP:** The Microsoft AES Cryptographic Provider was named Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span>

<span data-ttu-id="b232c-108">為了維持與先前的提供者版本之間的回溯相容性，提供者名稱（如 Wincrypt .h 標頭檔中所定義）會保留版本1.0 指定，即使已寄出此提供者的較新版本也一樣。</span><span class="sxs-lookup"><span data-stu-id="b232c-108">To maintain backward compatibility with earlier provider versions, the provider name, as defined in the Wincrypt.h header file, retains the version 1.0 designation even though newer versions of this provider have been shipped.</span></span> <span data-ttu-id="b232c-109">若要判斷使用中的提供者版本，請呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) ，並將 *dwParam* 參數設定為 PP \_ 版本。</span><span class="sxs-lookup"><span data-stu-id="b232c-109">To determine the version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* parameter set to PP\_VERSION.</span></span> <span data-ttu-id="b232c-110">如果傳回0x0200，則會使用2.0 版。</span><span class="sxs-lookup"><span data-stu-id="b232c-110">Version 2.0 is in use if 0x0200 is returned.</span></span>

|                   | <span data-ttu-id="b232c-111">值</span><span class="sxs-lookup"><span data-stu-id="b232c-111">Value</span></span>                    |
|-------------------|--------------------------|
| <span data-ttu-id="b232c-112">**提供者類型**</span><span class="sxs-lookup"><span data-stu-id="b232c-112">**Provider type**</span></span> | <span data-ttu-id="b232c-113">>PROV \_ RSA \_ AES</span><span class="sxs-lookup"><span data-stu-id="b232c-113">PROV\_RSA\_AES</span></span>           |
| <span data-ttu-id="b232c-114">**提供者名稱**</span><span class="sxs-lookup"><span data-stu-id="b232c-114">**Provider name**</span></span> | <span data-ttu-id="b232c-115">MS \_ ENH \_ RSA \_ AES \_ >PROV</span><span class="sxs-lookup"><span data-stu-id="b232c-115">MS\_ENH\_RSA\_AES\_PROV</span></span>  |



 

<span data-ttu-id="b232c-116">下表強調基底提供者、強式提供者和 AES 提供者之間的差異。</span><span class="sxs-lookup"><span data-stu-id="b232c-116">The following table highlights differences between the Base Provider, Strong Provider, and AES Provider.</span></span> <span data-ttu-id="b232c-117">所顯示的 [*金鑰長度*](../secgloss/k-gly.md) 為預設金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="b232c-117">The [*key lengths*](../secgloss/k-gly.md) shown are the default key lengths.</span></span>



| <span data-ttu-id="b232c-118">演算法</span><span class="sxs-lookup"><span data-stu-id="b232c-118">Algorithm</span></span>                                                                                | <span data-ttu-id="b232c-119">基底提供者金鑰長度</span><span class="sxs-lookup"><span data-stu-id="b232c-119">Base Provider key length</span></span> | <span data-ttu-id="b232c-120">強式提供者金鑰長度</span><span class="sxs-lookup"><span data-stu-id="b232c-120">Strong Provider key length</span></span> | <span data-ttu-id="b232c-121">AES 提供者金鑰長度</span><span class="sxs-lookup"><span data-stu-id="b232c-121">AES Provider key length</span></span>                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| <span data-ttu-id="b232c-122">RSA 公開金鑰簽章演算法</span><span class="sxs-lookup"><span data-stu-id="b232c-122">RSA public key signature algorithm</span></span>                                                       | <span data-ttu-id="b232c-123">512位</span><span class="sxs-lookup"><span data-stu-id="b232c-123">512 bits</span></span>                 | <span data-ttu-id="b232c-124">1024位</span><span class="sxs-lookup"><span data-stu-id="b232c-124">1,024 bits</span></span>                 | <span data-ttu-id="b232c-125">1024位</span><span class="sxs-lookup"><span data-stu-id="b232c-125">1,024 bits</span></span>                                  |
| <span data-ttu-id="b232c-126">RSA 公開金鑰交換演算法</span><span class="sxs-lookup"><span data-stu-id="b232c-126">RSA public key exchange algorithm</span></span>                                                        | <span data-ttu-id="b232c-127">512位</span><span class="sxs-lookup"><span data-stu-id="b232c-127">512 bits</span></span>                 | <span data-ttu-id="b232c-128">1024位</span><span class="sxs-lookup"><span data-stu-id="b232c-128">1,024 bits</span></span>                 | <span data-ttu-id="b232c-129">1024位</span><span class="sxs-lookup"><span data-stu-id="b232c-129">1,024 bits</span></span>                                  |
| <span data-ttu-id="b232c-130">RC2 區塊加密演算法</span><span class="sxs-lookup"><span data-stu-id="b232c-130">RC2 block encryption algorithm</span></span>                                                           | <span data-ttu-id="b232c-131">40位</span><span class="sxs-lookup"><span data-stu-id="b232c-131">40 bits</span></span>                  | <span data-ttu-id="b232c-132">128 位元</span><span class="sxs-lookup"><span data-stu-id="b232c-132">128 bits</span></span>                   | <span data-ttu-id="b232c-133">可以設定128位 Salt 長度。</span><span class="sxs-lookup"><span data-stu-id="b232c-133">128 bits Salt length can be set.</span></span><br/> |
| <span data-ttu-id="b232c-134">RC4 串流加密演算法</span><span class="sxs-lookup"><span data-stu-id="b232c-134">RC4 stream encryption algorithm</span></span>                                                          | <span data-ttu-id="b232c-135">40位</span><span class="sxs-lookup"><span data-stu-id="b232c-135">40 bits</span></span>                  | <span data-ttu-id="b232c-136">128 位元</span><span class="sxs-lookup"><span data-stu-id="b232c-136">128 bits</span></span>                   | <span data-ttu-id="b232c-137">可以設定128位 Salt 長度。</span><span class="sxs-lookup"><span data-stu-id="b232c-137">128 bits Salt length can be set.</span></span><br/> |
| <span data-ttu-id="b232c-138">DES</span><span class="sxs-lookup"><span data-stu-id="b232c-138">DES</span></span>                                                                                      | <span data-ttu-id="b232c-139">56位</span><span class="sxs-lookup"><span data-stu-id="b232c-139">56 bits</span></span>                  | <span data-ttu-id="b232c-140">56位</span><span class="sxs-lookup"><span data-stu-id="b232c-140">56 bits</span></span>                    | <span data-ttu-id="b232c-141">56位</span><span class="sxs-lookup"><span data-stu-id="b232c-141">56 bits</span></span>                                     |
| <span data-ttu-id="b232c-142">[*三重 DES*](../secgloss/t-gly.md) (2 金鑰) </span><span class="sxs-lookup"><span data-stu-id="b232c-142">[*Triple DES*](../secgloss/t-gly.md) (2 key)</span></span> | <span data-ttu-id="b232c-143">不支援</span><span class="sxs-lookup"><span data-stu-id="b232c-143">Not supported</span></span>            | <span data-ttu-id="b232c-144">112位</span><span class="sxs-lookup"><span data-stu-id="b232c-144">112 bits</span></span>                   | <span data-ttu-id="b232c-145">112位</span><span class="sxs-lookup"><span data-stu-id="b232c-145">112 bits</span></span>                                    |
| <span data-ttu-id="b232c-146">三重 DES (3 金鑰) </span><span class="sxs-lookup"><span data-stu-id="b232c-146">Triple DES (3 key)</span></span>                                                                       | <span data-ttu-id="b232c-147">不支援</span><span class="sxs-lookup"><span data-stu-id="b232c-147">Not supported</span></span>            | <span data-ttu-id="b232c-148">168位</span><span class="sxs-lookup"><span data-stu-id="b232c-148">168 bits</span></span>                   | <span data-ttu-id="b232c-149">168位</span><span class="sxs-lookup"><span data-stu-id="b232c-149">168 bits</span></span>                                    |



 

<span data-ttu-id="b232c-150">如需支援之演算法的完整清單，請參閱 [AES 提供者演算法](aes-provider-algorithms.md)。</span><span class="sxs-lookup"><span data-stu-id="b232c-150">For a complete list of supported algorithms, see [AES Provider Algorithms](aes-provider-algorithms.md).</span></span>

<span data-ttu-id="b232c-151">強式提供者、增強的提供者和 AES 提供者與基底提供者回溯相容，不同之處在于提供者只能產生預設金鑰長度的 RC2 或 RC4 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b232c-151">The Strong Provider, Enhanced Provider, and AES Provider are backward-compatible with the Base Provider except that the providers can generate only RC2 or RC4 keys of default key length.</span></span> <span data-ttu-id="b232c-152">基底提供者的預設長度是40位。</span><span class="sxs-lookup"><span data-stu-id="b232c-152">The default length for the Base Provider is 40 bits.</span></span> <span data-ttu-id="b232c-153">AES 提供者的預設長度是128位。</span><span class="sxs-lookup"><span data-stu-id="b232c-153">The default length for the AES Provider is 128 bits.</span></span> <span data-ttu-id="b232c-154">因此 AES 提供者無法建立具有基底提供者相容金鑰長度的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b232c-154">Thus the AES Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="b232c-155">不過，AES 提供者可以匯入最多128位的 RC2 和 RC4 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b232c-155">However, the AES Provider can import RC2 and RC4 keys of up to 128 bits.</span></span> <span data-ttu-id="b232c-156">因此，AES 提供者可以匯入和使用使用基底提供者所產生的40位金鑰。</span><span class="sxs-lookup"><span data-stu-id="b232c-156">Therefore, the AES Provider can import and use 40-bit keys generated by using the Base Provider.</span></span>

 

 

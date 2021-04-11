---
description: Blob 可與 RSA/安全通道提供者搭配使用，以將金鑰從密碼編譯服務提供者匯出，並將金鑰匯入 (CSP) 。
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: RSA/Schannel 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848147"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="2be77-103">RSA/Schannel 金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="2be77-104">[*Blob*](../secgloss/b-gly.md)可與 [*RSA*](../secgloss/r-gly.md)安全通道提供者搭配使用， / [](../secgloss/s-gly.md)以在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="2be77-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="2be77-105">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="2be77-106">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="2be77-107">簡單的金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="2be77-108">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-108">Public Key BLOBs</span></span>

<span data-ttu-id="2be77-109">[*公開金鑰 blob*](../secgloss/p-gly.md)（類型 **PUBLICKEYBLOB**）是用來儲存 [*公開金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2be77-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="2be77-110">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="2be77-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="2be77-111">下表描述每個公開金鑰元件。</span><span class="sxs-lookup"><span data-stu-id="2be77-111">The following table describes each public key component.</span></span> <span data-ttu-id="2be77-112">所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。</span><span class="sxs-lookup"><span data-stu-id="2be77-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="2be77-113">欄位</span><span class="sxs-lookup"><span data-stu-id="2be77-113">Field</span></span>          | <span data-ttu-id="2be77-114">描述</span><span class="sxs-lookup"><span data-stu-id="2be77-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be77-115">模數</span><span class="sxs-lookup"><span data-stu-id="2be77-115">modulus</span></span>        | <span data-ttu-id="2be77-116">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-116">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-117">公開金鑰模數資料位於 **RSAPUBKEY** 結構的正後方。</span><span class="sxs-lookup"><span data-stu-id="2be77-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="2be77-118">這項資料的長度會隨著公開金鑰的長度而有所不同。</span><span class="sxs-lookup"><span data-stu-id="2be77-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="2be77-119">您可以藉由將 **RSAPUBKEY** 的 **bitlen** 成員值除以八來判斷位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2be77-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="2be77-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2be77-120">publickeystruc</span></span> | <span data-ttu-id="2be77-121">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="2be77-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="2be77-122">rsapubkey</span></span>      | <span data-ttu-id="2be77-123">[**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="2be77-124">**魔術** 成員必須設為0x31415352。</span><span class="sxs-lookup"><span data-stu-id="2be77-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="2be77-125">此十六進位值是 RSA1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="2be77-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="2be77-126">公開金鑰 Blob 未加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="2be77-127">它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="2be77-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="2be77-128">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-128">Private Key BLOBs</span></span>

<span data-ttu-id="2be77-129">[*私用金鑰 blob*](../secgloss/p-gly.md)（類型 **PRI加值稅EKEYBLOB**）是用來儲存 [*公開/私密金鑰*](../secgloss/p-gly.md)組。</span><span class="sxs-lookup"><span data-stu-id="2be77-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="2be77-130">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="2be77-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="2be77-131">如果 [*金鑰 blob*](../secgloss/k-gly.md) 已加密，則 Blob 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密，但不會加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="2be77-132">加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。</span><span class="sxs-lookup"><span data-stu-id="2be77-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="2be77-133">應用程式必須負責管理這項資訊。</span><span class="sxs-lookup"><span data-stu-id="2be77-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="2be77-134">下表說明每個私密金鑰 BLOB 元件。</span><span class="sxs-lookup"><span data-stu-id="2be77-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="2be77-135">這些欄位會對應到 [*公開金鑰加密標準*](../secgloss/p-gly.md) 的7.2 章節中所述的欄位 (PKCS) \# 1，但有些許差異。</span><span class="sxs-lookup"><span data-stu-id="2be77-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="2be77-136">欄位</span><span class="sxs-lookup"><span data-stu-id="2be77-136">Field</span></span>           | <span data-ttu-id="2be77-137">描述</span><span class="sxs-lookup"><span data-stu-id="2be77-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be77-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="2be77-138">exponent1</span></span>       | <span data-ttu-id="2be77-139">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-139">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-140">第一個指數。</span><span class="sxs-lookup"><span data-stu-id="2be77-140">The first exponent.</span></span> <span data-ttu-id="2be77-141">此值的數值為 d mod (p – 1) 。</span><span class="sxs-lookup"><span data-stu-id="2be77-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="2be77-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="2be77-142">exponent2</span></span>       | <span data-ttu-id="2be77-143">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-143">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-144">第二個指數。</span><span class="sxs-lookup"><span data-stu-id="2be77-144">The second exponent.</span></span> <span data-ttu-id="2be77-145">此值的數值為 d mod (q – 1) 。</span><span class="sxs-lookup"><span data-stu-id="2be77-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="2be77-146">係數</span><span class="sxs-lookup"><span data-stu-id="2be77-146">coefficient</span></span>     | <span data-ttu-id="2be77-147">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-147">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-148">係數。</span><span class="sxs-lookup"><span data-stu-id="2be77-148">Coefficient.</span></span> <span data-ttu-id="2be77-149">此值為 q) mod p (反向的數值。</span><span class="sxs-lookup"><span data-stu-id="2be77-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="2be77-150">模組</span><span class="sxs-lookup"><span data-stu-id="2be77-150">Modulus</span></span>         | <span data-ttu-id="2be77-151">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-151">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-152">模數。</span><span class="sxs-lookup"><span data-stu-id="2be77-152">The modulus.</span></span> <span data-ttu-id="2be77-153">這包含包含 *Prime1* \* *Prime2* 的字串。</span><span class="sxs-lookup"><span data-stu-id="2be77-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="2be77-154">它通常稱為 n。</span><span class="sxs-lookup"><span data-stu-id="2be77-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="2be77-155">prime1</span><span class="sxs-lookup"><span data-stu-id="2be77-155">prime1</span></span>          | <span data-ttu-id="2be77-156">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-156">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-157">質數1，通常稱為 p。</span><span class="sxs-lookup"><span data-stu-id="2be77-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2be77-158">prime2</span><span class="sxs-lookup"><span data-stu-id="2be77-158">prime2</span></span>          | <span data-ttu-id="2be77-159">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-159">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-160">質數2，通常稱為 q。</span><span class="sxs-lookup"><span data-stu-id="2be77-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2be77-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2be77-161">publickeystruc</span></span>  | <span data-ttu-id="2be77-162">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="2be77-163">privateExponent</span><span class="sxs-lookup"><span data-stu-id="2be77-163">privateExponent</span></span> | <span data-ttu-id="2be77-164">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-164">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-165">私用指數，通常稱為 d。</span><span class="sxs-lookup"><span data-stu-id="2be77-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="2be77-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="2be77-166">rsapubkey</span></span>       | <span data-ttu-id="2be77-167">[**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="2be77-168">**魔術** 成員必須設為0x32415352。</span><span class="sxs-lookup"><span data-stu-id="2be77-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="2be77-169">此十六進位值是 RSA2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="2be77-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="2be77-170">私密金鑰 Blob 未加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="2be77-171">它們包含純文字格式的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2be77-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="2be77-172">呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2be77-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="2be77-173">如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。</span><span class="sxs-lookup"><span data-stu-id="2be77-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="2be77-174">但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="2be77-175">加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。</span><span class="sxs-lookup"><span data-stu-id="2be77-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="2be77-176">應用程式必須管理和儲存此資訊。</span><span class="sxs-lookup"><span data-stu-id="2be77-176">The application must manage and store this information.</span></span> <span data-ttu-id="2be77-177">如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="2be77-178">匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。</span><span class="sxs-lookup"><span data-stu-id="2be77-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="2be77-179">簡單的金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="2be77-179">Simple Key BLOBs</span></span>

<span data-ttu-id="2be77-180">[*簡單的金鑰 blob*](../secgloss/s-gly.md)（類型 **SIMPLEBLOB**）是用來儲存和傳輸工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="2be77-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="2be77-181">這些一律會以 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密。</span><span class="sxs-lookup"><span data-stu-id="2be77-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="2be77-182">這些金鑰會以下列格式匯出並匯入為一連串的位元組。</span><span class="sxs-lookup"><span data-stu-id="2be77-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="2be77-183">下表說明每個簡單的 BLOB 元件。</span><span class="sxs-lookup"><span data-stu-id="2be77-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="2be77-184">欄位</span><span class="sxs-lookup"><span data-stu-id="2be77-184">Field</span></span>          | <span data-ttu-id="2be77-185">描述</span><span class="sxs-lookup"><span data-stu-id="2be77-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be77-186">algid</span><span class="sxs-lookup"><span data-stu-id="2be77-186">algid</span></span>          | <span data-ttu-id="2be77-187">[**ALG \_ 識別碼**](alg-id.md)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="2be77-188">這通常會指定 CALG \_ RSA \_ KEYX 演算法，這表示使用 [*rsa 公開金鑰演算法*](../secgloss/r-gly.md)，以金鑰交換公開金鑰來加密工作階段金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="2be77-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="2be77-189">encryptedkey</span><span class="sxs-lookup"><span data-stu-id="2be77-189">encryptedkey</span></span>   | <span data-ttu-id="2be77-190">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="2be77-190">A **BYTE** sequence.</span></span> <span data-ttu-id="2be77-191">加密工作階段金鑰資料的格式為 PKCS \# 1，type 2 encryption block。</span><span class="sxs-lookup"><span data-stu-id="2be77-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="2be77-192">如需此資料格式的相關資訊，請參閱 RSA Data Security，Inc. 發行的公開金鑰加密標準 (PKCS) 。</span><span class="sxs-lookup"><span data-stu-id="2be77-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="2be77-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2be77-193">publickeystruc</span></span> | <span data-ttu-id="2be77-194">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="2be77-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="2be77-195">這項資料的大小一律與公開金鑰的模數相同。</span><span class="sxs-lookup"><span data-stu-id="2be77-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="2be77-196">例如，Microsoft 基礎密碼編譯提供者所產生的公開金鑰一律為512位 (64 位元組) 長度，因此加密的工作階段金鑰資料也一律為64個位元組。</span><span class="sxs-lookup"><span data-stu-id="2be77-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 

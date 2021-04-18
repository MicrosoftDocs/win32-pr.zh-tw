---
description: 基底提供者、強式提供者和增強型提供者都使用相同的金鑰 Blob。
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: 增強的提供者金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f693fd469a1df2e76078e61bb69c90ea5d5041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978081"
---
# <a name="enhanced-provider-key-blobs"></a><span data-ttu-id="b304c-103">增強的提供者金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-103">Enhanced Provider Key BLOBs</span></span>

<span data-ttu-id="b304c-104">基底提供者、強式提供者和增強型提供者都使用相同的 [*金鑰 blob*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b304c-104">The Base Provider, Strong Provider, and Enhanced Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="b304c-105">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="b304c-106">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="b304c-107">簡單的金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="b304c-108">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-108">Public Key BLOBs</span></span>

<span data-ttu-id="b304c-109">[*公開金鑰 blob*](../secgloss/p-gly.md)（類型 **PUBLICKEYBLOB**）是用來將 [*公開金鑰*](../secgloss/p-gly.md) 儲存在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 之外。</span><span class="sxs-lookup"><span data-stu-id="b304c-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="b304c-110">擴充提供者的公開金鑰 Blob 具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="b304c-110">Extended provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="b304c-111">下表描述每個公開金鑰元件。</span><span class="sxs-lookup"><span data-stu-id="b304c-111">The following table describes each public key component.</span></span> <span data-ttu-id="b304c-112">所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。</span><span class="sxs-lookup"><span data-stu-id="b304c-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="b304c-113">欄位</span><span class="sxs-lookup"><span data-stu-id="b304c-113">Field</span></span>          | <span data-ttu-id="b304c-114">描述</span><span class="sxs-lookup"><span data-stu-id="b304c-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b304c-115">模數</span><span class="sxs-lookup"><span data-stu-id="b304c-115">modulus</span></span>        | <span data-ttu-id="b304c-116">公開金鑰模數資料位於 [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) 結構的正後方。</span><span class="sxs-lookup"><span data-stu-id="b304c-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="b304c-117">這項資料的大小會因公開金鑰的大小而有所不同。</span><span class="sxs-lookup"><span data-stu-id="b304c-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="b304c-118">您可以將 **RSAPUBKEY bitlen** 欄位的值除以八來判斷位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b304c-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="b304c-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="b304c-119">publickeystruc</span></span> | <span data-ttu-id="b304c-120">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="b304c-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="b304c-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="b304c-121">rsapubkey</span></span>      | <span data-ttu-id="b304c-122">[**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="b304c-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="b304c-123">**魔術** 成員必須設為0x31415352。</span><span class="sxs-lookup"><span data-stu-id="b304c-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="b304c-124">此十六進位值是 RSA1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="b304c-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="b304c-125">公開金鑰 Blob 未加密。</span><span class="sxs-lookup"><span data-stu-id="b304c-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="b304c-126">它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="b304c-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="b304c-127">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-127">Private Key BLOBs</span></span>

<span data-ttu-id="b304c-128">[*私用金鑰 blob*](../secgloss/p-gly.md)（類型 **PRI加值稅EKEYBLOB**）是用來將 [*私密金鑰*](../secgloss/p-gly.md) 儲存在 CSP 外部。</span><span class="sxs-lookup"><span data-stu-id="b304c-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="b304c-129">擴充提供者的私密金鑰 Blob 具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="b304c-129">Extended provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="b304c-130">下表描述私密金鑰 BLOB 元件。</span><span class="sxs-lookup"><span data-stu-id="b304c-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="b304c-131">這些欄位會對應到 [*公開金鑰加密標準*](../secgloss/p-gly.md) 的7.2 章節中所述的欄位 (PKCS) \# 1，但有些許差異。</span><span class="sxs-lookup"><span data-stu-id="b304c-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="b304c-132">欄位</span><span class="sxs-lookup"><span data-stu-id="b304c-132">Field</span></span>           | <span data-ttu-id="b304c-133">描述</span><span class="sxs-lookup"><span data-stu-id="b304c-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b304c-134">係數</span><span class="sxs-lookup"><span data-stu-id="b304c-134">coefficient</span></span>     | <span data-ttu-id="b304c-135">係數。</span><span class="sxs-lookup"><span data-stu-id="b304c-135">Coefficient.</span></span> <span data-ttu-id="b304c-136">此值為 q) mod p (反向的數值。</span><span class="sxs-lookup"><span data-stu-id="b304c-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="b304c-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="b304c-137">exponent1</span></span>       | <span data-ttu-id="b304c-138">指數1。</span><span class="sxs-lookup"><span data-stu-id="b304c-138">Exponent 1.</span></span> <span data-ttu-id="b304c-139">此值的數值為 d mod (p – 1) 。</span><span class="sxs-lookup"><span data-stu-id="b304c-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="b304c-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="b304c-140">exponent2</span></span>       | <span data-ttu-id="b304c-141">指數2。</span><span class="sxs-lookup"><span data-stu-id="b304c-141">Exponent 2.</span></span> <span data-ttu-id="b304c-142">此值的數值為 d mod (q – 1) 。</span><span class="sxs-lookup"><span data-stu-id="b304c-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="b304c-143">模組</span><span class="sxs-lookup"><span data-stu-id="b304c-143">Modulus</span></span>         | <span data-ttu-id="b304c-144">模數。</span><span class="sxs-lookup"><span data-stu-id="b304c-144">The modulus.</span></span> <span data-ttu-id="b304c-145">這具有 *Prime1*×*Prime2* 的值，通常稱為 n。</span><span class="sxs-lookup"><span data-stu-id="b304c-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="b304c-146">prime1</span><span class="sxs-lookup"><span data-stu-id="b304c-146">prime1</span></span>          | <span data-ttu-id="b304c-147">質數1，通常稱為 p。</span><span class="sxs-lookup"><span data-stu-id="b304c-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="b304c-148">prime2</span><span class="sxs-lookup"><span data-stu-id="b304c-148">prime2</span></span>          | <span data-ttu-id="b304c-149">質數2，通常稱為 q。</span><span class="sxs-lookup"><span data-stu-id="b304c-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="b304c-150">privateExponent</span><span class="sxs-lookup"><span data-stu-id="b304c-150">privateExponent</span></span> | <span data-ttu-id="b304c-151">私用指數，通常稱為 d。</span><span class="sxs-lookup"><span data-stu-id="b304c-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="b304c-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="b304c-152">publickeystruc</span></span>  | <span data-ttu-id="b304c-153">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="b304c-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="b304c-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="b304c-154">rsapubkey</span></span>       | <span data-ttu-id="b304c-155">[**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。</span><span class="sxs-lookup"><span data-stu-id="b304c-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="b304c-156">**魔術** 成員必須設為0x32415352。</span><span class="sxs-lookup"><span data-stu-id="b304c-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="b304c-157">此十六進位值是 RSA2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="b304c-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="b304c-158">私密金鑰 Blob 未加密。</span><span class="sxs-lookup"><span data-stu-id="b304c-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="b304c-159">它們包含純文字格式的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b304c-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="b304c-160">呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b304c-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="b304c-161">如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。</span><span class="sxs-lookup"><span data-stu-id="b304c-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="b304c-162">但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。</span><span class="sxs-lookup"><span data-stu-id="b304c-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="b304c-163">加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。</span><span class="sxs-lookup"><span data-stu-id="b304c-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="b304c-164">應用程式必須管理和儲存此資訊。</span><span class="sxs-lookup"><span data-stu-id="b304c-164">The application must manage and store this information.</span></span> <span data-ttu-id="b304c-165">如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。</span><span class="sxs-lookup"><span data-stu-id="b304c-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="b304c-166">匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。</span><span class="sxs-lookup"><span data-stu-id="b304c-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="b304c-167">簡單的金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b304c-167">Simple Key BLOBs</span></span>

<span data-ttu-id="b304c-168">[*簡單的金鑰 blob*](../secgloss/s-gly.md)（類型 **SIMPLEBLOB**）是用來儲存和傳輸 CSP 外部的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="b304c-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="b304c-169">擴充提供者簡單金鑰 Blob 一律會以 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密。</span><span class="sxs-lookup"><span data-stu-id="b304c-169">Extended provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="b304c-170">**SIMPLEBLOB** 的 **>pbdata** 成員是採用下列格式的位元組序列。</span><span class="sxs-lookup"><span data-stu-id="b304c-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="b304c-171">下表說明 **SIMPLEBLOB** 之 **>pbdata** 成員的每個元件。</span><span class="sxs-lookup"><span data-stu-id="b304c-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="b304c-172">欄位</span><span class="sxs-lookup"><span data-stu-id="b304c-172">Field</span></span>          | <span data-ttu-id="b304c-173">描述</span><span class="sxs-lookup"><span data-stu-id="b304c-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b304c-174">algid</span><span class="sxs-lookup"><span data-stu-id="b304c-174">algid</span></span>          | <span data-ttu-id="b304c-175">[**ALG \_ 識別碼**](alg-id.md)結構，指定用來加密工作階段金鑰資料的加密演算法。</span><span class="sxs-lookup"><span data-stu-id="b304c-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="b304c-176">這通常是 CALG \_ RSA KEYX 的值 \_ ，這表示已使用 [*rsa 公開金鑰演算法*](../secgloss/r-gly.md)，以金鑰交換公開金鑰來加密工作階段金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="b304c-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="b304c-177">encryptedkey</span><span class="sxs-lookup"><span data-stu-id="b304c-177">encryptedkey</span></span>   | <span data-ttu-id="b304c-178">**位元組** 序列，代表加密工作階段金鑰資料（格式為 PKCS \# 1），類型2加密區塊。</span><span class="sxs-lookup"><span data-stu-id="b304c-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="b304c-179">如需此資料格式的相關資訊，請參閱 \# RSA Data Security，inc. 發行的公開金鑰加密標準 (PKCS) 1。這項資料的大小一律與公開金鑰的模數相同。</span><span class="sxs-lookup"><span data-stu-id="b304c-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="b304c-180">例如，Microsoft RSA 基底提供者所產生的公開金鑰可能是512位 (64 個位元組) 長度，因此加密的工作階段金鑰資料也一律為512位 (64 位元組) 。</span><span class="sxs-lookup"><span data-stu-id="b304c-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="b304c-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="b304c-181">publickeystruc</span></span> | <span data-ttu-id="b304c-182">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="b304c-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="b304c-183">如需基底提供者和擴充的提供者金鑰 Blob 的相關資訊，請參閱 [基底提供者金鑰 blob](base-provider-key-blobs.md)。</span><span class="sxs-lookup"><span data-stu-id="b304c-183">For information about the Base Provider and Extended Provider key BLOBs, see [Base Provider Key BLOBs](base-provider-key-blobs.md).</span></span>

 

 

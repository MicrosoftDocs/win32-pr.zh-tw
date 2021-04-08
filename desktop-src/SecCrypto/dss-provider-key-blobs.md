---
description: 與數位簽章標準 (DSS) 提供者一起使用，可在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: DSS 提供者金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943334"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="b1d3c-103">DSS 提供者金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b1d3c-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="b1d3c-104">[*Blob*](../secgloss/b-gly.md) 可與 [*數位簽章標準*](../secgloss/d-gly.md) (DSS) 提供者一起使用，以在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="b1d3c-105">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b1d3c-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="b1d3c-106">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b1d3c-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="b1d3c-107">公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b1d3c-107">Public Key BLOBs</span></span>

<span data-ttu-id="b1d3c-108">DSS [*公開金鑰*](../secgloss/p-gly.md) 會匯出並匯入為 BLOB，這是一系列結構如下的位元組。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="b1d3c-109">下表描述這些元件。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-109">The following table describes these components.</span></span> <span data-ttu-id="b1d3c-110">所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="b1d3c-111">欄位</span><span class="sxs-lookup"><span data-stu-id="b1d3c-111">Field</span></span>          | <span data-ttu-id="b1d3c-112">描述</span><span class="sxs-lookup"><span data-stu-id="b1d3c-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d3c-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="b1d3c-113">dsspubkey</span></span>      | <span data-ttu-id="b1d3c-114">[**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85))結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="b1d3c-115">**魔術** 成員的值必須是0x31535344。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="b1d3c-116">此十六進位數位是 DSS1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="b1d3c-117">g</span><span class="sxs-lookup"><span data-stu-id="b1d3c-117">g</span></span>              | <span data-ttu-id="b1d3c-118">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-118">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-119">發電機，g。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-119">The generator, g.</span></span> <span data-ttu-id="b1d3c-120">必須與 p 的長度相同。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-120">Must be the same length as p.</span></span> <span data-ttu-id="b1d3c-121">如果與 p 的長度不同，則必須以0x00 位元組填補。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="b1d3c-122">p</span><span class="sxs-lookup"><span data-stu-id="b1d3c-122">p</span></span>              | <span data-ttu-id="b1d3c-123">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-123">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-124">質數模數 p。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-124">The prime modulus, p.</span></span> <span data-ttu-id="b1d3c-125">最重要的位元組中最重要的位必須設定為一個。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="b1d3c-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="b1d3c-126">publickeystruc</span></span> | <span data-ttu-id="b1d3c-127">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="b1d3c-128">q</span><span class="sxs-lookup"><span data-stu-id="b1d3c-128">q</span></span>              | <span data-ttu-id="b1d3c-129">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-129">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-130">質數、q、20位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="b1d3c-131">最重要的位元組中最重要的位必須設定為一個。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="b1d3c-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="b1d3c-132">seedstruct</span></span>     | <span data-ttu-id="b1d3c-133">[**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed)結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="b1d3c-134">用於驗證質數的種子和計數器值。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="b1d3c-135">y</span><span class="sxs-lookup"><span data-stu-id="b1d3c-135">y</span></span>              | <span data-ttu-id="b1d3c-136">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-136">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-137">公開金鑰，y。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-137">The public key, y.</span></span> <span data-ttu-id="b1d3c-138">的長度必須與 p 相同。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-138">Must be same length as p.</span></span> <span data-ttu-id="b1d3c-139">如果與 p 的長度不同，則必須以0x00 位元組填補。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="b1d3c-140">[*公開金鑰 blob*](../secgloss/p-gly.md) 未加密。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="b1d3c-141">它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="b1d3c-142">私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="b1d3c-142">Private Key BLOBs</span></span>

<span data-ttu-id="b1d3c-143">DSS [*私密金鑰*](../secgloss/p-gly.md) 會以位元組順序匯出和匯入，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="b1d3c-144">下表說明每個元件。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-144">The following table describes each component.</span></span> <span data-ttu-id="b1d3c-145">所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="b1d3c-146">欄位</span><span class="sxs-lookup"><span data-stu-id="b1d3c-146">Field</span></span>          | <span data-ttu-id="b1d3c-147">描述</span><span class="sxs-lookup"><span data-stu-id="b1d3c-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d3c-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="b1d3c-148">dsspubkey</span></span>      | <span data-ttu-id="b1d3c-149">[**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85))結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="b1d3c-150">**魔術** 成員必須設為0x32535344。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="b1d3c-151">此十六進位數位是 DSS2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="b1d3c-152">g</span><span class="sxs-lookup"><span data-stu-id="b1d3c-152">g</span></span>              | <span data-ttu-id="b1d3c-153">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-153">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-154">發電機，g。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-154">The generator, g.</span></span> <span data-ttu-id="b1d3c-155">必須與 p 的長度相同。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-155">Must be the same length as p.</span></span> <span data-ttu-id="b1d3c-156">如果與 p 的長度不同，則必須以0x00 位元組填補。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="b1d3c-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="b1d3c-157">publickeystruc</span></span> | <span data-ttu-id="b1d3c-158">[**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="b1d3c-159">p</span><span class="sxs-lookup"><span data-stu-id="b1d3c-159">p</span></span>              | <span data-ttu-id="b1d3c-160">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-160">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-161">質數模數 p。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-161">The prime modulus, p.</span></span> <span data-ttu-id="b1d3c-162">最重要的位元組中最重要的位必須設定為一個。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="b1d3c-163">q</span><span class="sxs-lookup"><span data-stu-id="b1d3c-163">q</span></span>              | <span data-ttu-id="b1d3c-164">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-164">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-165">質數、q。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-165">The prime, q.</span></span> <span data-ttu-id="b1d3c-166">q 的長度是20個位元組。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-166">q is 20 bytes in length.</span></span> <span data-ttu-id="b1d3c-167">最重要的位元組中最重要的位必須設定為一個。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="b1d3c-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="b1d3c-168">seedstruct</span></span>     | <span data-ttu-id="b1d3c-169">[**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed)結構。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="b1d3c-170">用於驗證質數的種子和計數器值。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="b1d3c-171">x</span><span class="sxs-lookup"><span data-stu-id="b1d3c-171">x</span></span>              | <span data-ttu-id="b1d3c-172">**位元組** 序列。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-172">A **BYTE** sequence.</span></span> <span data-ttu-id="b1d3c-173">秘密指數 x。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-173">The secret exponent, x.</span></span> <span data-ttu-id="b1d3c-174">必須一律為20個位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="b1d3c-175">如果 x 的長度小於20個位元組，則必須以0x00 填補。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="b1d3c-176">呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="b1d3c-177">如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="b1d3c-178">但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="b1d3c-179">加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="b1d3c-180">應用程式必須管理和儲存此資訊。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-180">The application must manage and store this information.</span></span> <span data-ttu-id="b1d3c-181">如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="b1d3c-182">匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。</span><span class="sxs-lookup"><span data-stu-id="b1d3c-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 

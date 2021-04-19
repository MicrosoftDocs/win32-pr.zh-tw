---
description: 不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者隔開。
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: CNG 密碼編譯演算法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988322"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="b897d-103">CNG 密碼編譯演算法提供者</span><span class="sxs-lookup"><span data-stu-id="b897d-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="b897d-104">不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者隔開。</span><span class="sxs-lookup"><span data-stu-id="b897d-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="b897d-105">基本密碼編譯演算法作業（例如雜湊和簽章）稱為基本作業或單純的基本作業。</span><span class="sxs-lookup"><span data-stu-id="b897d-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="b897d-106">CNG 包含可執行下列演算法的提供者。</span><span class="sxs-lookup"><span data-stu-id="b897d-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="b897d-107">對稱演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="b897d-108">非對稱演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="b897d-109">雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="b897d-110">金鑰交換演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="b897d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="b897d-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="b897d-112">對稱演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="b897d-113">Name</span><span class="sxs-lookup"><span data-stu-id="b897d-113">Name</span></span>                                   | <span data-ttu-id="b897d-114">支援的模式</span><span class="sxs-lookup"><span data-stu-id="b897d-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="b897d-115">金鑰大小（位） (預設/最小/最大) </span><span class="sxs-lookup"><span data-stu-id="b897d-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b897d-116">進階加密標準 (AES)</span><span class="sxs-lookup"><span data-stu-id="b897d-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="b897d-117">ECB、CBC、CFB8、CFB128、GCM、CCM、GMAC、CMAC、AES 金鑰包裝、XTS</span><span class="sxs-lookup"><span data-stu-id="b897d-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="b897d-118">**Windows 8：** CFB128 和 CMAC 模式的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="b897d-119">**Windows 10：** 支援 XTS-AES 模式開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="b897d-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="b897d-120">128/192/256</span></span>                        |
| <span data-ttu-id="b897d-121">資料加密標準 (DES) </span><span class="sxs-lookup"><span data-stu-id="b897d-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="b897d-122">ECB、CBC、CFB8、CFB64</span><span class="sxs-lookup"><span data-stu-id="b897d-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="b897d-123">**Windows 8：** CFB64 模式的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="b897d-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="b897d-124">56/56/56</span></span>                           |
| <span data-ttu-id="b897d-125">資料加密標準進行 xor (DESX) </span><span class="sxs-lookup"><span data-stu-id="b897d-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="b897d-126">ECB、CBC、CFB8、CFB64</span><span class="sxs-lookup"><span data-stu-id="b897d-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="b897d-127">**Windows 8：** CFB64 模式的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="b897d-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="b897d-128">192/192/192</span></span>                        |
| <span data-ttu-id="b897d-129">三重資料加密標準 (3DES) </span><span class="sxs-lookup"><span data-stu-id="b897d-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="b897d-130">ECB、CBC、CFB8、CFB64</span><span class="sxs-lookup"><span data-stu-id="b897d-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="b897d-131">**Windows 8：** CFB64 模式的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="b897d-132">112/168</span><span class="sxs-lookup"><span data-stu-id="b897d-132">112/168</span></span>                            |
| <span data-ttu-id="b897d-133">RSA Data Security 2 (RC2) </span><span class="sxs-lookup"><span data-stu-id="b897d-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="b897d-134">支援 ECB、CBC、CFB8、CFB64 模式。</span><span class="sxs-lookup"><span data-stu-id="b897d-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="b897d-135">**Windows 8：** CFB64 模式的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="b897d-136">8位遞增的16至128</span><span class="sxs-lookup"><span data-stu-id="b897d-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="b897d-137">RSA Data Security 4 (RC4) </span><span class="sxs-lookup"><span data-stu-id="b897d-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="b897d-138">8至512，以8位遞增</span><span class="sxs-lookup"><span data-stu-id="b897d-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="b897d-139">非對稱演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="b897d-140">名稱</span><span class="sxs-lookup"><span data-stu-id="b897d-140">Name</span></span>                              | <span data-ttu-id="b897d-141">注意</span><span class="sxs-lookup"><span data-stu-id="b897d-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="b897d-142">金鑰大小（位） (預設/最小/最大) </span><span class="sxs-lookup"><span data-stu-id="b897d-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b897d-143"> (DSA) 的數位簽章演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="b897d-144">針對1024與3072位之間的金鑰大小，執行符合 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="b897d-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="b897d-145">執行符合 FIPS 186-2 的金鑰大小，從512到1024位。</span><span class="sxs-lookup"><span data-stu-id="b897d-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="b897d-146">512至3072，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="b897d-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="b897d-147">**Windows 8：** 3072位金鑰的支援開始。</span><span class="sxs-lookup"><span data-stu-id="b897d-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="b897d-148">RSA</span><span class="sxs-lookup"><span data-stu-id="b897d-148">RSA</span></span>                               | <span data-ttu-id="b897d-149">包含使用 PKCS1 的 RSA 演算法、優化的非對稱式加密填補 (OAEP) 編碼或填補，或概率簽章配置 (PSS) 純文字填補</span><span class="sxs-lookup"><span data-stu-id="b897d-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="b897d-150">512至16384，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="b897d-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="b897d-151">雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-151">Hashing Algorithms</span></span>



| <span data-ttu-id="b897d-152">名稱</span><span class="sxs-lookup"><span data-stu-id="b897d-152">Name</span></span>                               | <span data-ttu-id="b897d-153">注意</span><span class="sxs-lookup"><span data-stu-id="b897d-153">Notes</span></span>               | <span data-ttu-id="b897d-154">金鑰大小（位） (預設/最小/最大) </span><span class="sxs-lookup"><span data-stu-id="b897d-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="b897d-155">安全雜湊演算法 1 (SHA1) </span><span class="sxs-lookup"><span data-stu-id="b897d-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="b897d-156">包含 HmacSha1</span><span class="sxs-lookup"><span data-stu-id="b897d-156">Includes HmacSha1</span></span>   | <span data-ttu-id="b897d-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="b897d-157">160/160/160</span></span>                        |
| <span data-ttu-id="b897d-158">安全雜湊演算法 256 (SHA256) </span><span class="sxs-lookup"><span data-stu-id="b897d-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="b897d-159">包含 HmacSha256</span><span class="sxs-lookup"><span data-stu-id="b897d-159">Includes HmacSha256</span></span> | <span data-ttu-id="b897d-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="b897d-160">256/256/256</span></span>                        |
| <span data-ttu-id="b897d-161">安全雜湊演算法 384 (SHA384) </span><span class="sxs-lookup"><span data-stu-id="b897d-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="b897d-162">包含 HmacSha384</span><span class="sxs-lookup"><span data-stu-id="b897d-162">Includes HmacSha384</span></span> | <span data-ttu-id="b897d-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="b897d-163">384/384/384</span></span>                        |
| <span data-ttu-id="b897d-164">安全雜湊演算法 512 (SHA512) </span><span class="sxs-lookup"><span data-stu-id="b897d-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="b897d-165">包含 HmacSha512</span><span class="sxs-lookup"><span data-stu-id="b897d-165">Includes HmacSha512</span></span> | <span data-ttu-id="b897d-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="b897d-166">512/512/512</span></span>                        |
| <span data-ttu-id="b897d-167">訊息摘要 2 (MD2) </span><span class="sxs-lookup"><span data-stu-id="b897d-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="b897d-168">包含 HmacMd2</span><span class="sxs-lookup"><span data-stu-id="b897d-168">Includes HmacMd2</span></span>    | <span data-ttu-id="b897d-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="b897d-169">128/128/128</span></span>                        |
| <span data-ttu-id="b897d-170">訊息摘要 4 (MD4) </span><span class="sxs-lookup"><span data-stu-id="b897d-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="b897d-171">包含 HmacMd4</span><span class="sxs-lookup"><span data-stu-id="b897d-171">Includes HmacMd4</span></span>    | <span data-ttu-id="b897d-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="b897d-172">128/128/128</span></span>                        |
| <span data-ttu-id="b897d-173">訊息摘要 5 (MD5) </span><span class="sxs-lookup"><span data-stu-id="b897d-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="b897d-174">包含 HmacMd5</span><span class="sxs-lookup"><span data-stu-id="b897d-174">Includes HmacMd5</span></span>    | <span data-ttu-id="b897d-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="b897d-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="b897d-176">金鑰交換演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b897d-177">演算法名稱</span><span class="sxs-lookup"><span data-stu-id="b897d-177">Algorithm name</span></span></th>
<th><span data-ttu-id="b897d-178">備註</span><span class="sxs-lookup"><span data-stu-id="b897d-178">Notes</span></span></th>
<th><span data-ttu-id="b897d-179">金鑰大小（位） (預設/最小/最大) </span><span class="sxs-lookup"><span data-stu-id="b897d-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b897d-180">Diffie-Hellman 金鑰交換演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="b897d-181">512至4096，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="b897d-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b897d-182"> (ECDH) 的橢圓曲線 Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="b897d-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="b897d-183">包含使用256、384和521位公開金鑰的曲線（如 SP800-56A 中所指定）。</span><span class="sxs-lookup"><span data-stu-id="b897d-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="b897d-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="b897d-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b897d-185"> (ECDSA) 的橢圓曲線數位簽章演算法</span><span class="sxs-lookup"><span data-stu-id="b897d-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="b897d-186">包含使用256、384和521位公開金鑰的曲線，如 FIPS 186-3 中所指定。</span><span class="sxs-lookup"><span data-stu-id="b897d-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b897d-187">若要顯示所有命名的橢圓曲線，請使用 <strong>Certutil displayEccCurve</strong>。</span><span class="sxs-lookup"><span data-stu-id="b897d-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="b897d-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="b897d-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b897d-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="b897d-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b897d-190">**CNG 演算法識別碼**</span><span class="sxs-lookup"><span data-stu-id="b897d-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="b897d-191">CNG 密碼編譯基本函數</span><span class="sxs-lookup"><span data-stu-id="b897d-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="b897d-192">瞭解密碼編譯提供者</span><span class="sxs-lookup"><span data-stu-id="b897d-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 


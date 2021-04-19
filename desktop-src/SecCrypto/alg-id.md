---
description: 指定演算法識別碼。
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: 'ALG_ID (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982759"
---
# <a name="alg_id"></a><span data-ttu-id="9c5bb-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="9c5bb-103">ALG_ID</span></span>

<span data-ttu-id="9c5bb-104">**ALG_ID** 資料類型會指定演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="9c5bb-105">此資料類型的參數會傳遞至 CryptoAPI 中的大部分函數。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="9c5bb-106">下表列出目前定義的演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="9c5bb-107">自訂 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (csp) 的作者可以定義新值。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="9c5bb-108">此外，自定義 csp 針對金鑰規格所使用的 ALG_ID **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 與提供者相依。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="9c5bb-109">目前的對應會在資料表之後。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c5bb-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="9c5bb-110">Identifier</span></span></th>
<th><span data-ttu-id="9c5bb-111">值</span><span class="sxs-lookup"><span data-stu-id="9c5bb-111">Value</span></span></th>
<th><span data-ttu-id="9c5bb-112">描述</span><span class="sxs-lookup"><span data-stu-id="9c5bb-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c5bb-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="9c5bb-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="9c5bb-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="9c5bb-114">0x00006603</span></span></td>
<td><span data-ttu-id="9c5bb-115"><a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="9c5bb-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="9c5bb-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="9c5bb-117">0x00006609</span></span></td>
<td><span data-ttu-id="9c5bb-118">具有等於112位之有效金鑰長度的雙金鑰 <a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="9c5bb-119">CALG_AES</span></span></td>
<td><span data-ttu-id="9c5bb-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="9c5bb-120">0x00006611</span></span></td>
<td><span data-ttu-id="9c5bb-121">進階加密標準 (AES) 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="9c5bb-122"><a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="9c5bb-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="9c5bb-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="9c5bb-124">0x0000660e</span></span></td>
<td><span data-ttu-id="9c5bb-125">128位 AES。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-125">128 bit AES.</span></span> <span data-ttu-id="9c5bb-126"><a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="9c5bb-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="9c5bb-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="9c5bb-128">0x0000660f</span></span></td>
<td><span data-ttu-id="9c5bb-129">192位 AES。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-129">192 bit AES.</span></span> <span data-ttu-id="9c5bb-130"><a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="9c5bb-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="9c5bb-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="9c5bb-132">0x00006610</span></span></td>
<td><span data-ttu-id="9c5bb-133">256位 AES。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-133">256 bit AES.</span></span> <span data-ttu-id="9c5bb-134"><a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="9c5bb-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="9c5bb-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="9c5bb-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="9c5bb-137">Diffie-hellman 的控制碼的暫存演算法識別碼-已同意的金鑰。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="9c5bb-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="9c5bb-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="9c5bb-139">0x0000660c</span></span></td>
<td><span data-ttu-id="9c5bb-140">用來建立40位 DES 金鑰的演算法，該金鑰具有同位位和零的金鑰位，以使其金鑰長度64位。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="9c5bb-141"><a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="9c5bb-142">CALG_DES</span></span></td>
<td><span data-ttu-id="9c5bb-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="9c5bb-143">0x00006601</span></span></td>
<td><span data-ttu-id="9c5bb-144">DES 加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="9c5bb-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="9c5bb-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="9c5bb-146">0x00006604</span></span></td>
<td><span data-ttu-id="9c5bb-147">DESX 加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="9c5bb-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="9c5bb-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="9c5bb-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="9c5bb-150">Diffie-Hellman 暫時金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="9c5bb-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="9c5bb-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="9c5bb-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="9c5bb-153">Diffie-Hellman 儲存和轉寄金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="9c5bb-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="9c5bb-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="9c5bb-155">0x00002200</span></span></td>
<td><span data-ttu-id="9c5bb-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰</em></a> 簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="9c5bb-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="9c5bb-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="9c5bb-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="9c5bb-159">橢圓曲線 Diffie-Hellman 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c5bb-160">只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9c5bb-161"><strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="9c5bb-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="9c5bb-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="9c5bb-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="9c5bb-164">暫時的橢圓曲線 Diffie-Hellman 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c5bb-165">只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9c5bb-166"><strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="9c5bb-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="9c5bb-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="9c5bb-168">0x00002203</span></span></td>
<td><span data-ttu-id="9c5bb-169">橢圓曲線數位簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c5bb-170">只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9c5bb-171"><strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="9c5bb-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="9c5bb-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="9c5bb-173">0x0000a001</span></span></td>
<td><span data-ttu-id="9c5bb-174">橢圓曲線 Menezes、Qu 和 Vanstone (MQV) 的金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="9c5bb-175">不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="9c5bb-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="9c5bb-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="9c5bb-177">0x0000800b</span></span></td>
<td><span data-ttu-id="9c5bb-178">單向函數雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="9c5bb-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="9c5bb-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="9c5bb-180">0x0000a003</span></span></td>
<td><span data-ttu-id="9c5bb-181">Hughes MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="9c5bb-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="9c5bb-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="9c5bb-183">0x00008009</span></span></td>
<td><span data-ttu-id="9c5bb-184">HMAC 金鑰雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="9c5bb-185"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="9c5bb-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="9c5bb-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="9c5bb-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="9c5bb-188"> (FORTEZZA) 的 KEA 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="9c5bb-189">不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="9c5bb-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="9c5bb-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="9c5bb-191">0x00008005</span></span></td>
<td><span data-ttu-id="9c5bb-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> 金鑰雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="9c5bb-193"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="9c5bb-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="9c5bb-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="9c5bb-195">0x00008001</span></span></td>
<td><span data-ttu-id="9c5bb-196">MD2 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="9c5bb-197"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="9c5bb-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="9c5bb-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="9c5bb-199">0x00008002</span></span></td>
<td><span data-ttu-id="9c5bb-200">MD4 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="9c5bb-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="9c5bb-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="9c5bb-202">0x00008003</span></span></td>
<td><span data-ttu-id="9c5bb-203">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="9c5bb-204"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="9c5bb-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="9c5bb-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="9c5bb-206">0x00002000</span></span></td>
<td><span data-ttu-id="9c5bb-207">沒有簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="9c5bb-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="9c5bb-209">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="9c5bb-209">0xffffffff</span></span></td>
<td><span data-ttu-id="9c5bb-210">演算法只會在 CNG 中執行。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="9c5bb-211">宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c5bb-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="9c5bb-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="9c5bb-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="9c5bb-214">演算法是在編碼的參數中定義。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="9c5bb-215">只有使用 CNG 才支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="9c5bb-216">宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="9c5bb-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="9c5bb-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="9c5bb-218">0x00004c04</span></span></td>
<td><span data-ttu-id="9c5bb-219">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-220">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="9c5bb-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="9c5bb-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="9c5bb-222">0x00006602</span></span></td>
<td><span data-ttu-id="9c5bb-223">RC2 區塊加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="9c5bb-224"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="9c5bb-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="9c5bb-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="9c5bb-226">0x00006801</span></span></td>
<td><span data-ttu-id="9c5bb-227">RC4 資料流程加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="9c5bb-228"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="9c5bb-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="9c5bb-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="9c5bb-230">0x0000660d</span></span></td>
<td><span data-ttu-id="9c5bb-231">RC5 區塊加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="9c5bb-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="9c5bb-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="9c5bb-233">0x0000a400</span></span></td>
<td><span data-ttu-id="9c5bb-234">RSA 公開金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="9c5bb-235"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="9c5bb-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="9c5bb-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="9c5bb-237">0x00002400</span></span></td>
<td><span data-ttu-id="9c5bb-238">RSA 公開金鑰簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="9c5bb-239"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="9c5bb-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="9c5bb-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="9c5bb-241">0x00004c07</span></span></td>
<td><span data-ttu-id="9c5bb-242">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-243">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="9c5bb-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="9c5bb-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="9c5bb-245">0x00004c03</span></span></td>
<td><span data-ttu-id="9c5bb-246">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-247">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="9c5bb-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="9c5bb-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="9c5bb-249">0x00004c02</span></span></td>
<td><span data-ttu-id="9c5bb-250">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-251">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="9c5bb-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="9c5bb-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="9c5bb-253">0x00006802</span></span></td>
<td><span data-ttu-id="9c5bb-254">密封加密演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="9c5bb-255">不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="9c5bb-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="9c5bb-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="9c5bb-257">0x00008004</span></span></td>
<td><span data-ttu-id="9c5bb-258">SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-258">SHA hashing algorithm.</span></span> <span data-ttu-id="9c5bb-259"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="9c5bb-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="9c5bb-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="9c5bb-261">0x00008004</span></span></td>
<td><span data-ttu-id="9c5bb-262">與 <strong>CALG_SHA</strong>相同。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="9c5bb-263"><a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="9c5bb-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="9c5bb-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="9c5bb-265">0x0000800c</span></span></td>
<td><span data-ttu-id="9c5bb-266">256位 SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="9c5bb-267">Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="9c5bb-268"><strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="9c5bb-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="9c5bb-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="9c5bb-270">0x0000800d</span></span></td>
<td><span data-ttu-id="9c5bb-271">384位 SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="9c5bb-272">Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="9c5bb-273"><strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="9c5bb-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="9c5bb-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="9c5bb-275">0x0000800e</span></span></td>
<td><span data-ttu-id="9c5bb-276">512位 SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="9c5bb-277">Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="9c5bb-278"><strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="9c5bb-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="9c5bb-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="9c5bb-280">0x0000660a</span></span></td>
<td><span data-ttu-id="9c5bb-281">Skipjack 區塊加密演算法 (FORTEZZA) 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="9c5bb-282">不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="9c5bb-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="9c5bb-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="9c5bb-284">0x00004c05</span></span></td>
<td><span data-ttu-id="9c5bb-285">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-286">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="9c5bb-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="9c5bb-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="9c5bb-288">0x00004c01</span></span></td>
<td><span data-ttu-id="9c5bb-289">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-290">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="9c5bb-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="9c5bb-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="9c5bb-292">0x00008008</span></span></td>
<td><span data-ttu-id="9c5bb-293">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-294">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="9c5bb-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="9c5bb-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="9c5bb-296">0x0000660b</span></span></td>
<td><span data-ttu-id="9c5bb-297">TEK-TIPS FORUMS (FORTEZZA) 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="9c5bb-298">不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c5bb-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="9c5bb-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="9c5bb-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="9c5bb-300">0x00004c06</span></span></td>
<td><span data-ttu-id="9c5bb-301">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-302">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c5bb-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="9c5bb-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="9c5bb-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="9c5bb-304">0x0000800a</span></span></td>
<td><span data-ttu-id="9c5bb-305">由 Schannel.dll 作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="9c5bb-306">應用程式不應使用此 <strong>ALG_ID</strong> 。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9c5bb-307">針對 [Microsoft 基礎密碼編譯提供者](microsoft-base-cryptographic-provider.md)、 [microsoft 強式密碼](microsoft-strong-cryptographic-provider.md)編譯提供者，[以及 Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)，用於 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的主要規格 **ALG_IDs** 如下所示：</span><span class="sxs-lookup"><span data-stu-id="9c5bb-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="9c5bb-308">**CALG_RSA_KEYX** 用於 **AT_KEYEXCHANGE**。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="9c5bb-309">**CALG_RSA_SIGN** 用於 **AT_SIGNATURE**。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="9c5bb-310">針對 [Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)，用於金鑰規格 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的 **ALG_IDs** 如下所示：</span><span class="sxs-lookup"><span data-stu-id="9c5bb-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="9c5bb-311">**CALG_DH_SF** 用於 **AT_KEYEXCHANGE**。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="9c5bb-312">**CALG_DSS_SIGN** 用於 **AT_SIGNATURE**。</span><span class="sxs-lookup"><span data-stu-id="9c5bb-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c5bb-313">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c5bb-313">Requirements</span></span>



| <span data-ttu-id="9c5bb-314">需求</span><span class="sxs-lookup"><span data-stu-id="9c5bb-314">Requirement</span></span> | <span data-ttu-id="9c5bb-315">值</span><span class="sxs-lookup"><span data-stu-id="9c5bb-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5bb-316">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c5bb-316">Minimum supported client</span></span><br/> | <span data-ttu-id="9c5bb-317">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c5bb-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9c5bb-318">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c5bb-318">Minimum supported server</span></span><br/> | <span data-ttu-id="9c5bb-319">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c5bb-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c5bb-320">標頭</span><span class="sxs-lookup"><span data-stu-id="9c5bb-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c5bb-321"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c5bb-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c5bb-322">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c5bb-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c5bb-323">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="9c5bb-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="9c5bb-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="9c5bb-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="9c5bb-325">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="9c5bb-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 

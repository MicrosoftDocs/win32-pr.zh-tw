---
description: 用來識別各種 CNG 函數和結構中的標準加密演算法，例如 CRYPT \_ 介面 \_ REG 結構。
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: 'CNG 演算法識別碼 (Bcrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba244f2a815933322793fdd572ed7a4e69256a0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000239"
---
# <a name="cng-algorithm-identifiers"></a><span data-ttu-id="7452b-103">CNG 演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="7452b-103">CNG Algorithm Identifiers</span></span>

<span data-ttu-id="7452b-104">下列識別碼用來識別各種 CNG 函式和結構中的標準加密演算法，例如 [**CRYPT \_ 介面 \_ REG**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) 結構。</span><span class="sxs-lookup"><span data-stu-id="7452b-104">The following identifiers are used to identify standard encryption algorithms in various CNG functions and structures, such as the [**CRYPT\_INTERFACE\_REG**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) structure.</span></span> <span data-ttu-id="7452b-105">協力廠商提供者可能會有其他支援的演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-105">Third party providers may have additional algorithms that they support.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7452b-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="7452b-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7452b-107">Description</span><span class="sxs-lookup"><span data-stu-id="7452b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <span data-ttu-id="7452b-108"><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3des &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-108"><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt>&quot;3DES&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-109">三重資料加密標準對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-109">The triple data encryption standard symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-110">標準： SP800-67，SP800-38A</span><span class="sxs-lookup"><span data-stu-id="7452b-110">Standard: SP800-67, SP800-38A</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <span data-ttu-id="7452b-111"><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-111"><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt>&quot;3DES_112&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-112">112位的三重資料加密標準對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-112">The 112-bit triple data encryption standard symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-113">標準： SP800-67，SP800-38A</span><span class="sxs-lookup"><span data-stu-id="7452b-113">Standard: SP800-67, SP800-38A</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <span data-ttu-id="7452b-114"><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-114"><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt>&quot;AES&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-115">Advanced encryption standard 對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-115">The advanced encryption standard symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-116">標準： FIPS 197</span><span class="sxs-lookup"><span data-stu-id="7452b-116">Standard: FIPS 197</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <span data-ttu-id="7452b-117"><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-117"><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt>&quot;AES-CMAC&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-118">Advanced encryption standard (AES) 以密碼為基礎的訊息驗證碼 (CMAC) 對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-118">The advanced encryption standard (AES) cipher based message authentication code (CMAC) symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-119">標準： SP 800-38B</span><span class="sxs-lookup"><span data-stu-id="7452b-119">Standard: SP 800-38B</span></span><br/> <span data-ttu-id="7452b-120"><strong>Windows 8：</strong> 此演算法的支援開始。</span><span class="sxs-lookup"><span data-stu-id="7452b-120"><strong>Windows 8:</strong> Support for this algorithm begins.</span></span><br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <span data-ttu-id="7452b-121"><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-121"><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt>&quot;AES-GMAC&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-122">Advanced encryption standard (AES) Galois 訊息驗證碼 (GMAC) 對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-122">The advanced encryption standard (AES) Galois message authentication code (GMAC) symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-123">標準： SP800-38D</span><span class="sxs-lookup"><span data-stu-id="7452b-123">Standard: SP800-38D</span></span><br/> <span data-ttu-id="7452b-124"><strong>Windows Vista：</strong> 從 Windows Vista SP1 開始支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-124"><strong>Windows Vista:</strong> This algorithm is supported beginning with Windows Vista with SP1.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <span data-ttu-id="7452b-125"><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-125"><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L&quot;CAPI_KDF&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-126"> (CAPI) 金鑰衍生函式演算法的加密 API。</span><span class="sxs-lookup"><span data-stu-id="7452b-126">Crypto API (CAPI) key derivation function algorithm.</span></span> <span data-ttu-id="7452b-127">由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7452b-127">Used by the <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> and <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <span data-ttu-id="7452b-128"><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; DES &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-128"><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt>&quot;DES&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-129">資料加密標準對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-129">The data encryption standard symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-130">標準： FIPS 46-3、FIPS 81</span><span class="sxs-lookup"><span data-stu-id="7452b-130">Standard: FIPS 46-3, FIPS 81</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <span data-ttu-id="7452b-131"><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-131"><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt>&quot;DESX&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-132">擴充的資料加密標準對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-132">The extended data encryption standard symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-133">標準：無</span><span class="sxs-lookup"><span data-stu-id="7452b-133">Standard: None</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <span data-ttu-id="7452b-134"><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-134"><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt>&quot;DH&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-135">Diffie-Hellman 的金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-135">The Diffie-Hellman key exchange algorithm.</span></span><br/> <span data-ttu-id="7452b-136">標準： PKCS #3</span><span class="sxs-lookup"><span data-stu-id="7452b-136">Standard: PKCS #3</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <span data-ttu-id="7452b-137"><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-137"><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt>&quot;DSA&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-138">數位簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-138">The digital signature algorithm.</span></span><br/> <span data-ttu-id="7452b-139">標準： FIPS 186-2</span><span class="sxs-lookup"><span data-stu-id="7452b-139">Standard: FIPS 186-2</span></span><br/> <span data-ttu-id="7452b-140"><strong>Windows 8：</strong> 從 Windows 8 開始，此演算法支援 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-140"><strong>Windows 8:</strong> Beginning with Windows 8, this algorithm supports FIPS 186-3.</span></span> <span data-ttu-id="7452b-141">小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-141">Keys less than or equal to 1024 bits adhere to FIPS 186-2 and keys greater than 1024 to FIPS 186-3.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <span data-ttu-id="7452b-142"><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-142"><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt>&quot;ECDH_P256&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-143">256位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-143">The 256-bit prime elliptic curve Diffie-Hellman key exchange algorithm.</span></span><br/> <span data-ttu-id="7452b-144">標準： SP800-56A</span><span class="sxs-lookup"><span data-stu-id="7452b-144">Standard: SP800-56A</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <span data-ttu-id="7452b-145"><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-145"><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt>&quot;ECDH_P384&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-146">384位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-146">The 384-bit prime elliptic curve Diffie-Hellman key exchange algorithm.</span></span><br/> <span data-ttu-id="7452b-147">標準： SP800-56A</span><span class="sxs-lookup"><span data-stu-id="7452b-147">Standard: SP800-56A</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <span data-ttu-id="7452b-148"><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-148"><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt>&quot;ECDH_P521&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-149">521位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-149">The 521-bit prime elliptic curve Diffie-Hellman key exchange algorithm.</span></span><br/> <span data-ttu-id="7452b-150">標準： SP800-56A</span><span class="sxs-lookup"><span data-stu-id="7452b-150">Standard: SP800-56A</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <span data-ttu-id="7452b-151"><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-151"><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt>&quot;ECDSA_P256&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-152">256位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="7452b-152">The 256-bit prime elliptic curve digital signature algorithm (FIPS 186-2).</span></span><br/> <span data-ttu-id="7452b-153">標準： FIPS 186-2、X x9.62</span><span class="sxs-lookup"><span data-stu-id="7452b-153">Standard: FIPS 186-2, X9.62</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <span data-ttu-id="7452b-154"><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-154"><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt>&quot;ECDSA_P384&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-155">384位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="7452b-155">The 384-bit prime elliptic curve digital signature algorithm (FIPS 186-2).</span></span><br/> <span data-ttu-id="7452b-156">標準： FIPS 186-2、X x9.62</span><span class="sxs-lookup"><span data-stu-id="7452b-156">Standard: FIPS 186-2, X9.62</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <span data-ttu-id="7452b-157"><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-157"><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt>&quot;ECDSA_P521&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-158">521位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="7452b-158">The 521-bit prime elliptic curve digital signature algorithm (FIPS 186-2).</span></span><br/> <span data-ttu-id="7452b-159">標準： FIPS 186-2、X x9.62</span><span class="sxs-lookup"><span data-stu-id="7452b-159">Standard: FIPS 186-2, X9.62</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <span data-ttu-id="7452b-160"><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-160"><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt>&quot;MD2&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-161">MD2 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-161">The MD2 hash algorithm.</span></span><br/> <span data-ttu-id="7452b-162">標準： RFC 1319</span><span class="sxs-lookup"><span data-stu-id="7452b-162">Standard: RFC 1319</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <span data-ttu-id="7452b-163"><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-163"><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt>&quot;MD4&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-164">MD4 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-164">The MD4 hash algorithm.</span></span><br/> <span data-ttu-id="7452b-165">標準： RFC 1320</span><span class="sxs-lookup"><span data-stu-id="7452b-165">Standard: RFC 1320</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <span data-ttu-id="7452b-166"><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-166"><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt>&quot;MD5&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-167">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-167">The MD5 hash algorithm.</span></span><br/> <span data-ttu-id="7452b-168">標準： RFC 1321</span><span class="sxs-lookup"><span data-stu-id="7452b-168">Standard: RFC 1321</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <span data-ttu-id="7452b-169"><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-169"><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt>&quot;RC2&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-170">RC2 區塊對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-170">The RC2 block symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-171">標準： RFC 2268</span><span class="sxs-lookup"><span data-stu-id="7452b-171">Standard: RFC 2268</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <span data-ttu-id="7452b-172"><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-172"><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt>&quot;RC4&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-173">RC4 對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-173">The RC4 symmetric encryption algorithm.</span></span><br/> <span data-ttu-id="7452b-174">標準：各種</span><span class="sxs-lookup"><span data-stu-id="7452b-174">Standard: Various</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <span data-ttu-id="7452b-175"><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-175"><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt>&quot;RNG&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-176">亂數字產生器演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-176">The random-number generator algorithm.</span></span><br/> <span data-ttu-id="7452b-177">標準： FIPS 186-2、FIPS 140-2、NIST SP 800-90</span><span class="sxs-lookup"><span data-stu-id="7452b-177">Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7452b-178">從 Windows Vista SP1 和 Windows Server 2008 開始，亂數產生器是以 NIST SP 800-90 標準中指定的 AES 計數器模式為基礎。</span><span class="sxs-lookup"><span data-stu-id="7452b-178">Beginning with Windows Vista with SP1 and Windows Server 2008, the random number generator is based on the AES counter mode specified in the NIST SP 800-90 standard.</span></span>
</blockquote>
<br/> <span data-ttu-id="7452b-179"><strong>Windows Vista：</strong> 亂數產生器是根據 FIPS 186-2 標準中指定的雜湊型亂數產生器。</span><span class="sxs-lookup"><span data-stu-id="7452b-179"><strong>Windows Vista:</strong> The random number generator is based on the hash-based random number generator specified in the FIPS 186-2 standard.</span></span><br/> <span data-ttu-id="7452b-180"><strong>Windows 8：</strong> 從 Windows 8 開始，RNG 演算法支援 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-180"><strong>Windows 8:</strong> Beginning with Windows 8, the RNG algorithm supports FIPS 186-3.</span></span> <span data-ttu-id="7452b-181">小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-181">Keys less than or equal to 1024 bits adhere to FIPS 186-2 and keys greater than 1024 to FIPS 186-3.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <span data-ttu-id="7452b-182"><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-182"><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt>&quot;DUALECRNG&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-183">雙重橢圓曲線亂數字產生器演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-183">The dual elliptic curve random-number generator algorithm.</span></span> <br/> <span data-ttu-id="7452b-184">標準： SP800-90。</span><span class="sxs-lookup"><span data-stu-id="7452b-184">Standard: SP800-90.</span></span><br/> <span data-ttu-id="7452b-185"><strong>Windows 8：</strong> 從 Windows 8 開始，EC RNG 演算法支援 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-185"><strong>Windows 8:</strong> Beginning with Windows 8, the EC RNG algorithm supports FIPS 186-3.</span></span> <span data-ttu-id="7452b-186">小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。</span><span class="sxs-lookup"><span data-stu-id="7452b-186">Keys less than or equal to 1024 bits adhere to FIPS 186-2 and keys greater than 1024 to FIPS 186-3.</span></span><br/> <span data-ttu-id="7452b-187"><strong>Windows 10：</strong> 從 Windows 10 開始，已移除雙重橢圓曲線亂數字產生器演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-187"><strong>Windows 10:</strong> Beginning with Windows 10, the dual elliptic curve random number generator algorithm has been removed.</span></span> <span data-ttu-id="7452b-188">此演算法的現有用法將繼續運作;不過，亂數產生器是以 NIST SP 800-90 標準中指定的 AES 計數器模式為基礎。</span><span class="sxs-lookup"><span data-stu-id="7452b-188">Existing uses of this algorithm will continue to work; however, the random number generator is based on the AES counter mode specified in the NIST SP 800-90 standard.</span></span> <span data-ttu-id="7452b-189">新的程式碼應該使用 <strong>BCRYPT_RNG_ALGORITHM</strong>，建議您將現有的程式碼變更為使用 <strong>BCRYPT_RNG_ALGORITHM</strong>。</span><span class="sxs-lookup"><span data-stu-id="7452b-189">New code should use <strong>BCRYPT_RNG_ALGORITHM</strong>, and it is recommended that existing code be changed to use <strong>BCRYPT_RNG_ALGORITHM</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <span data-ttu-id="7452b-190"><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-190"><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt>&quot;FIPS186DSARNG&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-191">適用于 DSA (數位簽章演算法) 的亂數字產生器演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-191">The random-number generator algorithm suitable for DSA (Digital Signature Algorithm).</span></span> <br/> <span data-ttu-id="7452b-192">標準： FIPS 186-2。</span><span class="sxs-lookup"><span data-stu-id="7452b-192">Standard: FIPS 186-2.</span></span><br/> <span data-ttu-id="7452b-193"><strong>Windows 8：</strong> FIPS 186-3 的支援開始。</span><span class="sxs-lookup"><span data-stu-id="7452b-193"><strong>Windows 8:</strong> Support for FIPS 186-3 begins.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <span data-ttu-id="7452b-194"><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-194"><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt>&quot;RSA&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-195">RSA 公開金鑰演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-195">The RSA public key algorithm.</span></span> <br/> <span data-ttu-id="7452b-196">標準： PKCS #1 1.5 和2.0 版。</span><span class="sxs-lookup"><span data-stu-id="7452b-196">Standard: PKCS #1 v1.5 and v2.0.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <span data-ttu-id="7452b-197"><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-197"><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt>&quot;RSA_SIGN&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-198">RSA 簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-198">The RSA signature algorithm.</span></span> <span data-ttu-id="7452b-199">目前不支援此演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-199">This algorithm is not currently supported.</span></span> <span data-ttu-id="7452b-200">您可以使用 <strong>BCRYPT_RSA_ALGORITHM</strong> 演算法來執行 RSA 簽署作業。</span><span class="sxs-lookup"><span data-stu-id="7452b-200">You can use the <strong>BCRYPT_RSA_ALGORITHM</strong> algorithm to perform RSA signing operations.</span></span> <br/> <span data-ttu-id="7452b-201">標準： PKCS #1 1.5 和2.0 版。</span><span class="sxs-lookup"><span data-stu-id="7452b-201">Standard: PKCS #1 v1.5 and v2.0.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <span data-ttu-id="7452b-202"><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-202"><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt>&quot;SHA1&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-203">160位的安全雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-203">The 160-bit secure hash algorithm.</span></span> <br/> <span data-ttu-id="7452b-204">標準： FIPS 180-2、FIPS 198。</span><span class="sxs-lookup"><span data-stu-id="7452b-204">Standard: FIPS 180-2, FIPS 198.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <span data-ttu-id="7452b-205"><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-205"><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt>&quot;SHA256&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-206">256位的安全雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-206">The 256-bit secure hash algorithm.</span></span><br/> <span data-ttu-id="7452b-207">標準： FIPS 180-2、FIPS 198。</span><span class="sxs-lookup"><span data-stu-id="7452b-207">Standard: FIPS 180-2, FIPS 198.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <span data-ttu-id="7452b-208"><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-208"><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt>&quot;SHA384&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-209">384位的安全雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-209">The 384-bit secure hash algorithm.</span></span> <br/> <span data-ttu-id="7452b-210">標準： FIPS 180-2、FIPS 198。</span><span class="sxs-lookup"><span data-stu-id="7452b-210">Standard: FIPS 180-2, FIPS 198.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <span data-ttu-id="7452b-211"><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-211"><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt>&quot;SHA512&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-212">512位的安全雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-212">The 512-bit secure hash algorithm.</span></span> <br/> <span data-ttu-id="7452b-213">標準： FIPS 180-2、FIPS 198。</span><span class="sxs-lookup"><span data-stu-id="7452b-213">Standard: FIPS 180-2, FIPS 198.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <span data-ttu-id="7452b-214"><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-214"><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L&quot;SP800_108_CTR_HMAC&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-215">計數器模式、雜湊式訊息驗證碼 (HMAC) 金鑰衍生函式演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-215">Counter mode, hash-based message authentication code (HMAC) key derivation function algorithm.</span></span> <span data-ttu-id="7452b-216">由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7452b-216">Used by the <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> and <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <span data-ttu-id="7452b-217"><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-217"><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L&quot;SP800_56A_CONCAT&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-218">SP800-56A 主要衍生函式演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-218">SP800-56A key derivation function algorithm.</span></span> <span data-ttu-id="7452b-219">由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7452b-219">Used by the <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> and <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <span data-ttu-id="7452b-220"><dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-220"><dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt> <dt>L&quot;PBKDF2&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-221">以密碼為基礎的金鑰衍生函數 2 (PBKDF2) 演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-221">Password-based key derivation function 2 (PBKDF2) algorithm.</span></span> <span data-ttu-id="7452b-222">由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7452b-222">Used by the <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> and <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <span data-ttu-id="7452b-223"><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-223"><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt>&quot;ECDSA&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-224">一般質數橢圓曲線數位簽章演算法 (如需詳細資訊) ，請參閱 <strong>備註</strong> 。</span><span class="sxs-lookup"><span data-stu-id="7452b-224">Generic prime elliptic curve digital signature algorithm (see <strong>Remarks</strong> for more information).</span></span> <br/> <span data-ttu-id="7452b-225">標準： ANSI X x9.62。</span><span class="sxs-lookup"><span data-stu-id="7452b-225">Standard: ANSI X9.62.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <span data-ttu-id="7452b-226"><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-226"><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt>&quot;ECDH&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-227">一般質數橢圓曲線 Diffie-Hellman 金鑰交換演算法 (如需詳細資訊，請參閱 <strong>備註</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="7452b-227">Generic prime elliptic curve Diffie-Hellman key exchange algorithm (see <strong>Remarks</strong> for more information).</span></span> <br/> <span data-ttu-id="7452b-228">標準： SP800-56A。</span><span class="sxs-lookup"><span data-stu-id="7452b-228">Standard: SP800-56A.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <span data-ttu-id="7452b-229"><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </span><span class="sxs-lookup"><span data-stu-id="7452b-229"><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt>&quot;XTS-AES&quot;</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7452b-230">XTS 模式中的先進加密標準對稱式加密演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-230">The advanced encryption standard symmetric encryption algorithm in XTS mode.</span></span> <br/> <span data-ttu-id="7452b-231">標準： SP-800-38E、IEEE Std 1619-2007。</span><span class="sxs-lookup"><span data-stu-id="7452b-231">Standard: SP-800-38E, IEEE Std 1619-2007.</span></span><br/> <span data-ttu-id="7452b-232"><strong>Windows 10：</strong> 此演算法的支援開始。</span><span class="sxs-lookup"><span data-stu-id="7452b-232"><strong>Windows 10:</strong> Support for this algorithm begins.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="7452b-233">備註</span><span class="sxs-lookup"><span data-stu-id="7452b-233">Remarks</span></span>

<span data-ttu-id="7452b-234">若要 **使用 BCRYPT \_ ecdsa \_ ALGORITM** 或 **BCRYPT \_ ecdh \_ 演算法**，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)做為 *pszAlgId*。</span><span class="sxs-lookup"><span data-stu-id="7452b-234">To use **BCRYPT\_ECDSA\_ALGORITM** or **BCRYPT\_ECDH\_ALGORITHM**, call [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) with either **BCRYPT\_ECDSA\_ALGORITHM** or **BCRYPT\_ECDH\_ALGORITHM** as the *pszAlgId*.</span></span> <span data-ttu-id="7452b-235">然後使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為 [CNG 命名曲線] 中所列的名為演算法。</span><span class="sxs-lookup"><span data-stu-id="7452b-235">Then use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) to set the **BCRYPT\_ECC\_CURVE\_NAME** property to a named algorithm listed in CNG Named Curves.</span></span>

<span data-ttu-id="7452b-236">若要直接提供使用者定義的橢圓曲線參數，請使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 來設定 **BCRYPT \_ ECC \_ 參數** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7452b-236">To provider user-defined elliptic curve parameters directly, use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) to set the **BCRYPT\_ECC\_PARAMETERS** property.</span></span> <span data-ttu-id="7452b-237">下載 [Windows 10 密碼編譯提供者開發人員套件 (CPDK) ](https://www.microsoft.com/download/details.aspx?id=30688) 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7452b-237">Download the [Windows 10 Cryptographic Provider Developer Kit (CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7452b-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="7452b-238">Requirements</span></span>



| <span data-ttu-id="7452b-239">需求</span><span class="sxs-lookup"><span data-stu-id="7452b-239">Requirement</span></span> | <span data-ttu-id="7452b-240">值</span><span class="sxs-lookup"><span data-stu-id="7452b-240">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7452b-241">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7452b-241">Minimum supported client</span></span><br/> | <span data-ttu-id="7452b-242">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7452b-242">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7452b-243">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7452b-243">Minimum supported server</span></span><br/> | <span data-ttu-id="7452b-244">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7452b-244">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7452b-245">標頭</span><span class="sxs-lookup"><span data-stu-id="7452b-245">Header</span></span><br/>                   | <dl> <span data-ttu-id="7452b-246"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="7452b-246"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7452b-247">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7452b-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7452b-248">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="7452b-248">**BCryptOpenAlgorithmProvider**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="7452b-249">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="7452b-249">**NCryptCreatePersistedKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 





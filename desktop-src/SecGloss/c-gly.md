---
description: 包含以字母 C 為開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: 'C (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863422525326ec0a04a597d33a29553006bb014b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979916"
---
# <a name="c-security-glossary"></a><span data-ttu-id="b1ec1-103">C (安全性詞彙) </span><span class="sxs-lookup"><span data-stu-id="b1ec1-103">C (Security Glossary)</span></span>

<span data-ttu-id="b1ec1-104">[](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="b1ec1-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b1ec1-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**約**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-106">請參閱 *憑證授權單位* 單位。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-106">See *certification authority*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA 憑證**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA certificate**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-108">識別 (CA) 的憑證授權單位單位，可對要求這些憑證的伺服器和用戶端發出伺服器和用戶端驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-108">Identifies the certification authority (CA) that issues server and client authentication certificates to the servers and clients that request these certificates.</span></span> <span data-ttu-id="b1ec1-109">由於此憑證包含數位簽章中所用的公開金鑰，因此也稱為「簽章憑證」(Signature Certificate)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-109">Because it contains a public key used in digital signatures, it is also referred to as a signature certificate.</span></span> <span data-ttu-id="b1ec1-110">如果 CA 是根授權單位，CA 憑證可能稱為根憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-110">If the CA is a root authority, the CA certificate may be referred to as a root certificate.</span></span> <span data-ttu-id="b1ec1-111">有時亦稱為「網站憑證」(Site Certificate)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-111">Also sometimes known as a site certificate.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA 階層**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA hierarchy**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-113">憑證授權單位單位 (CA) 階層包含多個 Ca。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-113">A certification authority (CA) hierarchy contains multiple CAs.</span></span> <span data-ttu-id="b1ec1-114">其組織方式是讓每個 CA 都經過較高層級階層中的另一個 CA 認證，直到達到階層的最上層（也稱為「根授權單位」）為止。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-114">It is organized such that each CA is certified by another CA in a higher level of the hierarchy until the top of the hierarchy, also known as the root authority, is reached.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG \_ DH \_ EPHEM**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG\_DH\_EPHEM**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-116">用於產生暫時金鑰時，Diffie-Hellman 金鑰交換演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-116">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of ephemeral keys.</span></span>

<span data-ttu-id="b1ec1-117">另請參閱 [*diffie-hellman (暫時) 金鑰交換演算法*](d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-117">See also [*Diffie-Hellman (ephemeral) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG \_ DH \_ SF**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG\_DH\_SF**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-119">用於產生儲存和轉寄索引鍵的 Diffie-Hellman 金鑰交換演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-119">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of store-and-forward keys.</span></span>

<span data-ttu-id="b1ec1-120">另請參閱 [*diffie-hellman (儲存和轉寄) 的金鑰交換演算法*](d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-120">See also [*Diffie-Hellman (store and forward) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG \_ HMAC**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG\_HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-122">以雜湊為基礎的訊息驗證碼演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-122">The CryptoAPI algorithm identifier for the hash-based Message Authentication Code algorithm.</span></span>

<span data-ttu-id="b1ec1-123">另請參閱以 [*雜湊為基礎的訊息驗證碼*](h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-123">See also [*Hash-Based Message Authentication Code*](h-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG \_ MAC**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG\_MAC**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-125">訊息驗證碼演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-125">The CryptoAPI algorithm identifier for the Message Authentication Code algorithm.</span></span>

<span data-ttu-id="b1ec1-126">另請參閱 [*訊息驗證碼*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-126">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG\_MD2**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-128">MD2 雜湊演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-128">The CryptoAPI algorithm identifier for the MD2 hash algorithm.</span></span>

<span data-ttu-id="b1ec1-129">另請參閱 [*MD2 演算法*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-129">See also [*MD2 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-131">MD5 雜湊演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-131">The CryptoAPI algorithm identifier for the MD5 hash algorithm.</span></span>

<span data-ttu-id="b1ec1-132">另請參閱 [*MD5 演算法*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-132">See also [*MD5 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG\_RC2**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-134">RC2 區塊加密演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-134">The CryptoAPI algorithm identifier for the RC2 block cipher algorithm.</span></span>

<span data-ttu-id="b1ec1-135">另請參閱 [*RC2 區塊演算法*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-135">See also [*RC2 block algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG\_RC4**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-137">RC4 資料流程加密演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-137">The CryptoAPI algorithm identifier for the RC4 stream cipher algorithm.</span></span>

<span data-ttu-id="b1ec1-138">另請參閱 [*RC4 串流演算法*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-138">See also [*RC4 stream algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG \_ RSA \_ KEYX**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG\_RSA\_KEYX**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-140">使用於金鑰交換時的 RSA 公開金鑰演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-140">The CryptoAPI algorithm identifier for the RSA public key algorithm when used for key exchange.</span></span>

<span data-ttu-id="b1ec1-141">另請參閱 [*RSA 公開金鑰演算法*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-141">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG \_ RSA \_ SIGN**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG\_RSA\_SIGN**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-143">用來產生數位簽章時，RSA 公開金鑰演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-143">The CryptoAPI algorithm identifier for the RSA public key algorithm when used to generate digital signatures.</span></span>

<span data-ttu-id="b1ec1-144">另請參閱 [*RSA 公開金鑰演算法*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-144">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG \_ SHA**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG\_SHA**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-146"> (SHA-1) 的安全雜湊演算法的 CryptoAPI 演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-146">The CryptoAPI algorithm identifier for the Secure Hash Algorithm (SHA-1).</span></span>

<span data-ttu-id="b1ec1-147">另請參閱 [*安全雜湊演算法*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-147">See also [*Secure Hash Algorithm*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**投**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-149">由 c. 所開發的一組 DES 對稱封鎖密碼。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-149">A group of DES-like symmetric block ciphers developed by C. M.</span></span> <span data-ttu-id="b1ec1-150">Adams 和 S. E。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-150">Adams and S. E.</span></span> <span data-ttu-id="b1ec1-151">塔瓦雷斯。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-151">Tavares.</span></span> <span data-ttu-id="b1ec1-152">>PROV \_ MS \_ EXCHANGE 提供者類型會指定使用64位區塊大小的特定轉換演算法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-152">PROV\_MS\_EXCHANGE provider types specify a particular CAST algorithm that uses a 64-bit block size.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**Cbc**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-154">請參閱 *加密區塊鏈*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-154">See *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**證書**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificate**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-156">包含實體與實體公開金鑰相關資訊的數位簽署陳述式，因此會將這兩個資訊片段繫結在一起。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-156">A digitally signed statement that contains information about an entity and the entity's public key, thus binding these two pieces of information together.</span></span> <span data-ttu-id="b1ec1-157">憑證是由信任的組織 (或稱為 *憑證授權單位單位) 證書 (頒發機構* 單位的實體在 ca 驗證該實體是否為其所指的實體之後) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-157">A certificate is issued by a trusted organization (or entity) called a *certification authority* (CA) after the CA has verified that the entity is who it says it is.</span></span>

<span data-ttu-id="b1ec1-158">憑證可包含不同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-158">Certificates can contain different types of data.</span></span> <span data-ttu-id="b1ec1-159">例如，X.509 憑證包含憑證格式、憑證序號、用來簽署憑證的演算法、發行憑證的 CA 名稱、要求憑證的實體名稱與其公開金鑰，以及 CA 的簽章。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-159">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the CA that issued the certificate, the name and public key of the entity requesting the certificate, and the CA's signature.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**憑證 BLOB**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**certificate BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-161">包含憑證資料的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-161">A BLOB that contains the certificate data.</span></span>

<span data-ttu-id="b1ec1-162">憑證 BLOB 是由呼叫 **CryptEncodeObject** 所建立。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-162">A certificate BLOB is created by calls to **CryptEncodeObject**.</span></span> <span data-ttu-id="b1ec1-163">當呼叫的輸出包含所有憑證資料時，此程式就會完成。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-163">The process is complete when the output of the call contains all the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**憑證內容**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**certificate context**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-165">\_憑證內容結構，其中包含憑證存放區的控制碼、原始編碼憑證 BLOB 的指標、憑證 \_ 資訊結構的指標，以及編碼類型成員。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-165">A CERT\_CONTEXT structure that contains a handle to a certificate store, a pointer to the original encoded certificate BLOB, a pointer to a CERT\_INFO structure, and an encoding type member.</span></span> <span data-ttu-id="b1ec1-166">它是包含大部分憑證資訊的 **CERT \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-166">It is the **CERT\_INFO** structure that contains most of the certificate information.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**憑證編碼/解碼函數**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**certificate encode/decode functions**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-168">管理將憑證和相關材質轉譯成可在不同環境中使用之標準二進位格式的函式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-168">Functions that manage the translation of certificates and related material into standard, binary formats that can be used in different environments.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**憑證編碼類型**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**certificate encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-170">定義憑證的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-170">Defines how the certificate is encoded.</span></span> <span data-ttu-id="b1ec1-171">憑證編碼類型會儲存在編碼類型 (**DWORD**) 結構的低序位字組中。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-171">The certificate encoding type is stored in the low-order word of the encoding type (**DWORD**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**透過 CMS 的憑證管理**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Certificate Management over CMS**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-173">Cmc。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-173">CMC.</span></span> <span data-ttu-id="b1ec1-174">透過 CMS 的憑證管理。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-174">Certificate Management over CMS.</span></span> <span data-ttu-id="b1ec1-175">CMC 是一種憑證管理通訊協定，它會使用 (CMS) 的密碼編譯訊息語法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-175">CMC is a certificate management protocol that uses Cryptographic Message Syntax (CMS).</span></span> <span data-ttu-id="b1ec1-176">在將要求傳送至註冊伺服器之前，Microsoft 會包裝 [*PKCS \# 7*](p-gly.md) (CMS) 要求物件中的 CMC 憑證要求。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-176">Microsoft wraps CMC certificate requests in a [*PKCS \#7*](p-gly.md) (CMS) request object before sending the request to an enrollment server.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**憑證名稱 BLOB**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**certificate name BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-178">憑證中包含的名稱資訊編碼標記法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-178">An encoded representation of the name information that is included in certificates.</span></span> <span data-ttu-id="b1ec1-179">每個名稱 BLOB 都會對應到 **憑證 \_ 名稱 \_ blob** 結構。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-179">Each name BLOB is mapped to a **CERT\_NAME\_BLOB** structure.</span></span>

<span data-ttu-id="b1ec1-180">例如， **cert \_ 資訊** 結構所參考的簽發者和主體資訊會儲存在兩個 **憑證 \_ 名稱 \_ BLOB** 結構中。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-180">For example, the issuer and subject information referenced by a **CERT\_INFO** structure is stored in two **CERT\_NAME\_BLOB** structures.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**憑證原則**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**certificate policy**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-182">一組命名規則，指出具有一般安全性需求之特定應用程式類別的憑證適用性。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-182">A named set of rules that indicate the applicability of certificates for a specific class of applications with common security requirements.</span></span> <span data-ttu-id="b1ec1-183">例如，這類原則可能會將特定憑證限制在指定價格限制內的電子資料交換交易。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-183">Such a policy might, for example, limit certain certificates to electronic data interchange transactions within given price limits.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**憑證要求**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**certificate request**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-185">特殊格式的電子郵件 (傳送給 CA) 用來要求憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-185">A specially formatted electronic message (sent to a CA) used to request a certificate.</span></span> <span data-ttu-id="b1ec1-186">要求必須包含 CA 驗證要求所需的資訊，以及要求憑證之實體的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-186">The request must contain the information required by the CA to authenticate the request, plus the public key of the entity requesting the certificate.</span></span>

<span data-ttu-id="b1ec1-187">建立要求所需的所有資訊都會對應到 **CERT \_ 要求 \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-187">All the information necessary to create the request is mapped to a **CERT\_REQUEST\_INFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**憑證撤銷清單**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**certificate revocation list**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-189"> (CRL) 由憑證授權單位單位維護及發佈的檔 (CA) ，其中列出不再有效的 CA 所發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-189">(CRL) A document maintained and published by a certification authority (CA) that lists certificates issued by the CA that are no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**憑證伺服器**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**certificate server**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-191">針對特定 CA 發行憑證的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-191">A server that issues certificates for a particular CA.</span></span> <span data-ttu-id="b1ec1-192">憑證伺服器軟體提供可自訂的服務，可用來發行和管理在採用公開金鑰加密的安全性系統中所使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-192">The certificate server software provides customizable services for issuing and managing certificates used in security systems that employ public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**憑證服務**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Certificate Services**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-194">針對特定 *憑證授權單位* 單位發行憑證 (CA) 的軟體服務。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-194">A software service that issues certificates for a particular *certification authority* (CA).</span></span> <span data-ttu-id="b1ec1-195">它提供可自訂的服務來發行和管理企業的憑證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-195">It provides customizable services for issuing and managing certificates for the enterprise.</span></span> <span data-ttu-id="b1ec1-196">憑證可以用來提供驗證支援，包括安全電子郵件、web 驗證，以及智慧卡驗證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-196">Certificates can be used to provide authentication support, including secure email, web-based authentication, and smart card authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**憑證存放區**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-198">一般來說，指的是用來存放憑證、憑證撤銷清單 (CRL)，以及憑證信任清單 (CTL) 的永久存放區。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-198">Typically, a permanent storage where certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs) are stored.</span></span> <span data-ttu-id="b1ec1-199">然而，當您使用不需要存放在永久存放區的憑證時，可以單純在記憶體中建立並開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-199">It is possible, however, to create and open a certificate store solely in memory when working with certificates that do not need to be put in permanent storage.</span></span>

<span data-ttu-id="b1ec1-200">憑證存放區是 CryptoAPI 中許多憑證功能的核心。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-200">The certificate store is central to much of the certificate functionality in CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**憑證存放區功能**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**certificate store functions**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-202">管理儲存體和抓取資料的函式，例如憑證、憑證撤銷清單 (Crl) ，以及 (Ctl) 的憑證信任清單。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-202">Functions that manage the storage and retrieval data such as certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs).</span></span> <span data-ttu-id="b1ec1-203">這些函式可分成一般憑證函式、憑證撤銷清單函式，以及憑證信任清單功能。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-203">These functions can be separated into common certificate functions, certificate revocation list functions, and certificate trust list functions.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**憑證範本**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**certificate template**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-205">分析憑證 (的 Windows 結構，也就是根據其預期的使用方式，來 prespecifies 格式和內容) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-205">A Windows construct that profiles certificates (that is, it prespecifies the format and content) based on their intended usage.</span></span> <span data-ttu-id="b1ec1-206">從 Windows 企業 *憑證授權單位* 單位要求 [*憑證*](/windows) (CA) 時，憑證要求者會根據其存取權限，從以憑證範本為基礎的各種憑證類型（例如使用者和程式碼簽署）進行選取。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-206">When requesting a [*certificate*](/windows) from a Windows enterprise *certification authority* (CA), certificate requesters are, depending on their access rights, able to select from a variety of certificate types that are based on certificate templates, such as User and Code Signing.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**憑證信任清單**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**certificate trust list**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-208"> (CTL) 由受信任實體簽署的預先定義專案清單。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-208">(CTL) A predefined list of items that have been signed by a trusted entity.</span></span> <span data-ttu-id="b1ec1-209">CTL 可以任何形式出現，例如憑證的雜湊清單，或是檔案名稱清單。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-209">A CTL can be anything, such as a list of hashes of certificates, or a list of file names.</span></span> <span data-ttu-id="b1ec1-210">清單裡的所有項目都會經由簽署實體加以驗證 (核准)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-210">All the items in the list are authenticated (approved) by the signing entity.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-212"> (CA) 信賴于發出憑證的實體，其會判斷提示要求憑證的收件者個人、電腦或組織是否滿足已建立原則的條件。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-212">(CA) An entity entrusted to issue certificates that assert that the recipient individual, computer, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**Cfb**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-214">請參閱 *加密意見* 反應。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-214">See *Cipher Feedback*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**連結模式**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**chaining mode**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-216">一種區塊加密模式，藉由結合加密文字和純文字來引入意見反應。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-216">A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="b1ec1-217">另請參閱 *加密區塊鏈*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-217">See also *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**密碼**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**cipher**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-219">用來加密資料的密碼編譯演算法;亦即，使用預先定義的金鑰將純文字轉換成加密文字。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-219">A cryptographic algorithm used to encrypt data; that is, to transform plaintext into ciphertext using a predefined key.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**加密區塊鏈**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Cipher Block Chaining**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-221"> (CBC) 運作對稱式區塊加密的方法，此加密方法會使用意見將先前產生的加密文字與新的純文字結合在一起。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-221">(CBC) A method of operating a symmetric block cipher that uses feedback to combine previously generated ciphertext with new plaintext.</span></span>

<span data-ttu-id="b1ec1-222">在加密之前，每個純文字區塊都會與前一個區塊的加密文字合併，再加上位 **XOR** 運算。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-222">Each plaintext block is combined with the ciphertext of the previous block by a bitwise-**XOR** operation before it is encrypted.</span></span> <span data-ttu-id="b1ec1-223">結合加密文字和純文字可確保即使純文字包含許多相同的區塊，它們都會加密為不同的加密文字區塊。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-223">Combining ciphertext and plaintext ensures that even if the plaintext contains many identical blocks, they will each encrypt to a different ciphertext block.</span></span>

<span data-ttu-id="b1ec1-224">使用 Microsoft 基底密碼編譯提供者時，CBC 是預設的加密模式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-224">When the Microsoft Base Cryptographic Provider is used, CBC is the default cipher mode.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**加密區塊連結 MAC**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cipher Block Chaining MAC**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-226">區塊加密方法，它會使用區塊密碼將基底資料加密，然後使用最後一個加密區塊做為雜湊值。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-226">A block cipher method that encrypts the base data with a block cipher and then uses the last encrypted block as the hash value.</span></span> <span data-ttu-id="b1ec1-227">用來建立 [*訊息驗證碼*](m-gly.md) (MAC) 的加密演算法是建立工作階段金鑰時所指定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-227">The encryption algorithm used to build the [*Message Authentication Code*](m-gly.md) (MAC) is the one that was specified when the session key was created.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**加密意見反應**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Cipher Feedback**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-229"> (CFB) 一個區塊加密模式，它會以純文字格式處理少量的純文字，而不是一次處理整個區塊。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-229">(CFB) A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="b1ec1-230">這個模式會使用一個區塊大小的 shift 暫存器，並將其分成數個區段。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-230">This mode uses a shift register that is one block size in length and divided into sections.</span></span> <span data-ttu-id="b1ec1-231">例如，如果區塊大小是每次處理八個位的64位，則移位暫存器會分成八個區段。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-231">For example, if the block size is 64 bits with eight bits processed at a time, then the shift register would be divided into eight sections.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**密碼模式**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**cipher mode**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-233">區塊加密模式 (每個區塊都會個別加密，) 可使用 **CryptSetKeyParam** 函式來指定。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-233">A block cipher mode (each block is encrypted individually) that can be specified by using the **CryptSetKeyParam** function.</span></span> <span data-ttu-id="b1ec1-234">如果應用程式未明確指定其中一種模式，則會使用 (CBC) cipher 模式的加密區塊鏈。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-234">If the application does not explicitly specify one of these modes, then the cipher block chaining (CBC) cipher mode is used.</span></span>

<span data-ttu-id="b1ec1-235">ECB：不使用任何意見反應的區塊加密模式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-235">ECB: A block cipher mode that uses no feedback.</span></span>

<span data-ttu-id="b1ec1-236">CBC：藉由結合加密文字和純文字來引進意見反應的區塊加密模式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-236">CBC: A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="b1ec1-237">CFB：一種區塊加密模式，可將純文字的小型遞增處理為加密文字，而不是一次處理整個區塊。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-237">CFB: A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="b1ec1-238">OFB：使用類似于 CFB 之意見反應的區塊加密模式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-238">OFB: A block cipher mode that uses feedback similar to CFB.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**密文**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-240">已加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-240">A message that has been encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**明文**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**cleartext**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-242">請參閱 [*純文字*](p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-242">See [*plaintext*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**客戶**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-244">起始與伺服器之連接的應用程式，而不是伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-244">The application, rather than the server application, that initiates a connection to a server.</span></span>

<span data-ttu-id="b1ec1-245">與 [*伺服器*](s-gly.md)比較。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-245">Compare with [*server*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**用戶端憑證**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**client certificate**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-247">是指用於用戶端驗證的憑證，例如在 web 伺服器上驗證網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-247">Refers to a certificate used for client authentication, such as authenticating a web browser on a web server.</span></span> <span data-ttu-id="b1ec1-248">當網頁瀏覽器用戶端嘗試存取安全的 web 伺服器時，用戶端會將其憑證傳送至伺服器，以允許它驗證用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-248">When a web browser client attempts to access a secured web server, the client sends its certificate to the server to allow it to verify the client's identity.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**Cmc**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-250">請參閱透過 *CMS 的憑證管理*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-250">See *Certificate Management over CMS*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**天然氣**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-252">請參閱 *密碼編譯 API：新一代*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-252">See *Cryptography API: Next Generation*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**communication protocol**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-254">序列化資料的方法 (轉換成字串，) 和還原序列化。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-254">The method in which data is serialized (converted to a string of ones and zeros) and deserialized.</span></span> <span data-ttu-id="b1ec1-255">此通訊協定是由軟體和資料傳輸硬體所控制。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-255">The protocol is controlled by both software and data-transmission hardware.</span></span>

<span data-ttu-id="b1ec1-256">一般來說，以圖層為根據，簡化通訊協定可能包含應用層、編碼/解碼層和硬體層。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-256">Typically discussed in terms of layers, a simplified communication protocol might consist of an application layer, encode/decode layer, and hardware layer.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**限制委派**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**constrained delegation**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-258">允許伺服器將要求僅代表用戶端轉寄給指定服務清單的行為。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-258">Behavior that allows the server to forward requests on behalf of the client only to a specified list of services.</span></span>

<span data-ttu-id="b1ec1-259">**WINDOWS XP：** 不支援限制委派。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-259">**Windows XP:** Constrained delegation is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**上下文**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-261">與連接相關的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-261">The security data relevant to a connection.</span></span> <span data-ttu-id="b1ec1-262">內容包含工作階段金鑰和會話持續時間等資訊。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-262">A context contains information such as a session key and duration of the session.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**coNtext 函數**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**context function**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-264">用來連線至密碼編譯服務提供者 (CSP) 的函式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-264">Functions used to connect to a cryptographic service provider (CSP).</span></span> <span data-ttu-id="b1ec1-265">這些函式可讓應用程式依名稱選擇特定的 CSP，或使用所需的功能類別取得一個。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-265">These functions enable applications to choose a specific CSP by name or get one with a needed class of functionality.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**副署**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**countersignature**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-267">現有簽章和訊息的簽章，或現有簽章的簽章。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-267">A signature of an existing signature and message or a signature of an existing signature.</span></span> <span data-ttu-id="b1ec1-268">副署可用來簽署現有簽章的加密雜湊，或用來為訊息建立時間戳記。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-268">A countersignature is used to sign the encrypted hash of an existing signature or to time stamp a message.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**憑據**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credentials**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-270">[*安全性主體*](s-gly.md)先前經過驗證的登入資料，可用來建立自己的身分識別，例如密碼或 Kerberos 通訊協定票證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-270">Previously authenticated logon data used by a [*security principal*](s-gly.md) to establish its own identity, such as a password, or a Kerberos protocol ticket.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**Crl**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-272">請參閱 *憑證撤銷清單*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-272">See *certificate revocation list*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT \_ ASN \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-274">指定憑證編碼方式的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-274">Encoding type that specifies certificate encoding.</span></span> <span data-ttu-id="b1ec1-275">憑證編碼類型會以 **DWORD** 的低序位字組儲存 (值為： 0x00000001) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-275">Certificate encoding types are stored in the low-order word of a **DWORD** (value is: 0x00000001).</span></span> <span data-ttu-id="b1ec1-276">此編碼類型的功能與 X509 \_ ASN \_ 編碼編碼類型相同。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-276">This encoding type is functionally the same as the X509\_ASN\_ENCODING encoding type.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**加密分析**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-278">加密分析是中斷加密文字的藝術與科學。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-278">Cryptanalysis is the art and science of breaking ciphertext.</span></span> <span data-ttu-id="b1ec1-279">相反地，保護訊息安全的藝術與科學是密碼編譯。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-279">In contrast, the art and science of keeping messages secure is cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-281">應用程式開發介面，可讓應用程式開發人員將驗證、編碼和加密新增至以 Windows 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-281">Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**密碼編譯演算法**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**cryptographic algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-283">用於加密和解密的數學函數。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-283">A mathematical function used for encryption and decryption.</span></span> <span data-ttu-id="b1ec1-284">大部分的密碼編譯演算法是以替代密碼、調換密碼或兩者的組合為基礎。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-284">Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**密碼編譯摘要**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Cryptographic Digest**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-286">單向雜湊函式，採用可變長度的輸入字串，並將它轉換成固定長度的輸出字串， (稱為密碼編譯摘要。 ) 此固定長度的輸出字串對於每個不同的輸入字串是機率唯一的，因此可作為檔案的指紋。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-286">A one-way hash function that takes a variable-length input string and converts it to a fixed-length output string (called a cryptographic digest.) This fixed-length output string is probabilistically unique for every different input string and thus can act as a fingerprint of a file.</span></span> <span data-ttu-id="b1ec1-287">下載具有密碼編譯摘要的檔案時，接收者會旁邊摘要。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-287">When a file with a cryptographic digest is downloaded, the receiver recomputes the digest.</span></span> <span data-ttu-id="b1ec1-288">如果輸出字串符合檔案中包含的摘要，則接收者會證明接收的檔案未遭篡改，而且與原先傳送的檔案相同。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-288">If the output string matches the digest contained in the file, the receiver has proof that the received file was not tampered with and is identical to the file originally sent.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**密碼編譯金鑰**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**cryptographic key**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-290">密碼編譯金鑰是初始化密碼編譯演算法所需的一段資料。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-290">A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm.</span></span> <span data-ttu-id="b1ec1-291">密碼編譯系統的設計通常是為了確保其安全性只取決於其密碼編譯金鑰的安全性，而不是在保持演算法秘密的情況下。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-291">Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.</span></span>

<span data-ttu-id="b1ec1-292">有許多不同類型的密碼編譯金鑰，對應至各種不同的密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-292">There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms.</span></span> <span data-ttu-id="b1ec1-293">您可以根據用於 (的演算法類型來分類金鑰，例如對稱或非對稱金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-293">Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys).</span></span> <span data-ttu-id="b1ec1-294">它們也可以根據系統內的存留期進行分類 (例如，長期或工作階段金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-294">They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**密碼編譯服務提供者**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**cryptographic service provider**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-296"> (CSP) 獨立的軟體模組，此模組實際上會執行驗證、編碼和加密的密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-296">(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**密碼**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-298">資訊安全的藝術與科學。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-298">The art and science of information security.</span></span> <span data-ttu-id="b1ec1-299">它包含資訊機密性、資料完整性、實體驗證及資料來源驗證。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-299">It includes information confidentiality, data integrity, entity authentication, and data origin authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**密碼編譯 API**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Cryptography API**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-301">請參閱 *CryptoAPI*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-301">See *CryptoAPI*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**密碼編譯 API：新一代**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Cryptography API: Next Generation**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-303"> (CNG) 第二次產生 *CryptoAPI*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-303">(CNG) The second generation of the *CryptoAPI*.</span></span> <span data-ttu-id="b1ec1-304">CNG 可讓您將現有的演算法提供者取代為您自己的提供者，並在可用時加入新的演算法。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-304">CNG allows you to replace existing algorithm providers with your own providers and add new algorithms as they become available.</span></span> <span data-ttu-id="b1ec1-305">CNG 也允許從使用者和核心模式應用程式使用相同的 Api。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-305">CNG also allows the same APIs to be used from user and kernel mode applications.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**密碼**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-307">包含密碼編譯和加密分析的數學分支。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-307">The branch of mathematics that encompasses both cryptography and cryptanalysis.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-309">搭配 *密碼編譯服務提供者* 使用的系統程式介面 (CSP) 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-309">The system program interface used with a *cryptographic service provider* (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**Csp**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-311">請參閱 *密碼編譯服務提供者*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-311">See *cryptographic service provider*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP 系列**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP family**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-313">唯一的 Csp 群組，使用相同的一組資料格式並以相同的方式執行其功能。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-313">A unique group of CSPs that use the same set of data formats and perform their function in the same way.</span></span> <span data-ttu-id="b1ec1-314">即使兩個 CSP 系列使用相同的演算法 (例如，RC2 區塊加密) 、其不同的填補配置、金鑰長度或預設模式都會使每個群組相異。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-314">Even when two CSP families use the same algorithm (for example, the RC2 block cipher), their different padding schemes, keys lengths, or default modes make each group distinct.</span></span> <span data-ttu-id="b1ec1-315">CryptoAPI 的設計目的是讓每個 CSP 類型都代表一個特定的系列。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-315">CryptoAPI has been designed so that each CSP type represents a particular family.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP 名稱**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP name**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-317">CSP 的文字名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-317">The textual name of the CSP.</span></span> <span data-ttu-id="b1ec1-318">如果 CSP 已經由 Microsoft 簽署，此名稱必須完全符合匯出合規性憑證 (ECC) 中所指定的 CSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-318">If the CSP has been signed by Microsoft, this name must exactly match the CSP name that was specified in the Export Compliance Certificate (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP 類型**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP type**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-320">指出與提供者相關聯的 CSP 系列。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-320">Indicates the CSP family associated with a provider.</span></span> <span data-ttu-id="b1ec1-321">當應用程式連接到特定類型的 CSP 時，每個 CryptoAPI 函式預設會以對應至該 CSP 類型的系列所規定的方式運作。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-321">When an application connects to a CSP of a particular type, each of the CryptoAPI functions will, by default, operate in a way prescribed by the family that corresponds to that CSP type.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**Ctl**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-323">請參閱 *憑證信任清單*。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-323">See *certificate trust list*.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec1-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK \_ MEK**</span><span class="sxs-lookup"><span data-stu-id="b1ec1-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK\_MEK**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec1-325">一種加密演算法，使用40位的 DES 金鑰變異，其中16位的56位 DES 金鑰會設定為零。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-325">An encryption algorithm that uses a 40-bit variant of a DES key where 16 bits of the 56-bit DES key are set to zero.</span></span> <span data-ttu-id="b1ec1-326">此演算法會依照40位 DES 的 IETF 草稿規格中的指定來執行。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-326">This algorithm is implemented as specified in the IETF Draft specification for 40-bit DES.</span></span> <span data-ttu-id="b1ec1-327">在撰寫本文時，可以在 ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt 找到草稿規格。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-327">The draft specification, at the time of this writing can be found at ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span></span> <span data-ttu-id="b1ec1-328">此演算法與 **ALG \_ 識別碼** 值 CALG \_ CYLINK MEK 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b1ec1-328">This algorithm is used with the **ALG\_ID** value CALG\_CYLINK\_MEK.</span></span>

</dd> </dl>

 

 

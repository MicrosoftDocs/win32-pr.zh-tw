---
description: 包含以字母 B 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: 'B (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001739"
---
# <a name="b-security-glossary"></a><span data-ttu-id="a35ba-103">B (安全性詞彙) </span><span class="sxs-lookup"><span data-stu-id="a35ba-103">B (Security Glossary)</span></span>

<span data-ttu-id="a35ba-104">[B](a-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="a35ba-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a35ba-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**備份授權單位**</span><span class="sxs-lookup"><span data-stu-id="a35ba-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-106">在安全電腦上執行的受信任應用程式，可為其用戶端的工作階段金鑰提供次要儲存體。</span><span class="sxs-lookup"><span data-stu-id="a35ba-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="a35ba-107">備份授權單位會將工作階段金鑰儲存為金鑰 Blob，並以備份授權單位的公開金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="a35ba-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**基底內容類型**</span><span class="sxs-lookup"><span data-stu-id="a35ba-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-109">PKCS 7 訊息中包含的資料類型 \# 。</span><span class="sxs-lookup"><span data-stu-id="a35ba-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="a35ba-110">基底內容類型只包含資料，不包含任何密碼編譯增強功能，例如雜湊或簽章。</span><span class="sxs-lookup"><span data-stu-id="a35ba-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="a35ba-111">目前，唯一的基底內容類型是資料內容類型。</span><span class="sxs-lookup"><span data-stu-id="a35ba-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**基底加密函式**</span><span class="sxs-lookup"><span data-stu-id="a35ba-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-113">CryptoAPI 架構中最低層級的函數。</span><span class="sxs-lookup"><span data-stu-id="a35ba-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="a35ba-114">應用程式和其他高階 CryptoAPI 函式會使用這些功能來存取 CSP 提供的密碼編譯演算法、安全的金鑰產生，以及安全地儲存秘密。</span><span class="sxs-lookup"><span data-stu-id="a35ba-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="a35ba-115">另請參閱 [*加密服務提供者*](c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a35ba-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**基本編碼規則**</span><span class="sxs-lookup"><span data-stu-id="a35ba-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-117"> (BER) 用來將 ASN. 1 定義的資料編碼成位資料流程的規則集 (零或) 用於外部儲存體或傳輸。</span><span class="sxs-lookup"><span data-stu-id="a35ba-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="a35ba-118">單一 asn.1 物件可以有數個對等的 BER 編碼。</span><span class="sxs-lookup"><span data-stu-id="a35ba-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="a35ba-119">BER 定義于 CCITT 建議的209中。</span><span class="sxs-lookup"><span data-stu-id="a35ba-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="a35ba-120">這是 CryptoAPI 目前所使用的兩種編碼方法之一。</span><span class="sxs-lookup"><span data-stu-id="a35ba-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**誤碼率**</span><span class="sxs-lookup"><span data-stu-id="a35ba-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-122">請參閱 *基本編碼規則*。</span><span class="sxs-lookup"><span data-stu-id="a35ba-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**位元組由大到小**</span><span class="sxs-lookup"><span data-stu-id="a35ba-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-124">記憶體或資料格式，其中最重要的位元組會儲存在較低的位址，或先到達。</span><span class="sxs-lookup"><span data-stu-id="a35ba-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="a35ba-125">另請參閱 [*位元組由小到小*](l-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a35ba-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**Blob**</span><span class="sxs-lookup"><span data-stu-id="a35ba-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-127">包含一或多個固定長度標頭結構和內容特定資料的一般位序列。</span><span class="sxs-lookup"><span data-stu-id="a35ba-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="a35ba-128">另請參閱 [*主要 blob*](k-gly.md)、 [*憑證 blob*](c-gly.md)、 [*憑證名稱 blob*](c-gly.md)和 [*屬性 blob*](a-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a35ba-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**區塊加密**</span><span class="sxs-lookup"><span data-stu-id="a35ba-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-130">一種加密演算法，可將離散單位中的資料加密 (稱為區塊) ，而不是連續的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="a35ba-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="a35ba-131">最常見的區塊大小為64位。</span><span class="sxs-lookup"><span data-stu-id="a35ba-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="a35ba-132">例如，DES 是封鎖密碼。</span><span class="sxs-lookup"><span data-stu-id="a35ba-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="a35ba-133">另請參閱 [*資料流程加密*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a35ba-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ba-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**大量加密金鑰**</span><span class="sxs-lookup"><span data-stu-id="a35ba-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="a35ba-135">從主要金鑰衍生的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="a35ba-135">A session key derived from a master key.</span></span> <span data-ttu-id="a35ba-136">大量加密金鑰用於 [*Schannel*](s-gly.md) 加密中。</span><span class="sxs-lookup"><span data-stu-id="a35ba-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 




---
description: 包含以字母 H 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: 'H (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987242"
---
# <a name="h-security-glossary"></a><span data-ttu-id="5967c-103">H (安全性詞彙) </span><span class="sxs-lookup"><span data-stu-id="5967c-103">H (Security Glossary)</span></span>

<span data-ttu-id="5967c-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](u-gly.md) [](v-gly.md) [G](g-gly.md) H [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="5967c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5967c-105"><span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**處理**</span><span class="sxs-lookup"><span data-stu-id="5967c-105"><span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**handle**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-106">用來識別或存取物件的 token，例如密碼編譯提供者的控制碼、憑證存放區、訊息或金鑰組。</span><span class="sxs-lookup"><span data-stu-id="5967c-106">A token used to identify or access an object, such as the handle to a cryptographic provider, certificate store, message, or key pair.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-107"><span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**散 列**</span><span class="sxs-lookup"><span data-stu-id="5967c-107"><span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**hash**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-108">藉由套用數學函式 (*雜湊演算法*) 至任意數量的資料，即可取得固定大小的結果。</span><span class="sxs-lookup"><span data-stu-id="5967c-108">A fixed-size result obtained by applying a mathematical function (the *hashing algorithm*) to an arbitrary amount of data.</span></span> <span data-ttu-id="5967c-109"> (也稱為「訊息摘要」。) </span><span class="sxs-lookup"><span data-stu-id="5967c-109">(Also known as "message digest.")</span></span>

<span data-ttu-id="5967c-110">另請參閱 *雜湊函數*。</span><span class="sxs-lookup"><span data-stu-id="5967c-110">See also *hashing functions*.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-111"><span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**hash 物件**</span><span class="sxs-lookup"><span data-stu-id="5967c-111"><span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**hash object**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-112">用來雜湊訊息或會話索引鍵的物件。</span><span class="sxs-lookup"><span data-stu-id="5967c-112">An object used to hash messages or session keys.</span></span> <span data-ttu-id="5967c-113">雜湊物件是由呼叫 **CryptCreateHash** 所建立。</span><span class="sxs-lookup"><span data-stu-id="5967c-113">The hash object is created by a call to **CryptCreateHash**.</span></span> <span data-ttu-id="5967c-114">物件的定義是由呼叫中指定的 CSP 所定義。</span><span class="sxs-lookup"><span data-stu-id="5967c-114">The definition of the object is defined by the CSP specified in the call.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-115"><span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**雜湊演算法**</span><span class="sxs-lookup"><span data-stu-id="5967c-115"><span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**hashing algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-116">演算法，用來產生某些資料片段 (例如訊息或工作階段金鑰) 的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="5967c-116">An algorithm used to produce a hash value of some piece of data, such as a message or session key.</span></span> <span data-ttu-id="5967c-117">傳統的雜湊演算法包含 MD2、MD4、MD5，與 SHA-1。</span><span class="sxs-lookup"><span data-stu-id="5967c-117">Typical hashing algorithms include MD2, MD4, MD5, and SHA-1.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-118"><span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**雜湊函數**</span><span class="sxs-lookup"><span data-stu-id="5967c-118"><span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**hashing functions**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-119">一組函數，用來建立和終結雜湊物件、取得或設定雜湊物件的參數，以及雜湊資料和工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="5967c-119">A set of functions used to create and destroy hash objects, get or set the parameters of a hash object, and hash data and session keys.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-120"><span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**以雜湊為基礎的訊息驗證碼**</span><span class="sxs-lookup"><span data-stu-id="5967c-120"><span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Hash-Based Message Authentication Code**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-121"> (HMAC) Microsoft 密碼編譯服務提供者所執行的對稱式金鑰雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="5967c-121">(HMAC) A symmetric keyed hashing algorithm implemented by Microsoft cryptographic service providers.</span></span> <span data-ttu-id="5967c-122">HMAC 可用來確認資料的完整性，以協助確保在儲存或傳輸時，不會修改資料。</span><span class="sxs-lookup"><span data-stu-id="5967c-122">An HMAC is used to verify the integrity of data to help ensure it has not been modified while in storage or transit.</span></span> <span data-ttu-id="5967c-123">它可以搭配任何反復的密碼編譯雜湊演算法（例如 MD5 或 SHA-1）使用。</span><span class="sxs-lookup"><span data-stu-id="5967c-123">It can be used with any iterated cryptographic hash algorithm, such as MD5 or SHA-1.</span></span> <span data-ttu-id="5967c-124">CryptoAPI 會依據演算法識別碼來參考此演算法 (CALG \_ HMAC) 和類別 (ALG \_ 類別 \_ 雜湊) 。</span><span class="sxs-lookup"><span data-stu-id="5967c-124">CryptoAPI references this algorithm by its algorithm identifier (CALG\_HMAC) and class (ALG\_CLASS\_HASH).</span></span>

<span data-ttu-id="5967c-125">另請參閱 [*訊息驗證碼*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="5967c-125">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5967c-126"><span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**</span><span class="sxs-lookup"><span data-stu-id="5967c-126"><span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-127">作為憑證服務備份內容之控制碼的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5967c-127">Data type which serves as a handle to a Certificate Services backup context.</span></span> <span data-ttu-id="5967c-128">其角色是在執行備份時，維護伺服器與備份 Api 之間的內容狀態。</span><span class="sxs-lookup"><span data-stu-id="5967c-128">Its role is to maintain context state between the server and the backup APIs when a backup is being performed.</span></span>

</dd> <dt>

<span data-ttu-id="5967c-129"><span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**Hmac**</span><span class="sxs-lookup"><span data-stu-id="5967c-129"><span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="5967c-130">請參閱以 *雜湊為基礎的訊息驗證碼*。</span><span class="sxs-lookup"><span data-stu-id="5967c-130">See *Hash-Based Message Authentication Code*.</span></span>

</dd> </dl>

 

 




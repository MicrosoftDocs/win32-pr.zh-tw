---
description: 搭配 BCryptGetProperty 和 BCryptSetProperty 函數使用，以識別屬性。
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: '加密基本屬性識別碼 (Bcrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847717"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="102df-103">加密基本屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="102df-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="102df-104">下列值會搭配 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 和 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 函數使用，以識別屬性。</span><span class="sxs-lookup"><span data-stu-id="102df-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="102df-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT \_ 演算法 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="102df-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-106">L "AlgorithmName"</span><span class="sxs-lookup"><span data-stu-id="102df-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="102df-107">以 null 終止的 Unicode 字串，其中包含演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="102df-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT \_ AUTH \_ TAG \_ LENGTH**</span><span class="sxs-lookup"><span data-stu-id="102df-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-109">L "AuthTagLength"</span><span class="sxs-lookup"><span data-stu-id="102df-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-110">演算法所支援的驗證標記長度。</span><span class="sxs-lookup"><span data-stu-id="102df-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="102df-111">這個屬性是 [**BCRYPT \_ AUTH \_ TAG \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="102df-112">這個屬性只適用于演算法。</span><span class="sxs-lookup"><span data-stu-id="102df-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT \_ 區塊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-114">L "BlockLength"</span><span class="sxs-lookup"><span data-stu-id="102df-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-115">演算法之加密區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="102df-116">這個屬性只適用于區塊加密演算法。</span><span class="sxs-lookup"><span data-stu-id="102df-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="102df-117">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT \_ 區塊 \_ 大小 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="102df-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-119">L "BlockSizeList"</span><span class="sxs-lookup"><span data-stu-id="102df-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="102df-120">加密演算法所支援的區塊長度清單。</span><span class="sxs-lookup"><span data-stu-id="102df-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="102df-121">此資料類型是 **dword** 的陣列。</span><span class="sxs-lookup"><span data-stu-id="102df-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="102df-122">陣列中的元素數目可以藉由將單一 **DWORD** 的大小所抓取的位元組數目進行分割來決定。</span><span class="sxs-lookup"><span data-stu-id="102df-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT \_ 連結 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="102df-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-124">L "ChainingMode"</span><span class="sxs-lookup"><span data-stu-id="102df-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="102df-125">以 null 結束的 Unicode 字串指標，表示加密演算法的連結模式。</span><span class="sxs-lookup"><span data-stu-id="102df-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="102df-126">這個屬性可以在演算法控制碼或索引鍵控制碼上設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="102df-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="102df-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="102df-127">Identifier</span></span>                   | <span data-ttu-id="102df-128">值</span><span class="sxs-lookup"><span data-stu-id="102df-128">Value</span></span>                         | <span data-ttu-id="102df-129">描述</span><span class="sxs-lookup"><span data-stu-id="102df-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102df-130">**BCRYPT \_ 鏈 \_ 模式 \_ CBC**</span><span class="sxs-lookup"><span data-stu-id="102df-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="102df-131">L "ChainingModeCBC"</span><span class="sxs-lookup"><span data-stu-id="102df-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="102df-132">將演算法的連結模式設定為 [*加密區塊鏈*](/windows/desktop/SecGloss/c-gly)。</span><span class="sxs-lookup"><span data-stu-id="102df-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="102df-133">**BCRYPT \_ 鏈 \_ 模式 \_ CCM**</span><span class="sxs-lookup"><span data-stu-id="102df-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="102df-134">L "ChainingModeCCM"</span><span class="sxs-lookup"><span data-stu-id="102df-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="102df-135">將演算法的連結模式設定為使用 CBC (CCM) 的 MAC 模式來進行計數器。**Windows Vista：** 從 Windows Vista SP1 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="102df-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="102df-136">**BCRYPT \_ 鏈 \_ 模式 \_ CFB**</span><span class="sxs-lookup"><span data-stu-id="102df-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="102df-137">L "ChainingModeCFB"</span><span class="sxs-lookup"><span data-stu-id="102df-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="102df-138">將演算法的連結模式設定為 [*加密意見*](/windows/desktop/SecGloss/c-gly)反應。</span><span class="sxs-lookup"><span data-stu-id="102df-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="102df-139">**BCRYPT \_ 鏈 \_ 模式 \_ ECB**</span><span class="sxs-lookup"><span data-stu-id="102df-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="102df-140">L "ChainingModeECB"</span><span class="sxs-lookup"><span data-stu-id="102df-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="102df-141">將演算法的連結模式設定為 [*電子 codebook*](/windows/desktop/SecGloss/e-gly)。</span><span class="sxs-lookup"><span data-stu-id="102df-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="102df-142">**BCRYPT \_ 鏈 \_ 模式 \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="102df-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="102df-143">L "ChainingModeGCM"</span><span class="sxs-lookup"><span data-stu-id="102df-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="102df-144">將演算法的連結模式設定為 Galois/counter 模式 (GCM) 。**Windows Vista：** 從 Windows Vista SP1 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="102df-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="102df-145">**BCRYPT \_ 鏈 \_ 模式 \_ NA**</span><span class="sxs-lookup"><span data-stu-id="102df-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="102df-146">L "ChainingModeN/A"</span><span class="sxs-lookup"><span data-stu-id="102df-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="102df-147">演算法不支援連結。</span><span class="sxs-lookup"><span data-stu-id="102df-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT \_ DH \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="102df-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-149">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="102df-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="102df-150">指定要搭配 Diffie-Hellman 索引鍵使用的參數。</span><span class="sxs-lookup"><span data-stu-id="102df-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="102df-151">此資料類型是 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="102df-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="102df-152">這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。</span><span class="sxs-lookup"><span data-stu-id="102df-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT \_ DSA \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="102df-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-154">L "DSAParameters"</span><span class="sxs-lookup"><span data-stu-id="102df-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="102df-155">指定要與 DSA 金鑰搭配使用的參數。</span><span class="sxs-lookup"><span data-stu-id="102df-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="102df-156">這個屬性是 [**BCRYPT \_ dsa \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) 或 [**BCRYPT \_ dsa \_ 參數 \_ 標頭 \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="102df-157">這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。</span><span class="sxs-lookup"><span data-stu-id="102df-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="102df-158">**Windows 8：** 從 Windows 8 開始，此屬性可以是 [**BCRYPT \_ DSA \_ 參數 \_ 標頭 \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="102df-159">如果金鑰大小超過1024個位且小於或等於3072位，請使用此結構。</span><span class="sxs-lookup"><span data-stu-id="102df-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="102df-160">如果金鑰大小大於或等於512但小於或等於1024位，請使用 [**BCRYPT \_ DSA \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT \_ 有效 \_ 金鑰 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-162">L "EffectiveKeyLength"</span><span class="sxs-lookup"><span data-stu-id="102df-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-163">RC2 金鑰有效長度的大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="102df-164">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT \_ 雜湊 \_ 區塊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-166">L "HashBlockLength"</span><span class="sxs-lookup"><span data-stu-id="102df-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-167">雜湊區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="102df-168">這個屬性只適用于雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="102df-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="102df-169">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT \_ 雜湊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-171">L "HashDigestLength"</span><span class="sxs-lookup"><span data-stu-id="102df-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-172">雜湊提供者雜湊值的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="102df-173">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT \_ 雜湊 \_ OID \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="102df-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-175">L "HashOIDList"</span><span class="sxs-lookup"><span data-stu-id="102df-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="102df-176">以 [*DER*](/windows/desktop/SecGloss/d-gly)編碼的雜湊 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) 清單 (oid) 。</span><span class="sxs-lookup"><span data-stu-id="102df-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="102df-177">這個屬性是 [**BCRYPT 的 \_ OID \_ 清單**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="102df-178">只能讀取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="102df-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT \_ 初始化 \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="102df-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="102df-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="102df-181">包含金鑰的 [*初始化向量*](/windows/desktop/SecGloss/i-gly) (IV) 。</span><span class="sxs-lookup"><span data-stu-id="102df-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="102df-182">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="102df-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT \_ 金鑰 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-184">L "KeyLength"</span><span class="sxs-lookup"><span data-stu-id="102df-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-185">對稱金鑰提供者之金鑰值的大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="102df-186">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT \_ 金鑰 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-188">L "KeyLengths"</span><span class="sxs-lookup"><span data-stu-id="102df-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="102df-189">演算法所支援的金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="102df-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="102df-190">這個屬性是 BCRYPT 的索引 [**\_ 鍵 \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) 結構。</span><span class="sxs-lookup"><span data-stu-id="102df-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="102df-191">這個屬性只適用于演算法。</span><span class="sxs-lookup"><span data-stu-id="102df-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT 索引 \_ 鍵 \_ 物件 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-193">L "KeyObjectLength"</span><span class="sxs-lookup"><span data-stu-id="102df-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-194">不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="102df-194">This property is not used.</span></span> <span data-ttu-id="102df-195">**BCRYPT \_ 物件 \_ 長度** 屬性是用來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="102df-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT \_ 金鑰 \_ 強度**</span><span class="sxs-lookup"><span data-stu-id="102df-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-197">L "KeyStrength"</span><span class="sxs-lookup"><span data-stu-id="102df-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-198">機碼中的位數。</span><span class="sxs-lookup"><span data-stu-id="102df-198">The number of bits in the key.</span></span> <span data-ttu-id="102df-199">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="102df-200">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="102df-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT \_ 訊息 \_ 區塊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-202">L "MessageBlockLength"</span><span class="sxs-lookup"><span data-stu-id="102df-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-203">這可以在已設定 CFB 連結模式的任何索引鍵控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="102df-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="102df-204">根據預設，這個屬性會設定為1，以進行8位 CFB。</span><span class="sxs-lookup"><span data-stu-id="102df-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="102df-205">將它設定為區塊大小（以位元組為單位）會導致使用完整區塊 CFB。</span><span class="sxs-lookup"><span data-stu-id="102df-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="102df-206">針對 XTS 索引鍵，它是用來設定 XTS 資料單位的大小（以位元組為單位）， (通常是512或 4096) 。</span><span class="sxs-lookup"><span data-stu-id="102df-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ 多 \_ 物件 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-208">L "MultiObjectLength"</span><span class="sxs-lookup"><span data-stu-id="102df-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-209">這個屬性會傳回 [**BCRYPT \_ 多 \_ 物件 \_ 長度 \_ 結構**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)，其中包含計算物件緩衝區大小所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="102df-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="102df-210">只有支援 [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) 函式的作業系統版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="102df-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT \_ 物件 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-212">L "ObjectLength"</span><span class="sxs-lookup"><span data-stu-id="102df-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-213">提供者之子物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="102df-214">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="102df-215">目前，雜湊和對稱式加密演算法提供者會使用呼叫端配置的緩衝區來儲存其子服務。</span><span class="sxs-lookup"><span data-stu-id="102df-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="102df-216">例如，雜湊提供者要求您針對以 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數取得的雜湊物件配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="102df-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="102df-217">這個屬性會提供提供者物件的緩衝區大小，讓您可以為提供者所建立的物件配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="102df-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT \_ 填補 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="102df-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-219">L "PaddingSchemes"</span><span class="sxs-lookup"><span data-stu-id="102df-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="102df-220">代表 RSA 演算法提供者的填補配置。</span><span class="sxs-lookup"><span data-stu-id="102df-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="102df-221">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="102df-222">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="102df-222">This can be one of the following values.</span></span>



| <span data-ttu-id="102df-223">識別碼</span><span class="sxs-lookup"><span data-stu-id="102df-223">Identifier</span></span>                             | <span data-ttu-id="102df-224">值</span><span class="sxs-lookup"><span data-stu-id="102df-224">Value</span></span>      | <span data-ttu-id="102df-225">描述</span><span class="sxs-lookup"><span data-stu-id="102df-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="102df-226">**BCRYPT \_ 支援的 \_ PAD \_ 路由器**</span><span class="sxs-lookup"><span data-stu-id="102df-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="102df-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="102df-227">0x00000001</span></span> | <span data-ttu-id="102df-228">提供者支援由路由器新增的填補。</span><span class="sxs-lookup"><span data-stu-id="102df-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="102df-229">**BCRYPT \_ 支援的 \_ PAD \_ PKCS1 \_ ENC**</span><span class="sxs-lookup"><span data-stu-id="102df-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="102df-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="102df-230">0x00000002</span></span> | <span data-ttu-id="102df-231">提供者支援 PKCS1 加密填補配置。</span><span class="sxs-lookup"><span data-stu-id="102df-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="102df-232">**BCRYPT \_ 支援的 \_ PAD \_ PKCS1 \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="102df-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="102df-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="102df-233">0x00000004</span></span> | <span data-ttu-id="102df-234">提供者支援 PKCS1 簽章填補配置。</span><span class="sxs-lookup"><span data-stu-id="102df-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="102df-235">**BCRYPT \_ 支援的 \_ PAD \_ OAEP**</span><span class="sxs-lookup"><span data-stu-id="102df-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="102df-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="102df-236">0x00000008</span></span> | <span data-ttu-id="102df-237">提供者支援 OAEP 填補配置。</span><span class="sxs-lookup"><span data-stu-id="102df-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="102df-238">**BCRYPT \_ 支援的 \_ PAD \_ PSS**</span><span class="sxs-lookup"><span data-stu-id="102df-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="102df-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="102df-239">0x00000010</span></span> | <span data-ttu-id="102df-240">提供者支援 PSS 填補配置。</span><span class="sxs-lookup"><span data-stu-id="102df-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT \_ 提供者 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="102df-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-242">L "ProviderHandle"</span><span class="sxs-lookup"><span data-stu-id="102df-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="102df-243">CNG 提供者的控制碼，它會建立在 *hObject* 參數中傳遞的物件。</span><span class="sxs-lookup"><span data-stu-id="102df-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="102df-244">此資料類型是 **BCRYPT \_ ALG \_ 控制碼**。</span><span class="sxs-lookup"><span data-stu-id="102df-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="102df-245">只能抓取此屬性;無法設定。</span><span class="sxs-lookup"><span data-stu-id="102df-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102df-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT \_ 簽名 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="102df-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102df-247">L "SignatureLength"</span><span class="sxs-lookup"><span data-stu-id="102df-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="102df-248">金鑰簽章長度的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="102df-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="102df-249">此資料類型為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="102df-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="102df-250">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="102df-250">This property only applies to keys.</span></span> <span data-ttu-id="102df-251">只能抓取此屬性;無法設定。</span><span class="sxs-lookup"><span data-stu-id="102df-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="102df-252">規格需求</span><span class="sxs-lookup"><span data-stu-id="102df-252">Requirements</span></span>



| <span data-ttu-id="102df-253">需求</span><span class="sxs-lookup"><span data-stu-id="102df-253">Requirement</span></span> | <span data-ttu-id="102df-254">值</span><span class="sxs-lookup"><span data-stu-id="102df-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="102df-255">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="102df-255">Minimum supported client</span></span><br/> | <span data-ttu-id="102df-256">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102df-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="102df-257">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="102df-257">Minimum supported server</span></span><br/> | <span data-ttu-id="102df-258">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102df-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="102df-259">標頭</span><span class="sxs-lookup"><span data-stu-id="102df-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="102df-260"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="102df-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 


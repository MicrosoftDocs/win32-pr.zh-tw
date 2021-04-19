---
description: 用來識別索引鍵存放區屬性。
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: '金鑰儲存區屬性識別碼 (Ncrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971648"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="2d617-103">金鑰儲存區屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="2d617-104">以下是用來識別索引鍵儲存屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2d617-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="2d617-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT \_ 演算法 \_ 群組 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-106">L "演算法群組"</span><span class="sxs-lookup"><span data-stu-id="2d617-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-107">以 null 終止的 Unicode 字串，其中包含物件之演算法群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="2d617-108">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-108">This property only applies to keys.</span></span> <span data-ttu-id="2d617-109">以下是 Microsoft 金鑰儲存提供者所傳回的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="2d617-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-110">Identifier</span></span>                                     | <span data-ttu-id="2d617-111">值</span><span class="sxs-lookup"><span data-stu-id="2d617-111">Value</span></span>              | <span data-ttu-id="2d617-112">描述</span><span class="sxs-lookup"><span data-stu-id="2d617-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="2d617-113">**NCRYPT \_ RSA \_ 演算法 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="2d617-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="2d617-114">與眾不同</span><span class="sxs-lookup"><span data-stu-id="2d617-114">"RSA"</span></span><br/>   | <span data-ttu-id="2d617-115">RSA 演算法群組。</span><span class="sxs-lookup"><span data-stu-id="2d617-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="2d617-116">**NCRYPT \_ DH \_ 演算法 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="2d617-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="2d617-117">DH</span><span class="sxs-lookup"><span data-stu-id="2d617-117">"DH"</span></span><br/>    | <span data-ttu-id="2d617-118">Diffie-Hellman 演算法群組。</span><span class="sxs-lookup"><span data-stu-id="2d617-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="2d617-119">**NCRYPT \_ DSA \_ 演算法 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="2d617-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="2d617-120">DSA</span><span class="sxs-lookup"><span data-stu-id="2d617-120">"DSA"</span></span><br/>   | <span data-ttu-id="2d617-121">DSA 演算法群組。</span><span class="sxs-lookup"><span data-stu-id="2d617-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="2d617-122">**NCRYPT \_ ECDSA \_ 演算法 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="2d617-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="2d617-123">ECDSA</span><span class="sxs-lookup"><span data-stu-id="2d617-123">"ECDSA"</span></span><br/> | <span data-ttu-id="2d617-124">橢圓曲線 DSA 演算法群組。</span><span class="sxs-lookup"><span data-stu-id="2d617-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="2d617-125">**NCRYPT \_ ECDH \_ 演算法 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="2d617-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="2d617-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="2d617-126">"ECDH"</span></span><br/>  | <span data-ttu-id="2d617-127">橢圓曲線 Diffie-Hellman 演算法群組。</span><span class="sxs-lookup"><span data-stu-id="2d617-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT \_ 演算法 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-129">L "演算法名稱"</span><span class="sxs-lookup"><span data-stu-id="2d617-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-130">以 null 終止的 Unicode 字串，其中包含物件之演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="2d617-131">這可以是其中一個預先定義的 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 或另一個已註冊的演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="2d617-132">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT \_ 相關聯的 \_ ECDH \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="2d617-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-134">L "SmartCardAssociatedECDHKey"</span><span class="sxs-lookup"><span data-stu-id="2d617-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-135">**LPWSTR** 值，這個值會指出橢圓曲線的容器名稱 Diffie-Hellman (ECDH) 金鑰，以在針對橢圓曲線數位簽章演算法 (ECDSA) 索引鍵的指定控制碼登入時使用。</span><span class="sxs-lookup"><span data-stu-id="2d617-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="2d617-136">如果卡片上沒有任何 ECDH 金鑰，則 [*金鑰儲存提供者*](/windows/desktop/SecGloss/k-gly) (KSP) 會傳回 **「 \_ 未 \_ 找到上限**」。</span><span class="sxs-lookup"><span data-stu-id="2d617-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="2d617-137">這個屬性會套用至 ECDSA 金鑰以用於以智慧卡登入。</span><span class="sxs-lookup"><span data-stu-id="2d617-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="2d617-138">Microsoft 智慧卡金鑰儲存提供者（而不是 Microsoft 軟體金鑰儲存提供者）支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="2d617-139">**Windows Server 2008 和 Windows Vista：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="2d617-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT \_ 區塊 \_ 長度 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-141">L "區塊長度"</span><span class="sxs-lookup"><span data-stu-id="2d617-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-142">**DWORD** ，其中包含加密區塊的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d617-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="2d617-143">這個屬性只適用于支援加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2d617-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT \_ 憑證 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-145">L "SmartCardKeyCertificate"</span><span class="sxs-lookup"><span data-stu-id="2d617-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-146">包含與金鑰相關聯之 x.509 憑證的 [*BLOB*](/windows/desktop/SecGloss/b-gly) 。</span><span class="sxs-lookup"><span data-stu-id="2d617-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="2d617-147">**Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 包含 [*智慧卡*](/windows/desktop/SecGloss/s-gly)金鑰 [*憑證*](/windows/desktop/SecGloss/c-gly)的 [*BLOB*](/windows/desktop/SecGloss/b-gly) 。</span><span class="sxs-lookup"><span data-stu-id="2d617-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="2d617-148">Microsoft 軟體金鑰儲存提供者不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT \_ DH \_ 參數 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-150">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="2d617-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-151">指定要搭配 Diffie-Hellman 索引鍵使用的參數。</span><span class="sxs-lookup"><span data-stu-id="2d617-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="2d617-152">此資料類型是 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2d617-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="2d617-153">這個屬性只能設定，而且必須在金鑰完成之前針對索引鍵設定。</span><span class="sxs-lookup"><span data-stu-id="2d617-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT \_ 匯出 \_ 原則 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-155">L 「匯出原則」</span><span class="sxs-lookup"><span data-stu-id="2d617-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-156">**DWORD** ，其中包含一組旗標，可指定保存金鑰的匯出原則。</span><span class="sxs-lookup"><span data-stu-id="2d617-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="2d617-157">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-157">This property only applies to keys.</span></span> <span data-ttu-id="2d617-158">這可以包含零個或一個或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="2d617-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="2d617-159">識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-159">Identifier</span></span>                                    | <span data-ttu-id="2d617-160">值</span><span class="sxs-lookup"><span data-stu-id="2d617-160">Value</span></span>      | <span data-ttu-id="2d617-161">描述</span><span class="sxs-lookup"><span data-stu-id="2d617-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d617-162">**NCRYPT \_ 允許 \_ 匯出 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="2d617-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d617-163">0x00000001</span></span> | <span data-ttu-id="2d617-164">您可以匯出私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2d617-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2d617-165">**NCRYPT \_ 允許 \_ 純文字 \_ 匯出 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="2d617-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2d617-166">0x00000002</span></span> | <span data-ttu-id="2d617-167">私密金鑰可以用純文字格式匯出。</span><span class="sxs-lookup"><span data-stu-id="2d617-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2d617-168">**NCRYPT \_ 允許 \_ 封存 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="2d617-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2d617-169">0x00000004</span></span> | <span data-ttu-id="2d617-170">私密金鑰可以匯出一次，以供封存之用。</span><span class="sxs-lookup"><span data-stu-id="2d617-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="2d617-171">此旗標只適用于設定它的原始金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="2d617-172">此原則只能套用至原始金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="2d617-173">關閉金鑰控制碼之後，就無法再匯出金鑰以供封存之用。</span><span class="sxs-lookup"><span data-stu-id="2d617-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="2d617-174">**NCRYPT \_ 允許 \_ 純文字封存 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="2d617-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2d617-175">0x00000008</span></span> | <span data-ttu-id="2d617-176">私密金鑰可以用純文字格式匯出一次，以供封存之用。</span><span class="sxs-lookup"><span data-stu-id="2d617-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="2d617-177">此旗標只適用于設定它的原始金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="2d617-178">此原則只能套用至原始金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="2d617-179">關閉金鑰控制碼之後，就無法再匯出金鑰以供封存之用。</span><span class="sxs-lookup"><span data-stu-id="2d617-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT \_ IMPL \_ TYPE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-181">L "Impl Type"</span><span class="sxs-lookup"><span data-stu-id="2d617-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-182">包含一組旗標的 **DWORD** ，這些旗標會定義提供者的執行詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d617-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="2d617-183">這個屬性只適用于金鑰儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="2d617-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="2d617-184">這可以包含零個或一個或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="2d617-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="2d617-185">識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-185">Identifier</span></span>                            | <span data-ttu-id="2d617-186">值</span><span class="sxs-lookup"><span data-stu-id="2d617-186">Value</span></span>      | <span data-ttu-id="2d617-187">描述</span><span class="sxs-lookup"><span data-stu-id="2d617-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="2d617-188">**NCRYPT \_ IMPL \_ 硬體 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="2d617-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d617-189">0x00000001</span></span> | <span data-ttu-id="2d617-190">提供者是以硬體為基礎。</span><span class="sxs-lookup"><span data-stu-id="2d617-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="2d617-191">**NCRYPT \_ IMPL \_ SOFTWARE \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="2d617-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2d617-192">0x00000002</span></span> | <span data-ttu-id="2d617-193">提供者是以軟體為基礎。</span><span class="sxs-lookup"><span data-stu-id="2d617-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="2d617-194">**NCRYPT \_ IMPL \_ 可移動 \_ 旗旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="2d617-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2d617-195">0x00000008</span></span> | <span data-ttu-id="2d617-196">提供者是可移動的。</span><span class="sxs-lookup"><span data-stu-id="2d617-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="2d617-197">**NCRYPT \_ IMPL \_ 硬體 \_ RNG \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="2d617-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d617-198">0x00000010</span></span> | <span data-ttu-id="2d617-199">提供者是以硬體為基礎的亂數字產生器。</span><span class="sxs-lookup"><span data-stu-id="2d617-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT 索引 \_ 鍵 \_ 類型 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-201">L "金鑰類型"</span><span class="sxs-lookup"><span data-stu-id="2d617-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-202">**DWORD** ，包含定義索引鍵類型的一組旗標。</span><span class="sxs-lookup"><span data-stu-id="2d617-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="2d617-203">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-203">This property only applies to keys.</span></span> <span data-ttu-id="2d617-204">這可以包含零或下列值。</span><span class="sxs-lookup"><span data-stu-id="2d617-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="2d617-205">識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-205">Identifier</span></span>                     | <span data-ttu-id="2d617-206">值</span><span class="sxs-lookup"><span data-stu-id="2d617-206">Value</span></span>      | <span data-ttu-id="2d617-207">描述</span><span class="sxs-lookup"><span data-stu-id="2d617-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d617-208">**NCRYPT \_ 機 \_ 碼 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="2d617-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d617-209">0x00000001</span></span> | <span data-ttu-id="2d617-210">金鑰適用于本機電腦。</span><span class="sxs-lookup"><span data-stu-id="2d617-210">The key applies to the local computer.</span></span> <span data-ttu-id="2d617-211">如果不存在此旗標，則會將金鑰套用至目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="2d617-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT \_ 金鑰 \_ 使用方式 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-213">L [金鑰使用方法]</span><span class="sxs-lookup"><span data-stu-id="2d617-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-214">包含一組旗標的 **DWORD** ，這些旗標會定義索引鍵的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d617-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="2d617-215">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-215">This property only applies to keys.</span></span> <span data-ttu-id="2d617-216">這可以包含零個或一個或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="2d617-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="2d617-217">識別碼</span><span class="sxs-lookup"><span data-stu-id="2d617-217">Identifier</span></span>                              | <span data-ttu-id="2d617-218">值</span><span class="sxs-lookup"><span data-stu-id="2d617-218">Value</span></span>      | <span data-ttu-id="2d617-219">描述</span><span class="sxs-lookup"><span data-stu-id="2d617-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="2d617-220">**NCRYPT \_ 允許 \_ 解密 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="2d617-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d617-221">0x00000001</span></span> | <span data-ttu-id="2d617-222">金鑰可以用來解密。</span><span class="sxs-lookup"><span data-stu-id="2d617-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="2d617-223">**NCRYPT \_ 允許 \_ 簽署 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="2d617-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2d617-224">0x00000002</span></span> | <span data-ttu-id="2d617-225">金鑰可以用來簽署。</span><span class="sxs-lookup"><span data-stu-id="2d617-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="2d617-226">**NCRYPT \_ 允許 \_ 金鑰 \_ 合約 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2d617-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="2d617-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2d617-227">0x00000004</span></span> | <span data-ttu-id="2d617-228">金鑰可用於秘密協定加密。</span><span class="sxs-lookup"><span data-stu-id="2d617-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="2d617-229">**NCRYPT \_ 允許 \_ 所有 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="2d617-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="2d617-230">0x00ffffff</span><span class="sxs-lookup"><span data-stu-id="2d617-230">0x00ffffff</span></span> | <span data-ttu-id="2d617-231">金鑰可用於任何用途。</span><span class="sxs-lookup"><span data-stu-id="2d617-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT \_ 上次 \_ 修改的 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-233">L 「已修改」</span><span class="sxs-lookup"><span data-stu-id="2d617-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-234">指出金鑰上次修改的時間。</span><span class="sxs-lookup"><span data-stu-id="2d617-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="2d617-235">此資料類型是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2d617-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="2d617-236">這個屬性只適用于保存的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2d617-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT \_ LENGTH \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-238">L "Length"</span><span class="sxs-lookup"><span data-stu-id="2d617-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-239">**DWORD** ，其中包含索引鍵的長度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d617-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="2d617-240">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT \_ 長度 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-242">L "長度"</span><span class="sxs-lookup"><span data-stu-id="2d617-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-243">指出金鑰所支援的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="2d617-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="2d617-244">此資料類型是 [**NCRYPT \_ 支援 \_ 長度**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) 結構的指標，其中包含這項資訊。</span><span class="sxs-lookup"><span data-stu-id="2d617-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="2d617-245">這個屬性只適用于索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT \_ MAX \_ NAME \_ LENGTH \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-247">L "最大名稱長度"</span><span class="sxs-lookup"><span data-stu-id="2d617-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-248">**DWORD** ，其中包含持續性索引鍵名稱的最大長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d617-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="2d617-249">這個屬性只適用于提供者。</span><span class="sxs-lookup"><span data-stu-id="2d617-249">This property only applies to a provider.</span></span>

<span data-ttu-id="2d617-250">這個屬性主要是供金鑰儲存提供者使用，這些提供者會將金鑰儲存在具有有限可用記憶體數量（例如智慧卡）的裝置上。</span><span class="sxs-lookup"><span data-stu-id="2d617-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT \_ NAME \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-252">L "Name"</span><span class="sxs-lookup"><span data-stu-id="2d617-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-253">以 null 終止的 Unicode 字串指標，其中包含物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT \_ PIN \_ 提示 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-255">L "SmartCardPinPrompt"</span><span class="sxs-lookup"><span data-stu-id="2d617-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-256">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="2d617-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT \_ 釘選 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-258">L "SmartCardPin"</span><span class="sxs-lookup"><span data-stu-id="2d617-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-259">以 null 終止的 Unicode 字串指標，其中包含 PIN。</span><span class="sxs-lookup"><span data-stu-id="2d617-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="2d617-260">PIN 可用於智慧卡金鑰或儲存在以軟體為基礎的 KSP 中的密碼保護金鑰密碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="2d617-261">只能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-261">This property can only be set.</span></span> <span data-ttu-id="2d617-262">Microsoft Ksp 會快取此值，因此每個進程只會提示使用者一次。</span><span class="sxs-lookup"><span data-stu-id="2d617-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT \_ 提供者 \_ 控制碼 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-264">L 「提供者控制碼」</span><span class="sxs-lookup"><span data-stu-id="2d617-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-265">**NCRYPT \_ >prov \_ 控制碼**，其中包含 CNG 金鑰儲存提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="2d617-266">當您完成使用控制碼時，您必須呼叫 [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) 來釋放它。</span><span class="sxs-lookup"><span data-stu-id="2d617-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT \_ 讀取器 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-268">L "SmartCardReader"</span><span class="sxs-lookup"><span data-stu-id="2d617-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-269">以 null 終止的 Unicode 字串指標，其中包含智慧卡讀取器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="2d617-270">只能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT \_ 根 \_ CERTSTORE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-272">L "SmartcardRootCertStore"</span><span class="sxs-lookup"><span data-stu-id="2d617-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-273">代表智慧卡根憑證存放區的 **HCERTSTORE** 。</span><span class="sxs-lookup"><span data-stu-id="2d617-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_捨棄 \_ PIN \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="2d617-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-275">L "SmartCardPinId"</span><span class="sxs-lookup"><span data-stu-id="2d617-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-276">與 [*智慧卡*](/windows/desktop/SecGloss/s-gly)上指定之 [*密碼編譯金鑰*](/windows/desktop/SecGloss/c-gly)相關聯的 **PIN \_ 識別碼** 值指標。</span><span class="sxs-lookup"><span data-stu-id="2d617-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="2d617-277">這是一個唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-277">This is a read-only property.</span></span> <span data-ttu-id="2d617-278">**PIN \_ 識別碼** 資料類型定義于 cardmod.h 中。</span><span class="sxs-lookup"><span data-stu-id="2d617-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="2d617-279">**Windows Server 2008 和 Windows Vista：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="2d617-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT \_ 捨棄 \_ PIN \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2d617-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-281">L "SmartCardPinInfo"</span><span class="sxs-lookup"><span data-stu-id="2d617-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-282">[**Pin 碼 \_ 資訊**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info)結構的指標，該 pin 與智慧卡上指定的密碼編譯金鑰相關聯。</span><span class="sxs-lookup"><span data-stu-id="2d617-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="2d617-283">呼叫端會提供金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d617-283">The caller provides the key handle.</span></span> <span data-ttu-id="2d617-284">這個屬性是唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-284">This property is a read-only property.</span></span> <span data-ttu-id="2d617-285">**PIN \_ 資訊** 結構定義于 cardmod.h 中。</span><span class="sxs-lookup"><span data-stu-id="2d617-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="2d617-286">**Windows Server 2008 和 Windows Vista：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="2d617-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT \_ 安全 \_ PIN \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-288">L "SmartCardSecurePin"</span><span class="sxs-lookup"><span data-stu-id="2d617-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-289">以 null 終止的 Unicode 字串指標，其中包含智慧卡會話 PIN。</span><span class="sxs-lookup"><span data-stu-id="2d617-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="2d617-290">只能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-290">This property can only be set.</span></span>

<span data-ttu-id="2d617-291">**Windows Vista：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT \_ 安全性 \_ 描述 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-293">L "Security 描述"</span><span class="sxs-lookup"><span data-stu-id="2d617-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-294">[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構的指標，其中包含索引鍵的存取控制資訊。</span><span class="sxs-lookup"><span data-stu-id="2d617-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="2d617-295">這個屬性只適用于持續性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="2d617-296">[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)或 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)函數的 *dwFlags* 參數會識別要取得或設定的安全描述項部分。</span><span class="sxs-lookup"><span data-stu-id="2d617-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT \_ SECURITY \_ 描述 \_ SUPPORT \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-298">L "Security 描述 Support"</span><span class="sxs-lookup"><span data-stu-id="2d617-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-299">指出提供者是否支援金鑰的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="2d617-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="2d617-300">如果提供者支援索引鍵的安全描述項，則這個屬性是包含1的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="2d617-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="2d617-301">如果此屬性包含任何其他值，或如果 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式傳回 **\_ 不 \_ 支援的上限**，則提供者不支援金鑰的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="2d617-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="2d617-302">這個屬性只適用于提供者。</span><span class="sxs-lookup"><span data-stu-id="2d617-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT \_ 智慧卡 \_ GUID \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-304">L "SmartCardGuid"</span><span class="sxs-lookup"><span data-stu-id="2d617-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-305">包含智慧卡識別碼的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="2d617-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT \_ UI \_ 原則 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-307">L "UI 原則"</span><span class="sxs-lookup"><span data-stu-id="2d617-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-308">如果搭配 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) 或 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式使用，這是 [**NCRYPT \_ UI \_ 原則**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) 結構的指標，其中包含索引鍵的強式金鑰使用者介面原則。</span><span class="sxs-lookup"><span data-stu-id="2d617-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="2d617-309">這個屬性只適用于持續性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="2d617-310">只有在產生金鑰時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="2d617-311">針對此索引鍵呼叫 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) 函式之後，這個屬性會變成隻讀。</span><span class="sxs-lookup"><span data-stu-id="2d617-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="2d617-312">金鑰儲存提供者可以透過 [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) 回呼函式接收此參數。</span><span class="sxs-lookup"><span data-stu-id="2d617-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="2d617-313">參數值是 NCRYPT \_ UI \_ 原則 \_ BLOB 結構，其中包含相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="2d617-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="2d617-314">同樣地，當應用程式透過 NCryptSetPropertyFn 對提供者提出要求以傳回此屬性時，提供者應該會傳回 NCRYPT \_ UI \_ 原則 \_ BLOB 結構。</span><span class="sxs-lookup"><span data-stu-id="2d617-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT \_ 唯一 \_ 名稱 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-316">L 「唯一名稱」</span><span class="sxs-lookup"><span data-stu-id="2d617-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-317">以 null 終止的 Unicode 字串指標，其中包含物件的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="2d617-318">這是存取金鑰時可使用的替代名稱。</span><span class="sxs-lookup"><span data-stu-id="2d617-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="2d617-319">當您認為原本傳遞給 [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) 的索引鍵名稱不是唯一的，而無法可靠地識別保存的金鑰時，就會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="2d617-320">Microsoft 金鑰儲存提供者將會以這個屬性傳回金鑰的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2d617-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ 使用 \_ 上下文 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-322">L 「使用內容」</span><span class="sxs-lookup"><span data-stu-id="2d617-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-323">以 null 結束的 Unicode 字串指標，描述作業的內容。</span><span class="sxs-lookup"><span data-stu-id="2d617-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="2d617-324">這個屬性不是持續性的，而且可以在提供者或索引鍵上進行設定。</span><span class="sxs-lookup"><span data-stu-id="2d617-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="2d617-325">索引鍵無法存取提供者的 **NCRYPT \_ USE \_ CONTEXT \_ property** 屬性，因為該屬性只是針對它所設定的控制碼所特有。</span><span class="sxs-lookup"><span data-stu-id="2d617-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="2d617-326">在提供者的內容中使用此屬性的範例，就是在呼叫 ([**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 時需要提示使用者的金鑰儲存提供者，例如「在讀取器中插入您的智慧卡」。) 。</span><span class="sxs-lookup"><span data-stu-id="2d617-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="2d617-327">由於在 **NCryptOpenKey** 傳回之前無法使用金鑰控制碼，因此應用程式應該在呼叫 **NCryptOpenKey** 之前，在提供者控制碼上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="2d617-328">在金鑰控制碼的內容中使用此屬性的範例是金鑰儲存提供者，需要在使用 (金鑰的作業期間提示使用者，例如「此應用程式必須使用此金鑰來簽署檔」。) 。</span><span class="sxs-lookup"><span data-stu-id="2d617-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="2d617-329">然後，提供者可以將此內容資訊轉送至作業期間所顯示之任何使用者介面中的使用者。</span><span class="sxs-lookup"><span data-stu-id="2d617-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT \_ USE \_ COUNT \_ ENABLED \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-331">L 「啟用的使用計數」</span><span class="sxs-lookup"><span data-stu-id="2d617-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-332">指出提供者是否支援索引鍵的使用計數。</span><span class="sxs-lookup"><span data-stu-id="2d617-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="2d617-333">如果提供者支援索引鍵的使用計數，則這個屬性是包含1的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="2d617-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="2d617-334">如果此屬性包含任何其他值，或如果 [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) 函式傳回 **\_ 不 \_ 支援的上限**，則提供者不支援索引鍵的使用計數。</span><span class="sxs-lookup"><span data-stu-id="2d617-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="2d617-335">這個屬性只適用于提供者。</span><span class="sxs-lookup"><span data-stu-id="2d617-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT \_ USE \_ COUNT \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-337">L 「使用計數」</span><span class="sxs-lookup"><span data-stu-id="2d617-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-338">[**ULARGE \_ 整數**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1)變數，其中包含指定的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)已執行的作業數目。</span><span class="sxs-lookup"><span data-stu-id="2d617-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="2d617-339">這個屬性是選擇性的，並非所有提供者都支援。</span><span class="sxs-lookup"><span data-stu-id="2d617-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="2d617-340">在索引鍵上支援此屬性的提供者，也應該支援提供者控制碼上的 **NCRYPT \_ USE \_ COUNT \_ ENABLED \_ 屬性** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="2d617-341">Microsoft 金鑰儲存提供者不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2d617-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="2d617-342">這個屬性只適用于持續性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d617-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT \_ 使用者 \_ CERTSTORE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-344">L "SmartCardUserCertStore"</span><span class="sxs-lookup"><span data-stu-id="2d617-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-345">**HCERTSTORE** ，代表智慧卡使用者憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="2d617-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT \_ VERSION \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-347">L "Version"</span><span class="sxs-lookup"><span data-stu-id="2d617-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-348">**DWORD** ，其中包含提供者的軟體版本。</span><span class="sxs-lookup"><span data-stu-id="2d617-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="2d617-349">最大的單字包含主要版本，而低字組則包含次要版本。</span><span class="sxs-lookup"><span data-stu-id="2d617-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="2d617-350">例如，0x00030033 = 3.51。</span><span class="sxs-lookup"><span data-stu-id="2d617-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="2d617-351">這個屬性只適用于提供者。</span><span class="sxs-lookup"><span data-stu-id="2d617-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d617-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT \_ 視窗 \_ 控制碼 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2d617-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d617-353">L "HWND 控制碼"</span><span class="sxs-lookup"><span data-stu-id="2d617-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="2d617-354">視窗控制碼的指標 (**HWND**) 要做為顯示之任何使用者介面的父系。</span><span class="sxs-lookup"><span data-stu-id="2d617-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="2d617-355">由於使用父系的 **Null** 視窗控制碼來顯示使用者介面時可能會發生不必要的行為，因此強烈建議您不要在設定這個屬性的情況下，將金鑰儲存提供者顯示為使用者介面。</span><span class="sxs-lookup"><span data-stu-id="2d617-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="2d617-356">以下是用來定義屬性資料限制的值。</span><span class="sxs-lookup"><span data-stu-id="2d617-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="2d617-357">常數/值</span><span class="sxs-lookup"><span data-stu-id="2d617-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="2d617-358">Description</span><span class="sxs-lookup"><span data-stu-id="2d617-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="2d617-359"><dt>**NCRYPT \_最大 \_ 屬性 \_ 資料**</dt> <dt>0x100000</dt></span><span class="sxs-lookup"><span data-stu-id="2d617-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="2d617-360">指定屬性值的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d617-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="2d617-361"><dt>**NCRYPT \_最大 \_ 屬性 \_ 名稱**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="2d617-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="2d617-362">指定屬性名稱的大小上限（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d617-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2d617-363">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d617-363">Requirements</span></span>



| <span data-ttu-id="2d617-364">需求</span><span class="sxs-lookup"><span data-stu-id="2d617-364">Requirement</span></span> | <span data-ttu-id="2d617-365">值</span><span class="sxs-lookup"><span data-stu-id="2d617-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2d617-366">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d617-366">Minimum supported client</span></span><br/> | <span data-ttu-id="2d617-367">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d617-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2d617-368">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d617-368">Minimum supported server</span></span><br/> | <span data-ttu-id="2d617-369">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d617-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2d617-370">標頭</span><span class="sxs-lookup"><span data-stu-id="2d617-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d617-371"><dt>Ncrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d617-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d617-372">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d617-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d617-373">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="2d617-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="2d617-374">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="2d617-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 


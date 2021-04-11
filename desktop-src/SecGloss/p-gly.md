---
description: 包含以字母 P 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: 'P (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850515"
---
# <a name="p-security-glossary"></a><span data-ttu-id="6298e-103">P (安全性詞彙) </span><span class="sxs-lookup"><span data-stu-id="6298e-103">P (Security Glossary)</span></span>

<span data-ttu-id="6298e-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [](u-gly.md) [](v-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="6298e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="6298e-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**填充**</span><span class="sxs-lookup"><span data-stu-id="6298e-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-106">通常會在最後一個純文字區塊很短時加入的字串。</span><span class="sxs-lookup"><span data-stu-id="6298e-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="6298e-107">例如，如果區塊長度是64位，而最後一個區塊只包含40個位，則必須將24位的填補加入至最後一個區塊。</span><span class="sxs-lookup"><span data-stu-id="6298e-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="6298e-108">填補字串可能包含零、替代零和一或其他模式。</span><span class="sxs-lookup"><span data-stu-id="6298e-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="6298e-109">使用 [*CryptoAPI*](c-gly.md) 的應用程式不需要在其加密之前將填補新增至其純文字，也不需要在解密後將其移除。</span><span class="sxs-lookup"><span data-stu-id="6298e-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="6298e-110">這會自動處理。</span><span class="sxs-lookup"><span data-stu-id="6298e-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**密碼篩選**</span><span class="sxs-lookup"><span data-stu-id="6298e-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-112">提供密碼原則強制執行和變更通知的 DLL。</span><span class="sxs-lookup"><span data-stu-id="6298e-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="6298e-113">由密碼篩選器所執行的函式是由 [*本地安全機構*](l-gly.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="6298e-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**持續性儲存體**</span><span class="sxs-lookup"><span data-stu-id="6298e-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-115">當它的電源中斷連線時，任何保持不變的儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="6298e-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="6298e-116">許多 [*憑證存放區*](c-gly.md) 資料庫都是持續性儲存的形式。</span><span class="sxs-lookup"><span data-stu-id="6298e-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**Pkcs**</span><span class="sxs-lookup"><span data-stu-id="6298e-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-118">請參閱 *公開金鑰加密標準*。</span><span class="sxs-lookup"><span data-stu-id="6298e-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="6298e-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-120">根據 [RFC 3447](https://tools.ietf.org/html/rfc3447)中定義的 RSA 演算法來實行公開金鑰加密的建議標準。</span><span class="sxs-lookup"><span data-stu-id="6298e-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="6298e-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-122">RSA Data Security，Inc. 開發和維護的個人資訊交換語法標準此語法標準會指定可移植格式，以儲存或傳輸使用者的私密金鑰、憑證和其他秘密。</span><span class="sxs-lookup"><span data-stu-id="6298e-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="6298e-123">另請參閱 [*憑證*](c-gly.md) 和 *公開金鑰加密標準*。</span><span class="sxs-lookup"><span data-stu-id="6298e-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \# 7 簽署的資料**</span><span class="sxs-lookup"><span data-stu-id="6298e-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-125">使用公開金鑰加密標準 \# 7 (PKCS 7) 簽署的資料物件， \# 並封裝用來簽署檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="6298e-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="6298e-126">通常，它會包含簽署者的憑證和 [*根憑證*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="6298e-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-128">密碼編譯訊息語法標準。</span><span class="sxs-lookup"><span data-stu-id="6298e-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="6298e-129">一種通用的資料語法，可套用在數位簽章與加密之類的密碼編譯上。</span><span class="sxs-lookup"><span data-stu-id="6298e-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="6298e-130">它也提供將憑證或憑證撤銷清單和其他訊息屬性（例如時間戳記）傳播至訊息的語法。</span><span class="sxs-lookup"><span data-stu-id="6298e-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS \_ 7 \_ ASN \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="6298e-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-132">[*訊息編碼類型*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="6298e-133">訊息編碼類型會儲存在 **DWORD** (值的高序位字組中： 0x00010000) 。</span><span class="sxs-lookup"><span data-stu-id="6298e-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**明文**</span><span class="sxs-lookup"><span data-stu-id="6298e-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-135">尚未加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="6298e-135">A message that is not encrypted.</span></span> <span data-ttu-id="6298e-136">純文字 (Plaintext) 訊息有時亦稱為「純文字」(Cleartext) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6298e-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**可攜式可執行檔 (PE) 映射**</span><span class="sxs-lookup"><span data-stu-id="6298e-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-138">標準 Windows 可執行檔案格式。</span><span class="sxs-lookup"><span data-stu-id="6298e-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**Prf**</span><span class="sxs-lookup"><span data-stu-id="6298e-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-140">請參閱 *虛擬隨機函數*。</span><span class="sxs-lookup"><span data-stu-id="6298e-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**主要認證**</span><span class="sxs-lookup"><span data-stu-id="6298e-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-142">MsV1 \_ 0 authentication 套件會定義主要認證金鑰字串值：主要認證字串會保留初始登入時提供的認證。</span><span class="sxs-lookup"><span data-stu-id="6298e-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="6298e-143">它包含使用者名稱，以及區分大小寫且區分大小寫的使用者密碼格式。</span><span class="sxs-lookup"><span data-stu-id="6298e-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="6298e-144">另請參閱 [*補充認證*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**主要服務提供者**</span><span class="sxs-lookup"><span data-stu-id="6298e-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-146">提供卡片控制項介面的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6298e-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="6298e-147">每個智慧卡都可以在智慧卡資料庫中註冊其主要服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6298e-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**主要權杖**</span><span class="sxs-lookup"><span data-stu-id="6298e-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-149">通常只由 Windows 核心建立的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="6298e-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="6298e-150">它可能會指派給處理常式，以代表該進程的預設安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="6298e-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="6298e-151">另請參閱 [*存取權杖*](a-gly.md) 和模擬 [*權杖*](i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**主要**</span><span class="sxs-lookup"><span data-stu-id="6298e-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-153">請參閱 [*安全性主體*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**隱私**</span><span class="sxs-lookup"><span data-stu-id="6298e-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-155">從 view 或 secret 隔離的條件。</span><span class="sxs-lookup"><span data-stu-id="6298e-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="6298e-156">就訊息而言，私用訊息是加密的訊息，其文字會隱藏在視野之外。</span><span class="sxs-lookup"><span data-stu-id="6298e-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="6298e-157">就金鑰而言，私密金鑰是與其他金鑰隱藏的秘密金鑰。</span><span class="sxs-lookup"><span data-stu-id="6298e-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**私密金鑰**</span><span class="sxs-lookup"><span data-stu-id="6298e-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-159">公開金鑰演算法中所使用之金鑰組的密碼一半。</span><span class="sxs-lookup"><span data-stu-id="6298e-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="6298e-160">一般來說，私密金鑰可用來加密對稱工作階段金鑰、對訊息進行數位簽署，或是針對使用對應公開金鑰加密的訊息進行解密。</span><span class="sxs-lookup"><span data-stu-id="6298e-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="6298e-161">另請參閱 *公開金鑰*。</span><span class="sxs-lookup"><span data-stu-id="6298e-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**私密金鑰 BLOB**</span><span class="sxs-lookup"><span data-stu-id="6298e-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-163">包含完整公開/私密金鑰組的金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="6298e-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="6298e-164">系統管理程式會使用私密金鑰 Blob 來傳輸金鑰組。</span><span class="sxs-lookup"><span data-stu-id="6298e-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="6298e-165">因為金鑰組的私密金鑰部分非常機密，所以這些 Blob 通常會以對稱加密來加密。</span><span class="sxs-lookup"><span data-stu-id="6298e-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="6298e-166">這些金鑰 Blob 也可供高階應用程式使用，其中金鑰組會儲存在應用程式中，而不是依賴 CSP 的儲存機制。</span><span class="sxs-lookup"><span data-stu-id="6298e-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="6298e-167">藉由呼叫 **CryptExportKey** 函數來建立金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="6298e-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**特權**</span><span class="sxs-lookup"><span data-stu-id="6298e-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-169">使用者用來執行各種系統相關作業的權限，例如關閉系統、載入裝置驅動程式，或是變更系統時間等等。</span><span class="sxs-lookup"><span data-stu-id="6298e-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="6298e-170">使用者的存取權杖包含使用者或使用者群組所持有的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="6298e-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**過程**</span><span class="sxs-lookup"><span data-stu-id="6298e-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-172">應用程式賴以執行的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="6298e-172">The security context under which an application runs.</span></span> <span data-ttu-id="6298e-173">一般來說，安全性內容會與使用者相關聯，因此所有在特定處理序下執行的應用程式都會具備擁有之使用者的權限。</span><span class="sxs-lookup"><span data-stu-id="6298e-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**>PROV \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="6298e-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-175">請參閱 *>prov \_ DSS 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**>PROV \_ DSS 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-177">預先定義的提供者類型，僅支援數位簽章和雜湊。</span><span class="sxs-lookup"><span data-stu-id="6298e-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="6298e-178">它會指定 DSA 簽名演算法，以及 MD5 和 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**>PROV \_ DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="6298e-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-180">請參閱 *>prov \_ DSS \_ DH 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**>PROV \_ DSS \_ DH 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-182">預先定義的提供者類型，可提供金鑰交換、數位簽章和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="6298e-183">它類似于 >PROV \_ DSS 提供者類型。</span><span class="sxs-lookup"><span data-stu-id="6298e-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**>PROV \_ FORTEZZA**</span><span class="sxs-lookup"><span data-stu-id="6298e-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-185">請參閱 *>prov \_ FORTEZZA 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**>PROV \_ FORTEZZA 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-187">預先定義的提供者類型，可提供金鑰交換、數位簽章、加密和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="6298e-188">此提供者類型所指定的密碼編譯通訊協定和演算法，是由美國國家標準和技術協會所擁有 (NIST) 。</span><span class="sxs-lookup"><span data-stu-id="6298e-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**>PROV \_ MS \_ EXCHANGE**</span><span class="sxs-lookup"><span data-stu-id="6298e-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-190">請參閱 *>prov \_ MS \_ EXCHANGE 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**>PROV \_ MS \_ EXCHANGE 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-192">預先定義的提供者類型，專為 Microsoft Exchange 的需求以及與 Microsoft Mail 相容的其他應用程式所設計。</span><span class="sxs-lookup"><span data-stu-id="6298e-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="6298e-193">它提供了金鑰交換、數位簽章、加密和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**>PROV \_ RSA \_ FULL**</span><span class="sxs-lookup"><span data-stu-id="6298e-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-195">請參閱 *>prov \_ RSA \_ 完整提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**>PROV \_ RSA \_ 完整提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-197">由 Microsoft 和 RSA Data Security，Inc. 定義的預先定義提供者類型。此一般目的提供者類型提供了金鑰交換、數位簽章、加密和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="6298e-198">金鑰交換、數位簽章和加密演算法是以 RSA 公開金鑰加密為基礎。</span><span class="sxs-lookup"><span data-stu-id="6298e-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**>PROV \_ RSA \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="6298e-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-200">請參閱 *>prov \_ RSA \_ SIG 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**>PROV \_ RSA \_ SIG 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-202">由 Microsoft 和 RSA 資料安全性定義的預先定義提供者類型。</span><span class="sxs-lookup"><span data-stu-id="6298e-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="6298e-203">此提供者類型是 >PROV \_ RSA FULL 的子集 \_ ，僅提供數位簽章和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="6298e-204">數位簽章演算法是 RSA 公開金鑰演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**>PROV \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="6298e-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-206">請參閱 *>prov \_ SSL 提供者類型*。</span><span class="sxs-lookup"><span data-stu-id="6298e-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**>PROV \_ SSL 提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-208">支援安全通訊端層 (SSL) 通訊協定的預先定義提供者類型。</span><span class="sxs-lookup"><span data-stu-id="6298e-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="6298e-209">此類型提供金鑰加密、數位簽章、加密和雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6298e-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="6298e-210">可從 Netscape communication Corp 取得說明 SSL 的規格。</span><span class="sxs-lookup"><span data-stu-id="6298e-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="6298e-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-212">請參閱 [*密碼編譯服務提供者*](c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6298e-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**提供者名稱**</span><span class="sxs-lookup"><span data-stu-id="6298e-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-214">用來識別 CSP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6298e-214">A name used to identify a CSP.</span></span> <span data-ttu-id="6298e-215">例如，Microsoft 基底密碼編譯提供者版本1.0。</span><span class="sxs-lookup"><span data-stu-id="6298e-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="6298e-216">通常會在呼叫 **CryptAcquireCoNtext** 函式以連接至 CSP 時使用提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="6298e-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**提供者類型**</span><span class="sxs-lookup"><span data-stu-id="6298e-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-218">用來識別密碼編譯服務提供者類型 (CSP) 的詞彙。</span><span class="sxs-lookup"><span data-stu-id="6298e-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="6298e-219">Csp 會分組為不同的提供者類型，以代表標準資料格式和通訊協定的特定系列。</span><span class="sxs-lookup"><span data-stu-id="6298e-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="6298e-220">相較于 CSP 的唯一提供者名稱，提供者類型對指定的 CSP 而言並不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6298e-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="6298e-221">通常會在呼叫 **CryptAcquireCoNtext** 函式以連接至 CSP 時使用提供者類型。</span><span class="sxs-lookup"><span data-stu-id="6298e-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**虛擬隨機函式**</span><span class="sxs-lookup"><span data-stu-id="6298e-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-223"> (PRF) 一個函式，該函式會採用索引鍵、標籤和種子做為輸入，然後產生任意長度的輸出。</span><span class="sxs-lookup"><span data-stu-id="6298e-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**公開/私密金鑰組**</span><span class="sxs-lookup"><span data-stu-id="6298e-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-225">一組用在公開金鑰密碼編譯上的密碼編譯金鑰。</span><span class="sxs-lookup"><span data-stu-id="6298e-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="6298e-226">針對每個使用者，CSP 通常會維護兩組公開/私密金鑰組：交換金鑰組和數位簽章金鑰組。</span><span class="sxs-lookup"><span data-stu-id="6298e-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="6298e-227">兩組金鑰不管任何工作階段都會受到維護。</span><span class="sxs-lookup"><span data-stu-id="6298e-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="6298e-228">請參閱 [*exchange 金鑰*](e-gly.md) 組和簽章 [*金鑰*](s-gly.md)組。</span><span class="sxs-lookup"><span data-stu-id="6298e-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="6298e-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**公開金鑰**</span><span class="sxs-lookup"><span data-stu-id="6298e-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-230">解密工作階段金鑰或數位簽章時，慣常使用的密碼編譯金鑰。</span><span class="sxs-lookup"><span data-stu-id="6298e-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="6298e-231">公開金鑰也可以用來加密訊息，以保證只有擁有對應之私密金鑰的使用者才能解密訊息。</span><span class="sxs-lookup"><span data-stu-id="6298e-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="6298e-232">另請參閱 *私密金鑰*。</span><span class="sxs-lookup"><span data-stu-id="6298e-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**公開金鑰演算法**</span><span class="sxs-lookup"><span data-stu-id="6298e-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-234">使用兩個金鑰的非對稱式加密，一個用於加密、公開金鑰和另一個用於解密，也就是私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="6298e-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="6298e-235">如同金鑰名稱所暗示，用來將純文字編碼的公開金鑰可供任何人使用。</span><span class="sxs-lookup"><span data-stu-id="6298e-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="6298e-236">不過，私密金鑰必須保持秘密。</span><span class="sxs-lookup"><span data-stu-id="6298e-236">However, the private key must remain secret.</span></span> <span data-ttu-id="6298e-237">只有私密金鑰可以解密加密文字。</span><span class="sxs-lookup"><span data-stu-id="6298e-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="6298e-238">在此程式中使用的公開金鑰演算法很慢 (的順序比) 1000 的對稱演算法慢，而且通常用來加密工作階段金鑰或數位簽署訊息。</span><span class="sxs-lookup"><span data-stu-id="6298e-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="6298e-239">另請參閱 *公開金鑰* 和 *私密金鑰*。</span><span class="sxs-lookup"><span data-stu-id="6298e-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**公開金鑰 BLOB**</span><span class="sxs-lookup"><span data-stu-id="6298e-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-241">用來儲存公開/私密金鑰組之公開金鑰部分的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="6298e-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="6298e-242">公開金鑰 Blob 未加密，因為包含在中的公開金鑰不是秘密。</span><span class="sxs-lookup"><span data-stu-id="6298e-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="6298e-243">公開金鑰 BLOB 是藉由呼叫 **CryptExportKey** 函式所建立。</span><span class="sxs-lookup"><span data-stu-id="6298e-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**公開金鑰密碼編譯標準**</span><span class="sxs-lookup"><span data-stu-id="6298e-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-245"> (PKCS) 一組涵蓋安全性功能的公開金鑰加密語法標準，包括簽署資料的方法、交換金鑰、要求憑證、公開金鑰加密和解密，以及其他安全性功能。</span><span class="sxs-lookup"><span data-stu-id="6298e-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="6298e-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**公開金鑰加密**</span><span class="sxs-lookup"><span data-stu-id="6298e-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="6298e-247">使用一組金鑰來加密，其中一支金鑰用來加密資料，而另一支用來解密資料。</span><span class="sxs-lookup"><span data-stu-id="6298e-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="6298e-248">反之，對稱的加密演算法會使用相同的金鑰來進行加密與解密。</span><span class="sxs-lookup"><span data-stu-id="6298e-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="6298e-249">在實務上，公開金鑰加密通常用來保護對稱式加密演算法所使用的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="6298e-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="6298e-250">在此情況下，會使用公開金鑰來加密工作階段金鑰，而過去則是用它來加密一些資料，而私密金鑰則是用來解密。</span><span class="sxs-lookup"><span data-stu-id="6298e-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="6298e-251">除了保護工作階段金鑰之外，公開金鑰密碼編譯同時也可用來數位簽署訊息 (使用私密金鑰) 並驗證簽章 (使用公開金鑰)。</span><span class="sxs-lookup"><span data-stu-id="6298e-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="6298e-252">另請參閱 *公開金鑰演算法*。</span><span class="sxs-lookup"><span data-stu-id="6298e-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 




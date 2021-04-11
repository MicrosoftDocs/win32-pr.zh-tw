---
description: 有一些威脅防護技術可供您使用，以提供更安全的密碼。
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: 威脅緩和技巧
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ec2b8db3a634ea93ce77d585038909056c7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851684"
---
# <a name="threat-mitigation-techniques"></a><span data-ttu-id="e968e-103">威脅緩和技巧</span><span class="sxs-lookup"><span data-stu-id="e968e-103">Threat Mitigation Techniques</span></span>

<span data-ttu-id="e968e-104">有一些威脅防護技術可供您使用，以提供更安全的密碼。</span><span class="sxs-lookup"><span data-stu-id="e968e-104">There are a number of threat-mitigation techniques available that you can use to better secure passwords.</span></span> <span data-ttu-id="e968e-105">這些技術是使用下列四種主要技術的一或多個來實行。</span><span class="sxs-lookup"><span data-stu-id="e968e-105">These techniques are implemented by using one or more of the following four, primary technologies.</span></span>



| <span data-ttu-id="e968e-106">技術</span><span class="sxs-lookup"><span data-stu-id="e968e-106">Technology</span></span>                      | <span data-ttu-id="e968e-107">描述</span><span class="sxs-lookup"><span data-stu-id="e968e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e968e-108">CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="e968e-108">CryptoAPI</span></span>                       | <span data-ttu-id="e968e-109">CryptoAPI 提供一組功能，可協助您將密碼編譯常式套用至目標實體。</span><span class="sxs-lookup"><span data-stu-id="e968e-109">CryptoAPI provides a set of functions that help you apply cryptographic routines to target entities.</span></span> <span data-ttu-id="e968e-110">CryptoAPI 可以提供雜湊、摘要、加密和解密，以提及其主要功能。</span><span class="sxs-lookup"><span data-stu-id="e968e-110">CryptoAPI can provide hashes, digests, encryption, and decryption, to mention its primary functionality.</span></span> <span data-ttu-id="e968e-111">CryptoAPI 也有其他功能。</span><span class="sxs-lookup"><span data-stu-id="e968e-111">CryptoAPI also has other features.</span></span> <span data-ttu-id="e968e-112">若要瞭解密碼編譯和 CryptoAPI，請參閱 [密碼編譯基本](/windows/desktop/SecCrypto/cryptography-essentials)資訊。</span><span class="sxs-lookup"><span data-stu-id="e968e-112">To learn about cryptography and the CryptoAPI, see [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).</span></span>           |
| <span data-ttu-id="e968e-113">存取控制清單</span><span class="sxs-lookup"><span data-stu-id="e968e-113">Access control lists</span></span>            | <span data-ttu-id="e968e-114"> (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 是適用于物件的安全性保護清單。</span><span class="sxs-lookup"><span data-stu-id="e968e-114">An [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) is a list of security protections that applies to an object.</span></span> <span data-ttu-id="e968e-115">物件可以是檔案、進程、事件，或是具有安全描述項的任何其他專案。</span><span class="sxs-lookup"><span data-stu-id="e968e-115">An object can be a file, process, event, or anything else that has a security descriptor.</span></span> <span data-ttu-id="e968e-116">如需 Acl 的詳細資訊，請參閱)  (Acl 的 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists) 。</span><span class="sxs-lookup"><span data-stu-id="e968e-116">For more information on ACLs see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists) (ACLs).</span></span> |
| <span data-ttu-id="e968e-117">資料保護 API</span><span class="sxs-lookup"><span data-stu-id="e968e-117">Data protection API</span></span>             | <span data-ttu-id="e968e-118"> (DPAPI) 的資料保護 API 提供下列四個函式，用來加密和解密機密資料： [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata)、 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)、 [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)和 [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory)。</span><span class="sxs-lookup"><span data-stu-id="e968e-118">The data protection API (DPAPI) provides the following four functions that you use to encrypt and decrypt sensitive data: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory), and [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).</span></span>                  |
| <span data-ttu-id="e968e-119">儲存的使用者名稱和密碼</span><span class="sxs-lookup"><span data-stu-id="e968e-119">Stored user names and passwords</span></span> | <span data-ttu-id="e968e-120">可處理使用者密碼和其他認證的儲存功能，例如私密金鑰、更簡單、更一致且更安全。</span><span class="sxs-lookup"><span data-stu-id="e968e-120">Storage functionality that makes handling users' passwords and other credentials, such as private keys, easier, more consistent, and safer.</span></span> <span data-ttu-id="e968e-121">如需此功能的詳細資訊，請參閱 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)。</span><span class="sxs-lookup"><span data-stu-id="e968e-121">For more information on this functionality, see [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span>                                                                                                         |



 

<span data-ttu-id="e968e-122">這些技術在所有作業系統上都無法使用。</span><span class="sxs-lookup"><span data-stu-id="e968e-122">These technologies are not available on all operating systems.</span></span> <span data-ttu-id="e968e-123">因此，安全性可以改善的範圍取決於所涉及的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e968e-123">Therefore, the extent to which security can be improved depends on which operating systems are involved.</span></span> <span data-ttu-id="e968e-124">以下是每個作業系統所提供的技術。</span><span class="sxs-lookup"><span data-stu-id="e968e-124">Here are the technologies that are available in each operating system.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e968e-125">作業系統</span><span class="sxs-lookup"><span data-stu-id="e968e-125">Operating system</span></span></th>
<th><span data-ttu-id="e968e-126">技術</span><span class="sxs-lookup"><span data-stu-id="e968e-126">Technology</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e968e-127">Windows Server 2003 和 Windows XP</span><span class="sxs-lookup"><span data-stu-id="e968e-127">Windows Server 2003 and Windows XP</span></span></td>
<td><ul>
<li><span data-ttu-id="e968e-128">CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="e968e-128">CryptoAPI</span></span></li>
<li><span data-ttu-id="e968e-129">存取控制清單</span><span class="sxs-lookup"><span data-stu-id="e968e-129">Access control lists</span></span></li>
<li><span data-ttu-id="e968e-130">資料保護 API</span><span class="sxs-lookup"><span data-stu-id="e968e-130">Data protection API</span></span></li>
<li><span data-ttu-id="e968e-131">儲存的使用者名稱和密碼</span><span class="sxs-lookup"><span data-stu-id="e968e-131">Stored user names and passwords</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e968e-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e968e-132">Windows 2000</span></span></td>
<td><ul>
<li><span data-ttu-id="e968e-133">CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="e968e-133">CryptoAPI</span></span></li>
<li><span data-ttu-id="e968e-134">存取控制清單</span><span class="sxs-lookup"><span data-stu-id="e968e-134">Access control lists</span></span></li>
<li><span data-ttu-id="e968e-135"><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></span><span class="sxs-lookup"><span data-stu-id="e968e-135"><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></span></span></li>
<li><span data-ttu-id="e968e-136"><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></span><span class="sxs-lookup"><span data-stu-id="e968e-136"><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e968e-137">下列威脅防護技術會使用四種技術中的一或多個技術。</span><span class="sxs-lookup"><span data-stu-id="e968e-137">The following threat-mitigation techniques use one or more of the four technologies.</span></span> <span data-ttu-id="e968e-138">不能使用不包含在作業系統中的技術需要使用的技術。</span><span class="sxs-lookup"><span data-stu-id="e968e-138">Techniques that require the use of technologies that are not included in the operating system cannot be used.</span></span>

## <a name="getting-passwords-from-the-user"></a><span data-ttu-id="e968e-139">從使用者取得密碼</span><span class="sxs-lookup"><span data-stu-id="e968e-139">Getting Passwords from the User</span></span>

<span data-ttu-id="e968e-140">當您允許使用者設定密碼時，請強制使用強式密碼。</span><span class="sxs-lookup"><span data-stu-id="e968e-140">When you allow the user to set up a password, force the use of strong passwords.</span></span> <span data-ttu-id="e968e-141">例如，要求密碼必須是最小長度，例如八個字元以上。</span><span class="sxs-lookup"><span data-stu-id="e968e-141">For example, require that passwords be a minimum length such as eight characters or more.</span></span> <span data-ttu-id="e968e-142">密碼也必須包含大寫和小寫字母、數位和其他鍵盤字元，例如貨幣符號 ($) 、驚嘆號 (！ ) 或大於 (>) 。</span><span class="sxs-lookup"><span data-stu-id="e968e-142">Passwords should also be required to include uppercase and lowercase letters, numbers, and other keyboard characters such as the dollar sign ($), exclamation point (!), or greater than (>).</span></span>

<span data-ttu-id="e968e-143">取得密碼之後，您可以快速地 (使用盡可能少的程式碼) ，然後清除密碼的所有 vestiges。</span><span class="sxs-lookup"><span data-stu-id="e968e-143">After you get a password, use it quickly (using as little code as possible), and then erase all vestiges of the password.</span></span> <span data-ttu-id="e968e-144">這可將入侵者可用來「陷阱」密碼的時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="e968e-144">This minimizes the time available to an intruder to "trap" the password.</span></span> <span data-ttu-id="e968e-145">這項技術的取捨是必須從使用者抓取密碼的頻率。不過，您應該盡可能採用此原則。</span><span class="sxs-lookup"><span data-stu-id="e968e-145">The trade-off with this technique is the frequency with which the password must be retrieved from the user; however, the principle should be employed wherever possible.</span></span> <span data-ttu-id="e968e-146">如需如何正確取得密碼的相關資訊，請參閱 [要求使用者提供認證](asking-the-user-for-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="e968e-146">For information about how to properly get passwords, see [Asking the User for Credentials](asking-the-user-for-credentials.md).</span></span>

<span data-ttu-id="e968e-147">避免提供「記住我的密碼」使用者介面選項。</span><span class="sxs-lookup"><span data-stu-id="e968e-147">Avoid providing "remember my password" user interface options.</span></span> <span data-ttu-id="e968e-148">通常，使用者會要求使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e968e-148">Often, users will demand to have this option.</span></span> <span data-ttu-id="e968e-149">如果您必須提供，則至少要確保密碼會以安全的方式儲存。</span><span class="sxs-lookup"><span data-stu-id="e968e-149">If you must provide it, then at minimum, ensure that the password gets saved in a secure fashion.</span></span> <span data-ttu-id="e968e-150">如需詳細資訊，請參閱本主題稍後的「儲存密碼」一節。</span><span class="sxs-lookup"><span data-stu-id="e968e-150">For information, see the Storing Passwords section, later in this topic.</span></span>

<span data-ttu-id="e968e-151">限制密碼輸入嘗試。</span><span class="sxs-lookup"><span data-stu-id="e968e-151">Limit password entry tries.</span></span> <span data-ttu-id="e968e-152">在特定次數的嘗試次數沒有成功之後，請將使用者鎖定一段時間。</span><span class="sxs-lookup"><span data-stu-id="e968e-152">After a certain number of tries without success, lock out the user for a certain length of time.</span></span> <span data-ttu-id="e968e-153">（選擇性）延長每次嘗試的回應時間上限。</span><span class="sxs-lookup"><span data-stu-id="e968e-153">Optionally, lengthen the response time for each try over a maximum.</span></span> <span data-ttu-id="e968e-154">這項技術的目標是要失去猜測攻擊。</span><span class="sxs-lookup"><span data-stu-id="e968e-154">This technique is aimed at defeating a guessing attack.</span></span>

## <a name="storing-passwords"></a><span data-ttu-id="e968e-155">儲存密碼</span><span class="sxs-lookup"><span data-stu-id="e968e-155">Storing Passwords</span></span>

<span data-ttu-id="e968e-156">絕對不要將密碼以純文字格式儲存 (未加密的) 。</span><span class="sxs-lookup"><span data-stu-id="e968e-156">Never store passwords in plaintext (unencrypted).</span></span> <span data-ttu-id="e968e-157">加密密碼可大幅提高安全性。</span><span class="sxs-lookup"><span data-stu-id="e968e-157">Encrypting passwords significantly increases their security.</span></span> <span data-ttu-id="e968e-158">如需有關儲存加密密碼的詳細資訊，請參閱 [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata)。</span><span class="sxs-lookup"><span data-stu-id="e968e-158">For information about storing encrypted passwords, see [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata).</span></span> <span data-ttu-id="e968e-159">如需有關在記憶體中加密密碼的詳細資訊，請參閱 [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)。</span><span class="sxs-lookup"><span data-stu-id="e968e-159">For information about encrypting passwords in memory, see [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory).</span></span> <span data-ttu-id="e968e-160">將密碼儲存在盡可能少的位置。</span><span class="sxs-lookup"><span data-stu-id="e968e-160">Store passwords in as few places as possible.</span></span> <span data-ttu-id="e968e-161">儲存密碼的位置愈多，入侵者可能會發現它的機率就愈大。</span><span class="sxs-lookup"><span data-stu-id="e968e-161">The more places a password is stored, the greater the chance that an intruder might find it.</span></span> <span data-ttu-id="e968e-162">絕對不要將密碼儲存在網頁或網頁檔案中。</span><span class="sxs-lookup"><span data-stu-id="e968e-162">Never store passwords in a webpage or in a web-based file.</span></span> <span data-ttu-id="e968e-163">將密碼儲存在網頁或網頁檔案中，可讓使用者輕鬆遭到入侵。</span><span class="sxs-lookup"><span data-stu-id="e968e-163">Storing passwords in a webpage or in a web-based file allows them to be easily compromised.</span></span>

<span data-ttu-id="e968e-164">加密密碼並儲存密碼之後，請使用安全的 Acl 來限制檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="e968e-164">After you have encrypted a password and stored it, use secure ACLs to limit access to the file.</span></span> <span data-ttu-id="e968e-165">或者，您也可以將密碼和加密金鑰儲存在可移動裝置上。</span><span class="sxs-lookup"><span data-stu-id="e968e-165">Alternatively, you can store passwords and encryption keys on removable devices.</span></span> <span data-ttu-id="e968e-166">在卸載式媒體（例如智慧卡）上儲存密碼和加密金鑰，有助於建立更安全的系統。</span><span class="sxs-lookup"><span data-stu-id="e968e-166">Storing passwords and encryption keys on a removable media, such as a smart card, helps create a more secure system.</span></span> <span data-ttu-id="e968e-167">針對指定的會話取出密碼之後，就可以移除該卡片，藉此移除入侵者可以取得存取權的可能性。</span><span class="sxs-lookup"><span data-stu-id="e968e-167">After a password is retrieved for a given session, the card can be removed, thereby removing the possibility that an intruder can gain access to it.</span></span>

 

 

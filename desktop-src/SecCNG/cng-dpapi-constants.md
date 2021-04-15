---
description: CNG 資料保護 API 會使用下列常數。
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: 'CNG DPAPI 常數 (NCryptprotect .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468732"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="ed846-103">CNG DPAPI 常數</span><span class="sxs-lookup"><span data-stu-id="ed846-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="ed846-104">CNG 資料保護 API 會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="ed846-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="ed846-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT \_ 描述 \_ 分隔符號 \_ 和**</span><span class="sxs-lookup"><span data-stu-id="ed846-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-106">L "和"</span><span class="sxs-lookup"><span data-stu-id="ed846-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="ed846-107">可以用來測試和分隔符號的保護描述項字串。</span><span class="sxs-lookup"><span data-stu-id="ed846-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ 描述 \_ 等於**</span><span class="sxs-lookup"><span data-stu-id="ed846-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-109">L "="</span><span class="sxs-lookup"><span data-stu-id="ed846-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="ed846-110">可以用來測試等號的保護描述項字串。</span><span class="sxs-lookup"><span data-stu-id="ed846-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT \_ 描述 \_ 分隔符號 \_ 或**</span><span class="sxs-lookup"><span data-stu-id="ed846-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-112">L "或"</span><span class="sxs-lookup"><span data-stu-id="ed846-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="ed846-113">可以用來測試或分隔符號的保護描述項字串。</span><span class="sxs-lookup"><span data-stu-id="ed846-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**本機的 NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_**</span><span class="sxs-lookup"><span data-stu-id="ed846-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-115">"LOCAL"</span><span class="sxs-lookup"><span data-stu-id="ed846-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-116">本機保護描述項可將內容保護至登入會話、目前的使用者或本機電腦，如下列常數所識別：</span><span class="sxs-lookup"><span data-stu-id="ed846-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="ed846-117">**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="ed846-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="ed846-118">**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="ed846-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="ed846-119">**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="ed846-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="ed846-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-121">SDDL</span><span class="sxs-lookup"><span data-stu-id="ed846-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-122">將內容保護 (安全描述項定義語言的 SDDL，) 包含安全描述項資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="ed846-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="ed846-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-124">SID</span><span class="sxs-lookup"><span data-stu-id="ed846-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-125">SID 保護描述項包含群組或主體身分識別。</span><span class="sxs-lookup"><span data-stu-id="ed846-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ WEBCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="ed846-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-127">WEBCREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="ed846-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-128">保護使用者的 web 帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="ed846-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="ed846-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-130">登錄</span><span class="sxs-lookup"><span data-stu-id="ed846-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-131">保護目前登入會話的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-131">Protects content to the current logon session.</span></span> <span data-ttu-id="ed846-132">登出或重新開機之後，使用者將無法再解密受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="ed846-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-134">設備</span><span class="sxs-lookup"><span data-stu-id="ed846-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-135">保護本機電腦的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-135">Protects content to the local computer.</span></span> <span data-ttu-id="ed846-136">本機電腦上的所有使用者都可以解密受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="ed846-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-138">使用者名</span><span class="sxs-lookup"><span data-stu-id="ed846-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-139">保護目前使用者會話的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-139">Protects content to the current user session.</span></span> <span data-ttu-id="ed846-140">只有本機電腦上的此使用者才能解密受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="ed846-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS \_ 金鑰 \_ 保護 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="ed846-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-142">「Microsoft 金鑰保護提供者」</span><span class="sxs-lookup"><span data-stu-id="ed846-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-143">代表 Microsoft 金鑰保護提供者，它支援下列常數所代表的格式：</span><span class="sxs-lookup"><span data-stu-id="ed846-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="ed846-144">**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="ed846-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="ed846-145">**本機的 NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_**</span><span class="sxs-lookup"><span data-stu-id="ed846-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="ed846-146">**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="ed846-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed846-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS \_ 用戶端 \_ 金鑰 \_ 保護 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="ed846-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed846-148">「Windows 用戶端金鑰保護提供者」</span><span class="sxs-lookup"><span data-stu-id="ed846-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="ed846-149">代表只能在用戶端上使用的 Microsoft 金鑰保護提供者，並支援下列常數所代表的格式：</span><span class="sxs-lookup"><span data-stu-id="ed846-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="ed846-150">**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ WEBCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="ed846-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed846-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed846-151">Requirements</span></span>



| <span data-ttu-id="ed846-152">需求</span><span class="sxs-lookup"><span data-stu-id="ed846-152">Requirement</span></span> | <span data-ttu-id="ed846-153">值</span><span class="sxs-lookup"><span data-stu-id="ed846-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed846-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed846-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ed846-155">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed846-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed846-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed846-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ed846-157">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed846-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ed846-158">標頭</span><span class="sxs-lookup"><span data-stu-id="ed846-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed846-159"><dt>NCryptprotect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed846-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 





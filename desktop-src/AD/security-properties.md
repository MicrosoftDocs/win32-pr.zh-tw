---
title: 使用者安全性屬性
description: 除了命名使用者物件的屬性（例如 objectGUID、objectSid、cn、distinguishedName 等等）之外，還有其他安全性屬性用於登入、網路存取和存取控制。
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- 安全性屬性，使用 AD
- 使用者安全性屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/23/2020
ms.locfileid: "103933694"
---
# <a name="user-security-attributes"></a><span data-ttu-id="d165d-105">使用者安全性屬性</span><span class="sxs-lookup"><span data-stu-id="d165d-105">User Security Attributes</span></span>

<span data-ttu-id="d165d-106">除了命名使用者物件的屬性（例如 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)、 [**objectSid**](/windows/desktop/ADSchema/a-objectsid)、 [**cn**](/windows/desktop/ADSchema/a-cn)、 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)等等）之外，還有其他安全性屬性用於登入、網路存取和存取控制。</span><span class="sxs-lookup"><span data-stu-id="d165d-106">In addition to naming properties for user objects, for example, [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**cn**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), and so on, there are other security properties used for logon, network access, and access control.</span></span> <span data-ttu-id="d165d-107">Windows 2000 安全性系統會使用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d165d-107">These properties are used by the Windows 2000 security system.</span></span> <span data-ttu-id="d165d-108">這些屬性可由 Active Directory 使用者和電腦] 嵌入式管理單元來查看和管理。</span><span class="sxs-lookup"><span data-stu-id="d165d-108">These properties can be viewed and managed by the Active Directory User and Computers snap-in.</span></span>

<dl> <dt>

<span data-ttu-id="d165d-109"><span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)</span><span class="sxs-lookup"><span data-stu-id="d165d-109"><span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-110">[**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)屬性會指定帳戶到期的時間。</span><span class="sxs-lookup"><span data-stu-id="d165d-110">The [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute specifies when an account expires.</span></span> <span data-ttu-id="d165d-111">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-111">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="d165d-112">TIMEQ 中定義 **的 \_ 永久** (值) 指出帳戶永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="d165d-112">A value of **TIMEQ\_FOREVER** (defined in Lmaccess.h) indicates that an account never expires.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-113"><span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)</span><span class="sxs-lookup"><span data-stu-id="d165d-113"><span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-114">[**AltSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)屬性是多重值屬性，其中包含針對驗證目的，x.509 憑證或外部 Kerberos 使用者帳戶到這位使用者的對應。</span><span class="sxs-lookup"><span data-stu-id="d165d-114">The [**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) attribute is a multi-valued attribute that contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span> <span data-ttu-id="d165d-115">各種安全性套件（包括公開金鑰驗證套件和 Kerberos）會在使用者出示替代形式的身分識別（例如憑證、UNIX Kerberos 票證等等）時，使用這項資料來驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="d165d-115">Various security packages, including Public Key authentication package and Kerberos, use this data to authenticate users when they present the alternative form of identification such as certificate, UNIX Kerberos ticket, and so on.</span></span> <span data-ttu-id="d165d-116">根據對應的使用者帳戶建立 Windows 2000 權杖，讓他們可以存取系統資源。</span><span class="sxs-lookup"><span data-stu-id="d165d-116">Build a Windows 2000 token based on the corresponding user account such that they can access system resources.</span></span>

<span data-ttu-id="d165d-117">針對 x.509 憑證，這些值應為 x.509v3 憑證中的簽發者和主體名稱（由外部公開憑證授權單位單位所簽發），該憑證會對應到用來尋找帳戶以進行驗證的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-117">For X.509 certificates, the values should be the Issuer and Subject names in 509v3 certificates, issued by an external public certification authority, that map to the user account used to find an account for authentication.</span></span> <span data-ttu-id="d165d-118">SSL (Schannel) 封裝使用下列語法： X509： <somecertinfotype> somecertinfo。</span><span class="sxs-lookup"><span data-stu-id="d165d-118">The SSL (Schannel) package uses the following syntax: X509:<somecertinfotype>somecertinfo.</span></span> <span data-ttu-id="d165d-119">例如，下列值會以 dn " \<I\> c = us，o = InternetCA，CN = APublicCertificateAuthority"，以及 \<S\> Dn "c = Us，o = FABRIKAM，OU = SALES，CN = Jeff Smith" 的主體 dn ""，來指定簽發者 DN ""。</span><span class="sxs-lookup"><span data-stu-id="d165d-119">For example, the following value specifies the issuer DN "\<I\>" with the DN "C=US,O=InternetCA,CN=APublicCertificateAuthority" and the subject DN "\<S\>" with the DN "C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith".</span></span>


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



<span data-ttu-id="d165d-120">請注意， \<S\> 支援 "" 或 " \<I> " 和 " \<S\> "。</span><span class="sxs-lookup"><span data-stu-id="d165d-120">Be aware that "\<S\>" or "\<I>" and "\<S\>" are supported.</span></span> <span data-ttu-id="d165d-121">\<I\>不支援「」。</span><span class="sxs-lookup"><span data-stu-id="d165d-121">Having only "\<I\>" is not supported.</span></span> <span data-ttu-id="d165d-122">應用程式不應該修改 " \<I\> " 或 "" 內的值， \<S\> 因為不支援部分 DN 比對。</span><span class="sxs-lookup"><span data-stu-id="d165d-122">Applications should not modify the values within "\<I\>" or "\<S\>" because partial DN matching is not supported.</span></span>

<span data-ttu-id="d165d-123">若為外部 Kerberos 帳戶，值應為 Kerberos 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d165d-123">For external Kerberos accounts, the values should be the Kerberos account name.</span></span> <span data-ttu-id="d165d-124">Kerberos 封裝會使用下列語法： "Kerberos： MITaccountname"。</span><span class="sxs-lookup"><span data-stu-id="d165d-124">The Kerberos package uses the following syntax: "Kerberos:MITaccountname".</span></span> <span data-ttu-id="d165d-125">例如，以下是 Fabrikam.com 帳戶的值：</span><span class="sxs-lookup"><span data-stu-id="d165d-125">For example, the following is the value for an account at Fabrikam.com:</span></span>


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span data-ttu-id="d165d-126"><span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)</span><span class="sxs-lookup"><span data-stu-id="d165d-126"><span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-127">非複寫。</span><span class="sxs-lookup"><span data-stu-id="d165d-127">Non-replicated.</span></span> <span data-ttu-id="d165d-128">[**BadPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)屬性會指定使用者上次嘗試使用不正確的密碼登入帳戶的時間。</span><span class="sxs-lookup"><span data-stu-id="d165d-128">The [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) attribute specifies the last time the user attempted to log on to the account using an incorrect password.</span></span> <span data-ttu-id="d165d-129">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-129">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="d165d-130">這個屬性會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="d165d-130">This attribute is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="d165d-131">值為零表示最後一個錯誤的密碼時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="d165d-131">A value of zero means that the last bad password time is unknown.</span></span> <span data-ttu-id="d165d-132">若要取得使用者在網域中的上次錯誤密碼時間的準確值，您必須查詢網域中的每個網域控制站，並使用最大的值。</span><span class="sxs-lookup"><span data-stu-id="d165d-132">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried and the largest value should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-133"><span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)</span><span class="sxs-lookup"><span data-stu-id="d165d-133"><span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-134">非複寫。</span><span class="sxs-lookup"><span data-stu-id="d165d-134">Non-replicated.</span></span> <span data-ttu-id="d165d-135">[**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)屬性會指定使用者嘗試使用不正確的密碼登入帳戶的次數。</span><span class="sxs-lookup"><span data-stu-id="d165d-135">The [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) attribute specifies the number of times the user attempted to log on to the account using an incorrect password.</span></span> <span data-ttu-id="d165d-136">這個屬性會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="d165d-136">This attribute is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="d165d-137">值為0表示值不明。</span><span class="sxs-lookup"><span data-stu-id="d165d-137">A value of 0 indicates that the value is unknown.</span></span> <span data-ttu-id="d165d-138">若要取得使用者在網域中的錯誤密碼嘗試總數的精確值，必須查詢網域中的每個網域控制站，並使用值的總和。</span><span class="sxs-lookup"><span data-stu-id="d165d-138">To get an accurate value for the user's total bad password attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-139"><span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**字碼頁**](/windows/desktop/ADSchema/a-codepage)</span><span class="sxs-lookup"><span data-stu-id="d165d-139"><span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**codePage**](/windows/desktop/ADSchema/a-codepage)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-140">代碼 [**頁屬性會**](/windows/desktop/ADSchema/a-codepage) 指定使用者所選擇語言的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="d165d-140">The [**codePage**](/windows/desktop/ADSchema/a-codepage) attribute specifies the code page for the user's chosen language.</span></span> <span data-ttu-id="d165d-141">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="d165d-141">This value is not used by Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-142"><span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)</span><span class="sxs-lookup"><span data-stu-id="d165d-142"><span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-143">[**CountryCode**](/windows/desktop/ADSchema/a-countrycode)屬性會指定使用者語言的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-143">The [**countryCode**](/windows/desktop/ADSchema/a-countrycode) attribute specifies the country/region code for the user's language.</span></span> <span data-ttu-id="d165d-144">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="d165d-144">This value is not used by Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-145"><span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)</span><span class="sxs-lookup"><span data-stu-id="d165d-145"><span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-146">[**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory)屬性會指定使用者的主目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-146">The [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) attribute specifies the path of the home directory for the user.</span></span> <span data-ttu-id="d165d-147">字串可以是 null。</span><span class="sxs-lookup"><span data-stu-id="d165d-147">The string can be null.</span></span>

<span data-ttu-id="d165d-148">如果已設定 [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) 並指定磁碟機號， [**HOMEDIRECTORY**](/windows/desktop/ADSchema/a-homedirectory) 應該是 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-148">If [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) is set and specifies a drive letter, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) should be a UNC path.</span></span> <span data-ttu-id="d165d-149">路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d165d-149">The path must be a network UNC path of the form \\\\server\\share\\directory.</span></span> <span data-ttu-id="d165d-150">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="d165d-150">This value can be a null string.</span></span>

<span data-ttu-id="d165d-151">如果未設定 [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) ， [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) 應該是本機路徑，例如 C： \\ mylocaldir。</span><span class="sxs-lookup"><span data-stu-id="d165d-151">If [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) is not set, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) should be a local path, for example, C:\\mylocaldir.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-152"><span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)</span><span class="sxs-lookup"><span data-stu-id="d165d-152"><span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-153">[**HomeDrive**](/windows/desktop/ADSchema/a-homedrive)屬性會指定要對應 **homeDirectory** 所指定之 UNC 路徑的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="d165d-153">The [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) attribute specifies the drive letter to which to map the UNC path specified by **homeDirectory**.</span></span> <span data-ttu-id="d165d-154">磁碟機號必須以下列格式指定：</span><span class="sxs-lookup"><span data-stu-id="d165d-154">The drive letter must be specified in the following form:</span></span>


```C++
<drive letter>:
```



<span data-ttu-id="d165d-155">其中 " \<drive letter\> " 是要對應之磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="d165d-155">where "\<drive letter\>" is the letter of the drive to map.</span></span> <span data-ttu-id="d165d-156">例如：</span><span class="sxs-lookup"><span data-stu-id="d165d-156">For example:</span></span>


```C++
Z:
```



<span data-ttu-id="d165d-157">如果未設定此屬性， [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) 應該是本機路徑，例如 C： \\ mylocaldir。</span><span class="sxs-lookup"><span data-stu-id="d165d-157">If this attribute is not set, the [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) should be a local path, for example, C:\\mylocaldir.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-158"><span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)</span><span class="sxs-lookup"><span data-stu-id="d165d-158"><span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-159">非複寫。</span><span class="sxs-lookup"><span data-stu-id="d165d-159">Non-replicated.</span></span> <span data-ttu-id="d165d-160">[**LastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)屬性會指定上次發生登出的時間。</span><span class="sxs-lookup"><span data-stu-id="d165d-160">The [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) attribute specifies when the last logoff occurred.</span></span> <span data-ttu-id="d165d-161">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-161">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="d165d-162">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="d165d-162">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span> <span data-ttu-id="d165d-163">這個屬性會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="d165d-163">This attribute is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="d165d-164">值為零表示最後一次登出時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="d165d-164">A value of zero means that the last logoff time is unknown.</span></span> <span data-ttu-id="d165d-165">若要取得使用者在網域中上次登出的精確值，您必須查詢網域中的每個網域控制站，並使用最大的值。</span><span class="sxs-lookup"><span data-stu-id="d165d-165">To get an accurate value for the user's last logoff in the domain, each domain controller in the domain must be queried and the largest value should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-166"><span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)</span><span class="sxs-lookup"><span data-stu-id="d165d-166"><span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-167">非複寫。</span><span class="sxs-lookup"><span data-stu-id="d165d-167">Non-replicated.</span></span> <span data-ttu-id="d165d-168">[**LastLogon**](/windows/desktop/ADSchema/a-lastlogon)屬性會指定上次登入的時間。</span><span class="sxs-lookup"><span data-stu-id="d165d-168">The [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon) attribute specifies when the last logon occurred.</span></span> <span data-ttu-id="d165d-169">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-169">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="d165d-170">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="d165d-170">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span> <span data-ttu-id="d165d-171">這個屬性會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="d165d-171">This attribute is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="d165d-172">值為零表示最後一個登入時間未知。</span><span class="sxs-lookup"><span data-stu-id="d165d-172">A value of zero means that the last logon time is unknown.</span></span> <span data-ttu-id="d165d-173">若要取得使用者在網域中最後一次登入的精確值，您必須查詢網域中的每個網域控制站，並使用最大的值。</span><span class="sxs-lookup"><span data-stu-id="d165d-173">To get an accurate value for the user's last logon in the domain, each domain controller in the domain must be queried and the largest value should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-174"><span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)</span><span class="sxs-lookup"><span data-stu-id="d165d-174"><span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-175">[**LmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)屬性是區域網路管理員中使用者的密碼歷程記錄， (LM)  (OWF) 的單向格式。</span><span class="sxs-lookup"><span data-stu-id="d165d-175">The [**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) attribute is the password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="d165d-176">LM OWF 是用於與 LAN Manager 2.x 用戶端、Windows 95 和 Windows 98 的相容性。</span><span class="sxs-lookup"><span data-stu-id="d165d-176">The LM OWF is used for compatibility with LAN Manager 2.x clients, Windows 95, and Windows 98.</span></span> <span data-ttu-id="d165d-177">這個屬性僅供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="d165d-177">This attribute is used only by the operating system.</span></span> <span data-ttu-id="d165d-178">請注意，您無法從密碼的 OWF 形式衍生純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-178">Be aware that you cannot derive the plaintext password from the OWF form of the password.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-179"><span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)</span><span class="sxs-lookup"><span data-stu-id="d165d-179"><span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-180">非複寫。</span><span class="sxs-lookup"><span data-stu-id="d165d-180">Non-replicated.</span></span> <span data-ttu-id="d165d-181">[**LogonCount**](/windows/desktop/ADSchema/a-logoncount)屬性會計算使用者嘗試登入此帳戶的成功時間數目。</span><span class="sxs-lookup"><span data-stu-id="d165d-181">The [**logonCount**](/windows/desktop/ADSchema/a-logoncount) attribute counts the number of successful times that the user tried to log on to this account.</span></span> <span data-ttu-id="d165d-182">這個屬性會在網域中的每個網域控制站上進行維護。</span><span class="sxs-lookup"><span data-stu-id="d165d-182">This attribute is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="d165d-183">值為0表示值不明。</span><span class="sxs-lookup"><span data-stu-id="d165d-183">A value of 0 indicates that the value is unknown.</span></span> <span data-ttu-id="d165d-184">若要取得使用者在網域中成功登入嘗試總數的精確值，必須查詢網域中的每個網域控制站，並使用值的總和。</span><span class="sxs-lookup"><span data-stu-id="d165d-184">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-185"><span id="mail"></span><span id="MAIL"></span>[**郵件**](/windows/desktop/ADSchema/a-mail)</span><span class="sxs-lookup"><span data-stu-id="d165d-185"><span id="mail"></span><span id="MAIL"></span>[**mail**](/windows/desktop/ADSchema/a-mail)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-186">[**Mail**](/windows/desktop/ADSchema/a-mail)屬性是單一值屬性，其中包含使用者的 SMTP 位址，例如 " jeff@Fabrikam.com "。</span><span class="sxs-lookup"><span data-stu-id="d165d-186">The [**mail**](/windows/desktop/ADSchema/a-mail) attribute is a single-valued attribute that contains the SMTP address for the user, for example, "jeff@Fabrikam.com".</span></span>

</dd> <dt>

<span data-ttu-id="d165d-187"><span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)</span><span class="sxs-lookup"><span data-stu-id="d165d-187"><span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-188">[**MaxStorage**](/windows/desktop/ADSchema/a-maxstorage)屬性會指定使用者可使用的硬碟空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="d165d-188">The [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage) attribute specifies the maximum amount of hard-disk drive space that the user can use.</span></span> <span data-ttu-id="d165d-189">使用在 Lmaccess 中定義的「 **使用者 \_ MAXSTORAGE \_ 無限制** (，) 值來使用所有可用的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="d165d-189">Use the **USER\_MAXSTORAGE\_UNLIMITED** (defined in Lmaccess.h) value to use all available disk space.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-190"><span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)</span><span class="sxs-lookup"><span data-stu-id="d165d-190"><span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-191">[**MemberOf**](/windows/desktop/ADSchema/a-memberof)屬性是多重值的屬性，其中包含使用者是直接成員的群組，但主要群組除外，其由 [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)所代表。</span><span class="sxs-lookup"><span data-stu-id="d165d-191">The [**memberOf**](/windows/desktop/ADSchema/a-memberof) attribute is a multi-valued attribute that contains groups of which the user is a direct member, except for the primary group, which is represented by the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid).</span></span> <span data-ttu-id="d165d-192">群組成員資格相依于從中抓取此屬性 (DC) 的網域控制站：</span><span class="sxs-lookup"><span data-stu-id="d165d-192">Group membership is dependent on the domain controller (DC) from which this attribute is retrieved:</span></span>

-   <span data-ttu-id="d165d-193">在包含使用者之網域的 DC 中，使用者的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 是針對該網域中群組的成員資格完成的。不過， **memberOf** 不包含使用者在網域本機的成員資格以及其他網域中的全域群組。</span><span class="sxs-lookup"><span data-stu-id="d165d-193">At a DC for the domain that contains the user, [**memberOf**](/windows/desktop/ADSchema/a-memberof) for the user is complete with respect to membership for groups in that domain; however, **memberOf** does not contain the user's membership in domain local and global groups in other domains.</span></span>
-   <span data-ttu-id="d165d-194">在 GC 伺服器上，使用者的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 是針對所有通用群組成員資格完成的。</span><span class="sxs-lookup"><span data-stu-id="d165d-194">At a GC server, [**memberOf**](/windows/desktop/ADSchema/a-memberof) for the user is complete with respect to all universal group memberships.</span></span>

<span data-ttu-id="d165d-195">如果 DC 的這兩個條件都成立，則這兩組資料都會包含在 [**memberOf**](/windows/desktop/ADSchema/a-memberof)中。</span><span class="sxs-lookup"><span data-stu-id="d165d-195">If both conditions are true for the DC, both sets of data are contained in [**memberOf**](/windows/desktop/ADSchema/a-memberof).</span></span>

<span data-ttu-id="d165d-196">請注意，這個屬性會列出成員屬性中包含使用者的群組，而不包含嵌套前置項的遞迴清單。</span><span class="sxs-lookup"><span data-stu-id="d165d-196">Be aware that this attribute lists the groups that contain the user in their member attribute—it does not contain the recursive list of nested predecessors.</span></span> <span data-ttu-id="d165d-197">例如，如果 user O 是群組 C 的成員，而群組 B 是嵌套在群組 A 中，使用者 O 的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性會列出群組 C 和群組 b，但不會列出群組 a。</span><span class="sxs-lookup"><span data-stu-id="d165d-197">For example, if user O is a member of group C and group B and group B were nested in group A, the [**memberOf**](/windows/desktop/ADSchema/a-memberof) attribute of user O would list group C and group B, but not group A.</span></span>

<span data-ttu-id="d165d-198">這個屬性不會儲存，而是計算的後置連結屬性。</span><span class="sxs-lookup"><span data-stu-id="d165d-198">This attribute is not stored—it is a computed back-link attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-199"><span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)</span><span class="sxs-lookup"><span data-stu-id="d165d-199"><span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-200">[**NtPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)屬性是使用者的密碼歷程記錄，以 Windows NT 的單向格式 (OWF) 。</span><span class="sxs-lookup"><span data-stu-id="d165d-200">The [**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) attribute is the password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="d165d-201">Windows 2000 使用 Windows NT OWF。</span><span class="sxs-lookup"><span data-stu-id="d165d-201">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="d165d-202">這個屬性僅供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="d165d-202">This attribute is used only by the operating system.</span></span> <span data-ttu-id="d165d-203">請注意，您無法從密碼的 OWF 形式衍生純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-203">Be aware that you cannot derive the plaintext password back from the OWF form of the password.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-204"><span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)</span><span class="sxs-lookup"><span data-stu-id="d165d-204"><span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-205">[**OtherMailbox**](/windows/desktop/ADSchema/a-othermailbox)屬性是多重值屬性，其中包含表單中其他的其他郵寄地址，例如 "CCMAIL： JeffSmith"。</span><span class="sxs-lookup"><span data-stu-id="d165d-205">The [**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox) attribute is a multi-valued attribute that contains other additional mail addresses in a form, for example, "CCMAIL: JeffSmith".</span></span>

</dd> <dt>

<span data-ttu-id="d165d-206"><span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)</span><span class="sxs-lookup"><span data-stu-id="d165d-206"><span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-207">密碼到期日不是使用者物件上的屬性。</span><span class="sxs-lookup"><span data-stu-id="d165d-207">The password expiration date is not an attribute on the user object.</span></span> <span data-ttu-id="d165d-208">它是以使用者的 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) 與使用者網域 [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) 的總和為基礎的計算值。</span><span class="sxs-lookup"><span data-stu-id="d165d-208">It is a calculated value based on the sum of [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) for the user and [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) of the user's domain.</span></span> <span data-ttu-id="d165d-209">若要取得密碼到期日，請取得 [**IADsUser. PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d165d-209">To get the password expiration date, get the [**IADsUser.PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) property.</span></span> <span data-ttu-id="d165d-210">您無法為使用者修改此屬性;請改為設定 [**IADsDomain MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) 屬性，以變更網域的設定。</span><span class="sxs-lookup"><span data-stu-id="d165d-210">You cannot modify this attribute for a user; instead, set the [**IADsDomain.MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) property to change the setting for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-211"><span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)</span><span class="sxs-lookup"><span data-stu-id="d165d-211"><span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-212">[**PrimaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)屬性是單一值屬性，其中包含做為物件之主要群組的群組 [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) 。</span><span class="sxs-lookup"><span data-stu-id="d165d-212">The [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute is a single-valued attribute that contains the [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the group that is the primary group of the object.</span></span> <span data-ttu-id="d165d-213">物件的主要群組未包含在 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="d165d-213">The primary group of the object is not included in the [**memberOf**](/windows/desktop/ADSchema/a-memberof) attribute.</span></span> <span data-ttu-id="d165d-214">例如，根據預設，使用者物件的主要群組是 Domain Users 群組的 **primaryGroupToken** ，但是 domain users 群組不是 user 物件的 **memberOf** 屬性的一部分。</span><span class="sxs-lookup"><span data-stu-id="d165d-214">For example, by default, the primary group of a user object is the **primaryGroupToken** of the Domain Users group, but the Domain Users group is not part of the user object's **memberOf** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-215"><span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)</span><span class="sxs-lookup"><span data-stu-id="d165d-215"><span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-216">[**ProfilePath**](/windows/desktop/ADSchema/a-profilepath)屬性會指定使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-216">The [**profilePath**](/windows/desktop/ADSchema/a-profilepath) attribute specifies a path to the user's profile.</span></span> <span data-ttu-id="d165d-217">這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-217">This value can be a null string, a local absolute path, or a UNC path.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-218"><span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)</span><span class="sxs-lookup"><span data-stu-id="d165d-218"><span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-219">[**PwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)屬性會指定上次變更密碼的時間。</span><span class="sxs-lookup"><span data-stu-id="d165d-219">The [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) attribute specifies when the password was last changed.</span></span> <span data-ttu-id="d165d-220">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-220">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>

<span data-ttu-id="d165d-221">系統會使用此屬性的值和包含使用者物件之網域的 [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) 屬性，來計算密碼到期日。</span><span class="sxs-lookup"><span data-stu-id="d165d-221">The system uses the value of this attribute and the [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) attribute of the domain that contains the user object to calculate the password expiration date.</span></span> <span data-ttu-id="d165d-222">也就是使用者網域的使用者和 **maxPwdAge** 的 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)總和。</span><span class="sxs-lookup"><span data-stu-id="d165d-222">That is, the sum of [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) for the user and **maxPwdAge** of the user's domain.</span></span>

<span data-ttu-id="d165d-223">這個屬性會控制使用者下次登入時是否必須變更密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-223">This attribute controls whether the user must change the password when the user logs on next.</span></span> <span data-ttu-id="d165d-224">如果 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) 為零（預設值），則使用者必須在下次登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-224">If [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) is zero, the default, the user must change the password at next logon.</span></span> <span data-ttu-id="d165d-225">值-1 表示使用者不需要在下次登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-225">The value -1 indicates that the user is not required to change the password at next logon.</span></span> <span data-ttu-id="d165d-226">系統會在使用者設定密碼之後，將此值設定為-1。</span><span class="sxs-lookup"><span data-stu-id="d165d-226">The system sets this value to -1 after user has set the password.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-227"><span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)</span><span class="sxs-lookup"><span data-stu-id="d165d-227"><span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-228">[**SAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)屬性會指定代表帳戶類型的整數。</span><span class="sxs-lookup"><span data-stu-id="d165d-228">The [**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) attribute specifies an integer that represents the account type.</span></span> <span data-ttu-id="d165d-229">這是在建立物件時由作業系統設定。</span><span class="sxs-lookup"><span data-stu-id="d165d-229">This is set by the operating system when the object is created.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-230"><span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)</span><span class="sxs-lookup"><span data-stu-id="d165d-230"><span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-231">[**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath)屬性會指定使用者的登入腳本、.cmd、.exe 或 .bat 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-231">The [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath) attribute specifies the path of the user's logon script, .cmd, .exe, or .bat file.</span></span> <span data-ttu-id="d165d-232">字串可以是 null。</span><span class="sxs-lookup"><span data-stu-id="d165d-232">The string can be null.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-233"><span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)</span><span class="sxs-lookup"><span data-stu-id="d165d-233"><span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-234">[**UnicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)屬性是使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-234">The [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) attribute is the user password.</span></span>

<span data-ttu-id="d165d-235">若要設定使用者密碼，請使用 [**IADsUser**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) 方法，如果您的腳本或應用程式可讓使用者變更自己的密碼，或 [**IADsUser SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 方法（如果您的腳本或應用程式允許系統管理員重設密碼）。</span><span class="sxs-lookup"><span data-stu-id="d165d-235">To set the user password, use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) method, if your script or application enables the user to change his/her own password, or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method, if your script or application is allowing an administrator to reset a password.</span></span>

<span data-ttu-id="d165d-236">Windows NT 單向格式的使用者密碼 (OWF) 。</span><span class="sxs-lookup"><span data-stu-id="d165d-236">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="d165d-237">Windows 2000 使用 Windows NT OWF。</span><span class="sxs-lookup"><span data-stu-id="d165d-237">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="d165d-238">這個屬性僅供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="d165d-238">This attribute is used only by operating system.</span></span> <span data-ttu-id="d165d-239">請注意，您無法從密碼的 OWF 形式衍生純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-239">Be aware that you cannot derive the plaintext password back from the OWF form of the password.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-240"><span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)</span><span class="sxs-lookup"><span data-stu-id="d165d-240"><span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-241">[**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)屬性會指定旗標，以控制使用者的密碼、鎖定、停用/啟用、腳本和主目錄行為。</span><span class="sxs-lookup"><span data-stu-id="d165d-241">The [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) attribute specifies flags that control password, lockout, disable/enable, script, and home directory behavior for the user.</span></span> <span data-ttu-id="d165d-242">這個屬性也包含一個旗標，指出物件的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d165d-242">This attribute also contains a flag that indicates the account type of the object.</span></span> <span data-ttu-id="d165d-243">使用者物件通常會 \_ 設定 UF 一般 \_ 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-243">The user object usually has the UF\_NORMAL\_ACCOUNT set.</span></span>

<span data-ttu-id="d165d-244">下列旗標定義于 Lmaccess 中。</span><span class="sxs-lookup"><span data-stu-id="d165d-244">The following flags are defined in Lmaccess.h.</span></span>



| <span data-ttu-id="d165d-245">旗標</span><span class="sxs-lookup"><span data-stu-id="d165d-245">Flag</span></span>                     | <span data-ttu-id="d165d-246">描述</span><span class="sxs-lookup"><span data-stu-id="d165d-246">Description</span></span>                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d165d-247">UF \_ 腳本</span><span class="sxs-lookup"><span data-stu-id="d165d-247">UF\_SCRIPT</span></span>               | <span data-ttu-id="d165d-248">執行的登入腳本。</span><span class="sxs-lookup"><span data-stu-id="d165d-248">The logon script executed.</span></span> <span data-ttu-id="d165d-249">必須為 LAN Manager 2.0 或 Windows NT 設定此值。</span><span class="sxs-lookup"><span data-stu-id="d165d-249">This value must be set for LAN Manager 2.0 or Windows NT.</span></span>                                                                             |
| <span data-ttu-id="d165d-250">UF \_ ACCOUNTDISABLE</span><span class="sxs-lookup"><span data-stu-id="d165d-250">UF\_ACCOUNTDISABLE</span></span>       | <span data-ttu-id="d165d-251">使用者帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="d165d-251">The user account is disabled.</span></span>                                                                                                                                    |
| <span data-ttu-id="d165d-252">\_需要 UF HOMEDIR \_</span><span class="sxs-lookup"><span data-stu-id="d165d-252">UF\_HOMEDIR\_REQUIRED</span></span>    | <span data-ttu-id="d165d-253">需要主目錄。</span><span class="sxs-lookup"><span data-stu-id="d165d-253">The home directory is required.</span></span> <span data-ttu-id="d165d-254">在 Windows NT 和 Windows 2000 中，會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="d165d-254">This value is ignored in Windows NT and Windows 2000.</span></span>                                                                            |
| <span data-ttu-id="d165d-255">UF \_ PASSWD \_ NOTREQD</span><span class="sxs-lookup"><span data-stu-id="d165d-255">UF\_PASSWD\_NOTREQD</span></span>      | <span data-ttu-id="d165d-256">不需要密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-256">No password is required.</span></span>                                                                                                                                         |
| <span data-ttu-id="d165d-257">無法 \_ 變更 UF 密碼 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d165d-257">UF\_PASSWD\_CANT\_CHANGE</span></span> | <span data-ttu-id="d165d-258">使用者無法變更密碼。</span><span class="sxs-lookup"><span data-stu-id="d165d-258">The user cannot change the password.</span></span>                                                                                                                             |
| <span data-ttu-id="d165d-259">UF \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="d165d-259">UF\_LOCKOUT</span></span>              | <span data-ttu-id="d165d-260">帳戶目前已鎖定。</span><span class="sxs-lookup"><span data-stu-id="d165d-260">The account is currently locked.</span></span> <span data-ttu-id="d165d-261">您可以清除此值以解除鎖定先前鎖定的帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-261">This value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="d165d-262">此值不能用來鎖定先前鎖定的帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-262">This value cannot be used to lock a previously locked account.</span></span> |
| <span data-ttu-id="d165d-263">UF 不會讓 \_ \_ \_ PASSWD 過期</span><span class="sxs-lookup"><span data-stu-id="d165d-263">UF\_DONT\_EXPIRE\_PASSWD</span></span> | <span data-ttu-id="d165d-264">代表密碼，此密碼永遠不會在帳戶上到期。</span><span class="sxs-lookup"><span data-stu-id="d165d-264">Represents the password, which should never expire on the account.</span></span>                                                                                               |



 

<span data-ttu-id="d165d-265">下列旗標描述帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d165d-265">The following flags describe the account type.</span></span> <span data-ttu-id="d165d-266">只能設定一個值。</span><span class="sxs-lookup"><span data-stu-id="d165d-266">Only one value can be set.</span></span> <span data-ttu-id="d165d-267">您無法變更帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d165d-267">You cannot change the account type.</span></span>



| <span data-ttu-id="d165d-268">旗標</span><span class="sxs-lookup"><span data-stu-id="d165d-268">Flag</span></span>                            | <span data-ttu-id="d165d-269">描述</span><span class="sxs-lookup"><span data-stu-id="d165d-269">Description</span></span>                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d165d-270">UF \_ 一般 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="d165d-270">UF\_NORMAL\_ACCOUNT</span></span>             | <span data-ttu-id="d165d-271">這是代表一般使用者的預設帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d165d-271">This is a default account type that represents a typical user.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d165d-272">UF \_ 暫存 \_ 重複 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="d165d-272">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>    | <span data-ttu-id="d165d-273">這是主要帳戶位於另一個網域的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-273">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="d165d-274">此帳戶可讓使用者存取此網域，但不提供任何信任此網域的網域。</span><span class="sxs-lookup"><span data-stu-id="d165d-274">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="d165d-275">使用者管理員會將此帳戶類型稱為本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-275">The User Manager refers to this account type as a local user account.</span></span> |
| <span data-ttu-id="d165d-276">UF \_ 工作站 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="d165d-276">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span> | <span data-ttu-id="d165d-277">這是 Windows NT 工作站/Windows 2000 Professional 或 Windows NT Server/Windows 2000 伺服器（此網域的成員）的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-277">This is a computer account for a Windows NT Workstation/Windows 2000 Professional or Windows NT Server/Windows 2000 Server that is a member of this domain.</span></span>                                                                                     |
| <span data-ttu-id="d165d-278">UF \_ 伺服器 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="d165d-278">UF\_SERVER\_TRUST\_ACCOUNT</span></span>      | <span data-ttu-id="d165d-279">這是屬於此網域成員 Windows NT 備份網域控制站的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-279">This is a computer account for a Windows NT Backup Domain Controller that is a member of this domain.</span></span>                                                                                                                                           |
| <span data-ttu-id="d165d-280">每個 UF \_ 域 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="d165d-280">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span> | <span data-ttu-id="d165d-281">這是允許信任其他網域的 Windows NT 網域的帳戶。</span><span class="sxs-lookup"><span data-stu-id="d165d-281">This is a permit to trust account for a Windows NT domain that trusts other domains.</span></span>                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d165d-282"><span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)</span><span class="sxs-lookup"><span data-stu-id="d165d-282"><span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-283">[**UserCertificate**](/windows/desktop/ADSchema/a-usercertificate)屬性是多重值屬性，其中包含發給使用者的 DER 編碼 X509v3 憑證。</span><span class="sxs-lookup"><span data-stu-id="d165d-283">The [**userCertificate**](/windows/desktop/ADSchema/a-usercertificate) attribute is a multi-valued attribute that contains the DER-encoded X509v3 certificates issued to the user.</span></span> <span data-ttu-id="d165d-284">請注意，此屬性包含由 Microsoft 憑證服務發給此使用者的公開金鑰憑證。</span><span class="sxs-lookup"><span data-stu-id="d165d-284">Be aware that this attribute contains the public key certificates issued to this user by Microsoft Certificate Service.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-285"><span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)</span><span class="sxs-lookup"><span data-stu-id="d165d-285"><span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-286">[**UserSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)屬性會指定使用者的 [共用文件] 資料夾的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="d165d-286">The [**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) attribute specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="d165d-287">路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d165d-287">The path must be a network UNC path of the form \\\\server\\share\\directory.</span></span> <span data-ttu-id="d165d-288">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="d165d-288">This value can be a null string.</span></span>

</dd> <dt>

<span data-ttu-id="d165d-289"><span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)</span><span class="sxs-lookup"><span data-stu-id="d165d-289"><span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)</span></span>
</dt> <dd>

<span data-ttu-id="d165d-290">[**UserWorkstations**](/windows/desktop/ADSchema/a-userworkstations)屬性是單一值屬性，其中包含使用者可以登入之工作站的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="d165d-290">The [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) attribute is a single-valued attribute that contains the NetBIOS names of the workstations from which the user can log on to.</span></span> <span data-ttu-id="d165d-291">每個 NetBIOS 名稱會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="d165d-291">Each NetBIOS name is separated by a comma.</span></span>

<span data-ttu-id="d165d-292">如果未設定任何值，則表示沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="d165d-292">If no values are set, this indicates that there is no restriction.</span></span> <span data-ttu-id="d165d-293">若要停用此帳戶的所有工作站登入，請 \_ 在 [ [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) ] 屬性中，將 [ACCOUNTDISABLE]) 中定義的 [UF] 值設定 (。</span><span class="sxs-lookup"><span data-stu-id="d165d-293">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE value (defined in Lmaccess.h) in [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) attribute.</span></span>

</dd> </dl>

 

 

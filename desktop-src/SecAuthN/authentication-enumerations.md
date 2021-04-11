---
description: 列出驗證 Api 中使用的列舉。
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: 驗證列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690144"
---
# <a name="authentication-enumerations"></a><span data-ttu-id="da046-103">驗證列舉</span><span class="sxs-lookup"><span data-stu-id="da046-103">Authentication Enumerations</span></span>

<span data-ttu-id="da046-104">驗證列舉會根據使用方式進行分類，如下所示：</span><span class="sxs-lookup"><span data-stu-id="da046-104">Authentication enumerations are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="da046-105">認證管理列舉</span><span class="sxs-lookup"><span data-stu-id="da046-105">Credentials Management Enumerations</span></span>](#credentials-management-enumerations)
-   [<span data-ttu-id="da046-106">LSA 列舉</span><span class="sxs-lookup"><span data-stu-id="da046-106">LSA Enumerations</span></span>](#lsa-enumerations)
-   [<span data-ttu-id="da046-107">網路提供者列舉</span><span class="sxs-lookup"><span data-stu-id="da046-107">Network Provider Enumerations</span></span>](#network-provider-enumerations)
-   [<span data-ttu-id="da046-108">認證安全性支援提供者 (CredSSP) 列舉</span><span class="sxs-lookup"><span data-stu-id="da046-108">Credential Security Support Provider (CredSSP) Enumerations</span></span>](#credential-security-support-provider-credssp-enumerations)
-   [<span data-ttu-id="da046-109">其他列舉</span><span class="sxs-lookup"><span data-stu-id="da046-109">Other Enumerations</span></span>](#other-enumerations)

## <a name="credentials-management-enumerations"></a><span data-ttu-id="da046-110">認證管理列舉</span><span class="sxs-lookup"><span data-stu-id="da046-110">Credentials Management Enumerations</span></span>

<span data-ttu-id="da046-111">認證管理會使用下列列舉。</span><span class="sxs-lookup"><span data-stu-id="da046-111">Credentials Management uses the following enumerations.</span></span>



| <span data-ttu-id="da046-112">列舉型別</span><span class="sxs-lookup"><span data-stu-id="da046-112">Enumeration</span></span>                                            | <span data-ttu-id="da046-113">描述</span><span class="sxs-lookup"><span data-stu-id="da046-113">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da046-114">**認證 \_ 封送處理 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-114">**CRED\_MARSHAL\_TYPE**</span></span>](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | <span data-ttu-id="da046-115">包含可由 [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) 封送處理或由 [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)取消封送處理的認證類型。</span><span class="sxs-lookup"><span data-stu-id="da046-115">Contains the types of credential that can be marshaled by [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) or unmarshaled by [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).</span></span><br/> |
| [<span data-ttu-id="da046-116">**認證 \_ 保護 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-116">**CRED\_PROTECTION\_TYPE**</span></span>](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | <span data-ttu-id="da046-117">指定在使用 [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) 函式時，用來加密認證的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="da046-117">Specifies the security context in which credentials are encrypted when using the [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) function.</span></span><br/>                                                                  |



 

## <a name="lsa-enumerations"></a><span data-ttu-id="da046-118">LSA 列舉</span><span class="sxs-lookup"><span data-stu-id="da046-118">LSA Enumerations</span></span>

<span data-ttu-id="da046-119">LSA 使用下列列舉。</span><span class="sxs-lookup"><span data-stu-id="da046-119">LSA uses the following enumerations.</span></span>



| <span data-ttu-id="da046-120">列舉型別</span><span class="sxs-lookup"><span data-stu-id="da046-120">Enumeration</span></span>                                                                                   | <span data-ttu-id="da046-121">描述</span><span class="sxs-lookup"><span data-stu-id="da046-121">Description</span></span>                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da046-122">**KERB \_ 登入 \_ 提交 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-122">**KERB\_LOGON\_SUBMIT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | <span data-ttu-id="da046-123">列出所要求的登入類型。</span><span class="sxs-lookup"><span data-stu-id="da046-123">Lists the type of logon being requested.</span></span><br/>                                                                                                                                                                                                                  |
| [<span data-ttu-id="da046-124">**KERB \_ 設定檔 \_ 緩衝區 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-124">**KERB\_PROFILE\_BUFFER\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | <span data-ttu-id="da046-125">列出傳回的登入配置檔案類型。</span><span class="sxs-lookup"><span data-stu-id="da046-125">Lists the type of logon profile returned.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="da046-126">**KERB \_ 通訊協定 \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-126">**KERB\_PROTOCOL\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | <span data-ttu-id="da046-127">列出可透過呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)傳送至 [*Kerberos*](/windows/desktop/SecGloss/k-gly)驗證套件的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="da046-127">Lists the types of messages which can be sent to the [*Kerberos*](/windows/desktop/SecGloss/k-gly) authentication package by calling [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).</span></span><br/> |
| [<span data-ttu-id="da046-128">**LSA \_ 樹系 \_ 信任 \_ 衝突 \_ 記錄 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-128">**LSA\_FOREST\_TRUST\_COLLISION\_RECORD\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | <span data-ttu-id="da046-129">定義 LSA 樹系信任記錄之間可能發生的衝突類型。</span><span class="sxs-lookup"><span data-stu-id="da046-129">Defines the types of collision that can occur between LSA forest trust records.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="da046-130">**LSA \_ 樹系 \_ 信任 \_ 記錄 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-130">**LSA\_FOREST\_TRUST\_RECORD\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | <span data-ttu-id="da046-131">定義 LSA 樹系信任記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="da046-131">Defines the type of an LSA forest trust record.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="da046-132">**LSA \_ TOKEN \_ 資訊 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-132">**LSA\_TOKEN\_INFORMATION\_TYPE**</span></span>](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | <span data-ttu-id="da046-133">指定可包含在登入權杖中的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="da046-133">Specifies the levels of information that can be included in a logon token.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="da046-134">**MSV1 \_ 0 \_ 登入 \_ 提交 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-134">**MSV1\_0\_LOGON\_SUBMIT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | <span data-ttu-id="da046-135">列出所要求的登入類型。</span><span class="sxs-lookup"><span data-stu-id="da046-135">Lists the kind of logon being requested.</span></span><br/>                                                                                                                                                                                                                  |
| [<span data-ttu-id="da046-136">**MSV1 \_ 0 \_ 設定檔 \_ 緩衝區 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-136">**MSV1\_0\_PROFILE\_BUFFER\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | <span data-ttu-id="da046-137">列出傳回的登入配置檔案類型。</span><span class="sxs-lookup"><span data-stu-id="da046-137">Lists the kind of logon profile returned.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="da046-138">**MSV1 \_ 0 \_ 通訊協定 \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-138">**MSV1\_0\_PROTOCOL\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | <span data-ttu-id="da046-139">列出可透過呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)傳送至 [MSV1 \_ 0 驗證套件](msv1-0-authentication-package.md)的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="da046-139">Lists the types of messages which can be sent to the [MSV1\_0 Authentication Package](msv1-0-authentication-package.md) by calling [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).</span></span><br/>                                                 |
| [<span data-ttu-id="da046-140">**原則 \_ 網域 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="da046-140">**POLICY\_DOMAIN\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | <span data-ttu-id="da046-141">定義原則網域資訊的類型。</span><span class="sxs-lookup"><span data-stu-id="da046-141">Defines the type of policy domain information.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="da046-142">**安全性 \_ 登入 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-142">**SECURITY\_LOGON\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | <span data-ttu-id="da046-143">指出登入處理常式要求的登入類型。</span><span class="sxs-lookup"><span data-stu-id="da046-143">Indicates the type of logon requested by a logon process.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a><span data-ttu-id="da046-144">網路提供者列舉</span><span class="sxs-lookup"><span data-stu-id="da046-144">Network Provider Enumerations</span></span>

<span data-ttu-id="da046-145">網路提供者會使用下列列舉。</span><span class="sxs-lookup"><span data-stu-id="da046-145">Network Provider uses the following enumerations.</span></span>



| <span data-ttu-id="da046-146">列舉型別</span><span class="sxs-lookup"><span data-stu-id="da046-146">Enumeration</span></span>                                                                       | <span data-ttu-id="da046-147">描述</span><span class="sxs-lookup"><span data-stu-id="da046-147">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da046-148">**SECPKG \_ 擴充的 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="da046-148">**SECPKG\_EXTENDED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | <span data-ttu-id="da046-149">列舉類型，指定要設定或針對 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)取得的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="da046-149">Enumeration type that specifies the type of information to set or get for a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span><br/> |
| [<span data-ttu-id="da046-150">**SECPKG \_ 名稱 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-150">**SECPKG\_NAME\_TYPE**</span></span>](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | <span data-ttu-id="da046-151">列舉值，指定為帳戶指定的名稱類型。</span><span class="sxs-lookup"><span data-stu-id="da046-151">Enumeration value that specifies the type of name specified for an account.</span></span><br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a><span data-ttu-id="da046-152">認證安全性支援提供者 (CredSSP) 列舉</span><span class="sxs-lookup"><span data-stu-id="da046-152">Credential Security Support Provider (CredSSP) Enumerations</span></span>

<span data-ttu-id="da046-153">CredSSP 使用下列列舉。</span><span class="sxs-lookup"><span data-stu-id="da046-153">CredSSP uses the following enumerations.</span></span>



| <span data-ttu-id="da046-154">列舉型別</span><span class="sxs-lookup"><span data-stu-id="da046-154">Enumeration</span></span>                                          | <span data-ttu-id="da046-155">描述</span><span class="sxs-lookup"><span data-stu-id="da046-155">Description</span></span>                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da046-156">**CREDSPP \_ 提交 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-156">**CREDSPP\_SUBMIT\_TYPE**</span></span>](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | <span data-ttu-id="da046-157">指定 [**CREDSSP \_**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) 認證結構所指定的認證類型。</span><span class="sxs-lookup"><span data-stu-id="da046-157">Specifies the type of credentials specified by a [**CREDSSP\_CRED**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) structure.</span></span><br/> |



 

## <a name="other-enumerations"></a><span data-ttu-id="da046-158">其他列舉</span><span class="sxs-lookup"><span data-stu-id="da046-158">Other Enumerations</span></span>

<span data-ttu-id="da046-159">以下是驗證所使用的其他列舉。</span><span class="sxs-lookup"><span data-stu-id="da046-159">Here are the other enumerations used by Authentication.</span></span>



| <span data-ttu-id="da046-160">列舉型別</span><span class="sxs-lookup"><span data-stu-id="da046-160">Enumeration</span></span>                                                   | <span data-ttu-id="da046-161">描述</span><span class="sxs-lookup"><span data-stu-id="da046-161">Description</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da046-162">**身分識別 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-162">**IDENTITY\_TYPE**</span></span>](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | <span data-ttu-id="da046-163">指定要列舉的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="da046-163">Specifies the type of identities to enumerate.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="da046-164">**PKU2U \_ 登入 \_ 提交 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da046-164">**PKU2U\_LOGON\_SUBMIT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | <span data-ttu-id="da046-165">指出傳入 [**PKU2U \_ 憑證 \_ S4U \_ 登**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) 入結構的登入訊息類型。</span><span class="sxs-lookup"><span data-stu-id="da046-165">Indicates the type of logon message passed in a [**PKU2U\_CERTIFICATE\_S4U\_LOGON**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) structure.</span></span><br/>                                                                                |
| [<span data-ttu-id="da046-166">**SECPKG \_ ATTR \_ LCT \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="da046-166">**SECPKG\_ATTR\_LCT\_STATUS**</span></span>](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | <span data-ttu-id="da046-167">指出最近呼叫 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數的權杖是否為用戶端的最後一個 token。</span><span class="sxs-lookup"><span data-stu-id="da046-167">Indicates whether the token from the most recent call to the [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function is the last token from the client.</span></span><br/>                               |
| [<span data-ttu-id="da046-168">**SECPKG \_ 認證 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="da046-168">**SECPKG\_CRED\_CLASS**</span></span>](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | <span data-ttu-id="da046-169">指出用戶端內容中使用的認證類型。</span><span class="sxs-lookup"><span data-stu-id="da046-169">Indicates the type of credential used in a client context.</span></span> <span data-ttu-id="da046-170">[**SECPKG 認證 \_ \_ 類別**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)列舉用於 [**SecPkgCoNtext \_ CredInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo)結構中。</span><span class="sxs-lookup"><span data-stu-id="da046-170">The [**SECPKG\_CRED\_CLASS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) enumeration is used in the [**SecPkgContext\_CredInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) structure.</span></span><br/> |



 

 


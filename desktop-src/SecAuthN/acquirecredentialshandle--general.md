---
description: 取得安全性主體預先存在的認證控制碼。
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: 'AcquireCredentialsHandle (一般) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975223"
---
# <a name="acquirecredentialshandle-general-function"></a><span data-ttu-id="f7348-103">AcquireCredentialsHandle (一般) 函數</span><span class="sxs-lookup"><span data-stu-id="f7348-103">AcquireCredentialsHandle (General) function</span></span>

<span data-ttu-id="f7348-104">**AcquireCredentialsHandle (General)** 函式會取得 [*安全性主體*](../secgloss/s-gly.md)預先存在的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-104">The **AcquireCredentialsHandle (General)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f7348-105">[**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md)和 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md)函式需要此控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-105">This handle is required by the [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) and [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) functions.</span></span> <span data-ttu-id="f7348-106">這些可以是預先存在的認證，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-106">These can be either preexisting credentials, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="f7348-107">這不是「登入網路」，也不代表認證的收集。</span><span class="sxs-lookup"><span data-stu-id="f7348-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

<span data-ttu-id="f7348-108">如需有關使用此函式搭配特定 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="f7348-108">For information about using this function with a specific [*security support provider*](../secgloss/s-gly.md) (SSP), see the following topics.</span></span>



| <span data-ttu-id="f7348-109">主題</span><span class="sxs-lookup"><span data-stu-id="f7348-109">Topic</span></span>                                                                                           | <span data-ttu-id="f7348-110">描述</span><span class="sxs-lookup"><span data-stu-id="f7348-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7348-111">**AcquireCredentialsHandle (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="f7348-111">**AcquireCredentialsHandle (CredSSP)**</span></span>](acquirecredentialshandle--credssp.md)<br/>     | <span data-ttu-id="f7348-112">取得安全性主體的預先存在認證的控制碼，該安全性主體使用 (CredSSP) 的認證安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="f7348-112">Acquires a handle to preexisting credentials of a security principal that is using Credential Security Support Provider (CredSSP).</span></span><br/> |
| [<span data-ttu-id="f7348-113">**AcquireCredentialsHandle (摘要)**</span><span class="sxs-lookup"><span data-stu-id="f7348-113">**AcquireCredentialsHandle (Digest)**</span></span>](acquirecredentialshandle--digest.md)<br/>       | <span data-ttu-id="f7348-114">取得使用摘要之安全性主體預先存在認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-114">Acquires a handle to preexisting credentials of a security principal that is using Digest.</span></span><br/>                                         |
| [<span data-ttu-id="f7348-115">**AcquireCredentialsHandle (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="f7348-115">**AcquireCredentialsHandle (Kerberos)**</span></span>](acquirecredentialshandle--kerberos.md)<br/>   | <span data-ttu-id="f7348-116">取得使用 Kerberos 之安全性主體預先存在認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-116">Acquires a handle to preexisting credentials of a security principal that is using Kerberos.</span></span><br/>                                       |
| [<span data-ttu-id="f7348-117">**AcquireCredentialsHandle (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="f7348-117">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)<br/> | <span data-ttu-id="f7348-118">取得使用 Negotiate 之安全性主體預先存在認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-118">Acquires a handle to preexisting credentials of a security principal that is using Negotiate.</span></span><br/>                                      |
| [<span data-ttu-id="f7348-119">**AcquireCredentialsHandle (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="f7348-119">**AcquireCredentialsHandle (NTLM)**</span></span>](acquirecredentialshandle--ntlm.md)<br/>           | <span data-ttu-id="f7348-120">取得使用 NTLM 之安全性主體預先存在認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-120">Acquires a handle to preexisting credentials of a security principal that is using NTLM.</span></span><br/>                                           |
| [<span data-ttu-id="f7348-121">**AcquireCredentialsHandle (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="f7348-121">**AcquireCredentialsHandle (Schannel)**</span></span>](acquirecredentialshandle--schannel.md)<br/>   | <span data-ttu-id="f7348-122">取得使用 Schannel 之安全性主體的預先存在認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-122">Acquires a handle to preexisting credentials of a security principal that is using Schannel.</span></span><br/>                                       |



 

## <a name="syntax"></a><span data-ttu-id="f7348-123">語法</span><span class="sxs-lookup"><span data-stu-id="f7348-123">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="f7348-124">參數</span><span class="sxs-lookup"><span data-stu-id="f7348-124">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7348-125">*pszPrincipal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-125">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-126">以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7348-126">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="f7348-127">使用摘要 SSP 時，此參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f7348-127">When using the Digest SSP, this parameter is optional.</span></span>

<span data-ttu-id="f7348-128">使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-128">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="f7348-129">如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7348-129">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="f7348-130">Null 字串表示進程需要在其執行 [*安全性內容*](../secgloss/s-gly.md) 之使用者的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-130">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="f7348-131">*pszPackage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-131">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-132">以 null 結束的字串指標，指定將使用這些認證之 [*安全性封裝*](../secgloss/s-gly.md) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7348-132">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="f7348-133">這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的 [*安全性封裝*](../secgloss/s-gly.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="f7348-133">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="f7348-134">建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (一般)**](querycontextattributes--general.md) ，並將 *ULATTRIBUTE* 設定為 SECPKG \_ ATTR \_ 封裝 \_ 資訊，以傳回使用中 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7348-134">After a context is established, [**QueryContextAttributes (General)**](querycontextattributes--general.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="f7348-135">使用摘要 SSP 時，請將此參數設定為 WDIGEST \_ SP \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="f7348-135">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

<span data-ttu-id="f7348-136">使用 Schannel SSP 時，請將此參數設定為 UNISP \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="f7348-136">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-137">*fCredentialUse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-137">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-138">指出將如何使用這些認證的旗標。</span><span class="sxs-lookup"><span data-stu-id="f7348-138">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="f7348-139">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f7348-139">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f7348-140">值</span><span class="sxs-lookup"><span data-stu-id="f7348-140">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="f7348-141">意義</span><span class="sxs-lookup"><span data-stu-id="f7348-141">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="f7348-142"><dt>**SECPKG \_認證 \_ 自動 \_**</dt>登入限制的 <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-142"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="f7348-143">安全性不會使用預設的登入認證或 [認證管理員](credential-manager.md)的認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-143">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="f7348-144">只有 Negotiate [*限制委派*](../secgloss/s-gly.md)才支援此值。</span><span class="sxs-lookup"><span data-stu-id="f7348-144">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="f7348-145">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="f7348-145">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="f7348-146"><dt>**SECPKG \_ 認證 \_ 兩者**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-146"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="f7348-147">驗證傳入的認證或使用本機認證來準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="f7348-147">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="f7348-148">此旗標可啟用兩個其他旗標。</span><span class="sxs-lookup"><span data-stu-id="f7348-148">This flag enables both other flags.</span></span> <span data-ttu-id="f7348-149">此旗標對 Digest 和 Schannel Ssp 而言無效。</span><span class="sxs-lookup"><span data-stu-id="f7348-149">This flag is not valid with the Digest and Schannel SSPs.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="f7348-150"><dt>**SECPKG \_ 認證 \_ 輸入**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-150"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="f7348-151">驗證傳入的伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-151">Validate an incoming server credential.</span></span> <span data-ttu-id="f7348-152">當呼叫 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md) 或 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) 時，可能會使用驗證授權單位來驗證輸入認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-152">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) or [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) is called.</span></span> <span data-ttu-id="f7348-153">如果無法使用這類授權單位，此函式將會失敗，並傳回 SEC \_ E \_ NO \_ 驗證 \_ 授權單位。</span><span class="sxs-lookup"><span data-stu-id="f7348-153">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="f7348-154">驗證是套件特定的。</span><span class="sxs-lookup"><span data-stu-id="f7348-154">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="f7348-155"><dt>**SECPKG \_ 認證 \_ 輸出**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-155"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="f7348-156">允許本機用戶端認證準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="f7348-156">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="f7348-157"><dt>**SECPKG \_\_ \_ \_ 僅限認證進程原則**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-157"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="f7348-158">此函式會處理伺服器原則，並傳回 **SEC \_ E \_ NO \_ 認證**，表示應用程式應該提示輸入認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-158">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="f7348-159">只有 Negotiate [*限制委派*](../secgloss/s-gly.md)才支援此值。</span><span class="sxs-lookup"><span data-stu-id="f7348-159">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="f7348-160">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="f7348-160">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="f7348-161">*pvLogonID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-161">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-162">識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) 的指標。</span><span class="sxs-lookup"><span data-stu-id="f7348-162">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="f7348-163">此參數是針對檔案系統進程（例如網路重新導向程式）所提供。</span><span class="sxs-lookup"><span data-stu-id="f7348-163">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="f7348-164">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-164">This parameter can be **NULL**.</span></span>

<span data-ttu-id="f7348-165">使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-165">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-166">*pAuthData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-166">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-167">封裝特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="f7348-167">A pointer to package-specific data.</span></span> <span data-ttu-id="f7348-168">這個參數可以是 **Null**，這表示必須使用該 [*安全性封裝*](../secgloss/s-gly.md) 的預設認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-168">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="f7348-169">若要使用提供的認證，請在此參數中傳遞包含這些認證的 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構。</span><span class="sxs-lookup"><span data-stu-id="f7348-169">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="f7348-170">RPC 執行時間會傳遞 [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)中提供的任何內容。</span><span class="sxs-lookup"><span data-stu-id="f7348-170">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="f7348-171">使用摘要 SSP 時，此參數是指向 [**每秒的 \_ WINNT AUTH 身分 \_ \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構的指標，其中包含用來尋找認證的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="f7348-171">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

<span data-ttu-id="f7348-172">使用安全通道 SSP 時，請指定安全通道 [**認證結構， \_**](/windows/win32/api/schannel/ns-schannel-schannel_cred) 指出要使用的通訊協定，以及各種可自訂通道功能的設定。</span><span class="sxs-lookup"><span data-stu-id="f7348-172">When using the Schannel SSP, specify an [**SCHANNEL\_CRED**](/windows/win32/api/schannel/ns-schannel-schannel_cred) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

<span data-ttu-id="f7348-173">使用 NTLM 或 Negotiate 套件時，使用者名稱、密碼和網域的最大字元長度分別為256、256和15。</span><span class="sxs-lookup"><span data-stu-id="f7348-173">When using the NTLM or Negotiate packages, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-174">*pGetKeyFn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-174">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-175">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-175">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-176">*pvGetKeyArgument* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7348-176">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-177">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-177">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-178">*phCredential* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f7348-178">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-179">[CredHandle](sspi-handles.md)結構的指標，用來接收認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-179">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="f7348-180">*ptsExpiry* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f7348-180">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7348-181">[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。</span><span class="sxs-lookup"><span data-stu-id="f7348-181">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="f7348-182">這個 **時間戳記** 結構中所傳回的值取決於 [*限制委派*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="f7348-182">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f7348-183">[*安全性封裝*](../secgloss/s-gly.md)必須以本地時間傳回此值。</span><span class="sxs-lookup"><span data-stu-id="f7348-183">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="f7348-184">此參數會設定為常數的最長時間。</span><span class="sxs-lookup"><span data-stu-id="f7348-184">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="f7348-185">摘要式 [*安全性內容*](../secgloss/s-gly.md)或認證或使用摘要 SSP 時，沒有到期時間。</span><span class="sxs-lookup"><span data-stu-id="f7348-185">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

<span data-ttu-id="f7348-186">使用 Schannel SSP 時，此參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f7348-186">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="f7348-187">當用於驗證的認證是憑證時，此參數會收到該憑證的到期時間。</span><span class="sxs-lookup"><span data-stu-id="f7348-187">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="f7348-188">如果未提供任何憑證，則會傳回最大時間值。</span><span class="sxs-lookup"><span data-stu-id="f7348-188">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7348-189">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7348-189">Return value</span></span>

<span data-ttu-id="f7348-190">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f7348-190">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="f7348-191">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-191">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="f7348-192">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f7348-192">Return code</span></span>                                                                                                 | <span data-ttu-id="f7348-193">Description</span><span class="sxs-lookup"><span data-stu-id="f7348-193">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7348-194"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-194"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="f7348-195">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="f7348-195">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="f7348-196"><dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-196"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="f7348-197">發生未對應到 SSPI 錯誤碼的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7348-197">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="f7348-198"><dt>**SEC \_ E \_ 無 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-198"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="f7348-199">[*限制委派*](../secgloss/s-gly.md)中不提供任何認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-199">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="f7348-200"><dt>**秒 \_ E \_ 非 \_ 擁有者**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-200"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="f7348-201">函數的呼叫端沒有必要的認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-201">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="f7348-202"><dt>**\_ \_ \_ \_ 找不到 SEC E SECPKG**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-202"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="f7348-203">要求的 [*安全性封裝*](../secgloss/s-gly.md) 不存在。</span><span class="sxs-lookup"><span data-stu-id="f7348-203">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="f7348-204"><dt>**SEC \_ E \_ 未知的 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-204"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="f7348-205">無法辨識提供給封裝的認證。</span><span class="sxs-lookup"><span data-stu-id="f7348-205">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="f7348-206">備註</span><span class="sxs-lookup"><span data-stu-id="f7348-206">Remarks</span></span>

<span data-ttu-id="f7348-207">**AcquireCredentialsHandle (一般)** 函數會傳回主體的控制碼，例如使用者或用戶端，以供特定的 [*限制委派*](../secgloss/s-gly.md)使用。</span><span class="sxs-lookup"><span data-stu-id="f7348-207">The **AcquireCredentialsHandle (General)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f7348-208">這可能是預先存在的認證的控制碼，或函式可以建立新的認證集，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="f7348-208">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="f7348-209">這個控制碼可以在 AcceptSecurityCoNtext 的後續呼叫中使用 [**(一般)**](acceptsecuritycontext--general.md) 和 [**InitializeSecurityCoNtext (的一般)**](initializesecuritycontext--general.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="f7348-209">This handle can be used in subsequent calls to the [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) and [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) functions.</span></span>

<span data-ttu-id="f7348-210">一般而言， **AcquireCredentialsHandle (一般)** 不允許處理常式取得其他登入相同電腦的使用者認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7348-210">In general, **AcquireCredentialsHandle (General)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="f7348-211">不過，具有 SE TCB 名稱許可權的呼叫端可以 \_ \_ 選擇指定任何現有登入會話權杖的 [*登入識別碼*](../secgloss/l-gly.md) (LUID) ，以取得該會話認證的控制碼 [](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="f7348-211">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="f7348-212">一般來說，這是由必須代表已登入使用者的核心模式模組所使用。</span><span class="sxs-lookup"><span data-stu-id="f7348-212">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="f7348-213">封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="f7348-213">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="f7348-214">如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7348-214">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="f7348-215">針對核心模式呼叫端，必須注意下列差異：</span><span class="sxs-lookup"><span data-stu-id="f7348-215">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="f7348-216">這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="f7348-216">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="f7348-217">您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="f7348-217">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="f7348-218">當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f7348-218">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7348-219">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7348-219">Requirements</span></span>



| <span data-ttu-id="f7348-220">需求</span><span class="sxs-lookup"><span data-stu-id="f7348-220">Requirement</span></span> | <span data-ttu-id="f7348-221">值</span><span class="sxs-lookup"><span data-stu-id="f7348-221">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7348-222">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7348-222">Minimum supported client</span></span><br/> | <span data-ttu-id="f7348-223">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7348-223">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f7348-224">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7348-224">Minimum supported server</span></span><br/> | <span data-ttu-id="f7348-225">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7348-225">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f7348-226">標頭</span><span class="sxs-lookup"><span data-stu-id="f7348-226">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7348-227"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f7348-227"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="f7348-228">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7348-228">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7348-229"><dt>Secur32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-229"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="f7348-230">DLL</span><span class="sxs-lookup"><span data-stu-id="f7348-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7348-231"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7348-231"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="f7348-232">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f7348-232">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7348-233">**AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f7348-233">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f7348-234">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7348-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7348-235">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="f7348-235">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="f7348-236">**AcceptSecurityCoNtext (一般)**</span><span class="sxs-lookup"><span data-stu-id="f7348-236">**AcceptSecurityContext (General)**</span></span>](acceptsecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="f7348-237">**InitializeSecurityCoNtext (一般)**</span><span class="sxs-lookup"><span data-stu-id="f7348-237">**InitializeSecurityContext (General)**</span></span>](initializesecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="f7348-238">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="f7348-238">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 

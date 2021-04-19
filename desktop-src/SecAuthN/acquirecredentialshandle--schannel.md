---
description: 取得使用 Schannel 之安全性主體的預先存在認證控制碼。
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: 'AcquireCredentialsHandle (Schannel) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5b7de49e76cf5b09611790a12826f1a13fc38e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985288"
---
# <a name="acquirecredentialshandle-schannel-function"></a><span data-ttu-id="1cd2c-103">AcquireCredentialsHandle (Schannel) 函數</span><span class="sxs-lookup"><span data-stu-id="1cd2c-103">AcquireCredentialsHandle (Schannel) function</span></span>

<span data-ttu-id="1cd2c-104">**AcquireCredentialsHandle (Schannel)** 函式會取得 [*安全性主體*](../secgloss/s-gly.md)預先存在的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-104">The **AcquireCredentialsHandle (Schannel)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cd2c-105">[**InitializeSecurityCoNtext (schannel)**](initializesecuritycontext--schannel.md)和 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md)函式需要此控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-105">This handle is required by the [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) and [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) functions.</span></span> <span data-ttu-id="1cd2c-106">這些可以是預先存在的 *認證*，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="1cd2c-107">這不是「登入網路」，也不代表認證的收集。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1cd2c-108">語法</span><span class="sxs-lookup"><span data-stu-id="1cd2c-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="1cd2c-109">參數</span><span class="sxs-lookup"><span data-stu-id="1cd2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd2c-110">*pszPrincipal* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-110">*pszPrincipal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-111">以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="1cd2c-112">使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-112">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="1cd2c-113">如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="1cd2c-114">Null 字串表示進程需要在其執行 [*安全性內容*](../secgloss/s-gly.md) 之使用者的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="1cd2c-115">*pszPackage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-116">以 null 結束的字串指標，指定將使用這些認證之 [*安全性封裝*](../secgloss/s-gly.md) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="1cd2c-117">這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的 [*安全性封裝*](../secgloss/s-gly.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="1cd2c-118">建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (Schannel)**](querycontextattributes--schannel.md) ，並將 *ULATTRIBUTE* 設定為 SECPKG \_ ATTR \_ 封裝 \_ 資訊，以傳回使用中 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-118">After a context is established, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="1cd2c-119">使用 Schannel SSP 時，請將此參數設定為 UNISP \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-119">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-120">*fCredentialUse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-121">指出將如何使用這些認證的旗標。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="1cd2c-122">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1cd2c-123">值</span><span class="sxs-lookup"><span data-stu-id="1cd2c-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="1cd2c-124">意義</span><span class="sxs-lookup"><span data-stu-id="1cd2c-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="1cd2c-125"><dt>**SECPKG \_ 認證 \_ 輸入**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="1cd2c-126">驗證傳入的伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-126">Validate an incoming server credential.</span></span> <span data-ttu-id="1cd2c-127">輸入認證可能會在 [**InitializeSecurityCoNtext (schannel)**](initializesecuritycontext--schannel.md) 或 [**AcceptSecurityCoNtext (**](acceptsecuritycontext--schannel.md) 安全通道) 被呼叫時，使用驗證授權單位進行驗證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) or [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) is called.</span></span> <span data-ttu-id="1cd2c-128">如果無法使用這類授權單位，此函式將會失敗，並傳回 SEC \_ E \_ NO \_ 驗證 \_ 授權單位。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="1cd2c-129">驗證是套件特定的。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="1cd2c-130"><dt>**SECPKG \_ 認證 \_ 輸出**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="1cd2c-131">允許本機用戶端認證準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="1cd2c-132">*pvLogonID* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-132">*pvLogonID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-133">識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) 的指標。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="1cd2c-134">此參數是針對檔案系統進程（例如網路重新導向程式）所提供。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="1cd2c-135">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-135">This parameter can be **NULL**.</span></span>

<span data-ttu-id="1cd2c-136">使用安全通道 SSP 時，不會使用此參數，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-136">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-137">*pAuthData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-137">*pAuthData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-138">封裝特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-138">A pointer to package-specific data.</span></span> <span data-ttu-id="1cd2c-139">這個參數可以是 **Null**，這表示必須使用該 [*安全性封裝*](../secgloss/s-gly.md) 的預設認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="1cd2c-140">若要使用提供的認證，請在此參數中傳遞包含這些認證的 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="1cd2c-141">RPC 執行時間會傳遞 [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)中提供的任何內容。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="1cd2c-142">使用安全通道 SSP 時，請指定 [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) 結構，以指出要使用的通訊協定，以及各種可自訂通道功能的設定。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-142">When using the Schannel SSP, specify an [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-143">*pGetKeyFn* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-143">*pGetKeyFn* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-144">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-145">*pvGetKeyArgument* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-145">*pvGetKeyArgument* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-146">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-147">*phCredential* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-148">[CredHandle](sspi-handles.md)結構的指標，用來接收認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="1cd2c-149">*ptsExpiry* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-149">*ptsExpiry* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2c-150">[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="1cd2c-151">這個 **時間戳記** 結構中所傳回的值取決於 [*限制委派*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cd2c-152">[*安全性封裝*](../secgloss/s-gly.md)必須以本地時間傳回此值。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="1cd2c-153">使用 Schannel SSP 時，此參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-153">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="1cd2c-154">當用於驗證的認證是憑證時，此參數會收到該憑證的到期時間。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-154">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="1cd2c-155">如果未提供任何憑證，則會傳回最大時間值。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-155">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd2c-156">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cd2c-156">Return value</span></span>

<span data-ttu-id="1cd2c-157">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-157">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1cd2c-158">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-158">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="1cd2c-159">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1cd2c-159">Return code</span></span>                                                                                                 | <span data-ttu-id="1cd2c-160">Description</span><span class="sxs-lookup"><span data-stu-id="1cd2c-160">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cd2c-161"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-161"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="1cd2c-162">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-162">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="1cd2c-163"><dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-163"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="1cd2c-164">發生未對應到 SSPI 錯誤碼的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-164">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="1cd2c-165"><dt>**SEC \_ E \_ 無 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-165"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="1cd2c-166">[*限制委派*](../secgloss/s-gly.md)中不提供任何認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-166">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="1cd2c-167"><dt>**秒 \_ E \_ 非 \_ 擁有者**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-167"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="1cd2c-168">函數的呼叫端沒有必要的認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-168">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="1cd2c-169"><dt>**\_ \_ \_ \_ 找不到 SEC E SECPKG**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-169"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="1cd2c-170">要求的 [*安全性封裝*](../secgloss/s-gly.md) 不存在。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-170">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="1cd2c-171"><dt>**SEC \_ E \_ 未知的 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-171"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="1cd2c-172">無法辨識提供給封裝的認證。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-172">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1cd2c-173">備註</span><span class="sxs-lookup"><span data-stu-id="1cd2c-173">Remarks</span></span>

<span data-ttu-id="1cd2c-174">**AcquireCredentialsHandle (Schannel)** 函式會傳回主體（例如使用者或用戶端）之認證的控制碼，以供特定 [*限制委派*](../secgloss/s-gly.md)使用。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-174">The **AcquireCredentialsHandle (Schannel)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1cd2c-175">這可能是預先存在的認證的控制碼，或函式可以建立新的認證集，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-175">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="1cd2c-176">這個控制碼可用於對 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md) 和 [**InitializeSecurityCoNtext (schannel)**](initializesecuritycontext--schannel.md) 函式的後續呼叫中。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-176">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) and [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) functions.</span></span>

<span data-ttu-id="1cd2c-177">一般而言， **AcquireCredentialsHandle (Schannel)** 不允許處理常式取得其他登入相同電腦的使用者認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-177">In general, **AcquireCredentialsHandle (Schannel)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="1cd2c-178">不過，具有 SE TCB 名稱許可權的呼叫端可以 \_ \_ 選擇指定任何現有登入會話權杖的 [*登入識別碼*](../secgloss/l-gly.md) (LUID) ，以取得該會話認證的控制碼 [](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-178">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="1cd2c-179">一般來說，這是由必須代表已登入使用者的核心模式模組所使用。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-179">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="1cd2c-180">封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-180">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="1cd2c-181">如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-181">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="1cd2c-182">針對核心模式呼叫端，必須注意下列差異：</span><span class="sxs-lookup"><span data-stu-id="1cd2c-182">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="1cd2c-183">這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-183">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="1cd2c-184">您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-184">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="1cd2c-185">當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1cd2c-185">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd2c-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cd2c-186">Requirements</span></span>



| <span data-ttu-id="1cd2c-187">需求</span><span class="sxs-lookup"><span data-stu-id="1cd2c-187">Requirement</span></span> | <span data-ttu-id="1cd2c-188">值</span><span class="sxs-lookup"><span data-stu-id="1cd2c-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd2c-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cd2c-189">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd2c-190">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-190">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1cd2c-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cd2c-191">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd2c-192">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cd2c-192">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1cd2c-193">標頭</span><span class="sxs-lookup"><span data-stu-id="1cd2c-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cd2c-194"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-194"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="1cd2c-195">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cd2c-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cd2c-196"><dt>Secur32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-196"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="1cd2c-197">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd2c-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cd2c-198"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2c-198"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="1cd2c-199">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1cd2c-199">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1cd2c-200">**AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1cd2c-200">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1cd2c-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cd2c-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd2c-202">**AcceptSecurityCoNtext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="1cd2c-202">**AcceptSecurityContext (Schannel)**</span></span>](acceptsecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="1cd2c-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="1cd2c-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[<span data-ttu-id="1cd2c-204">**InitializeSecurityCoNtext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="1cd2c-204">**InitializeSecurityContext (Schannel)**</span></span>](initializesecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="1cd2c-205">**SCH_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="1cd2c-205">**SCH_CREDENTIALS**</span></span>](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[<span data-ttu-id="1cd2c-206">**SSPI 函數**</span><span class="sxs-lookup"><span data-stu-id="1cd2c-206">**SSPI Functions**</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 

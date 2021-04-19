---
description: 取得使用 Kerberos 之安全性主體預先存在認證的控制碼。
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: 'AcquireCredentialsHandle (Kerberos) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999925"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="772e6-103">AcquireCredentialsHandle (Kerberos) 函數</span><span class="sxs-lookup"><span data-stu-id="772e6-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="772e6-104">**AcquireCredentialsHandle (Kerberos)** 函式會取得 [*安全性主體*](../secgloss/s-gly.md)預先存在的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="772e6-105">[**InitializeSecurityCoNtext (kerberos)**](initializesecuritycontext--kerberos.md)和 [**AcceptSecurityCoNtext (kerberos)**](acceptsecuritycontext--kerberos.md)函式需要此控制碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="772e6-106">這些可以是預先存在的 *認證*，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="772e6-107">這不是「登入網路」，也不代表認證的收集。</span><span class="sxs-lookup"><span data-stu-id="772e6-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="772e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="772e6-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="772e6-109">參數</span><span class="sxs-lookup"><span data-stu-id="772e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772e6-110">*pszPrincipal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-111">以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="772e6-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="772e6-112">如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="772e6-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="772e6-113">Null 字串表示進程需要在其執行 [*安全性內容*](../secgloss/s-gly.md) 之使用者的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="772e6-114">*pszPackage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-115">以 null 結束的字串指標，指定將使用這些認證之 [*安全性封裝*](../secgloss/s-gly.md) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="772e6-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="772e6-116">這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的 [*安全性封裝*](../secgloss/s-gly.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="772e6-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="772e6-117">建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (Kerberos)**](querycontextattributes--kerberos.md) ，並將 *ULATTRIBUTE* 設定為 SECPKG \_ ATTR \_ 封裝 \_ 資訊，以傳回使用中 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="772e6-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="772e6-118">*fCredentialUse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-119">指出將如何使用這些認證的旗標。</span><span class="sxs-lookup"><span data-stu-id="772e6-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="772e6-120">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="772e6-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="772e6-121">值</span><span class="sxs-lookup"><span data-stu-id="772e6-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="772e6-122">意義</span><span class="sxs-lookup"><span data-stu-id="772e6-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="772e6-123"><dt>**SECPKG \_ 認證 \_ 兩者**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="772e6-124">驗證傳入的認證或使用本機認證來準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="772e6-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="772e6-125">此旗標可啟用兩個其他旗標。</span><span class="sxs-lookup"><span data-stu-id="772e6-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="772e6-126"><dt>**SECPKG \_ 認證 \_ 輸入**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="772e6-127">驗證傳入的伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-127">Validate an incoming server credential.</span></span> <span data-ttu-id="772e6-128">當呼叫 [**InitializeSecurityCoNtext (kerberos)**](initializesecuritycontext--kerberos.md) 或 [**AcceptSecurityCoNtext (kerberos)**](acceptsecuritycontext--kerberos.md) 時，可能會使用驗證授權單位來驗證輸入認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="772e6-129">如果無法使用這類授權單位，此函式將會失敗，並傳回 SEC \_ E \_ NO \_ 驗證 \_ 授權單位。</span><span class="sxs-lookup"><span data-stu-id="772e6-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="772e6-130">驗證是套件特定的。</span><span class="sxs-lookup"><span data-stu-id="772e6-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="772e6-131"><dt>**SECPKG \_ 認證 \_ 輸出**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="772e6-132">允許本機用戶端認證準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="772e6-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="772e6-133">*pvLogonID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-134">識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) 的指標。</span><span class="sxs-lookup"><span data-stu-id="772e6-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="772e6-135">此參數是針對檔案系統進程（例如網路重新導向程式）所提供。</span><span class="sxs-lookup"><span data-stu-id="772e6-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="772e6-136">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="772e6-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="772e6-137">*pAuthData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-138">封裝特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="772e6-138">A pointer to package-specific data.</span></span> <span data-ttu-id="772e6-139">這個參數可以是 **Null**，這表示必須使用該 [*安全性封裝*](../secgloss/s-gly.md) 的預設認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="772e6-140">若要使用提供的認證，請在此參數中傳遞包含這些認證的 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構。</span><span class="sxs-lookup"><span data-stu-id="772e6-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="772e6-141">RPC 執行時間會傳遞 [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)中提供的任何內容。</span><span class="sxs-lookup"><span data-stu-id="772e6-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="772e6-142">*pGetKeyFn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-143">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="772e6-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="772e6-144">*pvGetKeyArgument* \[在\]</span><span class="sxs-lookup"><span data-stu-id="772e6-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-145">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="772e6-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="772e6-146">*phCredential* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="772e6-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-147">[CredHandle](sspi-handles.md)結構的指標，用來接收認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="772e6-148">*ptsExpiry* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="772e6-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="772e6-149">[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。</span><span class="sxs-lookup"><span data-stu-id="772e6-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="772e6-150">這個 **時間戳記** 結構中所傳回的值取決於 [*限制委派*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="772e6-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="772e6-151">[*安全性封裝*](../secgloss/s-gly.md)必須以本地時間傳回此值。</span><span class="sxs-lookup"><span data-stu-id="772e6-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772e6-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="772e6-152">Return value</span></span>

<span data-ttu-id="772e6-153">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="772e6-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="772e6-154">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="772e6-155">傳回碼</span><span class="sxs-lookup"><span data-stu-id="772e6-155">Return code</span></span>                                                                                                 | <span data-ttu-id="772e6-156">Description</span><span class="sxs-lookup"><span data-stu-id="772e6-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="772e6-157"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="772e6-158">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="772e6-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="772e6-159"><dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="772e6-160">發生未對應到 SSPI 錯誤碼的錯誤。</span><span class="sxs-lookup"><span data-stu-id="772e6-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="772e6-161"><dt>**SEC \_ E \_ 無 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="772e6-162">[*限制委派*](../secgloss/s-gly.md)中不提供任何認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="772e6-163"><dt>**秒 \_ E \_ 非 \_ 擁有者**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="772e6-164">函數的呼叫端沒有必要的認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="772e6-165"><dt>**\_ \_ \_ \_ 找不到 SEC E SECPKG**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="772e6-166">要求的 [*安全性封裝*](../secgloss/s-gly.md) 不存在。</span><span class="sxs-lookup"><span data-stu-id="772e6-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="772e6-167"><dt>**SEC \_ E \_ 未知的 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="772e6-168">無法辨識提供給封裝的認證。</span><span class="sxs-lookup"><span data-stu-id="772e6-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="772e6-169">備註</span><span class="sxs-lookup"><span data-stu-id="772e6-169">Remarks</span></span>

<span data-ttu-id="772e6-170">**AcquireCredentialsHandle (Kerberos)** 函數會傳回主體的控制碼，例如使用者或用戶端，以供特定的 [*限制委派*](../secgloss/s-gly.md)使用。</span><span class="sxs-lookup"><span data-stu-id="772e6-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="772e6-171">這可能是預先存在的認證的控制碼，或函式可以建立新的認證集，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="772e6-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="772e6-172">這個控制碼可用於對 [**AcceptSecurityCoNtext (kerberos)**](acceptsecuritycontext--kerberos.md) 和 [**InitializeSecurityCoNtext (kerberos)**](initializesecuritycontext--kerberos.md) 函式的後續呼叫中。</span><span class="sxs-lookup"><span data-stu-id="772e6-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="772e6-173">一般而言， **AcquireCredentialsHandle (Kerberos)** 不允許處理常式取得其他登入相同電腦的使用者認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="772e6-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="772e6-174">不過，具有 SE TCB 名稱許可權的呼叫端可以 \_ \_ 選擇指定任何現有登入會話權杖的 [*登入識別碼*](../secgloss/l-gly.md) (LUID) ，以取得該會話認證的控制碼 [](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="772e6-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="772e6-175">一般來說，這是由必須代表已登入使用者的核心模式模組所使用。</span><span class="sxs-lookup"><span data-stu-id="772e6-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="772e6-176">封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="772e6-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="772e6-177">如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="772e6-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="772e6-178">針對核心模式呼叫端，必須注意下列差異：</span><span class="sxs-lookup"><span data-stu-id="772e6-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="772e6-179">這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="772e6-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="772e6-180">您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="772e6-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="772e6-181">當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="772e6-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="772e6-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="772e6-182">Requirements</span></span>



| <span data-ttu-id="772e6-183">需求</span><span class="sxs-lookup"><span data-stu-id="772e6-183">Requirement</span></span> | <span data-ttu-id="772e6-184">值</span><span class="sxs-lookup"><span data-stu-id="772e6-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772e6-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="772e6-185">Minimum supported client</span></span><br/> | <span data-ttu-id="772e6-186">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="772e6-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="772e6-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="772e6-187">Minimum supported server</span></span><br/> | <span data-ttu-id="772e6-188">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="772e6-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="772e6-189">標頭</span><span class="sxs-lookup"><span data-stu-id="772e6-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="772e6-190"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="772e6-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="772e6-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="772e6-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="772e6-192"><dt>Secur32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="772e6-193">DLL</span><span class="sxs-lookup"><span data-stu-id="772e6-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="772e6-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="772e6-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="772e6-195">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="772e6-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="772e6-196">**AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="772e6-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="772e6-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="772e6-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772e6-198">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="772e6-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="772e6-199">**AcceptSecurityCoNtext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="772e6-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="772e6-200">**InitializeSecurityCoNtext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="772e6-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="772e6-201">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="772e6-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 

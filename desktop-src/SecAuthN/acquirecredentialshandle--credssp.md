---
description: AcquireCredentialsHandle (CredSSP) 函數會取得安全性主體預先存在的認證控制碼。
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: AcquireCredentialsHandle (CredSSP) 函式
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969398"
---
# <a name="acquirecredentialshandle-credssp-function"></a><span data-ttu-id="e441f-103">AcquireCredentialsHandle (CredSSP) 函式</span><span class="sxs-lookup"><span data-stu-id="e441f-103">AcquireCredentialsHandle (CredSSP) function</span></span>

<span data-ttu-id="e441f-104">**AcquireCredentialsHandle (CredSSP)** 函數會取得安全性主體預先存在的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="e441f-104">The **AcquireCredentialsHandle (CredSSP)** function acquires a handle to preexisting credentials of a security principal.</span></span> <span data-ttu-id="e441f-105">[**InitializeSecurityCoNtext (credssp)**](initializesecuritycontext--credssp.md)和 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md)函式需要這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="e441f-105">This handle is required by the [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) and [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) functions.</span></span> <span data-ttu-id="e441f-106">這些可以是預先存在的 *認證*，其是透過系統登入所建立，而不是此處所述，或呼叫者可以提供替代的認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="e441f-107">這不是「登入網路」，也不代表認證的收集。</span><span class="sxs-lookup"><span data-stu-id="e441f-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="e441f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e441f-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a><span data-ttu-id="e441f-109">參數</span><span class="sxs-lookup"><span data-stu-id="e441f-109">Parameters</span></span>

<span data-ttu-id="e441f-110">*pszPrincipal* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e441f-110">*pszPrincipal* \[in, optional\]</span></span>

<span data-ttu-id="e441f-111">以 null 結束的字串指標，指定控制碼將參考其認證之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="e441f-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="e441f-112">如果要求控制碼的進程沒有認證的存取權，則函式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e441f-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="e441f-113">Null 字串表示進程需要在其執行安全性內容之使用者的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="e441f-113">A null string indicates that the process requires a handle to the credentials of the user under whose security context it is executing.</span></span>

<span data-ttu-id="e441f-114">*pszPackage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e441f-114">*pszPackage* \[in\]</span></span>

<span data-ttu-id="e441f-115">以 null 結束的字串指標，指定將使用這些認證之安全性封裝的名稱。</span><span class="sxs-lookup"><span data-stu-id="e441f-115">A pointer to a null-terminated string that specifies the name of the security package with which these credentials will be used.</span></span> <span data-ttu-id="e441f-116">這是在 [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa)函數所傳回之 [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的 **name** 成員中傳回的安全性封裝名稱。</span><span class="sxs-lookup"><span data-stu-id="e441f-116">This is a security package name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) function.</span></span> <span data-ttu-id="e441f-117">建立內容之後，您可以呼叫 [**QueryCoNtextAttributes (CredSSP)**](querycontextattributes--credssp.md) ，並將 *UlAttribute* 設定為 **SECPKG \_ ATTR \_ 封裝 \_ 資訊** ，以傳回使用中安全性封裝的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e441f-117">After a context is established, [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) can be called with *ulAttribute* set to **SECPKG\_ATTR\_PACKAGE\_INFO** to return information on the security package in use.</span></span>

<span data-ttu-id="e441f-118">*fCredentialUse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e441f-118">*fCredentialUse* \[in\]</span></span>

<span data-ttu-id="e441f-119">指出將如何使用這些認證的旗標。</span><span class="sxs-lookup"><span data-stu-id="e441f-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="e441f-120">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e441f-120">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="e441f-121">值</span><span class="sxs-lookup"><span data-stu-id="e441f-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="e441f-122">意義</span><span class="sxs-lookup"><span data-stu-id="e441f-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e441f-123">**SECPKG \_ 認證 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="e441f-123">**SECPKG\_CRED\_INBOUND**</span></span><br/><span data-ttu-id="e441f-124">0x1</span><span class="sxs-lookup"><span data-stu-id="e441f-124">0x1</span></span>  | <span data-ttu-id="e441f-125">驗證傳入的伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-125">Validate an incoming server credential.</span></span> <span data-ttu-id="e441f-126">當呼叫 [**InitializeSecurityCoNtext (credssp)**](initializesecuritycontext--credssp.md) 或 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md) 時，可能會使用驗證授權單位來驗證輸入認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-126">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) or [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) is called.</span></span> <span data-ttu-id="e441f-127">如果無法使用這類授權單位，此函式將會失敗，並傳回 **SEC \_ E \_ NO \_ 驗證 \_ 授權** 單位。</span><span class="sxs-lookup"><span data-stu-id="e441f-127">If such an authority is not available, the function will fail and return **SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY**.</span></span> <span data-ttu-id="e441f-128">驗證是套件特定的</span><span class="sxs-lookup"><span data-stu-id="e441f-128">Validation is package specific</span></span> |
| <span data-ttu-id="e441f-129">**SECPKG \_ 認證 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="e441f-129">**SECPKG\_CRED\_OUTBOUND**</span></span><br/><span data-ttu-id="e441f-130">0x0</span><span class="sxs-lookup"><span data-stu-id="e441f-130">0x0</span></span> | <span data-ttu-id="e441f-131">允許本機用戶端認證準備傳出權杖。</span><span class="sxs-lookup"><span data-stu-id="e441f-131">Allow a local client credential to prepare an outgoing token.</span></span> |

<span data-ttu-id="e441f-132">*pvLogonId* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e441f-132">*pvLogonId* \[in, optional\]</span></span>

<span data-ttu-id="e441f-133">識別使用者之 [*本機唯一識別碼*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) 的指標。</span><span class="sxs-lookup"><span data-stu-id="e441f-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) that identifies the user.</span></span> <span data-ttu-id="e441f-134">此參數是針對檔案系統進程（例如網路重新導向程式）所提供。</span><span class="sxs-lookup"><span data-stu-id="e441f-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="e441f-135">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e441f-135">This parameter can be **NULL**.</span></span>

<span data-ttu-id="e441f-136">*pAuthData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e441f-136">*pAuthData* \[in, optional\]</span></span>

<span data-ttu-id="e441f-137">[**CREDSSP \_**](/windows/win32/api/credssp/ns-credssp-credssp_cred)認證結構的指標，此結構會指定 Schannel 和 Negotiate 封裝的驗證資料。</span><span class="sxs-lookup"><span data-stu-id="e441f-137">A pointer to a [**CREDSSP\_CRED**](/windows/win32/api/credssp/ns-credssp-credssp_cred) structure that specifies authentication data for both Schannel and Negotiate packages.</span></span>

<span data-ttu-id="e441f-138">*pGetKeyFn* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e441f-138">*pGetKeyFn* \[in, optional\]</span></span>

<span data-ttu-id="e441f-139">保留的。</span><span class="sxs-lookup"><span data-stu-id="e441f-139">Reserved.</span></span> <span data-ttu-id="e441f-140">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e441f-140">This parameter is not used and should be set to **NULL**.</span></span>

<span data-ttu-id="e441f-141">*pvGetKeyArgument* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e441f-141">*pvGetKeyArgument* \[in, optional\]</span></span>

<span data-ttu-id="e441f-142">保留的。</span><span class="sxs-lookup"><span data-stu-id="e441f-142">Reserved.</span></span> <span data-ttu-id="e441f-143">此參數必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e441f-143">This parameter must be set to **NULL**.</span></span>

<span data-ttu-id="e441f-144">*phCredential* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e441f-144">*phCredential* \[out\]</span></span>

<span data-ttu-id="e441f-145">[CredHandle](sspi-handles.md)結構的指標，此結構會接收認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="e441f-145">A pointer to the [CredHandle](sspi-handles.md) structure that will receive the credential handle.</span></span>

<span data-ttu-id="e441f-146">*ptsExpiry* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="e441f-146">*ptsExpiry* \[out, optional\]</span></span>

<span data-ttu-id="e441f-147">[**時間戳記**](timestamp.md)結構的指標，該結構會接收所傳回認證到期的時間。</span><span class="sxs-lookup"><span data-stu-id="e441f-147">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="e441f-148">收到的結構值取決於安全性封裝，必須以本地時間指定值。</span><span class="sxs-lookup"><span data-stu-id="e441f-148">The structure value received depends on the security package, which must specify the value in local time.</span></span>

## <a name="return-value"></a><span data-ttu-id="e441f-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="e441f-149">Return value</span></span>

<span data-ttu-id="e441f-150">如果函式成功，則會傳回 **SEC \_ E \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e441f-150">If the function succeeds, it returns **SEC\_E\_OK**.</span></span>

<span data-ttu-id="e441f-151">如果函式失敗，則會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e441f-151">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="e441f-152">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e441f-152">Return code</span></span>                      | <span data-ttu-id="e441f-153">Description</span><span class="sxs-lookup"><span data-stu-id="e441f-153">Description</span></span>                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="e441f-154">**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="e441f-154">**SEC\_E\_INSUFFICIENT\_MEMORY**</span></span> | <span data-ttu-id="e441f-155">可用的記憶體不足，無法完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="e441f-155">There is insufficient memory available to complete the requested action.</span></span> |
| <span data-ttu-id="e441f-156">**SEC \_ E \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e441f-156">**SEC\_E\_INTERNAL\_ERROR**</span></span>      | <span data-ttu-id="e441f-157">發生未對應到 SSPI 錯誤碼的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e441f-157">An error occurred that did not map to an SSPI error code.</span></span>                |
| <span data-ttu-id="e441f-158">**SEC \_ E \_ 無 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="e441f-158">**SEC\_E\_NO\_CREDENTIALS**</span></span>      | <span data-ttu-id="e441f-159">安全性套件中沒有任何可用的認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-159">No credentials are available in the security package.</span></span>                    |
| <span data-ttu-id="e441f-160">**秒 \_ E \_ 非 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="e441f-160">**SEC\_E\_NOT\_OWNER**</span></span>           | <span data-ttu-id="e441f-161">函數的呼叫端沒有必要的認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-161">The caller of the function does not have the necessary credentials.</span></span>      |
| <span data-ttu-id="e441f-162">**\_ \_ \_ \_ 找不到 SEC E SECPKG**</span><span class="sxs-lookup"><span data-stu-id="e441f-162">**SEC\_E\_SECPKG\_NOT\_FOUND**</span></span>   | <span data-ttu-id="e441f-163">要求的安全性封裝不存在。</span><span class="sxs-lookup"><span data-stu-id="e441f-163">The requested security package does not exist.</span></span>                           |
| <span data-ttu-id="e441f-164">**SEC \_ E \_ 未知的 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="e441f-164">**SEC\_E\_UNKNOWN\_CREDENTIALS**</span></span> | <span data-ttu-id="e441f-165">無法辨識提供給封裝的認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-165">The credentials supplied to the package were not recognized.</span></span>             |

## <a name="remarks"></a><span data-ttu-id="e441f-166">備註</span><span class="sxs-lookup"><span data-stu-id="e441f-166">Remarks</span></span>

<span data-ttu-id="e441f-167">**AcquireCredentialsHandle (CredSSP)** 函數會傳回主體的控制碼，例如使用者或用戶端，以供特定的安全性套件使用。</span><span class="sxs-lookup"><span data-stu-id="e441f-167">The **AcquireCredentialsHandle (CredSSP)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific security package.</span></span> <span data-ttu-id="e441f-168">函數可將控制碼傳回預先存在的認證或新建立的認證，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="e441f-168">The function can return the handle to either preexisting credentials or newly created credentials and return it.</span></span> <span data-ttu-id="e441f-169">這個控制碼可用於對 [**AcceptSecurityCoNtext (credssp)**](acceptsecuritycontext--credssp.md) 的後續呼叫，以及 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="e441f-169">This handle can be used in subsequent calls to the [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) and [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) functions.</span></span>

<span data-ttu-id="e441f-170">一般而言， **AcquireCredentialsHandle (CredSSP)** 不會提供其他登入同一部電腦的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="e441f-170">In general, **AcquireCredentialsHandle (CredSSP)** does not provide the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="e441f-171">不過，具有 SE \_ TCB 名稱許可權的呼叫端 \_ 可以藉由指定該會話 (LUID) 的登入 [*識別碼*](../secgloss/l-gly.md#_security_logon_identifier_gly)，來取得現有登入會話的認證。 [](../secgloss/p-gly.md#_security_privilege_gly)</span><span class="sxs-lookup"><span data-stu-id="e441f-171">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/p-gly.md#_security_privilege_gly) can obtain the credentials of an existing logon session by specifying the [*logon identifier*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) of that session.</span></span> <span data-ttu-id="e441f-172">一般來說，這是由必須代表已登入使用者的核心模式模組所使用。</span><span class="sxs-lookup"><span data-stu-id="e441f-172">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="e441f-173">封裝可能會在 RPC 執行時間傳輸所提供的 *pGetKeyFn* 中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="e441f-173">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="e441f-174">如果傳輸不支援回呼的概念來取得認證，此參數必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e441f-174">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="e441f-175">針對核心模式呼叫端，必須注意下列差異：</span><span class="sxs-lookup"><span data-stu-id="e441f-175">For kernel mode callers, the following differences must be noted:</span></span>

- <span data-ttu-id="e441f-176">這兩個字串參數必須是 [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) 字串。</span><span class="sxs-lookup"><span data-stu-id="e441f-176">The two string parameters must be [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) strings.</span></span>
- <span data-ttu-id="e441f-177">您必須在處理虛擬記憶體（而不是從集區）中配置緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="e441f-177">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="e441f-178">當您完成使用傳回的認證時，請呼叫 [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) 函式來釋放認證所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e441f-178">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e441f-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="e441f-179">Requirements</span></span>

| <span data-ttu-id="e441f-180">需求</span><span class="sxs-lookup"><span data-stu-id="e441f-180">Requirement</span></span> | <span data-ttu-id="e441f-181">值</span><span class="sxs-lookup"><span data-stu-id="e441f-181">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e441f-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e441f-182">Minimum supported client</span></span> | <span data-ttu-id="e441f-183">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e441f-183">Windows Vista \[desktop apps only\]</span></span>                                              |
| <span data-ttu-id="e441f-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e441f-184">Minimum supported server</span></span> | <span data-ttu-id="e441f-185">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e441f-185">Windows Server 2008 \[desktop apps only\]</span></span>                                        |
| <span data-ttu-id="e441f-186">標頭</span><span class="sxs-lookup"><span data-stu-id="e441f-186">Header</span></span>                   | <span data-ttu-id="e441f-187">Sspi (包含 Security .h) </span><span class="sxs-lookup"><span data-stu-id="e441f-187">Sspi.h (include Security.h)</span></span>                                                      |
| <span data-ttu-id="e441f-188">程式庫</span><span class="sxs-lookup"><span data-stu-id="e441f-188">Library</span></span>                  | <span data-ttu-id="e441f-189">Secur32 .lib</span><span class="sxs-lookup"><span data-stu-id="e441f-189">Secur32.lib</span></span>                                                                      |
| <span data-ttu-id="e441f-190">DLL</span><span class="sxs-lookup"><span data-stu-id="e441f-190">DLL</span></span>                      | <span data-ttu-id="e441f-191">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="e441f-191">Secur32.dll</span></span>                                                                      |
| <span data-ttu-id="e441f-192">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e441f-192">Unicode and ANSI names</span></span>   | <span data-ttu-id="e441f-193">**AcquireCredentialsHandleW** (Unicode) 和 **AcquireCredentialsHandleA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e441f-193">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e441f-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e441f-194">See also</span></span>

- [<span data-ttu-id="e441f-195">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="e441f-195">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="e441f-196">**AcceptSecurityCoNtext (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="e441f-196">**AcceptSecurityContext (CredSSP)**</span></span>](acceptsecuritycontext--credssp.md)
- [<span data-ttu-id="e441f-197">**InitializeSecurityCoNtext (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="e441f-197">**InitializeSecurityContext (CredSSP)**</span></span>](initializesecuritycontext--credssp.md)
- [<span data-ttu-id="e441f-198">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="e441f-198">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

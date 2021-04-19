---
description: 抓取服務帳戶密碼。
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: 'GetServiceAccountPassword 函式 (Secpkg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987700"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="b7565-103">GetServiceAccountPassword 函式</span><span class="sxs-lookup"><span data-stu-id="b7565-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="b7565-104">抓取服務帳戶密碼，可供 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) (ssp) ，例如 Kerberos SSP。</span><span class="sxs-lookup"><span data-stu-id="b7565-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7565-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7565-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="b7565-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7565-107">*AccountName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7565-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-108">群組受管理的服務帳戶之以 Null 結束的帳戶名稱 (gMSA) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7565-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="b7565-109">使用者名稱可以是下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="b7565-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="b7565-110">GMSA 的 SAM 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b7565-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="b7565-111"> (FQDN) 的完整功能變數名稱中的使用者名稱，例如 *DomainName\ * **\\** _UserName_ 或 **www。**_網域_*_.com \\_\ *_名稱_。</span><span class="sxs-lookup"><span data-stu-id="b7565-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="b7565-112">使用者名稱必須只有 SAM 名稱。</span><span class="sxs-lookup"><span data-stu-id="b7565-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="b7565-113">功能變數名稱可以是 DNS 名稱或 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="b7565-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="b7565-114">GMSA 帳戶的隱含使用者主體名稱 (UPN) ，例如 *SomeName \* **@** _Domain_*_.com_*，其中根據隱含 UPN 的定義，*網域 \* \* \* .com\*\* 是實際的網域 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="b7565-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="b7565-115">*DomainName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b7565-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-116">選擇性的以 null 終止的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7565-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="b7565-117">只有 *AccountName* 參數是 SAM 帳戶名稱時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="b7565-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="b7565-118">功能變數名稱只能是 NetBIOS 名稱或完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="b7565-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="b7565-119">*CredFetch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7565-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-120">認證 [**\_ 提取**](cred-fetch.md) 列舉值，指定如何取得認證。</span><span class="sxs-lookup"><span data-stu-id="b7565-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="b7565-121">值</span><span class="sxs-lookup"><span data-stu-id="b7565-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="b7565-122">意義</span><span class="sxs-lookup"><span data-stu-id="b7565-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="b7565-123"><dt>**CredFetchDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="b7565-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="b7565-124">作業系統會先嘗試從本機快取取出密碼（如果不是取得密碼的時候）。</span><span class="sxs-lookup"><span data-stu-id="b7565-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="b7565-125">如果需要提取密碼，則作業系統會聯繫網域控制站，否則會傳回狀態為 success 的任何快取密碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="b7565-126"><dt>**CredFetchDPAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="b7565-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="b7565-127">將本機 DPAPI 認證傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="b7565-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="b7565-128">Ssp 通常不需要使用此值。</span><span class="sxs-lookup"><span data-stu-id="b7565-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="b7565-129"><dt>**CredFetchForced**</dt></span><span class="sxs-lookup"><span data-stu-id="b7565-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="b7565-130">強制作業系統嘗試從網域控制站讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="b7565-131">在密碼變換期間，網域控制站和其他成員主機上的密碼可能已變更，但 gMSA 成員主機會將密碼識別為有效。</span><span class="sxs-lookup"><span data-stu-id="b7565-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="b7565-132">這種情況可能是因為不同網域控制站之間的時鐘誤差問題所造成。</span><span class="sxs-lookup"><span data-stu-id="b7565-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="b7565-133">指定此值時，作業系統會判斷是否可能因為時鐘誤差而可能變更密碼，如果是，則會抓取密碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="b7565-134">否則會傳回快取的認證。</span><span class="sxs-lookup"><span data-stu-id="b7565-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="b7565-135">如果沒有快取的認證，則作業系統會嘗試從網域控制站取得一個。</span><span class="sxs-lookup"><span data-stu-id="b7565-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b7565-136">*FileTimeExpiry* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="b7565-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-137">在輸入時，如果此值為非 null，且不是 **FILETIME**， *FileTimeExpiry* 會包含服務帳戶認證的到期時間（如呼叫端已知）。</span><span class="sxs-lookup"><span data-stu-id="b7565-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="b7565-138">如果 *FileTimeExpiry* 參數與目前的其中一個認證相同，則此呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="b7565-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="b7565-139">在輸出中， *FileTimeExpiry* 參數包含所傳回之認證的到期時間。</span><span class="sxs-lookup"><span data-stu-id="b7565-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="b7565-140">*CurrentPassword* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7565-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-141">GMSA 的目前密碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="b7565-142">*PreviousPassword* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7565-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-143">GMSA 先前的密碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="b7565-144">*FileTimeCurrPwdValidForOutbound* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="b7565-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7565-145">表示目前的密碼對傳出要求有效的時間。</span><span class="sxs-lookup"><span data-stu-id="b7565-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="b7565-146">呼叫端應該將目前的時間與此值進行比較，並使用目前的密碼，只有在目前的時間大於或等於這個參數所傳回的值時才會傳回。</span><span class="sxs-lookup"><span data-stu-id="b7565-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="b7565-147">使用這個參數的目的，是針對在輸出邏輯中沒有重試的呼叫端（例如 NTLM）而設計。</span><span class="sxs-lookup"><span data-stu-id="b7565-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7565-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7565-148">Return value</span></span>

<span data-ttu-id="b7565-149">如果函式成功，則傳回值為「狀態 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="b7565-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="b7565-150">如果函式失敗，則傳回值為 NTSTATUS 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="b7565-151">如需詳細資訊，請參閱 [LSA 原則函數傳回值](management-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b7565-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="b7565-152">您可以使用 [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) 函數，將 NTSTATUS 程式碼轉換為 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7565-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="b7565-153">當您完成使用 *CurrentPassword* 和 *PreviousPassword* 參數中所傳回的緩衝區時，請呼叫 [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) 函式釋放它們。</span><span class="sxs-lookup"><span data-stu-id="b7565-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7565-154">備註</span><span class="sxs-lookup"><span data-stu-id="b7565-154">Remarks</span></span>

<span data-ttu-id="b7565-155">在下列案例中，可以呼叫 **GetServiceAccountPassword** 函數：</span><span class="sxs-lookup"><span data-stu-id="b7565-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="b7565-156">從安全性支援提供者的登入功能 (SSP) ，SSP 應該會偵測到服務 \_ 帳戶 \_ 密碼用來登入實體，而且應該檢查呼叫端是否具有 TCB 許可權或網路服務。</span><span class="sxs-lookup"><span data-stu-id="b7565-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="b7565-157">然後，若要取得最新的認證，SSP 應允許登入程式繼續進行，方法是呼叫 **GetServiceAccountPassword** 函式，並在認證 [**\_ 提取**](cred-fetch.md)列舉中使用 **CredFetchDefault** 值。</span><span class="sxs-lookup"><span data-stu-id="b7565-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="b7565-158">從 [**InitializeSecurityCoNtext**](../SecAuthN/initializesecuritycontext--general.md) 和 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) 呼叫中的 ssp。</span><span class="sxs-lookup"><span data-stu-id="b7565-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="b7565-159">Ssp 應該會偵測到服務 \_ 帳戶 \_ 密碼是用於這些呼叫，而如果呼叫是針對非主要認證，則 SSP 應確定呼叫端具有 TCB 許可權或為網路服務。</span><span class="sxs-lookup"><span data-stu-id="b7565-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="b7565-160">然後，SSP 應以認證 [**\_ 提取**](cred-fetch.md)列舉中的 **CredFetchDefault** 值呼叫 **GetServiceAccountPassword** 函式，然後繼續進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="b7565-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="b7565-161">如果 **InitializeSecurityCoNtext** 和 **AcceptSecurityCoNtext** 呼叫失敗，則 SSP 應使用從上一個呼叫中取出的 FileTimeExpiry，然後 **使用** 該做為輸入，以使用認證 **\_ 提取** 列舉中的 **GetServiceAccountPassword** 值再次呼叫 **CredFetchForced** 。</span><span class="sxs-lookup"><span data-stu-id="b7565-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="b7565-162">如果有新的 gMSA 認證可用，則第二次呼叫會成功，並提供新的認證，然後 SSP 應以新的認證重試。</span><span class="sxs-lookup"><span data-stu-id="b7565-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7565-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7565-163">Requirements</span></span>



| <span data-ttu-id="b7565-164">需求</span><span class="sxs-lookup"><span data-stu-id="b7565-164">Requirement</span></span> | <span data-ttu-id="b7565-165">值</span><span class="sxs-lookup"><span data-stu-id="b7565-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7565-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7565-166">Minimum supported client</span></span><br/> | <span data-ttu-id="b7565-167">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7565-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b7565-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7565-168">Minimum supported server</span></span><br/> | <span data-ttu-id="b7565-169">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7565-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7565-170">標頭</span><span class="sxs-lookup"><span data-stu-id="b7565-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7565-171"><dt>Secpkg。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7565-171"><dt>Secpkg.h</dt></span></span> </dl> |



 


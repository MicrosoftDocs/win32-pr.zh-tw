---
title: 'NAP 錯誤常數 (Winerror.h .h) '
description: 下列 NAP 錯誤常數定義于 Winerror.h 中。
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934872"
---
# <a name="nap-error-constants"></a><span data-ttu-id="d55f2-103">NAP 錯誤常數</span><span class="sxs-lookup"><span data-stu-id="d55f2-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="d55f2-104">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d55f2-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d55f2-105">下列 NAP 錯誤常數定義于 Winerror.h 中。</span><span class="sxs-lookup"><span data-stu-id="d55f2-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="d55f2-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E \_ 不正確封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="d55f2-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-107">\_HRESULT \_ TYPEDEF \_ (0x80270001L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-108">NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包無效。</span><span class="sxs-lookup"><span data-stu-id="d55f2-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ 遺失 \_ SOH**</span><span class="sxs-lookup"><span data-stu-id="d55f2-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-110">\_HRESULT \_ TYPEDEF \_ (0x80270002L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-111">NAP 封包中缺少 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="d55f2-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP \_ E \_ 衝突 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d55f2-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-113">\_HRESULT \_ TYPEDEF \_ (0x80270003L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-114">實體識別碼與已註冊的實體識別碼衝突。</span><span class="sxs-lookup"><span data-stu-id="d55f2-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E 沒有快取的 \_ \_ \_ SOH**</span><span class="sxs-lookup"><span data-stu-id="d55f2-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-116">\_HRESULT \_ TYPEDEF \_ (0x80270004L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-117">沒有快取的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 存在。</span><span class="sxs-lookup"><span data-stu-id="d55f2-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ 仍系結 \_**</span><span class="sxs-lookup"><span data-stu-id="d55f2-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-119">\_HRESULT \_ TYPEDEF \_ (0x80270005L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-120">實體仍系結至 NAP 系統。</span><span class="sxs-lookup"><span data-stu-id="d55f2-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="d55f2-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-122">\_HRESULT \_ TYPEDEF \_ (0x80270006L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-123">實體未向 NAP 系統註冊。</span><span class="sxs-lookup"><span data-stu-id="d55f2-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ 未 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="d55f2-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-125">\_HRESULT \_ TYPEDEF \_ (0x80270007L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-126">實體未使用 NAP 系統初始化。</span><span class="sxs-lookup"><span data-stu-id="d55f2-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP \_ E 不符的 \_ \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d55f2-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-128">\_HRESULT \_ TYPEDEF \_ (0x80270008L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-129">[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)要求和 **soh** 回應中的相互關聯識別碼不相符。</span><span class="sxs-lookup"><span data-stu-id="d55f2-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ 未 \_ 擱置**</span><span class="sxs-lookup"><span data-stu-id="d55f2-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-131">\_HRESULT \_ TYPEDEF \_ (0x80270009L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-132">在目前未暫止的要求上指出完成。</span><span class="sxs-lookup"><span data-stu-id="d55f2-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ \_ \_ \_ 找不到 NAP E 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d55f2-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-134">\_HRESULT \_ TYPEDEF \_ (0x8027000AL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-135">找不到 NAP 元件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d55f2-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MAXSIZE \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="d55f2-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-137">\_HRESULT \_ TYPEDEF \_ (0x8027000BL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-138">連接的大小上限對於 SoH 封包而言太小。</span><span class="sxs-lookup"><span data-stu-id="d55f2-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP \_ E \_ 服務 \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="d55f2-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-140">\_HRESULT \_ TYPEDEF \_ (0x8027000CL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-141">NapAgent 服務未執行。</span><span class="sxs-lookup"><span data-stu-id="d55f2-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP \_ S \_ 憑證 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="d55f2-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-143">\_HRESULT \_ TYPEDEF \_ (0x0027000DL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="d55f2-144">憑證已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="d55f2-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_ \_ \_ 已停用 NAP E 實體**</span><span class="sxs-lookup"><span data-stu-id="d55f2-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-146">\_HRESULT \_ TYPEDEF \_ (0x8027000EL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-147">已停用 NapAgent 服務的實體。</span><span class="sxs-lookup"><span data-stu-id="d55f2-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP \_ E \_ NETSH \_ GROUPPOLICY \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d55f2-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-149">\_HRESULT \_ TYPEDEF \_ (0x8027000FL) </span><span class="sxs-lookup"><span data-stu-id="d55f2-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-150">未設定群組原則。</span><span class="sxs-lookup"><span data-stu-id="d55f2-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ 電子 \_ \_ 通話太多 \_**</span><span class="sxs-lookup"><span data-stu-id="d55f2-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-152">\_HRESULT \_ TYPEDEF \_ (0x80270010L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-153">同時呼叫太多。</span><span class="sxs-lookup"><span data-stu-id="d55f2-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP \_ E \_ SHV 設定已 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="d55f2-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-155">\_HRESULT \_ TYPEDEF \_ (0x80270011L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-156">SHV 設定已經存在。</span><span class="sxs-lookup"><span data-stu-id="d55f2-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="d55f2-157">在 Windows 7 或更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d55f2-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</span><span class="sxs-lookup"><span data-stu-id="d55f2-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-159">\_HRESULT \_ TYPEDEF \_ (0x80270012L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-160">找不到 SHV 設定。</span><span class="sxs-lookup"><span data-stu-id="d55f2-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="d55f2-161">在 Windows 7 或更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d55f2-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d55f2-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP \_ E \_ SHV \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="d55f2-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d55f2-163">\_HRESULT \_ TYPEDEF \_ (0x80270013L) </span><span class="sxs-lookup"><span data-stu-id="d55f2-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="d55f2-164">SHV 在要求時過期。</span><span class="sxs-lookup"><span data-stu-id="d55f2-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="d55f2-165">在 Windows 7 或更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d55f2-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d55f2-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="d55f2-166">Requirements</span></span>



| <span data-ttu-id="d55f2-167">需求</span><span class="sxs-lookup"><span data-stu-id="d55f2-167">Requirement</span></span> | <span data-ttu-id="d55f2-168">值</span><span class="sxs-lookup"><span data-stu-id="d55f2-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d55f2-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d55f2-169">Minimum supported client</span></span><br/> | <span data-ttu-id="d55f2-170">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d55f2-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d55f2-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d55f2-171">Minimum supported server</span></span><br/> | <span data-ttu-id="d55f2-172">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d55f2-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d55f2-173">標頭</span><span class="sxs-lookup"><span data-stu-id="d55f2-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="d55f2-174"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="d55f2-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55f2-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d55f2-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55f2-176">**NAP 常數**</span><span class="sxs-lookup"><span data-stu-id="d55f2-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 






---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼9000-11999，適用于開發人員。
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: '系統錯誤碼 (9000-11999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688867"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="eee97-103">系統錯誤碼 (9000-11999) </span><span class="sxs-lookup"><span data-stu-id="eee97-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="eee97-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="eee97-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="eee97-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="eee97-106">下列清單描述 (錯誤9000到 11999) 的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="eee97-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="eee97-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="eee97-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="eee97-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="eee97-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="eee97-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS \_ 錯誤 \_ RCODE \_ 格式 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-110">9001 (0x2329) </span><span class="sxs-lookup"><span data-stu-id="eee97-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-111">DNS 伺服器無法解讀格式。</span><span class="sxs-lookup"><span data-stu-id="eee97-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS \_ 錯誤 \_ RCODE \_ 伺服器 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-113">9002 (0x232A) </span><span class="sxs-lookup"><span data-stu-id="eee97-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-114">DNS 伺服器失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS \_ 錯誤 \_ RCODE \_ 名稱 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-116">9003 (0x232B) </span><span class="sxs-lookup"><span data-stu-id="eee97-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-117">DNS 名稱不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS \_ 錯誤 \_ RCODE \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="eee97-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-119">9004 (0x232C) </span><span class="sxs-lookup"><span data-stu-id="eee97-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-120">名稱伺服器不支援 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="eee97-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_拒絕 DNS 錯誤 \_ RCODE \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-122">9005 (0x232D) </span><span class="sxs-lookup"><span data-stu-id="eee97-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-123">DNS 操作拒絕。</span><span class="sxs-lookup"><span data-stu-id="eee97-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS \_ 錯誤 \_ RCODE \_ YXDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="eee97-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-125">9006 (0x232E) </span><span class="sxs-lookup"><span data-stu-id="eee97-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-126">存在的 DNS 名稱不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS \_ 錯誤 \_ RCODE \_ YXRRSET**</span><span class="sxs-lookup"><span data-stu-id="eee97-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-128">9007 (0x232F) </span><span class="sxs-lookup"><span data-stu-id="eee97-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-129">不應該存在的 DNS RR 設定存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS \_ 錯誤 \_ RCODE \_ NXRRSET**</span><span class="sxs-lookup"><span data-stu-id="eee97-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-131">9008 (0x2330) </span><span class="sxs-lookup"><span data-stu-id="eee97-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-132">應存在的 DNS RR 設定不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS \_ 錯誤 \_ RCODE \_ NOTAUTH**</span><span class="sxs-lookup"><span data-stu-id="eee97-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-134">9009 (0x2331) </span><span class="sxs-lookup"><span data-stu-id="eee97-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-135">DNS 伺服器未授權區域。</span><span class="sxs-lookup"><span data-stu-id="eee97-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS \_ 錯誤 \_ RCODE \_ NOTZONE**</span><span class="sxs-lookup"><span data-stu-id="eee97-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-137">9010 (0x2332) </span><span class="sxs-lookup"><span data-stu-id="eee97-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-138">Update 或 >prereq 中的 DNS 名稱不在區域中。</span><span class="sxs-lookup"><span data-stu-id="eee97-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS \_ 錯誤 \_ RCODE \_ BADSIG**</span><span class="sxs-lookup"><span data-stu-id="eee97-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-140">9016 (0x2338) </span><span class="sxs-lookup"><span data-stu-id="eee97-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-141">DNS 簽章無法驗證。</span><span class="sxs-lookup"><span data-stu-id="eee97-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS \_ 錯誤 \_ RCODE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="eee97-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-143">9017 (0x2339) </span><span class="sxs-lookup"><span data-stu-id="eee97-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-144">DNS 錯誤的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="eee97-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS \_ 錯誤 \_ RCODE \_ BADTIME**</span><span class="sxs-lookup"><span data-stu-id="eee97-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-146">9018 (0x233A) </span><span class="sxs-lookup"><span data-stu-id="eee97-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-147">DNS 簽名碼有效期限已過期。</span><span class="sxs-lookup"><span data-stu-id="eee97-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**\_需要 DNS 錯誤 \_ KEYMASTER \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-149">9101 (0x238D) </span><span class="sxs-lookup"><span data-stu-id="eee97-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-150">只有作為區域金鑰主機的 DNS 伺服器，才能執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_ \_ \_ \_ \_ 簽署的 \_ 區域不允許 DNS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-152">9102 (0x238E) </span><span class="sxs-lookup"><span data-stu-id="eee97-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-153">這項作業不能用於已簽署或有簽署金鑰的區域。</span><span class="sxs-lookup"><span data-stu-id="eee97-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS \_ 錯誤 \_ NSEC3 \_ \_ 與 \_ RSA \_ SHA1 不相容**</span><span class="sxs-lookup"><span data-stu-id="eee97-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-155">9103 (0x238F) </span><span class="sxs-lookup"><span data-stu-id="eee97-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-156">NSEC3 與 RSA-SHA-1 演算法不相容。</span><span class="sxs-lookup"><span data-stu-id="eee97-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="eee97-157">選擇不同的演算法或使用 NSEC。</span><span class="sxs-lookup"><span data-stu-id="eee97-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="eee97-158">此值也稱為 **DNS \_ ERROR 無效 \_ 的 \_ NSEC3 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="eee97-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS \_ 錯誤 \_ 沒有 \_ 足夠的 \_ 簽署 \_ 金鑰 \_ 描述元**</span><span class="sxs-lookup"><span data-stu-id="eee97-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-160">9104 (0x2390) </span><span class="sxs-lookup"><span data-stu-id="eee97-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-161">區域沒有足夠的簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="eee97-162">至少必須有一個金鑰簽署金鑰 (KSK) ，以及至少一個 (ZSK) 的區域簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS \_ 錯誤 \_ 不支援的 \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="eee97-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-164">9105 (0x2391) </span><span class="sxs-lookup"><span data-stu-id="eee97-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-165">不支援指定的演算法。</span><span class="sxs-lookup"><span data-stu-id="eee97-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS \_ 錯誤 \_ 的 \_ 金鑰 \_ 大小無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-167">9106 (0x2392) </span><span class="sxs-lookup"><span data-stu-id="eee97-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-168">不支援指定的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="eee97-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_ \_ \_ \_ 無法存取 DNS 錯誤簽署 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="eee97-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-170">9107 (0x2393) </span><span class="sxs-lookup"><span data-stu-id="eee97-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-171">DNS 伺服器無法存取區域的一或多個簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="eee97-172">在解決此錯誤之前，區域簽署將無法運作。</span><span class="sxs-lookup"><span data-stu-id="eee97-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS \_ 錯誤 \_ KSP \_ 不 \_ \_ 支援 \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="eee97-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-174">9108 (0x2394) </span><span class="sxs-lookup"><span data-stu-id="eee97-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-175">指定的金鑰儲存提供者不支援 DPAPI + + 資料保護。</span><span class="sxs-lookup"><span data-stu-id="eee97-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="eee97-176">在解決此錯誤之前，區域簽署將無法運作。</span><span class="sxs-lookup"><span data-stu-id="eee97-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS \_ 錯誤未 \_ 預期的 \_ 資料 \_ 保護 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-178">9109 (0x2395) </span><span class="sxs-lookup"><span data-stu-id="eee97-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-179">遇到非預期的 DPAPI + + 錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="eee97-180">在解決此錯誤之前，區域簽署將無法運作。</span><span class="sxs-lookup"><span data-stu-id="eee97-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS \_ 錯誤非 \_ 預期的 \_ CNG \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-182">9110 (0x2396) </span><span class="sxs-lookup"><span data-stu-id="eee97-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-183">遇到未預期的加密錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="eee97-184">在解決此錯誤之前，區域簽署可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="eee97-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS \_ 錯誤 \_ 未知的 \_ 簽署 \_ 參數 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="eee97-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-186">9111 (0x2397) </span><span class="sxs-lookup"><span data-stu-id="eee97-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-187">DNS 伺服器發現具有未知版本的簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="eee97-188">在解決此錯誤之前，區域簽署將無法運作。</span><span class="sxs-lookup"><span data-stu-id="eee97-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_ \_ \_ 無法存取 DNS 錯誤 \_ KSP**</span><span class="sxs-lookup"><span data-stu-id="eee97-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-190">9112 (0x2398) </span><span class="sxs-lookup"><span data-stu-id="eee97-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-191">DNS 伺服器無法開啟指定的金鑰服務提供者。</span><span class="sxs-lookup"><span data-stu-id="eee97-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS \_ 錯誤 \_ 太 \_ 多 \_ SKD**</span><span class="sxs-lookup"><span data-stu-id="eee97-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-193">9113 (0x2399) </span><span class="sxs-lookup"><span data-stu-id="eee97-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-194">DNS 伺服器無法接受具有此區域指定演算法和 KSK 旗標值的其他任何簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS \_ 錯誤 \_ 的 \_ 變換 \_ 期間無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-196">9114 (0x239A) </span><span class="sxs-lookup"><span data-stu-id="eee97-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-197">指定的變換期間無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS \_ 錯誤 \_ 的 \_ 初始 \_ 變換 \_ 位移無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-199">9115 (0x239B) </span><span class="sxs-lookup"><span data-stu-id="eee97-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-200">指定的初始變換位移無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS \_ 錯誤 \_ 變換 \_ 正在 \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="eee97-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-202">9116 (0x239C) </span><span class="sxs-lookup"><span data-stu-id="eee97-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-203">指定的簽署金鑰已在變換金鑰的過程中。</span><span class="sxs-lookup"><span data-stu-id="eee97-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS \_ 錯誤 \_ 待命 \_ 金鑰 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-205">9117 (0x239D) </span><span class="sxs-lookup"><span data-stu-id="eee97-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-206">指定的簽署金鑰沒有要撤銷的待命金鑰。</span><span class="sxs-lookup"><span data-stu-id="eee97-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_ \_ \_ ZSK 上不允許 \_ DNS \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-208">9118 (0x239E) </span><span class="sxs-lookup"><span data-stu-id="eee97-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-209"> (ZSK) 的區域簽署金鑰上不允許此作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_ \_ \_ \_ \_ 主動 \_ SKD 上不允許 DNS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-211">9119 (0x239F) </span><span class="sxs-lookup"><span data-stu-id="eee97-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-212">使用中的簽署金鑰不允許進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS \_ 錯誤 \_ 變換 \_ 已 \_ 排入佇列**</span><span class="sxs-lookup"><span data-stu-id="eee97-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-214">9120 (0x23A0) </span><span class="sxs-lookup"><span data-stu-id="eee97-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-215">指定的簽署金鑰已排入佇列進行變換。</span><span class="sxs-lookup"><span data-stu-id="eee97-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_ \_ 未 \_ \_ \_ 簽署的 \_ 區域上不允許 DNS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-217">9121 (0x23A1) </span><span class="sxs-lookup"><span data-stu-id="eee97-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-218">不允許在未簽署的區域上執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS \_ 錯誤 \_ 錯誤 \_ KEYMASTER**</span><span class="sxs-lookup"><span data-stu-id="eee97-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-220">9122 (0x23A2) </span><span class="sxs-lookup"><span data-stu-id="eee97-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-221">無法完成此操作，因為列為此區域目前金鑰主機的 DNS 伺服器已關閉或設定不正確。</span><span class="sxs-lookup"><span data-stu-id="eee97-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="eee97-222">請解決此區域目前金鑰主機上的問題，或使用另一部 DNS 伺服器來佔用金鑰主機角色。</span><span class="sxs-lookup"><span data-stu-id="eee97-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS \_ 錯誤不正確簽章 \_ \_ \_ 有效 \_ 期間**</span><span class="sxs-lookup"><span data-stu-id="eee97-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-224">9123 (0x23A3) </span><span class="sxs-lookup"><span data-stu-id="eee97-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-225">指定的簽章有效期間無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS \_ 錯誤 \_ 不正確 \_ NSEC3 \_ 反覆運算 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="eee97-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-227">9124 (0x23A4) </span><span class="sxs-lookup"><span data-stu-id="eee97-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-228">指定的 NSEC3 反覆運算計數高於區域中使用的最小金鑰長度所允許的數目。</span><span class="sxs-lookup"><span data-stu-id="eee97-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS \_ 錯誤 \_ DNSSEC \_ 已 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="eee97-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-230">9125 (0x23A5) </span><span class="sxs-lookup"><span data-stu-id="eee97-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-231">因為 DNS 伺服器已設定為停用 DNSSEC 功能，所以無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="eee97-232">在 DNS 伺服器上啟用 DNSSEC。</span><span class="sxs-lookup"><span data-stu-id="eee97-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS \_ 錯誤 \_ 不正確 \_ XML**</span><span class="sxs-lookup"><span data-stu-id="eee97-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-234">9126 (0x23A6) </span><span class="sxs-lookup"><span data-stu-id="eee97-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-235">無法完成這項作業，因為收到的 XML 資料流程是空的或語法無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS \_ 錯誤 \_ 沒有 \_ 有效的 \_ 信任 \_ 錨點**</span><span class="sxs-lookup"><span data-stu-id="eee97-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-237">9127 (0x23A7) </span><span class="sxs-lookup"><span data-stu-id="eee97-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-238">這項作業已完成，但未新增任何信任錨點，因為收到的所有信賴起點都無效、不受支援、已過期，或在30天內不會有效。</span><span class="sxs-lookup"><span data-stu-id="eee97-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS \_ 錯誤 \_ 變換 \_ 未 \_ POKEABLE**</span><span class="sxs-lookup"><span data-stu-id="eee97-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-240">9128 (0x23A8) </span><span class="sxs-lookup"><span data-stu-id="eee97-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-241">指定的簽署金鑰未等候家長 DS 更新。</span><span class="sxs-lookup"><span data-stu-id="eee97-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS \_ 錯誤 \_ NSEC3 \_ 名稱 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="eee97-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-243">9129 (0x23A9) </span><span class="sxs-lookup"><span data-stu-id="eee97-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-244">在 NSEC3 簽署期間偵測到雜湊衝突。</span><span class="sxs-lookup"><span data-stu-id="eee97-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="eee97-245">請指定不同的使用者提供 salt，或使用隨機產生的 salt，然後再次嘗試簽署區域。</span><span class="sxs-lookup"><span data-stu-id="eee97-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS \_ 錯誤 \_ NSEC \_ \_ 與 \_ NSEC3 \_ RSA \_ SHA1 不相容**</span><span class="sxs-lookup"><span data-stu-id="eee97-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-247">9130 (0x23AA) </span><span class="sxs-lookup"><span data-stu-id="eee97-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-248">NSEC 與 NSEC3-RSA-SHA-1 演算法不相容。</span><span class="sxs-lookup"><span data-stu-id="eee97-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="eee97-249">選擇不同的演算法或使用 NSEC3。</span><span class="sxs-lookup"><span data-stu-id="eee97-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS \_ 資訊 \_ 沒有 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="eee97-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-251">9501 (0x251D) </span><span class="sxs-lookup"><span data-stu-id="eee97-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-252">沒有找到指定的 DNS 查詢記錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS \_ 錯誤的封 \_ \_ 包錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-254">9502 (0x251E) </span><span class="sxs-lookup"><span data-stu-id="eee97-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-255">錯誤的 DNS 封包。</span><span class="sxs-lookup"><span data-stu-id="eee97-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS \_ 錯誤的封 \_ \_ 包**</span><span class="sxs-lookup"><span data-stu-id="eee97-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-257">9503 (0x251F) </span><span class="sxs-lookup"><span data-stu-id="eee97-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-258">沒有 DNS 封包。</span><span class="sxs-lookup"><span data-stu-id="eee97-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS \_ 錯誤 \_ RCODE**</span><span class="sxs-lookup"><span data-stu-id="eee97-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-260">9504 (0x2520) </span><span class="sxs-lookup"><span data-stu-id="eee97-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-261">DNS 錯誤，請檢查 rcode。</span><span class="sxs-lookup"><span data-stu-id="eee97-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS \_ 錯誤不安全的封 \_ \_ 包**</span><span class="sxs-lookup"><span data-stu-id="eee97-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-263">9505 (0x2521) </span><span class="sxs-lookup"><span data-stu-id="eee97-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-264">不安全的 DNS 封包。</span><span class="sxs-lookup"><span data-stu-id="eee97-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS \_ 要求 \_ 擱置中**</span><span class="sxs-lookup"><span data-stu-id="eee97-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-266">9506 (0x2522) </span><span class="sxs-lookup"><span data-stu-id="eee97-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-267">DNS 查詢要求正在擱置中。</span><span class="sxs-lookup"><span data-stu-id="eee97-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS \_ 錯誤 \_ 的 \_ 類型無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-269">9551 (0x254F) </span><span class="sxs-lookup"><span data-stu-id="eee97-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-270">DNS 類型無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS \_ 錯誤 \_ 不正確 \_ IP \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="eee97-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-272">9552 (0x2550) </span><span class="sxs-lookup"><span data-stu-id="eee97-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-273">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS \_ 錯誤 \_ 的 \_ 屬性無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-275">9553 (0x2551) </span><span class="sxs-lookup"><span data-stu-id="eee97-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-276">屬性無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS \_ 錯誤 \_ 稍後再試一次 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-278">9554 (0x2552) </span><span class="sxs-lookup"><span data-stu-id="eee97-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-279">請稍後再試一次 DNS 操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS \_ 錯誤 \_ 不是 \_ 唯一的**</span><span class="sxs-lookup"><span data-stu-id="eee97-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-281">9555 (0x2553) </span><span class="sxs-lookup"><span data-stu-id="eee97-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-282">指定名稱和類型的記錄不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="eee97-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS \_ 錯誤 \_ 非 \_ RFC \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="eee97-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-284">9556 (0x2554) </span><span class="sxs-lookup"><span data-stu-id="eee97-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-285">DNS 名稱不符合 RFC 規格。</span><span class="sxs-lookup"><span data-stu-id="eee97-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS \_ 狀態 \_ FQDN**</span><span class="sxs-lookup"><span data-stu-id="eee97-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-287">9557 (0x2555) </span><span class="sxs-lookup"><span data-stu-id="eee97-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-288">DNS 名稱是完整的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="eee97-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS \_ 狀態 \_ 點 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="eee97-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-290">9558 (0x2556) </span><span class="sxs-lookup"><span data-stu-id="eee97-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-291">DNS 名稱是點 (多標籤) 。</span><span class="sxs-lookup"><span data-stu-id="eee97-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS \_ 狀態 \_ 單一 \_ 部分 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="eee97-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-293">9559 (0x2557) </span><span class="sxs-lookup"><span data-stu-id="eee97-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-294">DNS 名稱是單一部分的名稱。</span><span class="sxs-lookup"><span data-stu-id="eee97-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS \_ 錯誤 \_ 不正確 \_ 名稱 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="eee97-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-296">9560 (0x2558) </span><span class="sxs-lookup"><span data-stu-id="eee97-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-297">DNS 名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="eee97-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS \_ 錯誤 \_ 數值 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="eee97-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-299">9561 (0x2559) </span><span class="sxs-lookup"><span data-stu-id="eee97-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-300">DNS 名稱完全是數位。</span><span class="sxs-lookup"><span data-stu-id="eee97-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_ \_ \_ \_ \_ 根 \_ 伺服器上不允許 DNS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-302">9562 (0x255A) </span><span class="sxs-lookup"><span data-stu-id="eee97-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-303">DNS 根伺服器上不允許所要求的操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_ \_ \_ 委派下不允許 \_ DNS \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-305">9563 (0x255B) </span><span class="sxs-lookup"><span data-stu-id="eee97-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-306">因為 DNS 命名空間的這個部分已委派給另一部伺服器，所以無法建立記錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS \_ 錯誤找 \_ 不 \_ 到 \_ 根 \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="eee97-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-308">9564 (0x255C) </span><span class="sxs-lookup"><span data-stu-id="eee97-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-309">DNS 伺服器找不到一組根提示。</span><span class="sxs-lookup"><span data-stu-id="eee97-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS \_ 錯誤 \_ 的 \_ 根 \_ 提示不一致**</span><span class="sxs-lookup"><span data-stu-id="eee97-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-311">9565 (0x255D) </span><span class="sxs-lookup"><span data-stu-id="eee97-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-312">DNS 伺服器找到根目錄提示，但它們在所有介面卡之間都不一致。</span><span class="sxs-lookup"><span data-stu-id="eee97-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS \_ 錯誤 \_ DWORD \_ 值 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="eee97-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-314">9566 (0x255E) </span><span class="sxs-lookup"><span data-stu-id="eee97-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-315">指定的值對此參數而言太小。</span><span class="sxs-lookup"><span data-stu-id="eee97-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS \_ 錯誤 \_ DWORD \_ 值 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="eee97-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-317">9567 (0x255F) </span><span class="sxs-lookup"><span data-stu-id="eee97-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-318">指定的值對此參數而言太大。</span><span class="sxs-lookup"><span data-stu-id="eee97-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS \_ 錯誤 \_ 背景 \_ 載入**</span><span class="sxs-lookup"><span data-stu-id="eee97-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-320">9568 (0x2560) </span><span class="sxs-lookup"><span data-stu-id="eee97-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-321">當 DNS 伺服器在背景中載入區域時，不允許此操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="eee97-322">請稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="eee97-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_ \_ \_ RODC 上不允許 \_ DNS \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-324">9569 (0x2561) </span><span class="sxs-lookup"><span data-stu-id="eee97-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-325">針對在唯讀 DC 上執行的 DNS 伺服器，不允許所要求的操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_ \_ \_ \_ 在 DNAME 下不允許 DNS 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-327">9570 (0x2562) </span><span class="sxs-lookup"><span data-stu-id="eee97-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-328">在 DNAME 記錄下不允許有任何資料存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_需要 DNS 錯誤 \_ 委派 \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-330">9571 (0x2563) </span><span class="sxs-lookup"><span data-stu-id="eee97-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-331">此操作需要認證委派。</span><span class="sxs-lookup"><span data-stu-id="eee97-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS \_ 錯誤 \_ 不正確 \_ 原則 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="eee97-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-333">9572 (0x2564) </span><span class="sxs-lookup"><span data-stu-id="eee97-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-334">名稱解析原則資料表已損毀。</span><span class="sxs-lookup"><span data-stu-id="eee97-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="eee97-335">在修正之前，DNS 解析將會失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="eee97-336">請連絡網路系統管理員。</span><span class="sxs-lookup"><span data-stu-id="eee97-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS \_ 錯誤 \_ 區域 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-338">9601 (0x2581) </span><span class="sxs-lookup"><span data-stu-id="eee97-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-339">DNS 區域不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS \_ 錯誤 \_ 沒有 \_ 區域 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="eee97-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-341">9602 (0x2582) </span><span class="sxs-lookup"><span data-stu-id="eee97-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-342">DNS 區域資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="eee97-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS \_ 錯誤 \_ 不正確 \_ 區域 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="eee97-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-344">9603 (0x2583) </span><span class="sxs-lookup"><span data-stu-id="eee97-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-345">DNS 區域的操作無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS \_ 錯誤 \_ 區域 \_ 設定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-347">9604 (0x2584) </span><span class="sxs-lookup"><span data-stu-id="eee97-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-348">DNS 區域設定無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS \_ 錯誤 \_ 區域 \_ \_ 沒有 \_ SOA \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="eee97-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-350">9605 (0x2585) </span><span class="sxs-lookup"><span data-stu-id="eee97-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-351">DNS 區域沒有 (SOA) 記錄的授權啟動。</span><span class="sxs-lookup"><span data-stu-id="eee97-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS \_ 錯誤 \_ 區域 \_ \_ 沒有 \_ NS \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="eee97-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-353">9606 (0x2586) </span><span class="sxs-lookup"><span data-stu-id="eee97-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-354">DNS 區域沒有 (NS) 記錄的名稱伺服器。</span><span class="sxs-lookup"><span data-stu-id="eee97-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS \_ 錯誤 \_ 區域已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="eee97-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-356">9607 (0x2587) </span><span class="sxs-lookup"><span data-stu-id="eee97-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-357">DNS 區域已鎖定。</span><span class="sxs-lookup"><span data-stu-id="eee97-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_建立 DNS \_ 錯誤 \_ 區域 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-359">9608 (0x2588) </span><span class="sxs-lookup"><span data-stu-id="eee97-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-360">DNS 區域建立失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS \_ 錯誤 \_ 區域 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-362">9609 (0x2589) </span><span class="sxs-lookup"><span data-stu-id="eee97-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-363">DNS 區域已存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS \_ 錯誤 \_ AUTOZONE \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-365">9610 (0x258A) </span><span class="sxs-lookup"><span data-stu-id="eee97-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-366">DNS 自動區域已經存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS \_ 錯誤 \_ 不正確 \_ 區域 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="eee97-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-368">9611 (0x258B) </span><span class="sxs-lookup"><span data-stu-id="eee97-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-369">DNS 區欄位型別無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS \_ 錯誤 \_ 次要 \_ 需要 \_ 主要 \_ IP**</span><span class="sxs-lookup"><span data-stu-id="eee97-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-371">9612 (0x258C) </span><span class="sxs-lookup"><span data-stu-id="eee97-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-372">次要 DNS 區域需要主要 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="eee97-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS \_ 錯誤 \_ 區域 \_ 不是 \_ 次要**</span><span class="sxs-lookup"><span data-stu-id="eee97-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-374">9613 (0x258D) </span><span class="sxs-lookup"><span data-stu-id="eee97-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-375">DNS 區域不是次要。</span><span class="sxs-lookup"><span data-stu-id="eee97-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS \_ 錯誤 \_ 需要 \_ 次要 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="eee97-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-377">9614 (0x258E) </span><span class="sxs-lookup"><span data-stu-id="eee97-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-378">需要次要 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="eee97-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS \_ 錯誤 \_ WINS \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-380">9615 (0x258F) </span><span class="sxs-lookup"><span data-stu-id="eee97-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-381">WINS 初始化失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS \_ 錯誤 \_ 需要 \_ WINS \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="eee97-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-383">9616 (0x2590) </span><span class="sxs-lookup"><span data-stu-id="eee97-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-384">需要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eee97-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS \_ 錯誤 \_ NBSTAT \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-386">9617 (0x2591) </span><span class="sxs-lookup"><span data-stu-id="eee97-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-387">NBTSTAT 初始化呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS \_ 錯誤 \_ SOA \_ 刪除 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="eee97-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-389">9618 (0x2592) </span><span class="sxs-lookup"><span data-stu-id="eee97-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-390">不正確 (SOA) 刪除授權啟動。</span><span class="sxs-lookup"><span data-stu-id="eee97-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS \_ 錯誤轉寄站 \_ \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-392">9619 (0x2593) </span><span class="sxs-lookup"><span data-stu-id="eee97-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-393">該名稱已有條件式轉送區域存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS \_ 錯誤 \_ 區域 \_ 需要 \_ 主要 \_ IP**</span><span class="sxs-lookup"><span data-stu-id="eee97-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-395">9620 (0x2594) </span><span class="sxs-lookup"><span data-stu-id="eee97-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-396">此區域必須設定一或多個主要 DNS 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="eee97-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS \_ 錯誤 \_ 區域 \_ 已 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="eee97-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-398">9621 (0x2595) </span><span class="sxs-lookup"><span data-stu-id="eee97-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-399">無法執行操作，因為此區域已關閉。</span><span class="sxs-lookup"><span data-stu-id="eee97-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**已 \_ 鎖定 DNS 錯誤 \_ 區域 \_ \_ 進行 \_ 簽署**</span><span class="sxs-lookup"><span data-stu-id="eee97-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-401">9622 (0x2596) </span><span class="sxs-lookup"><span data-stu-id="eee97-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-402">因為目前正在簽署區域，所以無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="eee97-403">請稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="eee97-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS \_ 錯誤 \_ 主要 \_ 需要 \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="eee97-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-405">9651 (0x25B3) </span><span class="sxs-lookup"><span data-stu-id="eee97-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-406">主要 DNS 區域需要資料檔案。</span><span class="sxs-lookup"><span data-stu-id="eee97-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS \_ 錯誤 \_ 不正確 \_ 資料檔案 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="eee97-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-408">9652 (0x25B4) </span><span class="sxs-lookup"><span data-stu-id="eee97-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-409">DNS 區域的資料檔案名稱無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS \_ 錯誤 \_ 資料檔案 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-411">9653 (0x25B5) </span><span class="sxs-lookup"><span data-stu-id="eee97-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-412">無法開啟 DNS 區域的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="eee97-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS \_ 錯誤 \_ 檔案 \_ 回寫 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-414">9654 (0x25B6) </span><span class="sxs-lookup"><span data-stu-id="eee97-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-415">無法寫入 DNS 區域的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="eee97-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS \_ 錯誤 \_ 資料檔案 \_ 剖析**</span><span class="sxs-lookup"><span data-stu-id="eee97-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-417">9655 (0x25B7) </span><span class="sxs-lookup"><span data-stu-id="eee97-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-418">讀取 DNS 區域的資料檔案時失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS \_ 錯誤 \_ 記錄 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-420">9701 (0x25E5) </span><span class="sxs-lookup"><span data-stu-id="eee97-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-421">DNS 記錄不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS \_ 錯誤 \_ 記錄 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="eee97-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-423">9702 (0x25E6) </span><span class="sxs-lookup"><span data-stu-id="eee97-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-424">DNS 記錄格式錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_建立 DNS \_ 錯誤 \_ 節點 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-426">9703 (0x25E7) </span><span class="sxs-lookup"><span data-stu-id="eee97-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-427">DNS 中的節點建立失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS \_ 錯誤 \_ 未知的 \_ 記錄 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="eee97-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-429">9704 (0x25E8) </span><span class="sxs-lookup"><span data-stu-id="eee97-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-430">未知的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="eee97-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS \_ 錯誤 \_ 記錄 \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-432">9705 (0x25E9) </span><span class="sxs-lookup"><span data-stu-id="eee97-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-433">DNS 記錄超時。</span><span class="sxs-lookup"><span data-stu-id="eee97-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS \_ 錯誤 \_ 名稱 \_ 不 \_ 在 \_ 區域中**</span><span class="sxs-lookup"><span data-stu-id="eee97-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-435">9706 (0x25EA) </span><span class="sxs-lookup"><span data-stu-id="eee97-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-436">名稱不在 DNS 區域中。</span><span class="sxs-lookup"><span data-stu-id="eee97-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS \_ 錯誤 \_ CNAME \_ 迴圈**</span><span class="sxs-lookup"><span data-stu-id="eee97-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-438">9707 (0x25EB) </span><span class="sxs-lookup"><span data-stu-id="eee97-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-439">偵測到 CNAME 迴圈。</span><span class="sxs-lookup"><span data-stu-id="eee97-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS \_ 錯誤 \_ 節點 \_ 為 \_ CNAME**</span><span class="sxs-lookup"><span data-stu-id="eee97-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-441">9708 (0x25EC) </span><span class="sxs-lookup"><span data-stu-id="eee97-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-442">Node 是 CNAME DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS \_ 錯誤 \_ CNAME \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="eee97-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-444">9709 (0x25ED) </span><span class="sxs-lookup"><span data-stu-id="eee97-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-445">已有指定名稱的 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ \_ 只有 \_ 在 \_ 區域 \_ 根目錄的 DNS 錯誤記錄**</span><span class="sxs-lookup"><span data-stu-id="eee97-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-447">9710 (0x25EE) </span><span class="sxs-lookup"><span data-stu-id="eee97-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-448">只記錄在 DNS 區域根。</span><span class="sxs-lookup"><span data-stu-id="eee97-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS \_ 錯誤 \_ 記錄 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-450">9711 (0x25EF) </span><span class="sxs-lookup"><span data-stu-id="eee97-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-451">DNS 記錄已經存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS \_ 錯誤的 \_ 次要 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="eee97-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-453">9712 (0x25F0) </span><span class="sxs-lookup"><span data-stu-id="eee97-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-454">次要 DNS 區域資料錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS \_ 錯誤 \_ 沒有 \_ CREATE \_ CACHE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="eee97-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-456">9713 (0x25F1) </span><span class="sxs-lookup"><span data-stu-id="eee97-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-457">無法建立 DNS 快取資料。</span><span class="sxs-lookup"><span data-stu-id="eee97-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS \_ 錯誤 \_ 名稱 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-459">9714 (0x25F2) </span><span class="sxs-lookup"><span data-stu-id="eee97-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-460">DNS 名稱不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS \_ 警告 \_ PTR \_ 建立 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-462">9715 (0x25F3) </span><span class="sxs-lookup"><span data-stu-id="eee97-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-463">無法 (PTR) 記錄建立指標。</span><span class="sxs-lookup"><span data-stu-id="eee97-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS \_ 警告 \_ 網域取消 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="eee97-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-465">9716 (0x25F4) </span><span class="sxs-lookup"><span data-stu-id="eee97-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-466">DNS 網域已取消刪除。</span><span class="sxs-lookup"><span data-stu-id="eee97-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_ \_ 無法使用 DNS 錯誤 DS \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-468">9717 (0x25F5) </span><span class="sxs-lookup"><span data-stu-id="eee97-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-469">目錄服務無法使用。</span><span class="sxs-lookup"><span data-stu-id="eee97-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS \_ 錯誤 \_ DS \_ 區域 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-471">9718 (0x25F6) </span><span class="sxs-lookup"><span data-stu-id="eee97-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-472">DNS 區域已存在於目錄服務中。</span><span class="sxs-lookup"><span data-stu-id="eee97-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_ \_ \_ \_ 如果 \_ DS \_ 區域，DNS 錯誤無 BOOTFILE**</span><span class="sxs-lookup"><span data-stu-id="eee97-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-474">9719 (0x25F7) </span><span class="sxs-lookup"><span data-stu-id="eee97-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-475">DNS 伺服器不會建立或讀取目錄服務整合式 DNS 區域的開機檔案。</span><span class="sxs-lookup"><span data-stu-id="eee97-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS \_ 錯誤 \_ 節點 \_ 是 \_ DNAME**</span><span class="sxs-lookup"><span data-stu-id="eee97-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-477">9720 (0x25F8) </span><span class="sxs-lookup"><span data-stu-id="eee97-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-478">Node 是 DNAME DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS \_ 錯誤 \_ DNAME \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="eee97-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-480">9721 (0x25F9) </span><span class="sxs-lookup"><span data-stu-id="eee97-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-481">已有指定名稱的 DNAME 記錄存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS \_ 錯誤 \_ 別名 \_ 迴圈**</span><span class="sxs-lookup"><span data-stu-id="eee97-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-483">9722 (0x25FA) </span><span class="sxs-lookup"><span data-stu-id="eee97-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-484">偵測到具有 CNAME 或 DNAME 記錄的別名迴圈。</span><span class="sxs-lookup"><span data-stu-id="eee97-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS \_ 資訊 \_ AXFR \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="eee97-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-486">9751 (0x2617) </span><span class="sxs-lookup"><span data-stu-id="eee97-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-487">DNS AXFR (區域轉送) 完成。</span><span class="sxs-lookup"><span data-stu-id="eee97-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS \_ 錯誤 \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="eee97-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-489">9752 (0x2618) </span><span class="sxs-lookup"><span data-stu-id="eee97-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-490">DNS 區域傳輸失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS \_ 資訊 \_ 已新增 \_ 本機 \_ WINS**</span><span class="sxs-lookup"><span data-stu-id="eee97-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-492">9753 (0x2619) </span><span class="sxs-lookup"><span data-stu-id="eee97-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-493">已新增本機 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eee97-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_ \_ 需要繼續進行 DNS 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-495">9801 (0x2649) </span><span class="sxs-lookup"><span data-stu-id="eee97-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-496">安全更新呼叫需要繼續更新要求。</span><span class="sxs-lookup"><span data-stu-id="eee97-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS \_ 錯誤 \_ 沒有 \_ TCPIP**</span><span class="sxs-lookup"><span data-stu-id="eee97-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-498">9851 (0x267B) </span><span class="sxs-lookup"><span data-stu-id="eee97-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-499">未安裝 TCP/IP 網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="eee97-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS \_ 錯誤 \_ 沒有 \_ DNS \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="eee97-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-501">9852 (0x267C) </span><span class="sxs-lookup"><span data-stu-id="eee97-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-502">未針對本機系統設定任何 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eee97-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS \_ 錯誤 \_ DP \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-504">9901 (0x26AD) </span><span class="sxs-lookup"><span data-stu-id="eee97-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-505">指定的目錄分割不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS \_ 錯誤 \_ DP \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="eee97-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-507">9902 (0x26AE) </span><span class="sxs-lookup"><span data-stu-id="eee97-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-508">指定的目錄分割已存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS \_ 錯誤 \_ DP \_ 未 \_ 登記**</span><span class="sxs-lookup"><span data-stu-id="eee97-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-510">9903 (0x26AF) </span><span class="sxs-lookup"><span data-stu-id="eee97-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-511">此 DNS 伺服器未登錄于指定的目錄分割中。</span><span class="sxs-lookup"><span data-stu-id="eee97-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS \_ 錯誤 \_ DP \_ 已 \_ 登記**</span><span class="sxs-lookup"><span data-stu-id="eee97-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-513">9904 (0x26B0) </span><span class="sxs-lookup"><span data-stu-id="eee97-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-514">此 DNS 伺服器已登錄于指定的目錄分割中。</span><span class="sxs-lookup"><span data-stu-id="eee97-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS \_ 錯誤 \_ DP \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="eee97-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-516">9905 (0x26B1) </span><span class="sxs-lookup"><span data-stu-id="eee97-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-517">目錄分割目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="eee97-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="eee97-518">請稍候幾分鐘，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="eee97-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS \_ 錯誤 \_ DP \_ FSMO \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-520">9906 (0x26B2) </span><span class="sxs-lookup"><span data-stu-id="eee97-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-521">因為無法連線到網網域命名主機 FSMO 角色，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="eee97-522">持有網網域命名主機 FSMO 角色的網域控制站已關閉，或無法服務要求或未執行 Windows Server 2003 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="eee97-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="eee97-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-524">10004 (0x2714) </span><span class="sxs-lookup"><span data-stu-id="eee97-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-525">呼叫 WSACancelBlockingCall 時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="eee97-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span><span class="sxs-lookup"><span data-stu-id="eee97-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-527">10009 (0x2719) </span><span class="sxs-lookup"><span data-stu-id="eee97-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-528">提供的檔案控制代碼無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="eee97-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-530">10013 (0x271D) </span><span class="sxs-lookup"><span data-stu-id="eee97-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-531">嘗試以存取權限禁止的方式存取通訊端。</span><span class="sxs-lookup"><span data-stu-id="eee97-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="eee97-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-533">10014 (0x271E) </span><span class="sxs-lookup"><span data-stu-id="eee97-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-534">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="eee97-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="eee97-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-536">10022 (0x2726) </span><span class="sxs-lookup"><span data-stu-id="eee97-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-537">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span><span class="sxs-lookup"><span data-stu-id="eee97-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-539">10024 (0x2728) </span><span class="sxs-lookup"><span data-stu-id="eee97-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-540">開啟的通訊端太多。</span><span class="sxs-lookup"><span data-stu-id="eee97-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="eee97-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-542">10035 (0x2733) </span><span class="sxs-lookup"><span data-stu-id="eee97-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-543">無法立即完成非封鎖通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="eee97-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-545">10036 (0x2734) </span><span class="sxs-lookup"><span data-stu-id="eee97-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-546">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span><span class="sxs-lookup"><span data-stu-id="eee97-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-548">10037 (0x2735) </span><span class="sxs-lookup"><span data-stu-id="eee97-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-549">嘗試在操作中的非封鎖通訊端上執行操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="eee97-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-551">10038 (0x2736) </span><span class="sxs-lookup"><span data-stu-id="eee97-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-552">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="eee97-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-554">10039 (0x2737) </span><span class="sxs-lookup"><span data-stu-id="eee97-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-555">已從通訊端上的作業省略必要的位址。</span><span class="sxs-lookup"><span data-stu-id="eee97-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="eee97-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-557">10040 (0x2738) </span><span class="sxs-lookup"><span data-stu-id="eee97-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-558">資料包通訊端上傳送的郵件超過內部郵件緩衝區容量或其他一些網路限制，或用來接收資料包的緩衝區容量小於資料包本身。</span><span class="sxs-lookup"><span data-stu-id="eee97-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="eee97-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-560">10041 (0x2739) </span><span class="sxs-lookup"><span data-stu-id="eee97-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-561">在通訊端函數呼叫中指定的通訊協定不支援所要求之通訊端類型的語法。</span><span class="sxs-lookup"><span data-stu-id="eee97-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="eee97-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-563">10042 (0x273A) </span><span class="sxs-lookup"><span data-stu-id="eee97-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-564">在 getsockopt 或 setsockopt 呼叫中指定了未知、無效或不支援的選項或層級。</span><span class="sxs-lookup"><span data-stu-id="eee97-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="eee97-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-566">10043 (0x273B) </span><span class="sxs-lookup"><span data-stu-id="eee97-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-567">要求的通訊協定尚未設定到系統中，或其不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="eee97-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-569">10044 (0x273C) </span><span class="sxs-lookup"><span data-stu-id="eee97-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-570">這個地址家族中不存在對指定通訊端類型的支援。</span><span class="sxs-lookup"><span data-stu-id="eee97-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="eee97-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-572">10045 (0x273D) </span><span class="sxs-lookup"><span data-stu-id="eee97-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-573">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="eee97-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="eee97-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-575">10046 (0x273E) </span><span class="sxs-lookup"><span data-stu-id="eee97-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-576">通訊協定系列尚未設定為系統，或其不存在。</span><span class="sxs-lookup"><span data-stu-id="eee97-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="eee97-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-578">10047 (0x273F) </span><span class="sxs-lookup"><span data-stu-id="eee97-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-579">使用的位址與要求的通訊協定不相容。</span><span class="sxs-lookup"><span data-stu-id="eee97-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="eee97-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-581">10048 (錯誤碼為 0x2740) </span><span class="sxs-lookup"><span data-stu-id="eee97-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span><span class="sxs-lookup"><span data-stu-id="eee97-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="eee97-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-584">10049 (0x2741) </span><span class="sxs-lookup"><span data-stu-id="eee97-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-585">要求的位址在它的內容中無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="eee97-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-587">10050 (0x2742) </span><span class="sxs-lookup"><span data-stu-id="eee97-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-588">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="eee97-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span><span class="sxs-lookup"><span data-stu-id="eee97-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-590">10051 (0x2743) </span><span class="sxs-lookup"><span data-stu-id="eee97-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-591">已嘗試對無法連線的網路進行通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span><span class="sxs-lookup"><span data-stu-id="eee97-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-593">10052 (0x2744) </span><span class="sxs-lookup"><span data-stu-id="eee97-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-594">連接已中斷，因為在作業進行時偵測到失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="eee97-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-596">10053 (0x2745) </span><span class="sxs-lookup"><span data-stu-id="eee97-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-597">您主機機器中的軟體已中止建立的連接。</span><span class="sxs-lookup"><span data-stu-id="eee97-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="eee97-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-599">10054 (0x2746) </span><span class="sxs-lookup"><span data-stu-id="eee97-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-600">遠端主機已強制關閉一個現有連線。</span><span class="sxs-lookup"><span data-stu-id="eee97-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="eee97-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-602">10055 (0x2747) </span><span class="sxs-lookup"><span data-stu-id="eee97-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-603">無法執行通訊端上的作業，因為系統缺乏足夠的緩衝區空間，或佇列已滿。</span><span class="sxs-lookup"><span data-stu-id="eee97-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span><span class="sxs-lookup"><span data-stu-id="eee97-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-605">10056 (0x2748) </span><span class="sxs-lookup"><span data-stu-id="eee97-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-606">已連線的通訊端上提出了 connect 要求。</span><span class="sxs-lookup"><span data-stu-id="eee97-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="eee97-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-608">10057 (0x2749) </span><span class="sxs-lookup"><span data-stu-id="eee97-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-609">因為未連接通訊端且 (使用 sendto 呼叫在資料包通訊端上傳送時) 未提供位址，所以不允許傳送或接收資料的要求。</span><span class="sxs-lookup"><span data-stu-id="eee97-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="eee97-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-611">10058 (0x274A) </span><span class="sxs-lookup"><span data-stu-id="eee97-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-612">因為先前的關閉呼叫已將該方向的通訊端關閉，所以不允許傳送或接收資料的要求。</span><span class="sxs-lookup"><span data-stu-id="eee97-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span><span class="sxs-lookup"><span data-stu-id="eee97-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-614">10059 (0x274B) </span><span class="sxs-lookup"><span data-stu-id="eee97-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-615">某些核心物件的參考太多。</span><span class="sxs-lookup"><span data-stu-id="eee97-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="eee97-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-617">10060 (0x274C) </span><span class="sxs-lookup"><span data-stu-id="eee97-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-618">連接嘗試失敗，因為連線的合作物件在一段時間後未正確回應，或建立的連線失敗，因為連線的主機無法回應。</span><span class="sxs-lookup"><span data-stu-id="eee97-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span><span class="sxs-lookup"><span data-stu-id="eee97-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-620">10061 (0x274D) </span><span class="sxs-lookup"><span data-stu-id="eee97-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-621">無法進行連接，因為目的電腦主動拒絕連線。</span><span class="sxs-lookup"><span data-stu-id="eee97-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span><span class="sxs-lookup"><span data-stu-id="eee97-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-623">10062 (0x274E) </span><span class="sxs-lookup"><span data-stu-id="eee97-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-624">無法轉譯名稱。</span><span class="sxs-lookup"><span data-stu-id="eee97-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span><span class="sxs-lookup"><span data-stu-id="eee97-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-626">10063 (0x274F) </span><span class="sxs-lookup"><span data-stu-id="eee97-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-627">名稱元件或名稱太長。</span><span class="sxs-lookup"><span data-stu-id="eee97-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span><span class="sxs-lookup"><span data-stu-id="eee97-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-629">10064 (0x2750) </span><span class="sxs-lookup"><span data-stu-id="eee97-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-630">通訊端作業失敗，因為目的地主機已關閉。</span><span class="sxs-lookup"><span data-stu-id="eee97-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span><span class="sxs-lookup"><span data-stu-id="eee97-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-632">10065 (0x2751) </span><span class="sxs-lookup"><span data-stu-id="eee97-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-633">已嘗試對無法連接的主機進行通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="eee97-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span><span class="sxs-lookup"><span data-stu-id="eee97-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-635">10066 (0x2752) </span><span class="sxs-lookup"><span data-stu-id="eee97-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-636">無法移除非空白的目錄。</span><span class="sxs-lookup"><span data-stu-id="eee97-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span><span class="sxs-lookup"><span data-stu-id="eee97-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-638">10067 (0x2753) </span><span class="sxs-lookup"><span data-stu-id="eee97-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-639">Windows 通訊端執行可能會限制可同時使用它的應用程式數目。</span><span class="sxs-lookup"><span data-stu-id="eee97-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span><span class="sxs-lookup"><span data-stu-id="eee97-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-641">10068 (0x2754) </span><span class="sxs-lookup"><span data-stu-id="eee97-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-642">配額不足。</span><span class="sxs-lookup"><span data-stu-id="eee97-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span><span class="sxs-lookup"><span data-stu-id="eee97-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-644">10069 (0x2755) </span><span class="sxs-lookup"><span data-stu-id="eee97-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-645">磁片配額已用盡。</span><span class="sxs-lookup"><span data-stu-id="eee97-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span><span class="sxs-lookup"><span data-stu-id="eee97-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-647">10070 (0x2756) </span><span class="sxs-lookup"><span data-stu-id="eee97-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-648">無法再使用檔案控制代碼參考。</span><span class="sxs-lookup"><span data-stu-id="eee97-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span><span class="sxs-lookup"><span data-stu-id="eee97-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-650">10071 (0x2757) </span><span class="sxs-lookup"><span data-stu-id="eee97-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-651">專案無法在本機使用。</span><span class="sxs-lookup"><span data-stu-id="eee97-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span><span class="sxs-lookup"><span data-stu-id="eee97-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-653">10091 (0x276B) </span><span class="sxs-lookup"><span data-stu-id="eee97-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-654">WSAStartup 目前無法運作，因為它用來提供網路服務的基礎系統目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="eee97-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="eee97-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-656">10092 (0x276C) </span><span class="sxs-lookup"><span data-stu-id="eee97-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-657">不支援所要求的 Windows 通訊端版本。</span><span class="sxs-lookup"><span data-stu-id="eee97-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span><span class="sxs-lookup"><span data-stu-id="eee97-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-659">10093 (0x276D) </span><span class="sxs-lookup"><span data-stu-id="eee97-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-660">可能是應用程式未呼叫 WSAStartup，或 WSAStartup 失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span><span class="sxs-lookup"><span data-stu-id="eee97-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-662">10101 (0x2775) </span><span class="sxs-lookup"><span data-stu-id="eee97-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-663">由 WSARecv 或 WSARecvFrom 傳回，表示遠端方已起始正常關機順序。</span><span class="sxs-lookup"><span data-stu-id="eee97-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span><span class="sxs-lookup"><span data-stu-id="eee97-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-665">10102 (0x2776) </span><span class="sxs-lookup"><span data-stu-id="eee97-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-666">WSALookupServiceNext 不會傳回任何結果。</span><span class="sxs-lookup"><span data-stu-id="eee97-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span><span class="sxs-lookup"><span data-stu-id="eee97-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-668">10103 (0x2777) </span><span class="sxs-lookup"><span data-stu-id="eee97-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-669">呼叫 WSALookupServiceEnd 是在這個呼叫仍在處理時進行。</span><span class="sxs-lookup"><span data-stu-id="eee97-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="eee97-670">呼叫已取消。</span><span class="sxs-lookup"><span data-stu-id="eee97-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span><span class="sxs-lookup"><span data-stu-id="eee97-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-672">10104 (0x2778) </span><span class="sxs-lookup"><span data-stu-id="eee97-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-673">程序呼叫資料表無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span><span class="sxs-lookup"><span data-stu-id="eee97-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-675">10105 (0x2779) </span><span class="sxs-lookup"><span data-stu-id="eee97-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-676">要求的服務提供者無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span><span class="sxs-lookup"><span data-stu-id="eee97-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-678">10106 (0x277A) </span><span class="sxs-lookup"><span data-stu-id="eee97-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-679">無法載入或初始化要求的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="eee97-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="eee97-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-681">10107 (0x277B) </span><span class="sxs-lookup"><span data-stu-id="eee97-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-682">系統呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="eee97-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**\_找不 \_ 到 WSASERVICE**</span><span class="sxs-lookup"><span data-stu-id="eee97-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-684">10108 (0x277C) </span><span class="sxs-lookup"><span data-stu-id="eee97-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-685">沒有已知的服務。</span><span class="sxs-lookup"><span data-stu-id="eee97-685">No such service is known.</span></span> <span data-ttu-id="eee97-686">在指定的命名空間中找不到服務。</span><span class="sxs-lookup"><span data-stu-id="eee97-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**\_找不 \_ 到 WSATYPE**</span><span class="sxs-lookup"><span data-stu-id="eee97-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-688">10109 (0x277D) </span><span class="sxs-lookup"><span data-stu-id="eee97-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-689">找不到指定的類別。</span><span class="sxs-lookup"><span data-stu-id="eee97-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ 否 \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="eee97-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-691">10110 (0x277E) </span><span class="sxs-lookup"><span data-stu-id="eee97-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-692">WSALookupServiceNext 不會傳回任何結果。</span><span class="sxs-lookup"><span data-stu-id="eee97-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E 已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="eee97-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-694">10111 (0x277F) </span><span class="sxs-lookup"><span data-stu-id="eee97-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-695">呼叫 WSALookupServiceEnd 是在這個呼叫仍在處理時進行。</span><span class="sxs-lookup"><span data-stu-id="eee97-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="eee97-696">呼叫已取消。</span><span class="sxs-lookup"><span data-stu-id="eee97-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span><span class="sxs-lookup"><span data-stu-id="eee97-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-698">10112 (0x2780) </span><span class="sxs-lookup"><span data-stu-id="eee97-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-699">資料庫查詢失敗，因為它已被主動拒絕。</span><span class="sxs-lookup"><span data-stu-id="eee97-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**\_找不 \_ 到 WSAHOST**</span><span class="sxs-lookup"><span data-stu-id="eee97-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-701">11001 (0x2AF9) </span><span class="sxs-lookup"><span data-stu-id="eee97-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-702">沒有已知的此類主機。</span><span class="sxs-lookup"><span data-stu-id="eee97-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**\_再次 WSATRY**</span><span class="sxs-lookup"><span data-stu-id="eee97-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-704">11002 (0x2AFA) </span><span class="sxs-lookup"><span data-stu-id="eee97-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-705">這通常為主機名稱解析期間的暫時錯誤，表示本機伺服器未收到授權伺服器的回應。</span><span class="sxs-lookup"><span data-stu-id="eee97-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="eee97-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-707">11003 (0x2AFB) </span><span class="sxs-lookup"><span data-stu-id="eee97-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-708">資料庫查閱期間發生無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="eee97-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-710">11004 (0x2AFC) </span><span class="sxs-lookup"><span data-stu-id="eee97-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-711">要求的名稱有效，但是找不到要求類型的資料。</span><span class="sxs-lookup"><span data-stu-id="eee97-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA \_ QOS \_ 接收者**</span><span class="sxs-lookup"><span data-stu-id="eee97-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-713">11005 (0x2AFD) </span><span class="sxs-lookup"><span data-stu-id="eee97-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-714">至少有一個保留已抵達。</span><span class="sxs-lookup"><span data-stu-id="eee97-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA \_ QOS \_ 寄件者**</span><span class="sxs-lookup"><span data-stu-id="eee97-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-716">11006 (0x2AFE) </span><span class="sxs-lookup"><span data-stu-id="eee97-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-717">至少有一個路徑已抵達。</span><span class="sxs-lookup"><span data-stu-id="eee97-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ QOS \_ 無 \_ 寄件者**</span><span class="sxs-lookup"><span data-stu-id="eee97-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-719">11007 (0x2AFF) </span><span class="sxs-lookup"><span data-stu-id="eee97-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-720">沒有任何寄件者。</span><span class="sxs-lookup"><span data-stu-id="eee97-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA \_ QOS \_ 無 \_ 接收者**</span><span class="sxs-lookup"><span data-stu-id="eee97-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-722">11008 (0x2B00) </span><span class="sxs-lookup"><span data-stu-id="eee97-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-723">沒有任何接收者。</span><span class="sxs-lookup"><span data-stu-id="eee97-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**已 \_ 確認 WSA QOS \_ 要求 \_**</span><span class="sxs-lookup"><span data-stu-id="eee97-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-725">11009 (0x2B01) </span><span class="sxs-lookup"><span data-stu-id="eee97-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-726">保留已確認。</span><span class="sxs-lookup"><span data-stu-id="eee97-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA \_ QOS \_ 許可 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-728">11010 (0x2B02) </span><span class="sxs-lookup"><span data-stu-id="eee97-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-729">因為缺少資源而發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA \_ QOS \_ 原則 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="eee97-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-731">11011 (0x2B03) </span><span class="sxs-lookup"><span data-stu-id="eee97-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-732">因為系統管理原因而遭到拒絕-不正確的認證。</span><span class="sxs-lookup"><span data-stu-id="eee97-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA \_ QOS \_ 不良 \_ 樣式**</span><span class="sxs-lookup"><span data-stu-id="eee97-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-734">11012 (0x2B04) </span><span class="sxs-lookup"><span data-stu-id="eee97-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-735">未知或衝突的樣式。</span><span class="sxs-lookup"><span data-stu-id="eee97-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA \_ QOS \_ 不良 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="eee97-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-737">11013 (0x2B05) </span><span class="sxs-lookup"><span data-stu-id="eee97-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-738">一般 filterspec 或 providerspecific 緩衝區的部分問題。</span><span class="sxs-lookup"><span data-stu-id="eee97-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA \_ QOS \_ 流量 \_ CTRL \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-740">11014 (0x2B06) </span><span class="sxs-lookup"><span data-stu-id="eee97-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-741">Flowspec 某些部分的問題。</span><span class="sxs-lookup"><span data-stu-id="eee97-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA \_ QOS \_ 一般 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-743">11015 (0x2B07) </span><span class="sxs-lookup"><span data-stu-id="eee97-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-744">一般 QOS 錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee97-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ QOS \_ ESERVICETYPE**</span><span class="sxs-lookup"><span data-stu-id="eee97-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-746">11016 (0x2B08) </span><span class="sxs-lookup"><span data-stu-id="eee97-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-747">在 flowspec 中找到無效或無法辨識的服務類型。</span><span class="sxs-lookup"><span data-stu-id="eee97-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA \_ QOS \_ EFLOWSPEC**</span><span class="sxs-lookup"><span data-stu-id="eee97-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-749">11017 (0x2B09) </span><span class="sxs-lookup"><span data-stu-id="eee97-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-750">在 QOS 結構中發現無效或不一致的 flowspec。</span><span class="sxs-lookup"><span data-stu-id="eee97-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ QOS \_ EPROVSPECBUF**</span><span class="sxs-lookup"><span data-stu-id="eee97-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-752">11018 (0x2B0A) </span><span class="sxs-lookup"><span data-stu-id="eee97-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-753">QOS 提供者特定的緩衝區無效。</span><span class="sxs-lookup"><span data-stu-id="eee97-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ QOS \_ EFILTERSTYLE**</span><span class="sxs-lookup"><span data-stu-id="eee97-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-755">11019 (0x2B0B) </span><span class="sxs-lookup"><span data-stu-id="eee97-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-756">使用了不正確 QOS 篩選樣式。</span><span class="sxs-lookup"><span data-stu-id="eee97-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA \_ QOS \_ EFILTERTYPE**</span><span class="sxs-lookup"><span data-stu-id="eee97-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-758">11020 (0x2B0C) </span><span class="sxs-lookup"><span data-stu-id="eee97-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-759">使用了不正確 QOS 篩選類型。</span><span class="sxs-lookup"><span data-stu-id="eee97-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA \_ QOS \_ EFILTERCOUNT**</span><span class="sxs-lookup"><span data-stu-id="eee97-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-761">11021 (0x2B0D) </span><span class="sxs-lookup"><span data-stu-id="eee97-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-762">在 FLOWDESCRIPTOR 中指定了不正確的 QOS FILTERSPECs 數目。</span><span class="sxs-lookup"><span data-stu-id="eee97-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA \_ QOS \_ EOBJLENGTH**</span><span class="sxs-lookup"><span data-stu-id="eee97-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-764">11022 (0x2B0E) </span><span class="sxs-lookup"><span data-stu-id="eee97-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-765">在 QOS 提供者特定的緩衝區中指定了 ObjectLength 欄位不正確物件。</span><span class="sxs-lookup"><span data-stu-id="eee97-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA \_ QOS \_ EFLOWCOUNT**</span><span class="sxs-lookup"><span data-stu-id="eee97-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-767">11023 (0x2B0F) </span><span class="sxs-lookup"><span data-stu-id="eee97-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-768">QOS 結構中指定了不正確數目的流程描述項。</span><span class="sxs-lookup"><span data-stu-id="eee97-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ QOS \_ EUNKOWNPSOBJ**</span><span class="sxs-lookup"><span data-stu-id="eee97-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-770">11024 (0x2B10) </span><span class="sxs-lookup"><span data-stu-id="eee97-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-771">在 QOS 提供者特定的緩衝區中找到無法辨識的物件。</span><span class="sxs-lookup"><span data-stu-id="eee97-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ QOS \_ EPOLICYOBJ**</span><span class="sxs-lookup"><span data-stu-id="eee97-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-773">11025 (0x2B11) </span><span class="sxs-lookup"><span data-stu-id="eee97-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-774">在 QOS 提供者特定的緩衝區中找到不正確原則物件。</span><span class="sxs-lookup"><span data-stu-id="eee97-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ QOS \_ EFLOWDESC**</span><span class="sxs-lookup"><span data-stu-id="eee97-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-776">11026 (0x2B12) </span><span class="sxs-lookup"><span data-stu-id="eee97-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-777">在流程描述項清單中找到不正確 QOS 流程描述項。</span><span class="sxs-lookup"><span data-stu-id="eee97-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ QOS \_ EPSFLOWSPEC**</span><span class="sxs-lookup"><span data-stu-id="eee97-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-779">11027 (0x2B13) </span><span class="sxs-lookup"><span data-stu-id="eee97-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-780">在 QOS 提供者特定的緩衝區中找到無效或不一致的 flowspec。</span><span class="sxs-lookup"><span data-stu-id="eee97-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ QOS \_ EPSFILTERSPEC**</span><span class="sxs-lookup"><span data-stu-id="eee97-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-782">11028 (0x2B14) </span><span class="sxs-lookup"><span data-stu-id="eee97-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-783">在 QOS 提供者特定的緩衝區中找到不正確 FILTERSPEC。</span><span class="sxs-lookup"><span data-stu-id="eee97-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ QOS \_ ESDMODEOBJ**</span><span class="sxs-lookup"><span data-stu-id="eee97-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-785">11029 (0x2B15) </span><span class="sxs-lookup"><span data-stu-id="eee97-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-786">在 QOS 提供者特定緩衝區中找到不正確圖形捨棄模式物件。</span><span class="sxs-lookup"><span data-stu-id="eee97-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ QOS \_ ESHAPERATEOBJ**</span><span class="sxs-lookup"><span data-stu-id="eee97-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-788">11030 (0x2B16) </span><span class="sxs-lookup"><span data-stu-id="eee97-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-789">在 QOS 提供者特定的緩衝區中找到不正確成形率物件。</span><span class="sxs-lookup"><span data-stu-id="eee97-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA \_ QOS \_ 保留的 \_ PETYPE**</span><span class="sxs-lookup"><span data-stu-id="eee97-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-791">11031 (0x2B17) </span><span class="sxs-lookup"><span data-stu-id="eee97-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-792">在 QOS 提供者特定的緩衝區中找到保留的原則元素。</span><span class="sxs-lookup"><span data-stu-id="eee97-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ \_ 找不到 WSA 安全主機**</span><span class="sxs-lookup"><span data-stu-id="eee97-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-794">11032 (0x2B18) </span><span class="sxs-lookup"><span data-stu-id="eee97-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-795">無法安全地得知這類主機。</span><span class="sxs-lookup"><span data-stu-id="eee97-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eee97-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA \_ IPSEC \_ 名稱 \_ 原則 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="eee97-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee97-797">11033 (0x2B19) </span><span class="sxs-lookup"><span data-stu-id="eee97-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="eee97-798">無法新增以名稱為基礎的 IPSEC 原則。</span><span class="sxs-lookup"><span data-stu-id="eee97-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="eee97-799">規格需求</span><span class="sxs-lookup"><span data-stu-id="eee97-799">Requirements</span></span>



| <span data-ttu-id="eee97-800">需求</span><span class="sxs-lookup"><span data-stu-id="eee97-800">Requirement</span></span> | <span data-ttu-id="eee97-801">值</span><span class="sxs-lookup"><span data-stu-id="eee97-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eee97-802">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eee97-802">Minimum supported client</span></span><br/> | <span data-ttu-id="eee97-803">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eee97-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eee97-804">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eee97-804">Minimum supported server</span></span><br/> | <span data-ttu-id="eee97-805">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eee97-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eee97-806">標頭</span><span class="sxs-lookup"><span data-stu-id="eee97-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee97-807"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee97-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee97-808">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eee97-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee97-809">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="eee97-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





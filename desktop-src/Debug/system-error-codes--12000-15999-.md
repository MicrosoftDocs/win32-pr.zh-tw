---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼12000-1599，適用于開發人員。
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: '系統錯誤碼 (12000-15999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468248"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="06a79-103">系統錯誤碼 (12000-15999) </span><span class="sxs-lookup"><span data-stu-id="06a79-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="06a79-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="06a79-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="06a79-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="06a79-106">下列清單描述 (錯誤12000到 15999) 的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="06a79-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="06a79-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="06a79-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="06a79-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="06a79-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="06a79-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**錯誤 \_\_網際網路 \** _</span><span class="sxs-lookup"><span data-stu-id="06a79-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-110">12000-12175 (0x2EE0) </span><span class="sxs-lookup"><span data-stu-id="06a79-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-111">請參閱 [網際網路錯誤碼](../wininet/wininet-errors.md) 和 WinInet。</span><span class="sxs-lookup"><span data-stu-id="06a79-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *錯誤 \_ IPSEC \_ QM \_ 原則 \_ 存在*\*</span><span class="sxs-lookup"><span data-stu-id="06a79-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-113">13000 (0x32C8) </span><span class="sxs-lookup"><span data-stu-id="06a79-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-114">指定的快速模式原則已經存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC QM 原則錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-116">13001 (0x32C9) </span><span class="sxs-lookup"><span data-stu-id="06a79-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-117">找不到指定的快速模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**\_ \_ \_ \_ 使用中 IPSEC QM 原則時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-119">13002 (0x32CA) </span><span class="sxs-lookup"><span data-stu-id="06a79-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-120">正在使用指定的快速模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**\_IPSEC \_ MM \_ 原則 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-122">13003 (0x32CB) </span><span class="sxs-lookup"><span data-stu-id="06a79-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-123">指定的主要模式原則已經存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 原則錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-125">13004 (0x32CC) </span><span class="sxs-lookup"><span data-stu-id="06a79-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-126">找不到指定的主要模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**\_ \_ \_ \_ 使用中 IPSEC MM 原則時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-128">13005 (0x32CD) </span><span class="sxs-lookup"><span data-stu-id="06a79-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-129">正在使用指定的主要模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**\_IPSEC \_ MM \_ 篩選準則 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-131">13006 (0x32CE) </span><span class="sxs-lookup"><span data-stu-id="06a79-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-132">指定的主要模式篩選已經存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 篩選器錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-134">13007 (0x32CF) </span><span class="sxs-lookup"><span data-stu-id="06a79-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-135">找不到指定的主要模式篩選。</span><span class="sxs-lookup"><span data-stu-id="06a79-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**\_IPSEC \_ 傳輸 \_ 篩選準則 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-137">13008 (0x32D0) </span><span class="sxs-lookup"><span data-stu-id="06a79-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-138">指定的傳輸模式篩選已經存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC 傳輸篩選錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-140">13009 (0x32D1) </span><span class="sxs-lookup"><span data-stu-id="06a79-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-141">指定的傳輸模式篩選不存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**\_IPSEC \_ MM \_ 驗證 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-143">13010 (0x32D2) </span><span class="sxs-lookup"><span data-stu-id="06a79-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-144">指定的主要模式驗證清單存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC MM 驗證錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-146">13011 (0x32D3) </span><span class="sxs-lookup"><span data-stu-id="06a79-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-147">找不到指定的主要模式驗證清單。</span><span class="sxs-lookup"><span data-stu-id="06a79-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**\_ \_ \_ \_ 使用中的 IPSEC MM 驗證錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-149">13012 (0x32D4) </span><span class="sxs-lookup"><span data-stu-id="06a79-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-150">正在使用指定的主要模式驗證清單。</span><span class="sxs-lookup"><span data-stu-id="06a79-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設 MM 原則的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-152">13013 (0x32D5) </span><span class="sxs-lookup"><span data-stu-id="06a79-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-153">找不到指定的預設主要模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設值 MM 驗證的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-155">13014 (0x32D6) </span><span class="sxs-lookup"><span data-stu-id="06a79-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-156">找不到指定的預設主要模式驗證清單。</span><span class="sxs-lookup"><span data-stu-id="06a79-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 IPSEC 預設 QM 原則的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-158">13015 (0x32D7) </span><span class="sxs-lookup"><span data-stu-id="06a79-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-159">找不到指定的預設快速模式原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**\_IPSEC 通道 \_ \_ 篩選準則 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-161">13016 (0x32D8) </span><span class="sxs-lookup"><span data-stu-id="06a79-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-162">指定的通道模式篩選器存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**\_ \_ \_ \_ \_ 找不到 IPSEC 通道篩選器錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-164">13017 (0x32D9) </span><span class="sxs-lookup"><span data-stu-id="06a79-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-165">找不到指定的通道模式篩選。</span><span class="sxs-lookup"><span data-stu-id="06a79-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**\_IPSEC \_ MM \_ 篩選暫止 \_ \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-167">13018 (0x32DA) </span><span class="sxs-lookup"><span data-stu-id="06a79-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-168">主要模式篩選正在暫止刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**\_IPSEC \_ 傳輸 \_ 篩選器 \_ 暫止 \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-170">13019 (0x32DB) </span><span class="sxs-lookup"><span data-stu-id="06a79-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-171">傳輸篩選正在暫止刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**\_IPSEC 通道 \_ \_ 篩選暫 \_ 止 \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-173">13020 (0x32DC) </span><span class="sxs-lookup"><span data-stu-id="06a79-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-174">通道篩選器正在等待刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**\_IPSEC \_ MM \_ 原則暫止 \_ \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-176">13021 (0x32DD) </span><span class="sxs-lookup"><span data-stu-id="06a79-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-177">主要模式原則正在等待刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**\_IPSEC \_ MM \_ 驗證暫止 \_ \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-179">13022 (0x32DE) </span><span class="sxs-lookup"><span data-stu-id="06a79-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-180">主要模式驗證配套正在等待刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**\_IPSEC \_ QM \_ 原則暫止 \_ \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-182">13023 (0x32DF) </span><span class="sxs-lookup"><span data-stu-id="06a79-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-183">快速模式原則正在等待刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**已 \_ \_ 剪除 IPSEC MM \_ 原則 \_ 的警告**</span><span class="sxs-lookup"><span data-stu-id="06a79-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-185">13024 (0x32E0) </span><span class="sxs-lookup"><span data-stu-id="06a79-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-186">已成功新增主要模式原則，但不支援某些要求的供應專案。</span><span class="sxs-lookup"><span data-stu-id="06a79-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**已 \_ \_ 剪除 IPSEC QM \_ 原則 \_ 的警告**</span><span class="sxs-lookup"><span data-stu-id="06a79-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-188">13025 (0x32E1) </span><span class="sxs-lookup"><span data-stu-id="06a79-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-189">已成功新增快速模式原則，但不支援某些要求的供應專案。</span><span class="sxs-lookup"><span data-stu-id="06a79-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 開始時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-191">13800 (0x35E8) </span><span class="sxs-lookup"><span data-stu-id="06a79-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-192">\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 開始時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="06a79-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**\_IPSEC \_ IKE \_ 驗證 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-194">13801 (0x35E9) </span><span class="sxs-lookup"><span data-stu-id="06a79-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-195">IKE 驗證認證無法接受。</span><span class="sxs-lookup"><span data-stu-id="06a79-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**錯誤 \_ IPSEC \_ IKE \_ ATTRIB \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-197">13802 (0x35EA) </span><span class="sxs-lookup"><span data-stu-id="06a79-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-198">IKE 安全性屬性是無法接受的。</span><span class="sxs-lookup"><span data-stu-id="06a79-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**\_IPSEC \_ IKE \_ 協商 \_ 暫止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-200">13803 (0x35EB) </span><span class="sxs-lookup"><span data-stu-id="06a79-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-201">正在進行 IKE 協商。</span><span class="sxs-lookup"><span data-stu-id="06a79-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**\_IPSEC \_ IKE \_ 一般 \_ 處理 \_ 錯誤錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-203">13804 (0x35EC) </span><span class="sxs-lookup"><span data-stu-id="06a79-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-204">一般處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**\_IPSEC \_ IKE \_ 超時 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-206">13805 (0x35ED) </span><span class="sxs-lookup"><span data-stu-id="06a79-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-207">協商超時。</span><span class="sxs-lookup"><span data-stu-id="06a79-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**\_IPSEC \_ IKE \_ NO \_ CERT 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-209">13806 (0x35EE) </span><span class="sxs-lookup"><span data-stu-id="06a79-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-210">IKE 無法找到有效的電腦憑證。</span><span class="sxs-lookup"><span data-stu-id="06a79-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="06a79-211">請洽詢您的網路安全性系統管理員，瞭解如何在適當的憑證存放區中安裝有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="06a79-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**\_IPSEC \_ IKE \_ SA \_ 已刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-213">13807 (0x35EF) </span><span class="sxs-lookup"><span data-stu-id="06a79-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-214">建立完成之前，對等刪除 IKE SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**\_IPSEC \_ IKE \_ SA \_ REAPED 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-216">13808 (0x35F0) </span><span class="sxs-lookup"><span data-stu-id="06a79-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-217">已在建立完成之前刪除 IKE SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**錯誤 \_ IPSEC \_ IKE \_ MM \_ 取得 \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="06a79-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-219">13809 (0x35F1) </span><span class="sxs-lookup"><span data-stu-id="06a79-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-220">協調要求在佇列中的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**\_IPSEC \_ IKE \_ QM \_ 取得 \_ 捨棄錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-222">13810 (0x35F2) </span><span class="sxs-lookup"><span data-stu-id="06a79-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-223">協調要求在佇列中的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**\_IPSEC \_ IKE \_ 佇列 \_ 捨棄 \_ 分鐘錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-225">13811 (0x35F3) </span><span class="sxs-lookup"><span data-stu-id="06a79-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-226">協調要求在佇列中的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**\_IPSEC \_ IKE \_ 佇列 \_ 捨棄 \_ \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-228">13812 (0x35F4) </span><span class="sxs-lookup"><span data-stu-id="06a79-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-229">協調要求在佇列中的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**錯誤 \_ IPSEC \_ IKE \_ 捨棄 \_ 沒有 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="06a79-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-231">13813 (0x35F5) </span><span class="sxs-lookup"><span data-stu-id="06a79-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-232">沒有對等的回應。</span><span class="sxs-lookup"><span data-stu-id="06a79-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**錯誤 \_ IPSEC \_ IKE \_ MM \_ 延遲 \_ 下降**</span><span class="sxs-lookup"><span data-stu-id="06a79-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-234">13814 (0x35F6) </span><span class="sxs-lookup"><span data-stu-id="06a79-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-235">協商花費的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**\_IPSEC \_ IKE \_ QM \_ 延遲 \_ 下降錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-237">13815 (0x35F7) </span><span class="sxs-lookup"><span data-stu-id="06a79-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-238">協商花費的時間太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**\_IPSEC \_ IKE \_ 錯誤錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-240">13816 (0x35F8) </span><span class="sxs-lookup"><span data-stu-id="06a79-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-241">發生未知錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**\_IPSEC \_ IKE CRL \_ 錯誤 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-243">13817 (0x35F9) </span><span class="sxs-lookup"><span data-stu-id="06a79-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-244">憑證撤銷檢查失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 金鑰 \_ 使用方式錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-246">13818 (0x35FA) </span><span class="sxs-lookup"><span data-stu-id="06a79-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-247">憑證金鑰使用方式無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**\_IPSEC \_ IKE 無效 \_ 憑證 \_ \_ 類型錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-249">13819 (0x35FB) </span><span class="sxs-lookup"><span data-stu-id="06a79-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-250">不正確憑證類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**\_IPSEC \_ IKE \_ 沒有私用 \_ \_ 金鑰錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-252">13820 (0x35FC) </span><span class="sxs-lookup"><span data-stu-id="06a79-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-253">IKE 協商失敗，因為使用的電腦憑證沒有私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a79-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="06a79-254">IPsec 憑證需要私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a79-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="06a79-255">請洽詢您的網路安全性系統管理員，將取代為具有私密金鑰的憑證。</span><span class="sxs-lookup"><span data-stu-id="06a79-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**\_IPSEC IKE 同時重設 \_ \_ \_ 金鑰錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-257">13821 (0x35FD) </span><span class="sxs-lookup"><span data-stu-id="06a79-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-258">偵測到同時重新建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a79-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**\_IPSEC \_ IKE \_ DH \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-260">13822 (0x35FE) </span><span class="sxs-lookup"><span data-stu-id="06a79-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-261">Diffie-Hellman 計算失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**錯誤 \_ IPSEC \_ IKE \_ 重要 \_ 承載 \_ 無法 \_ 辨識**</span><span class="sxs-lookup"><span data-stu-id="06a79-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-263">13823 (0x35FF) </span><span class="sxs-lookup"><span data-stu-id="06a79-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-264">不知道如何處理重要承載。</span><span class="sxs-lookup"><span data-stu-id="06a79-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**\_IPSEC \_ IKE \_ 無效 \_ 標頭錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-266">13824 (0x3600) </span><span class="sxs-lookup"><span data-stu-id="06a79-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-267">不正確標頭。</span><span class="sxs-lookup"><span data-stu-id="06a79-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 原則錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-269">13825 (0x3601) </span><span class="sxs-lookup"><span data-stu-id="06a79-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-270">未設定任何原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**\_IPSEC \_ IKE \_ 無效 \_ 簽章錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-272">13826 (0x3602) </span><span class="sxs-lookup"><span data-stu-id="06a79-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-273">無法驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="06a79-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**\_IPSEC \_ IKE \_ KERBEROS \_ 錯誤錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-275">13827 (0x3603) </span><span class="sxs-lookup"><span data-stu-id="06a79-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-276">無法使用 Kerberos 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="06a79-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 公開金鑰 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-278">13828 (0x3604) </span><span class="sxs-lookup"><span data-stu-id="06a79-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-279">對等的憑證沒有公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a79-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-281">13829 (0x3605) </span><span class="sxs-lookup"><span data-stu-id="06a79-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-282">處理錯誤承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ SA 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-284">13830 (0x3606) </span><span class="sxs-lookup"><span data-stu-id="06a79-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-285">處理 SA 承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**\_IPSEC \_ IKE \_ 進程 \_ \_ 錯誤的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-287">13831 (0x3607) </span><span class="sxs-lookup"><span data-stu-id="06a79-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-288">處理提案承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 交易錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-290">13832 (0x3608) </span><span class="sxs-lookup"><span data-stu-id="06a79-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-291">處理轉換承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ KE 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-293">13833 (0x3609) </span><span class="sxs-lookup"><span data-stu-id="06a79-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-294">處理 KE 承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 識別碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-296">13834 (0x360A) </span><span class="sxs-lookup"><span data-stu-id="06a79-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-297">處理識別碼承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**\_IPSEC \_ IKE \_ 進程 \_ \_ 錯誤憑證錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-299">13835 (0x360B) </span><span class="sxs-lookup"><span data-stu-id="06a79-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-300">處理憑證承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ CERT \_ 要求時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-302">13836 (0x360C) </span><span class="sxs-lookup"><span data-stu-id="06a79-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-303">處理憑證要求承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**\_IPSEC \_ IKE \_ 進程 \_ ERR \_ 雜湊錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-305">13837 (0x360D) </span><span class="sxs-lookup"><span data-stu-id="06a79-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-306">處理雜湊承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ SIG 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-308">13838 (0x360E) </span><span class="sxs-lookup"><span data-stu-id="06a79-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-309">處理簽章承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ NONCE 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-311">13839 (0x360F) </span><span class="sxs-lookup"><span data-stu-id="06a79-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-312">處理 Nonce 承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 通知時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-314">13840 (0x3610) </span><span class="sxs-lookup"><span data-stu-id="06a79-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-315">處理通知承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-317">13841 (0x3611) </span><span class="sxs-lookup"><span data-stu-id="06a79-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-318">處理刪除承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ 廠商錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-320">13842 (0x3612) </span><span class="sxs-lookup"><span data-stu-id="06a79-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-321">處理 VendorId 承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**\_IPSEC \_ IKE \_ 無效 \_ 承載錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-323">13843 (0x3613) </span><span class="sxs-lookup"><span data-stu-id="06a79-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-324">收到不正確承載。</span><span class="sxs-lookup"><span data-stu-id="06a79-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**\_IPSEC \_ IKE \_ 載入 \_ 軟 \_ SA 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-326">13844 (0x3614) </span><span class="sxs-lookup"><span data-stu-id="06a79-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-327">已載入的軟 SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**\_IPSEC \_ IKE \_ 軟 \_ SA \_ \_ 錯誤的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-329">13845 (0x3615) </span><span class="sxs-lookup"><span data-stu-id="06a79-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-330">軟 SA 已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**\_IPSEC \_ IKE \_ 無效 \_ COOKIE 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-332">13846 (0x3616) </span><span class="sxs-lookup"><span data-stu-id="06a79-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-333">收到不正確 cookie。</span><span class="sxs-lookup"><span data-stu-id="06a79-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**\_IPSEC \_ IKE \_ 沒有 \_ 對等 \_ 憑證錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-335">13847 (0x3617) </span><span class="sxs-lookup"><span data-stu-id="06a79-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-336">對等無法傳送有效的電腦憑證。</span><span class="sxs-lookup"><span data-stu-id="06a79-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**\_IPSEC \_ IKE \_ 對等 \_ CRL 錯誤 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-338">13848 (0x3618) </span><span class="sxs-lookup"><span data-stu-id="06a79-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-339">對等憑證的認證撤銷檢查失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**\_IPSEC \_ IKE \_ 原則 \_ 變更時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-341">13849 (0x3619) </span><span class="sxs-lookup"><span data-stu-id="06a79-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-342">新原則是以舊原則形成的無效 SAs。</span><span class="sxs-lookup"><span data-stu-id="06a79-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**錯誤 \_ IPSEC \_ IKE \_ NO \_ MM \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="06a79-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-344">13850 (0x361A) </span><span class="sxs-lookup"><span data-stu-id="06a79-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-345">沒有可用的主要模式 IKE 原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**\_IPSEC \_ IKE \_ NOTCBPRIV 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-347">13851 (0x361B) </span><span class="sxs-lookup"><span data-stu-id="06a79-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-348">無法啟用 TCB 許可權。</span><span class="sxs-lookup"><span data-stu-id="06a79-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**\_IPSEC \_ IKE \_ SECLOADFAIL 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-350">13852 (0x361C) </span><span class="sxs-lookup"><span data-stu-id="06a79-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-351">無法載入 SECURITY.DLL。</span><span class="sxs-lookup"><span data-stu-id="06a79-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**\_IPSEC \_ IKE \_ FAILSSPINIT 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-353">13853 (0x361D) </span><span class="sxs-lookup"><span data-stu-id="06a79-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-354">無法從 SSPI 取得安全性函數資料表分派位址。</span><span class="sxs-lookup"><span data-stu-id="06a79-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**\_IPSEC \_ IKE \_ FAILQUERYSSP 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-356">13854 (0x361E) </span><span class="sxs-lookup"><span data-stu-id="06a79-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-357">無法查詢 Kerberos 套件以取得權杖大小上限。</span><span class="sxs-lookup"><span data-stu-id="06a79-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**\_IPSEC \_ IKE \_ SRVACQFAIL 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-359">13855 (0x361F) </span><span class="sxs-lookup"><span data-stu-id="06a79-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-360">無法取得 ISAKMP/錯誤 \_ IPSEC IKE 服務的 Kerberos 伺服器認證 \_ 。</span><span class="sxs-lookup"><span data-stu-id="06a79-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="06a79-361">Kerberos 驗證將無法運作。</span><span class="sxs-lookup"><span data-stu-id="06a79-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="06a79-362">最可能的原因是缺少網域成員資格。</span><span class="sxs-lookup"><span data-stu-id="06a79-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="06a79-363">如果您的電腦是工作組的成員，這是正常的。</span><span class="sxs-lookup"><span data-stu-id="06a79-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**\_IPSEC \_ IKE \_ SRVQUERYCRED 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-365">13856 (0x3620) </span><span class="sxs-lookup"><span data-stu-id="06a79-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-366">無法判斷 ISAKMP/錯誤 \_ IPSEC \_ IKE 服務 ([**QUERYCREDENTIALSATTRIBUTES**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)) 的 SSPI 主體名稱。</span><span class="sxs-lookup"><span data-stu-id="06a79-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**\_IPSEC \_ IKE \_ GETSPIFAIL 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-368">13857 (0x3621) </span><span class="sxs-lookup"><span data-stu-id="06a79-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-369">無法從 IPsec 驅動程式取得輸入 SA 的新 SPI。</span><span class="sxs-lookup"><span data-stu-id="06a79-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="06a79-370">最常見的原因是驅動程式沒有正確的篩選。</span><span class="sxs-lookup"><span data-stu-id="06a79-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="06a79-371">檢查您的原則，以驗證篩選準則。</span><span class="sxs-lookup"><span data-stu-id="06a79-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**\_IPSEC \_ IKE \_ 無效 \_ 篩選錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-373">13858 (0x3622) </span><span class="sxs-lookup"><span data-stu-id="06a79-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-374">指定的篩選準則無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**\_IPSEC \_ IKE \_ 記憶體不足 \_ 的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-376">13859 (0x3623) </span><span class="sxs-lookup"><span data-stu-id="06a79-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-377">記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**\_IPSEC \_ IKE \_ 新增 \_ 更新 \_ 金鑰 \_ 失敗的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-379">13860 (0x3624) </span><span class="sxs-lookup"><span data-stu-id="06a79-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-380">無法將安全性關聯新增至 IPsec 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="06a79-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="06a79-381">最常見的原因是 IKE 協商花費的時間太長而無法完成。</span><span class="sxs-lookup"><span data-stu-id="06a79-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="06a79-382">如果問題持續發生，請降低失敗電腦的負載。</span><span class="sxs-lookup"><span data-stu-id="06a79-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**\_IPSEC \_ IKE \_ 無效 \_ 原則錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-384">13861 (0x3625) </span><span class="sxs-lookup"><span data-stu-id="06a79-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-385">原則無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**\_IPSEC \_ IKE \_ 未知 \_ DOI 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-387">13862 (0x3626) </span><span class="sxs-lookup"><span data-stu-id="06a79-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-388">不正確 DOI。</span><span class="sxs-lookup"><span data-stu-id="06a79-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**\_IPSEC \_ IKE \_ 無效 \_ 狀況錯誤的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-390">13863 (0x3627) </span><span class="sxs-lookup"><span data-stu-id="06a79-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-391">不正確情況。</span><span class="sxs-lookup"><span data-stu-id="06a79-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**\_IPSEC \_ IKE \_ DH \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-393">13864 (0x3628) </span><span class="sxs-lookup"><span data-stu-id="06a79-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-394">Diffie-Hellman 失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**\_IPSEC \_ IKE \_ 無效 \_ 群組錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-396">13865 (0x3629) </span><span class="sxs-lookup"><span data-stu-id="06a79-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-397">不正確 Diffie-Hellman 群組。</span><span class="sxs-lookup"><span data-stu-id="06a79-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**\_IPSEC \_ IKE \_ 加密錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-399">13866 (0x362A) </span><span class="sxs-lookup"><span data-stu-id="06a79-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-400">加密承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**\_IPSEC \_ IKE \_ 解密時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-402">13867 (0x362B) </span><span class="sxs-lookup"><span data-stu-id="06a79-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-403">解密承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**\_IPSEC \_ IKE \_ 原則 \_ 相符錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-405">13868 (0x362C) </span><span class="sxs-lookup"><span data-stu-id="06a79-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-406">原則相符錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**\_IPSEC \_ IKE \_ 不支援的 \_ 識別碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-408">13869 (0x362D) </span><span class="sxs-lookup"><span data-stu-id="06a79-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-409">不支援的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**\_IPSEC \_ IKE \_ 無效 \_ 雜湊錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-411">13870 (0x362E) </span><span class="sxs-lookup"><span data-stu-id="06a79-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-412">雜湊驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**\_IPSEC \_ IKE \_ 無效 \_ 雜湊 \_ ALG 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-414">13871 (0x362F) </span><span class="sxs-lookup"><span data-stu-id="06a79-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-415">不正確雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="06a79-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 雜湊 \_ 大小錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-417">13872 (0x3630) </span><span class="sxs-lookup"><span data-stu-id="06a79-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-418">不正確雜湊大小。</span><span class="sxs-lookup"><span data-stu-id="06a79-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**\_IPSEC \_ IKE \_ 無效 \_ 加密 \_ ALG 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-420">13873 (0x3631) </span><span class="sxs-lookup"><span data-stu-id="06a79-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-421">不正確加密演算法。</span><span class="sxs-lookup"><span data-stu-id="06a79-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 驗證 \_ 演算法錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-423">13874 (0x3632) </span><span class="sxs-lookup"><span data-stu-id="06a79-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-424">不正確驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="06a79-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ SIG 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-426">13875 (0x3633) </span><span class="sxs-lookup"><span data-stu-id="06a79-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-427">不正確憑證簽章。</span><span class="sxs-lookup"><span data-stu-id="06a79-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**\_IPSEC \_ IKE \_ 載入 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-429">13876 (0x3634) </span><span class="sxs-lookup"><span data-stu-id="06a79-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-430">載入失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**\_IPSEC \_ IKE \_ RPC \_ 刪除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-432">13877 (0x3635) </span><span class="sxs-lookup"><span data-stu-id="06a79-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-433">已透過 RPC 呼叫刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**\_IPSEC \_ IKE \_ 良性 \_ 重新初始化錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-435">13878 (0x3636) </span><span class="sxs-lookup"><span data-stu-id="06a79-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-436">為了執行重新初始化而建立的暫時狀態。</span><span class="sxs-lookup"><span data-stu-id="06a79-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="06a79-437">這不是真正的失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**\_IPSEC \_ IKE \_ 無效回應程式 \_ \_ 存留期 \_ 通知錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-439">13879 (0x3637) </span><span class="sxs-lookup"><span data-stu-id="06a79-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-440">在回應程式存留期通知中收到的存留期值低於 Windows 2000 設定的最小值。</span><span class="sxs-lookup"><span data-stu-id="06a79-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="06a79-441">請修正對等電腦上的原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 主要 \_ 版本錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-443">13880 (0x3638) </span><span class="sxs-lookup"><span data-stu-id="06a79-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-444">收件者無法處理標頭中指定的 IKE 版本。</span><span class="sxs-lookup"><span data-stu-id="06a79-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**\_IPSEC \_ IKE \_ 無效 \_ CERT \_ KEYLEN 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-446">13881 (0x3639) </span><span class="sxs-lookup"><span data-stu-id="06a79-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-447">憑證中的金鑰長度太小，無法設定安全性需求。</span><span class="sxs-lookup"><span data-stu-id="06a79-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**\_IPSEC \_ IKE \_ MM \_ 限制錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-449">13882 (0x363A) </span><span class="sxs-lookup"><span data-stu-id="06a79-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-450">已超過對等的已建立 MM SAs 數目上限。</span><span class="sxs-lookup"><span data-stu-id="06a79-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**\_ \_ \_ 停用 IPSEC IKE 協商 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-452">13883 (0x363B) </span><span class="sxs-lookup"><span data-stu-id="06a79-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-453">IKE 收到停用協商的原則。</span><span class="sxs-lookup"><span data-stu-id="06a79-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**\_IPSEC \_ IKE \_ QM \_ 限制錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-455">13884 (0x363C) </span><span class="sxs-lookup"><span data-stu-id="06a79-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-456">已達到主要模式的最大快速模式限制。</span><span class="sxs-lookup"><span data-stu-id="06a79-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="06a79-457">將會啟動新的主要模式。</span><span class="sxs-lookup"><span data-stu-id="06a79-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**\_IPSEC \_ IKE \_ MM \_ 過期時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-459">13885 (0x363D) </span><span class="sxs-lookup"><span data-stu-id="06a79-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-460">主要模式 SA 存留期已過期或對等傳送了主要模式刪除。</span><span class="sxs-lookup"><span data-stu-id="06a79-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**\_IPSEC \_ IKE \_ 對等 \_ MM \_ 視為 \_ 不正確錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-462">13886 (0x363E) </span><span class="sxs-lookup"><span data-stu-id="06a79-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-463">主要模式 SA 假設為無效，因為對等已停止回應。</span><span class="sxs-lookup"><span data-stu-id="06a79-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**\_IPSEC \_ IKE 憑證 \_ \_ 鏈 \_ 原則 \_ 不符的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-465">13887 (0x363F) </span><span class="sxs-lookup"><span data-stu-id="06a79-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-466">憑證不會與 IPsec 原則中的根信任連結。</span><span class="sxs-lookup"><span data-stu-id="06a79-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**\_IPSEC \_ IKE 未 \_ 預期的 \_ 訊息 \_ 識別碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-468">13888 (0x3640) </span><span class="sxs-lookup"><span data-stu-id="06a79-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-469">收到未預期的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**\_IPSEC \_ IKE 無效 \_ 的 \_ 驗證 \_ 承載錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-471">13889 (0x3641) </span><span class="sxs-lookup"><span data-stu-id="06a79-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-472">收到不正確驗證優惠。</span><span class="sxs-lookup"><span data-stu-id="06a79-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**\_傳送 IPSEC \_ IKE \_ DOS \_ COOKIE \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-474">13890 (0x3642) </span><span class="sxs-lookup"><span data-stu-id="06a79-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-475">傳送的 DoS cookie 通知給啟動器。</span><span class="sxs-lookup"><span data-stu-id="06a79-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**\_IPSEC \_ IKE \_ 關閉 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-477">13891 (0x3643) </span><span class="sxs-lookup"><span data-stu-id="06a79-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-478">IKE 服務正在關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**\_IPSEC \_ IKE \_ CGA \_ 驗證 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-480">13892 (0x3644) </span><span class="sxs-lookup"><span data-stu-id="06a79-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-481">無法驗證 CGA 位址和憑證之間的系結。</span><span class="sxs-lookup"><span data-stu-id="06a79-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**\_IPSEC \_ IKE 進程 \_ 錯誤 \_ \_ NATOA 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-483">13893 (0x3645) </span><span class="sxs-lookup"><span data-stu-id="06a79-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-484">處理 NatOA 承載時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**\_IPSEC \_ IKE \_ 無效 \_ \_ 的 QM 錯誤 \_ MM**</span><span class="sxs-lookup"><span data-stu-id="06a79-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-486">13894 (0x3646) </span><span class="sxs-lookup"><span data-stu-id="06a79-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-487">主要模式的參數對此快速模式無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**\_IPSEC \_ IKE \_ QM \_ 過期時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-489">13895 (0x3647) </span><span class="sxs-lookup"><span data-stu-id="06a79-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-490">IPsec 驅動程式已過期的快速模式 SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**\_IPSEC \_ IKE \_ 太 \_ 多 \_ 篩選錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-492">13896 (0x3648) </span><span class="sxs-lookup"><span data-stu-id="06a79-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-493">偵測到太多動態新增的 IKEEXT 篩選。</span><span class="sxs-lookup"><span data-stu-id="06a79-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 結束時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-495">13897 (0x3649) </span><span class="sxs-lookup"><span data-stu-id="06a79-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-496">\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 結束時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="06a79-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**\_IPSEC \_ IKE \_ 終止 \_ 虛擬 \_ NAP \_ 通道時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-498">13898 (0x364A) </span><span class="sxs-lookup"><span data-stu-id="06a79-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-499">NAP reauth 成功，必須刪除虛擬 NAP IKEv2 通道。</span><span class="sxs-lookup"><span data-stu-id="06a79-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**\_IPSEC \_ IKE \_ 內部 \_ IP \_ 指派 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-501">13899 (0x364B) </span><span class="sxs-lookup"><span data-stu-id="06a79-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-502">在通道模式中將內部 IP 位址指派給啟動器時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**\_IPSEC \_ IKE \_ 要求 \_ \_ \_ 缺少 CP 承載時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-504">13900 (0x364C) </span><span class="sxs-lookup"><span data-stu-id="06a79-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-505">要求缺少設定承載。</span><span class="sxs-lookup"><span data-stu-id="06a79-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**錯誤 \_ IPSEC \_ KEY \_ MODULE \_ 模擬 \_ 協商 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="06a79-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-507">13901 (0x364D) </span><span class="sxs-lookup"><span data-stu-id="06a79-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-508">以發出連接的安全性準則進行的協商正在進行中。</span><span class="sxs-lookup"><span data-stu-id="06a79-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**\_IPSEC \_ IKE \_ 並存 \_ 隱藏錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-510">13902 (0x364E) </span><span class="sxs-lookup"><span data-stu-id="06a79-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-511">因為 IKEv1/AuthIP 並存隱藏了檢查，所以已刪除 SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**\_IPSEC \_ IKE \_ RATELIMIT \_ 捨棄錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-513">13903 (0x364F) </span><span class="sxs-lookup"><span data-stu-id="06a79-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-514">傳入的 SA 要求因為對等 IP 位址速率限制而被捨棄。</span><span class="sxs-lookup"><span data-stu-id="06a79-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**\_IPSEC \_ IKE 對等錯誤不 \_ \_ \_ 支援 \_ MOBIKE**</span><span class="sxs-lookup"><span data-stu-id="06a79-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-516">13904 (0x3650) </span><span class="sxs-lookup"><span data-stu-id="06a79-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-517">對等不支援 MOBIKE。</span><span class="sxs-lookup"><span data-stu-id="06a79-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**\_IPSEC \_ IKE \_ 授權 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-519">13905 (0x3651) </span><span class="sxs-lookup"><span data-stu-id="06a79-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-520">SA 建立未獲授權。</span><span class="sxs-lookup"><span data-stu-id="06a79-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**\_IPSEC \_ IKE 強 \_ 式 \_ \_ 認證授權 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-522">13906 (0x3652) </span><span class="sxs-lookup"><span data-stu-id="06a79-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-523">因為沒有足夠強式的 PKINIT 認證，所以未授權建立 SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**\_IPSEC \_ IKE \_ 授權 \_ 失敗 \_ 並 \_ 選擇性 \_ 重試錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-525">13907 (0x3653) </span><span class="sxs-lookup"><span data-stu-id="06a79-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-526">SA 建立未獲授權。</span><span class="sxs-lookup"><span data-stu-id="06a79-526">SA establishment is not authorized.</span></span> <span data-ttu-id="06a79-527">您可能需要輸入更新或不同的認證，例如智慧卡。</span><span class="sxs-lookup"><span data-stu-id="06a79-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**\_IPSEC \_ IKE 強 \_ 式 \_ \_ 認證授權 \_ 和 \_ CERTMAP \_ 失敗的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-529">13908 (0x3654) </span><span class="sxs-lookup"><span data-stu-id="06a79-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-530">因為沒有足夠強式的 PKINIT 認證，所以未授權建立 SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="06a79-531">這可能與 SA 的憑證對帳戶對應失敗相關。</span><span class="sxs-lookup"><span data-stu-id="06a79-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 延伸 \_ 結束時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-533">13909 (0x3655) </span><span class="sxs-lookup"><span data-stu-id="06a79-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-534">\_IPSEC \_ IKE \_ >NEG \_ 狀態 \_ 延伸 \_ 結束時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="06a79-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**\_IPSEC 錯誤 \_ \_ SPI 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-536">13910 (0x3656) </span><span class="sxs-lookup"><span data-stu-id="06a79-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-537">封包中的 SPI 不符合有效的 IPsec SA。</span><span class="sxs-lookup"><span data-stu-id="06a79-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**\_IPSEC \_ SA \_ 存留期已 \_ 過期時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-539">13911 (0x3657) </span><span class="sxs-lookup"><span data-stu-id="06a79-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-540">已在存留期過期的 IPsec SA 上收到封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**\_IPSEC 錯誤 \_ 的 \_ SA 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-542">13912 (0x3658) </span><span class="sxs-lookup"><span data-stu-id="06a79-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-543">IPsec SA 接收到的封包不符合封包特性。</span><span class="sxs-lookup"><span data-stu-id="06a79-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**\_IPSEC 重新 \_ 執行 \_ 檢查 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-545">13913 (0x3659) </span><span class="sxs-lookup"><span data-stu-id="06a79-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-546">封包序號重新執行檢查失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**\_IPSEC 不正確封 \_ \_ 包錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-548">13914 (0x365A) </span><span class="sxs-lookup"><span data-stu-id="06a79-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-549">封包中的 IPsec 標頭和/或結尾無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**\_IPSEC \_ 完整性 \_ 檢查 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-551">13915 (0x365B) </span><span class="sxs-lookup"><span data-stu-id="06a79-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-552">IPsec 完整性檢查失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**錯誤 \_ IPSEC \_ 純 \_ 文本 \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="06a79-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-554">13916 (0x365C) </span><span class="sxs-lookup"><span data-stu-id="06a79-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-555">IPsec 卸載了純文字封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**\_IPSEC \_ 驗證 \_ 防火牆 \_ 捨棄錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-557">13917 (0x365D) </span><span class="sxs-lookup"><span data-stu-id="06a79-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-558">IPsec 會以已驗證的防火牆模式卸載傳入的 ESP 封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="06a79-559">這項捨棄是良性的。</span><span class="sxs-lookup"><span data-stu-id="06a79-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**\_IPSEC \_ 節流 \_ 下降錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-561">13918 (0x365E) </span><span class="sxs-lookup"><span data-stu-id="06a79-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-562">IPsec 因 DoS 節流而捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**\_IPSEC \_ DOSP \_ 封鎖錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-564">13925 (0x3665) </span><span class="sxs-lookup"><span data-stu-id="06a79-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-565">IPsec DoS 保護符合明確封鎖規則。</span><span class="sxs-lookup"><span data-stu-id="06a79-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**\_IPSEC \_ DOSP \_ 收到 \_ 多播錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-567">13926 (0x3666) </span><span class="sxs-lookup"><span data-stu-id="06a79-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-568">IPsec DoS 保護收到 IPsec 專屬的多播封包，但這是不允許的。</span><span class="sxs-lookup"><span data-stu-id="06a79-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**\_IPSEC DOSP 不正確封 \_ \_ 包時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-570">13927 (0x3667) </span><span class="sxs-lookup"><span data-stu-id="06a79-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-571">IPsec DoS 保護收到格式不正確的封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**錯誤 \_ IPSEC \_ DOSP \_ 狀態 \_ 查閱 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-573">13928 (0x3668) </span><span class="sxs-lookup"><span data-stu-id="06a79-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-574">IPsec DoS 保護無法查閱狀態。</span><span class="sxs-lookup"><span data-stu-id="06a79-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**\_IPSEC \_ DOSP 的 \_ 專案數上限 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-576">13929 (0x3669) </span><span class="sxs-lookup"><span data-stu-id="06a79-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-577">IPsec DoS 保護無法建立狀態，因為已達到原則允許的最大專案數。</span><span class="sxs-lookup"><span data-stu-id="06a79-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**錯誤 \_ IPSEC \_ DOSP \_ KEYMOD \_ 不 \_ 允許**</span><span class="sxs-lookup"><span data-stu-id="06a79-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-579">13930 (0x366A) </span><span class="sxs-lookup"><span data-stu-id="06a79-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-580">IPsec DoS 保護收到「金鑰」模組的 IPsec 協商封包，但原則不允許此封包。</span><span class="sxs-lookup"><span data-stu-id="06a79-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**\_ \_ \_ 未安裝 IPSEC DOSP \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-582">13931 (0x366B) </span><span class="sxs-lookup"><span data-stu-id="06a79-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-583">尚未啟用 IPsec DoS 保護。</span><span class="sxs-lookup"><span data-stu-id="06a79-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**\_IPSEC \_ DOSP \_ \_ 每個 \_ IP \_ RATELIMIT \_ 佇列的最大錯誤數**</span><span class="sxs-lookup"><span data-stu-id="06a79-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-585">13932 (0x366C) </span><span class="sxs-lookup"><span data-stu-id="06a79-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-586">IPsec DoS 保護無法建立每個內部 IP 速率限制佇列，因為已達到原則允許的最大佇列數目。</span><span class="sxs-lookup"><span data-stu-id="06a79-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 區段**</span><span class="sxs-lookup"><span data-stu-id="06a79-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-588">14000 (0x36B0) </span><span class="sxs-lookup"><span data-stu-id="06a79-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-589">要求的區段不存在於啟用內容中。</span><span class="sxs-lookup"><span data-stu-id="06a79-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**錯誤 \_ SXS 無法進行 \_ \_ GEN \_ ACTCTX**</span><span class="sxs-lookup"><span data-stu-id="06a79-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-591">14001 (0x36B1) </span><span class="sxs-lookup"><span data-stu-id="06a79-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-592">應用程式無法啟動，因為其並存設定不正確。</span><span class="sxs-lookup"><span data-stu-id="06a79-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="06a79-593">如需詳細資訊，請參閱應用程式事件記錄檔或使用命令列 sxstrace.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="06a79-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**錯誤 \_ SXS \_ 不正確 \_ ACTCTXDATA \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="06a79-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-595">14002 (0x36B2) </span><span class="sxs-lookup"><span data-stu-id="06a79-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-596">應用程式系結資料格式無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 元件**</span><span class="sxs-lookup"><span data-stu-id="06a79-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-598">14003 (0x36B3) </span><span class="sxs-lookup"><span data-stu-id="06a79-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-599">未在您的系統上安裝參考的元件。</span><span class="sxs-lookup"><span data-stu-id="06a79-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 格式 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-601">14004 (0x36B4) </span><span class="sxs-lookup"><span data-stu-id="06a79-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-602">資訊清單檔案的開頭不是必要的標記和格式資訊。</span><span class="sxs-lookup"><span data-stu-id="06a79-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 剖析 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-604">14005 (0x36B5) </span><span class="sxs-lookup"><span data-stu-id="06a79-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-605">資訊清單檔案包含一或多個語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**錯誤 \_ SXS \_ 啟用 \_ 內容 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-607">14006 (0x36B6) </span><span class="sxs-lookup"><span data-stu-id="06a79-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-608">應用程式嘗試啟用已停用的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="06a79-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 SXS 索引鍵**</span><span class="sxs-lookup"><span data-stu-id="06a79-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-610">14007 (0x36B7) </span><span class="sxs-lookup"><span data-stu-id="06a79-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-611">在任何使用中的啟用內容中找不到要求的查閱索引鍵。</span><span class="sxs-lookup"><span data-stu-id="06a79-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**錯誤 \_ SXS \_ 版本 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="06a79-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-613">14008 (0x36B8) </span><span class="sxs-lookup"><span data-stu-id="06a79-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-614">應用程式所需的元件版本與另一個已在使用中的元件版本發生衝突。</span><span class="sxs-lookup"><span data-stu-id="06a79-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**錯誤 \_ SXS 錯誤的 \_ \_ 區段 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="06a79-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-616">14009 (0x36B9) </span><span class="sxs-lookup"><span data-stu-id="06a79-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-617">要求的啟用內容區段類型與使用的查詢 API 不符。</span><span class="sxs-lookup"><span data-stu-id="06a79-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**\_停用錯誤 SXS \_ 執行緒 \_ 查詢 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-619">14010 (0x36BA) </span><span class="sxs-lookup"><span data-stu-id="06a79-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-620">缺少系統資源必須針對目前執行中的執行緒停用隔離啟用。</span><span class="sxs-lookup"><span data-stu-id="06a79-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**\_ \_ 已設定錯誤 SXS 進程 \_ 預設值 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-622">14011 (0x36BB) </span><span class="sxs-lookup"><span data-stu-id="06a79-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-623">嘗試設定進程預設啟用內容失敗，因為已設定進程預設啟用內容。</span><span class="sxs-lookup"><span data-stu-id="06a79-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**錯誤 \_ SXS \_ 未知的 \_ 編碼 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="06a79-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-625">14012 (0x36BC) </span><span class="sxs-lookup"><span data-stu-id="06a79-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-626">無法辨識指定的編碼群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**錯誤 \_ SXS \_ 未知的 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="06a79-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-628">14013 (0x36BD) </span><span class="sxs-lookup"><span data-stu-id="06a79-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-629">無法辨識要求的編碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**錯誤 \_ SXS \_ 不正確 \_ XML \_ 命名空間 \_ URI**</span><span class="sxs-lookup"><span data-stu-id="06a79-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-631">14014 (0x36BE) </span><span class="sxs-lookup"><span data-stu-id="06a79-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-632">資訊清單包含無效 URI 的參考。</span><span class="sxs-lookup"><span data-stu-id="06a79-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**\_ \_ \_ \_ \_ 未 \_ 安裝錯誤 SXS 根資訊清單相依性**</span><span class="sxs-lookup"><span data-stu-id="06a79-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-634">14015 (0x36BF) </span><span class="sxs-lookup"><span data-stu-id="06a79-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-635">應用程式資訊清單包含未安裝之相依元件的參考。</span><span class="sxs-lookup"><span data-stu-id="06a79-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**\_未安裝錯誤 SXS 分 \_ 葉 \_ 資訊清單 \_ \_ \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="06a79-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-637">14016 (0x36C0) </span><span class="sxs-lookup"><span data-stu-id="06a79-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-638">應用程式所使用之元件的資訊清單具有未安裝之相依元件的參考。</span><span class="sxs-lookup"><span data-stu-id="06a79-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**錯誤 \_ SXS \_ 不正確 \_ 元件 \_ 標識 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="06a79-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-640">14017 (0x36C1) </span><span class="sxs-lookup"><span data-stu-id="06a79-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-641">資訊清單包含不正確元件身分識別的屬性。</span><span class="sxs-lookup"><span data-stu-id="06a79-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 遺失 \_ 必要的 \_ 預設 \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="06a79-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-643">14018 (0x36C2) </span><span class="sxs-lookup"><span data-stu-id="06a79-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-644">資訊清單遺漏 assembly 元素上所需的預設命名空間規格。</span><span class="sxs-lookup"><span data-stu-id="06a79-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 不正確 \_ 必要 \_ 預設 \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="06a79-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-646">14019 (0x36C3) </span><span class="sxs-lookup"><span data-stu-id="06a79-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-647">資訊清單具有元件元素上指定的預設命名空間，但其值不是 "urn：架構-microsoft-com： asm. v1"。</span><span class="sxs-lookup"><span data-stu-id="06a79-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**錯誤 \_ SXS \_ 私 \_ 用資訊清單 \_ \_ 與重新 \_ \_ 剖析點之間的交互路徑 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-649">14020 (0x36C4) </span><span class="sxs-lookup"><span data-stu-id="06a79-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-650">私用資訊清單探查已跨越具有不支援之重新分析點的路徑。</span><span class="sxs-lookup"><span data-stu-id="06a79-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**錯誤 \_ SXS \_ 重複 \_ DLL \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-652">14021 (0x36C5) </span><span class="sxs-lookup"><span data-stu-id="06a79-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-653">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="06a79-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**錯誤 \_ SXS \_ 重複 \_ WINDOWCLASS \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-655">14022 (0x36C6) </span><span class="sxs-lookup"><span data-stu-id="06a79-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-656">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同名稱的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="06a79-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**錯誤 \_ SXS \_ 重複 \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="06a79-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-658">14023 (0x36C7) </span><span class="sxs-lookup"><span data-stu-id="06a79-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-659">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM 伺服器 Clsid。</span><span class="sxs-lookup"><span data-stu-id="06a79-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**錯誤 \_ SXS \_ 重複 \_ IID**</span><span class="sxs-lookup"><span data-stu-id="06a79-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-661">14024 (0x36C8) </span><span class="sxs-lookup"><span data-stu-id="06a79-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-662">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同 COM 介面 Iid 的 proxy。</span><span class="sxs-lookup"><span data-stu-id="06a79-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**錯誤 \_ SXS \_ 重複 \_ TLBID**</span><span class="sxs-lookup"><span data-stu-id="06a79-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-664">14025 (0x36C9) </span><span class="sxs-lookup"><span data-stu-id="06a79-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-665">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM 類型程式庫 TLBIDs。</span><span class="sxs-lookup"><span data-stu-id="06a79-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**錯誤 \_ SXS \_ 重複 \_ PROGID**</span><span class="sxs-lookup"><span data-stu-id="06a79-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-667">14026 (0x36CA) </span><span class="sxs-lookup"><span data-stu-id="06a79-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-668">應用程式資訊清單直接或間接參考的兩個或多個元件具有相同的 COM Progid。</span><span class="sxs-lookup"><span data-stu-id="06a79-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**錯誤 \_ SXS \_ 重複的 \_ 元件 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-670">14027 (0x36CB) </span><span class="sxs-lookup"><span data-stu-id="06a79-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-671">應用程式資訊清單直接或間接參考的兩個或多個元件，是相同元件的不同版本，這是不允許的。</span><span class="sxs-lookup"><span data-stu-id="06a79-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**錯誤 \_ SXS \_ 檔案 \_ 雜湊 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="06a79-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-673">14028 (0x36CC) </span><span class="sxs-lookup"><span data-stu-id="06a79-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-674">元件的檔案不符合元件資訊清單中出現的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="06a79-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**錯誤 \_ SXS \_ 原則 \_ 剖析 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-676">14029 (0x36CD) </span><span class="sxs-lookup"><span data-stu-id="06a79-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-677">原則資訊清單包含一或多個語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGQUOTE**</span><span class="sxs-lookup"><span data-stu-id="06a79-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-679">14030 (0x36CE) </span><span class="sxs-lookup"><span data-stu-id="06a79-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-680">資訊清單剖析錯誤：必須是字串常值，但找不到任何左引號字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**錯誤 \_ SXS \_ XML \_ E \_ COMMENTSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="06a79-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-682">14031 (0x36CF) </span><span class="sxs-lookup"><span data-stu-id="06a79-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-683">資訊清單剖析錯誤：批註中使用的語法不正確。</span><span class="sxs-lookup"><span data-stu-id="06a79-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADSTARTNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="06a79-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-685">14032 (0x36D0) </span><span class="sxs-lookup"><span data-stu-id="06a79-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-686">資訊清單剖析錯誤：名稱是以不正確字元開頭。</span><span class="sxs-lookup"><span data-stu-id="06a79-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="06a79-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-688">14033 (0x36D1) </span><span class="sxs-lookup"><span data-stu-id="06a79-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-689">資訊清單剖析錯誤：名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADCHARINSTRING**</span><span class="sxs-lookup"><span data-stu-id="06a79-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-691">14034 (0x36D2) </span><span class="sxs-lookup"><span data-stu-id="06a79-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-692">資訊清單剖析錯誤：字串常值包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**錯誤 \_ SXS \_ XML \_ E \_ XMLDECLSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="06a79-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-694">14035 (0x36D3) </span><span class="sxs-lookup"><span data-stu-id="06a79-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-695">資訊清單剖析錯誤： xml 宣告的語法無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADCHARDATA**</span><span class="sxs-lookup"><span data-stu-id="06a79-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-697">14036 (0x36D4) </span><span class="sxs-lookup"><span data-stu-id="06a79-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-698">資訊清單剖析錯誤：在文字內容中找到不正確字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGWHITESPACE**</span><span class="sxs-lookup"><span data-stu-id="06a79-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-700">14037 (0x36D5) </span><span class="sxs-lookup"><span data-stu-id="06a79-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-701">資訊清單剖析錯誤：缺少必要的空白字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**錯誤 \_ SXS \_ XML \_ E \_ EXPECTINGTAGEND**</span><span class="sxs-lookup"><span data-stu-id="06a79-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-703">14038 (0x36D6) </span><span class="sxs-lookup"><span data-stu-id="06a79-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-704">資訊清單剖析錯誤：必須是 ' > ' 字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGSEMICOLON**</span><span class="sxs-lookup"><span data-stu-id="06a79-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-706">14039 (0x36D7) </span><span class="sxs-lookup"><span data-stu-id="06a79-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-707">資訊清單剖析錯誤：必須是分號字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNBALANCEDPAREN**</span><span class="sxs-lookup"><span data-stu-id="06a79-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-709">14040 (0x36D8) </span><span class="sxs-lookup"><span data-stu-id="06a79-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-710">資訊清單剖析錯誤：不對稱的括弧。</span><span class="sxs-lookup"><span data-stu-id="06a79-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**錯誤 \_ SXS \_ XML \_ E \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="06a79-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-712">14041 (0x36D9) </span><span class="sxs-lookup"><span data-stu-id="06a79-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-713">資訊清單剖析錯誤：內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**錯誤 \_ SXS \_ XML \_ E 非 \_ 預期的 \_ 空格**</span><span class="sxs-lookup"><span data-stu-id="06a79-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-715">14042 (0x36DA) </span><span class="sxs-lookup"><span data-stu-id="06a79-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-716">資訊清單剖析錯誤：此位置不允許空白字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**錯誤 \_ SXS \_ XML \_ 電子 \_ 未完成 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="06a79-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-718">14043 (0x36DB) </span><span class="sxs-lookup"><span data-stu-id="06a79-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-719">資訊清單剖析錯誤：以不正確狀態結束目前編碼的檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="06a79-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**錯誤 \_ SXS \_ XML \_ E \_ 遺失 \_ 括弧**</span><span class="sxs-lookup"><span data-stu-id="06a79-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-721">14044 (0x36DC) </span><span class="sxs-lookup"><span data-stu-id="06a79-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-722">資訊清單剖析錯誤：遺漏括弧。</span><span class="sxs-lookup"><span data-stu-id="06a79-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**錯誤 \_ SXS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**</span><span class="sxs-lookup"><span data-stu-id="06a79-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-724">14045 (0x36DD) </span><span class="sxs-lookup"><span data-stu-id="06a79-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-725">資訊清單剖析錯誤：遺漏單引號或雙右引號字元 (\\ ' 或 \\ ") 。</span><span class="sxs-lookup"><span data-stu-id="06a79-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**錯誤 \_ SXS \_ XML \_ E \_ 多個 \_ 冒號**</span><span class="sxs-lookup"><span data-stu-id="06a79-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-727">14046 (0x36DE) </span><span class="sxs-lookup"><span data-stu-id="06a79-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-728">資訊清單剖析錯誤：名稱中不允許多個冒號。</span><span class="sxs-lookup"><span data-stu-id="06a79-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ DECIMAL**</span><span class="sxs-lookup"><span data-stu-id="06a79-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-730">14047 (0x36DF) </span><span class="sxs-lookup"><span data-stu-id="06a79-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-731">資訊清單剖析錯誤：十進位數的字元無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ 十六進位**</span><span class="sxs-lookup"><span data-stu-id="06a79-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-733">14048 (0x36E0) </span><span class="sxs-lookup"><span data-stu-id="06a79-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-734">資訊清單剖析錯誤：十六進位數位的字元無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ UNICODE**</span><span class="sxs-lookup"><span data-stu-id="06a79-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-736">14049 (0x36E1) </span><span class="sxs-lookup"><span data-stu-id="06a79-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-737">資訊清單剖析錯誤：此平臺的 unicode 字元值無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**錯誤 \_ SXS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="06a79-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-739">14050 (0x36E2) </span><span class="sxs-lookup"><span data-stu-id="06a79-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-740">資訊清單剖析錯誤：應為空白或 '？ '。</span><span class="sxs-lookup"><span data-stu-id="06a79-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNEXPECTEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="06a79-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-742">14051 (0x36E3) </span><span class="sxs-lookup"><span data-stu-id="06a79-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-743">資訊清單剖析錯誤：這個位置不應該有結束標記。</span><span class="sxs-lookup"><span data-stu-id="06a79-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDTAG**</span><span class="sxs-lookup"><span data-stu-id="06a79-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-745">14052 (0x36E4) </span><span class="sxs-lookup"><span data-stu-id="06a79-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-746">資訊清單剖析錯誤：下列標記未關閉： %1。</span><span class="sxs-lookup"><span data-stu-id="06a79-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**錯誤 \_ SXS \_ XML \_ E \_ DUPLICATEATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="06a79-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-748">14053 (0x36E5) </span><span class="sxs-lookup"><span data-stu-id="06a79-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-749">資訊清單剖析錯誤：重複的屬性。</span><span class="sxs-lookup"><span data-stu-id="06a79-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**錯誤 \_ SXS \_ XML \_ E \_ MULTIPLEROOTS**</span><span class="sxs-lookup"><span data-stu-id="06a79-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-751">14054 (0x36E6) </span><span class="sxs-lookup"><span data-stu-id="06a79-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-752">資訊清單剖析錯誤： XML 檔中只允許一個最上層元素。</span><span class="sxs-lookup"><span data-stu-id="06a79-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDATROOTLEVEL**</span><span class="sxs-lookup"><span data-stu-id="06a79-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-754">14055 (0x36E7) </span><span class="sxs-lookup"><span data-stu-id="06a79-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-755">資訊清單剖析錯誤：在檔的最上層無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADXMLDECL**</span><span class="sxs-lookup"><span data-stu-id="06a79-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-757">14056 (0x36E8) </span><span class="sxs-lookup"><span data-stu-id="06a79-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-758">資訊清單剖析錯誤：不正確 xml 宣告。</span><span class="sxs-lookup"><span data-stu-id="06a79-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGROOT**</span><span class="sxs-lookup"><span data-stu-id="06a79-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-760">14057 (0x36E9) </span><span class="sxs-lookup"><span data-stu-id="06a79-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-761">資訊清單剖析錯誤： XML 檔必須有最上層元素。</span><span class="sxs-lookup"><span data-stu-id="06a79-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNEXPECTEDEOF**</span><span class="sxs-lookup"><span data-stu-id="06a79-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-763">14058 (0x36EA) </span><span class="sxs-lookup"><span data-stu-id="06a79-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-764">資訊清單剖析錯誤：非預期的檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="06a79-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADPEREFINSUBSET**</span><span class="sxs-lookup"><span data-stu-id="06a79-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-766">14059 (0x36EB) </span><span class="sxs-lookup"><span data-stu-id="06a79-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-767">資訊清單剖析錯誤：參數實體不能用在內部子集的標記宣告內。</span><span class="sxs-lookup"><span data-stu-id="06a79-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDSTARTTAG**</span><span class="sxs-lookup"><span data-stu-id="06a79-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-769">14060 (0x36EC) </span><span class="sxs-lookup"><span data-stu-id="06a79-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-770">資訊清單剖析錯誤：元素未關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="06a79-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-772">14061 (0x36ED) </span><span class="sxs-lookup"><span data-stu-id="06a79-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-773">資訊清單剖析錯誤： End 元素遺漏 ' > ' 字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDSTRING**</span><span class="sxs-lookup"><span data-stu-id="06a79-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-775">14062 (0x36EE) </span><span class="sxs-lookup"><span data-stu-id="06a79-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-776">資訊清單剖析錯誤：字串常值未關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDCOMMENT**</span><span class="sxs-lookup"><span data-stu-id="06a79-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-778">14063 (0x36EF) </span><span class="sxs-lookup"><span data-stu-id="06a79-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-779">資訊清單剖析錯誤：批註尚未關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDDECL**</span><span class="sxs-lookup"><span data-stu-id="06a79-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-781">14064 (0x36F0) </span><span class="sxs-lookup"><span data-stu-id="06a79-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-782">資訊清單剖析錯誤：宣告未關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**錯誤 \_ SXS \_ XML \_ E \_ UNCLOSEDCDATA**</span><span class="sxs-lookup"><span data-stu-id="06a79-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-784">14065 (0x36F1) </span><span class="sxs-lookup"><span data-stu-id="06a79-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-785">資訊清單剖析錯誤： CDATA 區段未關閉。</span><span class="sxs-lookup"><span data-stu-id="06a79-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**錯誤 \_ SXS \_ XML \_ E \_ RESERVEDNAMESPACE**</span><span class="sxs-lookup"><span data-stu-id="06a79-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-787">14066 (0x36F2) </span><span class="sxs-lookup"><span data-stu-id="06a79-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-788">資訊清單剖析錯誤：命名空間前置詞不能以保留字元串 "xml" 開頭。</span><span class="sxs-lookup"><span data-stu-id="06a79-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDENCODING**</span><span class="sxs-lookup"><span data-stu-id="06a79-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-790">14067 (0x36F3) </span><span class="sxs-lookup"><span data-stu-id="06a79-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-791">資訊清單剖析錯誤：系統不支援指定的編碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**錯誤 \_ SXS \_ XML \_ E \_ INVALIDSWITCH**</span><span class="sxs-lookup"><span data-stu-id="06a79-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-793">14068 (0x36F4) </span><span class="sxs-lookup"><span data-stu-id="06a79-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-794">資訊清單剖析錯誤：不支援從目前的編碼切換為指定的編碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**錯誤 \_ SXS \_ XML \_ E \_ BADXMLCASE**</span><span class="sxs-lookup"><span data-stu-id="06a79-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-796">14069 (0x36F5) </span><span class="sxs-lookup"><span data-stu-id="06a79-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-797">資訊清單剖析錯誤：名稱 ' xml ' 是保留的，而且必須是小寫。</span><span class="sxs-lookup"><span data-stu-id="06a79-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**錯誤 \_ SXS \_ XML \_ E \_ \_ 獨立無效**</span><span class="sxs-lookup"><span data-stu-id="06a79-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-799">14070 (0x36F6) </span><span class="sxs-lookup"><span data-stu-id="06a79-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-800">資訊清單剖析錯誤：獨立屬性的值必須為 ' yes ' 或 ' no '。</span><span class="sxs-lookup"><span data-stu-id="06a79-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**錯誤 \_ SXS \_ XML \_ 電子非 \_ 預期的 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="06a79-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-802">14071 (0x36F7) </span><span class="sxs-lookup"><span data-stu-id="06a79-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-803">資訊清單剖析錯誤：獨立屬性不能用在外部實體中。</span><span class="sxs-lookup"><span data-stu-id="06a79-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**錯誤 \_ SXS \_ XML \_ E \_ 不正確 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="06a79-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-805">14072 (0x36F8) </span><span class="sxs-lookup"><span data-stu-id="06a79-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-806">資訊清單剖析錯誤：版本號碼無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**錯誤 \_ SXS \_ XML \_ E \_ MISSINGEQUALS**</span><span class="sxs-lookup"><span data-stu-id="06a79-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-808">14073 (0x36F9) </span><span class="sxs-lookup"><span data-stu-id="06a79-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-809">資訊清單剖析錯誤：遺漏屬性與屬性值之間的等號。</span><span class="sxs-lookup"><span data-stu-id="06a79-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**錯誤 \_ SXS \_ 保護 \_ 復原 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-811">14074 (0x36FA) </span><span class="sxs-lookup"><span data-stu-id="06a79-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-812">元件保護錯誤：無法復原指定的元件。</span><span class="sxs-lookup"><span data-stu-id="06a79-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**錯誤 \_ SXS \_ 保護 \_ 的 \_ 公開金鑰 \_ 太 \_ 短**</span><span class="sxs-lookup"><span data-stu-id="06a79-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-814">14075 (0x36FB) </span><span class="sxs-lookup"><span data-stu-id="06a79-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-815">元件保護錯誤：元件的公開金鑰太短而無法允許。</span><span class="sxs-lookup"><span data-stu-id="06a79-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**錯誤 \_ SXS \_ 保護 \_ 類別 \_ 目錄 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="06a79-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-817">14076 (0x36FC) </span><span class="sxs-lookup"><span data-stu-id="06a79-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-818">元件保護錯誤：元件的目錄無效，或不符合元件的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="06a79-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**錯誤 \_ SXS \_ 產生無法翻譯 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06a79-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-820">14077 (0x36FD) </span><span class="sxs-lookup"><span data-stu-id="06a79-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-821">HRESULT 無法轉譯為對應的 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**\_遺漏錯誤 SXS \_ 保護 \_ 類別目錄 \_ \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="06a79-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-823">14078 (0x36FE) </span><span class="sxs-lookup"><span data-stu-id="06a79-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-824">元件保護錯誤：遺漏元件的目錄。</span><span class="sxs-lookup"><span data-stu-id="06a79-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**錯誤 \_ SXS \_ 遺漏 \_ 元件 \_ 標識 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="06a79-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-826">14079 (0x36FF) </span><span class="sxs-lookup"><span data-stu-id="06a79-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-827">提供的元件識別缺少一或多個必須存在於此內容中的屬性。</span><span class="sxs-lookup"><span data-stu-id="06a79-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**錯誤 \_ SXS \_ 不正確 \_ 元件 \_ 標識 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-829">14080 (0x3700) </span><span class="sxs-lookup"><span data-stu-id="06a79-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-830">提供的元件識別有一或多個屬性名稱包含 XML 名稱中不允許的字元。</span><span class="sxs-lookup"><span data-stu-id="06a79-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**\_遺漏錯誤 SXS \_ 元件 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-832">14081 (0x3701) </span><span class="sxs-lookup"><span data-stu-id="06a79-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-833">找不到參考的元件。</span><span class="sxs-lookup"><span data-stu-id="06a79-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**錯誤 \_ SXS \_ 已損毀 \_ 啟用 \_ 堆疊**</span><span class="sxs-lookup"><span data-stu-id="06a79-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-835">14082 (0x3702) </span><span class="sxs-lookup"><span data-stu-id="06a79-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-836">執行中線程的啟用內容啟用堆疊已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**錯誤 \_ SXS \_ 損毀**</span><span class="sxs-lookup"><span data-stu-id="06a79-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-838">14083 (0x3703) </span><span class="sxs-lookup"><span data-stu-id="06a79-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-839">此進程或執行緒的應用程式隔離中繼資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**錯誤 \_ SXS \_ 早期 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-841">14084 (0x3704) </span><span class="sxs-lookup"><span data-stu-id="06a79-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-842">正在停用的啟用內容不是最近啟用的內容。</span><span class="sxs-lookup"><span data-stu-id="06a79-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**錯誤 \_ SXS \_ 不正確 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-844">14085 (0x3705) </span><span class="sxs-lookup"><span data-stu-id="06a79-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-845">目前執行中的執行緒不會使用已停用的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="06a79-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**錯誤 \_ SXS \_ 多次 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-847">14086 (0x3706) </span><span class="sxs-lookup"><span data-stu-id="06a79-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-848">正在停用的啟用內容已停用。</span><span class="sxs-lookup"><span data-stu-id="06a79-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**要求的錯誤 \_ SXS \_ 進程 \_ 終止 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-850">14087 (0x3707) </span><span class="sxs-lookup"><span data-stu-id="06a79-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-851">隔離設備所使用的元件已要求終止進程。</span><span class="sxs-lookup"><span data-stu-id="06a79-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**錯誤 \_ SXS \_ 發行 \_ 啟用 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="06a79-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-853">14088 (0x3708) </span><span class="sxs-lookup"><span data-stu-id="06a79-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-854">核心模式元件正在釋放啟用內容的參考。</span><span class="sxs-lookup"><span data-stu-id="06a79-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**錯誤 \_ SXS \_ 系統 \_ 預設 \_ 啟用 \_ 內容 \_ 空白**</span><span class="sxs-lookup"><span data-stu-id="06a79-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-856">14089 (0x3709) </span><span class="sxs-lookup"><span data-stu-id="06a79-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-857">無法產生系統預設元件的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="06a79-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**錯誤 \_ SXS \_ 不正確 \_ 識別 \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="06a79-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-859">14090 (0x370A) </span><span class="sxs-lookup"><span data-stu-id="06a79-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-860">身分識別中的屬性值不在合法範圍內。</span><span class="sxs-lookup"><span data-stu-id="06a79-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**錯誤 \_ SXS \_ 不正確 \_ 識別 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-862">14091 (0x370B) </span><span class="sxs-lookup"><span data-stu-id="06a79-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-863">身分識別中的屬性名稱不在合法範圍內。</span><span class="sxs-lookup"><span data-stu-id="06a79-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**錯誤 \_ SXS \_ 識別 \_ 重複 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="06a79-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-865">14092 (0x370C) </span><span class="sxs-lookup"><span data-stu-id="06a79-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-866">身分識別包含相同屬性的兩個定義。</span><span class="sxs-lookup"><span data-stu-id="06a79-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**錯誤 \_ SXS 身分 \_ 識別 \_ 剖析 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-868">14093 (0x370D) </span><span class="sxs-lookup"><span data-stu-id="06a79-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-869">識別字串的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="06a79-869">The identity string is malformed.</span></span> <span data-ttu-id="06a79-870">這可能是因為尾端逗號、兩個未命名屬性、遺漏屬性名稱或遺漏屬性值所致。</span><span class="sxs-lookup"><span data-stu-id="06a79-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**錯誤 \_ 的 \_ 替代 \_ 字串格式錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-872">14094 (0x370E) </span><span class="sxs-lookup"><span data-stu-id="06a79-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-873">包含當地語系化的替換內容的字串格式不正確。</span><span class="sxs-lookup"><span data-stu-id="06a79-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="06a79-874">貨幣符號 ($) 後面接著左括弧以外的某個字元，或找不到其他貨幣符號或替換的右括弧。</span><span class="sxs-lookup"><span data-stu-id="06a79-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**錯誤 \_ SXS \_ 不正確的 \_ 公開金鑰 \_ \_ TOKEN**</span><span class="sxs-lookup"><span data-stu-id="06a79-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-876">14095 (0x370F) </span><span class="sxs-lookup"><span data-stu-id="06a79-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-877">公開金鑰標記未對應到指定的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a79-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**未對應的 \_ \_ 替代 \_ 字串時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-879">14096 (0x3710) </span><span class="sxs-lookup"><span data-stu-id="06a79-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-880">替代字串沒有對應。</span><span class="sxs-lookup"><span data-stu-id="06a79-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**錯誤 \_ SXS \_ 元件 \_ 未 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="06a79-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-882">14097 (0x3711) </span><span class="sxs-lookup"><span data-stu-id="06a79-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-883">在提出要求之前，必須先鎖定元件。</span><span class="sxs-lookup"><span data-stu-id="06a79-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**錯誤 \_ SXS \_ 元件 \_ 存放區 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="06a79-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-885">14098 (0x3712) </span><span class="sxs-lookup"><span data-stu-id="06a79-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-886">元件存放區已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**錯誤 \_ ADVANCED \_ INSTALLER \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-888">14099 (0x3713) </span><span class="sxs-lookup"><span data-stu-id="06a79-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-889">在安裝或服務期間，advanced installer 失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**錯誤 \_ XML \_ 編碼 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="06a79-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-891">14100 (0x3714) </span><span class="sxs-lookup"><span data-stu-id="06a79-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-892">XML 宣告中的字元編碼與檔中使用的編碼不相符。</span><span class="sxs-lookup"><span data-stu-id="06a79-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 識別 \_ 相同 \_ 但 \_ 內容 \_ 不同**</span><span class="sxs-lookup"><span data-stu-id="06a79-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-894">14101 (0x3715) </span><span class="sxs-lookup"><span data-stu-id="06a79-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-895">資訊清單的身分識別完全相同，但其內容不同。</span><span class="sxs-lookup"><span data-stu-id="06a79-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**錯誤 \_ SXS 身分識別 \_ \_ 不同**</span><span class="sxs-lookup"><span data-stu-id="06a79-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-897">14102 (0x3716) </span><span class="sxs-lookup"><span data-stu-id="06a79-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-898">元件身分識別不同。</span><span class="sxs-lookup"><span data-stu-id="06a79-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**錯誤 \_ SXS \_ 元件 \_ \_ 不是 \_ \_ 部署**</span><span class="sxs-lookup"><span data-stu-id="06a79-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-900">14103 (0x3717) </span><span class="sxs-lookup"><span data-stu-id="06a79-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-901">元件不是部署。</span><span class="sxs-lookup"><span data-stu-id="06a79-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**錯誤 \_ SXS \_ 檔案 \_ 不 \_ \_ 是元件的一部分 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-903">14104 (0x3718) </span><span class="sxs-lookup"><span data-stu-id="06a79-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-904">檔案不是元件的一部分。</span><span class="sxs-lookup"><span data-stu-id="06a79-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**錯誤 \_ SXS \_ 資訊清單 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="06a79-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-906">14105 (0x3719) </span><span class="sxs-lookup"><span data-stu-id="06a79-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-907">資訊清單的大小超過允許的最大值。</span><span class="sxs-lookup"><span data-stu-id="06a79-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**\_ \_ \_ 未註冊錯誤 SXS \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="06a79-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-909">14106 (0x371A) </span><span class="sxs-lookup"><span data-stu-id="06a79-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-910">設定未註冊。</span><span class="sxs-lookup"><span data-stu-id="06a79-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**錯誤 \_ SXS \_ 交易 \_ 關閉 \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="06a79-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-912">14107 (0x371B) </span><span class="sxs-lookup"><span data-stu-id="06a79-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-913">一或多個必要的交易成員不存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**錯誤的 \_ SMI-S \_ 基本 \_ 安裝程式 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-915">14108 (0x371C) </span><span class="sxs-lookup"><span data-stu-id="06a79-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-916">在安裝或服務期間，SMI-S 基本安裝程式失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**錯誤 \_ 一般 \_ 命令 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-918">14109 (0x371D) </span><span class="sxs-lookup"><span data-stu-id="06a79-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-919">泛型命令可執行檔傳回指出失敗的結果。</span><span class="sxs-lookup"><span data-stu-id="06a79-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**錯誤 \_ SXS \_ 檔案 \_ 雜湊 \_ 遺失**</span><span class="sxs-lookup"><span data-stu-id="06a79-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-921">14110 (0x371E) </span><span class="sxs-lookup"><span data-stu-id="06a79-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-922">元件的資訊清單中遺漏檔案驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="06a79-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="06a79-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-924">15000 (0x3A98) </span><span class="sxs-lookup"><span data-stu-id="06a79-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-925">指定的通道路徑無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**錯誤 \_ .EVT \_ 不正確 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="06a79-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-927">15001 (0x3A99) </span><span class="sxs-lookup"><span data-stu-id="06a79-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-928">指定的查詢無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**\_ \_ \_ \_ 找不到簽發者中繼資料 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-930">15002 (0x3A9A) </span><span class="sxs-lookup"><span data-stu-id="06a79-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-931">在資源中找不到發行者中繼資料。</span><span class="sxs-lookup"><span data-stu-id="06a79-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件範本**</span><span class="sxs-lookup"><span data-stu-id="06a79-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-933">15003 (0x3A9B) </span><span class="sxs-lookup"><span data-stu-id="06a79-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-934">資源 (錯誤 = %1) 中找不到事件定義的範本。</span><span class="sxs-lookup"><span data-stu-id="06a79-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-936">15004 (0x3A9C) </span><span class="sxs-lookup"><span data-stu-id="06a79-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-937">指定的發行者名稱無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**錯誤 \_ .EVT \_ 不正確 \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="06a79-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-939">15005 (0x3A9D) </span><span class="sxs-lookup"><span data-stu-id="06a79-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-940">發行者所引發的事件資料與發行者資訊清單中的事件範本定義不相容。</span><span class="sxs-lookup"><span data-stu-id="06a79-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 頻道**</span><span class="sxs-lookup"><span data-stu-id="06a79-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-942">15007 (0x3A9F) </span><span class="sxs-lookup"><span data-stu-id="06a79-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-943">找不到指定的通道。</span><span class="sxs-lookup"><span data-stu-id="06a79-943">The specified channel could not be found.</span></span> <span data-ttu-id="06a79-944">檢查通道設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**錯誤 \_ .EVT \_ 格式不正確的 \_ XML \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="06a79-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-946">15008 (0x3AA0) </span><span class="sxs-lookup"><span data-stu-id="06a79-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-947">指定的 xml 文字格式不正確。</span><span class="sxs-lookup"><span data-stu-id="06a79-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="06a79-948">如需詳細資訊，請參閱擴充錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ \_ 對 \_ 直接 \_ 通道的錯誤 .EVT 訂用帳戶**</span><span class="sxs-lookup"><span data-stu-id="06a79-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-950">15009 (0x3AA1) </span><span class="sxs-lookup"><span data-stu-id="06a79-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-951">呼叫端嘗試訂閱不允許的直接通道。</span><span class="sxs-lookup"><span data-stu-id="06a79-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="06a79-952">直接通道的事件會直接移至記錄檔，而且無法訂閱。</span><span class="sxs-lookup"><span data-stu-id="06a79-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**錯誤 \_ .EVT \_ 設定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-954">15010 (0x3AA2) </span><span class="sxs-lookup"><span data-stu-id="06a79-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-955">組態錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 過時**</span><span class="sxs-lookup"><span data-stu-id="06a79-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-957">15011 (0x3AA3) </span><span class="sxs-lookup"><span data-stu-id="06a79-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-958">查詢結果過時/無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-958">The query result is stale / invalid.</span></span> <span data-ttu-id="06a79-959">這可能是因為在建立查詢結果之後清除或變換記錄所致。</span><span class="sxs-lookup"><span data-stu-id="06a79-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="06a79-960">使用者應藉由釋出查詢結果物件並重新發出查詢，來處理此程式碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 不正確 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="06a79-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-962">15012 (0x3AA4) </span><span class="sxs-lookup"><span data-stu-id="06a79-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-963">查詢結果目前的位置無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**錯誤 \_ .EVT \_ 非 \_ 驗證 \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="06a79-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-965">15013 (0x3AA5) </span><span class="sxs-lookup"><span data-stu-id="06a79-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-966">註冊的 MSXML 不支援驗證。</span><span class="sxs-lookup"><span data-stu-id="06a79-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**錯誤 \_ .EVT \_ 篩選 \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="06a79-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-968">15014 (0x3AA6) </span><span class="sxs-lookup"><span data-stu-id="06a79-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-969">如果運算式本身評估為節點集，且不屬於範圍作業的一些其他變更，則運算式只能在範圍作業的變更之後接著變更。</span><span class="sxs-lookup"><span data-stu-id="06a79-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**錯誤 \_ .EVT \_ 篩選 \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="06a79-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-971">15015 (0x3AA7) </span><span class="sxs-lookup"><span data-stu-id="06a79-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-972">無法從不代表元素集的詞彙執行步驟作業。</span><span class="sxs-lookup"><span data-stu-id="06a79-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="06a79-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-974">15016 (0x3AA8) </span><span class="sxs-lookup"><span data-stu-id="06a79-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-975">二元運算子的左邊引數必須是屬性、節點或變數，且右邊引數必須是常數。</span><span class="sxs-lookup"><span data-stu-id="06a79-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="06a79-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-977">15017 (0x3AA9) </span><span class="sxs-lookup"><span data-stu-id="06a79-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-978">步驟作業必須牽涉到節點測試，或者，如果是述詞，則會評估第一個節點集合所識別之節點集內每個節點的代數運算式。</span><span class="sxs-lookup"><span data-stu-id="06a79-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTYPE .。。**</span><span class="sxs-lookup"><span data-stu-id="06a79-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-980">15018 (0x3AAA) </span><span class="sxs-lookup"><span data-stu-id="06a79-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-981">目前不支援此資料類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**錯誤 \_ .EVT \_ 篩選 \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="06a79-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-983">15019 (0x3AAB) </span><span class="sxs-lookup"><span data-stu-id="06a79-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-984">位置 %1！ d！發生語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="06a79-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-986">15020 (0x3AAC) </span><span class="sxs-lookup"><span data-stu-id="06a79-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-987">此篩選準則的執行不支援這個運算子。</span><span class="sxs-lookup"><span data-stu-id="06a79-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="06a79-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-989">15021 (0x3AAD) </span><span class="sxs-lookup"><span data-stu-id="06a79-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-990">發現未預期的權杖。</span><span class="sxs-lookup"><span data-stu-id="06a79-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**錯誤 \_ .EVT \_ \_ 啟用的 \_ \_ \_ 直接 \_ 通道上有不正確操作**</span><span class="sxs-lookup"><span data-stu-id="06a79-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-992">15022 (0x3AAE) </span><span class="sxs-lookup"><span data-stu-id="06a79-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-993">要求的作業無法在啟用的直接通道上執行。</span><span class="sxs-lookup"><span data-stu-id="06a79-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="06a79-994">必須先停用通道，才能執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="06a79-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="06a79-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-996">15023 (0x3AAF) </span><span class="sxs-lookup"><span data-stu-id="06a79-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-997">通道屬性 %1！ s！</span><span class="sxs-lookup"><span data-stu-id="06a79-997">Channel property %1!s!</span></span> <span data-ttu-id="06a79-998">包含不正確值。</span><span class="sxs-lookup"><span data-stu-id="06a79-998">contains invalid value.</span></span> <span data-ttu-id="06a79-999">值的類型無效、不在有效範圍內、無法更新，或不支援此類型的通道。</span><span class="sxs-lookup"><span data-stu-id="06a79-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="06a79-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1001">15024 (0x3AB0) </span><span class="sxs-lookup"><span data-stu-id="06a79-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1002">發行者屬性 %1！ s！</span><span class="sxs-lookup"><span data-stu-id="06a79-1002">Publisher property %1!s!</span></span> <span data-ttu-id="06a79-1003">包含不正確值。</span><span class="sxs-lookup"><span data-stu-id="06a79-1003">contains invalid value.</span></span> <span data-ttu-id="06a79-1004">值的類型無效、不在有效範圍內、無法更新，或是此類型的發行者不支援此值。</span><span class="sxs-lookup"><span data-stu-id="06a79-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**錯誤 \_ .EVT \_ 通道 \_ 無法 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="06a79-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1006">15025 (0x3AB1) </span><span class="sxs-lookup"><span data-stu-id="06a79-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1007">通道無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06a79-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**錯誤 \_ .EVT \_ 篩選 \_ 太 \_ 複雜**</span><span class="sxs-lookup"><span data-stu-id="06a79-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1009">15026 (0x3AB2) </span><span class="sxs-lookup"><span data-stu-id="06a79-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1010">Xpath 運算式超過支援的複雜度。</span><span class="sxs-lookup"><span data-stu-id="06a79-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="06a79-1011">請 symplify 它，或將它分割成兩個或更簡單的運算式。</span><span class="sxs-lookup"><span data-stu-id="06a79-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 訊息**</span><span class="sxs-lookup"><span data-stu-id="06a79-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1013">15027 (0x3AB3) </span><span class="sxs-lookup"><span data-stu-id="06a79-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1014">訊息資源存在，但在字串/訊息資料表中找不到訊息。</span><span class="sxs-lookup"><span data-stu-id="06a79-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息識別碼**</span><span class="sxs-lookup"><span data-stu-id="06a79-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1016">15028 (0x3AB4) </span><span class="sxs-lookup"><span data-stu-id="06a79-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1017">找不到所需訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="06a79-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 值 \_ 插入**</span><span class="sxs-lookup"><span data-stu-id="06a79-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1019">15029 (0x3AB5) </span><span class="sxs-lookup"><span data-stu-id="06a79-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1020">找不到插入索引 (% 1) 的替代字串。</span><span class="sxs-lookup"><span data-stu-id="06a79-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 參數 \_ 插入**</span><span class="sxs-lookup"><span data-stu-id="06a79-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1022">15030 (0x3AB6) </span><span class="sxs-lookup"><span data-stu-id="06a79-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1023">找不到參數參考 (% 1) 的描述字串。</span><span class="sxs-lookup"><span data-stu-id="06a79-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**已 \_ 達到錯誤的 .EVT \_ 最大 \_ 插入 \_ 數**</span><span class="sxs-lookup"><span data-stu-id="06a79-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1025">15031 (0x3AB7) </span><span class="sxs-lookup"><span data-stu-id="06a79-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1026">已達到最大取代數目。</span><span class="sxs-lookup"><span data-stu-id="06a79-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件定義**</span><span class="sxs-lookup"><span data-stu-id="06a79-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1028">15032 (0x3AB8) </span><span class="sxs-lookup"><span data-stu-id="06a79-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1029">找不到事件識別碼 (% 1) 的事件定義。</span><span class="sxs-lookup"><span data-stu-id="06a79-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息地區設定**</span><span class="sxs-lookup"><span data-stu-id="06a79-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1031">15033 (0x3AB9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1032">所需訊息的地區設定特定資源不存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**錯誤的 \_ .EVT \_ 版本 \_ 太 \_ 舊**</span><span class="sxs-lookup"><span data-stu-id="06a79-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1034">15034 (0x3ABA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1035">資源太舊而無法相容。</span><span class="sxs-lookup"><span data-stu-id="06a79-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**錯誤 \_ .EVT \_ 版本 \_ 太 \_ 新**</span><span class="sxs-lookup"><span data-stu-id="06a79-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1037">15035 (0x3ABB) </span><span class="sxs-lookup"><span data-stu-id="06a79-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1038">資源太新，無法相容。</span><span class="sxs-lookup"><span data-stu-id="06a79-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**錯誤 \_ .EVT \_ 無法 \_ 開啟 \_ \_ 查詢通道 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1040">15036 (0x3ABC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1041">位於索引 %1！ d！的通道</span><span class="sxs-lookup"><span data-stu-id="06a79-1041">The channel at index %1!d!</span></span> <span data-ttu-id="06a79-1042">無法開啟查詢。</span><span class="sxs-lookup"><span data-stu-id="06a79-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**錯誤的 \_ .EVT \_ 發行者 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1044">15037 (0x3ABD) </span><span class="sxs-lookup"><span data-stu-id="06a79-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1045">發行者已停用，且其資源無法使用。</span><span class="sxs-lookup"><span data-stu-id="06a79-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="06a79-1046">當發行者正在卸載或升級時，通常就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="06a79-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**錯誤 \_ .EVT \_ 篩選 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="06a79-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1048">15038 (0x3ABE) </span><span class="sxs-lookup"><span data-stu-id="06a79-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1049">嘗試建立的數數值型別超出其有效範圍。</span><span class="sxs-lookup"><span data-stu-id="06a79-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**\_ \_ \_ 無法啟動錯誤 EC 訂用帳戶 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1051">15080 (0x3AE8) </span><span class="sxs-lookup"><span data-stu-id="06a79-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1052">訂用帳戶無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06a79-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**錯誤 \_ EC \_ 記錄檔 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="06a79-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1054">15081 (0x3AE9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1055">訂用帳戶的記錄處於停用狀態，無法用來將事件轉寄至。</span><span class="sxs-lookup"><span data-stu-id="06a79-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="06a79-1056">必須先啟用記錄檔，才能啟用訂閱。</span><span class="sxs-lookup"><span data-stu-id="06a79-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**錯誤 \_ EC \_ 迴圈 \_ 轉送**</span><span class="sxs-lookup"><span data-stu-id="06a79-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1058">15082 (0x3AEA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1059">從本機電腦轉送事件到本身時，訂閱的查詢不能包含訂用帳戶的目標記錄檔。</span><span class="sxs-lookup"><span data-stu-id="06a79-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**錯誤 \_ EC \_ CREDSTORE \_ FULL**</span><span class="sxs-lookup"><span data-stu-id="06a79-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1061">15083 (0x3AEB) </span><span class="sxs-lookup"><span data-stu-id="06a79-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1062">用來儲存認證的認證存放區已滿。</span><span class="sxs-lookup"><span data-stu-id="06a79-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 EC 認證**</span><span class="sxs-lookup"><span data-stu-id="06a79-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1064">15084 (0x3AEC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1065">在認證存放區中找不到此訂用帳戶所使用的認證。</span><span class="sxs-lookup"><span data-stu-id="06a79-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**錯誤 \_ EC 沒有作用中的 \_ \_ \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="06a79-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1067">15085 (0x3AED) </span><span class="sxs-lookup"><span data-stu-id="06a79-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1068">找不到查詢的作用中通道。</span><span class="sxs-lookup"><span data-stu-id="06a79-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 MUI 檔案**</span><span class="sxs-lookup"><span data-stu-id="06a79-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1070">15100 (0x3AFC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1071">資源載入器找不到 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**錯誤 \_ MUI \_ 不正確檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1073">15101 (0x3AFD) </span><span class="sxs-lookup"><span data-stu-id="06a79-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1074">資源載入器無法載入 MUI 檔案，因為檔案無法通過驗證。</span><span class="sxs-lookup"><span data-stu-id="06a79-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**錯誤 \_ MUI \_ 不正確 \_ RC \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="06a79-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1076">15102 (0x3AFE) </span><span class="sxs-lookup"><span data-stu-id="06a79-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1077">RC 資訊清單損毀，發生垃圾資料或不受支援的版本，或遺漏必要專案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**錯誤 \_ MUI \_ 不正確 \_ 地區設定 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1079">15103 (0x3AFF) </span><span class="sxs-lookup"><span data-stu-id="06a79-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1080">RC 資訊清單具有不正確文化特性名稱。</span><span class="sxs-lookup"><span data-stu-id="06a79-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**錯誤 \_ MUI \_ 不正確 \_ ULTIMATEFALLBACK \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1082">15104 (0x3B00) </span><span class="sxs-lookup"><span data-stu-id="06a79-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1083">RC 資訊清單有不正確 ultimatefallback 名稱。</span><span class="sxs-lookup"><span data-stu-id="06a79-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**\_ \_ \_ 未載入錯誤 MUI \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="06a79-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1085">15105 (0x3B01) </span><span class="sxs-lookup"><span data-stu-id="06a79-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1086">資源載入器快取沒有載入的 MUI 專案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**錯誤 \_ 資源 \_ 列舉 \_ 使用者 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="06a79-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1088">15106 (0x3B02) </span><span class="sxs-lookup"><span data-stu-id="06a79-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1089">使用者已停止資源列舉。</span><span class="sxs-lookup"><span data-stu-id="06a79-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**錯誤 \_ MUI \_ INTLSETTINGS \_ UILANG \_ 未 \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="06a79-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1091">15107 (0x3B03) </span><span class="sxs-lookup"><span data-stu-id="06a79-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1092">UI 語言安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**錯誤 \_ MUI \_ INTLSETTINGS \_ 不正確 \_ 地區設定 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="06a79-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1094">15108 (0x3B04) </span><span class="sxs-lookup"><span data-stu-id="06a79-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1095">地區設定安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**\_MRM \_ 執行時間 \_ 沒有 \_ 預設 \_ 或 \_ 中立的 \_ 資源時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1097">15110 (0x3B06) </span><span class="sxs-lookup"><span data-stu-id="06a79-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1098">資源沒有預設值或中性值。</span><span class="sxs-lookup"><span data-stu-id="06a79-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**\_MRM \_ 不正確 \_ PRICONFIG.DEFAULT.XML 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1100">15111 (0x3B07) </span><span class="sxs-lookup"><span data-stu-id="06a79-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1101">不正確 PRI 設定檔案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**\_MRM \_ 不正確 \_ 檔 \_ 類型時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1103">15112 (0x3B08) </span><span class="sxs-lookup"><span data-stu-id="06a79-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1104">不正確檔案類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**\_MRM \_ 未知 \_ 限定詞時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1106">15113 (0x3B09) </span><span class="sxs-lookup"><span data-stu-id="06a79-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1107">未知的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="06a79-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**\_MRM 不正確辨識 \_ \_ 符號 \_ 值時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1109">15114 (0x3B0A) </span><span class="sxs-lookup"><span data-stu-id="06a79-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1110">不正確辨識符號值。</span><span class="sxs-lookup"><span data-stu-id="06a79-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**\_MRM \_ 沒有 \_ 候選的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1112">15115 (0x3B0B) </span><span class="sxs-lookup"><span data-stu-id="06a79-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1113">找不到候選。</span><span class="sxs-lookup"><span data-stu-id="06a79-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**\_MRM \_ 沒有 \_ 相符 \_ 或 \_ 預設 \_ 候選項時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1115">15116 (0x3B0C) </span><span class="sxs-lookup"><span data-stu-id="06a79-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1116">Windows.applicationmodel.resources.core.resourcemap 或 NamedResource 的專案沒有預設或中立的資源。</span><span class="sxs-lookup"><span data-stu-id="06a79-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**\_MRM \_ 資源 \_ 類型 \_ 不符時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1118">15117 (0x3B0D) </span><span class="sxs-lookup"><span data-stu-id="06a79-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1119">不正確 ResourceCandidate 類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**\_MRM \_ 重複的 \_ 對應 \_ 名稱時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1121">15118 (0x3B0E) </span><span class="sxs-lookup"><span data-stu-id="06a79-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1122">重複的資源對應。</span><span class="sxs-lookup"><span data-stu-id="06a79-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**\_MRM \_ 重複 \_ 專案時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1124">15119 (0x3B0F) </span><span class="sxs-lookup"><span data-stu-id="06a79-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1125">重複的專案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**\_MRM \_ 不正確 \_ 資源 \_ 識別碼時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1127">15120 (0x3B10) </span><span class="sxs-lookup"><span data-stu-id="06a79-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1128">資源識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**\_MRM \_ FILEPATH \_ 太 \_ 長時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1130">15121 (0x3B11) </span><span class="sxs-lookup"><span data-stu-id="06a79-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1131">檔案路徑太長。</span><span class="sxs-lookup"><span data-stu-id="06a79-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**\_MRM \_ 不支援的 \_ 目錄 \_ 類型時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1133">15122 (0x3B12) </span><span class="sxs-lookup"><span data-stu-id="06a79-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1134">不支援的目錄類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**\_MRM \_ 不正確 \_ PRI \_ 檔案時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1136">15126 (0x3B16) </span><span class="sxs-lookup"><span data-stu-id="06a79-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1137">不正確 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="06a79-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**\_ \_ \_ \_ \_ 找不到名為資源的錯誤 MRM**</span><span class="sxs-lookup"><span data-stu-id="06a79-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1139">15127 (0x3B17) </span><span class="sxs-lookup"><span data-stu-id="06a79-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1140">找不到 NamedResource。</span><span class="sxs-lookup"><span data-stu-id="06a79-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ 找不到對應 \_ 的錯誤 MRM**</span><span class="sxs-lookup"><span data-stu-id="06a79-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1142">15135 (0x3B1F) </span><span class="sxs-lookup"><span data-stu-id="06a79-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1143">找不到 Windows.applicationmodel.resources.core.resourcemap。</span><span class="sxs-lookup"><span data-stu-id="06a79-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**\_MRM \_ 不支援的 \_ 設定檔 \_ 類型時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1145">15136 (0x3B20) </span><span class="sxs-lookup"><span data-stu-id="06a79-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1146">不支援的 MRT.LOG 配置檔案類型。</span><span class="sxs-lookup"><span data-stu-id="06a79-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**\_MRM 不正確辨識 \_ \_ 符號 \_ 運算子時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1148">15137 (0x3B21) </span><span class="sxs-lookup"><span data-stu-id="06a79-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1149">不正確辨識符號運算子。</span><span class="sxs-lookup"><span data-stu-id="06a79-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**\_MRM \_ 不定辨識 \_ 符號 \_ 值時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1151">15138 (0x3B22) </span><span class="sxs-lookup"><span data-stu-id="06a79-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1152">無法判斷辨識符號值或辨識符號值尚未設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**\_MRM 自動 \_ 合併 \_ 已啟用時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1154">15139 (0x3B23) </span><span class="sxs-lookup"><span data-stu-id="06a79-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1155">PRI 檔案中已啟用自動合併。</span><span class="sxs-lookup"><span data-stu-id="06a79-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**\_MRM \_ 太 \_ 多 \_ 資源時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1157">15140 (0x3B24) </span><span class="sxs-lookup"><span data-stu-id="06a79-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1158">為封裝定義了太多資源。</span><span class="sxs-lookup"><span data-stu-id="06a79-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**錯誤 \_ MCA \_ 不正確 \_ 功能 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="06a79-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1160">15200 (0x3B60) </span><span class="sxs-lookup"><span data-stu-id="06a79-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1161">此監視器傳回的 DDC/CI 功能字串不符合存取權。匯流排3.0、DDC/CI 1.1 或 MCCS 2 修訂1規格。</span><span class="sxs-lookup"><span data-stu-id="06a79-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**錯誤 \_ MCA \_ 不正確 \_ VCP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="06a79-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1163">15201 (0x3B61) </span><span class="sxs-lookup"><span data-stu-id="06a79-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1164">監視器的 VCP 版本 (0xDF) VCP 程式碼傳回不正確版本值。</span><span class="sxs-lookup"><span data-stu-id="06a79-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**錯誤 \_ MCA \_ 監視 \_ 違反 \_ MCCS \_ 規格**</span><span class="sxs-lookup"><span data-stu-id="06a79-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1166">15202 (0x3B62) </span><span class="sxs-lookup"><span data-stu-id="06a79-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1167">此監視器不符合其宣稱支援的 MCCS 規格。</span><span class="sxs-lookup"><span data-stu-id="06a79-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**錯誤 \_ MCA \_ MCCS \_ 版本 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="06a79-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1169">15203 (0x3B63) </span><span class="sxs-lookup"><span data-stu-id="06a79-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1170">監視器的 mccs ver 功能中的 MCCS 版本，與 \_ 使用 VCP 版本 (0xDF) VCP 程式碼時，監視器所報告的 mccs 版本不符。</span><span class="sxs-lookup"><span data-stu-id="06a79-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**\_MCA 錯誤 MCA \_ 不支援的 \_ MCCS \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="06a79-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1172">15204 (0x3B64) </span><span class="sxs-lookup"><span data-stu-id="06a79-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1173">監視器設定 API 僅適用于支援 MCCS 1.0 規格、MCCS 2.0 規格或 MCCS 2.0 修訂1規格的監視器。</span><span class="sxs-lookup"><span data-stu-id="06a79-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**錯誤 \_ MCA \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1175">15205 (0x3B65) </span><span class="sxs-lookup"><span data-stu-id="06a79-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1176">發生內部監視設定 API 錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**傳回的錯誤 \_ MCA \_ 無效 \_ 技術 \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1178">15206 (0x3B66) </span><span class="sxs-lookup"><span data-stu-id="06a79-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1179">監視器傳回的監視器技術類型無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="06a79-1180">CRT、等離子和 LCD (TFT) 是監視器技術類型的範例。</span><span class="sxs-lookup"><span data-stu-id="06a79-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="06a79-1181">此錯誤表示監視器違反了 MCCS 2.0 或 MCCS 2.0 修訂1規格。</span><span class="sxs-lookup"><span data-stu-id="06a79-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**錯誤 \_ MCA \_ 不支援 \_ 色 \_ 溫度**</span><span class="sxs-lookup"><span data-stu-id="06a79-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1183">15207 (0x3B67) </span><span class="sxs-lookup"><span data-stu-id="06a79-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1184">[**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)的呼叫者指定了目前監視器不支援的色溫。</span><span class="sxs-lookup"><span data-stu-id="06a79-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="06a79-1185">此錯誤表示監視器違反了 MCCS 2.0 或 MCCS 2.0 修訂1規格。</span><span class="sxs-lookup"><span data-stu-id="06a79-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**錯誤不 \_ 明確的 \_ 系統 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="06a79-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1187">15250 (0x3B92) </span><span class="sxs-lookup"><span data-stu-id="06a79-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1188">無法識別要求的系統裝置，因為有多個不區分的裝置可能符合識別準則。</span><span class="sxs-lookup"><span data-stu-id="06a79-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_ \_ \_ \_ 找不到錯誤系統裝置**</span><span class="sxs-lookup"><span data-stu-id="06a79-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1190">15299 (0x3BC3) </span><span class="sxs-lookup"><span data-stu-id="06a79-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1191">找不到要求的系統裝置。</span><span class="sxs-lookup"><span data-stu-id="06a79-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_ \_ 不支援錯誤雜湊 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1193">15300 (0x3BC4) </span><span class="sxs-lookup"><span data-stu-id="06a79-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1194">未在伺服器上啟用指定的雜湊版本與雜湊類型的雜湊產生。</span><span class="sxs-lookup"><span data-stu-id="06a79-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**錯誤 \_ 雜湊 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="06a79-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1196">15301 (0x3BC5) </span><span class="sxs-lookup"><span data-stu-id="06a79-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1197">從伺服器要求的雜湊無法使用或不再有效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**錯誤 \_ 次要 \_ IC \_ 提供者 \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="06a79-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1199">15321 (0x3BD9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1200">管理指定之中斷的次要中斷控制器實例並未註冊。</span><span class="sxs-lookup"><span data-stu-id="06a79-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**錯誤 \_ GPIO \_ 用戶端 \_ 資訊 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="06a79-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1202">15322 (0x3BDA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1203">GPIO 用戶端驅動程式所提供的資訊無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**\_ \_ \_ 不支援錯誤 GPIO \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="06a79-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1205">15323 (0x3BDB) </span><span class="sxs-lookup"><span data-stu-id="06a79-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1206">不支援 GPIO 用戶端驅動程式所指定的版本。</span><span class="sxs-lookup"><span data-stu-id="06a79-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**錯誤 \_ GPIO \_ 不正確 \_ 註冊封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="06a79-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1208">15324 (0x3BDC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1209">GPIO 用戶端驅動程式所提供的註冊封包無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**錯誤 \_ GPIO \_ 操作已 \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="06a79-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1211">15325 (0x3BDD) </span><span class="sxs-lookup"><span data-stu-id="06a79-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1212">指定的控制碼不支援要求的操作。</span><span class="sxs-lookup"><span data-stu-id="06a79-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**錯誤 \_ GPIO \_ 不相容的 \_ 連接 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="06a79-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1214">15326 (0x3BDE) </span><span class="sxs-lookup"><span data-stu-id="06a79-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1215">要求的連接模式與一或多個指定之 pin 的現有模式相衝突。</span><span class="sxs-lookup"><span data-stu-id="06a79-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**錯誤 \_ GPIO \_ 中斷 \_ 已取消 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="06a79-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1217">15327 (0x3BDF) </span><span class="sxs-lookup"><span data-stu-id="06a79-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1218">要求取消遮罩的插斷不會被遮罩。</span><span class="sxs-lookup"><span data-stu-id="06a79-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**錯誤 \_ 無法 \_ 切換 \_ RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="06a79-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1220">15400 (0x3C28) </span><span class="sxs-lookup"><span data-stu-id="06a79-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1221">要求的執行層級切換無法順利完成。</span><span class="sxs-lookup"><span data-stu-id="06a79-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**錯誤 \_ 不正確 \_ RUNLEVEL \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="06a79-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1223">15401 (0x3C29) </span><span class="sxs-lookup"><span data-stu-id="06a79-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1224">服務具有不正確執行層級設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="06a79-1225">服務的執行層級不得高於其相依服務的執行層級。</span><span class="sxs-lookup"><span data-stu-id="06a79-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**錯誤 \_ RUNLEVEL \_ 切換 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="06a79-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1227">15402 (0x3C2A) </span><span class="sxs-lookup"><span data-stu-id="06a79-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1228">要求的執行層級切換無法順利完成，因為一或多個服務將不會在指定的超時時間內停止或重新開機。</span><span class="sxs-lookup"><span data-stu-id="06a79-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_RUNLEVEL \_ 切換 \_ 代理程式 \_ 超時時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1230">15403 (0x3C2B) </span><span class="sxs-lookup"><span data-stu-id="06a79-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1231">執行層級切換代理程式未在指定的超時時間內回應。</span><span class="sxs-lookup"><span data-stu-id="06a79-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**錯誤 \_ RUNLEVEL \_ 切換 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="06a79-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1233">15404 (0x3C2C) </span><span class="sxs-lookup"><span data-stu-id="06a79-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1234">執行層級切換正在進行中。</span><span class="sxs-lookup"><span data-stu-id="06a79-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**錯誤 \_ 服務 \_ 失敗 \_ 自動啟動**</span><span class="sxs-lookup"><span data-stu-id="06a79-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1236">15405 (0x3C2D) </span><span class="sxs-lookup"><span data-stu-id="06a79-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1237">在執行層級切換的服務啟動階段期間，有一或多項服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06a79-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**\_COM \_ TASK \_ 停止 \_ 暫止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1239">15501 (0x3C8D) </span><span class="sxs-lookup"><span data-stu-id="06a79-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1240">因為工作需要更多時間才能關閉，所以無法立即完成工作停止要求。</span><span class="sxs-lookup"><span data-stu-id="06a79-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**\_安裝 \_ 開啟 \_ 套件 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1242">15600 (0x3CF0) </span><span class="sxs-lookup"><span data-stu-id="06a79-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1243">無法開啟封裝。</span><span class="sxs-lookup"><span data-stu-id="06a79-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**\_ \_ \_ 找不到安裝 \_ 套件的錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1245">15601 (0x3CF1) </span><span class="sxs-lookup"><span data-stu-id="06a79-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1246">找不到封裝。</span><span class="sxs-lookup"><span data-stu-id="06a79-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**\_安裝 \_ 不正確 \_ 套件時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1248">15602 (0x3CF2) </span><span class="sxs-lookup"><span data-stu-id="06a79-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1249">封裝資料無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**錯誤 \_ 安裝 \_ 解析相依性 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1251">15603 (0x3CF3) </span><span class="sxs-lookup"><span data-stu-id="06a79-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1252">封裝失敗的更新、相依性或衝突驗證。</span><span class="sxs-lookup"><span data-stu-id="06a79-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**\_ \_ \_ \_ 磁片 \_ 空間安裝錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1254">15604 (0x3CF4) </span><span class="sxs-lookup"><span data-stu-id="06a79-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1255">您的電腦上沒有足夠的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="06a79-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="06a79-1256">請釋放一些空間，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="06a79-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**\_安裝 \_ 網路 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1258">15605 (0x3CF5) </span><span class="sxs-lookup"><span data-stu-id="06a79-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1259">下載您的產品時發生問題。</span><span class="sxs-lookup"><span data-stu-id="06a79-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**\_安裝 \_ 註冊 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1261">15606 (0x3CF6) </span><span class="sxs-lookup"><span data-stu-id="06a79-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1262">無法註冊封裝。</span><span class="sxs-lookup"><span data-stu-id="06a79-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**\_安裝取消 \_ 註冊 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1264">15607 (0x3CF7) </span><span class="sxs-lookup"><span data-stu-id="06a79-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1265">無法取消註冊封裝。</span><span class="sxs-lookup"><span data-stu-id="06a79-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**\_安裝 \_ 取消時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1267">15608 (0x3CF8) </span><span class="sxs-lookup"><span data-stu-id="06a79-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1268">使用者已取消安裝要求。</span><span class="sxs-lookup"><span data-stu-id="06a79-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**\_安裝錯誤 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1270">15609 (0x3CF9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1271">安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1271">Install failed.</span></span> <span data-ttu-id="06a79-1272">請洽詢您的軟體廠商。</span><span class="sxs-lookup"><span data-stu-id="06a79-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_移除錯誤 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1274">15610 (0x3CFA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1275">移除失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1275">Removal failed.</span></span> <span data-ttu-id="06a79-1276">請洽詢您的軟體廠商。</span><span class="sxs-lookup"><span data-stu-id="06a79-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**錯誤 \_ 封裝 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="06a79-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1278">15611 (0x3CFB) </span><span class="sxs-lookup"><span data-stu-id="06a79-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1279">提供的封裝已安裝，且已封鎖重新安裝套件。</span><span class="sxs-lookup"><span data-stu-id="06a79-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="06a79-1280">請查看 AppXDeployment-Server 事件記錄檔，以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06a79-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**錯誤 \_ 需要 \_ 補救**</span><span class="sxs-lookup"><span data-stu-id="06a79-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1282">15612 (0x3CFC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1283">無法啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="06a79-1283">The application cannot be started.</span></span> <span data-ttu-id="06a79-1284">請嘗試重新安裝應用程式以修正問題。</span><span class="sxs-lookup"><span data-stu-id="06a79-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**錯誤 \_ 安裝 \_ 先決條件 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1286">15613 (0x3CFD) </span><span class="sxs-lookup"><span data-stu-id="06a79-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1287">無法滿足安裝的先決條件。</span><span class="sxs-lookup"><span data-stu-id="06a79-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**錯誤 \_ 套件存放 \_ 庫 \_ 損毀**</span><span class="sxs-lookup"><span data-stu-id="06a79-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1289">15614 (0x3CFE) </span><span class="sxs-lookup"><span data-stu-id="06a79-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1290">套件存放庫已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**\_安裝 \_ 原則 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1292">15615 (0x3CFF) </span><span class="sxs-lookup"><span data-stu-id="06a79-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1293">若要安裝此應用程式，您需要 Windows 開發人員授權或啟用側載功能的系統。</span><span class="sxs-lookup"><span data-stu-id="06a79-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_更新錯誤套件 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1295">15616 (0x3D00) </span><span class="sxs-lookup"><span data-stu-id="06a79-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1296">應用程式目前正在更新，所以無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06a79-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_ \_ 原則封鎖錯誤 \_ 部署 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1298">15617 (0x3D01) </span><span class="sxs-lookup"><span data-stu-id="06a79-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1299">原則封鎖了封裝部署作業。</span><span class="sxs-lookup"><span data-stu-id="06a79-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="06a79-1300">請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="06a79-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_ \_ 使用中的錯誤套件 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1302">15618 (0x3D02) </span><span class="sxs-lookup"><span data-stu-id="06a79-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1303">無法安裝封裝，因為它修改的資源目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="06a79-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**錯誤 \_ 修復 \_ 檔案 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="06a79-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1305">15619 (0x3D03) </span><span class="sxs-lookup"><span data-stu-id="06a79-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1306">無法復原封裝，因為復原所需的資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**錯誤的分段簽章 \_ 無效 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1308">15620 (0x3D04) </span><span class="sxs-lookup"><span data-stu-id="06a79-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1309">簽章無效。</span><span class="sxs-lookup"><span data-stu-id="06a79-1309">The signature is invalid.</span></span> <span data-ttu-id="06a79-1310">若要在開發人員模式下註冊，Appxsignature.p7x. appxsignature.p7x 和 AppxBlockMap.xml 必須是有效的，否則不應該存在。</span><span class="sxs-lookup"><span data-stu-id="06a79-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**\_刪除 \_ 現有的 \_ APPLICATIONDATA \_ 存放區 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1312">15621 (0x3D05) </span><span class="sxs-lookup"><span data-stu-id="06a79-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1313">刪除封裝先前現有的應用程式資料時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**\_安裝 \_ 套件 \_ 降級時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1315">15622 (0x3D06) </span><span class="sxs-lookup"><span data-stu-id="06a79-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1316">無法安裝封裝，因為已安裝此套件的較高版本。</span><span class="sxs-lookup"><span data-stu-id="06a79-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**錯誤 \_ 系統 \_ 需要 \_ 補救**</span><span class="sxs-lookup"><span data-stu-id="06a79-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1318">15623 (0x3D07) </span><span class="sxs-lookup"><span data-stu-id="06a79-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1319">偵測到系統二進位檔中有錯誤。</span><span class="sxs-lookup"><span data-stu-id="06a79-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="06a79-1320">請嘗試重新整理電腦以修正問題。</span><span class="sxs-lookup"><span data-stu-id="06a79-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**錯誤 \_ APPX \_ 完整性 \_ 失敗 \_ CLR \_ NGEN**</span><span class="sxs-lookup"><span data-stu-id="06a79-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1322">15624 (0x3D08) </span><span class="sxs-lookup"><span data-stu-id="06a79-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1323">在系統上偵測到損毀的 CLR NGEN 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="06a79-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**錯誤 \_ 復原 \_ 檔案 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="06a79-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1325">15625 (0x3D09) </span><span class="sxs-lookup"><span data-stu-id="06a79-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1326">因為復原所需的資料已損毀，所以無法繼續操作。</span><span class="sxs-lookup"><span data-stu-id="06a79-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**\_安裝 \_ 防火牆 \_ 服務 \_ 未 \_ 執行時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="06a79-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1328">15626 (0x3D0A) </span><span class="sxs-lookup"><span data-stu-id="06a79-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1329">無法安裝封裝，因為 Windows 防火牆服務未執行。</span><span class="sxs-lookup"><span data-stu-id="06a79-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="06a79-1330">啟用 Windows 防火牆服務，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="06a79-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL \_ 錯誤 \_ 沒有 \_ 套件**</span><span class="sxs-lookup"><span data-stu-id="06a79-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1332">15700 (0x3D54) </span><span class="sxs-lookup"><span data-stu-id="06a79-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1333">進程沒有套件識別。</span><span class="sxs-lookup"><span data-stu-id="06a79-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**已損毀的 APPMODEL \_ 錯誤 \_ 套件 \_ 運行 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="06a79-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1335">15701 (0x3D55) </span><span class="sxs-lookup"><span data-stu-id="06a79-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1336">封裝執行時間資訊已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**已損毀的 APPMODEL \_ 錯誤 \_ 套件身分 \_ 識別 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1338">15702 (0x3D56) </span><span class="sxs-lookup"><span data-stu-id="06a79-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1339">封裝身分識別已損毀。</span><span class="sxs-lookup"><span data-stu-id="06a79-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL \_ 錯誤 \_ 沒有 \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="06a79-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1341">15703 (0x3D57) </span><span class="sxs-lookup"><span data-stu-id="06a79-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1342">進程沒有應用程式識別。</span><span class="sxs-lookup"><span data-stu-id="06a79-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**錯誤 \_ 狀態 \_ 載入 \_ 存放區 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1344">15800 (0x3DB8) </span><span class="sxs-lookup"><span data-stu-id="06a79-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1345">載入狀態存放區失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**錯誤 \_ 狀態 \_ 取得 \_ 版本 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1347">15801 (0x3DB9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1348">取得應用程式的狀態版本失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**錯誤 \_ 狀態 \_ 集 \_ 版本 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1350">15802 (0x3DBA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1351">設定應用程式的狀態版本失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**錯誤 \_ 狀態 \_ 結構化 \_ 重設 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1353">15803 (0x3DBB) </span><span class="sxs-lookup"><span data-stu-id="06a79-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1354">重設應用程式的結構化狀態失敗。</span><span class="sxs-lookup"><span data-stu-id="06a79-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**錯誤 \_ 狀態 \_ 開啟 \_ 容器 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1356">15804 (0x3DBC) </span><span class="sxs-lookup"><span data-stu-id="06a79-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1357">狀態管理員無法開啟容器。</span><span class="sxs-lookup"><span data-stu-id="06a79-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**錯誤 \_ 狀態 \_ 建立 \_ 容器 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1359">15805 (0x3DBD) </span><span class="sxs-lookup"><span data-stu-id="06a79-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1360">狀態管理員無法建立容器。</span><span class="sxs-lookup"><span data-stu-id="06a79-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**錯誤 \_ 狀態 \_ 刪除 \_ 容器 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1362">15806 (0x3DBE) </span><span class="sxs-lookup"><span data-stu-id="06a79-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1363">狀態管理員無法刪除容器。</span><span class="sxs-lookup"><span data-stu-id="06a79-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**錯誤 \_ 狀態 \_ 讀取 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1365">15807 (0x3DBF) </span><span class="sxs-lookup"><span data-stu-id="06a79-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1366">狀態管理員無法讀取設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**錯誤 \_ 狀態 \_ 寫入 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1368">15808 (0x3DC0) </span><span class="sxs-lookup"><span data-stu-id="06a79-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1369">狀態管理員無法寫入設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**錯誤 \_ 狀態 \_ 刪除 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1371">15809 (0x3DC1) </span><span class="sxs-lookup"><span data-stu-id="06a79-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1372">狀態管理員無法刪除設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**錯誤 \_ 狀態 \_ 查詢 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1374">15810 (0x3DC2) </span><span class="sxs-lookup"><span data-stu-id="06a79-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1375">狀態管理員無法查詢設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**錯誤 \_ 狀態 \_ 讀取 \_ 複合 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1377">15811 (0x3DC3) </span><span class="sxs-lookup"><span data-stu-id="06a79-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1378">狀態管理員無法讀取複合設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**錯誤 \_ 狀態 \_ 寫入 \_ 複合 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1380">15812 (0x3DC4) </span><span class="sxs-lookup"><span data-stu-id="06a79-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1381">狀態管理員無法寫入複合設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**錯誤 \_ 狀態 \_ 列舉 \_ 容器 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1383">15813 (0x3DC5) </span><span class="sxs-lookup"><span data-stu-id="06a79-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1384">狀態管理員無法列舉容器。</span><span class="sxs-lookup"><span data-stu-id="06a79-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**錯誤 \_ 狀態 \_ 列舉 \_ 設定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="06a79-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1386">15814 (0x3DC6) </span><span class="sxs-lookup"><span data-stu-id="06a79-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1387">狀態管理員無法列舉設定。</span><span class="sxs-lookup"><span data-stu-id="06a79-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**已 \_ 超過錯誤狀態 \_ 複合 \_ 設定 \_ 值 \_ 大小 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1389">15815 (0x3DC7) </span><span class="sxs-lookup"><span data-stu-id="06a79-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1390">狀態管理員複合設定值的大小已超過限制。</span><span class="sxs-lookup"><span data-stu-id="06a79-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 設定 \_ 值 \_ 大小 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1392">15816 (0x3DC8) </span><span class="sxs-lookup"><span data-stu-id="06a79-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1393">狀態管理員設定值的大小已超過限制。</span><span class="sxs-lookup"><span data-stu-id="06a79-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 設定的 \_ 名稱 \_ 大小 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1395">15817 (0x3DC9) </span><span class="sxs-lookup"><span data-stu-id="06a79-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1396">狀態管理員設定名稱的長度已超過限制。</span><span class="sxs-lookup"><span data-stu-id="06a79-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_超過錯誤狀態 \_ 容器 \_ 名稱 \_ 大小 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="06a79-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1398">15818 (0x3DCA) </span><span class="sxs-lookup"><span data-stu-id="06a79-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1399">狀態管理員容器名稱的長度已超過限制。</span><span class="sxs-lookup"><span data-stu-id="06a79-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06a79-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**錯誤 \_ API \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="06a79-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a79-1401">15841 (0x3DE1) </span><span class="sxs-lookup"><span data-stu-id="06a79-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="06a79-1402">此 API 無法在呼叫端的應用程式類型內容中使用。</span><span class="sxs-lookup"><span data-stu-id="06a79-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06a79-1403">規格需求</span><span class="sxs-lookup"><span data-stu-id="06a79-1403">Requirements</span></span>



| <span data-ttu-id="06a79-1404">需求</span><span class="sxs-lookup"><span data-stu-id="06a79-1404">Requirement</span></span> | <span data-ttu-id="06a79-1405">值</span><span class="sxs-lookup"><span data-stu-id="06a79-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06a79-1406">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06a79-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="06a79-1407">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06a79-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06a79-1408">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06a79-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="06a79-1409">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06a79-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06a79-1410">標頭</span><span class="sxs-lookup"><span data-stu-id="06a79-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a79-1411"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="06a79-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a79-1412">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06a79-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a79-1413">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="06a79-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 

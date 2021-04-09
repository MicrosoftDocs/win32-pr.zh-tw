---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1700-3999，適用于開發人員。
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: '系統錯誤碼 (1700-3999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847068"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="6c124-103">系統錯誤碼 (1700-3999) </span><span class="sxs-lookup"><span data-stu-id="6c124-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="6c124-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c124-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6c124-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="6c124-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6c124-106">下列清單描述錯誤1700到3999的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c124-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="6c124-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="6c124-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6c124-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="6c124-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6c124-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC \_ S \_ 不正確 \_ 字串 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="6c124-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-110">1700 (0x6A4) </span><span class="sxs-lookup"><span data-stu-id="6c124-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-111">字串系結無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC \_ S \_ 錯誤的系結 \_ 類型 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-113">1701 (0x6A5) </span><span class="sxs-lookup"><span data-stu-id="6c124-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-114">系結控制碼不是正確的類型。</span><span class="sxs-lookup"><span data-stu-id="6c124-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC \_ S \_ 不正確系結 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-116">1702 (0x6A6) </span><span class="sxs-lookup"><span data-stu-id="6c124-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-117">系結控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_ \_ \_ 不支援 RPC S \_ PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="6c124-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-119">1703 (0x6A7) </span><span class="sxs-lookup"><span data-stu-id="6c124-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-120">不支援 RPC 通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="6c124-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ 不正確 \_ RPC \_ PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="6c124-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-122">1704 (0x6A8) </span><span class="sxs-lookup"><span data-stu-id="6c124-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-123">RPC 通訊協定序列無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC \_ S \_ 不正確 \_ 字串 \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="6c124-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-125">1705 (0x6A9) </span><span class="sxs-lookup"><span data-stu-id="6c124-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-126">字串通用唯一識別碼 (UUID) 無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC \_ S \_ 不正確 \_ 端點 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="6c124-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-128">1706 (0x6AA) </span><span class="sxs-lookup"><span data-stu-id="6c124-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-129">端點格式無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ 不正確 \_ NET \_ ADDR**</span><span class="sxs-lookup"><span data-stu-id="6c124-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-131">1707 (0x6AB) </span><span class="sxs-lookup"><span data-stu-id="6c124-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-132">網路位址無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ \_ 找不 \_ 到端點**</span><span class="sxs-lookup"><span data-stu-id="6c124-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-134">1708 (0x6AC) </span><span class="sxs-lookup"><span data-stu-id="6c124-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-135">找不到任何端點。</span><span class="sxs-lookup"><span data-stu-id="6c124-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC \_ S \_ 不正確 \_ 超時時間**</span><span class="sxs-lookup"><span data-stu-id="6c124-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-137">1709 (0x6AD) </span><span class="sxs-lookup"><span data-stu-id="6c124-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-138">Timeout 值無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 物件**</span><span class="sxs-lookup"><span data-stu-id="6c124-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-140">1710 (0x6AE) </span><span class="sxs-lookup"><span data-stu-id="6c124-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-141">找不到 (UUID) 的物件通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**\_ \_ 已 \_ 註冊 RPC**</span><span class="sxs-lookup"><span data-stu-id="6c124-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-143">1711 (0x6AF) </span><span class="sxs-lookup"><span data-stu-id="6c124-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-144">已註冊 (UUID) 的物件通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_ \_ \_ 已註冊 RPC S \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c124-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-146">1712 (0x6B0) </span><span class="sxs-lookup"><span data-stu-id="6c124-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-147">已註冊 (UUID) 類型的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ 已在 \_ 接聽**</span><span class="sxs-lookup"><span data-stu-id="6c124-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-149">1713 (0x6B1) </span><span class="sxs-lookup"><span data-stu-id="6c124-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-150">RPC 伺服器已經在接聽。</span><span class="sxs-lookup"><span data-stu-id="6c124-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ 未 \_ \_ 註冊 PROTSEQS**</span><span class="sxs-lookup"><span data-stu-id="6c124-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-152">1714 (0x6B2) </span><span class="sxs-lookup"><span data-stu-id="6c124-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-153">尚未註冊任何通訊協定序列。</span><span class="sxs-lookup"><span data-stu-id="6c124-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ 未 \_ 接聽**</span><span class="sxs-lookup"><span data-stu-id="6c124-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-155">1715 (0x6B3) </span><span class="sxs-lookup"><span data-stu-id="6c124-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-156">RPC 伺服器未接聽。</span><span class="sxs-lookup"><span data-stu-id="6c124-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC \_ S \_ 未知的 \_ MGR \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c124-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-158">1716 (0x6B4) </span><span class="sxs-lookup"><span data-stu-id="6c124-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-159">管理員類型未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ \_ 未知（ \_ 如果**</span><span class="sxs-lookup"><span data-stu-id="6c124-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-161">1717 (0x6B5) </span><span class="sxs-lookup"><span data-stu-id="6c124-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-162">介面未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ 沒有系結 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-164">1718 (0x6B6) </span><span class="sxs-lookup"><span data-stu-id="6c124-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-165">沒有任何系結。</span><span class="sxs-lookup"><span data-stu-id="6c124-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ 無 \_ PROTSEQS**</span><span class="sxs-lookup"><span data-stu-id="6c124-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-167">1719 (0x6B7) </span><span class="sxs-lookup"><span data-stu-id="6c124-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-168">沒有通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="6c124-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ 無法 \_ 建立 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="6c124-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-170">1720 (0x6B8) </span><span class="sxs-lookup"><span data-stu-id="6c124-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-171">無法建立端點。</span><span class="sxs-lookup"><span data-stu-id="6c124-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ \_ 資源不足 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-173">1721 (0x6B9) </span><span class="sxs-lookup"><span data-stu-id="6c124-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-174">可用的資源不足，無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="6c124-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC \_ S \_ 伺服器 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="6c124-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-176">1722 (0x6BA) </span><span class="sxs-lookup"><span data-stu-id="6c124-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-177">RPC 伺服器無法使用。</span><span class="sxs-lookup"><span data-stu-id="6c124-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC \_ S \_ 伺服器 \_ 太 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="6c124-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-179">1723 (0x6BB) </span><span class="sxs-lookup"><span data-stu-id="6c124-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-180">RPC 伺服器太忙碌，無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="6c124-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC \_ S \_ 不正確 \_ 網路 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="6c124-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-182">1724 (0x6BC) </span><span class="sxs-lookup"><span data-stu-id="6c124-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-183">網路選項無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S 沒有作用中的 \_ \_ 呼叫 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-185">1725 (0x6BD) </span><span class="sxs-lookup"><span data-stu-id="6c124-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-186">此執行緒上沒有作用中的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="6c124-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC \_ S \_ 呼叫 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-188">1726 (0x6BE) </span><span class="sxs-lookup"><span data-stu-id="6c124-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-189">遠端程序呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC \_ S \_ 呼叫 \_ 失敗 \_ DNE**</span><span class="sxs-lookup"><span data-stu-id="6c124-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-191">1727 (0x6BF) </span><span class="sxs-lookup"><span data-stu-id="6c124-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-192">遠端程序呼叫失敗且未執行。</span><span class="sxs-lookup"><span data-stu-id="6c124-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC \_ S \_ 通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-194">1728 (0x6C0) </span><span class="sxs-lookup"><span data-stu-id="6c124-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-195">發生 RPC) 通訊協定錯誤 (的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="6c124-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**已 \_ 拒絕 RPC S \_ PROXY \_ 存取 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-197">1729 (0x6C1) </span><span class="sxs-lookup"><span data-stu-id="6c124-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-198">拒絕存取 HTTP proxy。</span><span class="sxs-lookup"><span data-stu-id="6c124-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ S \_ 不支援的 \_ 交易 \_ SYN**</span><span class="sxs-lookup"><span data-stu-id="6c124-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-200">1730 (0x6C2) </span><span class="sxs-lookup"><span data-stu-id="6c124-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-201">RPC 伺服器不支援傳輸語法。</span><span class="sxs-lookup"><span data-stu-id="6c124-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC \_ S \_ 不支援的 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c124-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-203">1732 (0x6C4) </span><span class="sxs-lookup"><span data-stu-id="6c124-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-204">不支援 (UUID) 類型的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC \_ S \_ 無效 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="6c124-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-206">1733 (0x6C5) </span><span class="sxs-lookup"><span data-stu-id="6c124-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-207">標記無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC \_ S 系結 \_ 無效 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-209">1734 (0x6C6) </span><span class="sxs-lookup"><span data-stu-id="6c124-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-210">陣列界限無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ 沒有 \_ 專案 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-212">1735 (0x6C7) </span><span class="sxs-lookup"><span data-stu-id="6c124-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-213">系結不包含專案名稱。</span><span class="sxs-lookup"><span data-stu-id="6c124-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC \_ S \_ 不正確 \_ 名稱 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="6c124-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-215">1736 (0x6C8) </span><span class="sxs-lookup"><span data-stu-id="6c124-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-216">名稱語法無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC \_ S \_ 不支援的 \_ 名稱 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="6c124-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-218">1737 (0x6C9) </span><span class="sxs-lookup"><span data-stu-id="6c124-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-219">不支援名稱語法。</span><span class="sxs-lookup"><span data-stu-id="6c124-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ 沒有 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="6c124-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-221">1739 (0x6CB) </span><span class="sxs-lookup"><span data-stu-id="6c124-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-222">沒有任何可用的網路位址，無法用來建立 (UUID) 的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC \_ S \_ 重複 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="6c124-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-224">1740 (0x6CC) </span><span class="sxs-lookup"><span data-stu-id="6c124-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-225">端點重複。</span><span class="sxs-lookup"><span data-stu-id="6c124-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c124-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-227">1741 (0x6CD) </span><span class="sxs-lookup"><span data-stu-id="6c124-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-228">驗證類型未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC \_ S \_ 最大 \_ 呼叫數 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="6c124-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-230">1742 (0x6CE) </span><span class="sxs-lookup"><span data-stu-id="6c124-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-231">呼叫次數上限太小。</span><span class="sxs-lookup"><span data-stu-id="6c124-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC \_ S \_ 字串 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="6c124-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-233">1743 (0x6CF) </span><span class="sxs-lookup"><span data-stu-id="6c124-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-234">字串太長。</span><span class="sxs-lookup"><span data-stu-id="6c124-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="6c124-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-236">1744 (0x6D0) </span><span class="sxs-lookup"><span data-stu-id="6c124-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-237">找不到 RPC 通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="6c124-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="6c124-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-239">1745 (0x6D1) </span><span class="sxs-lookup"><span data-stu-id="6c124-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-240">程式編號超出範圍。</span><span class="sxs-lookup"><span data-stu-id="6c124-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC \_ S 系結 \_ \_ \_ 沒有 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="6c124-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-242">1746 (0x6D2) </span><span class="sxs-lookup"><span data-stu-id="6c124-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-243">系結不包含任何驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="6c124-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="6c124-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-245">1747 (0x6D3) </span><span class="sxs-lookup"><span data-stu-id="6c124-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-246">驗證服務未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC \_ S \_ 未知的 \_ 驗證 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="6c124-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-248">1748 (0x6D4) </span><span class="sxs-lookup"><span data-stu-id="6c124-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-249">驗證層級未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC \_ S \_ 不正確 \_ 驗證身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="6c124-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-251">1749 (0x6D5) </span><span class="sxs-lookup"><span data-stu-id="6c124-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-252">安全性內容無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ 未知的 \_ AUTHZ \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="6c124-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-254">1750 (0x6D6) </span><span class="sxs-lookup"><span data-stu-id="6c124-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-255">授權服務未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ 不正確 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="6c124-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-257">1751 (0x6D7) </span><span class="sxs-lookup"><span data-stu-id="6c124-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-258">專案無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ 無法 \_ 執行 \_ OP**</span><span class="sxs-lookup"><span data-stu-id="6c124-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-260">1752 (0x6D8) </span><span class="sxs-lookup"><span data-stu-id="6c124-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-261">伺服器端點無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="6c124-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-263">1753 (0x6D9) </span><span class="sxs-lookup"><span data-stu-id="6c124-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-264">端點對應程式中沒有其他可用的端點。</span><span class="sxs-lookup"><span data-stu-id="6c124-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ 沒有 \_ 要匯出的 \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="6c124-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-266">1754 (0x6DA) </span><span class="sxs-lookup"><span data-stu-id="6c124-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-267">未匯出任何介面。</span><span class="sxs-lookup"><span data-stu-id="6c124-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC \_ S \_ 不完整 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-269">1755 (0x6DB) </span><span class="sxs-lookup"><span data-stu-id="6c124-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-270">專案名稱不完整。</span><span class="sxs-lookup"><span data-stu-id="6c124-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ 無效 \_ 的 \_ 。**</span><span class="sxs-lookup"><span data-stu-id="6c124-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-272">1756 (0x6DC) </span><span class="sxs-lookup"><span data-stu-id="6c124-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-273">Version 選項無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ 沒有 \_ 更多 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="6c124-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-275">1757 (0x6DD) </span><span class="sxs-lookup"><span data-stu-id="6c124-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-276">沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="6c124-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ 並非 \_ 所有 \_ OBJ \_ UNEXPORTED**</span><span class="sxs-lookup"><span data-stu-id="6c124-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-278">1758 (0x6DE) </span><span class="sxs-lookup"><span data-stu-id="6c124-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-279">沒有任何要 unexport 的專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 介面**</span><span class="sxs-lookup"><span data-stu-id="6c124-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-281">1759 (0x6DF) </span><span class="sxs-lookup"><span data-stu-id="6c124-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-282">找不到介面。</span><span class="sxs-lookup"><span data-stu-id="6c124-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC \_ S \_ 專案 \_ 已經 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="6c124-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-284">1760 (0x6E0) </span><span class="sxs-lookup"><span data-stu-id="6c124-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-285">專案已經存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_ \_ \_ \_ 找不到 RPC S 專案**</span><span class="sxs-lookup"><span data-stu-id="6c124-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-287">1761 (0x6E1) </span><span class="sxs-lookup"><span data-stu-id="6c124-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-288">找不到專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC \_ S \_ 名稱 \_ 服務 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="6c124-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-290">1762 (0x6E2) </span><span class="sxs-lookup"><span data-stu-id="6c124-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-291">名稱服務無法使用。</span><span class="sxs-lookup"><span data-stu-id="6c124-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC \_ S \_ 不正確 \_ NAF \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-293">1763 (0x6E3) </span><span class="sxs-lookup"><span data-stu-id="6c124-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-294">網路位址系列無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ 無法 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="6c124-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-296">1764 (0x6E4) </span><span class="sxs-lookup"><span data-stu-id="6c124-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-297">不支援要求的作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S \_ 沒有 \_ 內容 \_ 可用**</span><span class="sxs-lookup"><span data-stu-id="6c124-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-299">1765 (0x6E5) </span><span class="sxs-lookup"><span data-stu-id="6c124-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-300">沒有任何安全性內容可允許模擬。</span><span class="sxs-lookup"><span data-stu-id="6c124-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC \_ S \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-302">1766 (0x6E6) </span><span class="sxs-lookup"><span data-stu-id="6c124-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-303"> (RPC) 的遠端程序呼叫中發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c124-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ 零 \_ 除**</span><span class="sxs-lookup"><span data-stu-id="6c124-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-305">1767 (0x6E7) </span><span class="sxs-lookup"><span data-stu-id="6c124-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-306">RPC 伺服器嘗試以零除的整數。</span><span class="sxs-lookup"><span data-stu-id="6c124-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC \_ S \_ 位址 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-308">1768 (0x6E8) </span><span class="sxs-lookup"><span data-stu-id="6c124-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-309">RPC 伺服器發生定址錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c124-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ DIV \_ 零**</span><span class="sxs-lookup"><span data-stu-id="6c124-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-311">1769 (0x6E9) </span><span class="sxs-lookup"><span data-stu-id="6c124-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-312">RPC 伺服器上的浮點運算導致零除。</span><span class="sxs-lookup"><span data-stu-id="6c124-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC \_ S \_ FP \_ 下溢**</span><span class="sxs-lookup"><span data-stu-id="6c124-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-314">1770 (0x6EA) </span><span class="sxs-lookup"><span data-stu-id="6c124-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-315">RPC 伺服器發生浮點下溢。</span><span class="sxs-lookup"><span data-stu-id="6c124-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC \_ S \_ FP \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="6c124-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-317">1771 (0x6EB) </span><span class="sxs-lookup"><span data-stu-id="6c124-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-318">RPC 伺服器發生浮點溢位。</span><span class="sxs-lookup"><span data-stu-id="6c124-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ 沒有 \_ 其他 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="6c124-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-320">1772 (0x6EC) </span><span class="sxs-lookup"><span data-stu-id="6c124-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-321">可用來系結 auto 控制碼的 RPC 伺服器清單已用盡。</span><span class="sxs-lookup"><span data-stu-id="6c124-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ CHAR \_ 交易 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-323">1773 (0x6ED) </span><span class="sxs-lookup"><span data-stu-id="6c124-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-324">無法開啟字元轉譯表檔。</span><span class="sxs-lookup"><span data-stu-id="6c124-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ CHAR \_ 交易 \_ 短 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="6c124-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-326">1774 (0x6EE) </span><span class="sxs-lookup"><span data-stu-id="6c124-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-327">包含字元轉譯表的檔案具有少於512個位元組。</span><span class="sxs-lookup"><span data-stu-id="6c124-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**\_ \_ \_ \_ Null 內容中的 RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-329">1775 (0x6EF) </span><span class="sxs-lookup"><span data-stu-id="6c124-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-330">在遠端程序呼叫期間，從用戶端傳遞至主機的是 null 內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC \_ X \_ SS \_ 內容 \_ 損毀**</span><span class="sxs-lookup"><span data-stu-id="6c124-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-332">1777 (0x6F1) </span><span class="sxs-lookup"><span data-stu-id="6c124-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-333">在遠端程序呼叫期間，內容控制碼已變更。</span><span class="sxs-lookup"><span data-stu-id="6c124-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS \_ 控制碼 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="6c124-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-335">1778 (0x6F2) </span><span class="sxs-lookup"><span data-stu-id="6c124-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-336">傳遞給遠端程序呼叫的系結控制碼不相符。</span><span class="sxs-lookup"><span data-stu-id="6c124-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ 無法 \_ 取得 \_ 呼叫 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-338">1779 (0x6F3) </span><span class="sxs-lookup"><span data-stu-id="6c124-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-339">Stub 無法取得遠端程序呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC \_ X \_ Null \_ REF \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="6c124-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-341">1780 (0x6F4) </span><span class="sxs-lookup"><span data-stu-id="6c124-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-342">傳遞給存根的 null 參考指標。</span><span class="sxs-lookup"><span data-stu-id="6c124-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC \_ X \_ 列舉 \_ 值 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="6c124-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-344">1781 (0x6F5) </span><span class="sxs-lookup"><span data-stu-id="6c124-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-345">列舉值超出範圍。</span><span class="sxs-lookup"><span data-stu-id="6c124-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC \_ X \_ 位元組 \_ 計數 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="6c124-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-347">1782 (0x6F6) </span><span class="sxs-lookup"><span data-stu-id="6c124-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-348">位元組計數太小。</span><span class="sxs-lookup"><span data-stu-id="6c124-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X \_ 錯誤的 \_ 存根 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6c124-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-350">1783 (0x6F7) </span><span class="sxs-lookup"><span data-stu-id="6c124-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-351">存根收到了不正確的資料。</span><span class="sxs-lookup"><span data-stu-id="6c124-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**錯誤 \_ 不正確 \_ 使用者 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="6c124-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-353">1784 (0x6F8) </span><span class="sxs-lookup"><span data-stu-id="6c124-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-354">提供的使用者緩衝區對要求的作業無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**\_無法辨識的 \_ 媒體錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-356">1785 (0x6F9) </span><span class="sxs-lookup"><span data-stu-id="6c124-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-357">無法辨認磁片媒體。</span><span class="sxs-lookup"><span data-stu-id="6c124-357">The disk media is not recognized.</span></span> <span data-ttu-id="6c124-358">它可能未格式化。</span><span class="sxs-lookup"><span data-stu-id="6c124-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**錯誤 \_ 沒有 \_ 信任 \_ LSA \_ 秘密**</span><span class="sxs-lookup"><span data-stu-id="6c124-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-360">1786 (0x6FA) </span><span class="sxs-lookup"><span data-stu-id="6c124-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-361">工作站沒有信任秘密。</span><span class="sxs-lookup"><span data-stu-id="6c124-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**錯誤 \_ 沒有 \_ 信任 \_ SAM \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="6c124-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-363">1787 (0x6FB) </span><span class="sxs-lookup"><span data-stu-id="6c124-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-364">伺服器上的安全性資料庫沒有此工作站信任關係的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c124-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**\_受信任的 \_ 網域 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-366">1788 (0x6FC) </span><span class="sxs-lookup"><span data-stu-id="6c124-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-367">主域與受信任網域之間的信任關係失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**錯誤 \_ 信任 \_ 關聯性 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-369">1789 (0x6FD) </span><span class="sxs-lookup"><span data-stu-id="6c124-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-370">此工作站和主要網域間的信任關係失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**錯誤 \_ 信任 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-372">1790 (0x6FE) </span><span class="sxs-lookup"><span data-stu-id="6c124-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-373">網路登入失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC \_ S \_ 呼叫 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="6c124-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-375">1791 (0x6FF) </span><span class="sxs-lookup"><span data-stu-id="6c124-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-376">此執行緒的遠端程序呼叫已經在進行中。</span><span class="sxs-lookup"><span data-stu-id="6c124-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**錯誤 \_ NETLOGON \_ 未 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="6c124-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-378">1792 (0x700) </span><span class="sxs-lookup"><span data-stu-id="6c124-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-379">嘗試登入，但未啟動網路登入服務。</span><span class="sxs-lookup"><span data-stu-id="6c124-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**錯誤 \_ 帳戶已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="6c124-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-381">1793 (0x701) </span><span class="sxs-lookup"><span data-stu-id="6c124-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-382">使用者的帳戶已過期。</span><span class="sxs-lookup"><span data-stu-id="6c124-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**錯誤 \_ 重新導向程式 \_ 具有 \_ 開啟 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-384">1794 (0x702) </span><span class="sxs-lookup"><span data-stu-id="6c124-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-385">重新導向器正在使用中，無法卸載。</span><span class="sxs-lookup"><span data-stu-id="6c124-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_已安裝錯誤的印表機 \_ 驅動程式 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-387">1795 (0x703) </span><span class="sxs-lookup"><span data-stu-id="6c124-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-388">已安裝指定的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6c124-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**錯誤 \_ 不明 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="6c124-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-390">1796 (0x704) </span><span class="sxs-lookup"><span data-stu-id="6c124-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-391">指定的埠未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**錯誤 \_ 未知的 \_ 印表機 \_ 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="6c124-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-393">1797 (0x705) </span><span class="sxs-lookup"><span data-stu-id="6c124-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-394">印表機驅動程式未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**錯誤 \_ 不明 \_ PRINTPROCESSOR**</span><span class="sxs-lookup"><span data-stu-id="6c124-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-396">1798 (0x706) </span><span class="sxs-lookup"><span data-stu-id="6c124-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-397">列印處理器未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**錯誤 \_ 不正確 \_ 分隔檔 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-399">1799 (0x707) </span><span class="sxs-lookup"><span data-stu-id="6c124-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-400">指定的分隔檔無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**錯誤 \_ 不正確 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="6c124-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-402">1800 (0x708) </span><span class="sxs-lookup"><span data-stu-id="6c124-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-403">指定的優先順序無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-405">1801 (0x709) </span><span class="sxs-lookup"><span data-stu-id="6c124-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-406">印表機名稱無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**錯誤 \_ 印表機 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="6c124-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-408">1802 (0x70A) </span><span class="sxs-lookup"><span data-stu-id="6c124-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-409">印表機已經存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="6c124-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-411">1803 (0x70B) </span><span class="sxs-lookup"><span data-stu-id="6c124-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-412">印表機命令無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**錯誤 \_ 的 \_ 資料類型無效**</span><span class="sxs-lookup"><span data-stu-id="6c124-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-414">1804 (0x70C) </span><span class="sxs-lookup"><span data-stu-id="6c124-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-415">指定的資料類型無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**錯誤 \_ 不正確 \_ 環境**</span><span class="sxs-lookup"><span data-stu-id="6c124-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-417">1805 (0x70D) </span><span class="sxs-lookup"><span data-stu-id="6c124-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-418">指定的環境無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ 沒有 \_ 其他 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="6c124-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-420">1806 (0x70E) </span><span class="sxs-lookup"><span data-stu-id="6c124-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-421">沒有其他系結。</span><span class="sxs-lookup"><span data-stu-id="6c124-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**\_NOLOGON \_ 域間 \_ 信任 \_ 帳戶時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-423">1807 (0x70F) </span><span class="sxs-lookup"><span data-stu-id="6c124-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-424">使用的帳戶是限域的信任帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c124-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="6c124-425">使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。</span><span class="sxs-lookup"><span data-stu-id="6c124-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**\_NOLOGON \_ 工作站 \_ 信任 \_ 帳戶時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-427">1808 (0x710) </span><span class="sxs-lookup"><span data-stu-id="6c124-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-428">使用的帳戶是電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c124-428">The account used is a computer account.</span></span> <span data-ttu-id="6c124-429">使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。</span><span class="sxs-lookup"><span data-stu-id="6c124-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**\_NOLOGON \_ 伺服器 \_ 信任 \_ 帳戶時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-431">1809 (0x711) </span><span class="sxs-lookup"><span data-stu-id="6c124-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-432">使用的帳戶是伺服器信任帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c124-432">The account used is a server trust account.</span></span> <span data-ttu-id="6c124-433">使用您的全域使用者帳戶或本機使用者帳戶來存取此伺服器。</span><span class="sxs-lookup"><span data-stu-id="6c124-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**錯誤 \_ 網域 \_ 信任 \_ 不一致**</span><span class="sxs-lookup"><span data-stu-id="6c124-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-435">1810 (0x712) </span><span class="sxs-lookup"><span data-stu-id="6c124-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-436">指定網域 (SID) 的名稱或安全性識別碼，與該網域的信任資訊不一致。</span><span class="sxs-lookup"><span data-stu-id="6c124-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**錯誤 \_ 伺服器 \_ 有 \_ 開啟的 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-438">1811 (0x713) </span><span class="sxs-lookup"><span data-stu-id="6c124-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-439">伺服器正在使用中，無法卸載。</span><span class="sxs-lookup"><span data-stu-id="6c124-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源資料**</span><span class="sxs-lookup"><span data-stu-id="6c124-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-441">1812 (0x714) </span><span class="sxs-lookup"><span data-stu-id="6c124-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-442">指定的影像檔案未包含資源區段。</span><span class="sxs-lookup"><span data-stu-id="6c124-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源類型**</span><span class="sxs-lookup"><span data-stu-id="6c124-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-444">1813 (0x715) </span><span class="sxs-lookup"><span data-stu-id="6c124-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-445">在影像檔中找不到指定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="6c124-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資源名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-447">1814 (0x716) </span><span class="sxs-lookup"><span data-stu-id="6c124-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-448">在影像檔中找不到指定的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6c124-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資來源語言**</span><span class="sxs-lookup"><span data-stu-id="6c124-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-450">1815 (0x717) </span><span class="sxs-lookup"><span data-stu-id="6c124-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-451">在影像檔中找不到指定的資源語言識別項。</span><span class="sxs-lookup"><span data-stu-id="6c124-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**錯誤 \_ 的 \_ \_ 配額不足**</span><span class="sxs-lookup"><span data-stu-id="6c124-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-453">1816 (0x718) </span><span class="sxs-lookup"><span data-stu-id="6c124-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-454">配額不足，無法處理此命令。</span><span class="sxs-lookup"><span data-stu-id="6c124-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ 沒有 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="6c124-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-456">1817 (0x719) </span><span class="sxs-lookup"><span data-stu-id="6c124-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-457">未註冊任何介面。</span><span class="sxs-lookup"><span data-stu-id="6c124-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC \_ S \_ 呼叫已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="6c124-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-459">1818 (0x71A) </span><span class="sxs-lookup"><span data-stu-id="6c124-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-460">遠端程序呼叫已取消。</span><span class="sxs-lookup"><span data-stu-id="6c124-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC \_ S 系結 \_ \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="6c124-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-462">1819 (0x71B) </span><span class="sxs-lookup"><span data-stu-id="6c124-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-463">系結控制碼不包含所有必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="6c124-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC \_ S \_ 通訊 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-465">1820 (0x71C) </span><span class="sxs-lookup"><span data-stu-id="6c124-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-466">遠端程序呼叫期間發生通訊失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC \_ S \_ 不支援的 \_ 驗證 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="6c124-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-468">1821 (0x71D) </span><span class="sxs-lookup"><span data-stu-id="6c124-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-469">不支援要求的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="6c124-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ 沒有 \_ PRINC \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-471">1822 (0x71E) </span><span class="sxs-lookup"><span data-stu-id="6c124-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-472">未註冊任何主體名稱。</span><span class="sxs-lookup"><span data-stu-id="6c124-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ 不 \_ RPC \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-474">1823 (0x71F) </span><span class="sxs-lookup"><span data-stu-id="6c124-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-475">指定的錯誤不是有效的 Windows RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c124-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_僅限 RPC S 的 \_ \_ 本機 UUID \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-477">1824 (0x720) </span><span class="sxs-lookup"><span data-stu-id="6c124-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-478">只有在這部電腦上才有有效的 UUID。</span><span class="sxs-lookup"><span data-stu-id="6c124-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC \_ S \_ SEC \_ PKG \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-480">1825 (0x721) </span><span class="sxs-lookup"><span data-stu-id="6c124-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-481">發生安全性封裝特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c124-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ 未 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="6c124-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-483">1826 (0x722) </span><span class="sxs-lookup"><span data-stu-id="6c124-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-484">執行緒尚未取消。</span><span class="sxs-lookup"><span data-stu-id="6c124-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC \_ X \_ 不正確 \_ ES \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="6c124-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-486">1827 (0x723) </span><span class="sxs-lookup"><span data-stu-id="6c124-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-487">編碼/解碼控制碼的操作無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ 錯誤的 \_ ES \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="6c124-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-489">1828 (0x724) </span><span class="sxs-lookup"><span data-stu-id="6c124-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-490">序列化封裝的版本不相容。</span><span class="sxs-lookup"><span data-stu-id="6c124-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC \_ X \_ 錯誤的 \_ 存根 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="6c124-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-492">1829 (0x725) </span><span class="sxs-lookup"><span data-stu-id="6c124-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-493">RPC 存根的版本不相容。</span><span class="sxs-lookup"><span data-stu-id="6c124-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ 不正確 \_ 管道 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="6c124-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-495">1830 (0x726) </span><span class="sxs-lookup"><span data-stu-id="6c124-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-496">RPC 管道物件無效或已損毀。</span><span class="sxs-lookup"><span data-stu-id="6c124-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X \_ 錯誤的 \_ 管道 \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="6c124-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-498">1831 (0x727) </span><span class="sxs-lookup"><span data-stu-id="6c124-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-499">在 RPC 管道物件上嘗試了不正確作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X \_ 錯誤的 \_ 管道 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="6c124-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-501">1832 (0x728) </span><span class="sxs-lookup"><span data-stu-id="6c124-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-502">不支援的 RPC 管道版本。</span><span class="sxs-lookup"><span data-stu-id="6c124-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC \_ S \_ COOKIE \_ 驗證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-504">1833 (0x729) </span><span class="sxs-lookup"><span data-stu-id="6c124-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-505">HTTP proxy 伺服器因為 cookie 驗證失敗，所以拒絕連線。</span><span class="sxs-lookup"><span data-stu-id="6c124-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ \_ \_ \_ 找不到 RPC S 群組成員**</span><span class="sxs-lookup"><span data-stu-id="6c124-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-507">1898 (0x76A) </span><span class="sxs-lookup"><span data-stu-id="6c124-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-508">找不到群組成員。</span><span class="sxs-lookup"><span data-stu-id="6c124-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ 無法 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="6c124-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-510">1899 (0x76B) </span><span class="sxs-lookup"><span data-stu-id="6c124-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-511">無法建立端點對應程式資料庫專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC \_ S \_ 無效 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="6c124-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-513">1900 (0x76C) </span><span class="sxs-lookup"><span data-stu-id="6c124-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-514">物件通用唯一識別碼 (UUID) 是 nil UUID。</span><span class="sxs-lookup"><span data-stu-id="6c124-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**錯誤 \_ 不正確 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="6c124-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-516">1901 (0x76D) </span><span class="sxs-lookup"><span data-stu-id="6c124-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-517">指定的時間無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**錯誤 \_ 不正確 \_ 表單 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6c124-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-519">1902 (0x76E) </span><span class="sxs-lookup"><span data-stu-id="6c124-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-520">指定的表單名稱無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**錯誤 \_ 的 \_ 表單 \_ 大小無效**</span><span class="sxs-lookup"><span data-stu-id="6c124-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-522">1903 (0x76F) </span><span class="sxs-lookup"><span data-stu-id="6c124-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-523">指定的表單大小無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**錯誤 \_ 已在 \_ 等候**</span><span class="sxs-lookup"><span data-stu-id="6c124-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-525">1904 (0x770) </span><span class="sxs-lookup"><span data-stu-id="6c124-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-526">指定的印表機控制碼已在等候。</span><span class="sxs-lookup"><span data-stu-id="6c124-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**\_印表機 \_ 已刪除錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-528">1905 (0x771) </span><span class="sxs-lookup"><span data-stu-id="6c124-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-529">指定的印表機已刪除。</span><span class="sxs-lookup"><span data-stu-id="6c124-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="6c124-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-531">1906 (0x772) </span><span class="sxs-lookup"><span data-stu-id="6c124-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-532">印表機的狀態無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**錯誤 \_ 密碼 \_ 必須 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="6c124-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-534">1907 (0x773) </span><span class="sxs-lookup"><span data-stu-id="6c124-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-535">使用者的密碼必須在登入之前變更。</span><span class="sxs-lookup"><span data-stu-id="6c124-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**\_ \_ \_ 找不到域 \_ 控制器的錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-537">1908 (0x774) </span><span class="sxs-lookup"><span data-stu-id="6c124-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-538">找不到此網域的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="6c124-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**錯誤 \_ 帳戶 \_ 被鎖定 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-540">1909 (0x775) </span><span class="sxs-lookup"><span data-stu-id="6c124-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-541">參考的帳戶目前已被鎖定，而且可能無法登入。</span><span class="sxs-lookup"><span data-stu-id="6c124-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**或 \_ 不正確 \_ OXID**</span><span class="sxs-lookup"><span data-stu-id="6c124-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-543">1910 (0x776) </span><span class="sxs-lookup"><span data-stu-id="6c124-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-544">找不到指定的物件匯出工具。</span><span class="sxs-lookup"><span data-stu-id="6c124-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**或 \_ 不正確 \_ OID**</span><span class="sxs-lookup"><span data-stu-id="6c124-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-546">1911 (0x777) </span><span class="sxs-lookup"><span data-stu-id="6c124-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-547">找不到指定的物件。</span><span class="sxs-lookup"><span data-stu-id="6c124-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**或 \_ 不正確 \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="6c124-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-549">1912 (0x778) </span><span class="sxs-lookup"><span data-stu-id="6c124-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-550">找不到指定的物件解析程式集合。</span><span class="sxs-lookup"><span data-stu-id="6c124-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ 傳送 \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="6c124-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-552">1913 (0x779) </span><span class="sxs-lookup"><span data-stu-id="6c124-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-553">某些資料仍會在要求緩衝區中傳送。</span><span class="sxs-lookup"><span data-stu-id="6c124-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ 不正確 \_ 非同步 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-555">1914 (0x77A) </span><span class="sxs-lookup"><span data-stu-id="6c124-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-556">非同步遠端程序呼叫控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ 不正確 \_ 非同步 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="6c124-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-558">1915 (0x77B) </span><span class="sxs-lookup"><span data-stu-id="6c124-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-559">此操作的非同步 RPC 呼叫控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC \_ X \_ 管線 \_ 已關閉**</span><span class="sxs-lookup"><span data-stu-id="6c124-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-561">1916 (0x77C) </span><span class="sxs-lookup"><span data-stu-id="6c124-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-562">RPC 管道物件已經關閉。</span><span class="sxs-lookup"><span data-stu-id="6c124-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC \_ X \_ 管道 \_ 專業 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-564">1917 (0x77D) </span><span class="sxs-lookup"><span data-stu-id="6c124-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-565">RPC 呼叫會在處理所有管道之前完成。</span><span class="sxs-lookup"><span data-stu-id="6c124-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC \_ X \_ 管道 \_ 空白**</span><span class="sxs-lookup"><span data-stu-id="6c124-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-567">1918 (0x77E) </span><span class="sxs-lookup"><span data-stu-id="6c124-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-568">RPC 管道中沒有其他可用的資料。</span><span class="sxs-lookup"><span data-stu-id="6c124-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**錯誤 \_ 的 \_ SITENAME**</span><span class="sxs-lookup"><span data-stu-id="6c124-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-570">1919 (0x77F) </span><span class="sxs-lookup"><span data-stu-id="6c124-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-571">這部電腦沒有可用的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="6c124-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**無法存取檔案時發生錯誤 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-573">1920 (0x780) </span><span class="sxs-lookup"><span data-stu-id="6c124-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-574">系統無法存取檔案。</span><span class="sxs-lookup"><span data-stu-id="6c124-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**錯誤 \_ 無法 \_ 解析 \_ 檔案名**</span><span class="sxs-lookup"><span data-stu-id="6c124-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-576">1921 (0x781) </span><span class="sxs-lookup"><span data-stu-id="6c124-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-577">系統無法解析檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c124-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC \_ S \_ 專案 \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="6c124-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-579">1922 (0x782) </span><span class="sxs-lookup"><span data-stu-id="6c124-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-580">專案不是預期的類型。</span><span class="sxs-lookup"><span data-stu-id="6c124-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ 未 \_ \_ 匯出所有 OBJ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-582">1923 (0x783) </span><span class="sxs-lookup"><span data-stu-id="6c124-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-583">並非所有物件 Uuid 都可以匯出至指定的專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_ \_ \_ 未匯出 RPC S \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="6c124-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-585">1924 (0x784) </span><span class="sxs-lookup"><span data-stu-id="6c124-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-586">無法將介面匯出至指定的專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_ \_ \_ 未新增 RPC S 設定檔 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-588">1925 (0x785) </span><span class="sxs-lookup"><span data-stu-id="6c124-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-589">無法加入指定的設定檔專案。</span><span class="sxs-lookup"><span data-stu-id="6c124-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT \_ 未 \_ 加入**</span><span class="sxs-lookup"><span data-stu-id="6c124-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-591">1926 (0x786) </span><span class="sxs-lookup"><span data-stu-id="6c124-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-592">無法加入指定的設定檔元素。</span><span class="sxs-lookup"><span data-stu-id="6c124-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT \_ 未 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="6c124-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-594">1927 (0x787) </span><span class="sxs-lookup"><span data-stu-id="6c124-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-595">無法移除指定的設定檔元素。</span><span class="sxs-lookup"><span data-stu-id="6c124-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**\_ \_ \_ \_ 未加入 RPC S GRP \_ ELT**</span><span class="sxs-lookup"><span data-stu-id="6c124-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-597">1928 (0x788) </span><span class="sxs-lookup"><span data-stu-id="6c124-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-598">無法加入群組元素。</span><span class="sxs-lookup"><span data-stu-id="6c124-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**\_ \_ \_ \_ 未移除 RPC S GRP \_ ELT**</span><span class="sxs-lookup"><span data-stu-id="6c124-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-600">1929 (0x789) </span><span class="sxs-lookup"><span data-stu-id="6c124-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-601">無法移除群組元素。</span><span class="sxs-lookup"><span data-stu-id="6c124-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**已 \_ 封鎖錯誤公里 \_ 驅動程式 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-603">1930 (0x78A) </span><span class="sxs-lookup"><span data-stu-id="6c124-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-604">印表機驅動程式與封鎖 NT 4.0 驅動程式的電腦上啟用的原則不相容。</span><span class="sxs-lookup"><span data-stu-id="6c124-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**錯誤 \_ 內容已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="6c124-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-606">1931 (0x78B) </span><span class="sxs-lookup"><span data-stu-id="6c124-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-607">內容已過期，無法再使用。</span><span class="sxs-lookup"><span data-stu-id="6c124-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**\_超過每個 \_ 使用者 \_ 信任 \_ 配額 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-609">1932 (0x78C) </span><span class="sxs-lookup"><span data-stu-id="6c124-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-610">已超過目前使用者的委派信任建立配額。</span><span class="sxs-lookup"><span data-stu-id="6c124-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**\_超出所有 \_ 使用者 \_ 信任 \_ 配額 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-612">1933 (0x78D) </span><span class="sxs-lookup"><span data-stu-id="6c124-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-613">已超過委派的信任建立配額總數。</span><span class="sxs-lookup"><span data-stu-id="6c124-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**\_超過使用者 \_ 刪除 \_ 信任 \_ 配額 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-615">1934 (0x78E) </span><span class="sxs-lookup"><span data-stu-id="6c124-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-616">已超過目前使用者的委派信任刪除配額。</span><span class="sxs-lookup"><span data-stu-id="6c124-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**錯誤 \_ 驗證 \_ 防火牆 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6c124-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-618">1935 (0x78F) </span><span class="sxs-lookup"><span data-stu-id="6c124-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-619">您登入的電腦會受到驗證防火牆的保護。</span><span class="sxs-lookup"><span data-stu-id="6c124-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="6c124-620">指定的帳號不允許對電腦進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6c124-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**\_封鎖遠端 \_ 列印 \_ 連接 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-622">1936 (0x790) </span><span class="sxs-lookup"><span data-stu-id="6c124-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-623">在您的電腦上設定的原則會封鎖與列印多工緩衝處理器的遠端連線。</span><span class="sxs-lookup"><span data-stu-id="6c124-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**\_封鎖 NTLM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-625">1937 (0x791) </span><span class="sxs-lookup"><span data-stu-id="6c124-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-626">驗證失敗，因為 NTLM 驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="6c124-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_ \_ 需要變更錯誤 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="6c124-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-628">1938 (0x792) </span><span class="sxs-lookup"><span data-stu-id="6c124-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-629">登入失敗： EAS 原則會要求使用者變更其密碼，才能執行這種操作。</span><span class="sxs-lookup"><span data-stu-id="6c124-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**錯誤 \_ 不正確 \_ 圖元 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="6c124-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-631">2000 (0x7D0) </span><span class="sxs-lookup"><span data-stu-id="6c124-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-632">像素格式無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**錯誤 \_ 的 \_ 驅動程式錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-634">2001 (0x7D1) </span><span class="sxs-lookup"><span data-stu-id="6c124-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-635">指定的驅動程式無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**錯誤 \_ 不正確 \_ 視窗 \_ 樣式**</span><span class="sxs-lookup"><span data-stu-id="6c124-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-637">2002 (0x7D2) </span><span class="sxs-lookup"><span data-stu-id="6c124-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-638">此操作的視窗樣式或類別屬性無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_ \_ 不支援的錯誤中繼檔 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-640">2003 (0x7D3) </span><span class="sxs-lookup"><span data-stu-id="6c124-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-641">不支援要求的中繼檔作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_ \_ 不支援錯誤 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="6c124-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-643">2004 (0x7D4) </span><span class="sxs-lookup"><span data-stu-id="6c124-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-644">不支援要求的轉換作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_ \_ 不支援錯誤 \_ 裁剪**</span><span class="sxs-lookup"><span data-stu-id="6c124-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-646">2005 (0x7D5) </span><span class="sxs-lookup"><span data-stu-id="6c124-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-647">不支援要求的剪切作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**錯誤 \_ 不正確 \_ CMM**</span><span class="sxs-lookup"><span data-stu-id="6c124-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-649">2010 (0x7DA) </span><span class="sxs-lookup"><span data-stu-id="6c124-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-650">指定的色彩管理模組無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**錯誤 \_ 不正確 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="6c124-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-652">2011 (0x7DB) </span><span class="sxs-lookup"><span data-stu-id="6c124-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-653">指定的色彩設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_ \_ 找不到錯誤標記 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-655">2012 (0x7DC) </span><span class="sxs-lookup"><span data-stu-id="6c124-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-656">找不到指定的標記。</span><span class="sxs-lookup"><span data-stu-id="6c124-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**錯誤 \_ 標記 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="6c124-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-658">2013 (0x7DD) </span><span class="sxs-lookup"><span data-stu-id="6c124-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-659">必要的標記不存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**錯誤 \_ 重複 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="6c124-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-661">2014 (0x7DE) </span><span class="sxs-lookup"><span data-stu-id="6c124-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-662">指定的標記已存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**錯誤 \_ 配置 \_ 檔 \_ 未 \_ 與 \_ 裝置相關聯**</span><span class="sxs-lookup"><span data-stu-id="6c124-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-664">2015 (0x7DF) </span><span class="sxs-lookup"><span data-stu-id="6c124-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-665">指定的色彩設定檔未與指定的裝置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6c124-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_ \_ 找不到錯誤設定檔 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-667">2016 (0x7E0) </span><span class="sxs-lookup"><span data-stu-id="6c124-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-668">找不到指定的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="6c124-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**錯誤 \_ 無效 \_ COLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="6c124-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-670">2017 (0x7E1) </span><span class="sxs-lookup"><span data-stu-id="6c124-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-671">指定的色彩空間無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**錯誤 \_ ICM \_ 未 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="6c124-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-673">2018 (0x7E2) </span><span class="sxs-lookup"><span data-stu-id="6c124-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-674">未啟用影像色彩管理。</span><span class="sxs-lookup"><span data-stu-id="6c124-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**\_刪除 \_ ICM \_ XFORM 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-676">2019 (0x7E3) </span><span class="sxs-lookup"><span data-stu-id="6c124-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-677">刪除色彩轉換時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c124-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**錯誤 \_ 不正確 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="6c124-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-679">2020 (0x7E4) </span><span class="sxs-lookup"><span data-stu-id="6c124-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-680">指定的色彩轉換無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**錯誤 \_ COLORSPACE \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="6c124-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-682">2021 (0x7E5) </span><span class="sxs-lookup"><span data-stu-id="6c124-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-683">指定的轉換與點陣圖的色彩空間不符。</span><span class="sxs-lookup"><span data-stu-id="6c124-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**錯誤 \_ 無效 \_ COLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="6c124-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-685">2022 (0x7E6) </span><span class="sxs-lookup"><span data-stu-id="6c124-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-686">設定檔中不存在指定的命名色彩索引。</span><span class="sxs-lookup"><span data-stu-id="6c124-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**錯誤 \_ 設定檔不 \_ \_ \_ 符合 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="6c124-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-688">2023 (0x7E7) </span><span class="sxs-lookup"><span data-stu-id="6c124-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-689">指定的設定檔適用于類型與指定裝置不同的裝置。</span><span class="sxs-lookup"><span data-stu-id="6c124-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**\_連接 \_ 其他 \_ 密碼時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-691">2108 (0x83C) </span><span class="sxs-lookup"><span data-stu-id="6c124-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-692">已成功建立網路連線，但使用者必須收到原本指定之密碼以外的提示。</span><span class="sxs-lookup"><span data-stu-id="6c124-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**\_連接 \_ 其他 \_ 密碼 \_ 預設值時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-694">2109 (0x83D) </span><span class="sxs-lookup"><span data-stu-id="6c124-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-695">已使用預設認證成功建立網路連接。</span><span class="sxs-lookup"><span data-stu-id="6c124-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**錯誤的使用者 \_ \_ 名稱錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-697">2202 (0x89A) </span><span class="sxs-lookup"><span data-stu-id="6c124-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-698">指定的使用者名稱無效。</span><span class="sxs-lookup"><span data-stu-id="6c124-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**\_未 \_ 連線錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-700">2250 (0x8CA) </span><span class="sxs-lookup"><span data-stu-id="6c124-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-701">此網路連接不存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**開啟檔案時發生錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-703">2401 (0x961) </span><span class="sxs-lookup"><span data-stu-id="6c124-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-704">此網路連線已開啟檔案或要求暫止。</span><span class="sxs-lookup"><span data-stu-id="6c124-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**使用中的連接時發生錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-706">2402 (0x962) </span><span class="sxs-lookup"><span data-stu-id="6c124-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-707">作用中的連接仍然存在。</span><span class="sxs-lookup"><span data-stu-id="6c124-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_ \_ 使用中的錯誤裝置 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-709">2404 (0x964) </span><span class="sxs-lookup"><span data-stu-id="6c124-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-710">使用中的進程正在使用此裝置，因此無法中斷連線。</span><span class="sxs-lookup"><span data-stu-id="6c124-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**錯誤 \_ 不明的 \_ 列印 \_ 監視器**</span><span class="sxs-lookup"><span data-stu-id="6c124-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-712">3000 (0xBB8) </span><span class="sxs-lookup"><span data-stu-id="6c124-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-713">指定的列印監視器未知。</span><span class="sxs-lookup"><span data-stu-id="6c124-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_ \_ \_ 使用中的印表機驅動程式時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-715">3001 (0xBB9) </span><span class="sxs-lookup"><span data-stu-id="6c124-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-716">指定的印表機驅動程式目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="6c124-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ \_ 找不到錯誤的多工緩衝處理檔案**</span><span class="sxs-lookup"><span data-stu-id="6c124-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-718">3002 (0xBBA) </span><span class="sxs-lookup"><span data-stu-id="6c124-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-719">找不到多工緩衝處理檔案。</span><span class="sxs-lookup"><span data-stu-id="6c124-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**\_SPL \_ 無 \_ STARTDOC 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-721">3003 (0xBBB) </span><span class="sxs-lookup"><span data-stu-id="6c124-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-722">未發出 StartDocPrinter 呼叫。</span><span class="sxs-lookup"><span data-stu-id="6c124-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**\_SPL \_ 無 \_ SYSTEM.PRINTING.PRINTQUEUE.ADDJOB 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-724">3004 (0xBBC) </span><span class="sxs-lookup"><span data-stu-id="6c124-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-725">未發出 System.printing.printqueue.addjob 呼叫。</span><span class="sxs-lookup"><span data-stu-id="6c124-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**\_ \_ \_ 已安裝錯誤列印 \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="6c124-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-727">3005 (0xBBD) </span><span class="sxs-lookup"><span data-stu-id="6c124-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-728">已安裝指定的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="6c124-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**\_ \_ \_ 已安裝錯誤列印 \_ 監視器**</span><span class="sxs-lookup"><span data-stu-id="6c124-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-730">3006 (0xBBE) </span><span class="sxs-lookup"><span data-stu-id="6c124-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-731">已安裝指定的列印監視器。</span><span class="sxs-lookup"><span data-stu-id="6c124-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**錯誤 \_ 不正確 \_ 列印 \_ 監視器**</span><span class="sxs-lookup"><span data-stu-id="6c124-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-733">3007 (0xBBF) </span><span class="sxs-lookup"><span data-stu-id="6c124-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-734">指定的列印監視器沒有必要的功能。</span><span class="sxs-lookup"><span data-stu-id="6c124-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**\_ \_ \_ 使用中的列印監視錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-736">3008 (0xBC0) </span><span class="sxs-lookup"><span data-stu-id="6c124-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-737">指定的列印監視器目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="6c124-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**錯誤 \_ 印表機 \_ 已將 \_ 作業 \_ 排入佇列**</span><span class="sxs-lookup"><span data-stu-id="6c124-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-739">3009 (0xBC1) </span><span class="sxs-lookup"><span data-stu-id="6c124-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-740">當有作業排入印表機佇列時，不允許要求的作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**\_ \_ 需要重新開機 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-742">3010 (0xBC2) </span><span class="sxs-lookup"><span data-stu-id="6c124-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-743">要求的作業已成功。</span><span class="sxs-lookup"><span data-stu-id="6c124-743">The requested operation is successful.</span></span> <span data-ttu-id="6c124-744">在系統重新開機之前，變更將不會生效。</span><span class="sxs-lookup"><span data-stu-id="6c124-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**\_ \_ 需要重新開機錯誤成功 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-746">3011 (0xBC3) </span><span class="sxs-lookup"><span data-stu-id="6c124-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-747">要求的作業已成功。</span><span class="sxs-lookup"><span data-stu-id="6c124-747">The requested operation is successful.</span></span> <span data-ttu-id="6c124-748">在服務重新開機之前，變更將不會生效。</span><span class="sxs-lookup"><span data-stu-id="6c124-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_ \_ 找不到錯誤印表機 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-750">3012 (0xBC4) </span><span class="sxs-lookup"><span data-stu-id="6c124-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-751">找不到任何印表機。</span><span class="sxs-lookup"><span data-stu-id="6c124-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**錯誤 \_ 印表機 \_ 驅動程式 \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="6c124-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-753">3013 (0xBC5) </span><span class="sxs-lookup"><span data-stu-id="6c124-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-754">印表機驅動程式已知不可靠。</span><span class="sxs-lookup"><span data-stu-id="6c124-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_印表機 \_ 驅動程式 \_ 封鎖錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-756">3014 (0xBC6) </span><span class="sxs-lookup"><span data-stu-id="6c124-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-757">已知印表機驅動程式會危害系統。</span><span class="sxs-lookup"><span data-stu-id="6c124-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**\_ \_ \_ \_ 使用中的印表機驅動程式套件錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-759">3015 (0xBC7) </span><span class="sxs-lookup"><span data-stu-id="6c124-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-760">指定的印表機驅動程式套件目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="6c124-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤核心驅動程式套件**</span><span class="sxs-lookup"><span data-stu-id="6c124-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-762">3016 (0xBC8) </span><span class="sxs-lookup"><span data-stu-id="6c124-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-763">找不到印表機驅動程式套件所需的核心驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="6c124-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**\_無法 \_ 重新開機 \_ 所需的錯誤**</span><span class="sxs-lookup"><span data-stu-id="6c124-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-765">3017 (0xBC9) </span><span class="sxs-lookup"><span data-stu-id="6c124-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-766">要求的作業失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-766">The requested operation failed.</span></span> <span data-ttu-id="6c124-767">需要重新開機系統，才能復原所做的變更。</span><span class="sxs-lookup"><span data-stu-id="6c124-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**啟動 \_ \_ 重新開機錯誤失敗 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-769">3018 (0xBCA) </span><span class="sxs-lookup"><span data-stu-id="6c124-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-770">要求的作業失敗。</span><span class="sxs-lookup"><span data-stu-id="6c124-770">The requested operation failed.</span></span> <span data-ttu-id="6c124-771">已起始系統重新開機以回復所做的變更。</span><span class="sxs-lookup"><span data-stu-id="6c124-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**\_需要下載錯誤的印表機 \_ 驅動程式 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-773">3019 (0xBCB) </span><span class="sxs-lookup"><span data-stu-id="6c124-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-774">在系統上找不到指定的印表機驅動程式，因此需要下載。</span><span class="sxs-lookup"><span data-stu-id="6c124-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**錯誤 \_ 列印 \_ 作業 \_ 需要重新開機 \_**</span><span class="sxs-lookup"><span data-stu-id="6c124-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-776">3020 (0xBCC) </span><span class="sxs-lookup"><span data-stu-id="6c124-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-777">要求的列印工作無法列印。</span><span class="sxs-lookup"><span data-stu-id="6c124-777">The requested print job has failed to print.</span></span> <span data-ttu-id="6c124-778">列印系統更新需要重新提交作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**錯誤 \_ 不正確 \_ 印表機 \_ 驅動程式 \_ 資訊清單**</span><span class="sxs-lookup"><span data-stu-id="6c124-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-780">3021 (0xBCD) </span><span class="sxs-lookup"><span data-stu-id="6c124-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-781">印表機驅動程式不包含有效的資訊清單，或包含太多資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6c124-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**\_ \_ 無法共用錯誤 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="6c124-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-783">3022 (0xBCE) </span><span class="sxs-lookup"><span data-stu-id="6c124-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-784">指定的印表機無法共用。</span><span class="sxs-lookup"><span data-stu-id="6c124-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**錯誤 \_ 要求已 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="6c124-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-786">3050 (0xBEA) </span><span class="sxs-lookup"><span data-stu-id="6c124-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-787">作業已暫停。</span><span class="sxs-lookup"><span data-stu-id="6c124-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c124-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**錯誤 \_ IO 重新 \_ 發出 \_ 為 \_ 快取**</span><span class="sxs-lookup"><span data-stu-id="6c124-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c124-789">3950 (0xF6E) </span><span class="sxs-lookup"><span data-stu-id="6c124-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="6c124-790">將指定的作業重新發出為快取的 IO 作業。</span><span class="sxs-lookup"><span data-stu-id="6c124-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="6c124-791">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c124-791">Requirements</span></span>



| <span data-ttu-id="6c124-792">需求</span><span class="sxs-lookup"><span data-stu-id="6c124-792">Requirement</span></span> | <span data-ttu-id="6c124-793">值</span><span class="sxs-lookup"><span data-stu-id="6c124-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c124-794">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c124-794">Minimum supported client</span></span><br/> | <span data-ttu-id="6c124-795">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c124-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c124-796">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c124-796">Minimum supported server</span></span><br/> | <span data-ttu-id="6c124-797">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c124-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c124-798">標頭</span><span class="sxs-lookup"><span data-stu-id="6c124-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c124-799"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c124-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c124-800">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c124-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c124-801">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6c124-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





---
title: RPC 結構
description: 本節說明 Microsoft RPC 定義和使用的結構。
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- 遠端程序呼叫 RPC、參考、結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682883"
---
# <a name="rpc-structures"></a><span data-ttu-id="f89c1-104">RPC 結構</span><span class="sxs-lookup"><span data-stu-id="f89c1-104">RPC Structures</span></span>

<span data-ttu-id="f89c1-105">本節說明 Microsoft RPC 定義和使用的結構。</span><span class="sxs-lookup"><span data-stu-id="f89c1-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="f89c1-106">[**NDR \_ SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="f89c1-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="f89c1-107">**Guid**</span><span class="sxs-lookup"><span data-stu-id="f89c1-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="f89c1-108">**NDR \_ 使用者 \_ 封送處理 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f89c1-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="f89c1-109">**NDR \_ 使用者 \_ 封送處理 \_ 資訊 \_ 1-1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="f89c1-110">**RPC \_ 非同步 \_ 通知 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f89c1-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="f89c1-111">**RPC \_ 非同步 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f89c1-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="f89c1-112">**RPC 系結 \_ \_ 控制碼 \_ 選項 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="f89c1-113">**RPC 系結 \_ \_ 處理 \_ 安全性 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="f89c1-114">**RPC 系結 \_ \_ 控制碼 \_ 範本 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="f89c1-115">**RPC 系結 \_ \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="f89c1-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="f89c1-116">**RPC \_ C \_ OPT \_ COOKIE \_ 驗證 \_ 描述元**</span><span class="sxs-lookup"><span data-stu-id="f89c1-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="f89c1-117">**RPC \_ 呼叫 \_ 屬性 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="f89c1-118">**RPC \_ 呼叫 \_ 屬性 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="f89c1-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="f89c1-119">**RPC \_ 呼叫 \_ 本機 \_ 位址 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f89c1-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="f89c1-120">**RPC \_ 用戶端 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="f89c1-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="f89c1-121">**RPC \_ 分派 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="f89c1-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="f89c1-122">**RPC \_ EE \_ 資訊 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="f89c1-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="f89c1-123">**RPC \_ 端點 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="f89c1-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="f89c1-124">**RPC \_ 錯誤 \_ 列舉 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="f89c1-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="f89c1-125">**RPC \_ 延伸 \_ 錯誤 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f89c1-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="f89c1-126">**RPC \_ HTTP \_ 傳輸 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="f89c1-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="f89c1-127">**RPC \_ HTTP \_ 傳輸 \_ 認證 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="f89c1-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="f89c1-128">**RPC \_ HTTP \_ 傳輸 \_ 認證 \_ V3**</span><span class="sxs-lookup"><span data-stu-id="f89c1-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="f89c1-129">**RPC （ \_ 如果 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="f89c1-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="f89c1-130">**RPC （ \_ 如果 \_ 識別碼 \_ 向量）**</span><span class="sxs-lookup"><span data-stu-id="f89c1-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="f89c1-131">**RPC \_ 介面 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="f89c1-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="f89c1-132">**RPC \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="f89c1-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="f89c1-133">**RPC \_ PROTSEQ \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="f89c1-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="f89c1-134">**RPC \_ 安全性 \_ QOS**</span><span class="sxs-lookup"><span data-stu-id="f89c1-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="f89c1-135">**RPC \_ 安全性 \_ QOS \_ V2**</span><span class="sxs-lookup"><span data-stu-id="f89c1-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="f89c1-136">**RPC \_ 安全性 \_ QOS \_ V3**</span><span class="sxs-lookup"><span data-stu-id="f89c1-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="f89c1-137">**RPC \_ 安全性 \_ QOS \_ V4**</span><span class="sxs-lookup"><span data-stu-id="f89c1-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="f89c1-138">**RPC \_ 安全性 \_ QOS \_ V5**</span><span class="sxs-lookup"><span data-stu-id="f89c1-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="f89c1-139">**RPC \_ 統計資料 \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="f89c1-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="f89c1-140">**秒的 \_ WINNT \_ 驗證身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f89c1-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="f89c1-141">**Uuid**</span><span class="sxs-lookup"><span data-stu-id="f89c1-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="f89c1-142">**UUID \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="f89c1-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 
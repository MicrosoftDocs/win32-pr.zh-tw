---
title: " (Fwpmu 的篩選內容識別碼) "
description: 內建于 Windows 篩選平台之篩選內容的識別碼。
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968985"
---
# <a name="filter-context-identifiers"></a><span data-ttu-id="f5496-103">篩選內容識別碼</span><span class="sxs-lookup"><span data-stu-id="f5496-103">Filter Context Identifiers</span></span>

<span data-ttu-id="f5496-104">內建于 Windows 篩選平台的篩選內容識別碼定義如下。</span><span class="sxs-lookup"><span data-stu-id="f5496-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="f5496-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ PASSTHRU、FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性、FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="f5496-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-106">輸入層中的 IPsec 傳輸篩選內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5496-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索，FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 隱藏的 \_ 協商**</span><span class="sxs-lookup"><span data-stu-id="f5496-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-108">輸出層中的 IPsec 傳輸篩選內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="f5496-109">若為 Windows 7，請使用 **FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 隱藏的 \_ 協商**。</span><span class="sxs-lookup"><span data-stu-id="f5496-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5496-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 安全性，FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 延遲 \_ SD \_ 評估**</span><span class="sxs-lookup"><span data-stu-id="f5496-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-111">用於 ALE 連接層的篩選內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5496-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 加密，FWPM \_ 內容 \_ ALE \_ 設定 \_ 連線 \_ 允許 \_ 第 \_ 一個 \_ 輸入 \_ 的 PKT 未加密，FWPM \_ 內容 \_ ALE \_ 允許 \_ 驗證 \_ FW**</span><span class="sxs-lookup"><span data-stu-id="f5496-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-113">用於 ALE 連接或接受層的篩選內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="f5496-114">若為 Windows 7，請使用 **FWPM \_ 內容 \_ ale \_ 設定連線 \_ \_ 允許 \_ 第一個 \_ 輸入的 \_ PKT \_ 未加密，** 或 **FWPM \_ 內容 \_ ale \_ 允許 \_ 驗證 \_ FW**。</span><span class="sxs-lookup"><span data-stu-id="f5496-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5496-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM \_ 內容 \_ TCP \_ 煙囪 \_ 卸載 \_ 啟用，FWPM \_ 內容 \_ TCP \_ 煙囪 \_ 卸載 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="f5496-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-116">TCP 煙囪卸載標注所使用的內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5496-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_已啟用 FWPM 內容 \_ RPC \_ AUDIT \_**</span><span class="sxs-lookup"><span data-stu-id="f5496-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5496-118">RPC audit 子層中使用的內容。</span><span class="sxs-lookup"><span data-stu-id="f5496-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5496-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5496-119">Requirements</span></span>



| <span data-ttu-id="f5496-120">需求</span><span class="sxs-lookup"><span data-stu-id="f5496-120">Requirement</span></span> | <span data-ttu-id="f5496-121">值</span><span class="sxs-lookup"><span data-stu-id="f5496-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5496-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5496-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5496-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5496-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5496-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5496-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5496-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5496-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5496-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f5496-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5496-127"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5496-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






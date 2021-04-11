---
title: '內建的標注識別碼 (Fwpmu .h) '
description: 內建于 Windows 篩選平台 (WFP) 的注標函式識別碼會以 GUID 表示。 這些識別碼的定義如下。
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935046"
---
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="16174-104">內建的標注識別碼</span><span class="sxs-lookup"><span data-stu-id="16174-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="16174-105">內建于 Windows 篩選平台 (WFP) 的注標函式識別碼會以 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="16174-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="16174-106">這些識別碼的定義如下。</span><span class="sxs-lookup"><span data-stu-id="16174-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="16174-107">注標識別碼結尾的 V4 和 V6 尾碼會指出標注是針對 IPv4 網路堆疊或 IPv6 網路堆疊。</span><span class="sxs-lookup"><span data-stu-id="16174-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="16174-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 傳輸 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 傳輸 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-109">確認每個接收到的封包都應安全地抵達傳輸模式安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="16174-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="16174-110">此標注適用于傳輸層。</span><span class="sxs-lookup"><span data-stu-id="16174-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 傳輸 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 傳輸 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-112">指出 IPsec 必須透過傳輸模式安全性關聯保護的輸出流量。</span><span class="sxs-lookup"><span data-stu-id="16174-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="16174-113">此標注適用于傳輸層。</span><span class="sxs-lookup"><span data-stu-id="16174-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-115">確認每個接收到的封包都會安全地抵達通道模式安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="16174-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="16174-116">此標注適用于傳輸層。</span><span class="sxs-lookup"><span data-stu-id="16174-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 通道 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-118">表示 IPsec 必須透過通道模式安全性關聯保護的輸出流量。</span><span class="sxs-lookup"><span data-stu-id="16174-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="16174-119">此標注適用于傳輸層。</span><span class="sxs-lookup"><span data-stu-id="16174-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸入 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸入 \_ 通道 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-121">確認每個接收到的封包都會安全地抵達通道模式安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="16174-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="16174-122">此標注適用于轉送層。</span><span class="sxs-lookup"><span data-stu-id="16174-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸出 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸出 \_ 通道 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-124">表示 IPsec 必須透過通道模式安全性關聯保護的輸出流量。</span><span class="sxs-lookup"><span data-stu-id="16174-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="16174-125">此標注適用于轉送層。</span><span class="sxs-lookup"><span data-stu-id="16174-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 起始 \_ 安全 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 起始 \_ 安全 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-127">確認每個應該送達安全的連入連線都安全地送達。</span><span class="sxs-lookup"><span data-stu-id="16174-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="16174-128">此標注適用于 ALE 接受層。</span><span class="sxs-lookup"><span data-stu-id="16174-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ ale \_ 接受 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ ale \_ 接受 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-130">允許 IPsec 通道模式的 IP 傳入 ip 封包在 ALE 接受層級進行分類。</span><span class="sxs-lookup"><span data-stu-id="16174-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ 標注 \_ ipsec \_ ale \_ connect \_ V4/FWPM \_ CALLOUT \_ ipsec \_ ale \_ connect \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-132">將 IPsec 原則修飾詞套用至用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="16174-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ 標注 \_ ipsec \_ DOSP \_ 轉寄 \_ V4/FWPM \_ CALLOUT \_ ipsec \_ DOSP \_ 轉寄 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-134">發出 IPsec DoS 保護的信號，指出需要驗證流量是否有潛在的 DoS，而且可能需要受到速率限制。</span><span class="sxs-lookup"><span data-stu-id="16174-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="16174-135">僅適用于 Windows 7 和 Windows Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="16174-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ 標注 \_ wfp \_ 傳輸 \_ 層 \_ V4 \_ 無訊息卸載 \_ /FWPM \_ 標注 \_ wfp \_ 傳輸 \_ 層 \_ V6 \_ 無 \_ 訊息卸載**</span><span class="sxs-lookup"><span data-stu-id="16174-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-137">以無訊息方式卸載所有 TCP 沒有接聽端點的傳入封包，以執行隱形模式篩選。</span><span class="sxs-lookup"><span data-stu-id="16174-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="16174-138">此標注適用于輸入傳輸捨棄層。</span><span class="sxs-lookup"><span data-stu-id="16174-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ 標注 \_ tcp \_ 煙囪 \_ 連接 \_ 層 \_ V4/FWPM \_ 注 \_ tcp \_ 煙囪 \_ 連接 \_ 層 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-140">啟用或停用每個連出連線的 TCP 煙囪卸載。</span><span class="sxs-lookup"><span data-stu-id="16174-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ 標注 \_ tcp \_ 煙囪 \_ 接受 \_ 層 \_ V4/FWPM \_ 注 \_ tcp \_ 煙囪 \_ 接受 \_ 層 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-142">針對每個連入連線啟用或停用 TCP 煙囪卸載。</span><span class="sxs-lookup"><span data-stu-id="16174-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ 標注 \_ set \_ options \_ auth \_ connect \_ layer \_ V4/FWPM \_ CALLOUT \_ set \_ options \_ auth \_ connect \_ layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-144">設定輸出流程的分類選項。</span><span class="sxs-lookup"><span data-stu-id="16174-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM 注標 \_ \_ 設定 \_ 選項 \_ 驗證 \_ 接收 \_ 接受 \_ 層 \_ V4/FWPM 注標 \_ \_ set \_ 選項 \_ 驗證 \_ 接收 \_ 接受 \_ 層 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-146">設定輸入流程的分類選項。</span><span class="sxs-lookup"><span data-stu-id="16174-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="16174-147">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="16174-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM 注標 \_ \_ 保留 \_ auth \_ CONNECT \_ layer \_ V4/FWPM \_ CALLOUT \_ reserved \_ auth \_ connect \_ layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-149">此識別碼已保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="16174-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ v6/FWPM \_ 注 \_ TEREDO \_ ale \_ 接聽 \_ v6**</span><span class="sxs-lookup"><span data-stu-id="16174-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-151">向 Teredo 服務發出通知，表示應用程式需要 Teredo 位址。</span><span class="sxs-lookup"><span data-stu-id="16174-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="16174-152">若為 Windows 7 和更新版本，請使用 **FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ V6**。</span><span class="sxs-lookup"><span data-stu-id="16174-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ale \_ 資源 \_ 指派 \_ v6/FWPM \_ 標注 \_ TEREDO \_ ale \_ 資源 \_ 指派 \_ v6**</span><span class="sxs-lookup"><span data-stu-id="16174-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-154">向 Teredo 服務發出通知，表示應用程式需要 Teredo 位址。</span><span class="sxs-lookup"><span data-stu-id="16174-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="16174-155">若為 Windows 7 和更新版本，請使用 **FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 資源 \_ 指派 \_ V6**。</span><span class="sxs-lookup"><span data-stu-id="16174-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 資源 \_ 指派 \_ V4**</span><span class="sxs-lookup"><span data-stu-id="16174-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-157">此識別碼保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="16174-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ V4**</span><span class="sxs-lookup"><span data-stu-id="16174-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-159">此識別碼保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="16174-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM 注標 \_ \_ tcp \_ 範本 \_ 連接 \_ 層 \_ V4/FWPM 注標 \_ \_ tcp \_ 範本 \_ 連接 \_ 層 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-161">針對相符的傳出連接套用 TCP 範本設定。</span><span class="sxs-lookup"><span data-stu-id="16174-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="16174-162">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="16174-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="16174-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM 注標 \_ \_ tcp \_ 範本 \_ 接受 \_ 層 \_ V4/FWPM 注標 \_ \_ tcp \_ 範本 \_ 接受 \_ 圖層 \_ V6**</span><span class="sxs-lookup"><span data-stu-id="16174-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="16174-164">套用 TCP 範本設定以進行相符的連入連線。</span><span class="sxs-lookup"><span data-stu-id="16174-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="16174-165">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="16174-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16174-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="16174-166">Requirements</span></span>



| <span data-ttu-id="16174-167">需求</span><span class="sxs-lookup"><span data-stu-id="16174-167">Requirement</span></span> | <span data-ttu-id="16174-168">值</span><span class="sxs-lookup"><span data-stu-id="16174-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16174-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16174-169">Minimum supported client</span></span><br/> | <span data-ttu-id="16174-170">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16174-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16174-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16174-171">Minimum supported server</span></span><br/> | <span data-ttu-id="16174-172">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16174-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16174-173">標頭</span><span class="sxs-lookup"><span data-stu-id="16174-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="16174-174"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="16174-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






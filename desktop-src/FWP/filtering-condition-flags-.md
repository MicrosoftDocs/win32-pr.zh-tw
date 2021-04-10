---
title: '篩選準則旗標 (Fwptypes .h) '
description: Windows 篩選平台 (WFP) 篩選準則旗標都是以位位表示。
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686320"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="b8dee-103">篩選準則旗標</span><span class="sxs-lookup"><span data-stu-id="b8dee-103">Filtering Condition Flags</span></span>

<span data-ttu-id="b8dee-104">Windows 篩選平台 (WFP) 篩選準則旗標都是以位位表示。</span><span class="sxs-lookup"><span data-stu-id="b8dee-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="b8dee-105">您可以使用這些旗標和篩選層來定義它們，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8dee-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="b8dee-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="b8dee-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-107">測試網路流量是否為回送流量。</span><span class="sxs-lookup"><span data-stu-id="b8dee-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="b8dee-108">篩選圖層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-108">Filtering layers:</span></span>

-   <span data-ttu-id="b8dee-109">FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-110">FWPM \_ 圖層 \_ 輸出 \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-111">FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-112">FWPM \_ 圖層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-113">FWPM \_ 圖層 \_ 資料流程 \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-114">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-115">FWPM \_ 圖層 \_ 輸入 \_ ICMP \_ 錯誤 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-116">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-117">FWPM \_ 圖層 \_ 輸出 \_ ICMP \_ 錯誤 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-118">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-119">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-120">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-121">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-122">FWPM \_ 圖層 \_ ALE \_ 流程已 \_ 建立 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-123">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ IPSEC \_ 安全**</span><span class="sxs-lookup"><span data-stu-id="b8dee-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-125">測試網路流量是否由 IPsec 保護。</span><span class="sxs-lookup"><span data-stu-id="b8dee-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="b8dee-126">篩選圖層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-126">Filtering layers:</span></span>

-   <span data-ttu-id="b8dee-127">FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-128">FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-129">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-130">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**\_ \_ \_ 已重新授權的 .FWP 條件旗標 \_**</span><span class="sxs-lookup"><span data-stu-id="b8dee-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-132">原則變更的測試，而不是新的連接。</span><span class="sxs-lookup"><span data-stu-id="b8dee-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="b8dee-133">篩選圖層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-133">Filtering layers:</span></span>

-   <span data-ttu-id="b8dee-134">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-135">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 萬用字元 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="b8dee-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-137">測試應用程式是否在系結至區域網路位址時指定萬用字元位址。</span><span class="sxs-lookup"><span data-stu-id="b8dee-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="b8dee-138">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-138">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-139">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 原始 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="b8dee-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-141">測試傳送和接收流量的本機端點是否為原始端點。</span><span class="sxs-lookup"><span data-stu-id="b8dee-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="b8dee-142">篩選圖層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-142">Filtering layers:</span></span>

-   <span data-ttu-id="b8dee-143">FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-144">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-145">FWPM \_ 圖層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-146">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-147">FWPM \_ 圖 \_ 層 \_ 資料包資料 \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="b8dee-148">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="b8dee-149">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-150">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-151">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 片段**</span><span class="sxs-lookup"><span data-stu-id="b8dee-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-153">測試 \_ \_ 傳遞給 callout 驅動程式的淨緩衝區清單結構是否為 IP 封包片段。</span><span class="sxs-lookup"><span data-stu-id="b8dee-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="b8dee-154">篩選圖層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-154">Filtering layers:</span></span>

-   <span data-ttu-id="b8dee-155">FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-156">FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6} \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="b8dee-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 片段 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="b8dee-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-158">測試 \_ \_ 傳遞給 callout 驅動程式的淨緩衝區清單結構是否描述封包片段的連結清單。</span><span class="sxs-lookup"><span data-stu-id="b8dee-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="b8dee-159">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-159">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-160">FWPM \_ LAYER \_ IPFORWARD \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ IPSEC NATT 重新 \_ \_ 分類**</span><span class="sxs-lookup"><span data-stu-id="b8dee-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-162">指出當 IPsec NAT 填充碼轉譯遠端埠值時，會將相同的封包重新分類至傳輸層。</span><span class="sxs-lookup"><span data-stu-id="b8dee-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**.FWP \_ 條件 \_ 旗標 \_ 需要 \_ ALE \_ 分類**</span><span class="sxs-lookup"><span data-stu-id="b8dee-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-164">指出將在 ALE 接收/接受層重新分類封包。</span><span class="sxs-lookup"><span data-stu-id="b8dee-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 隱含 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="b8dee-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-166">測試 Windows 通訊端是否正在執行隱含系結。</span><span class="sxs-lookup"><span data-stu-id="b8dee-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="b8dee-167">僅適用于 Windows Vista 和 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="b8dee-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**\_已重新 \_ \_ 組合的 \_ .FWP 條件旗標**</span><span class="sxs-lookup"><span data-stu-id="b8dee-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-169">測試封包是否已重組。</span><span class="sxs-lookup"><span data-stu-id="b8dee-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-170">僅適用于 Windows Server 2008、Windows Vista （含 SP1）及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="b8dee-171">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-171">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-172">FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**\_ \_ \_ 已 \_ \_ 指定名稱應用程式的 \_ .FWP 條件旗標**</span><span class="sxs-lookup"><span data-stu-id="b8dee-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-174">測試是否已透過 API （例如 [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) ）接收應用程式所要連接之對等電腦的名稱，而不是透過快取啟發學習法取得。</span><span class="sxs-lookup"><span data-stu-id="b8dee-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-175">僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="b8dee-176">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-176">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-177">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ 混合的**</span><span class="sxs-lookup"><span data-stu-id="b8dee-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-179">保留的。</span><span class="sxs-lookup"><span data-stu-id="b8dee-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 驗證 \_ FW**</span><span class="sxs-lookup"><span data-stu-id="b8dee-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-181">測試連接是否經過端對端驗證，即使個別的封包尚未經過驗證也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b8dee-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-182">僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="b8dee-183">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-183">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-184">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-185">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**\_已重新 \_ \_ 分類的 \_ .FWP 條件旗標**</span><span class="sxs-lookup"><span data-stu-id="b8dee-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-187">測試篩選引擎是否將先前的系結或接聽要求。</span><span class="sxs-lookup"><span data-stu-id="b8dee-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-188">僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="b8dee-189">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-189">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-190">FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-191">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ PROXY \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="b8dee-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-193">測試連接是否使用 proxy。</span><span class="sxs-lookup"><span data-stu-id="b8dee-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-194">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="b8dee-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 是 \_ APPCONTAINER \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="b8dee-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-196">測試網路流量是否為應用程式容器回送流量。</span><span class="sxs-lookup"><span data-stu-id="b8dee-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-197">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="b8dee-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**.FWP \_ 條件 \_ 旗標 \_ 為 \_ 非 \_ APPCONTAINER \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="b8dee-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-199">測試網路流量是否為非應用程式容器回送流量。</span><span class="sxs-lookup"><span data-stu-id="b8dee-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-200">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="b8dee-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**\_ \_ \_ 已保留 .FWP 條件旗標 \_**</span><span class="sxs-lookup"><span data-stu-id="b8dee-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-202">保留的。</span><span class="sxs-lookup"><span data-stu-id="b8dee-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**.FWP \_ 條件 \_ 旗標 \_ 正在接受 \_ \_ 原則 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="b8dee-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-204">指出正在執行目前的分類，以接受重新導向的 Windows Store 應用程式連接至指定主機的意圖。</span><span class="sxs-lookup"><span data-stu-id="b8dee-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="b8dee-205">這類分類將包含的資料欄值與應用程式永遠不會重新導向的相同。</span><span class="sxs-lookup"><span data-stu-id="b8dee-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="b8dee-206">此旗標也會指出將會叫用未來的分類，以符合有效的重新導向目的地。</span><span class="sxs-lookup"><span data-stu-id="b8dee-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="b8dee-207">如果將應用程式重新導向至 proxy 服務進行檢查，也表示將在 proxy 連線上叫用未來的分類。</span><span class="sxs-lookup"><span data-stu-id="b8dee-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="b8dee-208">注標驅動程式通常應該允許此分類。</span><span class="sxs-lookup"><span data-stu-id="b8dee-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-209">僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="b8dee-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="b8dee-210">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-210">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-211">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="b8dee-212">下列旗標指定之先前授權連接的原因。</span><span class="sxs-lookup"><span data-stu-id="b8dee-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="b8dee-213">您可以使用這些旗標和篩選層來定義它們，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8dee-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-214">這些篩選準則僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="b8dee-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 原則 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="b8dee-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-216">指出因為加入或移除篩選而重新授權連接。</span><span class="sxs-lookup"><span data-stu-id="b8dee-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="b8dee-217">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-217">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-218">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-219">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 新 \_ 抵達 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="b8dee-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-221">指出封包已從未知的介面抵達。</span><span class="sxs-lookup"><span data-stu-id="b8dee-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="b8dee-222">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-222">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-223">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-224">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**.FWP \_ 條件 \_ 重新授權 \_ 原因 \_ 新的 \_ NEXTHOP \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="b8dee-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-226">指出封包將從未知的介面中脫離。</span><span class="sxs-lookup"><span data-stu-id="b8dee-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="b8dee-227">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-227">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-228">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-229">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**已 \_ \_ \_ 交叉分析的重新授權原因 \_ 設定檔 \_**</span><span class="sxs-lookup"><span data-stu-id="b8dee-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-231">指出封包已通過一個以上網路類別的介面。</span><span class="sxs-lookup"><span data-stu-id="b8dee-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="b8dee-232">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-232">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-233">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-234">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**已 \_ \_ \_ \_ \_ 完成分類完成的 .FWP 條件重新授權原因**</span><span class="sxs-lookup"><span data-stu-id="b8dee-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-236">表示現在已允許先前保留的連接完成。</span><span class="sxs-lookup"><span data-stu-id="b8dee-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="b8dee-237">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-237">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-238">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-239">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_ \_ \_ \_ \_ 已變更 IPSEC 屬性的重新授權 \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="b8dee-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-241">指出 IPsec 屬性已變更，或連接已從純文字變更為安全連線。</span><span class="sxs-lookup"><span data-stu-id="b8dee-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="b8dee-242">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-242">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-243">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-244">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**\_重新授權進行 \_ \_ \_ \_ 資料流程 \_ 檢查的 .FWP 條件**</span><span class="sxs-lookup"><span data-stu-id="b8dee-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-246">指出先前建立的 TCP 連接現在正在檢查。</span><span class="sxs-lookup"><span data-stu-id="b8dee-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="b8dee-247">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-247">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-248">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-249">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_已變更的 .FWP 條件 \_ 重新授權 \_ 原因 \_ 通訊端 \_ 屬性 \_**</span><span class="sxs-lookup"><span data-stu-id="b8dee-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-251">指出在授權並建立連接之後，已設定通訊端屬性。</span><span class="sxs-lookup"><span data-stu-id="b8dee-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="b8dee-252">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-252">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-253">FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-254">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_ \_ 重新授權新的 \_ \_ \_ 輸入 \_ MCAST BCAST 封 \_ \_ 包的 .FWP 條件**</span><span class="sxs-lookup"><span data-stu-id="b8dee-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-256">指出新的輸入多播或廣播封包正在重新授權于 ALE \_ 接收 \_ 接受標注。</span><span class="sxs-lookup"><span data-stu-id="b8dee-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="b8dee-257">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-257">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-258">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="b8dee-259">下列旗標會指定與應用程式是否要接收 Edge 遍歷流量相關的通訊端屬性。</span><span class="sxs-lookup"><span data-stu-id="b8dee-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="b8dee-260">您可以使用這些旗標和篩選層來定義它們，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8dee-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-261">這些篩選準則僅適用于 Windows Server 2008 R2、Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8dee-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="b8dee-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 是 \_ 系統 \_ 埠 \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="b8dee-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-263">指出應用程式正在與動態 RPC 埠通訊。</span><span class="sxs-lookup"><span data-stu-id="b8dee-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="b8dee-264">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-264">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-265">FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-266">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 允許 \_ 邊緣 \_ 流量**</span><span class="sxs-lookup"><span data-stu-id="b8dee-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-268">表示應用程式想要接收 edge 遍歷特定的流量。</span><span class="sxs-lookup"><span data-stu-id="b8dee-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="b8dee-269">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-269">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-270">FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-271">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**.FWP \_ 條件 \_ 通訊端 \_ 屬性 \_ 旗標 \_ 拒絕 \_ 邊緣 \_ 流量**</span><span class="sxs-lookup"><span data-stu-id="b8dee-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-273">表示應用程式不想接收或處理 edge 遍歷特定的流量。</span><span class="sxs-lookup"><span data-stu-id="b8dee-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="b8dee-274">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-274">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-275">FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="b8dee-276">FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="b8dee-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="b8dee-277">下列旗標指定與 L2 篩選相關的連接詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8dee-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="b8dee-278">這些篩選準則僅適用于 Windows 8 和 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="b8dee-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="b8dee-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ 原生 \_ 乙太網路**</span><span class="sxs-lookup"><span data-stu-id="b8dee-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-280">指出連接是原生乙太網路。</span><span class="sxs-lookup"><span data-stu-id="b8dee-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="b8dee-281">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-281">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-282">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-283">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-284">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-285">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI**</span><span class="sxs-lookup"><span data-stu-id="b8dee-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-287">指出連接是 Wi-fi。</span><span class="sxs-lookup"><span data-stu-id="b8dee-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="b8dee-288">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-288">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-289">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-290">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-291">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-292">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ MOBILE \_ 寬頻**</span><span class="sxs-lookup"><span data-stu-id="b8dee-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-294">指出連接是 mobile 寬頻。</span><span class="sxs-lookup"><span data-stu-id="b8dee-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="b8dee-295">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-295">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-296">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-297">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-298">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-299">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI \_ DIRECT \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="b8dee-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-301">表示連接 Wi-Fi 直接。</span><span class="sxs-lookup"><span data-stu-id="b8dee-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="b8dee-302">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-302">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-303">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-304">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-305">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-306">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_ \_ \_ 已 VM2VM 的 .fwp 條件 L2 \_**</span><span class="sxs-lookup"><span data-stu-id="b8dee-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-308">指出連接是在虛擬機器之間。</span><span class="sxs-lookup"><span data-stu-id="b8dee-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="b8dee-309">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-309">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-310">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-311">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-312">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-313">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ 格式不正確的封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="b8dee-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-315">指出封包看似格式不正確。</span><span class="sxs-lookup"><span data-stu-id="b8dee-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="b8dee-316">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-316">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-317">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-318">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-319">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-320">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**.FWP \_ 條件 \_ L2 \_ 是 \_ IP \_ 片段 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="b8dee-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-322">表示 IP 封包片段群組。</span><span class="sxs-lookup"><span data-stu-id="b8dee-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="b8dee-323">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-323">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-324">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-325">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-326">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-327">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8dee-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_ \_ \_ 當 \_ 連接器 \_ 存在時的 .fwp 條件 L2**</span><span class="sxs-lookup"><span data-stu-id="b8dee-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8dee-329">表示連接器存在。</span><span class="sxs-lookup"><span data-stu-id="b8dee-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="b8dee-330">篩選層：</span><span class="sxs-lookup"><span data-stu-id="b8dee-330">Filtering layer:</span></span>

-   <span data-ttu-id="b8dee-331">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-332">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="b8dee-333">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="b8dee-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="b8dee-334">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="b8dee-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8dee-335">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8dee-335">Requirements</span></span>



| <span data-ttu-id="b8dee-336">需求</span><span class="sxs-lookup"><span data-stu-id="b8dee-336">Requirement</span></span> | <span data-ttu-id="b8dee-337">值</span><span class="sxs-lookup"><span data-stu-id="b8dee-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dee-338">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8dee-338">Minimum supported client</span></span><br/> | <span data-ttu-id="b8dee-339">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8dee-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8dee-340">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8dee-340">Minimum supported server</span></span><br/> | <span data-ttu-id="b8dee-341">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8dee-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8dee-342">標頭</span><span class="sxs-lookup"><span data-stu-id="b8dee-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8dee-343"><dt>Fwptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8dee-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8dee-344">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8dee-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dee-345">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="b8dee-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 


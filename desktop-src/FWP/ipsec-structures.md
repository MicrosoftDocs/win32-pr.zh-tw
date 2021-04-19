---
title: IPsec 結構
description: IPsec 結構
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd268fda1ee98ec80d20d8c75625d4f68526c741
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "106967247"
---
# <a name="ipsec-structures"></a><span data-ttu-id="ddb46-103">IPsec 結構</span><span class="sxs-lookup"><span data-stu-id="ddb46-103">IPsec Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ddb46-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="ddb46-104">In this section</span></span>

-   [<span data-ttu-id="ddb46-105">**IPSEC \_ 位址 \_ INFO0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-105">**IPSEC\_ADDRESS\_INFO0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [<span data-ttu-id="ddb46-106">**IPSEC \_ 匯總 \_ 捨棄封 \_ 包 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-106">**IPSEC\_AGGREGATE\_DROP\_PACKET\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [<span data-ttu-id="ddb46-107">**IPSEC \_ 匯總 \_ 捨棄封 \_ 包 \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-107">**IPSEC\_AGGREGATE\_DROP\_PACKET\_STATISTICS1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [<span data-ttu-id="ddb46-108">**IPSEC \_ 匯總 \_ SA \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-108">**IPSEC\_AGGREGATE\_SA\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [<span data-ttu-id="ddb46-109">**IPSEC \_ AH \_ 捨棄封 \_ 包 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-109">**IPSEC\_AH\_DROP\_PACKET\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [<span data-ttu-id="ddb46-110">**IPSEC \_ 驗證 \_ 和 \_ 加密 \_ TRANSFORM0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-110">**IPSEC\_AUTH\_AND\_CIPHER\_TRANSFORM0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [<span data-ttu-id="ddb46-111">**IPSEC \_ 驗證 \_ TRANSFORM0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-111">**IPSEC\_AUTH\_TRANSFORM0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [<span data-ttu-id="ddb46-112">**IPSEC \_ 驗證 \_ 轉換 \_ ID0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-112">**IPSEC\_AUTH\_TRANSFORM\_ID0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [<span data-ttu-id="ddb46-113">**IPSEC \_ 加密 \_ TRANSFORM0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-113">**IPSEC\_CIPHER\_TRANSFORM0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [<span data-ttu-id="ddb46-114">**IPSEC \_ 密碼 \_ 轉換 \_ ID0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-114">**IPSEC\_CIPHER\_TRANSFORM\_ID0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [<span data-ttu-id="ddb46-115">**IPSEC \_ DOSP \_ OPTIONS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-115">**IPSEC\_DOSP\_OPTIONS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [<span data-ttu-id="ddb46-116">**IPSEC \_ DOSP \_ STATE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-116">**IPSEC\_DOSP\_STATE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [<span data-ttu-id="ddb46-117">**IPSEC \_ DOSP \_ 狀態 \_ 列舉 \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-117">**IPSEC\_DOSP\_STATE\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [<span data-ttu-id="ddb46-118">**IPSEC \_ DOSP \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-118">**IPSEC\_DOSP\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [<span data-ttu-id="ddb46-119">**IPSEC \_ ESP \_ 捨棄封 \_ 包 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-119">**IPSEC\_ESP\_DROP\_PACKET\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [<span data-ttu-id="ddb46-120">**IPSEC \_ GETSPI0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-120">**IPSEC\_GETSPI0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [<span data-ttu-id="ddb46-121">**IPSEC \_ GETSPI1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-121">**IPSEC\_GETSPI1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [<span data-ttu-id="ddb46-122">**IPSEC \_ ID0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-122">**IPSEC\_ID0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [<span data-ttu-id="ddb46-123">**IPSEC \_ 金鑰 \_ MANAGER0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-123">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="ddb46-124">**IPSEC \_ 金鑰 \_ 管理員 \_ CALLBACKS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-124">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="ddb46-125">**IPSEC \_ 金鑰 \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-125">**IPSEC\_KEYING\_POLICY0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [<span data-ttu-id="ddb46-126">**IPSEC \_ 金鑰 \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-126">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="ddb46-127">**IPSEC \_ KEYMODULE \_ STATE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-127">**IPSEC\_KEYMODULE\_STATE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [<span data-ttu-id="ddb46-128">**IPSEC \_ PROPOSAL0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-128">**IPSEC\_PROPOSAL0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [<span data-ttu-id="ddb46-129">**IPSEC \_ SA0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-129">**IPSEC\_SA0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [<span data-ttu-id="ddb46-130">**IPSEC \_ SA \_ 驗證 \_ 和 \_ 加密 \_ INFORMATION0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-130">**IPSEC\_SA\_AUTH\_AND\_CIPHER\_INFORMATION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [<span data-ttu-id="ddb46-131">**IPSEC \_ SA \_ 驗證 \_ INFORMATION0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-131">**IPSEC\_SA\_AUTH\_INFORMATION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [<span data-ttu-id="ddb46-132">**IPSEC \_ SA \_ BUNDLE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-132">**IPSEC\_SA\_BUNDLE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [<span data-ttu-id="ddb46-133">**IPSEC \_ SA \_ BUNDLE1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-133">**IPSEC\_SA\_BUNDLE1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [<span data-ttu-id="ddb46-134">**IPSEC \_ SA \_ 加密 \_ INFORMATION0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-134">**IPSEC\_SA\_CIPHER\_INFORMATION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [<span data-ttu-id="ddb46-135">**IPSEC \_ SA \_ CONTEXT0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-135">**IPSEC\_SA\_CONTEXT0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [<span data-ttu-id="ddb46-136">**IPSEC \_ SA \_ CONTEXT1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-136">**IPSEC\_SA\_CONTEXT1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [<span data-ttu-id="ddb46-137">**IPSEC \_ SA \_ 內容 \_ CHANGE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-137">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="ddb46-138">**IPSEC \_ SA \_ 內容 \_ 列舉 \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-138">**IPSEC\_SA\_CONTEXT\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [<span data-ttu-id="ddb46-139">**IPSEC \_ SA \_ 內容 \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-139">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="ddb46-140">**IPSEC \_ SA \_ DETAILS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-140">**IPSEC\_SA\_DETAILS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [<span data-ttu-id="ddb46-141">**IPSEC \_ SA \_ DETAILS1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-141">**IPSEC\_SA\_DETAILS1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [<span data-ttu-id="ddb46-142">**IPSEC \_ SA \_ 列舉 \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-142">**IPSEC\_SA\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [<span data-ttu-id="ddb46-143">**IPSEC \_ SA \_ 閒置 \_ TIMEOUT0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-143">**IPSEC\_SA\_IDLE\_TIMEOUT0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [<span data-ttu-id="ddb46-144">**IPSEC \_ SA \_ LIFETIME0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-144">**IPSEC\_SA\_LIFETIME0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [<span data-ttu-id="ddb46-145">**IPSEC \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-145">**IPSEC\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [<span data-ttu-id="ddb46-146">**IPSEC \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-146">**IPSEC\_STATISTICS1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [<span data-ttu-id="ddb46-147">**IPSEC \_ SA \_ TRANSFORM0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-147">**IPSEC\_SA\_TRANSFORM0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [<span data-ttu-id="ddb46-148">**IPSEC \_ TOKEN0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-148">**IPSEC\_TOKEN0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [<span data-ttu-id="ddb46-149">**IPSEC \_ TRAFFIC0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-149">**IPSEC\_TRAFFIC0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [<span data-ttu-id="ddb46-150">**IPSEC \_ 流量1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-150">**IPSEC\_TRAFFIC1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [<span data-ttu-id="ddb46-151">**IPSEC \_ 流量 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-151">**IPSEC\_TRAFFIC\_STATISTICS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [<span data-ttu-id="ddb46-152">**IPSEC \_ 流量 \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-152">**IPSEC\_TRAFFIC\_STATISTICS1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [<span data-ttu-id="ddb46-153">**IPSEC \_ 傳輸 \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-153">**IPSEC\_TRANSPORT\_POLICY0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [<span data-ttu-id="ddb46-154">**IPSEC \_ 傳輸 \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-154">**IPSEC\_TRANSPORT\_POLICY1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [<span data-ttu-id="ddb46-155">**IPSEC \_ 傳輸 \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="ddb46-155">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="ddb46-156">**IPSEC \_ 通道 \_ ENDPOINT0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-156">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="ddb46-157">**IPSEC \_ 通道 \_ ENDPOINTS0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-157">**IPSEC\_TUNNEL\_ENDPOINTS0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [<span data-ttu-id="ddb46-158">**IPSEC \_ 通道 \_ ENDPOINTS1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-158">**IPSEC\_TUNNEL\_ENDPOINTS1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [<span data-ttu-id="ddb46-159">**IPSEC \_ 通道 \_ ENDPOINTS2**</span><span class="sxs-lookup"><span data-stu-id="ddb46-159">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="ddb46-160">**IPSEC \_ 通道 \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-160">**IPSEC\_TUNNEL\_POLICY0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [<span data-ttu-id="ddb46-161">**IPSEC \_ 通道 \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="ddb46-161">**IPSEC\_TUNNEL\_POLICY1**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [<span data-ttu-id="ddb46-162">**IPSEC \_ 通道 \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="ddb46-162">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="ddb46-163">**IPSEC \_ V4 \_ UDP \_ ENCAPSULATION0**</span><span class="sxs-lookup"><span data-stu-id="ddb46-163">**IPSEC\_V4\_UDP\_ENCAPSULATION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [<span data-ttu-id="ddb46-164">**IPSEC \_ 虛擬（ \_ 如果通道 \_ \_ INFO0）**</span><span class="sxs-lookup"><span data-stu-id="ddb46-164">**IPSEC\_VIRTUAL\_IF\_TUNNEL\_INFO0**</span></span>](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 





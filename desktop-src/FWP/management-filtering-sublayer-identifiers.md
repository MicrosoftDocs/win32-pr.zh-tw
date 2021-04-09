---
title: '篩選子層識別碼 (Fwpmu .h) '
description: WFP API 管理篩選子層識別碼常數。
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844072"
---
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="b14e2-103">篩選子層識別碼</span><span class="sxs-lookup"><span data-stu-id="b14e2-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="b14e2-104">Windows 篩選平台 (WFP) 子層識別碼都是由 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="b14e2-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="b14e2-105">這些識別碼的定義如下。</span><span class="sxs-lookup"><span data-stu-id="b14e2-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="b14e2-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM \_ 子層 \_ EDGE \_ 遍歷/FWPM \_ 子層 \_ TEREDO**</span><span class="sxs-lookup"><span data-stu-id="b14e2-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-107">Edge 遍歷篩選會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="b14e2-108">針對 Windows 7 和更新版本，請使用 **FWPM \_ 子層 \_ EDGE \_ 遍歷**。</span><span class="sxs-lookup"><span data-stu-id="b14e2-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM \_ 子層 \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="b14e2-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-110">這是最低的加權子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="b14e2-111">它僅用於檢查篩選。</span><span class="sxs-lookup"><span data-stu-id="b14e2-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM \_ 子層 \_ IPSEC \_ DOSP**</span><span class="sxs-lookup"><span data-stu-id="b14e2-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-113">IPsec DoS 保護篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="b14e2-114">僅適用于 Windows Vista （含 SP1）、Windows Server 2008 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b14e2-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM \_ 子層 \_ IPSEC \_ 轉送 \_ 輸出 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="b14e2-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-116">IPsec 轉送輸出通道篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="b14e2-117">僅適用于 Windows 7、Windows Server 2008 R2 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b14e2-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM \_ 子層 \_ IPSEC \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="b14e2-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-119">IPsec 通道篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM \_ 子層 \_ LIP**</span><span class="sxs-lookup"><span data-stu-id="b14e2-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-121">舊版 IPsec 篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM \_ 子層 \_ RPC \_ AUDIT**</span><span class="sxs-lookup"><span data-stu-id="b14e2-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-123">RPC audit 篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="b14e2-124">這些篩選準則會以 C2 和通用準則合規性的一部分來審核 RPC 撥入電話。</span><span class="sxs-lookup"><span data-stu-id="b14e2-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM \_ 子層 \_ 安全 \_ 通訊端**</span><span class="sxs-lookup"><span data-stu-id="b14e2-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-126">安全通訊端篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM \_ 子層 \_ TCP \_ 煙囪 \_ 卸載**</span><span class="sxs-lookup"><span data-stu-id="b14e2-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-128">TCP 煙囪卸載篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM \_ 子層 \_ TCP \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="b14e2-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-130">TCP 範本篩選器會新增至此子層。</span><span class="sxs-lookup"><span data-stu-id="b14e2-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="b14e2-131">僅適用于 Windows 8、Windows Server 2012 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b14e2-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b14e2-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ 子層 \_ 通用**</span><span class="sxs-lookup"><span data-stu-id="b14e2-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b14e2-133">此子層裝載所有未指派給任何其他子層的篩選器。</span><span class="sxs-lookup"><span data-stu-id="b14e2-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b14e2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="b14e2-134">Requirements</span></span>



| <span data-ttu-id="b14e2-135">需求</span><span class="sxs-lookup"><span data-stu-id="b14e2-135">Requirement</span></span> | <span data-ttu-id="b14e2-136">值</span><span class="sxs-lookup"><span data-stu-id="b14e2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b14e2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b14e2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b14e2-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b14e2-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b14e2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b14e2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b14e2-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b14e2-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b14e2-141">標頭</span><span class="sxs-lookup"><span data-stu-id="b14e2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14e2-142"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="b14e2-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






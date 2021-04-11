---
title: 'Snmp 應用程式語法值 (Snmp. h) '
description: 使用 Microsoft SNMP 管理 API 的管理應用程式會使用 SNMP 應用程式語法值。
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094372"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="7efa2-103">SNMP 應用程式語法值</span><span class="sxs-lookup"><span data-stu-id="7efa2-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="7efa2-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7efa2-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7efa2-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="7efa2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7efa2-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="7efa2-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7efa2-107">使用 Microsoft SNMP 管理 API 的管理應用程式會使用 SNMP 應用程式語法值。</span><span class="sxs-lookup"><span data-stu-id="7efa2-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="7efa2-108">常數</span><span class="sxs-lookup"><span data-stu-id="7efa2-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="7efa2-109">描述</span><span class="sxs-lookup"><span data-stu-id="7efa2-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="7efa2-110"><dt>**ASN \_ IPADDRESS**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="7efa2-111">表示 IP 位址變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="7efa2-112"><dt>**ASN \_ COUNTER32**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="7efa2-113">指出計數器變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="7efa2-114"><dt>**ASN \_ GAUGE32**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="7efa2-115">表示量測計變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-115">Indicates a gauge variable.</span></span> <span data-ttu-id="7efa2-116">此變數描述項合 RFC 1902 的 Unsigned32 類型。</span><span class="sxs-lookup"><span data-stu-id="7efa2-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="7efa2-117"><dt>**ASN \_ TIMETICKS**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="7efa2-118">表示 timeticks 變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="7efa2-119"><dt>**ASN 不 \_ 透明**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="7efa2-120">表示不透明的變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="7efa2-121"><dt>**ASN \_ COUNTER64**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="7efa2-122">指出計數器變數，此變數會在到達 (2 ^ 64) -1 的最大值之前增加。</span><span class="sxs-lookup"><span data-stu-id="7efa2-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="7efa2-123"><dt>**ASN \_ UINTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="7efa2-124">表示32位不帶正負號的整數變數。</span><span class="sxs-lookup"><span data-stu-id="7efa2-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="7efa2-125">此變數描述項合 RFC 1442 的 UInteger32 類型。</span><span class="sxs-lookup"><span data-stu-id="7efa2-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="7efa2-126"><dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="7efa2-127">請參閱 ASN \_ GAUGE32。</span><span class="sxs-lookup"><span data-stu-id="7efa2-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="7efa2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7efa2-128">Requirements</span></span>



| <span data-ttu-id="7efa2-129">需求</span><span class="sxs-lookup"><span data-stu-id="7efa2-129">Requirement</span></span> | <span data-ttu-id="7efa2-130">值</span><span class="sxs-lookup"><span data-stu-id="7efa2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7efa2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7efa2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7efa2-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7efa2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7efa2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7efa2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7efa2-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7efa2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7efa2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="7efa2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7efa2-136"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7efa2-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efa2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7efa2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efa2-138">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="7efa2-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="7efa2-139">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="7efa2-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="7efa2-140">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="7efa2-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 


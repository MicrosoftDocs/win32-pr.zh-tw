---
title: SNMP 結構
description: 下表列出與 SNMP 搭配使用的結構。
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP 結構 SNMP
- 結構 SNMP，SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382613"
---
# <a name="snmp-structures"></a><span data-ttu-id="0ffa1-105">SNMP 結構</span><span class="sxs-lookup"><span data-stu-id="0ffa1-105">SNMP Structures</span></span>

<span data-ttu-id="0ffa1-106">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0ffa1-107">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0ffa1-108">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="0ffa1-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="0ffa1-109">下表列出與 SNMP 搭配使用的結構。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="0ffa1-110">SNMP 結構</span><span class="sxs-lookup"><span data-stu-id="0ffa1-110">SNMP Structure</span></span>                                         | <span data-ttu-id="0ffa1-111">Description</span><span class="sxs-lookup"><span data-stu-id="0ffa1-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ffa1-112">**AsnAny**</span><span class="sxs-lookup"><span data-stu-id="0ffa1-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="0ffa1-113">描述指定之 SNMP 變數的類型和值。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="0ffa1-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0ffa1-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="0ffa1-115">包含64位的計數器，此計數器是由描述其低序位和高序位位的兩個值所指定。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="0ffa1-116">**AsnObjectIdentifier**</span><span class="sxs-lookup"><span data-stu-id="0ffa1-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="0ffa1-117">描述 (OID) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="0ffa1-118">**AsnOctetString**</span><span class="sxs-lookup"><span data-stu-id="0ffa1-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="0ffa1-119">代表八位元組的字串，通常是位元組值。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="0ffa1-120">**SnmpVarBind**</span><span class="sxs-lookup"><span data-stu-id="0ffa1-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="0ffa1-121">描述 SNMP 變數系結。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="0ffa1-122">**SnmpVarBindList**</span><span class="sxs-lookup"><span data-stu-id="0ffa1-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="0ffa1-123">包含 SNMP 變數系結的清單。</span><span class="sxs-lookup"><span data-stu-id="0ffa1-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 
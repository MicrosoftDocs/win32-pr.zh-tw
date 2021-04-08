---
title: SNMP 變數類型和要求 PDU 類型
description: 某些 SNMP 變數類型和要求 PDU 類型的定義已變更。 Snmp 檔會將舊類型對應至對應的新類型。
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682771"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="03931-104">SNMP 變數類型和要求 PDU 類型</span><span class="sxs-lookup"><span data-stu-id="03931-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="03931-105">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="03931-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03931-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="03931-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="03931-107">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="03931-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="03931-108">某些 SNMP 變數類型和要求 PDU 類型的定義已變更。</span><span class="sxs-lookup"><span data-stu-id="03931-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="03931-109">Snmp 檔會將舊類型對應至對應的新類型。</span><span class="sxs-lookup"><span data-stu-id="03931-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="03931-110">修改後的 SNMP 變數類型</span><span class="sxs-lookup"><span data-stu-id="03931-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="03931-111">當您開發使用 Microsoft SNMP 管理 API 的管理員應用程式時，您應該使用下表所列的新 SNMP 變數類型。</span><span class="sxs-lookup"><span data-stu-id="03931-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="03931-112">資料表會列出舊的 SNMP 變數類型與對應的新變數類型。</span><span class="sxs-lookup"><span data-stu-id="03931-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="03931-113">舊變數類型</span><span class="sxs-lookup"><span data-stu-id="03931-113">Old variable type</span></span>        | <span data-ttu-id="03931-114">新變數類型</span><span class="sxs-lookup"><span data-stu-id="03931-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="03931-115">ASN \_ RFC1155 \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="03931-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="03931-116">ASN \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="03931-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="03931-117">ASN \_ RFC1155 \_ 計數器</span><span class="sxs-lookup"><span data-stu-id="03931-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="03931-118">ASN \_ COUNTER32</span><span class="sxs-lookup"><span data-stu-id="03931-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="03931-119">ASN RFC1155 量測計 \_ \_</span><span class="sxs-lookup"><span data-stu-id="03931-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="03931-120">ASN \_ GAUGE32</span><span class="sxs-lookup"><span data-stu-id="03931-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="03931-121">ASN \_ RFC1155 \_ TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="03931-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="03931-122">ASN \_ TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="03931-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="03931-123">ASN \_ RFC1155 不 \_ 透明</span><span class="sxs-lookup"><span data-stu-id="03931-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="03931-124">ASN 不 \_ 透明</span><span class="sxs-lookup"><span data-stu-id="03931-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="03931-125">ASN \_ RFC1213 \_ DISPSTRING</span><span class="sxs-lookup"><span data-stu-id="03931-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="03931-126">ASN \_ OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="03931-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="03931-127">修改過的 SNMP PDU 要求類型</span><span class="sxs-lookup"><span data-stu-id="03931-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="03931-128">當您開發使用 Microsoft SNMP 管理 API 的管理員應用程式時，您應該使用下表所列的新 SNMP PDU 類型。</span><span class="sxs-lookup"><span data-stu-id="03931-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="03931-129">資料表會列出舊的 SNMP PDU 類型與相對應的新 PDU 類型。</span><span class="sxs-lookup"><span data-stu-id="03931-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="03931-130">舊的 PDU 類型</span><span class="sxs-lookup"><span data-stu-id="03931-130">Old PDU type</span></span>                 | <span data-ttu-id="03931-131">新的 PDU 類型</span><span class="sxs-lookup"><span data-stu-id="03931-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="03931-132">ASN \_ RFC1157 \_ GETREQUEST</span><span class="sxs-lookup"><span data-stu-id="03931-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="03931-133">SNMP \_ PDU \_ GET</span><span class="sxs-lookup"><span data-stu-id="03931-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="03931-134">ASN \_ RFC1157 \_ GETNEXTREQUEST</span><span class="sxs-lookup"><span data-stu-id="03931-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="03931-135">SNMP \_ PDU \_ GETNEXT</span><span class="sxs-lookup"><span data-stu-id="03931-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="03931-136">ASN \_ RFC1157 \_ GETRESPONSE</span><span class="sxs-lookup"><span data-stu-id="03931-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="03931-137">SNMP \_ PDU \_ 回應</span><span class="sxs-lookup"><span data-stu-id="03931-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="03931-138">ASN \_ RFC1157 \_ SETREQUEST</span><span class="sxs-lookup"><span data-stu-id="03931-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="03931-139">SNMP \_ PDU \_ 設定</span><span class="sxs-lookup"><span data-stu-id="03931-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="03931-140">ASN \_ RFC1157 \_ 陷阱</span><span class="sxs-lookup"><span data-stu-id="03931-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="03931-141">SNMP \_ PDU \_ V1TRAP</span><span class="sxs-lookup"><span data-stu-id="03931-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 
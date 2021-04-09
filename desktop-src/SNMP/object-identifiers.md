---
title: " (SNMP) 的物件識別碼"
description: SNMP 物件識別碼可唯一命名物件，並在管理資訊基底 (MIB) 樹狀結構中識別其位置。
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685365"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="e739f-103"> (SNMP) 的物件識別碼</span><span class="sxs-lookup"><span data-stu-id="e739f-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="e739f-104">SNMP 物件識別碼可唯一命名物件，並在管理資訊基底 (MIB) 樹狀結構中識別其位置。</span><span class="sxs-lookup"><span data-stu-id="e739f-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="e739f-105">物件識別碼是與應用程式無關的抽象語法標記法 (一)  (asn.1) 包含非負整數或 subidentifiers 序列的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e739f-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="e739f-106">物件識別碼至少必須有兩個 subidentifiers，而且不能超過 128 subidentifiers。</span><span class="sxs-lookup"><span data-stu-id="e739f-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="e739f-107">WinSNMP 程式設計環境會使用 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構來管理物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e739f-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="e739f-108">在 **smiOID** 結構中，物件識別碼陣列的格式為每個陣列元素一次 subidentifier。</span><span class="sxs-lookup"><span data-stu-id="e739f-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="e739f-109">物件識別碼以點分隔的數值字串表示會以句號分隔其 subidentifiers。例如，"1.2.3.4.5.6"。</span><span class="sxs-lookup"><span data-stu-id="e739f-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="e739f-110">如需詳細資訊，請參閱 [SNMP 管理資訊基礎 (MIB) ](the-snmp-management-information-base-mib-.md) 和相關的 rfc。</span><span class="sxs-lookup"><span data-stu-id="e739f-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 





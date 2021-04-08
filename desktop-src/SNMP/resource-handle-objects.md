---
title: 資源控制碼物件
description: 資源物件的結構受限於 Microsoft 的 WinSNMP 實行。 WinSNMP 應用程式可以存取具有控制碼的資源物件。
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674907"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="e5683-104">資源控制碼物件</span><span class="sxs-lookup"><span data-stu-id="e5683-104">Resource Handle Objects</span></span>

<span data-ttu-id="e5683-105">資源物件的結構受限於 Microsoft 的 WinSNMP 實行。</span><span class="sxs-lookup"><span data-stu-id="e5683-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="e5683-106">WinSNMP 應用程式可以存取具有控制碼的資源物件。</span><span class="sxs-lookup"><span data-stu-id="e5683-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="e5683-107">此實作為可為 WinSNMP 應用程式佈建下列其中一種資源控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="e5683-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="e5683-108">控制碼類型</span><span class="sxs-lookup"><span data-stu-id="e5683-108">Handle type</span></span>        | <span data-ttu-id="e5683-109">Description</span><span class="sxs-lookup"><span data-stu-id="e5683-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="e5683-110">**HSNMP \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="e5683-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="e5683-111">對 WinSNMP 會話的處理</span><span class="sxs-lookup"><span data-stu-id="e5683-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="e5683-112">**HSNMP \_ 實體**</span><span class="sxs-lookup"><span data-stu-id="e5683-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="e5683-113">SNMP 實體的控制碼</span><span class="sxs-lookup"><span data-stu-id="e5683-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="e5683-114">**HSNMP \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e5683-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="e5683-115">對 WinSNMP 內容的控制碼</span><span class="sxs-lookup"><span data-stu-id="e5683-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="e5683-116">**HSNMP \_ PDU**</span><span class="sxs-lookup"><span data-stu-id="e5683-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="e5683-117">通訊協定資料單位的控制碼</span><span class="sxs-lookup"><span data-stu-id="e5683-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="e5683-118">**HSNMP \_ VBL**</span><span class="sxs-lookup"><span data-stu-id="e5683-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="e5683-119">變數系結清單的控制碼</span><span class="sxs-lookup"><span data-stu-id="e5683-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="e5683-120">您可以使用 WinSNMP 應用程式要求執行建立或刪除資源控制碼，但此執行作業會執行此作業。</span><span class="sxs-lookup"><span data-stu-id="e5683-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="e5683-121">如需釋放個別資源的詳細資訊，請參閱 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)、 [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)、 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)、 [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)和 [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="e5683-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 





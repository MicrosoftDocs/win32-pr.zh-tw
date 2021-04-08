---
title: 路由通訊協定介面參考
description: 本檔說明用來將路由通訊協定實作為使用者模式 DLL 的函式和結構。
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- 路由及遠端存取服務 RRAS，路由通訊協定介面，參考
- 路由通訊協定介面 RRAS，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839980"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="7771b-105">路由通訊協定介面參考</span><span class="sxs-lookup"><span data-stu-id="7771b-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="7771b-106">本檔說明用來將路由通訊協定實作為使用者模式 DLL 的函式和結構。</span><span class="sxs-lookup"><span data-stu-id="7771b-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="7771b-107">MPR50 應該在路由通訊協定的 make 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="7771b-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="7771b-108">**SIZEOF ip 系結 \_ \_ (x)** 宏會計算 ip 配接器系結 [**\_ \_ \_ 資訊**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info)結構的大小（以位元組為單位），其中包含 ip 位址的數目。</span><span class="sxs-lookup"><span data-stu-id="7771b-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="7771b-109">下列主題將描述這些參考元素：</span><span class="sxs-lookup"><span data-stu-id="7771b-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="7771b-110">路由通訊協定介面函式</span><span class="sxs-lookup"><span data-stu-id="7771b-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="7771b-111">路由通訊協定介面結構</span><span class="sxs-lookup"><span data-stu-id="7771b-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="7771b-112">IPX 服務資料表管理</span><span class="sxs-lookup"><span data-stu-id="7771b-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 





---
title: 複製 PDU
description: SnmpDuplicatePdu 函式會複製 PDU，並配置任何必要的記憶體。 若要釋放 SnmpDuplicatePdu 為新的 PDU 所配置的資源，則必須呼叫 SnmpFreePdu 函式。
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd860d84ac102f2c2cdd1132476b3279e640f9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674024"
---
# <a name="duplicating-a-pdu"></a><span data-ttu-id="68e33-104">複製 PDU</span><span class="sxs-lookup"><span data-stu-id="68e33-104">Duplicating a PDU</span></span>

<span data-ttu-id="68e33-105">[**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)函式會複製 PDU，並配置任何必要的記憶體。</span><span class="sxs-lookup"><span data-stu-id="68e33-105">The [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) function duplicates a PDU, allocating any necessary memory.</span></span> <span data-ttu-id="68e33-106">若要釋放 **SnmpDuplicatePdu** 為新的 PDU 所配置的資源，則必須呼叫 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) 函式。</span><span class="sxs-lookup"><span data-stu-id="68e33-106">To release resources allocated by **SnmpDuplicatePdu** for a new PDU, a WinSNMP application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function.</span></span>

 

 





---
title: 更新 PDU
description: 藉由使用 SnmpGetPduData 和 SnmpSetPduData 函式，WinSNMP 應用程式可以取出和更新選取的 PDU 欄位。
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675091"
---
# <a name="updating-a-pdu"></a><span data-ttu-id="f9dd6-103">更新 PDU</span><span class="sxs-lookup"><span data-stu-id="f9dd6-103">Updating a PDU</span></span>

<span data-ttu-id="f9dd6-104">藉由使用 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 和 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函式，WinSNMP 應用程式可以取出和更新選取的 PDU 欄位。</span><span class="sxs-lookup"><span data-stu-id="f9dd6-104">A WinSNMP application can retrieve and update selected PDU fields by using the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) and the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) functions.</span></span>

<span data-ttu-id="f9dd6-105">應用程式可以從特定的 PDU 取出 PDU 類型、要求識別碼、錯誤狀態和錯誤索引欄位。</span><span class="sxs-lookup"><span data-stu-id="f9dd6-105">The application can retrieve the PDU type, request identifier, error status, and error index fields from a specific PDU.</span></span> <span data-ttu-id="f9dd6-106">它也可以取出變數系結清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f9dd6-106">It can also retrieve the handle to the variable binding list.</span></span> <span data-ttu-id="f9dd6-107">應用程式可以更新 [ **PDU \_ 類型** ] 和 [ **要求 \_ 識別碼** ] 欄位。</span><span class="sxs-lookup"><span data-stu-id="f9dd6-107">The application can update the **PDU\_type** and **request\_id** fields.</span></span>

<span data-ttu-id="f9dd6-108">如果 PDU 類型等於 SNMP \_ PDU \_ GETBULK，則應用程式也可以更新 PDU 的 **非 \_ 中繼器** 和 **max \_ 重複** 欄位。</span><span class="sxs-lookup"><span data-stu-id="f9dd6-108">If the PDU type is equal to SNMP\_PDU\_GETBULK, the application can also update the **non\_repeaters** and the **max\_repetitions** fields of the PDU.</span></span>

 

 





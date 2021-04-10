---
title: 管理變數系結清單
description: SnmpGetVb 函式會從變數系結清單中捕獲變數系結資訊。 函數會從 WinSNMP 應用程式所指定的變數系結專案中，抓取變數名稱和變數的相關聯值。
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021201"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="9677f-104">管理變數系結清單</span><span class="sxs-lookup"><span data-stu-id="9677f-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="9677f-105">[**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)函式會從變數系結清單中捕獲變數系結資訊。</span><span class="sxs-lookup"><span data-stu-id="9677f-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="9677f-106">函數會從 WinSNMP 應用程式所指定的變數系結專案中，抓取變數名稱和變數的相關聯值。</span><span class="sxs-lookup"><span data-stu-id="9677f-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="9677f-107">若要更新變數系結清單中的變數繫結項目，請呼叫 [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) 函數。</span><span class="sxs-lookup"><span data-stu-id="9677f-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="9677f-108">**SnmpSetVb** 函式也會將新的變數繫結項目附加至現有的變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="9677f-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="9677f-109">WinSNMP 應用程式必須呼叫 [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) 函式，才能從變數系結清單中移除專案。</span><span class="sxs-lookup"><span data-stu-id="9677f-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="9677f-110">若要抓取、修改或刪除變數系結專案，WinSNMP 應用程式必須在變數系結清單中指定專案的位置。</span><span class="sxs-lookup"><span data-stu-id="9677f-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="9677f-111">[**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)函式的呼叫會將變數系結清單與 PDU 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9677f-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="9677f-112">[**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)函式的呼叫會從 PDU 取出變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="9677f-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="9677f-113">個別的變數系結不會直接與 PDU 相關聯，但會透過其包含在變數系結清單中間接關聯。</span><span class="sxs-lookup"><span data-stu-id="9677f-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 





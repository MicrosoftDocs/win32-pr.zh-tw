---
title: 管理重新傳輸原則
description: WinSNMP 應用程式可以要求 Microsoft WinSNMP 實行執行應用程式的重新傳輸原則。 當執行管理重新傳輸時，它會使用其資料庫中的超時時間和重試計數值。
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021778"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="10d59-104">管理重新傳輸原則</span><span class="sxs-lookup"><span data-stu-id="10d59-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="10d59-105">WinSNMP 應用程式可以要求 Microsoft WinSNMP 實行執行應用程式的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="10d59-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="10d59-106">當執行管理重新傳輸時，它會使用其資料庫中的超時時間和重試計數值。</span><span class="sxs-lookup"><span data-stu-id="10d59-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="10d59-107">實值會在初始化期間，從 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式的傳回值中識別預設的重新傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="10d59-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="10d59-108">模式可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="10d59-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="10d59-109">值</span><span class="sxs-lookup"><span data-stu-id="10d59-109">Value</span></span>        | <span data-ttu-id="10d59-110">意義</span><span class="sxs-lookup"><span data-stu-id="10d59-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="10d59-111">SNMPAPI \_ 于</span><span class="sxs-lookup"><span data-stu-id="10d59-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="10d59-112">此實作為執行應用程式的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="10d59-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="10d59-113">SNMPAPI \_ 關閉</span><span class="sxs-lookup"><span data-stu-id="10d59-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="10d59-114">執行不會執行應用程式的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="10d59-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="10d59-115">藉由呼叫 [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) 函式，可讓您隨時取得目前的重新傳輸模式，以取得目前的重新傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="10d59-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="10d59-116">WinSNMP API 提供其他 [資料庫功能](winsnmp-functions.md) ，可簡化重新傳輸原則的管理。</span><span class="sxs-lookup"><span data-stu-id="10d59-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="10d59-117">在程式執行期間，透過執行下列其中一個步驟，WinSNMP 應用程式可以調整原則的執行：</span><span class="sxs-lookup"><span data-stu-id="10d59-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="10d59-118">藉由呼叫 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式，要求執行啟動或停止執行重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="10d59-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="10d59-119">如需詳細資訊，請參閱 [開啟和關閉重新傳輸](turning-retransmission-on-and-off.md)。</span><span class="sxs-lookup"><span data-stu-id="10d59-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="10d59-120">修改執行的資料庫中的超時時間和重試計數值。</span><span class="sxs-lookup"><span data-stu-id="10d59-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="10d59-121">如需詳細資訊，請參閱 [變更重新傳輸原則](changing-the-retransmission-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="10d59-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="10d59-122">呼叫 [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) 函式來取消重新傳輸週期，並釋放與單一 SNMP 訊息要求相關聯的內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="10d59-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="10d59-123">如需詳細資訊，請參閱 [取消重新傳輸](canceling-retransmission.md)。</span><span class="sxs-lookup"><span data-stu-id="10d59-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="10d59-124">應用程式可以執行它自己的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="10d59-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="10d59-125">在此情況下，執行可能會或可能不會以資料庫中的值為基礎。</span><span class="sxs-lookup"><span data-stu-id="10d59-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




